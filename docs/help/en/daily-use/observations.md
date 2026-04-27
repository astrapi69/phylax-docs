# Observations

Observations are the core of your Phylax profile. An observation captures what you notice about your body, the pattern it fits into, and how you respond to it. People with chronic conditions or long unresolved diagnostic processes know the problem: individual symptoms get lost, patterns over weeks get forgotten. Phylax observations solve this by holding each note in a small, complete shape.

## What an observation contains

Unlike a classical diary entry, an observation in Phylax consists of several named fields. Three of them are required and carry the core idea of "Living Health":

- **Observation (fact):** What you noticed. Be concrete. Example: "This morning 7:30 AM, headache on the right side, woke up with pressure."
- **Pattern:** What context this fits into. Example: "Has shown up several times in the past two weeks, always after nights shorter than six hours."
- **Self-regulation:** What you do in response. Example: "From today, sleep at least seven hours, try magnesium in the evening, re-evaluate in two weeks."

This three-part split is intentional. It forces thinking in loops ("what do I notice, what does it mean, what do I do about it") rather than in isolated symptom lists.

There are two more required fields for structure:

- **Theme:** A short heading that groups this observation with related ones. Examples: "Sleep", "Migraine", "Digestion", "Energy". Phylax sorts the list by theme, so consistency in wording pays off.
- **Status:** Where you are with this observation right now. Free text. Typical values: "under observation", "resolved", "recurring", "subsided".

Three optional fields complete the picture:

- **Medical finding:** What a doctor or a lab report said about this. If filled, the observation is anchored in external assessment; if empty, it is your own perception only.
- **Cross-references:** Links to other observations, lab values or life events. Example: "Correlates with histamine themes, see lab report from 14 March."
- **Extra fields:** Free-named additional fields for unusual structures that do not fit the standard grid.

## When to record an observation

Low threshold, high precision. Good moments:

- Something new you cannot place yet
- A repetition that is now happening for the third or fourth time
- A change after an adjustment (sleep, diet, supplement, therapy)
- A value or impression you do not want to forget at the next physician appointment

Seven days later such impressions are almost always gone. Writing the observation now is the only way to keep it usable for later.

## Creating an observation

In the profile view, the "Observations" section has the create button.

1. Enter **theme** (required). Keep wording consistent with existing themes; otherwise grouping splinters.
2. Describe **observation (fact)**. Concrete, with date or time if relevant.
3. Fill in **pattern**. What you suspect, what context this fits.
4. Note **self-regulation**. What you intend to do. If nothing concrete yet, write "wait and re-evaluate in two weeks". Avoid leaving it empty.
5. Set **status**.
6. Add optional fields if relevant.
7. Save.

The observation appears in the list immediately, sorted by theme and within the theme by creation date.

## Editing and deleting

Observations are not frozen. In the detail view you can edit any entry and adjust all fields. Each change is saved with an updated timestamp, and the profile gets a new version on top (see [Profile base data](profile-base-data.md)).

Deletion is permanent. Delete an observation only if it was actually wrong. For "this happened but I no longer find it relevant", setting the status to "resolved" or "subsided" is the better path because the history stays intact.

## Source (provenance)

Every observation carries a **source** field showing where it came from:

- **Yourself:** Manually entered.
- **AI:** Extracted by the AI assistant from a finding or an input (see ePA import).
- **Doctor:** Carried over from a physician document (referral letter, lab report).

The source persists even when you edit the observation later. An AI observation that you refine stays marked as AI source; the edit is logged in the profile version history.

## Tips for usable observations

- Be specific. "Headache on the right side, pressure, woke up around 7:30 AM" helps two months later much more than "head hurt".
- Keep the theme short. One to three words is enough. Long themes fragment the grouping.
- Write pattern and self-regulation even when they are only hypotheses. A weak hypothesis is better than none because you can revise or discard it later.
- Use extra fields when the standard grid does not fit. Better a dedicated "sleep duration" field than cramming numeric data into prose.

## Read more

- Turning physician documents into observations automatically: [ePA import](../data/epa-import.md).
- Carrying your observations across devices: [Backup creation and restoration](../backup/create-and-restore.md).
- Conceptual background on the fact-pattern-self-regulation split: the article series "Living Health", starting with [From Patient to Partner](https://asterios-raptis.medium.com/living-health-from-patient-to-partner-9fff311a8c45).

Status: 2026-04-27 (Iteration 1, first content)
