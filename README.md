# Rumbo: Camp for Free in Oregon

What if I told you there were still pockets of wilderness you can camp at without giving a single dollar to the man? Rumbo (Spanish for heading or direction) is a simple, phone-friendly web map that shows the BLM land in Oregon you can dispersed camp on. It's built in Rust.

## Why

Dispersed camping on public land is free and legal for ~14 days at a time, but figuring out where you can go is on you. The BLM's own map is the best free option right now. It can't pinpoint lat/long, its colors are hard to tell apart, and you can't switch base maps. onX and Gaia GPS do it better, but they sit behind paywalls and logins. The underlying data is free straight from the BLM, so I think we can do better.

## Goals

- [ ] Axum server that queries the BLM's MapServer for BLM land
- [ ] Render that land on a static OpenStreetMap base map
- [ ] Toggle between a cartographic and a satellite base map
- [ ] Pinpoint lat/long on points of interest
- [ ] Show road segments to help plan access
- [ ] Save points and export them to apps like Google Maps

## Running it (in theory)

```bash
git clone https://github.com/<your-username>/rumbo.git
cd rumbo
cargo run
```

## Data

- BLM land status: [BLM_OR_Ownership MapServer](https://gis.blm.gov/orarcgis/rest/services/Land_Status/BLM_OR_Ownership/MapServer)
- Base map: © [OpenStreetMap](https://www.openstreetmap.org/) contributors

Rumbo shows you where BLM land is, not whether a spot is open. Check posted closures and [fire restrictions](https://www.blm.gov/orwafire) before you head out.

## License

Licensed under either of [Apache License, Version 2.0](LICENSE-APACHE) or [MIT license](LICENSE-MIT) at your option.

Unless you explicitly state otherwise, any contribution intentionally submitted for inclusion in the work by you, as defined in the Apache-2.0 license, shall be dual licensed as above, without any additional terms or conditions.

---

*DISCLOSURE: this README was written with the assistance of the Claude LLM*
