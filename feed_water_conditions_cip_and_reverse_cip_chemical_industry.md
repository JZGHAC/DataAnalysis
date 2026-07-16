# Repository research record: feed-water conditions requiring CIP and when reverse CIP is needed

## 1. Executive answer

**Directly sourced fact.** For composite-polyamide RO/NF elements, Hydranautics says to clean when there is evidence of fouling, before a long-term shutdown, or on a scheduled maintenance basis. Its current service bulletin uses normalized-performance deviations as the operational trigger: typical feeds: 10% decline in normalized permeate flow or quality, or 15% increase in normalized pressure drop (dP); high-fouling industrial/municipal wastewater: 20%, 20%, and 30%, respectively. Clean as soon as practical rather than waiting for heavy fouling. [S1, p. 2; S1, p. 3]

**Directly sourced fact.** Reverse CIP (reverse-direction chemical cleaning from reject/brine end to feed end) is a conditional cleaning method, not the default. It is beneficial where heavy biological, colloidal, or particulate foulant is concentrated at the feed end of lead/front elements; forward cleaning can then struggle to remove the deposit because it pushes loosened foulant through the vessel. [S2, p. 1]

**Directly sourced fact.** Do **not** start reverse CIP when tail-end scale is present: perform forward cleaning first to remove scaling. The source warns that sharp scale crystals can cause greater membrane damage during reverse cleaning. Reverse CIP must use controlled flow because the lead element lacks a thrust-ring support against telescoping. [S2, pp. 1-2]

**Engineering inference.** For a chemical-industry RO treating plant wastewater, use the normalized thresholds and foulant location - not the label "chemical industry" alone - to decide CIP. Escalate to reverse CIP only after evidence indicates a feed-end/lead-element solids, colloidal, or biofouling plug, tail-end scaling has been addressed, the installed piping permits two-way CIP, and the element manufacturer permits the procedure.

## 2. Research scope and method

**Question interpreted.** Identify (a) feed-water/foulant conditions that create a need for RO CIP and the performance criteria that indicate timing, and (b) the conditions under which reverse-direction CIP is appropriate, with application to chemical-industry plant wastewater.

**Included.** RO/NF spiral-wound composite-polyamide cleaning guidance; chemical-industry wastewater case evidence; the dedicated reverse-direction cleaning service bulletin.

**Excluded.** Public-web material; unverified site-specific cleaning prescriptions; non-RO UF maintenance/recovery cleaning except where reported as case context.

**Terms and synonyms searched.** CIP / clean-in-place; RO / reverse osmosis; NF / nanofiltration; reverse CIP / reverse cleaning / reverse-direction cleaning; forward cleaning; feed end / lead element / front element; brine/reject end / tail end; dP / differential pressure / pressure drop; fouling / scaling / biofouling / colloidal / particulate; chemical industry / plant wastewater.

**Repository process completed.** Searched `catalog/document_catalog.csv`; searched `knowledge/indexes/cleaning_methods.json` and `knowledge/indexes/troubleshooting_symptoms.json`; checked `knowledge/taxonomy/acronyms.csv`; read normalized records for S1-S4; traced the quoted findings to the listed original PDF pages. The catalogue and library contain no flagged superseding versions of TSB107 or TSB125.

## 3. Process explanation

**Directly sourced fact.** Normal CIP sends cleaning solution from pressure-vessel feed end to reject end, the same direction as service flow. Reverse CIP sends it from reject end to feed end. [S2, p. 1]

**Directly sourced fact.** Feedwater quality and system recovery influence the nature and rate of fouling. The service bulletin lists mineral scale, metal oxides, polymerized silica, inorganic or mixed colloids, natural and man-made organics, and biological material as common RO foulants. [S1, p. 2]

**Directly sourced fact.** Wastewaters high in soluble organics can show an initial 10-20% normalized-flow decrease and salt-passage decrease over 2-4 weeks due to adsorption. Hydranautics recommends basing a cleaning decision on the decline rate after this initial stabilization, rather than automatically treating that initial change as a CIP trigger. [S1, p. 2]

## 4. Evidence table

