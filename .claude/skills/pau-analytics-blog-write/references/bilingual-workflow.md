# Bilingual Blog Writing Workflow

This reference defines how to decide the language for each blog post, how to write it, and how to handle review before publishing. Follow this before starting any blog post.

---

## Step 1 — Decide the Language

Choose the language based on the target audience of the insight, not the dataset.

| If the insight serves... | Write in... | Reason |
|---|---|---|
| Retail, F&B, trading, hawker businesses, traditional SMEs | Mandarin (中文) | These sectors skew Mandarin-speaking in Malaysia |
| Manufacturing, export, professional services, B2B | English | Decision-makers in these sectors are typically English-comfortable |
| General business audience (could be either) | English first | Write English now, adapt Mandarin later if the post performs well |

When unsure, ask: who is the business owner most likely to Google this topic? Write in the language they search in.

---

## Step 2 — Write Natively, Do Not Translate

Each blog post is written fresh in the chosen language — not translated word-for-word from the other language.

**For English posts:**
- Use the pau-analytics-blog-write skill in English mode
- Audience: Malaysian SME owners comfortable reading English
- Tone: plain, direct, practical — no academic language

**For Mandarin posts:**
- Use the pau-analytics-blog-write skill in Mandarin mode
- Language standard: 马来西亚华语 (Malaysian Chinese) — not Simplified Chinese written for a China audience
- Tone: conversational, grounded in Malaysian business context
- Business terms: write out in plain language (e.g. 客户流失率 is fine, but explain it in context)
- Do not translate English idioms — find the equivalent Mandarin expression

---

## Step 3 — Review Before Publishing

| Post language | Review level | What to check |
|---|---|---|
| English | Light | Facts and numbers match the dataset; CTA links are correct; reading flows naturally |
| Mandarin | Close | Business terms feel natural; numbers and findings are accurate; CTA text is clear; no awkward phrasing from over-literal translation |

For Mandarin posts, have a Mandarin-proficient person read the CTA and conclusion section before publishing. These are the highest-stakes parts.

---

## Step 4 — Assign Language Tag

Every blog post must carry a language tag used by the blog listing page filter.

| Language | Badge text | data-category value |
|---|---|---|
| English | EN | en |
| Mandarin | 中文 | zh |

This tag goes into the blog card on the listing page and into the HTML of the individual post page.

---

## Step 5 — Second-Language Version (Not Immediate)

Do not produce both language versions of every post immediately. It is not required and creates unnecessary work upfront.

**When to produce a second-language version:**
- After 30 days, if a post shows strong traffic or engagement, adapt it into the second language
- Adaptation means rewriting natively for the new audience — not translating
- A Mandarin version of an English post may use different examples or emphasis if that better serves the Mandarin-speaking reader

**Rollout priority for bilingual content:**
1. Blog posts — write in chosen language, adapt later if popular
2. Homepage hero section — translate when 5 or more Mandarin posts are live
3. Case study pages — translate when client base justifies it

---

## Quick Reference

| Situation | What to do |
|---|---|
| Retail / F&B / hawker insight | Write in Mandarin |
| B2B / export / professional services insight | Write in English |
| Not sure which language | Write in English first |
| Mandarin post is done | Do a close review before publishing — especially CTA and conclusion |
| Popular post after 30 days | Consider adapting into the second language |
| Someone asks for auto-translation | Do not use Google Translate — write natively instead |
