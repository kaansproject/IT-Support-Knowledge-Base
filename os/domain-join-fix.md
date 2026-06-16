# Troubleshooting Active Directory Domain Join Errors

This guide fixes the common corporate error: *"The trust relationship between this workstation and the primary domain failed."* This happens when a computer loses its secure connection with the company's main server network (Domain Controller).

## Step 1: Check the System Time (The Hidden Culprit)
Before changing any network settings, you need to check the computer's local clock. 
*   **Why?** Active Directory uses a security protocol called Kerberos. If the computer's time is even **5 minutes different** from the company server's time, the server rejects the PC, and the login fails.

### How to check and force a sync:
1. Click the Windows Start menu, type `cmd`.
2. Right-click on **Command Prompt** and select **Run as Administrator**.
3. Inside the black window, type this command to see if the PC can sync its clock with the network server, then press **Enter**:

```cmd
net time /set /y