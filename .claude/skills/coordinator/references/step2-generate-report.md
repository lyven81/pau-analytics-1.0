# Step 2 — Generate the Weekly Report

Use the data collected in Step 1 to produce the full weekly report. Work through each section in order.

---

## Section A: Content Published This Week

List every piece of content published in the past 7 days:

- Blog posts: title, slug, URL, language
- Case studies: title, slug, URL (if any new ones were published to pauanalytics.com)
- LinkedIn posts: which slugs went live, approximate date

If nothing was published, write: "No content was published this week."

---

## Section B: LinkedIn Queue Status

Report the current state of the LinkedIn drafts folder:

- How many posts are drafted and waiting to be posted (`.txt` files)
- How many posts have already been published (`.posted.txt` files)
- Which post is next in the queue (oldest unposted `.txt` file)
- Estimated weeks of LinkedIn content remaining at 1 post per week

---

## Section C: Leads This Week

Report lead activity clearly and simply:

- Total new leads received
- Breakdown by channel: CH-A (Google Ads), CH-B (Blog/LinkedIn), CH-W (Website Chat)
- Which blog posts drove CH-B leads (list slugs and lead count per slug)
- Total pipeline status: how many leads at each stage

If no leads yet: "No leads received this week. The pipeline is in the content-building phase."

---

## Section D: What Is Working

Analyse the connection between content and leads:

**Proven topics** — any blog slug that has generated 2 or more total leads (across all weeks, not just this week). List them. These should be prioritised for follow-up content (e.g. a Mandarin version, a deeper case study, a related topic).

**Top channel this week** — which channel brought the most leads? Note any trend (e.g. CH-B growing, CH-A flat).

If there are no leads yet, skip this section and write: "Not enough lead data yet to identify what is working. This section will populate once leads start coming in."

---

## Section E: Next Week Plan

Report what is planned:

- Case study selected for the next blog post (from publish-queue.md)
- Language of the next blog post
- LinkedIn post scheduled for next Wednesday (slug)
- Any content gaps or risks (e.g. LinkedIn queue running low, no topic queued)

If no plan exists: "No content is queued for next week. Run the content-scheduler skill to set the next topic."

---

## Section F: Action Items for the Business Owner

Generate a clear, numbered action list. Only include items that genuinely require human action. Do not pad with tasks the agents handle automatically.

Examples of valid action items:
- Follow up on leads at "New" status for more than 24 hours (list their names or challenge descriptions)
- Approve or override the next week's blog topic
- Mark specific leads as Lost if no reply after 5+ days at Follow-up Sent
- Schedule the next LinkedIn post in Buffer if not yet done this week

Format:
```
[ ] 1. Follow up on 2 leads still at "New" — received more than 24 hours ago
[ ] 2. Confirm next week's blog topic: [slug] — reply "confirmed" or suggest a change
[ ] 3. [any other action]
```

If there are no action items: "No action required from you this week."

---

## Assemble the Full Report

Combine all sections into the following format:

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
PAU ANALYTICS — WEEK [WW] [YEAR]
[Start date] – [End date]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

CONTENT PUBLISHED THIS WEEK
─────────────────────────────
[Section A content]

LINKEDIN QUEUE STATUS
─────────────────────────────
[Section B content]

LEADS THIS WEEK
─────────────────────────────
[Section C content]

WHAT IS WORKING
─────────────────────────────
[Section D content]

NEXT WEEK PLAN
─────────────────────────────
[Section E content]

YOUR ACTION ITEMS
─────────────────────────────
[Section F content]

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

Show the completed report to the user and ask:
> "Here is the weekly report. Does everything look correct before I save and push it to GitHub?"

Wait for confirmation before loading `references/step3-save-send.md`.
