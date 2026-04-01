# Step 3 — Save, Push, and Confirm

## 3A — Save the Blog Post Page

Save the completed HTML to:
`C:\Users\Lenovo\pau-analytics-1.0\blog\[slug].html`

If a file with that name already exists and the user has not already confirmed overwrite in Step 1, warn again before writing.

---

## 3B — Save the Updated Listing Page

Save the updated `blog/index.html` with the new card inserted at the top of the grid.

Verify the card was inserted correctly — the new card should appear before the `<!-- Blog post cards are added here` comment block and before all existing cards.

---

## 3C — Commit and Push

Run git commands from the repo root at `C:\Users\Lenovo\pau-analytics-1.0\`:

```
git add blog/[slug].html blog/index.html
git commit -m "Add blog post: [post title]"
git push
```

If the push fails, show the error to the user and do not retry automatically.

---

## 3D — Confirm Completion

After a successful push, confirm with the user:

> "Done. Both files have been pushed and should be live shortly.
>
> - **Blog post:** https://www.pauanalytics.com/blog/[slug].html
> - **Blog listing:** https://www.pauanalytics.com/blog/
>
> Note: GitHub Pages may take 1–2 minutes to update. Refresh the blog listing page to confirm the new card appears."

---

## 3E — Hand Off to LinkedIn Post Writer

Immediately after confirming the push, continue without waiting for the user to ask.

Tell the user:
> "Blog is live. Now writing the LinkedIn teaser post for this blog."

Load the `linkedit-post-writer` skill and begin Step 1 using:
- Blog source: the live URL just published — `https://www.pauanalytics.com/blog/[slug].html`
- Language: same language as the blog post just published
- Output: save to `C:\Users\Lenovo\pau-analytics-1.0\blog\linkedin-drafts\[slug]-linkedin-[YYYY-MM-DD].txt`

Do not ask the user whether to proceed — writing the LinkedIn post is a fixed part of the blog publish workflow. Every blog published gets a LinkedIn teaser. There are no exceptions.
