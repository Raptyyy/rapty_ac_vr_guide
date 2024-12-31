# VR guide for Assetto Corsa and CSP

The purpose of this guide is to help with basic VR setup and cover some of the main settings and features.  
It also covers usage of OpenComposite and the OpenXR Toolkit  
This guide is written with Content Manager and Custom Shaders Patch in mind, not intended to work with vanilla Assetto Corsa.

> [!NOTE]
> If you have anything useful to add to the guide or see a mistake, feel free to make an issue and I will correct it.  

## 0. Table of Contents
1. [Prerequisites](#1-prerequisites)  
2. [Basic VR Setup](#2-basic-vr-setup)  
3. [Setting up Custom Shaders Patch (CSP)](#3-setting-up-custom-shaders-patch-csp)  
4. [Setting up Pure](#4-setting-up-pure)
5. [Video and CSP Presets](#5-video-and-csp-presets)  
6. [What is Foveated Rendering](#6-what-is-foveated-rendering)  
7. [Video Settings](#7-video-settings)  
8. [Custom Shaders Patch settings](#8-custom-shaders-patch-settings)  
9. [OpenComposite and OpenXR Toolkit](#9-opencomposite-and-openxr-toolkit)  
10. [VRPerfKit](#10-vrperfkit)  
11. [Additional Notes](#11-additional-notes)  

Quick links: 
- [Settings Presets](#5-video-and-csp-presets)
- [What is Foveated Rendering](#6-what-is-foveated-rendering)  
- [OpenComposite and OpenXR Toolkit](#9-opencomposite-and-openxr-toolkit)  

## 1. Prerequisites
- Non-pirated copy of Assetto Corsa (Pirated copies do not get any support or help in the CSP discord)
- Latest version of Content Manager  
- Latest version of Custom Shaders Patch unless said otherwise.  
- Latest version of Pure (Delivers the best image in VR)  

## 2. Basic VR setup
Click on your brand of headset to expand the instructions  
<details>
  <summary>Oculus / Meta</summary>

**Native Oculus implementation (easiest method):**  
1. First make sure that you have successfully set up Quest link or Air link and that the headset is connected to your PC - [Tutorial how to do so](https://www.meta.com/help/quest/articles/headsets-and-accessories/oculus-link/connect-with-air-link/)  
  1.1. If youre using an Oculus Rift (S) then you simply need to have the headset connected and showing in the oculus app.  
2. In the Oculus App, Settings > General enable "Unknown sources" and next to the "OpenXR Runtime" press "Set Oculus as active" (If its greyed out then you don't need to press it)  
3. In content manager go to Settings > Assetto Corsa > Video and set "Rendering Mode" to "Oculus Rift", this does not require SteamVR.  

**Using Virtual Desktop and OpenComposite (Can give better results however costs money):**  
1. Purchase Virtual Desktop on the Oculus / Meta store (do not buy it on steam itself)
2. Follow the instructions provided in Virtual Desktop to connect your headset to your PC (Quest / Air Link is not required).   
3. Open the Virtual Desktop Streamer application, and under settings, select VirtualDesktopXR (VDXR) as the OpenXR runtime.
4. Set up OpenComposite, [instructions here](#to-install-opencomposite)
5. In content manager go to Settings > Assetto Corsa > Video and set "Rendering Mode" to "OpenVR"  

Using this method you can also look into the [OpenXR Toolkit](#openxr-toolkit)

**Using SteamVR (Generally not recommended):**  
1. First make sure that you have successfully set up Quest link or Air link and that the headset is connected to your PC - [Tutorial how to do so](https://www.meta.com/help/quest/articles/headsets-and-accessories/oculus-link/connect-with-air-link/)
  1.1. If youre using an Oculus Rift (S) then you simply need to have the headset connected and showing in the oculus app.  
3. Install and set up SteamVR from Steam  
4. In content manager go to Settings > Assetto Corsa > Video and set "Rendering Mode" to "OpenVR"

### Oculus / Meta additional notes and troubleshooting  

- Game lagging when using the headset wirelessly: Your router might not be able to handle the high amount of bandwidth required for a smooth experience, this will generally show as high network latency. Try to lower the bitrate in the [Oculus Debug Tool](https://smartglasseshub.com/oculus-debug-tool/) or set it to 0 for auto bitrate.  
- USB-C, Make sure your headset runs USB 3 and not USB 2, if it keeps connecting via USB 2 even with a new cable and using a USB 3 port, reset your headset to factory defaults which will fix the issue.
- using USB-C set the bitrate to 500mbps or higher in the Oculus Debug Tool. More info about the [Oculus Debug Tool here](https://smartglasseshub.com/oculus-debug-tool/).  

</details>

<details>
  <summary>SteamVR headsets (Vive, Index, Bigscreen beyond)</summary>
  
1. Make sure your headset is connected to your PC
2. Install and set up SteamVR from Steam  
3. In Content Manager go to Settings > Assetto Corsa > Video and change "Rendering Mode" to "OpenVR"
</details>

<details>
  <summary>Windows Mixed Reality headsets</summary>


**Using OpenComposite (Highly recommended):**  
1. Make sure your headset is connected to your PC  
2. Install and set up Windows Mixed Reality from the Microsoft Store
3. Install and set up OpenXR Tools for Windows Mixed Reality from the Microsoft Store  
  3.1. If you see a button that says "Set as active runtime" - press it.  
5. Set up OpenComposite, [instructions here](#to-install-opencomposite)  
6. In Content Manager go to Settings > Assetto Corsa > Video and change "Rendering Mode" to "OpenVR"  

Using this method you can also look into the [OpenXR Toolkit](#openxr-toolkit)

**Using SteamVR:**  
1. Make sure your headset is connected to your PC  
2. Install and set up Windows Mixed Reality from the Microsoft Store  
3. Install and set up SteamVR from Steam  
4. Install Windows Mixed Reality for SteamVR from Steam  
5. In Content Manager go to Settings > Assetto Corsa > Video and change "Rendering Mode" to "OpenVR"  
</details>

<details>
  <summary>Pimax headsets</summary>

**Using OpenComposite (Highly recommended):**  
1. Make sure your headset is connected to your PC  
2. Install and set up Pimax Play, [link here](https://pimax.com/pages/downloads-manuals)  
3. Set the OpenXR Runtime to Pimax OpenXR in Pimax Play, [instructions here](https://pimax.com/blogs/blogs/how-to-use-pimax-openxr)  
5. Set up OpenComposite, [instructions here](#to-install-opencomposite)  
6. In Content Manager go to Settings > Assetto Corsa > Video and change "Rendering Mode" to "OpenVR"  

Using this method you can also look into the [OpenXR Toolkit](#openxr-toolkit)

**Using SteamVR:**  
1. Make sure your headset is connected to your PC
2. Install and set up Pimax Play, [Link here](https://pimax.com/pages/downloads-manuals)
3. Install and set up SteamVR from Steam  
4. In Content Manager go to Settings > Assetto Corsa > Video and change "Rendering Mode" to "OpenVR"
</details>

> [!TIP]
> Once you have the correct settings applied for your headset, test it out in singleplayer first before joining a server !

## 3. Setting up Custom Shaders Patch (CSP)
1. In Content Manager go to Settings > Custom Shader Patch  
  1.1 If you are prompted to install Custom Shaders Patch, press install  
2. Go to Settings > Custom Shader Patch > About & Updates and verify that you are on the latest version which should be at the top of the list on the right side.  
  2.1 I don't recommend using the "recommended" version as it is quite old by now and wont work in some servers

If you are using a preview version of CSP from Patreon then install it manually or through the quick install link in the Patreon post  

## 4. Setting up Pure
Pure is recommended for VR as it delivers a more realistic and consistent image, also has a lot of adjustability and various post processing filters to change the look of the game.  
1. Make sure you are on the latest version of CSP
2. Go to Peter Boese Patreon page and download Pure from there, it costs $1 - [Pure Patreon](https://www.patreon.com/c/peterboese/posts)
3. There is an installation guide in the Pure post, follow it thoroughly. [Link to the guide here too](https://youtu.be/456BO7vKui0?si=BQ0YIq6q3f7BuZyc)
4. Make sure that exposure is set to 100% in Settings > Assetto Corsa > Miscellaneous > Exposure

> [!WARNING]
> Incorrect installation of Pure can cause major performance issues !

## 4.1 Pure pp filters 
Pure, PureVR - these come with Pure, PureVR would be my recommendation out of those two  
[Natural Mod PP Filter](https://www.overtake.gg/downloads/natural-mod-pp-filter.4551/) Natural looking filter with good performance  
[Improved Visuals PureCS Filter](https://www.overtake.gg/downloads/improved-visuals-pure-cs-filter-screen-and-vr-ppfilter.54256/) VR focused pp filter with great adjustability  
[C13 Aegis Filter](https://www.overtake.gg/downloads/c13-aegis-post-processing-filter.59979/) Probably one of the best looking filters, newer versions are available on patreon, might not be great performance wise  

## 5. Video and CSP Presets
> [!WARNING]
> Save your current settings as presets in Content Manager !
## 5.1 Video Presets for VR
These are some video presets I made if you don't want to read through the settings below, try each one out and see what works best. Also adjust to your needs.  
Make sure to double check the Rendering Mode so that its set correctly for your headset !  

- High Performance: [Link here](https://acstuff.club/s/lW4B) (Disable post processing if you need even more performance)  
- Balanced: [Link here](https://acstuff.club/s/MvZ2)
- High Quality: [Link here](https://acstuff.club/s/GKoQ) (For best graphics find a good pp filter)

## 5.2 CSP Setting Presets
These presets are simply to be used as a base for your own preference. Test the presets out and adjust as needed.  
> [!NOTE]
> Foveated rendering (VRS) is NOT enabled in any of these, set it yourself as needed.

- High Performance - [Link here](https://acstuff.club/s/rFa) (This preset has a lot of modules disabled for a little extra performance)  
- Balanced - [Link here](https://acstuff.club/s/OG43)  
- High Quality - [Link here](https://acstuff.club/s/Lywh)  

## 6. What is Foveated Rendering
Foveated rendering is a method in VR to achieve greater performance by rendering the outer parts of the image at lower resolution as shown in the example below. This makes sense on most headsets as only the center part of the lense is in focus and can display the image clearly.  
Foveated rendering is the biggest performance increase that you can get in VR so it is highly recommended to take advantage of it.  

<img src="https://github.com/Raptyyy/rapty_ac_vr_guide/blob/980c83fc6ec2016ade1d3e7c172c3838679fc5f9/resources/fov_rend_example.jpg" width="1280">   

Ways to enable / use Foveated rendering (Use only one of these methods):  
- Enable "Nvidia VRS" in Custom Shaders Patch, [explained further here](#nvidia-vrs) (Easiest way to enable it)  
- Enable Foveated Rendering in the OpenXR Toolkit if you're using OpenComposite, [explained further here](#recommended-settings-for-the-toolkit) (Gives more adjustability compares to Nvidia VRS)  
- For Pimax users you can enable Foveated Rendering in Pimax Play (More convenient but less options compared to the OpenXR Toolkit)  
- VRPerfKit also has Foveated Rendering, [explained further here](#10-vrperfkit) (Only recommended for SteamVR users who want more adjustability compared to Nvidia VRS)  

> [!WARNING]
> Foveated rendering might be undesirable on headsets that use pancake lenses with large sweetspots such as Quest 3 or Pico 4, on such headsets it is recommended to use a very large center part of the Foveated image or to just not use Foveated rendering at all.

> [!NOTE]
> Note that since Assetto Corsa is a DirectX 11 game, Foveated Rendering works ONLY on Nvidia 16xx, 20xx, 30xx and 40xx series GPUs or newer. 

## 7. Video Settings
This covers all the settings in Content Manager > Settings > Video  
> [!TIP]
> Note that in Content Manager most settings have a green "i" icon next to them that will show what each setting does and the performance impact  

### Resolution and FPS
**Rendering Mode** should already be set depending on your headset as shown above.  

**Fullscreen** will simply display the game in Fullscreen instead of a window, recommended to have it `enabled` as it slightly helps with performance but its not a must.  

**Resolution** doesnt really matter for VR use, it will only set the game window size, does not affect VR image quality.  

**Virtual synchronization** is not needed, keep it `disabled`  

**Limit framerate** is not needed in VR as the headset will limit fps as needed by itself, keep it `disabled`.  

### Quality
**MSAA** is an Anti-Aliasing technique which helps a lot with jagged edges / pixelation or shimmering especially into the distance. Highly recommended to keep it enabled in VR, either `2x` or `4x`. `8x` will have a major impact on performance and is generally not worth using.  

**Anisotropic Filtering** helps with texture clarity into the distance, it has a very low performance impact so recommended to just keep it at `16x`.  

**World details** will affect object amount on tracks (if they support it), set it as needed. Can also be adjust in-game using the "View & Video Settings" app.  

**Shadows resolution** affects how sharp the shadows will look. Higher resolution will make shadows look better but decrease performance. I would recommended using `1024x1024` and increase if performance isnt an issue.  

**Smoke generation** Simply controls the smoke quantity, adjust as needed, but I would recommend using CSP smoke instead (Custom Shaders Patch > Particles FX > New smoke and dust)  

### Reflections
**Reflection Resolution** simply adjusts how sharp / clear the reflections will look, `512x512` is a good base value to start with, can increase if needed.  

**Rendering frequency** adjusts how smoothly the reflections will reflect, Set it to either `one or two faces per frame`, any higher is not really needed as they get reprojected anyway. don't use Static either.  

**Rendering distance** Adjusts the reflection rendering distance, does not have a noticeable performance impact so you can set it to `at least 1000m` or higher if needed.  

### Post-Processsing
**Enable post-processing effects** this enables post processing in general, very useful to have to improve the graphics and look of the game, however has a big performance impact. Most PCs should have it `enabled` but low-end PCs should probably `disable` it on more demanding servers.  

**Overall Quality** sets the post processing resolution, `High` is a good middle ground performance wise but can also just set it to `Maximum`.  

**Glare Quality** sets the quality of glare effects, `High` is a good middle ground performance wise but can also just set it to `Maximum`.  

**Depth of field** adjusts the depth of field quality, only works in replays so can keep it `Off` if you don't care about it.  

**Motion blur** not recommended to use with VR, set it to `Off`  

**Saturation** is basically the intensity of the colors, keep it at `100%` and adjusts colors in Pure instead if needed.  

**Heat shimmering** adds a heat shimmering effect, `set as needed`  

**Sunrays** enables sun rays / god rays / sun shafts, `set as needed`  

**FXAA** is an anti aliasing technique, keep it `enabled` as it is required for some CSP functionality but will not affect image quality in VR.

### Mirrors
**Mirror resolution** how sharp / clear the mirrors will look, higher resolutions will reduce performance, `256x1024` is a good base value  

**High quality** enables additional effects in the mirrors and increases the rendering distance (from 400 to 800 meters), will reduce performance, recommended to `enable`.    

### Oculus (only affects Oculus / Meta headsets)
**Pixels per display** is same as resolution multiplier in the oculus app or oculus pixels per display pixel override in oculus debug app, `set as needed`  

**Mirror texture** enables the game window to show your VR view, recommended to `enable` it  

### System
I would recommend not messing with these settings as they don't really have any meaningful impact and can cause issues.

## 8. Custom Shaders Patch settings
I will not cover every setting in CSP (that would be a lot to cover), but only the ones that matter for VR performance.  

### General Patch Settings
**Audio > Decompress Samples** recommended to have it `enabled` if you have more than 16GB of RAM, helps with CPU load.  

**New KN5 loader** recommended to have it `enabled`, helps with memory usage  

CPU optimizations:
- **Flatten nodes** keep it `enabled`  
- **Chunks optimization** helps with CPU load. Set it to `Advanced` unless you have issues (like the screen going black), then keep it at `Basic`.  
- **Limit audio for other cars** set it to `Always` if you have a slower PC.

GPU optimizations: 
- **Optimize meshes some more** helps with GPU load, have it `enabled`  
- "**Deduplicate meshes**" helps with VRAM, have it `enabled`  
- "**Upgrade AC textures**" will make certain textures more efficient VRAM wise, recommended to have it `enabled`. Don't enable this if you have a low amount of free disk space.

### Extra FX
Extra FX doesnt work in VR so this will have no effect, keep it `disabled` if you don't ever use Extra FX.

### GUI
**New driver tags** recommended to have it `enabled` so you can see driver names in VR. Its not a performance tweak but a very useful thing to have.  
**Font Scale** Set this to `125%` or higher if you struggle reading the names.  

### Graphics Adjustments
**AMD FidelityFX SuperResolution** also known as "FSR" is an upscaler that can help with performance by rendering the game at a lower resolution and then upscaling the image. Should only be needed for lower end PCs.  

LOD settings:
- **Force low-res drivers for other cars in first person view** have it `enabled` for performance
- **Multiplier for car LODs** this sets how far away the car LOD (level of detail) will change, lower multiplier will help with performance but can make cars look worse up close, for performance set it to `75%`.
- **Multiplier for track LODs** same thing as car LODs but for the track, I would recommend not going below `80%` as it can cause issues.
- **Multiplier for trees LODs** same thing as car LODs but for 3D trees, you can set it to `0% for best performance` if you don't care about 3D trees (makes them 2D instead), otherwise keep it around `100%`.  
- **Add extra collider-based LODs for distant cars** will make low quality LODs for cars that don't have them, can help a lot in dense lobbies like VDC, recommended to have it `enabled`. Set the "Limit LODless cars" to a low value between 5 to 10 for best performance.

**Post processing antialiasing** set to `disabled` as post process AA doesnt work in VR (Will update this if it changes)  

**Accessible color buffer > Full resolution for better quality** set to `disabled` for a tiny boost in performance  

**Draw grooves over track, but before dynamic entities** Can help with performance but can also cause issues on some tracks (Like mirror / see through roads), use with caution.  

### Lighting FX
**Cars casting lights** set this to a lower amount like `5` for better performance in dense lobbies, lights are expensive performance wise.

**Disable mirroring in first person view**"helps with performance a bit, have it `enabled`  

**Enable lighting in reflections** `disabled` for a performance boost  

### Neck FX
Not related to performance but there are good NeckFX scripts for VR to enhance immersion or comfort, here are two most popular ones: 
- [AC Head Physics](https://www.overtake.gg/downloads/ac-head-physics.68266) fancier script, has more movement  
- [NeckFX LUA script](https://www.overtake.gg/downloads/neckfx-lua-script-vr-stabilize.65087) more basic, static script.

### Smart Mirror
**Custom render distance** `enabled` and set the distance to 400 meters if you use High Quality mirrors in video settings, helps with performance.

**Real mirrors** highly recommended in VR, makes the mirrors change perspective based on your head movement also lets you adjust mirror positioning through the "Mirrors" app in-game
- **Active** `enabled`
- **Alter FOV** set based on your preference, I have it `disabled`
- **Refresh rate per frame** set to` Update single reflection per frame` for best performance, can look a little laggy on lower refresh rate headsets, use higher if needed.

### Weather FX
**Weather style** this should be set to either `Pure Gamma` or `Pure LCS`, Gamma is better performance wise as of now but LCS will produce a more natural image (Can have various issues).  

**Replace YEBIS with lightweight alternative** `enabled`, helps a lot to reduce the performance impact of post-processing, does not work with some pp filters like C13.  

**Automatically guess white reference point** This can make the UI very bright when using Pure, `disable` it.  

### Mode Tweaks VR:
Make sure the extension is enabled (Active)  

**Single Pass Stereo** Highly recommend to `enable` this, helps a lot with CPU load, can cause certain Pure effects to not work. Might work for AMD GPUs too.  

**Single YEBIS pass** makes post processing slightly less demanding to run, `enable` for performance if needed, can cause certain Pure effects to not work.  

### Nvidia VRS
also known as Foveated rendering ([What is Foveated Rendering](#6-what-is-foveated-rendering)) is probably the most important performance tweak for VR, however only works for Nvidia GPUs.  
If you want to use Nvidia VRS:  
- **Nvidia VRS** `enabled`
- **VRS preset** `Custom`
- **VRS rate** `High performance`, can set to Highest performance if you need every bit of performance but it will be more visible.
- **VRS detailed area** `Balanced`, set it to `Wide` if you use a Quest 3 or Pico 4 as they will show foveated rendering more clearly.

You can also test using the "VRS preset" presets.

**Corners masking optimization** recommended to keep this one `enabled`, helps with performance but will create a black area around the VR image in the game window / VR mirror  

**Custom VR HUD rendering** recommended to keep this `enabled` as it makes the HUD work better in VR  

## 9. OpenComposite and OpenXR Toolkit
### OpenComposite
Allows you to play SteamVR games without actually needing SteamVR, it is highly recommended for users wanting more performance.  
On non native SteamVR headsets (Quest, Pimax, WMR) SteamVR simply acts as a middle layer which increases resource usage while bringing no real benefit to your VR experience.  
OpenComposite can also be used with Virtual Desktop when using it with VDXR, [more info here](https://github.com/mbucchia/VirtualDesktop-OpenXR/wiki)  
> [!IMPORTANT]
> Using OpenComposite with native SteamVR headsets wont really bring much benefit since they will require SteamVR either with OpenVR or OpenXR.

> [!WARNING]
> Pico standalone headsets dont have their own OpenXR runtime, so to bypass SteamVR you would need to use Virtual Desktop with VDXR and OpenComposite.

### To install OpenComposite:
1. Download the opencomposite dll file either from [this repository](https://github.com/Raptyyy/rapty_ac_vr_guide/raw/refs/heads/main/resources/openvr_api.dll) or from the [OpenComposite mirror](https://opencomposite.znix.xyz/builds/) (Select the first result and download the Platform: x64	x64/openvr_api.dll file)
2. Make sure the file is called "openvr_api.dll" and place it in to "steamapps\common\assettocorsa\system\x64", if prompted to overwrite files, press yes.
3. In Content Manager > Settings > Video set "Rendering Mode" to "OpenVR"
4. You also need to make sure your headset is using its native OpenXR Runtime (or VDXR for Virtual Desktop) and not the SteamVR one  

> [!IMPORTANT]
> If you encounter any issues using OpenComposite, I have the [original dll file uploaded here](https://github.com/Raptyyy/rapty_ac_vr_guide/raw/refs/heads/main/resources/openvr_api.dll.og), rename it to "openvr_api.dll", put it in the same location as the opencomposite dll and overwrite, this will remove opencomposite.  

### OpenXR Toolkit
OpenComposite also lets you use the OpenXR Toolkit which brings additional functionality and tweaks.  
The toolkit allows you to use things like Upscaling (NIS,FSR,CAS), Foveated rendering (Like VRS but adjustable in-game and has more settings) and more. The toolkit [can be downloaded here](https://mbucchia.github.io/OpenXR-Toolkit/#downloads)  
If you have OpenComposite set up correctly and the Toolkit installed, it should pop up by itself in game. I would recommend changing the default hotkeys from F keys to arrow keys for convenience in the OpenXR Toolkit Companion app in windows.   
<img src="https://github.com/Raptyyy/rapty_ac_vr_guide/blob/ad7065aa9a3be800edde90a72d2039db4e025605/resources/companion_5K7N6kLbKY.png" width="250">  

### Recommended settings for the Toolkit:
Set these settings in game through the toolkit menu (CTRL + F2 by default to open or whatever hotkey you change it to).  
- Upscaling set to `FSR` if you need more performance or set to `CAS` to improve image quality by sharpening the image, strength of `80% to 100%` should work best.
- Foveated rendering ([What is Foveated Rendering](#10-what-is-foveated-rendering)) set to `Preset - Quality - Balanced`, this will be a good starting point, adjust as needed. `Custom` will allow you to tweak things further if you understand how Foveated rendering works.
- System > FOV allows you to change the size of the FOV (Field of View). This has the benefit of increasing image quality at the expense of reduced FOV, I personally use `94%` on my Revern G2 V1. Might not work well with every headset.  
There is additional functionality in the toolkit which [you can see here](https://mbucchia.github.io/OpenXR-Toolkit/features.html)

## 10. VRPerfKit
VR Perf Kit is a utility that has some of the same feature as the OpenXR Toolkit (Upscaling and Foveated rendering) but does not require the use of OpenXR (OpenComposite).  
This is useful for people who use native SteamVR headsets (Vive,Index,Bigscreen) and want some of the same functionality.  
> [!NOTE]
> Since foveated rendering is built into CSP itself I don't recommend this utility as much nowadays. its only beneficial to users who want to tweak things further.

[Link to VRPerfkit](https://github.com/fholger/vrperfkit), The installation and usage are explained in the download link.  
There is another version of the VRPerfkit called VRPerfKit_RSF with more features which you can [find here](https://github.com/RavenSystem/VRPerfKit_RSF), However its also more complicated to use so would only recommend this to advanced users.  

## 11. Additional Notes

When it comes to VR performance, the most important thing is having a consistent framerate. You want to utilize your GPU as much as possible by increasing the headsets resolution or graphical settings, but also leaving enough headroom to avoid any fluctuation in performance. You can use things like SteamVR performance graph, OpenXR advanced overlay or programs like GPU-Z to monitor GPU and CPU usage and adjust settings as needed.  

If your framerate is stuck to a specific value like 30, 45 or 60 fps, its likely that you have reprojection enabled. Reprojection halves your framerate and inserts fake frames to reduce the load on your system. You can disable this behaviour if needed.  
On Oculus / Meta headsets it should be called ASW or Asynchronous Spacewarp, on SteamVR its motion smoothing, on WMR you should be able to adjust it in the OpenXR Toolkit, Pimax has it in the PiTool.  

> [!WARNING]
> On some systems using HAGS (Hardware accelerated GPU Scheduling) can cause performance issues, you can change it in Windows Settings > System > Display > Graphics settings or just search for "GPU" in the start search.  

> [!NOTE]
> Reshade is available for VR too but it can also significantly impact performance so generally would not recommend using it.  


