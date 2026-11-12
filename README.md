# Cybersecurity Risk Assessment & Information Security Policy

A simulated GRC case study applying the **NIST Cybersecurity Framework (CSF)** to a fictional manufacturing company.

> **Project type:** Masters module coursework project
> **Focus areas:** Governance, risk assessment, risk treatment, security policy, third-party risk 
> **Framework:** NIST Cybersecurity Framework (CSF) — Identify, Protect, Detect, Respond, Recover

## Overview

The fictional organisation manufactures customised products and has recently introduced an automated Manufacturing Control System (MCS). Its environment includes a customer-facing website, office IT infrastructure, sensitive customer and employee records, intellectual property, remote-access devices, and third-party technology support.

The case study identified security weaknesses in the public website, risks to proprietary product designs, and potential compromise of the manufacturing environment. The project translated these findings into a qualitative risk assessment, attack-tree analysis, and an organisation-wide information security policy.

## Objectives

- Identify critical business assets, threats, vulnerabilities, and potential business impacts.
- Prioritise risks using qualitative likelihood and impact assessments.
- Develop attack trees for the three highest-priority threat scenarios.
- Recommend proportionate risk treatments and security controls.
- Create a policy structure aligned with the five NIST CSF functions.

## Key findings

| Priority | Risk scenario | Qualitative assessment | Business impact |
|---|---|---|---|
| 1 | Exploitation of website vulnerabilities, including SQL injection and remote code execution | High likelihood / High impact | Potential unauthorised access, data breach, malware deployment, and wider network compromise |
| 2 | Theft of proprietary widget design specifications | High likelihood / High impact | Loss of intellectual property and competitive advantage |
| 3 | Compromise of the Manufacturing Control System (MCS) | Medium likelihood / High impact | Production disruption, reduced productivity, and potential loss of competitiveness |

These ratings reflect the qualitative conclusions in the original case-study report; they are not numerical scores or independently validated measurements.

## Deliverables

- [`methodology-and-risk-analysis.md`](docs/methodology-and-risk-analysis.md) — assessment approach, scope, assumptions, and risk-prioritisation rationale.
- [`risk-register.csv`](risk-register.csv) — concise portfolio risk register.
- [`attack-trees.md`](docs/attack-trees.md) — attack-tree diagrams for the three priority scenarios.
- [`information-security-policy.md`](docs/information-security-policy.md) — policy recommendations structured around the NIST CSF functions.

## Personal contribution

In the original group assignment, my main contributions were:

- Developing the attack trees for the priority threat scenarios.
- Drafting the information security policy across the five NIST CSF functions.
- Contributing to the qualitative risk analysis and discussion of risk priorities.

This repository is a reorganised portfolio presentation of the group project, not a claim that the original work was completed individually.

## How to explore the project

1. Start with the methodology and risk analysis to understand the organisation, scope, and risk priorities.
2. Review the risk register for a concise view of the main risks and proposed treatments.
3. Open the attack-tree diagrams to see how the threat scenarios were decomposed.
4. Review the information security policy to see how the risks translate into governance and security controls.

The diagrams use Mermaid and can be rendered by GitHub in Markdown files.

## Limitations and assumptions

- The organisation and scenario are fictional and supplied as an academic case study.
- This is a desktop assessment based on the information provided in the case study; no live penetration testing, scanning, or validation of a real environment was performed.
- The original report identifies the NIST CSF and its five functions but does not specify a CSF version. This repository therefore avoids claiming alignment to a particular version or claiming formal certification/compliance.
- Risk ratings are qualitative and based on the original report's stated likelihood and impact conclusions. A production assessment would require agreed scoring criteria, asset owners, evidence, and management risk acceptance.

## Suggested future enhancements

- Add a defined likelihood/impact scoring scale and calculate inherent and residual risk.
- Map each recommended control to relevant NIST CSF outcomes and, where appropriate, CIS Controls or ISO/IEC 27001 Annex A.
- Add control owners, target dates, evidence requirements, and residual-risk acceptance.
- Develop a simple risk-treatment tracker and incident-response tabletop scenario.

## Disclaimer

For educational and portfolio demonstration purposes only. No real organisation, system, or website was tested.
