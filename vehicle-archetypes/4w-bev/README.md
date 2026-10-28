# ⚡ 4W-BEV (Four-Wheeler Electric) Specification

Modern Software-Defined Vehicles (SDVs), electric sedans, SUVs, and commercial EVs.

---

## 1. Quick Statistics

| Metric | Value |
|---|---|
| **Archetype Identifier** | `4W-BEV` |
| **Active Pillars** | 11 |
| **Total Canonical Attributes** | 426 |

---

## 2. Pillar Summary

| # | Category Pillar | Total Attributes | Dominant Data Types |
|:---:|---|:---:|---|
| 1 | **Overview & Basic Information** | 47 | unit (20), string (17), enum (4) |
| 2 | **Engine, Motor & Performance** | 14 | unit (7), string (3), enum (2) |
| 3 | **Battery & Charging** | 30 | string (13), unit (11), boolean (5) |
| 4 | **Dimensions, Body & Capacity** | 20 | unit (14), string (3), integer (2) |
| 5 | **Chassis, Suspension & Brakes** | 14 | enum (7), string (3), dimension_tuple (2) |
| 6 | **Safety, Security & Restraints** | 28 | boolean (28) |
| 7 | **Autonomous & Driving Assistance (ADAS)** | 52 | boolean (37), string (8), integer (7) |
| 8 | **Exterior, Lighting & Glass** | 42 | boolean (40), unit (1), enum (1) |
| 9 | **Interior, Seats & Comfort** | 70 | boolean (44), string (20), unit (5) |
| 10 | **Infotainment, Telematics & Screens** | 40 | boolean (28), string (7), unit (3) |
| 11 | **Optional Packages & Accessories** | 69 | boolean (47), string (22) |

---

## 3. Complete Attribute Inventory by Pillar

### Overview & Basic Information
*Total Attributes: 47*

| Attribute Slug | Type | Unit / Details |
|---|:---:|---|
| `acceleration-0-100` | `unit` | `second` |
| `acceleration-0-50` | `unit` | `second` |
| `advanced-driver-assistance-system` | `boolean` | — |
| `air-intake-type` | `enum` | — |
| `assisted-driving-chips` | `boolean` | — |
| `battery-capacity` | `unit` | `kilowatt-hour` |
| `battery-cell-maker` | `string` | — |
| `co2-emissions` | `unit` | `gram-per-km` |
| `compression-ratio` | `unit` | `ratio` |
| `cylinder-arrangement` | `enum` | — |
| `cylinder-block-material` | `string` | — |
| `cylinder-head-material` | `string` | — |
| `dc-charging-30-80` | `string` | — |
| `drive` | `string` | — |
| `emission-standard` | `enum` | — |
| `energy-consumption` | `unit` | `kwh-per-100km` |
| `engine-layout` | `string` | — |
| `engine-model` | `string` | — |
| `engine-thermal-efficiency` | `unit` | `percent` |
| `first-owner-warranty-period` | `string` | — |
| `fuel-consumption-nedc` | `unit` | `liters-per-100km` |
| `fuel-consumption-wltp` | `unit` | `liters-per-100km` |
| `fuel-grade` | `unit` | `unknown` |
| `fuel-type` | `enum` | — |
| `ice` | `string` | — |
| `ice-fuel-type` | `string` | — |
| `ice-technology` | `boolean` | — |
| `l-w-h` | `string` | — |
| `lubrication-method` | `string` | — |
| `manufacturer` | `string` | — |
| `msrp-at-launch` | `string` | — |
| `number-of-cylinders` | `integer` | — |
| `number-of-lidars` | `integer` | — |
| `number-of-valves-per-cylinder` | `integer` | — |
| `platform` | `string` | — |
| `power-engine` | `unit` | `kilowatt` |
| `power-rpm` | `unit` | `rpm` |
| `power-total` | `unit` | `kilowatt` |
| `range-cltc` | `unit` | `kilometer` |
| `range-nedc` | `unit` | `kilometer` |
| `released` | `string` | — |
| `top-speed` | `unit` | `km-per-h` |
| `torque-engine` | `unit` | `newton-meter` |
| `torque-motor-peak` | `unit` | `newton-meter` |
| `torque-rpm` | `unit` | `rpm` |
| `torque-total` | `unit` | `newton-meter` |
| `valve-mechanism` | `string` | — |

