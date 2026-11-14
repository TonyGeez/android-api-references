# MediaExtractor

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MediaExtractor

Kotlin| [Java](MediaExtractor.md) 
| --- | --- |

```
class MediaExtractor
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.MediaExtractor](MediaExtractor.md) |

MediaExtractor facilitates extraction of demuxed, typically encoded, media data from a data source.

It is generally used like this: 

```kotlin
MediaExtractor extractor = new MediaExtractor();
  extractor.setDataSource(...);
  int numTracks = extractor.getTrackCount();
  for (int i = 0; i < numTracks; ++i) {
    MediaFormat format = extractor.getTrackFormat(i);
    String mime = format.getString(MediaFormat.KEY_MIME);
    if (weAreInterestedInThisTrack) {
      extractor.selectTrack(i);
    }
  }
  ByteBuffer inputBuffer = ByteBuffer.allocate(...)
  while (extractor.readSampleData(inputBuffer, ...) >= 0) {
    int trackIndex = extractor.getSampleTrackIndex();
    long presentationTimeUs = extractor.getSampleTime();
    ...
    extractor.advance();
  }
 
  extractor.release();
  extractor = null;
  
```

This class requires the [android.Manifest.permission#INTERNET](../android/Manifest.permission.md) permission when used with network-based content.

## Summary

| Nested classes ||
|---|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [CasInfo](../android/media/MediaExtractor.CasInfo.md) Describes the conditional access system used to scramble a track. |
| | [MetricsConstants](../android/media/MediaExtractor.MetricsConstants.md) <br /> |

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SAMPLE_FLAG_ENCRYPTED](MediaExtractor.md) The sample is (at least partially) encrypted, see also the documentation for [android.media.MediaCodec#queueSecureInputBuffer](MediaCodec.md)) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SAMPLE_FLAG_PARTIAL_FRAME](MediaExtractor.md) This indicates that the buffer only contains part of a frame, and the decoder should batch the data until a buffer without this flag appears before decoding the frame. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SAMPLE_FLAG_SYNC](MediaExtractor.md) The sample is a sync sample (or in [MediaCodec](MediaCodec.md)'s terminology it is a key frame. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SEEK_TO_CLOSEST_SYNC](MediaExtractor.md) If possible, seek to the sync sample closest to the specified time |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SEEK_TO_NEXT_SYNC](MediaExtractor.md) If possible, seek to a sync sample at or after the specified time |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SEEK_TO_PREVIOUS_SYNC](MediaExtractor.md) If possible, seek to a sync sample at or before the specified time |
| --- | --- |

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------|---|
| [MediaExtractor](MediaExtractor.md))`()` <br /> |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [advance](MediaExtractor.md))`()` Advance to the next sample. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [AudioPresentation](AudioPresentation.md)!\> | [getAudioPresentations](MediaExtractor.md))`(`trackIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the list of available audio presentations for the track. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getCachedDuration](MediaExtractor.md))`()` Returns an estimate of how much data is presently cached in memory expressed in microseconds. |
| --- | --- |
| [MediaExtractor.CasInfo](../android/media/MediaExtractor.CasInfo.md)! | [getCasInfo](MediaExtractor.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves the information about the conditional access system used to scramble a track. |
| [DrmInitData](DrmInitData.md)! | [getDrmInitData](MediaExtractor.md))`()` Extract DRM initialization data if it exists |
| [LogSessionId](../android.media.metrics/LogSessionId.md) | [getLogSessionId](MediaExtractor.md))`()` Returns the [LogSessionId](../android.media.metrics/LogSessionId.md) for MediaExtractor. |
| --- | --- |
| [PersistableBundle](../android.os/PersistableBundle.md)! | [getMetrics](MediaExtractor.md))`()` Return Metrics data about the current media container. |
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [UUID](../java.util/UUID.md)!, [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!\>? | [getPsshInfo](MediaExtractor.md))`()` Get the PSSH info if present. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getSampleCryptoInfo](MediaExtractor.md))`(`info:` ` [MediaCodec.CryptoInfo](../android/media/MediaCodec.CryptoInfo.md)`)` If the sample flags indicate that the current sample is at least partially encrypted, this call returns relevant information about the structure of the sample data required for decryption. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSampleFlags](MediaExtractor.md))`()` Returns the current sample's flags. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getSampleSize](MediaExtractor.md))`()` <br /> |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getSampleTime](MediaExtractor.md))`()` Returns the current sample's presentation time in microseconds. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSampleTrackIndex](MediaExtractor.md))`()` Returns the track index the current sample originates from (or -1 if no more samples are available) |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTrackCount](MediaExtractor.md))`()` Count the number of tracks found in the data source. |
| [MediaFormat](MediaFormat.md) | [getTrackFormat](MediaExtractor.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the track format at the specified index. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasCacheReachedEndOfStream](MediaExtractor.md))`()` Returns true iff we are caching data and the cache has reached the end of the data stream (for now, a future seek may of course restart the fetching of data). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [readSampleData](MediaExtractor.md))`(`byteBuf:` ` [ByteBuffer](../java.nio/ByteBuffer.md)`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieve the current encoded sample and store it in the byte buffer starting at the given offset. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [release](MediaExtractor.md))`()` Make sure you call this when you're done to free up any resources instead of relying on the garbage collector to do this for you at some point in the future. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [seekTo](MediaExtractor.md))`(`timeUs:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `mode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` All selected tracks seek near the requested time according to the specified mode. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [selectTrack](MediaExtractor.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Subsequent calls to [readSampleData](MediaExtractor.md)), [getSampleTrackIndex](MediaExtractor.md))and [getSampleTime](MediaExtractor.md))only retrieve information for the subset of tracks selected. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDataSource](MediaExtractor.md))`(`context:` ` [Context](../android.content/Context.md)`, `uri:` ` [Uri](../android.net/Uri.md)`, `headers:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>?`)` Sets the data source as a content Uri. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDataSource](MediaExtractor.md))`(`afd:` ` [AssetFileDescriptor](../android.content.res/AssetFileDescriptor.md)`)` Sets the data source (AssetFileDescriptor) to use. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDataSource](MediaExtractor.md))`(`dataSource:` ` [MediaDataSource](MediaDataSource.md)`)` Sets the data source (MediaDataSource) to use. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDataSource](MediaExtractor.md))`(`fd:` ` [FileDescriptor](../java.io/FileDescriptor.md)`)` Sets the data source (FileDescriptor) to use. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDataSource](MediaExtractor.md))`(`fd:` ` [FileDescriptor](../java.io/FileDescriptor.md)`, `offset:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `length:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the data source (FileDescriptor) to use. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDataSource](MediaExtractor.md))`(`path:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Sets the data source (file-path or http URL) to use. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDataSource](MediaExtractor.md))`(`path:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `headers:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>?`)` Sets the data source (file-path or http URL) to use. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLogSessionId](MediaExtractor.md))`(`logSessionId:` ` [LogSessionId](../android.media.metrics/LogSessionId.md)`)` Sets the [LogSessionId](../android.media.metrics/LogSessionId.md) for MediaExtractor. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMediaCas](MediaExtractor.md))`(`mediaCas:` ` [MediaCas](MediaCas.md)`)` Sets the MediaCas instance to use. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unselectTrack](MediaExtractor.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Subsequent calls to [readSampleData](MediaExtractor.md)), [getSampleTrackIndex](MediaExtractor.md))and [getSampleTime](MediaExtractor.md))only retrieve information for the subset of tracks selected. |
| --- | --- |

| Protected methods ||
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](MediaExtractor.md))`()` <br /> |

