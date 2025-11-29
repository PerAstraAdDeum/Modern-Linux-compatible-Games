# Games compatible with modern Linux

A curated list of games that run on Linux and neither require x86 compatibility nor XWayland.

## Introduction

With the advent of DXVK, Proton and Gaming Distros like CachyOS and Bazzite, Gaming on Linux has reached an all-time-high.

This is a list of Windows games that you can play on Linux without the need for XWayland or 32-bit dependencies. All of the following games were tested with `ia32_emulation=0` Kernel argument. They were installed using Heroic Games Launcher's download system, which unlike GOG's offline installers does not require x86 emulation. To run them both `Enable Wine-Wayland(Experimental) (Wine version needs to support it)` and `Enable WoW64 (Experimental)` were enabled in Heroic's Wine settings.  



## List

| Game Name  | Platform | Tested with | DXVK/VK3D version | Runs? | Comment | 
| ------------- | ------------- | ------------- | ------------- | ------------- | ------------- |
| Batman™: Arkham Knight   | GOG | Heroic Games Launcher  | GE-Proton-Latest | yes |
| Bulwark Evolution: Falconeer Chronicles  | GOG | Heroic Games Launcher | GE-Proton Latest | yes |
| Control Ultimate Edition | GOG | Heroic Games Launcher  | GE-Proton-Latest | yes |
| Cyberpunk 2077 | GOG | Heroic Games Launcher  | GE-Proton-Latest | yes |
| Crysis®   | GOG | Heroic Games Launcher  | GE-Proton-Latest | yes | Uses the C1-Launcher. Warhead and Wars should work with it as well. |
| Dorfromantik   | GOG | Heroic Games Launcher  | GE-Proton-Latest | yes |
| Factorio   | GOG | Heroic Games Launcher  | GE-Proton-Latest | yes | Also has a native Linux port. |
| Middle-earth™: Shadow of Mordor™ Game of the Year Edition   | GOG | Heroic Games Launcher  | GE-Proton-Latest | yes |
| No Man's Sky | GOG | Heroic Games Launcher  | GE-Proton-Latest | yes |
| Rise of the Tomb Raider: 20 Year Celebration   | GOG | Heroic Games Launcher  | GE-Proton-Latest | yes |
| S.T.A.L.K.E.R.: Call of Prypiat - Enhanced Edition   | GOG | Heroic Games Launcher  | GE-Proton-Latest | yes |
| S.T.A.L.K.E.R.: Shadow of Chornobyl - Enhanced Edition   | GOG | Heroic Games Launcher  | GE-Proton-Latest | yes |
| Scorn   | GOG | Heroic Games Launcher  | GE-Proton-Latest | yes |
| Shadow of the Tomb Raider: Definitive Edition   | GOG | Heroic Games Launcher  | GE-Proton-Latest | yes |
| The Elder Scrolls V: Skyrim Special Edition   | GOG | Heroic Games Launcher  | GE-Proton-Latest | yes |  |
| The Witcher 3: Wild Hunt - Complete Edition   | GOG | Heroic Games Launcher  | GE-Proton-Latest | yes | You may need to launch the game exe directly. |
| Warhammer 40,000: Boltgun | GOG | Heroic Games Launcher  | GE-Proton-Latest | yes |
| Warhammer 40,000: Dawn of War - Definitive Edition   | GOG | Heroic Games Launcher  | GE-Proton-Latest | yes |


## How to check for compatibility

### 64-bit executable

The first thing you'd want to check if you'd like to know whether your favorite game relies on X86 is the [PCGamingWiki Website](https://www.pcgamingwiki.com/wiki/Home). Here you should check the API section to see if a 64-bit executable is available for the game in question:

<img width="836" height="192" alt="image" src="https://github.com/user-attachments/assets/5aae172d-e5bb-463b-9ee7-04d9d920e9f1" title="Tomb Raider (2013) API section" />  

This is from the Tomb Raider (2013) API section. As you can see, while there is a 64-bit executable for MacOS, Linux and Windows are lacking one and instead rely on a 32-bit executable.

Be advised that just because PCGamingWiki does list a 64-bit executable, that doesn't necessarily mean that the game will run in a pure 64-bit environment. For instance some games bring their own launchers which rely on 32-bit, and without them, you can't launch the game. If that is the case launching the game's executable might be a workaround.  

It may also be possible that the information on the PCGamingWiki is outdated or only valid for a certain distributor. GOG for instance often incorporates fan modifications in older games as part of their GOG Preservation Program, which sometimes include FOSS engine or executable recreations that run in 64bit.  

If you're on Linux and want to check if your game is running on 64-bit, you can do so either by installing [MangoHud](https://github.com/flightlessmango/MangoHud?tab=readme-ov-file#hud-configuration) and enable the `arch` variable in the config file, which will display the architecture of the current executable on the HUD:

![](https://github.com/user-attachments/assets/49732182-409d-4622-8983-2a5f5bc7f413)  
*Factorio with MangoHud being enabled. Notice the lines for arch and display server.*

This, however, is also not a conclusive indicator for a lack of dependence on 32bit. Grim Dawn for instance is a game that is playable in 64bit (and MangoHud will correctly report it so), starting the game however requires 32bit being enabled.

The only way to be sure that your game runs without the need for 32bit is by setting `ia32_emulation=0` as a Kernel argument and see if the game runs fine. If it does require 32bit, launching the game will most likely fail with `ShellExecuteEx failed: Internal error.`.

### XWayland

Sadly, determining whether a game needs XWayland without actually trying it is not possible, or at least I'm not aware of any means of doing so. Also, be advised that due to the nature of the interaction between a display server and your hardware/GPU drivers, the results of successfully testing a game with certain hardware doesn't necessarily mean it will run the same on a different system with a different GPU/driver version etc.

For already installed games you can again make use of MangoHud by setting the `display_server` variable:

![](https://github.com/user-attachments/assets/49732182-409d-4622-8983-2a5f5bc7f413)  
*Factorio with MangoHud being enabled. Notice the lines for arch and display server.*

# What about Steam?

While there are certainly many games on Steam that do not require any 32-bit dependencies, Steam itself still does. That, however, may change in the future [(Source)](https://www.gamingonlinux.com/2025/11/valve-put-up-a-new-steam-linux-runtime-4-0-with-a-move-towards-64-bit/). A 64-bit client is already available for MacOS [(Source)](https://help.steampowered.com/en/faqs/view/5E0D-522A-4E62-B6EF).







