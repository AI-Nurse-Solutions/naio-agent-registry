# Agent Framework Field Guide for Nurse Stewards

**Agents propose. Humans judge. Nurses steward.**

> You do not need to *build* with these frameworks. You need to *recognize* them — so when a vendor, a hospital IT team, or a colleague shows you an "AI agent," you can name what's under the hood, ask the one question that matters, and place it on the EDENA ladder.
>
> This is governance literacy, not a coding course. Carry the lamp. Keep the ledger.

⚠️ **Inclusion is not endorsement.** Naming a framework here does not validate any product built on it, and nothing here is legal, compliance, or clinical advice. See the [README](./README.md) disclaimer and [GOVERNANCE.md](./GOVERNANCE.md) for the EDENA rubric.

---

## Why a nurse should care about "frameworks"

When you browse the repos behind healthcare-AI products, the same handful of building blocks appear again and again. They are **developer infrastructure** — the plumbing, not the product. A nurse will never `pip install` one of these at the bedside, and shouldn't have to.

But the **Nurse AI Orchestrator / steward** has a different job: to look at any AI tool being proposed for a unit and answer three things —

1. **What kind of system is this?** (Does it just answer, or does it *act*? Does it act *alone*, or as a *team*? Does it *loop* on its own?)
2. **What is its autonomy ceiling?** (How far can it go without a human?)
3. **Where is the human gate, and the stop condition?**

The frameworks below are the vocabulary for answering #1. The autonomy levels and EDENA tiers answer #2 and #3.

---

## The mental model: four jobs frameworks do

Almost every agent repo is some mix of these four jobs. Learn the jobs, and the brand names stop mattering.

| Job | Plain-English question it answers | Risk instinct |
|-----|-----------------------------------|---------------|
| **1. Orchestrate** | "How do steps and tool calls get wired together?" | The loop is where autonomy hides — look here first. |
| **2. Collaborate** | "Do multiple agents work as a team?" | More agents = more places a human gate can be skipped. |
| **3. Ground** | "Where do the answers come from — a model's guess, or real documents?" | Ungrounded clinical claims are a patient-safety risk. |
| **4. Guard** | "What checks the output before it reaches a human or patient?" | This is the steward's best friend — demand it. |

> **The steward's reflex:** capability is cheap; *control* is the product. A framework that can act is only as safe as the gate you put in front of it.

---

## Field cards: the frameworks you'll actually see

Each card gives: **what it does**, its **autonomy ceiling**, its **EDENA tier instinct**, and **the one question to ask**. Tiers follow [GOVERNANCE.md](./GOVERNANCE.md) — they describe the *framework's potential*, not any specific product (a product can always be governed up or down).

### 🟢 Orchestration — single-agent / starter

**LangChain · openai-agents (SDK) · LlamaIndex (as a query engine)**

