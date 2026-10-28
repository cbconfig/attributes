# Dimension Tuple Attribute Type (`dimension_tuple`)

The `dimension_tuple` data type represents linked, multi-axial mechanical specifications that naturally belong together as a single physical entity rather than separate fragmented numbers (e.g. standard tire size codes, overall LxWxH dimensions, bore & stroke, or wheel rim profiles).

---

## 1. Specification

| Property | Value | Description |
|---|---|---|
| **Type Identifier** | `dimension_tuple` | Canonical type string in schema definitions |
| **JSON Representation** | Structured object (e.g. `{"length": 4300, "width": 1790, "height": 1620, "unit": "mm"}`) or standardized alphanumeric industry code (`"215/55 R17"`) | Compound dimensional specification |
| **Go Type** | Custom struct or parsed string model | Allows parsing individual dimensions on demand |
| **PostgreSQL Type** | JSONB or composite type | Supports targeted indexing on sub-fields |
| **UI Filter Widget** | Formatted Badge / Interactive 3D Wireframe Car Diagram | Clear multi-dimensional rendering |

---

## 2. Common Automotive Use Cases

### A. Tire Specifications
Tire dimensions follow the international ISO metric tire-code standard:
`[Section Width in mm] / [Aspect Ratio %] [Construction: Radial] [Rim Diameter in Inches]`
- `tire-size-front`: `"215/55 R17"`
  - Width: 215 mm
  - Aspect Ratio: 55%
  - Radial construction
  - Rim: 17 inches
- `tire-size-rear`: `"235/50 R18"` (staggered setup)

### B. Compound Vehicle Dimensions (LxWxH)
- `overall-dimensions-lxwxh`:
  ```json
  {
    "length": 4300,
    "width": 1790,
    "height": 1620,
    "unit": "mm"
  }
  ```

### C. Engine Bore x Stroke (ICE)
Cylinder bore diameter multiplied by piston stroke distance:
- `bore-x-stroke`: `"75.0 mm x 84.8 mm"`

### D. Wheel Rim Dimensions
- `wheel-rim-size`: `"18 x 7.5J"`
  - 18 inch diameter, 7.5 inch width, "J" bead profile

---

## 3. Blueprint Schema Definition

```yaml
tire-size-front:
  name: "Front Tire Size"
  type: dimension_tuple
  category: "Wheels & Tires"
  pattern: "^(\\d{3})/(\\d{2})\\s*(R|ZR|D)?(\\d{2})$"
  filterable: true
  description: "Standard ISO metric tire code specification for front axle."

tire-size-rear:
  name: "Rear Tire Size"
  type: dimension_tuple
  category: "Wheels & Tires"
  pattern: "^(\\d{3})/(\\d{2})\\s*(R|ZR|D)?(\\d{2})$"
  filterable: true
  description: "Standard ISO metric tire code specification for rear axle."

overall-dimensions:
  name: "Overall Dimensions (L x W x H)"
  type: dimension_tuple
  category: "Dimensions & Capacity"
  standard_unit: "mm"
  filterable: false
  description: "Exterior physical envelope of the vehicle body excluding side mirrors."
```

---

## 4. Variant Data JSON Examples

```json
{
  "attributes": {
    "tire-size-front": "215/55 R17",
    "tire-size-rear": "215/55 R17",
    "overall-dimensions": {
      "length": 4300,
      "width": 1790,
      "height": 1620,
      "unit": "mm"
    },
    "wheel-rim-size": "17 x 7.0J",
    "bore-x-stroke": "74.5 mm x 85.9 mm"
  }
}
```

---

## 5. UI & Display Formatting

- **Tire Badge**: Rendered with tire icon: `🛞 215/55 R17`
- **Dimension Diagram**: Shows an interactive 3D / isometric wireframe car displaying Length (4,300 mm), Width (1,790 mm), and Height (1,620 mm) along corresponding dimensional axes.
- **Tire Search**: Allows filtering by rim diameter (e.g. `R17`, `R18`, `R19`) or section width.
