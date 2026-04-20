# Persona: IT Manager / CTO (Technical Evaluator)

---

## Overview

**Title(s):** IT Manager, Head of IT, CTO, Technical Director, Systems Administrator, ERP Administrator
**Typical seniority:** Manager / Director
**Decision role:** Technical evaluator — validates integration feasibility, security, and implementation approach. Can block a deal; rarely initiates.
**Found at companies:** Mid-market 150–1,000 employees where IT is a centralized function. At larger companies, this role may be an ERP specialist or IT Director.

---

## What They Care About

**Their primary metric:** System uptime, integration reliability, implementation risk, security posture, maintenance burden

**Their biggest problem right now:** Finance teams keep requesting new tools that require IT to set up and maintain. They're stretched. Any new integration needs to work reliably with their ERP and not require ongoing developer support. They've been burned by tools that promised "easy integration" and required 3 months of custom development.

**What a good week looks like for them:** New tools are self-service for the business team. Integrations run without alerts. No tickets from finance complaining that the system is down or a supplier format broke.

**What a bad week looks like:** Finance submits an IT ticket because a new invoice format isn't being recognized. The ERP sync broke and AP/AR data is out of date. They're debugging a webhook that was "supposed to just work."

---

## How They Buy

**Involvement in purchase:** Not the initiator — brought in after Finance Manager or CFO decides to evaluate. Their job is to validate that the tool is technically viable and won't create IT debt. Can veto if integration is complex or security concerns arise.
**Discovery behavior:** Product documentation, API docs, integration marketplace listings for their ERP
**Evaluation style:** Technical — wants to see the API, understand the ERP integration method (native connector vs. API vs. flat file), ask about data residency and security certifications, and understand what happens when a new document format appears
**Common objections:**
- "We'll need to do custom development" → Dost has native connectors for SAP, NetSuite, Dynamics, Sage — no custom dev; walk through the integration architecture
- "What's the data security / GDPR posture?" → [inferred: EU-hosted, GDPR-compliant; confirm details internally]
- "Who maintains it when formats change?" → Dost's AI auto-adapts to new supplier formats without IT intervention — this is the core value for IT

---

## How to Reach Them

**Best channel:** Directly in product evaluation stage (they're introduced by Finance Manager), or via ERP integration documentation/marketplace
**Best time:** During technical evaluation phase, not initial outreach
**What gets their attention:** Specific integration architecture documentation, security whitepaper, reference from same ERP stack, commitment to ongoing maintenance
**What gets ignored:** Business ROI messaging, month-end close stories — they care about technical fit, not outcomes

---

## Message Framework

**Value prop for this persona:**
Dost is a finance-team-native tool — once integrated, IT doesn't touch it. Native ERP connectors for SAP, NetSuite, Dynamics, and Sage. AI auto-adapts to new supplier formats. No ongoing developer maintenance.

**Proof points that resonate:**
- Native ERP integrations (not custom webhook configurations)
- Finance team owns the tool after go-live — no IT tickets for new document formats
- Verifactu and EU e-invoicing compliance built in

**Reference customers for this persona:**
- IASO (healthcare) — complex document environment; IT team not involved post go-live

---

## Sample Outreach Hooks

*(This persona is rarely cold-outreached — they join the deal in technical evaluation. These hooks are for if they're looped in directly.)*

**During evaluation:**
> "Happy to walk through the ERP integration architecture specifically. We have a native [SAP/NetSuite/Dynamics/Sage] connector — no custom development required. What questions do you have on the integration side?"

**If they raise concerns about maintenance:**
> "The piece that typically matters most to IT teams: our AI handles new supplier formats automatically. Finance teams can add a new supplier without submitting a ticket. We can demo exactly how that works."
