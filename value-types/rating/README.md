# Rating / Score Attribute Type (`rating`)

The `rating` data type represents formal safety crash test scores, agency evaluations, and environmental/ingress protection standards. It ensures that star ratings, test agencies, and certification protocols are not lost as generic numbers or unstructured strings.

---

## 1. Specification

| Property | Value | Description |
|---|---|---|
| **Type Identifier** | `rating` | Canonical type string in schema definitions |
| **JSON Representation** | `{"score": number, "scale": number, "agency": string, "year": int}` or standardized code (`"IP67"`) | Structured rating or verified certification standard |
| **Go Type** | `struct { Score float64; Scale float64; Agency string; Year int }` | Structured rating model |
| **PostgreSQL Type** | JSONB or structured composite columns | Allows filtering by agency and minimum stars |
| **UI Filter Widget** | Star Rating Badges / Agency Seals / Ingress Protection Pills | E.g. [★★★★★ Global NCAP] |

---

## 2. Automotive Evaluation Domains

### A. Crash Test Safety Agencies
- **Global NCAP** (New Car Assessment Programme)
- **Bharat NCAP** (India)
- **Euro NCAP** (Europe)
- **C-NCAP** (China)
- **ANCAP** (Australasia)
- **IIHS** (USA - Top Safety Pick+)
- **NHTSA** (USA - 5-Star Safety Ratings)

### B. Ingress Protection (IP Ratings)
Critical for EV traction batteries and electric motors operating in extreme monsoons or water wading:
- `IP67` (Dust tight, protected against immersion up to 1m for 30 min)
- `IP68` (Dust tight, continuous submersion beyond 1m)
- `IP6K9K` (High-pressure, high-temperature washdown resistance)

---

## 3. Blueprint Schema Definition

```yaml
ncap-rating:
  name: "Safety Crash Rating"
  type: rating
  category: "Safety & Security"
  filterable: true
  description: "Official occupant crashworthiness safety score from an accredited NCAP agency."

battery-ip-rating:
  name: "Battery Pack Ingress Protection"
  type: rating
  category: "Battery & Charging"
  filterable: true
  description: "Standardized dust and water ingress protection rating (IEC 60529)."
```

---

## 4. Variant Data JSON Examples

### Structured NCAP Rating
```json
{
  "attributes": {
    "ncap-rating": {
      "score": 5,
      "scale": 5,
      "agency": "Global NCAP",
      "year": 2024,
      "adult_safety_score": "34.00/34.00",
      "child_safety_score": "41.00/49.00"
    },
    "battery-ip-rating": "IP67",
    "motor-ip-rating": "IP67"
  }
}
```

---

## 5. UI & Filtering Behavior

- **Filter Query**: `?min_safety_stars=5&agency=Global%20NCAP`
- **Frontend Presentation**:
  - Gold star visual indicator: `★★★★★ 5-Star (Global NCAP 2024)`
  - Sub-scores displayed in modal sheet: Adult Safety 96%, Child Safety 88%
  - IP Rating badge: Shield icon with `IP67 Water & Dust Resistance`.
