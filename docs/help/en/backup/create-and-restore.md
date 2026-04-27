# Backup creation and restoration

In Phylax, backups are not optional hygiene. They are the only real protection between you and a device loss. Phylax does not sync to a cloud. If your device breaks, gets stolen, or the browser clears its IndexedDB, then without a backup all your observations, lab values, supplements, open points and profile versions are gone. This page shows how to prevent that.

## Two backup paths

Phylax offers two backup formats; both have legitimate uses.

### Encrypted `.phylax` backup

The default backup. A `.phylax` file is:

- complete (contains all your profile data)
- encrypted with your master password (AES-256-GCM)
- only readable with the same master password
- a binary file, not human-readable
- not openable by any other program

This is the path when you want to back up your profile or move it between devices without leaving plaintext data anywhere.

### Markdown export

The second backup. A Markdown file is:

- fully readable in plaintext
- not encrypted
- openable in any text editor
- directly importable back into Phylax (see [Importing a profile](../data/profile-import.md))

This is the path when you want to archive your profile outside of Phylax (for example in a private notes system), when you want to print it, or when you want to give it to someone else.

!!! warning "Markdown backups are unencrypted"
    A Markdown backup contains all your health data in plaintext. Treat the file the way you would a medical dossier: secure storage, no email attachment to strangers, no cloud storage without your own encryption layer.

## Creating a backup

In the **Settings** page, the Backups section. Clicking **Create backup** opens a small form where you pick the format (`.phylax` or Markdown). Phylax bundles your data and the browser offers the file for download.

The file lands in your browser's download folder. Move it to a safe storage location promptly; the download folder is neither organized nor protected against accidents.

## When to take a backup

- **After major edits.** A new diagnosis, a new lab report with twenty values, a reorganization of the supplement list. You do not want to redo this work if something goes wrong.
- **Before browser cleanup actions.** If you plan to "Clear cookies and site data" anyway, back up first.
- **Periodically, regardless of occasion.** A weekly or monthly calendar entry "Phylax backup" is enough. Frequency depends on your entry activity.
- **Before device or browser changes.** Phylax data is per browser; without a backup you start from zero on a new device.

## Where to store backups

A backup in your current device's download folder does not protect you from losing that device. Multiple locations reduce the risk of total loss.

- **Second device:** External drive, USB stick, second computer.
- **Private cloud:** Your own Nextcloud, Synology NAS, or similar with encryption.
- **Encrypted drive:** A BitLocker volume, FileVault USB stick, VeraCrypt container.
- **Public cloud (`.phylax` only):** Since `.phylax` files are already encrypted with your master password, they can sit in a public cloud (Dropbox, Google Drive, etc.). The file would be encrypted at rest; the risk is the strength of your master password. Markdown backups do not belong there.

Three different locations are better than one perfect one. An older backup at a second location is worth more than the newest backup at the same location as the original.

## Restoring a backup

Phylax provides two restore paths, depending on the state of the app.

### Before login (welcome screen)

When the app is empty (fresh install, or after a reset), the onboarding screen offers **Import backup**. You pick a `.phylax` file, enter the master password it was encrypted with, and Phylax restores the profile.

This is the standard migration to a new device: open the app, import the backup, done.

### After login (Settings)

When you are in an unlocked Phylax session and want to import an older backup (for example after an accidental deletion), open Settings, Backups area, **Import backup**.

!!! warning "Restore overwrites"
    A restore replaces the current profile state completely with the state of the backup. If you have made entries since the backup, those will be gone afterward. When in doubt: take a current backup first, then restore, so you can roll back to the current version in an emergency.

Both paths require the master password the backup was created with. That is not necessarily your current master password: if you changed your master password after creating the backup, you need the old one to import it.

## What backups do NOT solve

Encrypted backups protect you against:

- Loss or failure of the device
- Accidental deletion of an observation or a profile
- Browser cleanup actions that remove IndexedDB data
- iOS Safari clearing data after 7 days of inactivity

Encrypted backups do NOT protect you against:

- **A forgotten master password.** The backup is encrypted with the same password as your live data. If you forget the password, the backup is just as inaccessible as the database. See [First Steps: Master password](../getting-started/first-steps.md#2-set-your-master-password).
- **Losing all your backup strategies at the same time.** If the device breaks, the backup USB was in the same bag, and you have no cloud copy, everything is gone. Multiple locations. Always.

## A practical recommendation

A combination that works for most Phylax users:

1. **Weekly calendar entry:** create a `.phylax` backup and copy it to your private cloud.
2. **Quarterly:** also write to a USB stick or external drive.
3. **Before travel or device changes:** ad-hoc backup.

Plus: master password stored in at least two places (password manager and physical note). See [First Steps: Recommended strategies](../getting-started/first-steps.md#recommended-strategies).

## Read more

- Storing the master password safely: [First Steps](../getting-started/first-steps.md#2-set-your-master-password).
- What is inside the `.phylax` format: architectural background at [github.com/astrapi69/phylax](https://github.com/astrapi69/phylax).
- Importing a Markdown profile: [Importing a profile](../data/profile-import.md).

Status: 2026-04-27 (Iteration 1, first content)
