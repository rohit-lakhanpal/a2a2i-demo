# Agent Setup — Research Agent

> Facilitator reference: how the **Research Agent** at [aka.ms/a2a2i](https://aka.ms/a2a2i) was built. Use this if you want to recreate it in your own tenant, adapt it for a different audience, or understand why it behaves the way it does in the demo.

---

## Purpose

Help a non-technical user move from a **vague frustration** to a **structured agent specification** (problem, persona, jobs-to-be-done, use case, success signals) through a guided, conversational interview.

This agent is the *first* step in the Agent-to-Agent-to-Impact (A2A2I) flow. Its output is pasted into the [Instruction Generator Agent](02-instruction-generator.md).

---

## Where it lives

- **Platform:** Microsoft 365 Copilot — Agent Builder
- **Public link:** [aka.ms/a2a2i](https://aka.ms/a2a2i)
- **Owner:** *(facilitator: add owner / contact)*

---

## Configuration

### Identity

| Field | Value |
|---|---|
| **Name** | Research Agent |
| **Description** | Helps you turn a vague problem into a clear, structured spec for a Copilot agent — by asking the right questions. |
| **Icon** | *(describe or attach)* |

### Starter prompts

1. *I have a process I think could be automated, but I'm not sure where to start.*
2. *Help me figure out what kind of agent my team actually needs.*
3. *We waste time on something repetitive — can you help me describe it?*
4. *I want to build an agent but I don't know how to brief it.*

### Knowledge sources

- **None.** This agent is intentionally knowledge-light — it should rely on the user's own context, not pre-loaded documents.

### Capabilities / tools

- Web search: *(on / off — record decision)*
- Code interpreter: off
- Image generation: off

---

## Instructions (system prompt)

> Paste the exact instructions used in the live agent here so facilitators can recreate it verbatim.

```text
<<< Paste the Research Agent system prompt here >>>
```

Key behaviours the prompt enforces:

- Acts as a **structured interviewer**, not an answer machine
- Asks **one question at a time** and stays conversational
- Probes for: the painful moment, the persona, jobs-to-be-done, the use case, and success signals
- Produces a **final structured summary** the user can copy-paste into the next agent
- Does **not** try to design the agent's instructions itself — that's Stage 2's job

---

## How to recreate it

1. In [Microsoft 365 Copilot](https://m365.cloud.microsoft/chat), click **New agent** → **Skip to configure**
2. Set the identity fields above
3. Paste the system prompt into **Instructions**
4. Add the four starter prompts
5. Leave **Knowledge** empty
6. **Save** and **Publish** (or share via link, depending on tenant policy)
7. Test using the [sample transcript](../sample-transcripts/research-agent.md) as a smoke test

---

## Known quirks / things to watch

- *(Add notes from real facilitator runs — e.g. the agent sometimes summarises too early, drifts into solutioning, etc.)*

---

## Related

- Demo script: [01-research-agent.md](../demo-scripts/01-research-agent.md)
- Sample transcript: [research-agent.md](../sample-transcripts/research-agent.md)
- Next agent in the flow: [Instruction Generator](02-instruction-generator.md)
