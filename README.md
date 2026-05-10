# Home Assistant

This repository is for the Home Assistant setup for my house.

The Home Assistant system itself will run on Home Assistant OS. This repo is the place to keep the important configuration, notes, and setup history so the house is easier to maintain over time.

## What belongs here

- key YAML configuration from `/config`
- automation, script, and scene files
- notes about devices, rooms, and integrations
- HACS and custom integration notes
- install and recovery checklists

## What does not belong here

- secrets
- large backups
- database files
- logs
- temporary files

Those are ignored in `.gitignore`.

## Current structure

- `config/`: Home Assistant YAML files we want to keep under version control
- `config/dashboards/`: YAML dashboards that should be reproducible after reinstall
- `config/packages/`: package-level helpers, utility meters, and integration logic
- `docs/install-plan.md`: practical setup steps for the Home Assistant OS machine
- `docs/home-notes.md`: house-specific notes, devices, and integration ideas

## Working style

This repo is meant to stay simple:

1. keep only the files we actually want to understand and maintain
2. avoid committing secrets or noisy runtime files
3. document custom integrations and HACS choices
4. make future recovery easier without turning this into a complicated project

## Next steps

1. choose the machine for Home Assistant OS
2. install Home Assistant OS
3. restore the last backup carefully
4. bring custom integrations back one by one
5. copy the important YAML and notes into this repo
