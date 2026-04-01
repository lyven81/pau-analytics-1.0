# User Guide — Coordinator Skill

This guide explains how to use the Coordinator skill in plain language. No technical knowledge needed.

---

## What This Skill Does

This skill is your weekly business check-in. Every Sunday, you run it and it tells you:

- What content was published this week
- Which LinkedIn posts went out
- How many leads came in and from which channel
- Which blog posts are driving leads
- What is planned for next week
- What you personally need to do before Monday

It saves the report to GitHub so you have a running record. It also gives you a plain-text version you can email to yourself.

---

## How to Start

Open Claude Code and say something like:

> "Run the weekly report."

or

> "Run the coordinator."

or

> "What happened this week?"

Claude will automatically detect this and start the workflow.

---

## What You Need to Prepare

Before running this skill, have your **leads data ready**. Claude will ask you for it during the skill.

You can provide it in one of three ways:

**Option A — Paste a summary (easiest)**
Open your Railway dashboard at `https://web-chat-lead-manager.railway.app`, look at this week's leads, and paste a short summary into Claude. For example:
> "3 new leads this week. 1 from CH-A, 2 from CH-B — both from the fixing-the-sales-leaks blog. Current pipeline: 3 New, 2 Qualifying, 1 Follow-up Sent."

**Option B — Share a CSV export**
If your Railway dashboard has an export button, download the CSV and tell Claude the file path.

**Option C — No leads yet**
If no leads have come in yet, just say: "No leads this week." Claude will note it in the report and move on.

---

## What Happens at Each Step

### Step 1 — Collect Data
Claude reads your GitHub commit history, your LinkedIn drafts folder, and your publish queue. Then it asks you for the leads data.

**What you need to do:** Provide the leads summary when Claude asks.

---

### Step 2 — Generate the Report
Claude writes the full weekly report — what was published, what leads came in, what is working, what is planned, and what you need to do.

**What you need to do:** Review the report and confirm it looks correct before it is saved.

---

### Step 3 — Save and Deliver
Claude saves the report to GitHub and gives you a Gmail-ready version to copy and send to yourself.

**What you need to do:** Copy the Gmail version and send it to yourself.

---

## What You Get at the End

- A weekly report saved to: `pau-analytics-1.0/reports/weekly/YYYY-WW.md`
- A plain-text version formatted for Gmail — copy and send to yourself
- A clear action list of what needs your attention before Monday

---

## When to Run This Skill

**Every Sunday evening** — takes about 5 to 10 minutes including the time to look up your leads data.

---

## Tips

- **If there are no leads yet**, that is fine — just say "no leads this week." The report will still cover publishing and LinkedIn activity.
- **If you forgot to check the dashboard**, run the skill anyway and enter "unknown" for leads. You can update the next week's report when you have the data.
- **The report history is in GitHub** — go to `pau-analytics-1.0/reports/weekly/` to see all past reports.
- **The action items section is the most important part** — read it first. It tells you exactly what you need to do.

---

## File Reference

| File | What It Is |
|---|---|
| `SKILL.md` | The main skill file — Claude reads this to know the workflow |
| `references/step1-read-data.md` | Instructions for collecting data from all sources |
| `references/step2-generate-report.md` | Instructions for writing the weekly report |
| `references/step3-save-send.md` | Instructions for saving to GitHub and preparing the Gmail version |
| `USER-GUIDE.md` | This file |

---

## Quick Reference

| Situation | What to Do |
|---|---|
| Running the weekly report | Say "run the coordinator" or "run the weekly report" |
| No leads data available | Say "no leads this week" when Claude asks |
| Report looks wrong | Tell Claude what to correct before confirming |
| Want to see a past report | Go to pau-analytics-1.0/reports/weekly/ on GitHub |
