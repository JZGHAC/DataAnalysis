# Research record: digital advisory for chemical-dose optimisation, RO diagnostics, CIP, and replacement forecasting

**Research date:** 2026-07-17  
**Question:** Can a new digital advisory solution, combining Hydranautics membrane knowledge with plant data, O&M and chemical expertise, credibly deliver prescriptive recommendations for chemical dosage, CIP, and membrane replacement in chlor-alkali and fertiliser applications? What is required to demonstrate implementation credibility and savings causality?  
**Repository constraint:** Local repository only; no public-web search performed.

## 1. Executive answer

**[Engineering inference]** The repository provides a credible *technical basis* for an advisory that (1) normalizes RO performance, (2) diagnoses fouling from performance and feed/pretreatment data, (3) gates CIP and chemical selection on identified foulants, and (4) forecasts condition-based intervention. It does **not** provide evidence of an existing Hydranautics digital advisory product, a chlor-alkali deployment, a fertiliser deployment, a validated savings-attribution protocol, or a general dose-optimisation model.

**[Recommendation]** Position the project as a jointly delivered, plant-specific decision-support pilot-not an autonomous chemical-dose controller. Secure: the customer/plant operator and O&M team; Hydranautics membrane/OEM expertise; the chemical supplier; the system integrator/data historian owner; and an independent customer finance/technical validator. Do not claim savings until the trial protocol, baseline, comparators, data-quality controls, intervention log, and customer sign-off are agreed in writing.

**[Directly sourced fact]** Hydranautics' current cleaning bulletin makes normalized permeate flow, permeate quality, and pressure drop the core performance measures for identifying fouling; for high-fouling industrial/municipal wastewater it lists 20%, 20%, and 30% deviation values, respectively, from stabilized performance. [S1, p. 2]

**[Directly sourced fact]** The strongest repository dose-economics example is municipal wastewater, not chemical industry: a tested CaPO4-specific antiscalant allowed pH 7 operation without calcium-phosphate scale; the source reports the tested antiscalant cost was 43% lower and calculates a 62% annual RO chemical-cost reduction when acid savings were included. This is a site-specific result under its stated chemistry and is not a transferable chlor-alkali or fertiliser dose. [S3, p. 5]

## 2. Research scope, interpretation, and method

### Scope

Included: RO/NF diagnostics; pretreatment/chemical dosing; CIP decision rules and chemical selection; condition monitoring and intervention/replacement forecasting; chemical-industry evidence; chlor-alkali and fertiliser applicability. Excluded: electrolyser membrane selection, unverified customer economics, public-web sources, and a plant-specific dose or replacement date.

### Terms, acronyms, and synonyms searched

- RO = reverse osmosis; NF = nanofiltration; CIP = clean-in-place. [taxonomy: `knowledge/taxonomy/acronyms.csv`]
- Differential pressure = pressure drop = delta-P; antiscalant = scale inhibitor; permeate = product water; concentrate = reject/brine (context dependent). [taxonomy: `knowledge/taxonomy/synonyms.csv`]
- Additional search terms: chlor-alkali/chlor alkali, fertiliser/fertilizer, chemical industry/manufacturer, chemical dose/dosage, acid dosing, antiscalant, normalised/normalized performance, diagnostics, monitoring, advisory, analytics, forecast/prediction, membrane life/replacement, savings, validation, KPI, and causality.

### Repository workflow completed

1. Searched `catalog/document_catalog.csv` before broader corpus review.
2. Searched the relevant indexes: `cleaning_methods.json`, `troubleshooting_symptoms.json`, `control_variables.json`, `sensors.json`, `technical_performance_metrics.json`, `chemicals.json`, `industries.json`, and `failure_modes.json`.
3. Read normalized content for S1-S6 and inspected the original PDF pages cited below. Original-page extraction confirmed the cleaning table, chemical recipes, case-study operating table, performance charts, and forecasting assumptions.
4. Checked `catalog/document_versions.csv`; no superseding relationship is recorded for the core sources.

## 3. Relevant process / technology explanation

**[Directly sourced fact]** RO fouling may arise from mineral scale, metal oxides, polymerized silica, inorganic or mixed colloids, natural/man-made organics (including antiscalant/dispersant and cationic polyelectrolytes), and biological material. Feedwater quality and system recovery affect the nature and rapidity of fouling. [S1, p. 2]

**[Directly sourced fact]** Hydranautics says that, when operating conditions vary, permeate flow, permeate back-pressure, recovery, temperature, and feed TDS should be normalized to distinguish fouling from a change in a critical operating parameter. [S1, p. 2]

**[Directly sourced fact]** Its cleaning guidance requires investigating the signs of fouling before selecting cleaning chemicals/protocol. Typical complex-fouling sequence: permeate flush with a non-oxidising biocide; high-pH CIP; rinse until brine-side pH is below 8.5; low-pH CIP; acid/permeate flush with non-oxidising biocide. It also warns that an incorrect chemical or sequence can worsen fouling. [S1, p. 6]

