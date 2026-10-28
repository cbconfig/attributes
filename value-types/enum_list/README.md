# Enum List / Multi-Select Attribute Type (`enum_list`)

The `enum_list` (or `multi_select`) data type represents attributes where a vehicle can simultaneously possess multiple predefined capabilities, operating modes, sensor packages, or certified standards.

---

## 1. Specification

| Property | Value | Description |
|---|---|---|
| **Type Identifier** | `enum_list` | Canonical type string in schema definitions |
| **JSON Primitive** | `array of strings` (`string[]`) | All elements must belong to the allowed `options` pool |
| **Go Type** | `[]string` | Slice of strings in Go models |
| **PostgreSQL Type** | `TEXT[]` or JSONB array | Queryable via PostgreSQL array containment operators (`@>`, `&&`) |
| **UI Filter Widget** | Multi-Select Chips / Filter Tags / Multi-Checkbox Group | Allows users to filter for vehicles matching *any* or *all* selected tags |

---

## 2. Standardized Automotive Suites

### A. `riding-modes` (2W-ICE & 2W-BEV)
- **Options**: `["Eco", "City", "Sport", "Sport+", "Track", "Rain", "Off-Road", "Custom"]`

### B. `driving-modes` (4W-ICE & 4W-BEV)
- **Options**: `["Eco", "Comfort", "Sport", "Sport Plus", "Track", "Snow", "Mud", "Sand", "Rock", "Custom / Individual"]`

### C. `adas-features`
- **Options**:
  - `AEB` (Autonomous Emergency Braking)
  - `ACC` (Adaptive Cruise Control)
  - `LKA` (Lane Keeping Assist)
  - `LDW` (Lane Departure Warning)
  - `BSM` (Blind Spot Monitoring)
  - `RCTA` (Rear Cross Traffic Alert)
  - `TSR` (Traffic Sign Recognition)
  - `HMA` (High Beam Assist)
  - `APA` (Auto Parking Assist)

### D. `charging-standards`
- **Options**: `["CCS2", "Type 2", "GB/T (DC)", "GB/T (AC)", "CHAdeMO", "NACS (Tesla)"]`

### E. `connectivity-features`
- **Options**: `["Wireless Apple CarPlay", "Wired Apple CarPlay", "Android Auto", "Bluetooth 5.0", "4G eSIM", "5G Connectivity", "OTA Updates", "Wi-Fi Hotspot"]`

---

## 3. Blueprint Schema Definition

```yaml
riding-modes:
  name: "Riding Modes"
  type: enum_list
  category: "Motor & Performance"
  filterable: true
  options:
    - "Eco"
    - "City"
    - "Sport"
    - "Rain"
    - "Track"
    - "Custom"
  description: "Available factory throttle maps and traction control profiles."

adas-features:
  name: "Advanced Driver Assistance Features"
  type: enum_list
  category: "Safety & ADAS"
  filterable: true
  options:
    - "AEB"
    - "ACC"
    - "LKA"
    - "BSM"
    - "RCTA"
    - "TSR"
  description: "Set of active autonomous safety and perception capabilities equipped."
```

---

## 4. Variant Data JSON Examples

```json
{
  "attributes": {
    "riding-modes": ["Eco", "City", "Sport", "Track"],
    "adas-features": ["AEB", "ACC", "LKA", "BSM", "RCTA"],
    "charging-standards": ["CCS2", "Type 2"],
    "connectivity-features": ["Wireless Apple CarPlay", "Android Auto", "OTA Updates", "4G eSIM"],
    "brake-assist-technologies": ["ABS", "EBD", "Cornering Brake Control (CBC)", "Hill Hold Assist"]
  }
}
```

---

## 5. UI & Filtering Behavior

- **Filter Query**:
  - Match ALL: `?adas-features=AEB,ACC&match=all`
  - Match ANY: `?riding-modes=Sport,Track&match=any`
- **Database Query Example (PostgreSQL)**:
  ```sql
  SELECT * FROM variants WHERE attributes->'adas-features' ?& array['AEB', 'ACC'];
  ```
- **UI Chip Rendering**: Displays as interactive, removable pill chips on comparison screens.
