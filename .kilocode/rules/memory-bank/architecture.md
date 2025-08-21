# System Architecture

## Project Structure

```
Extension-Objective/
├── index.js              # Main extension logic and initialization
├── manifest.json         # Extension metadata and configuration
├── settings.html          # UI template for extension settings panel
├── style.css             # Extension-specific styling
├── README.md             # Basic project documentation
├── LICENSE               # GNU AGPL v3 license
└── Objective _ docs.ST.app.html  # Offline documentation copy
```

## Core Architecture

### Extension Framework Integration
- **SillyTavern Extension System**: Follows standard SillyTavern extension patterns
- **Module Registration**: Proper integration with extension loading system
- **Event System**: Hooks into SillyTavern's event-driven architecture
- **Settings Integration**: Seamless integration with SillyTavern's settings system

### Data Architecture

#### Task Tree Structure
```javascript
ObjectiveTask {
  id: number              // Unique identifier
  description: string     // Human-readable task description
  completed: boolean      // Completion status
  parentId: string        // Parent task reference (empty for root)
  children: Array         // Child tasks array
}
```

#### State Management
- **Global State**: Extension settings stored in `extension_settings.objective`
- **Chat State**: Per-chat task trees stored in `chat_metadata.objective`
- **Session State**: Runtime variables for current task tracking
- **UI State**: Dynamic DOM management for task visualization

### Component Architecture

#### Task Management (`ObjectiveTask` Class)
- **Core Operations**: Create, update, delete, complete tasks
- **Hierarchy Management**: Parent-child relationships and tree traversal
- **UI Integration**: DOM element creation and event handling
- **State Persistence**: Serialization for save/load operations

#### Prompt System
- **Template Engine**: Variable substitution system (`{{objective}}`, `{{task}}`, etc.)
- **Custom Prompts**: User-configurable prompt templates
- **Context Injection**: Integration with SillyTavern's prompt system
- **AI Integration**: Quiet prompt generation for task operations

#### UI System
- **Settings Panel**: Main configuration and task management interface
- **Popup System**: Modal dialogs for prompt editing and task operations
- **Draggable Interface**: Popout window functionality
- **Event Handling**: Comprehensive user interaction management

## Key Design Patterns

### Observer Pattern
- Event listeners for chat state changes
- Task completion monitoring
- UI update propagation

### Command Pattern
- Slash command integration (`/taskcheck`)
- Manual task operations (check, complete, generate)
- Undo/redo capability through state management

### Strategy Pattern
- Pluggable prompt templates
- Configurable task checking strategies
- Multiple UI presentation modes

## Integration Points

### SillyTavern Core
- **Extension Prompt System**: Injects current task into chat context
- **Event System**: Responds to message events and chat changes
- **Settings Framework**: Persists configuration and custom prompts
- **UI Framework**: Integrates with extension panels and popups

### AI API Integration
- **Quiet Generation**: Background AI calls for task operations
- **Context Management**: Proper handling of AI context and parameters
- **Error Handling**: Graceful fallback for API failures

## Critical Implementation Details

### Task Selection Algorithm
- Depth-first traversal for hierarchical task trees
- Automatic current task advancement
- Parent completion logic when all children complete

### State Synchronization
- Real-time UI updates on task changes
- Automatic save on state modifications
- Migration handling for legacy data formats

### Performance Considerations
- Configurable check frequency to manage API usage
- Debounced save operations
- Efficient DOM manipulation for large task lists
