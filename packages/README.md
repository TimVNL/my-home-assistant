# Configuration packages

Loaded by `homeassistant.packages: !include_dir_named packages` in
`configuration.yaml`.

- One `.yaml` file per feature or room, for example `guest_mode.yaml`.
- Only `.yaml` files are scanned; each file is a mapping of top-level config
  keys, with no indentation for those keys.
- File names and keys (such as helper names) must be unique across packages
  and the main configuration.
- Never store secrets here — use `!secret` with a key in `secrets.yaml`.
