# Hand-written automations

Loaded by `automation manual: !include_dir_merge_list automations/` in
`configuration.yaml`.

- One file per area or feature, for example `living_lights.yaml`.
- Only `.yaml` files are scanned (not `.yml`); they merge in filename order.
- Each file is a YAML list of automations, starting at column 0:
  `- id: unique_id` followed by `alias`, `triggers`, `conditions`, `actions`
  and `mode`.
- UI-created automations belong in `automations.yaml`, not here.
- Keep IDs unique and stable; changing an ID creates a new automation.
