# Acceleration Time (`acceleration_time`)

Measurement domain specification for automotive **Acceleration Time** values.

---

## 1. Domain Specification

| Specification | Value |
|---|---|
| **Domain Identifier** | `acceleration_time` |
| **Canonical Base Unit** | `s` |
| **Canonical Base Slug** | `second` |
| **Data Representation** | `float` |

---

## 2. Supported Units & Conversion Factors

| Unit Symbol | Unit Slug | Full Name | Conversion Factor to Canonical |
|:---:|:---:|---|:---:|
| `s` | `second` | Seconds | `1.0` |

---

## 3. Engineering Invariants

1. **Database Canonicalization**: All incoming metrics are stored in canonical base units (`second`) for exact numeric comparisons and queries.
2. **Dynamic UI Rendering**: Front-end applications convert from canonical base units to regional user preferences (e.g. Metric vs Imperial).
3. **Decoupled Slugs**: Attribute slugs (e.g. `acceleration-0-100`) never embed units in their names; they point dynamically to `second`.