### Engine, Motor & Performance
*Total Attributes: 14*

| Attribute Slug | Type | Unit / Details |
|---|:---:|---|
| `drive-type` | `enum` | — |
| `electric-motor-type` | `string` | — |
| `number-of-gears` | `integer` | — |
| `number-of-motors` | `integer` | — |
| `operating-efficiency` | `string` | — |
| `power-motor-front` | `unit` | `kilowatt` |
| `power-motor-peak` | `unit` | `kilowatt` |
| `power-motor-rear` | `unit` | `kilowatt` |
| `power-total` | `unit` | `kilowatt` |
| `torque-motor-front` | `unit` | `newton-meter` |
| `torque-motor-rear` | `unit` | `newton-meter` |
| `torque-total` | `unit` | `newton-meter` |
| `transmission-description` | `string` | — |
| `transmission-type` | `enum` | — |

### Battery & Charging
*Total Attributes: 30*

| Attribute Slug | Type | Unit / Details |
|---|:---:|---|
| `ac-charge-port-location` | `string` | — |
| `ac-charging-power` | `unit` | `kilowatt` |
| `battery-cell-maker` | `string` | — |
| `battery-energy-density` | `unit` | `watt-hour-per-kg` |
| `battery-pack-warranty` | `string` | — |
| `battery-pre-conditioning-thermal-management` | `string` | — |
| `battery-swap-support` | `boolean` | — |
| `battery-technology` | `string` | — |
| `battery-temperature-management-system` | `string` | — |
| `battery-type` | `enum` | — |
| `branded-charging-stations` | `boolean` | — |
| `charging-port-standard` | `string` | — |
| `charging-time-fast-30-80` | `unit` | `minute` |
| `dc-charge-port-location` | `string` | — |
| `dc-charging-30-80` | `string` | — |
| `dc-charging-power` | `unit` | `kilowatt` |
| `dc-charging-volume` | `string` | — |
| `energy-consumption` | `unit` | `kwh-per-100km` |
| `fuel-consumption-cltc` | `unit` | `liters-per-100km` |
| `peak-dc-charging-rate-kw` | `string` | — |
| `range-cltc` | `unit` | `kilometer` |
| `range-nedc` | `unit` | `kilometer` |
| `range-wltp` | `unit` | `kilometer` |
| `single-pedal-mode` | `boolean` | — |
| `system-voltage` | `unit` | `volt` |
| `v2l-discharge-power` | `unit` | `kilowatt` |
| `v2l-minimum-limit` | `string` | — |
| `vehicle-to-load-v2l` | `boolean` | — |
| `vehicle-to-vehicle-v2v` | `boolean` | — |
| `wltc-fuel-consumption-with-depleted-battery` | `string` | — |

### Dimensions, Body & Capacity
*Total Attributes: 20*

| Attribute Slug | Type | Unit / Details |
|---|:---:|---|
| `approach-angle` | `unit` | `degree` |
| `body-type` | `enum` | — |
| `boot-capacity` | `unit` | `liter` |
| `curb-weight` | `unit` | `kilogram` |
| `departure-angle` | `unit` | `degree` |
| `door-opening-method` | `string` | — |
| `drag-coefficient` | `unit` | `coefficient-cd` |
| `frunk-capacity` | `unit` | `liter` |
| `fuel-tank-capacity` | `unit` | `liter` |
| `gross-vehicle-weight` | `unit` | `kilogram` |
| `height` | `unit` | `millimeter` |
| `length` | `unit` | `millimeter` |
| `maximum-gradability` | `string` | — |
| `maximum-load-mass` | `string` | — |
| `number-of-doors` | `integer` | — |
| `number-of-seats` | `integer` | — |
| `track-width-front` | `unit` | `millimeter` |
| `track-width-rear` | `unit` | `millimeter` |
| `wheelbase` | `unit` | `millimeter` |
| `width` | `unit` | `millimeter` |

### Chassis, Suspension & Brakes
*Total Attributes: 14*

| Attribute Slug | Type | Unit / Details |
|---|:---:|---|
| `4wd-type` | `enum` | — |
| `car-body-structure` | `string` | — |
| `center-differential-structure` | `string` | — |
| `drive` | `string` | — |
| `front-brake-type` | `enum` | — |
| `front-suspension` | `enum` | — |
| `front-tire-size` | `dimension_tuple` | — |
| `parking-brake-type` | `enum` | — |
| `rear-brake-type` | `enum` | — |
| `rear-suspension` | `enum` | — |
| `rear-tire-size` | `dimension_tuple` | — |
| `spare-tire-placement` | `boolean` | — |
| `spare-tire-specification` | `boolean` | — |
| `steering-type` | `enum` | — |

