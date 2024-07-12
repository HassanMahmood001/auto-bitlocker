# BitLocker Drive Monitor and Locker

## Overview
This Python script monitors BitLocker encrypted drives on Windows systems and automatically locks them when they are not in use. It utilizes PowerShell commands to detect active BitLocker drives and `psutil` for process management to determine drive usage.

## Features
- Detects active BitLocker encrypted drives.
- Monitors drive activity using process inspection.
- Automatically locks BitLocker drives after a period of inactivity.

## Requirements
- Python 3.x
- `psutil` library (`pip install psutil`)
- Administrative privileges on Windows

## Usage
1. **Setup Environment:**
   - Install Python from [python.org](https://www.python.org/downloads/).
   - Install `psutil` library:
     ```
     pip install psutil
     ```

2. **Run the Script:**
   - Open a command prompt or PowerShell as administrator.
   - Navigate to the directory containing the script.
   - Execute the script:
     ```
     python bitlocker.py
     ```

3. **Build Executable (Optional):**
   - You can build an executable using tools like PyInstaller for distribution:
     ```
     pip install pyinstaller
     pyinstaller --onefile bitlocker.py
     ```
   - The executable will be located in the `dist` directory.

4. **Schedule as Task (Persistence):**
   - To run the script automatically on startup or at specific times:
     - Open Task Scheduler (`taskschd.msc`) as administrator.
     - Create a new task, set the trigger (e.g., on login), and configure the action to run the script (`bitlocker.exe` or `python bitlocker.py`).
     - Ensure to set it to run with highest privileges under the Security options.

## Contributions
Contributions and suggestions are welcome! Feel free to fork and submit pull requests for improvements or new features.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
