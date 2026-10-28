# 🚗 4W-ICE (Four-Wheeler Combustion) Specification

Petrol, diesel, and hybrid passenger cars, sedans, hatchbacks, and SUVs.

---

## 1. Quick Statistics

| Metric | Value |
|---|---|
| **Archetype Identifier** | `4W-ICE` |
| **Active Pillars** | 8 |
| **Total Canonical Attributes** | 203 |

---

## 2. Pillar Summary

| # | Category Pillar | Total Attributes | Dominant Data Types |
|:---:|---|:---:|---|
| 1 | **Engine, Motor & Performance** | 18 | string (6), unit (5), enum (3) |
| 2 | **Dimensions, Body & Capacity** | 8 | unit (5), integer (2), string (1) |
| 3 | **Chassis, Suspension & Brakes** | 7 | enum (5), string (2) |
| 4 | **Safety, Security & Restraints** | 51 | boolean (46), string (5) |
| 5 | **Autonomous & Driving Assistance (ADAS)** | 8 | boolean (7), string (1) |
| 6 | **Exterior, Lighting & Glass** | 31 | boolean (27), string (2), dimension_tuple (1) |
| 7 | **Interior, Seats & Comfort** | 58 | boolean (51), string (5), unit (2) |
| 8 | **Infotainment, Telematics & Screens** | 22 | boolean (15), string (4), integer (3) |

---

## 3. Complete Attribute Inventory by Pillar

### Engine, Motor & Performance
*Total Attributes: 18*

| Attribute Slug | Type | Unit / Details |
|---|:---:|---|
| `compression-ration` | `string` | — |
| `drive-type` | `enum` | — |
| `emission-norms-compliance` | `string` | — |
| `engiene-type` | `string` | — |
| `engine-displacement` | `unit` | `cubic-centimeter` |
| `fuel-supply-system` | `unit` | `unknown` |
| `fuel-tank-capacity` | `unit` | `liter` |
| `fuel-type` | `enum` | — |
| `gear-box` | `string` | — |
| `milage` | `string` | — |
| `number-of-cylinders` | `integer` | — |
| `number-of-valves-per-cylinder` | `integer` | — |
| `power-total` | `unit` | `kilowatt` |
| `super-charge` | `boolean` | — |
| `torque-total` | `unit` | `newton-meter` |
| `transmission-type` | `enum` | — |
| `turbocharged-engine` | `boolean` | — |
| `valve-configuration` | `string` | — |

### Dimensions, Body & Capacity
*Total Attributes: 8*

| Attribute Slug | Type | Unit / Details |
|---|:---:|---|
| `boot-capacity` | `unit` | `liter` |
| `ground-clearance` | `unit` | `millimeter` |
| `height` | `unit` | `millimeter` |
| `length` | `unit` | `millimeter` |
| `number-of-doors` | `integer` | — |
| `number-of-seats` | `integer` | — |
| `wheel-base-mm` | `string` | — |
| `width` | `unit` | `millimeter` |

### Chassis, Suspension & Brakes
*Total Attributes: 7*

| Attribute Slug | Type | Unit / Details |
|---|:---:|---|
| `front-brake-type` | `enum` | — |
| `front-suspension` | `enum` | — |
| `rear-brake-type` | `enum` | — |
| `rear-suspension` | `enum` | — |
| `shock-absorbers-type` | `string` | — |
| `steering-gear-type` | `string` | — |
| `steering-type` | `enum` | — |

### Safety, Security & Restraints
*Total Attributes: 51*

