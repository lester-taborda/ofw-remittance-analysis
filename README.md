# The $30B Lifeline: Understanding OFW Remittance Trends

Google Data Analytics Certificate — Capstone Project
Analyst: Lester John Taborda | March 2026

📊 [View Interactive Dashboard — Tableau Public](https://public.tableau.com/views/OFWRemittanceAnalysis-UnderservedCorridors2019-2024/OFWRemittanceAnalysis?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

---

## Business Task

Analyze OFW remittance data to identify high-volume corridors underserved by formal banking channels, and provide a Philippine commercial bank with data-driven recommendations on where to prioritize digital remittance expansion.

---

## Background

Every year, millions of Overseas Filipino Workers (OFWs) send money home — collectively over $34 billion in 2024 alone. Yet a significant portion of these remittances still flows through informal channels rather than the formal banking system. Philippine commercial banks face a strategic challenge: OFW remittance volumes are large and growing, but bank usage nationally sits at only 61% (PSA SOF 2024). The remaining 39% flows through money transfer operators and informal channels.
Without corridor-level data on where this gap is largest, expansion decisions are made without a clear evidence base. This project builds that evidence base.

---

## Data Sources

| Source | Dataset | Use |
| Bangko Sentral ng Pilipinas (BSP) | Cash Remittances by Country, 2019–2024 | Primary — corridor volume and ranking |
| Philippine Statistics Authority (PSA) | Survey on Overseas Filipinos (SOF) 2019–2024, Table 9/6 | Supplementary — bank vs. non-bank usage rates |

Both datasets are publicly available from Philippine government institutions. Full documentation in [Deliverable 2 — Data Sources](deliverables/Deliverable_2_Data_Sources.docx).

---

## Process
Tools: Google Sheets (cleaning and analysis), Tableau Public (visualization)

Cleaning highlights:
- Scoped BSP data to 27 corridors meeting the ≥ USD 100M annual threshold
- Validated all 6 annual grand totals against BSP published figures
- Resolved Taiwan naming inconsistency across years
- Applied PSA 2024 bank usage rate (61%) as national proxy for non-bank estimation

Full cleaning decisions documented in the working file's CLEANING_LOG tab.

---

## Key Findings

Finding 1 — US corridor dominance is structural
At $14.01B in 2024, the US corridor is 5.6× larger than #2 Singapore and accounts for ~40.6% of all tracked OFW remittances. Over 6 years, the US corridor generated a cumulative $77.1B.

Finding 2 — COVID created a tale of two corridors
Western corridors (US +5.5%, Singapore +12.7%) grew in 2020 while Gulf labor corridors contracted sharply (Kuwait -23.5%, Bahrain -29.2%, UAE -19.2%). Recovery has been uneven — Saudi Arabia returned to above-2019 levels by 2023, but UAE and Kuwait have not.

Finding 3 — High-CAGR emerging corridors signal opportunity
Cyprus (+14.9%), Greece (+14.7%), Panama (+13.9%), Taiwan ROC (+9.7%), and Malaysia (+7.2%) are growing 2–3× faster than top-volume corridors.

Finding 4 — $13.04B flows outside formal banking annually
Applying the 39% non-bank proxy across 27 corridors using 2024 volumes, an estimated $13.04B annually flows outside formal banking. The US corridor alone accounts for $5.47B — 41.9% of total estimated opportunity.

---

## Recommendations

| Priority | Corridor(s) | Rationale |
| 1 — Immediate | United States | $5.47B non-bank opportunity, 40.6% of total. Single corridor justifies dedicated digital infrastructure. |
| 2 — Near-term | Saudi Arabia, Qatar | Post-COVID recovery ongoing, growing CAGR. Competitive fee structures can capture displaced flows. |
| 3 — Strategic | Cyprus, Taiwan ROC, Malaysia | High CAGR (7–15%). Early infrastructure before volumes peak = first-mover advantage. |

---

## Limitations

- PSA bank usage rate (61%) applied uniformly as national proxy — corridor-level mode data is not available in public datasets
- Partial-year data for 3 corridors (Israel, Liberia, Marshall Islands) that entered the threshold mid-period
- UAE and Kuwait CAGR trends suggest structural workforce reduction post-COVID — directional but requires further validation

---
## Deliverables

- 📊 [Interactive Tableau Dashboard](https://public.tableau.com/views/OFWRemittanceAnalysis-UnderservedCorridors2019-2024/OFWRemittanceAnalysis?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)
- 📁 Cleaned Analysis File — BSP_OFW_Analysis.xlsx
- 📄 [Data Sources Documentation](Deliverable_2_Data_Sources.docx)
- 📑 [Presentation](OFW_Analysis_Presentation.pptx) 

---

## Repository Structure
ofw-remittance-analysis/
├── README.md
├── Deliverable_2_Data_Sources.docx
├── OFW_Analysis_Presentation_v2.pptx
│
└── viz/
└── tableau_dashboard_link.md
