# Boolean Attribute Type (`boolean`)

The `boolean` data type represents binary flags, presence/absence of physical features, or enablement states of vehicle systems.

---

## 1. Specification

| Property | Value | Description |
|---|---|---|
| **Type Identifier** | `boolean` | Canonical type string in schema definitions |
| **JSON Primitive** | `boolean` \| `null` | Allowed JSON types |
| **Go Type** | `*bool` | Nullable boolean pointer in Go models |
| **PostgreSQL Type** | `BOOLEAN` | Native SQL boolean column |
| **Default Fallback** | `false` (when feature is confirmed absent) / `null` (unknown) | Never use mock or assumed values |
| **UI Filter Widget** | Toggle Switch / Single Checkbox / Yes-No Badge | Primary frontend interactive component |

---

## 2. Blueprint Schema Definition

In YAML blueprint definitions (`metrix/blueprint/data/`):

```yaml
abs:
  name: "Anti-lock Braking System (ABS)"
  type: boolean
  category: "Safety & Security"
  filterable: true
  description: "Prevents wheels from locking up during braking, maintaining tractive contact with the road."

ventilated-seats:
  name: "Ventilated Front Seats"
  type: boolean
  category: "Comfort & Convenience"
  filterable: true
  description: "Internal seat fans providing forced air ventilation through seat upholstery."

reverse-mode:
  name: "Reverse Mode"
  type: boolean
  category: "Motor & Performance"
  filterable: true
  description: "Electric motor reverse crawling assistance (specifically in 2W-BEV)."
```

---

## 3. Variant Data JSON Examples

### Example 1: Full Presence / Absence Representation
```json
{
  "attributes": {
    "abs": true,
    "brake-assist": true,
    "electronic-stability-program-esp": true,
    "hill-descent-control": false,
    "ventilated-seats": false,
    "panoramic-sunroof": true,
    "wireless-phone-charging": true
  }
}
```

### Example 2: Two-Wheeler Specific Attributes (`2W-BEV`)
```json
{
  "attributes": {
    "reverse-mode": true,
    "walk-assist-reverse-crawl": true,
    "hill-hold-assist": true,
    "cruise-control": false,
    "geo-fencing": true,
    "anti-theft-alarm": true
  }
}
```

---

## 4. UI & Filtering Behavior

- **Filter Query**: `?abs=true&panoramic-sunroof=true`
- **Faceted Search**:
  - `abs`: 420 models available
  - `ventilated-seats`: 85 models available
- **Display Component**:
  - On specification tables: A green checkmark badge (`Yes`) or subtle dash (`No`).
  - In comparison tables: Direct visual matrix comparison between variants.

---

## 5. Typical Automotive Attribute Slugs

- `abs`
- `hill-hold-assist`
- `reverse-mode`
- `traction-control`
- `electronic-stability-program-esp`
- `sunroof`
- `panoramic-sunroof`
- `ventilated-seats`
- `ambient-lighting`
- `keyless-entry`
- `push-button-start`
- `cruise-control`
- `automatic-climate-control`
- `wireless-phone-charging`
- `auto-dimming-irvm`
- `rain-sensing-wipers`
- `rear-defogger`
- `isofix-child-seat-mounts`
