# 🛵 2W-BEV (Two-Wheeler Electric) Specification

Electric scooters, commuter e-motorcycles, and high-performance electric two-wheelers.

---

## 1. Quick Statistics

| Metric | Value |
|---|---|
| **Archetype Identifier** | `2W-BEV` |
| **Active Pillars** | 7 |
| **Total Canonical Attributes** | 90 |

---

## 2. Pillar Summary

| # | Category Pillar | Total Attributes | Dominant Data Types |
|:---:|---|:---:|---|
| 1 | **Engine, Motor & Performance** | 19 | unit (9), boolean (5), enum (2) |
| 2 | **Battery & Charging** | 19 | unit (8), string (5), enum (3) |
| 3 | **Dimensions, Body & Capacity** | 10 | unit (9), integer (1) |
| 4 | **Chassis, Suspension & Brakes** | 16 | string (7), enum (3), unit (2) |
| 5 | **Safety, Security & Restraints** | 10 | boolean (10) |
| 6 | **Exterior, Lighting & Glass** | 6 | boolean (6) |
| 7 | **Infotainment, Telematics & Screens** | 10 | boolean (6), string (3), unit (1) |

---

## 3. Complete Attribute Inventory by Pillar

### Engine, Motor & Performance
*Total Attributes: 19*

| Attribute Slug | Type | Unit / Details |
|---|:---:|---|
| `acceleration-0-40` | `unit` | `second` |
| `acceleration-0-60` | `unit` | `second` |
| `cruise-control` | `boolean` | — |
| `drive-type` | `enum` | — |
| `gradeability` | `unit` | `percent` |
| `hill-hold-assist` | `boolean` | — |
| `motor-ip-rating` | `rating` | — |
| `motor-placement` | `string` | — |
| `motor-type` | `enum` | — |
| `power-motor` | `unit` | `kilowatt` |
| `power-motor-continuous` | `unit` | `kilowatt` |
| `power-motor-peak` | `unit` | `kilowatt` |
| `reverse-mode` | `boolean` | — |
| `riding-modes` | `boolean` | — |
| `top-speed` | `unit` | `km-per-h` |
| `torque-total` | `unit` | `newton-meter` |
| `torque-wheel` | `unit` | `newton-meter` |
| `transmission` | `string` | — |
| `walk-assist` | `boolean` | — |

### Battery & Charging
*Total Attributes: 19*

| Attribute Slug | Type | Unit / Details |
|---|:---:|---|
| `battery-capacity` | `unit` | `kilowatt-hour` |
| `battery-cell-manufacturer` | `string` | — |
| `battery-chemistry` | `enum` | — |
| `battery-ip-rating` | `rating` | — |
| `battery-swapping-support` | `string` | — |
| `battery-type` | `enum` | — |
| `battery-voltage` | `unit` | `volt` |
| `battery-warranty` | `string` | — |
| `charger-type` | `enum` | — |
| `charging-port` | `string` | — |
| `charging-time-fast` | `unit` | `minute` |
| `charging-time-slow` | `unit` | `hour` |
| `dual-battery-support` | `boolean` | — |
| `portable-charger-wattage` | `string` | — |
| `range-city` | `unit` | `kilometer` |
| `range-claimed` | `unit` | `kilometer` |
| `range-extender-option` | `unit` | `unknown` |
| `range-highway` | `unit` | `kilometer` |
| `removable-battery` | `boolean` | — |

### Dimensions, Body & Capacity
*Total Attributes: 10*

| Attribute Slug | Type | Unit / Details |
|---|:---:|---|
| `curb-weight` | `unit` | `kilogram` |
| `ground-clearance` | `unit` | `millimeter` |
| `height` | `unit` | `millimeter` |
| `length` | `unit` | `millimeter` |
| `number-of-seats` | `integer` | — |
| `payload-capacity` | `unit` | `kilogram` |
| `seat-height` | `unit` | `millimeter` |
| `under-seat-storage` | `unit` | `liter` |
| `wheelbase` | `unit` | `millimeter` |
| `width` | `unit` | `millimeter` |

### Chassis, Suspension & Brakes
*Total Attributes: 16*

| Attribute Slug | Type | Unit / Details |
|---|:---:|---|
| `brake-rotor-diameter-front` | `unit` | `millimeter` |
| `brake-rotor-diameter-rear` | `unit` | `millimeter` |
| `braking-system` | `string` | — |
| `chassis-frame` | `string` | — |
| `front-brake` | `string` | — |
| `front-suspension` | `enum` | — |
| `front-tyre-size` | `dimension_tuple` | — |
| `front-wheel-size` | `string` | — |
| `rear-brake` | `string` | — |
| `rear-suspension` | `enum` | — |
| `rear-tyre-size` | `dimension_tuple` | — |
| `rear-wheel-size` | `string` | — |
| `regenerative-braking` | `boolean` | — |
| `regenerative-braking-levels` | `boolean` | — |
| `tyre-type` | `string` | — |
| `wheel-type` | `enum` | — |

### Safety, Security & Restraints
*Total Attributes: 10*

| Attribute Slug | Type | Unit / Details |
|---|:---:|---|
| `anti-lock-braking-system` | `boolean` | — |
| `anti-theft-alarm` | `boolean` | — |
| `cbs-combi-brake-system` | `boolean` | — |
| `central-locking` | `boolean` | — |
| `geo-fencing` | `boolean` | — |
| `keyless-entry` | `boolean` | — |
| `pass-switch` | `boolean` | — |
| `pillion-footrest` | `boolean` | — |
| `pillion-grabrail` | `boolean` | — |
| `side-stand-sensor` | `boolean` | — |

### Exterior, Lighting & Glass
*Total Attributes: 6*

| Attribute Slug | Type | Unit / Details |
|---|:---:|---|
| `daytime-running-lights` | `boolean` | — |
| `hazard-lights` | `boolean` | — |
| `headlight` | `boolean` | — |
| `low-battery-indicator` | `boolean` | — |
| `tail-light` | `boolean` | — |
| `turn-signal-light` | `boolean` | — |

### Infotainment, Telematics & Screens
*Total Attributes: 10*

| Attribute Slug | Type | Unit / Details |
|---|:---:|---|
| `bluetooth-connectivity` | `boolean` | — |
| `call-sms-alerts` | `boolean` | — |
| `center-screen-size` | `unit` | `inch` |
| `companion-app-telematics` | `string` | — |
| `display-type` | `string` | — |
| `instrument-console` | `string` | — |
| `mobile-app-connectivity` | `boolean` | — |
| `navigation-gps` | `boolean` | — |
| `ota-updates` | `boolean` | — |
| `usb-charging-port` | `boolean` | — |
