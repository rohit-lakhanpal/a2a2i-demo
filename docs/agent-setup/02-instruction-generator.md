# Agent Setup — Instruction Generator Agent

> Facilitator reference: how the **Instruction Generator Agent** at [aka.ms/a2a2i](https://aka.ms/a2a2i) was built. Use this if you want to recreate it in your own tenant, adapt it for a different audience, or understand why it behaves the way it does in the demo.

---

## Purpose

Take the structured spec produced by the [Research Agent](01-research-agent.md) and turn it into a **production-quality system prompt** that can be pasted directly into Microsoft 365 Copilot Agent Builder.

This is the *second* step in the A2A2I flow. Its output goes into Agent Builder, and the resulting agent is then summarised for the [Trust & Safety Agent](03-trust-and-safety.md).

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
| **Name** | Instruction Generator Agent |
| **Description** | Converts a structured agent spec into clear, well-scoped instructions you can drop straight into Copilot Agent Builder. |
| **Icon** | *(describe or attach)* |

### Starter prompts

1. *Here's my Research Agent output — turn it into agent instructions.*
2. *Help me write the system prompt for the agent I just scoped.*
3. *I have a problem statement and persona — give me the instructions.*
4. *Generate Copilot Agent Builder instructions from this spec.*

### Knowledge sources

- **None.** The user provides all context by pasting in their Research Agent output.

### Capabilities / tools

- Web search: off
- Code interpreter: off
- Image generation: off

---

## Instructions (system prompt)

> Paste the exact instructions used in the live agent here so facilitators can recreate it verbatim.

```text
<<< Paste the Instruction Generator system prompt here >>>
```

Key behaviours the prompt enforces:

- Expects the input to look like a Research Agent summary — if it doesn't, asks the user to provide one
- Produces a **single, ready-to-paste** instruction block (not a discussion)
- Uses a consistent structure: role, scope, behaviours, tone, refusal rules, output format
- Stays grounded in the user's spec — does **not** invent new requirements
- Keeps instructions concise enough to fit Agent Builder's character limits

---

## How to recreate it

1. In [Microsoft 365 Copilot](https://m365.cloud.microsoft/chat), click **New agent** → **Skip to configure**
2. Set the identity fields above
3. Paste the system prompt into **Instructions**
4. Add the four starter prompts
5. Leave **Knowledge** empty
6. **Save** and **Publish** (or share via link)
7. Test using the [sample transcript](../sample-transcripts/instruction-generator.md) as a smoke test

---

## Known quirks / things to watch

- *(Add notes from real facilitator runs — e.g. tendency to over-elaborate, importance of clean Stage 1 input, etc.)*

---

## Related

- Demo script: [02-instruction-generator.md](../demo-scripts/02-instruction-generator.md)
- Sample transcript: [instruction-generator.md](../sample-transcripts/instruction-generator.md)
- Previous agent: [Research Agent](01-research-agent.md)
- Next agent: [Trust & Safety Agent](03-trust-and-safety.md)
