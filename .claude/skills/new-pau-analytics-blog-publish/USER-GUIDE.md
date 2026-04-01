# User Guide — Pau Analytics Blog Publish Skill

This guide explains how to use this skill in plain language. No technical knowledge needed.

---

## What This Skill Does

This skill takes a completed blog post draft (written by the `pau-analytics-blog-write` skill) and publishes it to the Pau Analytics website. It handles everything: building the HTML page, adding a card to the blog listing page, and pushing both to GitHub.

You do not need to write HTML. You do not need to touch git manually. Just provide the draft file and confirm a few details.

---

## How to Start

After finishing a blog post draft, open Claude Code and say:

> "Publish this blog post to Pau Analytics: C:\Users\Lenovo\pau-analytics-1.0\blog\drafts\why-customers-leave-2026-03-05.md"

Or simply:

> "Publish the blog draft to Pau Analytics"

Claude will detect the skill and start the workflow automatically.

---

## What Happens at Each Step

### Step 1 — Gather Inputs
Claude reads your draft file and extracts the title, slug, language, date, meta description, and related case study slug. It confirms everything with you before building anything.

**What you need to do:** Review the confirmed values. Correct anything that looks wrong — especially the related case study slug, since this is what the "See the Full Case Study" link at the bottom of the post will point to.

---

### Step 2 — Build the HTML
Claude converts the Markdown draft to a complete HTML page using the blog post template. It also prepares a new card for the blog listing page.

**What you need to do:** Review the summary of what will be saved. Type yes to confirm.

---

### Step 3 — Save and Push
Claude saves both files and pushes to GitHub. The blog post page and the updated listing page go live within 1–2 minutes.

**What you need to do:** Check the live URLs after the push to confirm everything looks right.

---

## Things to Prepare Before You Start

- The draft file path — e.g. `C:\Users\Lenovo\pau-analytics-1.0\blog\drafts\[filename].md`
- The draft must already have passed the quality review in Step 3 of the `pau-analytics-blog-write` skill
- For Mandarin posts: confirm you have completed a human review of the CTA and conclusion before running this skill

---

## What You Get at the End

1. A **live blog post page** at `https://www.pauanalytics.com/blog/[slug].html`
2. An **updated blog listing page** at `https://www.pauanalytics.com/blog/` — with the new post card at the top
3. The new card is automatically filterable by language (English / 中文) on the listing page

---

## Tips

- **If the push fails**, copy the error message and share it with Claude — do not retry the push yourself
- **If the card description is missing from the draft**, Claude will write a short one based on the post content — review it before confirming
- **If you want a second-language version** of the same post, use the `pau-analytics-blog-write` skill again with the same dataset and select the other language

---

## Full Workflow Reference

This skill is the second half of the blog publishing workflow:

```
pau-analytics-blog-write       →   new-pau-analytics-blog-publish
(write + review the draft)         (build HTML + publish to GitHub)
```

The complete content workflow from dataset to live blog post:

```
analyst-report skill           →   pau-analytics-blog-write skill   →   new-pau-analytics-blog-publish skill
(analyse data, write report)       (write blog post draft)               (build HTML + publish)
```

---

## File Reference

| File | What It Is |
|---|---|
| `SKILL.md` | Main skill file — Claude reads this to activate the workflow |
| `references/step1-gather-inputs.md` | Step 1 instructions — extract and confirm inputs |
| `references/step2-build-html.md` | Step 2 instructions — convert Markdown to HTML, build card |
| `references/step3-save-push.md` | Step 3 instructions — save files, push, confirm live URL |
| `USER-GUIDE.md` | This file |

---

## Quick Reference Card

| Situation | What to Do |
|---|---|
| Starting the publish | Provide the draft file path and say you want to publish to Pau Analytics |
| Wrong case study slug | Correct it in Step 1 before confirming |
| Push fails | Share the error message with Claude |
| Post not appearing on site | Wait 1–2 minutes then refresh — GitHub Pages takes a moment |
| Want a Mandarin version too | Run `pau-analytics-blog-write` again with same dataset, select 中文 |
