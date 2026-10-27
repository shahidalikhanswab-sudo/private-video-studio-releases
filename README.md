# Private Video Studio — Windows Releases

This repository is the **public release channel** for Private Video Studio, a private, local-first Windows video editor.

**This is not the application's source-code repository.** It is deliberately separate from BotLance, PubZora, and other SaaS projects. It holds only public release documentation and (once published) signed application downloads.

## Release status

**Update channel prepared; first signed release not yet published.**

Do not assume a version exists until it appears under [GitHub Releases](../../releases). The installed editor must contain the matching update endpoint and public signature-verification key.

## Downloads and updates

- Official release page: [Releases](../../releases)
- Update manifest URL (active **only after a valid release is published**): `https://github.com/shahidalikhanswab-sudo/private-video-studio-releases/releases/latest/download/latest.json`
- Each release must have a Windows setup executable and its Tauri v2 detached updater signature (`.exe.sig`).
- For the first test, install a signed baseline version, then publish a **higher** version to verify in-app updating.

## What is allowed here

- Windows installer: `*-setup.exe`
- Tauri v2 detached Windows setup signature: `*-setup.exe.sig`
- `latest.json` update manifest
- Release notes and non-sensitive documentation

## Never publish

- Source code of unrelated SaaS projects
- `08-Owner-Private/`, `*.key`, signing passwords, API keys, environment files or authentication tokens
- Personal videos, voiceover files, projects, backups, or other private data

## How to publish

Read [RELEASE-GUIDE.md](RELEASE-GUIDE.md) and [SECURITY.md](SECURITY.md). Only publish files produced by a successful signed Windows build. **Do not create placeholder `latest.json` files or publish unsigned updates.**

The signing **private** key stays with the owner, outside GitHub. Only its corresponding **public** key is embedded in the app.
