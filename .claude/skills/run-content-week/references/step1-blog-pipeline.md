# Step 1 — Pau Analytics Blog Pipeline

This step chains 4 existing skills to produce and publish one blog post plus its LinkedIn teaser.

---

## 1A: Check for Coordinator Recommendation

Read `C:\Users\Lenovo\pau-analytics-1.0\next-week-plan.md` if it exists.

If it recommends a specific topic or case study slug, pass that to the content-scheduler as a preference. If the file does not exist or has no recommendation, let the content-scheduler pick based on its default priority rules.

---

## 1B: Run Content Scheduler

Invoke the `content-scheduler` skill. This will:
1. Scan case studies that haven't been blogged about yet
2. Cross-check against publish-log.txt
3. Present top 3 options (or use the coordinator's recommendation)
4. Write publish-queue.md with the selected topic

If the user has a specific preference, tell the content-scheduler: "The coordinator recommends [topic]."

Wait for the content-scheduler to complete and confirm the selected topic.

---

## 1C: Run Blog Write

Invoke the `pau-analytics-blog-write` skill. Tell it:

> "Write a blog post from the publish queue at C:\Users\Lenovo\pau-analytics-1.0\publish-queue.md"

Wait for the blog draft to be written and saved to the drafts folder.

---

## 1D: Run Blog Publish

Invoke the `new-pau-analytics-blog-publish` skill. Tell it:

> "Publish the blog draft at C:\Users\Lenovo\pau-analytics-1.0\blog\drafts\[draft-filename]"

Wait for the blog to be published (HTML built, pushed to GitHub Pages).

Record the published blog slug — it will be needed for the LinkedIn teaser.

---

## 1E: Run LinkedIn Post Writer

Invoke the `linkedit-post-writer` skill. Tell it:

> "Write a LinkedIn post for the [slug] blog"

Wait for the LinkedIn teaser to be written and saved to `linkedin-drafts/`.

---

## End of Step 1

Confirm with the user:

> "Blog pipeline complete:
> - Blog published: [slug] ([language])
> - LinkedIn teaser saved: [filename]
>
> Moving to Step 2 — standalone insight post."

Load `references/step2-insight-post.md`.
