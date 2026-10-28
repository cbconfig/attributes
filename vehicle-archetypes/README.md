# Vehicle Archetypes & Blueprint Specifications

This guide outlines the four canonical vehicle archetypes, their technical pillar allocations, attribute distributions, and structural blueprint schemas across the Sawari Sadhan platform.

---

## 1. Executive Matrix

| Archetype | Class | Category Pillars | Attributes | Target Vehicles | Dominant Powertrain |
|---|---|:---:|:---:|---|---|
| [**`2W-BEV`**](./2w-bev/README.md) | Two-Wheeler | **7** | **90** | Electric Scooters, E-Motorcycles | Permanent Magnet BLDC / Hub Motor |
| [**`2W-ICE`**](./2w-ice/README.md) | Two-Wheeler | **6** | **77** | Petrol Motorcycles, Commuter Scooters | Single/Twin Cylinders (100cc–1200cc) |
| [**`4W-BEV`**](./4w-bev/README.md) | Four-Wheeler | **11** | **426** | Electric Sedans, SUVs, Commercial EVs | Dual/Tri-Motor AWD, 400V/800V Architecture |
| [**`4W-ICE`**](./4w-ice/README.md) | Four-Wheeler | **8** | **203** | Petrol, Diesel, Hybrid Cars & SUVs | Inline-4 / V6 / Hybrid Turbocharged |

---

## 2. Cross-Archetype Pillar Coverage

The table below indicates which pillars are active for each vehicle archetype:

| # | Automotive Pillar Slug | Display Name | 2W-BEV | 2W-ICE | 4W-BEV | 4W-ICE |
|:---:|---|---|:---:|:---:|:---:|:---:|
| 1 | `overview-basic-info` | Overview & Basic Information | — | — | ✅ (47) | — |
| 2 | `powertrain-performance` | Engine, Motor & Performance | ✅ (19) | ✅ (30) | ✅ (14) | ✅ (18) |
| 3 | `battery-charging` | Battery & Charging | ✅ (19) | — | ✅ (30) | — |
| 4 | `dimensions-body-capacity` | Dimensions, Body & Capacity | ✅ (10) | ✅ (10) | ✅ (20) | ✅ (8) |
| 5 | `chassis-suspension-brakes` | Chassis, Suspension & Brakes | ✅ (16) | ✅ (13) | ✅ (14) | ✅ (7) |
| 6 | `safety-security` | Safety, Security & Restraints | ✅ (10) | ✅ (11) | ✅ (28) | ✅ (51) |
| 7 | `adas-driving-assist` | Autonomous & Driving Assistance (ADAS) | — | — | ✅ (52) | ✅ (8) |
| 8 | `exterior-lighting-glass` | Exterior, Lighting & Glass | ✅ (6) | ✅ (8) | ✅ (42) | ✅ (31) |
| 9 | `interior-seats-comfort` | Interior, Seats & Comfort | — | — | ✅ (70) | ✅ (58) |
| 10 | `infotainment-screens-connectivity` | Infotainment, Telematics & Screens | ✅ (10) | ✅ (5) | ✅ (40) | ✅ (22) |
| 11 | `optional-packages` | Optional Packages & Accessories | — | — | ✅ (69) | — |
| **Total** | | | **90** | **77** | **426** | **203** |

---

## 3. Detailed Archetype Breakdown

### 🛵 2W-BEV — Two-Wheeler Electric
*Total Attributes: 90 across 7 Pillars*

Designed specifically for electric two-wheelers with dedicated focus on battery chemistry, range, fast-charging, motor ratings, and connected scooter telematics without automotive cabin bloat.

- **Engine, Motor & Performance** (19 attributes):
  - *Quantities (`unit`)*: `power-motor`, `power-motor-peak`, `power-motor-continuous`, `torque-total`, `torque-wheel`, `top-speed`, `acceleration-0-40`, `acceleration-0-60`, `gradeability`.
  - *Features & Flags*: `riding-modes`, `reverse-mode`, `cruise-control`, `walk-assist`, `hill-hold-assist`, `motor-ip-rating`.
