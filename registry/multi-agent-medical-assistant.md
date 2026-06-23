---
name: Multi-Agent Medical Assistant
repo: souvikmajumder26/Multi-Agent-Medical-Assistant
license: Apache-2.0
stars: 906
last_verified: 2026-06-23
liveness: active
edena_tier: red
autonomy: L3
track: healthcare
healthcare_fit: clinical-risk
verdict: watch
---

# Multi-Agent Medical Assistant

**Repo:** [`souvikmajumder26/Multi-Agent-Medical-Assistant`](https://github.com/souvikmajumder26/Multi-Agent-Medical-Assistant) · **License:** Apache-2.0 · **Stars:** ~906 · **Verified:** 2026-06-23

## EDENA Tier: 🔴 Red (cautionary exemplar) · Autonomy: L3

## Claim vs. Proof
- **Claims:** "GenAI-powered multi-agentic medical **diagnostics** and healthcare research assistance chatbot… designed for healthcare professionals, researchers **and patients**." Disease detection / computer vision.
- **Proof:** ✅ Verified it's real and properly licensed (Apache-2.0, `requirements.txt`, Dockerfile, LangGraph-based, has a `guardrails` topic). ⚠️ **Strong claim, unproven safety:** "diagnostics" + "patients" is a patient-facing diagnostic claim with **no clinical validation evidence.** This is the highest-risk class of claim.

## Nurse-entrepreneur use case
**Study, do not deploy.** Use it to understand how a multi-agent diagnostic chatbot is architected — and precisely why such a system must never reach a patient without a clinician gate.

## Healthcare contextualization
Clinical-risk, patient-facing, diagnostic. The exact category EDENA exists to govern.

## PHI / safety boundary
🔴 **Cautionary listing — NOT endorsed for use.** Patient-facing diagnosis by an unvalidated agent is unsafe. Never deploy to patients. Never enter PHI. A licensed clinician must own every output. This card exists to make the boundary visible.

## Florence-X / EDENA note
The teaching case of the registry: "Agents propose. Humans judge. Nurses steward." This is what *must* be gated. Listed Red precisely to demonstrate the disclaimer in action.

## Verdict: WATCH (cautionary)
Architecturally instructive; do not deploy clinically. The registry's worked example of a 🔴 boundary.
