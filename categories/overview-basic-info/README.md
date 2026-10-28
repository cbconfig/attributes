# 📋 Overview & Basic Information

**Pillar Slug**: `overview-basic-info`  
**International Standards**: *ISO 3833, Manufacturer Regulatory Filing Standards*

Foundational vehicle release metadata, platform architecture, trim levels, pricing, classification, and manufacturing attributes.

---

## 1. Domain Overview

| Metric | Value |
|---|---|
| **Canonical Pillar Slug** | `overview-basic-info` |
| **Total Standardized Attributes** | 47 |
| **Active In Blueprints** | 4W-BEV |

---

## 2. Standardized Attributes Catalog

| Attribute Slug | Value Type | Unit / Specification | Applicable Blueprints |
|---|:---:|:---:|---|
| `acceleration-0-100` | `unit` | `second` | 4W-BEV |
| `acceleration-0-50` | `unit` | `second` | 4W-BEV |
| `advanced-driver-assistance-system` | `boolean` | — | 4W-BEV |
| `air-intake-type` | `enum` | — | 4W-BEV |
| `assisted-driving-chips` | `boolean` | — | 4W-BEV |
| `battery-capacity` | `unit` | `kilowatt-hour` | 4W-BEV |
| `battery-cell-maker` | `string` | — | 4W-BEV |
| `co2-emissions` | `unit` | `gram-per-km` | 4W-BEV |
| `compression-ratio` | `unit` | `ratio` | 4W-BEV |
| `cylinder-arrangement` | `enum` | — | 4W-BEV |
| `cylinder-block-material` | `string` | — | 4W-BEV |
| `cylinder-head-material` | `string` | — | 4W-BEV |
| `dc-charging-30-80` | `string` | — | 4W-BEV |
| `drive` | `string` | — | 4W-BEV |
| `emission-standard` | `enum` | — | 4W-BEV |
| `energy-consumption` | `unit` | `kwh-per-100km` | 4W-BEV |
| `engine-layout` | `string` | — | 4W-BEV |
| `engine-model` | `string` | — | 4W-BEV |
| `engine-thermal-efficiency` | `unit` | `percent` | 4W-BEV |
| `first-owner-warranty-period` | `string` | — | 4W-BEV |
| `fuel-consumption-nedc` | `unit` | `liters-per-100km` | 4W-BEV |
| `fuel-consumption-wltp` | `unit` | `liters-per-100km` | 4W-BEV |
| `fuel-grade` | `unit` | `unknown` | 4W-BEV |
| `fuel-type` | `enum` | — | 4W-BEV |
| `ice` | `string` | — | 4W-BEV |
| `ice-fuel-type` | `string` | — | 4W-BEV |
| `ice-technology` | `boolean` | — | 4W-BEV |
| `l-w-h` | `string` | — | 4W-BEV |
| `lubrication-method` | `string` | — | 4W-BEV |
| `manufacturer` | `string` | — | 4W-BEV |
| `msrp-at-launch` | `string` | — | 4W-BEV |
| `number-of-cylinders` | `integer` | — | 4W-BEV |
| `number-of-lidars` | `integer` | — | 4W-BEV |
| `number-of-valves-per-cylinder` | `integer` | — | 4W-BEV |
| `platform` | `string` | — | 4W-BEV |
| `power-engine` | `unit` | `kilowatt` | 4W-BEV |
| `power-rpm` | `unit` | `rpm` | 4W-BEV |
| `power-total` | `unit` | `kilowatt` | 4W-BEV |
| `range-cltc` | `unit` | `kilometer` | 4W-BEV |
| `range-nedc` | `unit` | `kilometer` | 4W-BEV |
| `released` | `string` | — | 4W-BEV |
| `top-speed` | `unit` | `km-per-h` | 4W-BEV |
| `torque-engine` | `unit` | `newton-meter` | 4W-BEV |
| `torque-motor-peak` | `unit` | `newton-meter` | 4W-BEV |
| `torque-rpm` | `unit` | `rpm` | 4W-BEV |
| `torque-total` | `unit` | `newton-meter` | 4W-BEV |
| `valve-mechanism` | `string` | — | 4W-BEV |

---

## 3. Implementation Guidelines

- **Attribute Decoupling**: Attribute slugs describe physical metrics; units are tracked dynamically.
- **Discrete Counts**: Discrete whole-number quantities must strictly use `number-of-*` prefixes.
- **Cross-Archetype Consistency**: Any attribute shared between two-wheelers and four-wheelers maintains identical typing.
