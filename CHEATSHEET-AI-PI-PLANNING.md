# SAFe CoPilot & AI PI Planning Cheatsheet

A quick-reference guide for Release Train Engineers (RTEs) utilizing AI to automate dependency mapping and risk analysis during Program Increment (PI) planning.

## 1. Pre-PI Readiness Checklist (Automated Auditing)
Before teams arrive for PI Planning, connect your enterprise LLM to your backlog to run these automated checks:
*   [ ] **Identify Undocumented Debt:** Have the AI flag features lacking clear architectural definitions or un-estimated epics.
*   [ ] **Cross-Board Scanning:** Instruct the natural language processor to scan feature descriptions and map shared API dependencies automatically.
*   [ ] **Draft Summaries:** Have the AI compile initial backlog health reports into structured executive overviews.

## 2. Deterministic Prompts for AI Risk Analysis
Vague prompts create hallucinations. Use precise, contextual prompting to audit planning boards during the draft review phase.

**Prompt 1: Capacity vs. Historical Velocity**
> *"Analyze the draft PI board for Team [Name]. Cross-reference their committed sprint load against their 3-quarter rolling velocity. Flag any overlapping dependency timelines and generate a risk severity score from 1-5."*

**Prompt 2: Dependency Collision Detection**
> *"Identify any sprints where dependencies from Team [A] land in the same iteration as the target delivery date for Team [B]. List the associated feature IDs and draft a brief summary of the potential bottleneck."*

## 3. Human-In-The-Loop (HITL) Safeguards
AI cannot read team dynamics. **Always intervene manually when:**
1.  **Capacity Negotiation:** AI flags a capacity issue, but human context (e.g., a developer returning from leave, unrecorded legacy tech debt) changes the reality.
2.  **Stakeholder Communications:** AI drafts the PI report or status update. You must audit the tone and ensure sensitive corporate micro-politics are properly navigated before sending.
3.  **Conflict Resolution:** AI highlights severe misalignment between two distributed teams. Do not let the bot send an alert; use your "Empathy Moat" to facilitate a live mediation session.
