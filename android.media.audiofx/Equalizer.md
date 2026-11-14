Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Equalizer

Kotlin | [Java](Equalizer.md)
| --- | --- |

```
open class Equalizer : AudioEffect
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.media.audiofx.AudioEffect](AudioEffect.md) ||
| | ↳ | [android.media.audiofx.Equalizer](Equalizer.md) |

An Equalizer is used to alter the frequency response of a particular music source or of the main output mix.

An application creates an Equalizer object to instantiate and control an Equalizer engine in the audio framework. The application can either simply use predefined presets or have a more precise control of the gain in each frequency band controlled by the equalizer.

The methods, parameter types and units exposed by the Equalizer implementation are directly mapping those defined by the OpenSL ES 1.0.1 Specification (http://www.khronos.org/opensles/) for the SLEqualizerItf interface. Please refer to this specification for more details.

To attach the Equalizer to a particular AudioTrack or MediaPlayer, specify the audio session ID of this AudioTrack or MediaPlayer when constructing the Equalizer.

NOTE: attaching an Equalizer to the global audio output mix by use of session 0 is deprecated.

See `https://developer.android.com/reference/kotlin/android/media/MediaPlayer.html#getAudioSessionId()` for details on audio sessions.

See `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect` class for more details on controlling audio effects.

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/media/audiofx/Equalizer.OnParameterChangeListener` The OnParameterChangeListener interface defines a method called by the Equalizer when a parameter value has changed. |
| open | `https://developer.android.com/reference/kotlin/android/media/audiofx/Equalizer.Settings` The Settings class regroups all equalizer parameters. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/audiofx/Equalizer#PARAM_BAND_FREQ_RANGE:kotlin.Int` Band frequency range. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/audiofx/Equalizer#PARAM_BAND_LEVEL:kotlin.Int` Band level. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/audiofx/Equalizer#PARAM_CENTER_FREQ:kotlin.Int` Band center frequency. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/audiofx/Equalizer#PARAM_CURRENT_PRESET:kotlin.Int` Current preset. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/audiofx/Equalizer#PARAM_GET_BAND:kotlin.Int` Band for a given frequency. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/audiofx/Equalizer#PARAM_GET_NUM_OF_PRESETS:kotlin.Int` Request number of presets. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/audiofx/Equalizer#PARAM_GET_PRESET_NAME:kotlin.Int` Request preset name. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/audiofx/Equalizer#PARAM_LEVEL_RANGE:kotlin.Int` Band level range. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/audiofx/Equalizer#PARAM_NUM_BANDS:kotlin.Int` Number of bands. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/audiofx/Equalizer#PARAM_STRING_SIZE_MAX:kotlin.Int` Maximum size for preset name |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ACTION_CLOSE_AUDIO_EFFECT_CONTROL_SESSION:kotlin.String` Intent to signal to the effect control application or service that an audio session is closed and that effects should not be applied anymore. The effect control application receiving this intent will delete all effects on this session and store current settings in package specific storage. The calling package name is indicated by the `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EXTRA_PACKAGE_NAME:kotlin.String` extra and the audio session ID by the `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EXTRA_AUDIO_SESSION:kotlin.String` extra. Both extras are mandatory. It is good practice for applications to broadcast this intent when music playback stops and/or when exiting to free system resources consumed by audio effect engines. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ACTION_DISPLAY_AUDIO_EFFECT_CONTROL_PANEL:kotlin.String` Intent to launch an audio effect control panel UI. The goal of this intent is to enable separate implementations of music/media player applications and audio effect control application or services. This will allow platform vendors to offer more advanced control options for standard effects or control for platform specific effects. The intent carries a number of extras used by the player application to communicate necessary pieces of information to the control panel application. The calling application must use the android.app.Activity#startActivityForResult(Intent, int) method to launch the control panel so that its package name is indicated and used by the control panel application to keep track of changes for this particular application. The `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EXTRA_AUDIO_SESSION:kotlin.String` extra will indicate an audio session to which the audio effects should be applied. If no audio session is specified, either one of the follownig will happen: - If an audio session was previously opened by the calling application with `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ACTION_OPEN_AUDIO_EFFECT_CONTROL_SESSION:kotlin.String` intent, the effect changes will be applied to that session. - If no audio session is opened, the changes will be stored in the package specific storage area and applied whenever a new audio session is opened by this application. The `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EXTRA_CONTENT_TYPE:kotlin.String` extra will help the control panel application customize both the UI layout and the default audio effect settings if none are already stored for the calling application. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ACTION_OPEN_AUDIO_EFFECT_CONTROL_SESSION:kotlin.String` Intent to signal to the effect control application or service that a new audio session is opened and requires audio effects to be applied. This is different from `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ACTION_DISPLAY_AUDIO_EFFECT_CONTROL_PANEL:kotlin.String` in that no UI should be displayed in this case. Music player applications can broadcast this intent before starting playback to make sure that any audio effect settings previously selected by the user are applied. The effect control application receiving this intent will look for previously stored settings for the calling application, create all required audio effects and apply the effect settings to the specified audio session. The calling package name is indicated by the `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EXTRA_PACKAGE_NAME:kotlin.String` extra and the audio session ID by the `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EXTRA_AUDIO_SESSION:kotlin.String` extra. Both extras are mandatory. If no stored settings are found for the calling application, default settings for the content type indicated by `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EXTRA_CONTENT_TYPE:kotlin.String` will be applied. The default settings for a given content type are platform specific. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ALREADY_EXISTS:kotlin.Int` Internal operation status. Not returned by any method. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#CONTENT_TYPE_GAME:kotlin.Int` Value for `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EXTRA_CONTENT_TYPE:kotlin.String` when the type of content played is game audio <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#CONTENT_TYPE_MOVIE:kotlin.Int` Value for `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EXTRA_CONTENT_TYPE:kotlin.String` when the type of content played is video or movie <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#CONTENT_TYPE_MUSIC:kotlin.Int` Value for `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EXTRA_CONTENT_TYPE:kotlin.String` when the type of content played is music <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#CONTENT_TYPE_VOICE:kotlin.Int` Value for `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EXTRA_CONTENT_TYPE:kotlin.String` when the type of content played is voice audio <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_AUXILIARY:kotlin.String` Effect connection mode is auxiliary. Auxiliary effects must be created on session 0 (global output mix). In order for a MediaPlayer or AudioTrack to be fed into this effect, they must be explicitely attached to this effect and a send level must be specified. Use the effect ID returned by `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#getId()` to designate this particular effect when attaching it to the MediaPlayer or AudioTrack. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_INSERT:kotlin.String` Effect connection mode is insert. Specifying an audio session ID when creating the effect will insert this effect after all players in the same audio session. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_POST_PROCESSING:kotlin.String` Effect connection mode is post processing. The audio post processing effects are attached to an audio output stream or device <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_PRE_PROCESSING:kotlin.String` Effect connection mode is pre processing. The audio pre processing effects are attached to an audio input stream or device <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ERROR:kotlin.Int` Unspecified error. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ERROR_BAD_VALUE:kotlin.Int` Operation failed due to bad parameter value. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ERROR_DEAD_OBJECT:kotlin.Int` Operation failed due to dead remote object. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ERROR_INVALID_OPERATION:kotlin.Int` Operation failed because it was requested in wrong state. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ERROR_NO_INIT:kotlin.Int` Operation failed due to bad object initialization. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ERROR_NO_MEMORY:kotlin.Int` Operation failed due to lack of memory. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EXTRA_AUDIO_SESSION:kotlin.String` Contains the ID of the audio session the effects should be applied to. This extra is for use with `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ACTION_DISPLAY_AUDIO_EFFECT_CONTROL_PANEL:kotlin.String`, `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ACTION_OPEN_AUDIO_EFFECT_CONTROL_SESSION:kotlin.String` and `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ACTION_CLOSE_AUDIO_EFFECT_CONTROL_SESSION:kotlin.String` intents. The extra value is of type int and is the audio session ID. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EXTRA_CONTENT_TYPE:kotlin.String` Indicates which type of content is played by the application. This extra is for use with `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ACTION_DISPLAY_AUDIO_EFFECT_CONTROL_PANEL:kotlin.String` and `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ACTION_OPEN_AUDIO_EFFECT_CONTROL_SESSION:kotlin.String` intents. This information is used by the effect control application to customize UI and select appropriate default effect settings. The content type is one of the following: - `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#CONTENT_TYPE_MUSIC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#CONTENT_TYPE_MOVIE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#CONTENT_TYPE_GAME:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#CONTENT_TYPE_VOICE:kotlin.Int` If omitted, the content type defaults to `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#CONTENT_TYPE_MUSIC:kotlin.Int`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EXTRA_PACKAGE_NAME:kotlin.String` Contains the package name of the calling application. This extra is for use with `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ACTION_OPEN_AUDIO_EFFECT_CONTROL_SESSION:kotlin.String` and `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#ACTION_CLOSE_AUDIO_EFFECT_CONTROL_SESSION:kotlin.String` intents. The extra value is a string containing the full package name. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#SUCCESS:kotlin.Int` Successful operation. <br /> | ||

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/media/audiofx/Equalizer#Equalizer(kotlin.Int,%20kotlin.Int)(priority: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, audioSession: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Class constructor. |

