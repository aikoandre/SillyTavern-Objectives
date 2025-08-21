# Extension-Objective (Forked)

> **This is a forked version of the original SillyTavern Extension-Objective**  
> Original repository: [SillyTavern/Extension-Objective](https://github.com/SillyTavern/Extension-Objective)

Set an Objective for the AI to aim for during the chat with enhanced control features.

## Original Documentation
<https://docs.sillytavern.app/extensions/objective>

## Fork Changes

### Enhanced Control Features

#### **Enable/Disable Toggle**
- **Added**: On/Off toggle button in the extension header
- **Location**: Next to the "Objective" title in the settings panel
- **Functionality**: 
  - **When Enabled** (default): Extension works normally - tasks are injected into chat prompts and AI pursues objectives
  - **When Disabled**: Task prompts are not injected into chat context, effectively pausing objective pursuit while preserving all task data
- **Benefits**:
  - Quick temporary disable without losing work
  - Reduced API calls when objectives aren't needed
  - Full control over when AI should focus on objectives vs. free conversation
  - Settings persist per chat session

#### **Implementation Details**
- Toggle state is saved per chat session
- UI remains fully functional when disabled (tasks can still be edited/managed)
- Console logging indicates when extension is disabled
- Seamless integration with existing functionality

## Installation

Install this forked version by placing the files in your SillyTavern extensions directory, or use the original version from the official SillyTavern extensions repository.

## Usage

Use exactly as documented in the original extension, with the added benefit of being able to toggle the extension on/off using the "Enabled" checkbox in the header.
