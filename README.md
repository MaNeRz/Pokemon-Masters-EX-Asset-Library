# Pokémon Masters EX Asset Library

A human-readable asset library for **Pokémon Masters EX**.

Release `v1.1.0` expands the original Item + atlas library with
standalone UI textures while preserving every canonical and alias identity
published in `v1.0.0`.

## Release

- Library version: `v1.1.0`
- Game data version: `2.71.1`
- Canonical PNG assets: **27,419**
- Namespaced aliases: **13,144**
- Canonical READY assets: **27,266**
- Canonical HOLD assets: **153**

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

The `v1.1.0` expansion does not change the identity or metadata of
any canonical asset or alias already published in `v1.0.0`.

## Integrity

`SHA256SUMS.txt` covers every public file except the checksum file itself.

For bulk downloads, use the release assets rather than a full Git LFS clone.