### Safety, Security & Restraints
*Total Attributes: 28*

| Attribute Slug | Type | Unit / Details |
|---|:---:|---|
| `active-brake` | `boolean` | — |
| `active-safety-warning-system` | `boolean` | — |
| `anti-lock-braking-system` | `boolean` | — |
| `blind-spot-monitoring` | `boolean` | — |
| `brake-assist` | `boolean` | — |
| `central-airbag` | `boolean` | — |
| `driver-monitoring-system` | `boolean` | — |
| `electronic-brake-force-distribution` | `boolean` | — |
| `electronic-stability-control` | `boolean` | — |
| `fatigue-driving-alert` | `boolean` | — |
| `front-airbags` | `boolean` | — |
| `front-knee-airbags` | `boolean` | — |
| `isofix-child-seat-anchors` | `boolean` | — |
| `lane-centering` | `boolean` | — |
| `lane-keeping-assist` | `boolean` | — |
| `night-vision-system` | `boolean` | — |
| `occupant-detection-reminder` | `boolean` | — |
| `passenger-seat-cushion-airbag` | `boolean` | — |
| `passive-pedestrian-protection` | `boolean` | — |
| `positive-rear-airbags` | `boolean` | — |
| `safety-tire` | `boolean` | — |
| `seat-belt-reminder` | `boolean` | — |
| `side-airbag` | `boolean` | — |
| `side-curtain-airbags` | `boolean` | — |
| `tire-pressure-monitoring-system` | `boolean` | — |
| `traction-control` | `boolean` | — |
| `traffic-lights-recognition` | `boolean` | — |
| `traffic-sign-recognition` | `boolean` | — |

### Autonomous & Driving Assistance (ADAS)
*Total Attributes: 52*

| Attribute Slug | Type | Unit / Details |
|---|:---:|---|
| `adjustable-suspension` | `boolean` | — |
| `advanced-driver-assistance-system` | `boolean` | — |
| `air-suspension` | `boolean` | — |
| `assisted-driving-chip-arithmetic` | `boolean` | — |
| `assisted-driving-chips` | `boolean` | — |
| `autohold` | `boolean` | — |
| `automatic-lane-change-assist` | `boolean` | — |
| `automatic-parking` | `boolean` | — |
| `automatic-ramp-exit-entry` | `boolean` | — |
| `center-differential-lock` | `boolean` | — |
| `crawl-control` | `boolean` | — |
| `cruise-control` | `boolean` | — |
| `driver-assistance-video` | `boolean` | — |
| `driving-assist-level` | `string` | — |
| `driving-mode-selection` | `string` | — |
| `electromagnetic-suspension` | `boolean` | — |
| `front-axle-limited-slip-mode` | `boolean` | — |
| `front-vehicle-start-reminder` | `boolean` | — |
| `high-precision-gnss-positioning` | `boolean` | — |
| `high-precision-map` | `boolean` | — |
| `hill-descent-control` | `boolean` | — |
| `hill-start-assist` | `boolean` | — |
| `in-vehicle-camera-head-pixels` | `boolean` | — |
| `in-vehicle-intelligent-chip` | `string` | — |
| `in-vehicle-intelligent-system` | `string` | — |
| `integral-active-steering` | `boolean` | — |
| `lidar-brand` | `string` | — |
| `low-speed-driving-warning` | `boolean` | — |
| `low-speed-four-wheel-drive` | `boolean` | — |
| `magic-carpet-suspension` | `boolean` | — |
| `maximum-forward-detection-distance` | `string` | — |
| `mobile-app-remote-control` | `boolean` | — |
| `number-of-in-vehicle-cameras` | `integer` | — |
| `number-of-lidar-lines` | `integer` | — |
| `number-of-lidar-points` | `integer` | — |
| `number-of-lidars` | `integer` | — |
| `number-of-millimeter-wave-radars` | `integer` | — |
| `number-of-surround-view-cameras` | `integer` | — |
| `number-of-ultrasonic-sensors` | `integer` | — |
| `out-of-vehicle-camera-head-pixels` | `boolean` | — |
| `parking-memory` | `boolean` | — |
| `parking-sensors` | `boolean` | — |
| `rear-axle-limited-slip-mode` | `boolean` | — |
| `rear-driving-assist` | `boolean` | — |
| `regenerative-braking` | `boolean` | — |
| `sentinel-mode` | `boolean` | — |
| `start-stop-technology` | `boolean` | — |
| `v2x-connection` | `boolean` | — |
| `variable-steering-ratio` | `boolean` | — |
| `vehicle-system-memory` | `string` | — |
| `vehicle-system-storage` | `string` | — |
| `wading-sensor` | `boolean` | — |

