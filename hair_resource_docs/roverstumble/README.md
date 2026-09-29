# roverstumble standalone PAC3 hair

PAC3 model path: `models/val/bg3/hair/roverstumble.mdl`

This ZIP contains one hair from `hair_resource_extracted`, with the original Source-relative paths and byte-for-byte original assets. Extract into a separate `garrysmod/addons/standalone_roverstumble/` directory so `models/` and `materials/` are directly inside that directory.

## Materials and texture dependencies

`materials/models/val/bg3/hair/hair_straight_long_a.vmt`:

- `$basetexture`: `models/val/bg3/hair/HAIR_Straight_Long_A` ? `materials/models/val/bg3/hair/hair_straight_long_a.vtf`
- `$phongwarptexture`: `models/val/shared/phongwarphair` ? `materials/models/val/shared/phongwarphair.vtf`
- `$lightwarptexture`: `models/val/shared/lightwarpHair` ? `materials/models/val/shared/lightwarphair.vtf`

`materials/models/val/bg3/hair/hair_straight_long_a_t.vmt`:

- `$basetexture`: `models/val/bg3/hair/HAIR_Straight_Long_A` ? `materials/models/val/bg3/hair/hair_straight_long_a.vtf`
- `$phongwarptexture`: `models/val/shared/phongwarphair` ? `materials/models/val/shared/phongwarphair.vtf`
- `$lightwarptexture`: `models/val/shared/lightwarpHair` ? `materials/models/val/shared/lightwarphair.vtf`

## Included asset files

- `materials/models/val/bg3/hair/hair_straight_long_a.vmt`
- `materials/models/val/bg3/hair/hair_straight_long_a.vtf`
- `materials/models/val/bg3/hair/hair_straight_long_a_t.vmt`
- `materials/models/val/shared/lightwarphair.vtf`
- `materials/models/val/shared/phongwarphair.vtf`
- `models/val/bg3/hair/roverstumble.dx90.vtx`
- `models/val/bg3/hair/roverstumble.mdl`
- `models/val/bg3/hair/roverstumble.vvd`

## Verification and limitations

The IDST version 49 MDL material table contains 2 materials; its skin table references both. Material search paths were read from the MDL, not inferred from the hairstyle name. VVD and DX90 VTX checksums match the MDL. The VTX has no LOD material replacements, and the MDL declares no included models or external animation blocks. Every VMT texture dependency exists in this ZIP. All assets were checked against the source by SHA-256.

Only `.mdl`, `.vvd`, and `.dx90.vtx` companions are supplied for this model. No `.phy`, `.dx80.vtx`, or `.sw.vtx` is present in the source bundle. Runtime appearance and compatibility have not been tested in Garry's Mod/PAC3. Embedded material/texture references use mixed case while the original asset filenames are lowercase; lookup was case-insensitive, and neither paths nor file contents were changed. Case-sensitive runtime behavior remains untested.

Binary layout reference: [Valve Source SDK studio.h](https://github.com/ValveSoftware/source-sdk-2013/blob/master/src/public/studio.h).
