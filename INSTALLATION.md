# Aayatti Desktop Companion — Install Guide

Download the installer for your computer from the [Releases](../../releases)
page, install it, then sign in with your company account. It takes about five
minutes.

This build is **not signed by Apple or Microsoft yet**, so your computer warns
you before it opens. That is expected. The steps below show how to allow it on
each system. Only do this for files downloaded from this page.

## Before you start

- **An account.** Your administrator creates it. You also need your
  **company domain** (for example `vardaam`); ask your administrator if you do
  not know it.
- **Administrator rights** on the computer. The Windows and Linux installers
  ask for your computer password.
- **A supported system:** macOS on Apple Silicon or Intel, Windows 10 or 11
  (64-bit), or 64-bit Ubuntu 22.04 or later, Debian 12 or later, Fedora or
  RHEL.

## Download

1. Open the [Releases](../../releases) page.
2. Open the newest release and expand **Assets**. Download the file for your
   system:
   - macOS: `Aayatti-Desktop-Companion_<version>_macos_universal.dmg`
   - Windows: `Aayatti-Desktop-Companion_<version>_windows_x64.msi`
   - Ubuntu / Debian: `Aayatti-Desktop-Companion_<version>_linux_amd64.deb`
   - Fedora / RHEL: `Aayatti-Desktop-Companion_<version>_linux_amd64.rpm`
