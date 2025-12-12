# Games compatible with modern Linux

A curated list of games that run on Linux and neither require 32-bit compatibility nor XWayland.

---

## **Table of content**

- [Introduction](#introduction)
- [Heroic Games Launcher](#heroic-games-launcher)
  - [List of Games (GOG)](#list-of-games-gog)
- [Playing Games with FOSS (engine) recreations](#playing-games-with-foss-engine-recreations)
  - [List of Games](#list-of-games)
- [How to check for compatibility](#how-to-check-for-compatibility)
- [FAQ](#faq)

---

## Introduction

With the advent of DXVK, Proton and Gaming Distros like CachyOS and Bazzite, Gaming on Linux has reached an all-time-high.

This is a list of Windows games that you can play on Linux without the need for XWayland or 32-bit dependencies, using compatibility tools for Wine or engine recreations.

## Heroic Games Launcher

All of the following games were tested with `ia32_emulation=0` Kernel argument. They were installed using Heroic Games Launcher's download system, which unlike GOG's offline installers does not require 32-bit emulation. To run them, both `Enable Wine-Wayland(Experimental) (Wine version needs to support it)` and `Enable WoW64 (Experimental)` were enabled in Heroic's Wine settings.  

### List of Games (GOG)

<details>
  <summary>Click to show full list</summary>

| Game Name  | Platform | Tested with | DXVK/VK3D version | Runs? | Comment | 
| ------------- | ------------- | ------------- | ------------- | ------------- | ------------- |
| Batman™: Arkham Knight   | GOG | Heroic Games Launcher  | GE-Proton-Latest | yes |
| Bulwark Evolution: Falconeer Chronicles  | GOG | Heroic Games Launcher | GE-Proton Latest | yes |
| Control Ultimate Edition | GOG | Heroic Games Launcher  | GE-Proton-Latest | yes |
| Cyberpunk 2077 | GOG | Heroic Games Launcher  | GE-Proton-Latest | yes |
| Crysis®   | GOG | Heroic Games Launcher  | GE-Proton-Latest | yes | Uses the C1-Launcher. Warhead and Wars should work with it as well. |
| Dishonored 2 | GOG | Heroic Games Launcher  | GE-Proton-Latest | yes |
| Dishonored®: Death of the Outsider™ | GOG | Heroic Games Launcher | GE-Proton-Latest | yes |
| Dorfromantik   | GOG | Heroic Games Launcher  | GE-Proton-Latest | yes |
| Factorio   | GOG | Heroic Games Launcher  | GE-Proton-Latest | yes | Also has a native Linux port. |
| Metro 2033 Redux | GOG | Heroic Games Launcher  | GE-Proton-Latest | yes |
| Metro Exodus | GOG | Heroic Games Launcher  | GE-Proton-Latest | yes |
| Metro: Last Light Redux | GOG | Heroic Games Launcher  | GE-Proton-Latest | yes |
| Middle-earth™: Shadow of Mordor™ Game of the Year Edition   | GOG | Heroic Games Launcher  | GE-Proton-Latest | yes |
| No Man's Sky | GOG | Heroic Games Launcher  | GE-Proton-Latest | yes |
| Project Zomboid | GOG | Heroic Games Launcher  | GE-Proton-Latest | yes | Need to manually select x64 executable. Also has a native Linux port. |
| Quake Enhanced | GOG | Heroic Games Launcher | GE-Proton-Latest | yes |
| Quake II | GOG | Heroic Games Launcher | GE-Proton-Latest | yes | This is the "Enhanced" version, the original is named "Quake II (Original)" on GOG. |
| Quake II RTX | GOG | Heroic Games Launcher | GE-Proton-Latest | yes |
| Rise of the Tomb Raider: 20 Year Celebration   | GOG | Heroic Games Launcher  | GE-Proton-Latest | yes |
| S.T.A.L.K.E.R.: Call of Prypiat - Enhanced Edition   | GOG | Heroic Games Launcher  | GE-Proton-Latest | yes |
| S.T.A.L.K.E.R.: Clear Sky - Enhanced Edition | GOG | Heroic Games Launcher  | GE-Proton-Latest | yes |
| S.T.A.L.K.E.R.: Shadow of Chornobyl - Enhanced Edition   | GOG | Heroic Games Launcher  | GE-Proton-Latest | yes |
| Scorn   | GOG | Heroic Games Launcher  | GE-Proton-Latest | yes |
| Shadow of the Tomb Raider: Definitive Edition   | GOG | Heroic Games Launcher  | GE-Proton-Latest | yes |
| The Elder Scrolls V: Skyrim Special Edition   | GOG | Heroic Games Launcher  | GE-Proton-Latest | yes | For mod management see [LOOT](https://flathub.org/en/apps/io.github.loot.loot). |
| The Witcher 3: Wild Hunt - Complete Edition   | GOG | Heroic Games Launcher  | GE-Proton-Latest | yes | You may need to launch the game exe directly. |
| Warhammer 40,000: Boltgun | GOG | Heroic Games Launcher  | GE-Proton-Latest | yes |
| Warhammer 40,000: Dawn of War - Definitive Edition   | GOG | Heroic Games Launcher  | GE-Proton-Latest | yes |

</details>


## Playing Games with FOSS (engine) recreations

If you are inclined to disable 32-bit emulation and XWayland, but still want to keep playing your favourite game, maybe you'll be lucky and find your game among any of the lists of FOSS engine recreations (Like this one [here](https://en.wikipedia.org/wiki/List_of_game_engine_recreations)). Chances are high that the new engine will support both native Wayland and 64-bit.

For instance, if you'd like to keep playing Heroes of Might and Magic III, you may just install [VCMI](https://vcmi.eu/):

![](https://github.com/user-attachments/assets/e035928a-27a8-4ae7-8f84-c53535e26856)
*VCMI is a FOSS engine recreation for Heroes of Might and Magic III that runs great on modern systems.*

Note that you still need to provide the original data files. For that you either need to own the original CD or have the game on GOG and download their offline installer. You don't have to install the game through wine though, you can use [innoextract](https://constexpr.org/innoextract/) which will extract the game files for you. Some projects even include `innoextract` by default. Also certain games can run with Pipewire instead of Pulseaudio by granting `xdg-run/pipewire-0:ro` file access.

All of the following were tested with Flathub on Fedora Atomic and meet the following requirements:
+ Do not require any other permissions other than Wayland, DRI, Pulseaudio and network for multiplayer.
+ The Flatpak is verified.
+ Does not rely on outdated runtimes.


### List of Games

<details>
  <summary>Click to show full list</summary>

| Game Name  | Re-implementation |  Minimal set of permissions | Comment | 
| ------------- | ------------- | -------------  | ------------- |
| Caesar III | [Augustus](https://flathub.org/en/apps/com.github.keriew.augustus) | Wayland, DRI, Pipewire |  |
| Commander Keen (various) | [Commander Genius](https://flathub.org/en/apps/io.sourceforge.clonekeenplus) | Wayland, DRI, Pipewire, (Network) | Network permission can be used to download various freely available episodes. |
| Diablo | [DevilutionX](https://flathub.org/en/apps/org.diasurgical.DevilutionX) | Wayland, DRI, Pulseaudio, (Network) | Network permission is required for multiplayer only. Also works with the expansion, Hellfire. |
| Doom | [Odamex](https://flathub.org/en/apps/net.odamex.Odamex) | Wayland, DRI, Pipewire |  |
| Doom II | [Odamex](https://flathub.org/en/apps/net.odamex.Odamex) | Wayland, DRI, Pipewire |  |
| DOOM 3: BFG Edition | [Doom BFA](https://flathub.org/en/apps/io.github.maddecoder.Classic-RBDOOM-3-BFG) | Wayland, DRI, Pipewire, (Network)  | Network permission is required for multiplayer only. |
|  | [RBDOOM-3-BFG](https://flathub.org/en/apps/io.github.RobertBeckebans.RBDOOM-3-BFG) | Wayland, DRI, Pulseaudio, (Network)  | Network permission is required for multiplayer only. |
| Heroes of Might and Magic® 2: Gold | [fheroes2](https://flathub.org/en/apps/io.github.ihhub.Fheroes2) | Wayland, DRI, Pipewire  |  |
| Heroes of Might and Magic® 3: Complete | [VCMI](https://flathub.org/en/apps/eu.vcmi.VCMI) | Wayland, DRI, Pipewire, (Network)  | Network permission is required for multiplayer and mod management. Also works for Horn of the Abyss expansion. |
| STAR WARS™ Dark Forces (Classic, 1995) | [The Force Engine](https://flathub.org/en/apps/io.github.theforceengine.tfe) | Wayland, DRI, Pipewire |  |
| RollerCoaster Tycoon® 2: Triple Thrill Pack | [OpenRCT2](https://flathub.org/en/apps/io.openrct2.OpenRCT2) | Wayland, DRI, Pipewire, (Network) | Network permission is required for multiplayer only.  |
| Theme Hospital | [CorsixTH](https://flathub.org/en/apps/com.corsixth.corsixth) | Wayland, DRI, Pipewire |  |
| The Elder Scrolls III: Morrowind GOTY Edition | [OpenMW](https://flathub.org/en/apps/org.openmw.OpenMW) | Wayland, DRI, Pulseaudio  | For mod management see [LOOT](https://flathub.org/en/apps/io.github.loot.loot). |
| The Settlers® 2: Gold Edition | [Return to the Roots](https://flathub.org/en/apps/info.rttr.Return-To-The-Roots) | Wayland, DRI, Pipewire, (Network) | Network permission is required for multiplayer only.  | 
| Various: Adventure and role-playing games | [ScummVM](https://flathub.org/en/apps/org.scummvm.ScummVM) | Wayland, DRI, Pipewire | Tested with Beneath a Steel Sky (1994). |

</details>


## How to check for compatibility

### 64-bit executable

The first thing you'd want to check if you'd like to know whether your favorite game relies on 32-bit is the [PCGamingWiki Website](https://www.pcgamingwiki.com/wiki/Home). Here you should check the API section to see if a 64-bit executable is available for the game in question:

<img width="836" height="192" alt="image" src="https://github.com/user-attachments/assets/5aae172d-e5bb-463b-9ee7-04d9d920e9f1" title="Tomb Raider (2013) API section" />  

This is from the Tomb Raider (2013) API section. As you can see, while there is a 64-bit executable for MacOS, Linux and Windows are lacking one and instead rely on a 32-bit executable.

Be advised that just because PCGamingWiki does list a 64-bit executable, that doesn't necessarily mean that the game will run in a pure 64-bit environment. For instance some games bring their own launchers which rely on 32-bit, and without them, you can't launch the game. If that is the case launching the game's executable might be a workaround.  

It may also be possible that the information on the PCGamingWiki is outdated or only valid for a certain distributor. GOG for instance often incorporates fan modifications in older games as part of their GOG Preservation Program, which sometimes include FOSS engine or executable recreations that run in 64-bit.  

If you're on Linux and want to check if your game is running on 64-bit, you can do so by installing [MangoHud](https://github.com/flightlessmango/MangoHud?tab=readme-ov-file#hud-configuration) and enable the `arch` variable in the config file, which will display the architecture of the current executable on the HUD:

![](https://github.com/user-attachments/assets/49732182-409d-4622-8983-2a5f5bc7f413)  
*Factorio with MangoHud being enabled. Notice the lines for arch and display server.*

This, however, is also not a conclusive indicator for a lack of dependence on 32-bit. Grim Dawn for instance is a game that is playable in 64-bit (and MangoHud will correctly report it so), starting the game however requires 32-bit being enabled.

The only way to be sure that your game runs without the need for 32-bit is by setting `ia32_emulation=0` as a Kernel argument and see if the game runs fine. If it does require 32-bit, launching the game will most likely fail with `ShellExecuteEx failed: Internal error.`.

### XWayland

Sadly, determining whether a game needs XWayland without actually trying it is not possible, or at least I'm not aware of any means of doing so. Also, be advised that due to the nature of the interaction between a display server and your hardware/GPU drivers, the results of successfully testing a game with certain hardware doesn't necessarily mean it will run the same on a different system with a different GPU/driver version etc.

For already installed games you can again make use of MangoHud by setting the `display_server` variable:

![](https://github.com/user-attachments/assets/49732182-409d-4622-8983-2a5f5bc7f413)  
*Factorio with MangoHud being enabled. Notice the lines for arch and display server.*

## FAQ

# My favourite game requires either 32-bit or XWayland, what should I do?

Unless you have very specific reasons to force-disable both 32-bit emulation and XWayland you should simply keep them enabled. If you only care about gaming, I'd recommend not changing these at all.  

# What about Bottles, Lutris, Umu-Launcher ... ?

While Bottles and Lutris allow for the same experimental settings/runners to be chosen to run Windows games, they do not feature the same content-downloading-system Heroic uses for installing games. Meaning you'd have to rely on GOG's offline installers, which require 32-bit.

# What about Steam?

While there are certainly many games on Steam that do not require any 32-bit dependencies, Steam itself still does. That, however, [may change in the future](https://www.gamingonlinux.com/2025/11/valve-put-up-a-new-steam-linux-runtime-4-0-with-a-move-towards-64-bit/). [A 64-bit client is already available for MacOS](https://help.steampowered.com/en/faqs/view/5E0D-522A-4E62-B6EF).







