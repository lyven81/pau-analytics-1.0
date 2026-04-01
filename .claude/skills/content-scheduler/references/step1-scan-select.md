# Step 1 — Scan and Select

Work through each sub-step in order. Do not write the queue file until the user confirms the selection at the end of this step.

---

## Sub-step 1A: Read the Publish Log

Read `C:\Users\Lenovo\pau-analytics-1.0\publish-log.txt`.

If the file does not exist, note that no case studies have been scheduled yet and continue. Create the file at the end of Step 2.

Extract the list of case study slugs that have already been scheduled. These must not be selected again.

---

## Sub-step 1B: Read the Case Study Folder

List all `.html` files in `C:\Users\Lenovo\pau-analytics-1.0\case-study\`.

Exclude: `generate_cases.py` and any non-HTML files.

Produce a clean list of case study slugs (filename without `.html`).

---

## Sub-step 1C: Read the Blog Index

Read `C:\Users\Lenovo\pau-analytics-1.0\blog\index.html`.

Extract all blog post slugs that are already published. Look for `href` links pointing to blog post HTML files in the blog folder.

---

## Sub-step 1D: Cross-Reference

Compare the case study slug list against:
1. The blog index slugs (blogs already written)
2. The publish log slugs (cases already scheduled)

Produce a clean list of case studies that have no blog yet and have not been scheduled. These are the eligible candidates.

---

## Sub-step 1E: Apply Priority Rules

From the eligible candidates, apply the following rules:

**Rule 1 — Audience relevance first**
Prioritise case studies whose topics are relevant to Malaysian F&B, retail, or e-commerce SME owners. Examples of relevant topics: sales, customers, products, pricing, revenue, staff, inventory, outlet performance, seasonal trends. Flag any that are clearly out of scope (e.g. heavy industrial, academic datasets).

**Rule 2 — Language balance**
Check the last 3 entries in publish-log.txt. If the last 2 were English, a Mandarin topic can be considered next. If the last entry was Mandarin, prefer English next. If publish-log.txt is empty, start with English.

**Rule 3 — User preference**
If the user mentioned a preferred theme or industry when starting the session, elevate those topics to the top regardless of other rules.

---

## Sub-step 1F: Present Top 3 Options

Present exactly 3 case study options to the user. For each one, include:

- Case study slug (filename)
- Suggested blog angle in one sentence (what insight could this become for an SME owner?)
- Recommended language: English or Mandarin
- Why it ranked in the top 3

Format example:
```
Option 1: not-all-shoppers-are-equal
Angle: How to identify your most valuable customer segments and focus on them.
Language: English
Why: Strong F&B/retail relevance. No blog yet. Last 3 posts were English — language balance is fine.

Option 2: what-causes-product-returns
Angle: What drives returns in your business and how to reduce them.
Language: English
Why: Relevant to retail and e-commerce. Clear problem angle for SME owners.

Option 3: selling-the-right-products (Mandarin angle)
Angle: 哪些产品真正为你赚钱？
Language: Mandarin
Why: Core retail topic. Existing English blog published — a Mandarin version serves a different audience.
```

Then ask the user:
> "Which of these three would you like to schedule next? Or would you prefer a different case study from the list?"

Wait for confirmation before loading `references/step2-write-queue.md`.

---

## End of Step 1

Confirm the selected case study slug and language with the user before proceeding:
> "Confirmed: [slug] in [language]. Moving to Step 2 — reading the case study and writing the publish queue."
