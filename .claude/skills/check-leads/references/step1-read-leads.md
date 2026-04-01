# Step 1 — Read and Prioritize Leads

---

## 1A: Fetch Lead Data

Call the Web Chat Lead Manager API:

```
GET http://localhost:8000/api/leads
GET http://localhost:8000/api/stats
```

Use curl or httpx. If the API is unreachable, tell the user:

> "The Web Chat Lead Manager is not running. Start it first:
> Double-click start.bat in C:\Users\Lenovo\Documents\Pau Analytics\Web Chat Lead Manager\"

If the API returns data, continue.

---

## 1B: Show Summary

Display a quick summary:

```
Lead Dashboard Summary
═══════════════════════
Total leads:        [n]
This week:          [n]
Needs follow-up:    [n]

By channel:
  CH-A (Google Ads): [n]
  CH-B (Blog):       [n]
  CH-W (Chat):       [n]
```

---

## 1C: Filter Actionable Leads

From the full lead list, filter leads that need attention:

1. **Status = "New"** — not yet reviewed (highest priority)
2. **Status = "Qualifying"** — reviewed but no action taken
3. **Any lead at "New" for more than 24 hours** — flag as overdue

Sort by:
1. Overdue leads first (New for >24 hours)
2. Then by urgency score (if Ollama classification is available): 5 first, 1 last
3. Then by date (newest first)

---

## 1D: Display Actionable Leads

For each lead needing attention, show:

```
[URGENCY] Lead #[id] — [name]
  Status:    [status] (since [date])
  Channel:   [source]
  Challenge: [challenge text]
  Blog slug: [slug if CH-B]
  Urgency:   [score]/5 — [category]
  Opener:    [AI-suggested WhatsApp opener]
```

If there are no leads needing attention:

> "All clear — no leads need follow-up right now."

---

## End of Step 1

If there are actionable leads, say:

> "[n] leads need follow-up. Moving to Step 2 — drafting WhatsApp messages."

Load `references/step2-draft-followups.md`.

If no leads need attention, end the skill here.
