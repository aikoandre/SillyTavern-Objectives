# Technology Stack

## Core Technologies

### JavaScript (ES6+)
- **Main Language**: Vanilla JavaScript with modern ES6+ features
- **Module System**: ES6 imports/exports for clean dependency management
- **Async/Await**: Promise-based asynchronous operations
- **Classes**: Object-oriented design with ES6 class syntax

### Frontend Technologies

#### HTML5
- **Semantic Markup**: Well-structured HTML for accessibility
- **Template System**: HTML templates for dynamic UI generation
- **Form Controls**: Comprehensive form elements for settings

#### CSS3
- **Flexbox Layout**: Modern layout system for responsive design
- **CSS Variables**: Custom properties for theming
- **Transitions**: Smooth UI animations and state changes
- **Component Styling**: Modular CSS for extension components

#### jQuery
- **DOM Manipulation**: Efficient DOM operations and event handling
- **AJAX Operations**: HTTP requests for AI integration
- **UI Interactions**: Rich user interface behaviors
- **Event System**: Robust event binding and delegation

## SillyTavern Framework

### Extension API
- **Extension Registration**: Standard SillyTavern extension lifecycle
- **Settings Integration**: Built-in configuration persistence
- **Event System**: Hook into chat and message events
- **Prompt Injection**: Extension prompt system integration

### UI Framework
- **Extension Panels**: Standardized panel system
- **Popup System**: Modal dialogs and confirmation prompts
- **Draggable Elements**: Moveable UI components
- **Responsive Design**: Adaptive layouts for different screen sizes

### Core Utilities
- **Template Rendering**: Extension template system
- **Parameter Substitution**: Variable replacement engine
- **Quiet Generation**: Background AI prompt processing
- **State Management**: Chat metadata and settings persistence

## Development Environment

### Package Management
- **No Build System**: Direct browser-compatible JavaScript
- **No Dependencies**: Self-contained extension code
- **Version Control**: Git-based development workflow

### File Structure
- **Manifest-based**: JSON configuration for extension metadata
- **Modular Code**: Logical separation of concerns
- **Asset Organization**: Clean separation of code, styles, and templates

## Browser Compatibility
- **Modern Browsers**: ES6+ support required
- **Cross-Platform**: Works on desktop and mobile browsers
- **WebView Support**: Compatible with Electron-based applications

## Integration Requirements

### SillyTavern Version
- **Latest Version**: Requires up-to-date SillyTavern installation
- **Extension System**: Compatible with SillyTavern extension framework
- **API Access**: Requires configured LLM API connection

### Runtime Dependencies
- **No External Libraries**: Self-contained implementation
- **SillyTavern Core**: Depends on host application's jQuery and utilities
- **Browser APIs**: Standard web APIs for storage and DOM manipulation

## Performance Characteristics

### Resource Usage
- **Lightweight**: Minimal memory footprint
- **Efficient DOM**: Optimized DOM manipulation
- **API Conscious**: Configurable to minimize AI API calls

### Scalability
- **Task Trees**: Handles complex hierarchical structures
- **Large Objectives**: Supports extensive task lists
- **Session Management**: Efficient state persistence

## Technical Constraints

### API Limitations
- **Rate Limiting**: Respects AI service rate limits
- **Context Windows**: Works within LLM token constraints
- **Error Handling**: Graceful degradation on API failures

### Browser Security
- **Content Security Policy**: Adheres to extension security models
- **Local Storage**: Uses browser-safe storage mechanisms
- **Cross-Origin**: Handles CORS appropriately for AI requests