## Constants

### SAMPLE_FLAG_ENCRYPTED

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SAMPLE_FLAG_ENCRYPTED: Int
```

The sample is (at least partially) encrypted, see also the documentation for [android.media.MediaCodec#queueSecureInputBuffer](MediaCodec.md)) 

 Value: 2

### SAMPLE_FLAG_PARTIAL_FRAME

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SAMPLE_FLAG_PARTIAL_FRAME: Int
```

This indicates that the buffer only contains part of a frame, and the decoder should batch the data until a buffer without this flag appears before decoding the frame. 

 Value: 4

**See Also**

- [android.media.MediaCodec#BUFFER_FLAG_PARTIAL_FRAME](MediaCodec.md) 

### SAMPLE_FLAG_SYNC

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SAMPLE_FLAG_SYNC: Int
```

The sample is a sync sample (or in [MediaCodec](MediaCodec.md)'s terminology it is a key frame.) 

 Value: 1

**See Also**

- [android.media.MediaCodec#BUFFER_FLAG_KEY_FRAME](MediaCodec.md) 

### SEEK_TO_CLOSEST_SYNC

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SEEK_TO_CLOSEST_SYNC: Int
```

If possible, seek to the sync sample closest to the specified time 

 Value: 2

### SEEK_TO_NEXT_SYNC

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SEEK_TO_NEXT_SYNC: Int
```

If possible, seek to a sync sample at or after the specified time 

 Value: 1

### SEEK_TO_PREVIOUS_SYNC

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SEEK_TO_PREVIOUS_SYNC: Int
```

If possible, seek to a sync sample at or before the specified time 

 Value: 0

## Public constructors

### MediaExtractor

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
MediaExtractor()
```

## Public methods

### advance

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun advance(): Boolean
```

Advance to the next sample. Returns false if no more sample data is available (end of stream). When extracting a local file, the behaviors of [advance](MediaExtractor.md))and [readSampleData](MediaExtractor.md))are undefined in presence of concurrent writes to the same local file; more specifically, end of stream could be signalled earlier than expected. 

