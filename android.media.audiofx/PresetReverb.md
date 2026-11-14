# PresetReverb

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PresetReverb

Kotlin| [Java](PresetReverb.md) 
| --- | --- |

```
open class PresetReverb : AudioEffect
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.media.audiofx.AudioEffect](AudioEffect.md) ||
| | ↳ | [android.media.audiofx.PresetReverb](PresetReverb.md) |

A sound generated within a room travels in many directions. The listener first hears the direct sound from the source itself. Later, he or she hears discrete echoes caused by sound bouncing off nearby walls, the ceiling and the floor. As sound waves arrive after undergoing more and more reflections, individual reflections become indistinguishable and the listener hears continuous reverberation that decays over time. Reverb is vital for modeling a listener's environment. It can be used in music applications to simulate music being played back in various environments, or in games to immerse the listener within the game's environment. The PresetReverb class allows an application to configure the global reverb using a reverb preset. This is primarily used for adding some reverb in a music playback context. Applications requiring control over a more advanced environmental reverb are advised to use the [android.media.audiofx.EnvironmentalReverb](EnvironmentalReverb.md) class.

An application creates a PresetReverb object to instantiate and control a reverb engine in the audio framework.

The methods, parameter types and units exposed by the PresetReverb implementation are directly mapping those defined by the OpenSL ES 1.0.1 Specification (http://www.khronos.org/opensles/) for the SLPresetReverbItf interface. Please refer to this specification for more details.

The PresetReverb is an output mix auxiliary effect and should be created on Audio session 0. In order for a MediaPlayer or AudioTrack to be fed into this effect, they must be explicitely attached to it and a send level must be specified. Use the effect ID returned by getId() method to designate this particular effect when attaching it to the MediaPlayer or AudioTrack.

Creating a reverb on the output mix (audio session 0) requires permission [android.Manifest.permission#MODIFY_AUDIO_SETTINGS](../android/Manifest.permission.md)

See [android.media.audiofx.AudioEffect](AudioEffect.md) class for more details on controlling audio effects.

## Summary

| Nested classes ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [OnParameterChangeListener](../android/media/audiofx/PresetReverb.OnParameterChangeListener.md) The OnParameterChangeListener interface defines a method called by the PresetReverb when a parameter value has changed. |
| open | [Settings](../android/media/audiofx/PresetReverb.Settings.md) The Settings class regroups all preset reverb parameters. |

| Constants ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARAM_PRESET](PresetReverb.md) Preset. |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [PRESET_LARGEHALL](PresetReverb.md) Reverb preset representing a large-sized hall suitable for a full orchestra |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [PRESET_LARGEROOM](PresetReverb.md) Reverb preset representing a large-sized room suitable for live performances |
| --- | --- |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [PRESET_MEDIUMHALL](PresetReverb.md) Reverb preset representing a medium-sized hall |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [PRESET_MEDIUMROOM](PresetReverb.md) Reverb preset representing a medium room with a length of ten meters or less |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [PRESET_NONE](PresetReverb.md) No reverb or reflections |
| --- | --- |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [PRESET_PLATE](PresetReverb.md) Reverb preset representing a synthesis of the traditional plate reverb |
| static [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [PRESET_SMALLROOM](PresetReverb.md) Reverb preset representing a small room less than five meters in length |

| Inherited constants ||
|---|---|
| From class [AudioEffect](AudioEffect.md) |----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_CLOSE_AUDIO_EFFECT_CONTROL_SESSION](AudioEffect.md) <br /> Intent to signal to the effect control application or service that an audio session is closed and that effects should not be applied anymore. The effect control application receiving this intent will delete all effects on this session and store current settings in package specific storage. The calling package name is indicated by the [EXTRA_PACKAGE_NAME](AudioEffect.md) extra and the audio session ID by the [EXTRA_AUDIO_SESSION](AudioEffect.md) extra. Both extras are mandatory. It is good practice for applications to broadcast this intent when music playback stops and/or when exiting to free system resources consumed by audio effect engines. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_DISPLAY_AUDIO_EFFECT_CONTROL_PANEL](AudioEffect.md) <br /> Intent to launch an audio effect control panel UI. The goal of this intent is to enable separate implementations of music/media player applications and audio effect control application or services. This will allow platform vendors to offer more advanced control options for standard effects or control for platform specific effects. The intent carries a number of extras used by the player application to communicate necessary pieces of information to the control panel application. The calling application must use the android.app.Activity#startActivityForResult(Intent, int) method to launch the control panel so that its package name is indicated and used by the control panel application to keep track of changes for this particular application. The [EXTRA_AUDIO_SESSION](AudioEffect.md) extra will indicate an audio session to which the audio effects should be applied. If no audio session is specified, either one of the follownig will happen: - If an audio session was previously opened by the calling application with [ACTION_OPEN_AUDIO_EFFECT_CONTROL_SESSION](AudioEffect.md) intent, the effect changes will be applied to that session. - If no audio session is opened, the changes will be stored in the package specific storage area and applied whenever a new audio session is opened by this application. The [EXTRA_CONTENT_TYPE](AudioEffect.md) extra will help the control panel application customize both the UI layout and the default audio effect settings if none are already stored for the calling application. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_OPEN_AUDIO_EFFECT_CONTROL_SESSION](AudioEffect.md) <br /> Intent to signal to the effect control application or service that a new audio session is opened and requires audio effects to be applied. This is different from [ACTION_DISPLAY_AUDIO_EFFECT_CONTROL_PANEL](AudioEffect.md) in that no UI should be displayed in this case. Music player applications can broadcast this intent before starting playback to make sure that any audio effect settings previously selected by the user are applied. The effect control application receiving this intent will look for previously stored settings for the calling application, create all required audio effects and apply the effect settings to the specified audio session. The calling package name is indicated by the [EXTRA_PACKAGE_NAME](AudioEffect.md) extra and the audio session ID by the [EXTRA_AUDIO_SESSION](AudioEffect.md) extra. Both extras are mandatory. If no stored settings are found for the calling application, default settings for the content type indicated by [EXTRA_CONTENT_TYPE](AudioEffect.md) will be applied. The default settings for a given content type are platform specific. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ALREADY_EXISTS](AudioEffect.md) <br /> Internal operation status. Not returned by any method. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_TYPE_GAME](AudioEffect.md) <br /> Value for [EXTRA_CONTENT_TYPE](AudioEffect.md) when the type of content played is game audio <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_TYPE_MOVIE](AudioEffect.md) <br /> Value for [EXTRA_CONTENT_TYPE](AudioEffect.md) when the type of content played is video or movie <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_TYPE_MUSIC](AudioEffect.md) <br /> Value for [EXTRA_CONTENT_TYPE](AudioEffect.md) when the type of content played is music <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_TYPE_VOICE](AudioEffect.md) <br /> Value for [EXTRA_CONTENT_TYPE](AudioEffect.md) when the type of content played is voice audio <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EFFECT_AUXILIARY](AudioEffect.md) <br /> Effect connection mode is auxiliary. Auxiliary effects must be created on session 0 (global output mix). In order for a MediaPlayer or AudioTrack to be fed into this effect, they must be explicitely attached to this effect and a send level must be specified. Use the effect ID returned by [getId()](AudioEffect.md))to designate this particular effect when attaching it to the MediaPlayer or AudioTrack. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EFFECT_INSERT](AudioEffect.md) <br /> Effect connection mode is insert. Specifying an audio session ID when creating the effect will insert this effect after all players in the same audio session. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EFFECT_POST_PROCESSING](AudioEffect.md) <br /> Effect connection mode is post processing. The audio post processing effects are attached to an audio output stream or device <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EFFECT_PRE_PROCESSING](AudioEffect.md) <br /> Effect connection mode is pre processing. The audio pre processing effects are attached to an audio input stream or device <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR](AudioEffect.md) <br /> Unspecified error. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_BAD_VALUE](AudioEffect.md) <br /> Operation failed due to bad parameter value. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_DEAD_OBJECT](AudioEffect.md) <br /> Operation failed due to dead remote object. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_INVALID_OPERATION](AudioEffect.md) <br /> Operation failed because it was requested in wrong state. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_NO_INIT](AudioEffect.md) <br /> Operation failed due to bad object initialization. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_NO_MEMORY](AudioEffect.md) <br /> Operation failed due to lack of memory. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_AUDIO_SESSION](AudioEffect.md) <br /> Contains the ID of the audio session the effects should be applied to. This extra is for use with [ACTION_DISPLAY_AUDIO_EFFECT_CONTROL_PANEL](AudioEffect.md), [ACTION_OPEN_AUDIO_EFFECT_CONTROL_SESSION](AudioEffect.md) and [ACTION_CLOSE_AUDIO_EFFECT_CONTROL_SESSION](AudioEffect.md) intents. The extra value is of type int and is the audio session ID. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_CONTENT_TYPE](AudioEffect.md) <br /> Indicates which type of content is played by the application. This extra is for use with [ACTION_DISPLAY_AUDIO_EFFECT_CONTROL_PANEL](AudioEffect.md) and [ACTION_OPEN_AUDIO_EFFECT_CONTROL_SESSION](AudioEffect.md) intents. This information is used by the effect control application to customize UI and select appropriate default effect settings. The content type is one of the following: - [CONTENT_TYPE_MUSIC](AudioEffect.md) - [CONTENT_TYPE_MOVIE](AudioEffect.md) - [CONTENT_TYPE_GAME](AudioEffect.md) - [CONTENT_TYPE_VOICE](AudioEffect.md) If omitted, the content type defaults to [CONTENT_TYPE_MUSIC](AudioEffect.md). <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_PACKAGE_NAME](AudioEffect.md) <br /> Contains the package name of the calling application. This extra is for use with [ACTION_OPEN_AUDIO_EFFECT_CONTROL_SESSION](AudioEffect.md) and [ACTION_CLOSE_AUDIO_EFFECT_CONTROL_SESSION](AudioEffect.md) intents. The extra value is a string containing the full package name. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SUCCESS](AudioEffect.md) <br /> Successful operation. <br /> | ||

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PresetReverb](PresetReverb.md))`(`priority:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `audioSession:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Class constructor. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [getPreset](PresetReverb.md))`()` Gets current reverb preset. |
| open [PresetReverb.Settings](../android/media/audiofx/PresetReverb.Settings.md)! | [getProperties](PresetReverb.md))`()` Gets the preset reverb properties. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setParameterListener](PresetReverb.md))`(`listener:` ` [PresetReverb.OnParameterChangeListener](../android/media/audiofx/PresetReverb.OnParameterChangeListener.md)!`)` Registers an OnParameterChangeListener interface. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPreset](PresetReverb.md))`(`preset:` ` [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)`)` Enables a preset on the reverb. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setProperties](PresetReverb.md))`(`settings:` ` [PresetReverb.Settings](../android/media/audiofx/PresetReverb.Settings.md)!`)` Sets the preset reverb properties. |

