# 🛞 Chassis, Suspension & Brakes

**Pillar Slug**: `chassis-suspension-brakes`  
**International Standards**: *Federal Motor Vehicle Safety Standards (FMVSS), ECE R13-H*

Chassis frame geometry, front/rear suspension architectures (MacPherson, multi-link, air suspension), braking mechanisms (ventilated discs, ABS/EBD), steering ratios, and tire/wheel specifications.

---

## 1. Domain Overview

| Metric | Value |
|---|---|
| **Canonical Pillar Slug** | `chassis-suspension-brakes` |
| **Total Standardized Attributes** | 36 |
| **Active In Blueprints** | 2W-BEV, 2W-ICE, 4W-BEV, 4W-ICE |

---

## 2. Standardized Attributes Catalog

| Attribute Slug | Value Type | Unit / Specification | Applicable Blueprints |
|---|:---:|:---:|---|
| `4wd-type` | `enum` | — | 4W-BEV |
| `body-graphics` | `boolean` | — | 2W-ICE |
| `body-type` | `enum` | — | 2W-ICE |
| `brake-rotor-diameter-front` | `unit` | `millimeter` | 2W-BEV, 2W-ICE |
| `brake-rotor-diameter-rear` | `unit` | `millimeter` | 2W-BEV |
| `braking-system` | `string` | — | 2W-BEV |
| `car-body-structure` | `string` | — | 4W-BEV |
| `center-differential-structure` | `string` | — | 4W-BEV |
| `chasis` | `string` | — | 2W-ICE |
| `chassis-frame` | `string` | — | 2W-BEV |
| `drive` | `string` | — | 4W-BEV |
| `front-brake` | `string` | — | 2W-BEV, 2W-ICE |
| `front-brake-type` | `enum` | — | 4W-BEV, 4W-ICE |
| `front-suspension` | `enum` | — | 2W-BEV, 2W-ICE, 4W-BEV, 4W-ICE |
| `front-tire-size` | `dimension_tuple` | — | 4W-BEV |
| `front-tyre-size` | `dimension_tuple` | — | 2W-BEV |
| `front-wheel-size` | `string` | — | 2W-BEV |
| `parking-brake-type` | `enum` | — | 4W-BEV |
| `rear-brake` | `string` | — | 2W-BEV, 2W-ICE |
| `rear-brake-type` | `enum` | — | 4W-BEV, 4W-ICE |
| `rear-suspension` | `enum` | — | 2W-BEV, 2W-ICE, 4W-BEV, 4W-ICE |
| `rear-tire-size` | `dimension_tuple` | — | 4W-BEV |
| `rear-tyre-size` | `dimension_tuple` | — | 2W-BEV |
| `rear-wheel-size` | `string` | — | 2W-BEV |
| `regenerative-braking` | `boolean` | — | 2W-BEV |
| `regenerative-braking-levels` | `boolean` | — | 2W-BEV |
| `shock-absorbers-type` | `string` | — | 4W-ICE |
| `spare-tire-placement` | `boolean` | — | 4W-BEV |
| `spare-tire-specification` | `boolean` | — | 4W-BEV |
| `steering-gear-type` | `string` | — | 4W-ICE |
| `steering-type` | `enum` | — | 4W-BEV, 4W-ICE |
| `tyre-size` | `dimension_tuple` | — | 2W-ICE |
| `tyre-type` | `string` | — | 2W-BEV, 2W-ICE |
| `wheel-diameter` | `unit` | `inch` | 2W-ICE |
| `wheel-size` | `unit` | `inch` | 2W-ICE |
| `wheel-type` | `enum` | — | 2W-BEV, 2W-ICE |

---

## 3. Implementation Guidelines

- **Attribute Decoupling**: Attribute slugs describe physical metrics; units are tracked dynamically.
- **Discrete Counts**: Discrete whole-number quantities must strictly use `number-of-*` prefixes.
- **Cross-Archetype Consistency**: Any attribute shared between two-wheelers and four-wheelers maintains identical typing.
