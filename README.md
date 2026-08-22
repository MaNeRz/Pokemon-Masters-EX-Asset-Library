# Pokémon Masters EX Asset Library

A human-readable asset library for **Pokémon Masters EX**.

This repository organizes standalone item images and atlas-derived UI sprites
into semantic folders while preserving machine-readable asset identities,
aliases, status, and SHA256 hashes.

## Release

- Library release: `v1.0.0`
- Game data version: `2.71.1`
- Canonical PNG assets: `8,121`
- Aliases: `8,663`

## Structure

```text
Items/
UI/
data/
```

### `Items/`

Standalone item assets grouped into semantic item categories.

### `UI/`

UI sprites extracted from atlases, normalized for orientation and exact visual
duplicates, then organized by interface context and visual family.

### `data/assets.csv`

Canonical asset index for every public PNG.

### `data/aliases.csv`

Namespaced aliases that point to canonical public assets.

Alias namespaces currently include:

- `ITEM_ID`
- `ATLAS_LOGICAL`

### `data/status-summary.csv`

Summary of `READY` and `HOLD` states.

`READY` / `HOLD` is metadata only; the filesystem is organized semantically.

### `data/provenance.json`

Release-level provenance and product contract.

## Integrity

`SHA256SUMS.txt` contains a SHA256 entry for every tracked public file except
the checksum file itself.

## Versioning

Repository releases follow normal semantic release numbering beginning at
`v1.0.0`. The game-data version used to build a release is recorded separately.
