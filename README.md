# C++ IDE - Visual Studio Code-like Editor

A full-featured C++ IDE built with Qt6, designed to closely resemble Visual Studio Code.

## Features

- **Code Editor**: Multi-tab editor with syntax highlighting for C++
- **File Explorer**: Project file browser with directory tree
- **Syntax Highlighting**: C++ syntax with semantic analysis
- **Auto-completion**: Context-aware code completion for C++
- **Integrated Terminal**: Built-in terminal for compilation and execution
- **Git Integration**: Git status, diff viewer, and basic git operations
- **Debugger**: GDB integration for step-by-step debugging
- **Search & Replace**: Find and replace across files
- **VS Code Theme**: Dark theme matching VS Code's Dracula-like appearance
- **Minimap**: Code overview minimap on the right side
- **Status Bar**: Information about file, line numbers, encoding

## Building

### Requirements
- Qt6 (Core, Gui, Widgets)
- CMake 3.20+
- C++17 compiler
- Git (for git integration)
- GDB (for debugging)

### Build Instructions

```bash
mkdir build
cd build
cmake ..
make
./CppIDE
```

## Project Structure

```
src/
├── main.cpp              # Entry point
├── mainwindow.h/cpp      # Main application window
├── editor/
│   ├── codeeditor.h/cpp  # Code editor widget
│   └── syntaxhighlighter.h/cpp  # C++ syntax highlighting
├── ui/
│   ├── sidebar.h/cpp     # Left sidebar with action buttons
│   ├── explorer.h/cpp    # File explorer panel
│   ├── terminal.h/cpp    # Integrated terminal
│   └── bottombar.h/cpp   # Bottom status/git panel
├── git/
│   └── gitmanager.h/cpp  # Git operations wrapper
├── autocomplete/
│   ├── autocompleter.h/cpp  # Code completion engine
│   └── parser.h/cpp      # C++ parser for completion
└── resources/
    └── resources.qrc     # Icons and resources
```

## Keyboard Shortcuts

- `Ctrl+N` - New file
- `Ctrl+O` - Open file
- `Ctrl+S` - Save file
- `Ctrl+Shift+S` - Save all
- `Ctrl+Q` - Quit
- `Ctrl+F` - Find
- `Ctrl+H` - Find and Replace
- `Ctrl+Alt+T` - Toggle terminal
- `Ctrl+\`` - Toggle sidebar
- `Ctrl+B` - Toggle file explorer
- `F5` - Run
- `F9` - Build
- `F10` - Debug

## License

MIT License
