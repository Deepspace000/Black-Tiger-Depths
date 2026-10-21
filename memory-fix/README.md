# Idlyte memory fix (v3.00)

`idlyte-release-stage-art.patch` changes `pk()` in `index.html` so only the stage being flown keeps its sprite art.
Apply from the repo root: `patch -p1 < idlyte-release-stage-art.patch`

Measured in headless Chromium, visiting all 24 stages three times:
- before: renderer memory about 485 MB, about 6,600 canvases kept for the whole session
- after: about 347 MB, flat across tours; each stage rebuilds its art (70-680 ms) when you switch to it

Not found: the 2-3 GB a player reported. No leak showed up in missions (60 min of game time), stage restarts,
the Surface mini-game, hub screens or 200 dialog open/closes.
