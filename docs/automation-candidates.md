# Automation Candidates

## Promoted into the new config structure

These have been moved into categorized Home Assistant automation files, but are disabled by default until their dependencies are stable.

- `config/automations/vehicle.yaml`
  `Kona preheat at work`
  Depends on weather, car battery sensors, plug state, and the car integration.
- `config/automations/maintenance.yaml`
  `Home Assistant auto-update`
  Kept as a disabled candidate only. Re-enable only when the new setup is stable.

## Intentionally not migrated

- `DeebotWater`
  Dropped because the Deebot hardware is no longer part of the house.
- `Daily Gas Consumption`
  This old automation looks conceptually wrong for the new setup and should be replaced by proper utility meter and Energy dashboard logic.

## Future categories agreed for the new setup

- `config/automations/lights.yaml`
- `config/automations/climate.yaml`
- `config/automations/notifications.yaml`
- `config/automations/presence.yaml`

These are intentionally present as clean placeholders so new house automations can be added in an organized way.

## Later idea

- analog water meter reading
  Worth considering later as a dedicated project once the main Home Assistant rebuild is stable.

## Rework notes

- Car automation should probably be rewritten against the maintained car integration you choose later.
- Auto-update should not be enabled on day one of the rebuilt system.
- Gas tracking should be rebuilt from real source sensors, not from the legacy automation.

## Migration principle

Only migrate an automation when all of its dependencies are already stable in the new Home Assistant OS setup.

Examples:

- do not migrate Samsung automations before Samsung is stable
- do not migrate Tuya automations before the required Tuya devices are visible in Home Assistant
- do not migrate Alexa routines blindly; translate the intent into Home Assistant first
