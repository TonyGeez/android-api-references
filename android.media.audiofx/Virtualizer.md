# Virtualizer

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Virtualizer

Kotlin| [Java](Virtualizer.md) 
| --- | --- |

```
open class Virtualizer : AudioEffect
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.media.audiofx.AudioEffect](AudioEffect.md) ||
| | ↳ | [android.media.audiofx.Virtualizer](Virtualizer.md) |

| **This class was deprecated in API level 35.**
|
| use the [android.media.Spatializer](../android.media/Spatializer.md) class to query the capabilities of the platform with regards to spatialization, a different name for audio channel virtualization, and the [android.media.AudioAttributes.Builder#setSpatializationBehavior(int)](../android/media/AudioAttributes.Builder.md))to characterize how you want your content to be played when spatialization is supported.

An audio virtualizer is a general name for an effect to spatialize audio channels. The exact behavior of this effect is dependent on the number of audio input channels and the types and number of audio output channels of the device. For example, in the case of a stereo input and stereo headphone output, a stereo widening effect is used when this effect is turned on.

An application creates a Virtualizer object to instantiate and control a virtualizer engine in the audio framework.

The methods, parameter types and units exposed by the Virtualizer implementation are directly mapping those defined by the OpenSL ES 1.0.1 Specification (http://www.khronos.org/opensles/) for the SLVirtualizerItf interface. Please refer to this specification for more details.

To attach the Virtualizer to a particular AudioTrack or MediaPlayer, specify the audio session ID of this AudioTrack or MediaPlayer when constructing the Virtualizer.

NOTE: attaching a Virtualizer to the global audio output mix by use of session 0 is deprecated.

See [android.media.MediaPlayer#getAudioSessionId()](../android.media/MediaPlayer.md))for details on audio sessions.

See [android.media.audiofx.AudioEffect](AudioEffect.md) class for more details on controlling audio effects.

## Summary

| Nested classes ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [OnParameterChangeListener](../android/media/audiofx/Virtualizer.OnParameterChangeListener.md) The OnParameterChangeListener interface defines a method called by the Virtualizer when a parameter value has changed. |
| open | [Settings](../android/media/audiofx/Virtualizer.Settings.md) The Settings class regroups all virtualizer parameters. |

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARAM_STRENGTH](Virtualizer.md) Virtualizer effect strength. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARAM_STRENGTH_SUPPORTED](Virtualizer.md) Is strength parameter supported by virtualizer engine. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VIRTUALIZATION_MODE_AUTO](Virtualizer.md) A virtualization mode used to indicate the virtualizer effect must stop forcing the processing to a particular mode in [forceVirtualizationMode(int)](Virtualizer.md)). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VIRTUALIZATION_MODE_BINAURAL](Virtualizer.md) A virtualization mode typically used over headphones. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VIRTUALIZATION_MODE_OFF](Virtualizer.md) A virtualization mode indicating virtualization processing is not active. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VIRTUALIZATION_MODE_TRANSAURAL](Virtualizer.md) A virtualization mode typically used over speakers. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class [AudioEffect](AudioEffect.md) |----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_CLOSE_AUDIO_EFFECT_CONTROL_SESSION](AudioEffect.md) <br /> Intent to signal to the effect control application or service that an audio session is closed and that effects should not be applied anymore. The effect control application receiving this intent will delete all effects on this session and store current settings in package specific storage. The calling package name is indicated by the [EXTRA_PACKAGE_NAME](AudioEffect.md) extra and the audio session ID by the [EXTRA_AUDIO_SESSION](AudioEffect.md) extra. Both extras are mandatory. It is good practice for applications to broadcast this intent when music playback stops and/or when exiting to free system resources consumed by audio effect engines. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_DISPLAY_AUDIO_EFFECT_CONTROL_PANEL](AudioEffect.md) <br /> Intent to launch an audio effect control panel UI. The goal of this intent is to enable separate implementations of music/media player applications and audio effect control application or services. This will allow platform vendors to offer more advanced control options for standard effects or control for platform specific effects. The intent carries a number of extras used by the player application to communicate necessary pieces of information to the control panel application. The calling application must use the android.app.Activity#startActivityForResult(Intent, int) method to launch the control panel so that its package name is indicated and used by the control panel application to keep track of changes for this particular application. The [EXTRA_AUDIO_SESSION](AudioEffect.md) extra will indicate an audio session to which the audio effects should be applied. If no audio session is specified, either one of the follownig will happen: - If an audio session was previously opened by the calling application with [ACTION_OPEN_AUDIO_EFFECT_CONTROL_SESSION](AudioEffect.md) intent, the effect changes will be applied to that session. - If no audio session is opened, the changes will be stored in the package specific storage area and applied whenever a new audio session is opened by this application. The [EXTRA_CONTENT_TYPE](AudioEffect.md) extra will help the control panel application customize both the UI layout and the default audio effect settings if none are already stored for the calling application. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_OPEN_AUDIO_EFFECT_CONTROL_SESSION](AudioEffect.md) <br /> Intent to signal to the effect control application or service that a new audio session is opened and requires audio effects to be applied. This is different from [ACTION_DISPLAY_AUDIO_EFFECT_CONTROL_PANEL](AudioEffect.md) in that no UI should be displayed in this case. Music player applications can broadcast this intent before starting playback to make sure that any audio effect settings previously selected by the user are applied. The effect control application receiving this intent will look for previously stored settings for the calling application, create all required audio effects and apply the effect settings to the specified audio session. The calling package name is indicated by the [EXTRA_PACKAGE_NAME](AudioEffect.md) extra and the audio session ID by the [EXTRA_AUDIO_SESSION](AudioEffect.md) extra. Both extras are mandatory. If no stored settings are found for the calling application, default settings for the content type indicated by [EXTRA_CONTENT_TYPE](AudioEffect.md) will be applied. The default settings for a given content type are platform specific. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ALREADY_EXISTS](AudioEffect.md) <br /> Internal operation status. Not returned by any method. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_TYPE_GAME](AudioEffect.md) <br /> Value for [EXTRA_CONTENT_TYPE](AudioEffect.md) when the type of content played is game audio <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_TYPE_MOVIE](AudioEffect.md) <br /> Value for [EXTRA_CONTENT_TYPE](AudioEffect.md) when the type of content played is video or movie <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_TYPE_MUSIC](AudioEffect.md) <br /> Value for [EXTRA_CONTENT_TYPE](AudioEffect.md) when the type of content played is music <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENT_TYPE_VOICE](AudioEffect.md) <br /> Value for [EXTRA_CONTENT_TYPE](AudioEffect.md) when the type of content played is voice audio <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EFFECT_AUXILIARY](AudioEffect.md) <br /> Effect connection mode is auxiliary. Auxiliary effects must be created on session 0 (global output mix). In order for a MediaPlayer or AudioTrack to be fed into this effect, they must be explicitely attached to this effect and a send level must be specified. Use the effect ID returned by [getId()](AudioEffect.md))to designate this particular effect when attaching it to the MediaPlayer or AudioTrack. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EFFECT_INSERT](AudioEffect.md) <br /> Effect connection mode is insert. Specifying an audio session ID when creating the effect will insert this effect after all players in the same audio session. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EFFECT_POST_PROCESSING](AudioEffect.md) <br /> Effect connection mode is post processing. The audio post processing effects are attached to an audio output stream or device <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EFFECT_PRE_PROCESSING](AudioEffect.md) <br /> Effect connection mode is pre processing. The audio pre processing effects are attached to an audio input stream or device <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR](AudioEffect.md) <br /> Unspecified error. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_BAD_VALUE](AudioEffect.md) <br /> Operation failed due to bad parameter value. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_DEAD_OBJECT](AudioEffect.md) <br /> Operation failed due to dead remote object. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_INVALID_OPERATION](AudioEffect.md) <br /> Operation failed because it was requested in wrong state. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_NO_INIT](AudioEffect.md) <br /> Operation failed due to bad object initialization. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_NO_MEMORY](AudioEffect.md) <br /> Operation failed due to lack of memory. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_AUDIO_SESSION](AudioEffect.md) <br /> Contains the ID of the audio session the effects should be applied to. This extra is for use with [ACTION_DISPLAY_AUDIO_EFFECT_CONTROL_PANEL](AudioEffect.md), [ACTION_OPEN_AUDIO_EFFECT_CONTROL_SESSION](AudioEffect.md) and [ACTION_CLOSE_AUDIO_EFFECT_CONTROL_SESSION](AudioEffect.md) intents. The extra value is of type int and is the audio session ID. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_CONTENT_TYPE](AudioEffect.md) <br /> Indicates which type of content is played by the application. This extra is for use with [ACTION_DISPLAY_AUDIO_EFFECT_CONTROL_PANEL](AudioEffect.md) and [ACTION_OPEN_AUDIO_EFFECT_CONTROL_SESSION](AudioEffect.md) intents. This information is used by the effect control application to customize UI and select appropriate default effect settings. The content type is one of the following: - [CONTENT_TYPE_MUSIC](AudioEffect.md) - [CONTENT_TYPE_MOVIE](AudioEffect.md) - [CONTENT_TYPE_GAME](AudioEffect.md) - [CONTENT_TYPE_VOICE](AudioEffect.md) If omitted, the content type defaults to [CONTENT_TYPE_MUSIC](AudioEffect.md). <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_PACKAGE_NAME](AudioEffect.md) <br /> Contains the package name of the calling application. This extra is for use with [ACTION_OPEN_AUDIO_EFFECT_CONTROL_SESSION](AudioEffect.md) and [ACTION_CLOSE_AUDIO_EFFECT_CONTROL_SESSION](AudioEffect.md) intents. The extra value is a string containing the full package name. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SUCCESS](AudioEffect.md) <br /> Successful operation. <br /> | ||

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Virtualizer](Virtualizer.md))`(`priority:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `audioSession:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Class constructor. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [canVirtualize](Virtualizer.md))`(`inputChannelMask:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `virtualizationMode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Checks if the combination of a channel mask and virtualization mode is supported by this virtualizer. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [forceVirtualizationMode](Virtualizer.md))`(`virtualizationMode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Forces the virtualizer effect to use the given processing mode. |
| open [Virtualizer.Settings](../android/media/audiofx/Virtualizer.Settings.md)! | [getProperties](Virtualizer.md))`()` Gets the virtualizer properties. |
| --- | --- |
| open [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [getRoundedStrength](Virtualizer.md))`()` Gets the current strength of the effect. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getSpeakerAngles](Virtualizer.md))`(`inputChannelMask:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `virtualizationMode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `angles:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` Queries the virtual speaker angles (azimuth and elevation) for a combination of a channel mask and virtualization mode. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getStrengthSupported](Virtualizer.md))`()` Indicates whether setting strength is supported. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVirtualizationMode](Virtualizer.md))`()` Return the virtualization mode being used, if any. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setParameterListener](Virtualizer.md))`(`listener:` ` [Virtualizer.OnParameterChangeListener](../android/media/audiofx/Virtualizer.OnParameterChangeListener.md)!`)` Registers an OnParameterChangeListener interface. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setProperties](Virtualizer.md))`(`settings:` ` [Virtualizer.Settings](../android/media/audiofx/Virtualizer.Settings.md)!`)` Sets the virtualizer properties. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStrength](Virtualizer.md))`(`strength:` ` [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)`)` Sets the strength of the virtualizer effect. |

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

