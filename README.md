# Pokémon Masters EX Asset Library

A human-readable asset library for **Pokémon Masters EX**.

## Current release

- Library version: `v1.1.2`
- Game data version: `2.71.1`
- Canonical PNG assets: **27,419**
- Namespaced aliases: **13,144**
- Canonical READY assets: **27,266**
- Canonical HOLD assets: **153**
- Standalone UI assets tracked with Git LFS: **19,298**

### What changed in v1.1.2

`v1.1.2` is a human-readable Trainer naming patch over `v1.1.1`.

- **4,507** canonical Trainer public paths were renamed.
- All **536** published Trainer variants now have a human-readable Trainer name.
- **220** variants use exact local `trainer_verbose_name` evidence.
- **9** additional specialized names use exact local CharaQuest evidence.
- **307** variants retain their proven base Trainer name.
- **1,844** standard Trainer emote assets now expose their proven BattleStamp labels:
  `Nice!`, `Watch out!`, `Let's do this!`, and `Thanks!`.
- Technical variant tails such as `01`, `02`, `expose`, and `01_expose` remain
  preserved where their exact in-game semantic label is not proven.

This patch changes **public navigation paths only**. PNG bytes, PNG SHA256,
`UnifiedAssetId`, source identity, and alias targets are unchanged.

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

- `Pokemon-Masters-EX-Asset-Library-v1.1.2-Items-Atlas.zip`
- `Pokemon-Masters-EX-Asset-Library-v1.1.2-Standalone-UI.zip`

## Integrity

`SHA256SUMS.txt` is the repository checksum manifest for the public payload
surface. The checksum file itself and repository-control files such as
`.gitattributes` are intentionally outside its self-checking membership.

The public Git repository is the canonical navigable library; GitHub Releases
provide versioned bulk-download packages.
