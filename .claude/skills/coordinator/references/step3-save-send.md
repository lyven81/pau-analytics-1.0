# Step 3 — Save and Deliver the Report

---

## Sub-step 3A: Determine the Report Filename

Use this format:
`YYYY-WW.md` where WW is the ISO week number (zero-padded).

Example: Week 12 of 2026 → `2026-12.md`

---

## Sub-step 3B: Create the Reports Folder (if needed)

Check if the folder exists:
`C:\Users\Lenovo\pau-analytics-1.0\reports\weekly\`

If it does not exist, create it before saving.

---

## Sub-step 3C: Save the Report

Save the completed report (from Step 2) as a Markdown file:
`C:\Users\Lenovo\pau-analytics-1.0\reports\weekly\[YYYY-WW].md`

Use the plain text format from Step 2 — no HTML, no fancy formatting. Just the report content exactly as written.

---

## Sub-step 3D: Commit and Push to GitHub

Run from the repo root:

```
git -C "C:\Users\Lenovo\pau-analytics-1.0" add reports/weekly/[YYYY-WW].md
git -C "C:\Users\Lenovo\pau-analytics-1.0" commit -m "Add weekly report: Week [WW] [YYYY]"
git -C "C:\Users\Lenovo\pau-analytics-1.0" push
```

If the push fails, show the error to the user and do not retry automatically.

---

## Sub-step 3E: Display the Gmail-Ready Version

After a successful push, display the report again formatted for easy copy-paste into Gmail:

Tell the user:
> "Your weekly report has been saved and pushed to GitHub. Here is the Gmail-ready version — copy and paste this into a new email to yourself:"

Then display:

```
To: [user's own Gmail address]
Subject: Pau Analytics Weekly — Week [WW] [YYYY]

[Full report text — plain text, no markdown symbols like ** or ##]
[Replace all bold markers with plain text]
[Replace all section dividers with simple dashes or blank lines]
```

Remind the user:
> "Copy and paste the above into Gmail and send it to yourself. This keeps a readable record of your weekly progress."

---

## End of Step 3

Confirm completion:

> "Done. Weekly report saved at:
> reports/weekly/[YYYY-WW].md
>
> GitHub: https://github.com/lyven81/pau-analytics-1.0/blob/main/reports/weekly/[YYYY-WW].md
>
> Run this skill again next Sunday to generate the Week [WW+1] report."
