# Resident Evil 4 - Leon jacket model

Source: Workshop item `3339300694`, `Resident Evil 4 Leon Playermodel.gma`. Extracted locally to ignored `extracted/3339300694/`; all 26 GMA entry CRCs verified and the source archive preserved.

## PAC3

Archive: [standalone_leon_jacket.zip](../../standalone_leon_jacket.zip)

Paste this direct ZIP URL into a PAC3 Model part after upload:

```text
https://raw.githubusercontent.com/Nostow/pac3/main/standalone_leon_jacket.zip
```

For a locally mounted resource, use `models/re4_leon_playermodel/leon_jacket.mdl`. This package contains the full character only. The separate first-person arms and playermodel-registration Lua are not included.

## Dependencies

Materials were resolved from the version 48 MDL material/search-path tables and all skin references. Each VMT uses only a base texture, plus rendering flags; there are no additional bump/detail/warp/mask textures.

| Material | Base texture |
| --- | --- |
| `materials/models/re4_leon_jacket/pl0012.vmt` | `materials/models/re4_leon_jacket/pl0012.vtf` |
| `materials/models/re4_leon_jacket/pl0013.vmt` | `materials/models/re4_leon_jacket/pl0013.vtf` |
| `materials/models/re4_leon_jacket/pl0014.vmt` | `materials/models/re4_leon_jacket/pl0014.vtf` |
| `materials/models/re4_leon_jacket/pl0005.vmt` | `materials/models/re4_leon_jacket/pl0005.vtf` |
| `materials/models/re4_leon_jacket/pl0004.vmt` | `materials/models/re4_leon_jacket/pl0004.vtf` |
| `materials/models/re4_leon_jacket/leon_tex.vmt` | `materials/models/re4_leon_jacket/leon_tex.vtf` |
| `materials/models/re4_leon_jacket/leon_kami_n.vmt` | `materials/models/re4_leon_jacket/leon_kami_n.vtf` |
| `materials/models/re4_leon_jacket/pl0011.vmt` | `materials/models/re4_leon_jacket/pl0011.vtf` |

Included files:

- `materials/models/re4_leon_jacket/leon_kami_n.vmt`
- `materials/models/re4_leon_jacket/leon_kami_n.vtf`
- `materials/models/re4_leon_jacket/leon_tex.vmt`
- `materials/models/re4_leon_jacket/leon_tex.vtf`
- `materials/models/re4_leon_jacket/pl0004.vmt`
- `materials/models/re4_leon_jacket/pl0004.vtf`
- `materials/models/re4_leon_jacket/pl0005.vmt`
- `materials/models/re4_leon_jacket/pl0005.vtf`
- `materials/models/re4_leon_jacket/pl0011.vmt`
- `materials/models/re4_leon_jacket/pl0011.vtf`
- `materials/models/re4_leon_jacket/pl0012.vmt`
- `materials/models/re4_leon_jacket/pl0012.vtf`
- `materials/models/re4_leon_jacket/pl0013.vmt`
- `materials/models/re4_leon_jacket/pl0013.vtf`
- `materials/models/re4_leon_jacket/pl0014.vmt`
- `materials/models/re4_leon_jacket/pl0014.vtf`
- `models/re4_leon_playermodel/leon_jacket.dx80.vtx`
- `models/re4_leon_playermodel/leon_jacket.dx90.vtx`
- `models/re4_leon_playermodel/leon_jacket.mdl`
- `models/re4_leon_playermodel/leon_jacket.phy`
- `models/re4_leon_playermodel/leon_jacket.vvd`

## Validation and limitations

All 21 ZIP entries use ZIP_STORED (no compression), contain only PAC3-supported asset types, preserve original paths, and match the extracted source bytes. MDL/VVD/DX80 VTX/DX90 VTX checksums match; the VTX files have no material replacements. The supplied PHY is included. No SW VTX is supplied. Documentation stays outside the ZIP to satisfy PAC3's file whitelist.

The MDL includes `models/m_anm.mdl`, an external animation dependency verified in the installed Garry's Mod `garrysmod_dir.vpk`; it is provided by the game and is not redistributed here. The MDL has no external animation blocks. Embedded material references use mixed case; original lowercase filenames and binary contents are preserved. Runtime appearance, animations, and case-sensitive behavior still require in-game testing.