### getAudioPresentations

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAudioPresentations(trackIndex: Int): MutableList<AudioPresentation!>
```

Get the list of available audio presentations for the track.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------|
| `trackIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index of the track. |

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [AudioPresentation](AudioPresentation.md)!> | a list of available audio presentations for a given valid audio track index. The list will be empty if the source does not contain any audio presentations. This value cannot be`null`. |

### getCachedDuration

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCachedDuration(): Long
```

Returns an estimate of how much data is presently cached in memory expressed in microseconds. Returns -1 if that information is unavailable or not applicable (no cache). 

### getCasInfo

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCasInfo(index: Int): MediaExtractor.CasInfo!
```

Retrieves the information about the conditional access system used to scramble a track.

| Parameters ||
|---------|------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):of the track. |

| Return ||
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [MediaExtractor.CasInfo](../android/media/MediaExtractor.CasInfo.md)! | an [CasInfo](../android/media/MediaExtractor.CasInfo.md) object describing the conditional access system. |

### getDrmInitData

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDrmInitData(): DrmInitData!
```

Extract DRM initialization data if it exists

If the media contains a PSSH box, only PSSH version 0 is supported. The result for media with other PSSH versions is undefined.

| Return ||
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [DrmInitData](DrmInitData.md)! | DRM initialization data in the content, or`null`if no recognizable DRM format is found; |

**See Also**

- [android.media.DrmInitData](DrmInitData.md) 

### getLogSessionId

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLogSessionId(): LogSessionId
```

Returns the [LogSessionId](../android.media.metrics/LogSessionId.md) for MediaExtractor.

| Return ||
|---------------------------------------------------------------------------------------------------|-----------------------------|
| [LogSessionId](../android.media.metrics/LogSessionId.md) | This value cannot be`null`. |

### getMetrics

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMetrics(): PersistableBundle!
```

Return Metrics data about the current media container.

| Return ||
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [PersistableBundle](../android.os/PersistableBundle.md)! | a [PersistableBundle](../android.os/PersistableBundle.md) containing the set of attributes and values available for the media container being handled by this instance of MediaExtractor. The attributes are descibed in [MetricsConstants](../android/media/MediaExtractor.MetricsConstants.md). Additional vendor-specific fields may also be present in the return value. |

### getPsshInfo

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPsshInfo(): MutableMap<UUID!, ByteArray!>?
```

Get the PSSH info if present.

This method only supports version 0 PSSH boxes. The result for other versions is undefined.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [UUID](../java.util/UUID.md)!,` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!>? | a map of uuid-to-bytes, with the uuid specifying the crypto scheme, and the bytes being the data specific to that scheme. This can be`null`if the source does not contain PSSH info. |

### getSampleCryptoInfo

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSampleCryptoInfo(info: MediaCodec.CryptoInfo): Boolean
```

