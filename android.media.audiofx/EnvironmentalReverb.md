# EnvironmentalReverb

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EnvironmentalReverb

Kotlin| [Java](EnvironmentalReverb.md) 
| --- | --- |

```
open class EnvironmentalReverb : AudioEffect
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.media.audiofx.AudioEffect](AudioEffect.md) ||
| | ↳ | [android.media.audiofx.EnvironmentalReverb](EnvironmentalReverb.md) |

A sound generated within a room travels in many directions. The listener first hears the direct sound from the source itself. Later, he or she hears discrete echoes caused by sound bouncing off nearby walls, the ceiling and the floor. As sound waves arrive after undergoing more and more reflections, individual reflections become indistinguishable and the listener hears continuous reverberation that decays over time. Reverb is vital for modeling a listener's environment. It can be used in music applications to simulate music being played back in various environments, or in games to immerse the listener within the game's environment. The EnvironmentalReverb class allows an application to control each reverb engine property in a global reverb environment and is more suitable for games. For basic control, more suitable for music applications, it is recommended to use the [android.media.audiofx.PresetReverb](PresetReverb.md) class.

An application creates a EnvironmentalReverb object to instantiate and control a reverb engine in the audio framework.

The methods, parameter types and units exposed by the EnvironmentalReverb implementation are directly mapping those defined by the OpenSL ES 1.0.1 Specification (http://www.khronos.org/opensles/) for the SLEnvironmentalReverbItf interface. Please refer to this specification for more details.

The EnvironmentalReverb is an output mix auxiliary effect and should be created on Audio session 0. In order for a MediaPlayer or AudioTrack to be fed into this effect, they must be explicitely attached to it and a send level must be specified. Use the effect ID returned by getId() method to designate this particular effect when attaching it to the MediaPlayer or AudioTrack.

Creating a reverb on the output mix (audio session 0) requires permission [android.Manifest.permission#MODIFY_AUDIO_SETTINGS](../android/Manifest.permission.md)

See [android.media.audiofx.AudioEffect](AudioEffect.md) class for more details on controlling audio effects.

## Summary

| Nested classes ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [OnParameterChangeListener](../android/media/audiofx/EnvironmentalReverb.OnParameterChangeListener.md) The OnParameterChangeListener interface defines a method called by the EnvironmentalReverb when a parameter value has changed. |
| open | [Settings](../android/media/audiofx/EnvironmentalReverb.Settings.md) The Settings class regroups all environmental reverb parameters. |

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARAM_DECAY_HF_RATIO](EnvironmentalReverb.md) Decay HF ratio. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARAM_DECAY_TIME](EnvironmentalReverb.md) Decay time. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARAM_DENSITY](EnvironmentalReverb.md) Density. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARAM_DIFFUSION](EnvironmentalReverb.md) Diffusion. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARAM_REFLECTIONS_DELAY](EnvironmentalReverb.md) Early reflections delay. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARAM_REFLECTIONS_LEVEL](EnvironmentalReverb.md) Early reflections level. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARAM_REVERB_DELAY](EnvironmentalReverb.md) Reverb delay. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARAM_REVERB_LEVEL](EnvironmentalReverb.md) Reverb level. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARAM_ROOM_HF_LEVEL](EnvironmentalReverb.md) Room HF level. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARAM_ROOM_LEVEL](EnvironmentalReverb.md) Room level. |

| Inherited constants ||
|---|---|
| From class [AudioEffect](AudioEffect.md) |----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_CLOSE_AUDIO_EFFECT_CONTROL_SESSION](AudioEffect.md) <br /> Intent to signal to the effect control application or service that an audio session is closed and that effects should not be applied anymore. The effect control application receiving this intent will delete all effects on this session and store current settings in package specific storage. The calling package name is indicated by the [EXTRA_PACKAGE_NAME](AudioEffect.md) extra and the audio session ID by the [EXTRA_AUDIO_SESSION](AudioEffect.md) extra. Both extras are mandatory. It is good practice for applications to broadcast this intent when music playback stops and/or when exiting to free system resources consumed by audio effect engines. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_DISPLAY_AUDIO_EFFECT_CONTROL_PANEL](AudioEffect.md) <br /> Intent to launch an audio effect control panel UI. The goal of this intent is to enable separate implementations of music/media player applications and audio effect control application or services. This will allow platform vendors to offer more advanced control options for standard effects or control for platform specific effects. The intent carries a number of extras used by the player application to communicate necessary pieces of information to the control panel application. The calling application must use the android.app.Activity#startActivityForResult(Intent, int) method to launch the control panel so that its package name is indicated and used by the control panel application to keep track of changes for this particular application. The [EXTRA_AUDIO_SESSION](AudioEffect.md) extra will indicate an audio session to which the audio effects should be applied. If no audio session is specified, either one of the follownig will happen: - If an audio session was previously opened by the calling application with [ACTION_OPEN_AUDIO_EFFECT_CONTROL_SESSION](AudioEffect.md) intent, the effect changes will be applied to that session. - If no audio session is opened, the changes will be stored in the package specific storage area and applied whenever a new audio session is opened by this application. The [EXTRA_CONTENT_TYPE](AudioEffect.md) extra will help the control panel application customize both the UI layout and the default audio effect settings if none are already stored for the calling application. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_OPEN_AUDIO_EFFECT_CONTROL_SESSION](AudioEffect.md) <br /> Intent to signal to the effect control application or service that a new audio session is opened and requires audio effects to be applied. This is different from [ACTION_DISPLAY_AUDIO_EFFECT_CONTROL_PANEL](AudioEffect.md) in that no UI should be displayed in this case. Music player applications can broadcast this intent before starting playback to make sure that any audio effect settings previously selected by the user are applied. The effect control application receiving this intent will look for previously stored settings for the calling application, create all required audio effects and apply the effect settings to the specified audio session. The calling package name is indicated by the [EXTRA_PACKAGE_NAME](AudioEffect.md) extra and the audio session ID by the [EXTRA_AUDIO_SESSION](AudioEffect.md) extra. Both extras are mandatory. If no stored settings are found for the calling application, default settings for the content type indicated by [EXTRA_CONTENT_TYPE](AudioEffect.md) will be applied. The default settings for a given content type are platform specific. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ALREADY_EXISTS](AudioEffect.md) <br /> Internal operation status. Not returned by any method. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_TYPE_GAME](AudioEffect.md) <br /> Value for [EXTRA_CONTENT_TYPE](AudioEffect.md) when the type of content played is game audio <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_TYPE_MOVIE](AudioEffect.md) <br /> Value for [EXTRA_CONTENT_TYPE](AudioEffect.md) when the type of content played is video or movie <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_TYPE_MUSIC](AudioEffect.md) <br /> Value for [EXTRA_CONTENT_TYPE](AudioEffect.md) when the type of content played is music <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_TYPE_VOICE](AudioEffect.md) <br /> Value for [EXTRA_CONTENT_TYPE](AudioEffect.md) when the type of content played is voice audio <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EFFECT_AUXILIARY](AudioEffect.md) <br /> Effect connection mode is auxiliary. Auxiliary effects must be created on session 0 (global output mix). In order for a MediaPlayer or AudioTrack to be fed into this effect, they must be explicitely attached to this effect and a send level must be specified. Use the effect ID returned by [getId()](AudioEffect.md))to designate this particular effect when attaching it to the MediaPlayer or AudioTrack. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EFFECT_INSERT](AudioEffect.md) <br /> Effect connection mode is insert. Specifying an audio session ID when creating the effect will insert this effect after all players in the same audio session. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EFFECT_POST_PROCESSING](AudioEffect.md) <br /> Effect connection mode is post processing. The audio post processing effects are attached to an audio output stream or device <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EFFECT_PRE_PROCESSING](AudioEffect.md) <br /> Effect connection mode is pre processing. The audio pre processing effects are attached to an audio input stream or device <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR](AudioEffect.md) <br /> Unspecified error. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_BAD_VALUE](AudioEffect.md) <br /> Operation failed due to bad parameter value. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_DEAD_OBJECT](AudioEffect.md) <br /> Operation failed due to dead remote object. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_INVALID_OPERATION](AudioEffect.md) <br /> Operation failed because it was requested in wrong state. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_NO_INIT](AudioEffect.md) <br /> Operation failed due to bad object initialization. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_NO_MEMORY](AudioEffect.md) <br /> Operation failed due to lack of memory. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_AUDIO_SESSION](AudioEffect.md) <br /> Contains the ID of the audio session the effects should be applied to. This extra is for use with [ACTION_DISPLAY_AUDIO_EFFECT_CONTROL_PANEL](AudioEffect.md), [ACTION_OPEN_AUDIO_EFFECT_CONTROL_SESSION](AudioEffect.md) and [ACTION_CLOSE_AUDIO_EFFECT_CONTROL_SESSION](AudioEffect.md) intents. The extra value is of type int and is the audio session ID. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_CONTENT_TYPE](AudioEffect.md) <br /> Indicates which type of content is played by the application. This extra is for use with [ACTION_DISPLAY_AUDIO_EFFECT_CONTROL_PANEL](AudioEffect.md) and [ACTION_OPEN_AUDIO_EFFECT_CONTROL_SESSION](AudioEffect.md) intents. This information is used by the effect control application to customize UI and select appropriate default effect settings. The content type is one of the following: - [CONTENT_TYPE_MUSIC](AudioEffect.md) - [CONTENT_TYPE_MOVIE](AudioEffect.md) - [CONTENT_TYPE_GAME](AudioEffect.md) - [CONTENT_TYPE_VOICE](AudioEffect.md) If omitted, the content type defaults to [CONTENT_TYPE_MUSIC](AudioEffect.md). <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_PACKAGE_NAME](AudioEffect.md) <br /> Contains the package name of the calling application. This extra is for use with [ACTION_OPEN_AUDIO_EFFECT_CONTROL_SESSION](AudioEffect.md) and [ACTION_CLOSE_AUDIO_EFFECT_CONTROL_SESSION](AudioEffect.md) intents. The extra value is a string containing the full package name. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SUCCESS](AudioEffect.md) <br /> Successful operation. <br /> | ||

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [EnvironmentalReverb](EnvironmentalReverb.md))`(`priority:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `audioSession:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Class constructor. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [getDecayHFRatio](EnvironmentalReverb.md))`()` Gets the ratio of high frequency decay time (at 5 kHz) relative to low frequencies. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDecayTime](EnvironmentalReverb.md))`()` Gets the decay time. |
| open [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [getDensity](EnvironmentalReverb.md))`()` Gets the density level. |
| --- | --- |
| open [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [getDiffusion](EnvironmentalReverb.md))`()` Gets diffusion level. |
| open [EnvironmentalReverb.Settings](../android/media/audiofx/EnvironmentalReverb.Settings.md)! | [getProperties](EnvironmentalReverb.md))`()` Gets the environmental reverb properties. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getReflectionsDelay](EnvironmentalReverb.md))`()` Gets the reflections delay. |
| --- | --- |
| open [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [getReflectionsLevel](EnvironmentalReverb.md))`()` Gets the volume level of the early reflections. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getReverbDelay](EnvironmentalReverb.md))`()` Gets the reverb delay. |
| open [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [getReverbLevel](EnvironmentalReverb.md))`()` Gets the reverb level. |
| --- | --- |
| open [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [getRoomHFLevel](EnvironmentalReverb.md))`()` Gets the room HF level. |
| open [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [getRoomLevel](EnvironmentalReverb.md))`()` Gets the master volume level of the environmental reverb effect. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDecayHFRatio](EnvironmentalReverb.md))`(`decayHFRatio:` ` [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)`)` Sets the ratio of high frequency decay time (at 5 kHz) relative to the decay time at low frequencies. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDecayTime](EnvironmentalReverb.md))`(`decayTime:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the time taken for the level of reverberation to decay by 60 dB. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDensity](EnvironmentalReverb.md))`(`density:` ` [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)`)` Controls the modal density of the late reverberation decay. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDiffusion](EnvironmentalReverb.md))`(`diffusion:` ` [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)`)` Sets the echo density in the late reverberation decay. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setParameterListener](EnvironmentalReverb.md))`(`listener:` ` [EnvironmentalReverb.OnParameterChangeListener](../android/media/audiofx/EnvironmentalReverb.OnParameterChangeListener.md)!`)` Registers an OnParameterChangeListener interface. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setProperties](EnvironmentalReverb.md))`(`settings:` ` [EnvironmentalReverb.Settings](../android/media/audiofx/EnvironmentalReverb.Settings.md)!`)` Sets the environmental reverb properties. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setReflectionsDelay](EnvironmentalReverb.md))`(`reflectionsDelay:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the delay time for the early reflections. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setReflectionsLevel](EnvironmentalReverb.md))`(`reflectionsLevel:` ` [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)`)` Sets the volume level of the early reflections. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setReverbDelay](EnvironmentalReverb.md))`(`reverbDelay:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the time between the first reflection and the reverberation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setReverbLevel](EnvironmentalReverb.md))`(`reverbLevel:` ` [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)`)` Sets the volume level of the late reverberation. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRoomHFLevel](EnvironmentalReverb.md))`(`roomHF:` ` [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)`)` Sets the volume level at 5 kHz relative to the volume level at low frequencies of the overall reverb effect. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRoomLevel](EnvironmentalReverb.md))`(`room:` ` [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)`)` Sets the master volume level of the environmental reverb effect. |

