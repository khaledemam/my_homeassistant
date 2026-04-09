# Automation Strategy

## Rule of the house

Home Assistant is the single source of truth for automations.

## What Alexa should do

- voice assistant access
- expose selected Home Assistant entities
- simple voice interaction only

Alexa should not be the place where important house logic lives.

## What Tuya should do

- device onboarding if needed
- firmware updates if needed
- vendor-only recovery actions

Tuya should not be the place where important house logic lives.

## What Home Assistant should do

- schedules
- presence-based logic
- climate routines
- energy logic
- lighting scenes
- notifications
- cross-device coordination

## File structure

- `config/automations/`
  YAML lists grouped by topic, room, or system
- `config/scripts/`
  reusable actions that can be called by automations, dashboards, or voice
- `config/packages/`
  integration-level config such as energy, waste, climate, and system helpers

## Suggested grouping

- `automations/climate.yaml`
- `automations/energy.yaml`
- `automations/lights.yaml`
- `automations/media.yaml`
- `automations/notifications.yaml`
- `automations/presence.yaml`
- `automations/maintenance.yaml`

## Migration rule

When moving an automation from Alexa or Tuya to Home Assistant:

1. identify the trigger
2. identify the devices and entities involved
3. identify any timing or safety rules
4. rebuild it in Home Assistant
5. disable the original Alexa or Tuya automation after validation

## Naming rule

Use clear aliases that say what the automation does, for example:

- `Hallway lights on after sunset`
- `Notify when washing machine finishes`
- `Preheat car on cold workdays`

## Design rule

- helpers store intent or mode
- scripts hold reusable actions
- automations orchestrate triggers and conditions
- dashboards control and observe, but should not contain hidden logic

## Safety rule

Do not run the same house behavior from multiple platforms at the same time.

If Home Assistant owns an automation, disable the duplicate in Alexa or Tuya.
