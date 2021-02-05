Rimworld 1.2 Multiplayer Kitchen Sink Modpack
===
[![License](https://i.creativecommons.org/l/by-nc/3.0/88x31.png)](https://creativecommons.org/licenses/by-nc/3.0/)
[![Version](https://img.shields.io/badge/Rimworld-1.2-green.svg)](http://rimworldgame.com/)

So many mods, good luck not desyncing!

## Host Installation
*NOTE 1*: You might want to backup your existing `Config`, `HugsLib`, `ModLists`, and `Mods` folders first!

1. Click `Subscribe to all` on the ![Steam](https://i.imgur.com/XEAiSka.png) [Mod Collection](https://steamcommunity.com/sharedfiles/filedetails/?id=2362582693) (like and favorite if you choose)
2. Download the [latest config files here](https://github.com/ubergarm/rimworld-mp-kitchen-sink/archive/master.zip)
3. Copy/paste the `Config`, `HugsLib`, and `ModLists` folders from the zip replacing yours e.g. `C:\Users\%USERPROFILE%\AppData\LocalLow\Ludeon Studios\RimWorld by Ludeon Studios\Config` or in Linux `~/.config/unity3d/Ludeon Studios/RimWorld by Ludeon Studios/Config`
4. Freeze/pin all your mod versions by copy/pasting all of the `1234567890` folders from `steamapps/workshop/content/294100/*` over into `steamapps/common/RimWorld/Mods/`. The mod configs in this repo assume that you do this step, and if you skip this step, you will have to manually load `Harmony` and `Mod Manager` in the proper order, restart rimworld, then load the provided `mp-kitchen-sink.xml` mod list and restart again.
5. Zip up all the mods from step 4 above and provide them to your players directly to use so that even if new releases appear on steam it will not mess up your playthrough. Unfortunately, steam workshop does not keep older mod versions like a real package manager (e.g. curseforge/npm/apt/pypi/etc), so the tooling for "real modpacks" (e.g. like Minecraft supports) isn't easily available yet for RimWorld. This compressed zip file is ~1GiB at the time of writing.

*NOTE 2*: Technically only the person hosting the server needs to install configs, as clients can download configs when connecting. Though some reports suggest it is best to manually do this as `HugsLib` configs may not all sync quite right.

## Thoughts
A few more mods you could swap in depending on your play style:
* [Hospitality](https://steamcommunity.com/sharedfiles/filedetails/?id=753498552) (remove [Keep Bed Ownership](https://steamcommunity.com/sharedfiles/filedetails/?id=2130184293) if you do)
* [Gastronomy](https://steamcommunity.com/sharedfiles/filedetails/?id=2279786905) (disable common sense 'clean before operating')
* [Rimsec Security](https://steamcommunity.com/sharedfiles/filedetails/?id=2323762086)
* [Graze Up](https://steamcommunity.com/sharedfiles/filedetails/?id=2302739121)
* [VFE Mechanoids](https://steamcommunity.com/workshop/filedetails/?id=2329011599)

## Issues
If you find something that consistently causes desync issues, please
report it here in the Issue Tracker, or in the collection comments if
you don't have github access.

Also, I plan to clean-up all of the `_copy` packageId mods
and straighten that out. Turns out the 'make a local copy'
button in Fluffy's Mod Manager mangles the name of mod in
the About.xml e.g. <packageId>rimfridge.kv.rw</packageId>
to be <packageId>rimfridge.kv.rw_copy</packageId> and then you will see
errors like `Mod XYZ (blah.blah) is not in valid format` and `Failed
to get meta from active mod XYZ Mod can't be checked for exclusion`.

This causes problems where Multiplayer-Compatibility mod does not seem
to detect/trigger the patches correctly.  (e.g. it is trying to target
based on the name [MpCompatFor("rimfridge.kv.rw")])

The work around is to *not* use mod manager 'make a local copy' button,
but just go copy/paste the 1234565789 steam id directory from the workshop
content directory over into the game's Mods folder (refer to step 4/5 above).

## References
* [Multiplayer Kitchen Sink Modpack Collection](https://steamcommunity.com/workshop/filedetails/?id=2362582693)
* [Companion Multiplayer Kitchen Sink Mod](https://steamcommunity.com/sharedfiles/filedetails/?id=2381578953)
* [Happy Accidents Multiplayer QoL Modpack](https://github.com/ubergarm/rimworld-happy-accidents)
