# Standalone BG3 hair resources

Each ZIP is independent and includes one model, its two materials, its base texture, and both shared lighting textures. Per-hair READMEs with dependency evidence are in `hair_resource_docs/<hair>/README.md`. The original extracted bundle is unchanged.

All standalone hair ZIPs use stored (uncompressed) entries. Preserve this setting when rebuilding them. Keep documentation outside the ZIPs: [PAC3 only accepts model, material, and animation files](https://ww.pac3.info/tutorial/using-mdl-files).

Keep local extracted addon sources under `extracted/`, which Git ignores. The hair source bundle is at `extracted/hair_resource_extracted/`; filenames inside it are unchanged. ZIP READMEs refer to this bundle by its original name, `hair_resource_extracted`. Publish the standalone ZIPs from the repository root.

| Hair / ZIP | PAC3 model path | Material pair |
| --- | --- | --- |
| [astarion](standalone_astarion.zip) | `models/val/bg3/hair/astarion.mdl` | `HAIR_Astarion`, `HAIR_Astarion_T` |
| [carrionfeathers](standalone_carrionfeathers.zip) | `models/val/bg3/hair/carrionfeathers.mdl` | `HAIR_Wavy_Medium_B`, `HAIR_Wavy_Medium_B_T` |
| [feywildtrickster](standalone_feywildtrickster.zip) | `models/val/bg3/hair/feywildtrickster.mdl` | `HAIR_Straight_Short_A`, `HAIR_Straight_Short_A_T` |
| [gale](standalone_gale.zip) | `models/val/bg3/hair/gale.mdl` | `HAIR_Wavy_Medium_B`, `HAIR_Wavy_Medium_B_T` |
| [minthara](standalone_minthara.zip) | `models/val/bg3/hair/minthara.mdl` | `HAIR_Straight_Short_A`, `HAIR_Straight_Short_A_T` |
| [mythmaker](standalone_mythmaker.zip) | `models/val/bg3/hair/mythmaker.mdl` | `HAIR_Astarion`, `HAIR_Astarion_T` |
| [roverstumble](standalone_roverstumble.zip) | `models/val/bg3/hair/roverstumble.mdl` | `HAIR_Straight_Long_A`, `HAIR_Straight_Long_A_T` |
| [sensibleextravagance](standalone_sensibleextravagance.zip) | `models/val/bg3/hair/sensibleextravagance.mdl` | `HAIR_Wavy_Medium_B`, `HAIR_Wavy_Medium_B_T` |
| [trobairitzknot](standalone_trobairitzknot.zip) | `models/val/bg3/hair/trobairitzknot.mdl` | `HAIR_Straight_Short_A`, `HAIR_Straight_Short_A_T` |

Extract a ZIP into its own `garrysmod/addons/standalone_<hair>/` directory, keeping `models/` and `materials/` directly beneath it. Use the model path above when the resource is mounted locally. ZIP hosting alone does not establish that a particular PAC3/server setup supports remote ZIP loading; runtime testing remains necessary.

For remote loading, paste the direct ZIP URL into the PAC3 Model part's model field, for example `https://raw.githubusercontent.com/Nostow/pac3/main/standalone_roverstumble.zip`. This avoids the redirect from `github.com/.../raw/...`. An HTTP failure needs console/network diagnosis; a generic mount error alone does not identify its cause. After updating an archive, a URL pinned to the new commit can distinguish it from cached versions.

For another hairstyle, read its MDL material and search-path tables, resolve all skin/LOD materials, inspect every VMT texture reference (including shared warp textures), copy the model companions and dependencies without renaming, then verify checksums and archive contents. These archives were built using that process; texture selection is never based on the hairstyle filename.
