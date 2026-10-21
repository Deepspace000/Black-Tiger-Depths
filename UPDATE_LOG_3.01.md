# Idlyte 3.01

## Fixed
* The game now uses less memory in long sessions. Before, it kept the art for every stage you had flown, for the whole session. That added up to thousands of small images in memory. Now only the stage you are flying keeps its art.
* In testing, memory after visiting all 24 stages dropped from about 485 MB to about 347 MB, and it stays flat however many times you go round.

## What you might notice
* When you switch to a different stage, its art is rebuilt. This takes between 70 and 680 milliseconds, so there may be a very short pause at the start of a mission.
* Flying the same stage again and again has no extra cost.
* Nothing else about play has changed.

## Tested
* 60 minutes of game time in one mission.
* All 24 stages, three times round.
* 40 mission restarts, the Surface worlds, every station screen, and 200 opens and closes of the settings screen.
* No memory leak was found in any of these.

## Still open
* One player reported 2 to 3 GB of memory and a freeze when closing a dialog. This could not be reproduced. If it still happens after this update, please tell us your browser, your device, and whether hardware acceleration is turned on.
