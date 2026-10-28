# Volume & Liquid Capacity (`volume`)

Measurement domain specification for automotive **Volume & Liquid Capacity** values.

---

## 1. Domain Specification

| Specification | Value |
|---|---|
| **Domain Identifier** | `volume` |
| **Canonical Base Unit** | `L` |
| **Canonical Base Slug** | `liter` |
| **Data Representation** | `float` |

---

## 2. Supported Units & Conversion Factors

| Unit Symbol | Unit Slug | Full Name | Conversion Factor to Canonical |
|:---:|:---:|---|:---:|
| `L` | `liter` | Liters | `1.0` |
| `cc` | `cubic-centimeter` | Cubic Centimeters (Displacement) | `0.001` |
| `cu ft` | `cubic-foot` | Cubic Feet | `28.3168` |

---

## 3. Engineering Invariants

1. **Database Canonicalization**: All incoming metrics are stored in canonical base units (`liter`) for exact numeric comparisons and queries.
2. **Dynamic UI Rendering**: Front-end applications convert from canonical base units to regional user preferences (e.g. Metric vs Imperial).
3. **Decoupled Slugs**: Attribute slugs (e.g. `fuel-tank-capacity`) never embed units in their names; they point dynamically to `liter`.
