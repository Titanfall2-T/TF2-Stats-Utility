# Stats Utility
A configurable utility mod to display your current match stats on your hud.

**Currently displayed stats include the following**

- Number of pilot kills(Displayed as 'Kills')
- Number of deaths(Displayed as 'Deaths' )
- Pilot kill/death ratio(Displayed as 'K/D')

Please keep in mind that this mod is still a work in progress and the first release of it was pretty rushed(due to the fact that people that had been told about it started asking for it to be released)(this means that some features that were intended to be in the first release are missing, however they are planned to be added soon), and there are a lot of different features that are planned to be added in the near future.

<hr>

## How To Install And Use The Stats Utility Mod
To install the mod simply click the download link for the latest version, and unzip the file when it finishes downloading. Once extracted open the 'mods' folder and drag the folder inside of it(should be named something like 'TimeIsUnending.StatsUtility.0.1.0') into your Northstar mods folder (located in your game install directory under /Titanfall2/R2Northstar/mods).

Now you can launch your game and you're ready to go! Just load into a match and you should see the stats hud displayed in the upper right hand corner of your screen. To show/hide the stats hud just press the hud toggle button(which is set to the 'p' key by default and can be changed at any time).

## Configuring And Customizing The Stats Utility Mod
By default all the hud displayed stats are colored white and have a alpha value of 0.5, and the hud toggle button is 'p'.

To configure and customize the mod you'll have to add the ConVars of the things you want to change to your 'ns_startup_args.txt' which is located in your game install directory.

To start simply create a new line in the 'ns_startup_args.txt' file and add '+ConVar VALUE' to configure/customize the mod(just replace 'ConVar' with any of the mod's ConVars  and 'VALUE' with the value you want to set it to).

### Available ConVars And Their Descriptions
- `sutil_hudEnabled` - This ConVar is just whether the stats hud is enabled/shown or not
- `sutil_killStatsColor` - This ConVar is what the color of the hud displayed stat for pilot kills is. Must be a string formatted like so(make sure to replace the 'RED_VALUE', 'GREEN_VALUE', and 'BLUE_VALUE' with the RGB values of the color you want, also remember each value must be between 0 and 255) : "RED_VALUE,GREEN_VALUE,BLUE_VALUE"
- `sutil_killStatsAlpha` - This ConVar is what the alpha(transparency) of the hud displayed stat for pilot kills is. Must be a float with a value between 0.0 and 1.0
- `sutil_deathStatsColor` - This ConVar is what the color of the hud displayed stat for deaths is. Must be a string formatted like so(make sure to replace the 'RED_VALUE', 'GREEN_VALUE', and 'BLUE_VALUE' with the RGB values of the color you want, also remember each value must be between 0 and 255) : "RED_VALUE,GREEN_VALUE,BLUE_VALUE"
- `sutil_deathStatsAlpha` - This ConVar is what the alpha(transparency) of the hud displayed stat for deaths is. Must be a float with a value between 0.0 and 1.0
- `sutil_kdStatsColor` - This ConVar is what the color of the hud displayed stat for pilot kill/death ratio is. Must be a string formatted like so(make sure to replace the 'RED_VALUE', 'GREEN_VALUE', and 'BLUE_VALUE' with the RGB values of the color you want, also remember each value must be between 0 and 255) : "RED_VALUE,GREEN_VALUE,BLUE_VALUE"
- `sutil_killStatsAlpha` - This ConVar is what the alpha(transparency) of the hud displayed stat for pilot kill/death ratio is. Must be a float with a value between 0.0 and 1.0
- `sutil_hudToggleButtonEnumValue` - This ConVar is the Enum value of the button that toggles whether the stats hud is shown or hidden. I will include a table of buttons and their Enum values below the list of available ConVars and their descriptions.

### Table Of Buttons And Their Enum Values Along With How To Find Them On Your Own
| Button | Value | \- | Button | Value | \- | Button | Value |
|----------|-----|---|----------|-----|---|----------|-----|
| 0 | 0 | \| | M | 22 | \| | F9 | 99 |
| 1 | 1 | \| | N | 23 | \| | F10 | 100 |
| 2 | 2 | \| | O | 24 | \| | F11 | 101 |
| 3 | 3 | \| | P | 25 | \| | F12 | 102 |
| 4 | 4 | \| | Q | 26 | \| | , | 57 |
| 5 | 5 | \| | R | 27 | \| | . | 58 |
| 6 | 6 | \| | S | 28 | \| | ; | 54 |
| 7 | 7 | \| | T | 29 | \| | ' | 55 |
| 8 | 8 | \| | U | 30 | \| | [ | 52 |
| 9 | 9 | \| | V | 31 | \| | ] | 53 |
| A | 10 | \| | W | 32 | \| | / | 59 |
| B | 11 | \| | X | 33 | \| | \ | 60 |
| C | 12 | \| | Y | 34 | \| | - | 61 |
| D | 13 | \| | Z | 35 | \| | = | 62 |
| E | 14 | \| | F1 | 91 | \| | RALT | 81 |
| F | 15 | \| | F2 | 92 | \| | RCTRL | 83 |
| G | 16 | \| | F3 | 93 | \| | RSHIFT | 79 |
| H | 17 | \| | F4 | 94 | \| | MOUSE_LEFT | 106 |
| I | 18 | \| | F5 | 95 | \| | MOUSE_RIGHT | 107 |
| J | 19 | \| | F6 | 96 | \| | MOUSE_MIDDLE | 108 |
| K | 20 | \| | F7 | 97 | \| | MOUSE_4 | 109 |
| L | 21 | \| | F8 | 98 | \| | MOUSE_5 | 110 |

#### How To Find Button Enum Values
If you do not know the Enum of the button you would like to use and it is not listed above simply load into the Northstar multiplayer menu or a Northstar Match, press the '~' key to open the console(The console button for Northstar can be changed in-game in the escape menu under Settings -> Controls -> Mouse/Keyboard -> Key Bindings -> Northstar -> Toggle Developer Console) and type 'script_client print( BUTTON )' (replace 'BUTTON' with the constant for the button's Enum. A couple examples would be the following : 'KEY_W', 'MOUSE_MIDDLE', 'KEY_RALT', 'MOUSE_4', 'KEY_PERIOD') and enter the command. After this look at the line that says '[info] [CLIENT SCRIPT] NUMBER'(the text 'NUMBER' is just a placeholder for the value the command will give you) and use the value that this gives you as the Enum value for the 'sutil_hudToggleButtonEnumValue' ConVar.

<hr>

## Major Versions, Minor Versions, And Revisions Release Log

### [05/27/2022] Version 0.0.1 Released
- Created README
- Created manifest.json
- Created icon.png

### [05/29/2022] Version 0.1.0 Released
- Added the ability to change the Alpha of the hud displayed stats
- Made it where the colors of the hud displayed stats are stored in a variable(will be used later for color changing animations)
- Updated method of getting player kills and deaths
- Removed cl_obituary.gnut(not required for counting player kills and deaths now)
- Fixed issue with enemys that the player has damaged killing themselves not counting as kills
- Updated README
