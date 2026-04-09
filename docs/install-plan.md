# Install Plan

## Goal

Run Home Assistant OS on a reliable always-on machine for the house.

## Chosen hardware

- device: Lenovo ThinkCentre M710q Tiny
- CPU: Intel Core i5 2.2 GHz class CPU
- RAM: 16 GB
- storage: 256 GB SSD
- network connection: wired Ethernet preferred

## Before it arrives

- have a monitor and keyboard ready for the first boot if needed
- have an Ethernet cable ready
- keep the Home Assistant backup file available
- prepare a USB stick for the Home Assistant OS installer
- keep your phone or laptop ready to access `http://homeassistant.local:8123`

## Arrival day checklist

1. Check that the box includes the power adapter.
2. Connect the machine to Ethernet.
3. Power it on and confirm it reaches BIOS or boots normally.
4. If the seller-installed OS is present, that is fine. We will replace it.
5. Download the Home Assistant OS image for Generic x86-64 on another computer.
6. Flash the image to the internal SSD using the official install method.
7. Boot the machine into Home Assistant OS.
8. Wait until Home Assistant finishes first startup.
9. Open `http://homeassistant.local:8123` or the device IP address.
10. Restore the December 12, 2024 backup if the system offers restore during onboarding.
11. Let Home Assistant settle before judging broken integrations.
12. Re-check HACS and custom integrations one by one.

## After first restore

- confirm dashboards load
- confirm mobile app reconnects
- confirm important devices appear
- confirm automations are present
- check logs for custom integration failures
- update only one thing at a time in the beginning

## Good practices

- keep the machine on a stable power source
- prefer wired Ethernet over Wi-Fi
- keep at least tens of GB of free SSD space
- use Google Drive for backups, not for the live database
- use this repo for notes and important config files

## Restore notes

Use this section to track what came back cleanly from backup and what needed manual fixes.

- backup used: Full Backup 2024-12-12 12:56:31.tar
- restore date:
- issues found:
- fixes applied:

## Day-one apps

See `docs/day-one-apps.md` for the first apps or add-ons to install once Home Assistant OS is up.
