---
name: OpenAI Agents SDK
repo: openai/openai-agents-python
license: MIT
stars: 27000
last_verified: 2026-06-23
liveness: active
edena_tier: yellow
autonomy: L3-L5
track: entrepreneurship
healthcare_fit: adaptable
verdict: adopt
---

# OpenAI Agents SDK

**Repo:** [`openai/openai-agents-python`](https://github.com/openai/openai-agents-python) · **License:** MIT · **Stars:** ~27k · **Verified:** 2026-06-23

## EDENA Tier: 🟡 Yellow · Autonomy: L3–L5

## Claim vs. Proof
- **Claims:** "Lightweight, powerful framework for multi-agent workflows"; provider-agnostic (100+ LLMs); includes agents, handoffs, guardrails, tracing.
- **Proof:** ✅ **EXECUTED** — `pip install openai-agents` succeeded; `import agents` works (v0.17.6). 783 Python files, 487 docs, `examples/` present. The only candidate in v1 confirmed by actual install + import, not just structure.

## Nurse-entrepreneur use case
A clean, well-documented starting framework for building multi-agent workflows with built-in **guardrails** and **handoffs** (agent-to-agent + agent-to-human). Good default for a founder who wants a supported, simple SDK.

## Healthcare contextualization
Adaptable. The built-in guardrails concept maps to EDENA gating, though you must define the rules. Not clinical out of the box.

## PHI / safety boundary
Yellow — capable of action, tool use, and handoffs. Guardrails are developer-defined, not automatic. No PHI without governance.

## Florence-X / EDENA note
"Guardrails + handoffs" is structurally close to "agents propose, humans judge." L3–L5 depending on orchestration depth.

## Verdict: ADOPT
The most verifiable entry (install + import confirmed) and a clean, supported on-ramp to real frameworks.
