# 04 · IR Tasks

**Navigate:** [README](../README.md) · [Assets](01-asset-inventory.md) · [Incidents](02-incident-register.md) · [Controls](03-ir-control-catalog.md) · [Tasks](04-ir-tasks.md)

Actions that close the gaps found in the [control catalog](03-ir-control-catalog.md) and the [incident register](02-incident-register.md).

## Summary

| ID | Title | Priority | Status | Assignee | Due |
|---|---|---|---|---|---|
| [TSK-001](#tsk-001) | Extend audit log retention for legacy EHR modules | Critical | In Progress | Platform Operations Manager | 2026-11-06 |
| [TSK-002](#tsk-002) | Automate 60-day breach notification deadline tracking | High | Planned | Compliance and Privacy Officer | 2026-11-20 |
| [TSK-003](#tsk-003) | Run first PHI breach tabletop exercise | High | Not Started | Security Operations Manager | 2026-12-04 |
| [TSK-004](#tsk-004) | Recalibrate severity matrix and train SOC analysts | Medium | Planned | SOC Lead | 2026-11-13 |
| [TSK-005](#tsk-005) | Approve incident response plan and playbooks | High | Completed | Security Operations Manager | 2026-09-15 |

## Details

### <a id="tsk-001"></a>**TSK-001** — Extend audit log retention for legacy EHR modules

Raise retention from 30 days to the period set by the logging policy so late-discovered breaches can be investigated. Addresses the Ineffective rating on IR-06. Confirm storage cost and capacity before rollout.

- **Related controls:** [IR-06](03-ir-control-catalog.md#ir-06)
- **Related incidents:** [INC-2026-002](02-incident-register.md#inc-2026-002)

### <a id="tsk-002"></a>**TSK-002** — Automate 60-day breach notification deadline tracking

Replace the manual spreadsheet with ticket-based tracking that starts the clock at discovery and alerts at 30, 45 and 55 days. Also refresh the covered-entity contact list. Addresses IR-05.

- **Related controls:** [IR-05](03-ir-control-catalog.md#ir-05)
- **Related incidents:** [INC-2026-002](02-incident-register.md#inc-2026-002)

### <a id="tsk-003"></a>**TSK-003** — Run first PHI breach tabletop exercise

Simulate a multi-hospital PHI exposure with legal, privacy, communications and executive participants. Record findings and open corrective actions. Needed before IR-07 can be rated.

- **Related controls:** [IR-07](03-ir-control-catalog.md#ir-07)
- **Related incidents:** —

### <a id="tsk-004"></a>**TSK-004** — Recalibrate severity matrix and train SOC analysts

Review the Critical/High/Medium/Low matrix, add worked examples, and make the rationale field mandatory in the incident register. Re-sample classifications after training. Addresses IR-03.

- **Related controls:** [IR-03](03-ir-control-catalog.md#ir-03)
- **Related incidents:** [INC-2026-001](02-incident-register.md#inc-2026-001)

### <a id="tsk-005"></a>**TSK-005** — Approve incident response plan and playbooks

Plan and five playbooks (phishing, ransomware, PHI breach, insider threat, availability outage) reviewed and approved by leadership and legal. Version-controlled in the policy repository.

- **Related controls:** [IR-01](03-ir-control-catalog.md#ir-01)
- **Related incidents:** [INC-2026-003](02-incident-register.md#inc-2026-003)

---
[← IR Control Catalog](03-ir-control-catalog.md) · [Back to README](../README.md)
