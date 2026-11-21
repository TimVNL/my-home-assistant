# Home Assistant configuration

The YAML portion of this installation's configuration. Secrets and runtime
state are deliberately excluded — see `.gitignore`.

## Layout

| Path | Purpose |
| --- | --- |
| `configuration.yaml` | Main entry point; defines all includes |
| `automations.yaml` | Automations created in the UI — do not hand-edit |
| `automations/` | Hand-written automations, one file per area or feature |
| `scripts.yaml`, `scenes.yaml` | UI-managed scripts and scenes |
| `packages/` | Feature- or room-based config spanning several domains |
| `themes/` | Custom themes |
| `blueprints/`, `custom_components/`, `www/` | Blueprints, custom integrations, static files |
| `zigbee2mqtt/` | Zigbee2MQTT config: `configuration.yaml` is tracked, `secret.yaml` is not |

## Secrets

Real values live in `secrets.yaml` (Home Assistant) and
`zigbee2mqtt/secret.yaml` (Zigbee2MQTT). `secrets.yaml.example` lists key names
without values. Never commit real values.

## UI-managed settings (not versioned here)

Areas, floors, labels, person, zones, dashboards, integration config entries
and the UI automations live in Home Assistant's internal storage. Back up the
instance if those need preserving.

## Editing

- Check syntax in Developer Tools → YAML before restarting.
- UI automation saves rewrite `automations.yaml`; keep existing entry IDs.
- Changes to `configuration.yaml`, `packages/` or a new include need a Core
  restart. Later edits to files in `automations/` can be reloaded.
