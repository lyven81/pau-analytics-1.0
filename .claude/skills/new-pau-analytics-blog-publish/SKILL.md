---
name: new-pau-analytics-blog-publish
description: Use when the user wants to publish a blog post draft to the Pau Analytics website (pauanalytics.com). Takes a Markdown draft from the blog/drafts/ folder, builds the HTML page, adds a card to the blog listing page, and pushes to GitHub. Trigger phrases: "publish blog post to pau analytics", "publish this blog draft", "add blog post to pau analytics", "publish the blog post".
---

# Pau Analytics Blog Publish Skill

This skill takes a completed Markdown draft from the `pau-analytics-blog-write` skill and publishes it to pauanalytics.com. It builds the HTML page, updates the blog listing page with a new card, and pushes both to the GitHub repo.

## Step Reference Files

| Step | What It Covers | File to Load |
|---|---|---|
| Step 1 | Gather inputs from the user — draft path, slug, date, language, case study slug | `references/step1-gather-inputs.md` |
| Step 2 | Read draft, build HTML page from template, add card to listing page | `references/step2-build-html.md` |
| Step 3 | Save files, commit, push to GitHub, confirm live URL | `references/step3-save-push.md` |

## Fixed Paths

| Item | Path |
|---|---|
| Blog post template | `C:\Users\Lenovo\pau-analytics-1.0\blog\template.html` |
| Blog listing page | `C:\Users\Lenovo\pau-analytics-1.0\blog\index.html` |
| Blog post output folder | `C:\Users\Lenovo\pau-analytics-1.0\blog\` |
| Drafts folder | `C:\Users\Lenovo\pau-analytics-1.0\blog\drafts\` |
| Repo root | `C:\Users\Lenovo\pau-analytics-1.0\` |
| Live blog base URL | `https://www.pauanalytics.com/blog/` |
| Live case study base URL | `https://www.pauanalytics.com/case-study/` |

## General Rules

- Follow steps in order. Do not skip ahead.
- Load the reference file for each step before starting that step.
- Do not fabricate content — use only what is in the draft file.
- Do not overwrite an existing file without warning the user first.
- Keep the user informed of which step you are on.
- Confirm with the user after each step before moving to the next.
- After pushing, always provide the live URL so the user can verify.

## How to Start

When the user provides a draft file path and asks to publish a blog post to Pau Analytics, immediately load `references/step1-gather-inputs.md` and begin Step 1.