| Inherited functions ||
|---|---|
| From class [AudioEffect](AudioEffect.md) |---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](AudioEffect.md))`()` <br /> | | [AudioEffect.Descriptor](../android/media/audiofx/AudioEffect.Descriptor.md)! | [getDescriptor](AudioEffect.md))`()` <br /> Get the effect descriptor. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getEnabled](AudioEffect.md))`()` <br /> Returns effect enabled state <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getId](AudioEffect.md))`()` <br /> Returns effect unique identifier. This system wide unique identifier can be used to attach this effect to a MediaPlayer or an AudioTrack when the effect is an auxiliary effect (Reverb) <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasControl](AudioEffect.md))`()` <br /> Checks if this AudioEffect object is controlling the effect engine. <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [AudioEffect.Descriptor](../android/media/audiofx/AudioEffect.Descriptor.md)!>! | [queryEffects](AudioEffect.md))`()` <br /> Query all effects available on the platform. Returns an array of [android.media.audiofx.AudioEffect.Descriptor](../android/media/audiofx/AudioEffect.Descriptor.md) objects <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [release](AudioEffect.md))`()` <br /> Releases the native AudioEffect resources. It is a good practice to release the effect engine when not in use as control can be returned to other applications or the native resources released. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setControlStatusListener](AudioEffect.md))`(`listener:` ` [AudioEffect.OnControlStatusChangeListener](../android/media/audiofx/AudioEffect.OnControlStatusChangeListener.md)!`)` <br /> Sets the listener AudioEffect notifies when the effect engine control is taken or returned. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEnableStatusListener](AudioEffect.md))`(`listener:` ` [AudioEffect.OnEnableStatusChangeListener](../android/media/audiofx/AudioEffect.OnEnableStatusChangeListener.md)!`)` <br /> Sets the listener AudioEffect notifies when the effect engine is enabled or disabled. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [setEnabled](AudioEffect.md))`(`enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Enable or disable the effect. Creating an audio effect does not automatically apply this effect on the audio source. It creates the resources necessary to process this effect but the audio signal is still bypassed through the effect engine. Calling this method will make that the effect is actually applied or not to the audio content being played in the corresponding audio session. <br /> | ||

