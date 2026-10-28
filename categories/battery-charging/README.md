# 🔋 Battery & Charging

**Pillar Slug**: `battery-charging`  
**International Standards**: *ISO 15118 (Plug & Charge), CharIN CCS, NACS, GB/T 27930*

High-voltage traction batteries, battery pack chemistry, usable capacity, thermal management, AC onboard chargers, DC ultra-fast charging curves, and bi-directional V2L/V2G.

---

## 1. Domain Overview

| Metric | Value |
|---|---|
| **Canonical Pillar Slug** | `battery-charging` |
| **Total Standardized Attributes** | 48 |
| **Active In Blueprints** | 2W-BEV, 4W-BEV |

---

## 2. Standardized Attributes Catalog

| Attribute Slug | Value Type | Unit / Specification | Applicable Blueprints |
|---|:---:|:---:|---|
| `ac-charge-port-location` | `string` | — | 4W-BEV |
| `ac-charging-power` | `unit` | `kilowatt` | 4W-BEV |
| `battery-capacity` | `unit` | `kilowatt-hour` | 2W-BEV |
| `battery-cell-maker` | `string` | — | 4W-BEV |
| `battery-cell-manufacturer` | `string` | — | 2W-BEV |
| `battery-chemistry` | `enum` | — | 2W-BEV |
| `battery-energy-density` | `unit` | `watt-hour-per-kg` | 4W-BEV |
| `battery-ip-rating` | `rating` | — | 2W-BEV |
| `battery-pack-warranty` | `string` | — | 4W-BEV |
| `battery-pre-conditioning-thermal-management` | `string` | — | 4W-BEV |
| `battery-swap-support` | `boolean` | — | 4W-BEV |
| `battery-swapping-support` | `string` | — | 2W-BEV |
| `battery-technology` | `string` | — | 4W-BEV |
| `battery-temperature-management-system` | `string` | — | 4W-BEV |
| `battery-type` | `enum` | — | 2W-BEV, 4W-BEV |
| `battery-voltage` | `unit` | `volt` | 2W-BEV |
| `battery-warranty` | `string` | — | 2W-BEV |
| `branded-charging-stations` | `boolean` | — | 4W-BEV |
| `charger-type` | `enum` | — | 2W-BEV |
| `charging-port` | `string` | — | 2W-BEV |
| `charging-port-standard` | `string` | — | 4W-BEV |
| `charging-time-fast` | `unit` | `minute` | 2W-BEV |
| `charging-time-fast-30-80` | `unit` | `minute` | 4W-BEV |
| `charging-time-slow` | `unit` | `hour` | 2W-BEV |
| `dc-charge-port-location` | `string` | — | 4W-BEV |
| `dc-charging-30-80` | `string` | — | 4W-BEV |
| `dc-charging-power` | `unit` | `kilowatt` | 4W-BEV |
| `dc-charging-volume` | `string` | — | 4W-BEV |
| `dual-battery-support` | `boolean` | — | 2W-BEV |
| `energy-consumption` | `unit` | `kwh-per-100km` | 4W-BEV |
| `fuel-consumption-cltc` | `unit` | `liters-per-100km` | 4W-BEV |
| `peak-dc-charging-rate-kw` | `string` | — | 4W-BEV |
| `portable-charger-wattage` | `string` | — | 2W-BEV |
| `range-city` | `unit` | `kilometer` | 2W-BEV |
| `range-claimed` | `unit` | `kilometer` | 2W-BEV |
| `range-cltc` | `unit` | `kilometer` | 4W-BEV |
| `range-extender-option` | `unit` | `unknown` | 2W-BEV |
| `range-highway` | `unit` | `kilometer` | 2W-BEV |
| `range-nedc` | `unit` | `kilometer` | 4W-BEV |
| `range-wltp` | `unit` | `kilometer` | 4W-BEV |
| `removable-battery` | `boolean` | — | 2W-BEV |
| `single-pedal-mode` | `boolean` | — | 4W-BEV |
| `system-voltage` | `unit` | `volt` | 4W-BEV |
| `v2l-discharge-power` | `unit` | `kilowatt` | 4W-BEV |
| `v2l-minimum-limit` | `string` | — | 4W-BEV |
| `vehicle-to-load-v2l` | `boolean` | — | 4W-BEV |
| `vehicle-to-vehicle-v2v` | `boolean` | — | 4W-BEV |
| `wltc-fuel-consumption-with-depleted-battery` | `string` | — | 4W-BEV |

---

## 3. Implementation Guidelines

- **Attribute Decoupling**: Attribute slugs describe physical metrics; units are tracked dynamically.
- **Discrete Counts**: Discrete whole-number quantities must strictly use `number-of-*` prefixes.
- **Cross-Archetype Consistency**: Any attribute shared between two-wheelers and four-wheelers maintains identical typing.
