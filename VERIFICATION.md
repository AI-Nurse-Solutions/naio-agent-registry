# Verification Log — v1

All entries verified on **2026-06-23** against the live GitHub API and repository contents (not search snippets).

## Method

1. **Metadata** — license (SPDX), star count, `pushed_at` (liveness), archived flag, open issues, pulled via GitHub REST API.
2. **Structure** — cloned each repo (shallow), inventoried install files (`pyproject.toml`/`requirements.txt`/`Dockerfile`/etc.), runnable example dirs, Python vs. Markdown file counts, and presence of a LICENSE file.
3. **Claim vs. Proof** — read each README and compared marketing claims against actual repo contents.
4. **Execution** — at least one framework smoke-tested by real install + import.

## Results

| Agent | License (file) | Stars | Last push | Verified as |
|-------|----------------|-------|-----------|-------------|
| agency-agents | MIT ✅ | ~115k | 2026-06-22 | Structure: 0 py / 275 md = prompt templates (matches claim) |
| crewAI | MIT ✅ | ~54k | 2026-06-23 | Structure: 1,253 py, active framework |
| awesome-llm-apps | Apache-2.0 ✅ | ~115k | 2026-06-15 | Structure: 503 py runnable apps |
| gpt-researcher | Apache-2.0 ✅ | ~28k | 2026-05-28 | Structure: full Docker + .env.example path |
| langgraph | MIT ✅ | ~36k | 2026-06-22 | Structure: 447 py + examples |
| agent-starter-pack | Apache-2.0 ✅ | ~6.5k | 2026-06-22 | Structure: pyproject + Makefile, official GCP |
| agno | Apache-2.0 ✅ | ~41k | 2026-06-23 | Structure: 3,993 py + cookbook |
| openai-agents-python | MIT ✅ | ~27k | 2026-06-23 | **EXECUTED:** pip install + `import agents` v0.17.6 ✅ |
| Awesome-AI-Agents-for-Healthcare | ⚠️ NONE | ~1.1k | 2026-06-04 | Resource/index (survey-backed) |
| OpenClaw-Medical-Skills | ⚠️ NONE | ~2.7k | 2026-06-18 | Structure: 609 py / 991 md skills; clinical validity unverified |
| Multi-Agent-Medical-Assistant | Apache-2.0 ✅ | ~906 | (active) | Structure: LangGraph-based, guardrails topic; diagnostic claim unvalidated |

## Cuts during verification

- **TrialGPT** — `ncbi/TrialGPT` returns 404; no viable public clone found. **Removed.**
- **SuperAGI** — last push 2025-01-22 (~18 months stale). **Removed.**
- **Replacement** — Multi-Agent Medical Assistant (Apache-2.0) added as the 🔴 cautionary exemplar.

## Honesty notes

- "Structurally verified" means install paths and runnable entrypoints exist and claims match code — it does **not** mean every agent was run end-to-end (several require paid API keys, cloud billing, or vector DBs).
- One framework was executed (install + import) so the slate has at least one fully-exercised entry.
- Clinical-risk entries (🟠/🔴) are listed for study and governance demonstration, never as endorsements.
