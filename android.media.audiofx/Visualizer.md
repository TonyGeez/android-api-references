# Visualizer

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Visualizer

Kotlin| [Java](Visualizer.md) 
| --- | --- |

```
open class Visualizer
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.audiofx.Visualizer](Visualizer.md) |

The Visualizer class enables application to retrieve part of the currently playing audio for visualization purpose. It is not an audio recording interface and only returns partial and low quality audio content. However, to protect privacy of certain audio data (e.g voice mail) the use of the visualizer requires the permission android.permission.RECORD_AUDIO.

The audio session ID passed to the constructor indicates which audio content should be visualized: 

- If the session is 0, the audio output mix is visualized
- If the session is not 0, the audio from a particular [android.media.MediaPlayer](../android.media/MediaPlayer.md) or [android.media.AudioTrack](../android.media/AudioTrack.md) using this audio session is visualized

Two types of representation of audio content can be captured: 

- Waveform data: consecutive 8-bit (unsigned) mono samples by using the[getWaveForm(byte[])](https://developer.android.com/reference/kotlin/android/media/audiofx/Visualizer#getWaveForm(kotlin.ByteArray))method
- Frequency data: 8-bit magnitude FFT by using the[getFft(byte[])](https://developer.android.com/reference/kotlin/android/media/audiofx/Visualizer#getFft(kotlin.ByteArray))method

The length of the capture can be retrieved or specified by calling respectively [getCaptureSize()](Visualizer.md))and [setCaptureSize(int)](Visualizer.md))methods. The capture size must be a power of 2 in the range returned by [getCaptureSizeRange()](Visualizer.md)).

In addition to the polling capture mode described above with[getWaveForm(byte[])](https://developer.android.com/reference/kotlin/android/media/audiofx/Visualizer#getWaveForm(kotlin.ByteArray))and[getFft(byte[])](https://developer.android.com/reference/kotlin/android/media/audiofx/Visualizer#getFft(kotlin.ByteArray))methods, a callback mode is also available by installing a listener by use of the [setDataCaptureListener(android.media.audiofx.Visualizer.OnDataCaptureListener,int,boolean,boolean)](Visualizer.md))method. The rate at which the listener capture method is called as well as the type of data returned is specified.

Before capturing data, the Visualizer must be enabled by calling the [setEnabled(boolean)](Visualizer.md))method. When data capture is not needed any more, the Visualizer should be disabled.

It is good practice to call the [release()](Visualizer.md))method when the Visualizer is not used anymore to free up native resources associated to the Visualizer instance.

Creating a Visualizer on the output mix (audio session 0) requires permission [android.Manifest.permission#MODIFY_AUDIO_SETTINGS](../android/Manifest.permission.md)

The Visualizer class can also be used to perform measurements on the audio being played back. The measurements to perform are defined by setting a mask of the requested measurement modes with [setMeasurementMode(int)](Visualizer.md)). Supported values are [MEASUREMENT_MODE_NONE](Visualizer.md) to cancel any measurement, and [MEASUREMENT_MODE_PEAK_RMS](Visualizer.md) for peak and RMS monitoring. Measurements can be retrieved through [getMeasurementPeakRms(android.media.audiofx.Visualizer.MeasurementPeakRms)](Visualizer.md)).

## Summary

| Nested classes ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [MeasurementPeakRms](../android/media/audiofx/Visualizer.MeasurementPeakRms.md) A class to store peak and RMS values. |
| abstract | [OnDataCaptureListener](../android/media/audiofx/Visualizer.OnDataCaptureListener.md) The OnDataCaptureListener interface defines methods called by the Visualizer to periodically update the audio visualization capture. |

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ALREADY_EXISTS](Visualizer.md) Internal operation status. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR](Visualizer.md) Unspecified error. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_BAD_VALUE](Visualizer.md) Operation failed due to bad parameter value. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_DEAD_OBJECT](Visualizer.md) Operation failed due to dead remote object. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_INVALID_OPERATION](Visualizer.md) Operation failed because it was requested in wrong state. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_NO_INIT](Visualizer.md) Operation failed due to bad object initialization. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_NO_MEMORY](Visualizer.md) Operation failed due to lack of memory. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEASUREMENT_MODE_NONE](Visualizer.md) Defines a measurement mode in which no measurements are performed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MEASUREMENT_MODE_PEAK_RMS](Visualizer.md) Defines a measurement mode which computes the peak and RMS value in mB below the "full scale", where 0mB is normally the maximum sample value (but see the note below). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCALING_MODE_AS_PLAYED](Visualizer.md) Defines a capture mode where the playback volume will affect (scale) the range of the captured data. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCALING_MODE_NORMALIZED](Visualizer.md) Defines a capture mode where amplification is applied based on the content of the captured data. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_ENABLED](Visualizer.md) State of a Visualizer object that is active. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_INITIALIZED](Visualizer.md) State of a Visualizer object that is ready to be used. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_UNINITIALIZED](Visualizer.md) State of a Visualizer object that was not successfully initialized upon creation |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SUCCESS](Visualizer.md) Successful operation. |
| --- | --- |

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Visualizer](Visualizer.md))`(`audioSession:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Class constructor. |

| Public methods ||
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCaptureSize](Visualizer.md))`()` Returns current capture size. |
| openstatic [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | [getCaptureSizeRange](Visualizer.md))`()` Returns the capture size range. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getEnabled](Visualizer.md))`()` Get current activation state of the visualizer. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getFft](Visualizer.md))`(`fft:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Returns a frequency capture of currently playing audio content. |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxCaptureRate](Visualizer.md))`()` Returns the maximum capture rate for the callback capture method. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMeasurementMode](Visualizer.md))`()` Returns the current measurement modes performed by this audio effect |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMeasurementPeakRms](Visualizer.md))`(`measurement:` ` [Visualizer.MeasurementPeakRms](../android/media/audiofx/Visualizer.MeasurementPeakRms.md)!`)` Retrieves the latest peak and RMS measurement. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSamplingRate](Visualizer.md))`()` Returns the sampling rate of the captured audio. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getScalingMode](Visualizer.md))`()` Returns the current scaling mode on the captured visualization data. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getWaveForm](Visualizer.md))`(`waveform:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Returns a waveform capture of currently playing audio content. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [release](Visualizer.md))`()` Releases the native Visualizer resources. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [setCaptureSize](Visualizer.md))`(`size:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the capture size, i. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [setDataCaptureListener](Visualizer.md))`(`listener:` ` [Visualizer.OnDataCaptureListener](../android/media/audiofx/Visualizer.OnDataCaptureListener.md)?`, `rate:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `waveform:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `fft:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Registers an OnDataCaptureListener interface and specifies the rate at which the capture should be updated as well as the type of capture requested. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [setEnabled](Visualizer.md))`(`enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Enable or disable the visualization engine. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [setMeasurementMode](Visualizer.md))`(`mode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the combination of measurement modes to be performed by this audio effect. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [setScalingMode](Visualizer.md))`(`mode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the type of scaling applied on the captured visualization data. |

| Protected methods ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](Visualizer.md))`()` <br /> |

## Constants

### ALREADY_EXISTS

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ALREADY_EXISTS: Int
```

Internal operation status. Not returned by any method. 

 Value: -2

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

### MEASUREMENT_MODE_NONE

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEASUREMENT_MODE_NONE: Int
```

Defines a measurement mode in which no measurements are performed. 

 Value: 0

### MEASUREMENT_MODE_PEAK_RMS

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MEASUREMENT_MODE_PEAK_RMS: Int
```

Defines a measurement mode which computes the peak and RMS value in mB below the "full scale", where 0mB is normally the maximum sample value (but see the note below). Minimum value depends on the resolution of audio samples used by the audio framework. The value of -9600mB is the minimum value for 16-bit audio systems and -14400mB or below for "high resolution" systems. Values for peak and RMS can be retrieved with [getMeasurementPeakRms(android.media.audiofx.Visualizer.MeasurementPeakRms)](Visualizer.md)).

**Note:** when Visualizer effect is attached to the global session (with session ID 0), it is possible to observe RMS peaks higher than 0 dBFS, for example in the case when there are multiple audio sources playing simultaneously. In this case [getMeasurementPeakRms(android.media.audiofx.Visualizer.MeasurementPeakRms)](Visualizer.md))method can return a positive value. 

 Value: 1

### SCALING_MODE_AS_PLAYED

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCALING_MODE_AS_PLAYED: Int
```

Defines a capture mode where the playback volume will affect (scale) the range of the captured data. A low playback volume will lead to low sample and fft values, and vice-versa. 

 Value: 1

### SCALING_MODE_NORMALIZED

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCALING_MODE_NORMALIZED: Int
```

Defines a capture mode where amplification is applied based on the content of the captured data. This is the default Visualizer mode, and is suitable for music visualization. 

 Value: 0

### STATE_ENABLED

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_ENABLED: Int
```

State of a Visualizer object that is active. 

 Value: 2

### STATE_INITIALIZED

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_INITIALIZED: Int
```

State of a Visualizer object that is ready to be used. 

 Value: 1

### STATE_UNINITIALIZED

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_UNINITIALIZED: Int
```

State of a Visualizer object that was not successfully initialized upon creation 

 Value: 0

### SUCCESS

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUCCESS: Int
```

Successful operation. 

 Value: 0

## Public constructors

### Visualizer

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Visualizer(audioSession: Int)
```

Class constructor.

| Parameters ||
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `audioSession` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):system wide unique audio session identifier. If audioSession is not 0, the visualizer will be attached to the MediaPlayer or AudioTrack in the same audio session. Otherwise, the Visualizer will apply to the output mix. |

| Exceptions ||
|-------------------------------------------|---|
| `java.lang.UnsupportedOperationException` | |
| `java.lang.RuntimeException` | |

## Public methods

### getCaptureSize

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCaptureSize(): Int
```

Returns current capture size.

| Return ||
|----------------------------------------------------------------------------|----------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the capture size in bytes. |

### getCaptureSizeRange

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getCaptureSizeRange(): IntArray!
```

Returns the capture size range.

| Return ||
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | the mininum capture size is returned in first array element and the maximum in second array element. |

### getEnabled

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEnabled(): Boolean
```

Get current activation state of the visualizer.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the visualizer is active, false otherwise |

### getFft

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFft(fft: ByteArray!): Int
```

Returns a frequency capture of currently playing audio content.

This method must be called when the Visualizer is enabled.

The capture is an 8-bit magnitude FFT, the frequency range covered being 0 (DC) to half of the sampling rate returned by [getSamplingRate()](Visualizer.md)). The capture returns the real and imaginary parts of a number of frequency points equal to half of the capture size plus one.

Note: only the real part is returned for the first point (DC) and the last point (sampling frequency / 2).

The layout in the returned byte array is as follows:

- n is the capture size returned by getCaptureSize()
- Rfk, Ifk are respectively the real and imaginary parts of the kth frequency component
- If Fs is the sampling frequency retuned by getSamplingRate() the kth frequency is: k \* Fs / n

| Index <br /> | 0 <br /> | 1 <br /> | 2 <br /> | 3 <br /> | 4 <br /> | 5 <br /> | ... <br /> | n - 2 <br /> | n - 1 <br /> |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Data <br /> | Rf0 <br /> | Rf(n/2) <br /> | Rf1 <br /> | If1 <br /> | Rf2 <br /> | If2 <br /> | ... <br /> | Rf(n/2-1) <br /> | If(n/2-1) <br /> |

In order to obtain magnitude and phase values the following code can be used: 

```kotlin
int n = fft.size();
        float[] magnitudes = new float[n / 2 + 1];
        float[] phases = new float[n / 2 + 1];
        magnitudes[0] = (float)Math.abs(fft[0]);      // DC
        magnitudes[n / 2] = (float)Math.abs(fft[1]);  // Nyquist
        phases[0] = phases[n / 2] = 0;
        for (int k = 1; k < n / 2; k++) {
            int i = k * 2;
            magnitudes[k] = (float)Math.hypot(fft[i], fft[i + 1]);
            phases[k] = (float)Math.atan2(fft[i + 1], fft[i]);
        }
```

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------------------------------|
| `fft` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:array of bytes where the FFT should be returned |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SUCCESS](Visualizer.md) in case of success, [ERROR_NO_MEMORY](Visualizer.md), [ERROR_INVALID_OPERATION](Visualizer.md) or [ERROR_DEAD_OBJECT](Visualizer.md) in case of failure. |

| Exceptions ||
|-----------------------------------|---|
| `java.lang.IllegalStateException` | |

### getMaxCaptureRate

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getMaxCaptureRate(): Int
```

Returns the maximum capture rate for the callback capture method. This is the maximum value for the rate parameter of the [setDataCaptureListener(android.media.audiofx.Visualizer.OnDataCaptureListener,int,boolean,boolean)](Visualizer.md))method.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the maximum capture rate expressed in milliHertz |

### getMeasurementMode

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMeasurementMode(): Int
```

Returns the current measurement modes performed by this audio effect

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the mask of the measurements, [MEASUREMENT_MODE_NONE](Visualizer.md)(when no measurements are performed) or [MEASUREMENT_MODE_PEAK_RMS](Visualizer.md). |

| Exceptions ||
|-----------------------------------|---|
| `java.lang.IllegalStateException` | |

### getMeasurementPeakRms

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMeasurementPeakRms(measurement: Visualizer.MeasurementPeakRms!): Int
```

Retrieves the latest peak and RMS measurement. Sets the peak and RMS fields of the supplied [Visualizer.MeasurementPeakRms](../android/media/audiofx/Visualizer.MeasurementPeakRms.md) to the latest measured values.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `measurement` | [Visualizer.MeasurementPeakRms](../android/media/audiofx/Visualizer.MeasurementPeakRms.md)!:a non-null [Visualizer.MeasurementPeakRms](../android/media/audiofx/Visualizer.MeasurementPeakRms.md) instance to store the measurement values. |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SUCCESS](Visualizer.md) in case of success, [ERROR_BAD_VALUE](Visualizer.md), [ERROR_NO_MEMORY](Visualizer.md), [ERROR_INVALID_OPERATION](Visualizer.md) or [ERROR_DEAD_OBJECT](Visualizer.md) in case of failure. |

### getSamplingRate

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSamplingRate(): Int
```

Returns the sampling rate of the captured audio.

| Return ||
|----------------------------------------------------------------------------|----------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the sampling rate in milliHertz. |

### getScalingMode

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getScalingMode(): Int
```

Returns the current scaling mode on the captured visualization data.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the scaling mode, see [SCALING_MODE_NORMALIZED](Visualizer.md) and [SCALING_MODE_AS_PLAYED](Visualizer.md). |

| Exceptions ||
|-----------------------------------|---|
| `java.lang.IllegalStateException` | |

### getWaveForm

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getWaveForm(waveform: ByteArray!): Int
```

Returns a waveform capture of currently playing audio content. The capture consists in a number of consecutive 8-bit (unsigned) mono PCM samples equal to the capture size returned by [getCaptureSize()](Visualizer.md)).

This method must be called when the Visualizer is enabled.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `waveform` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:array of bytes where the waveform should be returned, array length must be at least equals to the capture size returned by [getCaptureSize()](Visualizer.md)). |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SUCCESS](Visualizer.md) in case of success, [ERROR_NO_MEMORY](Visualizer.md), [ERROR_INVALID_OPERATION](Visualizer.md) or [ERROR_DEAD_OBJECT](Visualizer.md) in case of failure. |

| Exceptions ||
|--------------------------------------|---|
| `java.lang.IllegalStateException` | |
| `java.lang.IllegalArgumentException` | |

### release

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun release(): Unit
```

Releases the native Visualizer resources. It is a good practice to release the visualization engine when not in use. 

### setCaptureSize

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setCaptureSize(size: Int): Int
```

Sets the capture size, i.e. the number of bytes returned by[getWaveForm(byte[])](https://developer.android.com/reference/kotlin/android/media/audiofx/Visualizer#getWaveForm(kotlin.ByteArray))and[getFft(byte[])](https://developer.android.com/reference/kotlin/android/media/audiofx/Visualizer#getFft(kotlin.ByteArray))methods. The capture size must be a power of 2 in the range returned by [getCaptureSizeRange()](Visualizer.md)). This method must not be called when the Visualizer is enabled.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------|
| `size` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):requested capture size |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SUCCESS](Visualizer.md) in case of success, [ERROR_INVALID_OPERATION](Visualizer.md) if Visualizer effect enginer not enabled. |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------|
| `java.lang.IllegalStateException` | if the effect is not in proper state. |
| `java.lang.IllegalArgumentException` | if the size parameter is invalid (out of supported range). |

### setDataCaptureListener

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDataCaptureListener(
    listener: Visualizer.OnDataCaptureListener?, 
    rate: Int, 
    waveform: Boolean, 
    fft: Boolean
): Int
```

Registers an OnDataCaptureListener interface and specifies the rate at which the capture should be updated as well as the type of capture requested.

Call this method with a null listener to stop receiving the capture updates.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [Visualizer.OnDataCaptureListener](../android/media/audiofx/Visualizer.OnDataCaptureListener.md)?:OnDataCaptureListener registered This value may be`null`. |
| `rate` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):rate in milliHertz at which the capture should be updated |
| `waveform` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if a waveform capture is requested: the onWaveFormDataCapture() method will be called on the OnDataCaptureListener interface. |
| --- | --- |
| `fft` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if a frequency capture is requested: the onFftDataCapture() method will be called on the OnDataCaptureListener interface. |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SUCCESS](Visualizer.md) in case of success, [ERROR_NO_INIT](Visualizer.md) or [ERROR_BAD_VALUE](Visualizer.md) in case of failure. |

### setEnabled

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setEnabled(enabled: Boolean): Int
```

Enable or disable the visualization engine.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------|
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):requested enable state |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SUCCESS](Visualizer.md) in case of success, [ERROR_INVALID_OPERATION](Visualizer.md) or [ERROR_DEAD_OBJECT](Visualizer.md) in case of failure. |

| Exceptions ||
|-----------------------------------|---|
| `java.lang.IllegalStateException` | |

### setMeasurementMode

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setMeasurementMode(mode: Int): Int
```

Sets the combination of measurement modes to be performed by this audio effect.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a mask of the measurements to perform. The valid values are [MEASUREMENT_MODE_NONE](Visualizer.md)(to cancel any measurement) or [MEASUREMENT_MODE_PEAK_RMS](Visualizer.md). |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SUCCESS](Visualizer.md) in case of success, [ERROR_BAD_VALUE](Visualizer.md) in case of failure. |

| Exceptions ||
|-----------------------------------|---|
| `java.lang.IllegalStateException` | |

### setScalingMode

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setScalingMode(mode: Int): Int
```

Set the type of scaling applied on the captured visualization data.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):see [SCALING_MODE_NORMALIZED](Visualizer.md) and [SCALING_MODE_AS_PLAYED](Visualizer.md) |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SUCCESS](Visualizer.md) in case of success, [ERROR_BAD_VALUE](Visualizer.md) in case of failure. |

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
