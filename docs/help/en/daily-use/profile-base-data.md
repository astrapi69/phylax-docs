# Profile Base Data

The base data is the stable foundation of your profile: name, date of birth, sex, known diagnoses, current medications, relevant limitations. It changes less often than observations or open points and provides the frame inside which everything else makes sense. After three years of using the profile, this is the anchor.

## Which fields belong here

Base data currently includes:

- **Name:** What the profile should be called. For your own profile, your name or a short label; for a proxy profile, the name of the person you are caring for.
- **Date of birth:** ISO date. When present, it is always the better source than age.
- **Age:** Plain number. Useful only when the date of birth is unknown or deliberately not stored.
- **Sex:** Free text, not a closed dropdown. Examples: "female", "male", "diverse", "not specified".
- **Known diagnoses:** A list, one diagnosis per line. Examples: "Hashimoto's thyroiditis", "Migraine with aura", "Pollen allergy".
- **Current medications:** A list, regularly taken medications. This overlaps with the supplements area; the convention is: anything prescribed and not adjusted by you sits here, anything you steer yourself sits in supplements.
- **Relevant limitations:** A list, persistent limitations relevant for medical decisions. Examples: "Lactose intolerance", "Penicillin intolerance", "Contrast agent risk".

## Date of birth or age

If both are present, the date of birth wins. Phylax derives age from it where needed, and you do not have to update age every year by hand.

The age field still exists for three cases:

- For proxy profiles when the date of birth is unknown (for example an older relative with dementia, original birth certificate not available).
- When you do not want to store the exact date for privacy reasons.
- For a profile import that only carries age.

If you later add a date of birth, it overrides any previously entered age, because the date of birth is the more accurate source.

## Editing the profile

In the profile view, the "Base data" section has an **Edit profile** button. The click opens a form with all fields listed above.

1. Adjust fields.
2. Optionally enter a **reason for the change**. Examples: "Added new allergy after pollen season", "Hashimoto diagnosis from 14 March added".
3. Save.

On save, Phylax automatically creates a new profile-version entry.

## Profile versions

Every edit to the base data increases the profile version and adds an entry to the version history. This is not a background detail but an important feature:

- You can trace when you changed what.
- For medically relevant changes (new diagnosis, new allergy, discontinued medication), the version entry is your audit log.
- The **reason for the change** turns the entry from an anonymous timestamp into a meaningful note.

The version history itself lives in the profile's "Timeline" area (see that section once it gets its own page in a later iteration). Currently it is a list with date, version number and change reason.

## What is not in base data

The profile has additional fields that are not yet accessible through the same edit form in Phase 2:

- **Height and weight:** Currently importable, separate edit form to follow.
- **Primary care physician:** Name and contact, separate form planned.
- **Weight history:** Multiple values over time, separate edit to follow.
- **Context notes:** Free-form background text, separate form to follow.
- **External references and warning signs:** Will get their own edits over the course of Phase 2.

If these fields were present at profile import time, editing the base data leaves them untouched. Phylax does not overwrite them by accident.

## Own profile and proxy profile

Phylax knows two profile types:

- **Own profile (`self`):** You are the documented person.
- **Proxy profile (`proxy`):** You maintain the profile for someone else, for example a child or older relative. The **proxy for** field can record who.

The profile type is not part of the standard base-data edit form; it is set when a profile is created and rarely changes. Multi-profile per browser is planned for a later phase; currently one to two profiles are practical.

## Read more

- Keeping edits in sync across devices: [Backup creation and restoration](../backup/create-and-restore.md).
- Importing an existing profile from Markdown: [Importing a profile](../data/profile-import.md).
- [Observations](observations.md), [Lab values](lab-values.md), [Supplements](supplements.md) and [Open points](open-points.md) sit on top of the base data and use it as a frame.

Status: 2026-04-27 (Iteration 1, first content)