| Inherited properties ||
|---|---|
| From class [AudioEffect](AudioEffect.md) |------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [UUID](../java.util/UUID.md)! | [EFFECT_TYPE_AEC](AudioEffect.md) <br /> UUID for Acoustic Echo Canceler (AEC) <br /> | | [UUID](../java.util/UUID.md)! | [EFFECT_TYPE_AGC](AudioEffect.md) <br /> UUID for Automatic Gain Control (AGC) <br /> | | [UUID](../java.util/UUID.md)! | [EFFECT_TYPE_BASS_BOOST](AudioEffect.md) <br /> UUID for bass boost effect <br /> | | [UUID](../java.util/UUID.md)! | [EFFECT_TYPE_DYNAMICS_PROCESSING](AudioEffect.md) <br /> UUID for Dynamics Processing <br /> | | [UUID](../java.util/UUID.md)! | [EFFECT_TYPE_ENV_REVERB](AudioEffect.md) <br /> UUID for environmental reverberation effect <br /> | | [UUID](../java.util/UUID.md)! | [EFFECT_TYPE_EQUALIZER](AudioEffect.md) <br /> UUID for equalizer effect <br /> | | [UUID](../java.util/UUID.md) | [EFFECT_TYPE_HAPTIC_GENERATOR](AudioEffect.md) <br /> UUID for Haptic Generator. <br /> | | [UUID](../java.util/UUID.md)! | [EFFECT_TYPE_LOUDNESS_ENHANCER](AudioEffect.md) <br /> UUID for Loudness Enhancer <br /> | | [UUID](../java.util/UUID.md)! | [EFFECT_TYPE_NS](AudioEffect.md) <br /> UUID for Noise Suppressor (NS) <br /> | | [UUID](../java.util/UUID.md)! | [EFFECT_TYPE_PRESET_REVERB](AudioEffect.md) <br /> UUID for preset reverberation effect <br /> | | [UUID](../java.util/UUID.md)! | [EFFECT_TYPE_VIRTUALIZER](AudioEffect.md) <br /> UUID for virtualizer effect <br /> | ||

