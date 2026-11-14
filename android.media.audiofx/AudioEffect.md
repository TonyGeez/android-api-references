# AudioEffect

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AudioEffect

Kotlin| [Java](../android/media/audiofx/AudioEffect.md) 
| --- | --- |

```
open class AudioEffect
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.audiofx.AudioEffect](../android/media/audiofx/AudioEffect.md) |

| Known Direct Subclasses [AcousticEchoCanceler](../android/media/audiofx/AcousticEchoCanceler.md), [AutomaticGainControl](../android/media/audiofx/AutomaticGainControl.md), [BassBoost](../android/media/audiofx/BassBoost.md), [DynamicsProcessing](../android/media/audiofx/DynamicsProcessing.md), [EnvironmentalReverb](../android/media/audiofx/EnvironmentalReverb.md), [Equalizer](../android/media/audiofx/Equalizer.md), [HapticGenerator](../android/media/audiofx/HapticGenerator.md), [LoudnessEnhancer](../android/media/audiofx/LoudnessEnhancer.md), [NoiseSuppressor](../android/media/audiofx/NoiseSuppressor.md), [PresetReverb](../android/media/audiofx/PresetReverb.md), [Virtualizer](../android/media/audiofx/Virtualizer.md) |-------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------| | [AcousticEchoCanceler](../android/media/audiofx/AcousticEchoCanceler.md) | Acoustic Echo Canceler (AEC). | | [AutomaticGainControl](../android/media/audiofx/AutomaticGainControl.md) | Automatic Gain Control (AGC). | | [BassBoost](../android/media/audiofx/BassBoost.md) | Bass boost is an audio effect to boost or amplify low frequencies of the sound. | | [DynamicsProcessing](../android/media/audiofx/DynamicsProcessing.md) | DynamicsProcessing is an audio effect for equalizing and changing dynamic range properties of the sound. | | [EnvironmentalReverb](../android/media/audiofx/EnvironmentalReverb.md) | A sound generated within a room travels in many directions. | | [Equalizer](../android/media/audiofx/Equalizer.md) | An Equalizer is used to alter the frequency response of a particular music source or of the main output mix. | | [HapticGenerator](../android/media/audiofx/HapticGenerator.md) | Haptic Generator(HG). | | [LoudnessEnhancer](../android/media/audiofx/LoudnessEnhancer.md) | LoudnessEnhancer is an audio effect for increasing audio loudness. | | [NoiseSuppressor](../android/media/audiofx/NoiseSuppressor.md) | Noise Suppressor (NS). | | [PresetReverb](../android/media/audiofx/PresetReverb.md) | A sound generated within a room travels in many directions. | | [Virtualizer](../android/media/audiofx/Virtualizer.md) | An audio virtualizer is a general name for an effect to spatialize audio channels. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

AudioEffect is the base class for controlling audio effects provided by the android audio framework.

Applications should not use the AudioEffect class directly but one of its derived classes to control specific effects:

- [android.media.audiofx.Equalizer](../android/media/audiofx/Equalizer.md)
- [android.media.audiofx.Virtualizer](../android/media/audiofx/Virtualizer.md)
- [android.media.audiofx.BassBoost](../android/media/audiofx/BassBoost.md)
- [android.media.audiofx.PresetReverb](../android/media/audiofx/PresetReverb.md)
- [android.media.audiofx.EnvironmentalReverb](../android/media/audiofx/EnvironmentalReverb.md)
- [android.media.audiofx.DynamicsProcessing](../android/media/audiofx/DynamicsProcessing.md)
- [android.media.audiofx.HapticGenerator](../android/media/audiofx/HapticGenerator.md)

To apply the audio effect to a specific AudioTrack or MediaPlayer instance, the application must specify the audio session ID of that instance when creating the AudioEffect. (see [android.media.MediaPlayer#getAudioSessionId()](../android/media/MediaPlayer.md))for details on audio sessions).

NOTE: attaching insert effects (equalizer, bass boost, virtualizer) to the global audio output mix by use of session 0 is deprecated.

Creating an AudioEffect object will create the corresponding effect engine in the audio framework if no instance of the same effect type exists in the specified audio session. If one exists, this instance will be used.

The application creating the AudioEffect object (or a derived class) will either receive control of the effect engine or not depending on the priority parameter. If priority is higher than the priority used by the current effect engine owner, the control will be transfered to the new object. Otherwise control will remain with the previous object. In this case, the new application will be notified of changes in effect engine state or control ownership by the appropriate listener.

## Summary

| Nested classes ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [Descriptor](../android/media/audiofx/AudioEffect.Descriptor.md) The effect descriptor contains information on a particular effect implemented in the audio framework: - type: UUID identifying the effect type. May be one of: [AudioEffect.EFFECT_TYPE_AEC](../android/media/audiofx/AudioEffect.md), [AudioEffect.EFFECT_TYPE_AGC](../android/media/audiofx/AudioEffect.md), [AudioEffect.EFFECT_TYPE_BASS_BOOST](../android/media/audiofx/AudioEffect.md), [AudioEffect.EFFECT_TYPE_ENV_REVERB](../android/media/audiofx/AudioEffect.md), [AudioEffect.EFFECT_TYPE_EQUALIZER](../android/media/audiofx/AudioEffect.md), [AudioEffect.EFFECT_TYPE_NS](../android/media/audiofx/AudioEffect.md), [AudioEffect.EFFECT_TYPE_PRESET_REVERB](../android/media/audiofx/AudioEffect.md), [AudioEffect.EFFECT_TYPE_VIRTUALIZER](../android/media/audiofx/AudioEffect.md), [AudioEffect.EFFECT_TYPE_DYNAMICS_PROCESSING](../android/media/audiofx/AudioEffect.md), [AudioEffect.EFFECT_TYPE_HAPTIC_GENERATOR](../android/media/audiofx/AudioEffect.md). - uuid: UUID for this particular implementation - connectMode: [EFFECT_INSERT](../android/media/audiofx/AudioEffect.md) or [EFFECT_AUXILIARY](../android/media/audiofx/AudioEffect.md) - name: human readable effect name - implementor: human readable effect implementor name The method [queryEffects()](../android/media/audiofx/AudioEffect.md))returns an array of Descriptors to facilitate effects enumeration. <br /> |
| abstract | [OnControlStatusChangeListener](../android/media/audiofx/AudioEffect.OnControlStatusChangeListener.md) The OnControlStatusChangeListener interface defines a method called by the AudioEffect when control of the effect engine is gained or lost by the application |
| abstract | [OnEnableStatusChangeListener](../android/media/audiofx/AudioEffect.OnEnableStatusChangeListener.md) The OnEnableStatusChangeListener interface defines a method called by the AudioEffect when the enabled state of the effect engine was changed by the controlling application. |
| --- | --- |

| Constants ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_CLOSE_AUDIO_EFFECT_CONTROL_SESSION](../android/media/audiofx/AudioEffect.md) Intent to signal to the effect control application or service that an audio session is closed and that effects should not be applied anymore. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_DISPLAY_AUDIO_EFFECT_CONTROL_PANEL](../android/media/audiofx/AudioEffect.md) Intent to launch an audio effect control panel UI. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_OPEN_AUDIO_EFFECT_CONTROL_SESSION](../android/media/audiofx/AudioEffect.md) Intent to signal to the effect control application or service that a new audio session is opened and requires audio effects to be applied. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ALREADY_EXISTS](../android/media/audiofx/AudioEffect.md) Internal operation status. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_TYPE_GAME](../android/media/audiofx/AudioEffect.md) Value for [EXTRA_CONTENT_TYPE](../android/media/audiofx/AudioEffect.md) when the type of content played is game audio |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_TYPE_MOVIE](../android/media/audiofx/AudioEffect.md) Value for [EXTRA_CONTENT_TYPE](../android/media/audiofx/AudioEffect.md) when the type of content played is video or movie |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_TYPE_MUSIC](../android/media/audiofx/AudioEffect.md) Value for [EXTRA_CONTENT_TYPE](../android/media/audiofx/AudioEffect.md) when the type of content played is music |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_TYPE_VOICE](../android/media/audiofx/AudioEffect.md) Value for [EXTRA_CONTENT_TYPE](../android/media/audiofx/AudioEffect.md) when the type of content played is voice audio |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EFFECT_AUXILIARY](../android/media/audiofx/AudioEffect.md) Effect connection mode is auxiliary. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EFFECT_INSERT](../android/media/audiofx/AudioEffect.md) Effect connection mode is insert. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EFFECT_POST_PROCESSING](../android/media/audiofx/AudioEffect.md) Effect connection mode is post processing. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EFFECT_PRE_PROCESSING](../android/media/audiofx/AudioEffect.md) Effect connection mode is pre processing. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR](../android/media/audiofx/AudioEffect.md) Unspecified error. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_BAD_VALUE](../android/media/audiofx/AudioEffect.md) Operation failed due to bad parameter value. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_DEAD_OBJECT](../android/media/audiofx/AudioEffect.md) Operation failed due to dead remote object. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_INVALID_OPERATION](../android/media/audiofx/AudioEffect.md) Operation failed because it was requested in wrong state. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_NO_INIT](../android/media/audiofx/AudioEffect.md) Operation failed due to bad object initialization. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_NO_MEMORY](../android/media/audiofx/AudioEffect.md) Operation failed due to lack of memory. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_AUDIO_SESSION](../android/media/audiofx/AudioEffect.md) Contains the ID of the audio session the effects should be applied to. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_CONTENT_TYPE](../android/media/audiofx/AudioEffect.md) Indicates which type of content is played by the application. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_PACKAGE_NAME](../android/media/audiofx/AudioEffect.md) Contains the package name of the calling application. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SUCCESS](../android/media/audiofx/AudioEffect.md) Successful operation. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [AudioEffect.Descriptor](../android/media/audiofx/AudioEffect.Descriptor.md)! | [getDescriptor](../android/media/audiofx/AudioEffect.md))`()` Get the effect descriptor. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getEnabled](../android/media/audiofx/AudioEffect.md))`()` Returns effect enabled state |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getId](../android/media/audiofx/AudioEffect.md))`()` Returns effect unique identifier. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasControl](../android/media/audiofx/AudioEffect.md))`()` Checks if this AudioEffect object is controlling the effect engine. |
| openstatic [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [AudioEffect.Descriptor](../android/media/audiofx/AudioEffect.Descriptor.md)!\>! | [queryEffects](../android/media/audiofx/AudioEffect.md))`()` Query all effects available on the platform. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [release](../android/media/audiofx/AudioEffect.md))`()` Releases the native AudioEffect resources. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setControlStatusListener](../android/media/audiofx/AudioEffect.md))`(`listener:` ` [AudioEffect.OnControlStatusChangeListener](../android/media/audiofx/AudioEffect.OnControlStatusChangeListener.md)!`)` Sets the listener AudioEffect notifies when the effect engine control is taken or returned. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEnableStatusListener](../android/media/audiofx/AudioEffect.md))`(`listener:` ` [AudioEffect.OnEnableStatusChangeListener](../android/media/audiofx/AudioEffect.OnEnableStatusChangeListener.md)!`)` Sets the listener AudioEffect notifies when the effect engine is enabled or disabled. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [setEnabled](../android/media/audiofx/AudioEffect.md))`(`enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Enable or disable the effect. |
| --- | --- |

| Protected methods ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](../android/media/audiofx/AudioEffect.md))`()` <br /> |

| Properties ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [UUID](../java/util/UUID.md)! | [EFFECT_TYPE_AEC](../android/media/audiofx/AudioEffect.md) UUID for Acoustic Echo Canceler (AEC) |
| static [UUID](../java/util/UUID.md)! | [EFFECT_TYPE_AGC](../android/media/audiofx/AudioEffect.md) UUID for Automatic Gain Control (AGC) |
| static [UUID](../java/util/UUID.md)! | [EFFECT_TYPE_BASS_BOOST](../android/media/audiofx/AudioEffect.md) UUID for bass boost effect |
| --- | --- |
| static [UUID](../java/util/UUID.md)! | [EFFECT_TYPE_DYNAMICS_PROCESSING](../android/media/audiofx/AudioEffect.md) UUID for Dynamics Processing |
| static [UUID](../java/util/UUID.md)! | [EFFECT_TYPE_ENV_REVERB](../android/media/audiofx/AudioEffect.md) UUID for environmental reverberation effect |
| static [UUID](../java/util/UUID.md)! | [EFFECT_TYPE_EQUALIZER](../android/media/audiofx/AudioEffect.md) UUID for equalizer effect |
| --- | --- |
| static [UUID](../java/util/UUID.md) | [EFFECT_TYPE_HAPTIC_GENERATOR](../android/media/audiofx/AudioEffect.md) UUID for Haptic Generator. |
| static [UUID](../java/util/UUID.md)! | [EFFECT_TYPE_LOUDNESS_ENHANCER](../android/media/audiofx/AudioEffect.md) UUID for Loudness Enhancer |
| static [UUID](../java/util/UUID.md)! | [EFFECT_TYPE_NS](../android/media/audiofx/AudioEffect.md) UUID for Noise Suppressor (NS) |
| --- | --- |
| static [UUID](../java/util/UUID.md)! | [EFFECT_TYPE_PRESET_REVERB](../android/media/audiofx/AudioEffect.md) UUID for preset reverberation effect |
| static [UUID](../java/util/UUID.md)! | [EFFECT_TYPE_VIRTUALIZER](../android/media/audiofx/AudioEffect.md) UUID for virtualizer effect |

## Constants

### ACTION_CLOSE_AUDIO_EFFECT_CONTROL_SESSION

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_CLOSE_AUDIO_EFFECT_CONTROL_SESSION: String
```

Intent to signal to the effect control application or service that an audio session is closed and that effects should not be applied anymore.

The effect control application receiving this intent will delete all effects on this session and store current settings in package specific storage.

The calling package name is indicated by the [EXTRA_PACKAGE_NAME](../android/media/audiofx/AudioEffect.md) extra and the audio session ID by the [EXTRA_AUDIO_SESSION](../android/media/audiofx/AudioEffect.md) extra. Both extras are mandatory.

It is good practice for applications to broadcast this intent when music playback stops and/or when exiting to free system resources consumed by audio effect engines. 

 Value: "android.media.action.CLOSE_AUDIO_EFFECT_CONTROL_SESSION"

### ACTION_DISPLAY_AUDIO_EFFECT_CONTROL_PANEL

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_DISPLAY_AUDIO_EFFECT_CONTROL_PANEL: String
```

Intent to launch an audio effect control panel UI.

The goal of this intent is to enable separate implementations of music/media player applications and audio effect control application or services. This will allow platform vendors to offer more advanced control options for standard effects or control for platform specific effects.

The intent carries a number of extras used by the player application to communicate necessary pieces of information to the control panel application.

The calling application must use the android.app.Activity#startActivityForResult(Intent, int) method to launch the control panel so that its package name is indicated and used by the control panel application to keep track of changes for this particular application.

The [EXTRA_AUDIO_SESSION](../android/media/audiofx/AudioEffect.md) extra will indicate an audio session to which the audio effects should be applied. If no audio session is specified, either one of the follownig will happen:

- If an audio session was previously opened by the calling application with [ACTION_OPEN_AUDIO_EFFECT_CONTROL_SESSION](../android/media/audiofx/AudioEffect.md) intent, the effect changes will be applied to that session.

- If no audio session is opened, the changes will be stored in the package specific storage area and applied whenever a new audio session is opened by this application.

The [EXTRA_CONTENT_TYPE](../android/media/audiofx/AudioEffect.md) extra will help the control panel application customize both the UI layout and the default audio effect settings if none are already stored for the calling application. 

 Value: "android.media.action.DISPLAY_AUDIO_EFFECT_CONTROL_PANEL"

### ACTION_OPEN_AUDIO_EFFECT_CONTROL_SESSION

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_OPEN_AUDIO_EFFECT_CONTROL_SESSION: String
```

Intent to signal to the effect control application or service that a new audio session is opened and requires audio effects to be applied.

This is different from [ACTION_DISPLAY_AUDIO_EFFECT_CONTROL_PANEL](../android/media/audiofx/AudioEffect.md) in that no UI should be displayed in this case. Music player applications can broadcast this intent before starting playback to make sure that any audio effect settings previously selected by the user are applied.

The effect control application receiving this intent will look for previously stored settings for the calling application, create all required audio effects and apply the effect settings to the specified audio session.

The calling package name is indicated by the [EXTRA_PACKAGE_NAME](../android/media/audiofx/AudioEffect.md) extra and the audio session ID by the [EXTRA_AUDIO_SESSION](../android/media/audiofx/AudioEffect.md) extra. Both extras are mandatory.

If no stored settings are found for the calling application, default settings for the content type indicated by [EXTRA_CONTENT_TYPE](../android/media/audiofx/AudioEffect.md) will be applied. The default settings for a given content type are platform specific. 

 Value: "android.media.action.OPEN_AUDIO_EFFECT_CONTROL_SESSION"

### ALREADY_EXISTS

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ALREADY_EXISTS: Int
```

Internal operation status. Not returned by any method. 

 Value: -2

### CONTENT_TYPE_GAME

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTENT_TYPE_GAME: Int
```

Value for [EXTRA_CONTENT_TYPE](../android/media/audiofx/AudioEffect.md) when the type of content played is game audio 

 Value: 2

### CONTENT_TYPE_MOVIE

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTENT_TYPE_MOVIE: Int
```

Value for [EXTRA_CONTENT_TYPE](../android/media/audiofx/AudioEffect.md) when the type of content played is video or movie 

 Value: 1

### CONTENT_TYPE_MUSIC

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTENT_TYPE_MUSIC: Int
```

Value for [EXTRA_CONTENT_TYPE](../android/media/audiofx/AudioEffect.md) when the type of content played is music 

 Value: 0

### CONTENT_TYPE_VOICE

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTENT_TYPE_VOICE: Int
```

Value for [EXTRA_CONTENT_TYPE](../android/media/audiofx/AudioEffect.md) when the type of content played is voice audio 

 Value: 3

### EFFECT_AUXILIARY

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EFFECT_AUXILIARY: String
```

Effect connection mode is auxiliary.

Auxiliary effects must be created on session 0 (global output mix). In order for a MediaPlayer or AudioTrack to be fed into this effect, they must be explicitely attached to this effect and a send level must be specified.

Use the effect ID returned by [getId()](../android/media/audiofx/AudioEffect.md))to designate this particular effect when attaching it to the MediaPlayer or AudioTrack. 

 Value: "Auxiliary"

