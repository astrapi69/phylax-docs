# FAQ

Common questions about Phylax. If your question is not here, take a look at [First Steps](getting-started/first-steps.md), [Observations](daily-use/observations.md) or the [Background](background.md) page.

## What happens if I forget my master password?

There is no reset and no recovery path. Phylax does not know your master password and stores it nowhere. If you forget it, every piece of data stored in Phylax becomes inaccessible. Encrypted backups are also unopenable without the password. This property is what makes Phylax safe against cloud breaches; it also makes the password itself the critical point. Set up a strategy from the start: see [First Steps: Master password](getting-started/first-steps.md#2-set-your-master-password).

## Are my data uploaded anywhere?

No. Phylax has no server of its own. All data lives encrypted in your browser (IndexedDB). There is no telemetry, no analytics, no advertising tracker. The single exception: when you use the optional AI assistant, your requests go directly from the browser to the provider you chose (OpenAI or Anthropic) using your own API key. Phylax acts only as a relay there, with no intermediate storage.

## Does Phylax work offline?

Yes. Phylax is a Progressive Web App that continues to work offline once loaded for the first time. Every edit, entry and view works without an internet connection. You only need a connection when the AI assistant is in use or when the app loads an update from the network.

## Can I use Phylax on multiple devices?

Yes, but without automatic sync. Each browser on each device has its own encrypted data store. To use Phylax on multiple devices, you export a `.phylax` backup on device A and import it on device B. Later edits on B will leave A behind on its older state until you transfer another backup. More on this in [Backup creation and restoration](backup/create-and-restore.md).

## How long does my data stay in the browser?

As long as you do not delete it and the browser does not evict it. Browsers can clear IndexedDB data under storage pressure or after long inactivity, especially on mobile. Phylax requests persistent storage when you set the master password (`navigator.storage.persist()`); if the browser grants this, your data is protected from automatic eviction. Even so, regular backups are not optional.

## What happens when iOS Safari clears IndexedDB after 7 days of inactivity?

iOS Safari clears IndexedDB data for sites that are not added to the home screen after 7 days of no use. If this happens, the data in that browser is gone. Two countermeasures: install Phylax via "Add to Home Screen" so it counts as an app (the eviction does not apply), and keep at least weekly backups in a second storage location.

## Does Phylax provide diagnoses or therapy recommendations?

Never. Phylax is a documentation and structuring platform, not a medical device. If you enter an elevated lab value, Phylax does not tell you what it means. The AI assistant also only structures, it does not interpret. Diagnoses, therapy decisions and medical assessments stay with your physician.

## Which data can Phylax import from physician documents?

With the AI assistant and your own API key, you can upload PDFs (referral letters, lab reports, ePA documents), and the assistant extracts observations, lab values and similar entries in structured form. You see a preview and decide what actually goes into the profile. The ePA import path is the most developed today (see [ePA import](data/epa-import.md)); other sources will follow in later iterations.

## How strong is the encryption?

Phylax uses AES-256-GCM to encrypt data and PBKDF2 with SHA-256 (1,200,000 iterations) to derive the encryption key from your master password. The key itself lives only in the browser's memory, never on disk. The threat model and architectural decisions are documented in the source repository: [github.com/astrapi69/phylax](https://github.com/astrapi69/phylax).

## Can I share Phylax with someone else?

One profile per browser, one master password per profile. Multi-profile support (several people or proxy care on one device) is planned as Phase 8 but not yet available. What you can already do today: maintain a proxy profile for someone else (see [Profile base data](daily-use/profile-base-data.md)).

## What if a backup will not import?

Three common causes:

- **Wrong master password.** Backups are encrypted with the password that was active when the backup was created. If you have changed it since, you need the old one to import.
- **Damaged file.** `.phylax` files must not be modified or renamed, or validation will fail. If the file went through a cloud sync that altered it, it may be damaged; prefer the original from your backup storage.
- **Wrong format.** Phylax backups end in `.phylax`. Markdown backups are restored via the profile import path, not the backup import.

Status: 2026-04-27 (Iteration 1, first content)