## Constants

### PARAM_DECAY_HF_RATIO

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PARAM_DECAY_HF_RATIO: Int
```

Decay HF ratio. Parameter ID for [android.media.audiofx.EnvironmentalReverb.OnParameterChangeListener](../android/media/audiofx/EnvironmentalReverb.OnParameterChangeListener.md) 

 Value: 3

### PARAM_DECAY_TIME

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PARAM_DECAY_TIME: Int
```

Decay time. Parameter ID for OnParameterChangeListener 

 Value: 2

### PARAM_DENSITY

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PARAM_DENSITY: Int
```

Density. Parameter ID for OnParameterChangeListener 

 Value: 9

### PARAM_DIFFUSION

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PARAM_DIFFUSION: Int
```

Diffusion. Parameter ID for OnParameterChangeListener 

 Value: 8

### PARAM_REFLECTIONS_DELAY

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PARAM_REFLECTIONS_DELAY: Int
```

Early reflections delay. Parameter ID for OnParameterChangeListener 

 Value: 5

### PARAM_REFLECTIONS_LEVEL

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PARAM_REFLECTIONS_LEVEL: Int
```

Early reflections level. Parameter ID for OnParameterChangeListener 

 Value: 4

### PARAM_REVERB_DELAY

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PARAM_REVERB_DELAY: Int
```

Reverb delay. Parameter ID for OnParameterChangeListener 

 Value: 7

### PARAM_REVERB_LEVEL

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PARAM_REVERB_LEVEL: Int
```

