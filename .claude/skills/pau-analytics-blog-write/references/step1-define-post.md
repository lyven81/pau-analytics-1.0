# Step 1 — Define the Post

## What This Step Does

Before writing anything, establish three things: the language, the target reader, and the angle. Getting these right means the post reaches the right person and says something they actually care about.

---

## 1A — Read the Source Material

Read whatever the user has provided:
- A CSV file path → read the file and summarise what the data contains
- An analyst report → read the key findings and conclusions
- A case study slug → fetch the case study from pauanalytics.com/case-study/[slug].html
- A topic or insight described in words → work from the description

Identify:
- What business problem does this dataset address?
- What did the analysis find?
- What should a business owner do differently based on this finding?

---

## 1B — Decide the Language

Load `references/bilingual-workflow.md` and apply the language decision rule:

| If the insight serves... | Write in... |
|---|---|
| Retail, F&B, trading, hawker businesses, traditional SMEs | Mandarin (中文) |
| Manufacturing, export, professional services, B2B | English |
| General / mixed audience | English first |

Present the language recommendation to the user with one sentence of reasoning. Confirm before proceeding.

---

## 1C — Define the Target Reader

Write one sentence describing the exact reader:
- Their role (e.g. retail shop owner, restaurant operator, factory manager)
- Their problem (e.g. losing customers without knowing why, unsure which products to stock)
- What they are hoping to learn

Example: "A F&B business owner who notices repeat customer numbers are dropping and wants to understand what's driving it before spending on promotions."

---

## 1D — Choose the Angle

The angle is the specific promise the post makes to the reader. It should be informational — answering a question a business owner would actually Google.

Generate 3 angle options based on the dataset findings. Format:

| Option | Angle | Search intent |
|---|---|---|
| A | [One-line angle — what the post answers] | [What the reader is Googling] |
| B | ... | ... |
| C | ... | ... |

Ask the user to pick one, or confirm the recommended option (mark it clearly).

---

## 1E — Draft the Post Title

Based on the confirmed angle, propose 3 title options:
- Each title should be 50–65 characters
- Include a keyword the target reader would search
- Avoid generic titles like "Understanding Data Analytics"

Example titles:
- "Why Your Best Customers Are Leaving — And How to Stop It"
- "哪些客户最可能不再回来？数据告诉你答案"
- "The Hidden Reason Your Restocking Decisions Are Costing You"

Ask the user to pick one or suggest changes.

---

## Step 1 Output Summary

Before moving to Step 2, confirm with the user:

| Item | Confirmed value |
|---|---|
| Language | EN or 中文 |
| Target reader | [one sentence] |
| Angle | [chosen angle] |
| Post title | [confirmed title] |
| Related case study slug | [slug for cross-link at end of post] |
| Draft filename | `[post-slug]-[YYYY-MM-DD].md` |
