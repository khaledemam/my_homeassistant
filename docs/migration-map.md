# Migration Map

## Goal

Use the old backup as reference only and rebuild the real integrations fresh on a new clean Home Assistant OS installation.

## Keep and refactor

These are worth bringing into the new setup, but not blindly.

- automations and scripts that still match the house and devices
- scenes that still map to real rooms and devices
- themes if you still like them
- `www` assets and cards you still use
- selected blueprints you still trust
- planning documents, area model, and room/device notes

## Recreate fresh

These should be set up again from scratch in the new Home Assistant OS install.

- Samsung TV
- Honeywell Evohome
- DSMR
- Enphase or solar integrations
- Tuya
- Alexa-related integrations
- mobile app registrations
- HACS
- local network discovery integrations
- printer, cast, Bluetooth, and similar device entries

## Keep as data or reference

These are valuable, but should not be imported blindly into the new running system.

- `home-assistant_v2.db`
- `.storage/energy`
- `.storage/lovelace*`
- `.storage/core.area_registry`
- `.storage/core.entity_registry`
- `.storage/core.device_registry`

## Do not restore blindly

These are likely to bring back clutter, machine-specific problems, or stale credentials.

- `.storage/core.config_entries`
- `.storage/auth*`
- `.storage/http*`
- `.storage/hassio`
- `tts/`
- logs, temp files, and database size sensors
- Raspberry Pi specific integrations and system entries
- all old integration credentials and tokens

## Energy strategy

- keep the old database as an archive
- recreate DSMR and solar integrations fresh
- recreate the Energy dashboard cleanly using the new entities
- preserve the energy model, not the old integration setup
- decide later whether to import old long-term statistics

## First migration order

1. Fresh Home Assistant OS install
2. Day-one apps and access tools
3. Fresh DSMR integration
4. Fresh Enphase or solar integration
5. Fresh Evohome setup
6. Fresh Tuya and other critical integrations
7. Energy dashboard setup
8. HACS install
9. Fresh Samsung setup later when the base system is stable
10. Automations and scripts in small batches

## Automation ownership

- Alexa and Tuya automations are legacy logic
- move the useful ones into Home Assistant
- once validated in Home Assistant, disable duplicates in Alexa and Tuya
