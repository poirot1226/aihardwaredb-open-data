# Consumer AI Hardware 2-Year True Ownership Cost Dataset (v1.1.0)

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC_BY_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)
[![Canonical Source](https://img.shields.io/badge/Canonical-aihardwaredb.com%2Fdata%2F-0ea5e9)](https://aihardwaredb.com/data/)

> **Canonical Live Dataset, Interactive Table & Monthly Updates:** [https://aihardwaredb.com/data/](https://aihardwaredb.com/data/)  
> **Interactive 6–36 Month TCO Calculator:** [https://aihardwaredb.com/tools/true-cost-calculator/](https://aihardwaredb.com/tools/true-cost-calculator/)  
> **Formula & 5-Axis Scoring Methodology:** [https://aihardwaredb.com/methodology/#scoring](https://aihardwaredb.com/methodology/#scoring)

## Overview

This repository mirrors the open, document-verified **AIHardwareDB v1.1.0 dataset** covering **34 consumer AI hardware devices** across AI voice recorders, smart rings, AI glasses, translation earbuds, companion robots, and discontinued/bricked hardware (**8 deep-audited models** with live review pages + **26 spec-indexed models**).

Every active device is measured against one reproducible ownership formula:

```text
24-Month True Cost = Verified Retail Hardware Price (USD) + (24 × Monthly Equivalent Subscription Tier)
```

Discontinued and cloud-shutdown devices (such as **Humane AI Pin** and **Limitless Pendant**) are explicitly tagged with `status: service_shutdown` or `status: discontinued`, have `null` for active 24-month cost fields, and preserve their historical cost separately in `documented_cost_historical_usd` so automated pipelines never mistake bricked hardware for buyable devices.

## Files Included

| File | Format | Canonical Live URL |
|---|---|---|
| [`v1/hardware.csv`](./v1/hardware.csv) | CSV (34 rows, 31 fields) | `https://aihardwaredb.com/data/v1/hardware.csv` |
| [`v1/hardware.json`](./v1/hardware.json) | Structured JSON | `https://aihardwaredb.com/data/v1/hardware.json` |
| [`v1/schema.json`](./v1/schema.json) | JSON Schema (Draft 2020-12) | `https://aihardwaredb.com/data/v1/schema.json` |

## Highlighted Deep-Audited Wave 1 Devices (Verified 2026-11-22)

| Device | Hardware MSRP | 24-Mo Free/Min | 24-Mo Annual Pro | 24-Mo Unlimited | Local Storage | Deep Audit Page |
|---|---:|---:|---:|---:|---|---|
| **Plaud Note** | $159 | $159 | $359 | $639 | 64GB flash | [Audit](https://aihardwaredb.com/devices/plaud-note/) |
| **Plaud Note Pro** | $189 | $189 | $389 | $669 | 64GB flash | [Audit](https://aihardwaredb.com/devices/plaud-note-pro/) |
| **Plaud NotePin** | $159 | $159 | $359 | $639 | 64GB flash | [Audit](https://aihardwaredb.com/devices/plaud-notepin/) |
| **Pocket AI (HeyPocket)** | $129 | $129 | $609 | $609 | 64GB flash | [Audit](https://aihardwaredb.com/devices/pocket-ai-recorder/) |
| **Omi (Based Hardware)** | $129 | $129 | $129 (BYOK) | $669 | BLE + SD/BYOK | [Audit](https://aihardwaredb.com/devices/omi-pendant/) |
| **Anker Soundcore Work** | $159 | $159 | $359 | $359 | 8GB flash | [Audit](https://aihardwaredb.com/devices/anker-soundcore-work/) |
| **SwitchBot AI MindClip** | $120 | $120 | $320 | $320 | 64GB flash + CLI | [Audit](https://aihardwaredb.com/devices/switchbot-ai-mindclip/) |
| **Mobvoi TicNote** | $160 | $160 | $360 | $360 | 64GB flash | [Audit](https://aihardwaredb.com/devices/mobvoi-ticnote/) |

## Key Fields (`v1/schema.json`)

- `status`: `active` | `discontinued` | `service_shutdown`
- `coverage_level`: `deep_audit` (live full review page) | `indexed_spec` (master index row)
- `two_year_total_min_usd` / `two_year_total_annual_pro_usd` / `two_year_total_unlimited_usd` (`null` for inactive devices)
- `documented_cost_historical_usd` (populated for discontinued / bricked hardware only)
- `has_recording_led`, `has_camera`, `local_storage`, `export_formats`, `byok_api_support`, `open_source_firmware`, `openness_score_out_of_5`
- `verified_date` & `official_source_url`

## How to Cite (CC BY 4.0)

**APA / Editorial:**
```text
AIHardwareDB. (2026). Consumer AI Hardware 2-Year True Cost Dataset (Version 1.1.0) [Data set]. Verified 2026-11-22. https://aihardwaredb.com/data/
```

**BibTeX:**
```bibtex
@dataset{aihardwaredb_2026_v1,
  author    = {{AIHardwareDB}},
  title     = {2026 Consumer AI Hardware 2-Year True Cost Dataset},
  year      = {2026},
  version   = {1.1.0},
  note      = {Verified 2026-11-22; CC BY 4.0},
  url       = {https://aihardwaredb.com/data/}
}
```

## Corrections & Contact

Spotted a pricing or subscription tier update? Open an issue here or email `contact@aihardwaredb.com` with the official vendor documentation URL.
