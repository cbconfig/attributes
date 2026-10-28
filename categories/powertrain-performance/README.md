# ⚡ Engine, Motor & Performance

**Pillar Slug**: `powertrain-performance`  
**International Standards**: *SAE J1349 (ICE Ratings), SAE J2907 (EV Ratings), UNECE R85*

ICE combustion engines, electric propulsion traction motors, transmissions, horsepower/kilowatt output, torque curves, and dynamic acceleration metrics.

---

## 1. Domain Overview

| Metric | Value |
|---|---|
| **Canonical Pillar Slug** | `powertrain-performance` |
| **Total Standardized Attributes** | 62 |
| **Active In Blueprints** | 2W-BEV, 2W-ICE, 4W-BEV, 4W-ICE |

---

## 2. Standardized Attributes Catalog

| Attribute Slug | Value Type | Unit / Specification | Applicable Blueprints |
|---|:---:|:---:|---|
| `acceleration-0-100` | `unit` | `second` | 2W-ICE |
| `acceleration-0-40` | `unit` | `second` | 2W-BEV |
| `acceleration-0-60` | `unit` | `second` | 2W-BEV, 2W-ICE |
| `braking-60-0` | `string` | — | 2W-ICE |
| `city-milage` | `string` | — | 2W-ICE |
| `clutch` | `string` | — | 2W-ICE |
| `compression-ratio` | `unit` | `ratio` | 2W-ICE |
| `compression-ration` | `string` | — | 4W-ICE |
| `cooling-system` | `enum` | — | 2W-ICE |
| `cruise-control` | `boolean` | — | 2W-BEV |
| `drive-type` | `enum` | — | 2W-BEV, 2W-ICE, 4W-BEV, 4W-ICE |
| `electric-motor-type` | `string` | — | 4W-BEV |
| `emission-norms-compliance` | `string` | — | 4W-ICE |
| `emission-standard` | `enum` | — | 2W-ICE |
| `engiene-type` | `string` | — | 2W-ICE, 4W-ICE |
| `engine-bore` | `unit` | `millimeter` | 2W-ICE |
| `engine-displacement` | `unit` | `cubic-centimeter` | 2W-ICE, 4W-ICE |
| `engine-stroke` | `unit` | `millimeter` | 2W-ICE |
| `fuel-supply` | `unit` | `unknown` | 2W-ICE |
| `fuel-supply-system` | `unit` | `unknown` | 4W-ICE |
| `fuel-tank-capacity` | `unit` | `liter` | 4W-ICE |
| `fuel-type` | `enum` | — | 4W-ICE |
| `gear-box` | `string` | — | 2W-ICE, 4W-ICE |
| `gradeability` | `unit` | `percent` | 2W-BEV |
| `highway-milage` | `string` | — | 2W-ICE |
| `hill-hold-assist` | `boolean` | — | 2W-BEV |
| `ignition` | `string` | — | 2W-ICE |
| `milage` | `string` | — | 4W-ICE |
| `motor-ip-rating` | `rating` | — | 2W-BEV |
| `motor-placement` | `string` | — | 2W-BEV |
| `motor-type` | `enum` | — | 2W-BEV |
| `number-of-cylinders` | `integer` | — | 2W-ICE, 4W-ICE |
| `number-of-gears` | `integer` | — | 4W-BEV |
| `number-of-motors` | `integer` | — | 4W-BEV |
| `number-of-valves-per-cylinder` | `integer` | — | 2W-ICE, 4W-ICE |
| `operating-efficiency` | `string` | — | 4W-BEV |
| `overall-milage` | `string` | — | 2W-ICE |
| `power-motor` | `unit` | `kilowatt` | 2W-BEV |
| `power-motor-continuous` | `unit` | `kilowatt` | 2W-BEV |
| `power-motor-front` | `unit` | `kilowatt` | 4W-BEV |
| `power-motor-peak` | `unit` | `kilowatt` | 2W-BEV, 4W-BEV |
| `power-motor-rear` | `unit` | `kilowatt` | 4W-BEV |
| `power-total` | `unit` | `kilowatt` | 2W-ICE, 4W-BEV, 4W-ICE |
| `quickshifter` | `string` | — | 2W-ICE |
| `reverse-mode` | `boolean` | — | 2W-BEV |
| `riding-modes` | `boolean` | — | 2W-BEV, 2W-ICE |
| `slipper-clutch` | `boolean` | — | 2W-ICE |
| `starting` | `boolean` | — | 2W-ICE |
| `starting-method` | `boolean` | — | 2W-ICE |
| `super-charge` | `boolean` | — | 4W-ICE |
| `top-speed` | `unit` | `km-per-h` | 2W-BEV, 2W-ICE |
| `torque-motor-front` | `unit` | `newton-meter` | 4W-BEV |
| `torque-motor-rear` | `unit` | `newton-meter` | 4W-BEV |
| `torque-total` | `unit` | `newton-meter` | 2W-BEV, 2W-ICE, 4W-BEV, 4W-ICE |
| `torque-wheel` | `unit` | `newton-meter` | 2W-BEV |
| `traction-control` | `boolean` | — | 2W-ICE |
| `transmission` | `string` | — | 2W-BEV, 2W-ICE |
| `transmission-description` | `string` | — | 4W-BEV |
| `transmission-type` | `enum` | — | 4W-BEV, 4W-ICE |
| `turbocharged-engine` | `boolean` | — | 4W-ICE |
| `valve-configuration` | `string` | — | 4W-ICE |
| `walk-assist` | `boolean` | — | 2W-BEV |

---

## 3. Implementation Guidelines

- **Attribute Decoupling**: Attribute slugs describe physical metrics; units are tracked dynamically.
- **Discrete Counts**: Discrete whole-number quantities must strictly use `number-of-*` prefixes.
- **Cross-Archetype Consistency**: Any attribute shared between two-wheelers and four-wheelers maintains identical typing.
