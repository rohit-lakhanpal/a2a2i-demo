# Sample Transcript — Instruction Generator Agent

> This is a real transcript from a test run of the Instruction Generator Agent. Use it as a reference for what the conversation looks like in practice. The facilitator pastes the Research Agent output and walks through the configuration steps.

---

## Opening

> 🤖 **Agent**
>
> Welcome, you're in the DIS Instruction Generator Agent.
>
> To start, tell me what you have on hand:
>
> - the structured handoff from the Research and Definition Agent or
> - a freeform description of the agent you have in mind and how you expect it to help.
>
> From there, I'll help you shape and refine that input until we have a single block of text you can paste directly into the Copilot Agent Builder "Describe" field.

---

## Beat 1 — Paste the Research Agent Output

> 💬 **You**
>
> ✅ **Context**
> A small community nonprofit in Melbourne struggles with wasted time and leadership energy on grant applications that turn out to be a poor fit. The lack of a quick, systematic way to assess eligibility and alignment forces staff to either skip opportunities or invest heavily in the wrong ones, leading to burnout and missed chances.
>
> **Problem Statement (validated)**
> Our nonprofit lacks a quick, reliable way to determine whether a grant is truly a good fit without reading lengthy guidelines and manually cross-checking against our own eligibility and priorities. As a result, we either skip opportunities or waste significant time on applications that fail, draining limited staff capacity and leadership energy.
>
> **Primary Persona (validated)**
> A part-time Grants Coordinator (or whoever fills that role) responsible for identifying, screening, and preparing grant applications. They need to quickly assess which opportunities are worth pursuing and which are not, so they can focus limited time on the best-fit grants.
>
> **Primary JTBD (validated)**
> When I come across a potential grant, I want to know quickly whether it's a good fit for our organization and what key steps or people are involved if we proceed, so I can make an informed go/no-go decision without wasting time or missing critical inputs.
>
> **Prioritized Use Case — Grant Opportunity Assessment Assistant**
> *What it is:* An AI copilot that reviews a grant opportunity, extracts key eligibility and priority criteria, and compares them to the organization's profile to flag major fit issues. It provides a concise summary and a preliminary "fit" assessment to support an early go/no-go decision.
>
> *Why this is the right focus now:* This use case directly addresses the root cause of wasted effort and burnout, has high impact on decision quality, and is feasible for an AI copilot to deliver through summarization, comparison, and structured reasoning — without requiring heavy system integration.
>
> **Key constraints / risks to respect**
> Must work with unstructured grant guidelines (PDFs, web pages). Needs a simple way to reference the org's profile (mission, geography, size, priorities). Should provide clear reasoning for its assessment to build trust.

> 🤖 **Agent**
>
> Here's the framing I've captured from your input. Please review and confirm or correct before we move forward:
>
> **Primary Persona**
> Part-time Grants Coordinator (or equivalent) responsible for identifying, screening, and preparing grant applications.
>
> **Primary JTBD**
> When encountering a potential grant, quickly determine if it's a good fit for the organization and identify key steps or people if proceeding — enabling an informed go/no-go decision without wasting time or missing critical inputs.
>
> **Prioritized Use Case — Grant Opportunity Assessment Assistant**
> - Reviews a grant opportunity, extracts key eligibility and priority criteria, and compares them to the organization's profile.
> - Flags major fit issues and provides a concise summary plus a preliminary "fit" assessment to support early go/no-go decisions.
>
> **Key Constraints / Risks**
> - Must handle unstructured grant guidelines (PDFs, web pages).
> - Needs a simple way to reference the org's profile (mission, geography, size, priorities).
> - Must provide clear reasoning for its assessment to build trust.
>
> ✅ Please confirm if this is correct or suggest any edits.
> Once confirmed, we'll move to selecting the agent archetype that best fits this scenario.

> 💬 **You**
>
> Looks good

---

## Beat 2 — Select the Agent Archetype

> 🤖 **Agent**
>
> Great — framing is confirmed!
>
> Next step: choose the agent archetype that best fits this use case. Based on your scenario, here are three feasible options for Copilot Agent Builder:
>
> **Option 1: Screening Assistant**
> Purpose: Rapidly extract key eligibility and priority criteria from grant text and compare to org profile.
> Output: Fit summary with reasoning and a go/no-go recommendation.
>
> **Option 2: Decision Support Advisor**
> Purpose: Provide structured decision support by summarizing grant details, highlighting alignment gaps, and suggesting next steps.
> Output: Decision matrix or checklist for leadership review.
>
> **Option 3: Research Summarizer**
> Purpose: Focus on condensing long grant guidelines into concise, scannable summaries without explicit fit scoring.
> Output: Key points only; user interprets fit.
>
> Which archetype feels most aligned with your goal?
> (You can pick one, combine elements, or suggest a refinement.)

