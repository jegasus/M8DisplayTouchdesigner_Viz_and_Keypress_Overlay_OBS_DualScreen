# M8 Display for OBS Output

This M8 Display for TouchDesigner makes it slightly easier to stream content out to OBS if users want to display the M8 Screen and the M8 Body simultaneously.

This version was built on top of [Gleix's TouchDesigner M8Display](https://github.com/Gleix/M8DisplayTouchdesigner_Viz_and_Keypress_Overlay).

See Gleix's video overview for more info on the original: https://youtu.be/FMR5dIHkMnY

# Requirements

You will need to have the following items ready to use: 

* Derivative Touchdesigner: https://derivative.ca/download
* OBS: https://obsproject.com/download
* Syphon Spout: https://offworld.live/spout-plugin-for-obs-studio
* M8 (hardware or headless) running firmware 1.0.3 or above

# Setting things up for the first time

1. Download or clone this repository onto your local drive
2. Unzip the contents of the zipfile somewhere easy to find. For example, "C:/Users/username/M8_Stuff"
3. Set up audio monitoring (see details below)
4. In OBS, click on `Scene Collection > Import` and import the `OBS_M8_TouchDisplay.json` file that is found in this repository's `OBS` folder
![](https://github.com/jegasus/M8DisplayTouchdesigner_Viz_and_Keypress_Overlay_OBS_DualScreen/assets/76404978/53e55bfd-6596-4ca9-8d93-cbfeefa94a37)


# Usage instructions

1. Plug your M8 device into your computer.
2. Open the `M8Display_GleixViz_LightweightKeypressOverlay_Both.toe` file that is found in this repository
3. In the TouchDisplay window, click on the `Connection & Keyboard Settings` button on the bottom left and choose the M8 on the `Serial Port` drop-down menu.
   ![](https://github.com/jegasus/M8DisplayTouchdesigner_Viz_and_Keypress_Overlay_OBS_DualScreen/assets/76404978/2b7d4510-e8ba-4462-a0f1-c744c07c5a95)
5. Open up OBS. 
6. In the OBS window, on the menu bar at the top, click on `Scene Collection > M8 TouchDisplay`
   ![](https://github.com/jegasus/M8DisplayTouchdesigner_Viz_and_Keypress_Overlay_OBS_DualScreen/assets/76404978/d1088eaf-f705-447e-80ad-e0f2f5c492e7)
7. Now, you can choose which of the three types of display OBS will stream out by picking one of the `Scenes` in the box at the bottom left of the OBS window.
   i. M8 TouchDisplay - 2in1: This is a widescreen 16:9 view that allows you to show the M8 screen on the left as well as the M8 body on the right with the button-press highlights.
   ii. M8 TouchDisplay - 2in1 (HFlip): This is the same as above, but horizontally flipped. If you're trying to stream using OBS' virtual camera, you might want to use this version instead.
   iii. M8 TouchDisplay - Original: This is the original output of Gleix's TouchDisplay. You can command what is actually shown on screen by clicking on the `Full View` button on the bottom right.
   ![](https://github.com/jegasus/M8DisplayTouchdesigner_Viz_and_Keypress_Overlay_OBS_DualScreen/assets/76404978/751597d7-41f8-4bc3-b284-2106ff602c2c)


# Setting Up M8 Input Audio Monitoring
Note: This section is copied directly from Dirtywave's original [Headless Setup guide](https://github.com/DirtyWave/M8Docs/blob/main/docs/M8HeadlessSetup.md).

In order to hear the audio from the M8 Teensy, you need to enable monitoring of the M8 Input device on your computer. You can do this with any software that supports this (like a Digital Audio Workstation (DAW) such as Ableton Live), but some simple recommendations follow.

## Windows
The simplest way to monitor the M8 Input device is to do the following:

1. Right click on the 🔊 sound icon in the system tray and click **Sounds**.

   ![](https://github.com/Dirtywave/M8Docs/raw/main/docs/images/windows_taskbar_sounds.png)
1. Switch to the Recording tab. Find the M8 device in the list, select it, and click Properties.

   ![](https://github.com/Dirtywave/M8Docs/raw/main/docs/images/windows_sound_setup_1.png)
1. Switch to the Listen tab. Check the Listen to this device box. Click OK.

   ![](https://github.com/Dirtywave/M8Docs/raw/main/docs/images/windows_sound_setup_2.png)
   
## Mac OS
There are multiple options for Mac OS:
1. **Use Quicktime Player** (free, but there may be audio lag):
   1. Open Quicktime Player.
   1. Select **File > New Audio Recording**
   1. Click the dropdown button next to the 🔴 record button, and select the M8 input.
   1. Adjust the volume slider to hear the M8 input. You don't need to click the record button.
1. **Use Audacity** (free):
   1. Download and install Audacity from [https://www.audacityteam.org/](https://www.audacityteam.org/)
   1. Open Audacity.
   1. Open Audacity's **Preferences** menu.
   1. Select the **Recording** section on the left. Check the **Software playthrough of input** box.
   
      ![](https://github.com/Dirtywave/M8Docs/raw/main/docs/images/mac_audacity_prefs.png)
   1. Exit the Preferences menu.
   1. Select **M8** as your microphone input, then click on the text that says **Click to Start Monitoring**. You should now hear M8's input through your speakers.
   
      ![](https://github.com/Dirtywave/M8Docs/raw/main/docs/images/mac_audacity_setup.png)
1. **Use Audio Hijack** (works, but costs $59 USD):
   1. You can purchase Audio Hijack here: [https://rogueamoeba.com/audiohijack/](https://rogueamoeba.com/audiohijack/)
1. **Use OBS Studio** (free, but overkill):
   1. You can download OBS Studio here: [https://obsproject.com/](https://obsproject.com/)
