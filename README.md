# Sulaiha Granites — Website

A 6-page static website (Home, About, Products, Gallery, Testimonials, Contact)
built with plain HTML, CSS and JS — no frameworks, no build step. You can host
it for free and edit it anytime with nothing more than a text editor.

## Before you publish — fix these 3 things

1. **Email address**: I used `sulaihagranites@gmail.com`. Your message said
   "sulaihagranitesgmail.com" (missing the `@`) — if the real address is
   different, find-and-replace `sulaihagranites@gmail.com` across all 6 `.html`
   files and in `contact.html`'s form `action` line.

2. **Contact form redirect link**: in `contact.html`, the hidden field
   `_next` currently points to:
   `https://YOUR-USERNAME.github.io/sulaiha-granites/contact.html?sent=true`
   Once your site is live, replace `YOUR-USERNAME` with your actual GitHub
   username (see hosting steps below), or just delete that whole `<input
   type="hidden" name="_next" ...>` line — FormSubmit will show its own
   default "thanks" page instead.

3. **Activate the contact form (one-time)**: the form uses a free service
   called [FormSubmit](https://formsubmit.co) — it emails form submissions
   straight to your inbox, with no backend or sign-up required. The **first**
   time anyone submits the form, FormSubmit sends a confirmation email to
   `sulaihagranites@gmail.com`. Open that email and click "Activate" — after
   that, every future submission lands in your inbox automatically.

## Replacing the placeholder stone images

There are no real photos in this site yet — the colored swatches in
**Products** and **Gallery** are drawn with CSS to stand in for real granite
and marble photos (this avoids using random, possibly copyrighted, internet
photos on your business site).

To swap in your own photos:
1. Put your photo files in the `images/` folder (e.g. `images/black-galaxy.jpg`).
2. In `products.html` or `gallery.html`, find a line like:
   `<div class="swatch stone-black-galaxy"></div>`
3. Replace it with:
   `<img src="images/black-galaxy.jpg" alt="Black Galaxy granite slab" class="swatch">`

Photos taken on any phone in good light work fine — just shoot the stone
straight-on, filling the frame.

## Editing content

- Text: open any `.html` file in a text editor and edit the words directly.
- Colors/fonts: everything is controlled from `css/style.css`, in the
  `:root { ... }` block at the top.
- Phone number / WhatsApp link: search for `9345559879` across the files if
  the number ever changes — it appears in `tel:` links, the WhatsApp link, and
  the footer.

## Hosting it for free — GitHub Pages (recommended)

1. Create a free account at [github.com](https://github.com) if you don't
   have one.
2. Click **New repository**. Name it `sulaiha-granites`. Set it to **Public**.
   Click **Create repository**.
3. On the new repo page, click **uploading an existing file**, then drag in
   every file and folder from this project (`index.html`, `about.html`,
   `css/`, `js/`, `images/`, all of it). Click **Commit changes**.
4. Go to the repo's **Settings → Pages**.
5. Under "Build and deployment", set **Source** to "Deploy from a branch",
   branch `main`, folder `/ (root)`. Click **Save**.
6. Wait 1–2 minutes, then refresh — GitHub shows your live link, something
   like: `https://your-username.github.io/sulaiha-granites/`
7. That's it — share that link as your website address. Any time you edit a
   file and re-upload it (or use "Edit" directly on GitHub), the live site
   updates automatically within a minute.

## Alternative — Netlify (drag-and-drop, no GitHub needed)

1. Go to [app.netlify.com/drop](https://app.netlify.com/drop)
2. Drag the whole project folder onto the page.
3. Netlify gives you a live link immediately (e.g.
   `https://sulaiha-granites.netlify.app`). You can rename it for free in
   **Site settings → Change site name**.
4. To update the site later, drag the updated folder onto the same page again.

## Using your own domain name later (optional, paid)

A domain like `sulaihagranites.in` or `sulaihagranites.com` (roughly
₹500–₹1,200/year from providers like GoDaddy, Hostinger, or Google Domains)
can be pointed at either GitHub Pages or Netlify for free — both have a
"Custom domain" setting under Site/Repo Settings that walks you through it.
The hosting itself stays free either way; only the domain name is a paid,
optional extra.
