# Charging & Operating Duration (`duration`)

Measurement domain specification for automotive **Charging & Operating Duration** values.

---

## 1. Domain Specification

| Specification | Value |
|---|---|
| **Domain Identifier** | `duration` |
| **Canonical Base Unit** | `minutes` |
| **Canonical Base Slug** | `minute` |
| **Data Representation** | `float` |

---

## 2. Supported Units & Conversion Factors

| Unit Symbol | Unit Slug | Full Name | Conversion Factor to Canonical |
|:---:|:---:|---|:---:|
| `minutes` | `minute` | Minutes | `1.0` |
| `hours` | `hour` | Hours | `60.0` |

---

## 3. Engineering Invariants

1. **Database Canonicalization**: All incoming metrics are stored in canonical base units (`minute`) for exact numeric comparisons and queries.
2. **Dynamic UI Rendering**: Front-end applications convert from canonical base units to regional user preferences (e.g. Metric vs Imperial).
3. **Decoupled Slugs**: Attribute slugs (e.g. `charging-time-fast`) never embed units in their names; they point dynamically to `minute`.
