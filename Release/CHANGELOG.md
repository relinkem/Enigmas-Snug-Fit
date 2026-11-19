# Changelog

## 0.2.0
Controls changed: please read the first two points.
- Mode cycle: hold Shift and scroll to pick what the scroll wheel does: move left and right, move up and down, move forward and back, tilt (rotate X), spin (rotate Y) or roll (rotate Z). Let go of Shift and the plain scroll wheel works the mode you stopped on. The mode name shows in the middle of the screen, where vanilla shows the snap point. A new piece always starts in spin, as in vanilla.
- The held keys are gone: Ctrl, Z and X nudge keys and the Shift tilt are replaced by the mode cycle. Their settings are removed, and the new setting is "Mode key" (Shift by default). Nudge step and limits are unchanged.
- New: roll (rotate Z) for the pieces that can tilt, 22.5 degrees per click by default (setting "Roll step"). Backspace clears the tilt, roll and nudge.
- Hint bar: one fixed "Mode  Shift + Scroll" row, and the game's own "Rotate" row is renamed "Adjust" because it now also moves and tilts the piece (setting "Rotate hint label", empty keeps the vanilla text).
- Fix: spin step, tilt, roll and nudge now work together with Valheim Performance Optimizations and Plantations. Before, they did nothing when either was installed. Both mods are on a safe list, so they no longer switch spin step and tilt off.
- Faster: less work every frame while placing and for the screen layout code, with the same behavior.
- Controller (untested): hold the alt button and rotate to pick the mode, then rotate works the mode. Alt + right stick still nudges.

## 0.1.18
First release.
- Spin step is configurable (22.5 degrees by default, the scroll wheel works as in vanilla).
- Tilt: hold Shift and scroll to tilt a building piece or item stand around its own X axis. Copying a placed piece (copy rotation) copies its tilt too.
- Nudge: hold Ctrl and scroll to move the piece up and down, hold Z and scroll for left and right, hold X and scroll for forward and back. 2 cm per click, up to 14 cm each way. Backspace clears the tilt and the nudge.
- Snap center: with a building piece in hand, Tab cycles the snap points and now also offers a Center point, so the middle of the piece snaps onto another piece's snap points and middles.
- Tilt and Nudge lines in the build key hints.
- If another mod rewrites the placement rotation code (Gizmo and similar), spin step and tilt switch themselves off, nudge keeps working, and the log says why.
