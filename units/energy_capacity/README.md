# Battery Energy & Electrical Capacity (`energy_capacity`)

Measurement domain specification for automotive **Battery Energy & Electrical Capacity** values.

---

## 1. Domain Specification

| Specification | Value |
|---|---|
| **Domain Identifier** | `energy_capacity` |
| **Canonical Base Unit** | `kWh` |
| **Canonical Base Slug** | `kilowatt-hour` |
| **Data Representation** | `float` |

---

## 2. Supported Units & Conversion Factors

| Unit Symbol | Unit Slug | Full Name | Conversion Factor to Canonical |
|:---:|:---:|---|:---:|
| `kWh` | `kilowatt-hour` | Kilowatt-hours | `1.0` |
| `Wh` | `watt-hour` | Watt-hours | `0.001` |
| `Ah` | `ampere-hour` | Ampere-hours | `1.0` |
| `Wh/kg` | `watt-hour-per-kg` | Gravimetric Energy Density | `1.0` |

---

## 3. Engineering Invariants

1. **Database Canonicalization**: All incoming metrics are stored in canonical base units (`kilowatt-hour`) for exact numeric comparisons and queries.
2. **Dynamic UI Rendering**: Front-end applications convert from canonical base units to regional user preferences (e.g. Metric vs Imperial).
3. **Decoupled Slugs**: Attribute slugs (e.g. `battery-capacity`) never embed units in their names; they point dynamically to `kilowatt-hour`.
