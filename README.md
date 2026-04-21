# Ghost Labs Project Architect

## Introduction

Ghost Labs Project Architect is a sophisticated, single-file web application that serves as a structural tool for organizing and managing web development projects. It provides a comprehensive file management system with real-time editing capabilities, live preview functionality, and advanced features typically found in complex IDEs, all contained within a single HTML file.

## Key Features

### Project Structure Management
- Visual hierarchical file explorer
- Drag-and-drop file and folder reorganization
- Real-time tree visualization
- Folder and file creation/deletion

### Advanced Text Editing
- Full-featured code editor with syntax considerations
- Line numbering with synchronized gutter display
- Auto-indentation and smart bracket/quote pairing
- Tab/Shift+Tab for multi-line indentation
- Word wrap toggle
- Auto-save with debouncing

### Live Preview & Debugging
- Real-time HTML preview with iframe isolation
- Integrated console logging with message interception
- Error tracking and reporting
- Secure cross-origin communication

### Import/Export Capabilities
- Structure import via indented text format
- ZIP export functionality
- Undo/redo operations for structural changes

### User Experience
- Neo-brutalist aesthetic with custom CSS properties
- Responsive design with mobile-friendly touch targets
- Keyboard shortcuts (Cmd/Ctrl+Z for undo, Cmd/Ctrl+S for save)
- Toast notifications for user feedback
- Modal dialogs for import/export operations

## Technical Architecture

### Modular Design
The application follows a modular architecture with clearly defined responsibilities:

- **StateManager**: Central data model and content persistence
- **FileSystemUtils**: Path helpers and sanitization
- **ImportParser**: Indented text to nested object conversion
- **Boilerplates**: Code template library
- **DragDropManager**: Drag-and-drop reordering
- **TreeRenderer**: DOM tree rendering from state
- **EditorController**: Ghost Editor for opening, editing, and auto-saving
- **PreviewController**: Blob iframe materialization
- **ConsoleService**: Iframe console interception
- **Toast**: Notification utility
- **UIController**: Event wiring and lifecycle bootstrap

### Technology Stack
- **HTML5**: Semantic markup and structure
- **CSS3**: Custom properties, modern layouts, and animations
- **JavaScript (ES2023+)**: Advanced vanilla JavaScript with IIFE modules
- **Tailwind CSS**: Utility-first CSS framework (loaded via CDN)
- **JSZip**: ZIP file generation for exports

### Design Patterns
- **Module Pattern**: Self-contained modules with private/public interfaces
- **Singleton Pattern**: State management and service instances
- **Event-Driven Architecture**: UI interactions and state changes
- **Separation of Concerns**: Clear boundaries between data, UI, and logic layers

## How It Works

The application maintains an in-memory representation of the project structure as a nested JavaScript object. All file operations are managed through the StateManager module, which provides a clean API for structural mutations while maintaining history for undo operations.

The UI is rendered dynamically from the state, with the file tree updated in real-time as changes occur. The editor provides a distraction-free coding environment with features like bracket matching, smart indentation, and line numbers.

Preview functionality works by generating blob URLs from HTML content, with automatic resolution of relative script and style references to inline content for proper rendering.

## Potential Improvements

### Performance Enhancements
- Implement virtual scrolling for large file trees
- Optimize DOM updates for better performance with large projects
- Add lazy loading for deeply nested structures

### Feature Extensions
- Syntax highlighting for different file types
- Multiple file editing tabs
- Search and replace functionality
- Git integration for version control
- Plugin system for extending functionality
- Collaboration features for team development

### User Experience Improvements
- Dark/light theme toggle
- More comprehensive keyboard navigation
- Enhanced accessibility features
- Better mobile optimization
- Improved error handling and validation

### Technical Improvements
- TypeScript migration for better type safety
- Unit tests for core modules
- Better separation of concerns with more granular modules
- Configuration system for customizing the editor
- Integration with external tools and services

## Skills Demonstrated

This project showcases expertise in:
- Advanced vanilla JavaScript development
- Modern CSS techniques and custom properties
- Complex UI component implementation
- Browser API utilization
- Performance optimization strategies
- Modular code architecture
- Cross-origin security considerations
- User experience design principles

## Usage

The application runs entirely in the browser with no server requirements. Simply open the HTML file in a modern browser to begin organizing and developing your web projects.