# Step 2 — Write the Blog Post

## What This Step Does

Write the full blog post based on the confirmed angle, title, language, and target reader from Step 1. The post must be structured for SEO, written for a Malaysian SME audience, and end with a cross-link to the related case study.

---

## 2A — Structure Overview

Every post follows this structure:

| Section | Length | Purpose |
|---|---|---|
| Title (H1) | Confirmed in Step 1 | The search keyword anchor |
| Introduction | 150–200 words | Hook reader, state the problem, promise the answer |
| Body sections (H2/H3) | 4–6 H2 sections | Answer the angle in logical steps |
| Conclusion | 100–150 words | Summarise 2–3 takeaways, actionable close |
| WhatsApp CTA | 1 block | Lead reader to start a conversation (lead generation exit) |

Minimum total length: 800 words. Target: 1,000–1,500 words.

---

## 2B — Introduction Rules

**Do not open with a generic definition or "X is important because..."**

Choose one hook type for the opening sentence:

| Hook type | Example |
|---|---|
| Provocative question | "What if the customers you think are loyal are already planning to leave?" |
| Specific scenario | "A retail shop owner in KL noticed her repeat customer numbers dropped 20% in three months — but her new customer numbers looked fine." |
| Surprising fact from the data | "In our analysis of 5,000 transactions, the top 10% of customers accounted for 60% of revenue — and most businesses had no idea who they were." |
| Bold statement | "Your best customers are not the ones who buy the most. They are the ones who stay." |

After the hook, follow the APP formula:
- **Agree** — acknowledge a problem or belief the reader already holds
- **Promise** — state clearly what the reader will learn from this post
- **Preview** — briefly outline the sections ahead (1–2 sentences)

Include the primary keyword naturally within the first 100 words.

---

## 2C — Body Section Rules

**Structure:**
- Use H2 for main sections (4–6 sections)
- Use H3 for subsections where needed
- Keep paragraphs to 2–4 sentences maximum
- Vary sentence length — mix short punchy sentences with longer explanatory ones

**Content:**
- Each H2 section must answer one specific sub-question related to the angle
- Use data from the dataset to support each point — specific numbers, not vague claims
- Include 2–3 mini-stories across the post (see below)
- Use bullet or numbered lists where they make content easier to scan

**Mini-stories (2–3 per post, 50–100 words each):**
Each mini-story needs:
- A specific person or business type (e.g. "A kedai runcit owner in Penang", "A clothing retailer named Siti")
- A concrete situation with a detail or number
- A clear outcome showing what changed

Example:
> "A grocery shop owner in Subang noticed that his top 50 customers hadn't returned in 60 days. He had assumed they were still active because his total sales were steady — new customers were masking the churn. Once he identified this group and sent a simple WhatsApp message with a loyalty offer, 30 returned within a week."

Place mini-stories:
- One in the introduction or first section (hook readers)
- One in the middle (re-engage skimmers)
- One near the conclusion (reinforce the main point)

---

## 2D — Mandarin Writing Rules

Apply these rules when writing in 中文:

- Write in 马来西亚华语 — natural, conversational Malaysian Chinese
- Do not translate English idioms literally — find equivalent Mandarin expressions
- Business terms: write plainly (e.g. 回头客 for returning customers, 流失率 for churn rate — then explain in context on first use)
- Keep sentences shorter than in English — Mandarin reads better in short, clear bursts
- Use 您 when addressing the reader directly (more respectful for a business audience)
- Numbers stay as numerals (e.g. 60% not 百分之六十) for readability

---

## 2E — Conclusion Rules

- Summarise 2–3 key takeaways in plain language
- Close with an actionable sentence — what should the reader do next with this information?
- Do not introduce new information in the conclusion
- Keep it under 150 words

---

## 2F — CTA Block (End of Post)

Every post ends with a web chat CTA block — this is the lead generation exit point. Readers who reach the end are warm; the CTA is a mini-form (name + challenge fields) that submits to the backend API (source=CH-B).

Write only the CTA copy in the draft — the publish skill inserts the complete mini-form HTML with the correct slug hardcoded.

**English posts:**
```
---
CTA copy: Want to find out what your own data is saying? Share a bit about your business and we'll look at it together.
Button: Chat with Us →
---
```

**Mandarin posts:**
```
---
CTA copy: 想知道您自己的数据在说什么？分享一下您生意上的困扰，我们一起来看看。
Button: 联系我们 →
---
```

The publish skill (`new-pau-analytics-blog-publish`) wraps this copy in the full mini-form HTML with:
- Name field (optional)
- Challenge field (required)
- Submit button that POSTs to backend `/chat/start` with source=CH-B and slug
- On success: form replaced with inline confirmation message
- Fallback: opens WhatsApp if backend not available

Do not write the HTML or any backend URL in the draft. Do not link to a case study in this block — the case study is referenced in the sidebar only.

---

## 2G — SEO Elements to Include

At the end of the post, provide these elements as a separate block:

```
---
Meta title: [50–60 characters]
Meta description: [150–160 characters — include primary keyword, make it compelling]
Primary keyword: [the main search term this post targets]
URL slug: [post-slug in lowercase-hyphens]
Language: EN or ZH
Date: [today's date]
Related case study slug: [slug]
---
```

---

## 2H — Output

Save the completed draft as a Markdown file:
- Location: `C:\Users\Lenovo\pau-analytics-1.0\blog\drafts\`
- Filename: `[post-slug]-[YYYY-MM-DD].md`
- Include: full post body + SEO elements block + CTA block at the end

Confirm the file path with the user before moving to Step 3.
