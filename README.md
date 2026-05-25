# Files 2 Folder (Windows 11)

A modern, lightweight Windows 11 context menu extension to quickly organize files by packing them into subfolders. Built from scratch with C# and .NET 8.

## Features
* **Single File**: Right-click a file and select "Files 2 Folder" to move it into a new folder named after the file.
* **Multiple Files**: Select multiple files/folders, right-click, enter a folder name, and they are all moved into the new folder together.
* **Directory Nesting**: Right-click a folder to wrap it in a parent folder (appends a `~` to prevent name conflicts).
* **No Admin Needed**: Registers context menus under `HKEY_CURRENT_USER` (HKCU). Standard users can install/uninstall without Administrator rights.
* **Win11 Native Menu**: Includes a toggle in the settings GUI to enable the classic context menu style, putting the command directly in the main right-click menu.

## How it Works
When you select multiple files, Windows Explorer spawns a separate process for each file. This utility uses a system **Mutex** and **Named Pipe** to instantly gather all paths into a single master process, ensuring only a single popup dialog is shown.

## Installation
1. Download `Files2Folder.exe`.
2. Run it and click **Register**.
3. *(Optional)* Click **Toggle Win11 Menu** and **Restart Windows Explorer** to put the command directly in the main right-click menu.

## Uninstallation
Run `Files2Folder.exe` and click **Unregister**, or run silently via command line:
```cmd
Files2Folder.exe -su
```

## Requirements
* Windows 10 or 11
* .NET 8.0 Desktop Runtime

## License
MIT License. See [LICENSE](LICENSE) for details.
