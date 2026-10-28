# 📱 Infotainment, Telematics & Screens

**Pillar Slug**: `infotainment-screens-connectivity`  
**International Standards**: *SDV (Software-Defined Vehicle) Benchmarks, Android Automotive OS, Apple CarPlay*

Central touchscreens, digital driver instrument clusters, Head-Up Displays (HUD), cockpit processors/SoCs, premium branded audio systems, 5G eSIM telematics, and Over-The-Air (OTA) firmware update systems.

---

## 1. Domain Overview

| Metric | Value |
|---|---|
| **Canonical Pillar Slug** | `infotainment-screens-connectivity` |
| **Total Standardized Attributes** | 71 |
| **Active In Blueprints** | 2W-BEV, 2W-ICE, 4W-BEV, 4W-ICE |

---

## 2. Standardized Attributes Catalog

| Attribute Slug | Value Type | Unit / Specification | Applicable Blueprints |
|---|:---:|:---:|---|
| `4g-5g-networks` | `string` | — | 4W-BEV |
| `acoustic-brand` | `string` | — | 4W-BEV |
| `active-noise-cancellation` | `boolean` | — | 4W-BEV |
| `app-store` | `boolean` | — | 4W-BEV |
| `ar-live-navigation` | `boolean` | — | 4W-BEV |
| `audio-system-remote-control` | `boolean` | — | 4W-ICE |
| `audiovisual-system` | `boolean` | — | 4W-BEV |
| `bluetooth-car-calls` | `boolean` | — | 4W-BEV |
| `bluetooth-connectivity` | `boolean` | — | 2W-BEV, 2W-ICE, 4W-ICE |
| `call-sms-alerts` | `boolean` | — | 2W-BEV, 2W-ICE |
| `car-tv` | `boolean` | — | 4W-BEV |
| `cd-changer` | `boolean` | — | 4W-ICE |
| `cd-player` | `boolean` | — | 4W-ICE |
| `center-console-color-screen-resolution` | `string` | — | 4W-BEV |
| `center-screen-size` | `unit` | `inch` | 2W-BEV |
| `co-pilot-screen-resolution` | `string` | — | 4W-BEV |
| `companion-app-telematics` | `string` | — | 2W-BEV |
| `connected-car-suite` | `string` | — | 4W-ICE |
| `connectivity` | `string` | — | 4W-ICE |
| `continuous-speech-recognition` | `boolean` | — | 4W-BEV |
| `display-type` | `string` | — | 2W-BEV |
| `dvd-player` | `boolean` | — | 4W-ICE |
| `emotion-recognition` | `boolean` | — | 4W-BEV |
| `facial-recognition` | `boolean` | — | 4W-BEV |
| `fingerprint-recognition` | `boolean` | — | 4W-BEV |
| `geo-fencing` | `boolean` | — | 4W-BEV |
| `gesture-control` | `boolean` | — | 4W-BEV |
| `gps-navigation` | `boolean` | — | 4W-BEV |
| `in-car-karaoke` | `boolean` | — | 4W-BEV |
| `instrument-console` | `string` | — | 2W-BEV |
| `instrument-console-type` | `string` | — | 2W-ICE |
| `integrated-2din-audio` | `boolean` | — | 4W-ICE |
| `internal-storage` | `boolean` | — | 4W-ICE |
| `lower-center-screen-size` | `string` | — | 4W-BEV |
| `media-easter-egg` | `boolean` | — | 4W-BEV |
| `mobile-app-connectivity` | `boolean` | — | 2W-BEV |
| `mobile-connected-mapping` | `string` | — | 4W-BEV |
| `multi-finger-screen-control` | `boolean` | — | 4W-BEV |
| `multimedia-interface` | `string` | — | 4W-BEV |
| `navigation-gps` | `boolean` | — | 2W-BEV, 2W-ICE |
| `number-of-front-speakers` | `integer` | — | 4W-ICE |
| `number-of-rear-speakers` | `integer` | — | 4W-ICE |
| `number-of-speakers` | `integer` | — | 4W-BEV, 4W-ICE |
| `number-of-usb-ports` | `integer` | — | 4W-BEV |
| `on-road-assistance` | `boolean` | — | 4W-BEV |
| `ota-updates` | `boolean` | — | 2W-BEV |
| `ota-upgrade` | `boolean` | — | 4W-BEV |
| `ota-version` | `boolean` | — | 4W-BEV |
| `passenger-screen-pixel-density` | `unit` | `ppi` | 4W-BEV |
| `passenger-screen-size` | `unit` | `inch` | 4W-BEV |
| `radio` | `boolean` | — | 4W-ICE |
| `real-time-navigation` | `boolean` | — | 4W-BEV |
| `rear-entertainment-system` | `boolean` | — | 4W-ICE |
| `rear-multimedia-controls` | `boolean` | — | 4W-BEV |
| `relax-mode` | `boolean` | — | 4W-BEV |
| `smart-voice-interaction` | `boolean` | — | 4W-BEV |
| `sound-system-brand` | `string` | — | 4W-ICE |
| `subwoofer` | `boolean` | — | 4W-ICE |
| `telematics-system` | `boolean` | — | 4W-BEV |
| `touch-screen-vibration-feedback` | `boolean` | — | 4W-BEV |
| `touchscreen` | `boolean` | — | 4W-ICE |
| `touchscreen-size-inches` | `string` | — | 4W-ICE |
| `usb-aux-input` | `boolean` | — | 4W-ICE |
| `usb-charging-port` | `boolean` | — | 2W-BEV, 2W-ICE |
| `usb-charging-power` | `unit` | `watt` | 4W-BEV |
| `voice-activation-wake-word` | `boolean` | — | 4W-BEV |
| `voice-recognition` | `boolean` | — | 4W-BEV |
| `wi-fi-hotspot` | `boolean` | — | 4W-BEV |
| `wireless-android-auto` | `boolean` | — | 4W-ICE |
| `wireless-apple-carplay` | `boolean` | — | 4W-ICE |
| `wireless-phone-charging` | `boolean` | — | 4W-ICE |

---

## 3. Implementation Guidelines

- **Attribute Decoupling**: Attribute slugs describe physical metrics; units are tracked dynamically.
- **Discrete Counts**: Discrete whole-number quantities must strictly use `number-of-*` prefixes.
- **Cross-Archetype Consistency**: Any attribute shared between two-wheelers and four-wheelers maintains identical typing.
