# Pokémon Masters EX Asset Library

A human-readable asset library for **Pokémon Masters EX**.

## Current release

- Release: [v1.1.3](https://github.com/MaNeRz/Pokemon-Masters-EX-Asset-Library/releases/tag/v1.1.3)
- Game data: `2.71.1`

For version-specific changes, checksums, and bulk downloads, see the linked GitHub Release.

## Asset sources

- standalone Item images
- atlas-derived UI sprites
- standalone UI textures

## Structure

```text
Items/
UI/
data/
```

`READY` / `HOLD` is metadata only. The filesystem is organized by semantic
object/interface context.

Large UI domains use additional navigation layers where necessary:

- Trainer assets are grouped by Trainer identity and human-readable variant name.
- Pokémon assets are grouped by their exact published human-readable name.
- Item UI assets are grouped by technical item family.
- Scout and Scout-banner assets are grouped by source-derived scout family.

These navigation folders do not change stable asset identity.

## Data

- `data/assets.csv` — canonical public PNG index
- `data/aliases.csv` — namespaced aliases to canonical assets
- `data/status-summary.csv` — READY/HOLD counts
- `data/standalone-ui-source-identities.csv` — original standalone UI source
  identities and final representation targets
- `data/provenance.json` — release/product contract

## Stable identity

Canonical assets use `UnifiedAssetId`.

Aliases use the composite identity:

`AliasNamespace + AliasId`

Public paths may evolve to improve navigation. Stable IDs, source provenance,
and content hashes are the durable identity layer.

## Git LFS and bulk downloads

The **19,298** standalone UI canonical assets are tracked with Git LFS.
The Item + Atlas payload remains normal Git content.

For bulk use, download the release assets instead of cloning individual files:

- `Pokemon-Masters-EX-Asset-Library-v1.1.3-Items-Atlas.zip`
- `Pokemon-Masters-EX-Asset-Library-v1.1.3-Standalone-UI.zip`

## Integrity

`SHA256SUMS.txt` is the repository checksum manifest for the public payload
surface. The checksum file itself and repository-control files such as
`.gitattributes` are intentionally outside its self-checking membership.

The public Git repository is the canonical navigable library; GitHub Releases
provide versioned bulk-download packages.
