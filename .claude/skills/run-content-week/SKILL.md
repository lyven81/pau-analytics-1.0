---
name: run-content-week
description: Use when the user wants to produce all weekly marketing content in one run. Chains content-scheduler, blog-write, blog-publish, and linkedin-post-writer for Pau Analytics, then generates Pau AI LinkedIn posts from solution templates. Produces 1 blog post + 4 LinkedIn drafts. Trigger phrases: "run content week", "produce this week's content", "generate weekly content", "run the content pipeline", "run marketing".
---

# Run Content Week Skill

This skill produces all weekly marketing content for Pau Analytics and Pau AI in a single run. It chains existing skills for the blog pipeline and generates standalone LinkedIn posts for Pau AI.

## Step Reference Files

| Step | What It Covers | File to Load |
|---|---|---|
| Step 1 | Run the Pau Analytics blog pipeline (content-scheduler → blog-write → blog-publish → linkedin teaser) | `references/step1-blog-pipeline.md` |
| Step 2 | Write a standalone Pau Analytics insight post (no blog needed) | `references/step2-insight-post.md` |
| Step 3 | Write a Pau AI solution showcase post | `references/step3-solution-post.md` |
| Step 4 | Write a Pau AI use case spotlight post | `references/step4-usecase-post.md` |

## Fixed Paths

| Item | Path |
|---|---|
| LinkedIn drafts output | `C:\Users\Lenovo\pau-analytics-1.0\blog\linkedin-drafts\` |
| Case study folder | `C:\Users\Lenovo\pau-analytics-1.0\case-study\` |
| Publish queue | `C:\Users\Lenovo\pau-analytics-1.0\publish-queue.md` |
| Publish log | `C:\Users\Lenovo\pau-analytics-1.0\publish-log.txt` |
| Pau AI templates | `C:\Users\Lenovo\Documents\Pau AI\template\` |
| Pau AI showcase log | `C:\Users\Lenovo\pau-analytics-1.0\pau-ai-showcase-log.txt` |
| Next week plan | `C:\Users\Lenovo\pau-analytics-1.0\next-week-plan.md` |
| Brand voice guidelines | `C:\Users\Lenovo\Documents\Pau Analytics\Foundation - Who we are\brand-voice-guidelines.md` |
| Campaign plan | `C:\Users\Lenovo\Documents\Pau Analytics\Strategy - How we plan\campaign-plan.md` |

## General Rules

- Follow steps in order. Do not skip steps.
- Load the reference file for each step before starting that step.
- If `next-week-plan.md` exists, read it first — the coordinator may have recommended a specific topic or angle. Follow the recommendation unless the user overrides.
- Read `brand-voice-guidelines.md` before writing any LinkedIn post — all posts must follow the brand voice.
- All LinkedIn posts must be 150–250 words.
- Save all LinkedIn drafts as plain text files in the linkedin-drafts folder.
- After all 4 steps, display a summary of everything produced.

## How to Start

When the user says "run content week", "produce this week's content", or anything that conveys they want to generate all weekly marketing content, read `next-week-plan.md` (if it exists) and `brand-voice-guidelines.md`, then load `references/step1-blog-pipeline.md` and begin Step 1.
