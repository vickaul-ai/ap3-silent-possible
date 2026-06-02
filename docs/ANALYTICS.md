# AP3 Silent Possible — Analytics

**Purpose:** Define events for GTM / Plausible / Segment on the **Vercel-hosted** studio (or any static host using this `index.html`).

---

## Implementation

The site pushes events to `window.dataLayer` (Google Tag Manager pattern) and logs to the console when `localStorage.ap3AnalyticsDebug === "1"`.

```javascript
localStorage.setItem("ap3AnalyticsDebug", "1"); // enable console logs
```

Silence web team: load GTM container on the parent site or studio page and map these event names to your tags.

---

## Event catalog

| Event name | When fired | Properties |
|------------|------------|------------|
| `studio_page_view` | DOM ready | `path`, `case` (query), `embed` |
| `studio_path_select` | Path chip clicked | `path`: explore \| builder \| enterprise |
| `studio_filter_select` | Atlas filter clicked | `filter` |
| `studio_case_load` | Load simulator / `?case=` | `case_id`, `case_title` |
| `studio_session_run` | Run simulated session | `case_id` |
| `studio_debate_toggle` | Without / With AP3 | `mode`: without \| with |
| `studio_copy_link` | Copy link on card | `case_id` |
| `studio_copy_share_text` | Copy share text | `case_id` |
| `studio_copy_hermes_skill` | Copy Hermes stub | — |
| `studio_copy_openclaw_card` | Copy AgentCard JSON | — |
| `studio_brief_save` | Pilot form submit | `framework`, `track` |
| `studio_brief_download` | JSON or MD export | `format`: json \| md |
| `studio_outbound_click` | Tracked external CTA | `destination`: playground \| github \| silent_compute \| anti_fraud \| book_call |
| `studio_compat_fail_preview` | Preview failure envelope | — |

---

## Outbound link tracking

Links with `data-track-outbound="<destination>"` fire `studio_outbound_click` on click.

Add destinations when new CTAs ship.

---

## UTM conventions (influencers / campaigns)

Base URL (your Vercel production domain, e.g. after `vercel --prod`):

```
https://ap3-silent-possible.vercel.app/
```

| Parameter | Example | Use |
|-----------|---------|-----|
| `utm_source` | `twitter`, `discord`, `newsletter` | Channel |
| `utm_medium` | `social`, `email` | Medium |
| `utm_campaign` | `hermes-ap3-june` | Campaign |
| `utm_content` | `skill-overlap` | Creative / case focus |
| `case` | `skill-overlap` | **Studio-native** — loads scenario (keep alongside UTMs) |

**Example:**

```
https://ap3-silent-possible.vercel.app/?case=skill-overlap&utm_source=twitter&utm_medium=social&utm_campaign=hermes-ap3-june
```

Document campaign links in your influencer brief; do not strip `case` when adding UTMs.

---

## Privacy

- No PII in event payloads by default.
- Pilot brief stays in `localStorage` only unless you add a server submit later.
- Add consent/GTM on Vercel via project script injection or tag manager if required by policy.

---

## Changelog

| Date | Change |
|------|--------|
| Jun 2026 | Initial catalog + dataLayer stub in index.html |