**Deprecated:** *Deprecated in Java.*

Virtualizer effect strength. Parameter ID for [android.media.audiofx.Virtualizer.OnParameterChangeListener](../android/media/audiofx/Virtualizer.OnParameterChangeListener.md) 

 Value: 1

### PARAM_STRENGTH_SUPPORTED

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PARAM_STRENGTH_SUPPORTED: Int
```

**Deprecated:** *Deprecated in Java.*

Is strength parameter supported by virtualizer engine. Parameter ID for getParameter(). 

 Value: 0

### VIRTUALIZATION_MODE_AUTO

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VIRTUALIZATION_MODE_AUTO: Int
```

**Deprecated:** *Deprecated in Java.*

A virtualization mode used to indicate the virtualizer effect must stop forcing the processing to a particular mode in [forceVirtualizationMode(int)](Virtualizer.md)). 

 Value: 1

### VIRTUALIZATION_MODE_BINAURAL

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VIRTUALIZATION_MODE_BINAURAL: Int
```

**Deprecated:** *Deprecated in Java.*

A virtualization mode typically used over headphones. Binaural virtualization describes an audio processing configuration for virtualization where the left and right channels are respectively reaching the left and right ear of the user, without also feeding the opposite ear (as is the case when listening over speakers).

Such a mode is therefore meant to be used when audio is playing over stereo wired headphones or headsets, but also stereo headphones through a wireless A2DP Bluetooth link.

See [canVirtualize(int,int)](Virtualizer.md))to verify this mode is supported by this Virtualizer. 

 Value: 2

### VIRTUALIZATION_MODE_OFF

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VIRTUALIZATION_MODE_OFF: Int
```

