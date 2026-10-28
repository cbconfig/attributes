# Integer Attribute Type (`integer`)

The `integer` data type represents pure, whole-number counts and discrete quantities without fractional parts or measurement units.

---

## 1. Specification

| Property | Value | Description |
|---|---|---|
| **Type Identifier** | `integer` | Canonical type string in schema definitions |
| **JSON Primitive** | `integer` (e.g. `5`, `6`, `4`) | Whole numeric value without decimals |
| **Go Type** | `int` or `int32` | Standard integer in Go models |
| **PostgreSQL Type** | `SMALLINT` or `INTEGER` | Compact integer column with fast comparison |
| **UI Filter Widget** | Discrete Pill Selector / Numeric Stepper / Min-Max Input | E.g. Seating: [2] [4] [5] [7] [8] |

---

## 2. Common Integer Attributes in Automotive Specs

| Attribute Slug | Description | Common Range |
|---|---|---|
| `seating-capacity` | Maximum passenger count certified | 1 to 9 |
| `number-of-doors` | Physical vehicle doors including hatch | 2, 3, 4, 5 |
| `number-of-cylinders` | Engine cylinder count (ICE) | 1, 2, 3, 4, 6, 8, 12 |
| `number-of-valves-per-cylinder` | Valvetrain count per cylinder | 2, 4 |
| `number-of-airbags` | Total occupant safety airbags installed | 2 to 10 |
| `number-of-speakers` | Sound system speaker count | 2 to 24 |
| `number-of-gears` | Forward gear ratios in manual/auto transmission | 4 to 10 |
| `number-of-cameras` | Surround view & ADAS optical cameras | 1 to 12 |
| `number-of-ultrasonic-sensors` | Parking sonar sensors installed | 4 to 12 |
| `number-of-millimeter-wave-radars` | ADAS radar sensors | 1 to 5 |
| `number-of-motors` | Electric propulsion motors count | 1, 2, 3, 4 |

---

## 3. Blueprint Schema Definition

```yaml
seating-capacity:
  name: "Seating Capacity"
  type: integer
  category: "Dimensions & Capacity"
  min_value: 1
  max_value: 9
  filterable: true
  description: "Total number of seat positions equipped with safety restraints."

number-of-airbags:
  name: "Number of Airbags"
  type: integer
  category: "Safety & Security"
  min_value: 0
  max_value: 12
  filterable: true
  description: "Total count of supplementary restraint system (SRS) airbags."

number-of-motors:
  name: "Number of Drive Motors"
  type: integer
  category: "Motor & Performance"
  min_value: 1
  max_value: 4
  filterable: true
  description: "Total electric traction motors installed across vehicle axles."
```

---

## 4. Variant Data JSON Examples

```json
{
  "attributes": {
    "seating-capacity": 5,
    "number-of-doors": 5,
    "number-of-cylinders": 4,
    "number-of-airbags": 6,
    "number-of-speakers": 8,
    "number-of-gears": 6,
    "number-of-motors": 2,
    "number-of-cameras": 4,
    "number-of-ultrasonic-sensors": 12
  }
}
```

---

## 5. UI & Filtering Behavior

- **Filter Query**: `?seating-capacity=5,7&number-of-airbags_min=6`
- **Pill Filter UI**:
  - `Seats`: `[2] [4] [5 (Active)] [7 (Active)] [8+]`
- **Comparison Table**: Clear numeric display with instant delta calculations (e.g. `+2 Airbags`).
