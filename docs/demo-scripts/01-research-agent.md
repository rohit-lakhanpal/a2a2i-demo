# Demo Script — Stage 1: Research Agent

- **Total time:** 25 minutes (~1 min context setting + ~10 min facilitator demo + ~14 min participant hands-on)
- **Facilitator role-plays as:** A staff member at Southern Community Collective
- **Agent:** Research Agent → [aka.ms/a2a2i](https://aka.ms/a2a2i)

---

## Before You Start

- Have the Research Agent open and ready
- Know your 3 disqualifiers cold (see [Cheat Sheet](../cheat-sheet.md))
- Remind yourself: you are NOT demoing the finished grant agent yet — you're demoing the *process of defining one*
- **Open a scratch document** (Word, OneNote, Notepad — anything) to copy-paste outputs as you go
- Review the [sample transcript](../sample-transcripts/research-agent.md) so you know what to expect from the agent

> **Important — tell participants this early:** The three workshop agents are not connected to each other. Conversation history is lost when you leave an agent. Everyone should have a helper document open where they copy-paste their outputs at each stage. The Research Agent summary gets pasted into the Instruction Generator, and those instructions get pasted into the Trust & Safety Agent. If you don't save it, you lose it.

---

## CONTEXT SETTING — Meet the Organisation (~1 min, no typing)

> *"Before I jump into the agent, let me set the scene. I'm going to role-play as a staff member at a small community nonprofit in Melbourne called Southern Community Collective. They run food programs — a community kitchen, food hampers, cooking workshops. Four staff, about 45 volunteers, $387K annual revenue. Small but mighty.*
>
> *Their problem? Grants. They chase grants constantly. Last quarter, their CEO Sarah spent two weeks writing an application for a state food relief grant — detailed project plan, budget, partner letters. Got rejected. Turns out there was a geographic priority criterion buried in the downloadable guidelines that they didn't match. Two weeks, gone.*
>
> *That's the kind of pain we're going to build an agent around. I'll start vague — just a frustration — and the Research Agent will help turn that into something sharp and structured. Watch how it goes from spark to spec."*

---

## PART A — Facilitator Demo (~10 min)

### BEAT 1 — Start Broad

**You type:**

> We're a small community nonprofit in Melbourne and we spend too much time chasing grants we don't win. We find opportunities, get excited, start writing, and then discover halfway through — or after we submit — that we were never a good fit. It's exhausting and it's burning out our grants officer.

**What the agent does:** Acknowledges the problem. Asks a clarifying question — zooms into a concrete moment: *"Can you describe a recent example?"*

**Presenter note:** Keep it conversational. You're venting, not briefing.

---

### BEAT 2 — The Painful Moment

**You type:**

> Last quarter we spent two weeks writing an application for a state government food relief grant. Detailed project plan, budget, partner letters — the lot. Got rejected. Turns out there was a geographic priority criterion buried in the downloadable guidelines document that we didn't match. Two weeks of Sarah's time, gone. And Sarah's our CEO — she shouldn't be doing this at all but we can't afford a dedicated grants person.

**What the agent does:** Latches onto the specifics — time wasted, buried criteria, CEO doing grunt work. Asks who is most affected.

---

### BEAT 3 — Identify the Persona

**You type:**

> Honestly, it's whoever has time. Usually Sarah, sometimes Tom our Program Manager. But the person who *should* be doing it — or at least the first-pass screening — is someone in a grants officer role. We're trying to get a part-time grants coordinator but haven't hired yet. In the meantime, anyone who spots an opportunity just starts chasing it.

**What the agent does:** Drafts a persona — *"A part-time Grants Coordinator responsible for identifying, screening, and preparing grant applications."* Asks you to confirm or tweak.

**You type:**

> Yeah, that's right — the grants officer, or whoever is doing that role on any given week. They need to quickly figure out: is this grant worth our time? Before anyone spends a day on it.

---

### BEAT 4 — Confirm the Problem

**The agent** presents a draft problem statement. Something like: *"Our nonprofit lacks a quick, reliable way to determine whether a grant is truly a good fit without reading lengthy guidelines and manually cross-checking against our own eligibility and priorities."*

**You type:**

> The core problem is that we can't tell the difference between "this looks relevant" and "this is actually a fit for us" without reading 30 pages of guidelines and cross-referencing against our own org details. And we don't have the time or expertise to do that systematically. So we either skip opportunities or waste time on wrong ones.

**What the agent does:** Refines the problem statement and asks you to confirm.

**You type:**

> Yeah

---

### BEAT 5 — Jobs to Be Done

**The agent** drafts a JTBD. Confirm it's close, then sharpen:

**You type:**

> What the grants officer really needs to do is: paste a grant opportunity, have it checked against our org profile, eligibility, strategic fit, and get a quick go/no-go with reasons. And if it's a no-go, tell us why and what we'd need to change. And if it's a go, tell us who in the org to talk to first — like who owns the budget, who has the program data, who signs off.

---

### BEAT 6 — Use Case Selection *(Key Moment)*

**The agent generates** 4–5 candidate use cases. From the transcript, these typically include:
1. Quick Fit Check
2. Go/No-Go Decision Brief
3. Internal Prep Checklist
4. Grant Landscape Snapshot
5. Lessons Learned Analyzer

**You type:**

> Maybe number 1. My initial idea was a Grant Opportunity Assessment Assistant. If we can get the screening right, everything downstream gets easier. No point drafting faster if we're drafting for the wrong grants.

**Presenter note to audience:**

> *"See what just happened? We started with 'we waste time on grants' — vague, frustrating, could go anywhere. The agent listened, clarified, and structured. Now we have a named use case with a persona, problem, and jobs to be done. That's the Research Agent's job."*

---

### BEAT 7 — Full Summary + Handoff

**The agent produces** a structured summary:
- **Context** — small Melbourne nonprofit, wasted time on poor-fit grants
- **Problem Statement** — validated
- **Persona** — Grants Coordinator (or whoever fills that role)
- **JTBD** — validated
- **Use Case** — Grant Opportunity Assessment Assistant
- **Constraints** — must work with unstructured guidelines, must reference org profile, must provide clear reasoning

The agent tells you to **copy the output** and take it to Agent 2.

**You type:**

> That's exactly right. Let's go with this.

**Presenter note to audience:**

> *"This is our foundation. Everything in Stage 2 and Stage 3 builds on this. The Instruction Generator will turn this into actual agent instructions. The Trust & Safety Agent will stress-test them. But it all starts here — understanding the problem from the human's perspective."*

---

## PART B — Participant Hands-On (~14 min)

### Transition

> *"Now it's your turn. Think about a real problem from your organisation — something where you or your team waste time, miss things, or don't have the capacity to do it properly. Open the Research Agent and start talking to it. Start vague. The agent will help you get sharp.*
>
> *You have about 14 minutes. We'll come back together and I'll show you how Stage 2 turns your output into actual Copilot agent instructions."*

### While Participants Work

- Walk the room, answer questions, help anyone who's stuck
- Encourage people who are being too polished: *"Just talk to it like you'd complain to a colleague"*
- If someone finishes early, ask them to read back their summary and see if it feels right

---

## Timing Guide

| Section | Duration |
|---------|----------|
| Context setting (meet the org) | 1 min |
| Beats 1–3 (broad → painful → persona) | 3–4 min |
| Beats 4–5 (confirm problem/JTBD) | 2–3 min |
| Beats 6–7 (use case selection + summary) | 3 min |
| Participant hands-on | ~14 min |
| **Total** | **~25 min** |

---

## If Things Go Sideways

| Problem | Recovery |
|---------|----------|
| Agent asks too many questions | "Let me just tell you the whole picture..." and give a longer answer to skip ahead |
| Agent goes off-track | "Let me bring it back — the core issue is..." |
| Agent summary is wrong | "Close, but let me adjust..." — correct it live, this actually demonstrates human-in-the-loop |
| Agent is slow | Fill with narration: "While it's thinking — this is where the agent is synthesising everything we've said..." |

---

**Next:** [Stage 2 — Instruction Generator Agent →](02-instruction-generator.md)

[← Back to README](../../README.md)
