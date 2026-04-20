# ICP Batch Score
Date: 2026-04-20
Scored by: Claude
Accounts: Volotea, VICIO, Juvé i Camps, JSV Logistic, Desigual

---

## Summary Table

| Account | Firmographic | Technographic | Organizational | Signals | **Total** | **Tier** | Action |
|---------|-------------|--------------|---------------|---------|-----------|----------|--------|
| VICIO | — | — | — | — | **EXISTING CUSTOMER** | Suppress | Do not contact. Use as reference. |
| Desigual | 19/30 | 16/20 | 10/20 | 0/30 | **45** | **Tier 3** | Add to automated sequence |
| JSV Logistic | 21/30 | 11/20 | 6/20 | 0/30 | **38** | **Tier 4** | Monitor — re-score if ERP or hiring signal fires |
| Juvé i Camps | 20/30 | 10/20 | 6/20 | 0/30 | **36** | **Tier 4** | Monitor — re-score if signal fires |
| Volotea | 11/30 | 8/20 | 10/20 | 0/30 | **29** | **Tier 4** | Monitor — industry mismatch is structural |

---

## Detailed Scores

---

### VICIO — ⛔ Existing Customer

**Status:** Active Dost customer. Samuel Nájera (Head of Accounting & Treasury) is a named reference.

Do not outreach. Flag as reference account. Use in outbound sequences targeting food/restaurant chains — VICIO is the best proof point for that vertical.

**Re-score trigger:** Not applicable. Flag for expansion conversation if AP volumes have grown since go-live.

---

### Desigual — Score: 45 | Tier 3

**Company:** Fashion retail, Barcelona. ~3,000 employees. €332M revenue (2024). Private.

| Category | Score | Max | Notes |
|----------|-------|-----|-------|
| Firmographic fit | 19 | 30 | Retail (10/10); ~3,000 employees — outside sweet spot but not anti-ICP (4/10); private/profitable, no investor event (5/10) |
| Technographic fit | 16 | 20 | SAP confirmed since 2008, likely SAP ECC or S/4HANA (9/10); no known AP competitor tool (5/5); secondary tools unknown (2/5) |
| Organizational fit | 10 | 20 | At 3,000 employees, finance leadership certain (10/10); no recent finance hire confirmed (0/5); no AP hiring detected (0/5) |
| Active signals | 0 | 30 | No Tier 1 or Tier 2 signal identified |
| **Total** | **45** | **100** | |

**Tier Assignment: Tier 3 — Add to automated sequence**

**What qualifies them:**
- SAP confirmed → exact ERP stack Dost integrates with natively
- Fashion retail with global operations → high supplier invoice volume (manufacturing, logistics, customs)
- Large finance function (100% certainty at this size)

**What reduces score:**
- 3,000 employees is at the top edge of ICP; risk of enterprise procurement motion
- No active signal → no urgency hook
- Private company with €332M revenue; likely has some finance tech in place already (unknown)
- Employee count above sweet spot means more stakeholders, longer sales cycle

**Recommended next action:** Add to Tier 3 automated sequence (ERP signal campaign — SAP variant). If a signal fires (ERP upgrade, finance leadership hire, or funding event), immediately escalate to Tier 1/2 and run Account Research skill.

**Re-score trigger:** SAP S/4HANA migration announced (Desigual may still be on SAP ECC — a migration would be a Tier 1 signal). New CFO hired. Any LinkedIn post about digitization or AP transformation.

---

### JSV Logistic — Score: 38 | Tier 4

**Company:** Multimodal freight logistics company. Miranda de Ebro, Burgos, Spain. 260+ employees. Private. 30+ years operating.

| Category | Score | Max | Notes |
|----------|-------|-----|-------|
| Firmographic fit | 21 | 30 | Logistics (10/10); 260 employees — lower end of range but within ICP (8/10); private, no investor event (3/10) |
| Technographic fit | 11 | 20 | ERP likely (logistics of this size needs TMS/ERP) but not confirmed (5/10); no AP competitor detected (5/5); secondary TMS tools likely (1/5) |
| Organizational fit | 6 | 20 | Finance team likely 2–3 people at 260 employees (6/10); no evidence of recent finance hire (0/5); no AP hiring detected (0/5) |
| Active signals | 0 | 30 | No Tier 1 or Tier 2 signal identified |
| **Total** | **38** | **100** | |

**Tier Assignment: Tier 4 — Monitor**

**What qualifies them:**
- Logistics is primary ICP vertical — multimodal freight = high supplier invoice volume (trucking, rail, customs, port fees)
- 260 employees is ideal size for Dost (finance team exists, budget available, not enterprise-complex)
- Spain-based, in ICP geography

**What reduces score:**
- No confirmed ERP → technographic fit is inferred
- Private company with no visible digitization trigger
- Small finance team means limited budget and slower decision cycle
- No signals visible from public data

