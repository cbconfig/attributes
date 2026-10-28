# Distance & Driving Range (`distance`)

Measurement domain specification for automotive **Distance & Driving Range** values.

---

## 1. Domain Specification

| Specification | Value |
|---|---|
| **Domain Identifier** | `distance` |
| **Canonical Base Unit** | `km` |
| **Canonical Base Slug** | `kilometer` |
| **Data Representation** | `float` |

---

## 2. Supported Units & Conversion Factors

| Unit Symbol | Unit Slug | Full Name | Conversion Factor to Canonical |
|:---:|:---:|---|:---:|
| `km` | `kilometer` | Kilometers | `1.0` |
| `miles` | `mile` | Miles | `1.60934` |

---

## 3. Engineering Invariants

1. **Database Canonicalization**: All incoming metrics are stored in canonical base units (`kilometer`) for exact numeric comparisons and queries.
2. **Dynamic UI Rendering**: Front-end applications convert from canonical base units to regional user preferences (e.g. Metric vs Imperial).
3. **Decoupled Slugs**: Attribute slugs (e.g. `range-claimed`) never embed units in their names; they point dynamically to `kilometer`.
