# BassBoost

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BassBoost

Kotlin| [Java](BassBoost.md) 
| --- | --- |

```
open class BassBoost : AudioEffect
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.media.audiofx.AudioEffect](AudioEffect.md) ||
| | ↳ | [android.media.audiofx.BassBoost](BassBoost.md) |

Bass boost is an audio effect to boost or amplify low frequencies of the sound. It is comparable to a simple equalizer but limited to one band amplification in the low frequency range.

An application creates a BassBoost object to instantiate and control a bass boost engine in the audio framework.

The methods, parameter types and units exposed by the BassBoost implementation are directly mapping those defined by the OpenSL ES 1.0.1 Specification (http://www.khronos.org/opensles/) for the SLBassBoostItf interface. Please refer to this specification for more details.

To attach the BassBoost to a particular AudioTrack or MediaPlayer, specify the audio session ID of this AudioTrack or MediaPlayer when constructing the BassBoost.

NOTE: attaching a BassBoost to the global audio output mix by use of session 0 is deprecated.

See [android.media.MediaPlayer#getAudioSessionId()](../android.media/MediaPlayer.md))for details on audio sessions.

See [android.media.audiofx.AudioEffect](AudioEffect.md) class for more details on controlling audio effects.

## Summary

| Nested classes ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [OnParameterChangeListener](../android/media/audiofx/BassBoost.OnParameterChangeListener.md) The OnParameterChangeListener interface defines a method called by the BassBoost when a parameter value has changed. |
| open | [Settings](../android/media/audiofx/BassBoost.Settings.md) The Settings class regroups all bass boost parameters. |

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARAM_STRENGTH](BassBoost.md) Bass boost effect strength. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARAM_STRENGTH_SUPPORTED](BassBoost.md) Is strength parameter supported by bass boost engine. |

| Inherited constants ||
|---|---|
| From class [AudioEffect](AudioEffect.md) |----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_CLOSE_AUDIO_EFFECT_CONTROL_SESSION](AudioEffect.md) <br /> Intent to signal to the effect control application or service that an audio session is closed and that effects should not be applied anymore. The effect control application receiving this intent will delete all effects on this session and store current settings in package specific storage. The calling package name is indicated by the [EXTRA_PACKAGE_NAME](AudioEffect.md) extra and the audio session ID by the [EXTRA_AUDIO_SESSION](AudioEffect.md) extra. Both extras are mandatory. It is good practice for applications to broadcast this intent when music playback stops and/or when exiting to free system resources consumed by audio effect engines. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_DISPLAY_AUDIO_EFFECT_CONTROL_PANEL](AudioEffect.md) <br /> Intent to launch an audio effect control panel UI. The goal of this intent is to enable separate implementations of music/media player applications and audio effect control application or services. This will allow platform vendors to offer more advanced control options for standard effects or control for platform specific effects. The intent carries a number of extras used by the player application to communicate necessary pieces of information to the control panel application. The calling application must use the android.app.Activity#startActivityForResult(Intent, int) method to launch the control panel so that its package name is indicated and used by the control panel application to keep track of changes for this particular application. The [EXTRA_AUDIO_SESSION](AudioEffect.md) extra will indicate an audio session to which the audio effects should be applied. If no audio session is specified, either one of the follownig will happen: - If an audio session was previously opened by the calling application with [ACTION_OPEN_AUDIO_EFFECT_CONTROL_SESSION](AudioEffect.md) intent, the effect changes will be applied to that session. - If no audio session is opened, the changes will be stored in the package specific storage area and applied whenever a new audio session is opened by this application. The [EXTRA_CONTENT_TYPE](AudioEffect.md) extra will help the control panel application customize both the UI layout and the default audio effect settings if none are already stored for the calling application. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_OPEN_AUDIO_EFFECT_CONTROL_SESSION](AudioEffect.md) <br /> Intent to signal to the effect control application or service that a new audio session is opened and requires audio effects to be applied. This is different from [ACTION_DISPLAY_AUDIO_EFFECT_CONTROL_PANEL](AudioEffect.md) in that no UI should be displayed in this case. Music player applications can broadcast this intent before starting playback to make sure that any audio effect settings previously selected by the user are applied. The effect control application receiving this intent will look for previously stored settings for the calling application, create all required audio effects and apply the effect settings to the specified audio session. The calling package name is indicated by the [EXTRA_PACKAGE_NAME](AudioEffect.md) extra and the audio session ID by the [EXTRA_AUDIO_SESSION](AudioEffect.md) extra. Both extras are mandatory. If no stored settings are found for the calling application, default settings for the content type indicated by [EXTRA_CONTENT_TYPE](AudioEffect.md) will be applied. The default settings for a given content type are platform specific. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ALREADY_EXISTS](AudioEffect.md) <br /> Internal operation status. Not returned by any method. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_TYPE_GAME](AudioEffect.md) <br /> Value for [EXTRA_CONTENT_TYPE](AudioEffect.md) when the type of content played is game audio <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_TYPE_MOVIE](AudioEffect.md) <br /> Value for [EXTRA_CONTENT_TYPE](AudioEffect.md) when the type of content played is video or movie <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_TYPE_MUSIC](AudioEffect.md) <br /> Value for [EXTRA_CONTENT_TYPE](AudioEffect.md) when the type of content played is music <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_TYPE_VOICE](AudioEffect.md) <br /> Value for [EXTRA_CONTENT_TYPE](AudioEffect.md) when the type of content played is voice audio <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EFFECT_AUXILIARY](AudioEffect.md) <br /> Effect connection mode is auxiliary. Auxiliary effects must be created on session 0 (global output mix). In order for a MediaPlayer or AudioTrack to be fed into this effect, they must be explicitely attached to this effect and a send level must be specified. Use the effect ID returned by [getId()](AudioEffect.md))to designate this particular effect when attaching it to the MediaPlayer or AudioTrack. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EFFECT_INSERT](AudioEffect.md) <br /> Effect connection mode is insert. Specifying an audio session ID when creating the effect will insert this effect after all players in the same audio session. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EFFECT_POST_PROCESSING](AudioEffect.md) <br /> Effect connection mode is post processing. The audio post processing effects are attached to an audio output stream or device <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EFFECT_PRE_PROCESSING](AudioEffect.md) <br /> Effect connection mode is pre processing. The audio pre processing effects are attached to an audio input stream or device <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR](AudioEffect.md) <br /> Unspecified error. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_BAD_VALUE](AudioEffect.md) <br /> Operation failed due to bad parameter value. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_DEAD_OBJECT](AudioEffect.md) <br /> Operation failed due to dead remote object. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_INVALID_OPERATION](AudioEffect.md) <br /> Operation failed because it was requested in wrong state. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_NO_INIT](AudioEffect.md) <br /> Operation failed due to bad object initialization. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_NO_MEMORY](AudioEffect.md) <br /> Operation failed due to lack of memory. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_AUDIO_SESSION](AudioEffect.md) <br /> Contains the ID of the audio session the effects should be applied to. This extra is for use with [ACTION_DISPLAY_AUDIO_EFFECT_CONTROL_PANEL](AudioEffect.md), [ACTION_OPEN_AUDIO_EFFECT_CONTROL_SESSION](AudioEffect.md) and [ACTION_CLOSE_AUDIO_EFFECT_CONTROL_SESSION](AudioEffect.md) intents. The extra value is of type int and is the audio session ID. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_CONTENT_TYPE](AudioEffect.md) <br /> Indicates which type of content is played by the application. This extra is for use with [ACTION_DISPLAY_AUDIO_EFFECT_CONTROL_PANEL](AudioEffect.md) and [ACTION_OPEN_AUDIO_EFFECT_CONTROL_SESSION](AudioEffect.md) intents. This information is used by the effect control application to customize UI and select appropriate default effect settings. The content type is one of the following: - [CONTENT_TYPE_MUSIC](AudioEffect.md) - [CONTENT_TYPE_MOVIE](AudioEffect.md) - [CONTENT_TYPE_GAME](AudioEffect.md) - [CONTENT_TYPE_VOICE](AudioEffect.md) If omitted, the content type defaults to [CONTENT_TYPE_MUSIC](AudioEffect.md). <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_PACKAGE_NAME](AudioEffect.md) <br /> Contains the package name of the calling application. This extra is for use with [ACTION_OPEN_AUDIO_EFFECT_CONTROL_SESSION](AudioEffect.md) and [ACTION_CLOSE_AUDIO_EFFECT_CONTROL_SESSION](AudioEffect.md) intents. The extra value is a string containing the full package name. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SUCCESS](AudioEffect.md) <br /> Successful operation. <br /> | ||

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [BassBoost](BassBoost.md))`(`priority:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `audioSession:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Class constructor. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [BassBoost.Settings](../android/media/audiofx/BassBoost.Settings.md)! | [getProperties](BassBoost.md))`()` Gets the bass boost properties. |
| open [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [getRoundedStrength](BassBoost.md))`()` Gets the current strength of the effect. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getStrengthSupported](BassBoost.md))`()` Indicates whether setting strength is supported. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setParameterListener](BassBoost.md))`(`listener:` ` [BassBoost.OnParameterChangeListener](../android/media/audiofx/BassBoost.OnParameterChangeListener.md)!`)` Registers an OnParameterChangeListener interface. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setProperties](BassBoost.md))`(`settings:` ` [BassBoost.Settings](../android/media/audiofx/BassBoost.Settings.md)!`)` Sets the bass boost properties. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStrength](BassBoost.md))`(`strength:` ` [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)`)` Sets the strength of the bass boost effect. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [AudioEffect](AudioEffect.md) |---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](AudioEffect.md))`()` <br /> | | [AudioEffect.Descriptor](../android/media/audiofx/AudioEffect.Descriptor.md)! | [getDescriptor](AudioEffect.md))`()` <br /> Get the effect descriptor. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getEnabled](AudioEffect.md))`()` <br /> Returns effect enabled state <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getId](AudioEffect.md))`()` <br /> Returns effect unique identifier. This system wide unique identifier can be used to attach this effect to a MediaPlayer or an AudioTrack when the effect is an auxiliary effect (Reverb) <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasControl](AudioEffect.md))`()` <br /> Checks if this AudioEffect object is controlling the effect engine. <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [AudioEffect.Descriptor](../android/media/audiofx/AudioEffect.Descriptor.md)!>! | [queryEffects](AudioEffect.md))`()` <br /> Query all effects available on the platform. Returns an array of [android.media.audiofx.AudioEffect.Descriptor](../android/media/audiofx/AudioEffect.Descriptor.md) objects <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [release](AudioEffect.md))`()` <br /> Releases the native AudioEffect resources. It is a good practice to release the effect engine when not in use as control can be returned to other applications or the native resources released. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setControlStatusListener](AudioEffect.md))`(`listener:` ` [AudioEffect.OnControlStatusChangeListener](../android/media/audiofx/AudioEffect.OnControlStatusChangeListener.md)!`)` <br /> Sets the listener AudioEffect notifies when the effect engine control is taken or returned. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEnableStatusListener](AudioEffect.md))`(`listener:` ` [AudioEffect.OnEnableStatusChangeListener](../android/media/audiofx/AudioEffect.OnEnableStatusChangeListener.md)!`)` <br /> Sets the listener AudioEffect notifies when the effect engine is enabled or disabled. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [setEnabled](AudioEffect.md))`(`enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Enable or disable the effect. Creating an audio effect does not automatically apply this effect on the audio source. It creates the resources necessary to process this effect but the audio signal is still bypassed through the effect engine. Calling this method will make that the effect is actually applied or not to the audio content being played in the corresponding audio session. <br /> | ||