> 💬 **You**
>
> Mostly number 1 but also include highlighting alignment gaps, and suggesting next steps where sensible

> 🤖 **Agent**
>
> Perfect — we'll go with Option 1 (Screening Assistant) as the core, enhanced with alignment gap highlights and suggested next steps from Option 2.
>
> Now we'll configure the agent's behavioral parameters to make sure it acts consistently with your needs.

---

## Beat 3 — Configure Behaviour (4 settings)

### 3a — Interaction Determinism

> 🤖 **Agent**
>
> **First configuration: Interaction determinism vs flexibility**
>
> How tightly should the agent stick to a structured, repeatable process versus allowing more open-ended interpretation?
>
> 1. **High determinism** – Always follow a strict step-by-step screening workflow (predictable, consistent).
> 2. **Moderate flexibility** – Follow the workflow but allow some adaptive interpretation when guidelines are ambiguous.
> 3. **High flexibility** – Act more like a brainstorming partner, less rigid in structure.
> 4. **Other / refine** – Suggest your own balance.
>
> Which do you prefer?

> 💬 **You**
>
> 1

> 🤖 **Agent**
>
> Great — High determinism confirmed. The agent will follow a strict, repeatable screening workflow for consistency.

### 3b — Variability / Creativity

> 🤖 **Agent**
>
> **Next configuration: Variability / creativity control**
>
> How much should the agent vary its language and approach versus keeping outputs uniform and predictable?
>
> 1. **Low variability** – Use consistent phrasing and structure every time (best for trust and repeatability).
> 2. **Moderate variability** – Slight variation in tone and examples, but keep structure intact.
> 3. **High variability** – Freer language and tone shifts for engagement.
> 4. **Other / refine** – Suggest your own.
>
> Which do you prefer?

> 💬 **You**
>
> 1

> 🤖 **Agent**
>
> Excellent — Low variability confirmed. The agent will keep outputs uniform and predictable for trust and repeatability.

### 3c — Handling Uncertainty

> 🤖 **Agent**
>
> **Next configuration: Handling uncertain or incomplete data**
>
> When the grant guidelines or org profile lack details, how should the agent respond?
>
> 1. **Strict flagging** – Clearly mark missing or unclear info and avoid assumptions.
> 2. **Suggestive mode** – Flag gaps but also propose likely interpretations (with disclaimers).
> 3. **Fill-in mode** – Make reasonable assumptions to keep the process moving.
> 4. **Other / refine** – Suggest your own.
>
> Which do you prefer?

> 💬 **You**
>
> 1

> 🤖 **Agent**
>
> Perfect — Strict flagging confirmed. The agent will clearly identify missing or unclear information and avoid assumptions.

### 3d — Output Structure

> 🤖 **Agent**
>
> **Final configuration: Output structuring strategy**
>
> How should the agent present its results for maximum usability?
>
> 1. **Compact decision block** – Summary, fit score, key reasons, and next steps in one scannable block.
> 2. **Detailed breakdown** – Separate sections for eligibility, alignment gaps, and recommendations.
> 3. **Hybrid** – Start with a compact decision block, then provide an expandable detailed breakdown.
> 4. **Other / refine** – Suggest your own.
>
> Which do you prefer?

> 💬 **You**
>
> 3

> 🤖 **Agent**
>
> Great — Hybrid confirmed: the agent will start with a compact decision block, then provide a detailed breakdown for those who need more depth.
>
> ✅ Here's the full configuration we've locked in:
>
> - **Archetype:** Screening Assistant with alignment gap highlights and suggested next steps
> - **Interaction:** High determinism (strict workflow)
> - **Variability:** Low (uniform, predictable outputs)
> - **Uncertainty Handling:** Strict flagging (no assumptions)
> - **Output Structure:** Hybrid (compact decision block + detailed breakdown)
>
> Please confirm this summary. Once you confirm, I'll generate the final copy-paste-ready prompt for Copilot Agent Builder.

> 💬 **You**
>
> Looks good

---

## Beat 4 — Generated Instructions (Copy-Paste Output)

