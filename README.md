# ahmed kamal — personal site

A minimal, dark purple, academic portfolio. Five pages:

- `index.html` — home (hero, selected research, featured projects)
- `research.html` — long-form research write-ups
- `projects.html` — featured projects with deeper detail
- `cv.html` — structured curriculum vitae
- `contact.html` — contact links

All shared styles live in `css/style.css`.

---

## Where to edit text

Every place you should fill in is marked with an HTML comment that starts with
`<!-- EDIT:` so you can find them quickly. Open any page in a text editor and
search for `EDIT:` — that's your to-do list.

Examples of things to replace:

- The intro paragraph on the home page hero
- The descriptions on each research and project section
- All `you@example.com` placeholder emails
- All `#` placeholder URLs (GitHub, LinkedIn, Twitter, CV PDF download)
- Years, dates, GPA, test scores, course lists
- Tags / skill chips

You don't need to touch any CSS unless you want to tweak the look.

---

## Tweaking the look

All theme colors are CSS variables at the top of `css/style.css`. Change them
in one place and they update everywhere.

```css
--accent:         #c9b8ff;   /* main purple — buttons, links, icons */
--accent-strong:  #d4c5ff;   /* slightly brighter for emphasis */
--accent-bg:      #2d1f4d;   /* purple background for tags */

--bg-base:        #0a0612;   /* darkest layer */
--bg-surface:     #120a1f;   /* nav, footer */
--bg-elevated:    #1a1030;   /* project cards */
```

Fonts are loaded from Google Fonts — `Cormorant Garamond` for the serif
display headings, `Geist` for body, `Geist Mono` for small mono labels.

---

## Deploying to GitHub Pages

1. Create a new GitHub repo. If you want the URL `yourusername.github.io`,
   name the repo exactly `yourusername.github.io`. Otherwise pick any name
   (the URL will be `yourusername.github.io/reponame`).

2. Push the contents of this folder to the repo:

   ```bash
   git init
   git add .
   git commit -m "initial site"
   git branch -M main
   git remote add origin https://github.com/YOURNAME/REPO.git
   git push -u origin main
   ```

3. On GitHub: **Settings → Pages → Source: Deploy from branch → main → /(root) → Save**.

4. Wait ~30 seconds. The site will be live at the URL Pages shows you.

---

## Custom domain

Once the site is live on GitHub Pages:

1. Buy a domain from any registrar (Namecheap, Cloudflare, Porkbun — Cloudflare
   is cheapest and has the best DNS).

2. In your domain's DNS settings, add these records:

   ```
   Type   Name    Value
   A      @       185.199.108.153
   A      @       185.199.109.153
   A      @       185.199.110.153
   A      @       185.199.111.153
   CNAME  www     YOURNAME.github.io
   ```

3. In your repo: **Settings → Pages → Custom domain** → enter your domain →
   Save. Tick "Enforce HTTPS" once it becomes available (can take an hour).

4. Add a file named `CNAME` (no extension) at the root of the repo containing
   just your domain name on one line, e.g. `ahmedkamal.dev`.

That's it. Your site is now live at your custom domain with HTTPS.

---

## Files

```
.
├── index.html
├── research.html
├── projects.html
├── cv.html
├── contact.html
├── README.md
├── css/
│   └── style.css
└── assets/        (put a profile photo, CV PDF, project images here)
```
