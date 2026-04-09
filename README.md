# Agent-to-Agent-to-Impact (A2A2I) Demo

> **A facilitator kit for running a 90-minute, human-centered Copilot build sprint at your own event — anywhere in the world.**

This repository contains everything you need to deliver the **"Agent-to-Agent-to-Impact"** workshop: agent definitions, a ready-made demo scenario, and facilitator guidance so you can adapt the session for your own audience of nonprofits, universities, or public-sector organisations.

---

## Origin Story

This workshop was created for **Microsoft's Sydney Elevate Day** — an invited event for Non Profits and Educational Institutions in Australia. The original facilitator is a Microsoft tech seller covering Aged Care orgs, Research Institutes, Health & Human Services nonprofits, and Educational Institutions. The goal was to show attendees how to use AI as a **comaker** to build a custom Copilot agent around a real problem — in just 90 minutes.

---

## The 3 Workshop Agents

All agents are available at **[aka.ms/a2a2i](https://aka.ms/a2a2i)**

| # | Agent | Purpose |
|---|-------|---------|
| 1 | **Research Agent** | Talks to the user and draws out the problem, persona, jobs to be done, prioritised use case, and key constraints/risks. Turns sparse ideas into a well-articulated overview. |
| 2 | **Instruction Generator Agent** | Translates Research Agent output into structured system instructions with clear scope, behaviour, and rules. Participants then manually copy these instructions into the **Copilot Agent Builder** and configure the agent appropriately. |
| 3 | **Trust & Safety Agent** | Provides guidance on how to improve the instructions and settings of the agent being developed — defining guardrails, ownership, and success criteria for responsible deployment. |

---

## Demo Scenario: Grant Opportunity Screener

A grants officer pastes a grant URL, and the custom Copilot agent cross-references the grant criteria against the organisation's own documents in SharePoint, producing a **go/no-go assessment** with reasons and who in the org to talk to.

### Why This Scenario?

It was chosen over alternatives (food bank logistics, aged care coordination, cross-org collaboration) for the following reasons:

- **Universal across the audience** — every nonprofit and university manages grants.
- **M365 connectors are natural (not forced)**:
  - *Public Web* → grant opportunity page
  - *SharePoint* → org docs + downloaded guidelines
  - *Email* → funder correspondence
  - *Teams* → program updates
  - *Org Chart* → who to talk to
- **Genuinely needs a custom agent** (not basic Copilot) — systematic cross-referencing, structured go/no-go output, refusal to guess on financial data, filtering hard disqualifiers vs soft risks, org chart routing.
- **Strong emotional hook** — *"Spent two weeks writing an application, rejected because of a criterion buried on page 12."*
- **Right complexity** — not trivial, not over-engineered.

---

## Demo Setup: The Fictitious Organisation

> **Why a fictitious org?** Facilitators are typically Microsoft employees or partners — not actual nonprofits. For the demo to work, we need a plausible Australian nonprofit with real-looking documents that participants can upload to SharePoint and query with their agent.

### Southern Community Collective Inc.

A volunteer-led community organisation based in Brighton (City of Bayside, Melbourne) delivering food access, social connection, and community wellbeing programs since 2011. The org is **deliberately designed to FAIL** against the demo grant opportunity on exactly 3 criteria:

| # | Disqualifier | Detail |
|---|-------------|--------|
| 1 | **Round is closed** | The grant round has already closed — the agent should flag this immediately. |
| 2 | **Excluded use of funds** | The org has food-adjacent programs but intends to use the grant for purposes outside the eligible activity scope. |
| 3 | **Non-priority region** | The org is Victorian-based (correct state ✅) but located in a non-priority LGA — Bayside is not a disadvantaged area. |

What the org **does** have right: correct organisation type, ACNC registered, relevant community programs, plausible financial profile.

### Documents for SharePoint

Upload these 5 files to a SharePoint site (or folder) that the Copilot agent can access as a knowledge source. They are located in the [`docs/org-profile/`](docs/org-profile/) folder of this repo:

| File | Description | ~Length |
|------|-------------|--------|
| [Organisation Profile.md](docs/org-profile/Organisation%20Profile.md) | Name, ABN, ACNC status, location, org type, mission, leadership | 1 page |
| [Strategic Plan Summary.md](docs/org-profile/Strategic%20Plan%20Summary.md) | Priorities, programs, geographic focus, financial sustainability | 2 pages |
| [Capability Statement.md](docs/org-profile/Capability%20Statement.md) | What they deliver, who they serve, key partnerships, governance | 1 page |
| [Past Grants Register.md](docs/org-profile/Past%20Grants%20Register.md) | 8 past grants, mix of funders, success rate | 1 page |
| [Annual Report Summary.md](docs/org-profile/Annual%20Report%20Summary.md) | FY24–25 highlights, financials, outcomes, challenges | 2 pages |

> **Tip for facilitators:** Convert these to `.docx` or `.pdf` before uploading to SharePoint if you want a more realistic experience. The markdown versions are provided for easy editing and version control.

### Setting Up the Demo Environment

Before the workshop, you'll need to create a Teams team (which auto-provisions a SharePoint site) and upload the org profile documents so the Copilot agent can use them as a knowledge source.

**→ [Facilitator Setup Guide](docs/facilitator-setup-guide.md)** — step-by-step instructions (15–20 min pre-workshop).

---

## Useful References

- [Build agents with Copilot Agent Builder](https://learn.microsoft.com/en-us/microsoft-365/copilot/extensibility/agent-builder-build-agents)
- [Add knowledge to your agent](https://learn.microsoft.com/en-us/microsoft-365/copilot/extensibility/agent-builder-add-knowledge)

---

## For Facilitators

This repo is designed so **any facilitator** — at a Microsoft event, a partner workshop, or a community meetup — can pick it up and run the session with their own audience. Contributions, localisation, and adaptations are welcome.

**Getting started:**
1. Read this README to understand the workshop structure and demo scenario
2. Follow the **[Facilitator Setup Guide](docs/facilitator-setup-guide.md)** to prepare your demo environment
3. Review the **[Cheat Sheet](docs/cheat-sheet.md)** — key facts, expected output, and recovery phrases
4. Run the demo scripts:
   - [Stage 1 — Research Agent](docs/demo-scripts/01-research-agent.md) (25 min: ~12 min demo + ~13 min hands-on)
   - [Stage 2 — Instruction Generator](docs/demo-scripts/02-instruction-generator.md) (20 min: ~7 min demo + ~13 min hands-on)
   - [Stage 3 — Trust & Safety](docs/demo-scripts/03-trust-and-safety.md) (10 min: ~5 min demo + ~5 min hands-on)
5. Familiarise yourself with the 3 agents at [aka.ms/a2a2i](https://aka.ms/a2a2i) before the session