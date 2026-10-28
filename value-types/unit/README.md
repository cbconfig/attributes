# Unit / Quantity Attribute Type (`unit`)

The `unit` data type represents physical measurements with engineering dimensions (e.g. power, torque, energy, dimensions, mass, velocity). It supports sorting, range filtering, and localized unit conversion.

---

## 1. Specification

| Property | Value | Description |
|---|---|---|
| **Type Identifier** | `unit` | Canonical type string in schema definitions |
| **JSON Representation** | `{"value": number, "unit": string}` or scalar with blueprint metadata | Standardized measurement structure |
| **Go Type** | `struct { Value float64; Unit string }` | Structured unit measurement in Go models |
| **PostgreSQL Type** | `NUMERIC(10,2)` (normalized to canonical SI) | Stored normalized in database for indexing and range searches |
| **Canonical Units** | `kW` (power), `Nm` (torque), `kWh` (battery), `mm` (dimensions), `kg` (mass) | System standard units |
| **UI Filter Widget** | Dual-ended Range Slider / Min & Max Numeric Inputs | Allows users to filter vehicles within specific intervals |

---

## 2. Measurement Categories & Standard Units

| Category | Primary Metric Unit | Secondary / Regional Unit | Slugs Example |
|---|---|---|---|
| **Power** | `kW` | `bhp`, `hp`, `ps` | `motor-power`, `peak-power`, `max-power-bhp` |
| **Torque** | `Nm` | `lb-ft` | `max-torque`, `wheel-torque` |
| **Battery Energy** | `kWh` | `Ah` | `battery-capacity`, `usable-battery-capacity` |
| **Engine Displacement** | `cc` | `L` (litres) | `engine-displacement`, `displacement` |
| **Dimensions** | `mm` | `cm`, `inches` | `length`, `width`, `height`, `wheelbase`, `ground-clearance` |
| **Volume / Capacity** | `L` (litres) | `cu ft` | `boot-space`, `fuel-tank-capacity`, `frunk-capacity` |
| **Mass / Weight** | `kg` | `lbs` | `kerb-weight`, `gross-vehicle-weight` |
| **Velocity / Speed** | `km/h` | `mph` | `top-speed` |
| **Acceleration Time** | `s` (seconds) | `s` | `acceleration-0-100-km-h`, `acceleration-0-40-kmph` |
| **Charging Power** | `kW` | `kW` | `max-dc-charging-power`, `max-ac-charging-rate` |

---

## 3. Blueprint Schema Definition

```yaml
battery-capacity:
  name: "Battery Capacity"
  type: unit
  category: "Battery & Charging"
  standard_unit: "kWh"
  allowed_units: ["kWh", "Ah"]
  datatype: float
  min_value: 1.0
  max_value: 200.0
  filterable: true
  description: "Total gross electrochemical energy capacity of the traction battery pack."

ground-clearance:
  name: "Ground Clearance (Unladen)"
  type: unit
  category: "Dimensions & Capacity"
  standard_unit: "mm"
  allowed_units: ["mm", "inches"]
  datatype: integer
  filterable: true
  description: "Minimum distance between the lowest point of the vehicle chassis and the road surface."

max-power:
  name: "Maximum Power"
  type: unit
  category: "Motor & Performance"
  standard_unit: "kW"
  allowed_units: ["kW", "bhp", "hp", "ps"]
  datatype: float
  filterable: true
```

---

## 4. Variant Data JSON Examples

### Variant Storage (Normalized Object Structure)
```json
{
  "attributes": {
    "battery-capacity": {
      "value": 60.48,
      "unit": "kWh"
    },
    "max-power": {
      "value": 150.0,
      "unit": "kW"
    },
    "max-torque": {
      "value": 310.0,
      "unit": "Nm"
    },
    "ground-clearance": {
      "value": 175,
      "unit": "mm"
    },
    "top-speed": {
      "value": 160,
      "unit": "km/h"
    },
    "acceleration-0-100-km-h": {
      "value": 7.3,
      "unit": "s"
    }
  }
}
```

### Flat String Stringified Legacy Fallback
When dealing with flat string values during migration:
```json
{
  "attributes": {
    "battery-capacity": "60.48 kWh",
    "ground-clearance": "175 mm",
    "top-speed": "160 km/h"
  }
}
```

---

## 5. UI & Filtering Behavior

- **Filter Query**: `?battery-capacity_min=50&battery-capacity_max=80&ground-clearance_min=170`
- **Unit Conversion Engine**:
  - Automatically convert `kW` to `bhp` based on user display preferences:
    $$1\text{ kW} = 1.34102\text{ bhp}$$
  - Automatically convert `mm` to `inches`:
    $$1\text{ inch} = 25.4\text{ mm}$$
