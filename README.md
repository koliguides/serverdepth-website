# ServerDepth Studio Website

The marketing site for [ServerDepth](https://github.com/koliguides) — a premium FiveM script studio building QBox and QBCore resources.

Single-page static HTML site. No build step, no JS framework, no dependencies. Just `index.html` and CSS/JS inline.

## Live preview

The published preview is hosted via Hyperagent for now. To put it on a real domain, follow the Deploy section below.

## What's on it

- Hero with stats
- Products grid (4 scripts) — each links to a detailed section
- "Server Depth Bundle" pitch
- 4 expanded product detail sections with feature lists, tech badges, and pricing
- "Why ServerDepth" pillars
- 3-step process
- FAQ accordion
- Final CTA + footer

All product images are loaded from Hyperagent's CDN. Replace them with your own (Tebex thumbnails, in-game screenshots, etc.) by editing the `<img src>` attributes in `index.html`.

## Edit before sharing

Update these placeholders to your real contact info:
- `hello@serverdepth.io` — email
- `https://discord.gg/serverdepth` — Discord invite

Search-and-replace in `index.html`. Both appear in the nav, the CTA section, and the footer.

## Deploy to a real domain (free)

### Option 1 — Vercel (recommended, easiest)

1. Sign up at [vercel.com](https://vercel.com) (free tier is plenty)
2. Click "Add New Project" → "Import Git Repository"
3. Connect your GitHub account and select `serverdepth-website`
4. Vercel auto-detects it as a static site. Click "Deploy"
5. Done — Vercel gives you a `serverdepth-website-koliguides.vercel.app` URL
6. To add a custom domain: Project Settings → Domains → Add → enter `serverdepth.dev` (or whatever you bought)
7. Vercel tells you the DNS records to add at your domain registrar (Namecheap, Cloudflare, etc.)
8. Add them, wait 5-30 minutes, done

Every time you push to `main` on this repo, Vercel re-deploys automatically. No manual steps.

### Option 2 — Netlify (also free, similar)

1. Sign up at [netlify.com](https://netlify.com)
2. "Import from Git" → select this repo
3. Build settings: leave blank (it's static)
4. Deploy → custom domain setup similar to Vercel

### Option 3 — GitHub Pages (free, slightly more work)

1. Repo Settings → Pages → Source: `main` branch, root folder
2. GitHub serves at `koliguides.github.io/serverdepth-website`
3. For custom domain: add a `CNAME` file with your domain, then point DNS

## Domains

Suggested options:
- `serverdepth.dev` — clean, dev-focused, ~$12/yr
- `serverdepth.io` — popular for studios, ~$45/yr
- `serverdepth.gg` — gaming-focused, ~$30/yr

Buy at Namecheap or Cloudflare Registrar (cheapest, no markup).

## Updates

Edit `index.html` and push. Vercel/Netlify rebuilds in ~30 seconds.

To add a new product:
1. Add a new card to the `<section id="products">` block
2. Add a new detail section with id `detail-<name>`
3. Update the bundle pricing math if relevant

## License

The website source is yours to modify for ServerDepth's use. The script repos it links to retain their own proprietary licenses (single-server use).