**Deprecated:** *Deprecated in Java.*

A virtualization mode indicating virtualization processing is not active. See [getVirtualizationMode()](Virtualizer.md))as one of the possible return value. 

 Value: 0

### VIRTUALIZATION_MODE_TRANSAURAL

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VIRTUALIZATION_MODE_TRANSAURAL: Int
```

**Deprecated:** *Deprecated in Java.*

A virtualization mode typically used over speakers. Transaural virtualization describes an audio processing configuration that differs from binaural (as described in [VIRTUALIZATION_MODE_BINAURAL](Virtualizer.md) in that cross-talk is present, i.e. audio played from the left channel also reaches the right ear of the user, and vice-versa.

When supported, such a mode is therefore meant to be used when audio is playing over the built-in stereo speakers of a device, if they are featured.

See [canVirtualize(int,int)](Virtualizer.md))to verify this mode is supported by this Virtualizer. 

 Value: 3

## Public constructors

### Virtualizer

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Virtualizer(
    priority: Int, 
    audioSession: Int)
```

Class constructor.

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `priority` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the priority level requested by the application for controlling the Virtualizer engine. As the same engine can be shared by several applications, this parameter indicates how much the requesting application needs control of effect parameters. The normal priority is 0, above normal is a positive number, below normal a negative number. |
| `audioSession` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):system wide unique audio session identifier. The Virtualizer will be attached to the MediaPlayer or AudioTrack in the same audio session. |

