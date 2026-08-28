
---

# 📄 spec/audit-trail-spec.md

```markdown
# OATS Specification v0.1

## 1. Overview

This document defines the canonical structure for audit trail events in GxP-regulated systems.

---

## 2. Canonical Model

### Required Fields

| Field | Description |
|------|-------------|
| event_id | Unique identifier |
| timestamp | Event timestamp (ISO 8601) |
| user | User performing the action |
| operation | Action type |

---

### Context Fields

| Field | Description |
|------|-------------|
| object_type | Type of object |
| object | Object name |
| field | Field affected |

---

### Change Tracking

| Field | Description |
|------|-------------|
| old_value | Value before change |
| new_value | Value after change |

---

### Compliance Fields

| Field | Description |
|------|-------------|
| reason | Reason for change |
| source | System or machine |

---

## 3. Field Mapping

### User

user id, operator, performed by, login, full name, modified by, changed by, executed by, user

---

### Operation

operation, action, action type, event, activity, transaction, change type, audit type

---

### Timestamp

date, time, timestamp, event timestamp, EventTime, created at, recorded at, logged at

---

### Event ID

eventID, AuditID, Record ID, AuditEntryID, AuditTrailID, logID, id

---

### Old Value

previous value, prior value, old value, before, old

---

### New Value

updated value, current value, new value, after, new

---

### Reason

reason for change, justification, comment, remarks, rationale

---

### Object Type

object type, entity type, record type, item type, module type, category

---

### Field

property, field name, field, attribute

---

### Object

object name, entity, module, table, parameter, target, subject, resource

---

### Source

location, machine id, workstation, terminal id, station, app

---

## 4. Processing Rules

1. Case-insensitive matching
2. Partial matching allowed
3. Priority order:
   - timestamp
   - user
   - operation
   - object_type
   - field
   - object
   - values
   - reason
   - source
   - event_id

---

## 5. Compliance Levels

### Minimum
- timestamp
- user
- operation

### Recommended
- event_id
- object
- field

### Full
All fields populated

---

## 6. Interoperability

Systems MUST:
- support mapping to canonical format
- preserve original values
- avoid data loss

---

## 7. Future Extensions

- JSON Schema validation
- Operation taxonomy
- Digital signatures
