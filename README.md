<div align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="branding/pinstash-wordmark-on-dark.png">
    <img src="branding/pinstash-wordmark-on-light.png" alt="Pinstash" width="460">
  </picture>

  <p><strong>Pin it. Stash it. Keep it yours.</strong></p>

  <img src="https://img.shields.io/badge/status-v0.1%20%28in%20development%29-FFB703?style=flat-square" alt="status"> <img src="https://img.shields.io/badge/platform-iOS%2017%2B-0B3C49?style=flat-square" alt="platform"> <img src="https://img.shields.io/badge/license-proprietary-555555?style=flat-square" alt="license"> <img src="https://img.shields.io/badge/by-Aquila%20Digital%20LLC-14213D?style=flat-square" alt="Aquila Digital LLC">
</div>

> **Showcase repository.** The source code for Pinstash is not published. This page presents what the product is and how it works.

## Overview

A private log for fishing and hunting spots. Drop a pin on the map or use your current location, save the spot with the conditions, and note what worked. Everything stays on the phone.

## How it works

```mermaid
flowchart LR
  A["Long-press the map, search, or paste a map link"] --> B["Save name, type, notes, tags"] --> C["Moon phase computed on-device; weather + pressure if opted in"] --> D["Find the spot again with the conditions that made it work"] --> E["Share one spot as a .pinstash file, only when you choose"]
```

## Features

- Topographic map: Standard, USGS Topo, Satellite, shaded relief, plus a reference-only public-land layer
- Paste Google/Apple Maps links or typed coordinates
- GPX and KML import/export with a review step
- Password-protected backup and restore (PBKDF2 + AES-GCM)
- Opt-in weather and pressure from the US National Weather Service
- App-switcher privacy cover, offline banner, versioned on-device database
- Local profile only, no cloud account

## Tech stack

| Layer | Choice |
|---|---|
| Language / UI | Swift, SwiftUI, SwiftData, iOS 17+ |
| Maps | MapKit + USGS topo tiles |
| Weather | api.weather.gov (opt-in) |
| Crypto | Apple CryptoKit |
| Tests | PinstashTests |

## Privacy & security

Spots are never uploaded. No account, no analytics, no third-party SDKs. Sharing is user-initiated and server-free.

## Brand

| | Name | Hex | Role |
|---|---|---|---|
| <img src="https://placehold.co/44x22/0B3C49/0B3C49.png" alt="#0B3C49" /> | Deep Water | `#0B3C49` | Icon field, text, dark surfaces |
| <img src="https://placehold.co/44x22/FFB703/FFB703.png" alt="#FFB703" /> | Gold | `#FFB703` | Pin, accent, key actions |
| <img src="https://placehold.co/44x22/5CC8E8/5CC8E8.png" alt="#5CC8E8" /> | Ripple | `#5CC8E8` | Water rings, accents on dark |
| <img src="https://placehold.co/44x22/FFF4D6/FFF4D6.png" alt="#FFF4D6" /> | Sand | `#FFF4D6` | Light surfaces |

**Mark.** A gold map pin with a keyhole cutout over water ripples: a private spot, locked away and kept yours.

**Voice.** Quiet and discreet, like a fishing buddy who keeps a secret. Plain words. Never imply anything is shared or uploaded.

## Roadmap

- Subscription via StoreKit 2 (free core, Pro: weather, offline topo, land layer)
- Offline topo maps
- Share-sheet extension
- Accessibility audit

## License

Proprietary. Shared publicly for portfolio and demonstration purposes only. See [LICENSE](LICENSE).

---

<div align="center">

Built by [Aquila Digital LLC](https://github.com/Steven6Brown) · *Per Aspera Ad Astra*

</div>