| Public methods ||
|---|---|
| open [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | `https://developer.android.com/reference/kotlin/android/media/audiofx/Equalizer#getBand(kotlin.Int)(frequency: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Gets the band that has the most effect on the given frequency. |
| open [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | `https://developer.android.com/reference/kotlin/android/media/audiofx/Equalizer#getBandFreqRange(kotlin.Short)(band: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)` Gets the frequency range of the given frequency band. |
| open [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | `https://developer.android.com/reference/kotlin/android/media/audiofx/Equalizer#getBandLevel(kotlin.Short)(band: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)` Gets the gain set for the given equalizer band. |
| --- | --- |
| open [ShortArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short-array/index.html)! | `https://developer.android.com/reference/kotlin/android/media/audiofx/Equalizer#getBandLevelRange()()` Gets the level range for use by `https://developer.android.com/reference/kotlin/android/media/audiofx/Equalizer#setBandLevel(kotlin.Short,%20kotlin.Short)`. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/audiofx/Equalizer#getCenterFreq(kotlin.Short)(band: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)` Gets the center frequency of the given band. |
| open [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | `https://developer.android.com/reference/kotlin/android/media/audiofx/Equalizer#getCurrentPreset()()` Gets current preset. |
| --- | --- |
| open [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | `https://developer.android.com/reference/kotlin/android/media/audiofx/Equalizer#getNumberOfBands()()` Gets the number of frequency bands supported by the Equalizer engine. |
| open [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | `https://developer.android.com/reference/kotlin/android/media/audiofx/Equalizer#getNumberOfPresets()()` Gets the total number of presets the equalizer supports. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/media/audiofx/Equalizer#getPresetName(kotlin.Short)(preset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)` Gets the preset name based on the index. |
| --- | --- |
| open [Equalizer.Settings](../android/media/audiofx/Equalizer.Settings.md)! | `https://developer.android.com/reference/kotlin/android/media/audiofx/Equalizer#getProperties()()` Gets the equalizer properties. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/audiofx/Equalizer#setBandLevel(kotlin.Short,%20kotlin.Short)(band: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html, level: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)` Sets the given equalizer band to the given gain value. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/audiofx/Equalizer#setParameterListener(android.media.audiofx.Equalizer.OnParameterChangeListener)(listener: https://developer.android.com/reference/kotlin/android/media/audiofx/Equalizer.OnParameterChangeListener!)` Registers an OnParameterChangeListener interface. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/audiofx/Equalizer#setProperties(android.media.audiofx.Equalizer.Settings)(settings: https://developer.android.com/reference/kotlin/android/media/audiofx/Equalizer.Settings!)` Sets the equalizer properties. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/audiofx/Equalizer#usePreset(kotlin.Short)(preset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)` Sets the equalizer according to the given preset. |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#finalize()()` Called by the garbage collector on an object when garbage collection determines that there are no more references to the object. A subclass overrides the `finalize` method to dispose of system resources or to perform other cleanup. The general contract of `finalize` is that it is invoked if and when the Java virtual machine has determined that there is no longer any means by which this object can be accessed by any thread that has not yet died, except as a result of an action taken by the finalization of some other object or class which is ready to be finalized. The `finalize` method may take any action, including making this object available again to other threads; the usual purpose of `finalize`, however, is to perform cleanup actions before the object is irrevocably discarded. For example, the finalize method for an object that represents an input/output connection might perform explicit I/O transactions to break the connection before the object is permanently discarded. The `finalize` method of class `Object` performs no special action; it simply returns normally. Subclasses of `Object` may override this definition. The Java programming language does not guarantee which thread will invoke the `finalize` method for any given object. It is guaranteed, however, that the thread that invokes finalize will not be holding any user-visible synchronization locks when finalize is invoked. If an uncaught exception is thrown by the finalize method, the exception is ignored and finalization of that object terminates. After the `finalize` method has been invoked for an object, no further action is taken until the Java virtual machine has again determined that there is no longer any means by which this object can be accessed by any thread that has not yet died, including possible actions by other objects or classes which are ready to be finalized, at which point the object may be discarded. The `finalize` method is never invoked more than once by a Java virtual machine for any given object. Any exception thrown by the `finalize` method causes the finalization of this object to be halted, but is otherwise ignored. <br /> | | `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect.Descriptor!` | `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#getDescriptor()()` Get the effect descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#getEnabled()()` Returns effect enabled state <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#getId()()` Returns effect unique identifier. This system wide unique identifier can be used to attach this effect to a MediaPlayer or an AudioTrack when the effect is an auxiliary effect (Reverb) <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#hasControl()()` Checks if this AudioEffect object is controlling the effect engine. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect.Descriptor!>!` | `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#queryEffects()()` Query all effects available on the platform. Returns an array of `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect.Descriptor` objects <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#release()()` Releases the native AudioEffect resources. It is a good practice to release the effect engine when not in use as control can be returned to other applications or the native resources released. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#setControlStatusListener(android.media.audiofx.AudioEffect.OnControlStatusChangeListener)(listener: https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect.OnControlStatusChangeListener!)` Sets the listener AudioEffect notifies when the effect engine control is taken or returned. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#setEnableStatusListener(android.media.audiofx.AudioEffect.OnEnableStatusChangeListener)(listener: https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect.OnEnableStatusChangeListener!)` Sets the listener AudioEffect notifies when the effect engine is enabled or disabled. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#setEnabled(kotlin.Boolean)(enabled: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Enable or disable the effect. Creating an audio effect does not automatically apply this effect on the audio source. It creates the resources necessary to process this effect but the audio signal is still bypassed through the effect engine. Calling this method will make that the effect is actually applied or not to the audio content being played in the corresponding audio session. <br /> | ||

| Inherited properties ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect` |---|---| | `https://developer.android.com/reference/kotlin/java/util/UUID.html#!` | `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_TYPE_AEC:java.util.UUID` UUID for Acoustic Echo Canceler (AEC) <br /> | | `https://developer.android.com/reference/kotlin/java/util/UUID.html#!` | `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_TYPE_AGC:java.util.UUID` UUID for Automatic Gain Control (AGC) <br /> | | `https://developer.android.com/reference/kotlin/java/util/UUID.html#!` | `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_TYPE_BASS_BOOST:java.util.UUID` UUID for bass boost effect <br /> | | `https://developer.android.com/reference/kotlin/java/util/UUID.html#!` | `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_TYPE_DYNAMICS_PROCESSING:java.util.UUID` UUID for Dynamics Processing <br /> | | `https://developer.android.com/reference/kotlin/java/util/UUID.html#!` | `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_TYPE_ENV_REVERB:java.util.UUID` UUID for environmental reverberation effect <br /> | | `https://developer.android.com/reference/kotlin/java/util/UUID.html#!` | `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_TYPE_EQUALIZER:java.util.UUID` UUID for equalizer effect <br /> | | `https://developer.android.com/reference/kotlin/java/util/UUID.html#` | `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_TYPE_HAPTIC_GENERATOR:java.util.UUID` UUID for Haptic Generator. <br /> | | `https://developer.android.com/reference/kotlin/java/util/UUID.html#!` | `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_TYPE_LOUDNESS_ENHANCER:java.util.UUID` UUID for Loudness Enhancer <br /> | | `https://developer.android.com/reference/kotlin/java/util/UUID.html#!` | `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_TYPE_NS:java.util.UUID` UUID for Noise Suppressor (NS) <br /> | | `https://developer.android.com/reference/kotlin/java/util/UUID.html#!` | `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_TYPE_PRESET_REVERB:java.util.UUID` UUID for preset reverberation effect <br /> | | `https://developer.android.com/reference/kotlin/java/util/UUID.html#!` | `https://developer.android.com/reference/kotlin/android/media/audiofx/AudioEffect#EFFECT_TYPE_VIRTUALIZER:java.util.UUID` UUID for virtualizer effect <br /> | ||

## Constants

### PARAM_BAND_FREQ_RANGE

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PARAM_BAND_FREQ_RANGE: Int
```

Band frequency range. Parameter ID for `https://developer.android.com/reference/kotlin/android/media/audiofx/Equalizer.OnParameterChangeListener`

 Value: 4

### PARAM_BAND_LEVEL

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PARAM_BAND_LEVEL: Int
```

Band level. Parameter ID for OnParameterChangeListener

 Value: 2

### PARAM_CENTER_FREQ

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PARAM_CENTER_FREQ: Int
```

Band center frequency. Parameter ID for OnParameterChangeListener

 Value: 3

### PARAM_CURRENT_PRESET

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PARAM_CURRENT_PRESET: Int
```

Current preset. Parameter ID for OnParameterChangeListener

 Value: 6

### PARAM_GET_BAND

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PARAM_GET_BAND: Int
```

Band for a given frequency. Parameter ID for OnParameterChangeListener

 Value: 5

### PARAM_GET_NUM_OF_PRESETS

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PARAM_GET_NUM_OF_PRESETS: Int
```

Request number of presets. Parameter ID for OnParameterChangeListener

 Value: 7

### PARAM_GET_PRESET_NAME

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PARAM_GET_PRESET_NAME: Int
```

Request preset name. Parameter ID for OnParameterChangeListener

 Value: 8

### PARAM_LEVEL_RANGE

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PARAM_LEVEL_RANGE: Int
```

Band level range. Parameter ID for OnParameterChangeListener

 Value: 1

### PARAM_NUM_BANDS

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PARAM_NUM_BANDS: Int
```

Number of bands. Parameter ID for OnParameterChangeListener

 Value: 0

### PARAM_STRING_SIZE_MAX

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PARAM_STRING_SIZE_MAX: Int
```

Maximum size for preset name

 Value: 32

## Public constructors

### Equalizer

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
Equalizer(
    priority: Int, 
    audioSession: Int)
```

Class constructor.

| Parameters ||
|---|---|
| `priority` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the priority level requested by the application for controlling the Equalizer engine. As the same engine can be shared by several applications, this parameter indicates how much the requesting application needs control of effect parameters. The normal priority is 0, above normal is a positive number, below normal a negative number. |
| `audioSession` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): system wide unique audio session identifier. The Equalizer will be attached to the MediaPlayer or AudioTrack in the same audio session. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | |
| `java.lang.IllegalStateException` | |
| `java.lang.RuntimeException` | |
| --- | --- |
| `java.lang.UnsupportedOperationException` | |

## Public methods

### getBand

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getBand(frequency: Int): Short
```

Gets the band that has the most effect on the given frequency.

| Parameters ||
|---|---|
| `frequency` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): frequency in milliHertz which is to be equalized via the returned band. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html` | the frequency band that has most effect on the given frequency. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | |
| `java.lang.IllegalStateException` | |
| `java.lang.UnsupportedOperationException` | |
| --- | --- |

### getBandFreqRange

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getBandFreqRange(band: Short): IntArray!
```

Gets the frequency range of the given frequency band.

| Parameters ||
|---|---|
| `band` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html): frequency band whose frequency range is requested. The numbering of the bands starts from 0 and ends at (number of bands - 1). |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` | the frequency range in millHertz in an array of integers. The first element is the lower limit of the range, the second element the upper limit. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | |
| `java.lang.IllegalStateException` | |
| `java.lang.UnsupportedOperationException` | |
| --- | --- |

### getBandLevel

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getBandLevel(band: Short): Short
```

Gets the gain set for the given equalizer band.

| Parameters ||
|---|---|
| `band` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html): frequency band whose gain is requested. The numbering of the bands starts from 0 and ends at (number of bands - 1). |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html` | the gain in millibels of the given band. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | |
| `java.lang.IllegalStateException` | |
| `java.lang.UnsupportedOperationException` | |
| --- | --- |

### getBandLevelRange

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getBandLevelRange(): ShortArray!
```

Gets the level range for use by `https://developer.android.com/reference/kotlin/android/media/audiofx/Equalizer#setBandLevel(kotlin.Short,%20kotlin.Short)`. The level is expressed in milliBel.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short-array/index.html!` | the band level range in an array of short integers. The first element is the lower limit of the range, the second element the upper limit. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | |
| `java.lang.IllegalStateException` | |
| `java.lang.UnsupportedOperationException` | |
| --- | --- |

### getCenterFreq

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCenterFreq(band: Short): Int
```

Gets the center frequency of the given band.

| Parameters ||
|---|---|
| `band` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html): frequency band whose center frequency is requested. The numbering of the bands starts from 0 and ends at (number of bands - 1). |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the center frequency in milliHertz |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | |
| `java.lang.IllegalStateException` | |
| `java.lang.UnsupportedOperationException` | |
| --- | --- |

### getCurrentPreset

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCurrentPreset(): Short
```

Gets current preset.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html` | the preset that is set at the moment. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | |
| `java.lang.IllegalStateException` | |
| `java.lang.UnsupportedOperationException` | |
| --- | --- |

### getNumberOfBands

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getNumberOfBands(): Short
```

Gets the number of frequency bands supported by the Equalizer engine.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html` | the number of bands |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | |
| `java.lang.IllegalStateException` | |
| `java.lang.UnsupportedOperationException` | |
| --- | --- |

### getNumberOfPresets

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getNumberOfPresets(): Short
```

Gets the total number of presets the equalizer supports. The presets will have indices \[0, number of presets-1\].

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html` | the number of presets the equalizer supports. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | |
| `java.lang.IllegalStateException` | |
| `java.lang.UnsupportedOperationException` | |
| --- | --- |

### getPresetName

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPresetName(preset: Short): String!
```

Gets the preset name based on the index.

| Parameters ||
|---|---|
| `preset` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html): index of the preset. The valid range is \[0, number of presets-1\]. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | a string containing the name of the given preset. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | |
| `java.lang.IllegalStateException` | |
| `java.lang.UnsupportedOperationException` | |
| --- | --- |

### getProperties

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getProperties(): Equalizer.Settings!
```

Gets the equalizer properties. This method is useful when a snapshot of current equalizer settings must be saved by the application.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/media/audiofx/Equalizer.Settings!` | an Equalizer.Settings object containing all current parameters values |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | |
| `java.lang.IllegalStateException` | |
| `java.lang.UnsupportedOperationException` | |
| --- | --- |

### setBandLevel

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setBandLevel(
    band: Short, 
    level: Short
): Unit
```

Sets the given equalizer band to the given gain value.

| Parameters ||
|---|---|
| `band` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html): frequency band that will have the new gain. The numbering of the bands starts from 0 and ends at (number of bands - 1). |
| `level` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html): new gain in millibels that will be set to the given band. getBandLevelRange() will define the maximum and minimum values. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | |
| `java.lang.IllegalStateException` | |
| `java.lang.UnsupportedOperationException` | |
| --- | --- |

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/audiofx/Equalizer#getNumberOfBands()`

### setParameterListener

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setParameterListener(listener: Equalizer.OnParameterChangeListener!): Unit
```

Registers an OnParameterChangeListener interface.

| Parameters ||
|---|---|
| `listener` | [Equalizer.OnParameterChangeListener](../android/media/audiofx/Equalizer.OnParameterChangeListener.md)!: OnParameterChangeListener interface registered |

### setProperties

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setProperties(settings: Equalizer.Settings!): Unit
```

Sets the equalizer properties. This method is useful when equalizer settings have to be applied from a previous backup.

| Parameters ||
|---|---|
| `settings` | [Equalizer.Settings](../android/media/audiofx/Equalizer.Settings.md)!: an Equalizer.Settings object containing the properties to apply |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | |
| `java.lang.IllegalStateException` | |
| `java.lang.UnsupportedOperationException` | |
| --- | --- |

### usePreset

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun usePreset(preset: Short): Unit
```

Sets the equalizer according to the given preset.

| Parameters ||
|---|---|
| `preset` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html): new preset that will be taken into use. The valid range is \[0, number of presets-1\]. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | |
| `java.lang.IllegalStateException` | |
| `java.lang.UnsupportedOperationException` | |
| --- | --- |

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/audiofx/Equalizer#getNumberOfPresets()`