3. Optional: also download `Aayatti-Desktop-Companion_<version>_checksums.txt`
   and [check your download](#check-your-download).

The macOS file works on both Apple Silicon and Intel Macs. There is no Linux
build for ARM computers yet.

## Install on macOS

macOS blocks the app the first time because this build is not notarized by
Apple. You allow it once in **Privacy & Security**.

1. Double-click `Aayatti-Desktop-Companion_<version>_macos_universal.dmg` in
   your Downloads folder.
2. In the window that opens, drag **Aayatti Desktop Companion** onto
   **Applications**. Then eject the disk image.
3. Open **Applications** and double-click **Aayatti Desktop Companion**.
4. macOS shows a warning such as *"Aayatti Desktop Companion" Not Opened* or
   *Apple could not verify it is free of malware*. Click **Done** (or **OK**).
   Do not click **Move to Trash**.
5. Open the **Apple menu → System Settings → Privacy & Security**.
6. Scroll down to the **Security** section. You see a line saying the app
   *was blocked to protect your Mac*.
7. Click **Open Anyway**. Enter your Mac password (or use Touch ID) when
   asked.
8. Click **Open Anyway** again in the window that appears. The app starts.

On older macOS (12 to 14) you can instead Control-click the app in
Applications → **Open** → **Open**.

The app lives in the menu bar (the Aayatti icon at the top of the screen). If
no window appears, click the icon and choose **Open Dashboard**.

## Install on Windows

Windows SmartScreen warns because this build has no publisher signature. You
allow it with **More info → Run anyway**.

1. If your browser marks the download as unsafe or uncommon, open the
   browser's downloads list, click **…** next to the file and choose **Keep**
   (Edge: **Keep → Show more → Keep anyway**).
2. Double-click `Aayatti-Desktop-Companion_<version>_windows_x64.msi`.
3. A blue window says *Windows protected your PC*. Click **More info**, then
   **Run anyway**.
4. Follow the installer. When User Account Control asks *Do you want to allow
   this app to make changes?* (publisher: Unknown), click **Yes**.
5. Wait for the install to finish, then click **Finish**.
6. Open **Aayatti Desktop Companion** from the Start menu.

If **Run anyway** does not appear, right-click the `.msi` → **Properties** →
tick **Unblock** at the bottom → **OK**, then double-click it again.

The app lives in the system tray (bottom right, possibly under **^**). If no
window appears, click the Aayatti icon and choose **Open Dashboard**.

## Install on Linux

The software centre may warn that the package is unverified or comes from a
third party. That is expected for this build: continue.

### Ubuntu / Debian (`.deb`)

1. Double-click `Aayatti-Desktop-Companion_<version>_linux_amd64.deb`. App
   Center (or Software) opens.
2. If it warns about an unverified or third-party package, choose to continue.
3. Click **Install** and enter your password.

Or in a terminal:

```bash
sudo apt install ~/Downloads/Aayatti-Desktop-Companion_<version>_linux_amd64.deb
```

### Fedora / RHEL (`.rpm`)

1. Double-click `Aayatti-Desktop-Companion_<version>_linux_amd64.rpm`.
   Software opens.
2. If it warns that the package is unsigned or unverified, choose to continue.
3. Click **Install** and enter your password.

Or in a terminal:

```bash
sudo dnf install ~/Downloads/Aayatti-Desktop-Companion_<version>_linux_amd64.rpm
```

### After installing on Linux

- Open **Aayatti Desktop Companion** from the applications menu.
- The app lives in the system tray. On GNOME the tray needs the
  **AppIndicator** extension (preinstalled on Ubuntu). If no window appears,
  click the Aayatti icon and choose **Open Dashboard**.
- On GNOME with Wayland, the app may offer to install a small GNOME extension.
  Accept it, then log out and log back in.

## Sign in

1. In the app, enter your **Company Domain** (for example `vardaam`) and click
   **Continue**.
2. Enter your **Email** and **Password** and click **Sign In**, or use your
   company's sign-in button if one is shown.
3. The dashboard opens. Closing the window keeps the app running in the menu
   bar / tray; choose **Quit** there to stop it.

## AI Analytics

AI Analytics is available only on **company-managed Macs**, and only if your
organization uses it. It is not available on Windows and Linux yet.

1. On the dashboard, find the **AI Analytics** card and click **Enable AI
   Analytics**. Enter your Mac password when asked.
2. Click **Connect this computer**. Your browser opens your company's Aayatti
   site.
3. Sign in if asked, check the device details, and confirm. Only confirm if
   you started this from the app on this computer just now.
4. Return to the app. The card shows **Connected**.

If the app says *Not installed: this device is not managed by your company
(MDM)*, your Mac is not enrolled in your company's device management. Contact
your administrator.

| Status | Meaning | What to do |
|---|---|---|
| Connected | AI Analytics is on for your account | Nothing |
| Not connected | Installed, but no account is linked | Click **Connect this computer** |
| Waiting for approval | The browser step is not finished | Finish it in the browser, or click the button again |
| Not installed | AI Analytics is off on this Mac | Click **Enable AI Analytics** |
| Stopped / Unavailable | The background service is not running | Restart the Mac; contact your administrator if it stays |

## Check your download

Download `Aayatti-Desktop-Companion_<version>_checksums.txt` from the same
release into the same folder as the installer.

macOS and Linux (Terminal, in that folder):

```bash
shasum -a 256 -c Aayatti-Desktop-Companion_<version>_checksums.txt --ignore-missing
```

Your installer's line must end in `OK`.

Windows (PowerShell, in that folder):

```powershell
Get-FileHash .\Aayatti-Desktop-Companion_<version>_windows_x64.msi -Algorithm SHA256
```

The hash must match the `.msi` line in the checksums file (letter case does
not matter).

## If something goes wrong

- **The app does not open on macOS.** Repeat steps 4 to 8 of "Install on
  macOS".
- **No window appears.** The app runs in the menu bar / tray. Click its icon →
  **Open Dashboard**. Opening the app a second time also shows the window.
- **The company domain or sign-in is not accepted.** Check the company domain
  and your email with your administrator.
- **No tray icon on Linux.** Enable the AppIndicator extension (GNOME), then
  log out and back in.
- **The network stops working after enabling AI Analytics.** Click **Turn off
  AI Analytics** in the app. Contact your administrator if that does not fix
  it.

## Updates

The app does not update itself yet. When a new version is listed in
[What's new](./WHATS-NEW.md), download it from [Releases](../../releases) and
install it over the old one, the same way as above. You stay signed in.

## Uninstall

- **macOS:** if AI Analytics is on, first click **Turn off AI Analytics** in
  the app and enter your password. Then quit the app (menu bar icon →
  **Quit**) and drag it from Applications to the Trash.
- **Windows:** **Settings → Apps → Installed apps → Aayatti Desktop Companion
  → Uninstall**.
- **Linux:** App Center / Software → **Aayatti Desktop Companion** →
  **Uninstall**, or `sudo apt remove aayatti-desktop-companion` (Ubuntu /
  Debian), `sudo dnf remove aayatti-desktop-companion` (Fedora / RHEL).

Your account and the data already sent to your organization stay on the
Aayatti website.
