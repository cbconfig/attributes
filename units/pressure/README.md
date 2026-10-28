# Pressure (`pressure`)

Measurement domain specification for automotive **Pressure** values.

---

## 1. Domain Specification

| Specification | Value |
|---|---|
| **Domain Identifier** | `pressure` |
| **Canonical Base Unit** | `psi` |
| **Canonical Base Slug** | `psi` |
| **Data Representation** | `float` |

---

## 2. Supported Units & Conversion Factors

| Unit Symbol | Unit Slug | Full Name | Conversion Factor to Canonical |
|:---:|:---:|---|:---:|
| `psi` | `psi` | Pounds per square inch | `1.0` |
| `bar` | `bar` | Bar | `14.5038` |
| `kPa` | `kilopascal` | Kilopascals | `0.145038` |

---

## 3. Engineering Invariants

1. **Database Canonicalization**: All incoming metrics are stored in canonical base units (`psi`) for exact numeric comparisons and queries.
2. **Dynamic UI Rendering**: Front-end applications convert from canonical base units to regional user preferences (e.g. Metric vs Imperial).
3. **Decoupled Slugs**: Attribute slugs (e.g. `tire-pressure`) never embed units in their names; they point dynamically to `psi`.
