# Pioneer Oil — Website Setup Guide

## File Structure

Put your files in this layout:

```
pioneer-oil/
├── index.html        ← Home page
├── pricing.html      ← Pricing tiers
├── contact.html      ← Scheduling form
├── style.css         ← Shared styles
└── assets/
    └── logo.png      ← Your logo file (rename yours to exactly this)
```

---

## Step 1 — Add Your Logo

1. Rename your logo file to `logo.png`
2. Create a folder called `assets` inside your project folder
3. Put `logo.png` inside `assets/`

> **Tip:** If you can get a version of your logo with a **transparent background** (a PNG with no white box), it will look cleaner on the dark navy navigation bar and footer. Ask your logo designer or use a free tool like **remove.bg** to strip the background.

---

## Step 2 — Set Up Formspree (Free Contact Form)

Formspree handles form submissions for free static sites (free tier: 50 submissions/month).

1. Go to **https://formspree.io** and create a free account
2. Click **"New Form"** and give it a name like "Pioneer Oil Scheduling"
3. Copy your **Form ID** (looks like `xabc1234`)
4. Open `contact.html` and find this line near the top of the `<form>` tag:

   ```html
   action="https://formspree.io/f/YOUR_FORM_ID"
   ```

5. Replace `YOUR_FORM_ID` with your actual ID, for example:

   ```html
   action="https://formspree.io/f/xabc1234"
   ```

6. Formspree will email you every time someone fills out the form.

---

## Step 3 — Push to GitHub

1. Go to **https://github.com** and create a free account (if you don't have one)
2. Click **"New Repository"**
3. Name it exactly: `pioneer-oil` (or any name you want)
4. Leave it **Public**
5. Click **"Create Repository"**

Then upload your files. The easiest way if you're not using Git:

- On your new repo page, click **"uploading an existing file"**
- Drag all your files into the uploader:
  - `index.html`
  - `pricing.html`
  - `contact.html`
  - `style.css`
  - The `assets/` folder with `logo.png` inside it
- Click **"Commit changes"**

---

## Step 4 — Enable GitHub Pages

1. In your repo, click **"Settings"** (top tab)
2. Scroll down to **"Pages"** in the left sidebar
3. Under **"Branch"**, select `main` and click **"Save"**
4. Wait 1–2 minutes, then your site will be live at:

   ```
   https://YOUR-GITHUB-USERNAME.github.io/pioneer-oil/
   ```

That's it! Share that link wherever you'd like.

---

## Step 5 — When You Get a Real Domain

When you're ready to pay for a domain (e.g., pioneeroil.com):

1. Buy the domain from any registrar (Namecheap, Porkbun, Google Domains)
2. In your repo Settings → Pages, enter your custom domain
3. At your registrar, add a CNAME record pointing to `YOUR-USERNAME.github.io`

GitHub has a full guide at: https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site

---

## Making Updates

To change prices, text, or anything else:

- Go to your repo on GitHub
- Click the file you want to edit
- Click the pencil icon (Edit)
- Make your changes and click **"Commit changes"**
- The site updates in about 60 seconds

---

## Quick Reference — What Each File Does

| File | Purpose |
|------|---------|
| `index.html` | Home page — hero, how it works, about, pricing preview |
| `pricing.html` | Full pricing tier cards with details |
| `contact.html` | Scheduling form with Formspree integration |
| `style.css` | All styles shared across every page |
| `assets/logo.png` | Your logo, used in nav and footer |
