# Open Audit Trail Standard (OATS)

An open, vendor-neutral standard for designing, storing, and analyzing audit trails in GxP-regulated systems.

---

## 🎯 Purpose

Audit trails across systems (LIMS, MES, QMS, etc.) are inconsistent, making audits, integration, and analysis difficult.

OATS defines a **canonical audit trail model** that enables:

- Interoperability across systems
- Consistent audit trail structure
- Easier regulatory compliance (FDA, GxP)
- Centralized audit trail analysis

---

## 🧩 Core Concept

Every audit trail entry is normalized into a single structure:

```json
AuditTrailEvent

