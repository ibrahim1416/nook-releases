# nook

Peer-to-peer hangouts for friends: chat, voice, screen sharing up to 4K,
apps like a shared whiteboard, with no server in the middle.

This repository only hosts the installers. Once installed, nook keeps itself
up to date.

## Coming from VirtualMeet?

nook used to be called VirtualMeet. Version 0.4.0 renamed everything, so
VirtualMeet doesn't turn into nook by itself: remove it, then install nook as
below. You start fresh: make a new identity, add your friends again with
friend codes, and re-create or re-join your spaces.

**Windows**

1. Close VirtualMeet.
2. Open **Settings → Apps → Installed apps**, find **VirtualMeet**, and choose
   **Uninstall**. If VirtualMeet already installed nook on its own as an
   update, keep nook and remove only VirtualMeet.
3. Optional, to remove its data too: press **Win + R**, enter
   `%APPDATA%\VirtualMeet`, and delete that folder. Also delete any leftover
   VirtualMeet shortcut on your desktop.

**Ubuntu**

```bash
sudo apt remove virtualmeet
```

This also removes VirtualMeet's update repository and key. Optional, to remove
its data too:

```bash
rm -rf ~/.config/VirtualMeet
```

## Windows 10 and 11

1. Download **[nook-setup.exe](https://github.com/ibrahim1416/nook-releases/releases/latest/download/nook-setup.exe)**.
2. Double-click it. Windows may say "Windows protected your PC" because the
   installer isn't signed with a paid certificate yet. Click **More info**,
   then **Run anyway**.
3. nook installs for your user (no administrator rights needed) and starts.
   Allow it through Windows Firewall when asked, so friends can connect to you.

Updates download in the background. When one is ready, nook offers a restart;
otherwise it updates the next time you close it. To check right away, open
Settings → Updates.

## Ubuntu 22.04 and newer (64-bit)

1. Download **[nook_amd64.deb](https://github.com/ibrahim1416/nook-releases/releases/latest/download/nook_amd64.deb)**.
2. Install it from a terminal in your Downloads folder:

   ```bash
   sudo apt install ./nook_amd64.deb
   ```

3. Start nook from the app menu.

The package adds the nook update repository, signed with the publisher's key.
Ubuntu installs nook updates automatically together with its security updates,
and they also show up in Software Updater. To update right away:

```bash
sudo apt update && sudo apt install --only-upgrade nook
```

When an update was installed while nook was running, it offers a restart.

To uninstall: `sudo apt remove nook`. This also removes the update repository
and its key.

## Your data

Your identity and chat history are stored outside the app, in `%APPDATA%\nook`
on Windows and `~/.config/nook` on Ubuntu, so updating or reinstalling keeps
them.
