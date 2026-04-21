# Changelog for Ghost Labs Project Architect

## [Unreleased] - 2026-03-02

### Added
- Initial release of Ghost Labs Project Architect
- Complete file management system with visual hierarchical file explorer
- Drag-and-drop file and folder reorganization with real-time tree visualization
- Full-featured code editor with line numbering, auto-indentation, and smart bracket/quote pairing
- Live preview functionality with integrated console logging and error tracking
- Import/export capabilities with structure import via indented text format and ZIP export
- Undo/redo operations for structural changes
- Responsive design with mobile-friendly touch targets
- Keyboard shortcuts (Cmd/Ctrl+Z for undo, Cmd/Ctrl+S for save)
- Toast notifications for user feedback
- Modal dialogs for import/export operations
- Neo-brutalist aesthetic with custom CSS properties
- Comprehensive documentation in README.md and skills.md

### Upgraded - Preview Resolution for Nested Paths
#### How it was implemented:
- Modified the PreviewController module to properly resolve nested paths when processing relative script and style references
- Updated the regex patterns in the render function to correctly handle paths at any nesting level
- Enhanced the path resolution logic to work with deeply nested folder structures
- Improved security by using window.location.origin for postMessage communication

#### Effect:
- HTML files in nested folders can now properly reference scripts and styles using relative paths
- Preview functionality works correctly regardless of how deeply nested the HTML file is in the project structure
- Security improvements prevent potential cross-origin issues with iframe communication

### Upgraded - Collapsible Folders in File Tree
#### How it was implemented:
- Enhanced the TreeRenderer module to support collapsible folder functionality
- Added click handlers to folder icons to toggle visibility of child nodes
- Implemented state management to track expanded/collapsed folders
- Added visual indicators for expandable/collapsible folders
- Maintained accessibility with proper ARIA attributes and keyboard navigation

#### Effect:
- Users can now collapse and expand folders in the file tree for better navigation
- Large project structures are easier to manage with collapsible sections
- Improved performance when dealing with deeply nested structures
- Better user experience with ability to focus on specific sections of the project

### Upgraded - Mobile-Friendly Drag/Drop Functionality
#### How it was implemented:
- Enhanced the drag-and-drop system to work properly on touch devices
- Added touch event handlers to complement mouse-based drag/drop
- Improved the visual feedback during drag operations for mobile devices
- Made touch targets larger and more accessible
- Added appropriate CSS transitions for smooth mobile interactions

#### Effect:
- Drag-and-drop functionality now works reliably on mobile devices
- Better user experience across all device types
- Improved accessibility for users with motor impairments
- Consistent behavior across desktop and mobile platforms

### Fixed
- Security vulnerability in iframe console interception by validating origin
- Memory leak in preview controller by properly revoking blob URLs
- Path resolution issue for nested files in preview functionality
- Accessibility improvements in file tree navigation
- Input validation improvements in file/folder creation forms
- Performance optimizations in tree rendering
- Keyboard navigation enhancements throughout the application