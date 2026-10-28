# Automotive Attribute Value Types

This directory defines the **10 canonical attribute value types** that govern the schema, storage primitives, filtering behavior, and rendering pipelines across the Sawari Sadhan platform.

---

## 1. Value Types Registry

| # | Type Identifier | Primitive / Go Type | Database Type | Description | Key Examples |
|:---:|---|---|---|---|---|
| 1 | [**`boolean`**](./boolean/README.md) | `bool` / `*bool` | `BOOLEAN` | Binary presence, capability, or toggle state | `abs`, `sunroof`, `reverse-mode` |
| 2 | [**`unit`**](./unit/README.md) | `float64` / `*float64` | `NUMERIC` + meta | Numeric quantity with physical measurement unit | `power-motor` (kW), `battery-capacity` (kWh) |
| 3 | [**`integer`**](./integer/README.md) | `int64` / `*int64` | `INTEGER` | Discrete whole-number counts (`number-of-*`) | `number-of-cylinders`, `number-of-doors` |
| 4 | [**`string`**](./string/README.md) | `string` / `*string` | `TEXT` | Free-form descriptive text, names, warranty terms | `model-name`, `warranty-terms` |
| 5 | [**`enum`**](./enum/README.md) | `string` / `*string` | `VARCHAR(64)` | Controlled single-select category | `fuel-type`, `motor-type`, `drive-type` |
| 6 | [**`enum_list`**](./enum_list/README.md) | `[]string` | `TEXT[]` / `JSONB` | Multi-select suite, tag arrays, drive modes | `riding-modes`, `adas-features` |
| 7 | [**`range`**](./range/README.md) | `struct{Min, Max}` | `NUMRANGE` / `JSONB` | Variable interval values (min to max) | `ground-clearance-range` |
| 8 | [**`rating`**](./rating/README.md) | `string` / `struct` | `JSONB` / `VARCHAR` | Safety crash test scores & IP ingress ratings | `ncap-rating` (5 Stars), `motor-ip-rating` (IP67) |
| 9 | [**`dimension_tuple`**](./dimension_tuple/README.md) | `string` / `struct` | `VARCHAR(64)` | Multi-axial compound codes (tires, envelope) | `tire-size-front` (215/55 R17) |
| 10 | [**`standardized_measurement`**](./standardized_measurement/README.md) | `struct` | `JSONB` | Protocol-specific certification tests | `range-wltp`, `range-cltc`, `mileage-arai` |

---

## 2. Technical Contracts & Invariants

1. **Separation of Measurement & Unit**:
   - `unit` attributes specify *what* is measured; units are declared in the schema, never concatenated into the slug (e.g. `power-motor` with `unit: kilowatt`, not `power-motor-kw`).
2. **Discrete Count Standard**:
   - `integer` attributes represent discrete whole objects and strictly follow the `number-of-*` naming convention (e.g. `number-of-cylinders`, `number-of-airbags`).
3. **Controlled Vocabularies**:
   - `enum` attributes enforce closed taxonomies (e.g. `fuel-type: [petrol, diesel, electric, hybrid]`) for reliable faceted searching and filtering.

---

## 3. Directory Structure

Each subfolder contains an exhaustive technical specification:
- **`boolean/`**: [Specification & UI rendering](./boolean/README.md)
- **`unit/`**: [Specification & conversion mechanics](./unit/README.md)
- **`integer/`**: [Discrete count contracts](./integer/README.md)
- **`string/`**: [Textual descriptions & standards](./string/README.md)
- **`enum/`**: [Single-select taxonomies](./enum/README.md)
- **`enum_list/`**: [Multi-select arrays](./enum_list/README.md)
- **`range/`**: [Interval boundaries & min-max handling](./range/README.md)
- **`rating/`**: [Crash test ratings & IP ratings](./rating/README.md)
- **`dimension_tuple/`**: [Compound multi-axial codes](./dimension_tuple/README.md)
- **`standardized_measurement/`**: [Regulatory test cycles](./standardized_measurement/README.md)