| Inherited properties ||
|---|---|
| From class [AudioEffect](AudioEffect.md) |------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [UUID](../java.util/UUID.md)! | [EFFECT_TYPE_AEC](AudioEffect.md) <br /> UUID for Acoustic Echo Canceler (AEC) <br /> | | [UUID](../java.util/UUID.md)! | [EFFECT_TYPE_AGC](AudioEffect.md) <br /> UUID for Automatic Gain Control (AGC) <br /> | | [UUID](../java.util/UUID.md)! | [EFFECT_TYPE_BASS_BOOST](AudioEffect.md) <br /> UUID for bass boost effect <br /> | | [UUID](../java.util/UUID.md)! | [EFFECT_TYPE_DYNAMICS_PROCESSING](AudioEffect.md) <br /> UUID for Dynamics Processing <br /> | | [UUID](../java.util/UUID.md)! | [EFFECT_TYPE_ENV_REVERB](AudioEffect.md) <br /> UUID for environmental reverberation effect <br /> | | [UUID](../java.util/UUID.md)! | [EFFECT_TYPE_EQUALIZER](AudioEffect.md) <br /> UUID for equalizer effect <br /> | | [UUID](../java.util/UUID.md) | [EFFECT_TYPE_HAPTIC_GENERATOR](AudioEffect.md) <br /> UUID for Haptic Generator. <br /> | | [UUID](../java.util/UUID.md)! | [EFFECT_TYPE_LOUDNESS_ENHANCER](AudioEffect.md) <br /> UUID for Loudness Enhancer <br /> | | [UUID](../java.util/UUID.md)! | [EFFECT_TYPE_NS](AudioEffect.md) <br /> UUID for Noise Suppressor (NS) <br /> | | [UUID](../java.util/UUID.md)! | [EFFECT_TYPE_PRESET_REVERB](AudioEffect.md) <br /> UUID for preset reverberation effect <br /> | | [UUID](../java.util/UUID.md)! | [EFFECT_TYPE_VIRTUALIZER](AudioEffect.md) <br /> UUID for virtualizer effect <br /> | ||

