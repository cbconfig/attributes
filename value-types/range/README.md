# Range / Min-Max Attribute Type (`range`)

The `range` data type represents specifications that naturally vary within an interval rather than existing as a single static scalar number. This occurs frequently with real-world operating conditions, ambient temperatures, and variable pneumatic air suspensions.

---

## 1. Specification

| Property | Value | Description |
|---|---|---|
| **Type Identifier** | `range` | Canonical type string in schema definitions |
| **JSON Representation** | `{"min": number, "max": number, "unit": string}` | Interval boundary structure |
| **Go Type** | `struct { Min float64; Max float64; Unit string }` | Structured range model in Go |
| **PostgreSQL Type** | `numrange` or JSONB object | Native PostgreSQL numeric range support |
| **UI Filter Widget** | Dual Range Slider / Interval Tag | Enables filtering vehicles whose interval overlaps user criteria |

---

## 2. Common Automotive Use Cases

### A. Real-World Driving Range
EV range varies significantly between highway/winter conditions and urban regenerative braking.
- `estimated-real-world-range`: `{"min": 350, "max": 420, "unit": "km"}`

### B. Adaptive Suspension Ground Clearance
Vehicles with air suspension can dynamically raise or lower chassis ride height.
- `ground-clearance-range`: `{"min": 170, "max": 220, "unit": "mm"}`

### C. DC Fast Charging Time Interval
Charging from 10% to 80% state of charge under optimal vs ambient temperature conditions.
- `fast-charging-time-range`: `{"min": 28, "max": 35, "unit": "minutes"}`

### D. Variable RPM Power / Torque Bands (ICE)
Torque band plateau in modern turbocharged engines.
- `torque-rpm-range`: `{"min": 1500, "max": 4100, "unit": "rpm"}`

---

## 3. Blueprint Schema Definition

```yaml
estimated-real-world-range:
  name: "Estimated Real-World Range"
  type: range
  category: "Battery & Charging"
  standard_unit: "km"
  filterable: true
  description: "Expected operational range spanning conservative highway driving to efficient city use."

ground-clearance-range:
  name: "Adaptive Ground Clearance Range"
  type: range
  category: "Suspension & Chassis"
  standard_unit: "mm"
  filterable: true
  description: "Adjustable clearance range facilitated by adaptive air suspension modes."
```

---

## 4. Variant Data JSON Examples

```json
{
  "attributes": {
    "estimated-real-world-range": {
      "min": 360,
      "max": 440,
      "unit": "km"
    },
    "ground-clearance-range": {
      "min": 165,
      "max": 215,
      "unit": "mm"
    },
    "torque-rpm-band": {
      "min": 1600,
      "max": 4300,
      "unit": "rpm"
    }
  }
}
```

---

## 5. UI & Filtering Behavior

- **Display Formatting**: Rendered cleanly as `360 – 440 km` or `165 mm (Off-Road: 215 mm)`.
- **Overlap Query Logic**: If a user filters for vehicles offering at least `400 km` range, vehicles with `max >= 400` are surfaced.