Reverb level. Parameter ID for OnParameterChangeListener 

 Value: 6

### PARAM_ROOM_HF_LEVEL

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PARAM_ROOM_HF_LEVEL: Int
```

Room HF level. Parameter ID for OnParameterChangeListener 

 Value: 1

### PARAM_ROOM_LEVEL

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PARAM_ROOM_LEVEL: Int
```

Room level. Parameter ID for OnParameterChangeListener 

 Value: 0

## Public constructors

### EnvironmentalReverb

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
EnvironmentalReverb(
    priority: Int, 
    audioSession: Int)
```

Class constructor.

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `priority` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the priority level requested by the application for controlling the EnvironmentalReverb engine. As the same engine can be shared by several applications, this parameter indicates how much the requesting application needs control of effect parameters. The normal priority is 0, above normal is a positive number, below normal a negative number. |
| `audioSession` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):system wide unique audio session identifier. If audioSession is not 0, the EnvironmentalReverb will be attached to the MediaPlayer or AudioTrack in the same audio session. Otherwise, the EnvironmentalReverb will apply to the output mix. As the EnvironmentalReverb is an auxiliary effect it is recommended to instantiate it on audio session 0 and to attach it to the MediaPLayer auxiliary output. |

| Exceptions ||
|-------------------------------------------|---|
| `java.lang.IllegalArgumentException` | |
| `java.lang.UnsupportedOperationException` | |
| `java.lang.RuntimeException` | |
| --- | --- |

## Public methods

### getDecayHFRatio

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDecayHFRatio(): Short
```

