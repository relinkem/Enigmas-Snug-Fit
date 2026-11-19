# Enigma's Snug Fit

*Place it a little closer to how you meant it.*

Spin, tilt, roll and nudge a piece by small steps while you place it, snap its middle onto another piece, and sink a beam end into the ground without any creative-mode tools. It keeps the feel of vanilla placement: the scroll wheel still spins, snapping still snaps, and everything is a setting. Client side, other players do not need it to see what you build.

![Spinning and tilting a beam](https://raw.githubusercontent.com/relinkem/Enigmas-Snug-Fit/main/Release/media/rotate-beam.gif)

## How to use it

Hold the mode key (Shift) and scroll to pick what the scroll wheel does. The name of the mode shows in the middle of the screen. Let go of Shift and the plain scroll wheel works that mode. A new piece always starts in spin, so it behaves like vanilla until you change the mode.

The modes, in the order Shift + scroll steps through them:

1. Move left and right (follows the piece)
2. Move up and down (world up, so a tilted piece still sinks straight down)
3. Move forward and back (follows the front of the piece, kept level)
4. Tilt (rotate around the piece's own X axis)
5. Spin (rotate around the vertical axis, plain vanilla)
6. Roll (rotate around the piece's own Z axis)

Each move click is 2 cm, up to 14 cm each way. Tilt and roll are 22.5 degrees per click.

## Features

- Spin step you can change. The scroll wheel works as in vanilla, 22.5 degrees per click by default.
- Mode cycle: Shift + scroll picks move left and right, up and down, forward and back, tilt, spin or roll. Plain scroll then works the picked mode.
- Tilt and roll: building pieces and item stands can be tilted around their own X axis and rolled around their own Z axis, 22.5 degrees per click by default. Chests, furniture, armor stands and crafting stations only spin, as they do in vanilla. You can add more pieces in the settings.
- Nudge in three directions, 2 cm per click, up to 14 cm each way by default.
- Snap center: Tab cycles a piece's snap points as in vanilla. For building pieces the cycle now ends with a Center point, which snaps the middle of your piece onto another piece's snap points and middles. Automatic snapping stays exactly as in vanilla.
- Backspace clears the tilt, roll and nudge. Copy rotation also copies the tilt of the piece you copy.
- A "Mode" line in the build key hints, and the game's own Rotate line renamed "Adjust", so you do not have to remember the keys.
- Controller support is built in (see Known issues).

## How it works

Pick a piece with the hammer and use the modes above. The changes are applied to the placement ghost before the game checks snapping and placing, so a tilted or nudged piece still snaps to joints and gets the usual placement checks. The nudge is added on top of the snapped position, so you can snap a beam end onto a crossing and then sink it a few centimeters.

Snug Fit does not need or use Gizmo. If another mod rewrites the game's placement rotation code (Gizmo and similar), Snug Fit switches spin step and tilt off so the two do not fight, keeps nudge working, and writes the reason to the log.

## Download

Install from Thunderstore with r2modman or the Thunderstore app. Dependencies are installed automatically:

[https://thunderstore.io/c/valheim/p/Enigma_Prime/Enigmas_Snug_Fit/](https://thunderstore.io/c/valheim/p/Enigma_Prime/Enigmas_Snug_Fit/)

To change settings in game, install Configuration Manager and press F1.

## Settings

Settings are in `BepInEx/config/EnigmaPrime.EnigmasSnugFit.cfg` after the first run:

- 1 - Rotation: spin step, tilt on or off, tilt step, roll step, mode key, which pieces can tilt, whether tilt clears when the piece changes, copy tilt.
- 2 - Nudge: nudge on or off, step size, the three limits, whether the nudge clears after placing.
- 3 - Other: reset key, key hints on or off, the label of the renamed Rotate hint, the switch that turns rotation features off when another mod changes rotation.
- 5 - Snap center: on or off, which piece categories get a Center point, extra pieces by name.

## Multiplayer and servers

Client side only. A dedicated server does not need it. Multiplayer has not been tested yet.

## Compatibility

- Valheim Performance Optimizations by OnTrigger and Plantations by Radamanto: safe to use together with Snug Fit (tested).
- Gizmo and other mods that rewrite the placement rotation code: spin step and tilt switch off, nudge keeps working. Using only one of them is simplest.
- Snug Fit patches the placement ghost conservatively and does not replace vanilla code where it can avoid it.

## Known issues

- Controller support is built in (hold the alt button and rotate to pick the mode, then rotate works the mode, hold the alt button and use the right stick to nudge) but untested, please report problems.
- Copy rotation copies the tilt but not the roll.
- Multiplayer is untested.
- A nudged position is not checked against other pieces again, which is fine for a few centimeters.

## Support

<a href="https://ko-fi.com/enigmaprime"><img src="https://raw.githubusercontent.com/relinkem/Enigmas-Snug-Fit/main/Release/media/Ko-Fi-badge-web.png" alt="I asked AI for help and it told me to get Ko-fi" width="220" align="left" hspace="16"></a>

If you like the mod and want to say thanks, you can:<br>[buy me a coffee on Ko-fi](https://ko-fi.com/enigmaprime)

<br clear="left">

Bug reports and ideas are just as welcome. Open an issue on [GitHub](https://github.com/relinkem/Enigmas-Snug-Fit/issues) and include your BepInEx log (`LogOutput.log`) and, if it is a settings problem, your config file. Ideas and suggestions are also welcome in the comments on my [Ko-fi page](https://ko-fi.com/enigmaprime).

## More mods by Enigma Prime

<a href="https://thunderstore.io/c/valheim/p/Enigma_Prime/Enigmas_Realistic_Smoke_Rework/"><img src="https://raw.githubusercontent.com/RELinkem/Enigmas-Realistic-Smoke-Rework/main/images/icon.png" alt="Enigma's Realistic Smoke Rework icon" width="96" align="left" hspace="16"></a>

**[Enigma's Realistic Smoke Rework](https://thunderstore.io/c/valheim/p/Enigma_Prime/Enigmas_Realistic_Smoke_Rework/)**<br>Smoke that rises, pools and bends in the wind, with flames that follow their fuel.

<br clear="left">

<a href="https://thunderstore.io/c/valheim/p/Enigma_Prime/Enigmas_Item_Salvager/"><img src="https://raw.githubusercontent.com/relinkem/Enigmas-Item-Salvager/main/Release/icon.png" alt="Enigma's Item Salvager icon" width="96" align="left" hspace="16"></a>

**[Enigma's Item Salvager](https://thunderstore.io/c/valheim/p/Enigma_Prime/Enigmas_Item_Salvager/)**<br>Take your gear apart at the Workbench, Forge, Black Forge or Galdr Table and get some of the materials back.

<br clear="left">

<a href="https://thunderstore.io/c/valheim/p/Enigma_Prime/Enigmas_Useful_Tasty_Mead/"><img src="https://raw.githubusercontent.com/relinkem/Enigmas-Useful-Tasty-Mead/main/Release/icon.png" alt="Enigma's Useful Tasty Mead icon" width="96" align="left" hspace="16"></a>

**[Enigma's Useful Tasty Mead](https://thunderstore.io/c/valheim/p/Enigma_Prime/Enigmas_Useful_Tasty_Mead/)**<br>A sweet mead that makes your food count as freshly eaten again, lifting your max health, stamina and Eitr before fading back.

<br clear="left">

<a href="https://thunderstore.io/c/valheim/p/Enigma_Prime/Enigmas_Enhanced_Forging/"><img src="https://raw.githubusercontent.com/relinkem/Enigmas-Enhanced-Forging/main/Release/icon.png" alt="Enigma's Enhanced Forging icon" width="96" align="left" hspace="16"></a>

**[Enigma's Enhanced Forging](https://thunderstore.io/c/valheim/p/Enigma_Prime/Enigmas_Enhanced_Forging/)**<br>Smelters, kilns and the Eitr refinery become walk-away machines with inventory screens, a Light button and winding animations.

<br clear="left">

<a href="https://thunderstore.io/c/valheim/p/Enigma_Prime/Enigmas_Tidy_Cart/"><img src="https://raw.githubusercontent.com/relinkem/Enigmas-Tidy-Cart/main/Release/icon.png" alt="Enigma's Tidy Cart icon" width="96" align="left" hspace="16"></a>

**[Enigma's Tidy Cart](https://thunderstore.io/c/valheim/p/Enigma_Prime/Enigmas_Tidy_Cart/)**<br>Back your empty cart up to a wall and stow it upright out of the way, with your character playing it out.

<br clear="left">

## How this mod was made

The ideas, the design, and every decision about how placing a piece should work are mine: keep it as close to vanilla as possible, tilt only the pieces where it looks right, keep the nudge small and limited, let Tab offer a center snap only for building pieces. However, I am not a programmer. The code was written by Claude, an AI assistant made by Anthropic, working from my direction through [Claude Code](https://claude.com/claude-code).

I want to be upfront about that. I am the one who plays the game, so I test every build in Valheim, read the game log for errors, and send back anything that looks or feels wrong until it behaves the way I intended. The code was also checked against Valheim's own code so it hooks in the right places. If you find a bug, please open an issue and I will work on a fix.

Not affiliated with or endorsed by Anthropic.

## Changelog

See [CHANGELOG.md](https://github.com/relinkem/Enigmas-Snug-Fit/blob/main/Release/CHANGELOG.md).

## License

All rights reserved. You are free to download and use the mod, but please don't redistribute, modify or re-upload it without asking first, see [LICENSE](https://github.com/relinkem/Enigmas-Snug-Fit/blob/main/Release/LICENSE). Valheim is the property of Iron Gate AB and Coffee Stain Publishing. This mod is not affiliated with or endorsed by them.