| Inherited functions ||
|---|---|
| From class [AudioEffect](AudioEffect.md) |---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](AudioEffect.md))`()` <br /> | | [AudioEffect.Descriptor](../android/media/audiofx/AudioEffect.Descriptor.md)! | [getDescriptor](AudioEffect.md))`()` <br /> Get the effect descriptor. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getEnabled](AudioEffect.md))`()` <br /> Returns effect enabled state <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getId](AudioEffect.md))`()` <br /> Returns effect unique identifier. This system wide unique identifier can be used to attach this effect to a MediaPlayer or an AudioTrack when the effect is an auxiliary effect (Reverb) <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasControl](AudioEffect.md))`()` <br /> Checks if this AudioEffect object is controlling the effect engine. <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [AudioEffect.Descriptor](../android/media/audiofx/AudioEffect.Descriptor.md)!>! | [queryEffects](AudioEffect.md))`()` <br /> Query all effects available on the platform. Returns an array of [android.media.audiofx.AudioEffect.Descriptor](../android/media/audiofx/AudioEffect.Descriptor.md) objects <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [release](AudioEffect.md))`()` <br /> Releases the native AudioEffect resources. It is a good practice to release the effect engine when not in use as control can be returned to other applications or the native resources released. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setControlStatusListener](AudioEffect.md))`(`listener:` ` [AudioEffect.OnControlStatusChangeListener](../android/media/audiofx/AudioEffect.OnControlStatusChangeListener.md)!`)` <br /> Sets the listener AudioEffect notifies when the effect engine control is taken or returned. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEnableStatusListener](AudioEffect.md))`(`listener:` ` [AudioEffect.OnEnableStatusChangeListener](../android/media/audiofx/AudioEffect.OnEnableStatusChangeListener.md)!`)` <br /> Sets the listener AudioEffect notifies when the effect engine is enabled or disabled. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [setEnabled](AudioEffect.md))`(`enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Enable or disable the effect. Creating an audio effect does not automatically apply this effect on the audio source. It creates the resources necessary to process this effect but the audio signal is still bypassed through the effect engine. Calling this method will make that the effect is actually applied or not to the audio content being played in the corresponding audio session. <br /> | ||

