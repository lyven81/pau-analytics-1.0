---
name: pau-analytics-blog-write
description: Use when the user wants to write a blog post for the Pau Analytics website (pauanalytics.com) from a dataset, analyst report, or business insight. Covers language selection, post angle, full article writing with SEO structure, and quality review. Output is a Markdown draft saved to drafts/. Trigger phrases: "write a blog post", "write a pau analytics blog", "write a post from this dataset", "write a blog post in mandarin", "write a blog post in english", "draft a blog post for pau analytics".
---

# Pau Analytics Blog Write Skill

This skill writes a complete, publish-ready blog post for the Pau Analytics blog. The post is written for Malaysian SME business owners — in English or Mandarin — and is structured to drive organic search traffic and lead readers into the related case study.

## Step Reference Files

| Step | What It Covers | File to Load |
|---|---|---|
| Step 1 | Decide language, identify audience and angle from dataset or report | `references/step1-define-post.md` |
| Step 2 | Write the full blog post — hook, structure, mini-stories, CTAs, cross-link | `references/step2-write-post.md` |
| Step 3 | Review quality, check against checklist, scrub AI patterns | `references/step3-review-scrub.md` |

## Fixed Paths

| Item | Path |
|---|---|
| Bilingual workflow rules | `references/bilingual-workflow.md` |
| Blog post template | `C:\Users\Lenovo\pau-analytics-1.0\blog\template.html` |
| Draft output folder | `C:\Users\Lenovo\pau-analytics-1.0\blog\drafts\` |

## General Rules

- Follow steps in order. Do not skip ahead.
- Load the reference file for each step before starting that step.
- Always read `references/bilingual-workflow.md` before deciding the language for any post.
- Write natively in the chosen language — do not translate from one to the other.
- Mandarin standard: 马来西亚华语 — not Simplified Chinese written for a China audience.
- Keep the user informed of which step you are on.
- Ask the user only when their input is genuinely needed (language confirmation, related case study slug). Do not ask unnecessary questions.
- After each step, briefly summarise what was done and confirm before moving on.
- Never run code yourself. If code is needed, generate it and instruct the user to run it.

## How to Start

When the user provides a dataset, analyst report, or topic and asks to write a blog post, immediately load `references/step1-define-post.md` and begin Step 1.