| Conclusion and classification | Exact supporting evidence | Applicability / condition | Source anchor |
|---|---|---|---|
| CIP is required by performance condition, shutdown planning, or schedule - **directly sourced fact** | Clean when there is evidence of fouling, before long-term shutdown, or scheduled maintenance; clean promptly to retain a clean/nearly-clean condition. | Composite-polyamide RO/NF elements. | S1, p. 2 |
| Typical CIP intervention values - **directly sourced fact** | Normalized flow decrease 10%; normalized permeate-quality decrease 10%; normalized dP increase 15%. | "Typical" feed conditions; normalized data assumed. | S1, p. 2 |
| High-fouling wastewater values - **directly sourced fact** | 20% normalized-flow decrease, 20% normalized-quality decrease, 30% normalized-dP increase. | Industrial/municipal wastewater with more extreme fouling; baseline may be stabilized performance after one week. | S1, p. 2 |
| Relevant feedwater conditions - **directly sourced fact** | Common foulants: carbonate/sulfate scale; metal oxides; silica; colloids; organics; biological matter. | Potential mechanisms, not independently sufficient CIP criteria without performance/foulant assessment. | S1, p. 2 |
| Avoid delaying cleaning - **directly sourced fact** | At 30-50% normalized-performance loss, baseline recovery may be impossible; heavy fouling blocks chemical penetration and foulant removal. | Any RO condition becoming heavily fouled. | S1, p. 3 |
| Reverse CIP decision - **directly sourced fact** | Reverse flow can be beneficial for heavy biological, colloidal, or particulate foulant concentrated at the feed end of lead/front elements. | Do not generalize to tail-end scale or uniformly distributed foulant. | S2, p. 1 |
| Reverse CIP restriction - **directly sourced fact** | Forward cleaning is always recommended when scaling is present; remove tail-end scale before reverse cleaning. | Scaling case; scale crystals may damage membrane in reverse flow. | S2, p. 1 |
| Reverse-CIP flow safeguards - **directly sourced fact** | Start low and increase as dP falls. For standard 8-in elements: reverse 24-32 gpm (91-121 L/min); heavily fouled reverse 12-16 gpm (45-61 L/min); inlet pressure <=60 psi (4 bar). | Per pressure tube; lead-element telescoping risk. | S2, p. 2 |
| Chemical-industry plant-wastewater example - **directly sourced fact** | Organic chemical manufacturer, Gujarat; plant wastewater; UF+RO system; RO CIP with HCl once/month; 85% RO recovery. | One Hydranautics case study; demonstrates actual operating practice, not a general trigger. | S3, pp. 1-3 |
| Practical decision rule - **engineering inference** | Use performance trigger plus foulant localization; choose reverse CIP only for feed-end heavy bio/colloidal/particulate loading, after forward scale removal and equipment/element compatibility checks. | Chemical-industry wastewater RO. | Inference from S1-S2 |

## 5. Quantitative findings

All figures below retain the original units; metric equivalents are printed in the source.

| Parameter | Typical | High-fouling industrial/municipal wastewater | Source |
|---|---:|---:|---|
| Normalized permeate flow decrease | 10% | 20% | S1, p. 2 |
| Normalized permeate quality decrease | 10% | 20% | S1, p. 2 |
| Normalized pressure-drop increase | 15% | 30% | S1, p. 2 |
| Initial high-soluble-organic change | 10-20% over 2-4 weeks | Not applicable | S1, p. 2 |
| Typical site cleaning frequency | every 3-12 months | Not a criterion | S1, p. 3 |
| Reverse-CIP flow, standard 8-in non-LD | 24-32 gpm (91-121 L/min) | 12-16 gpm (45-61 L/min) when heavily fouled / dP has more than doubled | S2, p. 2 |
| Maximum inlet pressure during reverse cleaning | 60 psi (4 bar) | 60 psi (4 bar) | S2, p. 2 |

## 6. Conditional/conflicting information

