# Home Notes

Use this file for the practical details that matter in the house.

## Areas to create in Home Assistant

- entrance hall
- living room
- kitchen
- winter garden
- backyard
- shed
- toilet room
- office room
- bedroom
- Leila's bedroom
- bathroom
- attic
- boiler room

## Floor mapping

### Ground floor

- entrance hall
- living room
- kitchen
- winter garden
- toilet room
- backyard
- shed

### First floor

- office room
- bedroom
- Leila's bedroom
- bathroom

### Second floor

- attic
- boiler room

## Device inventory by area

### Entrance hall

- five Tuya spot lights
- currently bundled as one group in the Tuya app

### Living room

- couch light
- light stand
- bookshelf LED strip controlled via Broadlink remote
- Samsung TV
- KPN TV Box planned for May 1, 2026
- TV light strip planned, not yet bought
- Chromecast living room
- Honeywell Evohome with three thermostat knobs treated as one climate group

### Kitchen

- no smart devices yet
- keep as its own Home Assistant area for future expansion

### Winter garden

- its own area
- one Honeywell thermostat knob
- Tuya electric heater

### Backyard

- smart switch for outdoor lights

### Shed

- smart washing machine

### Toilet room

- presence sensor planned, not yet bought
- two Tuya lamps currently bundled as one group in the Tuya app

### Office room

- one thermostat knob
- one smart lamp

### Bedroom

- lava lamp
- one thermostat knob

### Leila's bedroom

- one thermostat knob

### Bathroom

- one thermostat knob
- Tuya extractor fan

### Attic

- one thermostat knob

### Boiler room

- non-smart Remeha central heating boiler
- Ariston heat pump boiler
- small separate nook on the second floor

## Climate layout

- living room climate is centered around Evohome plus three thermostat knobs as one climate group
- winter garden is its own climate zone
- bedroom has one thermostat knob
- Leila's bedroom has one thermostat knob
- bathroom has one thermostat knob
- office room has one thermostat knob
- attic has one thermostat knob
- boiler room contains heating equipment and is not a comfort climate zone

## Lighting and grouping recommendation

- entrance hall lights should ideally be exposed as individual bulbs in Home Assistant if possible
- toilet room lights should ideally be exposed as individual bulbs in Home Assistant if possible
- even if the bulbs are visible individually, create one Home Assistant light group per room because they are meant to act together all the time
- this keeps flexibility for troubleshooting while preserving simple room-level control

## Automation focus

### Lights

- entrance hall lighting
- living room lighting scenes
- bookshelf LED strip control
- office smart lamp behavior
- toilet room lights
- backyard outdoor lights
- future TV ambient lighting
- winter garden electric heater should stay separate from lighting logic

### Climate

- Evohome living room schedule and comfort modes
- winter garden heating logic
- bedroom temperature control
- Leila's bedroom temperature control
- bathroom heating schedule
- office room heating schedule
- attic heating schedule
- Ariston heat pump boiler monitoring and optimization

### Notifications

- washing machine finished in the shed
- heating or boiler issues
- important energy events
- maintenance reminders
- vehicle charging or battery alerts later

### Presence

- toilet room presence lighting once the sensor is installed
- later whole-house presence logic via phones or other sensors

## Integration notes

- Samsung TV should be added fresh in the new system`r`n- Honeywell Evohome should be added fresh in the new system
- Broadlink remains useful for the bookshelf LED strip
- Tuya logic should move out of the Tuya app and into Home Assistant over time
- Alexa routines should move into Home Assistant over time
- KPN TV Box will likely require fresh media setup after May 1, 2026
- winter garden electric heater should be managed in Home Assistant, not left as a Tuya-only automation

## Vehicle

- Hyundai Kona 2021 EV
- available through the Hyundai or Kia connected app environment
- candidate for Home Assistant integration after the core house setup is stable

### Possible future vehicle automations

- preheat or defrost before leaving
- charging reminders
- notify when battery is low
- notify when charging stops unexpectedly
- charging schedule coordination with energy pricing or solar production

## Future ideas

- analog water meter automated reading
- TV light strip in the living room
- toilet room presence sensor

