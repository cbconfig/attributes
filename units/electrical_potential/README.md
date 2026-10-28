# Electrical Potential (Voltage) (`electrical_potential`)

Measurement domain specification for automotive **Electrical Potential (Voltage)** values.

---

## 1. Domain Specification

| Specification | Value |
|---|---|
| **Domain Identifier** | `electrical_potential` |
| **Canonical Base Unit** | `V` |
| **Canonical Base Slug** | `volt` |
| **Data Representation** | `float` |

---

## 2. Supported Units & Conversion Factors

| Unit Symbol | Unit Slug | Full Name | Conversion Factor to Canonical |
|:---:|:---:|---|:---:|
| `V` | `volt` | Volts | `1.0` |
| `kV` | `kilovolt` | Kilovolts | `1000.0` |

---

## 3. Engineering Invariants

1. **Database Canonicalization**: All incoming metrics are stored in canonical base units (`volt`) for exact numeric comparisons and queries.
2. **Dynamic UI Rendering**: Front-end applications convert from canonical base units to regional user preferences (e.g. Metric vs Imperial).
3. **Decoupled Slugs**: Attribute slugs (e.g. `battery-voltage`) never embed units in their names; they point dynamically to `volt`.
