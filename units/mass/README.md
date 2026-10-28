# Mass & Vehicle Weight (`mass`)

Measurement domain specification for automotive **Mass & Vehicle Weight** values.

---

## 1. Domain Specification

| Specification | Value |
|---|---|
| **Domain Identifier** | `mass` |
| **Canonical Base Unit** | `kg` |
| **Canonical Base Slug** | `kilogram` |
| **Data Representation** | `float` |

---

## 2. Supported Units & Conversion Factors

| Unit Symbol | Unit Slug | Full Name | Conversion Factor to Canonical |
|:---:|:---:|---|:---:|
| `kg` | `kilogram` | Kilograms | `1.0` |
| `lbs` | `pound` | Pounds | `0.453592` |

---

## 3. Engineering Invariants

1. **Database Canonicalization**: All incoming metrics are stored in canonical base units (`kilogram`) for exact numeric comparisons and queries.
2. **Dynamic UI Rendering**: Front-end applications convert from canonical base units to regional user preferences (e.g. Metric vs Imperial).
3. **Decoupled Slugs**: Attribute slugs (e.g. `curb-weight`) never embed units in their names; they point dynamically to `kilogram`.
