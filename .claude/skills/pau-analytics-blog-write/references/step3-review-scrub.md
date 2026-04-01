# Step 3 — Review and Scrub

## What This Step Does

Before the draft is handed off for publishing, check it against a quality checklist and remove AI writing patterns that would make it sound robotic or generated.

---

## 3A — Quality Checklist

Go through each item. Flag any that are not met and fix them before moving on.

### Structure
- [ ] Post opens with a hook — not a generic definition or "X is important"
- [ ] Introduction follows APP formula (Agree, Promise, Preview)
- [ ] Primary keyword appears naturally in the first 100 words
- [ ] At least 4 H2 sections with logical flow
- [ ] Paragraphs are 2–4 sentences maximum
- [ ] Post ends with a clear conclusion and CTA block linking to case study
- [ ] SEO elements block is present (meta title, meta description, keyword, slug, date)

### Content
- [ ] All numbers and findings come directly from the dataset — nothing fabricated
- [ ] At least 2 mini-stories with specific person/scenario/outcome
- [ ] No section simply restates what another section already said
- [ ] Conclusion summarises 2–3 takeaways — no new information introduced

### Language (English posts)
- [ ] Sentences average 15–20 words — not all short, not all long
- [ ] Active voice used throughout — passive voice only where it reads naturally
- [ ] No filler phrases: "It is worth noting", "In today's world", "It goes without saying"
- [ ] No em-dash overuse — replace with comma, semicolon, or new sentence where possible

### Language (Mandarin posts)
- [ ] Written in 马来西亚华语 — not translated from English sentence by sentence
- [ ] Business terms explained in context on first use
- [ ] 您 used when addressing the reader directly
- [ ] Sentences feel natural when read aloud — not stiff or academic
- [ ] Numbers written as numerals (60%, not 百分之六十)

### Length
- [ ] Minimum 800 words (target 1,000–1,500 words)
- [ ] No section is padded with filler to hit word count — every paragraph earns its place

---

## 3B — AI Pattern Scrub

After passing the checklist, scan the draft for these patterns and rewrite wherever found:

| Pattern to remove | Replace with |
|---|---|
| Em-dashes used mid-sentence (—) | Comma, semicolon, or split into two sentences |
| "Delve into" | "Look at", "explore", "examine" |
| "It is important to note that" | Delete or rewrite the point directly |
| "In conclusion" as an opener | Just write the conclusion without announcing it |
| "Leverage" (used as a verb) | "Use", "apply", "take advantage of" |
| "Comprehensive" or "robust" | Describe specifically what is comprehensive or robust |
| "In today's competitive landscape" | Delete — state the point directly |
| Three or more rhetorical questions in a row | Keep one, remove the rest |
| Bullet lists of 6+ items with no explanation | Break into 2 shorter lists or convert to prose |

For Mandarin posts, watch for:
- Overly formal 书面语 phrasing that sounds like an academic paper
- 所以 used at the start of every conclusion sentence
- 非常 and 很 overused — vary with 相当、格外、尤其

---

## 3C — Final Confirmation

After completing the checklist and scrub, confirm with the user:

| Item | Value |
|---|---|
| Draft file path | `C:\Users\Lenovo\pau-analytics-1.0\blog\drafts\[slug]-[date].md` |
| Word count | [actual count] |
| Language | EN or 中文 |
| Checklist | All items passed |
| AI patterns scrubbed | Yes |
| Ready for publish skill | Yes / Needs human review first |

**For Mandarin posts:** Flag the draft as needing a human review pass before publishing — specifically the CTA text and conclusion section. Note this in the confirmation.

The draft is now ready to be passed to the `new-pau-analytics-blog-publish` skill.
