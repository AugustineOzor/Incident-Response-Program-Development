# 01 · Asset Inventory

**Navigate:** [README](../README.md) · [Assets](01-asset-inventory.md) · [Incidents](02-incident-register.md) · [Controls](03-ir-control-catalog.md) · [Tasks](04-ir-tasks.md)

Systems and data stores in scope for the incident response program. Classification reflects business and PHI impact.

## Summary

| ID | Name | Type | Classification | Owner | Environment | Related incidents |
|---|---|---|---|---|---|---|
| [AST-001](#ast-001) | HealthTech EHR Platform (Web Application) | Application | Critical | Platform Operations Manager | Production | [INC-2026-003](02-incident-register.md#inc-2026-003) |
| [AST-002](#ast-002) | Patient Records Database Cluster | Database | Critical | Database Engineering Lead | Production | [INC-2026-002](02-incident-register.md#inc-2026-002), [INC-2026-003](02-incident-register.md#inc-2026-003) |
| [AST-003](#ast-003) | AWS Production Cloud Account | Cloud Account | High | Cloud Security Lead | Production | [INC-2026-001](02-incident-register.md#inc-2026-001), [INC-2026-002](02-incident-register.md#inc-2026-002) |
| [AST-004](#ast-004) | Disaster Recovery Backup Store | Data Store | High | Infrastructure Manager | DR | — |

## Details

### <a id="ast-001"></a>**AST-001** — HealthTech EHR Platform (Web Application)

Multi-tenant EHR web application used by clinicians at 200+ hospitals to view and update patient records. Processes and displays PHI; downtime directly affects patient care.

- **Related incidents:** [INC-2026-003](02-incident-register.md#inc-2026-003)

### <a id="ast-002"></a>**AST-002** — Patient Records Database Cluster

Primary relational database cluster storing PHI for over 2 million patients, encrypted at rest. Holds demographics, clinical notes, medications and billing identifiers.

- **Related incidents:** [INC-2026-002](02-incident-register.md#inc-2026-002), [INC-2026-003](02-incident-register.md#inc-2026-003)

### <a id="ast-003"></a>**AST-003** — AWS Production Cloud Account

Primary cloud account hosting EHR workloads, storage and networking. Access is governed by SSO with MFA and least-privilege roles; compromise would expose multiple critical systems.

- **Related incidents:** [INC-2026-001](02-incident-register.md#inc-2026-001), [INC-2026-002](02-incident-register.md#inc-2026-002)

### <a id="ast-004"></a>**AST-004** — Disaster Recovery Backup Store

Encrypted, cross-region backup storage holding replicated EHR database snapshots and logs for recovery. Contains PHI copies and is required to meet recovery time objectives.

- **Related incidents:** —

---
Next: [Incident Register →](02-incident-register.md)
