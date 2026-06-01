# SOX Section 404 ITGC Pre-Assessment NorthernPower Energy Corp.


## Plain-Language Summary

This project simulates an internal technology audit for a fictional Canadian energy company listed on both the Toronto Stock Exchange and the New York Stock Exchange. Because the company was listed in the United States, it was legally required each year to have its internal financial controls independently verified by an external accounting firm. This internal audit was conducted before that external review to find and fix problems before the accounting firm arrived.

The audit found a serious control failure in the financial reporting systems. A change had been made to the software that generates the company's cash flow statement in 2025, but that change was never documented, approved, or reviewed through the standard change control process. Because this went undocumented, the company could not prove to its external auditors that the change was authorized and appropriate, which is the definition of a material weakness in financial controls. This finding was serious enough to require immediate notification to the company's Audit Committee and its external accounting firm, because if it remained unresolved, the auditors would be required to issue an adverse opinion on the company's financial controls, which would need to be disclosed publicly in the company's annual report.

This report documents this critical finding alongside two significant deficiencies and fourteen additional control gaps, classifies each finding according to the standard used by external auditors, and provides a prioritized remediation plan to resolve all issues before the external audit begins in September 2026.

**Framework:** US Sarbanes-Oxley Act (SOX) Section 302 and 404 | PCAOB AS 2201 | NI 52-109 (Canadian Equivalent)
**Industry:** Energy and Utilities Canadian Integrated Energy Company (Dual-Listed TSX and NYSE)
**Entity (Fictional):** NorthernPower Energy Corp. Natural gas distribution, renewable generation, and energy trading across 6 Canadian provinces
**Assessment Type:** Internal SOX ITGC Pre-Assessment (Pre-KPMG Fieldwork Gap Identification)
**Auditor:** Edem Messiga, ISO 27001 Certified Lead Auditor | Internal Audit Division
**Assessment Period:** May 1 to 23, 2026 (15 business days)
**External Auditor:** KPMG LLP | ITGC fieldwork scheduled September 2026

---

## Why Energy and Utilities?

Energy companies are among the most demanding SOX environments in Canada. They operate complex ERP systems (SAP S/4HANA for financial reporting, Salesforce for customer billing, Workday for HR and payroll), manage large volumes of capital project payments to construction and maintenance vendors, and face revenue recognition complexity from long-term power purchase agreements, multi-period contracts, and IFRS 15 compliance. Dual-listing on TSX and NYSE adds both US SOX and Canadian NI 52-109 obligations simultaneously.

This project fills the only remaining industry gap in the portfolio energy and utilities while introducing the SOX framework, which is required knowledge for any GRC or internal audit practitioner working with publicly traded companies.

---

## Engagement Context

NorthernPower Energy Corp. is a dual-listed integrated energy company subject to US SOX Section 404(b) (external auditor attestation on ICFR) and Canadian NI 52-109. KPMG LLP is the appointed external auditor with ITGC fieldwork scheduled for September 2026.

The Internal Audit Division commissioned this pre-assessment to identify and remediate ITGC gaps before KPMG begins testing. The prior year's audit produced one Significant Deficiency (SAP HR access provisioning), which was remediated in March 2026. This year-end assessment evaluates whether the remediation held and whether new gaps have emerged.

**The assessment found 1 Material Weakness, 2 Significant Deficiencies, and 14 Control Deficiencies.**

---

## Key Findings

| Ref | Domain | Finding | Classification |
|---|---|---|---|
| MW-001 | Financial Reporting Systems | SAP cash flow statement report parameter changed in Q3 2025 without a documented change control record | Affects Q3 2025, Q4 2025, Q1 2026 financial statements | **Material Weakness** |
| SD-001 | Logical Access | P. Chaudhary (terminated March 19) retained SAP BW financial reporting access for 8 days | SAP BW not in Workday offboarding automation | Significant Deficiency |
| SD-002 | Logical Access | 5 undocumented SOD conflicts including Create Vendor | Approve Payment combination in AP for 2 users | Significant Deficiency |
| CD-001 | Logical Access | 2 Finance Analyst SAP accounts activated without documented IT Security sign-off | Control Deficiency |
| CD-002 | Logical Access | 4 of 20 Firefighter ID log reviews not completed | No backup reviewer designated | Control Deficiency |
| CD-003 | CD-004 | Change Management | Emergency change documentation gaps | IT sign-off and CFO authorization outside ServiceNow | Control Deficiency |
| CD-005 | Change Management | Revenue recognition regression test plan not updated since 2023 | IFRS 15 configuration changes not covered | Control Deficiency |
| CD-010 | Financial Reporting | Intercompany Elimination completed before Intercompany Reconciliation in 2 consecutive months | Control Deficiency |

