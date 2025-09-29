# Bokuchi Editor Usage Guide

This guide introduces convenient ways to use the Bokuchi editor.

## Tab Feature Usage

### Multi-file Editing
- **New File**: `Ctrl+N` (Windows/Linux) or `Cmd+N` (Mac)
- **Open File**: `Ctrl+O` (Windows/Linux) or `Cmd+O` (Mac)
- **Tab Switching**: `Ctrl+Tab` for next tab, `Ctrl+Shift+Tab` for previous tab

### Practical Examples
1. Edit main document
2. Open reference materials in separate tab
3. Manage template files in separate tab
4. Copy & paste between multiple tabs

## Zoom Feature

### Zoom Adjustment
- **Zoom In**: `Ctrl++` (Windows/Linux) or `Cmd++` (Mac)
- **Zoom Out**: `Ctrl+-` (Windows/Linux) or `Cmd+-` (Mac)
- **Reset**: `Ctrl+0` (Windows/Linux) or `Cmd+0` (Mac)

### Use Cases
- **Presentations**: Large text for better visibility
- **Detailed Editing**: Small text to see the big picture
- **Dual Monitor**: Adjust to fit one monitor

## Theme Feature

### Theme Switching
- **Dark Mode**: Easy on the eyes, suitable for long work sessions
- **Light Mode**: Suitable for printing or working in bright environments

### Customization
- Fine customization possible with CSS variables
- Custom CSS for preview can also be configured

## State Persistence

### Auto-save Feature
- State is restored when the application is restarted
- Open tabs, active tab, and unsaved content are preserved
- File paths are also remembered, so externally modified files are automatically reloaded

### Usage Tips
- When interrupting work, simply close the application
- Next startup will restore the previous work state
- Especially convenient when working on multiple projects in parallel

## Variable Feature Applications

### Template Creation
```markdown
<!-- @var projectName: My Project -->
<!-- @var version: 1.0.0 -->
<!-- @var author: Your Name -->

# {{projectName}} Documentation

Version: {{version}}
Author: {{author}}

## Overview
This document describes the {{projectName}} project.
```

### Global Variable Usage
- Set common information like company name, department name, author name as global variables
- Manage consistent information across multiple documents

## Checkbox Feature Usage

### Task Management
```markdown
## Today's Tasks
- [ ] Prepare meeting materials
- [ ] Conduct code review
- [ ] Update documentation
- [x] Check morning emails
```

### Project Management
- Visualize progress status
- Confirm completed tasks
- Share progress within team

## File Operation Best Practices

### File Naming Conventions
- Include dates: `2025-01-15-meeting-notes.md`
- Include project names: `project-alpha-spec.md`
- Version control: `api-docs-v2.md`

### Folder Structure
```
docs/
├── meetings/
│   ├── 2025-01-15-weekly.md
│   └── 2025-01-22-weekly.md
├── specs/
│   ├── api-spec.md
│   └── ui-spec.md
└── templates/
    ├── meeting-template.md
    └── project-template.md
```

## Summary

Bokuchi Editor goes beyond being just a markdown editor, providing an efficient document creation environment.
It excels particularly in the following areas:

- **Multi-tasking Support**: Simultaneous editing of multiple files
- **Usability**: Intuitive operation and state persistence
- **Customizability**: Flexible settings with themes and variables
- **Practicality**: Practical features like checkboxes and zoom

By combining these features, more efficient and comfortable document creation becomes possible.
