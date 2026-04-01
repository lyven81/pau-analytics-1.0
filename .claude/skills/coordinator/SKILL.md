---
name: coordinator
description: Use when the user wants a weekly business summary covering what was published, what LinkedIn posts went out, how many leads came in, which content is driving leads, and what is planned for next week. Generates a weekly report and saves it to GitHub. Trigger phrases: "run the weekly report", "generate the coordinator report", "what happened this week", "weekly business review", "run the coordinator".
---

# Coordinator Skill

This skill produces the weekly business intelligence report for Pau Analytics. It reads data from the publishing pipeline and the lead dashboard, connects publishing activity to lead outcomes, flags action items for the business owner, and saves the report to GitHub.

## Step Reference Files

| Step | What It Covers | File to Load |
|---|---|---|
| Step 1 | Collect data — publishing activity, LinkedIn posts, leads, next week's plan | `references/step1-read-data.md` |
| Step 2 | Generate the weekly report — correlate content to leads, flag actions | `references/step2-generate-report.md` |
| Step 3 | Save report to GitHub, display Gmail-ready version for the user | `references/step3-save-send.md` |

## Fixed Paths

| Item | Path |
|---|---|
| Pinnacles repo root | `C:\Users\Lenovo\pau-analytics-1.0\` |
| Blog folder | `C:\Users\Lenovo\pau-analytics-1.0\blog\` |
| LinkedIn drafts folder | `C:\Users\Lenovo\pau-analytics-1.0\blog\linkedin-drafts\` |
| Publish queue file | `C:\Users\Lenovo\pau-analytics-1.0\publish-queue.md` |
| Publish log file | `C:\Users\Lenovo\pau-analytics-1.0\publish-log.txt` |
| Weekly reports output folder | `C:\Users\Lenovo\pau-analytics-1.0\reports\weekly\` |
| Posted log file | `C:\Users\Lenovo\pau-analytics-1.0\blog\linkedin-drafts\posted-log.txt` |

## General Rules

- Follow steps in order. Do not skip steps.
- Load the reference file for each step before starting that step.
- Do not fabricate lead numbers — only use data the user provides or data readable from local files.
- If lead data is not available, note it clearly in the report rather than guessing.
- Keep the report factual and direct. No padding, no filler sentences.
- Always save the report before displaying the Gmail version.
- Keep the user informed of which step you are on.

## How to Start

When the user asks to run the weekly report or coordinator, immediately load `references/step1-read-data.md` and begin Step 1.
