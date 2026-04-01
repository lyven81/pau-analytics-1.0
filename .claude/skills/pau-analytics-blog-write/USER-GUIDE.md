# User Guide — Pau Analytics Blog Write Skill

This guide explains how to use this skill in plain language. No technical knowledge needed.

---

## What This Skill Does

This skill writes a complete blog post for the Pau Analytics website from a dataset, analyst report, or business insight. It handles everything: choosing the language, defining the angle, writing the full post, and checking quality before handing off to the publish skill.

You do not need to write anything yourself. You provide the source material and make a few decisions. Claude does the rest.

---

## How to Start

Open Claude Code and say something like:

> "Write a blog post for Pau Analytics from this dataset: C:\Users\...\data.csv"

> "Write a Mandarin blog post for Pau Analytics based on the reseller case study"

> "Write a blog post from the analyst report I just finished"

Claude will detect this and start the workflow automatically.

---

## What Happens at Each Step

### Step 1 — Define the Post
Claude reads your source material and figures out:
- What language to write in (English or Mandarin) — based on who the insight serves
- Who the target reader is
- What angle to take (the specific question the post answers)
- What the post title should be

**What you need to do:** Confirm the language, pick an angle from 3 options, and approve the title. Also provide the related case study slug so the post can link to it at the end.

---

### Step 2 — Write the Post
Claude writes the full blog post with:
- A hook opening (not a generic definition)
- Proper H2/H3 heading structure
- Data-backed points from your dataset
- 2–3 mini-stories with specific scenarios
- A conclusion with key takeaways
- A CTA block linking to the related case study
- SEO elements (meta title, meta description, keyword, URL slug)

The draft is saved as a Markdown file to:
`C:\Users\Lenovo\pau-analytics-1.0\blog\drafts\`

**What you need to do:** Review the draft. Tell Claude if anything needs changing.

---

### Step 3 — Review and Scrub
Claude checks the draft against a quality checklist and removes AI writing patterns (em-dashes, filler phrases, robotic constructions) before signing off.

**What you need to do:**
- For English posts: a light read-through is enough
- For Mandarin posts: do a close review of the CTA text and conclusion before publishing — Claude will flag this

---

## Things to Prepare Before You Start

- Your source material: a CSV file path, analyst report file, or case study URL
- Know roughly which industry the insight serves (retail, F&B, B2B, etc.) — this helps decide the language
- The slug of the related case study (e.g. `know-your-reseller`) so the post can link to it

---

## What You Get at the End

By the time the skill is done, you will have:

1. A **complete blog post draft** in Markdown — structured, SEO-ready, bilingual-appropriate
2. A **SEO elements block** — meta title, meta description, primary keyword, URL slug
3. A **CTA block** linking to the related case study
4. A **quality sign-off** — checklist passed, AI patterns removed

The draft is then ready to pass to the `new-pau-analytics-blog-publish` skill which builds the HTML page and publishes it to the blog.

---

## Tips

- **If you are unsure which language to use**, let Claude recommend — just describe who the insight is for
- **If the angle options don't feel right**, say so and describe the angle you have in mind
- **For Mandarin posts**, always do a human review of the CTA and conclusion before publishing
- **To write multiple posts from the same dataset**, start a fresh session for each post — the skill always starts from Step 1

---

## Full Workflow Reference

This skill is Step 1 of the blog publishing workflow:

```
pau-analytics-blog-write   →   new-pau-analytics-blog-publish
(this skill — write draft)      (next skill — build HTML + push to GitHub)
```

---

## File Reference

| File | What It Is |
|---|---|
| `SKILL.md` | Main skill file — Claude reads this to activate the workflow |
| `references/bilingual-workflow.md` | Language decision rules — loaded at Step 1 |
| `references/step1-define-post.md` | Step 1 instructions — language, angle, title |
| `references/step2-write-post.md` | Step 2 instructions — full writing methodology |
| `references/step3-review-scrub.md` | Step 3 instructions — quality checklist and AI scrub |
| `USER-GUIDE.md` | This file |

---

## Quick Reference Card

| Situation | What to Do |
|---|---|
| Starting a new blog post | Provide the source material and say you want to write a blog post for Pau Analytics |
| Unsure about language | Describe the target audience — Claude will recommend |
| Don't like the angle options | Say so and describe the angle you want |
| Mandarin post is done | Do a human review of CTA and conclusion before publishing |
| Ready to publish | Pass the draft file path to `new-pau-analytics-blog-publish` skill |
