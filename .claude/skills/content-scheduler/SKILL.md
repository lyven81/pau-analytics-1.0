---
name: content-scheduler
description: Use when the user wants to select the next case study to write a blog post about. Reads all case studies on pauanalytics.com, cross-checks against published blogs, and produces a publish-queue.md file that tells the blog writing skill exactly what to produce next. Trigger phrases: "what should we publish next", "select the next case study", "run the content scheduler", "pick the next blog topic", "what case study should we blog about".
---

# Content Scheduler Skill

This skill selects the next case study to turn into a blog post. It reads what has already been published, finds what has not, applies priority rules, and writes a publish-queue.md file that the blog writing pipeline picks up next.

## Step Reference Files

| Step | What It Covers | File to Load |
|---|---|---|
| Step 1 | Scan case studies, cross-check against published blogs, select next topic | `references/step1-scan-select.md` |
| Step 2 | Read selected case study, extract content, write publish-queue.md | `references/step2-write-queue.md` |

## Fixed Paths

| Item | Path |
|---|---|
| Case study folder | `C:\Users\Lenovo\pau-analytics-1.0\case-study\` |
| Blog index page | `C:\Users\Lenovo\pau-analytics-1.0\blog\index.html` |
| Publish queue file | `C:\Users\Lenovo\pau-analytics-1.0\publish-queue.md` |
| Publish log file | `C:\Users\Lenovo\pau-analytics-1.0\publish-log.txt` |
| Pau Analytics case study base URL | `https://www.pauanalytics.com/case-study/` |

## Priority Rules

When selecting the next case study, apply these rules in order:

1. Never select a case study already listed in `publish-log.txt`
2. Prefer topics relevant to F&B, retail, or e-commerce (Pau Analytics target audience)
3. Prefer English topics first — aim for no more than 1 in every 3 posts in Mandarin
4. If the user has stated a preferred topic or theme, apply that first
5. If multiple case studies are equally valid, present the top 3 for the user to choose from

## General Rules

- Follow steps in order. Do not skip steps.
- Load the reference file for each step before starting that step.
- Always check publish-log.txt before making a selection — never repeat a case study.
- Always present the selection to the user for confirmation before writing the queue file.
- Keep the user informed of which step you are on.
- After each step, briefly summarise what was done and confirm before moving on.

## How to Start

When the user asks what to publish next or asks to run the content scheduler, immediately load `references/step1-scan-select.md` and begin Step 1.