| Inherited properties ||
|---|---|
| From class [AudioEffect](AudioEffect.md) |------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [UUID](../java.util/UUID.md)! | [EFFECT_TYPE_AEC](AudioEffect.md) <br /> UUID for Acoustic Echo Canceler (AEC) <br /> | | [UUID](../java.util/UUID.md)! | [EFFECT_TYPE_AGC](AudioEffect.md) <br /> UUID for Automatic Gain Control (AGC) <br /> | | [UUID](../java.util/UUID.md)! | [EFFECT_TYPE_BASS_BOOST](AudioEffect.md) <br /> UUID for bass boost effect <br /> | | [UUID](../java.util/UUID.md)! | [EFFECT_TYPE_DYNAMICS_PROCESSING](AudioEffect.md) <br /> UUID for Dynamics Processing <br /> | | [UUID](../java.util/UUID.md)! | [EFFECT_TYPE_ENV_REVERB](AudioEffect.md) <br /> UUID for environmental reverberation effect <br /> | | [UUID](../java.util/UUID.md)! | [EFFECT_TYPE_EQUALIZER](AudioEffect.md) <br /> UUID for equalizer effect <br /> | | [UUID](../java.util/UUID.md) | [EFFECT_TYPE_HAPTIC_GENERATOR](AudioEffect.md) <br /> UUID for Haptic Generator. <br /> | | [UUID](../java.util/UUID.md)! | [EFFECT_TYPE_LOUDNESS_ENHANCER](AudioEffect.md) <br /> UUID for Loudness Enhancer <br /> | | [UUID](../java.util/UUID.md)! | [EFFECT_TYPE_NS](AudioEffect.md) <br /> UUID for Noise Suppressor (NS) <br /> | | [UUID](../java.util/UUID.md)! | [EFFECT_TYPE_PRESET_REVERB](AudioEffect.md) <br /> UUID for preset reverberation effect <br /> | | [UUID](../java.util/UUID.md)! | [EFFECT_TYPE_VIRTUALIZER](AudioEffect.md) <br /> UUID for virtualizer effect <br /> | ||

