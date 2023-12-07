# Glossary
## Tracks and Channels
Tracks and channels are different things:
* [A track](#a_studio_one_track) is a component of the *Song Arranger* view. 
* [A channel](#a_studio_one_channel) is a component of the *Console* view

These concepts are explored further in [this Presonus video](https://www.youtube.com/watch?v=5POLA2HMtRM)

## Sends
A [send effect](#a_studio_one_send_with_compressor) can be used to blend the effected audio (wet) with the non-effected (dry). Ideal candidates as things like reverb. A second
advantage is that when you add a reverb to a send Studio One creates a separate effects channel for it. You can then add
an EQ to the effects channel to take out, say 40Hz, from the wet signal without applying the EQ to the dry signal.
Here is a channel showing a send configured for a compressor:

## Inserts
An [insert effect](#a_studio_one_insert_with_reverb) will process the whole audio stream. A little like an effects pedal in a signal chain. What comes out is
a wholly effected copy of what goes in. Ideal candidates are compression, distortion and pitch shifters. Anything where
you want the effect to be applied to the whole signal. Here is a channel with an insert configured for a reverb:

## Track List
Supports interaction with automation tracks for e.g. volume and pan. See [opening and viewing the track list](#studio_one_opening_and_viewing_track_list)

## Channel List<a name="channel_list"></a>
The *Channel List* offers tools for grouping and adding busses for tracks. You can also show and hide tracks from here.
It can be opened using the *Channel List button*. See [opening and viewing the channel list](#studio_one_opening_and_viewing_channel_list)

# Audio Setup
## Options
### Processing and the *audio roundtrip* value
This can be set from the following menu:
```
    Studio one | Options... | Audio Setup | Processing 
```
Values below 10ms are recommended:

![Audio Roundtrip](https://github.com/objectivedynamics42/studio-one/blob/main/images/latency-display.png?raw=true)

# Programming a drum track

## General Midi
Here is a [general midi percussion key map](https://musescore.org/sites/musescore.org/files/General%20MIDI%20Standard%20Percussion%20Set%20Key%20Map.pdf)

## Tips
1. To duplicate a part or pattern, select the part or pattern and hit the D key

## Steps to add a drum track
1. Add an instrument track called "Kick"
2. Drag an instance of Impact onto the newly added track
3. Assign sound samples to midi channels by dragging the sound file onto the corresponding Impact pad. See the general midi percussion key map listed above for the pads to target
4. After dropping a sample onto a pad, right-click and select "Rename pad". Applying a naming convention to pads can make the role of each pad easier to remember.
Drum samples are stored here:
> C:\Users\mike\Documents\Recording\Downloaded Samples\Drums

| Key |Name|Sample|
|-----|----|------|
| C1  |Kick|Bass Drums\TS_NIR_Z_JJ_kick_one_shot_true_hard.wav|
| D1  |Acoustic snare|Snares\TS_NIR_Z_JJ_snare_one_shot_craviolow_hard.wav|
| F1  |Floor Tom|Toms\TS_NIR_Z_JJ_tom_one_shot_modern_tom_3_hard.wav|
| B1  |Low-Mid Tom|Toms\TS_NIR_Z_JJ_tom_one_shot_modern_tom_2_hard.wav|
| D2  |High Tom|Toms\TS_NIR_Z_JJ_tom_one_shot_modern_tom_1_hard.wav|
| F#1 |Closed Hi-Hat|Hats\TS_NIR_Z_JJ_hat_one_shot_tight_soft.wav|

## Assigning a drum to an output channel
In Impact, click the drum pad's "output channel assignment" button. From the popup you can assign the drum to any
channel:
![Impact Output Assignment Channel](https://github.com/objectivedynamics42/studio-one/blob/main/images/impact-output-channelhighlighted.png?raw=true)

## Adding effects
### TODO Complete This Section

## Sequencing patterns
The Pattern Inspector can be used to create variations of a pattern. Click the 'i' as shown here:
![Pattern Editor Image](https://github.com/objectivedynamics42/studio-one/blob/main/images/pattern-editor-showing-info-button.png?raw=true)

## Quantizing
Double-click on the track and it will open the midi editor

## Separating Midi Drums into separate tracks
This doesn't appear to work for drums where you've used "Convert part to pattern"...
Right click on the track (where the recording is) and select 
	Instrument Tracks
		Explode Pitches to Tracks

## Bouncing down Midi Tracks to Audio
Right-click the channel that you want to bounce down and select *Transform to Audio Track*:

![Transform to Audio Track](https://github.com/objectivedynamics42/studio-one/blob/main/images/transform-to-audio-track.png?raw=true)

For further examples see 
[this Presonus video on YouTube](https://www.youtube.com/watch?v=P4t4zngkrko)

# Recording Audio
## Audiobox iTwo
Each of the two inputs can accept line or instrument levels. You can switch between line and instrument level using the
input source button. Channel 1's (left) input source button is highlighted below:
![AudioBox iTwo input source](https://github.com/objectivedynamics42/studio-one/blob/main/images/audiobox-itwo-input-source.png?raw=true)

For a guitar, if connecting directly to the iTwo, you should be using the instrument setting and the corresponding blue
LED should be illuminated.
If connecting via the Helix, you should use line level and the blue LED should be off.

## Hiding unused channels
You can hide tracks using [the channel list](#channel_list)

## Automatically returning to the start of a track once you've finished playing or recording
Transport | Options |  Return to Start on Stop

## Setting levels in Studio One
### TODO add an example image and update the text

Don't monitor using the normal channel strips. While you can use them they are really for use with outputs
Instead, monitor the input level using the inputs tab in the console. See [this video](https://www.youtube.com/watch?v=Qz0afhER6fo) for more information


Viewing the console:
View | Console (F3)

TODO Make proper markdown links and update the text
The inputs tab can be opened and closed by clicking on the ->| icon on the left of the console
https://www.youtube.com/watch?v=ZCJN9XxtPM4

TODO Make proper markdown links and update the text
On the AudioBox iTwo, turn the input level shaft encoder down to zero and then edge it up gradualy while playing pretty
hard in between increments. You want the input level to be in the range -12db to -10db
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
1. Does the AudioBox iTwo support zero latency hardware monitoring?
    1. it does, see if you can monitor Ampire and the like directly from the headphone out on the iTwo
2. is it possible to add, say, reverb to the headphone mix without it being added to the recording.
	This latter trick is often employed to make the performer feel more comfortable with the overall
	sound without actually committing the reverb to the track

# Appendix
## A Studio One Track <a name="a_studio_one_track"></a>

![A Studio One Track](https://github.com/objectivedynamics42/studio-one/blob/main/images/track-527-60.png?raw=true)

## A Studio One Channel <a name="a_studio_one_channel"></a>

![A Studio One Channel](https://github.com/objectivedynamics42/studio-one/blob/main/images/channel-50-205.png?raw=true)

## A channel with a compressor as a send effect<a name="a_studio_one_send_with_compressor"></a>

![A Studio One Send with Compressor](https://github.com/objectivedynamics42/studio-one/blob/main/images/channel-with-send-fulls-size.png?raw=true)

## A channel with a Reverb as an insert <a name="a_studio_one_insert_with_reverb"></a>

![Insert with Reverb](https://github.com/objectivedynamics42/studio-one/blob/main/images/channel-with-insert-full-size.png?raw=true)


## Opening and viewing the track list<a name="studio_one_opening_and_viewing_track_list"></a>

The Track List button:

![Track List Button](https://github.com/objectivedynamics42/studio-one/blob/main/images/track-list-full-size.png?raw=true)

The Track List showing automation tracks for volume and pan:

![Track List Open](https://github.com/objectivedynamics42/studio-one/blob/main/images/track-list-open-full-size.png?raw=true)

##  Opening and viewing the channel list<a name="studio_one_opening_and_viewing_channel_list"></a>

The Channel List button:

![Channel List Button](https://github.com/objectivedynamics42/studio-one/blob/main/images/channel-list-full-size.png?raw=true)

The Channel List:

![Channel List Open](https://github.com/objectivedynamics42/studio-one/blob/main/images/channel-list-open-full-size.png?raw=true)

Channel List Operations:

![Channel List Operations](https://github.com/objectivedynamics42/studio-one/blob/main/images/channel-list-operations-full-size.png?raw=true)
