# NotSoRandomizer

Modified version of the [Randomizer Team Fortress 2 plugin by FortyTwoFortyTwo](https://github.com/FortyTwoFortyTwo/Randomizer) that allows player to choose their own loadout.
Supports all TF2 stock gamemodes excluding Mann Vs Machine.

## Builds
All builds can be found [here](https://github.com/Doclic/NotSoRandomizer/releases).

## Requirements
- SourceMod 1.10
- [tf2attributes](https://forums.alliedmods.net/showthread.php?t=210221)
- [tf_econ_data](https://forums.alliedmods.net/showthread.php?t=315011)
- [dhooks with detour support](https://forums.alliedmods.net/showpost.php?p=2588686&postcount=589)

## ConVars
- `randomizer_version`: Plugin version number, don't touch.
- `randomizer_enabled`: Enable/Disable the entire plugin, another option for load/unload plugins.
- `randomizer_droppedweapons`: Enable/Disable dropped weapons.
- `randomizer_huds`: Mode to display weapons from hud.
  - 0: No hud display
  - 1: Hud text
  - 2: Menu

## Commands
- `sm_loadout`: Sets your loadout; Syntax: sm_loadout \<class_name> \<primary_id> \<secondary_id> \<melee_id> \[watch_id]
- `sm_cantsee`: Set your active weapon transparent or fully visible, for everyone

Examples on parameters that is valid to use for `sm_rndsetweapon`, `sm_rndsetslotweapon` and `sm_rndgiveweapon`:
- `220` for Shortstop (item def index)
- `direct hit` for Direct Hit (name based in translations)
- `backburner, loch, 424` for Backburner, Loch-n-Load and Tomislav
- `primary shotgun, secondary panic attack` for Shotgun from primary slot and Panic Attack from secondary slot

## Configs
There currently 5 [configs](https://github.com/FortyTwoFortyTwo/Randomizer/tree/master/configs/randomizer) able to easily change for future TF2 updates:
- `controls.cfg`: Manages how weapons with `attack2` passive button should be handled, should it be `attack3` or `reload` instead.
- `huds.cfg`: Lists all of the netprop meters to display in hud for many weapons.
- `reskins.cfg`: List of reskins for players to equip weapon from loadout instead of default weapon.
- `viewmodels.cfg`: List of all weapons with class specified to set transparent by default, without needing to use `sm_cantsee` on weapon that covers player screen everytime.
- `weapons.cfg`: Whitelist of weapon indexs to select from random pool, along with weapon name to display in HUD.

## TF2 Updates
This plugin itself aims to not not require modifications when valve releases TF2 updates.
Gamedatas is likely to break if TF2 update were to also break other plugin's gamedata (e.g. TF2Items).
If weapon additions or rebalances were to happen, it's possible configs need an update, or possibly even plugin itself if TF2 update were to make changes only work for one class.