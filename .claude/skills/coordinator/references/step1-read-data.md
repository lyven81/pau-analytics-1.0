# Step 1 — Collect Data

Work through each sub-step in order. Collect all available data before moving to Step 2. If a data source is unavailable, note it clearly — do not guess or fabricate numbers.

---

## Sub-step 1A: Determine the Report Week

Identify the reporting week:
- Start date: last Monday
- End date: last Sunday
- Format as: Week [WW] YYYY (e.g. Week 12 2026, 16–22 Mar 2026)

---

## Sub-step 1B: Read Publishing Activity

Run this git command from the repo root to get commits from the past 7 days:

```
git -C "C:\Users\Lenovo\pau-analytics-1.0" log --since="7 days ago" --oneline --no-merges
```

From the commit messages, extract:
- Blog posts published (look for "Add blog post:" in commit messages)
- Case studies published (look for "Add case study:" in commit messages)
- Any other content pushes

If no commits in the past 7 days, note: "No content published this week."

---

## Sub-step 1C: Read LinkedIn Post Activity

Read the `/blog/linkedin-drafts/` folder:
`C:\Users\Lenovo\pau-analytics-1.0\blog\linkedin-drafts\`

Count:
- `.txt` files — drafted but not yet posted
- `.posted.txt` files — already published to LinkedIn

Read `posted-log.txt` if it exists. Extract:
- Which slugs were posted this week (check the date column)
- Total posts published to date

If posted-log.txt does not exist yet, note: "LinkedIn posting has not started yet."

Note: LinkedIn posts are scheduled via Buffer. The `.posted.txt` rename and `posted-log.txt` update are done manually by the user after each post goes live. If these have not been updated, ask the user: "Has any LinkedIn post gone out this week? If yes, which slug?" and record the answer.

---

## Sub-step 1D: Read the Publish Queue

Read `C:\Users\Lenovo\pau-analytics-1.0\publish-queue.md`.

Extract:
- Next scheduled case study slug and language
- Scheduled date

If the file does not exist, note: "No content is queued for next week yet. Run the content-scheduler skill to set the next topic."

---

## Sub-step 1E: Read the Publish Log

Read `C:\Users\Lenovo\pau-analytics-1.0\publish-log.txt`.

Calculate:
- Total case studies scheduled to date
- How many case studies remain (total case studies in folder minus scheduled)
- Estimated weeks of content remaining at current pace

---

## Sub-step 1F: Collect Lead Data

Ask the user:

> "To complete the weekly report, I need this week's lead data from the Railway dashboard. Please provide one of the following:
>
> Option A — Paste a summary: total leads this week, how many from CH-A, CH-B, and CH-W, and which blog slugs appeared in CH-B leads.
>
> Option B — Share the downloaded CSV export from your Railway dashboard and I will read it.
>
> Option C — If there are no leads yet, just say 'no leads this week' and I will note it."

Wait for the user's response before continuing.

Once received, extract and record:
- Total new leads this week
- Leads by channel: CH-A, CH-B, CH-W
- Blog slugs that generated CH-B leads (if any)
- Leads currently at each status: New, Qualifying, Qualified, Follow-up Sent, Closed, Lost
- Leads at "New" status for more than 24 hours (flag these as needing follow-up)

---

## End of Step 1

Summarise all data collected:
- Publishing activity (what was published)
- LinkedIn activity (what was posted)
- Next week's queue
- Lead summary

Then say:
> "Data collected. Moving to Step 2 — generating the weekly report."

Load `references/step2-generate-report.md`.