If the sample flags indicate that the current sample is at least partially encrypted, this call returns relevant information about the structure of the sample data required for decryption.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `info` | [MediaCodec.CryptoInfo](../android/media/MediaCodec.CryptoInfo.md):The android.media.MediaCodec.CryptoInfo structure to be filled in. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true iff the sample flags contain [SAMPLE_FLAG_ENCRYPTED](MediaExtractor.md) |

### getSampleFlags

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSampleFlags(): Int
```

Returns the current sample's flags.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is either`0`or a combination of [android.media.MediaExtractor#SAMPLE_FLAG_SYNC](MediaExtractor.md), [android.media.MediaExtractor#SAMPLE_FLAG_ENCRYPTED](MediaExtractor.md), and [android.media.MediaExtractor#SAMPLE_FLAG_PARTIAL_FRAME](MediaExtractor.md) |

### getSampleSize

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSampleSize(): Long
```

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | size of the current sample in bytes or -1 if no more samples are available. |

### getSampleTime

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSampleTime(): Long
```

Returns the current sample's presentation time in microseconds. or -1 if no more samples are available. 

### getSampleTrackIndex

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSampleTrackIndex(): Int
```

Returns the track index the current sample originates from (or -1 if no more samples are available) 

### getTrackCount

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTrackCount(): Int
```

Count the number of tracks found in the data source. 

### getTrackFormat

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTrackFormat(index: Int): MediaFormat
```

Get the track format at the specified index. More detail on the representation can be found at [android.media.MediaCodec](MediaCodec.md)

The following table summarizes support for format keys across android releases:

