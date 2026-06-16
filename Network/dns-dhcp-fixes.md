# Fixing IP Assignment & DNS Cache Issues

This guide is for when a computer connects to the network via cable or Wi-Fi but shows "Unidentified Network / No Internet" or cannot open specific internal servers.

# Step 1: Open the Command Line (CMD)
To start troubleshooting, I need to open the Windows command line tool on the user's PC:
1. Press the **Windows Key + R** on the keyboard to open the "Run" dialog box.
2. Type `cmd` into the box and press **Enter**.
3. A black Command Prompt window will now appear on the screen.

# Step 2: Check the Current IP Network Settings
Inside the black CMD window, type the following command and press **Enter**:
```cmd
ipconfig /all

If you confirmed in Step 2 that your IP is stuck on 169.254.x.x, we need to reset it. Type these two commands inside the same CMD window one by one (press Enter after each):

ipconfig /release

This command forces the computer to ask the network router for a brand new, working IP address:

ipconfig /renew

Wait about 5-10 seconds. The text on the screen will update, and your IPv4 Address should now change to a proper corporate IP (like 10.x.x.x).


