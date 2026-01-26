# FortiGate Geo Address Objects (All Countries + Continents)


This repo contains a ready-to-paste FortiGate configuration snippet that creates **geography-based firewall address objects** for countries/regions.


FortiGate includes the *geography* address-object feature, but the individual **geo address objects are not present in the config by default**. This list adds them for you so you can reference them anywhere you’d normally use address objects.


## What’s Included


- **`config firewall address`**
- Creates `geo_<CountryName>` objects using `set type geography` and the appropriate country code.
- **`config firewall addrgrp`**
- `all_countries` group (everything)
- Continent groups (e.g., **European**, **African**, **Asian**, **North_American**, **South_American**, **Oceanian**, and **Antarctic**)


## How to Use


1. Copy the config snippet from this repo.
2. Paste it into your FortiGate CLI:
- **GUI:** *Dashboard → CLI Console*
- **SSH:** connect to the firewall and paste the config
3. Verify the objects:
- Firewall Address Objects: `Policy & Objects → Addresses`
- Address Groups: `Policy & Objects → Addresses → Address Groups`


## Common Use Cases


- Geo-blocking inbound or outbound traffic in firewall policies or  local-in policies
- Restricting VPN access by source country/region
- Building “allow-list” or “deny-list” policies by continent or country


## Notes


- Test in a lab or maintenance window if you’re adding a large number of objects to a production firewall.
- If you already have objects with the same names, you may want to rename or remove duplicates before pasting.


## License


Use freely — modify as needed for your environment.
