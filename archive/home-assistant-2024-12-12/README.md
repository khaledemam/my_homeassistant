# Home Assistant Config Snapshot - 2024-12-12

This is a sanitized reference snapshot from the extracted Home Assistant backup at:

`C:\Users\khaled\OneDrive - Inepro\Git\home-assistant\backup-review\2024-12-12\data`

It is kept as recovery/reference material for the rebuild, not as a drop-in restore.

## Included

- top-level Home Assistant YAML files
- reusable blueprints
- themes
- local image and `www` assets
- `custom_components.txt`, listing the custom integrations that existed in the backup

## Excluded

- `secrets.yaml`
- `.storage/`
- `.cloud/`
- `.ssh/`
- Home Assistant databases
- logs
- `deps/`
- `tts/`
- HACS-generated `www/community/`
- vendored `custom_components/` source code
- Alexa cookie/cache HTML files

## Sanitization

Inline credentials and private location fields in copied text files were replaced with
`!secret legacy_*` placeholders before committing.
