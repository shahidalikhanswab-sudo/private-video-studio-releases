# Security and signing policy

This repository is **public** so installed applications can download updates without GitHub credentials.

## Signing identity

- All updater archives must be signed with the owner's existing Tauri updater signing key.
- The updater public key must be embedded in the desktop application before that version is built.
- The private signing key and signing password must **never** be committed, uploaded as a release asset, shared in chat, or stored in this repository.
- Back up the owner-only signing identity to secure, offline storage. Losing it can prevent existing installations from accepting future updates.
- Do not regenerate a key for a published update channel unless intentionally planning a key rotation/migration for installed users.

## Allowed public artifacts

A release may include `<app>-<version>-setup.exe`, the matching Tauri v2 `*-setup.exe.sig`, and `latest.json`. Filenames must exactly match the output of the current signed build.

## Release safety checks

Before publishing verify: version increased, setup EXE opens, signed Windows setup executable and matching `.exe.sig` exist, signature matches installer, `latest.json` contains the matching version and HTTPS URL, and user projects remain preserved through installation. GitHub Release assets are **not** a safe place for user data.

## Security incidents

If the private updater key is exposed, stop publishing and do not rely on that identity. Investigate and plan a secure migration before offering new updates. Avoid posting secret values in issues.