**[Engineering inference]** A suitable advisory architecture is therefore: plant historian/lab/CIP records -> quality validation and normalization -> diagnostic rules/model -> expert-approved recommendation -> recorded intervention -> post-intervention outcome measurement. The rule/model must prevent a direct dosage recommendation when chemistry, instrument quality, or membrane compatibility is unverified.

## 4. Evidence table

| Conclusion and classification | Exact supporting evidence | Applicability / limit | Source anchor |
|---|---|---|---|
| Normalized RO trends can support diagnostics - **directly sourced fact** | Typical thresholds: 10% flow decrease, 10% permeate-quality decrease, 15% pressure-drop increase; high-fouling: 20%, 20%, 30%. Effective cleaning returns normalized parameters to startup value. | Composite-polyamide RO/NF cleaning guidance; high-fouling values are conditional, stabilized after a week. | S1, p. 2 |
| Cleaning should be early and foulant-led - **directly sourced fact** | Clean as soon as practical; at 30-50% normalized-performance loss, full recovery may be impossible. | Does not prescribe a universal site threshold. | S1, p. 3 |
| Feed/pretreatment data are essential - **directly sourced fact** | Excess coagulant can foul RO; guidance names turbidity, SDI, and particle counters, with particles >2 microns stated as <100 particles/mL. | This is manufacturer guidance, not a chlor-alkali/fertiliser standard. | S1, p. 3 |
| Chemical selection must follow diagnosis - **directly sourced fact** | High-pH cleaning is typically used for oil/biological matter; low pH for mineral scale/metal oxides; wrong chemistry/sequence can make fouling worse. | Requires actual foulant identification and compatibility review. | S1, p. 6 |
| Quantified cleaning recipes exist but are not operating-dose setpoints - **directly sourced fact** | Examples: 2.0% w/w citric acid; pH 10 with 2.0% STPP + 0.8% Na-EDTA; pH 2.5 with 0.5% w/w HCl; pH 11.5 with 0.1% NaOH + 0.03% SDS. | CIP solutions only; apply only within membrane pH/temperature limits and with SDS/compatibility checks. | S1, pp. 7-8 |
| RO dose optimisation has a credible analogous precedent - **directly sourced fact** | One CaPO4-specific antiscalant at OCWD allowed pH 7 without CaPO4 scaling; 43% lower antiscalant cost and calculated 62% lower annual RO chemical consumption with acid savings. | Municipal wastewater case; no chlor-alkali/fertiliser dose is established. | S3, p. 5 |
| Plant/OEM/chemical collaboration is an implementation precedent - **directly sourced fact** | A troubled reuse plant needed a combined effort of plant operator plus membrane and cleaning-chemical suppliers. | Municipal tertiary-effluent reuse; demonstrates collaboration need, not a contract model. | S4, p. 2 |
| Performance evidence can justify an intervention but not prove universal causality - **directly sourced fact** | Before replacement, one train lost 30% normalized flow and gained 128% normalized dP; the source linked the trends to fouling. After changes, it reports 5 cleanings and 7-15-week first-stage cleaning intervals. | Multi-intervention case (membrane changes, cleaning, biocide, recovery/flux changes); effects cannot be isolated from the paper. | S4, pp. 3, 6-8 |
| Condition-based forecast is technically plausible - **directly sourced fact** | A 2021 NF study derived a 28%/year flux-decline fouling index from pilot data, modeled two CIP scenarios, and used remote condition monitoring/data trending to plan intervention. | Subsea NF sulfate removal, not industrial RO; predictions assumed a fixed fouling rate. | S5, pp. 15-17 |
| Replacement forecast needs uncertainty and maintenance planning - **directly sourced fact** | The same study says actual intervals depend on condition-monitoring data; its NF replacement was expected at five years with CIP at 2.5 years. | Design case, not a validated general membrane-life rule. | S5, pp. 16-17 |
| Chemical-industry relevance exists, but not for the two target sectors - **directly sourced fact** | Gujarat aromatics manufacturer: wastewater UF-RO, 824 m3/day UF filtrate, 700 m3/day RO permeate, 85% RO recovery; monthly HCl RO CIP; original membranes after 45 months. | Organic-chemical case; not chlor-alkali or fertiliser and not a digital advisory. | S6, pp. 2-3 |

## 5. Quantitative findings