| Exceptions ||
|-------------------------------------------|---|
| `java.lang.IllegalStateException` | |
| `java.lang.IllegalArgumentException` | |
| `java.lang.UnsupportedOperationException` | |
| --- | --- |
| `java.lang.RuntimeException` | |

## Public methods

### canVirtualize

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun canVirtualize(
    inputChannelMask: Int, 
    virtualizationMode: Int
): Boolean
```

**Deprecated:** *Deprecated in Java.*

Checks if the combination of a channel mask and virtualization mode is supported by this virtualizer. Some virtualizer implementations may only support binaural processing (i.e. only support headphone output, see [VIRTUALIZATION_MODE_BINAURAL](Virtualizer.md)), some may support transaural processing (i.e. for speaker output, see [VIRTUALIZATION_MODE_TRANSAURAL](Virtualizer.md)) for the built-in speakers. Use this method to query the virtualizer implementation capabilities.

| Parameters ||
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `inputChannelMask` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the channel mask of the content to virtualize. |
| `virtualizationMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the mode for which virtualization processing is to be performed, one of [VIRTUALIZATION_MODE_BINAURAL](Virtualizer.md), [VIRTUALIZATION_MODE_TRANSAURAL](Virtualizer.md). Value is [android.media.audiofx.Virtualizer#VIRTUALIZATION_MODE_BINAURAL](Virtualizer.md), or [android.media.audiofx.Virtualizer#VIRTUALIZATION_MODE_TRANSAURAL](Virtualizer.md) |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the combination of channel mask and virtualization mode is supported, false otherwise. An indication that a certain channel mask is not supported doesn't necessarily mean you cannot play content with that channel mask, it more likely implies the content will be downmixed before being virtualized. For instance a virtualizer that only supports a mask such as [AudioFormat.CHANNEL_OUT_STEREO](../android.media/AudioFormat.md) will still be able to process content with a mask of [AudioFormat.CHANNEL_OUT_5POINT1](../android.media/AudioFormat.md), but will downmix the content to stereo first, and then will virtualize, as opposed to virtualizing each channel individually. |

| Exceptions ||
|-------------------------------------------|---|
| `java.lang.IllegalStateException` | |
| `java.lang.IllegalArgumentException` | |
| `java.lang.UnsupportedOperationException` | |
| --- | --- |

### forceVirtualizationMode

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun forceVirtualizationMode(virtualizationMode: Int): Boolean
```

**Deprecated:** *Deprecated in Java.*

Forces the virtualizer effect to use the given processing mode. The effect must be enabled for the forced mode to be applied.

| Parameters ||
|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `virtualizationMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):one of [VIRTUALIZATION_MODE_BINAURAL](Virtualizer.md), [VIRTUALIZATION_MODE_TRANSAURAL](Virtualizer.md) to force a particular processing mode, or {@value #VIRTUALIZATION_MODE_AUTO} to stop forcing a mode. Value is [android.media.audiofx.Virtualizer#VIRTUALIZATION_MODE_AUTO](Virtualizer.md), [android.media.audiofx.Virtualizer#VIRTUALIZATION_MODE_BINAURAL](Virtualizer.md), or [android.media.audiofx.Virtualizer#VIRTUALIZATION_MODE_TRANSAURAL](Virtualizer.md) |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the processing mode is supported, and it is successfully set, or forcing was successfully disabled, false otherwise. |

| Exceptions ||
|-------------------------------------------|---|
| `java.lang.IllegalStateException` | |
| `java.lang.IllegalArgumentException` | |
| `java.lang.UnsupportedOperationException` | |
| --- | --- |

### getProperties

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getProperties(): Virtualizer.Settings!
```

**Deprecated:** *Deprecated in Java.*

Gets the virtualizer properties. This method is useful when a snapshot of current virtualizer settings must be saved by the application.

| Return ||
|--------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Virtualizer.Settings](../android/media/audiofx/Virtualizer.Settings.md)! | a Virtualizer.Settings object containing all current parameters values |

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

**Deprecated:** *Deprecated in Java.*

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

### getSpeakerAngles

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSpeakerAngles(
    inputChannelMask: Int, 
    virtualizationMode: Int, 
    angles: IntArray!
): Boolean
```

**Deprecated:** *Deprecated in Java.*

Queries the virtual speaker angles (azimuth and elevation) for a combination of a channel mask and virtualization mode. If the virtualization configuration (mask and mode) is supported (see [canVirtualize(int,int)](Virtualizer.md)), the array angles will contain upon return the definition of each virtual speaker and its azimuth and elevation angles relative to the listener. 
Note that in some virtualizer implementations, the angles may be strength-dependent.

| Parameters ||
|----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `inputChannelMask` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the channel mask of the content to virtualize. |
| `virtualizationMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the mode for which virtualization processing is to be performed, one of [VIRTUALIZATION_MODE_BINAURAL](Virtualizer.md), [VIRTUALIZATION_MODE_TRANSAURAL](Virtualizer.md). Value is [android.media.audiofx.Virtualizer#VIRTUALIZATION_MODE_BINAURAL](Virtualizer.md), or [android.media.audiofx.Virtualizer#VIRTUALIZATION_MODE_TRANSAURAL](Virtualizer.md) |
| `angles` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!:a non-null array whose length is 3 times the number of channels in the channel mask. If the method indicates the configuration is supported, the array will contain upon return triplets of values: for each channel`i`among the channels of the mask: - the element at index`3*i`in the array contains the speaker identification (e.g. [AudioFormat.CHANNEL_OUT_FRONT_LEFT](../android.media/AudioFormat.md)), - the element at index`3*i+1`contains its corresponding azimuth angle expressed in degrees, where 0 is the direction the listener faces, 180 is behind the listener, and -90 is to her/his left, - the element at index`3*i+2`contains its corresponding elevation angle where +90 is directly above the listener, 0 is the horizontal plane, and -90 is directly below the listener. |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the combination of channel mask and virtualization mode is supported, false otherwise. |

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

**Deprecated:** *Deprecated in Java.*

Indicates whether setting strength is supported. If this method returns false, only one strength is supported and the setStrength() method always rounds to that value.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true is strength parameter is supported, false otherwise |

### getVirtualizationMode

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getVirtualizationMode(): Int
```

**Deprecated:** *Deprecated in Java.*

Return the virtualization mode being used, if any.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the virtualization mode being used. If virtualization is not active, the virtualization mode will be [VIRTUALIZATION_MODE_OFF](Virtualizer.md). Otherwise the value will be [VIRTUALIZATION_MODE_BINAURAL](Virtualizer.md) or [VIRTUALIZATION_MODE_TRANSAURAL](Virtualizer.md). Virtualization may not be active either because the effect is not enabled or because the current output device is not compatible with this virtualization implementation. |

| Exceptions ||
|-------------------------------------------|---|
| `java.lang.IllegalStateException` | |
| `java.lang.UnsupportedOperationException` | |

### setParameterListener

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setParameterListener(listener: Virtualizer.OnParameterChangeListener!): Unit
```

**Deprecated:** *Deprecated in Java.*

Registers an OnParameterChangeListener interface.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [Virtualizer.OnParameterChangeListener](../android/media/audiofx/Virtualizer.OnParameterChangeListener.md)!:OnParameterChangeListener interface registered |

### setProperties

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setProperties(settings: Virtualizer.Settings!): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the virtualizer properties. This method is useful when virtualizer settings have to be applied from a previous backup.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `settings` | [Virtualizer.Settings](../android/media/audiofx/Virtualizer.Settings.md)!:a Virtualizer.Settings object containing the properties to apply |

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

**Deprecated:** *Deprecated in Java.*

Sets the strength of the virtualizer effect. If the implementation does not support per mille accuracy for setting the strength, it is allowed to round the given strength to the nearest supported value. You can use the [getRoundedStrength()](Virtualizer.md))method to query the (possibly rounded) value that was actually set.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `strength` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html):strength of the effect. The valid range for strength strength is \[0, 1000\], where 0 per mille designates the mildest effect and 1000 per mille designates the strongest. |

| Exceptions ||
|-------------------------------------------|---|
| `java.lang.IllegalStateException` | |
| `java.lang.IllegalArgumentException` | |
| `java.lang.UnsupportedOperationException` | |
| --- | --- |
