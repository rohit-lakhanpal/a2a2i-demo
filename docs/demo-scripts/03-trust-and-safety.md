# Demo Script — Stage 3: Trust & Safety Agent

**Total time:** 10 minutes (4–5 min facilitator demo + 5–6 min participant hands-on)
**Facilitator role-plays as:** Same nonprofit staff member, now stress-testing the agent instructions
**Agent:** Trust & Safety Agent → [aka.ms/a2a2i](https://aka.ms/a2a2i)

---

## Before You Start

- Have the Trust & Safety Agent open in a new tab/window
- Have your Instruction Generator output ready to paste in

---

## PART A — Facilitator Demo (~4–5 min)

### SETUP — Narration (no typing) — 30 sec

> *"We have a well-defined problem and a solid set of agent instructions. But before we hand this to real users, we need to ask: what could go wrong? What happens when the agent gets bad input, or can't find data, or someone asks it to do something it shouldn't? That's what the Trust & Safety Agent helps us think through."*

---

### BEAT 1 — Paste the Instructions

**You do:** Copy your Instruction Generator output and paste it into the Trust & Safety Agent.

**What the agent does:** Reviews the instructions and provides guidance on how to improve them. This typically covers:
- **Guardrail gaps** — things the agent should refuse to do but the instructions don't explicitly cover
- **Failure modes** — what happens when data is missing, ambiguous, or conflicting
- **Scope boundaries** — where the agent should hand off to a human
- **Ownership and accountability** — who is responsible for the agent's outputs
- **Success criteria** — how you know the agent is working as intended

**Presenter note:** While it generates, narrate:

> *"This isn't about adding bureaucracy — it's about catching the things you'd discover the hard way in production. Like: what if someone pastes a grant URL that's actually a scam page? What if the agent can't find the org's financial data — does it guess or does it say 'check with Finance'?"*

---

### BEAT 2 — Highlight Key Improvements

**Scan the output** and call out 1–2 recommendations:

> *"Look at this one — it's suggesting we add a rule that the agent should never produce a GO recommendation without confirming at least three eligibility criteria from the source documents. That's smart — it prevents the agent from being over-confident on incomplete data."*

> *"And this — it's recommending we define who owns this agent. Who reviews the output before it's acted on? Who updates the instructions when grant programs change? These are the questions that separate a demo from a deployment."*

---

### BEAT 3 — Close the Loop

> *"The Trust & Safety Agent doesn't change your agent for you — it gives you a checklist of improvements. You take these back into your instructions, refine them, and update your agent in Copilot Agent Builder. It's the final quality pass before you share the agent with your team."*

**Presenter note to audience:**

> *"Three stages, one flow: understand the problem → generate the instructions → make it safe. You started with a frustration. Now you have a deployable agent specification. The Research Agent helped you think clearly. The Instruction Generator helped you write precisely. And the Trust & Safety Agent helped you think defensively."*

---

## PART B — Participant Hands-On (~5–6 min)

### Transition

> *"Last round — paste your instructions into the Trust & Safety Agent and see what it flags. You might be surprised what you missed. Then take those recommendations and update your instructions if you have time.*
>
> *You have about 5 minutes. After that, we'll wrap up together."*

### While Participants Work

- Help anyone who's stuck
- If someone says "it didn't find anything wrong" — ask: *"What happens if the agent can't find one of the documents it needs? Is that covered?"*
- Encourage people to think about: *"Who in your org would actually use this agent? What would they get wrong?"*

---

## Timing Guide

| Section | Duration |
|---------|----------|
| Setup narration | 30 sec |
| Beat 1 (paste + generate) | 1–2 min |
| Beat 2 (highlight improvements) | 1–2 min |
| Beat 3 (close the loop) | 1 min |
| Participant hands-on | 5–6 min |
| **Total** | **~10 min** |

---

## If Things Go Sideways

| Problem | Recovery |
|---------|----------|
| Agent output is too academic | "Focus on the practical ones — which of these would actually bite you in the first week?" |
| Agent doesn't flag much | "That's a good sign — your instructions were already solid. But let me ask it about [specific edge case]..." |
| Running low on time | Skip participant hands-on for this stage — summarise the key point: "Run your instructions through the Trust & Safety Agent after the workshop. It's a 5-minute exercise that could save you a real problem." |

---

[← Back to README](../../README.md) | [← Stage 2: Instruction Generator](02-instruction-generator.md)
