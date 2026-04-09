# Demo Script — Stage 2: Instruction Generator Agent

**Total time:** 20 minutes (5–7 min facilitator demo + 13–15 min participant hands-on)
**Facilitator role-plays as:** Same nonprofit staff member, now carrying the Research Agent output
**Agent:** Instruction Generator Agent → [aka.ms/a2a2i](https://aka.ms/a2a2i)

---

## Before You Start

- Have the Instruction Generator Agent open in a new tab/window
- Have your Research Agent output ready to copy-paste (from Stage 1)
- Have Copilot Agent Builder open and ready in another tab — you'll paste instructions into it after
- Review the [sample transcript](sample-transcript-instruction-generator.md) beforehand so you know what to expect

> **Reminder:** The agents are not connected — participants need their Research Agent output saved in their scratch document. If anyone didn't copy it, they'll need to go back and re-run Stage 1 or use your demo output as a starting point.

---

## PART A — Facilitator Demo (~5–7 min)

### SETUP — Narration (no typing) — 30 sec

> *"We've done the hard thinking — we know the problem, the persona, the jobs to be done, and the use case. Now we need to turn that into actual instructions that a Copilot agent can follow. That's what the Instruction Generator does. Watch — I'm going to paste the Research Agent output straight in."*

---

### BEAT 1 — Paste the Research Agent Output

**You do:** Copy your full Research Agent summary from Stage 1 and paste it into the Instruction Generator Agent.

**What the agent does:** Reads and mirrors back the framing — persona, JTBD, use case, constraints — and asks you to confirm before proceeding.

**You type:**

> Looks good

---

### BEAT 2 — Choose an Archetype

**The agent offers** 3 archetype options. From the transcript, these are typically:
1. **Screening Assistant** — extract criteria, compare to org profile, go/no-go recommendation
2. **Decision Support Advisor** — structured decision matrix with alignment gaps and next steps
3. **Research Summarizer** — condense guidelines into scannable summaries (no fit scoring)

**You type:**

> Mostly number 1 but also include highlighting alignment gaps, and suggesting next steps where sensible

**Presenter note:** This is a design choice — explain it to the audience:

> *"We're picking Screening Assistant as the core behaviour — that's the go/no-go engine. But we're borrowing the alignment gap analysis from option 2. The agent lets you mix and match."*

---

### BEAT 3 — Configure Behaviour

**The agent walks you through** 3–4 configuration questions, one at a time. Move through these quickly:

| Config | What You Pick | Why |
|--------|--------------|-----|
| **Determinism** | High — strict workflow | Grants screening needs consistency, not creativity |
| **Variability** | Low — uniform outputs | Builds trust; same format every time |
| **Uncertainty handling** | Strict flagging — no assumptions | If data is missing, say so — never guess |
| **Output structure** | Hybrid — compact decision block + detailed breakdown | Quick answer first, detail available if needed |

**You type** `1`, `1`, `1`, `3` for each question respectively.

**Presenter note to audience:**

> *"Notice these aren't technical settings — they're behaviour choices. How structured should the agent be? What happens when data is missing? How should it present results? You're designing how the agent thinks, not writing code."*

---

### BEAT 4 — Generated Instructions + Copy to Agent Builder

**The agent produces** a full block of copy-paste-ready instructions covering:
- **Objective** — what the agent does
- **Response rules** — one question at a time, never fabricate, flag gaps
- **Workflow** — input collection → extraction → comparison → assessment → output
- **Output formatting** — decision block first (High/Medium/Low fit), then detailed breakdown
- **Knowledge sources** — SharePoint, web, email, Teams

> *"Now here's the key step — these instructions don't create the agent automatically. We copy them into Copilot Agent Builder."*

**You do:**
1. Copy the generated instructions
2. Switch to Copilot Agent Builder
3. Paste into the agent's instructions field
4. Briefly show the knowledge source configuration (SharePoint site from the [setup guide](../facilitator-setup-guide.md))
5. Briefly show enabling the web connector for grant URLs

**Presenter note:** Don't build the full agent live — just show the copy-paste flow and where the key settings are.

> *"The Instruction Generator gives you what to say to the agent. Copilot Agent Builder is where you wire it up — connect SharePoint, enable the web connector, set who can use it. The instructions are the brain; the builder is the body."*

---

## PART B — Participant Hands-On (~13–15 min)

### Transition

> *"Your turn. Take the output from your Research Agent session, paste it into the Instruction Generator, and see what comes back. Read through the instructions it gives you — do they capture what you intended? Is anything missing? Tweak it until it feels right.*
>
> *If you want to go further, open Copilot Agent Builder and start configuring your agent with the instructions. You can find it at [microsoft365.com/copilot](https://microsoft365.com/copilot) — look for Agent Builder.*
>
> *You have about 13 minutes. Then we'll do one final stage — making sure your agent is safe and responsible."*

### While Participants Work

- Help anyone who's stuck on the copy-paste flow
- If someone's instructions look thin, suggest: *"Ask it to add more specific guardrails — what should the agent refuse to do?"*
- For advanced participants who are configuring in Agent Builder: help them connect their SharePoint site as a knowledge source
- Remind people: *"You don't have to finish configuring the agent today — the instructions are the valuable output. You can take them home."*

---

## Timing Guide

| Section | Duration |
|---------|----------|
| Setup narration | 30 sec |
| Beat 1 (paste + confirm) | 1 min |
| Beat 2 (archetype selection) | 1 min |
| Beat 3 (behaviour config) | 1–2 min |
| Beat 4 (generated instructions + Agent Builder) | 2–3 min |
| Participant hands-on | 13–15 min |
| **Total** | **~20 min** |

---

## If Things Go Sideways

| Problem | Recovery |
|---------|----------|
| Instructions are too generic | "Let me give it more context..." — paste in a specific constraint or scenario |
| Instructions are too long | "In practice you'd trim this down — focus on the rules that matter most for your use case" |
| Agent Builder isn't loading | Show the instructions output and explain: "This is what you'd paste in — the Agent Builder step is just configuration" |
| Participant didn't finish Stage 1 | Have a pre-prepared Research Agent output they can use (your demo output from Stage 1) |

---

**Next:** [Stage 3 — Trust & Safety Agent →](03-trust-and-safety.md)

[← Back to README](../../README.md) | [← Stage 1: Research Agent](01-research-agent.md)
