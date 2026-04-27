# Supplements

The supplements section in Phylax documents what you take, regularly or as needed, and why. "Supplement" is read broadly here: vitamins, minerals, herbal preparations, over-the-counter products, and prescription medications when you want to see them next to the rest of your self-applied therapy. The list belongs to you, not to an app vendor.

## Fields of a supplement entry

- **Name (required):** What the package calls it. Example: "Magnesium glycinate", "Vitamin D3 + K2".
- **Category (required):** How regularly you take it (see below).
- **Brand (optional):** Manufacturer or product label. Useful when comparing brands or reordering.
- **Recommendation (optional):** When and how. Examples: "1 capsule, evening with water", "morning fasted, 2000 IU", "as needed, max 3x daily".
- **Rationale (optional):** Why you take it. Examples: "Improve sleep quality", "Suggested by primary care after low Vitamin D in February".

The optional fields are exactly that: optional. If a supplement needs no rationale, leave the field blank. But you will be glad for a short note in two years when you no longer remember why you started magnesium.

## The four categories

The category controls where the supplement shows up in your list and how you can manage the lifecycle.

- **Daily (`daily`):** You take it every day, without breaks. Examples: vitamin D in winter, thyroid hormone, long-term stable medications.
- **Regular (`regular`):** A fixed schedule, but not every day. Examples: "magnesium three times a week", "morning and evening separated".
- **On demand (`on-demand`):** Only for an acute reason. Examples: pain medication for a migraine, antihistamine during pollen season.
- **Paused (`paused`):** Currently inactive but not deleted. Examples: a supplement you have to stop for an upcoming test, a past recommendation whose effect you want to monitor.

The paused category matters. Phylax is a long-term record; what you tried and stopped six months ago is part of your picture. Pausing instead of deleting preserves the trail.

## Creating a supplement

In the "Supplements" section of the profile view.

1. Click **New supplement**.
2. Enter the name.
3. Choose the category.
4. Optionally add brand, recommendation, rationale.
5. Save.

## Editing and changing the category

A frequent action is moving entries between categories:

- A newly started daily supplement gets a test-stop after three months: switch the category to "Paused", later either back to "Daily" or to "On demand".
- An "On demand" supplement that you now need continuously moves to "Daily".

Editing happens from the detail view. All fields can be changed. The category change is the most common, so it is visible directly in the edit form.

## What Phylax does not do

Phylax is a record, not a coach.

- **No reminders.** Phylax does not remind you whether you took your supplement today. Adherence tracking is a different class of feature and not in scope here.
- **No interaction checks.** If you enter iron and magnesium together, Phylax does not warn about absorption interactions. That is medical advice and belongs with your physician or pharmacist.
- **No dosage suggestions.** Phylax records what you enter and shows it; it does not recommend "morning rather than evening" or "1000 IU rather than 2000 IU".

This restraint is deliberate. Phylax is meant to be your source of truth about your own therapy without interpreting it.

## Connection to other profile areas

Supplements often live in cross-references with observations and lab values:

- An observation "Sleep improved after starting magnesium" can point at the supplement in its cross-references field.
- A lab value "Vitamin D 22 ng/ml in February" can be the rationale for starting a new vitamin D supplement.

These cross-references are text, not clickable links; that is enough for human review over years and avoids brittle data-model coupling.

## Read more

- Documenting effect over time: [Observations](observations.md).
- Specific deficiencies and trends: [Lab values](lab-values.md).
- Cross-device maintenance of your list: [Backup creation and restoration](../backup/create-and-restore.md).

Status: 2026-04-27 (Iteration 1, first content)
