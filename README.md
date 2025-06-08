
# Dennis DevDrive (DennisPD)

Dennis DevDrive is a portable development environment script that can be run directly from a USB drive. It helps set up a development environment with tools like Python, Node.js, .NET SDK, Java, Git, and Visual Studio Code without needing to install them on the host system. This script ensures that the development environment is consistent and isolated by leveraging the USB drive's portable resources.

---

## Features

- **Portable Development Setup**: Run Python, .NET SDK, Java, Node.js, Git, and other tools directly from the USB drive.
- **Python Environment Management**: Switch between multiple Python environments stored on the USB drive.
- **Custom Terminal Prompt**: Modify the terminal prompt to indicate you are using the portable development environment.
- **Environment Configuration**: Automatically adds relevant directories to the `PATH` environment variable for easy access to development tools.
- **No Host Installation Required**: The tools are self-contained on the USB drive, ensuring no installation on the host system.

---

## Requirements

- A USB drive with at least 8GB of free space.
- PowerShell 7.0 or higher.
- A compatible version of Windows for the terminal setup (for setting environment variables and paths).
  
---

## Setup Instructions

1. **Clone this Repository**
   First, clone this repository to your local machine:
   
   ```bash
   git clone https://github.com/taldb/DennisPD.git
2. **Copy the Script to the USB Drive**
   Copy the contents of the repository (including the script) to a folder on your USB drive. Make sure the folder contains the necessary subdirectories for Python, Node.js, Git, etc.

3. **Run the Script**
   Open a PowerShell terminal and run the script directly from the USB drive. The script will automatically configure the environment.

   Example:

   ```powershell
   .\DennisPD.ps1
   ```

4. **Start Developing**
   Once the script runs, it will configure your terminal with the correct paths for tools such as Python, Node.js, and more. You can now run the following tools directly from the terminal:

   * **Visual Studio Code**: Type `code` to launch VSCode.
   * **LibreCAD Portable**: Type `librecadportable` to run LibreCAD.

---

## How it Works

* **Customizing PATH**: The script dynamically adds directories from the USB drive to your `PATH` environment variable, allowing you to use tools like Python, Node.js, Git, .NET SDK, and others directly from the terminal.

* **Python Environment Management**:

  * You can switch between Python environments stored on the USB drive by running the `Switch-Pyenv` function.
  * The script will automatically add the correct directories for the selected Python environment to `PATH`.

* **Terminal Prompt Customization**: The script customizes the terminal prompt to display `(DennisPD)` before the current directory.

* **Verification**: The script verifies that the Python executable being used is from the USB drive, ensuring consistency across different systems.

---

## Functions

### `Add-DirToPath($dir)`

Adds the specified directory to the `PATH` environment variable.

### `Remove-DirFromPath($dir)`

Removes the specified directory from the `PATH` environment variable.

### `Set-Prompt`

Customizes the terminal prompt to display `(DennisPD)` before the current directory.

### `Confirm-Python`

Verifies that Python is running from the USB drive and outputs the Python version and executable location.

### `Switch-Pyenv`

Lists available Python environments stored on the USB drive and allows you to switch between them. It updates the `PATH` and environment variables accordingly.

---

## Troubleshooting

* **USB Drive Not Found**: If the script cannot find the USB drive, it will display an error message. Make sure the drive is connected properly and try again.

* **Python Environment Issues**: If the Python environment isn't set correctly, try running the `Switch-Pyenv` function manually to select a different environment.

* **Missing Tools**: Ensure the necessary tools (e.g., Python, Node.js, Java) are available in the correct directories on the USB drive as expected by the script.

---

## License

This project is licensed under the CC BY-NC 4.0 License - see the [LICENSE](LICENSE) file for details.
