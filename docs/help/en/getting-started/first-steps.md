# First Steps

This guide walks you from "app opened" to your first saved observation. Plan for five to ten minutes on the first run.

## 1. Open Phylax

Phylax runs as a Progressive Web App (PWA) directly in the browser, no app-store install required.

- URL: [https://astrapi69.github.io/phylax/](https://astrapi69.github.io/phylax/)
- Recommended: a recent Chrome, Firefox, Safari or Edge
- On a phone: use "Add to Home Screen" so Phylax behaves like a native app

The app loads from the network once and works offline afterwards. From the first click onward, your data does not leave the device.

## 2. Set your master password

On first launch you see the onboarding screen. You set your **master password**. Phylax derives the encryption key for all your profile data from this password.

Recommendations for a good master password:

- Long beats clever. A passphrase made of several words that means something to you is stronger than a short string of special characters.
- Use it only for Phylax. Recycled passwords from other services are the most common real-world weakness.
- Store it in a password manager or write it down somewhere safe.

!!! warning "Master password: your data's Achilles heel"

    Phylax does not know your master password. It is not stored
    anywhere, not on your device and not on any server. This is the
    reason your data is safe; it is also why there is no reset: there
    is nobody who could recover the password.

    If you forget your master password, every piece of data stored in
    Phylax is irrevocably lost. Even encrypted backups cannot be
    opened without the password.

    **This is the single most important thing you have to get right
    in Phylax.** Spend deliberate time on a strategy that fits you.

### Recommended strategies

Pick at least two of the following options, ideally three. A single backup is a backup that fails you when you actually need it.

#### Password manager (digital, most convenient)

A password manager stores your master password encrypted and syncs it across your devices. Options:

- **Locally encrypted:** Bitwarden (free, open-source), KeePass (file-based, full control), 1Password (commercial, very polished)
- **Browser-integrated:** Firefox Account, Chrome Passwords, Safari Keychain. Convenient but tied to your browser account.

If you use Phylax for data sovereignty, a self-hosted Bitwarden server (Vaultwarden) or KeePass with your own cloud sync fits the same posture best.

#### Private cloud / self-hosted solution

If you run your own Nextcloud, Synology NAS or similar, store your master password there in an encrypted notes tool (for example Joplin with end-to-end encryption, Standard Notes, or encrypted Markdown files). Advantage: your existing backup strategy for that cloud automatically protects the Phylax password too.

#### Physical note

Write the master password down and keep it in a safe place, not on the device itself, not in the wallet you carry every day. Examples: a safe, a lockable drawer, deposited with a trusted person, a safe deposit box. Multiple copies in different locations reduce the risk of total loss.

#### Emergency recovery plan

Decide who should get access to your master password in case of illness, death or accident. Write the instruction down together with your will, or leave it with an estate lawyer.

### What backups do NOT solve

Encrypted backups protect against:

- Device loss (broken laptop, lost phone)
- Accidental deletion
- File corruption

Encrypted backups do NOT protect against:

- A forgotten master password; the backup is encrypted with the same password
- Losing all your backup strategies at the same time

### A practical recommendation

Most Phylax users do well with this combination:

1. Master password stored in a password manager (for example Bitwarden with your own cloud sync)
2. A physical backup note in a safe place
3. Regular encrypted Phylax backups on a second device or in your private cloud (see [Backup creation and restoration](../backup/create-and-restore.md))

Together these three cover the most common scenarios: device loss, forgotten password, sync issues.

## 3. Create your profile

After the master password is set, Phylax asks whether you want to create a new profile or import an existing backup.

On a fresh start: **create a new profile**.

You enter a profile name, optionally date of birth or age and sex. That is enough to start. Every other field (weight, diagnoses, medications, context notes) can be filled in later.

## 4. Where your data lives

Phylax stores your profile encrypted in your browser's local database (IndexedDB). This means:

- Data stays on your device, inside your browser profile
- Switching browsers (for example Firefox to Chrome) means a different data store; you would import the backup
- Switching devices goes through the `.phylax` backup file (see [Backup creation and restoration](../backup/create-and-restore.md))
- Browser cleanup actions ("Clear cookies and site data") may also clear Phylax data, depending on browser settings

!!! info "iOS Safari"
    iOS Safari clears IndexedDB data for sites that are not added to the home screen after 7 days of inactivity. If you use Phylax on iPhone or iPad, add it to the home screen and use it at least weekly, or take regular backups.

## 5. Create your first observation

An **observation** is the smallest unit in Phylax. Three types are available: fact, pattern, self-regulation. For the first one, a fact is enough: for example "this morning 7:30 AM, headache on the right side, woke up with pressure".

Switch to the "Observations" view, create a new entry, choose type "Fact", write your text and save. With that, your profile is officially started.

## 6. Coming back later

When you reopen Phylax after a break, you see the unlock screen. Enter your master password; Phylax derives the key, decrypts your data, and you continue working.

After a stretch of inactivity (default: 5 minutes) Phylax locks itself and clears the key from memory. This is intentional: a forgotten tab in a cafe should not expose your data.

## Next steps

- Take a first backup once you have a few entries: [Backup creation and restoration](../backup/create-and-restore.md).
- Learn more about observations and their three types: [Observations](../daily-use/observations.md).
- For the thinking behind Phylax: [What is Phylax](what-is-phylax.md) and the article series Living Health, starting with [From Patient to Partner](https://asterios-raptis.medium.com/living-health-from-patient-to-partner-9fff311a8c45).

Status: 2026-04-27 (Iteration 1, first content)
