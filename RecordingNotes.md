# Some Technical Bits About The Page
This page is best viewed using a Markdown Viwer. I use [Markdown Viewer](https://github.com/simov/markdown-viewer) in Chrome.

# Glossary
## Track
A component of the "Arrange" view. Shows the actual recorded signal
## Channel
A component of the "Console" view. Used in muting soloing, panning and setting the output volume of a single source
## Sends
Sends can blend the effected audio (wet) with the non-effected (dry). Ideal candidates as things like reverb. A second advantage is that when you add a reverb to a send Studio One creates a separate effects channel for it. You can then add an EQ to the effects channel to take out, say 40Hz, from the wet signal without applying the EQ to the dry signal
## Inserts
Insert effects will process the whole audio stream. A little like an effects pedal in a signal chain. What comes out is a wholly effected copy of what goes in.
Ideal candidates are compression, distortion and pitch shifters. Anything where you want the effect to be applied to the whole signal.

# Programming a drum track

## General Midi
Here is a [ general midi percussion key map](https://musescore.org/sites/musescore.org/files/General%20MIDI%20Standard%20Percussion%20Set%20Key%20Map.pdf)

## Tips
1. To duplicate a part or pattern, select the part or pattern and hit the D key

## Steps to add a drum track
1. Add an instrument track called "Kick"
2. Drag an instance of Impact onto the newly added track
3. Assign sound samples to midi channels by dragging the sound file onto the corresponding Impact pad. See the general midi percussion key map listed above for the pads to target
4. After dropping a sample onto a pad, right click and select "Rename pad". Applying a naming convention to pads can make the role of each pad easier to remember.
Drum samples are stored here:
> C:\Users\mike\Documents\Recording\Downloaded Samples\Drums

|Key|Name|Sample|
|---|----|------|
C1|Kick|Bass Drums\TS_NIR_Z_JJ_kick_one_shot_true_hard.wav
D1|Acoustic snare|Snares\TS_NIR_Z_JJ_snare_one_shot_craviolow_hard.wav
F1|Floor Tom|Toms\TS_NIR_Z_JJ_tom_one_shot_modern_tom_3_hard.wav
B1|Low-Mid Tom|Toms\TS_NIR_Z_JJ_tom_one_shot_modern_tom_2_hard.wav
D2|High Tom|Toms\TS_NIR_Z_JJ_tom_one_shot_modern_tom_1_hard.wav
F#1|Closed Hi-Hat|Hats\TS_NIR_Z_JJ_hat_one_shot_tight_soft.wav

## Assigning a drum to an output channel
In Impact, click the drum pad's "output channel assignment" button. From the popup you can assign the drum to any channel:
![Impact Output Assignment Channel](https://github.com/objectivedynamics42/studio-one/blob/main/images/impact-output-channelhighlighted.png?raw=true)

## Adding effects
### TODO Complete This Section

## Sequencing patterns
The Pattern Inspector can be used to create variations of a pattern. Click the 'i' as shown here:
![Pattern Editor Image](https://github.com/objectivedynamics42/studio-one/blob/main/images/pattern-editor-showing-info-button.png?raw=true)

## Quantizing
Double click on the track and it will open the midie editor

## Separating Midi Drums into separate tracks
This doesn't appear to work for drums where you've used "Convert part to pattern"...
Right click on the track (where the recording is) and select 
	Instrument Tracks
		Explode Pitches to Tracks

## Bouncing down Midi Tracks to Audio
### TODO Make proper markdown links
Select the tracks you want to bounce down (left hand side where the arm and monitor buttons are), right click and select "Transform to Audio Track"
	https://www.youtube.com/watch?v=P4t4zngkrko


# Recording Audio
## Audiobox iTwo
### TODO Grab an example image from the net and update the text
Each of the two inputs can accept line or instrument levels. You can switch between line and instrument level using the input source button:
![AudioBox iTwo input source](https://github.com/objectivedynamics42/studio-one/blob/main/images/audiobox-itwo-input-source.png?raw=true)

For a guitar, if connecting directly to the iTwo, you should be using the instrument setting and the corresponding blue LED should be illuminated.
If connecting via the Helix, you should use line level and the blue LED should be off.

## Hiding unused channels
### TODO Add an example image and update the text
It looks like Impact adds eight channels. If you assign all of your drums to the same channel that will give you 7 channels that you don't need.
You can hide them from the channel list - click on the hamburger in the bottom left corner of studio one to bring it up. Then right click on
a channel and select hide

## Automatically returning to the start of a track once you've finished playing or recording
Transport | Options |  Return to Start on Stop

## Setting levels in Studio One
### TODO Make proper markdown links, add an example image and update the text
Don't monitor using the normal channel strips. While you can use them they are really for use with outputs
Instead, monitor the input level using the inputs tab in the console.
	https://www.youtube.com/watch?v=Qz0afhER6fo

Viewing the console:
View | Console (F3)

TODO Make proper markdown links and update the text
The inputs tab can be opened and closed by clicking on the ->| icon on the left of the console
https://www.youtube.com/watch?v=ZCJN9XxtPM4

TODO Make proper markdown links and update the text
On the AudioBox iTwo, turn the input level shaft encoder down to zero and then edge it up gradualy while playing pretty hard in between increments.
You want the input level to be in the range -12db to -10db
https://youtu.be/koho2W8FRkY?t=419

## Effects
Some guff or other goes here

## Click Track Volume
### TODO add images and update the text
Above the "Main" fader (whatever it's called?) are three icons:
	Click On/Off	Seems independent of the one on the transport panel
	Click Volume	Changes the click volume - set it low about -16dB
	Channel Mode	(looks like it's similar to the arm button but I'm not sure)

## Troubleshooting
### TODO add images and update the text
1. Nothing showing on the input level meters in the inputs tab in the console:
Check that you have the input (left or right/input 1 or input 2) selected for the channel

## Questions
Does the AudioBox iTwo support zero latency hardware monitoring?
	If it does, see if you can monitor Ampire and the like directly from the headphone out on the iTwo
	Also, is it possible to add, say, reverb to the headphone mix without it being added to the recording.
	This latter trick is often employed to make the performer feel more comfortable with the overall
	sound without actually committing the reverb to the track


# Appendix
