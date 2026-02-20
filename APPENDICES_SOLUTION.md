# The Solution — OMXUS, Ring, VexConnect, VexID

*What exists. What it does. Where to find it.*

---

## Overview

The books diagnose enclosure failures. The solution is not theory — it is built. Identity without state or corporate authority. Emergency response that arrives in 60 seconds, not 20 minutes. Community that sees you before harm is done.

---

## Identity: OMXUS HER + VexID

**OMXUS HER (Human Existence Record)** — On-chain.
- One soulbound token per verified human. Non-transferable.
- 3-vouch verification: three already-verified humans must vouch for you.
- Trust score (0–1000) propagates through the network.
- Ripple responsibility: bad behaviour by a vouched identity ripples 1/3 to those who vouched.

**VexID** — Identity API (Cloudflare Workers, R2).
- OMXUS-style vouching and reputation.
- Contribution tracking, identity hashing, human directory.
- Works without full on-chain deployment.

You're never truly alone. The three people who vouched for you — they see you. Isolation, the abuser's main tool, becomes impossible when mutual visibility is the default.

---

## Emergency: The Ring + Civic Proximity

**The problem:** Centralised dispatch has irreducible latency. Call processing (60–90 sec) → dispatch (30–60 sec) → travel (4+ min) = 7–14 minutes median. For cardiac arrest, haemorrhage, choking, violence — those minutes determine survival.

**The ring:** NFC ring. Tap it. Alert goes to nearby verified humans via mesh. They choose to respond or not. Target: first contact in 60 seconds. Triple Zero (000) continues operating; the ring is a supplementary layer.

**VexConnect** — BLE mesh (iOS). GATT server/client, packet relay, 7-hop TTL, store-and-forward, deduplication. The mesh that carries the alert when someone taps.

**Evidence:** DV (domestic violence) safety buttons — direct personal alerts that work. GoodSAM, PulsePoint, Hatzalah — civilians respond when alerted; survival doubles when a trained bystander receives a personal alert. The French *obligation de porter secours* (Code pénal Art. 223-6): you can be prosecuted for not helping someone in danger. The ring doesn't require legal obligation — it relies on a tiny fraction of people volunteering occasionally.

**Coverage math (Australia):** ~1 in 4,600 people per day need emergency response (~8% per year). If 1 in 10 people will respond once a year when alerted, supply exceeds demand. The Mathematical Foundations paper: in 100,000 verified humans, ~20–50 emergencies/day. The constraint is willingness, not density.

---

## DV: Why the Abuser's Playbook Breaks

**Why DV exists:**
- Isolation — abuser cuts victim off from community
- Secrecy — no one sees what happens inside
- Slow response — police take 20+ mins; damage done
- Victim not believed — system is adversarial
- Abuser controls the narrative

**Token system:**
- **Transparency** — community sees patterns. Person stops coming to meetings, stops responding. Red flags visible.
- **Safety button** — instant. Local responders. 60 seconds, not 20 minutes.
- **Vouch network** — the three who vouched for you see you. You're never truly alone.
- **Can't isolate** — mutual visibility breaks the abuser's main tool.
- **Community response** — not cops who don't believe you. People who know you.

| Abuser tactic | Current system | Token system |
|---------------|-----------------|--------------|
| Isolate victim | Easy | Impossible — community sees |
| Control narrative | Works | Can't — transparency |
| Victim not believed | Common | Vouch network knows them |
| Slow response | 20+ mins | 60 seconds |
| Hide abuse | Secrecy default | Visibility default |

Safety buttons work. Fast response works. Community connection works. The current system has all three broken. The token system has all three fixed. This isn't incremental improvement. It's structural elimination.

---

## Infrastructure

- **OperationsController** — MeshNode, Keeper, Gateway, Emergency provider registration; uptime-weighted payments.
- **VoteAnchor** — Merkle roots to Bitcoin; vote recording with MMR proofs.
- **OMXUSCommons** — Revenue sharing; 70% of verification fees to HER holders.

---

## Where to Find It

- **Papers:** omxus.com/research
- **Wiki:** wiki.omxus.com (80+ articles)
- **Deployed contracts:** See FEATURE_INVENTORY in omxus-main
