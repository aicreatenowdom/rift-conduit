# Rift Conduit support

For setup, licensing and product support, contact **[info@aicreatenow.com](mailto:info@aicreatenow.com)**.

[Official help](https://riftconduit.com/help.html) · [Connection guide](https://riftconduit.com/connection-guide.html) · [Download and requirements](https://riftconduit.com/download.html)

## What to include

- Rift Conduit version and your Windows edition/build.
- The SFTP client name and version, if the issue occurs while connecting.
- The step that failed and the exact error message.
- Whether you are connecting over the local network, a configured Tailscale connection, or another reachable network path.
- A redacted screenshot or short activity-log excerpt when useful.

Do not post license keys, passwords, connection credential files, or personal network details in public issues. Send licensing questions privately by email; never send your account password.

## Connection checklist

1. Confirm the Windows host is awake and reachable and Rift Conduit reports that SFTP is listening.
2. Select **SFTP** in your client, use **TCP port 22**, and connect to the host address reachable from that client.
3. Confirm the allowed incoming IPv4 matches the source address the host receives. With a VPN or network change, this may differ from the address you expected.
4. Compare the server host-key fingerprint with the one saved by Rift Conduit before accepting it.
5. Check the account credentials and Windows file permissions. Review existing firewall rules and your network configuration if a connection times out.

Rift Conduit configures the host-side SFTP listener. Router forwarding, VPN setup, network reachability and a separately installed SFTP client remain part of your connection setup. The [connection guide](https://riftconduit.com/connection-guide.html) explains these steps.

## Trial and activation

The trial lasts 48 elapsed hours after **Start Trial** succeeds. Installing the application alone does not start it, and reinstalling does not restart it. At expiry, the application stops its managed SFTP access.

A purchased ten-digit key must be activated in the app with Internet access and server approval. Payment alone does not activate the application. Keep the key for reactivation after reinstall or recovery.

## Security reports

Email potential security issues privately to **info@aicreatenow.com**. Include the affected version, a description and reproduction steps, with credentials and personal information removed. Avoid publishing exploit details or customer connection information in a public issue.

This repository contains product documentation and artwork. Application source code and installers are distributed separately through the official product website.
