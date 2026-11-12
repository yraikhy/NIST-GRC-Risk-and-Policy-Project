# Methodology and Risk Analysis

## 1. Business context

The case study concerns a fictional manufacturing company seeking to increase production capacity through a new automated Manufacturing Control System (MCS). The organisation also operates a customer-facing website and maintains sensitive business information across office systems and servers.

Key assets described in the case include:

- Manufacturing Control System and supporting production infrastructure.
- Customer ordering website and customer records.
- Proprietary product designs and specifications.
- Employee and personnel records.
- Financial records.
- Production schedules and inventory information.
- Remote-access devices used by employees and managers.
- Third-party services and vendor remote access.

## 2. Why a risk assessment was required

The case study describes several drivers for a structured assessment:

- The public website contains input-handling weaknesses that may enable SQL injection and remote code execution.
- Proprietary designs are commercially sensitive and support the organisation's competitive position.
- Remote devices connect to office systems and may increase the attack surface.
- The MCS introduces operational dependency on a new technology platform and its supplier.
- Customer, employee, and financial information requires appropriate protection.
- Vendor access and support arrangements create third-party security dependencies.

A risk assessment helps management understand which scenarios could cause the greatest harm and decide where limited resources should be applied first.

## 3. Framework and assessment approach

The group selected the **NIST Cybersecurity Framework (CSF)** as the organising framework. The report favoured a prioritised, business-oriented approach and used the five CSF functions:

1. **Identify** — understand assets, business context, governance, and risk.
2. **Protect** — implement safeguards to reduce the likelihood or impact of incidents.
3. **Detect** — identify anomalous activity and potential security events.
4. **Respond** — coordinate actions to contain and manage incidents.
5. **Recover** — restore services and improve resilience after incidents.

The risk analysis itself was qualitative: scenarios were considered in terms of likelihood and business impact rather than assigned numerical scores. The original report does not specify a particular CSF version or a formal numerical scoring methodology.

## 4. Priority risk scenarios

### Risk 1 — Website exploitation and data compromise

The case describes website input fields that produce errors when a single quotation mark is entered, as well as an example SQL injection string and the ability to access server files and execute a remotely loaded script.

**Assessment in the report:** High likelihood and high impact.

**Potential consequences:** Unauthorised access to data, compromise of customer information, malware deployment, and potential further compromise of connected systems.

**Proposed treatment:** Correct the vulnerable application code; implement server-side input validation and parameterised database queries; prevent script execution in upload locations; review file permissions; and segment the network to limit lateral movement.

### Risk 2 — Theft of proprietary product designs

The organisation stores electronic product designs and specifications on internal systems. These designs are commercially sensitive and contribute to its competitive advantage.

**Assessment in the report:** High likelihood and high impact.

**Potential consequences:** Loss of intellectual property, competitive disadvantage, and commercial harm.

**Proposed treatment:** Restrict access to approved corporate devices; prevent unmanaged home devices from accessing sensitive servers; encrypt design files; and periodically review access permissions.

### Risk 3 — Manufacturing Control System compromise

The MCS is a critical operational system supported by a third-party vendor. The case describes vendor remote access and the use of email by shift supervisors on devices associated with production operations.

**Assessment in the report:** Medium likelihood and high impact.

**Potential consequences:** Production disruption, reduced output, operational delays, and loss of competitiveness.

**Proposed treatment:** Separate email and general-purpose activity from MCS controller environments; restrict and monitor vendor remote access; strengthen supplier security requirements and incident notification obligations; and establish clear service expectations.

## 5. Other risk themes

The policy also addresses broader control areas raised by the case:

- Remote access and identity management.
- Least-privilege access and multi-factor authentication.
- Employee awareness and phishing education.
- Encryption and protection of sensitive information.
- Secure configuration, patching, and change management.
- Logging, monitoring, and vulnerability scanning.
- Incident response and recovery planning.
- Vendor assurance and controlled remote maintenance.

## 6. Risk assessment limitations

This is a qualitative academic assessment based on a fictional scenario. It does not include a live technical assessment, verified exploitability, a full asset valuation, a formally calibrated risk matrix, or confirmed residual-risk calculations. A real assessment should validate assumptions with system owners, gather technical evidence, define consistent scoring criteria, and obtain management approval for risk treatment and acceptance.
