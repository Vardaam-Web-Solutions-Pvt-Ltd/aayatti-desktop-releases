# Installing Aayatti Desktop Companion

Download installers only from the
[Releases](https://github.com/Vardaam-Web-Solutions-Pvt-Ltd/aayatti-desktop-releases/releases)
page of this repository.

## Which file do I need?

| Computer | File |
|----------|------|
| Mac (Apple Silicon or Intel) | `Aayatti-Desktop-Companion_<version>_macos_universal.dmg` |
| Windows 10 or 11 (64-bit) | `Aayatti-Desktop-Companion_<version>_windows_x64.msi` |
| Debian, Ubuntu | `Aayatti-Desktop-Companion_<version>_linux_amd64.deb` |
| Fedora, RHEL | `Aayatti-Desktop-Companion_<version>_linux_amd64.rpm` |
| Other Linux | `Aayatti-Desktop-Companion_<version>_linux_amd64.AppImage` |

The macOS file works on Apple Silicon and Intel Macs. Most Windows and Linux
computers are 64-bit Intel or AMD (`x64` / `amd64`). There are no Linux builds
for ARM (`aarch64`) computers yet.

## Unsigned builds

Current builds are **not code-signed** yet. Your operating system cannot
confirm the publisher, so it shows a warning the first time you open the app.
Continue only if you downloaded the file from this repository's Releases page
and its checksum matches (see below). If your company manages your computer,
ask your IT team before installing.

## macOS

1. Download the `.dmg` file.
2. Open the downloaded file.
3. Drag the app to Applications.
4. Open the app.
5. If macOS shows a security warning, right-click the app and choose **Open**,
   or go to **System Settings → Privacy & Security** and choose **Open Anyway**.

## Windows

1. Download the `.msi` installer.
2. Run the installer.
3. If Windows shows "Windows protected your PC", review the file name, then
   choose **More info → Run anyway**.
4. Follow the installation wizard.
5. Launch the application from the Start menu.

## Linux

### Debian/Ubuntu

1. Download the `.deb` package.
2. Install it with your software installer, or run:
   `sudo apt install ./Aayatti-Desktop-Companion_<version>_linux_amd64.deb`
3. Launch the application.

### Fedora/RHEL

1. Download the `.rpm` package.
2. Install it with your software installer, or run:
   `sudo dnf install ./Aayatti-Desktop-Companion_<version>_linux_amd64.rpm`
3. Launch the application.

### Other distributions (AppImage)

1. Download the `.AppImage` file.
2. Make it executable: `chmod +x Aayatti-Desktop-Companion_<version>_linux_amd64.AppImage`
3. Run it.

Linux packages downloaded from GitHub are not signed by a package repository.
Your trust in them comes from downloading from this page and checking the
checksum.

## Check your download

Download `Aayatti-Desktop-Companion_<version>_checksums.txt` from the same
release into the same folder as the installer.

macOS and Linux:

```bash
shasum -a 256 -c Aayatti-Desktop-Companion_<version>_checksums.txt --ignore-missing
```

The installer's line must end in `OK`.

Windows (PowerShell):

```powershell
Get-FileHash .\Aayatti-Desktop-Companion_<version>_windows_x64.msi -Algorithm SHA256
```

The hash must match the `.msi` line in the checksums file (letter case does
not matter).

## Uninstall

- **macOS:** quit the app from its menu bar icon, then move it from
  Applications to the Trash.
- **Windows:** Settings → Apps → Installed apps → Aayatti Desktop Companion →
  Uninstall.
- **Debian/Ubuntu, Fedora/RHEL:** remove Aayatti Desktop Companion with your
  software manager.
- **AppImage:** delete the file.
