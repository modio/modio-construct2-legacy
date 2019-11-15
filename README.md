<a href="https://mod.io"><img src="https://static.mod.io/v1/images/branding/modio-color-dark.svg" alt="mod.io" width="360" align="right"/></a>
# Construct 2 Plugin
[![License](https://img.shields.io/badge/license-MIT-brightgreen.svg)](https://github.com/modio/C2Plugin/blob/master/LICENSE)
[![Discord](https://img.shields.io/discord/389039439487434752.svg?label=Discord&logo=discord&color=7289DA&labelColor=2C2F33)](https://discord.mod.io)

Welcome to [mod.io](https://mod.io) Construct 2 Plugin. It allows game developers to easily control the browsing and installation of mod files in their games. It provides a interface built on the Construct 2 Engine to connect to the [mod.io API](https://docs.mod.io). We have a [test environment](https://test.mod.io) available which offers developers a private sandbox to try the Construct 2 Plugin out.

## Thanks

This plugin was created by TetroniMike for [Hypnospace Outlaw](https://hypnospace.mod.io/) and has been released open source for other game developers to use in their projects.

<p align="center"><a href="https://store.steampowered.com/app/844590/Hypnospace_Outlaw/"><img src="https://image.mod.io/games/ca46/214/hypospace-outlaw.png" alt="Hypnospace Outlaw" width="380"></a></p>

## Documentation

A quick start guide is provided below.

## Usage

### Browse mods

![Alt text](img/Readme/Browse.png?raw=true "Title")

```c++
example code here
```

### Auth (via email)

First step is to request a security code to your email.

![Alt text](img/Readme/EmailRequest.png?raw=true "Title")

```c++
example code here
```

Finish authentication by submitting the 5-digit code.

![Alt text](img/Readme/EmailExchange.png?raw=true "Title")

```c++
example code here
```

### External Auth

If your game is running inside a popular distribution platform such as Steam or GOG Galaxy you can authenticate 100% seamlessly.

#### Steam Auth

![Alt text](img/Readme/SteamAuth.png?raw=true "Title")

```c++
example code here
```


### Subscriptions

Download and remove mods locally by subscribing and unsubscribing.

#### Subscribe

![Alt text](img/Readme/Subscribe.png?raw=true "Title")

```c++
example code here
```

### Unsubscribe

![Alt text](img/Readme/Unsubscribe.png?raw=true "Title")

```c++
example code here
```

### Mod submission

Share mods by creating a mod profile and attaching modfiles to it.

#### Create a mod profile

![Alt text](img/Readme/AddMod.png?raw=true "Title")

```c++
example code here
```

#### Upload a modfile

![Alt text](img/Readme/AddModfile.png?raw=true "Title")

```c++
example code here
```

### Listeners

#### Download listener

![Alt text](img/Readme/DownloadListener.png?raw=true "Title")

```c++
example code here
```

#### Upload listener

![Alt text](img/Readme/UploadListener.png?raw=true "Title")

```c++
example code here
```

## Getting started
If you are a game developer, first step is to add mod support to your Construct 2 game. Once mod support is up and running, [create your games profile](https://mod.io/games/add) on mod.io, to get an API key and access to all [functionality mod.io offers](https://apps.mod.io/guides/getting-started). Next, input your `Game ID` and `API Key` under the mod.io `Project Settings` in the Construct 2.

![Alt text](img/settings.png?raw=true "Title")

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
