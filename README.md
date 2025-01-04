# VR guide for Assetto Corsa and CSP

The purpose of this guide is to help with basic VR setup, installing Custom Shaders Patch, Pure and adjusting your settings for the best experience.  
It also covers usage of OpenComposite and the OpenXR Toolkit.  
This guide is written with Content Manager and Custom Shaders Patch in mind, not intended to work with vanilla Assetto Corsa.  
If you have anything useful to add to the guide or see a mistake, feel free to make an issue and I will correct it.  

> [!TIP]
> Most people should only have to read the first 6 chapters (Up to video settings), beyond that is more in depth coverage of various settings.

> [!NOTE]
> For further help or if you want to report a game issue, join the Custom Shaders Patch discord and use the `virtual-reality-talk` channel  
> [![](https://dcbadge.limes.pink/api/server/zN4XtmZ4Jf)](https://discord.gg/zN4XtmZ4Jf)



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
10. [Additional Notes](#10-additional-notes)  

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
3. In Content Manager go to <ins>Settings > Assetto Corsa > Video</ins> and set "Rendering Mode" to "Oculus Rift", this does not require SteamVR.  

**Using Virtual Desktop and OpenComposite (Can give better results however costs money):**  
1. Purchase Virtual Desktop on the Oculus / Meta store (do not buy it on steam itself)
2. Follow the instructions provided in Virtual Desktop to connect your headset to your PC (Quest / Air Link is not required).   
3. Open the Virtual Desktop Streamer application, and under settings, select VirtualDesktopXR (VDXR) as the OpenXR runtime.
4. Set up OpenComposite, [instructions here](#to-install-opencomposite)
5. In Content Manager go to <ins>Settings > Assetto Corsa > Video</ins> and set "Rendering Mode" to "OpenVR"  

Using this method you can also look into the [OpenXR Toolkit](#openxr-toolkit)

**Using SteamVR (Generally not recommended):**  
1. First make sure that you have successfully set up Quest link or Air link and that the headset is connected to your PC - [Tutorial how to do so](https://www.meta.com/help/quest/articles/headsets-and-accessories/oculus-link/connect-with-air-link/)
  1.1. If youre using an Oculus Rift (S) then you simply need to have the headset connected and showing in the oculus app.  
3. Install and set up SteamVR from Steam  
4. In Content Manager go to <ins>Settings > Assetto Corsa > Video</ins> and set "Rendering Mode" to "OpenVR"

### Oculus / Meta additional notes and troubleshooting  

- Game lagging when using the headset wirelessly: Your router might not be able to handle the high amount of bandwidth required for a smooth experience, this will generally show as high network latency. Try to lower the bitrate in the [Oculus Debug Tool](https://smartglasseshub.com/oculus-debug-tool/) or set it to 0 for auto bitrate.  
- USB-C, Make sure your headset runs USB 3 and not USB 2, if it keeps connecting via USB 2 even with a new cable and using a USB 3 port, reset your headset to factory defaults which will fix the issue.
- using USB-C set the bitrate to 500mbps or higher in the Oculus Debug Tool. More info about the [Oculus Debug Tool here](https://smartglasseshub.com/oculus-debug-tool/).  

</details>

<details>
  <summary>SteamVR headsets (Vive, Index, Bigscreen beyond)</summary>
  
1. Make sure your headset is connected to your PC
2. Install and set up SteamVR from Steam  
3. In Content Manager go to <ins>Settings > Assetto Corsa > Video</ins> and change "Rendering Mode" to "OpenVR"
</details>

<details>
  <summary>Windows Mixed Reality headsets</summary>


**Using OpenComposite (Highly recommended):**  
1. Make sure your headset is connected to your PC  
2. Install and set up Windows Mixed Reality from the Microsoft Store
3. Install and set up OpenXR Tools for Windows Mixed Reality from the Microsoft Store  
  3.1. If you see a button that says "Set as active runtime" - press it.  
5. Set up OpenComposite, [instructions here](#to-install-opencomposite)  
6. In Content Manager go to <ins>Settings > Assetto Corsa > Video</ins> and change "Rendering Mode" to "OpenVR"  

Using this method you can also look into the [OpenXR Toolkit](#openxr-toolkit)

**Using SteamVR:**  
1. Make sure your headset is connected to your PC  
2. Install and set up Windows Mixed Reality from the Microsoft Store  
3. Install and set up SteamVR from Steam  
4. Install Windows Mixed Reality for SteamVR from Steam  
5. In Content Manager go to <ins>Settings > Assetto Corsa > Video</ins> and change "Rendering Mode" to "OpenVR"  
</details>

<details>
  <summary>Pimax headsets</summary>

**Using OpenComposite (Highly recommended):**  
1. Make sure your headset is connected to your PC  
2. Install and set up Pimax Play, [link here](https://pimax.com/pages/downloads-manuals)  
3. Set the OpenXR Runtime to Pimax OpenXR in Pimax Play, [instructions here](https://pimax.com/blogs/blogs/how-to-use-pimax-openxr)  
5. Set up OpenComposite, [instructions here](#to-install-opencomposite)  
6. In Content Manager go to <ins>Settings > Assetto Corsa > Video</ins> and change "Rendering Mode" to "OpenVR"  

Using this method you can also look into the [OpenXR Toolkit](#openxr-toolkit)

**Using SteamVR:**  
1. Make sure your headset is connected to your PC
2. Install and set up Pimax Play, [Link here](https://pimax.com/pages/downloads-manuals)
3. Install and set up SteamVR from Steam  
4. In Content Manager go to <ins>Settings > Assetto Corsa > Video</ins> and change "Rendering Mode" to "OpenVR"
</details>

> [!TIP]
> Once you have the correct settings applied for your headset, test it out in singleplayer first before joining a server !

## 2.1. VR Resolution
Unlike monitors, VR headsets dont have a "native" resolution because of [barrel distortion](https://images.anandtech.com/doci/9305/MRSOptics.jpg) which reduces detail in the image.  
It is important to set the resolution high enough to have a clear image, but also not too high to not cause performance issues.  

- **Oculus / Meta** headsets you can adjust it in the Oculus app (Settings > Graphics Preference > Render Resolution) Or in the [Oculus Debug Tool](https://smartglasseshub.com/oculus-debug-tool/) with the Pixels Per Display Pixel Override setting.  
- **Steam VR** headsets you can adjust it in SteamVR settings (Video > Resolution Per Eye).  
- **Windows Mixed Reality** headsets you can adjust it in OpenXR Tools for Windows Mixed Reality (Custom Render Scale).  
- **Pimax** headsets you can adjust it in the Pimax Play software (Render Quality).  

Any headset using OpenComposite and the OpenXR Toolkit can also adjust resolution through the OpenXR Toolkit.  

> [!NOTE]
> The Resolution in Content Manager > Settings > Video does NOT affect VR image quality.  

## 2.2. VR Reprojection
Reprojection reduces system load by halving the needed amount of rendered frames and extrapolating the rest to maintain a smooth experience.  
For example - a 90Hz headset would need only 45fps with reprojection instead of 90fps.  
However, it may cause artifacts, input delay, or stuttering. 

- **Oculus / Meta** headsets you can disable it in the [Oculus Debug Tool](https://smartglasseshub.com/oculus-debug-tool/) with the PC Asynchronous Spacewarp setting.  
- **Steam VR** headsets you can disable it in SteamVR settings (Video > Motion Smoothing).  
- **Windows Mixed Reality** headsets you can disable it in OpenXR Tools for Windows Mixed Reality (Motion Reprojection Rate).  
- **Pimax** headsets you can disable it in the Pimax Play software (Smart Smoothing).  

Any headset using OpenComposite and the OpenXR Toolkit can also adjust Reprojection through the OpenXR Toolkit.  

## 3. Setting up Custom Shaders Patch (CSP)
1. In Content Manager go to Settings > Custom Shader Patch  
  1.1 If you are prompted to install Custom Shaders Patch, press install  
2. Go to Settings > Custom Shader Patch > About & Updates and verify that you are on the latest version which should be at the top of the list on the right side.  
  2.1. I don't recommend using the "recommended" version as it is quite old by now and wont work in some servers

> [!NOTE]
> If you are using a preview version of CSP from Patreon then install it manually or through the quick install link in the Patreon post  

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
> Save your current settings as presets in Content Manager for Video and Custom Shaders Patch !

## 5.1 Video Presets for VR
These are some video presets I made if you don't want to read through the settings below, try each one out and see what works best. Also adjust to your needs.  
Make sure to double check the Rendering Mode so that its set correctly for your headset !  

- High Performance: [Link here](https://acstuff.club/s/lW4B) (Disable post processing if you need even more performance)  
- Balanced: [Link here](https://acstuff.club/s/oFw)
- High Quality: [Link here](https://acstuff.club/s/hPvJ) (For best graphics find a good pp filter)

## 5.2 CSP Setting Presets
These presets are simply to be used as a base for your own preference. Test the presets out and adjust as needed.  
> [!NOTE]
> Foveated rendering / Nvidia VRS is NOT enabled in any of these, read the 6th chapter below.  

- High Performance - [Link here](https://acstuff.club/s/MbOb) (This preset has a lot of modules disabled for a little extra performance)  
- Balanced - [Link here](https://acstuff.club/s/l1xe)  
- High Quality - [Link here](https://acstuff.club/s/fi4I)  

## 6. What is Foveated Rendering
Foveated rendering is a method in VR to achieve greater performance by rendering the outer parts of the image at lower resolution as shown in the example below. This makes sense on most headsets as only the center part of the lense is in focus and can display the image clearly.  
Foveated rendering is the biggest performance increase (GPU load wise) that you can get in VR so it is highly recommended to take advantage of it.  

<img src="https://github.com/Raptyyy/rapty_ac_vr_guide/blob/980c83fc6ec2016ade1d3e7c172c3838679fc5f9/resources/fov_rend_example.jpg" width="1280">   

Ways to enable / use Foveated rendering (Use only one of these methods):  
- Enable "Nvidia VRS" in Custom Shaders Patch, [explained further here](#nvidia-vrs) (Easiest way to enable it)  
- Enable Foveated Rendering in the OpenXR Toolkit if you're using OpenComposite, [explained further here](#recommended-settings-for-the-toolkit) (Gives more adjustability compares to Nvidia VRS)  
- For Pimax users you can enable Foveated Rendering in Pimax Play (More convenient but less options compared to the OpenXR Toolkit)  
- VRPerfKit also has Foveated Rendering, [explained further here](#10-vrperfkit) (Only recommended for SteamVR users who want more adjustability compared to Nvidia VRS)  

> [!NOTE]
> Foveated rendering might be undesirable on headsets that use pancake lenses with large sweetspots such as Quest 3 or Pico 4, on such headsets it is recommended to use a very large center ring or just not use Foveated rendering at all.

> [!WARNING]
> Note that since Assetto Corsa is a DirectX 11 game, Foveated Rendering works ONLY on Nvidia 16xx, 20xx, 30xx and 40xx series GPUs or newer. 

## 7. Video Settings
This covers all the settings in Content Manager > Settings > Video  
> [!TIP]
> Note that in Content Manager > Video most settings have an ![image](https://github.com/user-attachments/assets/9f386396-4427-4b7a-b75b-127258967f94) icon next to them that will show what each setting does and the performance impact.  

### Resolution and FPS
**Rendering Mode** should already be set depending on your headset as shown above.  

**Fullscreen** will simply display the game in Fullscreen instead of a window, recommended to have it `enabled` as it slightly helps with performance but its not a must.  

**Resolution** doesnt really matter for VR use, it will only set the game window size, does not affect VR image quality.  

**Virtual synchronization** is not needed, keep it `disabled`  

**Limit framerate** is not needed in VR as the headset will limit fps as needed by itself, keep it `disabled`.  

### Quality
**MSAA** (Multisample anti-aliasing) is an Anti-Aliasing technique which helps with jagged edges, pixelation or shimmering especially into the distance. Highly recommended to keep it enabled in VR, either `2x` or `4x`. `8x` will have a major impact on performance and is generally not worth using.  

**Anisotropic Filtering** helps with texture clarity into the distance, it has a very low performance impact so it's recommended to just keep it at `16x`.  

**World details** will affect object count on tracks (if they support it), set it as needed. Can also be adjust in-game using the "View & Video Settings" app.  

**Shadows resolution** affects how sharp the shadows will look. Higher resolution will make shadows look better but decrease performance. I would recommended using `1024x1024` and increase if performance isnt an issue.  

**Smoke generation** simply controls the smoke quantity, adjust as needed, but I would recommend using CSP smoke instead (Custom Shaders Patch > Particles FX > New smoke and dust)  

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

**Mirror texture** enables the game window to show your VR view, recommended to have it `enabled`  

### System
I would recommend not messing with these settings as they don't really have any meaningful impact and can cause issues.

## 8. Custom Shaders Patch settings
I will not cover every setting in CSP (that would be a lot to cover), but only the ones that matter for VR performance.  

### General Patch Settings
**Audio > Decompress Samples** recommended to have it `enabled`. Reduces CPU overhead for higher memory (RAM) usage.  

**New KN5 loader** recommended to have it `enabled`, reduces RAM and VRAM usage.  

CPU optimizations:
- **Flatten nodes** keep it `enabled`  
- **Chunks optimization** helps with CPU load. Set it to `Advanced` unless you have issues (like the screen going black), then keep it at `Basic`.  
- **Limit audio for other cars** set it to `Always` if you have a slower PC.

GPU optimizations: 
- **Optimize meshes some more** helps with GPU load, have it `enabled`  
- "**Deduplicate meshes**" helps with VRAM, have it `enabled`  
- "**Upgrade AC textures**" can improve loading times and reduce VRAM usage, recommended to have it `enabled`. Can make the game folder size bigger.  

### Extra FX
Extra FX doesnt work in VR so this will have no effect, keep it `disabled` if you don't ever use Extra FX.  

### GUI
**New driver tags** recommended to have it `enabled` so you can see driver names in VR. Its not a performance tweak but a very useful thing to have.  
**Font Scale** Set this to `125%` or higher if you struggle reading the names.  

### Graphics Adjustments
**AMD FidelityFX SuperResolution** also known as "FSR" is an upscaler that can help with performance by rendering the game at a lower resolution and then upscaling the image. Should only be needed for lower end PCs. Can also be used through the OpenXR Toolkit or VRPerfkit instead.    

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

**Disable mirroring in first person view** helps with performance a bit, have it `enabled`  

**Enable lighting in reflections** `disabled` for a performance boost  

### Neck FX
Not related to performance but there are good NeckFX scripts for VR to enhance immersion or comfort, here are two most popular ones: 
- [AC Head Physics](https://www.overtake.gg/downloads/ac-head-physics.68266) fancier script, has more movement  
- [NeckFX LUA script](https://www.overtake.gg/downloads/neckfx-lua-script-vr-stabilize.65087) more basic, static script.

### Smart Mirror
**Custom render distance** `enabled` and set the distance to 400 meters if you use High Quality mirrors in video settings, helps with performance.

**Real mirrors** highly recommended in VR, makes the mirrors change perspective based on your head movement also lets you adjust mirror positioning through the "Car Mirrors" app in-game (Install it from the "App Shelf" app in-game first)  
- **Active** `enabled`
- **Alter FOV** This will change the Field of View of the mirror depending how close you are to it. Set based on your preference, I have it `disabled`
- **Refresh rate per frame** set to `Update single reflection per frame` for best performance, can look a little laggy on lower refresh rate headsets, use higher if needed.

### Weather FX
**Weather style** this should be set to either `Pure Gamma` or `Pure LCS`. `Pure Gamma` is the recommended option as of now and has better performance, `Pure LCS` is able to produce a better looking image but could cause some issues too.  

**Replace YEBIS with lightweight alternative** is a more basic post-processing implementation which uses less CPU and GPU resources, for performance I would recommend to `enable` it. Does not work with some pp filters like C13.  

**Automatically guess white reference point** This can make the UI very bright when using Pure, `disable` it.  

### Mode Tweaks VR:
Make sure the extension is enabled (Active)  

**Single Pass Stereo** Highly recommended to `enable`, especially on slower CPUs. It renders both eye images at the same time into one packed Render Texture, meaning that the whole Scene is only rendered once, and CPU processing time is significantly reduced. Can make some Pure shaders not work.  

**Single YEBIS pass** Recommended to `enable` for best performance if needed. Instead of running post-processing individually for each eye, runs it once for both eyes. Can potentially affect glare effects in an undesirable way.  

### Nvidia VRS
also known as Foveated rendering ([What is Foveated Rendering](#6-what-is-foveated-rendering)), only works for Nvidia GPUs.  
If you want to use Nvidia VRS:  
- **Nvidia VRS** `enabled`
- **VRS preset** `Custom`
- **VRS rate** `High performance`, can set to Highest performance if you need every bit of performance but it will be more visible.
- **VRS detailed area** `Balanced`, set it to `Wide` if you use a Quest 3 or Pico 4 as they will show foveated rendering more clearly.

You can also test using the VRS presets if those work better for you.  

**Corners masking optimization** Recommended to keep this one `enabled`. Also known as [Hidden Area Mesh](https://forum.il2sturmovik.com/topic/81723-enable-the-use-of-ham-hidden-area-mesh-in-openvr/), it allows your GPU to not waste time rendering parts of the image that you wouldnt be able to see because of how the lenses work. Disable this if the black shape in the VR mirror (game window) is not wanted.    

**Custom VR HUD rendering** Recommended to keep this `enabled` as it makes the HUD work better in VR  

## 9. OpenComposite and OpenXR Toolkit
### OpenComposite
Allows you to play SteamVR games without actually needing SteamVR, it is highly recommended for users wanting more performance.  
On non native SteamVR headsets (Quest, Pimax, WMR) SteamVR simply acts as a middle layer which increases resource usage while bringing no real benefit to your VR experience.  
OpenComposite can also be used with Virtual Desktop when using it with VDXR, [more info here](https://github.com/mbucchia/VirtualDesktop-OpenXR/wiki)  
> [!IMPORTANT]
> Using OpenComposite with native SteamVR headsets (Vide, Index, Beyond) wont allow you to bypass SteamVR as it is required no matter what. However it would give you access to the OpenXR Toolkit if needed.  

> [!WARNING]
> Pico standalone headsets dont have their own OpenXR runtime, so to bypass SteamVR you would need to use Virtual Desktop with VDXR and OpenComposite.

### To install OpenComposite:
1. Download the OpenComposite dll file either from [this repository](https://github.com/Raptyyy/rapty_ac_vr_guide/raw/refs/heads/main/resources/openvr_api.dll) or from the [OpenComposite mirror](https://opencomposite.znix.xyz/builds/) (Select the first result and download the Platform: x64	x64/openvr_api.dll file)
2. Make sure the file is called "openvr_api.dll" (rename it if needed) and place it in to "steamapps\common\assettocorsa\system\x64", overwrite files if prompted to.
3. In Content Manager > Settings > Video set "Rendering Mode" to "OpenVR"
4. You also need to make sure your headset is using its native OpenXR Runtime (or VDXR for Virtual Desktop) and not the SteamVR one  

> [!IMPORTANT]
> If you encounter any issues using OpenComposite, I have the [original dll file uploaded here](https://github.com/Raptyyy/rapty_ac_vr_guide/raw/refs/heads/main/resources/openvr_api.dll.og), rename it to "openvr_api.dll", put it in the same location as the opencomposite dll and overwrite, this will remove opencomposite.  

### OpenXR Toolkit
OpenComposite also lets you use the OpenXR Toolkit which brings additional functionality and tweaks.  
The toolkit allows you to use things like Upscaling (NIS,FSR,CAS), Foveated rendering (Like VRS but adjustable in-game and has more settings) and more. The toolkit [can be downloaded here](https://mbucchia.github.io/OpenXR-Toolkit/#downloads)  
If you have OpenComposite set up correctly and the Toolkit installed, it should pop up by itself in game. I would recommend changing the default hotkeys from F keys to arrow keys for convenience in the OpenXR Toolkit Companion app in windows.   
<img src="https://github.com/user-attachments/assets/6b1f4817-cae9-4907-a9fa-5c9aff2a0b05" width="300">  


### Recommended settings for the Toolkit:
Set these settings in game through the toolkit menu (CTRL + F2 by default to open or whatever hotkey you change it to).  
- Upscaling set to `FSR` if you need more performance or set to `CAS` to improve image quality by sharpening the image, strength of `80% to 100%` should work best.
- Foveated rendering set to `Preset - Quality - Balanced`, this will be a good starting point, adjust as needed. `Custom` will allow you to tweak things further.  
- System > FOV allows you to change the size of the FOV (Field of View). This has the benefit of increasing image quality at the expense of reduced FOV, I personally use `94%` on my Revern G2 V1. Might not work well with every headset.  
There is additional functionality in the toolkit which [you can see here](https://mbucchia.github.io/OpenXR-Toolkit/features.html)

## 10. Additional Notes

When it comes to VR performance, the most important thing is having a consistent framerate. You want to utilize your GPU as much as possible by increasing the headsets resolution or graphical settings, but also leaving enough headroom to avoid any fluctuation in framerate. You can use things like Render Stats app in-game, SteamVR performance graph, OpenXR advanced overlay or programs like GPU-Z to monitor GPU and CPU usage and adjust settings as needed.  

### Nvidia Control Panel tweaks
<details>
  <summary>Anisotropic Filtering</summary>
  
Setting Anisotropic Filtering in the Nvidia Control Panel can potentially improve texture quality. Set it as shown in the image below.    
<img src="https://github.com/user-attachments/assets/58802765-659f-497d-81f7-e9fd0489795f" width="600">  
</details>

<details>
  <summary>MFAA (Multi-Frame Anti-Aliasing)</summary>
  
[MFAA](https://www.nvidia.com/en-us/geforce/news/multi-frame-sampled-anti-aliasing-delivers-better-performance-and-superior-image-quality/) is an anti-aliasing technique which by alternating AA sample patterns both temporally and spatially can improve the quality of MSAA.  
4xMFAA has the performance cost of 2xMSAA, with anti-aliasing properties equivalent to 4xMSAA.  
Requires MSAA to bet set to atleast 2x in Content Manager > Settings > MSAA  
<img src="https://github.com/user-attachments/assets/ea28aeec-ca77-4f4c-b614-32174566e79c" width="600"> 
</details>


> [!WARNING]
> On some systems using HAGS (Hardware accelerated GPU Scheduling) can cause performance issues, you can change it in Windows Settings > System > Display > Graphics settings or just search for "GPU" in the start search.  

> [!NOTE]
> Reshade is available for VR too but it can also significantly impact performance so generally would not recommend using it.  