### Exterior, Lighting & Glass
*Total Attributes: 42*

| Attribute Slug | Type | Unit / Details |
|---|:---:|---|
| `acoustic-glass` | `boolean` | — |
| `active-ambient-lighting` | `boolean` | — |
| `active-grille-shutter` | `boolean` | — |
| `adaptive-frontlighting-system` | `boolean` | — |
| `adaptive-high-low-beams` | `boolean` | — |
| `alloy-wheels` | `boolean` | — |
| `anti-pinch-power-windows` | `boolean` | — |
| `auto-dimming-rear-view-mirror` | `boolean` | — |
| `automatic-headlights` | `boolean` | — |
| `car-cosmetic-mirror` | `boolean` | — |
| `car-interior-sunshade` | `boolean` | — |
| `daytime-running-lights` | `boolean` | — |
| `delayed-headlights-turn-off` | `boolean` | — |
| `door-slides` | `boolean` | — |
| `frameless-doors` | `boolean` | — |
| `front-fog-lights` | `boolean` | — |
| `front-windshield-heater` | `boolean` | — |
| `headlamps-with-steering` | `boolean` | — |
| `headlight-rain-and-fog-mode` | `boolean` | — |
| `headlight-washers` | `boolean` | — |
| `headlights-features` | `boolean` | — |
| `headlights-height-adjustment` | `boolean` | — |
| `heated-water-nozzles` | `boolean` | — |
| `hidden-door-handles` | `boolean` | — |
| `high-beam-headlights` | `boolean` | — |
| `interior-ambient-lighting` | `boolean` | — |
| `light-sensitive-canopy` | `boolean` | — |
| `low-beam-headlights` | `boolean` | — |
| `motorized-spoiler` | `boolean` | — |
| `one-touch-power-windows` | `boolean` | — |
| `power-folding-mirrors` | `boolean` | — |
| `power-window` | `unit` | `unknown` |
| `rain-sensor` | `boolean` | — |
| `rear-tinted-glass` | `boolean` | — |
| `rear-window-opening` | `boolean` | — |
| `rear-wiper` | `boolean` | — |
| `roof-rack` | `boolean` | — |
| `side-footrests` | `boolean` | — |
| `sliding-door` | `boolean` | — |
| `sport-appearance-package` | `boolean` | — |
| `sunroof-type` | `enum` | — |
| `trailer-hitch` | `boolean` | — |

### Interior, Seats & Comfort
*Total Attributes: 70*