### EFFECT_INSERT

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EFFECT_INSERT: String
```

Effect connection mode is insert. Specifying an audio session ID when creating the effect will insert this effect after all players in the same audio session. 

 Value: "Insert"

### EFFECT_POST_PROCESSING

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EFFECT_POST_PROCESSING: String
```

Effect connection mode is post processing. The audio post processing effects are attached to an audio output stream or device 

 Value: "Post Processing"

### EFFECT_PRE_PROCESSING

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EFFECT_PRE_PROCESSING: String
```

Effect connection mode is pre processing. The audio pre processing effects are attached to an audio input stream or device 

 Value: "Pre Processing"

### ERROR

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR: Int
```

Unspecified error. 

 Value: -1

### ERROR_BAD_VALUE

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_BAD_VALUE: Int
```

Operation failed due to bad parameter value. 

 Value: -4

### ERROR_DEAD_OBJECT

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_DEAD_OBJECT: Int
```

Operation failed due to dead remote object. 

 Value: -7

### ERROR_INVALID_OPERATION

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_INVALID_OPERATION: Int
```

Operation failed because it was requested in wrong state. 

 Value: -5

### ERROR_NO_INIT

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_NO_INIT: Int
```

Operation failed due to bad object initialization. 

 Value: -3

### ERROR_NO_MEMORY

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_NO_MEMORY: Int
```

Operation failed due to lack of memory. 

 Value: -6

### EXTRA_AUDIO_SESSION

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_AUDIO_SESSION: String
```

