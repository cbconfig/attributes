# Angle & Gradient (`angle`)

Measurement domain specification for automotive **Angle & Gradient** values.

---

## 1. Domain Specification

| Specification | Value |
|---|---|
| **Domain Identifier** | `angle` |
| **Canonical Base Unit** | `degrees` |
| **Canonical Base Slug** | `degree` |
| **Data Representation** | `float` |

---

## 2. Supported Units & Conversion Factors

| Unit Symbol | Unit Slug | Full Name | Conversion Factor to Canonical |
|:---:|:---:|---|:---:|
| `degrees` | `degree` | Degrees | `1.0` |
| `%` | `percent` | Gradeability Percentage | `1.0` |

---

## 3. Engineering Invariants

1. **Database Canonicalization**: All incoming metrics are stored in canonical base units (`degree`) for exact numeric comparisons and queries.
2. **Dynamic UI Rendering**: Front-end applications convert from canonical base units to regional user preferences (e.g. Metric vs Imperial).
3. **Decoupled Slugs**: Attribute slugs (e.g. `approach-angle`) never embed units in their names; they point dynamically to `degree`.
