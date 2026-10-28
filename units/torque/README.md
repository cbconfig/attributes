# Torque (`torque`)

Measurement domain specification for automotive **Torque** values.

---

## 1. Domain Specification

| Specification | Value |
|---|---|
| **Domain Identifier** | `torque` |
| **Canonical Base Unit** | `Nm` |
| **Canonical Base Slug** | `newton-meter` |
| **Data Representation** | `float` |

---

## 2. Supported Units & Conversion Factors

| Unit Symbol | Unit Slug | Full Name | Conversion Factor to Canonical |
|:---:|:---:|---|:---:|
| `Nm` | `newton-meter` | Newton-meters | `1.0` |
| `lb-ft` | `pound-foot` | Pound-feet | `1.35582` |

---

## 3. Engineering Invariants

1. **Database Canonicalization**: All incoming metrics are stored in canonical base units (`newton-meter`) for exact numeric comparisons and queries.
2. **Dynamic UI Rendering**: Front-end applications convert from canonical base units to regional user preferences (e.g. Metric vs Imperial).
3. **Decoupled Slugs**: Attribute slugs (e.g. `torque-engine`) never embed units in their names; they point dynamically to `newton-meter`.
