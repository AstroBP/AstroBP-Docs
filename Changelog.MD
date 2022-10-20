# Changelog.MD
## these are old / new version changelogs, which detail what has changed since the last version of AstroBP / Astro2Emoji.<br><br>This has been ported from the [AstroBP Discord Server](https://discord.gg/gxJ4mytyce) to make it easier to maintain.

## AstroBP Public Beta 1
- a shit ton has changed.

## AstroBP Public Beta 1.5
- added more mobile friendly UI buttons to make object selection way more accessible
- added most special objects
- fixed many bugs
- increased scroll speed using on screen buttons

## AstroBP Public Beta 2:
- Fixed many many bugs
- Optimized some performance related things
- Optimized UI
- Added mode display
- Tweaked fps thresholds for FPS text coloring
- Added Firebase integration
- Added pop-ups
- Added connection status display
- Removed some unwanted resources in files

## AstroBP Public Beta 2.1:
- Fixed some bugs
- Changed the pulse effectivity for blocks around the recently placed block

## AstroBP Public Beta 3:
- Fixed an overwhelmingly large amount of bugs
- Added exporting
- - to Clipboard
- - to Firebase
- - to Documents folder
- Added importing
- - from Clipboard
- - from Document file
- Added file save management
- Added File deletion recovery with clipboard
- Added password protection (optional) to firebase exports

## AstroBP Public Beta 3.2:
- Fixed a few more bugs discovered along the way
- Patched some things listed in [#known-issues](./Known_Issues.MD#astrobp-public-beta-3)
- Added all of Astrogon's block textures, thanks to Thorsen
- - Note: the astrogon block textures that we know and love the most are not added correctly, the edge tracing code will be rewritten another day
- You can now load from firebase (needs password if required)
- fixed issue with loading levels that are longer than what your grid size was currently at
- Optimized the UI a little bit
- Added one-ways

## AstroBP Public Beta 3.5:
- Main editor UI now no longer goes away when deleting with right click (thanks to Thorsen for pointing that out)
- Fixed *"If you try to load a firebase save without having the AstroBPSaves folder in your documents, it hangs"*
- Fixed *"when toggling breaks or color, blocksUI shows wrong texture"*
- Fixed *"After once loading a save and then going back to load scene then back out, it will reload what you loaded the time before that. causing some potential overwriting in your creation"*
- Added a whole placeholder tutorial video. the UI for it is also placeholder. i made it in like 40 minutes including lazy video editing.
- You can skip-select what block/item you want to place down with number keys

## Astro2Emoji Expirimental Release 1:
- Initial Release

## Astro2Emoji Expirimental Release 2:
- Fixed all [Astro2Emoji Expirimental Release 1 issues](./Known_Issues.MD#astro2emoji-experimental-release-1)
- Added scrollbar toggling and osu-like cursor

## AstroBP Public Beta 4:
- Added SFX
- Turned some UI elements into Astrogon ones
- Dynamic grid lighting related to mouse position
- Astrogon custom mouse (~~bro stole my idea -bey~~)
- Added Grid and Block Culling to improve some performance
- Added drag and drop to move blocks
- Added grid property editing
- Added the ability to load from a .abp file on your computer outside of the main folder
- Added custom file type: .abp, to make old projects work, add ".apb" to old saves' file extensions
- Removed mobile friendly UI elements to make it more cleaner
- Hold shift while scrolling on gridview to hyperscroll
- Fixed many issues i cant remember them all (i can -bey)

## AstroBP Public Beta 5:
- Added first-time-use-only registry
- Added player position
- Added ability to change player start color
- Added End position
- Added ability to add and remove Checkpoint
- Added stars, max 3, like in game
- Added protection for your uploaded levels (firebase)  to not be deleted by others at will
- Added helpful hotkey text at top of screen
- Added Treadmills
- Added movables, and move on touch
- **Added Astrogon level export. click the button, and do "ctrl+V" in the level editor in Astrogon Steam 2.0.2 or later to import your ABP creations to Astrogon**
- Revamped ABP format exports
- Added all 2.0 textures (Factory is buggy)
- Fixed oh- so many annoying bugs. like a lot.. even a lot have risen during the past couple weeks, they're gone though. dont worry.
- Added bulk delete and bulk property editing.
