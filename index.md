# NAIO Agent Registry — Index

**Agents propose. Humans judge. Nurses steward.**

Browse all v1 agents below. See [GOVERNANCE.md](./GOVERNANCE.md) for the EDENA tiering rubric.
⚠️ Inclusion is **not** clinical validation or endorsement. See the [README](./README.md) disclaimer.

> 🧭 **New here, or not a coder?** Start with the [**Agent Framework Field Guide for Nurse Stewards**](./FIELD-GUIDE.md) — what each kind of framework does, its autonomy ceiling, and the *one governance question* to ask. Governance literacy, not a coding course.

## By EDENA tier

### 🟢 Green — low risk, use freely with basic hygiene
| Agent | Repo | License | Autonomy | Use case |
|-------|------|---------|----------|----------|
| [The Agency](./registry/agency-agents.md) | `msitarzewski/agency-agents` | MIT | L1 | Persona agents to run a solo business |
| [Awesome LLM Apps](./registry/awesome-llm-apps.md) | `Shubhamsaboo/awesome-llm-apps` | Apache-2.0 | L1–L2 | 100+ runnable starter apps |
| [GPT Researcher](./registry/gpt-researcher.md) | `assafelovic/gpt-researcher` | Apache-2.0 | L2 | Autonomous research & reports |
| [Awesome Healthcare Agents](./registry/awesome-healthcare-agents.md) | `AgenticHealthAI/...` | ⚠️ NONE | n/a | Field map (reading resource) |

### 🟡 Yellow — bound autonomy with goal + evaluation + stop + human review
| Agent | Repo | License | Autonomy | Use case |
|-------|------|---------|----------|----------|
| [CrewAI](./registry/crewai.md) | `crewAIInc/crewAI` | MIT | L3–L5 | Agent *teams* (Nurse Intelligence Workforce) |
| [LangGraph](./registry/langgraph.md) | `langchain-ai/langgraph` | MIT | L3–L5 | Governance-native orchestration |
| [Agent Starter Pack](./registry/agent-starter-pack.md) | `GoogleCloudPlatform/...` | Apache-2.0 | L4 | Prototype → production deploy |
| [Agno](./registry/agno.md) | `agno-agi/agno` | Apache-2.0 | L4–L5 | Own-your-stack agent platform |
| [OpenAI Agents SDK](./registry/openai-agents-sdk.md) | `openai/openai-agents-python` | MIT | L3–L5 | Guardrails + handoffs framework |

### 🟠 Orange — clinical content; mandatory human gate, no PHI without governance
| Agent | Repo | License | Autonomy | Use case |
|-------|------|---------|----------|----------|
| [OpenClaw Medical Skills](./registry/openclaw-medical-skills.md) | `FreedomIntelligence/...` | ⚠️ NONE | L3 | Clinical skills library (study/pilot only) |

### 🔴 Red — cautionary listing; NOT endorsed for use
| Agent | Repo | License | Autonomy | Use case |
|-------|------|---------|----------|----------|
| [Multi-Agent Medical Assistant](./registry/multi-agent-medical-assistant.md) | `souvikmajumder26/...` | Apache-2.0 | L3 | Patient-facing diagnostic chatbot — **study, do not deploy** |

## 🛡️ Governance & Guardrails — the EDENA substrate (use these to govern the agents above)

> The open-source tools that implement "agents propose, humans judge." A registry that lists agents should also list the tools that keep them safe.

| Tool | Repo | License | Autonomy | Role |
|------|------|---------|----------|------|
| [Guardrails AI](./registry/guardrails-ai.md) | `guardrails-ai/guardrails` | Apache-2.0 | L2 | Output structure/type/quality validation |
| [NeMo Guardrails](./registry/nemo-guardrails.md) | `NVIDIA-NeMo/Guardrails` | Apache-2.0 | L2 | Conversation-flow / topic rails |
| [LLM Guard](./registry/llm-guard.md) | `protectai/llm-guard` | MIT | L2 | PII/PHI-leak + prompt-injection scanning |

### 📜 Governance References — frameworks & standards (read, not run)

> Not software — the regulatory and risk frameworks that define *what* responsible deployment requires. These set the bar the guardrail tools above help you meet. Listed as authoritative references, not endorsements; they do not constitute legal or compliance advice.

| Reference | Source | What it is | Why it matters for nurse-led AI |
|-----------|--------|------------|----------------------------------|
| **EU AI Act** | [European Commission](https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai) | Binding EU law. Risk tiers: Unacceptable / High-Risk / Limited / Minimal. | Most healthcare AI falls in **High-Risk**. Full high-risk obligations take effect **Aug 2, 2026**. Maps closely to EDENA's tiering instinct. |
| **NIST AI RMF 1.0** | [NIST (US)](https://www.nist.gov/itl/ai-risk-management-framework) | Voluntary US framework: **Govern, Map, Measure, Manage.** | A practical, function-based way to structure governance — the closest public analogue to operationalizing the EDENA Stewardship Lens. |

> **EDENA cross-walk (informal):** 🔴 Red ≈ EU "Unacceptable/High-Risk patient-facing"; 🟠 Orange ≈ "High-Risk requiring human oversight"; 🟡 Yellow ≈ "Limited-risk, transparency obligations"; 🟢 Green ≈ "Minimal-risk." This is an orientation aid, **not** a legal classification.

## Slate at a glance

- **13 agents** · **5 🟢 / 6 🟡 / 1 🟠 / 1 🔴** — a deliberate ladder demonstrating EDENA in public
- **Tracks:** 7 entrepreneurship + 3 healthcare-adaptable + 3 governance & guardrails
- **Licenses:** 11 clean (MIT/Apache-2.0), 2 no-license (link-only)
- **Liveness:** all 13 active as of 2026-06-23
- See [VERIFICATION.md](./VERIFICATION.md) for how each was vetted.
