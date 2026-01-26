# Useful FortiGate / Network Config Snippets

This repo is a living collection of **config snippets and notes** that I’ve found useful while working on FortiGate and general network/security projects.

I’ll be updating it over time as I add more reusable templates, examples, and automation-friendly config blocks.

## Current Contents

### FortiGate Geo Address Objects (All Countries + Continents)
A ready-to-paste FortiGate CLI snippet that builds:
- `geo_<Country>` geography address objects
- Address groups for **all countries** and **continents**

This is helpful because **geo objects aren’t populated in the config by default**, but you can still use them once they exist as address objects (policies, VPN rules, etc.).

## How to Use

- Browse the folders/files and copy the snippet you need.
- Paste into your firewall (CLI console or SSH).
- Validate in the GUI under *Policy & Objects*.

## Notes
- Treat this as a reference repo — review before deploying in production.
- If you want to contribute or suggest improvements, feel free to open an issue/PR.