> 🤖 **Agent**
>
> Copy this code block into the Describe field in Copilot Agent Builder.
>
> ```
> # OBJECTIVE
> Enable a Grants Coordinator to quickly assess if a grant opportunity
> fits the organization by extracting key eligibility and priority
> criteria, comparing them to the org profile, highlighting alignment
> gaps, and suggesting next steps. Provide a concise decision block
> plus detailed breakdown to support early go/no-go decisions.
>
> # RESPONSE RULES
> - Ask one question at a time.
> - Be concise, structured, and scannable.
> - Confirm key inputs before acting.
> - Never assume or fabricate information.
> - Flag missing or unclear data explicitly.
>
> # WORKFLOW
> 1. **Input Collection**
>    - Goal: Gather grant text and org profile.
>    - Action: Prompt user for grant guidelines (paste text or link)
>      and org profile basics.
>    - Transition: Validate completeness; flag gaps.
> 2. **Extraction**
>    - Goal: Identify eligibility, priorities, deadlines, and key
>      conditions.
>    - Action: Parse grant text; summarize in bullet form.
>    - Transition: Move to comparison.
> 3. **Comparison**
>    - Goal: Check alignment with org profile.
>    - Action: Highlight matches and gaps; note critical blockers.
>    - Transition: Prepare fit assessment.
> 4. **Assessment**
>    - Goal: Provide preliminary fit rating and reasoning.
>    - Action: Generate compact decision block (fit score, reasons,
>      next steps).
>    - Transition: Offer detailed breakdown.
> 5. **Output**
>    - Goal: Deliver hybrid output.
>    - Action: Show decision block first; then detailed sections for
>      eligibility, gaps, and recommendations.
>
> # OUTPUT FORMATTING RULES
> - Start with **Decision Block**: Fit score (High/Medium/Low), key
>   reasons, next steps.
> - Follow with **Detailed Breakdown**: Eligibility summary, alignment
>   gaps, flagged missing info.
> - Use bold headers and bullets.
> - Keep language uniform and predictable.
> - Limit initial results; offer option to expand.
>
> # EXAMPLES
> - **Valid**: Grant text + org profile → Output: "Fit: Medium. Key
>   blockers: geographic mismatch. Next steps: confirm eligibility
>   with funder."
> - **Invalid**: User asks for grant writing tips without providing
>   grant details.
>
> # KNOWLEDGE
> - Enable organization-wide SharePoint (excluding OneDrive) for
>   document access.
> - Enable organization-wide Teams messages and meetings for context.
> - Enable organization-wide email search for grant-related
>   communications.
> - Enable public web browsing for grant guidelines.
>
> Manual Knowledge Setup (if needed):
> Upload or link your org profile document (mission, geography, size,
> priorities) to a shared SharePoint folder.
> Provide sample grant guidelines PDFs or URLs for testing.
> Conversation history is not saved, so keep your own notes if needed.
> ```
>
> Would you like a few example test prompts to try with this agent?

---

## Testing the Built Agent

Once you've created the agent in Copilot Agent Builder (see [Facilitator Setup Guide — Step 4](../facilitator-setup-guide.md#step-4-create-the-agent-in-copilot-agent-builder)), run these two tests to verify everything is working.

### Test 1 — Knowledge Source Check

> 💬 **You**
>
> What was the "Chair's Message" in my last annual report?

> 🤖 **Grant Fit Check Agent**
>
> Here's the **Chair's Message** from your most recent annual report:
>
> **From Annual Report Summary (FY2024–25)**
>
> *"This past year has reinforced both the importance and the fragility of community-led food programs. Demand for our Community Kitchen meals and Pantry Share hampers continued to rise — up 14% and 11% respectively — while our operating costs grew faster than our revenue. The Board and team have worked hard to maintain service quality in a challenging funding environment.*
>
> *I want to acknowledge our incredible volunteers — over 45 people who gave more than 8,200 hours this year — and our dedicated staff team led by CEO Sarah Chen. Their commitment to our community is the foundation of everything we do."*
>
> **Margaret O'Brien**
> *Chair, Board of Directors*

If you get this back with the correct quote and attribution, your SharePoint knowledge source is connected and indexed.

### Test 2 — Full Grant Assessment

> 💬 **You**
>
> We're considering applying for this grant: https://www.vic.gov.au/community-food-relief-program-local-grants
>
> Please assess whether Southern Community Collective is a good fit. Our org documents are in SharePoint. The grant guidelines DOCX has also been uploaded there.

