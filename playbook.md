---
layout: default
title: Implementation Playbook — Multi‑Organization HMS
permalink: /playbook/
---


# Implementation Playbook — HMS (5 Organizations)


## 1. Governance & Compliance
- Sign DPA/BAA equivalents per organization; define data residency, retention, and access controls.
- Appoint Security Officer and Privacy Officer roles; finalize audit scope and cadence.


## 2. Environment Setup
- Primary region within country, DR region as permitted; VPC per environment (dev/test/stage/prod).
- Secrets in KMS/HSM; per‑org keys; org‑scoped buckets/prefixes.


## 3. Identity & Access
- SSO (SAML/OIDC) per org; MFA; RBAC roles; least‑privilege policies.
- JIT provisioning or SCIM; quarterly access reviews.


## 4. Data Model & Migration
- Mapping: patients, providers, encounters, orders, results, claims, inventory.
- Normalize ICD‑10, LOINC, ATC; deduplicate patient masters.
- Two dress rehearsals; reconcile reports before cutover.


## 5. Integrations
- HL7/FHIR interfaces for LIS, PACS/RIS; insurer e‑claims; payment gateway.
- Device interfacing: barcoding, analyzers, vitals; message broker for events.


## 6. Security Engineering
- TLS 1.3; AES‑256; signed audit logs; endpoint protection; vulnerability scans; WAF.
- Backups: PITR; immutable snapshots; RPO 15 min; RTO 4 hrs; DR runbooks tested semi‑annually.


## 7. Application Configuration
- Per‑org theming; clinical templates; order sets; tariffs; roles & permissions; notifications.
- Feature flags for org‑specific rules; avoid code forks.


## 8. Testing & UAT
- Unit/integration tests; interface simulators; performance baseline.
- UAT scenarios per department; sign‑off gates.


## 9. Training & Change Management
- Role‑based curricula; train‑the‑trainer; micro‑videos and quick guides.
- Adoption metrics: e‑order usage, turnaround times, claim first‑pass rate.


## 10. Cutover & Hypercare
- Freeze window; final delta import; go‑live checklist; command center.
- Hypercare 1–2 weeks; daily standups; issue triage; knowledge transfer.


## 11. Operations & SLAs
- Monitoring: availability, latency, error budgets, per‑org dashboards.
- Incident mgmt: P1/P2 flows; post‑mortems; problem mgmt.
- Change mgmt: CAB for major changes; maintenance windows.


## 12. KPI Pack (90‑day)
- Registration cycle time; OPD wait time; ADT accuracy; e‑Orders; TAT; claim FPR; DSO; stock‑outs; bed occupancy; OR utilization; uptime; MTTR; CSAT; clinician NPS.