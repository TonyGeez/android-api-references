# MediaParser.OutputConsumer

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OutputConsumer

Kotlin| [Java](../android/media/MediaParser.OutputConsumer.md) 
| --- | --- |

```
interface OutputConsumer
```

| [android.media.MediaParser.OutputConsumer](../android/media/MediaParser.OutputConsumer.md) |

Receives extracted media sample data and metadata from [MediaParser](../android/media/MediaParser.md).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSampleCompleted](../android/media/MediaParser.OutputConsumer.md))`(`trackIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `timeMicros:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `size:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `cryptoInfo:` ` [MediaCodec.CryptoInfo](../android/media/MediaCodec.CryptoInfo.md)?`)` Called once all the data of a sample has been passed to [onSampleDataFound](../android/media/MediaParser.OutputConsumer.md)). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSampleDataFound](../android/media/MediaParser.OutputConsumer.md))`(`trackIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `inputReader:` ` [MediaParser.InputReader](../android/media/MediaParser.InputReader.md)`)` Called when sample data is found in the stream. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSeekMapFound](../android/media/MediaParser.OutputConsumer.md))`(`seekMap:` ` [MediaParser.SeekMap](../android/media/MediaParser.SeekMap.md)`)` Called when a [SeekMap](../android/media/MediaParser.SeekMap.md) has been extracted from the stream. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onTrackCountFound](../android/media/MediaParser.OutputConsumer.md))`(`numberOfTracks:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when the number of tracks is found. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onTrackDataFound](../android/media/MediaParser.OutputConsumer.md))`(`trackIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `trackData:` ` [MediaParser.TrackData](../android/media/MediaParser.TrackData.md)`)` Called when new [TrackData](../android/media/MediaParser.TrackData.md) is found in the stream. |

## Public methods

### onSampleCompleted

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onSampleCompleted(
    trackIndex: Int, 
    timeMicros: Long, 
    flags: Int, 
    size: Int, 
    offset: Int, 
    cryptoInfo: MediaCodec.CryptoInfo?
): Unit
```

Called once all the data of a sample has been passed to [onSampleDataFound](../android/media/MediaParser.OutputConsumer.md)).

Includes sample metadata, like presentation timestamp and flags.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `trackIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index of the track to which the sample corresponds. |
| `timeMicros` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The media timestamp associated with the sample, in microseconds. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Flags associated with the sample. See the`SAMPLE_FLAG_*`constants. Value is either`0`or a combination of [android.media.MediaParser#SAMPLE_FLAG_KEY_FRAME](../android/media/MediaParser.md), [android.media.MediaParser#SAMPLE_FLAG_HAS_SUPPLEMENTAL_DATA](../android/media/MediaParser.md), [android.media.MediaParser#SAMPLE_FLAG_LAST_SAMPLE](../android/media/MediaParser.md), [android.media.MediaParser#SAMPLE_FLAG_ENCRYPTED](../android/media/MediaParser.md), and [android.media.MediaParser#SAMPLE_FLAG_DECODE_ONLY](../android/media/MediaParser.md) |
| --- | --- |
| `size` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The size of the sample data, in bytes. |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The number of bytes that have been consumed by`onSampleDataFound(int, MediaParser.InputReader)`for the specified track, since the last byte belonging to the sample whose metadata is being passed. |
| `cryptoInfo` | [MediaCodec.CryptoInfo](../android/media/MediaCodec.CryptoInfo.md)?:Encryption data required to decrypt the sample. May be null for unencrypted samples. Implementors should treat any output [CryptoInfo](../android/media/MediaCodec.CryptoInfo.md) instances as immutable. MediaParser will not modify any output`cryptoInfos`and implementors should not modify them either. |
| --- | --- |

### onSampleDataFound

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onSampleDataFound(
    trackIndex: Int, 
    inputReader: MediaParser.InputReader
): Unit
```

Called when sample data is found in the stream.

If the invocation of this method returns before the entire`inputReader` [length](../android/media/MediaParser.InputReader.md))is consumed, the method will be called again for the implementer to read the remaining data. Implementers should surface any thrown [IOException](../java/io/IOException.md) caused by reading from`input`.

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `trackIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index of the track to which the sample data corresponds. |
| `inputReader` | [MediaParser.InputReader](../android/media/MediaParser.InputReader.md):The [InputReader](../android/media/MediaParser.InputReader.md) from which to read the data. This value cannot be`null`. |

| Exceptions ||
|-----------------------|---------------------------------------------------------|
| `java.io.IOException` | If an exception occurs while reading from`inputReader`. |

### onSeekMapFound

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onSeekMapFound(seekMap: MediaParser.SeekMap): Unit
```

Called when a [SeekMap](../android/media/MediaParser.SeekMap.md) has been extracted from the stream.

This method is called at least once before any samples are [complete](../android/media/MediaParser.OutputConsumer.md)). May be called multiple times after that in order to add [SeekPoints](../android/media/MediaParser.SeekPoint.md).

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `seekMap` | [MediaParser.SeekMap](../android/media/MediaParser.SeekMap.md):The extracted [SeekMap](../android/media/MediaParser.SeekMap.md). This value cannot be`null`. |

### onTrackCountFound

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onTrackCountFound(numberOfTracks: Int): Unit
```

Called when the number of tracks is found.

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------|
| `numberOfTracks` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The number of tracks in the stream. |

### onTrackDataFound

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onTrackDataFound(
    trackIndex: Int, 
    trackData: MediaParser.TrackData
): Unit
```

Called when new [TrackData](../android/media/MediaParser.TrackData.md) is found in the stream.

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `trackIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index of the track for which the [TrackData](../android/media/MediaParser.TrackData.md) was extracted. |
| `trackData` | [MediaParser.TrackData](../android/media/MediaParser.TrackData.md):The extracted [TrackData](../android/media/MediaParser.TrackData.md). This value cannot be`null`. |