## Constants

### PARAM_STRENGTH

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PARAM_STRENGTH: Int
```

Bass boost effect strength. Parameter ID for [android.media.audiofx.BassBoost.OnParameterChangeListener](../android/media/audiofx/BassBoost.OnParameterChangeListener.md) 

 Value: 1

### PARAM_STRENGTH_SUPPORTED

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PARAM_STRENGTH_SUPPORTED: Int
```

Is strength parameter supported by bass boost engine. Parameter ID for getParameter(). 

 Value: 0

## Public constructors

### BassBoost

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BassBoost(
    priority: Int, 
    audioSession: Int)
```

Class constructor.

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `priority` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the priority level requested by the application for controlling the BassBoost engine. As the same engine can be shared by several applications, this parameter indicates how much the requesting application needs control of effect parameters. The normal priority is 0, above normal is a positive number, below normal a negative number. |
| `audioSession` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):system wide unique audio session identifier. The BassBoost will be attached to the MediaPlayer or AudioTrack in the same audio session. |

| Exceptions ||
|-------------------------------------------|---|
| `java.lang.IllegalStateException` | |
| `java.lang.IllegalArgumentException` | |
| `java.lang.UnsupportedOperationException` | |
| --- | --- |
| `java.lang.RuntimeException` | |

## Public methods

### getProperties

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getProperties(): BassBoost.Settings!
```

