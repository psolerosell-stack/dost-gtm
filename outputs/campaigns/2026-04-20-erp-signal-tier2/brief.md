# Campaign Brief: ERP Signal — Tier 2 Multi-Persona
Date: 2026-04-20
Campaign type: Signal-triggered outbound
Signal: ERP keyword activity (SAP, Sage, Microsoft Business Central)
ICP tier: Tier 2 (primary), Tier 3 (light variant)

---

## Campaign Objective

Activate accounts showing active ERP signals — job postings, LinkedIn posts, or press mentions of SAP, Sage, or Business Central in a finance context — and convert them into discovery calls by reaching the right persona with the right angle.

**Target:** 20–40 discovery calls from first campaign run.
**Primary outcome:** Meeting booked with Finance Manager, CFO, or IT/ERP Admin.
**Secondary outcome:** Partner/VAR relationships established for referral channel.

---

## Trigger Logic

### Primary trigger (Tier 2 activation)

Account must match ALL of the following:
- Signal type: ERP keyword detected in job posting OR LinkedIn company post
- ERP scope: SAP, Sage (any version), or Microsoft Business Central / Dynamics 365 Business Central
- Recency: Signal fired within last 60 days
- ICP base score: ≥40 pts from firmographic + technographic + organizational scoring
- Industry: food, retail, manufacturing, logistics, automotive, construction, or healthcare
- Geography: Spain or UK

**What the trigger tells us:** Company has confirmed ERP maturity. Invoice volume exists at scale. Finance team is active (they're hiring for ERP-adjacent roles OR they're posting about an implementation). This is the technographic confirmation that raises a cold account into warm territory.

### Signal scoring addition

A confirmed ERP in active use adds to technographic score:
- SAP (any version): +9/10 technographic → likely pushes accounts from Tier 4 to Tier 3/2
- Sage: +7/10 technographic
- Business Central: +8/10 technographic

If the ERP signal is a confirmed GO-LIVE (not just usage): apply the Tier 1 ERP Go-Live signal (40 pts) and escalate immediately — this campaign does not apply.

### Suppression conditions

Do NOT enroll accounts that match any of:
- Active Dost customer (existing account list)
- Active opportunity in CRM (suppress automated sequences)
- Contact unsubscribed in last 90 days
- Known Basware or Medius contract in place
- Contact at same account reached in last 30 days via any other sequence
- Account score < 40 pts after full ICP scoring

---

## Target Segments

| Segment | Persona | Volume estimate | Sequence |
|---------|---------|----------------|----------|
| A | CFO / Finance Director | 20–30% of target list | sequences.md — Persona 1 |
| B | Head of Operations | 15–20% | sequences.md — Persona 2 |
| C | IT Manager / ERP Admin | 15–20% | sequences.md — Persona 3 |
| D | Partner / VAR (indirect) | Separate list | sequences.md — Persona 4 |
| E | AP/AR Specialist | 20–25% | sequences.md — Persona 5 |

**Note on Persona D (Partner/VAR):** This segment targets companies and individuals who implement SAP, Sage, or Business Central for clients — not end customers. This is a separate campaign motion (channel development, not direct sales). Contact list built separately from ERP reseller and consultant databases.

---

## Sequence Architecture (Tier 2)

5–6 touches over 21 days. Email + LinkedIn. Semi-automated with signal variable injection.

| Touch | Day | Channel | Goal |
|-------|-----|---------|------|
| 1 | 0 | Email | Signal hook — ERP reference, insight, frictionless CTA |
| 2 | 3 | LinkedIn | Connection request with 1-line context |
| 3 | 7 | Email | Value shift — proof from similar company, different angle |
| 4 | 12 | Email | Asset or framework — something useful regardless of buying intent |
| 5 | 17 | Phone/VM | Direct ask — short, honest |
| 6 | 21 | Email | Break-up |

---

## Measurement Plan

| Metric | Target |
|--------|--------|
| Reply rate (all touches) | ≥ 4% |
| Positive reply rate | ≥ 2% |
| Meeting booked rate | ≥ 2% |
| Open rate (email) | ≥ 35% |
| LinkedIn accept rate | ≥ 20% |

**First review:** 2 weeks from launch (enough volume to see patterns by persona and ERP type).
**Full review:** 6 weeks — compare performance by ERP signal type (SAP vs. Sage vs. BC) and by persona. Kill lowest-performing persona variant. Double down on best performer.

**What to watch:**
- Which ERP type converts best (SAP users may have more sophisticated finance ops, Sage may indicate smaller/easier decision)
- Which persona responds first — if AP Specialist replies most, the champion sequence is working; if CFO replies, buyer sequence is landing
- Touch number where most replies occur — if it's touch 4+, shorten the front of the sequence

---

## Variables to Inject (Clay / CRM)

| Variable | Source | Used in |
|----------|--------|---------|
| `{{company_name}}` | CRM | All touches |
| `{{first_name}}` | CRM | All touches |
| `{{erp_system}}` | Clay enrichment (job posting / LinkedIn) | Touches 1, 2 |
| `{{erp_signal_type}}` | Manual tag: "job posting" / "go-live post" / "ERP admin hire" | Touch 1 |
| `{{industry_reference_customer}}` | Map by industry: food→VICIO, retail→Primaprix, logistics→[anon] | Touch 3 |
| `{{sender_name}}` | CRM | All touches |

---

## Sender Assignment

- Spain accounts → Fernando Martín or designated SDR (Spanish language sequences)
- UK accounts → Adam Barbera or designated SDR
- Partner/VAR sequence → Adam Barbera (channel development is CEO-led at this stage)
