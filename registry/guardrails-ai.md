---
name: Guardrails AI
repo: guardrails-ai/guardrails
license: Apache-2.0
stars: 7035
last_verified: 2026-06-23
liveness: active
edena_tier: green
autonomy: L2
track: governance
healthcare_fit: adaptable
verdict: adopt
---

# Guardrails AI

**Repo:** [`guardrails-ai/guardrails`](https://github.com/guardrails-ai/guardrails) · **License:** Apache-2.0 · **Stars:** ~7.0k · **Verified:** 2026-06-23

## EDENA Tier: 🟢 Green → 🟡 Yellow · Autonomy: L2

## Claim vs. Proof
- **Claims:** Structural, type, and quality guarantees for LLM outputs; validate and correct model responses.
- **Proof:** ✅ **EXECUTED** — `pip install guardrails-ai` succeeded and `import guardrails` works. 351 Python files, `pyproject.toml`, active commits (last push today).

## Nurse-entrepreneur use case
The "make the AI's output trustworthy" layer. A nurse founder building any patient-education or business tool can enforce that outputs match a required schema, stay on-topic, and reject unsafe content — *before* a human ever sees them.

## Healthcare contextualization
Adaptable and important: output validation is a prerequisite for any responsible healthcare-adjacent tool. It does not make a tool clinical — it makes outputs checkable.

## PHI / safety boundary
Green as a library (it validates text, holds no PHI itself). Becomes part of a Yellow system when wired into an acting agent. Use it to *enforce* the human gate, not replace it.

## Florence-X / EDENA note
This is EDENA's doctrine in code: "agents propose, [a guardrail checks], humans judge." A literal technical substrate for the Stewardship Lens.

## Verdict: ADOPT
Foundational governance primitive. Every Yellow/Orange agent in the registry is safer wrapped in something like this.
