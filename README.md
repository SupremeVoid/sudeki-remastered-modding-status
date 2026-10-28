# Sudeki Remastered: modding status

*Last updated 2026-10-28*

What mods can change in Sudeki Remastered today, what is experimental and what is still planned. Mods go into the mods folder (or the configuration tool's Mods tab) and never touch the installed game. We update this page as the work moves on.

**The page: https://supremevoid.github.io/sudeki-remastered-modding-status/**

🟢 Supported · 🟡 Supported, with limits · 🟠 Experimental · 🔵 In progress · ⚪ Planned · ⚫ Not planned

## Mods in general

| Feature | Status | Notes |
|---|---|---|
| Mod folders and .zip files, mod.ini (name, author, version, description in five languages) | 🟢 Supported |  |
| Load order, conflicts between mods, switching mods on and off | 🟢 Supported | In the configuration tool's Mods tab. |
| TexMod / uMod packages (.tpf) turned into mods | 🟢 Supported | All 406 known texture hashes matched. |
| Checking a mod (errors and warnings for every file) | 🟢 Supported | Modding Suite, Mods tab. |
| Changes while the game runs | 🟢 Supported | Pictures, .materials and .lights are taken again when saved ([Mods] HotReload). Everything else applies at start. |
| Requires= (a mod that needs another one) | 🟡 Supported, with limits | Checked and warned about; the game does not act on it yet. |

## Textures and models

| Feature | Status | Notes |
|---|---|---|
| Replacing any file of the game's archives (models, textures, entities, tables) | 🟢 Supported | Same format as the original. |
| High-resolution textures (.png, .jpg, .dds BC1-BC3, BC7) | 🟢 Supported | Any resolution; animated textures frame by frame. |
| New textures under new names | 🟢 Supported | For a mod's model that names them. |
| Surface relief and parallax per texture (.materials) | 🟢 Supported |  |
| Models exported to glTF | 🟢 Supported | All 2,432 models of the game. |
| Models imported from glTF (props, effects, outfits) | 🟡 Supported, with limits | Characters keep their skeleton (same bones). Not yet: tangent frames, two-component UVs, cutscene morphs, interface models. |
| Showing the name of the texture under the cursor in the game | ⚪ Planned |  |

## Sound and video

| Feature | Status | Notes |
|---|---|---|
| Movies (Bink 1 .bik) | 🟢 Supported |  |
| Whole sound banks (.xwb, .xsb, .sf) | 🟢 Supported |  |
| Single sounds (.wav) | 🟢 Supported | Replaces one entry of a wave bank. |
| New sounds and cues, retimed speech | 🟠 Experimental | Looping new cues and the lip sync of retimed speech are not tested yet. |

## Texts, data and balancing

| Feature | Status | Notes |
|---|---|---|
| Texts (.strings), in every language | 🟢 Supported | Several mods add up. |
| Data values (.patch) | 🟡 Supported, with limits | Several mods add up. Not yet for character templates (enemy HP, XP, skills): the mod check refuses them, and a patched enemy is not tested in the game yet. |
| A balancing editor in the Modding Suite (enemies, skills, the XP table) | ⚪ Planned |  |
| Difficulty scaling (damage, enemy HP, XP, money) | ⚪ Planned | On top of whatever balancing mods set. |
| Interfaces (menus, the HUD) | ⚪ Planned | Research first: where the layouts live and what a mod can replace. |

## Animation

| Feature | Status | Notes |
|---|---|---|
| Poses and animations for photo mode (.anim) | 🟢 Supported | Made with the Animation Editor. |
| Replacing the game's own animation clips (walks, idles, attacks) | 🟢 Supported | On any skeleton: party, NPCs, monsters. |
| Clip events (footsteps, sounds, effects) | 🟢 Supported |  |
| New clips played by a character's states | 🟢 Supported | Through a .patch of the character's .ani file. |

## Light and look

| Feature | Status | Notes |
|---|---|---|
| New lights in zones, changes to the game's lamps, torches and fires (.lights) | 🟢 Supported | Placed in the Modding Suite's zone view; ray-traced shadows where ray tracing is on. |
| Colour grading (LUTs) from mods | ⚪ Planned |  |

## World and content

| Feature | Status | Notes |
|---|---|---|
| New doors, rooms and places to sit (.doors, .rooms, .places) | 🟠 Experimental | A new door into a tavern and places to sit work in the game. A copied room loads but its geometry is not drawn yet. |
| New characters (NPCs with an outfit, a name, lines, a walk) | 🟠 Experimental | Made in the Modding Suite. Voices for new lines are not supported yet. |
| Script mods (quests, events, mechanics) | 🔵 In progress | A disassembler, an assembler and a linker exist; a decompiler and a compiler are next. |
| Whole new levels | ⚫ Not planned | Needs collision and navigation formats that are not decoded. |
| Save games, the game's code | ⚫ Not planned | Mods change the game's data, not its program or your saves. |

## Tools for modders

- **Configuration tool, Mods tab**: Install, order, switch and import mods; the modding guide in five languages.
- **Sudeki Modding Suite**: Every asset of the game read from your own install: textures, models, characters, animations, zones, sounds, texts, data. Checks mods and makes them (materials, lights, new characters, glTF import).
- **Sudeki Animation Editor**: Poses and animations for Tal, Ailish, Buki and Elco, and edits of the game's own clips for any skeleton.
- **Extract Game Assets**: The game's models (glTF) and textures (PNG) from your own install, as a start for mods.

Sudeki Remastered is a fan project; you need your own copy of Sudeki.