**Recommended next action:** Enrich with Clay — confirm ERP stack and finance team size. If ERP is confirmed (SAP/Sage/Business Central), score would rise to ~46+ → Tier 3. If a hiring signal fires, re-evaluate immediately.

**Re-score trigger:** Job posting for Finance/AP role. ERP implementation mentioned in LinkedIn. Any press coverage. Logistics contract expansion or new facility announcement.

---

### Juvé i Camps — Score: 36 | Tier 4

**Company:** Family-owned cava and wine producer. Sant Sadurní d'Anoia, Catalonia. Founded 1921. ~3M bottles/year, 2,700 acres. Employee count [inferred: 150–350].

| Category | Score | Max | Notes |
|----------|-------|-----|-------|
| Firmographic fit | 20 | 30 | Food/beverage production (10/10); estimated 150–350 employees (7/10); family-owned since 1921, no VC funding (3/10) |
| Technographic fit | 10 | 20 | ERP inferred for winery at this scale (likely Sage or SAP Business One) — not confirmed (5/10); no AP competitor detected (5/5); secondary tools unknown (0/5) |
| Organizational fit | 6 | 20 | Finance team likely 2–4 people at this size (6/10); no recent hire confirmed (0/5); no AP hiring detected (0/5) |
| Active signals | 0 | 30 | No Tier 1 or Tier 2 signal identified. (Note: company appears on Mercado de Facturas invoice financing platform — weak AR signal but not from our signal library) |
| **Total** | **36** | **100** | |

**Tier Assignment: Tier 4 — Monitor**

**What qualifies them:**
- Food/beverage manufacturing is primary ICP vertical
- High supplier invoice volume at scale: grape growers, equipment, bottling materials, logistics, export documentation
- Spain-based, in ICP geography
- Presence on invoice financing platform hints at AR complexity

**What reduces score:**
- Family-owned, centenary company — historically conservative about technology adoption
- No investor driving digitization spend
- Employee count is inferred — actual headcount may be below 150 (seasonal workers counted differently)
- No confirmed ERP

**Recommended next action:** Enrich to confirm employee count and ERP stack. If they're on Sage or SAP Business One (common in Spanish wineries at this scale), score rises to ~46 → Tier 3. Monitor LinkedIn for any ERP upgrade or finance hire signal.

**Re-score trigger:** Any job posting mentioning ERP or finance. Verifactu compliance announcement (Spanish winery → Spain-mandated e-invoicing directly applies). Export expansion into UK (new geography = invoice complexity increase).

---

### Volotea — Score: 29 | Tier 4

**Company:** Low-cost regional airline. Barcelona, Spain. ~2,000 employees. €840M revenue forecast 2025. €56M total raised (mix of founder/Aegean/PAR Capital). CFO: Stephen Rapp (25-person finance team).

| Category | Score | Max | Notes |
|----------|-------|-----|-------|
| Firmographic fit | 11 | 30 | Aviation — not in ICP verticals (0/10); ~2,000 employees (6/10); profitable, no investor-driven digitization trigger (5/10) |
| Technographic fit | 8 | 20 | ERP unknown — airlines use specialized systems (airline OPS, PSS, accounting) not standard ERP (3/10); no AP competitor detected (5/5); secondary tools unknown (0/5) |
| Organizational fit | 10 | 20 | Finance team of 25 confirmed, CFO identified (10/10); recent finance hire unknown (0/5); AP hiring unknown (0/5) |
| Active signals | 0 | 30 | No Tier 1 or Tier 2 signal identified |
| **Total** | **29** | **100** | |

**Tier Assignment: Tier 4 — Monitor (with flag)**

**What qualifies them:**
- Large finance team (25 people) with identified CFO
- High supplier invoice volume: fuel suppliers, catering, airport fees, maintenance contractors, crew services
- Spain-based

**Why the score is low:**
- **Industry mismatch is structural:** Aviation is not in Dost's defined ICP verticals. Airline procurement uses specialized systems (PSS, GDS, aviation-specific ERP modules) that differ from our integration profile.
- No ERP confirmation — may use specialized airline finance software incompatible with Dost's current integrations
- Revenue/scale suggests enterprise procurement motion, not mid-market

**Recommended next action:** Do not activate. Log as Monitor. Revisit only if Volotea announces a move to SAP or a standard ERP for finance operations — that would change the technographic picture.

**Re-score trigger:** Job posting for finance roles mentioning SAP/Sage/Business Central specifically. Press release about ERP modernization. New CFO in seat (Stephen Rapp replaced).

---

## Batch Calibration Note

All 5 accounts scored 0 on signals — none have active Tier 1 or Tier 2 signals firing today. Before activating any of these accounts, run a Clay enrichment to:
1. Confirm ERP stack (most likely to unlock Desigual → Tier 2, JSV and Juvé i Camps → Tier 3)
2. Check for open finance/AP job postings (most impactful signal available)
3. Confirm headcount on LinkedIn (especially Juvé i Camps — under-researched)
