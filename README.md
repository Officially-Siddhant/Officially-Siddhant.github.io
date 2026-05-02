# sous_chef's : Portfolio Site
**Live at:** https://officially-siddhant.github.io


## File structure

```
Officially-Siddhant.github.io/
├── index.html       ← Home
├── projects.html    ← All 7 projects + Q&A (Giscus)
├── blog.html        ← Articles, math, external finds
├── contact.html     ← Contact form (Formspree)
└── style.css        ← Shared styles
```


## How to deploy

```bash
git clone https://github.com/Officially-Siddhant/Officially-Siddhant.github.io
cd Officially-Siddhant.github.io
# copy all 5 files from this folder into the repo
git add .
git commit -m "Initial portfolio site"
git push
```

Go to **Settings → Pages → Source: main branch** and save.
Your site is live in ~60 seconds.

---

## Activate Q&A (Giscus)

1. In your repo: **Settings → Features → enable Discussions**
2. Go to **giscus.app**, enter `Officially-Siddhant/Officially-Siddhant.github.io`
3. Copy the `<script>` tag it generates
4. In `projects.html`, find the `id="giscus-placeholder"` div and replace it with the script

---

## Activate the contact form (Formspree)

1. Sign up at **formspree.io**
2. Create a new form → copy the endpoint URL (looks like `https://formspree.io/f/XXXXXXXX`)
3. In `contact.html`, replace `https://formspree.io/f/YOUR_FORM_ID` with your URL

--- 
## Adding a blog post

**My own article:**
```
blog/
└── my-post-title.html   ← create this file
```
Then add a `.post-entry` block in `blog.html` with `data-type="article"`.

**Math post with LaTeX:**
Add KaTeX to the post file:
```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/katex@0.16.9/dist/katex.min.css">
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.16.9/dist/katex.min.js"></script>
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.16.9/dist/contrib/auto-render.min.js"
  onload="renderMathInElement(document.body)"></script>
```
Write math as `$$\int_0^\infty e^{-x^2} dx$$` and it renders automatically.

**External find:**
No new file needed — just add the block in `blog.html` with `data-type="external"` and link directly to the URL.

---

## Update your contact info

In `contact.html` and `index.html`, replace:
- `YOUR_HANDLE` → your LinkedIn slug
- `YOUR_EMAIL` → your email address
