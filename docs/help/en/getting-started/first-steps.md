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

!!! warning "Phylax cannot reset your master password"
    Phylax does not know your password. It is not stored anywhere, not on your device and not on any server. If you forget it, your encrypted data becomes inaccessible. There is a Reset function, but it wipes everything and starts from zero. This same property is what makes Phylax safe against cloud breaches; it also makes the master password the critical point.

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
