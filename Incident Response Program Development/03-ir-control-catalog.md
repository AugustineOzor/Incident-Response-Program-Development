# 03 · IR Control Catalog

**Navigate:** [README](../README.md) · [Assets](01-asset-inventory.md) · [Incidents](02-incident-register.md) · [Controls](03-ir-control-catalog.md) · [Tasks](04-ir-tasks.md)

Incident response controls with effectiveness ratings and rationale. Framework references are paraphrased pointers; verify against the source text before relying on them.

## Summary

| ID | Name | Framework | Reference | Effectiveness | Frequency | Owner |
|---|---|---|---|---|---|---|
| [IR-01](#ir-01) | Incident Response Plan and Playbooks | HIPAA | 45 CFR 164.308(a)(6)(i) | Effective | Annual | Security Operations Manager |
| [IR-02](#ir-02) | 24x7 Security Monitoring and Alerting | NIST CSF | DE.CM-01 | Effective | Continuous | SOC Lead |
| [IR-03](#ir-03) | Incident Triage and Severity Classification | NIST CSF | RS.MA-03 | Partially Effective | Continuous | SOC Lead |
| [IR-04](#ir-04) | Containment and Eradication Procedures | NIST CSF | RS.MI-01 | Effective | Quarterly | IR Lead |
| [IR-05](#ir-05) | HHS and Customer Breach Notification Procedure | HIPAA | 45 CFR 164.410; 164.408 | Partially Effective | Quarterly | Compliance and Privacy Officer |
| [IR-06](#ir-06) | Forensic Evidence and Log Retention | ISO 27001 | A.5.28 | Ineffective | Monthly | Platform Operations Manager |
| [IR-07](#ir-07) | Incident Response Tabletop Exercises | NIST CSF | ID.IM-02 | Not Tested | Annual | Security Operations Manager |
| [IR-08](#ir-08) | Post-Incident Review and Lessons Learned | ISO 27001 | A.5.27 | Partially Effective | Monthly | IR Lead |

## Details

### <a id="ir-01"></a>**IR-01** — Incident Response Plan and Playbooks

**Description:** Maintain a board-approved incident response plan with playbooks for phishing, ransomware, PHI data breach, insider threat and EHR availability outages. Each playbook defines roles, escalation paths, decision points and evidence to capture.

**Decision rationale:** Plan and five playbooks are approved, version-controlled and reviewed in the last 12 months. Walkthrough with the SOC confirmed analysts can locate and follow them.

- **Related incidents:** [INC-2026-003](02-incident-register.md#inc-2026-003)
- **Remediation tasks:** [TSK-005](04-ir-tasks.md#tsk-005)

### <a id="ir-02"></a>**IR-02** — 24x7 Security Monitoring and Alerting

**Description:** Centralize logs from EHR application servers, identity provider, cloud workloads and endpoints in the SIEM. Use tuned detection rules for PHI access anomalies, impossible travel and mass data export, with alerts routed to the on-call analyst.

**Decision rationale:** Sampled alerts from the last quarter were acknowledged within the 15-minute target. Detection rules cover the main PHI systems and are reviewed monthly.

- **Related incidents:** [INC-2026-001](02-incident-register.md#inc-2026-001), [INC-2026-002](02-incident-register.md#inc-2026-002)
- **Remediation tasks:** —

### <a id="ir-03"></a>**IR-03** — Incident Triage and Severity Classification

**Description:** Classify every incident as Critical, High, Medium or Low using a defined matrix covering PHI exposure, patient-safety impact, number of hospitals affected and regulatory notification triggers. Record the rating and rationale in the incident register.

**Decision rationale:** The matrix exists and is used, but 2 of 5 sampled incidents were rated inconsistently and the rationale field was blank in one. Analyst calibration and a mandatory rationale field are needed.

- **Related incidents:** [INC-2026-001](02-incident-register.md#inc-2026-001), [INC-2026-002](02-incident-register.md#inc-2026-002)
- **Remediation tasks:** [TSK-004](04-ir-tasks.md#tsk-004)

### <a id="ir-04"></a>**IR-04** — Containment and Eradication Procedures

**Description:** Provide pre-approved containment actions such as account disablement, host isolation, API key revocation and storage access lockdown, with authority levels. Verify eradication and recovery before service is restored to hospital customers.

**Decision rationale:** Containment steps were executed within target in the last three incidents, and pre-approval removed delays in obtaining sign-off. Recovery validation checklist was completed each time.

- **Related incidents:** [INC-2026-002](02-incident-register.md#inc-2026-002), [INC-2026-003](02-incident-register.md#inc-2026-003)
- **Remediation tasks:** —

### <a id="ir-05"></a>**IR-05** — HHS and Customer Breach Notification Procedure

**Description:** Run the HIPAA four-factor risk assessment for each suspected PHI incident. As a business associate, notify affected covered entities without unreasonable delay and within 60 days of discovery, supporting their notices to individuals, HHS OCR and the media where required. Track the notification clock for every incident.

**Decision rationale:** Templates, legal review path and contact list are in place. The 60-day clock is tracked manually in a spreadsheet, and one customer contact list was out of date at last review. Automated deadline tracking is recommended.

- **Related incidents:** [INC-2026-001](02-incident-register.md#inc-2026-001), [INC-2026-002](02-incident-register.md#inc-2026-002)
- **Remediation tasks:** [TSK-002](04-ir-tasks.md#tsk-002)

### <a id="ir-06"></a>**IR-06** — Forensic Evidence and Log Retention

**Description:** Preserve logs, disk images and chain-of-custody records for incident investigations. Retain EHR application, access and cloud audit logs long enough to support investigation lookback and regulatory inquiries.

**Decision rationale:** Audit logs for legacy EHR modules are retained for only 30 days, which is too short to reconstruct events in a late-discovered breach. Chain-of-custody forms are not used consistently. Retention must be extended before this control can be rated higher.

- **Related incidents:** [INC-2026-002](02-incident-register.md#inc-2026-002)
- **Remediation tasks:** [TSK-001](04-ir-tasks.md#tsk-001)

### <a id="ir-07"></a>**IR-07** — Incident Response Tabletop Exercises

**Description:** Run at least one tabletop exercise per year simulating a PHI breach affecting multiple hospital customers, including legal, privacy, communications and executive participants. Record findings and track improvement actions to closure.

**Decision rationale:** The playbooks were only recently finalized and no exercise has been run against them. The control cannot be rated until the first tabletop is completed and evidence is retained.

- **Related incidents:** —
- **Remediation tasks:** [TSK-003](04-ir-tasks.md#tsk-003)

### <a id="ir-08"></a>**IR-08** — Post-Incident Review and Lessons Learned

**Description:** Hold a blameless review within 10 business days of every High or Critical incident. Document root cause, timeline and corrective actions, and review incident trends monthly with security leadership.

**Decision rationale:** Reviews are held and reports are written, but corrective actions are tracked in separate tickets and closure is not verified. Two actions from the last quarter were still open past their due dates.

- **Related incidents:** [INC-2026-003](02-incident-register.md#inc-2026-003)
- **Remediation tasks:** —

---
[← Incident Register](02-incident-register.md) · Next: [IR Tasks →](04-ir-tasks.md)