**Total deficiencies:** 1 Material Weakness | 2 Significant Deficiencies | 14 Control Deficiencies | 14 Management Actions

---

## Deliverables

| File | Description |
|---|---|
| `NorthernPower_SOX_ITGC_Workbook.xlsx` | 4-tab workbook: Engagement Overview (ITGC domains, deficiency classification reference with PCAOB AS 2201 definitions, findings summary with formulas), ITGC Assessment (22 controls across 5 domains with audit procedure, population and sample, evidence obtained, control status, deficiency classification, root cause, financial reporting risk, recommended action, and KPMG blocker column), Deficiency Tracker (16 deficiencies with aggregation risk analysis, management response, and evidence of remediation), Management Action Plan (14 actions with KPMG blocker designation and Audit Committee escalation column) |
| `NorthernPower_SOX_ITGC_Report.docx` | Formal SOX pre-assessment report: Material Weakness escalation notice with Audit Committee communication requirement, PCAOB AS 2201 deficiency classification table, detailed Material Weakness finding with financial statement impact analysis, 2 Significant Deficiency findings, domain-by-domain Control Deficiency summaries, aggregation risk analysis table, SOX and NI 52-109 crosswalk, phased remediation timeline to KPMG readiness, and report approval page |

---

## What Makes a SOX ITGC Assessment Different

**Deficiency classification has real consequences.** In a SOX engagement, the classification of a finding as a Material Weakness, Significant Deficiency, or Control Deficiency is not academic. A Material Weakness requires external auditor disclosure in the annual report, puts CEO and CFO Section 302 certifications at risk, and can trigger an adverse opinion on internal controls over financial reporting (ICFR). This project applies that classification framework correctly and consistently.

**Aggregation judgment is a distinctive SOX skill.** Multiple Control Deficiencies can collectively constitute a more serious deficiency. This project identifies four aggregation risk areas and explains the KPMG judgment that applies. The revenue recognition aggregation risk (MW-001, CD-005, CD-008) is the most significant because all three gaps relate to the same financial statement line and process.

**The financial reporting system domain is unique to SOX.** Unlike ISO 27001, NIST CSF, or HIPAA, SOX explicitly focuses controls on systems that produce financial statements. The MW-001 finding (SAP report parameter change without change control documentation) is a textbook SOX ITGC finding that would not appear in a general security assessment but is central to a SOX engagement.

**The pre-assessment function is itself a SOX maturity indicator.** An organization that conducts a formal internal pre-assessment before KPMG fieldwork, identifies its own Material Weakness, and self-reports to the Audit Committee demonstrates a mature internal audit function. This is more sophisticated than discovering the deficiency during external audit fieldwork.

---

## PCAOB AS 2201 Deficiency Classification

| Classification | Definition | NorthernPower Consequence |
|---|---|---|
| Material Weakness | Reasonable possibility that a material misstatement will not be prevented or detected on a timely basis | Adverse ICFR opinion from KPMG if not remediated. Mandatory 10-K disclosure. CEO and CFO certifications at risk. |
| Significant Deficiency | Less severe than a Material Weakness but important enough to merit Audit Committee attention | Communicated to Audit Committee and KPMG. Audit scope increases. No adverse opinion if remediated. |
| Control Deficiency | Design or operation of a control does not prevent or detect misstatements on a timely basis | Management letter communication. Monitored for aggregation risk. |
| Aggregation Risk | Multiple Control Deficiencies affecting the same account or process may collectively constitute a more severe deficiency | KPMG applies aggregation judgment. Internal Audit must proactively identify and communicate aggregation risks. |

---

## SOX and NI 52-109 Crosswalk

| Requirement | US SOX | Canadian NI 52-109 |
|---|---|---|
| CEO and CFO Certifications | Section 302: quarterly and annual | Annual certifications only (Form 52-109F1 and F2) |
| External Auditor Attestation | Section 404(b): required for large accelerated filers | Not required for most issuers | NorthernPower does this under NYSE requirements |
| Material Weakness Disclosure | Required in annual report (10-K) | Required in annual report |
| Assessment Basis | PCAOB AS 2201 | COSO 2013 | COSO 2013 or equivalent recognized framework |
| Quarterly ICFR Certification | Required (SOX 302) | Not required under NI 52-109 |
| IT Controls Framework | ITGC requirements driven by PCAOB AS 2201 | No separate IT control framework | COSO-based assessment drives ITGC scope |

---

## Remediation Timeline

