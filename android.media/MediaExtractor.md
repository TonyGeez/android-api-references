# MediaExtractor

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MediaExtractor

Kotlin| [Java](https://developer.android.com/reference/android/media/MediaExtractor "View this page in Java") 

```
class MediaExtractor
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.media.MediaExtractor](https://developer.android.com/reference/kotlin/android/media/MediaExtractor#) |

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

This class requires the [android.Manifest.permission#INTERNET](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#INTERNET:kotlin.String) permission when used with network-based content.

## Summary

| Nested classes ||
|---|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [CasInfo](https://developer.android.com/reference/kotlin/android/media/MediaExtractor.CasInfo) Describes the conditional access system used to scramble a track. |
| | [MetricsConstants](https://developer.android.com/reference/kotlin/android/media/MediaExtractor.MetricsConstants) <br /> |

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SAMPLE_FLAG_ENCRYPTED](https://developer.android.com/reference/kotlin/android/media/MediaExtractor#SAMPLE_FLAG_ENCRYPTED:kotlin.Int) The sample is (at least partially) encrypted, see also the documentation for [android.media.MediaCodec#queueSecureInputBuffer](https://developer.android.com/reference/kotlin/android/media/MediaCodec#queueSecureInputBuffer(kotlin.Int,%20kotlin.Int,%20android.media.MediaCodec.CryptoInfo,%20kotlin.Long,%20kotlin.Int)) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SAMPLE_FLAG_PARTIAL_FRAME](https://developer.android.com/reference/kotlin/android/media/MediaExtractor#SAMPLE_FLAG_PARTIAL_FRAME:kotlin.Int) This indicates that the buffer only contains part of a frame, and the decoder should batch the data until a buffer without this flag appears before decoding the frame. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SAMPLE_FLAG_SYNC](https://developer.android.com/reference/kotlin/android/media/MediaExtractor#SAMPLE_FLAG_SYNC:kotlin.Int) The sample is a sync sample (or in [MediaCodec](https://developer.android.com/reference/kotlin/android/media/MediaCodec)'s terminology it is a key frame. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SEEK_TO_CLOSEST_SYNC](https://developer.android.com/reference/kotlin/android/media/MediaExtractor#SEEK_TO_CLOSEST_SYNC:kotlin.Int) If possible, seek to the sync sample closest to the specified time |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SEEK_TO_NEXT_SYNC](https://developer.android.com/reference/kotlin/android/media/MediaExtractor#SEEK_TO_NEXT_SYNC:kotlin.Int) If possible, seek to a sync sample at or after the specified time |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SEEK_TO_PREVIOUS_SYNC](https://developer.android.com/reference/kotlin/android/media/MediaExtractor#SEEK_TO_PREVIOUS_SYNC:kotlin.Int) If possible, seek to a sync sample at or before the specified time |

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------|---|
| [MediaExtractor](https://developer.android.com/reference/kotlin/android/media/MediaExtractor#MediaExtractor())`()` <br /> |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [advance](https://developer.android.com/reference/kotlin/android/media/MediaExtractor#advance())`()` Advance to the next sample. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [AudioPresentation](https://developer.android.com/reference/kotlin/android/media/AudioPresentation)!\> | [getAudioPresentations](https://developer.android.com/reference/kotlin/android/media/MediaExtractor#getAudioPresentations(kotlin.Int))`(`trackIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the list of available audio presentations for the track. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getCachedDuration](https://developer.android.com/reference/kotlin/android/media/MediaExtractor#getCachedDuration())`()` Returns an estimate of how much data is presently cached in memory expressed in microseconds. |
| [MediaExtractor.CasInfo](https://developer.android.com/reference/kotlin/android/media/MediaExtractor.CasInfo)! | [getCasInfo](https://developer.android.com/reference/kotlin/android/media/MediaExtractor#getCasInfo(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves the information about the conditional access system used to scramble a track. |
| [DrmInitData](https://developer.android.com/reference/kotlin/android/media/DrmInitData)! | [getDrmInitData](https://developer.android.com/reference/kotlin/android/media/MediaExtractor#getDrmInitData())`()` Extract DRM initialization data if it exists |
| [LogSessionId](https://developer.android.com/reference/kotlin/android/media/metrics/LogSessionId) | [getLogSessionId](https://developer.android.com/reference/kotlin/android/media/MediaExtractor#getLogSessionId())`()` Returns the [LogSessionId](https://developer.android.com/reference/kotlin/android/media/metrics/LogSessionId) for MediaExtractor. |
| [PersistableBundle](https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#)! | [getMetrics](https://developer.android.com/reference/kotlin/android/media/MediaExtractor#getMetrics())`()` Return Metrics data about the current media container. |
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#)!, [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!\>? | [getPsshInfo](https://developer.android.com/reference/kotlin/android/media/MediaExtractor#getPsshInfo())`()` Get the PSSH info if present. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getSampleCryptoInfo](https://developer.android.com/reference/kotlin/android/media/MediaExtractor#getSampleCryptoInfo(android.media.MediaCodec.CryptoInfo))`(`info:` ` [MediaCodec.CryptoInfo](https://developer.android.com/reference/kotlin/android/media/MediaCodec.CryptoInfo)`)` If the sample flags indicate that the current sample is at least partially encrypted, this call returns relevant information about the structure of the sample data required for decryption. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSampleFlags](https://developer.android.com/reference/kotlin/android/media/MediaExtractor#getSampleFlags())`()` Returns the current sample's flags. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getSampleSize](https://developer.android.com/reference/kotlin/android/media/MediaExtractor#getSampleSize())`()` <br /> |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getSampleTime](https://developer.android.com/reference/kotlin/android/media/MediaExtractor#getSampleTime())`()` Returns the current sample's presentation time in microseconds. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSampleTrackIndex](https://developer.android.com/reference/kotlin/android/media/MediaExtractor#getSampleTrackIndex())`()` Returns the track index the current sample originates from (or -1 if no more samples are available) |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTrackCount](https://developer.android.com/reference/kotlin/android/media/MediaExtractor#getTrackCount())`()` Count the number of tracks found in the data source. |
| [MediaFormat](https://developer.android.com/reference/kotlin/android/media/MediaFormat) | [getTrackFormat](https://developer.android.com/reference/kotlin/android/media/MediaExtractor#getTrackFormat(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the track format at the specified index. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasCacheReachedEndOfStream](https://developer.android.com/reference/kotlin/android/media/MediaExtractor#hasCacheReachedEndOfStream())`()` Returns true iff we are caching data and the cache has reached the end of the data stream (for now, a future seek may of course restart the fetching of data). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [readSampleData](https://developer.android.com/reference/kotlin/android/media/MediaExtractor#readSampleData(java.nio.ByteBuffer,%20kotlin.Int))`(`byteBuf:` ` [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieve the current encoded sample and store it in the byte buffer starting at the given offset. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [release](https://developer.android.com/reference/kotlin/android/media/MediaExtractor#release())`()` Make sure you call this when you're done to free up any resources instead of relying on the garbage collector to do this for you at some point in the future. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [seekTo](https://developer.android.com/reference/kotlin/android/media/MediaExtractor#seekTo(kotlin.Long,%20kotlin.Int))`(`timeUs:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `mode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` All selected tracks seek near the requested time according to the specified mode. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [selectTrack](https://developer.android.com/reference/kotlin/android/media/MediaExtractor#selectTrack(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Subsequent calls to [readSampleData](https://developer.android.com/reference/kotlin/android/media/MediaExtractor#readSampleData(java.nio.ByteBuffer,%20kotlin.Int)), [getSampleTrackIndex](https://developer.android.com/reference/kotlin/android/media/MediaExtractor#getSampleTrackIndex())and [getSampleTime](https://developer.android.com/reference/kotlin/android/media/MediaExtractor#getSampleTime())only retrieve information for the subset of tracks selected. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDataSource](https://developer.android.com/reference/kotlin/android/media/MediaExtractor#setDataSource(android.content.Context,%20android.net.Uri,%20kotlin.collections.MutableMap))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)`, `uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `headers:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>?`)` Sets the data source as a content Uri. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDataSource](https://developer.android.com/reference/kotlin/android/media/MediaExtractor#setDataSource(android.content.res.AssetFileDescriptor))`(`afd:` ` [AssetFileDescriptor](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor.html#)`)` Sets the data source (AssetFileDescriptor) to use. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDataSource](https://developer.android.com/reference/kotlin/android/media/MediaExtractor#setDataSource(android.media.MediaDataSource))`(`dataSource:` ` [MediaDataSource](https://developer.android.com/reference/kotlin/android/media/MediaDataSource)`)` Sets the data source (MediaDataSource) to use. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDataSource](https://developer.android.com/reference/kotlin/android/media/MediaExtractor#setDataSource(java.io.FileDescriptor))`(`fd:` ` [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#)`)` Sets the data source (FileDescriptor) to use. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDataSource](https://developer.android.com/reference/kotlin/android/media/MediaExtractor#setDataSource(java.io.FileDescriptor,%20kotlin.Long,%20kotlin.Long))`(`fd:` ` [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#)`, `offset:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `length:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the data source (FileDescriptor) to use. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDataSource](https://developer.android.com/reference/kotlin/android/media/MediaExtractor#setDataSource(kotlin.String))`(`path:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Sets the data source (file-path or http URL) to use. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDataSource](https://developer.android.com/reference/kotlin/android/media/MediaExtractor#setDataSource(kotlin.String,%20kotlin.collections.MutableMap))`(`path:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `headers:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>?`)` Sets the data source (file-path or http URL) to use. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLogSessionId](https://developer.android.com/reference/kotlin/android/media/MediaExtractor#setLogSessionId(android.media.metrics.LogSessionId))`(`logSessionId:` ` [LogSessionId](https://developer.android.com/reference/kotlin/android/media/metrics/LogSessionId)`)` Sets the [LogSessionId](https://developer.android.com/reference/kotlin/android/media/metrics/LogSessionId) for MediaExtractor. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMediaCas](https://developer.android.com/reference/kotlin/android/media/MediaExtractor#setMediaCas(android.media.MediaCas))`(`mediaCas:` ` [MediaCas](https://developer.android.com/reference/kotlin/android/media/MediaCas)`)` Sets the MediaCas instance to use. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unselectTrack](https://developer.android.com/reference/kotlin/android/media/MediaExtractor#unselectTrack(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Subsequent calls to [readSampleData](https://developer.android.com/reference/kotlin/android/media/MediaExtractor#readSampleData(java.nio.ByteBuffer,%20kotlin.Int)), [getSampleTrackIndex](https://developer.android.com/reference/kotlin/android/media/MediaExtractor#getSampleTrackIndex())and [getSampleTime](https://developer.android.com/reference/kotlin/android/media/MediaExtractor#getSampleTime())only retrieve information for the subset of tracks selected. |

| Protected methods ||
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](https://developer.android.com/reference/kotlin/android/media/MediaExtractor#finalize())`()` <br /> |

## Constants

### SAMPLE_FLAG_ENCRYPTED

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SAMPLE_FLAG_ENCRYPTED: Int
```

The sample is (at least partially) encrypted, see also the documentation for [android.media.MediaCodec#queueSecureInputBuffer](https://developer.android.com/reference/kotlin/android/media/MediaCodec#queueSecureInputBuffer(kotlin.Int,%20kotlin.Int,%20android.media.MediaCodec.CryptoInfo,%20kotlin.Long,%20kotlin.Int)) 

 Value: 2

### SAMPLE_FLAG_PARTIAL_FRAME

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SAMPLE_FLAG_PARTIAL_FRAME: Int
```

This indicates that the buffer only contains part of a frame, and the decoder should batch the data until a buffer without this flag appears before decoding the frame. 

 Value: 4

**See Also**

- [android.media.MediaCodec#BUFFER_FLAG_PARTIAL_FRAME](https://developer.android.com/reference/kotlin/android/media/MediaCodec#BUFFER_FLAG_PARTIAL_FRAME:kotlin.Int) 

### SAMPLE_FLAG_SYNC

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SAMPLE_FLAG_SYNC: Int
```

The sample is a sync sample (or in [MediaCodec](https://developer.android.com/reference/kotlin/android/media/MediaCodec)'s terminology it is a key frame.) 

 Value: 1

**See Also**

- [android.media.MediaCodec#BUFFER_FLAG_KEY_FRAME](https://developer.android.com/reference/kotlin/android/media/MediaCodec#BUFFER_FLAG_KEY_FRAME:kotlin.Int) 

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

Advance to the next sample. Returns false if no more sample data is available (end of stream). When extracting a local file, the behaviors of [advance](https://developer.android.com/reference/kotlin/android/media/MediaExtractor#advance())and [readSampleData](https://developer.android.com/reference/kotlin/android/media/MediaExtractor#readSampleData(java.nio.ByteBuffer,%20kotlin.Int))are undefined in presence of concurrent writes to the same local file; more specifically, end of stream could be signalled earlier than expected. 

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
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [AudioPresentation](https://developer.android.com/reference/kotlin/android/media/AudioPresentation)!> | a list of available audio presentations for a given valid audio track index. The list will be empty if the source does not contain any audio presentations. This value cannot be`null`. |

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
| [MediaExtractor.CasInfo](https://developer.android.com/reference/kotlin/android/media/MediaExtractor.CasInfo)! | an [CasInfo](https://developer.android.com/reference/kotlin/android/media/MediaExtractor.CasInfo) object describing the conditional access system. |

### getDrmInitData

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDrmInitData(): DrmInitData!
```

Extract DRM initialization data if it exists

If the media contains a PSSH box, only PSSH version 0 is supported. The result for media with other PSSH versions is undefined.

| Return ||
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [DrmInitData](https://developer.android.com/reference/kotlin/android/media/DrmInitData)! | DRM initialization data in the content, or`null`if no recognizable DRM format is found; |

**See Also**

- [android.media.DrmInitData](https://developer.android.com/reference/kotlin/android/media/DrmInitData) 

### getLogSessionId

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLogSessionId(): LogSessionId
```

Returns the [LogSessionId](https://developer.android.com/reference/kotlin/android/media/metrics/LogSessionId) for MediaExtractor.

| Return ||
|---------------------------------------------------------------------------------------------------|-----------------------------|
| [LogSessionId](https://developer.android.com/reference/kotlin/android/media/metrics/LogSessionId) | This value cannot be`null`. |

### getMetrics

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMetrics(): PersistableBundle!
```

Return Metrics data about the current media container.

| Return ||
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [PersistableBundle](https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#)! | a [PersistableBundle](https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#) containing the set of attributes and values available for the media container being handled by this instance of MediaExtractor. The attributes are descibed in [MetricsConstants](https://developer.android.com/reference/kotlin/android/media/MediaExtractor.MetricsConstants). Additional vendor-specific fields may also be present in the return value. |

### getPsshInfo

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPsshInfo(): MutableMap<UUID!, ByteArray!>?
```

Get the PSSH info if present.

This method only supports version 0 PSSH boxes. The result for other versions is undefined.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#)!,` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!>? | a map of uuid-to-bytes, with the uuid specifying the crypto scheme, and the bytes being the data specific to that scheme. This can be`null`if the source does not contain PSSH info. |

### getSampleCryptoInfo

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSampleCryptoInfo(info: MediaCodec.CryptoInfo): Boolean
```

If the sample flags indicate that the current sample is at least partially encrypted, this call returns relevant information about the structure of the sample data required for decryption.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `info` | [MediaCodec.CryptoInfo](https://developer.android.com/reference/kotlin/android/media/MediaCodec.CryptoInfo):The android.media.MediaCodec.CryptoInfo structure to be filled in. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true iff the sample flags contain [SAMPLE_FLAG_ENCRYPTED](https://developer.android.com/reference/kotlin/android/media/MediaExtractor#SAMPLE_FLAG_ENCRYPTED:kotlin.Int) |

### getSampleFlags

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSampleFlags(): Int
```

Returns the current sample's flags.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is either`0`or a combination of [android.media.MediaExtractor#SAMPLE_FLAG_SYNC](https://developer.android.com/reference/kotlin/android/media/MediaExtractor#SAMPLE_FLAG_SYNC:kotlin.Int), [android.media.MediaExtractor#SAMPLE_FLAG_ENCRYPTED](https://developer.android.com/reference/kotlin/android/media/MediaExtractor#SAMPLE_FLAG_ENCRYPTED:kotlin.Int), and [android.media.MediaExtractor#SAMPLE_FLAG_PARTIAL_FRAME](https://developer.android.com/reference/kotlin/android/media/MediaExtractor#SAMPLE_FLAG_PARTIAL_FRAME:kotlin.Int) |

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

Get the track format at the specified index. More detail on the representation can be found at [android.media.MediaCodec](https://developer.android.com/reference/kotlin/android/media/MediaCodec)

The following table summarizes support for format keys across android releases:

| OS Version(s) | `MediaFormat`keys used for |||
| OS Version(s) | All Tracks | Audio Tracks | Video Tracks |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [android.os.Build.VERSION_CODES#JELLY_BEAN](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#JELLY_BEAN:kotlin.Int) | [MediaFormat.KEY_MIME](https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_MIME:kotlin.String), [MediaFormat.KEY_DURATION](https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_DURATION:kotlin.String), [MediaFormat.KEY_MAX_INPUT_SIZE](https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_MAX_INPUT_SIZE:kotlin.String) | [MediaFormat.KEY_SAMPLE_RATE](https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_SAMPLE_RATE:kotlin.String), [MediaFormat.KEY_CHANNEL_COUNT](https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_CHANNEL_COUNT:kotlin.String), [MediaFormat.KEY_CHANNEL_MASK](https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_CHANNEL_MASK:kotlin.String), gapless playback information.mp3, .mp4, [MediaFormat.KEY_IS_ADTS](https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_IS_ADTS:kotlin.String) AAC if streaming, codec-specific dataAAC, Vorbis | [MediaFormat.KEY_WIDTH](https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_WIDTH:kotlin.String), [MediaFormat.KEY_HEIGHT](https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_HEIGHT:kotlin.String), codec-specific dataAVC, MPEG4 |
| [android.os.Build.VERSION_CODES#JELLY_BEAN_MR1](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#JELLY_BEAN_MR1:kotlin.Int) | [MediaFormat.KEY_MIME](https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_MIME:kotlin.String), [MediaFormat.KEY_DURATION](https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_DURATION:kotlin.String), [MediaFormat.KEY_MAX_INPUT_SIZE](https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_MAX_INPUT_SIZE:kotlin.String) | [MediaFormat.KEY_SAMPLE_RATE](https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_SAMPLE_RATE:kotlin.String), [MediaFormat.KEY_CHANNEL_COUNT](https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_CHANNEL_COUNT:kotlin.String), [MediaFormat.KEY_CHANNEL_MASK](https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_CHANNEL_MASK:kotlin.String), gapless playback information.mp3, .mp4, [MediaFormat.KEY_IS_ADTS](https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_IS_ADTS:kotlin.String) AAC if streaming, codec-specific dataAAC, Vorbis | [MediaFormat.KEY_WIDTH](https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_WIDTH:kotlin.String), [MediaFormat.KEY_HEIGHT](https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_HEIGHT:kotlin.String), codec-specific dataAVC, MPEG4 |
| [android.os.Build.VERSION_CODES#JELLY_BEAN_MR2](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#JELLY_BEAN_MR2:kotlin.Int) | [MediaFormat.KEY_MIME](https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_MIME:kotlin.String), [MediaFormat.KEY_DURATION](https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_DURATION:kotlin.String), [MediaFormat.KEY_MAX_INPUT_SIZE](https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_MAX_INPUT_SIZE:kotlin.String) | [MediaFormat.KEY_SAMPLE_RATE](https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_SAMPLE_RATE:kotlin.String), [MediaFormat.KEY_CHANNEL_COUNT](https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_CHANNEL_COUNT:kotlin.String), [MediaFormat.KEY_CHANNEL_MASK](https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_CHANNEL_MASK:kotlin.String), gapless playback information.mp3, .mp4, [MediaFormat.KEY_IS_ADTS](https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_IS_ADTS:kotlin.String) AAC if streaming, codec-specific dataAAC, Vorbis | as above, plus Pixel aspect ratio informationAVC, \* |
| [android.os.Build.VERSION_CODES#KITKAT](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#KITKAT:kotlin.Int) | [MediaFormat.KEY_MIME](https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_MIME:kotlin.String), [MediaFormat.KEY_DURATION](https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_DURATION:kotlin.String), [MediaFormat.KEY_MAX_INPUT_SIZE](https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_MAX_INPUT_SIZE:kotlin.String) | [MediaFormat.KEY_SAMPLE_RATE](https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_SAMPLE_RATE:kotlin.String), [MediaFormat.KEY_CHANNEL_COUNT](https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_CHANNEL_COUNT:kotlin.String), [MediaFormat.KEY_CHANNEL_MASK](https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_CHANNEL_MASK:kotlin.String), gapless playback information.mp3, .mp4, [MediaFormat.KEY_IS_ADTS](https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_IS_ADTS:kotlin.String) AAC if streaming, codec-specific dataAAC, Vorbis | as above, plus Pixel aspect ratio informationAVC, \* |
| [android.os.Build.VERSION_CODES#KITKAT_WATCH](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#KITKAT_WATCH:kotlin.Int) | [MediaFormat.KEY_MIME](https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_MIME:kotlin.String), [MediaFormat.KEY_DURATION](https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_DURATION:kotlin.String), [MediaFormat.KEY_MAX_INPUT_SIZE](https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_MAX_INPUT_SIZE:kotlin.String) | [MediaFormat.KEY_SAMPLE_RATE](https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_SAMPLE_RATE:kotlin.String), [MediaFormat.KEY_CHANNEL_COUNT](https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_CHANNEL_COUNT:kotlin.String), [MediaFormat.KEY_CHANNEL_MASK](https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_CHANNEL_MASK:kotlin.String), gapless playback information.mp3, .mp4, [MediaFormat.KEY_IS_ADTS](https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_IS_ADTS:kotlin.String) AAC if streaming, codec-specific dataAAC, Vorbis | as above, plus Pixel aspect ratio informationAVC, \* |
| [android.os.Build.VERSION_CODES#LOLLIPOP](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#LOLLIPOP:kotlin.Int) | [MediaFormat.KEY_MIME](https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_MIME:kotlin.String), [MediaFormat.KEY_DURATION](https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_DURATION:kotlin.String), [MediaFormat.KEY_MAX_INPUT_SIZE](https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_MAX_INPUT_SIZE:kotlin.String) | as above, plus [MediaFormat.KEY_BIT_RATE](https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_BIT_RATE:kotlin.String) AAC, codec-specific dataOpus | as above, plus [MediaFormat.KEY_ROTATION](https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_ROTATION:kotlin.String).mp4, [MediaFormat.KEY_BIT_RATE](https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_BIT_RATE:kotlin.String) MPEG4, codec-specific dataHEVC |
| [android.os.Build.VERSION_CODES#LOLLIPOP_MR1](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#LOLLIPOP_MR1:kotlin.Int) | [MediaFormat.KEY_MIME](https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_MIME:kotlin.String), [MediaFormat.KEY_DURATION](https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_DURATION:kotlin.String), [MediaFormat.KEY_MAX_INPUT_SIZE](https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_MAX_INPUT_SIZE:kotlin.String) | as above, plus [MediaFormat.KEY_BIT_RATE](https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_BIT_RATE:kotlin.String) AAC, codec-specific dataOpus | as above, plus [MediaFormat.KEY_ROTATION](https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_ROTATION:kotlin.String).mp4, [MediaFormat.KEY_BIT_RATE](https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_BIT_RATE:kotlin.String) MPEG4, codec-specific dataHEVC |
| [android.os.Build.VERSION_CODES#M](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#M:kotlin.Int) | [MediaFormat.KEY_MIME](https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_MIME:kotlin.String), [MediaFormat.KEY_DURATION](https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_DURATION:kotlin.String), [MediaFormat.KEY_MAX_INPUT_SIZE](https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_MAX_INPUT_SIZE:kotlin.String) | as above, plus gapless playback informationOpus | as above, plus [MediaFormat.KEY_FRAME_RATE](https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_FRAME_RATE:kotlin.String)(integer) |
| [android.os.Build.VERSION_CODES#N](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#N:kotlin.Int) | as above, plus [MediaFormat.KEY_TRACK_ID](https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_TRACK_ID:kotlin.String), [MediaFormat.KEY_BIT_RATE](https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_BIT_RATE:kotlin.String), .mp4 | as above, plus [MediaFormat.KEY_PCM_ENCODING](https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_PCM_ENCODING:kotlin.String), [MediaFormat.KEY_PROFILE](https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_PROFILE:kotlin.String) AAC | as above, plus [MediaFormat.KEY_HDR_STATIC_INFO](https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_HDR_STATIC_INFO:kotlin.String), .webm, [MediaFormat.KEY_COLOR_STANDARD](https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_COLOR_STANDARD:kotlin.String), [MediaFormat.KEY_COLOR_TRANSFER](https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_COLOR_TRANSFER:kotlin.String), [MediaFormat.KEY_COLOR_RANGE](https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_COLOR_RANGE:kotlin.String), [MediaFormat.KEY_PROFILE](https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_PROFILE:kotlin.String) MPEG2, H.263, MPEG4, AVC, HEVC, VP9, [MediaFormat.KEY_LEVEL](https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_LEVEL:kotlin.String) H.263, MPEG4, AVC, HEVC, VP9, codec-specific dataVP9 |
| **Notes:** #: container-specified value only. .mp4, .webm...: for listed containers MPEG4, AAC...: for listed codecs ||||
| Note that that level information contained in the container many times does not match the level of the actual bitstream. You may want to clear the level using`MediaFormat.setString(KEY_LEVEL, null)`before using the track format to find a decoder that can play back a particular track. ||||
| **\*Pixel (sample) aspect ratio**is returned in the following keys. The display width can be calculated for example as: display-width = display-height \* crop-width / crop-height \* sar-width / sar-height ||||
| `"sar-width"` | Integer | Pixel aspect ratio width ||
| `"sar-height"` | Integer | Pixel aspect ratio height ||

### hasCacheReachedEndOfStream

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasCacheReachedEndOfStream(): Boolean
```

Returns true iff we are caching data and the cache has reached the end of the data stream (for now, a future seek may of course restart the fetching of data). This API only returns a meaningful result if [getCachedDuration](https://developer.android.com/reference/kotlin/android/media/MediaExtractor#getCachedDuration())indicates the presence of a cache, i.e. does NOT return -1. 

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
| `byteBuf` | [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#):the destination byte buffer This value cannot be`null`. |

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
| `mode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.media.MediaExtractor#SEEK_TO_PREVIOUS_SYNC](https://developer.android.com/reference/kotlin/android/media/MediaExtractor#SEEK_TO_PREVIOUS_SYNC:kotlin.Int), [android.media.MediaExtractor#SEEK_TO_NEXT_SYNC](https://developer.android.com/reference/kotlin/android/media/MediaExtractor#SEEK_TO_NEXT_SYNC:kotlin.Int), or [android.media.MediaExtractor#SEEK_TO_CLOSEST_SYNC](https://developer.android.com/reference/kotlin/android/media/MediaExtractor#SEEK_TO_CLOSEST_SYNC:kotlin.Int) |

### selectTrack

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun selectTrack(index: Int): Unit
```

Subsequent calls to [readSampleData](https://developer.android.com/reference/kotlin/android/media/MediaExtractor#readSampleData(java.nio.ByteBuffer,%20kotlin.Int)), [getSampleTrackIndex](https://developer.android.com/reference/kotlin/android/media/MediaExtractor#getSampleTrackIndex())and [getSampleTime](https://developer.android.com/reference/kotlin/android/media/MediaExtractor#getSampleTime())only retrieve information for the subset of tracks selected. Selecting the same track multiple times has no effect, the track is only selected once. 

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
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#):the Context to use when resolving the Uri This value cannot be`null`. |
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):the Content URI of the data you want to extract from. When`uri`refers to a network file the [android.Manifest.permission#INTERNET](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#INTERNET:kotlin.String) permission is required. This value cannot be`null`. |
| `headers` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?:the headers to be sent together with the request for the data. This can be`null`if no specific headers are to be sent with the request. |

### setDataSource

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setDataSource(afd: AssetFileDescriptor): Unit
```

Sets the data source (AssetFileDescriptor) to use. It is the caller's responsibility to close the file descriptor. It is safe to do so as soon as this call returns.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `afd` | [AssetFileDescriptor](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor.html#):the AssetFileDescriptor for the file you want to extract from. This value cannot be`null`. |

### setDataSource

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setDataSource(dataSource: MediaDataSource): Unit
```

Sets the data source (MediaDataSource) to use.

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dataSource` | [MediaDataSource](https://developer.android.com/reference/kotlin/android/media/MediaDataSource):the MediaDataSource for the media you want to extract from This value cannot be`null`. |

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
| `fd` | [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#):the FileDescriptor for the file you want to extract from. This value cannot be`null`. |

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
| `fd` | [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#):the FileDescriptor for the file you want to extract from. This value cannot be`null`. |
| `offset` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the offset into the file where the data to be extracted starts, in bytes |
| `length` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the length in bytes of the data to be extracted |

### setDataSource

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setDataSource(path: String): Unit
```

Sets the data source (file-path or http URL) to use.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `path` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the path of the file, or the http URL of the stream When`path`refers to a local file, the file may actually be opened by a process other than the calling application. This implies that the pathname should be an absolute path (as any other process runs with unspecified current working directory), and that the pathname should reference a world-readable file. As an alternative, the application could first open the file for reading, and then use the file descriptor form [setDataSource(java.io.FileDescriptor)](https://developer.android.com/reference/kotlin/android/media/MediaExtractor#setDataSource(java.io.FileDescriptor)). When`path`refers to a network file the [android.Manifest.permission#INTERNET](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#INTERNET:kotlin.String) permission is required. This value cannot be`null`. |

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
| `path` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the path of the file, or the http URL When`path`refers to a network file the [android.Manifest.permission#INTERNET](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#INTERNET:kotlin.String) permission is required. This value cannot be`null`. |
| `headers` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?:the headers associated with the http request for the stream you want to play. This can be`null`if no specific headers are to be sent with the request. |

### setLogSessionId

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setLogSessionId(logSessionId: LogSessionId): Unit
```

Sets the [LogSessionId](https://developer.android.com/reference/kotlin/android/media/metrics/LogSessionId) for MediaExtractor.

| Parameters ||
|----------------|-------------------------------------------------------------------------------------------------------------------------------|
| `logSessionId` | [LogSessionId](https://developer.android.com/reference/kotlin/android/media/metrics/LogSessionId):This value cannot be`null`. |

### setMediaCas

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setMediaCas(mediaCas: MediaCas): Unit
```

**Deprecated:** *Use the`Descrambler`system API instead, or DRM public APIs like [MediaDrm](https://developer.android.com/reference/kotlin/android/media/MediaDrm).*

Sets the MediaCas instance to use. This should be called after a successful setDataSource() if at least one track reports mime type of [android.media.MediaFormat#MIMETYPE_AUDIO_SCRAMBLED](https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_AUDIO_SCRAMBLED:kotlin.String) or [android.media.MediaFormat#MIMETYPE_VIDEO_SCRAMBLED](https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_VIDEO_SCRAMBLED:kotlin.String). Stream parsing will not proceed until a valid MediaCas object is provided.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `mediaCas` | [MediaCas](https://developer.android.com/reference/kotlin/android/media/MediaCas):the MediaCas object to use. This value cannot be`null`. |

### unselectTrack

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun unselectTrack(index: Int): Unit
```

Subsequent calls to [readSampleData](https://developer.android.com/reference/kotlin/android/media/MediaExtractor#readSampleData(java.nio.ByteBuffer,%20kotlin.Int)), [getSampleTrackIndex](https://developer.android.com/reference/kotlin/android/media/MediaExtractor#getSampleTrackIndex())and [getSampleTime](https://developer.android.com/reference/kotlin/android/media/MediaExtractor#getSampleTime())only retrieve information for the subset of tracks selected.

## Protected methods

### finalize

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected fun finalize(): Unit
```

| Exceptions ||
|-----------------------|-------------------------------------|
| `java.lang.Throwable` | the`Exception`raised by this method |
