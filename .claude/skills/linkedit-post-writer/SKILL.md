---
name: linkedit-post-writer
description: Use when the user wants to write a LinkedIn post from a Pau Analytics blog post. Reads the blog draft or published blog, extracts the key insight, and writes a ready-to-copy LinkedIn post in the same language as the blog (English or Mandarin). Trigger phrases: "write a linkedin post", "write a linkedit post", "write a linkedin post from this blog", "turn this blog into a linkedin post", "create a linkedin post from the draft", "write a social post for this blog".
---

# LinkedIn Post Writer Skill

This skill turns a written Pau Analytics blog post into a LinkedIn post. The LinkedIn post is not a summary — it is a teaser that gives enough insight to create curiosity, then directs the reader to the blog for the full answer.

## How This Skill Fits the Channel B Funnel

```
LinkedIn post  →  Blog post  →  WhatsApp
(this skill)      (already         (CTA at
                   written)       end of blog)
```

The LinkedIn post is the top of the funnel. Its only job is to earn the click to the blog.

## Step Reference Files

| Step | What It Covers | File to Load |
|---|---|---|
| Step 1 | Read the blog, identify the hook angle and key data point | `references/step1-read-blog.md` |
| Step 2 | Write the LinkedIn post — hook, insight, proof, CTA, hashtags | `references/step2-write-post.md` |
| Step 3 | Review against checklist, scrub weak phrases, confirm output | `references/step3-review.md` |

## Fixed Paths

| Item | Path |
|---|---|
| Blog drafts folder | `C:\Users\Lenovo\pau-analytics-1.0\blog\drafts\` |
| LinkedIn drafts output | `C:\Users\Lenovo\pau-analytics-1.0\blog\linkedin-drafts\` |
| Published blog base URL | `https://www.pauanalytics.com/blog/` |

## General Rules

- Follow steps in order. Do not skip ahead.
- Match the language of the LinkedIn post to the language of the blog (English blog → English post, Mandarin blog → Mandarin post).
- The LinkedIn post must never give away the full answer — it earns the click.
- Keep the user informed of which step you are on.
- Ask the user only when their input is genuinely needed (blog URL slug for the link). Do not ask unnecessary questions.
- After each step, briefly summarise what was done and confirm before moving on.

## How to Start

When the user provides a blog draft path or blog slug and asks to write a LinkedIn post, immediately load `references/step1-read-blog.md` and begin Step 1.

## User Guide

For plain-language instructions on how to use this skill and what to expect, read `references/user-guide.md`.