| Finding | Value | Classification and qualification | Source |
|---|---:|---|---|
| Typical RO trigger deviations | Flow 10%; quality 10%; dP 15% | **Directly sourced fact**; normalized parameters. | S1, p. 2 |
| High-fouling deviations | Flow 20%; quality 20%; dP 30% | **Directly sourced fact**; industrial/municipal wastewater; stabilized baseline. | S1, p. 2 |
| Early high-soluble-organic response | 10-20% normalized-flow decrease over 2-4 weeks | **Directly sourced fact**; decisions should follow post-stabilisation decline rate. | S1, p. 2 |
| Rough acceptable cleaning frequency | Once every 3-12 months | **Directly sourced fact**; site-dependent rule of thumb. | S1, p. 3 |
| Site-specific chemical saving | 43% lower antiscalant cost; 62% calculated annual chemical-cost reduction | **Directly sourced fact**; one municipal CaPO4 test and acid-savings calculation. | S3, p. 5 |
| Organic-chemical UF-RO operation | 824 m3/day UF; 700 m3/day RO; RO 85% recovery; RO HCl CIP monthly | **Directly sourced fact**; one Gujarat site. | S6, pp. 2-3 |
| Forecasting case assumption | 28% annual flux-decline index | **Assumption in source model**, derived from its pilot; not transferable. | S5, p. 15 |
| Forecasting-case outcome | CIP at 2.5 years: estimated 94% five-year feed-pressure rise vs 178% without CIP | **Calculation/model output in source**, under fixed-rate assumption. | S5, p. 15 |

## 6. Conflicting or conditional information

1. **[Directly sourced fact]** TSB107 permits larger high-fouling deviations, but also says to clean as soon as practical; these are allowable decision values, not a reason to delay cleaning. [S1, pp. 2-3]
2. **[Directly sourced fact]** High-soluble-organic wastewater can show an early adsorption-related 10-20% normalized-flow decrease for which aggressive cleaning has only short-lived benefit; use the post-stabilisation decline rate. [S1, p. 2]
3. **[Directly sourced fact]** In the replacement case, several changes occurred together-element replacement/repositioning, high-pH cleaning, biocide, recovery reduction, flux reduction, and configuration change-so the reported improvement cannot establish the isolated causal effect of any one action. [S4, pp. 6-11]
4. **[Directly sourced fact]** The life-forecast paper both recommends condition-based maintenance and presents a five-year intervention design interval. The interval is explicitly dependent on condition-monitoring data, and its prediction assumes a fixed fouling rate. [S5, pp. 15-17]
5. **[Directly sourced fact]** No document-version relationship/supersession was identified in `catalog/document_versions.csv` for S1-S6. S1 itself is TSB107.29 (April 2026); S2 is TSB125.03 (September 2018). The catalogue dates for S4 and S6 are PDF creation dates and are not independently verified publication dates.

## 7. Knowledge gaps

- **Not found in the repository:** a chlor-alkali case study or a fertiliser case study for RO/NF chemical-dose optimisation, CIP recommendation, membrane replacement forecasting, or digital advisory deployment.
- **Not found in the repository:** a Hydranautics digital analytics/advisory product specification, algorithm, software-validation record, cybersecurity/data-governance specification, or commercial reference.
- **Not found in the repository:** chemical dosing ranges/setpoints for a specific chlor-alkali or fertiliser plant, feed-water chemistry, scaling calculations, chemical compatibility matrix, RO/P&ID, historian tags, lab methods, CIP history, element autopsies, or replacement records.
- **Not found in the repository:** an agreed savings KPI, a causal-inference protocol, customer validation form, baseline utility/chemical prices, or evidence that customer savings resulted from an advisory intervention.

## 8. Recommended conclusion and implementation-credibility plan

**[Recommendation]** Proceed only as a gated pilot with the following evidence package.

| Gate | Required proof / KPI | Causality approach |
|---|---|---|
| 1. Partner and authority | Named customer sponsor, O&M owner, chemical supplier, Hydranautics/OEM reviewer, data owner/integrator, and customer finance validator; written change-control and safety authority. | No intervention without owner approval. |
| 2. Data readiness | Time-aligned raw historian data, lab analyses, chemical batch/dose/flow logs, CIP records, membrane inventory/age/location, operating mode, alarms, maintenance events, and quality checks; retain unmodified source data. | Data-completeness and calibration KPI before modelling. |
| 3. Diagnostic validity | Normalized flow, permeate quality, dP, recovery, temperature, feed TDS and pretreatment indicators; diagnosis reviewed against foulant evidence. | Compare advisory diagnosis with O&M and, where feasible, autopsy/cleaning outcome. |
| 4. Prescriptive pilot | Pre-registered intervention limits: dose/rate change or CIP plan, chemical/membrane compatibility, stop conditions, and predicted mechanism. | Prefer parallel matched trains; otherwise use a pre-specified stepped-wedge or interrupted-time-series design with operating-condition adjustment. |
| 5. Primary success KPI | Site-specific, e.g. verified chemical cost per m3 of compliant permeate, subject to no deterioration in product quality, normalized permeability/dP trend, or unplanned CIP rate. | Measure treatment and comparator over the same feed/production regime; lock energy, chemical-price, and allocation method before trial. |
| 6. Savings validation | Reconciled chemical invoices/tank inventory, flow totals, energy data, CIP labour/waste cost, and avoided/re-timed membrane expenditure. | Finance sign-off must state the baseline, counterfactual, adjustments, uncertainty, and whether savings are attributable to the intervention. |
| 7. Replacement forecast | Forecast interval/risk band and decision trigger-not a single deterministic replacement date-updated from condition trends and observed CIP recovery. | Back-test forecasts on held-out historical periods; report error and missed/false intervention rates. |

