# Step 1 — Gather Inputs

Before building anything, collect all required information from the user and the draft file.

---

## 1A — Read the Draft File

The user will provide a draft file path from the drafts folder, e.g.:
`C:\Users\Lenovo\pau-analytics-1.0\blog\drafts\why-customers-leave-2026-03-05.md`

Read the file and extract:

| Field | Where to find it |
|---|---|
| Post title | The H1 line (`# Title`) at the top of the draft |
| Post body | All content between the title and the SEO elements block |
| Meta description | From the SEO elements block at the end of the draft |
| Primary keyword | From the SEO elements block |
| URL slug | From the SEO elements block (e.g. `why-customers-leave`) |
| Language | From the SEO elements block (EN or ZH) |
| Date | From the SEO elements block |
| Related case study slug | From the SEO elements block or CTA block at the end |

If any of these fields are missing from the draft, ask the user to supply them before continuing.

---

## 1B — Confirm Inputs

Once extracted, confirm all values with the user before building anything:

> "Here is what I will publish:
>
> - **Title:** [post title]
> - **Slug:** [slug] → will save as `blog/[slug].html`
> - **Language:** [EN / 中文] → badge on card and post page
> - **Date:** [date]
> - **Meta description:** [meta description]
> - **Related case study:** [case-study-slug]
> - **Card description:** [1–2 sentence summary for the blog listing card]
>
> Is that correct? Type yes to continue or let me know what needs to change."

**Slug convention rule:** The blog post slug must match the related case study slug from the SEO elements block. Do not derive the slug from the post title. Always use the `Related case study slug` value as the blog post slug. If the user provides a slug that differs from the draft, use the user-provided value and flag the discrepancy.

**Card description:** If not present in the draft, write a 1–2 sentence plain-language summary of the post's main point. Keep it under 30 words. This appears on the blog listing card.

---

## 1C — Check for Existing File

Before proceeding, check whether `blog/[slug].html` already exists in the repo.

If it exists:
> "A file named `[slug].html` already exists in the blog folder. Do you want to overwrite it?"

Only proceed after the user confirms.

---

## Step 1 Output

Confirmed values to carry into Step 2:

| Field | Value |
|---|---|
| Draft file path | [path] |
| Post title | [title] |
| Post slug | [slug] |
| Language badge | EN or 中文 |
| Date (display format) | e.g. 5 March 2026 |
| Meta description | [150–160 chars] |
| Card description | [1–2 sentences, under 30 words] |
| Related case study slug | [slug] |
