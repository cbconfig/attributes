# Standardized Measurement Attribute Type (`standardized_measurement`)

The `standardized_measurement` data type represents numerical performance figures whose validity and meaning strictly depend on the regulatory or industrial testing cycle applied (e.g. EV driving range under CLTC vs. WLTP, or fuel efficiency under ARAI vs. EPA).

---

## 1. Specification

| Property | Value | Description |
|---|---|---|
| **Type Identifier** | `standardized_measurement` | Canonical type string in schema definitions |
| **JSON Representation** | `{"value": number, "unit": string, "cycle": string}` | Value with measurement unit and accredited testing protocol |
| **Go Type** | `struct { Value float64; Unit string; Cycle string }` | Structured model in Go |
| **PostgreSQL Type** | JSONB or normalized columns (`numeric`, `varchar`) | Indexed for cycle-aware queries |
| **UI Filter Widget** | Cycle-Aware Range Slider / Standard Badges | E.g. Range Slider with Cycle Selector [CLTC | WLTP | EPA] |

---

## 2. Standardized Testing Protocols

### A. Electric Vehicle Range Cycles
- **CLTC** (China Light-Duty Vehicle Test Cycle) — Typical of Chinese EV imports (`v3`). Generally the most optimistic.
- **WLTP** (Worldwide Harmonised Light Vehicles Test Procedure) — European standard. Realistic mixed driving conditions.
- **EPA** (United States Environmental Protection Agency) — Strict, multi-cycle real-world testing.
- **NEDC** (New European Driving Cycle) — Legacy cycle (pre-2018).
- **MIDC / ARAI** (Modified Indian Driving Cycle) — Standard in South Asia (`v1`, `v2`).
- **WMTC** (World Motorcycle Test Cycle) — Standard for 2W ICE and 2W BEV.

### B. Fuel Economy / Consumption Cycles
- **ARAI** (`km/l`) — Indian standard test
- **WLTP Combined** (`L/100km`) — European combined fuel consumption
- **EPA Combined** (`MPG`) — US miles per gallon

---

## 3. Blueprint Schema Definition

```yaml
range-cltc:
  name: "Range (CLTC)"
  type: standardized_measurement
  category: "Battery & Charging"
  standard_unit: "km"
  cycle: "CLTC"
  datatype: float
  filterable: true
  description: "Driving range certified under China Light-Duty Vehicle Test Cycle."

range-wltp:
  name: "Range (WLTP Combined)"
  type: standardized_measurement
  category: "Battery & Charging"
  standard_unit: "km"
  cycle: "WLTP"
  datatype: float
  filterable: true
  description: "Driving range certified under Worldwide Harmonised Light Vehicle Test Procedure."

mileage-arai:
  name: "Fuel Economy (ARAI)"
  type: standardized_measurement
  category: "Engine & Performance"
  standard_unit: "km/l"
  cycle: "ARAI"
  datatype: float
  filterable: true
  description: "Certified fuel efficiency tested by the Automotive Research Association of India."
```

---

## 4. Variant Data JSON Examples

### Structured Representation
```json
{
  "attributes": {
    "range-cltc": {
      "value": 520,
      "unit": "km",
      "cycle": "CLTC"
    },
    "range-wltp": {
      "value": 440,
      "unit": "km",
      "cycle": "WLTP"
    },
    "mileage-arai": {
      "value": 20.8,
      "unit": "km/l",
      "cycle": "ARAI"
    }
  }
}
```

### Flat String Stringified Migration Equivalent
```json
{
  "attributes": {
    "range-cltc": "520 km",
    "range-wltp": "440 km",
    "mileage-arai": "20.8 kmpl"
  }
}
```

---

## 5. UI & Filtering Behavior

- **Cycle Normalization**:
  The UI allows filtering by range regardless of test standard, applying conservative conversion estimates when cross-comparing:
  $$\text{WLTP} \approx \text{CLTC} \times 0.82$$
- **Badge Presentation**: Displays clearly with the testing cycle acronym:
  - `520 km` <span style="background:#e0f2fe;color:#0369a1;padding:2px 6px;border-radius:4px;font-size:12px;">CLTC</span>
  - `440 km` <span style="background:#fef3c7;color:#92400e;padding:2px 6px;border-radius:4px;font-size:12px;">WLTP</span>