| Attribute Slug | Type | Unit / Details |
|---|:---:|---|
| `a-c-control-method` | `enum` | — |
| `ac-power-outlet-220v` | `boolean` | — |
| `active-noise-reduction` | `boolean` | — |
| `air-purifier` | `boolean` | — |
| `ar-hud` | `boolean` | — |
| `boss-key` | `boolean` | — |
| `built-in-dvr` | `boolean` | — |
| `captain-chairs-in-the-second-row` | `boolean` | — |
| `car-fragnance-diffuser` | `boolean` | — |
| `car-refrigerator` | `boolean` | — |
| `car-screen` | `string` | — |
| `center-screen-pixel-density` | `unit` | `ppi` |
| `center-screen-size` | `unit` | `inch` |
| `central-locking` | `boolean` | — |
| `climate-control` | `boolean` | — |
| `engine-immobilizer` | `boolean` | — |
| `etc` | `string` | — |
| `foldable-front-seats` | `boolean` | — |
| `front-rear-armrest` | `boolean` | — |
| `front-seat-function` | `string` | — |
| `head-up-display` | `boolean` | — |
| `heat-pump-system` | `boolean` | — |
| `heated-cooled-cup-holders` | `boolean` | — |
| `hepa-filter` | `boolean` | — |
| `hud-projection-size` | `string` | — |
| `in-car-pm25-filter` | `boolean` | — |
| `inductive-power-tailgate` | `boolean` | — |
| `instrument-cluster-pixel-density` | `unit` | `ppi` |
| `instrument-cluster-styles` | `string` | — |
| `integral-adjustment-of-the-main-drivers-seat` | `string` | — |
| `integral-adjustment-of-the-second-row-of-seats` | `string` | — |
| `keyless-entry` | `boolean` | — |
| `keyless-start` | `boolean` | — |
| `lcd-instrument-panel` | `string` | — |
| `negative-ion-generator` | `boolean` | — |
| `partial-adjustment-of-the-main-drivers-seat` | `string` | — |
| `partial-adjustment-of-the-passenger-seat` | `string` | — |
| `passenger-seat-overall-adjustment` | `string` | — |
| `power-door-handles` | `boolean` | — |
| `power-door-suction` | `boolean` | — |
| `power-seat-adjustments` | `unit` | `unknown` |
| `power-tailgate` | `boolean` | — |
| `power-tailgate-memory` | `boolean` | — |
| `rear-a-c-control` | `boolean` | — |
| `rear-air-vents` | `boolean` | — |
| `rear-cup-holders` | `boolean` | — |
| `rear-seat-folding-ratio` | `string` | — |
| `rear-seat-power-folding` | `boolean` | — |
| `remote-car-start` | `boolean` | — |
| `remote-key-type` | `string` | — |
| `rotatable-screen` | `boolean` | — |
| `screen-resolution` | `string` | — |
| `seat-layout` | `string` | — |
| `seat-leather` | `string` | — |
| `seats-material` | `string` | — |
| `second-row-screen` | `boolean` | — |
| `second-row-seat-adjustment` | `boolean` | — |
| `second-row-tables` | `boolean` | — |
| `sport-seats` | `boolean` | — |
| `steering-wheel-adjustment` | `string` | — |
| `steering-wheel-functions` | `string` | — |
| `steering-wheel-material` | `string` | — |
| `steering-wheel-power-adjustment` | `boolean` | — |
| `third-row` | `boolean` | — |
| `third-row-seat-adjustment` | `boolean` | — |
| `trunk-12v-power-outlet` | `boolean` | — |
| `vehicle-remote-control` | `boolean` | — |
| `vehicle-summon` | `boolean` | — |
| `wireless-charging-power` | `unit` | `watt` |
| `wireless-phone-charging` | `boolean` | — |

### Infotainment, Telematics & Screens
*Total Attributes: 40*

| Attribute Slug | Type | Unit / Details |
|---|:---:|---|
| `4g-5g-networks` | `string` | — |
| `acoustic-brand` | `string` | — |
| `active-noise-cancellation` | `boolean` | — |
| `app-store` | `boolean` | — |
| `ar-live-navigation` | `boolean` | — |
| `audiovisual-system` | `boolean` | — |
| `bluetooth-car-calls` | `boolean` | — |
| `car-tv` | `boolean` | — |
| `center-console-color-screen-resolution` | `string` | — |
| `co-pilot-screen-resolution` | `string` | — |
| `continuous-speech-recognition` | `boolean` | — |
| `emotion-recognition` | `boolean` | — |
| `facial-recognition` | `boolean` | — |
| `fingerprint-recognition` | `boolean` | — |
| `geo-fencing` | `boolean` | — |
| `gesture-control` | `boolean` | — |
| `gps-navigation` | `boolean` | — |
| `in-car-karaoke` | `boolean` | — |
| `lower-center-screen-size` | `string` | — |
| `media-easter-egg` | `boolean` | — |
| `mobile-connected-mapping` | `string` | — |
| `multi-finger-screen-control` | `boolean` | — |
| `multimedia-interface` | `string` | — |
| `number-of-speakers` | `integer` | — |
| `number-of-usb-ports` | `integer` | — |
| `on-road-assistance` | `boolean` | — |
| `ota-upgrade` | `boolean` | — |
| `ota-version` | `boolean` | — |
| `passenger-screen-pixel-density` | `unit` | `ppi` |
| `passenger-screen-size` | `unit` | `inch` |
| `real-time-navigation` | `boolean` | — |
| `rear-multimedia-controls` | `boolean` | — |
| `relax-mode` | `boolean` | — |
| `smart-voice-interaction` | `boolean` | — |
| `telematics-system` | `boolean` | — |
| `touch-screen-vibration-feedback` | `boolean` | — |
| `usb-charging-power` | `unit` | `watt` |
| `voice-activation-wake-word` | `boolean` | — |
| `voice-recognition` | `boolean` | — |
| `wi-fi-hotspot` | `boolean` | — |

