# Step 2 — Build the HTML Page

## What This Step Does

Convert the Markdown draft into a complete HTML blog post page and prepare a new card for the blog listing page. Both are based on existing templates — do not invent new structure.

---

## 2A — Read the Template

Read the blog post template at:
`C:\Users\Lenovo\pau-analytics-1.0\blog\template.html`

This is the base HTML. You will replace all `[PLACEHOLDER]` values with real content from the draft.

---

## 2B — Populate the Template Placeholders

Replace every placeholder in the template with the confirmed values from Step 1:

| Placeholder | Replace with |
|---|---|
| `[POST TITLE]` (in `<title>` tag) | Post title |
| `[POST SLUG]` (in canonical URL) | Post slug |
| `[META DESCRIPTION — 150-160 characters]` | Meta description from draft |
| `[POST TITLE]` (in `<h1>`) | Post title |
| `[DATE — e.g. 5 March 2026]` | Display date |
| `[EN or 中文]` (lang-badge) | Language badge text |
| `[CASE STUDY SLUG]` (sidebar button href) | Related case study slug |

---

## 2C — Convert Markdown Body to HTML

Convert the post body from Markdown to HTML. Replace the placeholder sections in the template's `<article class="blog-post-content">` with the converted content.

Apply these conversion rules:

| Markdown | HTML |
|---|---|
| `# Title` | Already used as `<h1>` — skip in body |
| `## Heading` | `<h2>Heading</h2>` |
| `### Subheading` | `<h3>Subheading</h3>` |
| `**bold text**` | `<strong>bold text</strong>` |
| `*italic text*` | `<em>italic text</em>` |
| Blank-line separated paragraph | `<p>paragraph text</p>` |
| `- item` or `* item` | `<ul><li>item</li></ul>` (group consecutive items) |
| `1. item` | `<ol><li>item</li></ol>` (group consecutive items) |
| `> blockquote` | `<blockquote><p>text</p></blockquote>` |
| `---` (horizontal rule before SEO block) | Stop — do not include SEO block in HTML body |

**Important:** The SEO elements block at the end of the Markdown draft (meta title, meta description, keyword, slug, date) is for reference only — do not render it as HTML content. Stop converting at the `---` separator before the SEO block.

---

## 2D — Build the CTA Block (Channel B Lead Capture)

The CTA block is a mini-form with two input fields (name + challenge) and a submit button. On submit, `submitBlogCTA(slug, lang)` opens WhatsApp with a pre-formatted `[CH-B: slug]` message. The Marketing Lead Manager app receives this via webhook and processes it automatically.

Replace `SLUG` in `submitBlogCTA('SLUG', ...)` with the confirmed post slug from Step 1.

**IMPORTANT:** The WhatsApp message labels MUST match what `channel_b.py` expects:
- EN: `Name:` and `My biggest challenge:`
- ZH: `姓名：` and `我最大的困扰：`

Add the CSS block inside the post's `<style>` tag if not already present.

**CSS to add inside `<style>` block:**
```css
.post-cta {
  margin-top: 2.5rem;
  padding: 2rem;
  background: var(--alt);
  border: 1px solid var(--border);
  border-radius: var(--radius);
  text-align: center;
}
.post-cta p { font-size: 0.95rem; color: var(--muted); margin-bottom: 1rem; }
.cta-form { display: flex; flex-direction: column; gap: 0.75rem; max-width: 420px; margin: 0 auto; }
.cta-form input {
  padding: 0.75rem 1rem;
  border: 1px solid var(--border);
  border-radius: 8px;
  font-family: 'Inter', sans-serif;
  font-size: 0.9rem;
  color: var(--text);
  background: var(--white);
  transition: border-color 0.25s ease;
}
.cta-form input:focus { outline: none; border-color: var(--gold); }
.cta-form input::placeholder { color: #aaa; }
.cta-link {
  display: inline-block;
  padding: 0.75rem 1.5rem;
  background: var(--gold);
  color: var(--white);
  border: none;
  border-radius: 8px;
  font-family: 'Inter', sans-serif;
  font-weight: 600;
  font-size: 0.95rem;
  cursor: pointer;
  transition: background 0.25s ease, transform 0.25s ease;
}
.cta-link:hover { background: var(--gold-hover); transform: translateY(-1px); }
```

