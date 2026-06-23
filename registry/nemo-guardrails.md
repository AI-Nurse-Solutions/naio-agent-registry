---
name: NeMo Guardrails
repo: NVIDIA-NeMo/Guardrails
license: Apache-2.0
stars: 6514
last_verified: 2026-06-23
liveness: active
edena_tier: yellow
autonomy: L2
track: governance
healthcare_fit: adaptable
verdict: adopt
---

# NeMo Guardrails

**Repo:** [`NVIDIA-NeMo/Guardrails`](https://github.com/NVIDIA-NeMo/Guardrails) · **License:** Apache-2.0 · **Stars:** ~6.5k · **Verified:** 2026-06-23

## EDENA Tier: 🟡 Yellow · Autonomy: L2

## Claim vs. Proof
- **Claims:** Programmable guardrails for conversational systems — control dialogue flow, topics, and safety rails.
- **Proof:** ✅ Verified — NVIDIA-maintained, 764 Python files, `pyproject.toml`, active (last push today). (Note: repo moved to the `NVIDIA-NeMo` org — old `NVIDIA/NeMo-Guardrails` path redirects.)

## Nurse-entrepreneur use case
For a founder building a conversational agent (intake bot, education assistant), this enforces "the bot may discuss X, must refuse Y, and must hand off to a human at Z." It encodes conversation-level boundaries declaratively.

## Healthcare contextualization
Adaptable — conversation rails are exactly how you keep a non-clinical assistant from drifting into clinical advice it shouldn't give.

## PHI / safety boundary
Yellow — it governs an interactive/conversational system. Rails are author-defined, not automatic safety. No PHI without governance; rails reduce but don't eliminate risk.

## Florence-X / EDENA note
Conversation-level enforcement of the human gate. Pairs with Guardrails AI (output validation) to cover both *what is said* and *how it is structured*.

## Verdict: ADOPT
The dialogue-safety half of the governance toolkit.
