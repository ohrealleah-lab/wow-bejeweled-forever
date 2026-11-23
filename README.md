# Bejeweled for World of Warcraft: Forever

The classic PopCap game Bejeweled, playable in a window inside World of Warcraft.

This version has been updated to load and run on **World of Warcraft: Forever** (Interface 16001), and it still includes support for modern retail and the Classic flavors.

## Install

1. Download this repo (green **Code** button, then **Download ZIP**) and unzip it.
2. Copy the `Bejeweled` folder into your game's AddOns folder:
   - **Forever:** `World of Warcraft/_forever_/Interface/AddOns/`
   - **Retail:** `World of Warcraft/_retail_/Interface/AddOns/`
3. Restart the game. Make sure **Bejeweled** is ticked on the AddOns screen at character select.
4. In game, type `/bej` or `/bejeweled` to open it.

## What was changed for Forever

- `Bejeweled_Mainline.toc` now lists Forever's Interface number (16001), so Forever no longer marks the addon as incompatible.
- Replaced the removed `MouseIsOver()` function with `IsMouseOver()`. The old call crashed every time the window opened and left the board empty.
- The board now redraws any gem whose picture is blank when the window opens or the game resumes. This fixes a grey board that sometimes showed until a gem was clicked.

Forever uses the Mainline files (`Bejeweled_Mainline.toc` and `.lua`). The Cata, TBC and Vanilla files are unchanged.

## Known issues (not yet tested or not working on Forever)

- Syncing high scores with guild and friends probably doesn't work yet.
- Five "fun" achievements that depend on the combat log (falling damage, killing critters, dying in combat, killing elites and rares) are switched off, because the combat log isn't available to addons.
- Some item-related achievements may not trigger, because an old item function was removed.
- The Ultra gem lightning effect may be missing or look different.
- Flight Path timing uses a fixed estimate instead of the real flight time.

If you find a bug, please open an issue and include the red error text if the game shows any. Turning on **Display Lua Errors** helps.

## Credits and notices

- Bejeweled is © 2000, 2008 PopCap Games, Inc. All rights reserved. The PopCap name, logo and trademarks belong to PopCap or its licensors. This is an unofficial community update and is not endorsed by PopCap, Electronic Arts or Blizzard.
- The art and sounds in this addon belong to their owners. No license to them is granted by this repo. See `Bejeweled/readme.txt` for the original notices.
- Third-party code credits (Lua, LuaSrcDiet) are in `Bejeweled/readme.txt`.
- Thanks to the earlier community maintainers who ported the addon to newer game versions, including the contributor credited in `Bejeweled/changelog.txt` for the resizing fix.
