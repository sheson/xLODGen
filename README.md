=======================================================================

xLODGen - xEdit tool mode to generate LOD for several Bethesda games

=======================================================================

Supported game modes FNV, FO3, FO4, FO4VR, TES5, TES5VR, SSE, ENDERAL, ENDERALSE

Install into a dedicated and empty folder outside of any game folders, mod manager folders, Steam or other third party folders or special Windows folders like Program Files, Users, Desktop, Documents, Downloads etc. For example C:\Modding\xLODGen\

Always use the x64 version. The x86 versions may run into memory errors and is included foor poor souls that use a x86 OS.

Rename xLODGenx64.exe to [game mode]LODGenx64.exe (TES5LODGenx64.exe for example) or start with command line argument -fnv, -fo3, -fo4, -fo4vr, -tes5, -tes5vr, -sse, -enderal, -enderalse

Always set -o:"c:\OutputPath\" command line argument to change where files are generated to. The default is the game folder which risks replacing existing files and is problematic with mod managers, especially if they use some kind of virtualization. Do not generate into any game or any mod manager folders that are part (direct or indirect) of the virtual file system. Do not generate into the Overwrite folder of MO2.

Install the output as a mod. Typically the output should overwrite everything for it to be able to take effect.

Only pack output into BSA/BA2 if the overwrite order of archives and loose files is properly understood and it is known how to verify which files are winning.

Use command line arguments to set the paths to the INI folder, plugins.txt and the data folder if required. For example:
-m:"c:\Users\[USERNAME]\Documents\My Games\Skyrim Special Edition GOG\"
-p:"c:\Users\[USERNAME]\AppData\Local\Skyrim Special Edition GOG\plugins.txt"
-d:"c:\GOG Games\Skyrim Special Edition GOG\Data\"

If a mod manager is used, refer to its manual how to add tools and their command line arguments. Otherwise use a windows shortcut.

=======================================================================

Reset Settings to Default

See https://tes5edit.github.io/docs/2-overview.html#KeyboardShortcuts to reset all xEdit settings

To only reset the LODGen settings, delete everything under the section header [<GAME MODE>LOD Options] in c:\Users\<USERNAME>\AppData\Local\[Game Name]\Plugins.<GAME MODE>viewsettings

Replace <GAME MODE> with FNV, FO3, FO4, FO4VR, TES5, TES5VR, SSE, ENDERAL, ENDERALSE

Replace <USERNAME> with the actual username

=======================================================================

For LODSettings file generation read LODSettings-File-Readme.txt

For terrain LOD generation read Terrain-LOD-Readme.txt

For terrain height map generation read Terrain-Heightmap-Readme.txt

For terrain underside generation read Terrain-Underside-Readme.txt

For Skyrim occlusion data generation read Skyrim-Occlusion-Readme.txt

For seasonal LOD generation read Seasons-Readme.txt

For combining the LOD of worldspace see Combine-Worldspaces-Readme.txt

=======================================================================

For object and tree LOD generation instructions and additional resources see

FNVLODGen https://www.nexusmods.com/newvegas/mods/58562
FO3LODGen https://www.nexusmods.com/fallout3/mods/21174
FO4LODGen http://forum.step-project.com/topic/12466-fo4lodgen/
TES5LODGen https://www.nexusmods.com/skyrim/mods/62698
SSELODGen https://www.nexusmods.com/skyrimspecialedition/mods/6642

Object LOD generation uses terrain LOD meshes to optimize the object LOD meshes by removing any triangles that are below the terrain or water planes. Generate terrain LOD before or in the same session as object LOD.
