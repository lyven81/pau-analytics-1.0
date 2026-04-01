# Step 4 — Pau AI Use Case Spotlight Post (Friday)

This step writes a LinkedIn post zooming into one specific use case within a Pau AI solution category.

---

## 4A: Pick a Use Case

Read the same solution category used in Step 3 (or a different one if the user prefers).

Inside the category folder, find the use-case subfolders. Each subfolder contains a `config.yaml` with business-specific details.

Pick a use case that:
1. Has NOT been spotlighted before (check `pau-ai-showcase-log.txt` for entries with `usecase-spotlight` type)
2. Is relatable to a Malaysian SME owner (prefer F&B, service, retail)

Read the use case's `config.yaml` to extract:
- Business type and name
- Services/products offered with pricing
- Specific operational details (hours, capacity, staff)

---

## 4B: Write the Post

Write a LinkedIn post (150–250 words) as a micro-story:

1. **Hook (lines 1–2):** Paint the business owner's daily pain in one sentence.
   - Good: "Ahmad runs a plumbing business with 3 workers. Every missed call during a job is a lost customer."
   - Weak: "AI can help service businesses."
2. **The scenario (1 paragraph):** Describe what happens when a customer contacts the business — without the AI, it's a mess. With the AI, it's handled.
3. **What the AI does (2–3 bullet points):** Specific actions, pulled from config.yaml.
   - Example: "Quotes RM180 for a leaking pipe fix within 5 seconds"
   - Example: "Books Saturday 9am, confirms via WhatsApp, sends reminder Friday evening"
4. **The outcome (1 sentence):** What changes for the business owner.
5. **CTA:** "See how it works: [demo URL]"
6. **Hashtags:** 3–5 relevant. Always include #AI #MalaysianSME.

Tone: storytelling, grounded, specific. Use the business owner's name from config.yaml. Make it feel like a real scenario, not a feature list.

---

## 4C: Save and Log

Save the post:
- Location: `C:\Users\Lenovo\pau-analytics-1.0\blog\linkedin-drafts\`
- Filename: `pau-ai-usecase-[category]-[usecase]-[YYYY-MM-DD].txt`

Append to `C:\Users\Lenovo\pau-analytics-1.0\pau-ai-showcase-log.txt`:
```
[YYYY-MM-DD] | [category]/[usecase] | usecase-spotlight
```

---

## End of Step 4

Display a full summary of everything produced this week:

```
Weekly Content Summary
═══════════════════════════════════════

BLOG (published to pauanalytics.com):
  [slug] — [language]

LINKEDIN DRAFTS (ready to paste):
  Monday  : [blog-teaser-filename]     — Pau Analytics blog teaser
  Tuesday : [solution-filename]        — Pau AI solution showcase
  Thursday: [insight-filename]         — Pau Analytics standalone insight
  Friday  : [usecase-filename]         — Pau AI use case spotlight

FILES UPDATED:
  publish-queue.md — updated
  publish-log.txt — entry added
  pau-ai-showcase-log.txt — 2 entries added

NEXT STEPS:
  1. Paste Monday's LinkedIn post now
  2. Paste remaining posts on their scheduled days
  3. Run /coordinator on Friday for the weekly report
```
