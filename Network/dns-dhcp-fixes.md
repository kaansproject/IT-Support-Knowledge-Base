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

🔍 How to Read the Screen:

Once you hit Enter, a lot of text will scroll down. Scroll up slightly and look for the section called "Ethernet adapter Ethernet" or "Wireless LAN adapter Wi-Fi".

Inside that section, find the line that says IPv4 Address.

    What you might see: If your computer cannot talk to the network router, Windows gives up and automatically assigns a fake, useless IP address that always starts with 169.254.x.x (This is called an APIPA address).

    The Diagnostic: If you see 169.254 at the beginning of your IP address, it means your computer is completely disconnected from the corporate network server.

Step 3: Why and How to Reset the IP Address

Because we found out in Step 2 that the IP is stuck on 169.254, we cannot access the internet. We need to clear this fake IP and force the computer to ask the network for a real, working connection.

Type these two commands inside the same CMD window one by one (press Enter after each):

    This command drops the fake 169.254 IP address and empties your network card:

    ipconfig /release

    This command forces the computer to reach out to the company's router and grab a brand new, working corporate IP (which will start with 10.x.x.x or 192.168.x.x):

    ipconfig /renew

    The Result: After a few seconds, the screen will update. Look at the IPv4 Address line again. The fake 169.254 should be gone, replaced by a real network IP.

Step 4: Flush the Corrupted DNS Cache

If the internet connection is back but certain corporate websites or internal tools still refuse to load, the local DNS memory is corrupted. To clear it, type this command in CMD and press Enter:

ipconfig /flushdns

What happens: You will see a success message saying "Successfully flushed the DNS Resolver Cache." The websites will now open correctly.

