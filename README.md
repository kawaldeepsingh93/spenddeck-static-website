# SpendDeck Website

Static marketing and legal site for the [SpendDeck](https://github.com/devkawal/spenddeck-mobile-app) mobile app. Matches the app's dark UI with carbon background, hot pink accents, and electric lime highlights.

## Pages

| Page | URL | Purpose |
|------|-----|---------|
| Landing | `index.html` | App overview, features, screenshots, Play Store CTA |
| Privacy Policy | `privacy.html` | **Required** for Google Play Console |
| Terms of Service | `terms.html` | Legal terms for app usage |

## Play Console checklist

Use these URLs after deploying:

- **Privacy policy URL:** `https://kawaldeepsingh93.github.io/spenddeck-static-website/privacy.html`
- **Contact email:** planetkawal@gmail.com
- **App name:** SpendDeck
- **Category:** Finance
- **Package:** `com.devkawal.spenddeckmobileapp`

### Suggested store copy

**Short description (80 chars):**
> Track every card, one runway, zero guesswork. Monitor limits and monthly spend.

**Full description:**
> Track every card, one runway, zero guesswork. SpendDeck helps you monitor limits, log expenses, and stay ahead of your monthly spend.
>
> Stack all your cards in one deck, watch your global runway, get burn-rate insights and category breakdowns, and log expenses in seconds. Budget alerts notify you at 80% and 90% of your limits. All data stays on your device — no account required.

## Local preview

```bash
cd /Users/binnyrana/Documents/code/spenddeck-website
npx serve .
# or: python3 -m http.server 8080
```

Open http://localhost:3000 (serve) or http://localhost:8080 (python).

## Deploy (GitHub Pages)

This is a plain static site — no build step. GitHub Actions deploys automatically on every push to `main`.

### One-time setup

1. Push this repo to GitHub (`kawaldeepsingh93/spenddeck-static-website`).
2. Open **Settings → Pages** in the GitHub repo.
3. Under **Build and deployment → Source**, choose **GitHub Actions**.
4. Push to `main` (or run the **Deploy to GitHub Pages** workflow manually under **Actions**).

After the workflow finishes, the site is live at:

- **Home:** https://kawaldeepsingh93.github.io/spenddeck-static-website/
- **Privacy:** https://kawaldeepsingh93.github.io/spenddeck-static-website/privacy.html
- **Terms:** https://kawaldeepsingh93.github.io/spenddeck-static-website/terms.html

### Custom domain (optional)

Add a `CNAME` file with your domain (e.g. `spenddeck.app`), then configure DNS and enable the custom domain under **Settings → Pages**. Use `https://your-domain.com/privacy.html` in Play Console.

### Other hosts

- **Netlify** — drag-and-drop the folder or connect the repo
- **Vercel** — `vercel deploy`
- **Cloudflare Pages** — connect repo, no build command

## Structure

```
spenddeck-website/
├── index.html          # Landing page
├── privacy.html        # Privacy policy
├── terms.html          # Terms of service
├── css/styles.css      # Shared styles (app palette)
├── js/main.js          # Mobile nav toggle
└── assets/
    ├── images/         # Icon, favicon, feature graphic
    └── screenshots/    # Phone screenshots from store-assets
```

## Play Store link

All Google Play links open in a new tab (`target="_blank"` + `rel="noopener noreferrer"`):

```
https://play.google.com/store/apps/details?id=com.devkawal.spenddeckmobileapp
```

Update this URL in `index.html` if the listing ID changes.
