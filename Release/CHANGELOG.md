# Changelog

## 0.1.18
First release.
- Spin step is configurable (22.5 degrees by default, the scroll wheel works as in vanilla).
- Tilt: hold Shift and scroll to tilt a building piece or item stand around its own X axis. Copying a placed piece (copy rotation) copies its tilt too.
- Nudge: hold Ctrl and scroll to move the piece up and down, hold Z and scroll for left and right, hold X and scroll for forward and back. 2 cm per click, up to 14 cm each way. Backspace clears the tilt and the nudge.
- Snap center: with a building piece in hand, Tab cycles the snap points and now also offers a Center point, so the middle of the piece snaps onto another piece's snap points and middles.
- Tilt and Nudge lines in the build key hints.
- Cleaner screen: an empty strip is reserved at the bottom of the screen for the key hints, other on-screen elements (such as extra slot bars) are moved up out of it, the hint bar is a little smaller and centered, the piece box sits just above the strip, and the health bar of the piece under your crosshair is hidden while you place a piece (it still shows with Repair).
- If another mod rewrites the placement rotation code (Gizmo and similar), spin step and tilt switch themselves off, nudge keeps working, and the log says why.