Gets the ratio of high frequency decay time (at 5 kHz) relative to low frequencies.

| Return ||
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | the decay HF ration. See [setDecayHFRatio(short)](EnvironmentalReverb.md))for units. |

| Exceptions ||
|-------------------------------------------|---|
| `java.lang.IllegalStateException` | |
| `java.lang.IllegalArgumentException` | |
| `java.lang.UnsupportedOperationException` | |
| --- | --- |

### getDecayTime

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDecayTime(): Int
```

Gets the decay time.

| Return ||
|----------------------------------------------------------------------------|---------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the decay time in milliseconds. |

| Exceptions ||
|-------------------------------------------|---|
| `java.lang.IllegalStateException` | |
| `java.lang.IllegalArgumentException` | |
| `java.lang.UnsupportedOperationException` | |
| --- | --- |

### getDensity

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDensity(): Short
```

Gets the density level.

| Return ||
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | the density level. See [setDiffusion(short)](EnvironmentalReverb.md))for units. |

| Exceptions ||
|-------------------------------------------|---|
| `java.lang.IllegalStateException` | |
| `java.lang.IllegalArgumentException` | |
| `java.lang.UnsupportedOperationException` | |
| --- | --- |

### getDiffusion

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDiffusion(): Short
```

Gets diffusion level.

| Return ||
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | the diffusion level. See [setDiffusion(short)](EnvironmentalReverb.md))for units. |

| Exceptions ||
|-------------------------------------------|---|
| `java.lang.IllegalStateException` | |
| `java.lang.IllegalArgumentException` | |
| `java.lang.UnsupportedOperationException` | |
| --- | --- |

### getProperties

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getProperties(): EnvironmentalReverb.Settings!
```

Gets the environmental reverb properties. This method is useful when a snapshot of current reverb settings must be saved by the application.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [EnvironmentalReverb.Settings](../android/media/audiofx/EnvironmentalReverb.Settings.md)! | an EnvironmentalReverb.Settings object containing all current parameters values |

| Exceptions ||
|-------------------------------------------|---|
| `java.lang.IllegalStateException` | |
| `java.lang.IllegalArgumentException` | |
| `java.lang.UnsupportedOperationException` | |
| --- | --- |

### getReflectionsDelay

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getReflectionsDelay(): Int
```

Gets the reflections delay.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the early reflections delay in milliseconds. |

| Exceptions ||
|-------------------------------------------|---|
| `java.lang.IllegalStateException` | |
| `java.lang.IllegalArgumentException` | |
| `java.lang.UnsupportedOperationException` | |
| --- | --- |

### getReflectionsLevel

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getReflectionsLevel(): Short
```

Gets the volume level of the early reflections.

