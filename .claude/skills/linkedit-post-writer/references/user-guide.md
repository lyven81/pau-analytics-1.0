# User Guide — LinkedIn Post Writer

This is a plain-language guide for using the LinkedIn Post Writer skill. No technical knowledge needed.

---

## What This Skill Does

You give it a blog post you have already written. It reads the blog, picks out the most interesting finding, and writes a short LinkedIn post that makes people want to click through and read the full blog.

The LinkedIn post is not a copy of the blog. It is a teaser — just enough to create curiosity, then it points the reader to the blog for the full answer.

---

## When to Use This Skill

Use this skill after you have finished writing a blog post with the `pau-analytics-blog-write` skill (or after the blog is already published on pauanalytics.com).

**Typical order:**
1. Write the blog post → `pau-analytics-blog-write`
2. Publish the blog post → `new-pau-analytics-blog-publish`
3. Write the LinkedIn post → this skill (`linkedit-post-writer`)
4. Copy the LinkedIn post, paste into Buffer, and schedule for Wednesday 9am

---

## How to Start

Just tell Claude one of the following:

- "Write a LinkedIn post from this blog draft: [file path]"
- "Write a LinkedIn post for the know-your-reseller blog"
- "Turn this blog into a LinkedIn post"

You do not need to prepare anything. The skill will read the blog and do the rest.

---

## What You Need to Provide

Just one thing — the blog source. This can be:

| What you have | What to say |
|---|---|
| The draft file (you just wrote the blog) | Share the file path, e.g. `C:\Users\Lenovo\pau-analytics-1.0\blog\drafts\know-your-reseller-2026-03-07.md` |
| The blog is already published | Share the blog slug, e.g. `know-your-reseller` |

That is all. The skill handles everything else.

---

## What Happens Step by Step

**Step 1 — Read the blog**
The skill reads your blog post and identifies the most interesting finding, the best data point to highlight, and the blog URL to link to. It shows you a short summary and asks you to confirm before writing.

**Step 2 — Write the LinkedIn post**
The skill writes a LinkedIn post in the same language as the blog (English or Mandarin). The post is 150–250 words and follows a proven structure:
- A hook that makes people stop scrolling (shown before the "see more" button)
- The key insight from the blog
- One specific data point that proves it
- A link to the full blog
- 3–5 relevant hashtags

**Step 3 — Review and save**
The skill checks the post against a quality checklist and fixes any weak spots. It then shows you the final post and saves it as a text file you can copy and paste into LinkedIn.

---

## Where the Output Is Saved

Your LinkedIn post is saved as a plain text file here:

```
C:\Users\Lenovo\pau-analytics-1.0\blog\linkedin-drafts\
```

File name format: `[blog-slug]-linkedin-[date].txt`

Example: `know-your-reseller-linkedin-2026-03-07.txt`

Open the file, select all, copy, and paste directly into LinkedIn.

---

## Language

The skill automatically matches the language of the blog:
- English blog → English LinkedIn post
- Mandarin blog → Mandarin LinkedIn post

You do not need to specify the language — it detects it from the blog.

---

## What the Skill Does NOT Do

- It does not post to LinkedIn for you — you copy the output into Buffer and schedule it
- It does not write a different version in the other language (if you want both English and Mandarin posts, run the skill twice on the two language versions of the blog)
- It does not create images or graphics for the post

---

## Tips for a Better LinkedIn Post

- Run this skill after the blog is fully finished and reviewed — not from a rough draft
- If the hook the skill writes does not feel right, tell it: "Try a different opening line" and it will rewrite
- You can ask it to make the post shorter ("cut it to under 150 words") or adjust the tone ("make it sound less formal")
- For Mandarin posts, do a quick read-aloud before posting — if any sentence sounds stiff, ask the skill to rewrite that line

---

## Full Workflow Summary

```
Write blog             →  pau-analytics-blog-write
Publish blog           →  new-pau-analytics-blog-publish
Write LinkedIn post    →  linkedit-post-writer  (this skill)
Schedule in Buffer     →  you paste into Buffer → posts Wednesday 9am automatically
```

Each skill is separate. You can run them in any order or skip any step. The LinkedIn post writer only needs the blog — it does not care whether the blog has been published yet.