| OS Version(s) | `MediaFormat`keys used for |||
| --- | --- | --- | --- |
| OS Version(s) | All Tracks | Audio Tracks | Video Tracks |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [android.os.Build.VERSION_CODES#JELLY_BEAN](../android/os/Build.VERSION_CODES.md) | [MediaFormat.KEY_MIME](MediaFormat.md), [MediaFormat.KEY_DURATION](MediaFormat.md), [MediaFormat.KEY_MAX_INPUT_SIZE](MediaFormat.md) | [MediaFormat.KEY_SAMPLE_RATE](MediaFormat.md), [MediaFormat.KEY_CHANNEL_COUNT](MediaFormat.md), [MediaFormat.KEY_CHANNEL_MASK](MediaFormat.md), gapless playback information.mp3, .mp4, [MediaFormat.KEY_IS_ADTS](MediaFormat.md) AAC if streaming, codec-specific dataAAC, Vorbis | [MediaFormat.KEY_WIDTH](MediaFormat.md), [MediaFormat.KEY_HEIGHT](MediaFormat.md), codec-specific dataAVC, MPEG4 |
| [android.os.Build.VERSION_CODES#JELLY_BEAN_MR1](../android/os/Build.VERSION_CODES.md) | [MediaFormat.KEY_MIME](MediaFormat.md), [MediaFormat.KEY_DURATION](MediaFormat.md), [MediaFormat.KEY_MAX_INPUT_SIZE](MediaFormat.md) | [MediaFormat.KEY_SAMPLE_RATE](MediaFormat.md), [MediaFormat.KEY_CHANNEL_COUNT](MediaFormat.md), [MediaFormat.KEY_CHANNEL_MASK](MediaFormat.md), gapless playback information.mp3, .mp4, [MediaFormat.KEY_IS_ADTS](MediaFormat.md) AAC if streaming, codec-specific dataAAC, Vorbis | [MediaFormat.KEY_WIDTH](MediaFormat.md), [MediaFormat.KEY_HEIGHT](MediaFormat.md), codec-specific dataAVC, MPEG4 |
| [android.os.Build.VERSION_CODES#JELLY_BEAN_MR2](../android/os/Build.VERSION_CODES.md) | [MediaFormat.KEY_MIME](MediaFormat.md), [MediaFormat.KEY_DURATION](MediaFormat.md), [MediaFormat.KEY_MAX_INPUT_SIZE](MediaFormat.md) | [MediaFormat.KEY_SAMPLE_RATE](MediaFormat.md), [MediaFormat.KEY_CHANNEL_COUNT](MediaFormat.md), [MediaFormat.KEY_CHANNEL_MASK](MediaFormat.md), gapless playback information.mp3, .mp4, [MediaFormat.KEY_IS_ADTS](MediaFormat.md) AAC if streaming, codec-specific dataAAC, Vorbis | as above, plus Pixel aspect ratio informationAVC, \* |
| --- | --- | --- | --- |
| [android.os.Build.VERSION_CODES#KITKAT](../android/os/Build.VERSION_CODES.md) | [MediaFormat.KEY_MIME](MediaFormat.md), [MediaFormat.KEY_DURATION](MediaFormat.md), [MediaFormat.KEY_MAX_INPUT_SIZE](MediaFormat.md) | [MediaFormat.KEY_SAMPLE_RATE](MediaFormat.md), [MediaFormat.KEY_CHANNEL_COUNT](MediaFormat.md), [MediaFormat.KEY_CHANNEL_MASK](MediaFormat.md), gapless playback information.mp3, .mp4, [MediaFormat.KEY_IS_ADTS](MediaFormat.md) AAC if streaming, codec-specific dataAAC, Vorbis | as above, plus Pixel aspect ratio informationAVC, \* |
| [android.os.Build.VERSION_CODES#KITKAT_WATCH](../android/os/Build.VERSION_CODES.md) | [MediaFormat.KEY_MIME](MediaFormat.md), [MediaFormat.KEY_DURATION](MediaFormat.md), [MediaFormat.KEY_MAX_INPUT_SIZE](MediaFormat.md) | [MediaFormat.KEY_SAMPLE_RATE](MediaFormat.md), [MediaFormat.KEY_CHANNEL_COUNT](MediaFormat.md), [MediaFormat.KEY_CHANNEL_MASK](MediaFormat.md), gapless playback information.mp3, .mp4, [MediaFormat.KEY_IS_ADTS](MediaFormat.md) AAC if streaming, codec-specific dataAAC, Vorbis | as above, plus Pixel aspect ratio informationAVC, \* |
| [android.os.Build.VERSION_CODES#LOLLIPOP](../android/os/Build.VERSION_CODES.md) | [MediaFormat.KEY_MIME](MediaFormat.md), [MediaFormat.KEY_DURATION](MediaFormat.md), [MediaFormat.KEY_MAX_INPUT_SIZE](MediaFormat.md) | as above, plus [MediaFormat.KEY_BIT_RATE](MediaFormat.md) AAC, codec-specific dataOpus | as above, plus [MediaFormat.KEY_ROTATION](MediaFormat.md).mp4, [MediaFormat.KEY_BIT_RATE](MediaFormat.md) MPEG4, codec-specific dataHEVC |
| --- | --- | --- | --- |
| [android.os.Build.VERSION_CODES#LOLLIPOP_MR1](../android/os/Build.VERSION_CODES.md) | [MediaFormat.KEY_MIME](MediaFormat.md), [MediaFormat.KEY_DURATION](MediaFormat.md), [MediaFormat.KEY_MAX_INPUT_SIZE](MediaFormat.md) | as above, plus [MediaFormat.KEY_BIT_RATE](MediaFormat.md) AAC, codec-specific dataOpus | as above, plus [MediaFormat.KEY_ROTATION](MediaFormat.md).mp4, [MediaFormat.KEY_BIT_RATE](MediaFormat.md) MPEG4, codec-specific dataHEVC |
| [android.os.Build.VERSION_CODES#M](../android/os/Build.VERSION_CODES.md) | [MediaFormat.KEY_MIME](MediaFormat.md), [MediaFormat.KEY_DURATION](MediaFormat.md), [MediaFormat.KEY_MAX_INPUT_SIZE](MediaFormat.md) | as above, plus gapless playback informationOpus | as above, plus [MediaFormat.KEY_FRAME_RATE](MediaFormat.md)(integer) |
| [android.os.Build.VERSION_CODES#N](../android/os/Build.VERSION_CODES.md) | as above, plus [MediaFormat.KEY_TRACK_ID](MediaFormat.md), [MediaFormat.KEY_BIT_RATE](MediaFormat.md), .mp4 | as above, plus [MediaFormat.KEY_PCM_ENCODING](MediaFormat.md), [MediaFormat.KEY_PROFILE](MediaFormat.md) AAC | as above, plus [MediaFormat.KEY_HDR_STATIC_INFO](MediaFormat.md), .webm, [MediaFormat.KEY_COLOR_STANDARD](MediaFormat.md), [MediaFormat.KEY_COLOR_TRANSFER](MediaFormat.md), [MediaFormat.KEY_COLOR_RANGE](MediaFormat.md), [MediaFormat.KEY_PROFILE](MediaFormat.md) MPEG2, H.263, MPEG4, AVC, HEVC, VP9, [MediaFormat.KEY_LEVEL](MediaFormat.md) H.263, MPEG4, AVC, HEVC, VP9, codec-specific dataVP9 |
| --- | --- | --- | --- |
| **Notes:** #: container-specified value only. .mp4, .webm...: for listed containers MPEG4, AAC...: for listed codecs ||||
| Note that that level information contained in the container many times does not match the level of the actual bitstream. You may want to clear the level using`MediaFormat.setString(KEY_LEVEL, null)`before using the track format to find a decoder that can play back a particular track. ||||
| **\*Pixel (sample) aspect ratio**is returned in the following keys. The display width can be calculated for example as: display-width = display-height \* crop-width / crop-height \* sar-width / sar-height ||||
| --- | --- | --- | --- |
| `"sar-width"` | Integer | Pixel aspect ratio width ||
| `"sar-height"` | Integer | Pixel aspect ratio height ||

### hasCacheReachedEndOfStream

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasCacheReachedEndOfStream(): Boolean
```

Returns true iff we are caching data and the cache has reached the end of the data stream (for now, a future seek may of course restart the fetching of data). This API only returns a meaningful result if [getCachedDuration](MediaExtractor.md))indicates the presence of a cache, i.e. does NOT return -1. 

### readSampleData

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun readSampleData(
    byteBuf: ByteBuffer, 
    offset: Int
): Int
```

Retrieve the current encoded sample and store it in the byte buffer starting at the given offset.

**Note:** As of API 21, on success the position and limit of`byteBuf`is updated to point to the data just read.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `byteBuf` | [ByteBuffer](../java.nio/ByteBuffer.md):the destination byte buffer This value cannot be`null`. |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the sample size (or -1 if no more samples are available). |

### release

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun release(): Unit
```

Make sure you call this when you're done to free up any resources instead of relying on the garbage collector to do this for you at some point in the future. 

### seekTo

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun seekTo(
    timeUs: Long, 
    mode: Int
): Unit
```

All selected tracks seek near the requested time according to the specified mode.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.media.MediaExtractor#SEEK_TO_PREVIOUS_SYNC](MediaExtractor.md), [android.media.MediaExtractor#SEEK_TO_NEXT_SYNC](MediaExtractor.md), or [android.media.MediaExtractor#SEEK_TO_CLOSEST_SYNC](MediaExtractor.md) |

### selectTrack

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun selectTrack(index: Int): Unit
```

Subsequent calls to [readSampleData](MediaExtractor.md)), [getSampleTrackIndex](MediaExtractor.md))and [getSampleTime](MediaExtractor.md))only retrieve information for the subset of tracks selected. Selecting the same track multiple times has no effect, the track is only selected once. 

### setDataSource

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setDataSource(
    context: Context, 
    uri: Uri, 
    headers: MutableMap<String!, String!>?
): Unit
```

Sets the data source as a content Uri.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android.content/Context.md):the Context to use when resolving the Uri This value cannot be`null`. |
| `uri` | [Uri](../android.net/Uri.md):the Content URI of the data you want to extract from. When`uri`refers to a network file the [android.Manifest.permission#INTERNET](../android/Manifest.permission.md) permission is required. This value cannot be`null`. |
| `headers` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?:the headers to be sent together with the request for the data. This can be`null`if no specific headers are to be sent with the request. |
| --- | --- |

### setDataSource

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setDataSource(afd: AssetFileDescriptor): Unit
```

Sets the data source (AssetFileDescriptor) to use. It is the caller's responsibility to close the file descriptor. It is safe to do so as soon as this call returns.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `afd` | [AssetFileDescriptor](../android.content.res/AssetFileDescriptor.md):the AssetFileDescriptor for the file you want to extract from. This value cannot be`null`. |

### setDataSource

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setDataSource(dataSource: MediaDataSource): Unit
```

Sets the data source (MediaDataSource) to use.

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dataSource` | [MediaDataSource](MediaDataSource.md):the MediaDataSource for the media you want to extract from This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|---------------------------|
| `java.lang.IllegalArgumentException` | if dataSource is invalid. |

### setDataSource

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setDataSource(fd: FileDescriptor): Unit
```

Sets the data source (FileDescriptor) to use. It is the caller's responsibility to close the file descriptor. It is safe to do so as soon as this call returns.

| Parameters ||
|------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fd` | [FileDescriptor](../java.io/FileDescriptor.md):the FileDescriptor for the file you want to extract from. This value cannot be`null`. |

### setDataSource

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setDataSource(
    fd: FileDescriptor, 
    offset: Long, 
    length: Long
): Unit
```

Sets the data source (FileDescriptor) to use. The FileDescriptor must be seekable (N.B. a LocalSocket is not seekable). It is the caller's responsibility to close the file descriptor. It is safe to do so as soon as this call returns.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fd` | [FileDescriptor](../java.io/FileDescriptor.md):the FileDescriptor for the file you want to extract from. This value cannot be`null`. |
| `offset` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the offset into the file where the data to be extracted starts, in bytes |
| `length` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the length in bytes of the data to be extracted |
| --- | --- |

### setDataSource

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setDataSource(path: String): Unit
```

Sets the data source (file-path or http URL) to use.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `path` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the path of the file, or the http URL of the stream When`path`refers to a local file, the file may actually be opened by a process other than the calling application. This implies that the pathname should be an absolute path (as any other process runs with unspecified current working directory), and that the pathname should reference a world-readable file. As an alternative, the application could first open the file for reading, and then use the file descriptor form [setDataSource(java.io.FileDescriptor)](MediaExtractor.md)). When`path`refers to a network file the [android.Manifest.permission#INTERNET](../android/Manifest.permission.md) permission is required. This value cannot be`null`. |

### setDataSource

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setDataSource(
    path: String, 
    headers: MutableMap<String!, String!>?
): Unit
```

Sets the data source (file-path or http URL) to use.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `path` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the path of the file, or the http URL When`path`refers to a network file the [android.Manifest.permission#INTERNET](../android/Manifest.permission.md) permission is required. This value cannot be`null`. |
| `headers` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?:the headers associated with the http request for the stream you want to play. This can be`null`if no specific headers are to be sent with the request. |

### setLogSessionId

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setLogSessionId(logSessionId: LogSessionId): Unit
```

Sets the [LogSessionId](../android.media.metrics/LogSessionId.md) for MediaExtractor.

| Parameters ||
|----------------|-------------------------------------------------------------------------------------------------------------------------------|
| `logSessionId` | [LogSessionId](../android.media.metrics/LogSessionId.md):This value cannot be`null`. |

### setMediaCas

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setMediaCas(mediaCas: MediaCas): Unit
```

**Deprecated:** *Use the`Descrambler`system API instead, or DRM public APIs like [MediaDrm](MediaDrm.md).*

Sets the MediaCas instance to use. This should be called after a successful setDataSource() if at least one track reports mime type of [android.media.MediaFormat#MIMETYPE_AUDIO_SCRAMBLED](MediaFormat.md) or [android.media.MediaFormat#MIMETYPE_VIDEO_SCRAMBLED](MediaFormat.md). Stream parsing will not proceed until a valid MediaCas object is provided.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `mediaCas` | [MediaCas](MediaCas.md):the MediaCas object to use. This value cannot be`null`. |

### unselectTrack

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun unselectTrack(index: Int): Unit
```

Subsequent calls to [readSampleData](MediaExtractor.md)), [getSampleTrackIndex](MediaExtractor.md))and [getSampleTime](MediaExtractor.md))only retrieve information for the subset of tracks selected.

## Protected methods

### finalize

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected fun finalize(): Unit
```

| Exceptions ||
|-----------------------|-------------------------------------|
| `java.lang.Throwable` | the`Exception`raised by this method |