1. **Directly sourced fact:** Reverse cleaning is not accepted universally: the reverse-cleaning technical paper says some manufacturers prohibit it because of potential element damage, whereas Hydranautics TSB125 provides a conditional procedure. [S4, pp. 1-2; S2, pp. 1-3]
2. **Directly sourced fact:** TSB125 requires cleaning in both directions; a reverse-only system should not be designed. [S2, p. 3]
3. **Directly sourced fact:** The high-fouling values are permitted deviations, not an automatic mandate to wait until those values. The same bulletin says clean as soon as practical and emphasizes early cleaning. [S1, pp. 2-3]
4. **Directly sourced fact:** High-soluble-organic wastewater can exhibit early adsorption-related performance change for which aggressive cleaning may have only short-lived benefit. [S1, p. 2]

## 7. Knowledge gaps

- **Not found in the repository:** feed analysis, RO performance trend, element model, vessel arrangement, stage-by-stage dP, CIP piping/P&ID, and foulant autopsy for the user's chemical-industry system.
- **Not found in the repository:** a chemical-industry case study that specifically documents reverse CIP.
- **Not found in the repository:** an independent standard or regulatory cleaning threshold for this specific application.
- **Not found in the repository:** a catalogued superseding version of TSB125.03. TSB107 is explicitly version `.29`, April 2026.

## 8. Recommended conclusion

**Recommendation.** Trend normalized permeate flow, quality, and dP by stage. Initiate normal CIP promptly at the S1 limits (or an approved, site-specific high-fouling baseline). Characterize the foulant and identify whether it is lead/feed-end localized. Consider reverse CIP only if that diagnosis shows heavy feed-end biological/colloidal/particulate fouling; first remove tail-end scale with normal forward cleaning; then follow the manufacturer-approved reverse-CIP connection and low-flow ramp procedure. Do not clean from the permeate side. [S1, pp. 2-3; S2, pp. 1-3]

## 9. Confidence assessment

**High** for the general CIP and reverse-CIP decision conditions: they come from Hydranautics' primary Technical Service Bulletins, including current TSB107.29 and the dedicated reverse-direction TSB125.03. **Moderate** for chemical-industry application: the direct industry evidence is one manufacturer case study, and it reports monthly CIP without specifying diagnostic trigger criteria or reverse CIP. **Low/not determinable** for a particular plant because its water chemistry, trend data, and CIP design were not supplied and were not found in the repository.

## 10. Full source citations

- **S1.** Hydranautics, *Foulants and Cleaning Procedures for Composite Polyamide RO/NF Membrane Elements*, Technical Service Bulletin **TSB107.29**, April 2026, **DOC-184B4B7D09F3BFCB**, original: `sources/raw/Technical_Service_Bulletin/TSB107.pdf`, pp. 1-3 (especially p. 2 thresholds and high-organic condition; p. 3 early-cleaning guidance).
- **S2.** Hydranautics, *Reverse Direction Cleaning of RO Membrane Elements*, Technical Service Bulletin **TSB125.03**, September 2018, **DOC-202085AA53922159**, original: `sources/raw/Technical_Service_Bulletin/TSB125.pdf`, pp. 1-3 (p. 1 conditions and scaling restriction; p. 2 flow limits; p. 3 bidirectional-system requirement).
- **S3.** Hydranautics, *Reducing Costs of an Organic Chemical Manufacturer: Applying Hydranautics Integrated Membrane Solution to Recover Good Quality Boiler Feed Water*, Case Study **CS-IND-001**, **DOC-4AD2E41C2E2E1C04**, original: `sources/raw/Case_Studies/CS-IND-001.pdf`, pp. 1-3. Date/version not printed in the extracted pages; catalogue records 2018-04-12 as PDF creation date and explicitly says it is not independently verified as the publication date.
- **S4.** K. Andes, C. Bartels, and G. Hijos (Nitto Hydranautics / Acciona), *Why Your RO Membrane Cleaning May Not Be Effective: The Benefits of Reverse Cleaning*, **DOC-C11B437CC279DE67**, original: `sources/raw/Technical_Papers/WHY-YOUR-RO-MEMBRANE-CLEANING-MAY-NOT-BE-EFFECTIVE.-THE-BENEFITS-OF-REVERSE-CLEANING.pdf`, pp. 1-2. Date/version not stated in inspected pages; catalogue records 2021-08-18 as PDF creation date and explicitly says it is not independently verified as the publication date.
