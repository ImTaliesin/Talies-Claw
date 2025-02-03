<img src="icon/ded.svg" width="100%" height="128">

# Talie's Star Citizen Kill Tracker
Star Citizen Game Log Reader

This program monitors the Star Citizen `Game.log` file in real-time, reporting player kills, vehicle kills, game loading progress, respawn events, and [more](#supported-events).

![example screenshot of the program running in windows console](https://github.com/user-attachments/assets/0fa1d08e-776e-449c-b78b-59bf07c5a20c)

## Usage
1. Start the game, and wait until the EasyAntiCheat splash screen closes and the main game window has appeared.
2. If Star Citizen is installed in the default location, simply run the program.
3. If Star Citizen is installed elsewhere, move the program into the game folder before running.

The program can also be run with the game log file as the first parameter in a terminal.\
For example: `E:\SC_Kill_Tracker.exe E:\StarCitizen\PTU\Game.log`

> [!TIP]
> Previous log files can be found in the `logbackups` folder.

## Game Log Version Compatibility
Compatible with `LIVE` (`4.0.1`).\
Originally developed for `4.0_PREVIEW`.\
Mostly compatible with `3.24.X`.

## Supported Events
* Player/NPC deaths
* Ship/vehicle destruction
* Player respawns
* Game load progress[^1]
* Quantum travel events[^1][^3], including inter-system jumps[^1]
* Quit to menu/desktop[^1]
* Incapacitation events[^2]

[^1]: Local client only
[^2]: Excludes incaps from combat
[^3]: Only available for `4.0_PREVIEW`

## Fun Fact
* Kills weren't logged until `3.24`

## Known Issues
* Antimalware False Positive\
See [pyinstaller's antivirus issue template](https://github.com/pyinstaller/pyinstaller/blob/develop/.github/ISSUE_TEMPLATE/antivirus.md).\
Workaround: Install [Python](https://www.python.org/downloads/) manually, download a copy of the repo, and run `main.py`.

## Supported Python Versions
* 3.10+

## Disclaimer
"This is an unofficial Fansite."

Star Citizen intellectual property, content, and trademarks are owned by Cloud Imperium Rights LLC, Cloud Imperium Rights Ltd., and their subsidiaries.


## Devs
pip install pyinstaller
pyi-makespec --onefile main.py
pyinstaller main.spec
