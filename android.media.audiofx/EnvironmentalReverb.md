# EnvironmentalReverb

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EnvironmentalReverb

Kotlin| [Java](https://developer.android.com/reference/android/media/audiofx/EnvironmentalReverb "View this page in Java") 

```
open class EnvironmentalReverb : AudioEffect
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [android.media.audiofx.AudioEffect](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect) ||
| | ↳ | [android.media.audiofx.EnvironmentalReverb](https://developer.android.com/reference/kotlin/android/media/audiofx/EnvironmentalReverb#) |

A sound generated within a room travels in many directions. The listener first hears the direct sound from the source itself. Later, he or she hears discrete echoes caused by sound bouncing off nearby walls, the ceiling and the floor. As sound waves arrive after undergoing more and more reflections, individual reflections become indistinguishable and the listener hears continuous reverberation that decays over time. Reverb is vital for modeling a listener's environment. It can be used in music applications to simulate music being played back in various environments, or in games to immerse the listener within the game's environment. The EnvironmentalReverb class allows an application to control each reverb engine property in a global reverb environment and is more suitable for games. For basic control, more suitable for music applications, it is recommended to use the [android.media.audiofx.PresetReverb](https://developer.android.com/reference/kotlin/android/media/audiofx/PresetReverb) class.

An application creates a EnvironmentalReverb object to instantiate and control a reverb engine in the audio framework.

The methods, parameter types and units exposed by the EnvironmentalReverb implementation are directly mapping those defined by the OpenSL ES 1.0.1 Specification (http://www.khronos.org/opensles/) for the SLEnvironmentalReverbItf interface. Please refer to this specification for more details.

The EnvironmentalReverb is an output mix auxiliary effect and should be created on Audio session 0. In order for a MediaPlayer or AudioTrack to be fed into this effect, they must be explicitely attached to it and a send level must be specified. Use the effect ID returned by getId() method to designate this particular effect when attaching it to the MediaPlayer or AudioTrack.

Creating a reverb on the output mix (audio session 0) requires permission [android.Manifest.permission#MODIFY_AUDIO_SETTINGS](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MODIFY_AUDIO_SETTINGS:kotlin.String)

See [android.media.audiofx.AudioEffect](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect) class for more details on controlling audio effects.

## Summary

| Nested classes ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [OnParameterChangeListener](https://developer.android.com/reference/kotlin/android/media/audiofx/EnvironmentalReverb.OnParameterChangeListener) The OnParameterChangeListener interface defines a method called by the EnvironmentalReverb when a parameter value has changed. |
| open | [Settings](https://developer.android.com/reference/kotlin/android/media/audiofx/EnvironmentalReverb.Settings) The Settings class regroups all environmental reverb parameters. |

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARAM_DECAY_HF_RATIO](https://developer.android.com/reference/kotlin/android/media/audiofx/EnvironmentalReverb#PARAM_DECAY_HF_RATIO:kotlin.Int) Decay HF ratio. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARAM_DECAY_TIME](https://developer.android.com/reference/kotlin/android/media/audiofx/EnvironmentalReverb#PARAM_DECAY_TIME:kotlin.Int) Decay time. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARAM_DENSITY](https://developer.android.com/reference/kotlin/android/media/audiofx/EnvironmentalReverb#PARAM_DENSITY:kotlin.Int) Density. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARAM_DIFFUSION](https://developer.android.com/reference/kotlin/android/media/audiofx/EnvironmentalReverb#PARAM_DIFFUSION:kotlin.Int) Diffusion. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARAM_REFLECTIONS_DELAY](https://developer.android.com/reference/kotlin/android/media/audiofx/EnvironmentalReverb#PARAM_REFLECTIONS_DELAY:kotlin.Int) Early reflections delay. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARAM_REFLECTIONS_LEVEL](https://developer.android.com/reference/kotlin/android/media/audiofx/EnvironmentalReverb#PARAM_REFLECTIONS_LEVEL:kotlin.Int) Early reflections level. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARAM_REVERB_DELAY](https://developer.android.com/reference/kotlin/android/media/audiofx/EnvironmentalReverb#PARAM_REVERB_DELAY:kotlin.Int) Reverb delay. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARAM_REVERB_LEVEL](https://developer.android.com/reference/kotlin/android/media/audiofx/EnvironmentalReverb#PARAM_REVERB_LEVEL:kotlin.Int) Reverb level. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARAM_ROOM_HF_LEVEL](https://developer.android.com/reference/kotlin/android/media/audiofx/EnvironmentalReverb#PARAM_ROOM_HF_LEVEL:kotlin.Int) Room HF level. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARAM_ROOM_LEVEL](https://developer.android.com/reference/kotlin/android/media/audiofx/EnvironmentalReverb#PARAM_ROOM_LEVEL:kotlin.Int) Room level. |

| Inherited constants ||
|---|---|
| From class [AudioEffect](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect) |----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_CLOSE_AUDIO_EFFECT_CONTROL_SESSION](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ACTION_CLOSE_AUDIO_EFFECT_CONTROL_SESSION:kotlin.String) <br /> Intent to signal to the effect control application or service that an audio session is closed and that effects should not be applied anymore. The effect control application receiving this intent will delete all effects on this session and store current settings in package specific storage. The calling package name is indicated by the [EXTRA_PACKAGE_NAME](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EXTRA_PACKAGE_NAME:kotlin.String) extra and the audio session ID by the [EXTRA_AUDIO_SESSION](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EXTRA_AUDIO_SESSION:kotlin.String) extra. Both extras are mandatory. It is good practice for applications to broadcast this intent when music playback stops and/or when exiting to free system resources consumed by audio effect engines. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_DISPLAY_AUDIO_EFFECT_CONTROL_PANEL](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ACTION_DISPLAY_AUDIO_EFFECT_CONTROL_PANEL:kotlin.String) <br /> Intent to launch an audio effect control panel UI. The goal of this intent is to enable separate implementations of music/media player applications and audio effect control application or services. This will allow platform vendors to offer more advanced control options for standard effects or control for platform specific effects. The intent carries a number of extras used by the player application to communicate necessary pieces of information to the control panel application. The calling application must use the android.app.Activity#startActivityForResult(Intent, int) method to launch the control panel so that its package name is indicated and used by the control panel application to keep track of changes for this particular application. The [EXTRA_AUDIO_SESSION](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EXTRA_AUDIO_SESSION:kotlin.String) extra will indicate an audio session to which the audio effects should be applied. If no audio session is specified, either one of the follownig will happen: - If an audio session was previously opened by the calling application with [ACTION_OPEN_AUDIO_EFFECT_CONTROL_SESSION](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ACTION_OPEN_AUDIO_EFFECT_CONTROL_SESSION:kotlin.String) intent, the effect changes will be applied to that session. - If no audio session is opened, the changes will be stored in the package specific storage area and applied whenever a new audio session is opened by this application. The [EXTRA_CONTENT_TYPE](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EXTRA_CONTENT_TYPE:kotlin.String) extra will help the control panel application customize both the UI layout and the default audio effect settings if none are already stored for the calling application. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_OPEN_AUDIO_EFFECT_CONTROL_SESSION](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ACTION_OPEN_AUDIO_EFFECT_CONTROL_SESSION:kotlin.String) <br /> Intent to signal to the effect control application or service that a new audio session is opened and requires audio effects to be applied. This is different from [ACTION_DISPLAY_AUDIO_EFFECT_CONTROL_PANEL](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ACTION_DISPLAY_AUDIO_EFFECT_CONTROL_PANEL:kotlin.String) in that no UI should be displayed in this case. Music player applications can broadcast this intent before starting playback to make sure that any audio effect settings previously selected by the user are applied. The effect control application receiving this intent will look for previously stored settings for the calling application, create all required audio effects and apply the effect settings to the specified audio session. The calling package name is indicated by the [EXTRA_PACKAGE_NAME](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EXTRA_PACKAGE_NAME:kotlin.String) extra and the audio session ID by the [EXTRA_AUDIO_SESSION](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EXTRA_AUDIO_SESSION:kotlin.String) extra. Both extras are mandatory. If no stored settings are found for the calling application, default settings for the content type indicated by [EXTRA_CONTENT_TYPE](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EXTRA_CONTENT_TYPE:kotlin.String) will be applied. The default settings for a given content type are platform specific. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ALREADY_EXISTS](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ALREADY_EXISTS:kotlin.Int) <br /> Internal operation status. Not returned by any method. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_TYPE_GAME](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#CONTENT_TYPE_GAME:kotlin.Int) <br /> Value for [EXTRA_CONTENT_TYPE](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EXTRA_CONTENT_TYPE:kotlin.String) when the type of content played is game audio <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_TYPE_MOVIE](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#CONTENT_TYPE_MOVIE:kotlin.Int) <br /> Value for [EXTRA_CONTENT_TYPE](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EXTRA_CONTENT_TYPE:kotlin.String) when the type of content played is video or movie <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_TYPE_MUSIC](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#CONTENT_TYPE_MUSIC:kotlin.Int) <br /> Value for [EXTRA_CONTENT_TYPE](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EXTRA_CONTENT_TYPE:kotlin.String) when the type of content played is music <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_TYPE_VOICE](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#CONTENT_TYPE_VOICE:kotlin.Int) <br /> Value for [EXTRA_CONTENT_TYPE](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EXTRA_CONTENT_TYPE:kotlin.String) when the type of content played is voice audio <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EFFECT_AUXILIARY](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_AUXILIARY:kotlin.String) <br /> Effect connection mode is auxiliary. Auxiliary effects must be created on session 0 (global output mix). In order for a MediaPlayer or AudioTrack to be fed into this effect, they must be explicitely attached to this effect and a send level must be specified. Use the effect ID returned by [getId()](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#getId())to designate this particular effect when attaching it to the MediaPlayer or AudioTrack. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EFFECT_INSERT](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_INSERT:kotlin.String) <br /> Effect connection mode is insert. Specifying an audio session ID when creating the effect will insert this effect after all players in the same audio session. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EFFECT_POST_PROCESSING](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_POST_PROCESSING:kotlin.String) <br /> Effect connection mode is post processing. The audio post processing effects are attached to an audio output stream or device <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EFFECT_PRE_PROCESSING](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_PRE_PROCESSING:kotlin.String) <br /> Effect connection mode is pre processing. The audio pre processing effects are attached to an audio input stream or device <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ERROR:kotlin.Int) <br /> Unspecified error. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_BAD_VALUE](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ERROR_BAD_VALUE:kotlin.Int) <br /> Operation failed due to bad parameter value. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_DEAD_OBJECT](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ERROR_DEAD_OBJECT:kotlin.Int) <br /> Operation failed due to dead remote object. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_INVALID_OPERATION](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ERROR_INVALID_OPERATION:kotlin.Int) <br /> Operation failed because it was requested in wrong state. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_NO_INIT](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ERROR_NO_INIT:kotlin.Int) <br /> Operation failed due to bad object initialization. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_NO_MEMORY](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ERROR_NO_MEMORY:kotlin.Int) <br /> Operation failed due to lack of memory. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_AUDIO_SESSION](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EXTRA_AUDIO_SESSION:kotlin.String) <br /> Contains the ID of the audio session the effects should be applied to. This extra is for use with [ACTION_DISPLAY_AUDIO_EFFECT_CONTROL_PANEL](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ACTION_DISPLAY_AUDIO_EFFECT_CONTROL_PANEL:kotlin.String), [ACTION_OPEN_AUDIO_EFFECT_CONTROL_SESSION](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ACTION_OPEN_AUDIO_EFFECT_CONTROL_SESSION:kotlin.String) and [ACTION_CLOSE_AUDIO_EFFECT_CONTROL_SESSION](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ACTION_CLOSE_AUDIO_EFFECT_CONTROL_SESSION:kotlin.String) intents. The extra value is of type int and is the audio session ID. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_CONTENT_TYPE](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EXTRA_CONTENT_TYPE:kotlin.String) <br /> Indicates which type of content is played by the application. This extra is for use with [ACTION_DISPLAY_AUDIO_EFFECT_CONTROL_PANEL](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ACTION_DISPLAY_AUDIO_EFFECT_CONTROL_PANEL:kotlin.String) and [ACTION_OPEN_AUDIO_EFFECT_CONTROL_SESSION](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ACTION_OPEN_AUDIO_EFFECT_CONTROL_SESSION:kotlin.String) intents. This information is used by the effect control application to customize UI and select appropriate default effect settings. The content type is one of the following: - [CONTENT_TYPE_MUSIC](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#CONTENT_TYPE_MUSIC:kotlin.Int) - [CONTENT_TYPE_MOVIE](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#CONTENT_TYPE_MOVIE:kotlin.Int) - [CONTENT_TYPE_GAME](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#CONTENT_TYPE_GAME:kotlin.Int) - [CONTENT_TYPE_VOICE](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#CONTENT_TYPE_VOICE:kotlin.Int) If omitted, the content type defaults to [CONTENT_TYPE_MUSIC](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#CONTENT_TYPE_MUSIC:kotlin.Int). <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_PACKAGE_NAME](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EXTRA_PACKAGE_NAME:kotlin.String) <br /> Contains the package name of the calling application. This extra is for use with [ACTION_OPEN_AUDIO_EFFECT_CONTROL_SESSION](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ACTION_OPEN_AUDIO_EFFECT_CONTROL_SESSION:kotlin.String) and [ACTION_CLOSE_AUDIO_EFFECT_CONTROL_SESSION](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ACTION_CLOSE_AUDIO_EFFECT_CONTROL_SESSION:kotlin.String) intents. The extra value is a string containing the full package name. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SUCCESS](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#SUCCESS:kotlin.Int) <br /> Successful operation. <br /> | ||

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [EnvironmentalReverb](https://developer.android.com/reference/kotlin/android/media/audiofx/EnvironmentalReverb#EnvironmentalReverb(kotlin.Int,%20kotlin.Int))`(`priority:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `audioSession:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Class constructor. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [getDecayHFRatio](https://developer.android.com/reference/kotlin/android/media/audiofx/EnvironmentalReverb#getDecayHFRatio())`()` Gets the ratio of high frequency decay time (at 5 kHz) relative to low frequencies. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDecayTime](https://developer.android.com/reference/kotlin/android/media/audiofx/EnvironmentalReverb#getDecayTime())`()` Gets the decay time. |
| open [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [getDensity](https://developer.android.com/reference/kotlin/android/media/audiofx/EnvironmentalReverb#getDensity())`()` Gets the density level. |
| open [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [getDiffusion](https://developer.android.com/reference/kotlin/android/media/audiofx/EnvironmentalReverb#getDiffusion())`()` Gets diffusion level. |
| open [EnvironmentalReverb.Settings](https://developer.android.com/reference/kotlin/android/media/audiofx/EnvironmentalReverb.Settings)! | [getProperties](https://developer.android.com/reference/kotlin/android/media/audiofx/EnvironmentalReverb#getProperties())`()` Gets the environmental reverb properties. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getReflectionsDelay](https://developer.android.com/reference/kotlin/android/media/audiofx/EnvironmentalReverb#getReflectionsDelay())`()` Gets the reflections delay. |
| open [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [getReflectionsLevel](https://developer.android.com/reference/kotlin/android/media/audiofx/EnvironmentalReverb#getReflectionsLevel())`()` Gets the volume level of the early reflections. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getReverbDelay](https://developer.android.com/reference/kotlin/android/media/audiofx/EnvironmentalReverb#getReverbDelay())`()` Gets the reverb delay. |
| open [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [getReverbLevel](https://developer.android.com/reference/kotlin/android/media/audiofx/EnvironmentalReverb#getReverbLevel())`()` Gets the reverb level. |
| open [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [getRoomHFLevel](https://developer.android.com/reference/kotlin/android/media/audiofx/EnvironmentalReverb#getRoomHFLevel())`()` Gets the room HF level. |
| open [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [getRoomLevel](https://developer.android.com/reference/kotlin/android/media/audiofx/EnvironmentalReverb#getRoomLevel())`()` Gets the master volume level of the environmental reverb effect. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDecayHFRatio](https://developer.android.com/reference/kotlin/android/media/audiofx/EnvironmentalReverb#setDecayHFRatio(kotlin.Short))`(`decayHFRatio:` ` [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)`)` Sets the ratio of high frequency decay time (at 5 kHz) relative to the decay time at low frequencies. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDecayTime](https://developer.android.com/reference/kotlin/android/media/audiofx/EnvironmentalReverb#setDecayTime(kotlin.Int))`(`decayTime:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the time taken for the level of reverberation to decay by 60 dB. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDensity](https://developer.android.com/reference/kotlin/android/media/audiofx/EnvironmentalReverb#setDensity(kotlin.Short))`(`density:` ` [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)`)` Controls the modal density of the late reverberation decay. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDiffusion](https://developer.android.com/reference/kotlin/android/media/audiofx/EnvironmentalReverb#setDiffusion(kotlin.Short))`(`diffusion:` ` [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)`)` Sets the echo density in the late reverberation decay. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setParameterListener](https://developer.android.com/reference/kotlin/android/media/audiofx/EnvironmentalReverb#setParameterListener(android.media.audiofx.EnvironmentalReverb.OnParameterChangeListener))`(`listener:` ` [EnvironmentalReverb.OnParameterChangeListener](https://developer.android.com/reference/kotlin/android/media/audiofx/EnvironmentalReverb.OnParameterChangeListener)!`)` Registers an OnParameterChangeListener interface. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setProperties](https://developer.android.com/reference/kotlin/android/media/audiofx/EnvironmentalReverb#setProperties(android.media.audiofx.EnvironmentalReverb.Settings))`(`settings:` ` [EnvironmentalReverb.Settings](https://developer.android.com/reference/kotlin/android/media/audiofx/EnvironmentalReverb.Settings)!`)` Sets the environmental reverb properties. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setReflectionsDelay](https://developer.android.com/reference/kotlin/android/media/audiofx/EnvironmentalReverb#setReflectionsDelay(kotlin.Int))`(`reflectionsDelay:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the delay time for the early reflections. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setReflectionsLevel](https://developer.android.com/reference/kotlin/android/media/audiofx/EnvironmentalReverb#setReflectionsLevel(kotlin.Short))`(`reflectionsLevel:` ` [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)`)` Sets the volume level of the early reflections. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setReverbDelay](https://developer.android.com/reference/kotlin/android/media/audiofx/EnvironmentalReverb#setReverbDelay(kotlin.Int))`(`reverbDelay:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the time between the first reflection and the reverberation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setReverbLevel](https://developer.android.com/reference/kotlin/android/media/audiofx/EnvironmentalReverb#setReverbLevel(kotlin.Short))`(`reverbLevel:` ` [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)`)` Sets the volume level of the late reverberation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRoomHFLevel](https://developer.android.com/reference/kotlin/android/media/audiofx/EnvironmentalReverb#setRoomHFLevel(kotlin.Short))`(`roomHF:` ` [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)`)` Sets the volume level at 5 kHz relative to the volume level at low frequencies of the overall reverb effect. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRoomLevel](https://developer.android.com/reference/kotlin/android/media/audiofx/EnvironmentalReverb#setRoomLevel(kotlin.Short))`(`room:` ` [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)`)` Sets the master volume level of the environmental reverb effect. |

| Inherited functions ||
|---|---|
| From class [AudioEffect](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect) |---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#finalize())`()` <br /> | | [AudioEffect.Descriptor](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect.Descriptor)! | [getDescriptor](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#getDescriptor())`()` <br /> Get the effect descriptor. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getEnabled](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#getEnabled())`()` <br /> Returns effect enabled state <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getId](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#getId())`()` <br /> Returns effect unique identifier. This system wide unique identifier can be used to attach this effect to a MediaPlayer or an AudioTrack when the effect is an auxiliary effect (Reverb) <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasControl](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#hasControl())`()` <br /> Checks if this AudioEffect object is controlling the effect engine. <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [AudioEffect.Descriptor](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect.Descriptor)!>! | [queryEffects](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#queryEffects())`()` <br /> Query all effects available on the platform. Returns an array of [android.media.audiofx.AudioEffect.Descriptor](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect.Descriptor) objects <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [release](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#release())`()` <br /> Releases the native AudioEffect resources. It is a good practice to release the effect engine when not in use as control can be returned to other applications or the native resources released. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setControlStatusListener](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#setControlStatusListener(android.media.audiofx.AudioEffect.OnControlStatusChangeListener))`(`listener:` ` [AudioEffect.OnControlStatusChangeListener](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect.OnControlStatusChangeListener)!`)` <br /> Sets the listener AudioEffect notifies when the effect engine control is taken or returned. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEnableStatusListener](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#setEnableStatusListener(android.media.audiofx.AudioEffect.OnEnableStatusChangeListener))`(`listener:` ` [AudioEffect.OnEnableStatusChangeListener](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect.OnEnableStatusChangeListener)!`)` <br /> Sets the listener AudioEffect notifies when the effect engine is enabled or disabled. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [setEnabled](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#setEnabled(kotlin.Boolean))`(`enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Enable or disable the effect. Creating an audio effect does not automatically apply this effect on the audio source. It creates the resources necessary to process this effect but the audio signal is still bypassed through the effect engine. Calling this method will make that the effect is actually applied or not to the audio content being played in the corresponding audio session. <br /> | ||

| Inherited properties ||
|---|---|
| From class [AudioEffect](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect) |------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#)! | [EFFECT_TYPE_AEC](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_TYPE_AEC:java.util.UUID) <br /> UUID for Acoustic Echo Canceler (AEC) <br /> | | [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#)! | [EFFECT_TYPE_AGC](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_TYPE_AGC:java.util.UUID) <br /> UUID for Automatic Gain Control (AGC) <br /> | | [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#)! | [EFFECT_TYPE_BASS_BOOST](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_TYPE_BASS_BOOST:java.util.UUID) <br /> UUID for bass boost effect <br /> | | [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#)! | [EFFECT_TYPE_DYNAMICS_PROCESSING](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_TYPE_DYNAMICS_PROCESSING:java.util.UUID) <br /> UUID for Dynamics Processing <br /> | | [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#)! | [EFFECT_TYPE_ENV_REVERB](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_TYPE_ENV_REVERB:java.util.UUID) <br /> UUID for environmental reverberation effect <br /> | | [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#)! | [EFFECT_TYPE_EQUALIZER](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_TYPE_EQUALIZER:java.util.UUID) <br /> UUID for equalizer effect <br /> | | [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#) | [EFFECT_TYPE_HAPTIC_GENERATOR](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_TYPE_HAPTIC_GENERATOR:java.util.UUID) <br /> UUID for Haptic Generator. <br /> | | [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#)! | [EFFECT_TYPE_LOUDNESS_ENHANCER](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_TYPE_LOUDNESS_ENHANCER:java.util.UUID) <br /> UUID for Loudness Enhancer <br /> | | [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#)! | [EFFECT_TYPE_NS](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_TYPE_NS:java.util.UUID) <br /> UUID for Noise Suppressor (NS) <br /> | | [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#)! | [EFFECT_TYPE_PRESET_REVERB](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_TYPE_PRESET_REVERB:java.util.UUID) <br /> UUID for preset reverberation effect <br /> | | [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#)! | [EFFECT_TYPE_VIRTUALIZER](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_TYPE_VIRTUALIZER:java.util.UUID) <br /> UUID for virtualizer effect <br /> | ||

## Constants

### PARAM_DECAY_HF_RATIO

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PARAM_DECAY_HF_RATIO: Int
```

Decay HF ratio. Parameter ID for [android.media.audiofx.EnvironmentalReverb.OnParameterChangeListener](https://developer.android.com/reference/kotlin/android/media/audiofx/EnvironmentalReverb.OnParameterChangeListener) 

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

## Public methods

### getDecayHFRatio

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDecayHFRatio(): Short
```

Gets the ratio of high frequency decay time (at 5 kHz) relative to low frequencies.

| Return ||
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | the decay HF ration. See [setDecayHFRatio(short)](https://developer.android.com/reference/kotlin/android/media/audiofx/EnvironmentalReverb#setDecayHFRatio(kotlin.Short))for units. |

| Exceptions ||
|-------------------------------------------|---|
| `java.lang.IllegalStateException` | |
| `java.lang.IllegalArgumentException` | |
| `java.lang.UnsupportedOperationException` | |

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

### getDensity

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDensity(): Short
```

Gets the density level.

| Return ||
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | the density level. See [setDiffusion(short)](https://developer.android.com/reference/kotlin/android/media/audiofx/EnvironmentalReverb#setDiffusion(kotlin.Short))for units. |

| Exceptions ||
|-------------------------------------------|---|
| `java.lang.IllegalStateException` | |
| `java.lang.IllegalArgumentException` | |
| `java.lang.UnsupportedOperationException` | |

### getDiffusion

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDiffusion(): Short
```

Gets diffusion level.

| Return ||
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | the diffusion level. See [setDiffusion(short)](https://developer.android.com/reference/kotlin/android/media/audiofx/EnvironmentalReverb#setDiffusion(kotlin.Short))for units. |

| Exceptions ||
|-------------------------------------------|---|
| `java.lang.IllegalStateException` | |
| `java.lang.IllegalArgumentException` | |
| `java.lang.UnsupportedOperationException` | |

### getProperties

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getProperties(): EnvironmentalReverb.Settings!
```

Gets the environmental reverb properties. This method is useful when a snapshot of current reverb settings must be saved by the application.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [EnvironmentalReverb.Settings](https://developer.android.com/reference/kotlin/android/media/audiofx/EnvironmentalReverb.Settings)! | an EnvironmentalReverb.Settings object containing all current parameters values |

| Exceptions ||
|-------------------------------------------|---|
| `java.lang.IllegalStateException` | |
| `java.lang.IllegalArgumentException` | |
| `java.lang.UnsupportedOperationException` | |

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

### setParameterListener

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setParameterListener(listener: EnvironmentalReverb.OnParameterChangeListener!): Unit
```

Registers an OnParameterChangeListener interface.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [EnvironmentalReverb.OnParameterChangeListener](https://developer.android.com/reference/kotlin/android/media/audiofx/EnvironmentalReverb.OnParameterChangeListener)!:OnParameterChangeListener interface registered |

### setProperties

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setProperties(settings: EnvironmentalReverb.Settings!): Unit
```

Sets the environmental reverb properties. This method is useful when reverb settings have to be applied from a previous backup.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `settings` | [EnvironmentalReverb.Settings](https://developer.android.com/reference/kotlin/android/media/audiofx/EnvironmentalReverb.Settings)!:a EnvironmentalReverb.Settings object containing the properties to apply |

| Exceptions ||
|-------------------------------------------|---|
| `java.lang.IllegalStateException` | |
| `java.lang.IllegalArgumentException` | |
| `java.lang.UnsupportedOperationException` | |

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

### setReflectionsLevel

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setReflectionsLevel(reflectionsLevel: Short): Unit
```

Sets the volume level of the early reflections.

This level is combined with the overall room level (set using [setRoomLevel(short)](https://developer.android.com/reference/kotlin/android/media/audiofx/EnvironmentalReverb#setRoomLevel(kotlin.Short))).

| Parameters ||
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `reflectionsLevel` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html):reflection level in millibels. The valid range is \[-9000, 1000\]. |

| Exceptions ||
|-------------------------------------------|---|
| `java.lang.IllegalStateException` | |
| `java.lang.IllegalArgumentException` | |
| `java.lang.UnsupportedOperationException` | |

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

### setReverbLevel

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setReverbLevel(reverbLevel: Short): Unit
```

Sets the volume level of the late reverberation.

This level is combined with the overall room level (set using [setRoomLevel(short)](https://developer.android.com/reference/kotlin/android/media/audiofx/EnvironmentalReverb#setRoomLevel(kotlin.Short))).

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `reverbLevel` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html):reverb level in millibels. The valid range is \[-9000, 2000\]. |

| Exceptions ||
|-------------------------------------------|---|
| `java.lang.IllegalStateException` | |
| `java.lang.IllegalArgumentException` | |
| `java.lang.UnsupportedOperationException` | |

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
