# Windows Wi-Fi Profile Viewer

A simple Python script that utilizes the native Windows `netsh` command-line utility to retrieve and display saved Wi-Fi network profiles and their corresponding passwords in clear text.

## How It Works
The script executes two main commands via the Python `subprocess` module:
1. `netsh wlan show profiles` - Retrieves a list of all Wi-Fi networks previously connected to and saved on the Windows machine.
2. `netsh wlan show profile [Profile Name] key=clear` - Extracts the specific details for each profile, including the plaintext password ("Key Content").

The output is formatted into a clean, easy-to-read table displaying the Network Name (SSID) alongside its password.

## Prerequisites
- **Operating System:** Windows (The `netsh` command is specific to Windows).
- **Python:** Python 3.x installed.

## Usage
1. Save the script as `wifi_viewer.py` (or your preferred name).
2. Open a command prompt or terminal.
3. Run the script:
   ```bash
   python wifi_viewer.py
   ```

## Example Output
```
Network_SSID_1                | Password123
Guest_Network                 | GuestPass!
Coffee_Shop_WiFi              | 
```
*(Note: Networks without a saved password or open networks will display an empty space next to the SSID).*

## Disclaimer
This script is intended for personal use, such as recovering a forgotten Wi-Fi password for a network you own or have authorized access to. Do not use this script on machines or networks without explicit permission from the owner.