| Phase | By | Key Actions |
|---|---|---|
| Phase 1: Immediate | June 7, 2026 | Reconstruct MW-001 change control record. CFO retroactive approval. Audit Committee notification (June 3). KPMG communication (June 7). |
| Phase 2: Access | June 15, 2026 | Remove AP conflicting roles (SD-002). Remove J. Whitfield SAP access. ServiceNow provisioning gate. Firefighter backup reviewer. |
| Phase 3: Systems | June 30, 2026 | SAP BW offboarding automation (SD-001). SOD compensating controls. Financial report parameter reclassification. |
| Phase 4: Process | July 31, 2026 | Revenue regression test plan. MuleSoft risk assessment addendum. Workday role-change trigger. SharePoint period-end dependency. |
| KPMG Readiness | August 2026 | Internal Audit operating effectiveness test. Evidence package assembled. KPMG briefing on all remediated controls. |

---

## Skills Demonstrated

- SOX Section 404 ITGC methodology (Logical Access, Change Management, Computer Operations, Financial Reporting Systems, IT Risk)
- PCAOB AS 2201 deficiency classification (Material Weakness, Significant Deficiency, Control Deficiency)
- Aggregation risk analysis for Control Deficiencies
- SAP S/4HANA ITGC controls (GRC Access Control, Transport Management System, SAP BW, RAR)
- Segregation of duties assessment and conflict resolution in an ERP environment
- SOD compensating control design and CFO approval process
- Financial reporting system interface controls (Salesforce-to-SAP, Workday-to-SAP)
- Period-end close checklist controls and sequencing dependencies
- Pre-KPMG internal audit readiness assessment methodology
- SOX and NI 52-109 dual-framework compliance (Canadian dual-listed company context)
- Material Weakness escalation procedures (Audit Committee, CFO, external auditor communication)
- Remediation timeline planning for pre-external auditor fieldwork

---

## Lessons Learned

**A Material Weakness is a documentation problem as often as a control design problem.** MW-001 at NorthernPower is an example of a financially correct action (adjusting the cash flow presentation for intercompany financing transactions) that became a Material Weakness because it was not documented through the change control process. The substance of the change may be correct; the process failure is the finding. SOX is fundamentally about documentation and evidence, not just about whether controls work.

**The SAP change log is always available but it is not a substitute for ServiceNow.** When the Controller treated the report parameter change as a configuration adjustment rather than a formal change, the SAP change log captured the technical event. But the SAP change log alone does not satisfy ITGC evidence requirements. Business justification, UAT sign-off, IT Security approval, and release manager authorization are all required. Change log evidence without those approvals is an incomplete evidence package.

**Aggregation is where junior auditors struggle and senior auditors add value.** Finding 14 individual Control Deficiencies is straightforward. Recognizing that 3 of those 14 all relate to revenue recognition and collectively create a risk environment that KPMG will scrutinize as a unit requires a more sophisticated analytical lens. That is what distinguishes a SOX practitioner from someone who has only learned the framework checklist.

**The pre-assessment function is the highest-value Internal Audit activity in a SOX environment.** Self-identifying a Material Weakness before KPMG arrives and self-reporting it to the Audit Committee is the gold standard of SOX Internal Audit performance. It demonstrates independence, competence, and a commitment to the integrity of the financial reporting control environment. It is also better for the organization than learning about a Material Weakness from the external auditor.

---

## Related Projects

| Repository | Framework |
|---|---|
| [GRC-PCI-DSS-v4-MapleFinancial](../GRC-PCI-DSS-v4-MapleFinancial) | PCI-DSS v4.0 | Canadian Regional Bank |
| [GRC-SOC2-TypeI-CareSync](../GRC-SOC2-TypeI-CareSync) | SOC 2 Type I | Healthcare SaaS (EHR platform) |
| [GRC-ISO27001-GovTech-Ontario](../GRC-ISO27001-GovTech-Ontario) | ISO 27001 | Provincial Government Digital Services |
| [GRC-NIST-CSF-NovaSaaS](../GRC-NIST-CSF-NovaSaaS) | NIST CSF 2.0 | Canadian B2B SaaS company |
| [GRC-PIA-PIPEDA-CanRetail](../GRC-PIA-PIPEDA-CanRetail) | PIA | Canadian Retail Loyalty Program |
| [GRC-HIPAA-CrossBorder](../GRC-HIPAA-CrossBorder) | HIPAA Security Rule | Canadian Health Tech BA |

---

## About the Author

**Edem Messiga**
ISO 27001 Certified Lead Auditor | Cybersecurity GRC | Bilingual EN/FR
[linkedin.com/in/edem-messiga](https://linkedin.com/in/edem-messiga)

> All entities, individuals, financial figures, regulatory references, and systems in this project are fictional and created for professional portfolio and development purposes only.