> 🤖 **Grant Fit Check Agent**
>
> **Decision Block**
>
> **Fit score: Medium (project-dependent)**
>
> **Why it fits:**
> - The grant targets local food relief / food security activities in Victoria and requires direct food relief as part of every project. Your core programs already do this (meals + hampers).
> - Southern Community Collective Inc. is positioned like the "community and volunteer-led organisations" the program calls out, and operates locally in Melbourne's Bayside area.
>
> **Key blocker / risk:**
> - The program explicitly excludes core operational expenses such as rent and current wages. Your stated highest-priority funding need is Kitchen Coordinator salary and facility lease — which would likely be considered core ops and therefore ineligible.
>
> **Best next steps:**
> - Pursue this grant only if you can frame a project around eligible categories (e.g., equipment, infrastructure, additional delivery capacity, volunteer training/recruitment, partnership building) without using funds for existing lease/current wages.
> - Note: the program page currently shows Status: Closed (so treat this as fit assessment for a future round or if it reopens).
>
> ---
>
> **Detailed Breakdown**
>
> *1) Grant snapshot:* Community Food Relief Program – Local Grants, $15,000–$100,000, Status: Closed. All projects must involve direct food relief. Eligible: equipment, infrastructure, supplies, partnerships, training, extra staff. Excluded: rent, insurance, current wages, overheads.
>
> *2) Org profile from SharePoint:* Vision/mission emphasises food access in Bayside region. Community Kitchen (~60–80 people/session), Pantry Share (~120 households/cycle), both growing. Partnerships with OzHarvest, Foodbank Victoria, Bayside Community Health. Strategic Plan flags "non-negotiable" need to cover Kitchen Coordinator salary ($68K) and facility lease ($24K).
>
> *3) Alignment check:*
> - Direct food relief requirement — ✅ Strong match
> - Eligible activity types — ✅ Many good angles (equipment, supplies, training, volunteer uplift)
> - Core ops exclusion — ⚠️ Potential blocker (salary + lease vs. excluded categories)
> - Timing — ⚠️ Currently closed
>
> *4) Recommended project framings:* Capacity uplift for Pantry Share; Kitchen infrastructure refresh; Partnership/network strengthening
>
> *5) Missing info:* Grant guidelines DOCX not found in SharePoint search — used public program page instead.

### How Good Is This Answer?

Cross-referencing against the [Cheat Sheet](../cheat-sheet.md), the agent's response reveals both its strengths and a deliberate gap:

| Designed Disqualifier | Caught? | Details |
|---|---|---|
| **1. Round is closed** | ✅ Yes | Agent flagged "Status: Closed" from the grant web page |
| **2. Excluded use of funds** | ✅ Yes | Agent correctly identified that salary + lease = core ops, which the grant explicitly excludes |
| **3. Geographic priority mismatch** | ❌ No | Agent noted Bayside as the org's location but **did not flag** that Brighton/Bayside is affluent and the grant prioritises regional/rural Victoria and pockets of significant disadvantage (25% weighting criterion) |

**Why this matters for the demo:**

The agent caught **2 out of 3** disqualifiers — which is genuinely useful but not perfect. This is exactly the setup you need for the Trust & Safety conversation in Stage 3:

- It demonstrates real value (the core ops exclusion is buried in guidelines and easy to miss)
- It shows AI isn't infallible (the geographic mismatch was there to find)
- It validates the human-in-the-loop principle — the grants officer still needs to review the output

> **Recovery phrase if this comes up during the demo:**
> *"It caught two out of three. In a real workflow, the Trust & Safety layer helps close that gap."*
> — from the [Cheat Sheet](../cheat-sheet.md)

Also note the agent scored it as **Medium** rather than the expected **NO-GO**. This is because without the full guidelines DOCX in SharePoint, it's working from the public web page which doesn't surface the geographic weighting criteria as clearly. The agent is being appropriately cautious (strict flagging mode) rather than overcommitting to a verdict with incomplete data.

---

## ⚠️ Gotcha: Knowledge Source Override

The agent generated the following knowledge sources in the instructions above:

```
# KNOWLEDGE
- Enable organization-wide SharePoint (excluding OneDrive) for document access.
- Enable organization-wide Teams messages and meetings for context.
- Enable organization-wide email search for grant-related communications.
- Enable public web browsing for grant guidelines.
```

That's sensible for a real organisation — but **we're running a demo with a fictitious org**. Organisation-wide search will pull in real tenant data instead of our dummy documents, and Teams/email search will return nothing useful.

When creating the agent in Copilot Agent Builder, **replace the `# KNOWLEDGE` section** with the following so the agent only looks at the SharePoint site you set up in the [Facilitator Setup Guide](../facilitator-setup-guide.md):

```
# KNOWLEDGE
- For all organisation information (profile, strategy, capability,
  past grants, financials): search ONLY the designated SharePoint
  Site "Southern Community Collective Inc". Do NOT search the public
  web, email, or Teams for organisation details.
- For grant opportunity information (guidelines, eligibility criteria,
  deadlines, funder details): use public web browsing.
- If the user asks a question about the organisation that cannot be
  answered from SharePoint documents, flag it as missing information.
  Do not attempt to find it elsewhere.

Data Source Rules:
- SharePoint (designated folder only): Organisation Profile, Strategic
  Plan, Capability Statement, Past Grants Register, Annual Report,
  uploaded grant guidelines documents.
- Public web: Grant opportunity pages, funder websites, program
  announcements.
- Do NOT use: Organisation-wide email search, Teams messages, OneDrive,
  or web searches about the organisation itself.
```

> **Why this matters:** Without this override, the agent may ground its answers on real documents from your tenant rather than the fictitious Southern Community Collective files — which breaks the demo scenario and the deliberate disqualifiers we designed.
