# User Guide — Content Scheduler Skill

This guide explains how to use the Content Scheduler skill in plain language. No technical knowledge needed.

---

## What This Skill Does

This skill answers one question every week: **which case study should we turn into a blog post next?**

You have more than 40 case studies on pauanalytics.com. Only 10 have blog posts. This skill helps you work through the rest, one at a time, in a smart order — starting with the topics most relevant to your target audience.

It reads what has already been published, finds what has not, picks the best next topic, reads the case study, and prepares a ready-to-use brief for the blog writing skill.

---

## How to Start

Open Claude Code and say something like:

> "What should we publish next?"

or

> "Run the content scheduler."

or

> "Pick the next case study to blog about."

Claude will automatically detect this and start the workflow. You do not need to say "activate skill" or anything special.

---

## What Happens at Each Step

### Step 1 — Scan and Select

Claude reads your case study folder, checks which ones already have blog posts, and shortlists the best 3 options based on your target audience (Malaysian F&B, retail, and e-commerce SME owners).

**What you need to do:** Choose one of the 3 options — or tell Claude if you have a different topic in mind.

---

### Step 2 — Read Case Study and Write Queue

Claude reads the selected case study, extracts the key findings, and writes a publish-queue.md file. This file is the brief that the blog writing skill will use in the next step.

**What you need to do:** Confirm the brief looks right before Claude saves the file.

---

## What You Get at the End

- A `publish-queue.md` file saved to your website repo — ready for the blog writing skill to pick up
- An updated `publish-log.txt` so the same case study is never selected twice

---

## What to Do After This Skill Finishes

Run the blog writing skill next. Tell Claude:

> "Write a blog post from the publish queue at C:\Users\Lenovo\pau-analytics-1.0\publish-queue.md"

Claude will pick up the brief and write the full blog post from there.

---

## Tips

- **Run this skill once a week** — Monday morning is a good time, before the blog writing session
- **If you want a specific topic**, just tell Claude at the start: "I want to write about [topic]" and it will prioritise that
- **If the suggested options don't feel right**, say so — Claude will show more options from the full list
- **You don't need to run this skill if you already have a topic in mind** — you can go straight to the blog writing skill and tell Claude which case study to use

---

## File Reference

| File | What It Is |
|---|---|
| `SKILL.md` | The main skill file — Claude reads this to know the workflow |
| `references/step1-scan-select.md` | Instructions for scanning and selecting the next topic |
| `references/step2-write-queue.md` | Instructions for reading the case study and writing the queue file |
| `USER-GUIDE.md` | This file |

---

## Quick Reference

| Situation | What to Do |
|---|---|
| Starting a new week | Say "what should we publish next?" |
| You already have a topic in mind | Say "I want to write about [case study name]" |
| The 3 options don't look right | Say "show me more options" |
| Skipping this skill | Go straight to blog writing and name the case study yourself |
