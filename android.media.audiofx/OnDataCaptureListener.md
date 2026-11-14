# Visualizer.OnDataCaptureListener

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnDataCaptureListener

Kotlin| [Java](../android/media/audiofx/Visualizer.OnDataCaptureListener.md) 
| --- | --- |

```
interface OnDataCaptureListener
```

| [android.media.audiofx.Visualizer.OnDataCaptureListener](../android/media/audiofx/Visualizer.OnDataCaptureListener.md) |

The OnDataCaptureListener interface defines methods called by the Visualizer to periodically update the audio visualization capture. The client application can implement this interface and register the listener with the [setDataCaptureListener(android.media.audiofx.Visualizer.OnDataCaptureListener,int,boolean,boolean)](../android/media/audiofx/Visualizer.md))method.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onFftDataCapture](../android/media/audiofx/Visualizer.OnDataCaptureListener.md))`(`visualizer:` ` [Visualizer](../android/media/audiofx/Visualizer.md)!`, `fft:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `samplingRate:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Method called when a new frequency capture is available. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onWaveFormDataCapture](../android/media/audiofx/Visualizer.OnDataCaptureListener.md))`(`visualizer:` ` [Visualizer](../android/media/audiofx/Visualizer.md)!`, `waveform:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `samplingRate:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Method called when a new waveform capture is available. |

## Public methods

### onFftDataCapture

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onFftDataCapture(
    visualizer: Visualizer!, 
    fft: ByteArray!, 
    samplingRate: Int
): Unit
```

Method called when a new frequency capture is available.

Data in the fft buffer is valid only within the scope of the callback. Applications which need access to the fft data after returning from the callback should make a copy of the data instead of holding a reference.

For the explanation of the fft data array layout, and the example code for processing it, please see the documentation for[getFft(byte[])](https://developer.android.com/reference/kotlin/android/media/audiofx/Visualizer#getFft(kotlin.ByteArray))method.

| Parameters ||
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| `visualizer` | [Visualizer](../android/media/audiofx/Visualizer.md)!:Visualizer object on which the listener is registered. |
| `fft` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:array of bytes containing the frequency representation. |
| `samplingRate` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):sampling rate of the visualized audio. |
| --- | --- |

### onWaveFormDataCapture

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onWaveFormDataCapture(
    visualizer: Visualizer!, 
    waveform: ByteArray!, 
    samplingRate: Int
): Unit
```

Method called when a new waveform capture is available.

Data in the waveform buffer is valid only within the scope of the callback. Applications which need access to the waveform data after returning from the callback should make a copy of the data instead of holding a reference.

| Parameters ||
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| `visualizer` | [Visualizer](../android/media/audiofx/Visualizer.md)!:Visualizer object on which the listener is registered. |
| `waveform` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:array of bytes containing the waveform representation. |
| `samplingRate` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):sampling rate of the visualized audio. |
| --- | --- |
