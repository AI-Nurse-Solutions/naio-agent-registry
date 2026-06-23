---
name: LLM Guard
repo: protectai/llm-guard
license: MIT
stars: 3103
last_verified: 2026-06-23
liveness: active
edena_tier: yellow
autonomy: L2
track: governance
healthcare_fit: adaptable
verdict: adopt
---

# LLM Guard

**Repo:** [`protectai/llm-guard`](https://github.com/protectai/llm-guard) · **License:** MIT · **Stars:** ~3.1k · **Verified:** 2026-06-23

## EDENA Tier: 🟡 Yellow · Autonomy: L2

## Claim vs. Proof
- **Claims:** Security toolkit for LLM interactions — input/output scanning for prompt injection, data leakage, toxicity, and PII.
- **Proof:** ✅ Verified — 217 Python files, `pyproject.toml`, MIT, active (last push 2025-12-15). Real scanner suite.

## Nurse-entrepreneur use case
The **PII/PHI-leak tripwire.** For any nurse founder handling user input, this scans for and redacts sensitive data and detects prompt-injection attempts — the most direct technical support for the registry's "no PHI without governance" rule.

## Healthcare contextualization
Highly relevant: PII/PHI detection and redaction is a core healthcare-safety control. Note last push is ~6 months old — active but verify scanner currency before relying on it.

## PHI / safety boundary
Yellow — it is a *detection* aid, not a compliance guarantee. It reduces PHI-leak risk but does NOT make a system HIPAA-compliant. A detected leak still requires human governance response.

## Florence-X / EDENA note
The "scan before it reaches a human or a log" control. Completes the governance trio: structure (Guardrails AI) + conversation (NeMo) + security/PII (LLM Guard).

## Verdict: ADOPT
The PHI/security-scanning leg of the governance toolkit — directly serves NAIO's no-PHI discipline.
