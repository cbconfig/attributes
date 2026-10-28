# 👁️ Autonomous & Driving Assistance (ADAS)

**Pillar Slug**: `adas-driving-assist`  
**International Standards**: *SAE J3016 (Levels 0–5 Driving Automation), UNECE R157*

Perception hardware suites (LiDAR, 4D millimeter-wave radars, HD cameras), Adaptive Cruise Control, Lane Centering Assist, Autonomous Emergency Braking, Automated Valet Parking, and Navigate-on-Autopilot.

---

## 1. Domain Overview

| Metric | Value |
|---|---|
| **Canonical Pillar Slug** | `adas-driving-assist` |
| **Total Standardized Attributes** | 60 |
| **Active In Blueprints** | 4W-BEV, 4W-ICE |

---

## 2. Standardized Attributes Catalog

| Attribute Slug | Value Type | Unit / Specification | Applicable Blueprints |
|---|:---:|:---:|---|
| `adaptive-cruise-control` | `boolean` | — | 4W-ICE |
| `adas-level` | `string` | — | 4W-ICE |
| `adjustable-suspension` | `boolean` | — | 4W-BEV |
| `advanced-driver-assistance-system` | `boolean` | — | 4W-BEV |
| `air-suspension` | `boolean` | — | 4W-BEV |
| `assisted-driving-chip-arithmetic` | `boolean` | — | 4W-BEV |
| `assisted-driving-chips` | `boolean` | — | 4W-BEV |
| `autohold` | `boolean` | — | 4W-BEV |
| `automatic-lane-change-assist` | `boolean` | — | 4W-BEV |
| `automatic-parking` | `boolean` | — | 4W-BEV |
| `automatic-ramp-exit-entry` | `boolean` | — | 4W-BEV |
| `autonomous-emergency-braking-aeb` | `boolean` | — | 4W-ICE |
| `blind-spot-monitoring` | `boolean` | — | 4W-ICE |
| `center-differential-lock` | `boolean` | — | 4W-BEV |
| `crawl-control` | `boolean` | — | 4W-BEV |
| `cruise-control` | `boolean` | — | 4W-BEV |
| `driver-assistance-video` | `boolean` | — | 4W-BEV |
| `driving-assist-level` | `string` | — | 4W-BEV |
| `driving-mode-selection` | `string` | — | 4W-BEV |
| `electromagnetic-suspension` | `boolean` | — | 4W-BEV |
| `forward-collision-warning-fcw` | `boolean` | — | 4W-ICE |
| `front-axle-limited-slip-mode` | `boolean` | — | 4W-BEV |
| `front-vehicle-start-reminder` | `boolean` | — | 4W-BEV |
| `high-precision-gnss-positioning` | `boolean` | — | 4W-BEV |
| `high-precision-map` | `boolean` | — | 4W-BEV |
| `hill-descent-control` | `boolean` | — | 4W-BEV |
| `hill-start-assist` | `boolean` | — | 4W-BEV |
| `in-vehicle-camera-head-pixels` | `boolean` | — | 4W-BEV |
| `in-vehicle-intelligent-chip` | `string` | — | 4W-BEV |
| `in-vehicle-intelligent-system` | `string` | — | 4W-BEV |
| `integral-active-steering` | `boolean` | — | 4W-BEV |
| `lane-departure-warning-ldw` | `boolean` | — | 4W-ICE |
| `lane-keep-assist-lka` | `boolean` | — | 4W-ICE |
| `lidar-brand` | `string` | — | 4W-BEV |
| `low-speed-driving-warning` | `boolean` | — | 4W-BEV |
| `low-speed-four-wheel-drive` | `boolean` | — | 4W-BEV |
| `magic-carpet-suspension` | `boolean` | — | 4W-BEV |
| `maximum-forward-detection-distance` | `string` | — | 4W-BEV |
| `mobile-app-remote-control` | `boolean` | — | 4W-BEV |
| `number-of-in-vehicle-cameras` | `integer` | — | 4W-BEV |
| `number-of-lidar-lines` | `integer` | — | 4W-BEV |
| `number-of-lidar-points` | `integer` | — | 4W-BEV |
| `number-of-lidars` | `integer` | — | 4W-BEV |
| `number-of-millimeter-wave-radars` | `integer` | — | 4W-BEV |
| `number-of-surround-view-cameras` | `integer` | — | 4W-BEV |
| `number-of-ultrasonic-sensors` | `integer` | — | 4W-BEV |
| `out-of-vehicle-camera-head-pixels` | `boolean` | — | 4W-BEV |
| `parking-memory` | `boolean` | — | 4W-BEV |
| `parking-sensors` | `boolean` | — | 4W-BEV |
| `rear-axle-limited-slip-mode` | `boolean` | — | 4W-BEV |
| `rear-cross-traffic-alert-rcta` | `boolean` | — | 4W-ICE |
| `rear-driving-assist` | `boolean` | — | 4W-BEV |
| `regenerative-braking` | `boolean` | — | 4W-BEV |
| `sentinel-mode` | `boolean` | — | 4W-BEV |
| `start-stop-technology` | `boolean` | — | 4W-BEV |
| `v2x-connection` | `boolean` | — | 4W-BEV |
| `variable-steering-ratio` | `boolean` | — | 4W-BEV |
| `vehicle-system-memory` | `string` | — | 4W-BEV |
| `vehicle-system-storage` | `string` | — | 4W-BEV |
| `wading-sensor` | `boolean` | — | 4W-BEV |

---

## 3. Implementation Guidelines

- **Attribute Decoupling**: Attribute slugs describe physical metrics; units are tracked dynamically.
- **Discrete Counts**: Discrete whole-number quantities must strictly use `number-of-*` prefixes.
- **Cross-Archetype Consistency**: Any attribute shared between two-wheelers and four-wheelers maintains identical typing.
