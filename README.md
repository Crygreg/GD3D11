# G3D11 (Gothic Direct3D 11) Renderer - Atmospheric Edition

***English:***
First and foremost: I am no expert in C++ programming. DON'T WORRY! The Renderer works absolutely fine. The point is that I'd love to make even more changes and additions to the Renderer, bringing back features from the old Gothic DX7 Renderer but also expanding on features that would allow mods to determine their distinguished atmosphere with the new available sky textures, fog values etc.

Sadly, as of now, this is the best I can do. I'll provide the source files in the hopes that maybe someone takes interest in this forgotten code again and helps realize the Renderer's full potential.

*The goal of this version of the Renderer is different than the others. Here's what's changed:*
- Update from my last version (hidden) based on SaiyanKing's version with all its features and bugfixes over kirides'
- A better system to distinguish between various .zens and worldspaces (sadly no system to actually distinguish between mods, even if it's the same worldspace so I had to make a decision for NewWorld and AddonWorld and OldWorld: AddonWorld looks like the usual G2 Renderer experience, NewWorld has more of a G1-styled look but updated and OldWorld has its classic DX7 styled look)
- More Sky Texture variants from G1, G2 and custom ones to use in the future when modders create their own worldspaces etc. (hopefully there will be a better system in place for this too)
- a bit better  display of the skydome (a bit brighter but I still need to figure out how to improve it to be closer to DX7's display of the skybox)
- improved fog colors (no more orange tint in G1, a bit more reddish now etc.)


*Future plans:*
- As mentioned, I want to implement a system that allows to check for MODS, not just .zen file names as of now. Alternatively, even better, a menu that  allows you to determine your preferenced look for the game OR simply displaying whatever sky texture and fog values are determined by the game's / mod's settings and files!
- More sky variants appearing throughout the day, allowing for a more natural cycle (without withdrawing from the atmospheric artstyle that is meant to be GOTHIC)
- Features from the old DX7 Renderer (trees reacting to wind, sea waves, displaying atmospheric lights, maybe displaying whatever sky texture & fog values are determined by the game's / mod's settings and files as it was the case in the original Renderer, etc.)

If you are interested in helping out in the cause, let me know or ... well, simply download the source files and go ahead!
Thank you and have fun playing the game.

*Known Issues:*
- G1 is supposed to have a more updated skytexture, yet displays the original one still


***German / Deutsch:***
Zuallererst: Ich bin kein Experte in C++-Programmierung. KEINE BANGE! Der Renderer funktioniert absolut einwandfrei. Der Punkt ist, dass ich gerne noch mehr Änderungen und Ergänzungen an dem Renderer vornehmen würde, um die Funktionen des alten Gothic DX7 Renderers zurückzubringen, aber auch um Funktionen zu erweitern, die es Mods erlauben würden, ihre eigene Atmosphäre mit den neuen verfügbaren Himmelstexturen, Nebelwerten usw. zu bestimmen.

Leider ist das im Moment das Beste, was ich tun kann. Ich stelle die Quelldateien in der Hoffnung zur Verfügung, dass sich vielleicht jemand wieder für diesen vergessenen Code interessiert und dabei hilft, das volle Potenzial des Renderers auszuschöpfen.

*Das Ziel dieser Version des Renderers ist anders als die anderen. Hier ist, was sich geändert hat:*
- Update von meiner letzten Version (versteckt) basierend auf SaiyanKings Version mit all ihren Features und Bugfixes gegenüber kirides' Version
- Ein besseres System, um zwischen verschiedenen .zens und Welträumen zu unterscheiden (leider gibt es kein System, um zwischen Mods zu unterscheiden, selbst wenn es sich um denselben Weltraum handelt, so dass ich eine Entscheidung für NewWorld und AddonWorld und OldWorld treffen musste: AddonWorld sieht aus wie das übliche G2-Renderer-Erlebnis, NewWorld hat eher ein G1-artiges Aussehen, aber aktualisiert und OldWorld hat sein klassisches DX7-artiges Aussehen)
- Mehr Himmelstextur-Varianten aus G1, G2 und eigene, die in Zukunft verwendet werden können, wenn Modder ihre eigenen Welträume usw. erstellen (hoffentlich wird es auch dafür ein besseres System geben)
- eine etwas bessere Darstellung der Himmelskuppel (etwas heller, aber ich muss noch herausfinden, wie ich sie verbessern kann, damit sie näher an die Darstellung der Skybox in DX7 herankommt)
- verbesserte Nebelfarben (kein Orangestich mehr in G1, jetzt etwas rötlicher usw.)

*Zukünftige Pläne:*
- Wie bereits erwähnt, möchte ich ein System implementieren, das es erlaubt, nach MODS zu suchen, nicht nur nach .zen-Dateinamen wie bisher. Oder, noch besser, ein Menü, das es einem erlaubt, sein bevorzugtes Aussehen für das Spiel zu bestimmen ODER einfach die Himmelstextur und Nebelwerte anzuzeigen, die durch die Einstellungen und Dateien des Spiels/der Mods bestimmt werden!
- Mehr Himmelsvarianten, die im Laufe des Tages erscheinen, um einen natürlicheren Zyklus zu ermöglichen (ohne den atmosphärischen Artstyle, der GOTHIC sein soll, zu vernachlässigen)
- Features aus dem alten DX7 Renderer (Bäume, die auf Wind und Wellen reagieren, atmosphärische Lichter, vielleicht die Anzeige der Himmelstextur- und Nebelwerte, die durch die Einstellungen und Dateien des Spiels/Mods bestimmt werden, wie es im ursprünglichen Renderer der Fall war, usw.)

Wenn ihr Interesse habt, dabei zu helfen, lasst es mich wissen oder ... nun, ladet einfach die Quelldateien herunter und legt los!
Vielen Dank und viel Spaß mit dem Spiel.

*Bekannte Probleme:*
- G1 sollte eigentlich eine aktuellere Himmelstextur haben, zeigt aber immer noch die Originaltextur an.

CREDITS:
- Degenerated: Original creator of DX11
- Bonne6: Revamped the DX11 into the Clockwork Edition and allowed it to run smoothly and have more customization options
- Kirides: Again developing DX11 further with his "Yet Another D3D11 Renderer" version
- SaiyanKing: Another great upgrade and bugfixing with his work
- Gothic Reloaded & Gothic Modderdatabase: For the new skytextures



# ORIGINAL DESCRIPTION BY SAIYANKING


# GD3D11 (Gothic Direct3D 11) Renderer [![GitHub Actions](https://github.com/kirides/GD3D11/actions/workflows/build.yml/badge.svg)](https://github.com/Kirides/GD3D11/actions) [![GitHub release (latest by date including pre-releases)](https://img.shields.io/github/v/release/Kirides/GD3D11?include_prereleases)](https://github.com/Kirides/GD3D11/releases)


This mod for the games **Gothic** and **Gothic II** brings the engine of those games into a more modern state. Through a custom implementation of the DirectDraw-API and using hooking and assembler-code-modifications of Gothic's internal engine calls, this mod completely replaces Gothic's old rendering architecture.

The new renderer is able to utilize more of the current GPU generation's power. Since Gothic's engine in its original state tries to cull as much as possible, this takes a lot of work from the CPU, which was slowing down the game even on today's processors. While the original renderer did a really great job with the tech from 2002, GPUs have grown much faster. And now, that they can actually use their power to render, we not only get a big performance boost on most systems, but also more features:

* Dynamic Shadows
* Increased draw distance
* Increased Performance
* HBAO+
* Water refractions
* Atmospheric Scattering
* Heightfog
* Normalmapping
* Full DynamicLighting
* Vegetationgeneration
* Hardware Tessellation
* Editor-Panel to insert some of the renderers features into the world
* Custom-Built UI-Framework based on Direct2D
* Rewritten bink player for better compatibility with bink videos
* FPS-Limiter

## Installation & Usage
> **Note**: In the past there used to be separate files for Gothic 1 and Gothic 2, this has now changed since the mod will automatically detect the game.
1. Download the **GD3D11-*LATEST_VERSION*-ci.zip** file from the **Assets** section in the latest release of this repository (e.g. [kirides/releases](https://github.com/kirides/GD3D11/releases/latest)).
3. Unpack the zip file and copy the content into the `Gothic\system\` or `Gothic2\system\` game folder.
4. When starting the game you should see the version number of GD3D11 in the top-left corner.
5. As soon as you start the game for the first time after the installation you should press F11 to open the renderer menu and press `Apply(*)`. This saves all the options to `Gothic(2)\system\GD3D11\UserSettings.ini`.

## Bugs & Problems

If you have problems with building GD3D11 after following these instructions or experience bugs/problems with GD3D11 itself, open an issue on this GitHub page or post in the D3D11 thread on ["World of Gothic" (WOG)](http://forum.worldofplayers.de/forum/forums/104-Editing).  
But first take a look at the [KNOWN ISSUES](./known_issues.md)

## Building

### Latest version

Building the mod is currently only possible with windows, but should be easy to do for anyone. To build the mod, you need to do the following:

- Download & install **Git** (or any Git client) and clone this GitHub repository to get the GD3D11 code.
- Download & install **Microsoft Visual Studio 2019** (Community Edition is fine, make sure to enable C++ Tools during installation!). Might work on 2015 or 2017 but untested.
- ~~Download ... DirectX SDK ...~~ Not dependent on DirectX SDK anymore.
- Optional: Set environment variables "G2_SYSTEM_PATH" and/or "G1_SYSTEM_PATH", which should point to the "system"-folders of the games.

To build GD3D11, open its solution file (.sln) with Visual Studio. It will the load all the required projects. There are multiple build targets, one for release and one for developing / testing, for both games each:

* Gothic 2 Release using AVX: "Release_AVX"
* Gothic 1 Release using AVX: "Release_G1_AVX"
* Gothic 2 Release using old SSE2: "Release"
* Gothic 1 Release using old SSE2: "Release_G1"
* Gothic 2 Develop: "Release_NoOpt"
* Gothic 1 Develop: "Release_NoOpt_G1"

> **Note**: A real "debug" build is not possible, since mixing debug- and release-DLLs is not allowed, but for the Develop targets optimization is turned off, which makes it possible to use the debugger from Visual Studio with the built DLL when using a Develop target.

Select the target for which you want to built (if you don't want to create a release, select one of the Develop targets), then build the solution. When the C++ build has completed successfully, the DLL with the built code and all needed files (pdb, shaders) will be copied into the game directory as you specified with the environment variables.

After that, the game will be automatically started and should now run with the GD3D11 code that you just built.

When using a Develop target, you might get several exceptions during the start of the game. This is normal and you can safely continue to run the game for all of them (press continue, won't work for "real" exceptions of course).
When using a Release target, those same exceptions will very likely stop the execution of the game, which is why you should use Develop targets from Visual Studio and test your release builds by starting Gothic 1/2 directly from the game folder yourself.

### Producing the Redistributables
- Compile all versions (e.g. by running `BuildAll.bat`)
- Run `CreateRedist_All.bat` to create separate zip files containing the required files
> **Note**: On CI this process is different. Release builds will bundle all DLL files (SpacerNET is a seperate build) and the launcher will decide which version should be used at runtime. Therefore there is only one zip file for Gothic 1 and Gothic 2.

### Dependencies

- HBAO+ files from [dboleslawski/VVVV.HBAOPlus](https://github.com/dboleslawski/VVVV.HBAOPlus/tree/master/Dependencies/NVIDIA-HBAOPlus)
- [AntTweakBar](https://sourceforge.net/projects/anttweakbar/)
- [assimp](https://github.com/assimp/assimp)

## Special Thanks

... to the following people

- [@ataulien](https://github.com/ataulien) (Degenerated @ WoG) for creating this project.
- [@BonneCW](https://github.com/BonneCW) (Bonne6 @ WoG) for providing the base for this modified version.
- [@lucifer602288](https://github.com/lucifer602288) (Keks1 @ WoG) for testing, helping with conversions and implementing several features.
- [@SaiyansKing](https://github.com/SaiyansKing) for fixing a lot of issues and adding major features.

<a href="https://github.com/kirides/GD3D11/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=kirides/GD3D11" />
</a>

## License

- HBAO+ is licensed under [GameWorks Binary SDK EULA](https://developer.nvidia.com/gameworks-sdk-eula)
