# Enum Attribute Type (`enum`)

The `enum` data type represents single-select attributes strictly constrained to a finite, standardized list of valid options. It powers the primary navigation filters, faceted search dropdowns, and categorical grouping in Sawari Sadhan.

---

## 1. Specification

| Property | Value | Description |
|---|---|---|
| **Type Identifier** | `enum` | Canonical type string in schema definitions |
| **JSON Primitive** | `string` (must match an allowed option) | Value must exist in the blueprint `options` array |
| **Go Type** | Custom Go string alias / enum type | Strictly validated during ingestion |
| **PostgreSQL Type** | `VARCHAR(64)` or `enum` type | Indexed with B-Tree for sub-millisecond filtering |
| **UI Filter Widget** | Dropdown Selector / Radio Buttons / Segmented Pills | Faceted filters with vehicle counts |

---

## 2. Standardized Automotive Taxonomies

### A. `fuel-type`
- **Options**: `["Petrol", "Diesel", "Electric", "Hybrid", "Plug-in Hybrid (PHEV)", "CNG", "LPG", "Hydrogen FCEV"]`

### B. `transmission-type`
- **Options**: `["Manual", "Automatic", "CVT", "e-CVT", "Dual-Clutch (DCT)", "Automated Manual (AMT)", "Single-Speed Reduction"]`

### C. `drive-type`
- **Options**: `["FWD", "RWD", "AWD", "4WD", "Part-Time 4WD"]`

### D. `motor-type`
- **Options**: `["Permanent Magnet Synchronous Motor (PMSM)", "Brushless DC (BLDC)", "AC Induction Motor", "Interior Permanent Magnet (IPM-SynRM)", "Switched Reluctance Motor"]`

### E. `battery-chemistry`
- **Options**: `["Lithium Iron Phosphate (LFP)", "Nickel Manganese Cobalt (NMC)", "Nickel Cobalt Aluminum (NCA)", "Sodium-ion", "Solid-State", "Lead Acid"]`

### F. `body-type`
- **Options**: `["SUV", "Sedan", "Hatchback", "Coupe", "MPV", "Pickup", "Station Wagon", "Convertible", "Scooter", "Motorcycle", "Cruiser", "Adventure Tourer"]`

---

## 3. Blueprint Schema Definition

```yaml
motor-type:
  name: "Motor Type"
  type: enum
  category: "Motor & Performance"
  filterable: true
  options:
    - "PMSM"
    - "BLDC"
    - "AC Induction"
    - "IPM-SynRM"
  description: "Operating principle and magnetic construction of the electric propulsion motor."

drive-type:
  name: "Drive Type"
  type: enum
  category: "Drivetrain"
  filterable: true
  options:
    - "FWD"
    - "RWD"
    - "AWD"
    - "4WD"
  description: "Configuration of wheels receiving propulsive torque from the powertrain."

battery-chemistry:
  name: "Battery Chemistry"
  type: enum
  category: "Battery & Charging"
  filterable: true
  options:
    - "LFP"
    - "NMC"
    - "NCA"
    - "Sodium-ion"
  description: "Cathode and electrolyte chemical composition of traction battery cells."
```

---

## 4. Variant Data JSON Examples

```json
{
  "attributes": {
    "fuel-type": "Electric",
    "transmission-type": "Single-Speed Reduction",
    "drive-type": "AWD",
    "motor-type": "PMSM",
    "battery-chemistry": "LFP",
    "body-type": "SUV",
    "cooling-system": "Liquid Cooled"
  }
}
```

---

## 5. UI & Filtering Behavior

- **Filter Query**: `?drive-type=AWD&fuel-type=Electric&motor-type=PMSM`
- **Facet Counts Display**:
  - `drive-type`:
    - AWD (142)
    - FWD (620)
    - RWD (98)
- **Validation**: Rejects invalid values (e.g. `"drive-type": "All Wheel Drive"` is normalized to `"AWD"`).
