# Automotive Physical Units & Measurement System

This directory contains the complete technical specifications for **16 physical measurement domains** and their standardized unit representations in the Sawari Sadhan platform.

---

## 1. Physical Measurement Domains Directory

| # | Domain Directory | Physical Dimension | Canonical Unit | Base Slug | Unit Variants Count |
|:---:|---|---|:---:|:---:|:---:|
| 1 | [**`speed`**](./speed/README.md) | Speed / Velocity | `km/h` | `km-per-h` | 2 |
| 2 | [**`acceleration_time`**](./acceleration_time/README.md) | Acceleration Time | `s` | `second` | 1 |
| 3 | [**`duration`**](./duration/README.md) | Charging & Operating Duration | `minutes` | `minute` | 2 |
| 4 | [**`power`**](./power/README.md) | Power | `kW` | `kilowatt` | 5 |
| 5 | [**`torque`**](./torque/README.md) | Torque | `Nm` | `newton-meter` | 2 |
| 6 | [**`energy_capacity`**](./energy_capacity/README.md) | Battery Energy & Electrical Capacity | `kWh` | `kilowatt-hour` | 4 |
| 7 | [**`electrical_potential`**](./electrical_potential/README.md) | Electrical Potential (Voltage) | `V` | `volt` | 2 |
| 8 | [**`distance`**](./distance/README.md) | Distance & Driving Range | `km` | `kilometer` | 2 |
| 9 | [**`length_dimension`**](./length_dimension/README.md) | Dimensions & Clearances | `mm` | `millimeter` | 4 |
| 10 | [**`volume`**](./volume/README.md) | Volume & Liquid Capacity | `L` | `liter` | 3 |
| 11 | [**`mass`**](./mass/README.md) | Mass & Vehicle Weight | `kg` | `kilogram` | 2 |
| 12 | [**`rotational_speed`**](./rotational_speed/README.md) | Rotational Speed | `rpm` | `rpm` | 1 |
| 13 | [**`angle`**](./angle/README.md) | Angle & Gradient | `degrees` | `degree` | 2 |
| 14 | [**`energy_consumption`**](./energy_consumption/README.md) | Energy Consumption & Fuel Economy | `kWh/100km / L/100km` | `kwh-per-100km` | 4 |
| 15 | [**`pressure`**](./pressure/README.md) | Pressure | `psi` | `psi` | 3 |
| 16 | [**`pixel_density`**](./pixel_density/README.md) | Display Pixel Density | `PPI` | `ppi` | 1 |

---

## 2. Invariants & Conversion Architecture

1. **Single Source of Truth**: Every physical quantity is stored in its canonical SI/base unit (`canonical_slug`) inside the database.
2. **Clean Attribute Names**: Attribute slugs strictly describe physical properties without embedded units (e.g. `ground-clearance`, not `ground-clearance-mm`; `top-speed`, not `top-speed-kmph`).
3. **Lossless Conversion**: Conversion factors allow seamless switching between regional formats (Metric vs Imperial) in the view tier.
