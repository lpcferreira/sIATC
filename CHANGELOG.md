# Changelog

All notable changes to sIATC are documented here. The format is inspired by
[Keep a Changelog](https://keepachangelog.com/), and this project uses semantic
versioning where practical. The `version` field of the `.siatc.json` save format
is bumped only on incompatible changes.

This repository begins with public release `v1.2.0`. Earlier versions `v1.0.0`
and `v1.1.0` were developed before repository publication and are recorded here
for continuity, but are not separately archived as GitHub or Zenodo releases.

## [1.3.0] - 2026-06-17

### Added

* Load a previously exported `.siatc.json` file back into the tool. A new
  **Load .siatc.json** button restores every field — title, author, and each
  stage's extent, AI tool, and note — so an assessment can be revised or
  continued without re-entering it. The interface switches automatically to the
  language recorded in the file, and because stages are keyed by a stable
  identifier, a file saved in one language loads correctly regardless of the
  interface language. Loading is fully browser-local: the chosen file is read on
  the device and nothing is uploaded or sent to a server.
* Validation on load: files that are not valid JSON, are not sIATC statements
  (the `kind` discriminator is checked case-insensitively), or were produced by a
  newer save-format version are rejected with a clear message instead of loading
  partial data. Out-of-range or missing stage values fall back to safe defaults.

## [1.2.2] - 2026-06-17

### Fixed

* Long titles and subtitles no longer overflow or get clipped in the exported
  figure (SVG and PNG). The title and the tool name now wrap onto multiple lines
  according to the available width, and the export canvas grows in height to fit
  the wrapped header instead of using a fixed height. This previously cut off
  the full tool name and longer piece titles at the image edges.

## [1.2.1] - 2026-06-17

### Fixed

* Corrected the tool's full name in the page header, the browser tab title, and
  the exported figure caption (SVG/PNG) so it matches the official sIATC name in
  all three languages:
  * English — Statement of Intellectual Accountability and Transparency for
    Artificial Intelligence use for Content Development
  * Portuguese — Declaração de Responsabilidade Intelectual e Transparência no
    Uso de IA em Conteúdo
  * Spanish — Declaración de Responsabilidad Intelectual y Transparencia en el
    Uso de IA en Contenidos

## [1.2.0] - 2026-06-17

DOI: https://doi.org/10.5281/zenodo.20733182

First public, DOI-ready release of sIATC.

Although this is the first GitHub release, the version number starts at `v1.2.0`
because two earlier pre-publication versions were developed before repository
publication.

### Added

* Translation into Portuguese and Spanish.
* Language selector at the top of the page.
* Trilingual reflection guide in English, Portuguese, and Spanish.
* Public-release documentation for GitHub and Zenodo publication.
* Repository-level materials for citation, attribution, licensing, and version tracking.

### Notes

* This is the first release intended for GitHub publication.
* This is the first release intended for Zenodo archival and DOI assignment.
* Earlier versions are documented below but are not separately archived.

## [1.1.0] - Pre-publication

Internal working version.

### Changed

* Fixed PNG export behavior.
* Fixed SVG export behavior.

### Notes

* These fixes were made after the initial sIATC adaptation and before public repository publication.
* This version was not separately released through GitHub or archived through Zenodo.

## [1.0.0] - 2026-06-15

Initial internal release.

sIATC is adapted from the sIfA Tool by Jan Schomerus and Busara, released under the Apache License 2.0, and reworked for written, visual, editorial, and communicative content.

### Added

* Nine-stage content taxonomy, each with a definition and interaction examples:

  * Conception & Angle
  * Research & Sourcing
  * Structure
  * Drafting
  * Editing & Refinement
  * Revision
  * Translation
  * Fact-checking & Verification
  * Visuals & Design
* Single-author self-assessment, using a `0 / 1 / 2` extent control per stage.
* Per-stage `not applicable` setting, which removes the axis from the figure so that extent `0` specifically means "done by a human, no AI", distinct from a stage that never happened.
* Live brain figure that rebalances across whatever stages are active.
* Export of the figure as SVG.
* Export of the figure as PNG.
* Export of the assessment data as `.siatc.json`.
* `siatc.schema.json`, using JSON Schema draft 2020-12, to describe the save format.

### Changed from upstream sIfA

* Replaced the 14-role CRediT taxonomy with the nine content stages above.
* Removed the guided chatbot.
* Removed the Sole / Lead / Equal / Support contributor-weighting flow.
* Replaced the half-step extent values used in sIfA with whole numbers only.
* Enforced integer extent values from `0` to `2` in the schema.

### Attribution

* sIATC is adapted from the sIfA Tool by Jan Schomerus and Busara, released under the Apache License 2.0.
* The brain-figure artwork is reused verbatim from sIfA under the Apache License 2.0.
* The staged reflection approach is adapted for content work while preserving credit to the original sIfA materials.
