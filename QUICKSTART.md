# Rift Conduit — Quick start

Install Rift Conduit on the **Windows computer that holds your files**. Install your chosen SFTP client on the **computer you connect from**.

[Official website](https://riftconduit.com/) · [Download for Windows](https://download.aicreatenow.com/software/rift-Conduit2.0.0microsoftSigned.exe) · [Full connection guide](https://riftconduit.com/connection-guide.html)

## 1. Install and start your trial or activate

Use Windows 11 x64 or Windows Server 2022/2025 with Desktop Experience, administrator access and .NET Framework 4.7.2 or newer. Server Core and domain controllers are not supported.

Run the official installer. It prepares supported missing OpenSSH components from its bundled local source. If Windows requests a restart, restart the computer yourself, then rerun the installer to finish.

Open Rift Conduit and choose **Start Trial**, or enter your supplied ten-digit license key and activate. The trial lasts 48 elapsed hours from that explicit action. Installation alone does not start the trial or open SFTP access.

## 2. Set the incoming client address

In **Allowed IP address**, enter the source IPv4 address of the computer or network you connect **from**. For a direct internet connection, this is usually that location's public IPv4 address.

The Tailscale option adds an allowance for `100.64.0.0/10`. Use it when you have already configured Tailscale on both computers. Rift Conduit does not install or configure Tailscale.

Direct internet connections may require router TCP 22 forwarding and a restricted cloud firewall rule. Existing Windows Firewall rules and administrative policies remain in force; Rift Conduit's allowances do not override all other rules.

## 3. Turn on SFTP and authorize an account

Select **Turn On** and wait for the ready status. Use the account-creation button to create a local Windows administrator account, or follow the [existing-account instructions](https://riftconduit.com/connection-guide.html) to authorize an intended local account in Rift Conduit's access group.

Created accounts have broad administrator access, governed by Windows file permissions. Rift Conduit does not confine them to one folder.

When you create an account, the app saves a credentials file and a separate instructions file on the Desktop. The credentials file includes a plaintext password and host-key fingerprint. Its permissions are restricted, but it should still be stored securely or removed when no longer needed. Desktop synchronization or backups can copy it elsewhere.

## 4. Connect with your preferred SFTP client

Use a separately installed SFTP file browser or compatible remote-drive application. The [complete guide](https://riftconduit.com/connection-guide.html) provides official client links for Windows, macOS and Linux.

| Client setting | Value |
| --- | --- |
| Protocol | **SFTP** |
| Host / Server | The Windows host's reachable IPv4 address, or its Tailscale IPv4 address if using Tailscale |
| Port | **22** |
| Username | Your authorized local Windows account on the host |
| Password | The account password, **not** a Windows Hello PIN |
| Remote path | `/C:/` if the client requests it |
| Drive letter | An unused letter, such as `Z:`, if your remote-drive client requests one |

**Allowed IP is the client's source address. Host / Server is the computer holding your files.**

Before accepting the first connection, compare the host-key fingerprint with your credentials file. For an existing account, obtain the matching fingerprint from the server administrator through a trusted channel. Investigate an unexpected key change before accepting it.

You can now browse and transfer files according to the account's Windows permissions. Remote edits change the real files on the host. The managed listener is SFTP-only; it does not provide an SSH terminal, remote desktop or port forwarding.

## 5. Stop access when you choose

Closing the application window leaves the active listener running while your trial or license permits access.

To stop it, reopen Rift Conduit and select **Turn Off**. This stops its managed listener and sessions and removes its own firewall rules. Settings, host keys and Windows accounts remain available for next time. At trial expiry, the managed access stops even if the app window is closed.

## If a connection fails

- Confirm that **Allowed IP** identifies the incoming client, while the SFTP client's **Host / Server** identifies the Windows host.
- Confirm the host is reachable on TCP port 22 through the relevant router, cloud firewall, Windows Firewall and any Tailscale configuration.
- Use the account password rather than a Windows Hello PIN, and check the account's SFTP access-group membership.
- If OpenSSH is missing or damaged, repair the signed installation. **Turn On** verifies components; it does not download or install them.
- Read [Setup and help](https://riftconduit.com/help.html), or email [info@AICreateNow.com](mailto:info@AICreateNow.com). Do not publish passwords, license keys or private connection details in GitHub issues.

## Keep using Rift Conduit

The [one-time $7.99 lifetime license](https://buy.stripe.com/6oU7sN0JB5l66c40Fw5kk0d) is bound to the activated computer and includes lifetime support and upgrades. Purchase is followed by explicit activation of your supplied key in the app.

Keep that key: uninstalling removes registration, so reinstalling requires activation again. Reinstalling does not reset the free trial.

[Trial and license information](https://riftconduit.com/docs/LICENSE-INFORMATION.txt) · [Privacy policy](https://riftconduit.com/privacy.html)

Copyright © 2026 AI Creations Now Software Development. All rights reserved.
