# EDENA Governance — Tiering Rubric

> The registry exists to demonstrate governance in public. The tier is the product.

## The human-gate principle

**Agents propose. Humans judge. Nurses steward.** No agent in this registry is endorsed to make autonomous clinical decisions. The higher the autonomy and the closer to patient care, the heavier the required human gate.

## EDENA tiers

| Tier | Meaning | Typical traits | Governance posture |
|------|---------|----------------|--------------------|
| 🟢 **Green** | Low risk | Prompts/templates, read-only research, no PHI, human runs each step | Use freely; basic hygiene |
| 🟡 **Yellow** | Moderate risk | Multi-agent frameworks that can act, memory, tool use | Bound autonomy: trigger + goal + evaluation + stop + human review |
| 🟠 **Orange** | Elevated risk | Clinical content, integrations, connectors, healthcare-adaptable | Mandatory human gate; no PHI without governance; not clinically validated |
| 🔴 **Red** | Highest risk | Patient-facing, diagnostic claims, autonomous clinical action | Cautionary listing only — demonstrates what MUST be gated; never deploy without a clinician in the loop |

## Autonomy levels (Hermes L0–L7)

Governance scales with autonomy, access, memory, orchestration, integration, and async execution.

- **L0–L1** Beginner (prompts, single-shot) → Green
- **L2** Soul/Memory → Yellow
- **L3** Skills/Models → Yellow→Orange
- **L4** Integrator / MCP / connectors → Orange
- **L5** Orchestration → Red
- **L6** Builder, async scheduled execution → Red
- **L7** Agentic OS → Red+ (Strategic Autonomy)

## Card fields

Every registry card carries: license, stars, liveness, EDENA tier, autonomy level, claim-vs-proof, healthcare-fit, nurse-entrepreneur use case, PHI/safety boundary, and a verdict (Adopt / Pilot / Watch / Avoid).

## License note

Some listed resources have **no open-source license**. These are linked as reading resources only — do not fork or redistribute their content. Each card flags license status explicitly.
