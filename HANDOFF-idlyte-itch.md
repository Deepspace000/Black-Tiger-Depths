# Hand-off: upload Idlyte v3.01 to itch.io

Branch: `claude/idlyte-v2.15-build` in Deepspace000/Black-Tiger-Depths

## What is ready
- `idlyte-v3.01-itch.zip`: HTML5 build (index.html at the root). It is v3.00 with the stage-art memory patch applied and the version set to 3.01. Tested: all 24 stages load twice with no errors.
- `memory-fix/idlyte-release-stage-art.patch` and `memory-fix/README.md`: the patch and test notes (apply to the idlyte repo with `patch -p1`).
- `cover-art/itch_cover_630x500.png` (itch.io cover), `cover-art/itch_cover_1260x1000.png`, `cover-art/idlyte_cover_c64_planets.png` (portrait cover), plus the Uridium-style title and the bickering goat logo as transparent PNGs.

## To do on the desktop
1. Upload the zip to the itch.io game page as the HTML5 build (butler channel `html5`), replacing the old file, and tick "played in the browser".
2. Set the itch.io cover image to `cover-art/itch_cover_630x500.png`.
3. Paste the update notes below into the devlog.
4. Optional: apply the patch to Deepspace000/idlyte on GitHub and bump VERSION to 3.01 (the zip already has it).

## Update notes (v3.01)
- Fixed: the game now uses less memory in long sessions. It used to keep the art for every stage you had flown. Now only the stage you are flying keeps it. In testing, memory after visiting all 24 stages dropped from about 485 MB to about 347 MB and stayed flat.
- Note: switching to a different stage rebuilds its art, which takes 70 to 680 ms, so there may be a very short pause at the start of a mission. Flying the same stage again has no extra cost.
- Still open: one player reported 2 to 3 GB and a freeze when closing a dialog. This could not be reproduced. If it still happens, send browser, device and whether hardware acceleration is on.
