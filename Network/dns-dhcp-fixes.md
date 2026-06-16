# Fixing IP Assignment & DNS Cache Issues

This guide is for when a computer connects to the network via cable or Wi-Fi but shows "Unidentified Network / No Internet" or cannot open specific internal servers.

## Step 1: Open the Command Line (CMD)
To start troubleshooting, I need to open the Windows command line tool on the user's PC:
1. Press the **Windows Key + R** on the keyboard to open the "Run" dialog box.
2. Type `cmd` into the box and press **Enter**.
3. A black Command Prompt window will now appear on the screen.

## Step 2: Check the Current IP Network Settings
Inside the black CMD window, type the following command and press **Enter**:

```cmd

ipconfig /all

ipconfig /release

ipconfig /renew

ipconfig /flushdns