## Constants

### PARAM_PRESET

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PARAM_PRESET: Int
```

Preset. Parameter ID for [android.media.audiofx.PresetReverb.OnParameterChangeListener](../android/media/audiofx/PresetReverb.OnParameterChangeListener.md) 

 Value: 0

### PRESET_LARGEHALL

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PRESET_LARGEHALL: Short
```

Reverb preset representing a large-sized hall suitable for a full orchestra 

 Value: 5

### PRESET_LARGEROOM

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PRESET_LARGEROOM: Short
```

Reverb preset representing a large-sized room suitable for live performances 

 Value: 3

### PRESET_MEDIUMHALL

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PRESET_MEDIUMHALL: Short
```

Reverb preset representing a medium-sized hall 

 Value: 4

### PRESET_MEDIUMROOM

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PRESET_MEDIUMROOM: Short
```

Reverb preset representing a medium room with a length of ten meters or less 

 Value: 2

### PRESET_NONE

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PRESET_NONE: Short
```

No reverb or reflections 

 Value: 0

### PRESET_PLATE

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PRESET_PLATE: Short
```

Reverb preset representing a synthesis of the traditional plate reverb 

 Value: 6

### PRESET_SMALLROOM

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PRESET_SMALLROOM: Short
```

Reverb preset representing a small room less than five meters in length 

 Value: 1