**English posts:**
```html
<div class="post-cta">
    <p>Want to find out what your own data is saying? Share a bit about your business and we'll look at it together.</p>
    <div class="cta-form">
        <input type="text" id="cta-name" placeholder="Your name (optional)" />
        <input type="text" id="cta-challenge" placeholder="Your biggest business challenge *" />
        <button class="cta-link" onclick="submitBlogCTA('SLUG', 'en')">Chat with Us on WhatsApp →</button>
    </div>
</div>
```

**Mandarin posts:**
```html
<div class="post-cta">
    <p>想知道您自己的数据在说什么？分享一下您生意上的困扰，我们一起来看看。</p>
    <div class="cta-form">
        <input type="text" id="cta-name" placeholder="您的姓名（可选）" />
        <input type="text" id="cta-challenge" placeholder="您目前生意上最大的困扰 *" />
        <button class="cta-link" onclick="submitBlogCTA('SLUG', 'zh')">WhatsApp 联系我们 →</button>
    </div>
</div>
```

**Then add before `</body>`:**
```html
<script>
async function submitBlogCTA(slug, lang) {
  var nameEl = document.getElementById('cta-name');
  var challengeEl = document.getElementById('cta-challenge');
  var name = (nameEl ? nameEl.value.trim() : '') || 'Visitor';
  var challenge = (challengeEl ? challengeEl.value.trim() : '');
  if (!challenge) { if (challengeEl) challengeEl.focus(); return; }

  var btn = document.querySelector('.post-cta .cta-link');
  if (btn) { btn.disabled = true; btn.textContent = lang === 'zh' ? '提交中...' : 'Sending...'; }

  var msg;
  if (lang === 'zh') {
    msg = '[CH-B: ' + slug + ']\n姓名：' + name + '\n我最大的困扰：' + challenge;
  } else {
    msg = '[CH-B: ' + slug + ']\nName: ' + name + '\nMy biggest challenge: ' + challenge;
  }
  window.open('https://wa.me/60149207099?text=' + encodeURIComponent(msg), '_blank');
  if (btn) {
    btn.disabled = false;
    btn.textContent = lang === 'zh' ? 'WhatsApp 联系我们 →' : 'Chat with Us on WhatsApp →';
  }
}
</script>
```

The slug is hardcoded per blog post. Language (`'en'` or `'zh'`) matches the blog's language. No external scripts are needed — the WhatsApp URL opens directly.

---

## 2E — Prepare the Blog Listing Card

Prepare the card HTML to be inserted into `blog/index.html`. Use this exact format:

```html
<div class="blog-card fade-in" data-lang="[EN or ZH]">
  <div class="blog-card-body">
    <span class="blog-lang">[EN or ZH]</span>
    <h3>[POST TITLE]</h3>
    <p>[CARD DESCRIPTION]</p>
    <a href="[SLUG].html" class="read-more">[Read More → or 阅读全文 →]</a>
  </div>
</div>
```

Fill in all values from Step 1 confirmed inputs.

**data-lang:** Use `EN` for English posts, `ZH` for Mandarin posts — this is what the language toggle uses.
**blog-lang badge:** Use `EN` or `ZH` to match.
**read-more text:** Use `Read More →` for EN, `阅读全文 →` for ZH.

---

## 2F — Update the Blog Listing Page

Read `C:\Users\Lenovo\pau-analytics-1.0\blog\index.html`.

Find this comment block:
```html
<!-- Blog post cards are added here.
```

Insert the new card HTML **before** this comment block, so new posts appear at the top of the grid.

Also update the `resultsCount` initial display if needed — but this is handled dynamically by JavaScript, so no manual change is required.

---

## 2G — Confirm Before Saving

Show the user a summary of what will be written:

> "Ready to save:
>
> 1. New blog post page: `blog/[slug].html`
> 2. Updated listing page: `blog/index.html` (new card added at top)
>
> Type yes to save and proceed to Step 3, or let me know if anything needs adjusting."
