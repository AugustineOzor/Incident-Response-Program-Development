<p align="center">
  <img width="2800" height="680" alt="banner" src="https://github.com/user-attachments/assets/3c81ca4c-1bb0-4106-aaf4-b966e2e38344" />

</p>

# HealthTech Systems: Incident Response Program Toolkit

A project showing how a Security Operations Manager at an EHR provider builds an incident response program and keeps HIPAA breach notification on track. HealthTech Systems serves 200+ hospitals, holds PHI for over 2 million patients, and has 600 employees.

## Contents

| # | Document | What it covers |
|---|---|---|
| 1 | [Asset Inventory](docs/01-asset-inventory.md) | 4 systems and data stores in scope, with classification, owner and environment |
| 2 | [Incident Register](docs/02-incident-register.md) | 3 sample incidents: phishing, PHI data breach, and an EHR availability outage |
| 3 | [IR Control Catalog](docs/03-ir-control-catalog.md) | 8 incident response controls with framework references, effectiveness ratings and rationale |
| 4 | [IR Tasks](docs/04-ir-tasks.md) | 5 remediation tasks that close the gaps found in the controls and incidents |

## How the documents connect

Every record has an anchor, and each document links to the others:

- **Incidents** point to the affected assets, the controls that applied, and the follow-up tasks.
- **Controls** point to the incidents that tested them and the tasks that remediate them.
- **Assets** list the incidents that involved them.
- **Tasks** point back to the control gap and incident that triggered them.

The cross-references are a portfolio mapping created for this case study.

## Frameworks referenced

HIPAA Security Rule and Breach Notification Rule · NIST CSF · ISO/IEC 27001

## Disclaimer

All organizations, systems, incidents, ratings and dates are fictional and were created for skills practice and portfolio use. This is not legal advice or a compliance determination. Framework references are paraphrased pointers, so verify them against the source text before relying on them.
