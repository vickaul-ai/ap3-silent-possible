# Corporate website embed (deferred)

**Status:** Not planned for current release.

AP3 Silent Possible is hosted on **Vercel only**. See **[DEPLOYMENT.md](./DEPLOYMENT.md)** for deploy steps.

---

## If you revisit silencelaboratories.com later

Rough checklist (not maintained):

- Pick path (e.g. `/ap3-studio/`) and nav placement
- Set `SITE_CONFIG.canonicalOrigin` in `index.html`
- Update `sitemap.xml` and `robots.txt` to corporate origin
- Load corporate GTM / consent banner
- Optional: `?embed=1` iframe mode (already supported in the app)
- Brand overrides via [assets/embed-overrides.css](../assets/embed-overrides.css)

The repo already includes skip-link, OG meta, and `embed-mode` CSS for iframe use when needed.
