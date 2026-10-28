# Energy Consumption & Fuel Economy (`energy_consumption`)

Measurement domain specification for automotive **Energy Consumption & Fuel Economy** values.

---

## 1. Domain Specification

| Specification | Value |
|---|---|
| **Domain Identifier** | `energy_consumption` |
| **Canonical Base Unit** | `kWh/100km / L/100km` |
| **Canonical Base Slug** | `kwh-per-100km` |
| **Data Representation** | `float` |

---

## 2. Supported Units & Conversion Factors

| Unit Symbol | Unit Slug | Full Name | Conversion Factor to Canonical |
|:---:|:---:|---|:---:|
| `kWh/100km` | `kwh-per-100km` | Kilowatt-hours per 100 kilometers | `1.0` |
| `L/100km` | `liters-per-100km` | Liters per 100 kilometers | `1.0` |
| `km/l` | `km-per-liter` | Kilometers per liter | `1.0` |
| `mpg` | `miles-per-gallon` | Miles per gallon | `1.0` |

---

## 3. Engineering Invariants

1. **Database Canonicalization**: All incoming metrics are stored in canonical base units (`kwh-per-100km`) for exact numeric comparisons and queries.
2. **Dynamic UI Rendering**: Front-end applications convert from canonical base units to regional user preferences (e.g. Metric vs Imperial).
3. **Decoupled Slugs**: Attribute slugs (e.g. `energy-consumption`) never embed units in their names; they point dynamically to `kwh-per-100km`.
