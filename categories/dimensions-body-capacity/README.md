# 📐 Dimensions, Body & Capacity

**Pillar Slug**: `dimensions-body-capacity`  
**International Standards**: *ISO 3833 (Road Vehicles — Types, Terms & Definitions), DIN 70020*

Vehicle physical envelope, wheelbase, track widths, ground clearance, curb and gross weights, aerodynamic drag coefficient, seating volume, and luggage capacities.

---

## 1. Domain Overview

| Metric | Value |
|---|---|
| **Canonical Pillar Slug** | `dimensions-body-capacity` |
| **Total Standardized Attributes** | 26 |
| **Active In Blueprints** | 2W-BEV, 2W-ICE, 4W-BEV, 4W-ICE |

---

## 2. Standardized Attributes Catalog

| Attribute Slug | Value Type | Unit / Specification | Applicable Blueprints |
|---|:---:|:---:|---|
| `approach-angle` | `unit` | `degree` | 4W-BEV |
| `body-type` | `enum` | — | 4W-BEV |
| `boot-capacity` | `unit` | `liter` | 4W-BEV, 4W-ICE |
| `curb-weight` | `unit` | `kilogram` | 2W-BEV, 2W-ICE, 4W-BEV |
| `departure-angle` | `unit` | `degree` | 4W-BEV |
| `door-opening-method` | `string` | — | 4W-BEV |
| `drag-coefficient` | `unit` | `coefficient-cd` | 4W-BEV |
| `frunk-capacity` | `unit` | `liter` | 4W-BEV |
| `fuel-tank-capacity` | `unit` | `liter` | 2W-ICE, 4W-BEV |
| `gross-vehicle-weight` | `unit` | `kilogram` | 4W-BEV |
| `ground-clearance` | `unit` | `millimeter` | 2W-BEV, 2W-ICE, 4W-ICE |
| `height` | `unit` | `millimeter` | 2W-BEV, 2W-ICE, 4W-BEV, 4W-ICE |
| `length` | `unit` | `millimeter` | 2W-BEV, 2W-ICE, 4W-BEV, 4W-ICE |
| `maximum-gradability` | `string` | — | 4W-BEV |
| `maximum-load-mass` | `string` | — | 4W-BEV |
| `number-of-doors` | `integer` | — | 4W-BEV, 4W-ICE |
| `number-of-seats` | `integer` | — | 2W-BEV, 4W-BEV, 4W-ICE |
| `payload-capacity` | `unit` | `kilogram` | 2W-BEV |
| `seat-height` | `unit` | `millimeter` | 2W-BEV, 2W-ICE |
| `track-width-front` | `unit` | `millimeter` | 4W-BEV |
| `track-width-rear` | `unit` | `millimeter` | 4W-BEV |
| `under-seat-storage` | `unit` | `liter` | 2W-BEV, 2W-ICE |
| `wheel-base` | `string` | — | 2W-ICE |
| `wheel-base-mm` | `string` | — | 4W-ICE |
| `wheelbase` | `unit` | `millimeter` | 2W-BEV, 2W-ICE, 4W-BEV |
| `width` | `unit` | `millimeter` | 2W-BEV, 2W-ICE, 4W-BEV, 4W-ICE |

---

## 3. Implementation Guidelines

- **Attribute Decoupling**: Attribute slugs describe physical metrics; units are tracked dynamically.
- **Discrete Counts**: Discrete whole-number quantities must strictly use `number-of-*` prefixes.
- **Cross-Archetype Consistency**: Any attribute shared between two-wheelers and four-wheelers maintains identical typing.