| Return ||
|--------------------------------------------------------------------------------|-------------------------------------------|
| [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | the early reflections level in millibels. |

| Exceptions ||
|-------------------------------------------|---|
| `java.lang.IllegalStateException` | |
| `java.lang.IllegalArgumentException` | |
| `java.lang.UnsupportedOperationException` | |
| --- | --- |

### getReverbDelay

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getReverbDelay(): Int
```

Gets the reverb delay.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the reverb delay in milliseconds. |

| Exceptions ||
|-------------------------------------------|---|
| `java.lang.IllegalStateException` | |
| `java.lang.IllegalArgumentException` | |
| `java.lang.UnsupportedOperationException` | |
| --- | --- |

### getReverbLevel

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getReverbLevel(): Short
```

Gets the reverb level.

| Return ||
|--------------------------------------------------------------------------------|--------------------------------|
| [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | the reverb level in millibels. |

| Exceptions ||
|-------------------------------------------|---|
| `java.lang.IllegalStateException` | |
| `java.lang.IllegalArgumentException` | |
| `java.lang.UnsupportedOperationException` | |
| --- | --- |

### getRoomHFLevel

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRoomHFLevel(): Short
```

Gets the room HF level.

| Return ||
|--------------------------------------------------------------------------------|---------------------------------|
| [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | the room HF level in millibels. |

| Exceptions ||
|-------------------------------------------|---|
| `java.lang.IllegalStateException` | |
| `java.lang.IllegalArgumentException` | |
| `java.lang.UnsupportedOperationException` | |
| --- | --- |

### getRoomLevel

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRoomLevel(): Short
```

Gets the master volume level of the environmental reverb effect.

| Return ||
|--------------------------------------------------------------------------------|------------------------------|
| [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | the room level in millibels. |

| Exceptions ||
|-------------------------------------------|---|
| `java.lang.IllegalStateException` | |
| `java.lang.IllegalArgumentException` | |
| `java.lang.UnsupportedOperationException` | |
| --- | --- |

### setDecayHFRatio

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDecayHFRatio(decayHFRatio: Short): Unit
```

Sets the ratio of high frequency decay time (at 5 kHz) relative to the decay time at low frequencies.

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `decayHFRatio` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html):high frequency decay ratio using a permille scale. The valid range is \[100, 2000\]. A ratio of 1000 indicates that all frequencies decay at the same rate. |

| Exceptions ||
|-------------------------------------------|---|
| `java.lang.IllegalStateException` | |
| `java.lang.IllegalArgumentException` | |
| `java.lang.UnsupportedOperationException` | |
| --- | --- |

### setDecayTime

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDecayTime(decayTime: Int): Unit
```

Sets the time taken for the level of reverberation to decay by 60 dB.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `decayTime` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):decay time in milliseconds. The valid range is \[100, 20000\]. |

| Exceptions ||
|-------------------------------------------|---|
| `java.lang.IllegalStateException` | |
| `java.lang.IllegalArgumentException` | |
| `java.lang.UnsupportedOperationException` | |
| --- | --- |

### setDensity

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDensity(density: Short): Unit
```

Controls the modal density of the late reverberation decay.

The scale should approximately map linearly to the perceived change in reverberation. A lower density creates a hollow sound that is useful for simulating small reverberation spaces such as bathrooms.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `density` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html):density specified using a permille scale. The valid range is \[0, 1000\]. A value of 1000 o/oo indicates a natural sounding reverberation. Values below this level produce a more colored effect. |

| Exceptions ||
|-------------------------------------------|---|
| `java.lang.IllegalStateException` | |
| `java.lang.IllegalArgumentException` | |
| `java.lang.UnsupportedOperationException` | |
| --- | --- |

### setDiffusion

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDiffusion(diffusion: Short): Unit
```

Sets the echo density in the late reverberation decay.

The scale should approximately map linearly to the perceived change in reverberation.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `diffusion` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html):diffusion specified using a permille scale. The diffusion valid range is \[0, 1000\]. A value of 1000 o/oo indicates a smooth reverberation decay. Values below this level give a more*grainy*character. |

| Exceptions ||
|-------------------------------------------|---|
| `java.lang.IllegalStateException` | |
| `java.lang.IllegalArgumentException` | |
| `java.lang.UnsupportedOperationException` | |
| --- | --- |

### setParameterListener

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setParameterListener(listener: EnvironmentalReverb.OnParameterChangeListener!): Unit
```

Registers an OnParameterChangeListener interface.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [EnvironmentalReverb.OnParameterChangeListener](../android/media/audiofx/EnvironmentalReverb.OnParameterChangeListener.md)!:OnParameterChangeListener interface registered |

### setProperties

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setProperties(settings: EnvironmentalReverb.Settings!): Unit
```

Sets the environmental reverb properties. This method is useful when reverb settings have to be applied from a previous backup.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `settings` | [EnvironmentalReverb.Settings](../android/media/audiofx/EnvironmentalReverb.Settings.md)!:a EnvironmentalReverb.Settings object containing the properties to apply |

| Exceptions ||
|-------------------------------------------|---|
| `java.lang.IllegalStateException` | |
| `java.lang.IllegalArgumentException` | |
| `java.lang.UnsupportedOperationException` | |
| --- | --- |

### setReflectionsDelay

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setReflectionsDelay(reflectionsDelay: Int): Unit
```

Sets the delay time for the early reflections.

This method sets the time between when the direct path is heard and when the first reflection is heard.

| Parameters ||
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `reflectionsDelay` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):reflections delay in milliseconds. The valid range is \[0, 300\]. |

| Exceptions ||
|-------------------------------------------|---|
| `java.lang.IllegalStateException` | |
| `java.lang.IllegalArgumentException` | |
| `java.lang.UnsupportedOperationException` | |
| --- | --- |

### setReflectionsLevel

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setReflectionsLevel(reflectionsLevel: Short): Unit
```

Sets the volume level of the early reflections.

This level is combined with the overall room level (set using [setRoomLevel(short)](EnvironmentalReverb.md))).

