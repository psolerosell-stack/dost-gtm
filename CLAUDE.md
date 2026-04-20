# CLAUDE.md

This file is the persistent context layer for Dost's GTM repository. Claude reads it automatically at the start of every session.

Full context lives in `context/`. This file is the summary layer.

---

## Company

**Dost** helps mid-market finance teams in Europe automate invoice processing end-to-end — without manual data entry, matching errors, or week-long approval cycles.

Stage: Series A — ~30 employees, GTM team in Spain and UK
HQ: Barcelona, Spain | London, UK (opened Nov 2025)
Website: dost.io

GTM motion: Sales-led
ACV: [inferred: €15,000–€80,000] | Sales cycle: [inferred: 30–90 days]
Primary channels: Outbound (primary), Inbound (growing), Events (finance conferences)

---

## ICP

Full definition: `context/icp-definition.md`

**Who we sell to:** Mid-market companies (150–2,000 employees) in food, retail, manufacturing, logistics, automotive, construction, or healthcare — in Spain or UK — running SAP/NetSuite/Dynamics/Sage, with a finance team of 3+ managing high invoice volume.

**Tier 1 (Top 150):** 300–1,500 employees, Spain or UK, SAP/NetSuite/Dynamics, finance team 5+, recent ERP go-live or funding round or AP hiring signal

**Tier 2 (500–1,000):** 150–3,000 employees, Spain or UK, any ERP, adjacent verticals, at least one Tier 1 or Tier 2 signal fired in last 60 days

**Tier 3 (1,000–5,000):** 100–3,000 employees, Spain or UK, B2B with suppliers, finance team exists — automated outreach only

**Never target:**
- Pure SaaS companies — low invoice volume, AP automation is not a pain point
- <100 employees — no budget, no dedicated finance team
- Enterprise >3,000 employees without named champion — different procurement motion
- Public sector — multi-year procurement cycles, non-commercial compliance requirements
- Companies already locked into Basware or Medius contracts — switching cost too high
- Outsourced AP providers — channel conflict

---

## Personas

Full profiles: `context/personas/`

| Role | Title(s) | Primary concern | Best channel |
|------|----------|----------------|-------------|
| Champion | Finance Manager, Head of Accounting, AP Manager | Invoice processing speed, team overtime, error rate | Email, LinkedIn |
| Economic buyer | CFO, Finance Director, VP Finance | Cost reduction, operational leverage, accuracy | Peer intro, Email |
| Technical evaluator | IT Manager, ERP Admin, CTO (at smaller cos) | Integration reliability, maintenance burden | During eval only |

---

## Positioning

Full document: `context/positioning.md`

**We win when:** The buyer is a Finance Manager who has lived through manual month-end hell and has a CFO willing to fund automation. ERP is already in place. Multiple suppliers with varied document formats.

**We lose when:** No internal champion willing to drive adoption, or CFO views headcount as the cheaper solution, or account already has Basware/Medius in a long-term contract.

vs. Yooz: Proprietary AI (not templates) + unified AP+AR; Yooz is AP-only with generic extraction
vs. Rossum: Finance-team-native, no IT dependency; Rossum requires developer configuration
vs. Medius: Right-sized for mid-market; Medius is overbuilt and over-priced for <600-employee companies
vs. Basware: Built for mid-market; Basware is enterprise at enterprise pricing

**Voice:** Direct and outcome-focused. Write like a peer who's seen the problem before. No "AI-powered" buzzwords — say what it does. No generic ROI language — use real numbers.

---

## Signals

Full library: `context/signal-library.md`

**Act immediately (Tier 1):**
1. **ERP Go-Live or Upgrade** — company announces SAP/NetSuite/Dynamics/Sage go-live on LinkedIn or in job postings → evaluation window for AP automation is open right now (40 pts)
2. **Hiring AP/AR or Accounting Leadership** — open role for AP Manager, Head of Accounting, AR Specialist open 15+ days → manual invoice workload is at capacity, CFO is weighing hire vs. automate (35 pts)
3. **Funding Round Announced** — Seed or later, €1M+, in last 30 days → CFO is accountable to investors for operational efficiency, digitization budget unlocked (30 pts)

**Add to sequence (Tier 2):**
1. **Verifactu / E-Invoicing Compliance Mention** — Spanish company posts about Verifactu or AEAT compliance → regulatory urgency driving evaluation (20 pts)
2. **Multi-Location / International Expansion** — new office, new country, or acquisition announced → invoice complexity just multiplied (20 pts)

---

## Stack

CRM: [to be confirmed] | Enrichment: Clay (recommended) | Signals: LinkedIn, Crunchbase, Google Alerts
Outbound: [to be confirmed] | Call intel: [to be confirmed] | Intent: [none configured yet]

---

## Team

| Name | Role | Owns |
|------|------|------|
| Adam Barbera | CEO | UK GTM, executive relationships |
| Fernando Martín | COO | Spain operations, existing customer base |
| Naqqash Abassi | CTO | Product, integrations |

---

## This Week

- [ ] [Update with current priorities — see context/profile.md for quarterly focus]
- [ ] UK outbound: manufacturing and logistics accounts, 200–1,500 employees
- [ ] Spain: Verifactu compliance campaign for existing Tier 2 accounts

---

## Quick Commands

```
# Research an account
Read skills/account-research/SKILL.md and research [company.com]

# Score a list
Read skills/icp-scoring/SKILL.md and score these accounts: [paste list]

# Build a campaign
Read skills/signal-to-sequence/SKILL.md — build a Tier 2 campaign for
accounts that triggered [signal name], targeting [Finance Manager / CFO]

# Weekly pipeline review
Read skills/weekly-update/SKILL.md and run the weekly update
```
