# The `.siatc.json` file format

A `.siatc.json` file is the portable export of an sIATC statement. It records,
for one piece of written content, how much AI was involved at each of the nine
stages — enough for the record to be re-read, compared, or validated long after
the original session.

A formal JSON Schema lives at [`siatc.schema.json`](./siatc.schema.json),
written against JSON Schema **draft 2020-12**. It works with any compatible
validator (`check-jsonschema`, `ajv`, `python-jsonschema`). The schema file is
the source of truth; this document is the friendly overview.

## What a file looks like

```json
{
  "tool": "sIATC",
  "basedOn": "sIfA Tool (Schomerus/Busara), Apache-2.0",
  "version": 1,
  "kind": "siatc-statement",
  "savedAt": "2026-06-15T12:00:00.000Z",
  "title": "Launch announcement, Aug 2026",
  "author": "Luis Ferreira",
  "stages": [
    { "id": "conception", "label": "Conception & Angle", "applicable": true,  "extent": 1, "tool": "Claude", "note": "brainstormed angles" },
    { "id": "translation", "label": "Translation",       "applicable": false, "extent": 0, "tool": "", "note": "" }
  ]
}
```

## Top-level fields

| Field | Required | Notes |
| --- | --- | --- |
| `version` | yes | Schema major version. Currently `1`. Bumped only on incompatible change. |
| `kind` | yes | Always `"siatc-statement"`. Lets a file be recognised without its extension. |
| `savedAt` | yes | ISO 8601 timestamp. Informational. |
| `stages` | yes | One entry per content stage (a full statement has all nine). |
| `title` | no | Title of the piece. |
| `author` | no | Who takes responsibility for the content. |
| `tool`, `basedOn` | no | Informational provenance strings. |

## The stage object

| Field | Required | Notes |
| --- | --- | --- |
| `id` | yes | One of: `conception`, `research`, `structure`, `drafting`, `editing`, `revision`, `translation`, `verification`, `visuals`. |
| `extent` | yes | Integer `0`–`2`. `0` = no AI; `1` = some; `2` = extensive. |
| `applicable` | no | `false` when the stage did not happen for this piece (e.g. a monolingual piece has no Translation). When `false`, `extent` is `0` and the stage is dropped from the figure. |
| `label` | no | Human-readable stage name. |
| `tool` | no | AI tool/service used (e.g. `Claude`, `DeepL`). |
| `note` | no | Short audit-trail note on how AI was used. Recommended when `extent > 0`. |

## The key distinction the format protects

`extent: 0` with `applicable: true` means **a human did this stage, with no AI**.
`applicable: false` means **the stage never happened**. Conflating the two would
make a simple blog post and a fully translated report look the same; keeping them
apart is the reason Translation and Visuals are their own stages rather than
folded into Editing.

## Versioning

`version` is a major version. Additive changes (new optional fields) do not bump
it. Renames, removals, or a changed extent scale do — and an older reader should
refuse a newer file rather than load it partially.

## Validating a file

```bash
# Python
pip install check-jsonschema
check-jsonschema --schemafile siatc.schema.json my-piece.siatc.json

# Node
npx ajv-cli validate -s siatc.schema.json -d my-piece.siatc.json --spec=draft2020
```
