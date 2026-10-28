# Dimensions & Clearances (`length_dimension`)

Measurement domain specification for automotive **Dimensions & Clearances** values.

---

## 1. Domain Specification

| Specification | Value |
|---|---|
| **Domain Identifier** | `length_dimension` |
| **Canonical Base Unit** | `mm` |
| **Canonical Base Slug** | `millimeter` |
| **Data Representation** | `float` |

---

## 2. Supported Units & Conversion Factors

| Unit Symbol | Unit Slug | Full Name | Conversion Factor to Canonical |
|:---:|:---:|---|:---:|
| `mm` | `millimeter` | Millimeters | `1.0` |
| `cm` | `centimeter` | Centimeters | `10.0` |
| `m` | `meter` | Meters | `1000.0` |
| `inches` | `inch` | Inches | `25.4` |

---

## 3. Engineering Invariants

1. **Database Canonicalization**: All incoming metrics are stored in canonical base units (`millimeter`) for exact numeric comparisons and queries.
2. **Dynamic UI Rendering**: Front-end applications convert from canonical base units to regional user preferences (e.g. Metric vs Imperial).
3. **Decoupled Slugs**: Attribute slugs (e.g. `ground-clearance`) never embed units in their names; they point dynamically to `millimeter`.
