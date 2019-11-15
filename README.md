<a href="https://mod.io"><img src="https://static.mod.io/v1/images/branding/modio-color-dark.svg" alt="mod.io" width="360" align="right"/></a>
# Construct 2 Plugin
[![License](https://img.shields.io/badge/license-MIT-brightgreen.svg)](https://github.com/modio/C2Plugin/blob/master/LICENSE)
[![Discord](https://img.shields.io/discord/389039439487434752.svg?label=Discord&logo=discord&color=7289DA&labelColor=2C2F33)](https://discord.mod.io)

Welcome to [mod.io](https://mod.io) Construct 2 Plugin. It allows game developers to easily control the browsing and installation of mod files in their games. It provides a interface built on the Construct 2 Engine to connect to the [mod.io API](https://docs.mod.io). We have a [test environment](https://test.mod.io) available which offers developers a private sandbox to try the Construct 2 Plugin out.

## Thanks

This plugin was created by TetroniMike (Michael Lasch) for [Hypnospace Outlaw](https://hypnospace.mod.io/) and has been released open source for other game developers to use in their projects.

<p align="center"><a href="https://store.steampowered.com/app/844590/Hypnospace_Outlaw/"><img src="https://image.mod.io/games/ca46/214/hypospace-outlaw.png" alt="Hypnospace Outlaw" width="380"></a></p>

## Getting started
Please note that this plugin is only compatible with NW.js exported games on Windows, Mac, and Linux. It might be possible to alter the source code to make it compatible with other export methods, but we will not be going in to how to do so here. 

1) The first step is to add mod support to your Construct 2 game. Once mod support is up and running, [create your games profile](https://mod.io/games/add) on mod.io to get an API key and access to all [functionality mod.io offers](https://apps.mod.io/guides/getting-started).

2) Install the .c2addon files (json_plugin.c2addon and skymen_jszip_v1.4.c2addon) by clicking and dragging them into Construct 2. You will have to close and re-open Construct 2 to finish the installation.

3) Copy all assets from the provided .capx file's Layout into your game's C2 project, and arrange as you see fit. Add the following plugins to your game:

- AJAX
- Browser
- Function
- JSON
- jsZip
- Keyboard
- Mouse
- NWjs

4) Create the following Families, add their objects, and add these 'Faily instance variables'. These families and variables determine their font size on the screen relative to window size, and CSS properties:
![C2 Project Families](img/readme_families.png?raw=true "Title")

In the Hypnospace mod.io browser, we've set ModIOMature checkbox object's FontHeightPx to 8 and ExludeCSS to True. Modify as you see fit.

5) Finally, copy the events into a new Event Sheet.

6) Change the following variables to match your game's information:

- CompanyName
- GameName
- API (your mod.io API Key)
- GameID (your mod.io game's Game ID)

CompanyName and GameName are used to create a path on the player's computer to store mod files (for example: C:\Users\[user name]\CompanyName\GameName\mods). Change the code within 'On start of layout' to change where mod files are stored.

If you're using the mod.io test environment, change the BaseURL to "https://api.test.mod.io/v1/", otherwise leave it as "https://api.mod.io/v1/"

![C2 Project Variables](img/readme_variables.png?raw=true "Title")

7) Within the 'ModIO_Download' group, in 'Event sheet 1', there is some disabled code under 'On Zip Loaded' that checks the downloaded zip file for compatibility. For Hypnospace, we have a 'config.ini' file that is required to be either in the root folder or one folder deep in the zip file. This disabled code checks to make sure that it is present and no more than one folder deep. If the config file is at the root of the zip, a folder will be created titled using the mod's mod.io ID number, then the zip unpacked inside it. Feel free to re-enable this code and alter it to check that your game's downloaded mods follow the correct formatting for your game.

8) Test it and modify as you see fit!

## Error Codes

When downloading and installing a mod, the following errors can occur and show the following error codes on the download button:

- Error 001* - config.ini file not found in zip, mod is not formatted properly.
- Error 002* - config.ini file is more than 1 folder deep, mod is not formatted properly
- Error 003 - mod install path either does not exist or could not be created
- Error 004* - weird mod install error (config.ini found in zip but not in resulting unzipped folder contents)
- Error 005 - Error getting download url from mod.io
- Error 999 - Unknown error occured

\*These errors only show up if you have enabled the code that checks for mod compatibility. Please change it to match your mod's unique zip file specifications.

## Important Notes

While this is compatible with Mac and Linux in addition to Windows, we cannot guarantee it will work as expected on those platforms. Please do your own testing as you integrate this project into yours!

Subscriptions, updates, dependencies, and other features are not supported out of the box. You will have to code these yourself, if you want these features.

## Contributions Welcome
Our Construct 2 plugin is public and open source. Game developers are welcome to utilize it directly, to add support for mods in their games, or fork it for their games customized use. Want to make changes to our plugin? Submit a pull request with your recommended changes to be reviewed.

## Other Repositories
Our aim with [mod.io](https://mod.io), is to provide an open modding API. You are welcome to [view, fork and contribute to our other codebases](https://github.com/modio) in use:

* [Design](https://design.mod.io) is public and open source, the repository can be [found here](https://github.com/modio/WebDesign).
* [API documentation](https://docs.mod.io) is public and open source, the repository can be [found here](https://github.com/modio/APIDocs).
* [Browse engine tools](https://apps.mod.io), plugins and wrappers created by the community, or [share your own](https://apps.mod.io/add).
* [Unreal Engine 4 plugin](https://github.com/modio/UE4Plugin), easily manage the browsing and install of mods in Unreal Engine 4 games
* [Unity Engine plugin](https://github.com/modio/UnityPlugin), easily manage the browsing and install of mods in Unity Engine games
* [Python wrapper](https://github.com/ClementJ18/mod.io), a python wrapper for the mod.io API
* [Rust wrapper](https://github.com/nickelc/modio-rs), rust interface for mod.io
* And more...
