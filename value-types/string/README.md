# String Attribute Type (`string`)

The `string` data type represents arbitrary text, human-readable descriptions, manufacturer designations, and marketing terminology that cannot be constrained to a finite enum or physical quantity.

---

## 1. Specification

| Property | Value | Description |
|---|---|---|
| **Type Identifier** | `string` | Canonical type string in schema definitions |
| **JSON Primitive** | `string` | UTF-8 encoded text string |
| **Go Type** | `string` | Standard string in Go |
| **PostgreSQL Type** | `TEXT` or `VARCHAR(255)` | Stored as text column |
| **Search Indexing** | Full-Text Search (tsvector / pg_trgm) | Supports fuzzy matching and keyword searches |
| **UI Filter Widget** | Text Search Input / Read-Only Specification Cell | Displayed in technical specification grids |

---

## 2. Blueprint Schema Definition

```yaml
engine-description:
  name: "Engine Description"
  type: string
  category: "Engine & Performance"
  max_length: 500
  searchable: true
  description: "Detailed proprietary description of the engine layout and valvetrain."

sound-system-brand:
  name: "Audio System Brand"
  type: string
  category: "Infotainment & Telematics"
  max_length: 100
  searchable: true
  description: "Branded sound system partner (e.g. Bose, Harman Kardon, Bowers & Wilkins)."

warranty-terms:
  name: "Warranty Terms"
  type: string
  category: "Warranty & Service"
  max_length: 300
  searchable: false
  description: "Manufacturer warranty coverage for vehicle, battery pack, and roadside assistance."
```

---

## 3. Variant Data JSON Examples

```json
{
  "attributes": {
    "engine-description": "1.5L TSI 4-Cylinder Turbocharged Petrol with Active Cylinder Technology (ACT)",
    "sound-system-brand": "Bang & Olufsen 3D Premium Sound System with 16 Speakers",
    "warranty-terms": "3 Years or 100,000 km standard vehicle warranty, 8 Years / 160,000 km battery warranty",
    "paint-protection": "Factory ceramic coating option available",
    "chassis-frame-type": "Steel Trellis Frame with Powder Coating"
  }
}
```

---

## 4. UI & Display Rules

- **Display**: Rendered in technical specification overview tables.
- **Searchable**: Indexed in global search (e.g. searching "Harman Kardon" surfaces all models equipped with that sound system).
- **Localization**: Supports multi-lingual descriptions where applicable (English / Nepali / Chinese).

---

## 5. Typical Automotive Attribute Slugs

- `engine-description`
- `sound-system-brand`
- `warranty-terms`
- `battery-warranty`
- `special-edition-badge`
- `chassis-frame-type`
- `front-suspension-type`
- `rear-suspension-type`
- `paint-finish`
- `interior-color-theme`
- `key-highlights`
