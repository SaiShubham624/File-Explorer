# Problem Solving

Manual file-system management can be inconvenient, error-prone, and difficult to organize when users need to inspect, create, rename, or delete files and folders. Navigating directories through basic operating-system commands can also make it harder to understand the structure of a file system and quickly access useful information about stored objects. Users need a simple, interactive, and lightweight tool that centralizes common file and folder operations in one terminal application.

# Scope of the project

This project is a Python-based Command Line Interface (CLI) File Explorer designed to simplify common file-system management tasks. The application opens in the user's home directory and provides a menu-driven interface for traversing directories, creating files and folders, removing objects, renaming files or folders, deleting the current folder, and viewing metadata. It uses multiple Python modules and object-oriented classes to represent files and folders, while built-in modules such as `os` and `datetime` handle file-system operations and timestamps.

The scope includes recursive directory traversal, navigation to parent folders, creation of empty files and folders, removal of files and folders, renaming of directory objects, deletion of the current folder, and inspection of creation, modification, last-access, and size information. File sizes are converted into human-readable units such as bytes, kilobytes, megabytes, and gigabytes. The project is designed to run locally in a terminal using Python without external packages or an external database. It currently relies on the host operating system's file system and uses Windows-style path handling, so it is not a graphical file manager and does not provide cloud synchronization, recycle-bin recovery, or advanced permissions management.

# Target users

Students and Python Learners: Who want to understand recursion, modules, classes, operating-system file operations, and command-line interaction through a practical project.

Everyday Computer Users: Who need a lightweight terminal utility for carrying out basic file and folder operations without opening a graphical file manager.

Developers and System Administrators: Who want a simple local tool for inspecting directory contents, checking metadata, and experimenting with file-system automation.

# High-level features

Interactive Main Menu: Presents a numbered menu for accessing the application's file-system operations, including traversal, creation, deletion, renaming, information lookup, and quitting.

Recursive Filesystem Traversal: Lets users move through folders, open files, return to a parent directory, or stop traversal at the selected path. The recursive `traverse()` function demonstrates directory navigation using the `os.walk()` function.

File and Folder Creation: Allows users to create a new empty file or directory in the current folder and reports when an object with the requested name already exists.

Object Removal: Displays the contents of the current directory and allows the user to remove a selected file or folder using the appropriate operating-system operation.

Renaming Operations: Supports renaming a file or folder inside the current directory as well as renaming the current folder itself.

Metadata Inspection: Provides information about selected files, folders, and the current folder, including creation time, modification time, last-access time, and size where supported by the operating system.

Human-Readable Size Conversion: Converts raw file-size values from bytes into more understandable units such as B, KB, MB, GB, and TB.

Modular Object-Oriented Design: Separates functionality across `main.py`, `folder.py`, `file.py`, `directory_traverser.py`, and `extra_functions.py`, with `File` and `Folder` classes encapsulating object-specific operations.

Continuous Operation Loop: Keeps the explorer running after each operation so users can perform multiple file-system tasks without restarting the application. The program can be closed by selecting the Quit option from the main menu.
