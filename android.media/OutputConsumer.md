# MediaParser.OutputConsumer

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OutputConsumer

Kotlin| [Java](https://developer.android.com/reference/android/media/MediaParser.OutputConsumer "View this page in Java") 
| --- | --- |

```
interface OutputConsumer
```

| [android.media.MediaParser.OutputConsumer](https://developer.android.com/reference/kotlin/android/media/MediaParser.OutputConsumer#) |

Receives extracted media sample data and metadata from [MediaParser](https://developer.android.com/reference/kotlin/android/media/MediaParser).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSampleCompleted](https://developer.android.com/reference/kotlin/android/media/MediaParser.OutputConsumer#onSampleCompleted(kotlin.Int,%20kotlin.Long,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20android.media.MediaCodec.CryptoInfo))`(`trackIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `timeMicros:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `size:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `cryptoInfo:` ` [MediaCodec.CryptoInfo](https://developer.android.com/reference/kotlin/android/media/MediaCodec.CryptoInfo)?`)` Called once all the data of a sample has been passed to [onSampleDataFound](https://developer.android.com/reference/kotlin/android/media/MediaParser.OutputConsumer#onSampleDataFound(kotlin.Int,%20android.media.MediaParser.InputReader)). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSampleDataFound](https://developer.android.com/reference/kotlin/android/media/MediaParser.OutputConsumer#onSampleDataFound(kotlin.Int,%20android.media.MediaParser.InputReader))`(`trackIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `inputReader:` ` [MediaParser.InputReader](https://developer.android.com/reference/kotlin/android/media/MediaParser.InputReader)`)` Called when sample data is found in the stream. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSeekMapFound](https://developer.android.com/reference/kotlin/android/media/MediaParser.OutputConsumer#onSeekMapFound(android.media.MediaParser.SeekMap))`(`seekMap:` ` [MediaParser.SeekMap](https://developer.android.com/reference/kotlin/android/media/MediaParser.SeekMap)`)` Called when a [SeekMap](https://developer.android.com/reference/kotlin/android/media/MediaParser.SeekMap) has been extracted from the stream. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onTrackCountFound](https://developer.android.com/reference/kotlin/android/media/MediaParser.OutputConsumer#onTrackCountFound(kotlin.Int))`(`numberOfTracks:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when the number of tracks is found. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onTrackDataFound](https://developer.android.com/reference/kotlin/android/media/MediaParser.OutputConsumer#onTrackDataFound(kotlin.Int,%20android.media.MediaParser.TrackData))`(`trackIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `trackData:` ` [MediaParser.TrackData](https://developer.android.com/reference/kotlin/android/media/MediaParser.TrackData)`)` Called when new [TrackData](https://developer.android.com/reference/kotlin/android/media/MediaParser.TrackData) is found in the stream. |

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

Called once all the data of a sample has been passed to [onSampleDataFound](https://developer.android.com/reference/kotlin/android/media/MediaParser.OutputConsumer#onSampleDataFound(kotlin.Int,%20android.media.MediaParser.InputReader)).

Includes sample metadata, like presentation timestamp and flags.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `trackIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index of the track to which the sample corresponds. |
| `timeMicros` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The media timestamp associated with the sample, in microseconds. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Flags associated with the sample. See the`SAMPLE_FLAG_*`constants. Value is either`0`or a combination of [android.media.MediaParser#SAMPLE_FLAG_KEY_FRAME](https://developer.android.com/reference/kotlin/android/media/MediaParser#SAMPLE_FLAG_KEY_FRAME:kotlin.Int), [android.media.MediaParser#SAMPLE_FLAG_HAS_SUPPLEMENTAL_DATA](https://developer.android.com/reference/kotlin/android/media/MediaParser#SAMPLE_FLAG_HAS_SUPPLEMENTAL_DATA:kotlin.Int), [android.media.MediaParser#SAMPLE_FLAG_LAST_SAMPLE](https://developer.android.com/reference/kotlin/android/media/MediaParser#SAMPLE_FLAG_LAST_SAMPLE:kotlin.Int), [android.media.MediaParser#SAMPLE_FLAG_ENCRYPTED](https://developer.android.com/reference/kotlin/android/media/MediaParser#SAMPLE_FLAG_ENCRYPTED:kotlin.Int), and [android.media.MediaParser#SAMPLE_FLAG_DECODE_ONLY](https://developer.android.com/reference/kotlin/android/media/MediaParser#SAMPLE_FLAG_DECODE_ONLY:kotlin.Int) |
| --- | --- |
| `size` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The size of the sample data, in bytes. |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The number of bytes that have been consumed by`onSampleDataFound(int, MediaParser.InputReader)`for the specified track, since the last byte belonging to the sample whose metadata is being passed. |
| `cryptoInfo` | [MediaCodec.CryptoInfo](https://developer.android.com/reference/kotlin/android/media/MediaCodec.CryptoInfo)?:Encryption data required to decrypt the sample. May be null for unencrypted samples. Implementors should treat any output [CryptoInfo](https://developer.android.com/reference/kotlin/android/media/MediaCodec.CryptoInfo) instances as immutable. MediaParser will not modify any output`cryptoInfos`and implementors should not modify them either. |
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

If the invocation of this method returns before the entire`inputReader` [length](https://developer.android.com/reference/kotlin/android/media/MediaParser.InputReader#getLength())is consumed, the method will be called again for the implementer to read the remaining data. Implementers should surface any thrown [IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#) caused by reading from`input`.

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `trackIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index of the track to which the sample data corresponds. |
| `inputReader` | [MediaParser.InputReader](https://developer.android.com/reference/kotlin/android/media/MediaParser.InputReader):The [InputReader](https://developer.android.com/reference/kotlin/android/media/MediaParser.InputReader) from which to read the data. This value cannot be`null`. |

| Exceptions ||
|-----------------------|---------------------------------------------------------|
| `java.io.IOException` | If an exception occurs while reading from`inputReader`. |

### onSeekMapFound

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onSeekMapFound(seekMap: MediaParser.SeekMap): Unit
```

Called when a [SeekMap](https://developer.android.com/reference/kotlin/android/media/MediaParser.SeekMap) has been extracted from the stream.

This method is called at least once before any samples are [complete](https://developer.android.com/reference/kotlin/android/media/MediaParser.OutputConsumer#onSampleCompleted(kotlin.Int,%20kotlin.Long,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20android.media.MediaCodec.CryptoInfo)). May be called multiple times after that in order to add [SeekPoints](https://developer.android.com/reference/kotlin/android/media/MediaParser.SeekPoint).

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `seekMap` | [MediaParser.SeekMap](https://developer.android.com/reference/kotlin/android/media/MediaParser.SeekMap):The extracted [SeekMap](https://developer.android.com/reference/kotlin/android/media/MediaParser.SeekMap). This value cannot be`null`. |

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

Called when new [TrackData](https://developer.android.com/reference/kotlin/android/media/MediaParser.TrackData) is found in the stream.

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `trackIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index of the track for which the [TrackData](https://developer.android.com/reference/kotlin/android/media/MediaParser.TrackData) was extracted. |
| `trackData` | [MediaParser.TrackData](https://developer.android.com/reference/kotlin/android/media/MediaParser.TrackData):The extracted [TrackData](https://developer.android.com/reference/kotlin/android/media/MediaParser.TrackData). This value cannot be`null`. |
