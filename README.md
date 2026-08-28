# Mehedee Hasan Shikhon — Portfolio

A single self-contained `index.html` (all CSS, fonts link, and images are inlined — no build step, no dependencies).

## Deploy: GitHub → Vercel

**1. Create the GitHub repo**

```bash
mkdir mehedee-portfolio && cd mehedee-portfolio
# copy index.html into this folder
git init
git add index.html
git commit -m "Initial portfolio"
```

Create a new empty repository on GitHub (no README/license, so it stays empty), then:

```bash
git branch -M main
git remote add origin https://github.com/<your-username>/mehedee-portfolio.git
git push -u origin main
```

**2. Deploy on Vercel**

1. Go to [vercel.com](https://vercel.com) and sign in with your GitHub account.
2. Click **Add New → Project**.
3. Select the `mehedee-portfolio` repo you just pushed.
4. Framework preset: choose **Other** (it's plain HTML, no framework). Leave Build Command and Output Directory blank — Vercel will serve `index.html` as-is.
5. Click **Deploy**. It takes under a minute.

You'll get a live URL like `mehedee-portfolio.vercel.app`. You can add a custom domain later from the project's **Settings → Domains** tab if you buy one.

## Updating the site later

Edit `index.html`, then:

```bash
git add index.html
git commit -m "Update portfolio"
git push
```

Vercel automatically redeploys on every push to `main`.

## Notes

- All images (BunnyLoops, Skarion, BRAC University logos) are embedded directly in the HTML as base64 — nothing external to break or go missing.
- Google Fonts (Unbounded, Manrope, JetBrains Mono) load from `fonts.googleapis.com` — this needs an internet connection to render correctly, which any live deployment will have.
- No environment variables, API keys, or backend — it's a static page.