| Attribute Slug | Type | Unit / Details |
|---|:---:|---|
| `adjustable-seats` | `boolean` | — |
| `anti-lock-braking-system` | `boolean` | — |
| `anti-theft-alarm` | `boolean` | — |
| `anti-theft-device` | `boolean` | — |
| `automatic-headlamps` | `string` | — |
| `bharat-ncap-safety-rating` | `string` | — |
| `blind-spot-monitor` | `boolean` | — |
| `brake-assist` | `boolean` | — |
| `camera-360-degree` | `boolean` | — |
| `central-lock` | `boolean` | — |
| `centrally-mounted-fuel-tank` | `boolean` | — |
| `check-engine-warning` | `boolean` | — |
| `child-safety-lock` | `boolean` | — |
| `clutch-lock` | `boolean` | — |
| `crash-sensor` | `boolean` | — |
| `curtain-airbags` | `boolean` | — |
| `day-and-night-view-mirror` | `boolean` | — |
| `door-ajar-warning` | `boolean` | — |
| `driver-airbag` | `boolean` | — |
| `driver-knee-airbag` | `boolean` | — |
| `electronic-brake-force-distribution` | `boolean` | — |
| `electronic-stability-control` | `boolean` | — |
| `engine-immobilizer` | `boolean` | — |
| `euro-ncap-safety-rating` | `string` | — |
| `follow-me-home-headlights` | `boolean` | — |
| `front-impact-beams` | `boolean` | — |
| `front-side-airbags` | `boolean` | — |
| `global-ncap-safety-rating` | `string` | — |
| `head-up-display` | `boolean` | — |
| `hill-assist` | `boolean` | — |
| `hill-descent-control` | `boolean` | — |
| `hill-start-assist` | `boolean` | — |
| `impact-sensing-auto-door-unlock` | `boolean` | — |
| `isofix-child-seat-anchors` | `boolean` | — |
| `knee-airbags` | `boolean` | — |
| `no-of-airbags` | `boolean` | — |
| `passenger-airbags` | `boolean` | — |
| `passenger-side-rear-view-mirror` | `boolean` | — |
| `power-door-locks` | `boolean` | — |
| `pretensioners-force-limitor-seatbelts` | `string` | — |
| `rear-camera` | `boolean` | — |
| `rear-seatbelts` | `boolean` | — |
| `seat-belt-warning` | `boolean` | — |
| `side-airbags-front` | `boolean` | — |
| `side-airbags-rear` | `boolean` | — |
| `side-impact-beams` | `boolean` | — |
| `speed-sensing-door-locks` | `boolean` | — |
| `tpms-individual-pressure-readout` | `boolean` | — |
| `traction-control` | `boolean` | — |
| `tyre-pressure-monitor` | `boolean` | — |
| `xenon-headlamps` | `boolean` | — |

### Autonomous & Driving Assistance (ADAS)
*Total Attributes: 8*

| Attribute Slug | Type | Unit / Details |
|---|:---:|---|
| `adaptive-cruise-control` | `boolean` | — |
| `adas-level` | `string` | — |
| `autonomous-emergency-braking-aeb` | `boolean` | — |
| `blind-spot-monitoring` | `boolean` | — |
| `forward-collision-warning-fcw` | `boolean` | — |
| `lane-departure-warning-ldw` | `boolean` | — |
| `lane-keep-assist-lka` | `boolean` | — |
| `rear-cross-traffic-alert-rcta` | `boolean` | — |

### Exterior, Lighting & Glass
*Total Attributes: 31*

| Attribute Slug | Type | Unit / Details |
|---|:---:|---|
| `adjustable-headlights` | `boolean` | — |
| `chrome-garnish` | `boolean` | — |
| `chrome-grille` | `boolean` | — |
| `electric-folding-rear-view-mirror` | `boolean` | — |
| `fog-light-rear` | `boolean` | — |
| `fog-lights-front` | `boolean` | — |
| `halogen-headlamps` | `boolean` | — |
| `integrated-antenna` | `boolean` | — |
| `lighting` | `boolean` | — |
| `manual-rear-view-mirror` | `boolean` | — |
| `mirror-integrated-turn-signals` | `boolean` | — |
| `panoramic-sunroof` | `boolean` | — |
| `power-antenna` | `boolean` | — |
| `power-folding-mirrors` | `boolean` | — |
| `rain-sensing-wiper` | `boolean` | — |
| `rear-spoiler` | `boolean` | — |
| `rear-window-defogger` | `boolean` | — |
| `rear-window-washer` | `boolean` | — |
| `rear-window-wiper` | `boolean` | — |
| `removable-convertible-top` | `boolean` | — |
| `roof-carrier` | `boolean` | — |
| `roof-rails` | `boolean` | — |
| `side-stepper` | `boolean` | — |
| `smoke-headlamps` | `boolean` | — |
| `sun-roof` | `boolean` | — |
| `tinted-glass` | `boolean` | — |
| `trunk-opener` | `string` | — |
| `tyre-size` | `dimension_tuple` | — |
| `tyre-type` | `string` | — |
| `wheel-covers` | `boolean` | — |
| `wheel-size` | `unit` | `inch` |

