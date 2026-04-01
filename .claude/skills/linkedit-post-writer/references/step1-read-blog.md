# Step 1 — Read the Blog

## What This Step Does

Read the blog post and pull out the three things needed to write the LinkedIn post: the hook angle, the key data point, and the blog URL.

---

## 1A — Get the Blog Source

The user will provide one of the following:

| Input type | What to do |
|---|---|
| Draft file path (`.md`) | Read the file directly |
| Blog slug (e.g. `know-your-reseller`) | Read from `C:\Users\Lenovo\pau-analytics-1.0\blog\[slug].html` |
| Blog URL | Fetch the page and extract the article body |

If none is provided, ask: "Which blog post do you want to turn into a LinkedIn post? Share the draft file path or the blog slug."

---

## 1B — Detect the Language

Check whether the blog is in English or Mandarin. The LinkedIn post must be written in the same language.

| Blog language | LinkedIn post language |
|---|---|
| English | English |
| Mandarin (中文) | Mandarin (中文) |

Do not mix languages. Do not write in English if the blog is in Mandarin.

---

## 1C — Extract These Three Things

Read the full blog and identify:

**1. The hook angle**
The single most surprising, counterintuitive, or provocative finding in the blog. This is what the LinkedIn post will open with. It should make someone stop scrolling.

Ask yourself: what is the one line from this blog that, if someone read it cold, would make them want to know more?

**2. The key data point**
One specific number or finding from the blog that proves the hook. Specific always beats vague.

- Good: "The reseller receiving the highest discounts returned a gross margin of negative $1,250."
- Weak: "Some resellers were losing the company money."

**3. The blog URL**
Construct the blog link: `https://www.pauanalytics.com/blog/[slug]`

If the slug is not clear from the source, ask the user to confirm it.

---

## 1D — Confirm Before Writing

Show the user a brief summary before proceeding to Step 2:

> "Here's what I'll build the LinkedIn post around:
>
> - Language: [EN / 中文]
> - Hook angle: [one sentence]
> - Key data point: [the specific number or finding]
> - Blog link: [full URL]
>
> Type yes to continue, or adjust any of the above."
