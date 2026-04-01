# Step 2 — Read Case Study and Write Queue

Work through each sub-step in order. Do not write the queue file until all content has been extracted and confirmed.

---

## Sub-step 2A: Read the Case Study HTML

Read the case study HTML file at:
`C:\Users\Lenovo\pau-analytics-1.0\case-study\[slug].html`

Extract the following:
- **Title** — the main heading of the case study
- **Key findings** — the first 3 to 5 substantive paragraphs or the findings/conclusion section
- **Business problem addressed** — what question or challenge does this case study answer?
- **Target audience relevance** — which type of SME owner (F&B, retail, e-commerce, general) would find this most useful?
- **Live URL** — `https://www.pauanalytics.com/case-study/[slug].html`

If the case study is in Mandarin, extract all content in Mandarin. Do not translate.

---

## Sub-step 2B: Draft the Blog Brief

From the extracted content, prepare a brief that the blog writing skill will use as its input. The brief must include:

- **Case study title** — exact title from the HTML
- **Case study URL** — live URL on pauanalytics.com
- **Recommended blog language** — English or Mandarin (as confirmed in Step 1)
- **Target reader** — the SME owner profile this blog is written for
- **Core insight** — the single most useful thing an SME owner can learn from this case study (1–2 sentences)
- **Suggested blog angle** — how to frame the insight as a blog post title and hook (not a summary — a story or problem-first entry point)
- **Key data points to use** — 2 to 3 specific findings from the case study that can be cited in the blog
- **Related case study slug** — the same slug, to be used as a cross-link in the blog post

Show the brief to the user and ask:
> "Does this brief look right for the blog post? Confirm to proceed, or let me know if you want to adjust the angle."

Wait for confirmation before writing the queue file.

---

## Sub-step 2C: Write publish-queue.md

Write the confirmed brief to:
`C:\Users\Lenovo\pau-analytics-1.0\publish-queue.md`

Use this format exactly:

```
# Publish Queue

**Status:** Ready
**Scheduled:** [today's date]
**Case study slug:** [slug]
**Case study URL:** https://www.pauanalytics.com/case-study/[slug].html
**Blog language:** [English / Mandarin]
**Target reader:** [SME owner type]

## Core Insight
[1–2 sentences — the main thing an SME owner learns from this]

## Suggested Blog Angle
[How to enter the story — problem-first, not summary-first]

## Key Data Points
- [Finding 1]
- [Finding 2]
- [Finding 3]

## Cross-link
https://www.pauanalytics.com/case-study/[slug].html
```

---

## Sub-step 2D: Update publish-log.txt

Append one line to `C:\Users\Lenovo\pau-analytics-1.0\publish-log.txt`:

```
[YYYY-MM-DD] | [slug] | [language] | queued
```

If the file does not exist, create it with this line as the first entry.

---

## End of Step 2

Confirm completion with the user:

> "Done. publish-queue.md is ready. The next step is to run the pau-analytics-blog-write skill and tell Claude: 'Write a blog post from the publish queue at C:\Users\Lenovo\pau-analytics-1.0\publish-queue.md'."

Display the full contents of publish-queue.md so the user can verify it before starting the blog writing step.
