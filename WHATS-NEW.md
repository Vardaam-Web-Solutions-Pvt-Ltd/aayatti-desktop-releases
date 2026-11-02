# What's New

Changes in each version of the Aayatti Desktop Companion. Downloads are on the
[Releases](../../releases) page.

## 0.1.14

Not yet code-signed.

- **Windows: the app connects again while AI Analytics is on.** Since 0.1.8 the app misread the proxy setting AI Analytics uses, so signing in, punching and syncing failed with "Network error: Could not connect to server". On an affected computer the automatic update cannot reach the server either: download this version and install it by hand (it needs administrator permission). Signing in now also works on every system when the AI Analytics service is not answering.
- **Windows: the app moves to Program Files.** It is now installed once for the whole computer. This update asks for administrator permission; without it the app stays on the current version and keeps working.
- **Signing out during a server outage is no longer lost.** AI Analytics now records a sign-out made while the server cannot be reached.
- **The website shows each computer's current version.** AI Analytics now reports its version with each upload.
- **Security improvements.** On Linux, the app's data folder can be opened only by its owner. Debug features are off in released builds. The app opens web links only on its own sites.

## 0.1.5

Pre-release, for pilot users. Not yet code-signed.

- **Cursor answers are recorded.** A Cursor prompt is no longer recorded before its answer is written, so the answer is no longer missing. The amount of context the conversation uses is recorded too.
- **Antigravity is recorded.** Antigravity used to refuse the AI Analytics certificate, so nothing it did was recorded. It now works once the app is restarted after this update.
- **Branch, commit and changed files for more tools.** On macOS, prompts from Cursor, Antigravity and the Codex built into the ChatGPT app now show the git branch, commit and changed files of the project they were made in.

## 0.1.0

First release, for pilot users. Not yet code-signed.

- Sign in with your company domain and your Aayatti account.
- Punch in and punch out from the app or from the menu bar / system tray.
- See your punch status and today's summary on the dashboard.
- Get notifications from your organization.
- AI Analytics (company-managed Macs only, when your organization uses it).