**[Recommendation]** The initial commercial claim should be limited to: "a pilot-ready decision-support system that uses manufacturer cleaning constraints and plant data to generate reviewable recommendations." Do not claim autonomous optimisation, guaranteed savings, or proven chlor-alkali/fertiliser performance until Gates 1-6 produce signed customer evidence.

## 9. Confidence assessment

**High** for the generic RO diagnostic/CIP evidence: S1 is the current Hydranautics Technical Service Bulletin and gives explicit normalized metrics, foulant categories, and chemical-selection constraints.

**Moderate** for the feasibility of data-driven intervention forecasting: S5 is a primary technical paper with pilot-derived inputs and explicit forecast assumptions, but it is subsea NF rather than chemical-industry RO.

**Moderate** for the general case that chemical-pre-treatment optimisation can reduce chemical cost: S3 contains a quantified real-site calculation, but its feed chemistry is municipal wastewater and its reported saving is not a generalisable dose or guarantee.

**Low / not determinable** for chlor-alkali and fertiliser deployment credibility, project savings, and customer validation: the repository has no direct target-sector case, plant data, trial protocol, or signed customer evidence.

## 10. Full source citations

- **S1.** Hydranautics, *Foulants and Cleaning Procedures for Composite Polyamide RO/NF Membrane Elements*, Technical Service Bulletin **TSB107.29**, April 2026, **DOC-184B4B7D09F3BFCB**, original `sources/raw/Technical_Service_Bulletin/TSB107.pdf`, pp. 2-3 and 6-8.
- **S2.** Hydranautics, *Reverse Direction Cleaning of RO Membrane Elements*, Technical Service Bulletin **TSB125.03**, September 2018, **DOC-202085AA53922159**, original `sources/raw/Technical_Service_Bulletin/TSB125.pdf`, pp. 1-3. (Located and reviewed for scope; no reverse-CIP-specific conclusion is required above.)
- **S3.** Rich Franks, Craig R. Bartels, Keith Andes (Hydranautics), Mehul Patel (Orange County Water District), and Tian Xian Yong (Keppel Seghers), *Implementing Energy Saving RO Technology in Large Scale Wastewater Treatment Plants*, IDA World Congress, 21-26 October 2007, **DOC-79AAB6360C0EE928**, original `sources/raw/Technical_Papers/Implementing-Energy-Saving-RO-Technology-in-Large-Scale-Wastewater-Treatment-Plants.pdf`, pp. 5 and 17.
- **S4.** Craig Bartels, Roman Boda (Hydranautics), and Ahmed Abrar (SAFI), *Wastewater Reuse RO Plant: Road from Troubled to Stable Operation*, IDA World Congress reference IDAWC/TIAN13-093, **DOC-78153AD65D4CAD5A**, original `sources/raw/Technical_Papers/Wastewater-Reuse-RO-Plant-Road-from-Troubled-to-Stable-Operation.pdf`, pp. 2-3, 6-8, 11-12. Publication date not printed in inspected pages; catalogue records 2013-09-09 as PDF creation date, not independently verified as publication date.
- **S5.** Ojonimi Samuel Haruna and Torbjorn Hegdal (NOV); Xiaofei Huang (Hydranautics), *Subsea Sulfate Removal and Low Salinity Plant Membrane Life Prediction for IOR and EOR*, OTC-31035-MS, Offshore Technology Conference, 16-19 August 2021, **DOC-AD89E2661391CDE1**, original `sources/raw/Technical_Papers/Subsea-Sulfate-Removal-and-Low-Salinity-Plant-Membrane-Life-Prediction.pdf`, pp. 15-17.
- **S6.** Hydranautics, *Reducing Costs of an Organic Chemical Manufacturer: Applying Hydranautics Integrated Membrane Solution to Recover Good Quality Boiler Feed Water*, Case Study **CS-IND-001**, **DOC-4AD2E41C2E2E1C04**, original `sources/raw/Case_Studies/CS-IND-001.pdf`, pp. 1-3. Date/version not printed in inspected pages; catalogue records 2018-04-12 as PDF creation date, not independently verified as publication date.