## Public constructors

### PresetReverb

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PresetReverb(
    priority: Int, 
    audioSession: Int)
```

Class constructor.

| Parameters ||
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `priority` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the priority level requested by the application for controlling the PresetReverb engine. As the same engine can be shared by several applications, this parameter indicates how much the requesting application needs control of effect parameters. The normal priority is 0, above normal is a positive number, below normal a negative number. |
| `audioSession` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):system wide unique audio session identifier. If audioSession is not 0, the PresetReverb will be attached to the MediaPlayer or AudioTrack in the same audio session. Otherwise, the PresetReverb will apply to the output mix. As the PresetReverb is an auxiliary effect it is recommended to instantiate it on audio session 0 and to attach it to the MediaPLayer auxiliary output. |

| Exceptions ||
|-------------------------------------------|---|
| `java.lang.IllegalArgumentException` | |
| `java.lang.UnsupportedOperationException` | |
| `java.lang.RuntimeException` | |
| --- | --- |

## Public methods

### getPreset

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPreset(): Short
```

Gets current reverb preset.

| Return ||
|--------------------------------------------------------------------------------|---------------------------------------|
| [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | the preset that is set at the moment. |

| Exceptions ||
|-------------------------------------------|---|
| `java.lang.IllegalStateException` | |
| `java.lang.IllegalArgumentException` | |
| `java.lang.UnsupportedOperationException` | |
| --- | --- |

### getProperties

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getProperties(): PresetReverb.Settings!
```

Gets the preset reverb properties. This method is useful when a snapshot of current preset reverb settings must be saved by the application.

| Return ||
|----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [PresetReverb.Settings](../android/media/audiofx/PresetReverb.Settings.md)! | a PresetReverb.Settings object containing all current parameters values |

| Exceptions ||
|-------------------------------------------|---|
| `java.lang.IllegalStateException` | |
| `java.lang.IllegalArgumentException` | |
| `java.lang.UnsupportedOperationException` | |
| --- | --- |

### setParameterListener

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setParameterListener(listener: PresetReverb.OnParameterChangeListener!): Unit
```

Registers an OnParameterChangeListener interface.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [PresetReverb.OnParameterChangeListener](../android/media/audiofx/PresetReverb.OnParameterChangeListener.md)!:OnParameterChangeListener interface registered |

### setPreset

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPreset(preset: Short): Unit
```

Enables a preset on the reverb.

The reverb PRESET_NONE disables any reverb from the current output but does not free the resources associated with the reverb. For an application to signal to the implementation to free the resources, it must call the release() method.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `preset` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html):this must be one of the the preset constants defined in this class. e.g. [PRESET_SMALLROOM](PresetReverb.md) |

| Exceptions ||
|-------------------------------------------|---|
| `java.lang.IllegalStateException` | |
| `java.lang.IllegalArgumentException` | |
| `java.lang.UnsupportedOperationException` | |
| --- | --- |

### setProperties

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setProperties(settings: PresetReverb.Settings!): Unit
```

Sets the preset reverb properties. This method is useful when preset reverb settings have to be applied from a previous backup.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `settings` | [PresetReverb.Settings](../android/media/audiofx/PresetReverb.Settings.md)!:a PresetReverb.Settings object containing the properties to apply |

| Exceptions ||
|-------------------------------------------|---|
| `java.lang.IllegalStateException` | |
| `java.lang.IllegalArgumentException` | |
| `java.lang.UnsupportedOperationException` | |
| --- | --- |