### Interior, Seats & Comfort
*Total Attributes: 58*

| Attribute Slug | Type | Unit / Details |
|---|:---:|---|
| `accessory-power-outler` | `string` | — |
| `adjustable-climate-control` | `string` | — |
| `adjustable-steering` | `string` | — |
| `air-conditioner` | `boolean` | — |
| `air-quality-control` | `boolean` | — |
| `battery-saver` | `boolean` | — |
| `central-console-armrest` | `boolean` | — |
| `cigarette-lighter` | `boolean` | — |
| `cruise-control` | `boolean` | — |
| `cup-holders-front` | `boolean` | — |
| `cup-holders-rear` | `boolean` | — |
| `digital-clock` | `boolean` | — |
| `digital-odometer` | `boolean` | — |
| `digital-tripmeter` | `boolean` | — |
| `driving-experience-control-eco` | `boolean` | — |
| `dual-dashboard-displays` | `boolean` | — |
| `electric-adjustable-seats` | `boolean` | — |
| `engine-start-stop-button` | `boolean` | — |
| `fabric-upholstery` | `boolean` | — |
| `foldable-rear-seat` | `boolean` | — |
| `folding-table-rear` | `boolean` | — |
| `gear-shift-indicator` | `boolean` | — |
| `glove-box` | `boolean` | — |
| `glove-box-cooling` | `boolean` | — |
| `gps-navigation` | `boolean` | — |
| `hands-free-tailgate` | `boolean` | — |
| `heated-seats-front` | `boolean` | — |
| `heated-seats-rear` | `boolean` | — |
| `heater` | `boolean` | — |
| `height-adjustable-driver-seat` | `boolean` | — |
| `keyless-entry` | `boolean` | — |
| `lane-change-indicator` | `boolean` | — |
| `leather-seats` | `boolean` | — |
| `leather-steering-wheel` | `boolean` | — |
| `low-fuel-warning-light` | `boolean` | — |
| `luggage-hook-and-net` | `boolean` | — |
| `outside-temperature-display` | `boolean` | — |
| `parking-sensors` | `boolean` | — |
| `power-steering` | `boolean` | — |
| `power-window-front` | `unit` | `unknown` |
| `power-window-rear` | `unit` | `unknown` |
| `rear-ac-vents` | `boolean` | — |
| `rear-curtain` | `boolean` | — |
| `rear-headrests` | `boolean` | — |
| `rear-reading-lamp` | `boolean` | — |
| `rear-seat-armrest` | `boolean` | — |
| `remote-fuel-lid-opener` | `boolean` | — |
| `remote-trunk-opener` | `boolean` | — |
| `seat-lumbar-support` | `string` | — |
| `smart-access-card-entry` | `boolean` | — |
| `steering-wheel-gearshift` | `string` | — |
| `tachometer` | `boolean` | — |
| `tailgate-ajar-warning` | `boolean` | — |
| `trunk-light` | `boolean` | — |
| `usb-charger` | `boolean` | — |
| `vanity-mirror` | `boolean` | — |
| `ventilated-seats` | `boolean` | — |
| `voice-control` | `boolean` | — |

### Infotainment, Telematics & Screens
*Total Attributes: 22*

| Attribute Slug | Type | Unit / Details |
|---|:---:|---|
| `audio-system-remote-control` | `boolean` | — |
| `bluetooth-connectivity` | `boolean` | — |
| `cd-changer` | `boolean` | — |
| `cd-player` | `boolean` | — |
| `connected-car-suite` | `string` | — |
| `connectivity` | `string` | — |
| `dvd-player` | `boolean` | — |
| `integrated-2din-audio` | `boolean` | — |
| `internal-storage` | `boolean` | — |
| `number-of-front-speakers` | `integer` | — |
| `number-of-rear-speakers` | `integer` | — |
| `number-of-speakers` | `integer` | — |
| `radio` | `boolean` | — |
| `rear-entertainment-system` | `boolean` | — |
| `sound-system-brand` | `string` | — |
| `subwoofer` | `boolean` | — |
| `touchscreen` | `boolean` | — |
| `touchscreen-size-inches` | `string` | — |
| `usb-aux-input` | `boolean` | — |
| `wireless-android-auto` | `boolean` | — |
| `wireless-apple-carplay` | `boolean` | — |
| `wireless-phone-charging` | `boolean` | — |
