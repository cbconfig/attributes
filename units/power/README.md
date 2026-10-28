# Power (`power`)

Measurement domain specification for automotive **Power** values.

---

## 1. Domain Specification

| Specification | Value |
|---|---|
| **Domain Identifier** | `power` |
| **Canonical Base Unit** | `kW` |
| **Canonical Base Slug** | `kilowatt` |
| **Data Representation** | `float` |

---

## 2. Supported Units & Conversion Factors

| Unit Symbol | Unit Slug | Full Name | Conversion Factor to Canonical |
|:---:|:---:|---|:---:|
| `kW` | `kilowatt` | Kilowatts | `1.0` |
| `bhp` | `brake-horsepower` | Brake Horsepower | `0.7457` |
| `PS` | `metric-horsepower-ps` | Pferdestärke (Metric Horsepower) | `0.7355` |
| `hp` | `horsepower` | Mechanical Horsepower | `0.7457` |
| `W` | `watt` | Watts | `0.001` |

---

## 3. Engineering Invariants

1. **Database Canonicalization**: All incoming metrics are stored in canonical base units (`kilowatt`) for exact numeric comparisons and queries.
2. **Dynamic UI Rendering**: Front-end applications convert from canonical base units to regional user preferences (e.g. Metric vs Imperial).
3. **Decoupled Slugs**: Attribute slugs (e.g. `power-motor`) never embed units in their names; they point dynamically to `kilowatt`.