- **Battery & Charging** (19 attributes):
  - *Quantities (`unit`)*: `battery-capacity`, `battery-voltage`, `charging-time`, `fast-charging-time`, `range-claimed`, `range-real-world`, `charger-output`.
  - *Categorical*: `battery-type`, `battery-chemistry`, `battery-ip-rating`, `removable-battery`, `battery-swapping`.
- **Dimensions, Body & Capacity** (10 attributes):
  - `seat-height`, `ground-clearance`, `kerb-weight`, `underseat-storage`, `wheelbase`, `length`, `width`, `height`, `carrying-capacity`, `number-of-seats`.
- **Chassis, Suspension & Brakes** (16 attributes):
  - `suspension-front`, `suspension-rear`, `brake-front`, `brake-rear`, `tire-size-front`, `tire-size-rear`, `wheel-type`, `regenerative-braking`.
- **Safety, Security & Restraints** (10 attributes):
  - `cbs` (Combined Braking System), `side-stand-sensor`, `anti-theft-alarm`, `geo-fencing`, `emergency-sos`, `fall-sensor`.
- **Exterior, Lighting & Glass** (6 attributes):
  - `headlight-type`, `tail-light-type`, `led-turn-indicators`, `drl`, `hazard-lights`.
- **Infotainment, Telematics & Screens** (10 attributes):
  - `screen-size`, `display-type`, `touchscreen`, `bluetooth-connectivity`, `navigation`, `mobile-app-connectivity`, `ota-updates`.

---

### 🏍️ 2W-ICE — Two-Wheeler Combustion
*Total Attributes: 77 across 6 Pillars*

Standardized for internal combustion engine motorcycles, scooters, and mopeds, capturing displacement, transmission clutches, fuel economy, and emission compliance.

- **Engine, Motor & Performance** (30 attributes):
  - *Quantities (`unit`)*: `displacement` (cc), `power-engine` (kW), `torque-engine` (Nm), `mileage-claimed` (km/l), `bore`, `stroke`, `compression-ratio`, `top-speed`.
  - *Counts (`integer`)*: `number-of-cylinders`, `number-of-valves-per-cylinder`, `number-of-gears`.
  - *Mechanics*: `cooling-system`, `fuel-delivery-system` (FI/Carburetor), `clutch-type`, `transmission-type`.
- **Dimensions, Body & Capacity** (10 attributes):
  - `fuel-tank-capacity` (L), `reserve-fuel-capacity`, `seat-height`, `kerb-weight`, `ground-clearance`, `wheelbase`.
- **Chassis, Suspension & Brakes** (13 attributes):
  - `frame-type`, `front-suspension`, `rear-suspension`, `front-brake-type`, `rear-brake-type`, `radial-tires`.
- **Safety, Security & Restraints** (11 attributes):
  - `abs` (Single/Dual Channel), `hazard-switch`, `pass-switch`, `side-stand-engine-cut-off`.
- **Exterior, Lighting & Glass** (8 attributes):
  - `headlamp-bulb-type`, `pillion-grabrail`, `pillion-seat`, `pillion-footrest`.
- **Infotainment, Telematics & Screens** (5 attributes):
  - `speedometer-type` (Analog/Digital), `tripmeter-type`, `fuel-gauge`, `tachometer`.

---

### ⚡ 4W-BEV — Four-Wheeler Electric
*Total Attributes: 426 across 11 Pillars*

The most comprehensive blueprint on the platform, built for modern Software-Defined Electric Vehicles (SDVs), multi-motor drivetrains, high-voltage battery packs, autonomous perception suites, and smart cockpits.

