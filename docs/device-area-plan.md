# Device to Area Plan

This document maps the current and planned devices into Home Assistant areas, with recommended grouping and helper patterns.

## Guiding rules

- keep devices in their real physical area
- expose individual devices to Home Assistant where possible
- create Home Assistant groups for room-level control when devices should act together
- expose room-level groups to Alexa rather than raw bulbs where possible
- keep Tuya and Alexa as edge platforms, not the source of automation logic

## Entrance hall

### Devices

- five Tuya spot lights

### Home Assistant target

- `light.entrance_hall_spot_1` through `light.entrance_hall_spot_5` if individual exposure is possible
- `light.entrance_hall` as the grouped room light

### Notes

- dashboards and voice should use `light.entrance_hall`
- automations should normally also use the grouped entity

## Living room

### Devices

- couch light
- light stand
- bookshelf LED strip via Broadlink remote
- Samsung TV
- KPN TV Box planned for May 1, 2026
- TV light strip planned for later
- Chromecast living room
- Evohome plus three thermostat knobs treated as one living room climate group

### Home Assistant target

- `light.living_room_couch`
- `light.living_room_stand`
- `light.bookshelf`
- `light.living_room_main` as a grouped light helper if desired
- `media_player.living_room_tv`
- `media_player.living_room_chromecast`
- later `media_player.living_room_kpn_tv_box`
- later `light.living_room_tv_backlight`
- `climate.living_room` created after a fresh Evohome setup

### Notes

- keep Samsung setup fresh in the new system
- media controls can later be simplified behind scripts or dashboard buttons
- living room is the richest area and will likely get scenes first

## Kitchen

### Devices

- no smart devices yet

### Home Assistant target

- area exists now for future expansion

## Winter garden

### Devices

- one Honeywell thermostat knob
- Tuya electric heater

### Home Assistant target

- `climate.winter_garden`
- `switch.winter_garden_heater` or `climate.winter_garden_heater` depending on integration behavior

### Notes

- winter garden should stay its own climate zone
- heater logic should live in Home Assistant, not in Tuya automations

## Backyard

### Devices

- smart switch for outdoor lights

### Home Assistant target

- `switch.backyard_outdoor_lights`
- optionally wrap in UI as a light if that feels more natural

## Shed

### Devices

- smart washing machine

### Home Assistant target

- device in `shed` area
- notification-oriented entity handling once the integration is known

### Notes

- likely a strong candidate for finish notifications and energy usage tracking

## Toilet room

### Devices

- two Tuya lamps
- future presence sensor

### Home Assistant target

- `light.toilet_room_1`
- `light.toilet_room_2`
- `light.toilet_room`
- later `binary_sensor.toilet_room_presence`

### Notes

- room group should be the main control entity
- this area is a good early candidate for presence-based lighting

## Office room

### Devices

- one thermostat knob
- one smart lamp

### Home Assistant target

- `climate.office_room`
- `light.office_room`

## Bedroom

### Devices

- lava lamp
- one thermostat knob

### Home Assistant target

- `light.bedroom_lava_lamp`
- `climate.bedroom`

## Leila's bedroom

### Devices

- one thermostat knob

### Home Assistant target

- `climate.leilas_bedroom`

## Bathroom

### Devices

- one thermostat knob
- Tuya extractor fan

### Home Assistant target

- `climate.bathroom`
- `fan.bathroom_extractor`

### Notes

- strong future automation candidate for humidity-based extraction

## Attic

### Devices

- one thermostat knob

### Home Assistant target

- `climate.attic`

## Boiler room

### Devices

- non-smart Remeha central heating boiler
- Ariston heat pump boiler

### Home Assistant target

- Remeha remains reference equipment unless later instrumented
- Ariston entities likely land here, for example water heater, temperatures, and power usage

### Notes

- this area is equipment-oriented, not comfort-oriented

## Vehicle

### Devices

- Hyundai Kona 2021 EV

### Home Assistant target

- vehicle integration should be added later once core house systems are stable
- keep vehicle automations separate from room automations where practical

## Recommended groups and helpers

### Light groups

- `light.entrance_hall`
- `light.toilet_room`
- optional `light.living_room_main`

### Climate grouping ideas

- `climate.living_room` created after a fresh Evohome setup as the single user-facing living room climate
- optional helper later for upstairs eco mode
- optional helper later for whole-house away mode

### Media helpers

- optional living room media scripts for TV on, TV off, watch Chromecast, and later watch KPN

## Alexa exposure recommendation

Expose these kinds of entities to Alexa:

- room light groups
- selected single lights like lava lamp
- living room media controls if useful
- selected scripts and scenes

Avoid exposing everything blindly.

## Migration order by area

1. living room
2. climate zones
3. entrance hall and toilet room lighting groups
4. backyard and shed notifications
5. bathroom fan logic
6. winter garden heater logic
7. vehicle integration later

