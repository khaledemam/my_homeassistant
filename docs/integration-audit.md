# Integration Audit

## Rule

All real integrations should be added fresh on the new Home Assistant OS system.

The old backup is reference material only.

## Recreate early

These are core to the house and likely worth bringing back relatively early.

- `dsmr`
  Important for electricity and gas readings.
- `enphase_envoy`
  Important if you want solar production and Energy dashboard continuity.
- `evohome`
  Important for heating, but it should be added fresh during setup.
- `mobile_app`
  Reconnect fresh per device.
- `hacs`
  Install fresh, then re-add only needed custom integrations.

## Recreate later

Useful, but not day-one critical.

- `tplink_deco`
- `broadlink`
- `forecast_solar`
- `buienradar`
- `localtuya` or `tuya`
- `alexa_media`
- `picnic`
- `ariston`
- `sonoff`
- `kia_connect` or `kia_uvo`

## Fresh-only integrations called out explicitly

- `Samsung TV`
  Add fresh later after the base system is stable.
- `Honeywell Evohome`
  Add fresh during setup; do not carry over old YAML credentials or config.
- `Tuya`
  Reconnect the environment fresh and gradually move automation logic into Home Assistant.
- `Alexa`
  Reconnect only what is useful and treat Alexa as a voice layer, not the automation brain.

## Probably outdated or should be challenged

These are not necessarily wrong, but they should not be trusted without checking current maintenance and compatibility.

- `dwains_dashboard`
- `ui_lovelace_minimalist`
- `config_editor`
- `rpi_gpio`
- `rpi_power`
- `raspberry_pi`
- `cpuspeed`
- `filesize`
- `speedtestdotnet`
- `fastdotcom`
- `systemmonitor`

## Recommended rule

Only add back an integration if it is:

- still useful in the house
- actively maintained
- compatible with the current device or service
- simpler than the alternatives