Contains the ID of the audio session the effects should be applied to.

This extra is for use with [ACTION_DISPLAY_AUDIO_EFFECT_CONTROL_PANEL](../android/media/audiofx/AudioEffect.md), [ACTION_OPEN_AUDIO_EFFECT_CONTROL_SESSION](../android/media/audiofx/AudioEffect.md) and [ACTION_CLOSE_AUDIO_EFFECT_CONTROL_SESSION](../android/media/audiofx/AudioEffect.md) intents.

The extra value is of type int and is the audio session ID. 

 Value: "android.media.extra.AUDIO_SESSION"

**See Also**

- [android.media.MediaPlayer#getAudioSessionId()](../android/media/MediaPlayer.md)) 

### EXTRA_CONTENT_TYPE

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_CONTENT_TYPE: String
```

Indicates which type of content is played by the application.

This extra is for use with [ACTION_DISPLAY_AUDIO_EFFECT_CONTROL_PANEL](../android/media/audiofx/AudioEffect.md) and [ACTION_OPEN_AUDIO_EFFECT_CONTROL_SESSION](../android/media/audiofx/AudioEffect.md) intents.

This information is used by the effect control application to customize UI and select appropriate default effect settings. The content type is one of the following:

- [CONTENT_TYPE_MUSIC](../android/media/audiofx/AudioEffect.md)
- [CONTENT_TYPE_MOVIE](../android/media/audiofx/AudioEffect.md)
- [CONTENT_TYPE_GAME](../android/media/audiofx/AudioEffect.md)
- [CONTENT_TYPE_VOICE](../android/media/audiofx/AudioEffect.md)

If omitted, the content type defaults to [CONTENT_TYPE_MUSIC](../android/media/audiofx/AudioEffect.md). 

 Value: "android.media.extra.CONTENT_TYPE"

### EXTRA_PACKAGE_NAME

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_PACKAGE_NAME: String
```

Contains the package name of the calling application.

This extra is for use with [ACTION_OPEN_AUDIO_EFFECT_CONTROL_SESSION](../android/media/audiofx/AudioEffect.md) and [ACTION_CLOSE_AUDIO_EFFECT_CONTROL_SESSION](../android/media/audiofx/AudioEffect.md) intents.

The extra value is a string containing the full package name. 

 Value: "android.media.extra.PACKAGE_NAME"

### SUCCESS

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUCCESS: Int
```

Successful operation. 

 Value: 0

## Public methods

### getDescriptor

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDescriptor(): AudioEffect.Descriptor!
```

Get the effect descriptor.

| Exceptions ||
|-----------------------------------|---|
| `java.lang.IllegalStateException` | |

**See Also**

- [android.media.audiofx.AudioEffect.Descriptor](../android/media/audiofx/AudioEffect.Descriptor.md) 

### getEnabled

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEnabled(): Boolean
```

Returns effect enabled state

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the effect is enabled, false otherwise. |

| Exceptions ||
|-----------------------------------|---|
| `java.lang.IllegalStateException` | |

### getId

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getId(): Int
```

Returns effect unique identifier. This system wide unique identifier can be used to attach this effect to a MediaPlayer or an AudioTrack when the effect is an auxiliary effect (Reverb)

| Return ||
|----------------------------------------------------------------------------|------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the effect identifier. |

| Exceptions ||
|-----------------------------------|---|
| `java.lang.IllegalStateException` | |

### hasControl

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasControl(): Boolean
```

Checks if this AudioEffect object is controlling the effect engine.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this instance has control of effect engine, false otherwise. |

| Exceptions ||
|-----------------------------------|---|
| `java.lang.IllegalStateException` | |

### queryEffects

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun queryEffects(): Array<AudioEffect.Descriptor!>!
```

Query all effects available on the platform. Returns an array of [android.media.audiofx.AudioEffect.Descriptor](../android/media/audiofx/AudioEffect.Descriptor.md) objects

| Exceptions ||
|-----------------------------------|---|
| `java.lang.IllegalStateException` | |

### release

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun release(): Unit
```

Releases the native AudioEffect resources. It is a good practice to release the effect engine when not in use as control can be returned to other applications or the native resources released. 

### setControlStatusListener

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setControlStatusListener(listener: AudioEffect.OnControlStatusChangeListener!): Unit
```

Sets the listener AudioEffect notifies when the effect engine control is taken or returned.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [AudioEffect.OnControlStatusChangeListener](../android/media/audiofx/AudioEffect.OnControlStatusChangeListener.md)!: |

### setEnableStatusListener

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setEnableStatusListener(listener: AudioEffect.OnEnableStatusChangeListener!): Unit
```

Sets the listener AudioEffect notifies when the effect engine is enabled or disabled.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [AudioEffect.OnEnableStatusChangeListener](../android/media/audiofx/AudioEffect.OnEnableStatusChangeListener.md)!: |

### setEnabled

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setEnabled(enabled: Boolean): Int
```

Enable or disable the effect. Creating an audio effect does not automatically apply this effect on the audio source. It creates the resources necessary to process this effect but the audio signal is still bypassed through the effect engine. Calling this method will make that the effect is actually applied or not to the audio content being played in the corresponding audio session.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------|
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):the requested enable state |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SUCCESS](../android/media/audiofx/AudioEffect.md) in case of success, [ERROR_INVALID_OPERATION](../android/media/audiofx/AudioEffect.md) or [ERROR_DEAD_OBJECT](../android/media/audiofx/AudioEffect.md) in case of failure. |

