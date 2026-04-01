---
name: check-leads
description: Use when the user wants to check for new leads, review the lead pipeline, or draft WhatsApp follow-up messages. Reads lead data from the Web Chat Lead Manager API, prioritizes by urgency, and drafts personalized follow-up messages. Trigger phrases: "check leads", "any new leads", "check the lead dashboard", "draft follow-ups", "who needs follow-up", "check my leads".
---

# Check Leads Skill

This skill reads lead data from the Web Chat Lead Manager, identifies leads that need attention, and drafts WhatsApp follow-up messages with personalized openers.

## Step Reference Files

| Step | What It Covers | File to Load |
|---|---|---|
| Step 1 | Read leads from API, filter and prioritize | `references/step1-read-leads.md` |
| Step 2 | Draft follow-up messages for leads needing attention | `references/step2-draft-followups.md` |

## Fixed Paths

| Item | Path |
|---|---|
| Web Chat Lead Manager API | `http://localhost:8000` (or Railway URL if deployed) |
| Brand voice guidelines | `C:\Users\Lenovo\Documents\Pau Analytics\Foundation - Who we are\brand-voice-guidelines.md` |

## General Rules

- Follow steps in order.
- Load the reference file for each step before starting that step.
- Never fabricate lead data — only use what the API returns.
- If the API is unreachable, tell the user to start the Web Chat Lead Manager first.
- All follow-up messages must match the brand voice: warm, practical, no jargon.
- High-urgency leads (score 4-5) should be flagged prominently.

## How to Start

When the user says "check leads", "any new leads", or anything about reviewing leads or drafting follow-ups, load `references/step1-read-leads.md` and begin Step 1.
