MIDI-Drum-Controller
====================
This is a MIDI Drum Controller written in [Serpent](https://www.google.com) which can accept control messages via the [Open Sound Control (OSC) protocol](http://en.wikipedia.org/wiki/Open_Sound_Control).

##Set Up

a. Open TouchOSC on your Device (I use in IOS). 

b. This is the setting: You should replace the ‘Host’ with your IP address. Outgoing and incoming Port are 8001 and 60385

c. You should unzip my project folder and open it, in line 4 in “oscSender.srp”, you should change”128.237.207.143" to your device IP address which is running the TouchOSC. (my device IP address should be 128.237.207.143 as the image above)

d. For the layout in TouchOSC, please select ‘Beatmachine’.

******Note Start*******
There should be 4 windows of ‘Beatmachine’ layout in your TouchOSC, at very top of your device you can change the window. Window 1 is for ‘Drum Pad’ in wxserpent and window 2 is for ‘Drum Pattern’ in wxserpent
******Note End*******

e. Then you can open init.srp with wxserpent.

##Drum Pad Window

You can get most information about the function of each button/key/slider through the ‘Drum Pad’ window of wxserpent.

You can hit the drum pad to hear the sound.

Volume Slider: Value from 0 to 127. Just control the volume of drum pad in ‘Drum Pad’ window.

Mute: Mute the drum pad.

Tempo Slider: This is the tempo control for ‘Drum Pattern’ window. It can change the tempo of the drum loop. Value from 40 to 180.

Click: Turn on/off a metronome.

Random: Generate a random drum loop in ‘Drum Pattern’ window. 

Clear: Clear the loop information in ‘Drum Pattern’ window.

Load: Load a pre-defined drum loop in ‘Drum Pattern’ window.

******Note Start*******
While the drum loop is playing, you can also hit the drum pad to get drum sound, which has no relationship with the sound in the drum loop.
******Note End*******

##Drum Pattern Window

Here you can draw your own drum loop and play. There are sixteen-note long loop you can draw, and each line from top to bottom represents Crash, Tom 2, Tom 1, Hi-Hat, Snare and Kick.

There are also faders in the bottom of the screen, you can use that to control the volume of each ‘beat’. Values are from 0 to 100.

When you click ‘Random’ button in ‘Drum Pad Interface’, it will automatically load a random pattern into the screen, and the volume of each ‘beat’ is also set randomly.

When you click ‘Clear’ button in ‘Drum Pad Interface’, it will clear all notes here.

When you click ‘Load’ button in ‘Drum Pad Interface’ it will automatically load a pre-defined pattern into the screen, and the volume of each ‘beat’ is also set to 70.

******Note Start*******
Currently ‘Drum Pattern’ window can not talk back to your device running TouchOSC, which means when you draw your loop in TouchOSC the ‘Drum Pattern’ window can be updated. But when you draw your loop in ‘Drum Pattern’ window, you can not see that in TouchOSC.
******Note End*******

******Note Start*******
There should be a font warning when run this program:

CoreText performance note: Client called CTFontCreateWithName() using name "Times" and got font with PostScript name "Times-Roman". For best performance, only use PostScript names when calling this API.
******Note End*******

Have Fun!
