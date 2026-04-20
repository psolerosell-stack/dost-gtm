# Signal Library

Last updated: 2026-04-20

---

## Signal Scoring Model

| Score | Tier | Action |
|-------|------|--------|
| 80–100 | Hot | AE alert within 2 hours. Research brief within 24 hours. Outreach within 48 hours. |
| 60–79 | Warm | SDR triggers Tier 2 sequence within 48 hours. |
| 40–59 | Cool | Add to Tier 3 automated sequence. |
| 0–39 | Cold | Log and monitor. No outreach. |

---

## Tier 1 Signals — Act Immediately

### Signal: ERP Go-Live or Upgrade Announced

**Category:** Technographic / Organizational
**Points:** 40
**Source:** LinkedIn company posts, LinkedIn job postings, Crunchbase news, Google alerts
**Refresh cadence:** Weekly

**Definition:** Company announces completion of or active migration to SAP S/4HANA, NetSuite, Microsoft Dynamics 365, or Sage implementation. Includes job postings requiring "SAP implementation experience" or "post go-live support."

**Why it predicts fit:** ERP go-lives create an immediate evaluation window for adjacent automation tools. Finance teams have just finished a major project and are now looking to extract value — AP automation is the next logical spend. Pain is at its peak: manual processes are fully visible in the new system.

**Detection method:**
```
Clay: LinkedIn company posts → keyword filter ["SAP go-live", "NetSuite implementation", "Dynamics 365 launch", "new ERP", "digital transformation finance"]
LinkedIn: Job posts from finance team mentioning ERP + automation skills in last 30 days
Google Alert: "[company name] + ERP + implementation"
```

**Message hook:** "Saw [Company] went live on [ERP] — congrats on the rollout. Most finance teams find this is exactly when manual invoice handling becomes the next thing to fix."

---

### Signal: Hiring for AP/AR or Accounting Leadership Role

**Category:** Organizational
**Points:** 35
**Source:** LinkedIn Jobs, Clay
**Refresh cadence:** Daily

**Definition:** Company posts an open role for any of: Accounts Payable Manager, Head of Accounting, Treasury Manager, Finance Operations Manager, AP Specialist, AR Specialist, Financial Controller. Role has been open 15+ days.

**Why it predicts fit:** A company hiring for manual AP/AR roles is explicitly signaling that invoice volume has outgrown current capacity. This is the exact moment a CFO is weighing "hire vs. automate." We arrive when the question is live — not after it's been answered by a new hire who now defends their job by resisting automation.

**Detection method:**
```
Clay: LinkedIn Jobs → filter by title ["accounts payable", "AP manager", "AR specialist", "treasury", "head of accounting"] + company firmographic filters (size, industry, geo)
Apollo: similar job title + company filters
Refresh: daily scan, flag if open >15 days
```

**Message hook:** "Noticed [Company] is looking for an AP Manager — that search usually means invoice volume is outpacing the team. Worth a 15-minute call to see if we can solve it without the hire?"

---

### Signal: Funding Round Announced (Seed or Later)

**Category:** Firmographic
**Points:** 30
**Source:** Crunchbase, LinkedIn, TechCrunch, EU-Startups
**Refresh cadence:** Real-time (alert-based)

**Definition:** ICP-fit company announces a funding round of €1M+ within the last 30 days. Applies to Seed through Series B; Series C+ may indicate enterprise motion that diverges from our sweet spot.

**Why it predicts fit:** Post-funding, CFOs unlock digitization budgets. Finance infrastructure investment spikes in the 90 days after a round as companies professionalize. The CFO is accountable to investors for operational efficiency — AP automation is a visible, fast-ROI win.

**Detection method:**
```
Crunchbase: set up saved search + email alert for funding events → filter by industry + geography
LinkedIn: monitor "we're thrilled to announce" posts in company feed
Clay: Crunchbase funding enrichment on account list, flag if funded_date < 30 days ago
```

**Message hook:** "Congrats on the raise — finance teams at this stage usually hit an inflection point where invoice volume starts to outpace the team. Happy to show you how [similar company] cut processing time by 80% right after their Series A."

---

## Tier 2 Signals — Add to Active Sequences

### Signal: Verifactu / E-Invoicing Compliance Mention

**Category:** Behavioral / Regulatory
**Points:** 20
**Source:** LinkedIn posts, company blog, Google alerts
**Refresh cadence:** Weekly

**Definition:** Spanish company mentions Verifactu, AEAT compliance, or mandatory e-invoicing in company communications, job postings, or press in last 60 days.

**Why it predicts fit:** Spain's Verifactu mandate creates an external compliance deadline that forces finance teams to evaluate their invoice handling infrastructure. It's a regulatory forcing function — companies can no longer delay digitization. We have compliance built-in.

---

### Signal: Multi-Location or International Expansion Announcement

**Category:** Organizational / Firmographic
**Points:** 20
**Source:** LinkedIn, press releases, company blog
**Refresh cadence:** Weekly

**Definition:** Company announces opening of new offices, entering a new country, or acquiring another entity in the last 60 days. Or job postings show hiring in a new geography.

**Why it predicts fit:** Multi-entity expansion multiplies invoice complexity — new supplier relationships, new currencies, new approval hierarchies. Companies that just expanded are immediately aware that their existing AP process doesn't scale across entities.

---

## Tier 3 Signals — Monitor

- **Tech stack includes Excel or Google Sheets for AP** (+5 pts) — visible in job postings; signals fully manual process
- **Finance team grew by 2+ people in last 6 months** (+5 pts) — LinkedIn headcount signal; volume growing faster than automation
- **G2 intent signal for AP automation category** (+5 pts) — if using G2 Buyer Intent; indicates active evaluation
- **CEO or CFO posted about operational efficiency or scaling** (+5 pts) — LinkedIn behavioral signal; mindset aligned

---

## Signal Combinations

| Combination | Combined Score | What it means | Action |
|-------------|----------------|---------------|--------|
| Funding Round + AP Hiring | +15 bonus (total: 65) | Budget just unlocked AND pain is confirmed today | AE alert immediately, skip SDR qualification |
| ERP Go-Live + AP Hiring | +20 bonus (total: 75) | System is in place AND team is at capacity | Priority Tier 1 outreach within 24 hours |
| Funding Round + Multi-Location Expansion | +10 bonus (total: 60) | Growth-stage company scaling AP complexity | Executive-led outreach, lead with multi-entity case study |
| Verifactu mention + ERP mention | +15 bonus (total: 55 for Spain accounts) | Regulatory urgency + systems in motion | Compliance-led sequence, deadline-anchored messaging |

---

## Suppression Rules

- Account is an existing customer → suppress all outreach
- Contact has unsubscribed in last 90 days → suppress email
- Active opportunity in CRM → suppress automated sequences
- Account is in Basware or Medius contract (if known) → suppress for 6 months

---

## Signal Decay

| Signal age | Score multiplier |
|------------|-----------------|
| 0–30 days | 100% |
| 31–60 days | 75% |
| 61–90 days | 50% |
| 91–180 days | 25% |
| 180+ days | 0% (signal expires) |

Run a weekly batch to recalculate scores with decay applied.

---

## Signal Performance Log

| Signal | Outreach sent | Replies | Meetings | Pipeline | Notes |
|--------|--------------|---------|----------|----------|-------|
| ERP Go-Live | | | | | |
| AP/AR Hiring | | | | | |
| Funding Round | | | | | |
| Verifactu Mention | | | | | |
| Multi-Location Expansion | | | | | |
