# VR guide for Assetto Corsa and CSP

The purpose of this guide is to help with basic VR setup and cover some of the main settings and features.  
It also covers usage of OpenComposite and the OpenXR Toolkit  
This guide is written with Content Manager and Custom Shaders Patch in mind, not guaranteed to work with vanilla Assetto Corsa.

## 0. Table of Contents
1. [Prerequisites](#1-prerequisites)  
2. [Basic VR Setup](#2-basic-vr-setup)  
3. [Setting up Custom Shaders Patch (CSP)](#3-setting-up-custom-shaders-patch-csp)  
4. [Setting up Pure](#4-setting-up-pure)  
5. [Video Settings](#5-video-settings)  
6. [Custom Shaders Patch settings](#6-custom-shaders-patch-settings)  
7. [OpenComposite and OpenXR Toolkit](#7-opencomposite-and-openxr-toolkit)
8. [VRPerfKit](#8-vrperfkit)
9. [What is Foveated Rendering](#9-what-is-foveated-rendering)
10. [Additional Notes](#10-additional-notes)

Quick links: 
- [Video presets](#51-video-presets-for-vr)  
- [CSP presets](#61-csp-setting-presets)  
- [OpenComposite and OpenXR Toolkit](#7-opencomposite-and-openxr-toolkit)  
- [What is Foveated Rendering](#9-what-is-foveated-rendering)  

## 1. Prerequisites
- Legit copy of Assetto Corsa (Pirated copies do not get any support or help in the CSP discord)
- Latest version of Content Manager  
- Latest version of Custom Shaders Patch unless said otherwise.  
- Latest version of Pure (Delivers the best image in VR)  

## 2. Basic VR setup
### Oculus / Meta
1. First make sure that you have successfully set up Quest link or Air link and that the headset is connected to your PC - [Tutorial how to do so](https://www.meta.com/help/quest/articles/headsets-and-accessories/oculus-link/connect-with-air-link/)  
2. In the Oculus App, Settings > General enable "Unknown sources" and next to the "OpenXR Runtime" press "Set Oculus as active" (If its greyed out then you don't need to press it)  
3. In content manager go to Settings > Assetto Corsa > Video and set "Rendering Mode" to "Oculus Rift", this does not require SteamVR.  
  3.1 If you do wish to use SteamVR then set "Rendering Mode" to "OpenVR" instead, this applies to Virtual Desktop too.
4. Try launching the game in singleplayer and see if everything works.
Important to note that Oculus / Meta headsets can also be used with SteamVR, OpenComposite and Virtual Desktop (Standalone headsets only), Oculus Rift should be easiest to set up.  

### SteamVR headsets (Vive, Index, Bigscreen beyond)
1. Make sure your headset is connected to your PC
2. Install SteamVR from Steam
3. In Content Manager go to Settings > Assetto Corsa > Video and change "Rendering Mode" to "OpenVR"
4. Try launching the game in singleplayer and see if everything works.

### Windows Mixed Reality headsets
1. Make sure your headset is connected to your PC
2. Install Windows Mixed Reality from the Microsoft Store
3. Install SteamVR from Steam
4. Install Windows Mixed Reality for SteamVR from Steam
5. In Content Manager go to Settings > Assetto Corsa > Video and change "Rendering Mode" to "OpenVR"
6. Try launching the game in singleplayer and see if everything works.

### Pimax headsets
1. Make sure your headset is connected to your PC
2. Install PiTool
3. Install SteamVR from Steam
4. In Content Manager go to Settings > Assetto Corsa > Video and change "Rendering Mode" to "OpenVR"
5. Try launching the game in singleplayer and see if everything works.

## 3. Setting up Custom Shaders Patch (CSP)
1. In Content Manager go to Settings > Custom Shader Patch
  1.1 If you are prompted to install Custom Shaders Patch, press install
2 Go to Settings > Custom Shader Patch > About & Updates and verify that you are on the latest version which should be at the top of the list on the right side.
  2.1 I don't recommend using the "recommended" version as it is quite old by now and wont work in some servers  
If you are using a preview version of CSP from Patreon then install it manually or through the quick install link in the Patreon post

## 4. Setting up Pure
Pure is recommended for VR as it delivers a more realistic and consistent image, also has a lot of adjustability.
1. Make sure you are on the latest version of CSP
2. Go to Peter Boese Patreon page and download Pure from there, it costs $1 - [Pure Patreon](https://www.patreon.com/c/peterboese/posts)
3. There is an installation guide in the Pure post, follow it thoroughly. [Link to the guide here too](https://youtu.be/456BO7vKui0?si=BQ0YIq6q3f7BuZyc)
  3.1 Incorrect installation of Pure can cause major performance issues !
4. Make sure that exposure is set to 100% in Settings > Assetto Corsa > Miscellaneous > Exposure

## 4.1 Pure pp filters 
Pure, PureVR - these come with Pure, PureVR would be my recommendation out of those two  
[Natural Mod PP Filter](https://www.overtake.gg/downloads/natural-mod-pp-filter.4551/) Natural looking filter with good performance  
[Improved Visuals PureCS Filter](https://www.overtake.gg/downloads/improved-visuals-pure-cs-filter-screen-and-vr-ppfilter.54256/) VR focused pp filter with great adjustability  
[C13 Aegis Filter](https://www.overtake.gg/downloads/c13-aegis-post-processing-filter.59979/) Probably one of the best looking filters, newer versions are available on patreon, might not be great performance wise

## 5. Video Settings
This covers all the settings in Content Manager > Settings > Video  
Note that in Content Manager most settings have a green "i" icon next to them that will show what each setting does and the performance impact  

## 5.1 Video Presets for VR
These are some video presets I made if you don't want to read through the settings below, try each one out and see what works best. Also adjust to your needs.  
Make sure to double check the Rendering Mode so that its set correctly for your headset !  
- High Performance: [Link here](https://acstuff.club/s/lW4B) (Disable post processing if you need even more performance)  
- Balanced: [Link here](https://acstuff.club/s/MvZ2)
- High Quality: [Link here](https://acstuff.club/s/GKoQ)

## 5.2 Video Settings Explained

### Resolution and FPS
"**Rendering Mode**" should already be set depending on your headset as shown above.  
"**Fullscreen**" will simply display the game in Fullscreen instead of a window, recommended to have it enabled as it slightly helps with performance but its not a must.  
"**Resolution**" doesnt really matter for VR use, it will only set the game window size, does not affect VR image quality.  
"**Virtual synchronization**" is not needed, keep it disabled  
"**Limit framerate**" is not needed in VR as the headset will limit fps as needed by itself, keep it disabled.  

### Quality
"**MSAA**" is an Anti-Aliasing technique which helps a lot with jaggies or shimmering especially into the distance. Highly recommended to keep it enabled in VR, either 2x or 4x. 8x will have a major impact on performance and is generally not worth using.  
"**Anisotropic Filtering**" helps with texture clarity into the distance, it has a very low performance impact so recommended to just keep it at 16x.  
"**World details**" will affect object amount on tracks (if they support it), set it as needed. Can also be adjust in-game using the "View & Video Settings" app.  
"**Shadows resolution**" affects how sharp the shadows will look. Higher resolution will make shadows look better but decrease performance. I would recommended using 1024x1024 and increase if performance isnt an issue.  
"**Smoke generation**" Simply controls the smoke quantity, adjust as needed, but I would recommend using CSP smoke instead (Custom Shaders Patch > Particles FX > New smoke and dust)  

### Reflections
"**Reflection Resolution**" simply adjusts how sharp / clear the reflections will look, 512x512 is a good base value to start with, can increase if needed.  
"**Rendering frequency**" adjusts how smoothly the reflections will reflect, Set it to either one or two faces per frame, any higher is not really needed as they get reprojected anyway. don't use Static either.  
"**Rendering distance**" Adjusts the reflection rendering distance, does not have a noticeable performance impact so you can set it to at least 1000m or higher if needed.  

### Post-Processsing
"**Enable post-processing effects**" this enables post processing in general, very useful to have to improve the graphics and look of the game, however has a big performance impact. Most PCs should be able to handle post processing but low-end PCs should probably disable it on more demanding servers.  
"**Overall Quality**" sets the post processing resolution, High is a good middle ground performance wise but can also just set it to Maximum.  
"**Glare Quality**" sets the quality of glare effects, High is a good middle ground performance wise but can also just set it to Maximum.  
"**Depth of field**" adjusts the depth of field quality, only works in replays so can keep it Off if you don't care about it.  
"**Motion blur**" not recommended to use with VR, set it to Off  
"**Saturation**" is basically the intensity of the colors, keep it at 100% and adjusts colors in Pure instead if needed.  
"**Heat shimmering**" adds a heat shimmering effect, set as needed  
"**Sunrays**" enables sun rays / god rays / sun shafts, set as needed  
"**FXAA**" is an anti aliasing technique, keep it enabled as it is required for some CSP functionality but will not affect image quality in VR.

### Mirrors
"**Mirror resolution**" how sharp / clear the mirrors will look, higher resolutions will reduce performance, 256x1024 is a good base value  
"**High quality**" enables additional effects in the mirrors and increases the rendering distance (from 400 to 800 meters), will reduce performance  

### Oculus (only affects Oculus / Meta headsets)
"**Pixels per display**" is same as resolution multiplier in the oculus app or oculus pixels per display pixel override in oculus debug app, set as needed  
"**Mirror texture**" enables the game window to show your VR view, recommended to enable it  

### System
I would recommend not messing with these settings as they don't really have any meaningful impact and can cause issues.

## 6. Custom Shaders Patch settings
I will not cover every setting in CSP (that would be a lot to cover), but only the ones that matter for VR performance.  

## 6.1 CSP Setting Presets
These presets are simply to be used as a base for your own preference. Test the presets out and adjust as needed.  
Note: Foveated rendering (VRS) is NOT enabled in any of these, set it yourself as needed.  
- High Performance - [Link here](https://acstuff.club/s/rFa) (This preset has a lot of modules disabled for a little extra performance)  
- Balanced - [Link here](https://acstuff.club/s/OG43)  
- High Quality - [Link here](https://acstuff.club/s/Lywh)  

### General Patch Settings
"**Audio > Decompress Samples**" recommended to enable it if you have more than 16GB of RAM, helps with CPU load.  
"**New KN5 loader**" recommended to have it enabled, helps with memory usage  
CPU optimizations:
- "**Flatten nodes**" keep it enabled  
- "**Chunks optimization**" helps with CPU load. Set it to Advanced unless you have issues, then keep it at Basic.  
- "**Limit audio for other cars**" set it to Always if you have a slower PC.  
GPU optimizations: 
- "**Optimize meshes some more**" helps with GPU load
- "**Deduplicate meshes**" helps with VRAM
- "**Upgrade AC textures**" will make certain textures more efficient VRAM wise, don't enable this if you have a low amount of free disk space.

### Extra FX
Extra FX doesnt work in VR so this will have no effect, keep it disabled if you don't ever use Extra FX.

### Graphics Adjustments
"**AMD FidelityFX SuperResolution"** also known as "FSR" is an upscaler that can help with performance by rendering the game at a lower resolution and then upscaling the image. Should only be needed for lower end PCs.  
LOD settings:
- "**Force low-res drivers for other cars in first person view"** enable for performance
- "**Multiplier for car LODs**" this sets how far away the car LOD (level of detail) will change, lower multiplier will help with performance but can make cars look worse up close, for performance set it to 75%.
- "**Multiplier for track LODs**" same thing as car LODs but for the track, I would recommend not going below 80% as it can cause issues.
- "**Multiplier for trees LODs**" same thing as car LODs but for 3D trees, you can set it to 0% for best performance if you don't care about 3D trees.
- "**Add extra collider-based LODs for distant cars**" will make low quality LODs for cars that don't have them, can help a lot in dense lobbies like VDC. Set the "Limit LODless cars" to a low value between 5 to 10 for best performance.
"**Post processing antialiasing**" set to Disabled as post process AA doesnt work in VR (Will update this if it changes)
"**Accessible color buffer > Full resolution for better quality"** you can disable this for a tiny boost in performance
"**Draw grooves over track, but before dynamic entities**" Can help with performance but can also cause issues on some track (Like mirror / see through roads), use with caution.

### lighting FX
"**Cars casting lights**" set this to a lower amount for better performance in dense lobbies, lights are expensive performance wise.
"**Disable mirroring in first person view**" helps with performance a bit
"**Enable lighting in reflections**" disable for a performance boost

### Neck FX
Not related to performance but there are good NeckFX scripts for VR to enhance immersion or comfort, here are two most popular ones: 
- [AC Head Physics](https://www.overtake.gg/downloads/ac-head-physics.68266) fancier script, has more movement  
- [NeckFX LUA script](https://www.overtake.gg/downloads/neckfx-lua-script-vr-stabilize.65087) more basic, static script.

### Smart Mirror
"**Custom render distance"** enable it and set the distance to 400 meters if you use High Quality mirrors in video settings, helps with performance.
"**Real mirrors**" highly recommended in VR, makes the mirrors change perspective based on your head movement also lets you adjust mirror positioning through the "Mirrors" app in-game
- "**Active**" enabled of course
- "**Alter FOV**" set based on your preference, I have it off
- "**Refresh rate per frame**" set to Update single reflection per frame for best performance, can look a little laggy on lower refresh rate headsets, try higher if needed.

### Weather FX
"**Weather style**" this should be set to either Pure Gamma or Pure LCS, Gamma is better performance wise as of now but LCS will produce a more natural image.  
"**Replace YEBIS with lightweight alternative**" helps a lot to reduce the performance impact of post-processing, does not work with some pp filters like C13.  
"**Automatically guess white reference point**" This can make the UI very bright when using Pure, disable it.  

### Mode Tweaks VR:
Make sure the extension is enabled (Active)  
"**Single Pass Stereo**" Highly recommend to enable this, helps a lot with CPU load, can cause certain Pure effects to not work. Might work for AMD GPUs too.  
"**Single YEBIS pass"** makes post processing slightly less demanding to run, enable for performance if needed, can cause certain Pure effects to not work.  
"**Nvidia VRS**" also known as Foveated rendering ([What is Foveated Rendering?](#8-what-is-foveated-rendering)) is probably the most important performance tweak for VR, however only works for Nvidia GPUs.  
If you want to use Nvidia VRS:  
- "**Nvidia VRS**" enabled
- "**VRS preset**" Custom
- "**VRS rate"** High performance, can set to Highest performance if you need every bit of performance but it will be more visible.
- "**VRS detailed area**" Balanced, set it to wide if you use a Quest 3 or Pico 4 as they will show foveated rendering more clearly.  
You can also test using the "VRS preset" presets but they seem to be made for Pimax headsets.

"**Corners masking optimization**" Recommended to keep this one enabled, helps with performance but will create a black area around the VR image in the game window  
"**Custom VR HUD rendering**" recommended to keep this enabled as it makes the HUD work better in VR  

## 7. OpenComposite and OpenXR Toolkit
OpenComposite allows you to play SteamVR games without actually needing SteamVR, it is highly recommended for users wanting more performance.  
On non native SteamVR headsets(Quest,Pico,Pimax,WMR) SteamVR simply acts as a middle layer which increases resource usage while bringing no real benefit to your VR experience.  
OpenComposite can also be used with Virtual Desktop when using it with VDXR, [more info here](https://github.com/mbucchia/VirtualDesktop-OpenXR/wiki)  
To install OpenComposite:
1. Download the opencomposite dll file either from [this repository](https://github.com/Raptyyy/rapty_ac_vr_guide/raw/refs/heads/main/openvr_api.dll) or from the [OpenComposite mirror](https://opencomposite.znix.xyz/builds/) (Select the first result and download the Platform: x64	x64/openvr_api.dll file)
2. Make sure the file is called "openvr_api.dll" and place it in to "steamapps\common\assettocorsa\system\x64", if prompted to overwrite files, press yes.
3. In Content Manager > Settings > Video set "Rendering Mode" to "OpenVR"
4. You also need to make sure your headset is using its native OpenXR Runtime and not the SteamVR one
  
If you encounter any issues using OpenComposite, I have the [original dll file uploaded here](https://github.com/Raptyyy/rapty_ac_vr_guide/raw/refs/heads/main/openvr_api.dll.og), rename it to "openvr_api.dll", put it in the same location as the opencomposite dll and overwrite, this will remove opencomposite.  

OpenXR Toolkit (OpenXR only)
On top of OpenComposite allowing you to not need SteamVR to use SteamVR games, it is also compatible with the OpenXR Toolkit which brings additional functionality and tweaks.
The toolkit allows you to use things like Upscaling (NIS,FSR,CAS), Foveated rendering (Like VRS but adjustable in-game and has more settings) and more.
The toolkit [can be downloaded here](https://mbucchia.github.io/OpenXR-Toolkit/)  
If you have OpenComposite set up correctly and the Toolkit installed, it should pop up by itself in game. I would recommend changing the default hotkeys from F keys to arrow keys for convenience in the OpenXR Toolkit Companion app in windows.  
Recommended settings for the Toolkit:
- Upscaling set to FSR if you need more performance or set to CAS to improve image quality by sharpening the image, strength of 80% to 100% should work best.
- Foveated rendering ([What is Foveated Rendering?](#8-what-is-foveated-rendering)) set to Preset - Quality - Balanced, this will be a good starting point, adjust as needed. Custom will allow you to tweak things further if you understand how Foveated rendering works.
- System > FOV allows you to change the size of the FOV (Field of View). This has the benefit of increasing image quality at the expense of reduced FOV, I personally use 94% on my Revern G2 V1. Might not work well with every headset.  
There is additional functionality in the toolkit which [you can see here](https://mbucchia.github.io/OpenXR-Toolkit/features.html)

## 8. VRPerfKit
VR Perf Kit is a utility that has some of the same feature as the OpenXR Toolkit (Upscaling and Foveated rendering) but does not require the use of OpenXR.  
This is useful for people who use native SteamVR headsets (Vive,Index,Bigscreen) and want some of the same functionality.  
Since foveatred rendering is built into CSP itself I don't recommend this utility as much nowadays but it is somewhat more adjustable so feel free to try it.  
[Link to VRPerfkit](https://github.com/fholger/vrperfkit)  
The installation and usage are explain in the download link.  
There is a more advanced version of the VRPerfkit with more feature which you can [find here](https://github.com/RavenSystem/VRPerfKit_RSF), However its also more complicated to use so would only recommend this to advanced users.  

## 9. What is Foveated Rendering
Foveated rendering is a method in VR to achieve greater performance by rendering the outer parts of the image at lower resolution.  
As shown in the example below, the center part of the image stays at full resolution while the outer edges become less defined. This is a good thing on most headsets as the lenses have a "sweetspot" which means only the center portion of the lense will display a clear, sharp image anyway. Rendering the whole image at full resolution is wasteful for performance.  
Foveated rendering might be obvious and undesirable on headsets that use pancake lenses with large sweetspots such as Quest 3 or Pico 4, on such headsets it is recommended to use a very large center part of the Foveated image or to just not use Foveated rendering at all.   
<img src="https://i.redd.it/za7loskn6jy21.jpg" width="500">   

Note that since Assetto Corsa is a DirectX 11 game, Foveated Rendering works ONLY on Nvidia GPUs that are 20 series or newer. 


## 10. Additional Notes
As explained earlier, installing Pure correctly is crucial for good performance as a bad Pure installation can cause issues.  
On some systems using HAGS (Hardware accelerated GPU Scheduling) can cause performance issues, you can change it in Windows Settings > System > Display > Graphics settings or just search for "GPU" in the start search.  
Reshade is available for VR too but it can also significantly impact performance so generally would not recommend using it.  

