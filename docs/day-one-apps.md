# Day One Apps

These are the first Home Assistant OS apps or add-ons I would consider on day one.

## Install first

### SSH access

Choose one of these, not both:

- Official `SSH server`
  Good if you want a simple official option.
- Community `Advanced SSH & Web Terminal`
  Best if you want a stronger terminal workflow and likely the most useful path for working with Codex later.

## Very useful early

- `Samba share`
  Useful for easy file access from Windows.
- `File editor`
  Optional fallback for quick edits in the browser.

## Useful a bit later

- `Git pull`
  Useful later if you want Home Assistant to pull config from Git directly.
- `MariaDB`
  Only later if you outgrow the default database approach.
- `Mosquitto broker`
  Only if you actually need MQTT devices or services.

## Backup option

- `Home Assistant Google Drive Backup`
  Community add-on, useful if you want off-device backups in Google Drive.

## Recommendation for your setup

My suggested order:

1. `Advanced SSH & Web Terminal`
2. `Samba share`
3. `Home Assistant Google Drive Backup`
4. `File editor` only if you still want a browser editor after SSH is working

## Notes

- do not install too many add-ons on day one
- focus first on access, backup, and core integrations
- add optional tooling only after the base system is stable

## Sources

- Official Home Assistant apps repository: https://github.com/home-assistant/addons
- Home Assistant Community Add-ons repository: https://github.com/hassio-addons/repository
- Advanced SSH & Web Terminal: https://github.com/hassio-addons/addon-ssh
- Home Assistant Google Drive Backup: https://github.com/sabeechen/hassio-google-drive-backup
