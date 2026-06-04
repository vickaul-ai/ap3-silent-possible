# AP3 Silent Possible

A static HTML click-through wireframe for AP3 use cases.

This is not a real AP3 implementation. It is a developer/product explainer that simulates AP3 sessions for personal-agent and enterprise-agent workflows:

- Quiet Quorum
- Couplet
- Eldercare decision and cost split
- Personal admin proxy
- Confidential diligence
- Privacy-preserving fraud consortium
- Sanctions / PEP screen, open finance consent match, cross-border compliance
- Neighborhood mutual aid
- Hermes silent-compute skill
- Calendar soft-match, skill overlap, introducer dedup, roommate chore quorum (builder track)

**15 use cases** in the atlas. Feature work through Phase **4** is shipped; hosting is **Vercel only** ([DEPLOYMENT.md](docs/DEPLOYMENT.md)).

**Try:** `?case=skill-overlap` · `?embed=1` (compact chrome) · `localStorage.ap3AnalyticsDebug=1` for event logs.

## Documentation (start here for PMs)

| Document | Purpose |
|----------|---------|
| [docs/SHARE-BRIEF.md](docs/SHARE-BRIEF.md) | User-facing brief to send with the live website link |
| [docs/PRODUCT-BRIEF.md](docs/PRODUCT-BRIEF.md) | Purpose, design principles, priorities, vocabulary, how to extend |
| [docs/IMPLEMENTATION-PLAN.md](docs/IMPLEMENTATION-PLAN.md) | Phased roadmap (Phases 0–5) with acceptance criteria |
| [docs/TODO.md](docs/TODO.md) | Master checklist — track delivery task-by-task |
| [docs/FACILITATION-GUIDE.md](docs/FACILITATION-GUIDE.md) | 20-minute workshop script for sales and community |
| [docs/ANALYTICS.md](docs/ANALYTICS.md) | GTM/dataLayer event catalog and UTM conventions |
| [docs/DEPLOYMENT.md](docs/DEPLOYMENT.md) | **Vercel deploy** (primary hosting) |
| [docs/SITE-INTEGRATION.md](docs/SITE-INTEGRATION.md) | Corporate site embed — deferred |

## Local Preview

Open `index.html` directly in a browser, or serve the folder with any static server:

```bash
python3 -m http.server 8080
```

## Deployment (Vercel)

**Production:** https://ap3-silent-possible.vercel.app

Static site from the repository root — no build command. Project is linked under `vickaul/ap3-silent-possible`.

```bash
vercel --prod
```

Details: [docs/DEPLOYMENT.md](docs/DEPLOYMENT.md).

Corporate website embed is **not** in scope for now; outbound links to [Silent Compute](https://silencelaboratories.com/silent-compute) remain for GTM.

## Source References

- AP3 overview: https://ap3-protocol.org/
- AP3 roles: https://ap3-protocol.org/roles/
- AP3 service provider flow: https://ap3-protocol.org/use-cases/monetize-with-service-provider/
- AP3 playground: https://playground.ap3-protocol.org/
- Silent Compute: https://silencelaboratories.com/silent-compute
