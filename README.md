# Yabber
An unpacker/repacker for common Demon's Souls, Dark Souls 1-3, Bloodborne, and Sekiro file formats.
Supports `.btab, .fxr, .msb, .blt, .matbin, .mtd, .bnd, .bhd/.bdt, .dcx, .fltparam, .fmg, .gparam, .luagnl, .luainfo, .tpf`.
If you want to convert `.msb` files, you will need to create a file named `_er`, `_ds3`, etc. depending on the game the `.msb` is for (info is given when trying to convert).
So far Demon's Souls `.msb` files can't be converted, sorry.

You can drag and drop a folder of files which are of 1 filetype to convert them all.
Example: folder "A" has only files which end with `.fxr`. Drag and drop "A" onto Yabber to convert every `.fxr` file inside it.
Now folder "A" will contain only files which end with `.fxr.xml` and will have a subfolder `BAK-fxr` where all the original `.fxr` were moved.
If you drag and drop again folder "A" onto Yabber, you will be left again with `.fxr` files and two `BAK` folders - one for `.fxr` files and one for `.fxr.xml` files.

Does not support dvdbnds (the very large bhd/bdt pairs in the main game directory); use [UDSFM](https://www.nexusmods.com/darksouls/mods/1304) or [UXM](https://www.nexusmods.com/sekiro/mods/26) to unpack those first.  
Also does not support encrypted files (enc_regulation.bnd.dcx in DS2, Data0.bdt in DS3); you can edit these with [Yapped](https://www.nexusmods.com/darksouls3/mods/306) or unpack them with [BinderTool](https://github.com/Atvaark/BinderTool).  
Requires [.NET 6.0.0](https://dotnet.microsoft.com/en-us/download/dotnet/thank-you/runtime-6.0.8-windows-x64-installer) - Windows 10 users should already have this.  

Please see the included readme for detailed instructions.

# Contributors
*katalash* - GPARAM support  
*TKGP* - Everything else
*Rayan* - Testing

# Changelog
### 1.0.1
* Drag and drop a folder to convert every file inside it
* Backup folders instead of files.
* FXR3 support including Elden Ring (xml)
* MATBIN and MTD converted to (xml) instead of (json)
* BTAB support (json)
* Slight refactor

### 1.0.0
* MSB files for the different games can be handled (ER, BB, Sekiro, DeS, DS3, DS2, DS1). (jsons)
* MATBIN support (json)
* MTD support (json)
* BLT support (json)
* added latest SoulsFormats from DSMapStudio to the repo
* updated Yabber accordingly to use .Net 6.0
* for previous changelog - look at the original Yabber from TKGP
