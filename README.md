# Auto-Screenshot-and-Discord-Uploader
This Python script automatically captures screenshots every 10 seconds, saves them in date-based folders, and uploads them to a Discord channel via a webhook. The screenshots are timestamped for easy tracking. The script can run invisibly in the background and be set to start automatically on boot, ideal for monitoring or logging tasks.

## Features

- **Automatic Screenshot Capture**: Takes a screenshot every 10 seconds.
- **Date-based Folder Organization**: Creates folders named after the current date (in `DD_MM_YYYY` format) and saves the screenshots in these folders.
- **Custom Timestamped Filenames**: Each screenshot is saved with a filename in the format `shot_HHH_MMM_SSS_AMPM.png` (e.g., `shot_H09_M16_S22AM.png`), including hours, minutes, seconds, and AM/PM.
- **Discord Webhook Integration**: Automatically uploads each screenshot to a specified Discord channel via a webhook with a custom message containing the time the screenshot was taken.
- **Runs in the Background**: Can be set to run at startup using `pythonw`, so it works without a console window.

## Installation

### Prerequisites

- Python 3.x installed on your machine.
- The following Python libraries:
  - `Pillow` (for taking screenshots)
  - `requests` (for sending images to Discord via webhook)

You can install the required packages using `pip`:

```bash
pip install pillow requests
```

### Script Setup

- Clone or Download the Repository: Download the script or clone this repository to your local machine.

- Configure Discord Webhook: Open the script and replace the placeholder discord_webhook_url with your actual Discord webhook URL: "YOUR_WEBHOOK_URL_HERE"

- Set Directory for Screenshots: Modify the base_dir variable in the script to point to the directory where you want to save the screenshots:YOUR_DIR => D:\

### Running the Script

- Run with Console Window: If you want to run the script with a console window for debugging or monitoring purposes, you can execute it normally:
```
python auto_ss.py
```
- Run in the Background: To run the script in the background without a console window, use pythonw:
```
pythonw auto_ss.py
```
- This will keep the script running invisibly. To stop it, you can end the process using Task Manager or the command line
 