Gets the bass boost properties. This method is useful when a snapshot of current bass boost settings must be saved by the application.

| Return ||
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [BassBoost.Settings](../android/media/audiofx/BassBoost.Settings.md)! | a BassBoost.Settings object containing all current parameters values |

| Exceptions ||
|-------------------------------------------|---|
| `java.lang.IllegalStateException` | |
| `java.lang.IllegalArgumentException` | |
| `java.lang.UnsupportedOperationException` | |
| --- | --- |

### getRoundedStrength

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRoundedStrength(): Short
```

Gets the current strength of the effect.

| Return ||
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | the strength of the effect. The valid range for strength is \[0, 1000\], where 0 per mille designates the mildest effect and 1000 per mille the strongest |

| Exceptions ||
|-------------------------------------------|---|
| `java.lang.IllegalStateException` | |
| `java.lang.IllegalArgumentException` | |
| `java.lang.UnsupportedOperationException` | |
| --- | --- |

### getStrengthSupported

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getStrengthSupported(): Boolean
```

Indicates whether setting strength is supported. If this method returns false, only one strength is supported and the setStrength() method always rounds to that value.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true is strength parameter is supported, false otherwise |

### setParameterListener

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setParameterListener(listener: BassBoost.OnParameterChangeListener!): Unit
```

Registers an OnParameterChangeListener interface.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [BassBoost.OnParameterChangeListener](../android/media/audiofx/BassBoost.OnParameterChangeListener.md)!:OnParameterChangeListener interface registered |

### setProperties

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setProperties(settings: BassBoost.Settings!): Unit
```

Sets the bass boost properties. This method is useful when bass boost settings have to be applied from a previous backup.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `settings` | [BassBoost.Settings](../android/media/audiofx/BassBoost.Settings.md)!:a BassBoost.Settings object containing the properties to apply |

| Exceptions ||
|-------------------------------------------|---|
| `java.lang.IllegalStateException` | |
| `java.lang.IllegalArgumentException` | |
| `java.lang.UnsupportedOperationException` | |
| --- | --- |

### setStrength

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setStrength(strength: Short): Unit
```

Sets the strength of the bass boost effect. If the implementation does not support per mille accuracy for setting the strength, it is allowed to round the given strength to the nearest supported value. You can use the [getRoundedStrength()](BassBoost.md))method to query the (possibly rounded) value that was actually set.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `strength` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html):strength of the effect. The valid range for strength strength is \[0, 1000\], where 0 per mille designates the mildest effect and 1000 per mille designates the strongest. |

| Exceptions ||
|-------------------------------------------|---|
| `java.lang.IllegalStateException` | |
| `java.lang.IllegalArgumentException` | |
| `java.lang.UnsupportedOperationException` | |
| --- | --- |
