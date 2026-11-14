# SubtitleData

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SubtitleData

Kotlin| [Java](SubtitleData.md) 
| --- | --- |

```
class SubtitleData
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.SubtitleData](SubtitleData.md) |

Class encapsulating subtitle data, as received through the [MediaPlayer.OnSubtitleDataListener](../android/media/MediaPlayer.OnSubtitleDataListener.md) interface. The subtitle data includes:

- the track index
- the start time (in microseconds) of the data
- the duration (in microseconds) of the data
- the actual data.

The data is stored in a byte-array, and is encoded in one of the supported in-band subtitle formats. The subtitle encoding is determined by the MIME type of the [MediaPlayer.TrackInfo](../android/media/MediaPlayer.TrackInfo.md) of the subtitle track, one of [MediaFormat.MIMETYPE_TEXT_CEA_608](MediaFormat.md), [MediaFormat.MIMETYPE_TEXT_CEA_708](MediaFormat.md), [MediaFormat.MIMETYPE_TEXT_VTT](MediaFormat.md).

<br />

Here is an example of iterating over the tracks of a [MediaPlayer](MediaPlayer.md), and checking which encoding is used for the subtitle tracks:

<br />

```kotlin
MediaPlayer mp = new MediaPlayer();
  mp.setDataSource(myContentLocation);
  mp.prepare(); // synchronous prepare, ready to use when method returns
  final TrackInfo[] trackInfos = mp.getTrackInfo();
  for (TrackInfo info : trackInfo) {
      if (info.getTrackType() == TrackInfo.MEDIA_TRACK_TYPE_SUBTITLE) {
          final String mime = info.getFormat().getString(MediaFormat.KEY_MIME);
          if (MediaFormat.MIMETYPE_TEXT_CEA_608.equals(mime) {
              // subtitle encoding is CEA 608
          } else if (MediaFormat.MIMETYPE_TEXT_CEA_708.equals(mime) {
              // subtitle encoding is CEA 708
          } else if (MediaFormat.MIMETYPE_TEXT_VTT.equals(mime) {
              // subtitle encoding is WebVTT
          }
      }
  }
  
```

See [MediaPlayer.setOnSubtitleDataListener(android.media.MediaPlayer.OnSubtitleDataListener, android.os.Handler)](MediaPlayer.md))to receive subtitle data from a MediaPlayer object.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SubtitleData](SubtitleData.md))`(`trackIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `startTimeUs:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `durationUs:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `data:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`)` Constructor. |

| Public methods ||
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | [getData](SubtitleData.md))`()` Returns the encoded data for the subtitle content. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getDurationUs](SubtitleData.md))`()` Returns the duration in microsecond during which the subtitle should be displayed. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getStartTimeUs](SubtitleData.md))`()` Returns the media time at which the subtitle should be displayed, expressed in microseconds. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTrackIndex](SubtitleData.md))`()` Returns the index of the media player track which contains this subtitle data. |

## Public constructors

### SubtitleData

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SubtitleData(
    trackIndex: Int, 
    startTimeUs: Long, 
    durationUs: Long, 
    data: ByteArray)
```

Constructor.

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `trackIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index of the media player track which contains this subtitle data. |
| `startTimeUs` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the start time in microsecond for the subtitle data |
| `durationUs` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the duration in microsecond for the subtitle data |
| --- | --- |
| `data` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html):the data array for the subtitle data. It should not be null. No data copying is made. |

## Public methods

### getData

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getData(): ByteArray
```

Returns the encoded data for the subtitle content. Encoding format depends on the subtitle type, refer to [CEA 708](https://en.wikipedia.org/wiki/CEA-708), [CEA/EIA 608](https://en.wikipedia.org/wiki/EIA-608) and [WebVTT](https://www.w3.org/TR/webvtt1/), defined by the MIME type of the subtitle track.

| Return ||
|-----------------------------------------------------------------------------------------|-------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | the encoded subtitle data This value cannot be`null`. |

### getDurationUs

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDurationUs(): Long
```

Returns the duration in microsecond during which the subtitle should be displayed.

| Return ||
|------------------------------------------------------------------------------|---------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the display duration for the subtitle |

### getStartTimeUs

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getStartTimeUs(): Long
```

Returns the media time at which the subtitle should be displayed, expressed in microseconds.

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the display start time for the subtitle |

### getTrackIndex

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTrackIndex(): Int
```

Returns the index of the media player track which contains this subtitle data.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | an index in the array returned by [MediaPlayer.getTrackInfo()](MediaPlayer.md)). |
