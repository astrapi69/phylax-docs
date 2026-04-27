# Lab Values

Lab values in Phylax mirror how findings actually arrive in real life: one lab report per appointment, with many individual values inside. This two-tier structure (report plus values) keeps the data shaped the way the PDF presents it and makes later analysis across reports possible in the first place.

## Report and values

When you enter lab data into Phylax, you start by creating a **lab report**. The report carries the framing information:

- **Date (required):** When the report was issued. Reports sort by this date.
- **Lab (optional):** Which lab produced the report.
- **Doctor (optional):** Which physician ordered it.
- **Report number (optional):** If the PDF has a unique identifier.
- **Context (optional):** Why was the test done. Examples: "Routine primary-care check", "Thyroid follow-up after three months on medication".

Within that report you then add the individual **lab values**. For each value:

- **Category (required):** A free-form grouping like "Complete blood count", "Kidney panel", "Thyroid", "Vitamins".
- **Parameter (required):** What was measured, e.g. "Hemoglobin", "TSH", "Vitamin D".
- **Result (required):** The measured value, e.g. "13.7", "1:40", "<5", "positive". Free text because labs format results differently.
- **Unit (optional):** e.g. "g/dl", "ng/ml", "mg/l".
- **Reference range (optional):** As the lab states it, e.g. "13.5-17.5", "1:40", "<10".
- **Assessment (optional):** Your reading. Common values: "normal", "elevated", "low", "critical". Phylax suggests these four; you can also enter whatever fits the report.

## Why this split

A lab report rarely arrives alone. A blood draw comes back with twenty or fifty values, all sharing the same date, lab and reason. If Phylax treated each value separately, you would re-enter the date and lab twenty times. With report and values separated you fill the frame once and focus on the values themselves.

The separation also lets future trend analyses span multiple reports for the same parameter, once those analyses are built.

## Creating a report and values

In the "Lab values" section of the profile view.

1. Click **New report**.
2. Enter the date; optionally lab, doctor, report number, context.
3. Save. You land in the report detail view.
4. Inside the report, click **Add value**.
5. Pick a category (existing or new), then enter parameter, result, unit, reference range, assessment.
6. Save. The value appears immediately, grouped by category.
7. Repeat steps 4 to 6 for every value in the report.

On a phone it pays off to enter the report at a calm moment and to be aware of the auto-lock: after five minutes of inactivity Phylax locks itself. Long pauses during entry trigger a lock and unsaved input is lost.

## Assessment values

Phylax suggests four terms for the assessment field:

- **normal:** Within the reference range.
- **elevated:** Above the reference range.
- **low:** Below the reference range.
- **critical:** Far outside the range, requires immediate attention.

These are suggestions only because Phylax does not produce medical assessments itself. If a report uses different language ("within normal range", "noticeable"), you can take that over verbatim.

## Editing and deleting

Values and reports can be adjusted later, whether for a typo or because the lab issues a correction.

Deleting a report deletes all its values together. Phylax confirms before doing so. Individual values can be deleted on their own without touching the report.

## Phylax does not interpret

Important: Phylax will not tell you what a value means. If your TSH is slightly elevated, you do not hear that from Phylax. That conversation belongs with your physician. Phylax documents, sorts and keeps values findable across years; the assessment comes from a person with medical training.

The same applies during ePA import: the AI structures, it does not interpret. The value "TSH 4.8" is captured along with the PDF's reference range, but the question whether 4.8 is relevant for you stays with the appointment.

## Read more

- Capturing findings from PDF documents automatically: [ePA import](../data/epa-import.md).
- How observations and lab values relate (cross-references): [Observations](observations.md).
- Backing up your reports: [Backup creation and restoration](../backup/create-and-restore.md).

Status: 2026-04-27 (Iteration 1, first content)