- **Overview & Basic Information** (47 attributes): Model release year, platform architecture, vehicle trim, warranty terms.
- **Engine, Motor & Performance** (14 attributes): Permanent magnet synchronous motors, asynchronous induction motors, total combined output, 0–100 km/h acceleration.
- **Battery & Charging** (30 attributes): Cell chemistry (LFP/NMC), 400V/800V silicon-carbide architecture, V2L/V2G bi-directional capability, DC peak charging curves.
- **Dimensions, Body & Capacity** (20 attributes): Length, width, height, wheelbase, drag coefficient ($C_d$), front trunk (frunk) liters, trunk capacity.
- **Chassis, Suspension & Brakes** (14 attributes): Air suspension, adaptive continuous damping control, Brembo/carbon-ceramic brakes, wheel rim sizes.
- **Safety, Security & Restraints** (28 attributes): ISOFIX anchors, crumple zones, 360° side-curtain airbags, battery fire mitigation.
- **Autonomous & Driving Assistance (ADAS)** (52 attributes): SAE Level 2+ / Level 3 autonomous suites, LiDAR, 4D millimeter-wave radars, HD cameras, navigate-on-autopilot (NOA), auto-parking.
- **Exterior, Lighting & Glass** (42 attributes): Interactive matrix LED headlamps, frameless doors, acoustic dual-pane glass, panoramic sunroof with electrochromic dimming.
- **Interior, Seats & Comfort** (70 attributes): Nappa leather upholstery, 16-way power seats, heating/ventilation/massage, fragrance dispensers, multi-zone heat pump AC.
- **Infotainment, Telematics & Screens** (40 attributes): Cockpit SoC (Qualcomm 8295 / Orin-X), 2.5K/4K OLED center display, HUD, 23-speaker Dolby Atmos audio, 5G eSIM.
- **Optional Packages & Accessories** (69 attributes): Factory sport packages, cold weather suites, bespoke aerodynamic splitters.

---

### 🚗 4W-ICE — Four-Wheeler Combustion
*Total Attributes: 203 across 8 Pillars*

Engineered for internal combustion passenger vehicles, multi-link suspension geometries, turbochargers, hybrid motor assists, and active cabin ergonomics.

- **Engine, Motor & Performance** (18 attributes): Displacement, turbocharger configuration, transmission gear ratios, paddle shifters, drive modes (Eco/Sport).
- **Dimensions, Body & Capacity** (8 attributes): Kerb weight, gross vehicle weight, seating configuration, boot liters, fuel tank size.
- **Chassis, Suspension & Brakes** (7 attributes): MacPherson front struts, multi-link rear suspension, ventilated disc brakes, EPS steering gear.
- **Safety, Security & Restraints** (51 attributes): Curtain airbags, ABS with EBD, Electronic Stability Program (ESP), hill descent control, crash test ratings.
- **Autonomous & Driving Assistance (ADAS)** (8 attributes): Adaptive Cruise Control, Lane Departure Warning, Blind Spot Detection, Rear Cross Traffic Alert.
- **Exterior, Lighting & Glass** (31 attributes): Projector LED lamps, follow-me-home headlamps, rain-sensing wipers, roof rails, shark fin antenna.
- **Interior, Seats & Comfort** (58 attributes): Automatic climate control, rear AC vents, leather-wrapped steering, cooled glove box, driver seat memory.
- **Infotainment, Telematics & Screens** (22 attributes): Touchscreen infotainment, wireless Apple CarPlay / Android Auto, digital driver display, premium audio system.

---

## 4. Blueprint Schema Contract

All attributes within the YAML blueprints strictly comply with the canonical schema definition:

```yaml
"Pillar Display Name":
  "attribute-slug":
    type: "unit"
    unit: "canonical-unit-slug"
  
  "count-slug":
    type: "integer"
    
  "feature-flag-slug":
    type: "boolean"
    
  "taxonomy-slug":
    type: "enum"
```

### Schema Guarantees
1. **Sorted Structure**: Categories strictly follow the 10-Pillar sequence; attributes within each category are sorted alphabetically (A–Z).
2. **Decoupled Units**: All numeric measurements specify canonical units (`kilowatt`, `kilowatt-hour`, `millimeter`) without embedding units into the slug name.
3. **Canonical Counts**: Count attributes uniformly use the `number-of-*` prefix.
