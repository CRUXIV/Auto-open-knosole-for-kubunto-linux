# Autostart Konsole Script

This repository contains instructions for creating a script to automatically launch Konsole, the terminal emulator, when you start your computer on Kubuntu.

## How to Set Up the Autostart Script

Follow these steps to create and configure the script:

### 1. Create the Startup Script

1. Open a terminal and create a new script file:

	```bash
	nano ~/launch_konsole.sh
	```

2. Copy and paste the following content into `launch_konsole.sh`:

	```bash
	#!/bin/bash

	# Launch Konsole
	konsole &
	```

3. Save the file and exit the editor:
	- Press `Ctrl + X`
	- Press `Y` to confirm saving
	- Press `Enter` to exit

4. Make the script executable:

	```bash
	chmod +x ~/launch_konsole.sh
	```

### 2. Add the Script to Autostart

1. Open the KDE Autostart Configuration:
   - Go to **System Settings** > **Startup and Shutdown** > **Autostart**.

2. Add a New Startup Entry:
   - Click on **Add Script**.
   - Browse to and select your script file (`~/launch_konsole.sh`).
   - Click **OK** or **Apply** to save the changes.

### Alternative Method: Using a `.desktop` File

1. Create a `.desktop` file for Konsole:

	```bash
	nano ~/.config/autostart/konsole.desktop
	```

2. Copy and paste the following content into `konsole.desktop`:

	```ini
	[Desktop Entry]
	Type=Application
	Exec=konsole
	Hidden=false
	NoDisplay=false
	X-GNOME-Autostart-enabled=true
	Name=Konsole
	Comment=Launch Konsole terminal
	```

3. Save the file and exit the editor:
	- Press `Ctrl + X`
	- Press `Y` to confirm saving
	- Press `Enter` to exit

## License

This project is licensed under the MIT License.

## Contact

For any questions or issues, please contact [Charlieulmanxiv@gmail.com].


