# Contributing to sIATC

sIATC is built in the spirit of the sIfA project: a tool meant to travel, be
adapted, and improved through collective reflection. Contributions are welcome.

## Ways to help
- **Refine the taxonomy.** The nine stages and their definitions are the heart
  of sIATC. If a stage is unclear, overlapping, or missing for the kinds of
  content you produce, open an issue describing the case.
- **Improve the tool.** Bug fixes, accessibility improvements, and export
  options are all useful. Keep the single-file, build-step-free architecture.
- **Translate the interface.** sIATC is about written content in any language;
  a localized UI is a natural fit.

## Ground rules
- Keep the figure honest. sIATC's whole point is reflection, not precision:
  resist adding false granularity (see the whole-number extent decision in
  `CHANGELOG.md`).
- Preserve attribution. sIATC is an Apache-2.0 derivative of sIfA. Keep the
  `LICENSE`, `NOTICE`, and the in-file header comment intact, and mark any files
  you change (a short "modified by …" note is enough).
- The brain artwork is (c) Mareike Schomerus / Busara — leave its attribution in
  place.

## Making changes
1. Edit `siatc.html` (the `BRAND` object and `ROLES` array near the top of the
   script are the usual entry points).
2. Rebuild the offline file: `python3 embed-libraries.py`.
3. Note your change in `CHANGELOG.md`.
4. If you change the save format, update `siatc.schema.json` and `SCHEMA.md`,
   and bump `version` only if the change is incompatible.
