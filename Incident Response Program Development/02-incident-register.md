# 02 · Incident Register

**Navigate:** [README](../README.md) · [Assets](01-asset-inventory.md) · [Incidents](02-incident-register.md) · [Controls](03-ir-control-catalog.md) · [Tasks](04-ir-tasks.md)

Sample incidents logged against the assets in the [Asset Inventory](01-asset-inventory.md). Each record points to the controls that applied and the follow-up tasks it generated.

## Summary

| ID | Title | Type | Severity | Status | Detected | Closed | Owner |
|---|---|---|---|---|---|---|---|
| [INC-2026-001](#inc-2026-001) | Credential phishing campaign targeting billing staff | Phishing | High | Closed | 2026-08-12 09:14 | 2026-08-19 16:30 | SOC Lead |
| [INC-2026-002](#inc-2026-002) | Misconfigured cloud storage exposing PHI report exports | Data Breach | Critical | Investigating | 2026-09-03 22:41 | — | Security Operations Manager |
| [INC-2026-003](#inc-2026-003) | EHR platform outage after failed database patch | Availability | High | Resolved | 2026-09-21 02:05 | — | Platform Operations Manager |

## Details

### <a id="inc-2026-001"></a>**INC-2026-001** — Credential phishing campaign targeting billing staff

**Description:** 14 billing and support employees received spoofed Microsoft 365 sign-in emails. 3 users clicked the link and 1 entered credentials. No evidence of access to EHR or PHI systems.

**Resolution:** Compromised account disabled and credentials reset; sender domain blocked and emails purged; MFA enforced for all remaining accounts; targeted awareness refresher delivered. HIPAA four-factor risk assessment found low probability of PHI compromise, so no breach notification was required. Assessment documented and retained.

- **Affected assets:** [AST-003](01-asset-inventory.md#ast-003)
- **Related controls:** [IR-02](03-ir-control-catalog.md#ir-02), [IR-03](03-ir-control-catalog.md#ir-03), [IR-05](03-ir-control-catalog.md#ir-05)
- **Follow-up tasks:** [TSK-004](04-ir-tasks.md#tsk-004)

### <a id="inc-2026-002"></a>**INC-2026-002** — Misconfigured cloud storage exposing PHI report exports

**Description:** A storage bucket holding scheduled report exports for two hospital customers was publicly readable for about 36 hours. The exports contain records for roughly 18,400 patients. Access logs show requests from external IP addresses.

**Resolution:** In progress: public access removed and bucket secured; forensic review of access logs under way; affected covered entities notified. As a business associate, HealthTech notifies covered entities without unreasonable delay (no later than 60 days); covered entities then notify individuals and HHS OCR (and media where 500+ residents of a state are affected). Cloud configuration scanning to be added to the deployment pipeline.

- **Affected assets:** [AST-002](01-asset-inventory.md#ast-002), [AST-003](01-asset-inventory.md#ast-003)
- **Related controls:** [IR-02](03-ir-control-catalog.md#ir-02), [IR-03](03-ir-control-catalog.md#ir-03), [IR-04](03-ir-control-catalog.md#ir-04), [IR-05](03-ir-control-catalog.md#ir-05), [IR-06](03-ir-control-catalog.md#ir-06)
- **Follow-up tasks:** [TSK-001](04-ir-tasks.md#tsk-001), [TSK-002](04-ir-tasks.md#tsk-002)

### <a id="inc-2026-003"></a>**INC-2026-003** — EHR platform outage after failed database patch

**Description:** A scheduled database patch failed and left the EHR platform unavailable to 41 hospitals for about 4 hours 20 minutes. Clinicians fell back to downtime procedures. No evidence of unauthorized access to or disclosure of PHI.

**Resolution:** Patch rolled back and service restored; customers updated through the status page; root cause identified as a missing pre-patch compatibility test. Change-management gate and rollback rehearsal added. Closure pending post-incident review.

- **Affected assets:** [AST-001](01-asset-inventory.md#ast-001), [AST-002](01-asset-inventory.md#ast-002)
- **Related controls:** [IR-01](03-ir-control-catalog.md#ir-01), [IR-04](03-ir-control-catalog.md#ir-04), [IR-08](03-ir-control-catalog.md#ir-08)
- **Follow-up tasks:** [TSK-005](04-ir-tasks.md#tsk-005)

---
[← Asset Inventory](01-asset-inventory.md) · Next: [IR Control Catalog →](03-ir-control-catalog.md)