| Parameters ||
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `reflectionsLevel` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html):reflection level in millibels. The valid range is \[-9000, 1000\]. |

| Exceptions ||
|-------------------------------------------|---|
| `java.lang.IllegalStateException` | |
| `java.lang.IllegalArgumentException` | |
| `java.lang.UnsupportedOperationException` | |
| --- | --- |

### setReverbDelay

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setReverbDelay(reverbDelay: Int): Unit
```

Sets the time between the first reflection and the reverberation.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `reverbDelay` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):reverb delay in milliseconds. The valid range is \[0, 100\]. |

| Exceptions ||
|-------------------------------------------|---|
| `java.lang.IllegalStateException` | |
| `java.lang.IllegalArgumentException` | |
| `java.lang.UnsupportedOperationException` | |
| --- | --- |

### setReverbLevel

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setReverbLevel(reverbLevel: Short): Unit
```

Sets the volume level of the late reverberation.

This level is combined with the overall room level (set using [setRoomLevel(short)](EnvironmentalReverb.md))).

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `reverbLevel` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html):reverb level in millibels. The valid range is \[-9000, 2000\]. |

| Exceptions ||
|-------------------------------------------|---|
| `java.lang.IllegalStateException` | |
| `java.lang.IllegalArgumentException` | |
| `java.lang.UnsupportedOperationException` | |
| --- | --- |

### setRoomHFLevel

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setRoomHFLevel(roomHF: Short): Unit
```

Sets the volume level at 5 kHz relative to the volume level at low frequencies of the overall reverb effect.

This controls a low-pass filter that will reduce the level of the high-frequency.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `roomHF` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html):high frequency attenuation level in millibels. The valid range is \[-9000, 0\]. |

| Exceptions ||
|-------------------------------------------|---|
| `java.lang.IllegalStateException` | |
| `java.lang.IllegalArgumentException` | |
| `java.lang.UnsupportedOperationException` | |
| --- | --- |

### setRoomLevel

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setRoomLevel(room: Short): Unit
```

Sets the master volume level of the environmental reverb effect.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------------|
| `room` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html):room level in millibels. The valid range is \[-9000, 0\]. |

| Exceptions ||
|-------------------------------------------|---|
| `java.lang.IllegalStateException` | |
| `java.lang.IllegalArgumentException` | |
| `java.lang.UnsupportedOperationException` | |
| --- | --- |
