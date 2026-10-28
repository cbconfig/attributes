# Display Pixel Density (`pixel_density`)

Measurement domain specification for automotive **Display Pixel Density** values.

---

## 1. Domain Specification

| Specification | Value |
|---|---|
| **Domain Identifier** | `pixel_density` |
| **Canonical Base Unit** | `PPI` |
| **Canonical Base Slug** | `ppi` |
| **Data Representation** | `integer` |

---

## 2. Supported Units & Conversion Factors

| Unit Symbol | Unit Slug | Full Name | Conversion Factor to Canonical |
|:---:|:---:|---|:---:|
| `PPI` | `ppi` | Pixels Per Inch | `1.0` |

---

## 3. Engineering Invariants

1. **Database Canonicalization**: All incoming metrics are stored in canonical base units (`ppi`) for exact numeric comparisons and queries.
2. **Dynamic UI Rendering**: Front-end applications convert from canonical base units to regional user preferences (e.g. Metric vs Imperial).
3. **Decoupled Slugs**: Attribute slugs (e.g. `screen-pixel-density`) never embed units in their names; they point dynamically to `ppi`.
