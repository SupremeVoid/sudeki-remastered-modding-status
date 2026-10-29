# Sudeki Remastered: modding status

*Last updated 2026-10-29*

What mods can change in Sudeki Remastered today, what is experimental and what is still planned. Mods go into the mods folder (or the configuration tool's Mods tab) and never touch the installed game. We update this page as the work moves on.

**The page: https://supremevoid.github.io/sudeki-remastered-modding-status/**

<details>
<summary>Changelog (latest 2026-10-29)</summary>

**2026-10-29**

- A balancing editor in the Modding Suite: supported (the Balancing tab).
- New: balancing values the game's scripts set (.balance files), supported.
- New: enemies of one zone changed alone (region copies), supported.
- Data values (.patch) now include character templates (enemy HP, XP, skills).
- Difficulty scaling: supported with limits (a setting in the ini file for now).
- Mods tab: balancing mods are compared value by value.
- New: the Steam and GOG versions of the game, supported.
- mod.ini: one name and a Markdown description in the author's language.
- New: the remaster's own content (benches, sitting down), which mods can replace.
- Interfaces (menus, the HUD): not planned; interface models are no longer listed as coming.
- The Modding Suite and the Animation Editor save into a target mod chosen in their toolbar.

**2026-10-28**

- Initial status.

</details>

🟢 Supported · 🟡 Supported, with limits · 🟠 Experimental · 🔵 In progress · ⚪ Planned · ⚫ Not planned

## Mods in general

| Feature | Status | Notes |
|---|---|---|
| Mod folders and .zip files, mod.ini (name, author, version, a Markdown description) | 🟢 Supported | One name and description in the author's language; a mod works the same in every language of the game. |
| Steam and GOG versions of the game | 🟢 Supported | The same mods on both. |
| Load order, conflicts between mods, switching mods on and off | 🟢 Supported | In the configuration tool's Mods tab. Balancing mods are compared value by value: the Mods tab lists every value two mods set differently and which one wins. |
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
| Models imported from glTF (props, effects, outfits) | 🟡 Supported, with limits | Characters keep their skeleton (same bones). Not yet: tangent frames, two-component UVs, cutscene morphs. Interface models are not planned (see Interfaces). |
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
| Data values (.patch) | 🟡 Supported, with limits | Several mods add up, character templates (enemy HP, XP, skills) included. The party's base stats and ability gains are kept in the save, so a change shows in a new game only. |
| A balancing editor in the Modding Suite | 🟢 Supported | The Balancing tab: 14 tables (weapons, armour, potions, the party, abilities, the level curve, skills, enemies, drops ...) with the game's names; single cells or a whole column at once (multiply, add, set). |
| Balancing values the game's scripts set (.balance) | 🟢 Supported | Rune strengths, blacksmith and shop prices, what shops sell, traders' prices, defence factors, the AI's damage factor, quest rewards. Quest rewards are not tested in the game yet. |
| Enemies of one zone changed alone (region copies) | 🟢 Supported | A copy of a monster for one zone, edited on its own; bosses are left out (the scripts spawn them). |
| Difficulty scaling (damage, enemy HP, XP, money) | 🟡 Supported, with limits | On top of whatever balancing mods set. A setting in the ini file for now, not yet in the menus. |
| Interfaces (menus, the HUD) | ⚫ Not planned | The layouts live in the interface models and the game's program, out of a mod's reach. Interface changes come as features of the remaster itself, such as its options menu. |

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
| The remaster's own content (the benches of New Brightwater, sitting down) | 🟢 Supported | Built in and always there; a mod replaces any piece of it with a file or place of the same name. |
| New characters (NPCs with an outfit, a name, lines, a walk) | 🟠 Experimental | Made in the Modding Suite. Voices for new lines are not supported yet. |
| Script mods (quests, events, mechanics) | 🔵 In progress | A disassembler, an assembler and a linker exist; a decompiler and a compiler are next. |
| Whole new levels | ⚫ Not planned | Needs collision and navigation formats that are not decoded. |
| Save games, the game's code | ⚫ Not planned | Mods change the game's data, not its program or your saves. |

## Tools for modders

- **Configuration tool, Mods tab**: Install, order, switch and import mods; the modding guide in five languages.
- **Sudeki Modding Suite**: Every asset of the game read from your own install: textures, models, characters, animations, zones, sounds, texts, data. Checks mods and makes them (materials, lights, balancing, new characters, glTF import) into the target mod chosen in its toolbar.
- **Sudeki Animation Editor**: Poses and animations for Tal, Ailish, Buki and Elco, and edits of the game's own clips for any skeleton, saved into the target mod chosen in its toolbar.
- **Extract Game Assets**: The game's models (glTF) and textures (PNG) from your own install, as a start for mods.

Sudeki Remastered is a fan project; you need your own copy of Sudeki.