- **What it does:** Wires one model to tools and chains a few steps together. The "hello world" of agents. `openai-agents` is the lightweight one (you've run it); LangChain is the sprawling toolkit; LlamaIndex specializes in connecting a model to *your documents*.
- **Autonomy ceiling:** L2–L3. Answers, summarizes, retrieves, calls a tool or two.
- **EDENA tier instinct:** 🟢 Green → 🟡 Yellow the moment it touches a real tool (email, EHR, a write action).
- **The one question to ask:** *"Does it only read and answer, or can it also* ***do*** *something? List every action it can take."*

### 🟡 Orchestration — stateful / governance-native

**LangGraph**

- **What it does:** Builds agents as explicit **state machines** with checkpoints and "stop and ask a human here" interrupts. This is the framework that *models good governance* — it's in this registry specifically because it teaches **control**, not just capability.
- **Autonomy ceiling:** L3–L5, but bounded *by design* if built well.
- **EDENA tier instinct:** 🟡 Yellow. It *enables* governance (human gates) but doesn't *enforce* it — that's still your job.
- **The one question to ask:** *"Show me the human-in-the-loop interrupt. Where exactly does it pause for a nurse?"*

### 🟡 Collaboration — agent teams

**CrewAI · AutoGen · Agno**

- **What it does:** Multiple agents with **roles** (planner, researcher, writer, reviewer) that talk to each other to finish a task. This is the literal shape of a "Nurse Intelligence Workforce" — and the literal shape of where oversight gets diffuse.
- **Autonomy ceiling:** L3–L5. Teams plan and execute multi-step work.
- **EDENA tier instinct:** 🟡 Yellow → 🟠 Orange as the team gains tools and touches clinical content.
- **The one question to ask:** *"When the agents hand work to each other, who is the* ***human*** *in the chain — and can the team finish and act without ever reaching them?"*

### 🟢 Grounding — retrieval (RAG)

**LlamaIndex · retrieval layers inside LangChain**

- **What it does:** Connects the model to a real document set (policies, guidelines, literature) so answers are **grounded in sources** instead of invented. The antidote to confident-sounding fabrication.
- **Autonomy ceiling:** L2. Retrieves and cites; doesn't act on its own.
- **EDENA tier instinct:** 🟢 Green — *if* sources are trustworthy and citations are shown. Ungrounded = treat as unsafe.
- **The one question to ask:** *"Where does each answer come from? Show me the source it cited — and what happens when the source doesn't cover the question."*

### 🛡️ Guarding — the EDENA substrate

**Guardrails AI · NeMo Guardrails · LLM Guard**

- **What it does:** The checkpoints that implement "agents propose, humans judge." Validate output structure/quality (Guardrails AI), keep conversations on safe topics (NeMo), and scan for **PII/PHI leaks and prompt injection** (LLM Guard).
- **Autonomy ceiling:** L2 — these don't act, they *check*.
- **EDENA tier instinct:** 🛡️ These *lower* everyone else's risk. A steward should ask for them by name.
- **The one question to ask:** *"What scans the output before it reaches a patient or chart — for PHI leaks, for hallucination, for harm? If nothing does, why not?"*

### 🔧 Optimization — prompt/program tuning

**DSPy**

- **What it does:** Automatically tunes prompts/programs instead of hand-crafting them. Pure developer tooling — you'll see it named, but it's invisible to end users.
- **Autonomy ceiling:** Build-time only; no runtime autonomy of its own.
- **EDENA tier instinct:** 🟢 Green (it's a developer's workshop tool).
- **The one question to ask:** *"This is a build tool — fine. What did it produce, and which card above describes the thing that actually runs?"*

---

## The steward's pocket checklist

Use this on **any** agent product, regardless of which framework it's built on:

- [ ] **Read or act?** I can list every action the system can take.
- [ ] **Alone or team?** I know whether one agent or many are running.
- [ ] **Does it loop?** If it runs autonomously, it has a **trigger + goal + evaluation + memory + stop condition** — and I've seen the stop condition.
- [ ] **Human gate.** There is a specific, named point where a human (ideally a nurse) judges before action. I can point to it.
- [ ] **Grounded.** Clinical claims cite real sources; I've seen what happens when they can't.
- [ ] **Guarded.** Something scans output for PHI leaks, hallucination, and injection before it reaches a patient or chart.
- [ ] **PHI boundary.** No protected health information flows without organizational governance and a signed agreement.
- [ ] **Tiered.** I've placed this on the EDENA ladder (🟢/🟡/🟠/🔴) and the controls match the tier.

> If you can't complete this checklist, the answer isn't "no" — it's **"not yet, and here's what's missing."** That sentence is the nurse steward's superpower.

---

## How this maps to autonomy levels

Frameworks don't have a fixed danger level — *what you build with them* does. But their **ceiling** rises predictably:

| Autonomy | What it looks like | Typical frameworks | EDENA instinct |
|----------|--------------------|--------------------|----------------|
| **L1–L2** | Answers, retrieves, summarizes | starter LangChain, LlamaIndex, openai-agents | 🟢 Green |
| **L3** | Uses tools, takes bounded actions | LangGraph, CrewAI, openai-agents | 🟡 Yellow |
| **L4–L5** | Agent teams, integrations, orchestration | CrewAI, AutoGen, Agno, Agent Starter Pack | 🟡→🟠 |
| **L5+** | Autonomous loops, scheduled/async execution | any of the above, unbounded | 🔴 Red until gated |

> **Governance must scale with autonomy, access, memory, orchestration, integration, and async execution.** When in doubt, tier up.

---

## What to do with this guide

- **Bring it to a vendor demo.** Ask the "one question" for whatever framework they're using. Watch how they answer.
- **Use it in NAIO certification.** This is the framework-literacy module for the Nurse AI Orchestrator role.
- **Pair it with the [Registry](./index.md).** The Registry vets *specific repos*; this guide teaches the *categories* behind them.

---

*Part of the [NAIO Agent Registry](./index.md). Agents propose. Humans judge. Nurses steward.*
