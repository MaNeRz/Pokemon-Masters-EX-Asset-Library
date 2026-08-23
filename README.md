# Pokémon Masters EX Asset Library

A human-readable asset library for **Pokémon Masters EX**.

## Current release

- Library version: [`v1.1.1`](https://github.com/MaNeRz/Pokemon-Masters-EX-Asset-Library/releases/tag/v1.1.1)
- Game data version: `2.71.1`
- Canonical PNG assets: **27,419**
- Namespaced aliases: **13,144**
- Canonical READY assets: **27,266**
- Canonical HOLD assets: **153**
- Standalone UI assets tracked with Git LFS: **19,298**

### What changed in v1.1.1

`v1.1.1` is a navigation-only patch over `v1.1.0`.

No PNG content, PNG SHA256, `UnifiedAssetId`, or alias target changed.
High-cardinality UI directories were reorganized into semantic/source-derived
subfolders so the repository remains fully browsable through GitHub's web UI.

At the `v1.1.1` release boundary:

- directories with more than 1,000 direct entries: **0**
- directories in the 800–1,000 growth-risk band: **0**

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

Large UI domains use an additional navigation layer where necessary:

- Trainer assets are grouped by trainer identity/name
- Pokémon assets are grouped by their exact published human-readable name
- Item UI assets are grouped by technical item family
- Scout and Scout-banner assets are grouped by source-derived scout family

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

The **19,298 standalone UI canonical assets** are tracked with Git LFS.
The Item + Atlas payload from the original library remains normal Git content.

For bulk use, download the release assets instead of cloning individual files:

- `Pokemon-Masters-EX-Asset-Library-v1.1.1-Items-Atlas.zip`
- `Pokemon-Masters-EX-Asset-Library-v1.1.1-Standalone-UI.zip`

## Integrity

`SHA256SUMS.txt` covers every public file except the checksum file itself.

The public Git repository is the canonical navigable library; GitHub Releases
provide versioned bulk-download packages.
