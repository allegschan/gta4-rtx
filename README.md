<h1 align="center">Grand Theft Auto IV - RTX Remix Compatibility Mod</h1>

<br>

<div align="center" markdown="1"> 

Made specifically for NVIDIA's [RTX Remix](https://github.com/NVIDIAGameWorks/rtx-remix).  
Compatible with __Grand Theft Auto IV: The Complete Edition (1.2.0.59)__ 

**Feel free to join the discord server: https://discord.gg/FMnfhpfZy9**

<img width="1900" height="800" alt="image" src="https://github.com/user-attachments/assets/8608d1d7-5228-41c7-a62f-6335f38082f2" />

<br>

</div>

<div align="center" markdown="1"> 

### Table of Contents

__[Overview](#overview)__  
__[Installing](#installing)__   
__[Uninstalling](#uninstalling)__   
__[Usage](#usage)__   

<br>

</div>


## Overview
<div align="center" markdown="1"> 

First and foremost, __this is not a remaster__.  
It is a mod that allows the game to be modded with NVIDIA's [RTX Remix](https://github.com/NVIDIAGameWorks/rtx-remix).  
It comes with a [Baseline Remix Mod](https://github.com/xoxor4d/gta4-rtx-base-mod) and [GTAIV-AutoPBR](https://github.com/xoxor4d/gta4-rtx-autopbr-mod).  

<br>

RTX Remix has a certain overhead because of how it works and intercepts the game's draw calls and   
there are obvious drawbacks and things that will not work with such a new title. Don't expect this to be perfect.  

You'll likely experience a CPU bottleneck because of the amount of detailed meshes the game is rendering.  
This means that the performance you'll see in certain places is not entirely due to pathtracing.  

<br>

The mod comes with a custom [Remix Runtime](https://github.com/xoxor4d/dxvk-remix/tree/game/gta4_atmos10_nr2) required for a few game specific features,   
with [Ultimate ASI Loader](https://github.com/ThirteenAG/Ultimate-ASI-Loader/releases/tag/v9.0.0) to load the Compatibility Mod itself and a custom fork of [FusionFix](https://github.com/xoxor4d/GTAIV.EFLC.FusionFix.RTXRemix) tailored for RTX-Remix.

<img width="1909" height="665" alt="image" src="https://github.com/user-attachments/assets/9dd7646a-07f9-449b-b123-6f7f1a39404d" />


</div>

<br>

![img](.github/img/03.jpg)

<br>

###### The good:  
- **DLSS 4.5 (Ray Reconstruction 2) support**
- **DLSS 5.0 (Neural Rendering) support** (if you provide the necessary dll) - Integration made by [Sparkles](https://github.com/Kim2091/dxvk-remix/tree/gta4-atmos-dlss5)
- Includes an **Atmospheric sky system with Volumetric Clouds** made by the Community [Remix Plus / Numos](https://github.com/RemixProjGroup/dxvk-remix)
- Most objects rendered via fixed function to increase performance (compared to grabbing data from Vertexshaders)
- Cascaded anti culling of meshes
- All game lights (including the sun) are translated to remix lights
- Ability to create overrides for translated game lights (change position, color, intensity etc.)
- Vehicles now feature two headlights and two rear lights instead of single, centered ones
- Dynamic emissive surfaces work (vehicle lights, building-windows, shops etc.)
- Dynamic wetness that works similar to the original game  
  (only outdoors and with falloff on angled surfaces + raindroplets/impacts)
- Raindroplets on vehicles and character clothing
- Working vehicle dirt and livery
- Modification of remix runtime variables based on current timecycle settings
- Mobilephone works (but it is 3D and currently scales with the camera fov)
- Modified vertex shaders (based on FusionFix) so that remix is able to capture surface normals
- Ability to spawn unique _marker_ meshes that can be hidden based on distance, weather or time of day (these can be used to attach remix replacements or scene lights)
- Screenshot Mode, FreeCam Mode and other Utilities
- FusionFix compatible
- Many many tweakable settings via the in-game __F4__ menu
- A few PBR materials, hq-meshes (vegetation, modeled fences ..) and texture fixes
- Mod Installer / Updater

###### The bad:
- CPU Bottlenecked - Nvidia is constantly updating RTX-Remix and already made changes to improve this
- Can be stuttery when traversing the world
- No blood on peds

<br>
<br>

<div align="center" markdown="1"> 

<img width="1909" height="665" alt="image" src="https://github.com/user-attachments/assets/44471efe-594a-4498-a18a-66172395369a" />
<img width="1909" height="665" alt="image" src="https://github.com/user-attachments/assets/33d1abef-61c0-4636-860d-4680c82e9c8b" />

</div>

<br>

## Installing the Mod

- Grab the latest version
- Extract all files.
- Run the setup.
- Wait 5-10 mins.
- Enjoy the game!



## Uninstalling the Mod
- Delete `d3d9.dll` and `a_gta4-rtx.asi` or use the provided `_toggle-gta4-rtx.bat` to quickly toggle RTX-Remix
- Some other minor files remain in the updates folder (mainly `.img` files starting with `1__remix ..`)
- Re-install the official FusionFix mod if you used the custom Fork

<br>


## Usage
- Run the game like normal
- Press `F4` to open the in-game gui for some compatibility tweaks or debug settings
- If you notice heavy stuttering, launch the game with the included `_LaunchWithProcessorAffinity_2Cores_GTA4.bat`.  
  Doing this will assign 2 cores to GTA4 and the rest to Remix. If you want a 50/50 split, use `_LaunchWithProcessorAffinity_Half_GTA4__Half_Remix.bat`

<br>


<br>
<br>

##  Credits
- [NVIDIA - RTX Remix](https://github.com/NVIDIAGameWorks/rtx-remix)
- [People of the showcase discord](https://discord.gg/j6sh7JD3v9) - especially the nvidia engineers ✌️
- [Dear ImGui](https://github.com/ocornut/imgui)
- [imgui-blur-effect](https://github.com/3r4y/imgui-blur-effect)
- [minhook](https://github.com/TsudaKageyu/minhook)
- [toml11](https://github.com/ToruNiina/toml11)
- [Ultimate-ASI-Loader](https://github.com/ThirteenAG/Ultimate-ASI-Loader)
- [miniz](https://github.com/richgel999/miniz)
- [Rapidjson](https://github.com/Tencent/rapidjson)
- [DiscordRPC](https://github.com/discord/discord-rpc)
- [FusionFix](https://github.com/ThirteenAG/GTAIV.EFLC.FusionFix)
- [FusionShaders](https://github.com/Parallellines0451/GTAIV.EFLC.FusionShaders)
- [Rage-Shader-Editor](https://github.com/ImpossibleEchoes/rage-shader-editor-cpp)
- [IV-SDK](https://github.com/Zolika1351/iv-sdk/)
- [IV-SDK-DotNet](https://github.com/ClonkAndre/IV-SDK-DotNet)
- [AssaultKifle47](https://github.com/akifle47)
- [DayL](https://www.gtainside.de/de/user/falcogray)
- [Entity](https://www.youtube.com/@paprykszadolowski8796)
- [Gabdeg](https://www.youtube.com/@gabdeg793)
- [Hemry](https://www.youtube.com/@Hemry81)
- [Danlopand / Thundery_Dan](https://github.com/DANLOPAND)
- [KapibosRU](https://www.youtube.com/channel/UCqZ2NI_fQKRN-Onypt9aIGQ)
- [Budgie](https://www.patreon.com/c/BudgieGames)
- [Alex from Digital Foundry](https://www.youtube.com/watch?v=vGxPdcMQfwg)
- [Sparkles (Remix Plus - Numos - DLSS5 Integration)](https://github.com/Kim2091)
- [CR (Remix Plus)](https://github.com/sambow23)
- [TheGreatHMMMM (Remix Plus)](https://github.com/TheGreatHMMMM)
- [Gokuwashere (Remix Plus)](https://github.com/BrunchyChineapple)
- All 🍓 Testers

<div align="center" markdown="1"> 

<br>

<img width="2560" height="900" alt="image" src="https://github.com/user-attachments/assets/3d54540e-59ed-4f1a-9ca6-31b2a2bbdfec" />

<img width="1909" height="665" alt="image" src="https://github.com/user-attachments/assets/c6d08808-330b-44fa-8d93-da17a1c0e65f" />


</div>
