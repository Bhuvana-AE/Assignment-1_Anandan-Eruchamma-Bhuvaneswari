# FairScope - Jurisdiction-Aware Fair Lending Compliance Tool

**Course:** MH6822 Regulatory Technology  
**Student:** Anandan Eruchamma Bhuvaneswari
**Matriculation ID:** G2506438A
**Email ID:** anandane001@e.ntu.edu.sg
**Project option:** Option B - Architecture Design with prototype notebook  
**Entity:** HSBC Holdings plc, focusing on HSBC Bank USA, N.A. and HSBC UK Bank plc  
**Domain:** Fair Lending / Algorithmic Fairness in Credit Scoring

## Project summary

FairScope is a proposed RegTech tool that monitors credit-decision fairness across two jurisdictions: the United States and the United Kingdom. The project uses HSBC as the reference client because HSBC has meaningful retail banking and lending operations in both markets.

The central idea is that fair lending is not defined or monitored in the same way in the US and UK. In the US, the tool focuses on Regulation B, adverse action notice support, HMDA-related reporting support where applicable, and BISG-based aggregate monitoring where direct race or ethnicity data is unavailable. In the UK, the tool focuses on Equality Act protected characteristics, FCA Consumer Duty outcome monitoring, and lawfully collected self-declared equality data.

FairScope is not designed to make lending decisions. It is a monitoring and governance layer that sits after the bank's credit decisioning engine and before regulatory or internal governance reporting.

## Folder contents

| File | Purpose |
|---|---|
| `Task 1_Entity and Research.docx` | Selection and research section: explains why HSBC and fair lending / algorithmic fairness were selected. |
| `Task 2_Company details.docx` | Values audit: describes EquiLens Analytics, stakeholder tensions, risk-vs-documentation choices, and who bears the cost if the tool fails. |
| `Task 3_Detailed report_Architecture.docx` | Main Task 3 architecture report for FairScope. This is the detailed design document. |
| `Task 3- One Page summary.docx` | Short one-page plain-language summary of the FairScope design. |
| `Task3_Presentation .pdf` | Senior management presentation deck exported as PDF. |
| `Voice recording Presentation ` | Senior management presentation voice recording. |
| `FairScope_Compliance_Tool.ipynb` | Prototype notebook showing synthetic data generation, jurisdiction routing, BISG estimation, ML scoring, SHAP explainability, disparity analysis, and report generation. |

## Main design features

- Jurisdiction router that sends applications to the US or UK pipeline.
- Separate US and UK fairness-monitoring pipelines.
- US BISG-based aggregate monitoring for non-mortgage contexts where direct race or ethnicity data is unavailable.
- UK self-declared protected-characteristic monitoring where lawfully collected.
- Versioned jurisdiction configuration files for auditability.
- SHAP-based proxy-variable monitoring to detect hidden proxy risk.
- Human review gates for inconclusive BISG results, disparity alerts, SHAP proxy alerts, and regulatory outputs.
- Clear scope boundaries: the tool does not make lending decisions, provide legal advice, or auto-submit regulatory filings.

## How to use this repository

1. Start with `Task 1_Entity and Research.docx` to understand the entity and domain choice.
2. Read `Task 2_Company details.docx` to understand the values audit and design philosophy.
3. Read `Task 3_Detailed report_Architecture.docx` for the main tool design.
4. Use `Task 3- One Page summary.docx` as the executive summary.
5. Use `Task3_Presentation .pdf` and `Voice recording Presentation ` for the senior management pitch.
6. Run `FairScope_Compliance_Tool.ipynb` to see the prototype logic.

## Important note

All datasets used in the prototype are synthetic. No real HSBC customer, applicant, demographic, or credit data is used. The prototype is intended to demonstrate jurisdiction-aware compliance logic, not to prove real-world discrimination at HSBC.
