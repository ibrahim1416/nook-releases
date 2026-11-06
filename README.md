# VirtualMeet

Peer-to-peer hangouts for friends: text chat, voice, screen sharing up to 4K,
and a shared whiteboard, with no server in the middle.

This repository only hosts the installers. Once installed, VirtualMeet keeps
itself up to date.

## Windows 10 and 11

1. Download **[VirtualMeet-Setup.exe](https://github.com/ibrahim1416/virtualmeet-releases/releases/latest/download/VirtualMeet-Setup.exe)**.
2. Double-click it. Windows may say "Windows protected your PC" because the
   installer isn't signed with a paid certificate yet. Click **More info**,
   then **Run anyway**.
3. VirtualMeet installs for your user (no administrator rights needed) and
   starts. Allow it through Windows Firewall when asked, so friends can
   connect to you.

Updates download in the background. When one is ready, VirtualMeet offers a
restart; otherwise it updates the next time you close it.

## Ubuntu 22.04 and newer (64-bit)

1. Download **[virtualmeet_amd64.deb](https://github.com/ibrahim1416/virtualmeet-releases/releases/latest/download/virtualmeet_amd64.deb)**.
2. Install it from a terminal in your Downloads folder:

   ```bash
   sudo apt install ./virtualmeet_amd64.deb
   ```

3. Start VirtualMeet from the app menu.

The package adds the VirtualMeet update repository, signed with the
publisher's key. Ubuntu installs VirtualMeet updates automatically together
with its security updates, and they also show up in Software Updater. When
an update was installed while VirtualMeet was running, it offers a restart.

To uninstall: `sudo apt remove virtualmeet`. This also removes the update
repository and its key.

## Your data

Your identity and chat history are stored outside the app, in
`%APPDATA%\VirtualMeet` on Windows and `~/.config/VirtualMeet` on Ubuntu, so
updating or reinstalling keeps them.
