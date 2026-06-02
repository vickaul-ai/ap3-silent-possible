# AP3 Silent Possible — Facilitation Guide

**Duration:** 20 minutes  
**Audience:** Product, sales, partners, or builder community  
**Goal:** Spark conversation about agent privacy — then hand off to real protocol (Playground) and production compute (Silent Compute)

---

## Before the session

- [ ] Open the studio locally or on staging (`index.html`)
- [ ] Open [AP3 Playground](https://playground.ap3-protocol.org/) in a second tab
- [ ] Skim [PRODUCT-BRIEF.md](./PRODUCT-BRIEF.md) for vocabulary
- [ ] Pick **one primary use case** (recommendations below)
- [ ] Optional: pre-load share link `?case=<id>`

---

## Recommended flows by audience

| Audience | Primary case | Path chip | Close with |
|----------|--------------|-----------|------------|
| Personal / builders | Skill overlap or Quiet Quorum | I'm building agents | Hermes SKILL stub + Playground |
| Enterprise / bank | Sanctions PEP or Fraud consortium | Enterprise / regulated | Silent Compute + anti-fraud page |
| Mixed workshop | Couplet or Calendar soft-match | Explore scenarios | Builder brief export |

---

## 20-minute script

### 1. Frame the problem (3 min)

**Say:** "Personal and enterprise agents are getting good at memory and tools. The weak point is **collaboration** — they still solve coordination by copying full context into shared chat."

- Show hero **stack strip**: agents → AP3 → Silent Compute
- Point at status pill: *this page is imagination; Playground is real crypto*

**Ask:** "Where would leaking a full list, calendar, or CRM export hurt you?"

---

### 2. One use case, deep (5 min)

1. Open **Use-case atlas** (or `?case=` link)
2. Read **discussion prompt** on the card aloud
3. Click **Load simulator** → **Run**
4. Walk through stages: Discovery → Compatibility → `init` → `msg2` → Result
5. Open **Debate toggle**: Without AP3 vs With AP3

**Say for PSI cases:** "Only the **initiator** learns the intersection. The receiver helps compute but doesn't get the other side's full query."

---

### 3. Protocol truth (5 min)

Switch to [AP3 Playground](https://playground.ap3-protocol.org/).

1. Run **Compatibility lab** (optional: show PIR vs PSI mismatch)
2. Run **successful PSI** (bank sanctions story if enterprise audience)
3. Show **Inspector**: AgentCards, envelopes, directives

**Say:** "The studio tells the product story. The Playground proves the wire format."

---

### 4. Production path (4 min)

Scroll to **Silent Compute** section on the studio page.

- Walk the **mapping table** (PSI → Secure Match, etc.)
- For enterprise: mention [anti-fraud consortium](https://silencelaboratories.com/usecases/anti-fraud)

**Say:** "AP3 is the agent-facing protocol surface. Silent Compute is where regulated institutions run MPC at scale with audit and purpose binding."

**CTA:** Book a call / follow-up — not a commitment to architecture on the spot.

---

### 5. Capture interest (3 min)

- **Builders:** copy Hermes SKILL.md or OpenClaw AgentCard; fill **Builder brief** → Download Markdown
- **Enterprise:** note use case + compliance angle in CRM
- **Everyone:** copy **share link** on a card for async follow-up

**UTM tip for influencers:** `?case=skill-overlap&utm_source=...` (append your campaign params to the studio URL)

---

## Facilitator notes

| Pitfall | Avoid |
|---------|--------|
| Claiming live crypto on the studio | Always point to Playground |
| Saying receiver "learns nothing" in PSI | Receiver runs crypto; **output asymmetry** is what matters |
| Skipping evidence bundle | Trust story = directives + receipts, not magic |
| Enterprise → only AP3 | Always mention Silent Compute for production |

---

## Optional extensions (+10 min each)

- **Long-tail discovery:** `#discovery` section + marketplace narrative
- **Builder hackathon:** `#builders` + challenge to ship one AP3 skill in 30 days
- **Workshop breakout:** pairs pick different cards, compare minimal outputs

---

## Feedback to product

After sessions, log:

- Which use case sparked the most discussion?
- Did people open Playground?
- Enterprise vs builder ratio?
- Objections (crypto trust, latency, A2A adoption)?

Update [TODO.md](./TODO.md) and card **discussion prompts** based on what landed.

---

## Changelog

| Date | Change |
|------|--------|
| Jun 2026 | Initial 20-minute facilitation script |
