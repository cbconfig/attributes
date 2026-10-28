# Rotational Speed (`rotational_speed`)

Measurement domain specification for automotive **Rotational Speed** values.

---

## 1. Domain Specification

| Specification | Value |
|---|---|
| **Domain Identifier** | `rotational_speed` |
| **Canonical Base Unit** | `rpm` |
| **Canonical Base Slug** | `rpm` |
| **Data Representation** | `integer` |

---

## 2. Supported Units & Conversion Factors

| Unit Symbol | Unit Slug | Full Name | Conversion Factor to Canonical |
|:---:|:---:|---|:---:|
| `rpm` | `rpm` | Revolutions per minute | `1.0` |

---

## 3. Engineering Invariants

1. **Database Canonicalization**: All incoming metrics are stored in canonical base units (`rpm`) for exact numeric comparisons and queries.
2. **Dynamic UI Rendering**: Front-end applications convert from canonical base units to regional user preferences (e.g. Metric vs Imperial).
3. **Decoupled Slugs**: Attribute slugs (e.g. `power-rpm`) never embed units in their names; they point dynamically to `rpm`.
