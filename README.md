**This repo has moved to https://github.com/Tuirsevoll/OpenHueyVR**

# Haunting Ground VR

A PC VR mod of **Haunting Ground**, built on top of [OpenHuey](https://github.com/ArnautDaniel/OpenHuey). HUGE thanks and admiration for the original project, without which this mod would not exist. Show your support!

**[Download the latest release](../../releases)** · You need your own copy of the game. This was built on a USA ISO and I cannot vouch for full operation of any other region.

> ⚠️ Early release by somebody who has never modded before. Expect lots of bugs, jank, and possible softlocks. Save Often. As of release date I have progressed very little in the game and can't confirm yet it is playable all the way to the end.  Please feel free to report issues in [Issues](../../issues) with as much detail as you can. If at all possible, try to keep to VR-specific issues.

This mod was built using 100% code from various AI, with some manual Blender work and fine-tuning. A lot of inspiration was taken from other VR titles and mods. While I have added everything I can think of to reach a (somewhat) happy starting release point, there will be much to fix, iron out and add. At its core this is a fixed camera angle PS2 game and some things are much harder to bring to VR than others.

This was built and tested only on a Quest 3 via Virtual Desktop streaming. Unfortunately I cannot confirm how well it works on other headsets, but don't have a particular reason to believe it shouldn't. Let me know.

---

## 🎮 Controls (Meta Quest 3)

### Left controller
| Input | Action |
|---|---|
| Thumbstick | Movement |
| Thumbstick (click) | Toggle run |
| X | Backstep |
| Y | Status screen (open/close)<br>In a cutscene: opens the movie pause with Skip |
| Menu (☰) | Pause game |
| Trigger | Hold to crouch (slow sneak walk)<br>Menu: page left |
| Grip | Grab<br>Back out / close dialogue or menu |

### Right controller
| Input | Action |
|---|---|
| Thumbstick | Turn |
| Thumbstick (flick up) | Hewie: "Go" / "Attack" |
| Thumbstick (flick down) | Hewie: "Come" |
| Thumbstick (click) | Hewie: "Stay" / "Stop" |
| A | Interact / menu select |
| B | Hold to talk (voice commands) |
| Trigger | Kick / tackle |
| Grip | Grab |

> To access the VR menu while in game, open your status screen where you access your inventory. To the "right" of the options tab, the VR menu is available. It does not show until you access it,  and its tab replaces the options tab once you are in it. You can still get back to the normal options tab by moving tabs left or right. No features in the status screen are lost.

## Current Features - More detail below

- 6DOF Tracking.
- Hand collision with walls and surfaces.
- 3D models for most items in the game, with manually created hand-grab poses for each.
- Physical pick-up and use of defense and recovery items.
- Physical pick-up and use of key story items.
- Physical crouching to hide.
- Physics doors. Grab the doorknob, push or pull, and swing them in either direction. If you're in a rush, just swiping at the door without grabbing will slam it closed.
- Physical Hiding Spot usage.
- Physical Ladder Climbing
- Physical Lever Usage
- Attack using your hands
- Command Hewie with your voice via a tiny local Whisper model
- 3D positional audio with Steam Audio.
- Customizable panic settings.
- VR Comfort Options

## 6DOF Tracking and IK 

Fiona's hands track your controllers. If they seem off, enter the VR menu and hit the Calibrate button.
You are going to see weird IK jank with wrists bending into dust and elbows turning the wrong way occasionally. Hopefully can improve this over time.
Swing your hands to attack. A one hand swing should break vases. Stalkers and doors are only affected by a two hand shove. You will hear Fiona make her base-game kick sound if it triggered. Alternatively, use the right trigger to use the standard kick animation.

## Hand collision

Inspired by HIGGS for SkyrimVR, and very barebones. Your hands will stop when they meet most solid surfaces, and slide along.

## 3D Models

3D Models have been created and added for every item except for documents, and wearables (boots, earrings etc.) . Rather than the sparkle sprite from the base game, for consumables you will see a rotating, small model of the item just above it. Pick it up and you will grip it, let go and it gets added to your inventory. 

## Physical Recovery & Attack Item Usage

Go in to your inventory and select Equip to place the recovery item in your hand. If it is for Fiona, hold it to your lower face and let go. You will feel a buzz in the controller and the item is consumed and used. If it is for Hewie, grip and let go to drop it to the floor. Currently, this works best if you drop it close to him. If you do not want to use these features, the 'Use' option in the menu works as the base game.

Equip a defense item the same way. Drop magnesia on the ground, or throw your antimony at a stalker.

## Physical Use of Key Items

Go into your inventory and select 'Equip' on a key story item to place it in your hand. Manually created trigger zones were added and (hopefully) you should find that placing it in a logical place will activate the item. (For example, hold a plate to a Golem's mouth.) The standard 'Use' key remains as a backup.

## Physical Crouching

Crouch down to the floor to hide from stalkers. Operates as the base game as far as hiding. Alternatively, hold the left trigger to crouch.

## Physical Doors

Grab a door by the handle, push or pull it in either direction to open. Doors carry momentum and can be thrown closed or open by grabbing the handle, swinging with speed and letting go. A door that is left in between open and closed with no momentum will automatically adjust itself to the closest state. A door that is open can be swung closed by placing your hand on the leaf and swinging, no grip needed. A closed, unlocked door can be barged open by shoving it with both hands. Swing a door at a stalker with enough force to damage them.

## Physical Hiding Spots

Grab the leftmost side of a wardrobe to slide the door open along its rails. Step inside and close the door to hide. Optional toggle to make the doors transparent once you are hidden and watch stalkers search for you. Turn it off for a more immersive experience. Near the beginning of Daniella's section, step into the cubby and close the curtain to hide. Beds are still canned animations; Use the interaction button to slide underneath.

## Physical Ladder Climbing

Grab a ladder's rungs to start climbing hand over hand. Once you climb high enough, you will automatically step forward from it. Joining a ladder from the top will automatically swing your camera around to face the rungs. Letting go of a ladder with both hands too early will cause you to fall to the ground and increase your panic by a measure of how far you fell. It will also reduce your movement speed for a few seconds. 
This by itself will never set your panic past 95, so you will not enter panic mode from falling off of a ladder. Fall onto a stalker however...

## Physical Lever Usage

I could only find 3 instances in the game where this even applies:

Gate Lever beside Fresh Flowers

Breaker Switch in Doll Trap Room

Lever to activate iron maiden

Grab each one and pull it along its path to activate.

## Attack using your hands

Swinging with one hand should be enough to break vases. Vases have been made significantly bigger to accommodate this and sometimes clip.

Pushing with two hands is the only one to damage stalkers and force open doors.

You will know you have activated the attack when you hear Fiona grunt.

## Hewie

A local Whisper model running entirely on your machine listens to your voice and sends the commands to Hewie. Optional Push To Talk or Open Mic mode. Optional Subtitles to show which command you triggered. Currently, only Go, Come, and Stay work via the stick - Flick up or down to activate Go and Come, or click the right stick to Stay.

Pet Hewie with your hands to get controller feedback and increase your relationship.

Tell him to sit, stand nearby, and tell him to "Shake!" . He will offer his paw to you.

Protect him with your life

## 3D positional audio with Steam Audio.

Toggleable. Uses Steam Audio to improve locational accuracy. Hear more clearly where stalkers are.

## Customizable panic settings

Enter the VR options menu to see a Panic Effects submenu. In here, you can select 'Full' , 'Reduced' and 'Minimal' presets, or just pick which effects you do and don't want.

> ⚠️ Full effects are strong and will very likely to cause nausea, so be prepared. There is also real risk of photosensitive issues, so please start from minimal and work your way up if you are not sure.

## VR Comfort Options

A handful of your standard VR comfort settings that should work reliably. Available in the VR menu.

---

## Requirements

- A PC VR headset with an OpenXR runtime (SteamVR, Meta Quest Link, etc.)
- **Your own legally obtained copy of Haunting Ground (tested on USA) as an `.iso` disc image.** No game data is included, and none will be provided.
- [Microsoft Visual C++ Redistributable (x64)](https://aka.ms/vs/17/release/vc_redist.x64.exe), grab the latest.

## Install

1. Download and extract the latest `.zip` from [Releases](../../releases)
4. Double-click **`Play.bat`** with your headset ready to go. On first launch, you will be asked to select your Haunting Ground .iso , same as with openhuey.
6. The first time it launches, you will be asked to calibrate. You can do this at any time during the game by accessing the VR menu.

**Updating:** download the new zip and copy your `library` and `user` folders (your imported game and saves) into the new folder.

> ❗ It is not recommended to update to the latest openhuey version without confirming this mod will work with it first. I need to manually update each one to ensure compatibility.

## Current Known issues

- Some doors occasionally slam shut right after you walk through them. I have not found a reason for this yet. They do not lock, so feel free to just open it again (maybe it will save you time in a chase?)
- As this is a fixed camera angle game at base, there are many areas and viewpoints that were just never meant to be seen. Expect holes in geometry and odd looking areas. The most egregious is anywhere with a view of outside, where you will just be staring into a void in the sky. This is planned to be fixed but will require extensive manual reworking in Blender and will likely take a long time.
  

## Credits and thanks

**Huge thanks to ArnautDaniel [OpenHuey](https://github.com/ArnautDaniel/OpenHuey)**. Their rebuild of Haunting Ground for PC is the foundation of everything here. Without it, this mod would not exist. Please go and support the original project. Arnaut is extremely supportive and has a discord channel which is worth joining.

Haunting Ground is my #1 favourite game and being able to bring it to life in VR has been a fun experience and something I've wanted for years. I hope you enjoy.

Also inspired by Skyrim VR mods such as FRIK, VRIK and HIGGS, and by Half-Life 2 VR.



---

## Legal

- **Haunting Ground** and all related names, characters and assets are trademarks and copyright of **Capcom Co., Ltd.** This is an unofficial, non-commercial fan project. It is not affiliated with, endorsed by or sponsored by Capcom.
- This repository and its releases **do not include the game or its data files.** You must own a legitimate copy of Haunting Ground to play. Please don't ask for, or share, game files or disc images.
- The code is released under the **GNU General Public License v3.0**, the same as OpenHuey. See [`LICENSE`](LICENSE).
