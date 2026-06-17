# Changelog

All notable changes to sIATC are documented here. The format follows
[Keep a Changelog](https://keepachangelog.com/), and the `version` field of the
`.siatc.json` save format is bumped only on incompatible changes.
# Changelog

All notable changes to sIATC will be documented in this file.

This repository begins with public release `v1.2.0`. Earlier versions `v1.0.0` and `v1.1.0` were developed before repository publication and are recorded here for continuity, but are not separately archived as GitHub or Zenodo releases.

The format is inspired by [Keep a Changelog](https://keepachangelog.com/), and this project uses semantic versioning where practical.

## [1.2.0] - 2026-06-17

DOI: https://doi.org/10.5281/zenodo.20733182

First public, DOI-ready release of sIATC.

Although this is the first GitHub release, the version number starts at `v1.2.0` because two earlier pre-publication versions were developed before repository publication.

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

