# Automotive Specifications & Attribute Taxonomy

Welcome to the **Sawari Sadhan Attribute Taxonomy & Specification Documentation**.

This repository serves as the definitive reference manual for automotive vehicle specifications, physical measurement units, data types, categorization pillars, and standardization blueprints across all vehicle archetypes (**2-Wheeler ICE**, **2-Wheeler BEV**, **4-Wheeler ICE**, and **4-Wheeler BEV**).

---

## Documentation Directory

| Section | Directory | Focus & Standards |
|---|---|---|
| **Pillar Taxonomy** | [**`categories/`**](./categories/README.md) | The 10 Canonical Automotive Engineering Pillars (SAE J3016, ISO 3833, ISO 15118, Euro NCAP) |
| **Value Types** | [**`value-types/`**](./value-types/README.md) | Specifications for all 10 schema primitive value types (`unit`, `boolean`, `integer`, etc.) |
| **Physical Units** | [**`units/`**](./units/README.md) | Standardized measurement units across 16 dimensions and conversion factor equations |
| **Vehicle Archetypes** | [**`vehicle-archetypes/`**](./vehicle-archetypes/README.md) | Comprehensive blueprints for `2W-BEV`, `2W-ICE`, `4W-BEV`, and `4W-ICE` |

---

## Core Principles

1. **Physical Quantity vs. Measurement Unit**:
   - Attribute slugs describe *what* is measured (e.g., `power-engine`, `battery-capacity`, `curb-weight`).
   - Slugs *never* embed unit names (e.g. `power-engine-kw` or `speed-kmph` are strictly prohibited).
   - Units are tracked dynamically via canonical slugs (`kilowatt`, `kilowatt-hour`, `kilogram`).

2. **Strict Count Naming**:
   - Every countable discrete integer strictly uses the `number-of-*` prefix (e.g., `number-of-cylinders`, `number-of-valves-per-cylinder`, `number-of-doors`, `number-of-airbags`).

3. **Boolean Feature Normalization**:
   - Deduplicated and normalized feature flags across all vehicle archetypes (e.g. `voice-recognition` instead of redundant marketing variants).

4. **10 Industry-Standard Pillars**:
   - 47 fragmented legacy web-scraper categories consolidated into 10 international automotive pillars (+ 1 auxiliary packages pillar).
