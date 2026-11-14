# AudioEffect

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AudioEffect

Kotlin| [Java](https://developer.android.com/reference/android/media/audiofx/AudioEffect "View this page in Java") 

```
open class AudioEffect
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.media.audiofx.AudioEffect](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#) |

| Known Direct Subclasses [AcousticEchoCanceler](https://developer.android.com/reference/kotlin/android/media/audiofx/AcousticEchoCanceler), [AutomaticGainControl](https://developer.android.com/reference/kotlin/android/media/audiofx/AutomaticGainControl), [BassBoost](https://developer.android.com/reference/kotlin/android/media/audiofx/BassBoost), [DynamicsProcessing](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing), [EnvironmentalReverb](https://developer.android.com/reference/kotlin/android/media/audiofx/EnvironmentalReverb), [Equalizer](https://developer.android.com/reference/kotlin/android/media/audiofx/Equalizer), [HapticGenerator](https://developer.android.com/reference/kotlin/android/media/audiofx/HapticGenerator), [LoudnessEnhancer](https://developer.android.com/reference/kotlin/android/media/audiofx/LoudnessEnhancer), [NoiseSuppressor](https://developer.android.com/reference/kotlin/android/media/audiofx/NoiseSuppressor), [PresetReverb](https://developer.android.com/reference/kotlin/android/media/audiofx/PresetReverb), [Virtualizer](https://developer.android.com/reference/kotlin/android/media/audiofx/Virtualizer) |-------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------| | [AcousticEchoCanceler](https://developer.android.com/reference/kotlin/android/media/audiofx/AcousticEchoCanceler) | Acoustic Echo Canceler (AEC). | | [AutomaticGainControl](https://developer.android.com/reference/kotlin/android/media/audiofx/AutomaticGainControl) | Automatic Gain Control (AGC). | | [BassBoost](https://developer.android.com/reference/kotlin/android/media/audiofx/BassBoost) | Bass boost is an audio effect to boost or amplify low frequencies of the sound. | | [DynamicsProcessing](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing) | DynamicsProcessing is an audio effect for equalizing and changing dynamic range properties of the sound. | | [EnvironmentalReverb](https://developer.android.com/reference/kotlin/android/media/audiofx/EnvironmentalReverb) | A sound generated within a room travels in many directions. | | [Equalizer](https://developer.android.com/reference/kotlin/android/media/audiofx/Equalizer) | An Equalizer is used to alter the frequency response of a particular music source or of the main output mix. | | [HapticGenerator](https://developer.android.com/reference/kotlin/android/media/audiofx/HapticGenerator) | Haptic Generator(HG). | | [LoudnessEnhancer](https://developer.android.com/reference/kotlin/android/media/audiofx/LoudnessEnhancer) | LoudnessEnhancer is an audio effect for increasing audio loudness. | | [NoiseSuppressor](https://developer.android.com/reference/kotlin/android/media/audiofx/NoiseSuppressor) | Noise Suppressor (NS). | | [PresetReverb](https://developer.android.com/reference/kotlin/android/media/audiofx/PresetReverb) | A sound generated within a room travels in many directions. | | [Virtualizer](https://developer.android.com/reference/kotlin/android/media/audiofx/Virtualizer) | An audio virtualizer is a general name for an effect to spatialize audio channels. | |

AudioEffect is the base class for controlling audio effects provided by the android audio framework.

Applications should not use the AudioEffect class directly but one of its derived classes to control specific effects:

- [android.media.audiofx.Equalizer](https://developer.android.com/reference/kotlin/android/media/audiofx/Equalizer)
- [android.media.audiofx.Virtualizer](https://developer.android.com/reference/kotlin/android/media/audiofx/Virtualizer)
- [android.media.audiofx.BassBoost](https://developer.android.com/reference/kotlin/android/media/audiofx/BassBoost)
- [android.media.audiofx.PresetReverb](https://developer.android.com/reference/kotlin/android/media/audiofx/PresetReverb)
- [android.media.audiofx.EnvironmentalReverb](https://developer.android.com/reference/kotlin/android/media/audiofx/EnvironmentalReverb)
- [android.media.audiofx.DynamicsProcessing](https://developer.android.com/reference/kotlin/android/media/audiofx/DynamicsProcessing)
- [android.media.audiofx.HapticGenerator](https://developer.android.com/reference/kotlin/android/media/audiofx/HapticGenerator)

To apply the audio effect to a specific AudioTrack or MediaPlayer instance, the application must specify the audio session ID of that instance when creating the AudioEffect. (see [android.media.MediaPlayer#getAudioSessionId()](https://developer.android.com/reference/kotlin/android/media/MediaPlayer.html#getAudioSessionId())for details on audio sessions).

NOTE: attaching insert effects (equalizer, bass boost, virtualizer) to the global audio output mix by use of session 0 is deprecated.

Creating an AudioEffect object will create the corresponding effect engine in the audio framework if no instance of the same effect type exists in the specified audio session. If one exists, this instance will be used.

The application creating the AudioEffect object (or a derived class) will either receive control of the effect engine or not depending on the priority parameter. If priority is higher than the priority used by the current effect engine owner, the control will be transfered to the new object. Otherwise control will remain with the previous object. In this case, the new application will be notified of changes in effect engine state or control ownership by the appropriate listener.

## Summary

| Nested classes ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [Descriptor](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect.Descriptor) The effect descriptor contains information on a particular effect implemented in the audio framework: - type: UUID identifying the effect type. May be one of: [AudioEffect.EFFECT_TYPE_AEC](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_TYPE_AEC:java.util.UUID), [AudioEffect.EFFECT_TYPE_AGC](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_TYPE_AGC:java.util.UUID), [AudioEffect.EFFECT_TYPE_BASS_BOOST](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_TYPE_BASS_BOOST:java.util.UUID), [AudioEffect.EFFECT_TYPE_ENV_REVERB](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_TYPE_ENV_REVERB:java.util.UUID), [AudioEffect.EFFECT_TYPE_EQUALIZER](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_TYPE_EQUALIZER:java.util.UUID), [AudioEffect.EFFECT_TYPE_NS](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_TYPE_NS:java.util.UUID), [AudioEffect.EFFECT_TYPE_PRESET_REVERB](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_TYPE_PRESET_REVERB:java.util.UUID), [AudioEffect.EFFECT_TYPE_VIRTUALIZER](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_TYPE_VIRTUALIZER:java.util.UUID), [AudioEffect.EFFECT_TYPE_DYNAMICS_PROCESSING](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_TYPE_DYNAMICS_PROCESSING:java.util.UUID), [AudioEffect.EFFECT_TYPE_HAPTIC_GENERATOR](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_TYPE_HAPTIC_GENERATOR:java.util.UUID). - uuid: UUID for this particular implementation - connectMode: [EFFECT_INSERT](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_INSERT:kotlin.String) or [EFFECT_AUXILIARY](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_AUXILIARY:kotlin.String) - name: human readable effect name - implementor: human readable effect implementor name The method [queryEffects()](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#queryEffects())returns an array of Descriptors to facilitate effects enumeration. <br /> |
| abstract | [OnControlStatusChangeListener](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect.OnControlStatusChangeListener) The OnControlStatusChangeListener interface defines a method called by the AudioEffect when control of the effect engine is gained or lost by the application |
| abstract | [OnEnableStatusChangeListener](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect.OnEnableStatusChangeListener) The OnEnableStatusChangeListener interface defines a method called by the AudioEffect when the enabled state of the effect engine was changed by the controlling application. |

| Constants ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_CLOSE_AUDIO_EFFECT_CONTROL_SESSION](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ACTION_CLOSE_AUDIO_EFFECT_CONTROL_SESSION:kotlin.String) Intent to signal to the effect control application or service that an audio session is closed and that effects should not be applied anymore. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_DISPLAY_AUDIO_EFFECT_CONTROL_PANEL](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ACTION_DISPLAY_AUDIO_EFFECT_CONTROL_PANEL:kotlin.String) Intent to launch an audio effect control panel UI. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_OPEN_AUDIO_EFFECT_CONTROL_SESSION](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ACTION_OPEN_AUDIO_EFFECT_CONTROL_SESSION:kotlin.String) Intent to signal to the effect control application or service that a new audio session is opened and requires audio effects to be applied. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ALREADY_EXISTS](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ALREADY_EXISTS:kotlin.Int) Internal operation status. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_TYPE_GAME](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#CONTENT_TYPE_GAME:kotlin.Int) Value for [EXTRA_CONTENT_TYPE](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EXTRA_CONTENT_TYPE:kotlin.String) when the type of content played is game audio |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_TYPE_MOVIE](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#CONTENT_TYPE_MOVIE:kotlin.Int) Value for [EXTRA_CONTENT_TYPE](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EXTRA_CONTENT_TYPE:kotlin.String) when the type of content played is video or movie |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_TYPE_MUSIC](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#CONTENT_TYPE_MUSIC:kotlin.Int) Value for [EXTRA_CONTENT_TYPE](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EXTRA_CONTENT_TYPE:kotlin.String) when the type of content played is music |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_TYPE_VOICE](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#CONTENT_TYPE_VOICE:kotlin.Int) Value for [EXTRA_CONTENT_TYPE](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EXTRA_CONTENT_TYPE:kotlin.String) when the type of content played is voice audio |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EFFECT_AUXILIARY](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_AUXILIARY:kotlin.String) Effect connection mode is auxiliary. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EFFECT_INSERT](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_INSERT:kotlin.String) Effect connection mode is insert. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EFFECT_POST_PROCESSING](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_POST_PROCESSING:kotlin.String) Effect connection mode is post processing. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EFFECT_PRE_PROCESSING](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_PRE_PROCESSING:kotlin.String) Effect connection mode is pre processing. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ERROR:kotlin.Int) Unspecified error. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_BAD_VALUE](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ERROR_BAD_VALUE:kotlin.Int) Operation failed due to bad parameter value. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_DEAD_OBJECT](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ERROR_DEAD_OBJECT:kotlin.Int) Operation failed due to dead remote object. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_INVALID_OPERATION](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ERROR_INVALID_OPERATION:kotlin.Int) Operation failed because it was requested in wrong state. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_NO_INIT](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ERROR_NO_INIT:kotlin.Int) Operation failed due to bad object initialization. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_NO_MEMORY](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ERROR_NO_MEMORY:kotlin.Int) Operation failed due to lack of memory. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_AUDIO_SESSION](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EXTRA_AUDIO_SESSION:kotlin.String) Contains the ID of the audio session the effects should be applied to. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_CONTENT_TYPE](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EXTRA_CONTENT_TYPE:kotlin.String) Indicates which type of content is played by the application. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_PACKAGE_NAME](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EXTRA_PACKAGE_NAME:kotlin.String) Contains the package name of the calling application. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SUCCESS](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#SUCCESS:kotlin.Int) Successful operation. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [AudioEffect.Descriptor](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect.Descriptor)! | [getDescriptor](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#getDescriptor())`()` Get the effect descriptor. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getEnabled](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#getEnabled())`()` Returns effect enabled state |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getId](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#getId())`()` Returns effect unique identifier. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasControl](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#hasControl())`()` Checks if this AudioEffect object is controlling the effect engine. |
| openstatic [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [AudioEffect.Descriptor](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect.Descriptor)!\>! | [queryEffects](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#queryEffects())`()` Query all effects available on the platform. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [release](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#release())`()` Releases the native AudioEffect resources. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setControlStatusListener](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#setControlStatusListener(android.media.audiofx.AudioEffect.OnControlStatusChangeListener))`(`listener:` ` [AudioEffect.OnControlStatusChangeListener](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect.OnControlStatusChangeListener)!`)` Sets the listener AudioEffect notifies when the effect engine control is taken or returned. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEnableStatusListener](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#setEnableStatusListener(android.media.audiofx.AudioEffect.OnEnableStatusChangeListener))`(`listener:` ` [AudioEffect.OnEnableStatusChangeListener](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect.OnEnableStatusChangeListener)!`)` Sets the listener AudioEffect notifies when the effect engine is enabled or disabled. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [setEnabled](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#setEnabled(kotlin.Boolean))`(`enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Enable or disable the effect. |

| Protected methods ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#finalize())`()` <br /> |

| Properties ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#)! | [EFFECT_TYPE_AEC](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_TYPE_AEC:java.util.UUID) UUID for Acoustic Echo Canceler (AEC) |
| static [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#)! | [EFFECT_TYPE_AGC](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_TYPE_AGC:java.util.UUID) UUID for Automatic Gain Control (AGC) |
| static [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#)! | [EFFECT_TYPE_BASS_BOOST](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_TYPE_BASS_BOOST:java.util.UUID) UUID for bass boost effect |
| static [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#)! | [EFFECT_TYPE_DYNAMICS_PROCESSING](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_TYPE_DYNAMICS_PROCESSING:java.util.UUID) UUID for Dynamics Processing |
| static [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#)! | [EFFECT_TYPE_ENV_REVERB](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_TYPE_ENV_REVERB:java.util.UUID) UUID for environmental reverberation effect |
| static [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#)! | [EFFECT_TYPE_EQUALIZER](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_TYPE_EQUALIZER:java.util.UUID) UUID for equalizer effect |
| static [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#) | [EFFECT_TYPE_HAPTIC_GENERATOR](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_TYPE_HAPTIC_GENERATOR:java.util.UUID) UUID for Haptic Generator. |
| static [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#)! | [EFFECT_TYPE_LOUDNESS_ENHANCER](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_TYPE_LOUDNESS_ENHANCER:java.util.UUID) UUID for Loudness Enhancer |
| static [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#)! | [EFFECT_TYPE_NS](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_TYPE_NS:java.util.UUID) UUID for Noise Suppressor (NS) |
| static [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#)! | [EFFECT_TYPE_PRESET_REVERB](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_TYPE_PRESET_REVERB:java.util.UUID) UUID for preset reverberation effect |
| static [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#)! | [EFFECT_TYPE_VIRTUALIZER](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_TYPE_VIRTUALIZER:java.util.UUID) UUID for virtualizer effect |

## Constants

### ACTION_CLOSE_AUDIO_EFFECT_CONTROL_SESSION

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_CLOSE_AUDIO_EFFECT_CONTROL_SESSION: String
```

Intent to signal to the effect control application or service that an audio session is closed and that effects should not be applied anymore.

The effect control application receiving this intent will delete all effects on this session and store current settings in package specific storage.

The calling package name is indicated by the [EXTRA_PACKAGE_NAME](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EXTRA_PACKAGE_NAME:kotlin.String) extra and the audio session ID by the [EXTRA_AUDIO_SESSION](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EXTRA_AUDIO_SESSION:kotlin.String) extra. Both extras are mandatory.

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

The [EXTRA_AUDIO_SESSION](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EXTRA_AUDIO_SESSION:kotlin.String) extra will indicate an audio session to which the audio effects should be applied. If no audio session is specified, either one of the follownig will happen:

- If an audio session was previously opened by the calling application with [ACTION_OPEN_AUDIO_EFFECT_CONTROL_SESSION](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ACTION_OPEN_AUDIO_EFFECT_CONTROL_SESSION:kotlin.String) intent, the effect changes will be applied to that session.

- If no audio session is opened, the changes will be stored in the package specific storage area and applied whenever a new audio session is opened by this application.

The [EXTRA_CONTENT_TYPE](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EXTRA_CONTENT_TYPE:kotlin.String) extra will help the control panel application customize both the UI layout and the default audio effect settings if none are already stored for the calling application. 

 Value: "android.media.action.DISPLAY_AUDIO_EFFECT_CONTROL_PANEL"

### ACTION_OPEN_AUDIO_EFFECT_CONTROL_SESSION

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_OPEN_AUDIO_EFFECT_CONTROL_SESSION: String
```

Intent to signal to the effect control application or service that a new audio session is opened and requires audio effects to be applied.

This is different from [ACTION_DISPLAY_AUDIO_EFFECT_CONTROL_PANEL](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ACTION_DISPLAY_AUDIO_EFFECT_CONTROL_PANEL:kotlin.String) in that no UI should be displayed in this case. Music player applications can broadcast this intent before starting playback to make sure that any audio effect settings previously selected by the user are applied.

The effect control application receiving this intent will look for previously stored settings for the calling application, create all required audio effects and apply the effect settings to the specified audio session.

The calling package name is indicated by the [EXTRA_PACKAGE_NAME](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EXTRA_PACKAGE_NAME:kotlin.String) extra and the audio session ID by the [EXTRA_AUDIO_SESSION](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EXTRA_AUDIO_SESSION:kotlin.String) extra. Both extras are mandatory.

If no stored settings are found for the calling application, default settings for the content type indicated by [EXTRA_CONTENT_TYPE](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EXTRA_CONTENT_TYPE:kotlin.String) will be applied. The default settings for a given content type are platform specific. 

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

Value for [EXTRA_CONTENT_TYPE](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EXTRA_CONTENT_TYPE:kotlin.String) when the type of content played is game audio 

 Value: 2

### CONTENT_TYPE_MOVIE

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTENT_TYPE_MOVIE: Int
```

Value for [EXTRA_CONTENT_TYPE](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EXTRA_CONTENT_TYPE:kotlin.String) when the type of content played is video or movie 

 Value: 1

### CONTENT_TYPE_MUSIC

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTENT_TYPE_MUSIC: Int
```

Value for [EXTRA_CONTENT_TYPE](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EXTRA_CONTENT_TYPE:kotlin.String) when the type of content played is music 

 Value: 0

### CONTENT_TYPE_VOICE

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTENT_TYPE_VOICE: Int
```

Value for [EXTRA_CONTENT_TYPE](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EXTRA_CONTENT_TYPE:kotlin.String) when the type of content played is voice audio 

 Value: 3

### EFFECT_AUXILIARY

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EFFECT_AUXILIARY: String
```

Effect connection mode is auxiliary.

Auxiliary effects must be created on session 0 (global output mix). In order for a MediaPlayer or AudioTrack to be fed into this effect, they must be explicitely attached to this effect and a send level must be specified.

Use the effect ID returned by [getId()](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#getId())to designate this particular effect when attaching it to the MediaPlayer or AudioTrack. 

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

This extra is for use with [ACTION_DISPLAY_AUDIO_EFFECT_CONTROL_PANEL](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ACTION_DISPLAY_AUDIO_EFFECT_CONTROL_PANEL:kotlin.String), [ACTION_OPEN_AUDIO_EFFECT_CONTROL_SESSION](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ACTION_OPEN_AUDIO_EFFECT_CONTROL_SESSION:kotlin.String) and [ACTION_CLOSE_AUDIO_EFFECT_CONTROL_SESSION](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ACTION_CLOSE_AUDIO_EFFECT_CONTROL_SESSION:kotlin.String) intents.

The extra value is of type int and is the audio session ID. 

 Value: "android.media.extra.AUDIO_SESSION"

**See Also**

- [android.media.MediaPlayer#getAudioSessionId()](https://developer.android.com/reference/kotlin/android/media/MediaPlayer.html#getAudioSessionId()) 

### EXTRA_CONTENT_TYPE

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_CONTENT_TYPE: String
```

Indicates which type of content is played by the application.

This extra is for use with [ACTION_DISPLAY_AUDIO_EFFECT_CONTROL_PANEL](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ACTION_DISPLAY_AUDIO_EFFECT_CONTROL_PANEL:kotlin.String) and [ACTION_OPEN_AUDIO_EFFECT_CONTROL_SESSION](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ACTION_OPEN_AUDIO_EFFECT_CONTROL_SESSION:kotlin.String) intents.

This information is used by the effect control application to customize UI and select appropriate default effect settings. The content type is one of the following:

- [CONTENT_TYPE_MUSIC](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#CONTENT_TYPE_MUSIC:kotlin.Int)
- [CONTENT_TYPE_MOVIE](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#CONTENT_TYPE_MOVIE:kotlin.Int)
- [CONTENT_TYPE_GAME](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#CONTENT_TYPE_GAME:kotlin.Int)
- [CONTENT_TYPE_VOICE](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#CONTENT_TYPE_VOICE:kotlin.Int)

If omitted, the content type defaults to [CONTENT_TYPE_MUSIC](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#CONTENT_TYPE_MUSIC:kotlin.Int). 

 Value: "android.media.extra.CONTENT_TYPE"

### EXTRA_PACKAGE_NAME

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_PACKAGE_NAME: String
```

Contains the package name of the calling application.

This extra is for use with [ACTION_OPEN_AUDIO_EFFECT_CONTROL_SESSION](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ACTION_OPEN_AUDIO_EFFECT_CONTROL_SESSION:kotlin.String) and [ACTION_CLOSE_AUDIO_EFFECT_CONTROL_SESSION](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ACTION_CLOSE_AUDIO_EFFECT_CONTROL_SESSION:kotlin.String) intents.

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

- [android.media.audiofx.AudioEffect.Descriptor](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect.Descriptor) 

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

Query all effects available on the platform. Returns an array of [android.media.audiofx.AudioEffect.Descriptor](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect.Descriptor) objects

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
| `listener` | [AudioEffect.OnControlStatusChangeListener](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect.OnControlStatusChangeListener)!: |

### setEnableStatusListener

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setEnableStatusListener(listener: AudioEffect.OnEnableStatusChangeListener!): Unit
```

Sets the listener AudioEffect notifies when the effect engine is enabled or disabled.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [AudioEffect.OnEnableStatusChangeListener](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect.OnEnableStatusChangeListener)!: |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SUCCESS](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#SUCCESS:kotlin.Int) in case of success, [ERROR_INVALID_OPERATION](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ERROR_INVALID_OPERATION:kotlin.Int) or [ERROR_DEAD_OBJECT](https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ERROR_DEAD_OBJECT:kotlin.Int) in case of failure. |

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
