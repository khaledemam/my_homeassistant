# Secrets Guide

## Rule

Anything private goes into `secrets.yaml`, not into `configuration.yaml`, automations, scripts, or dashboards.

## Examples of secrets

- usernames
- passwords
- API keys
- OAuth tokens
- webhook IDs
- GPS coordinates if you want to keep them private
- internal hostnames that you do not want exposed publicly

## Recommended pattern

In YAML:

```yaml
evohome:
  username: !secret evohome_username
  password: !secret evohome_password
```

Another example:

```yaml
sensor:
  - platform: solaredge_local
    name: SolarEdge
    ip_address: !secret solaredge_host
```

## Files

- `config/secrets.example.yaml`: safe template for tracked placeholders
- `config/secrets.yaml`: real secrets on the Home Assistant machine only

## Important note

The extracted old backup contains plain credentials and tokens in multiple files. Those should be treated as compromised history and gradually rotated where possible.