### Optional Packages & Accessories
*Total Attributes: 69*

| Attribute Slug | Type | Unit / Details |
|---|:---:|---|
| `23-jan-deluxe-audio-package` | `string` | — |
| `active-rear-spoiler` | `boolean` | — |
| `adaptive-rotation-hover-pad` | `boolean` | — |
| `adas-advanced-package` | `boolean` | — |
| `aics-intelligent-cockpit` | `boolean` | — |
| `all-in-one-smart-driving-package` | `string` | — |
| `all-terrain-tire-at` | `string` | — |
| `ar-navigation` | `boolean` | — |
| `augmented-reality-navigation` | `boolean` | — |
| `automated-parking-assist` | `boolean` | — |
| `biometric-vein-recognition-unlock` | `boolean` | — |
| `business-suite-1` | `string` | — |
| `business-suite-2` | `string` | — |
| `cabin-comfort-package` | `boolean` | — |
| `cabin-luxury-package` | `boolean` | — |
| `comfort-option-package-1` | `string` | — |
| `comfort-set` | `boolean` | — |
| `comfort-tailgate-package` | `boolean` | — |
| `commemorative-edition-badge` | `boolean` | — |
| `customized-options` | `string` | — |
| `darth-vader-special` | `boolean` | — |
| `deluxe-cabin-set` | `string` | — |
| `deluxe-comfort-package` | `string` | — |
| `deluxe-package` | `boolean` | — |
| `dual-screen-linkage` | `boolean` | — |
| `entertainment-kit` | `string` | — |
| `exclusive-edition-styling-package` | `boolean` | — |
| `exterior-carbon-fiber-package` | `boolean` | — |
| `four-seater` | `boolean` | — |
| `full-vehicle-warranty` | `string` | — |
| `heat-pump-air-conditioning-package` | `boolean` | — |
| `heatwave-crimson-appearance-kit` | `boolean` | — |
| `ibcm-sensorless-start` | `boolean` | — |
| `imaging-radar-4d` | `boolean` | — |
| `intelligent-driving-system` | `boolean` | — |
| `intelligent-lighting-kit` | `boolean` | — |
| `intelligent-technology-package` | `boolean` | — |
| `intelligent-winter-kit` | `boolean` | — |
| `interior-carbon-fiber-package` | `boolean` | — |
| `lfp-battery-system` | `boolean` | — |
| `luxury-option-packages` | `string` | — |
| `massage-seats` | `boolean` | — |
| `nfs-sensorless-smart-start` | `boolean` | — |
| `option-package-1` | `string` | — |
| `option-package-i` | `string` | — |
| `option-package-ii` | `string` | — |
| `option-package-iii` | `string` | — |
| `option-package-v` | `string` | — |
| `outdoor-leisure-bag` | `boolean` | — |
| `over-view-summoning-parking` | `boolean` | — |
| `panoramic-ar-instrument-display` | `boolean` | — |
| `performance-wheel-package-20-inch` | `boolean` | — |
| `pro-premium-option-package` | `string` | — |
| `r-pilot-smart-driver-growth-pack` | `boolean` | — |
| `remote-control` | `boolean` | — |
| `rising-bach-cabin-ambience-upgrade-package` | `string` | — |
| `rising-bach-cockpit-seat-upgrade-package` | `string` | — |
| `say-hi` | `string` | — |
| `semi-aniline-leather-package` | `boolean` | — |
| `smart-etc` | `boolean` | — |
| `solar-roof-charging` | `boolean` | — |
| `technology-package` | `boolean` | — |
| `torque-vectoring-control` | `boolean` | — |
| `transparent-chassis-180` | `boolean` | — |
| `transparent-chassis-540` | `boolean` | — |
| `travelers-kit` | `boolean` | — |
| `ultra-visual-intelligent-interaction-package` | `string` | — |
| `value-upgrade-package` | `boolean` | — |
| `welcome-light-animation` | `boolean` | — |