| Exceptions ||
|-----------------------------------|---|
| `java.lang.IllegalStateException` | |

## Protected methods

### finalize

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun finalize(): Unit
```

| Exceptions ||
|-----------------------|-------------------------------------|
| `java.lang.Throwable` | the`Exception`raised by this method |

## Properties

### EFFECT_TYPE_AEC

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EFFECT_TYPE_AEC: UUID!
```

UUID for Acoustic Echo Canceler (AEC) 

### EFFECT_TYPE_AGC

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EFFECT_TYPE_AGC: UUID!
```

UUID for Automatic Gain Control (AGC) 

### EFFECT_TYPE_BASS_BOOST

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EFFECT_TYPE_BASS_BOOST: UUID!
```

UUID for bass boost effect 

### EFFECT_TYPE_DYNAMICS_PROCESSING

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EFFECT_TYPE_DYNAMICS_PROCESSING: UUID!
```

UUID for Dynamics Processing 

### EFFECT_TYPE_ENV_REVERB

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EFFECT_TYPE_ENV_REVERB: UUID!
```

UUID for environmental reverberation effect 

### EFFECT_TYPE_EQUALIZER

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EFFECT_TYPE_EQUALIZER: UUID!
```

UUID for equalizer effect 

### EFFECT_TYPE_HAPTIC_GENERATOR

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EFFECT_TYPE_HAPTIC_GENERATOR: UUID
```

UUID for Haptic Generator. 

### EFFECT_TYPE_LOUDNESS_ENHANCER

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EFFECT_TYPE_LOUDNESS_ENHANCER: UUID!
```

UUID for Loudness Enhancer 

### EFFECT_TYPE_NS

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EFFECT_TYPE_NS: UUID!
```

UUID for Noise Suppressor (NS) 

### EFFECT_TYPE_PRESET_REVERB

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EFFECT_TYPE_PRESET_REVERB: UUID!
```

UUID for preset reverberation effect 

### EFFECT_TYPE_VIRTUALIZER

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EFFECT_TYPE_VIRTUALIZER: UUID!
```

UUID for virtualizer effect
