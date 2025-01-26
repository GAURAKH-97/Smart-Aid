# Jarvis Assistant GUI Application

This Python script implements a graphical user interface (GUI) application using PyQt5 for a virtual assistant named Jarvis.

## Project Structure

- **Libraries Used**: PyQt5, dotenv, sys, os
- **Key Components**:
  - **Helper Functions**: Modify queries, manage status, and handle file paths.
  - **ChatSection Widget**: Display conversation history and messages.
  - **InitialScreen Widget**: Display initial screen with GIF and microphone icon.
  - **MessageScreen Widget**: Main chat interface with `ChatSection`.
  - **CustomTopBar Widget**: Navigation and window management.
  - **MainWindow**: Main application window with stacked widget.
  - **GraphicalUserInterface Function**: Entry point to run the application.

## Components Overview

### Helper Functions

- `AnswerModifier()`: Cleans up answer text.
- `QueryModifier()`: Formats user queries.
- `MicButtonInitialed()`, `MicButtonClosed()`: Manages microphone status.
- `GraphicsDirectoryPath()`, `TempDirectoryPath()`: Generate file paths.
- `ShowTextToScreen()`: Updates text display.

### Widgets

- **ChatSection Widget**
  - Displays chat history and messages.
  - Uses QTextEdit for text display and QMovie for GIFs.
  
- **InitialScreen Widget**
  - Shows an initial screen with a centered GIF (`Jarvis.gif`) and microphone icon (`Mic_on.png`).
  
- **MessageScreen Widget**
  - Main chat interface containing the `ChatSection`.

- **CustomTopBar Widget**
  - Provides navigation and window controls.
  - Includes buttons for home, chat, minimize, maximize/restore, and close.
  - Manages screen switching (`InitialScreen` and `MessageScreen`).

### Main Window

- **MainWindow**
  - Inherits `QMainWindow`.
  - Hosts a stacked widget (`QStackedWidget`) for different screens (`InitialScreen` and `MessageScreen`).
  - Uses `CustomTopBar` for menu and window controls.

## Running the Application

To run the application:
```bash
python your_script_name.py
