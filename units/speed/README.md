# Speed / Velocity (`speed`)

Measurement domain specification for automotive **Speed / Velocity** values.

---

## 1. Domain Specification

| Specification | Value |
|---|---|
| **Domain Identifier** | `speed` |
| **Canonical Base Unit** | `km/h` |
| **Canonical Base Slug** | `km-per-h` |
| **Data Representation** | `float` |

---

## 2. Supported Units & Conversion Factors

| Unit Symbol | Unit Slug | Full Name | Conversion Factor to Canonical |
|:---:|:---:|---|:---:|
| `km/h` | `km-per-h` | Kilometers per hour | `1.0` |
| `mph` | `miles-per-h` | Miles per hour | `1.60934` |

---

## 3. Engineering Invariants

1. **Database Canonicalization**: All incoming metrics are stored in canonical base units (`km-per-h`) for exact numeric comparisons and queries.
2. **Dynamic UI Rendering**: Front-end applications convert from canonical base units to regional user preferences (e.g. Metric vs Imperial).
3. **Decoupled Slugs**: Attribute slugs (e.g. `top-speed`) never embed units in their names; they point dynamically to `km-per-h`.
