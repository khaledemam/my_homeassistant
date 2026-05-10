# Enphase Solar Dashboard

This dashboard is based on the Enphase Envoy entities observed on 2026-05-10.

## Source entities

- `sensor.envoy_122311014773_current_power_production`
- `sensor.envoy_122311014773_energy_production_today`
- `sensor.envoy_122311014773_energy_production_last_seven_days`
- `sensor.envoy_122311014773_lifetime_energy_production`
- `sensor.inverter_482316030201`
- `sensor.inverter_482316031047`
- `sensor.inverter_482316031052`
- `sensor.inverter_482316031085`
- `sensor.inverter_482316031090`
- `sensor.inverter_482316031093`
- `sensor.inverter_482316031110`
- `sensor.inverter_482316031163`

## Added helpers

`config/packages/enphase_solar.yaml` adds helper sensors for:

- 7-day average production
- today compared with the 7-day average
- total inverter power
- active inverter count
- average active inverter power
- inverter imbalance percentage
- a problem binary sensor when imbalance is high during production

## Dashboard

`config/dashboards/solar_enphase.yaml` adds a Solar dashboard with:

- live production
- today, 7-day average, and lifetime totals
- 14-day daily trend
- microinverter tiles
- inverter health and imbalance alerting
