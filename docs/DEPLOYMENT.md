# Deployment — Vercel (primary)

**Hosting decision:** This studio ships on **Vercel only** for now. Embedding on silencelaboratories.com is **out of scope** unless product revisits it later.

---

## Quick deploy

### Git connected (recommended)

1. Import the repo in [Vercel](https://vercel.com/new).
2. **Framework preset:** Other (static).
3. **Root directory:** repository root (where `index.html` lives).
4. **Build command:** leave empty.
5. **Output directory:** `.` or leave default — the site is a single `index.html` plus `assets/`, `docs/` (docs are not served unless you want them; only static assets matter).

Deploy. Vercel serves `index.html` at `/`.

**Current production:** https://ap3-silent-possible.vercel.app

### CLI

```bash
cd /path/to/ap3-silent-possible
npx vercel
# production:
npx vercel --prod
```

Requires [Vercel CLI](https://vercel.com/docs/cli) and project link.

---

## What gets deployed

| Path | Served |
|------|--------|
| `index.html` | Yes — main app |
| `assets/**` | Yes — OG image, embed CSS stub |
| `robots.txt`, `sitemap.xml` | Yes |
| `vercel.json` | Config only |
| `docs/**` | Yes as static files (optional; not linked from app) |

No build step. No environment variables required for the app to run.

---

## After first production deploy

1. **Note your production URL** (e.g. `https://ap3-silent-possible.vercel.app` or a custom domain).

2. **Update [sitemap.xml](../sitemap.xml)** — replace every `https://ap3-silent-possible.vercel.app` with your real origin if different.

3. **Update [robots.txt](../robots.txt)** — set `Sitemap:` to your absolute sitemap URL.

4. **Optional custom domain** — Vercel project → Settings → Domains. Then refresh sitemap/robots.

`SITE_CONFIG` in `index.html` can stay with empty `canonicalOrigin`; the app uses `window.location.origin` for OG URLs and canonical tags automatically on Vercel.

Only set `canonicalOrigin` if you add a custom domain and want social crawlers to always see that host:

```javascript
const SITE_CONFIG = {
  canonicalOrigin: "https://your-custom-domain.com",
  canonicalPath: "/",
  ogImagePath: "/assets/og/default.svg"
};
```

---

## Configuration ([vercel.json](../vercel.json))

- `cleanUrls: true`
- Cache headers on `/assets/*` and images

No redirects required for a single-page site.

---

## Preview vs production

| Environment | Use |
|-------------|-----|
| Preview (PR branches) | Review copy/UI changes |
| Production | Share externally, workshops, influencers |

Share links: `https://<production>/?case=skill-overlap&utm_source=...`

See [ANALYTICS.md](./ANALYTICS.md) for UTM conventions.

---

## Analytics on Vercel

The app pushes to `window.dataLayer`. To collect events:

- Add **Vercel Web Analytics** or inject **GTM** via Vercel's script in project settings, or
- Add a small script tag in `index.html` (team choice).

Debug locally or on preview:

```javascript
localStorage.setItem("ap3AnalyticsDebug", "1");
```

---

## Out of scope (for now)

- iframe embed on silencelaboratories.com
- Silence corporate nav/footer rebrand
- 301 from Vercel → corporate domain

See [SITE-INTEGRATION.md](./SITE-INTEGRATION.md) if the corporate embed is revived later.

---

## Changelog

| Date | Change |
|------|--------|
| Jun 2026 | Vercel-only deployment documented; corporate site deferred |
