# Agent Setup

> Facilitator-only reference for **how the three workshop agents at [aka.ms/a2a2i](https://aka.ms/a2a2i) were built**.

---

## Purpose

The files in this folder document the configuration behind the three agents that drive the A2A2I workshop:

1. [Research Agent](01-research-agent.md) — turns a vague problem into a structured spec
2. [Instruction Generator Agent](02-instruction-generator.md) — turns that spec into Copilot Agent Builder instructions
3. [Trust & Safety Agent](03-trust-and-safety.md) — turns the built agent's self-summary into a lightweight Agent Charter

For each agent you'll find: identity, starter prompts, knowledge sources, capabilities, the full system prompt, recreate steps, and known quirks.

---

## Who this is for

- **Facilitators** who want to understand *why* the demo agents behave the way they do
- **Facilitators recreating the agents** in their own tenant (e.g. customer environment, restricted tenant, offline backup)
- **Contributors** proposing changes to the live agents — use these files as the source of truth

This folder is **not** part of the participant experience. Participants only see the demo scripts, sample transcripts, and the live agents at [aka.ms/a2a2i](https://aka.ms/a2a2i).

---

## How this differs from the rest of `docs/`

| Folder | Audience | Purpose |
|---|---|---|
| [`agent-setup/`](.) (this folder) | Facilitators | How the **three workshop agents** were built |
| [`demo-scripts/`](../demo-scripts/) | Facilitators | What to **say and type** during the live demo |
| [`sample-transcripts/`](../sample-transcripts/) | Facilitators | Reference outputs to expect from each agent |
| [`org-profile/`](../org-profile/) | Both | Fictitious org docs uploaded to SharePoint for the **demo agent** participants build |
| [`facilitator-setup-guide.md`](../facilitator-setup-guide.md) | Facilitators | How to set up the **demo agent** (Grant Fit Check) participants will build |

> **Important distinction:** [`facilitator-setup-guide.md`](../facilitator-setup-guide.md) covers the agent participants *build* during the workshop (Grant Fit Check). This folder covers the three agents that *guide* them through building it.

---

## Keeping this folder in sync with the live agents

If you update an agent at [aka.ms/a2a2i](https://aka.ms/a2a2i):

1. Update the matching file in this folder (identity, starter prompts, system prompt, etc.)
2. If behaviour changed, refresh the relevant [sample transcript](../sample-transcripts/)
3. If the demo flow changed, update the relevant [demo script](../demo-scripts/)
4. Open a PR so other facilitators inherit the change

---

## Related

- Workshop overview: [README](../../README.md)
- Cheat sheet: [cheat-sheet.md](../cheat-sheet.md)
- Setup for the agent participants build: [facilitator-setup-guide.md](../facilitator-setup-guide.md)
