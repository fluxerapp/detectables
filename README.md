# detectables

Application metadata for process-based activity detection.

## Layout

- `data/detectables.json` - application names, aliases, executable match rules,
  icon paths, and optional presence asset mappings.
- `schema/detectables.schema.json` - JSON Schema for the data file.
- `assets/` - local PNG image assets referenced by the data file.
- `REUSE.toml` and `LICENSES/` - per-path licensing metadata.

## Asset Paths

Asset paths in `data/detectables.json` are relative to `assets/`.

Example:

```json
{
  "icon": "osu.png",
  "presence_assets": {
    "mode_0": "osu/mode_0.png"
  }
}
```

## Licensing

- Schema, docs, workflows, and project metadata: Apache-2.0.
- Factual mapping data in `data/`: CC0-1.0.
- Image assets in `assets/`: property of their respective owners; not licensed
  by this project.

Product and company names are used only to identify matched software. See
`LICENSE`, `NOTICE`, `TRADEMARKS.md`, and `REUSE.toml`.

## Validate

```sh
python -m pip install jsonschema reuse

python - <<'PY'
import json
from pathlib import Path

from jsonschema import Draft202012Validator

schema = json.loads(Path("schema/detectables.schema.json").read_text())
data = json.loads(Path("data/detectables.json").read_text())

Draft202012Validator.check_schema(schema)
Draft202012Validator(schema).validate(data)
PY

reuse lint
```

Rights concerns: copyright@fluxer.app.
