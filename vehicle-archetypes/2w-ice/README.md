# 🏍️ 2W-ICE (Two-Wheeler Combustion) Specification

Internal combustion engine motorcycles, commuter scooters, cruisers, and mopeds.

---

## 1. Quick Statistics

| Metric | Value |
|---|---|
| **Archetype Identifier** | `2W-ICE` |
| **Active Pillars** | 6 |
| **Total Canonical Attributes** | 77 |

---

## 2. Pillar Summary

| # | Category Pillar | Total Attributes | Dominant Data Types |
|:---:|---|:---:|---|
| 1 | **Engine, Motor & Performance** | 30 | unit (10), string (10), boolean (5) |
| 2 | **Dimensions, Body & Capacity** | 10 | unit (9), string (1) |
| 3 | **Chassis, Suspension & Brakes** | 13 | enum (4), string (4), unit (3) |
| 4 | **Safety, Security & Restraints** | 11 | boolean (9), string (2) |
| 5 | **Exterior, Lighting & Glass** | 8 | boolean (6), unit (1), enum (1) |
| 6 | **Infotainment, Telematics & Screens** | 5 | boolean (4), string (1) |

---

## 3. Complete Attribute Inventory by Pillar

### Engine, Motor & Performance
*Total Attributes: 30*

| Attribute Slug | Type | Unit / Details |
|---|:---:|---|
| `acceleration-0-100` | `unit` | `second` |
| `acceleration-0-60` | `unit` | `second` |
| `braking-60-0` | `string` | — |
| `city-milage` | `string` | — |
| `clutch` | `string` | — |
| `compression-ratio` | `unit` | `ratio` |
| `cooling-system` | `enum` | — |
| `drive-type` | `enum` | — |
| `emission-standard` | `enum` | — |
| `engiene-type` | `string` | — |
| `engine-bore` | `unit` | `millimeter` |
| `engine-displacement` | `unit` | `cubic-centimeter` |
| `engine-stroke` | `unit` | `millimeter` |
| `fuel-supply` | `unit` | `unknown` |
| `gear-box` | `string` | — |
| `highway-milage` | `string` | — |
| `ignition` | `string` | — |
| `number-of-cylinders` | `integer` | — |
| `number-of-valves-per-cylinder` | `integer` | — |
| `overall-milage` | `string` | — |
| `power-total` | `unit` | `kilowatt` |
| `quickshifter` | `string` | — |
| `riding-modes` | `boolean` | — |
| `slipper-clutch` | `boolean` | — |
| `starting` | `boolean` | — |
| `starting-method` | `boolean` | — |
| `top-speed` | `unit` | `km-per-h` |
| `torque-total` | `unit` | `newton-meter` |
| `traction-control` | `boolean` | — |
| `transmission` | `string` | — |

### Dimensions, Body & Capacity
*Total Attributes: 10*

| Attribute Slug | Type | Unit / Details |
|---|:---:|---|
| `curb-weight` | `unit` | `kilogram` |
| `fuel-tank-capacity` | `unit` | `liter` |
| `ground-clearance` | `unit` | `millimeter` |
| `height` | `unit` | `millimeter` |
| `length` | `unit` | `millimeter` |
| `seat-height` | `unit` | `millimeter` |
| `under-seat-storage` | `unit` | `liter` |
| `wheel-base` | `string` | — |
| `wheelbase` | `unit` | `millimeter` |
| `width` | `unit` | `millimeter` |

### Chassis, Suspension & Brakes
*Total Attributes: 13*

| Attribute Slug | Type | Unit / Details |
|---|:---:|---|
| `body-graphics` | `boolean` | — |
| `body-type` | `enum` | — |
| `brake-rotor-diameter-front` | `unit` | `millimeter` |
| `chasis` | `string` | — |
| `front-brake` | `string` | — |
| `front-suspension` | `enum` | — |
| `rear-brake` | `string` | — |
| `rear-suspension` | `enum` | — |
| `tyre-size` | `dimension_tuple` | — |
| `tyre-type` | `string` | — |
| `wheel-diameter` | `unit` | `inch` |
| `wheel-size` | `unit` | `inch` |
| `wheel-type` | `enum` | — |

### Safety, Security & Restraints
*Total Attributes: 11*

| Attribute Slug | Type | Unit / Details |
|---|:---:|---|
| `anti-lock-braking-system` | `boolean` | — |
| `anti-theft-alarm` | `boolean` | — |
| `clock` | `boolean` | — |
| `console` | `string` | — |
| `daytime-running-lights` | `boolean` | — |
| `engiene-mobilizer` | `string` | — |
| `hazard-warning-lights` | `boolean` | — |
| `pass-switch` | `boolean` | — |
| `passenger-footrest` | `boolean` | — |
| `side-stand-engine-cut-off` | `boolean` | — |
| `step-up-seat` | `boolean` | — |

### Exterior, Lighting & Glass
*Total Attributes: 8*

| Attribute Slug | Type | Unit / Details |
|---|:---:|---|
| `battery-capacity` | `unit` | `kilowatt-hour` |
| `battery-type` | `enum` | — |
| `headlight` | `boolean` | — |
| `led-tial-lights` | `boolean` | — |
| `low-fuel-indicator` | `boolean` | — |
| `low-oil-indicator` | `boolean` | — |
| `tail-light` | `boolean` | — |
| `turn-signal-light` | `boolean` | — |

### Infotainment, Telematics & Screens
*Total Attributes: 5*

| Attribute Slug | Type | Unit / Details |
|---|:---:|---|
| `bluetooth-connectivity` | `boolean` | — |
| `call-sms-alerts` | `boolean` | — |
| `instrument-console-type` | `string` | — |
| `navigation-gps` | `boolean` | — |
| `usb-charging-port` | `boolean` | — |
