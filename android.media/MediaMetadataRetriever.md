# MediaMetadataRetriever

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MediaMetadataRetriever

Kotlin| [Java](../android/media/MediaMetadataRetriever.md) 
| --- | --- |

```
open class MediaMetadataRetriever : AutoCloseable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.MediaMetadataRetriever](../android/media/MediaMetadataRetriever.md) |

MediaMetadataRetriever class provides a unified interface for retrieving frame and meta data from an input media file.

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------------------------|
| | [BitmapParams](../android/media/MediaMetadataRetriever.BitmapParams.md) <br /> |

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_ALBUM](../android/media/MediaMetadataRetriever.md) The metadata key to retrieve the information about the album title of the data source. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_ALBUMARTIST](../android/media/MediaMetadataRetriever.md) The metadata key to retrieve the information about the performers or artist associated with the data source. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_ARTIST](../android/media/MediaMetadataRetriever.md) The metadata key to retrieve the information about the artist of the data source. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_AUTHOR](../android/media/MediaMetadataRetriever.md) The metadata key to retrieve the information about the author of the data source. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_BITRATE](../android/media/MediaMetadataRetriever.md) This key retrieves the average bitrate (in bits/sec), if available. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_BITS_PER_SAMPLE](../android/media/MediaMetadataRetriever.md) This key retrieves the bits per sample in numbers of bits, if available. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_CAPTURE_FRAMERATE](../android/media/MediaMetadataRetriever.md) This key retrieves the original capture framerate, if it's available. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_CD_TRACK_NUMBER](../android/media/MediaMetadataRetriever.md) The metadata key to retrieve the numeric string describing the order of the audio data source on its original recording. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_COLOR_RANGE](../android/media/MediaMetadataRetriever.md) This key retrieves the color range, if available. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_COLOR_STANDARD](../android/media/MediaMetadataRetriever.md) This key retrieves the color standard, if available. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_COLOR_TRANSFER](../android/media/MediaMetadataRetriever.md) This key retrieves the color transfer, if available. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_COMPILATION](../android/media/MediaMetadataRetriever.md) The metadata key to retrieve the music album compilation status. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_COMPOSER](../android/media/MediaMetadataRetriever.md) The metadata key to retrieve the information about the composer of the data source. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_DATE](../android/media/MediaMetadataRetriever.md) The metadata key to retrieve the date when the data source was created or modified. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_DISC_NUMBER](../android/media/MediaMetadataRetriever.md) The metadata key to retrieve the numberic string that describes which part of a set the audio data source comes from. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_DURATION](../android/media/MediaMetadataRetriever.md) The metadata key to retrieve the playback duration (in ms) of the data source. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_EXIF_LENGTH](../android/media/MediaMetadataRetriever.md) If the media contains EXIF data, this key retrieves the length (in bytes) of the data. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_EXIF_OFFSET](../android/media/MediaMetadataRetriever.md) If the media contains EXIF data, this key retrieves the offset (in bytes) of the data. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_GENRE](../android/media/MediaMetadataRetriever.md) The metadata key to retrieve the content type or genre of the data source. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_HAS_AUDIO](../android/media/MediaMetadataRetriever.md) If this key exists the media contains audio content. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_HAS_IMAGE](../android/media/MediaMetadataRetriever.md) If this key exists the media contains still image content. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_HAS_VIDEO](../android/media/MediaMetadataRetriever.md) If this key exists the media contains video content. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_IMAGE_COUNT](../android/media/MediaMetadataRetriever.md) If the media contains still images, this key retrieves the number of still images. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_IMAGE_HEIGHT](../android/media/MediaMetadataRetriever.md) If the media contains still images, this key retrieves the height of the primary image. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_IMAGE_PRIMARY](../android/media/MediaMetadataRetriever.md) If the media contains still images, this key retrieves the image index of the primary image. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_IMAGE_ROTATION](../android/media/MediaMetadataRetriever.md) If the media contains still images, this key retrieves the rotation angle (in degrees clockwise) of the primary image. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_IMAGE_WIDTH](../android/media/MediaMetadataRetriever.md) If the media contains still images, this key retrieves the width of the primary image. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_LOCATION](../android/media/MediaMetadataRetriever.md) This key retrieves the location information, if available. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_MIMETYPE](../android/media/MediaMetadataRetriever.md) The metadata key to retrieve the mime type of the data source. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_NUM_TRACKS](../android/media/MediaMetadataRetriever.md) The metadata key to retrieve the number of tracks, such as audio, video, text, in the data source, such as a mp4 or 3gpp file. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_SAMPLERATE](../android/media/MediaMetadataRetriever.md) This key retrieves the sample rate in Hz, if available. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_TITLE](../android/media/MediaMetadataRetriever.md) The metadata key to retrieve the data source title. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_VIDEO_FRAME_COUNT](../android/media/MediaMetadataRetriever.md) If the media contains video and this key exists, it retrieves the total number of frames in the video sequence. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_VIDEO_HEIGHT](../android/media/MediaMetadataRetriever.md) If the media contains video, this key retrieves its height. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_VIDEO_ROTATION](../android/media/MediaMetadataRetriever.md) This key retrieves the video rotation angle in degrees, if available. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_VIDEO_WIDTH](../android/media/MediaMetadataRetriever.md) If the media contains video, this key retrieves its width. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_WRITER](../android/media/MediaMetadataRetriever.md) The metadata key to retrieve the information of the writer (such as lyricist) of the data source. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_XMP_LENGTH](../android/media/MediaMetadataRetriever.md) If the media contains XMP data, this key retrieves the length (in bytes) of the data. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_XMP_OFFSET](../android/media/MediaMetadataRetriever.md) If the media contains XMP data, this key retrieves the offset (in bytes) of the data. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_YEAR](../android/media/MediaMetadataRetriever.md) The metadata key to retrieve the year when the data source was created or modified. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [OPTION_CLOSEST](../android/media/MediaMetadataRetriever.md) This option is used with [getFrameAtTime(long,int)](../android/media/MediaMetadataRetriever.md))to retrieve a frame (not necessarily a key frame) associated with a data source that is located closest to or at the given time. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [OPTION_CLOSEST_SYNC](../android/media/MediaMetadataRetriever.md) This option is used with [getFrameAtTime(long,int)](../android/media/MediaMetadataRetriever.md))to retrieve a sync (or key) frame associated with a data source that is located closest to (in time) or at the given time. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [OPTION_NEXT_SYNC](../android/media/MediaMetadataRetriever.md) This option is used with [getFrameAtTime(long,int)](../android/media/MediaMetadataRetriever.md))to retrieve a sync (or key) frame associated with a data source that is located right after or at the given time. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [OPTION_PREVIOUS_SYNC](../android/media/MediaMetadataRetriever.md) This option is used with [getFrameAtTime(long,int)](../android/media/MediaMetadataRetriever.md))to retrieve a sync (or key) frame associated with a data source that is located right before or at the given time. |

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [MediaMetadataRetriever](../android/media/MediaMetadataRetriever.md))`()` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](../android/media/MediaMetadataRetriever.md))`()` Releases any acquired resources. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [extractMetadata](../android/media/MediaMetadataRetriever.md))`(`keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Call this method after setDataSource(). |
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | [getEmbeddedPicture](../android/media/MediaMetadataRetriever.md))`()` Call this method after setDataSource(). |
| --- | --- |
| open [Bitmap](../android/graphics/Bitmap.md)? | [getFrameAtIndex](../android/media/MediaMetadataRetriever.md))`(`frameIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` This method is similar to [getFrameAtIndex(int,android.media.MediaMetadataRetriever.BitmapParams)](../android/media/MediaMetadataRetriever.md))except that the default for [BitmapParams](../android/media/MediaMetadataRetriever.BitmapParams.md) will be used. |
| open [Bitmap](../android/graphics/Bitmap.md)? | [getFrameAtIndex](../android/media/MediaMetadataRetriever.md))`(`frameIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `params:` ` [MediaMetadataRetriever.BitmapParams](../android/media/MediaMetadataRetriever.BitmapParams.md)`)` This method retrieves a video frame by its index. |
| open [Bitmap](../android/graphics/Bitmap.md)? | [getFrameAtTime](../android/media/MediaMetadataRetriever.md))`()` Call this method after setDataSource(). |
| --- | --- |
| open [Bitmap](../android/graphics/Bitmap.md)? | [getFrameAtTime](../android/media/MediaMetadataRetriever.md))`(`timeUs:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Call this method after setDataSource(). |
| open [Bitmap](../android/graphics/Bitmap.md)? | [getFrameAtTime](../android/media/MediaMetadataRetriever.md))`(`timeUs:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `option:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` This method is similar to [getFrameAtTime(long,int,android.media.MediaMetadataRetriever.BitmapParams)](../android/media/MediaMetadataRetriever.md))except that the device will choose the actual [Bitmap.Config](../android/graphics/Bitmap.Config.md) to use. |
| open [Bitmap](../android/graphics/Bitmap.md)? | [getFrameAtTime](../android/media/MediaMetadataRetriever.md))`(`timeUs:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `option:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `params:` ` [MediaMetadataRetriever.BitmapParams](../android/media/MediaMetadataRetriever.BitmapParams.md)`)` Call this method after setDataSource(). |
| --- | --- |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Bitmap](../android/graphics/Bitmap.md)!\> | [getFramesAtIndex](../android/media/MediaMetadataRetriever.md))`(`frameIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `numFrames:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` This method is similar to [getFramesAtIndex(int,int,android.media.MediaMetadataRetriever.BitmapParams)](../android/media/MediaMetadataRetriever.md))except that the default for [BitmapParams](../android/media/MediaMetadataRetriever.BitmapParams.md) will be used. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Bitmap](../android/graphics/Bitmap.md)!\> | [getFramesAtIndex](../android/media/MediaMetadataRetriever.md))`(`frameIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `numFrames:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `params:` ` [MediaMetadataRetriever.BitmapParams](../android/media/MediaMetadataRetriever.BitmapParams.md)`)` This method retrieves a consecutive set of video frames starting at the specified index. |
| open [Bitmap](../android/graphics/Bitmap.md)? | [getImageAtIndex](../android/media/MediaMetadataRetriever.md))`(`imageIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` This method is similar to [getImageAtIndex(int,android.media.MediaMetadataRetriever.BitmapParams)](../android/media/MediaMetadataRetriever.md))except that the default for [BitmapParams](../android/media/MediaMetadataRetriever.BitmapParams.md) will be used. |
| --- | --- |
| open [Bitmap](../android/graphics/Bitmap.md)? | [getImageAtIndex](../android/media/MediaMetadataRetriever.md))`(`imageIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `params:` ` [MediaMetadataRetriever.BitmapParams](../android/media/MediaMetadataRetriever.BitmapParams.md)`)` This method retrieves a still image by its index. |
| open [Bitmap](../android/graphics/Bitmap.md)? | [getPrimaryImage](../android/media/MediaMetadataRetriever.md))`()` This method is similar to [getPrimaryImage(android.media.MediaMetadataRetriever.BitmapParams)](../android/media/MediaMetadataRetriever.md))except that the default for [BitmapParams](../android/media/MediaMetadataRetriever.BitmapParams.md) will be used. |
| open [Bitmap](../android/graphics/Bitmap.md)? | [getPrimaryImage](../android/media/MediaMetadataRetriever.md))`(`params:` ` [MediaMetadataRetriever.BitmapParams](../android/media/MediaMetadataRetriever.BitmapParams.md)`)` This method retrieves the primary image of the media content. |
| --- | --- |
| open [Bitmap](../android/graphics/Bitmap.md)? | [getScaledFrameAtTime](../android/media/MediaMetadataRetriever.md))`(`timeUs:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `option:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dstWidth:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dstHeight:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` This method is similar to [getScaledFrameAtTime(long,int,int,int,android.media.MediaMetadataRetriever.BitmapParams)](../android/media/MediaMetadataRetriever.md))except that the device will choose the actual [Bitmap.Config](../android/graphics/Bitmap.Config.md) to use. |
| open [Bitmap](../android/graphics/Bitmap.md)? | [getScaledFrameAtTime](../android/media/MediaMetadataRetriever.md))`(`timeUs:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `option:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dstWidth:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dstHeight:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `params:` ` [MediaMetadataRetriever.BitmapParams](../android/media/MediaMetadataRetriever.BitmapParams.md)`)` Retrieve a video frame near a given timestamp scaled to a desired size. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [release](../android/media/MediaMetadataRetriever.md))`()` Releases any acquired resources. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDataSource](../android/media/MediaMetadataRetriever.md))`(`context:` ` [Context](../android/content/Context.md)!`, `uri:` ` [Uri](../android/net/Uri.md)!`)` Sets the data source as a content Uri. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDataSource](../android/media/MediaMetadataRetriever.md))`(`dataSource:` ` [MediaDataSource](../android/media/MediaDataSource.md)!`)` Sets the data source (MediaDataSource) to use. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDataSource](../android/media/MediaMetadataRetriever.md))`(`fd:` ` [FileDescriptor](../java/io/FileDescriptor.md)!`)` Sets the data source (FileDescriptor) to use. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDataSource](../android/media/MediaMetadataRetriever.md))`(`fd:` ` [FileDescriptor](../java/io/FileDescriptor.md)!`, `offset:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `length:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the data source (FileDescriptor) to use. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDataSource](../android/media/MediaMetadataRetriever.md))`(`path:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the data source (file pathname) to use. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDataSource](../android/media/MediaMetadataRetriever.md))`(`uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `headers:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Sets the data source (URI) to use. |
| --- | --- |

| Protected methods ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](../android/media/MediaMetadataRetriever.md))`()` <br /> |

## Constants

### METADATA_KEY_ALBUM

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val METADATA_KEY_ALBUM: Int
```

The metadata key to retrieve the information about the album title of the data source. 

 Value: 1

### METADATA_KEY_ALBUMARTIST

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val METADATA_KEY_ALBUMARTIST: Int
```

The metadata key to retrieve the information about the performers or artist associated with the data source. 

 Value: 13

### METADATA_KEY_ARTIST

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val METADATA_KEY_ARTIST: Int
```

The metadata key to retrieve the information about the artist of the data source. 

 Value: 2

### METADATA_KEY_AUTHOR

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val METADATA_KEY_AUTHOR: Int
```

The metadata key to retrieve the information about the author of the data source. 

 Value: 3

### METADATA_KEY_BITRATE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val METADATA_KEY_BITRATE: Int
```

This key retrieves the average bitrate (in bits/sec), if available. 

 Value: 20

### METADATA_KEY_BITS_PER_SAMPLE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val METADATA_KEY_BITS_PER_SAMPLE: Int
```

This key retrieves the bits per sample in numbers of bits, if available. This is a signed 32-bit integer formatted as a string in base 10. 

 Value: 39

### METADATA_KEY_CAPTURE_FRAMERATE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val METADATA_KEY_CAPTURE_FRAMERATE: Int
```

This key retrieves the original capture framerate, if it's available. The capture framerate will be a floating point number. 

 Value: 25

### METADATA_KEY_CD_TRACK_NUMBER

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val METADATA_KEY_CD_TRACK_NUMBER: Int
```

The metadata key to retrieve the numeric string describing the order of the audio data source on its original recording. 

 Value: 0

### METADATA_KEY_COLOR_RANGE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val METADATA_KEY_COLOR_RANGE: Int
```

This key retrieves the color range, if available. 

 Value: 37

**See Also**

- [android.media.MediaFormat#COLOR_RANGE_LIMITED](../android/media/MediaFormat.md)
- [android.media.MediaFormat#COLOR_RANGE_FULL](../android/media/MediaFormat.md) 

### METADATA_KEY_COLOR_STANDARD

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val METADATA_KEY_COLOR_STANDARD: Int
```

This key retrieves the color standard, if available. 

 Value: 35

**See Also**

- [android.media.MediaFormat#COLOR_STANDARD_BT709](../android/media/MediaFormat.md)
- [android.media.MediaFormat#COLOR_STANDARD_BT601_PAL](../android/media/MediaFormat.md)
- [android.media.MediaFormat#COLOR_STANDARD_BT601_NTSC](../android/media/MediaFormat.md)
- [android.media.MediaFormat#COLOR_STANDARD_BT2020](../android/media/MediaFormat.md) 

### METADATA_KEY_COLOR_TRANSFER

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val METADATA_KEY_COLOR_TRANSFER: Int
```

This key retrieves the color transfer, if available. 

 Value: 36

**See Also**

- [android.media.MediaFormat#COLOR_TRANSFER_LINEAR](../android/media/MediaFormat.md)
- [android.media.MediaFormat#COLOR_TRANSFER_SDR_VIDEO](../android/media/MediaFormat.md)
- [android.media.MediaFormat#COLOR_TRANSFER_ST2084](../android/media/MediaFormat.md)
- [android.media.MediaFormat#COLOR_TRANSFER_HLG](../android/media/MediaFormat.md) 

### METADATA_KEY_COMPILATION

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val METADATA_KEY_COMPILATION: Int
```

The metadata key to retrieve the music album compilation status. 

 Value: 15

### METADATA_KEY_COMPOSER

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val METADATA_KEY_COMPOSER: Int
```

The metadata key to retrieve the information about the composer of the data source. 

 Value: 4

### METADATA_KEY_DATE

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val METADATA_KEY_DATE: Int
```

The metadata key to retrieve the date when the data source was created or modified. 

 Value: 5

### METADATA_KEY_DISC_NUMBER

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val METADATA_KEY_DISC_NUMBER: Int
```

The metadata key to retrieve the numberic string that describes which part of a set the audio data source comes from. 

 Value: 14

### METADATA_KEY_DURATION

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val METADATA_KEY_DURATION: Int
```

The metadata key to retrieve the playback duration (in ms) of the data source. 

 Value: 9

### METADATA_KEY_EXIF_LENGTH

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val METADATA_KEY_EXIF_LENGTH: Int
```

If the media contains EXIF data, this key retrieves the length (in bytes) of the data. 

 Value: 34

### METADATA_KEY_EXIF_OFFSET

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val METADATA_KEY_EXIF_OFFSET: Int
```

If the media contains EXIF data, this key retrieves the offset (in bytes) of the data. 

 Value: 33

### METADATA_KEY_GENRE

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val METADATA_KEY_GENRE: Int
```

The metadata key to retrieve the content type or genre of the data source. 

 Value: 6

### METADATA_KEY_HAS_AUDIO

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val METADATA_KEY_HAS_AUDIO: Int
```

If this key exists the media contains audio content. 

 Value: 16

### METADATA_KEY_HAS_IMAGE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val METADATA_KEY_HAS_IMAGE: Int
```

If this key exists the media contains still image content. 

 Value: 26

### METADATA_KEY_HAS_VIDEO

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val METADATA_KEY_HAS_VIDEO: Int
```

If this key exists the media contains video content. 

 Value: 17

### METADATA_KEY_IMAGE_COUNT

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val METADATA_KEY_IMAGE_COUNT: Int
```

If the media contains still images, this key retrieves the number of still images. 

 Value: 27

### METADATA_KEY_IMAGE_HEIGHT

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val METADATA_KEY_IMAGE_HEIGHT: Int
```

If the media contains still images, this key retrieves the height of the primary image. 

 Value: 30

### METADATA_KEY_IMAGE_PRIMARY

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val METADATA_KEY_IMAGE_PRIMARY: Int
```

If the media contains still images, this key retrieves the image index of the primary image. 

 Value: 28

### METADATA_KEY_IMAGE_ROTATION

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val METADATA_KEY_IMAGE_ROTATION: Int
```

If the media contains still images, this key retrieves the rotation angle (in degrees clockwise) of the primary image. The image rotation angle must be one of 0, 90, 180, or 270 degrees. 

 Value: 31

### METADATA_KEY_IMAGE_WIDTH

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val METADATA_KEY_IMAGE_WIDTH: Int
```

If the media contains still images, this key retrieves the width of the primary image. 

 Value: 29

### METADATA_KEY_LOCATION

Added in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val METADATA_KEY_LOCATION: Int
```

This key retrieves the location information, if available. The location should be specified according to ISO-6709 standard, under a mp4/3gp box "@xyz". Location with longitude of -90 degrees and latitude of 180 degrees will be retrieved as "+180.0000-90.0000/", for instance. 

 Value: 23

### METADATA_KEY_MIMETYPE

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val METADATA_KEY_MIMETYPE: Int
```

The metadata key to retrieve the mime type of the data source. Some example mime types include: "video/mp4", "audio/mp4", "audio/amr-wb", etc. 

 Value: 12

### METADATA_KEY_NUM_TRACKS

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val METADATA_KEY_NUM_TRACKS: Int
```

The metadata key to retrieve the number of tracks, such as audio, video, text, in the data source, such as a mp4 or 3gpp file. 

 Value: 10

### METADATA_KEY_SAMPLERATE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val METADATA_KEY_SAMPLERATE: Int
```

This key retrieves the sample rate in Hz, if available. This is a signed 32-bit integer formatted as a string in base 10. 

 Value: 38

### METADATA_KEY_TITLE

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val METADATA_KEY_TITLE: Int
```

The metadata key to retrieve the data source title. 

 Value: 7

### METADATA_KEY_VIDEO_FRAME_COUNT

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val METADATA_KEY_VIDEO_FRAME_COUNT: Int
```

If the media contains video and this key exists, it retrieves the total number of frames in the video sequence. 

 Value: 32

### METADATA_KEY_VIDEO_HEIGHT

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val METADATA_KEY_VIDEO_HEIGHT: Int
```

If the media contains video, this key retrieves its height. 

 Value: 19

### METADATA_KEY_VIDEO_ROTATION

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val METADATA_KEY_VIDEO_ROTATION: Int
```

This key retrieves the video rotation angle in degrees, if available. The video rotation angle may be 0, 90, 180, or 270 degrees. 

 Value: 24

### METADATA_KEY_VIDEO_WIDTH

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val METADATA_KEY_VIDEO_WIDTH: Int
```

If the media contains video, this key retrieves its width. 

 Value: 18

### METADATA_KEY_WRITER

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val METADATA_KEY_WRITER: Int
```

The metadata key to retrieve the information of the writer (such as lyricist) of the data source. 

 Value: 11

### METADATA_KEY_XMP_LENGTH

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val METADATA_KEY_XMP_LENGTH: Int
```

If the media contains XMP data, this key retrieves the length (in bytes) of the data. 

 Value: 42

### METADATA_KEY_XMP_OFFSET

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val METADATA_KEY_XMP_OFFSET: Int
```

If the media contains XMP data, this key retrieves the offset (in bytes) of the data. 

 Value: 41

### METADATA_KEY_YEAR

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val METADATA_KEY_YEAR: Int
```

The metadata key to retrieve the year when the data source was created or modified. 

 Value: 8

### OPTION_CLOSEST

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OPTION_CLOSEST: Int
```

This option is used with [getFrameAtTime(long,int)](../android/media/MediaMetadataRetriever.md))to retrieve a frame (not necessarily a key frame) associated with a data source that is located closest to or at the given time. 

 Value: 3

**See Also**

- [#getFrameAtTime(long, int)](../android/media/MediaMetadataRetriever.md)) 

### OPTION_CLOSEST_SYNC

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OPTION_CLOSEST_SYNC: Int
```

This option is used with [getFrameAtTime(long,int)](../android/media/MediaMetadataRetriever.md))to retrieve a sync (or key) frame associated with a data source that is located closest to (in time) or at the given time. 

 Value: 2

**See Also**

- [#getFrameAtTime(long, int)](../android/media/MediaMetadataRetriever.md)) 

### OPTION_NEXT_SYNC

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OPTION_NEXT_SYNC: Int
```

This option is used with [getFrameAtTime(long,int)](../android/media/MediaMetadataRetriever.md))to retrieve a sync (or key) frame associated with a data source that is located right after or at the given time. 

 Value: 1

**See Also**

- [#getFrameAtTime(long, int)](../android/media/MediaMetadataRetriever.md)) 

### OPTION_PREVIOUS_SYNC

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OPTION_PREVIOUS_SYNC: Int
```

This option is used with [getFrameAtTime(long,int)](../android/media/MediaMetadataRetriever.md))to retrieve a sync (or key) frame associated with a data source that is located right before or at the given time. 

 Value: 0

**See Also**

- [#getFrameAtTime(long, int)](../android/media/MediaMetadataRetriever.md))

## Public constructors

### MediaMetadataRetriever

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
MediaMetadataRetriever()
```

## Public methods

### close

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

Releases any acquired resources. Call it when done with the object.

| Exceptions ||
|-----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | When an [IOException](../java/io/IOException.md) is thrown while closing a [MediaDataSource](../android/media/MediaDataSource.md) passed to [setDataSource(android.media.MediaDataSource)](../android/media/MediaMetadataRetriever.md)). This throws clause exists since API [android.os.Build.VERSION_CODES#TIRAMISU](../android/os/Build.VERSION_CODES.md), but this method can throw in earlier API versions where the exception is not declared. |

### extractMetadata

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun extractMetadata(keyCode: Int): String?
```

Call this method after setDataSource(). This method retrieves the meta data value associated with the keyCode. The keyCode currently supported is listed below as METADATA_XXX constants. With any other value, it returns a null pointer.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------|
| `keyCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):One of the constants listed below at the end of the class. |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | The meta data value associate with the given keyCode on success; null on failure. |

### getEmbeddedPicture

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEmbeddedPicture(): ByteArray?
```

Call this method after setDataSource(). This method finds the optional graphic or album/cover art associated associated with the data source. If there are more than one pictures, (any) one of them is returned.

| Return ||
|------------------------------------------------------------------------------------------|-----------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | null if no such graphic is found. |

### getFrameAtIndex

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFrameAtIndex(frameIndex: Int): Bitmap?
```

This method is similar to [getFrameAtIndex(int,android.media.MediaMetadataRetriever.BitmapParams)](../android/media/MediaMetadataRetriever.md))except that the default for [BitmapParams](../android/media/MediaMetadataRetriever.BitmapParams.md) will be used.

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `frameIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):0-based index of the video frame. The frame index must be that of a valid frame. The total number of frames available for retrieval can be queried via the [METADATA_KEY_VIDEO_FRAME_COUNT](../android/media/MediaMetadataRetriever.md) key. |

| Return ||
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Bitmap](../android/graphics/Bitmap.md)? | A Bitmap containing the requested video frame, or null if the retrieval fails. |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------|
| `java.lang.IllegalStateException` | if the container doesn't contain video or image sequences. |
| `java.lang.IllegalArgumentException` | if the requested frame index does not exist. |

**See Also**

- [#getFrameAtIndex(int, BitmapParams)](../android/media/MediaMetadataRetriever.md))
- [#getFramesAtIndex(int, int, BitmapParams)](../android/media/MediaMetadataRetriever.md))
- [#getFramesAtIndex(int, int)](../android/media/MediaMetadataRetriever.md)) 

### getFrameAtIndex

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFrameAtIndex(
    frameIndex: Int, 
    params: MediaMetadataRetriever.BitmapParams
): Bitmap?
```

This method retrieves a video frame by its index. It should only be called after #setDataSource. After the bitmap is returned, you can query the actual parameters that were used to create the bitmap from the`BitmapParams`argument, for instance to query the bitmap config used for the bitmap with [BitmapParams.getActualConfig](../android/media/MediaMetadataRetriever.BitmapParams.md)).

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `frameIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):0-based index of the video frame. The frame index must be that of a valid frame. The total number of frames available for retrieval can be queried via the [METADATA_KEY_VIDEO_FRAME_COUNT](../android/media/MediaMetadataRetriever.md) key. |
| `params` | [MediaMetadataRetriever.BitmapParams](../android/media/MediaMetadataRetriever.BitmapParams.md):BitmapParams that controls the returned bitmap config (such as pixel formats). This value cannot be`null`. |

| Return ||
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Bitmap](../android/graphics/Bitmap.md)? | A Bitmap containing the requested video frame, or null if the retrieval fails. |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------|
| `java.lang.IllegalStateException` | if the container doesn't contain video or image sequences. |
| `java.lang.IllegalArgumentException` | if the requested frame index does not exist. |

**See Also**

- [#getFrameAtIndex(int)](../android/media/MediaMetadataRetriever.md))
- [#getFramesAtIndex(int, int, BitmapParams)](../android/media/MediaMetadataRetriever.md))
- [#getFramesAtIndex(int, int)](../android/media/MediaMetadataRetriever.md)) 

### getFrameAtTime

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFrameAtTime(): Bitmap?
```

Call this method after setDataSource(). This method finds a representative frame at any time position if possible, and returns it as a bitmap. Call this method if one does not care about where the frame is located; otherwise, please call [getFrameAtTime(long)](../android/media/MediaMetadataRetriever.md))or [getFrameAtTime(long,int)](../android/media/MediaMetadataRetriever.md))

If you don't need a full-resolution frame (for example, because you need a thumbnail image), use #getScaledFrameAtTime instead of this method.

| Return ||
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [Bitmap](../android/graphics/Bitmap.md)? | A Bitmap containing a representative video frame, which can be null, if such a frame cannot be retrieved. |

**See Also**

- [#getFrameAtTime(long)](../android/media/MediaMetadataRetriever.md))
- [#getFrameAtTime(long, int)](../android/media/MediaMetadataRetriever.md)) 

### getFrameAtTime

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFrameAtTime(timeUs: Long): Bitmap?
```

Call this method after setDataSource(). This method finds a representative frame close to the given time position if possible, and returns it as a bitmap. Call this method if one does not care how the frame is found as long as it is close to the given time; otherwise, please call [getFrameAtTime(long,int)](../android/media/MediaMetadataRetriever.md)).

If you don't need a full-resolution frame (for example, because you need a thumbnail image), use #getScaledFrameAtTime instead of this method.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `timeUs` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The time position where the frame will be retrieved. When retrieving the frame at the given time position, there is no guarentee that the data source has a frame located at the position. When this happens, a frame nearby will be returned. If timeUs is negative, time position and option will ignored, and any frame that the implementation considers as representative may be returned. |

| Return ||
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [Bitmap](../android/graphics/Bitmap.md)? | A Bitmap of size dst_widthxdst_height containing a representative video frame, which can be null, if such a frame cannot be retrieved. |

**See Also**

- [#getFrameAtTime(long, int)](../android/media/MediaMetadataRetriever.md)) 

### getFrameAtTime

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFrameAtTime(
    timeUs: Long, 
    option: Int
): Bitmap?
```

This method is similar to [getFrameAtTime(long,int,android.media.MediaMetadataRetriever.BitmapParams)](../android/media/MediaMetadataRetriever.md))except that the device will choose the actual [Bitmap.Config](../android/graphics/Bitmap.Config.md) to use.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `timeUs` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The time position where the frame will be retrieved. When retrieving the frame at the given time position, there is no guarantee that the data source has a frame located at the position. When this happens, a frame nearby will be returned. If timeUs is negative, time position and option will ignored, and any frame that the implementation considers as representative may be returned. |
| `option` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a hint on how the frame is found. Use [OPTION_PREVIOUS_SYNC](../android/media/MediaMetadataRetriever.md) if one wants to retrieve a sync frame that has a timestamp earlier than or the same as timeUs. Use [OPTION_NEXT_SYNC](../android/media/MediaMetadataRetriever.md) if one wants to retrieve a sync frame that has a timestamp later than or the same as timeUs. Use [OPTION_CLOSEST_SYNC](../android/media/MediaMetadataRetriever.md) if one wants to retrieve a sync frame that has a timestamp closest to or the same as timeUs. Use [OPTION_CLOSEST](../android/media/MediaMetadataRetriever.md) if one wants to retrieve a frame that may or may not be a sync frame but is closest to or the same as timeUs. [OPTION_CLOSEST](../android/media/MediaMetadataRetriever.md) often has larger performance overhead compared to the other options if there is no sync frame located at timeUs. Value is [android.media.MediaMetadataRetriever#OPTION_PREVIOUS_SYNC](../android/media/MediaMetadataRetriever.md), [android.media.MediaMetadataRetriever#OPTION_NEXT_SYNC](../android/media/MediaMetadataRetriever.md), [android.media.MediaMetadataRetriever#OPTION_CLOSEST_SYNC](../android/media/MediaMetadataRetriever.md), or [android.media.MediaMetadataRetriever#OPTION_CLOSEST](../android/media/MediaMetadataRetriever.md) |

| Return ||
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Bitmap](../android/graphics/Bitmap.md)? | A Bitmap containing a representative video frame, which can be null, if such a frame cannot be retrieved. [Bitmap.getConfig()](../android/graphics/Bitmap.md))can be used to query the actual [Bitmap.Config](../android/graphics/Bitmap.Config.md). |

**See Also**

- [#getFrameAtTime(long, int, BitmapParams)](../android/media/MediaMetadataRetriever.md)) 

### getFrameAtTime

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFrameAtTime(
    timeUs: Long, 
    option: Int, 
    params: MediaMetadataRetriever.BitmapParams
): Bitmap?
```

Call this method after setDataSource(). This method finds a representative frame close to the given time position by considering the given option if possible, and returns it as a bitmap.

If you don't need a full-resolution frame (for example, because you need a thumbnail image), use #getScaledFrameAtTime instead of this method.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `timeUs` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The time position where the frame will be retrieved. When retrieving the frame at the given time position, there is no guarantee that the data source has a frame located at the position. When this happens, a frame nearby will be returned. If timeUs is negative, time position and option will ignored, and any frame that the implementation considers as representative may be returned. |
| `option` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a hint on how the frame is found. Use [OPTION_PREVIOUS_SYNC](../android/media/MediaMetadataRetriever.md) if one wants to retrieve a sync frame that has a timestamp earlier than or the same as timeUs. Use [OPTION_NEXT_SYNC](../android/media/MediaMetadataRetriever.md) if one wants to retrieve a sync frame that has a timestamp later than or the same as timeUs. Use [OPTION_CLOSEST_SYNC](../android/media/MediaMetadataRetriever.md) if one wants to retrieve a sync frame that has a timestamp closest to or the same as timeUs. Use [OPTION_CLOSEST](../android/media/MediaMetadataRetriever.md) if one wants to retrieve a frame that may or may not be a sync frame but is closest to or the same as timeUs. [OPTION_CLOSEST](../android/media/MediaMetadataRetriever.md) often has larger performance overhead compared to the other options if there is no sync frame located at timeUs. Value is [android.media.MediaMetadataRetriever#OPTION_PREVIOUS_SYNC](../android/media/MediaMetadataRetriever.md), [android.media.MediaMetadataRetriever#OPTION_NEXT_SYNC](../android/media/MediaMetadataRetriever.md), [android.media.MediaMetadataRetriever#OPTION_CLOSEST_SYNC](../android/media/MediaMetadataRetriever.md), or [android.media.MediaMetadataRetriever#OPTION_CLOSEST](../android/media/MediaMetadataRetriever.md) |
| `params` | [MediaMetadataRetriever.BitmapParams](../android/media/MediaMetadataRetriever.BitmapParams.md):BitmapParams that controls the returned bitmap config (such as pixel formats). This value cannot be`null`. |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [Bitmap](../android/graphics/Bitmap.md)? | A Bitmap containing a representative video frame, which can be null, if such a frame cannot be retrieved. |

**See Also**

- [#getFrameAtTime(long, int)](../android/media/MediaMetadataRetriever.md)) 

### getFramesAtIndex

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFramesAtIndex(
    frameIndex: Int, 
    numFrames: Int
): MutableList<Bitmap!>
```

This method is similar to [getFramesAtIndex(int,int,android.media.MediaMetadataRetriever.BitmapParams)](../android/media/MediaMetadataRetriever.md))except that the default for [BitmapParams](../android/media/MediaMetadataRetriever.BitmapParams.md) will be used.

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `frameIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):0-based index of the first video frame to retrieve. The frame index must be that of a valid frame. The total number of frames available for retrieval can be queried via the [METADATA_KEY_VIDEO_FRAME_COUNT](../android/media/MediaMetadataRetriever.md) key. |
| `numFrames` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):number of consecutive video frames to retrieve. Must be a positive value. The stream must contain at least numFrames frames starting at frameIndex. |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Bitmap](../android/graphics/Bitmap.md)!> | An list of Bitmaps containing the requested video frames. The returned array could contain less frames than requested if the retrieval fails. This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if the container doesn't contain video or image sequences. |
| `java.lang.IllegalArgumentException` | if the frameIndex or numFrames is invalid, or the stream doesn't contain at least numFrames starting at frameIndex. |

**See Also**

- [#getFrameAtIndex(int, BitmapParams)](../android/media/MediaMetadataRetriever.md))
- [#getFrameAtIndex(int)](../android/media/MediaMetadataRetriever.md))
- [#getFramesAtIndex(int, int, BitmapParams)](../android/media/MediaMetadataRetriever.md)) 

### getFramesAtIndex

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFramesAtIndex(
    frameIndex: Int, 
    numFrames: Int, 
    params: MediaMetadataRetriever.BitmapParams
): MutableList<Bitmap!>
```

This method retrieves a consecutive set of video frames starting at the specified index. It should only be called after #setDataSource. If the caller intends to retrieve more than one consecutive video frames, this method is preferred over [getFrameAtIndex(int,android.media.MediaMetadataRetriever.BitmapParams)](../android/media/MediaMetadataRetriever.md))for efficiency. After the bitmaps are returned, you can query the actual parameters that were used to create the bitmaps from the`BitmapParams`argument, for instance to query the bitmap config used for the bitmaps with [BitmapParams.getActualConfig](../android/media/MediaMetadataRetriever.BitmapParams.md)).

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `frameIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):0-based index of the first video frame to retrieve. The frame index must be that of a valid frame. The total number of frames available for retrieval can be queried via the [METADATA_KEY_VIDEO_FRAME_COUNT](../android/media/MediaMetadataRetriever.md) key. |
| `numFrames` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):number of consecutive video frames to retrieve. Must be a positive value. The stream must contain at least numFrames frames starting at frameIndex. |
| `params` | [MediaMetadataRetriever.BitmapParams](../android/media/MediaMetadataRetriever.BitmapParams.md):BitmapParams that controls the returned bitmap config (such as pixel formats). This value cannot be`null`. |
| --- | --- |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Bitmap](../android/graphics/Bitmap.md)!> | An list of Bitmaps containing the requested video frames. The returned array could contain less frames than requested if the retrieval fails. This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if the container doesn't contain video or image sequences. |
| `java.lang.IllegalArgumentException` | if the frameIndex or numFrames is invalid, or the stream doesn't contain at least numFrames starting at frameIndex. |

**See Also**

- [#getFrameAtIndex(int, BitmapParams)](../android/media/MediaMetadataRetriever.md))
- [#getFrameAtIndex(int)](../android/media/MediaMetadataRetriever.md))
- [#getFramesAtIndex(int, int)](../android/media/MediaMetadataRetriever.md)) 

### getImageAtIndex

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getImageAtIndex(imageIndex: Int): Bitmap?
```

This method is similar to [getImageAtIndex(int,android.media.MediaMetadataRetriever.BitmapParams)](../android/media/MediaMetadataRetriever.md))except that the default for [BitmapParams](../android/media/MediaMetadataRetriever.BitmapParams.md) will be used.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------|
| `imageIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):0-based index of the image. |

| Return ||
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Bitmap](../android/graphics/Bitmap.md)? | the requested still image, or null if the image cannot be retrieved. |

| Exceptions ||
|--------------------------------------|------------------------------------------------|
| `java.lang.IllegalStateException` | if the container doesn't contain still images. |
| `java.lang.IllegalArgumentException` | if the requested image does not exist. |

**See Also**

- [#getImageAtIndex(int, BitmapParams)](../android/media/MediaMetadataRetriever.md))
- [#getPrimaryImage(BitmapParams)](../android/media/MediaMetadataRetriever.md))
- <https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getPrimaryImage()> 

### getImageAtIndex

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getImageAtIndex(
    imageIndex: Int, 
    params: MediaMetadataRetriever.BitmapParams
): Bitmap?
```

This method retrieves a still image by its index. It should only be called after #setDataSource. After the bitmap is returned, you can query the actual parameters that were used to create the bitmap from the`BitmapParams`argument, for instance to query the bitmap config used for the bitmap with [BitmapParams.getActualConfig](../android/media/MediaMetadataRetriever.BitmapParams.md)).

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `imageIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):0-based index of the image. |
| `params` | [MediaMetadataRetriever.BitmapParams](../android/media/MediaMetadataRetriever.BitmapParams.md):BitmapParams that controls the returned bitmap config (such as pixel formats). This value cannot be`null`. |

| Return ||
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Bitmap](../android/graphics/Bitmap.md)? | the requested still image, or null if the image cannot be retrieved. |

| Exceptions ||
|--------------------------------------|------------------------------------------------|
| `java.lang.IllegalStateException` | if the container doesn't contain still images. |
| `java.lang.IllegalArgumentException` | if the requested image does not exist. |

**See Also**

- [#getImageAtIndex(int)](../android/media/MediaMetadataRetriever.md))
- [#getPrimaryImage(BitmapParams)](../android/media/MediaMetadataRetriever.md))
- <https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getPrimaryImage()> 

### getPrimaryImage

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPrimaryImage(): Bitmap?
```

This method is similar to [getPrimaryImage(android.media.MediaMetadataRetriever.BitmapParams)](../android/media/MediaMetadataRetriever.md))except that the default for [BitmapParams](../android/media/MediaMetadataRetriever.BitmapParams.md) will be used.

| Return ||
|-----------------------------------------------------------------------------------------|-------------------------------------------------------|
| [Bitmap](../android/graphics/Bitmap.md)? | the primary image, or null if it cannot be retrieved. |

| Exceptions ||
|-----------------------------------|------------------------------------------------|
| `java.lang.IllegalStateException` | if the container doesn't contain still images. |

**See Also**

- [#getImageAtIndex(int, BitmapParams)](../android/media/MediaMetadataRetriever.md))
- [#getImageAtIndex(int)](../android/media/MediaMetadataRetriever.md))
- [#getPrimaryImage(BitmapParams)](../android/media/MediaMetadataRetriever.md)) 

### getPrimaryImage

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPrimaryImage(params: MediaMetadataRetriever.BitmapParams): Bitmap?
```

This method retrieves the primary image of the media content. It should only be called after #setDataSource. After the bitmap is returned, you can query the actual parameters that were used to create the bitmap from the`BitmapParams`argument, for instance to query the bitmap config used for the bitmap with [BitmapParams.getActualConfig](../android/media/MediaMetadataRetriever.BitmapParams.md)).

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `params` | [MediaMetadataRetriever.BitmapParams](../android/media/MediaMetadataRetriever.BitmapParams.md):BitmapParams that controls the returned bitmap config (such as pixel formats). This value cannot be`null`. |

| Return ||
|-----------------------------------------------------------------------------------------|-------------------------------------------------------|
| [Bitmap](../android/graphics/Bitmap.md)? | the primary image, or null if it cannot be retrieved. |

| Exceptions ||
|-----------------------------------|------------------------------------------------|
| `java.lang.IllegalStateException` | if the container doesn't contain still images. |

**See Also**

- [#getImageAtIndex(int, BitmapParams)](../android/media/MediaMetadataRetriever.md))
- [#getImageAtIndex(int)](../android/media/MediaMetadataRetriever.md))
- <https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getPrimaryImage()> 

### getScaledFrameAtTime

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getScaledFrameAtTime(
    timeUs: Long, 
    option: Int, 
    dstWidth: Int, 
    dstHeight: Int
): Bitmap?
```

This method is similar to [getScaledFrameAtTime(long,int,int,int,android.media.MediaMetadataRetriever.BitmapParams)](../android/media/MediaMetadataRetriever.md))except that the device will choose the actual [Bitmap.Config](../android/graphics/Bitmap.Config.md) to use.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `timeUs` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The time position in microseconds where the frame will be retrieved. When retrieving the frame at the given time position, there is no guarantee that the data source has a frame located at the position. When this happens, a frame nearby will be returned. If timeUs is negative, time position and option will ignored, and any frame that the implementation considers as representative may be returned. |
| `option` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a hint on how the frame is found. Use [OPTION_PREVIOUS_SYNC](../android/media/MediaMetadataRetriever.md) if one wants to retrieve a sync frame that has a timestamp earlier than or the same as timeUs. Use [OPTION_NEXT_SYNC](../android/media/MediaMetadataRetriever.md) if one wants to retrieve a sync frame that has a timestamp later than or the same as timeUs. Use [OPTION_CLOSEST_SYNC](../android/media/MediaMetadataRetriever.md) if one wants to retrieve a sync frame that has a timestamp closest to or the same as timeUs. Use [OPTION_CLOSEST](../android/media/MediaMetadataRetriever.md) if one wants to retrieve a frame that may or may not be a sync frame but is closest to or the same as timeUs. [OPTION_CLOSEST](../android/media/MediaMetadataRetriever.md) often has larger performance overhead compared to the other options if there is no sync frame located at timeUs. Value is [android.media.MediaMetadataRetriever#OPTION_PREVIOUS_SYNC](../android/media/MediaMetadataRetriever.md), [android.media.MediaMetadataRetriever#OPTION_NEXT_SYNC](../android/media/MediaMetadataRetriever.md), [android.media.MediaMetadataRetriever#OPTION_CLOSEST_SYNC](../android/media/MediaMetadataRetriever.md), or [android.media.MediaMetadataRetriever#OPTION_CLOSEST](../android/media/MediaMetadataRetriever.md) |
| `dstWidth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):expected output bitmap width Value is 1 or greater |
| --- | --- |
| `dstHeight` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):expected output bitmap height Value is 1 or greater |

| Return ||
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Bitmap](../android/graphics/Bitmap.md)? | A Bitmap containing a representative video frame, which can be null, if such a frame cannot be retrieved. [Bitmap.getConfig()](../android/graphics/Bitmap.md))can be used to query the actual [Bitmap.Config](../android/graphics/Bitmap.Config.md). |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if passed in invalid option or width by height is less than or equal to 0. |

**See Also**

- [#getScaledFrameAtTime(long, int, int, int, BitmapParams)](../android/media/MediaMetadataRetriever.md)) 

### getScaledFrameAtTime

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getScaledFrameAtTime(
    timeUs: Long, 
    option: Int, 
    dstWidth: Int, 
    dstHeight: Int, 
    params: MediaMetadataRetriever.BitmapParams
): Bitmap?
```

Retrieve a video frame near a given timestamp scaled to a desired size. Call this method after setDataSource(). This method finds a representative frame close to the given time position by considering the given option if possible, and returns it as a bitmap with same aspect ratio as the source while scaling it so that it fits into the desired size of dst_width by dst_height. This is useful for generating a thumbnail for an input data source or just to obtain a scaled frame at the given time position.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `timeUs` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The time position in microseconds where the frame will be retrieved. When retrieving the frame at the given time position, there is no guarantee that the data source has a frame located at the position. When this happens, a frame nearby will be returned. If timeUs is negative, time position and option will ignored, and any frame that the implementation considers as representative may be returned. |
| `option` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a hint on how the frame is found. Use [OPTION_PREVIOUS_SYNC](../android/media/MediaMetadataRetriever.md) if one wants to retrieve a sync frame that has a timestamp earlier than or the same as timeUs. Use [OPTION_NEXT_SYNC](../android/media/MediaMetadataRetriever.md) if one wants to retrieve a sync frame that has a timestamp later than or the same as timeUs. Use [OPTION_CLOSEST_SYNC](../android/media/MediaMetadataRetriever.md) if one wants to retrieve a sync frame that has a timestamp closest to or the same as timeUs. Use [OPTION_CLOSEST](../android/media/MediaMetadataRetriever.md) if one wants to retrieve a frame that may or may not be a sync frame but is closest to or the same as timeUs. [OPTION_CLOSEST](../android/media/MediaMetadataRetriever.md) often has larger performance overhead compared to the other options if there is no sync frame located at timeUs. Value is [android.media.MediaMetadataRetriever#OPTION_PREVIOUS_SYNC](../android/media/MediaMetadataRetriever.md), [android.media.MediaMetadataRetriever#OPTION_NEXT_SYNC](../android/media/MediaMetadataRetriever.md), [android.media.MediaMetadataRetriever#OPTION_CLOSEST_SYNC](../android/media/MediaMetadataRetriever.md), or [android.media.MediaMetadataRetriever#OPTION_CLOSEST](../android/media/MediaMetadataRetriever.md) |
| `dstWidth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):expected output bitmap width Value is 1 or greater |
| --- | --- |
| `dstHeight` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):expected output bitmap height Value is 1 or greater |
| `params` | [MediaMetadataRetriever.BitmapParams](../android/media/MediaMetadataRetriever.BitmapParams.md):BitmapParams that controls the returned bitmap config (such as pixel formats). This value cannot be`null`. |

| Return ||
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [Bitmap](../android/graphics/Bitmap.md)? | A Bitmap of size not larger than dstWidth by dstHeight containing a scaled video frame, which can be null, if such a frame cannot be retrieved. |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if passed in invalid option or width by height is less than or equal to 0. |

**See Also**

- [#getScaledFrameAtTime(long, int, int, int)](../android/media/MediaMetadataRetriever.md)) 

### release

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun release(): Unit
```

Releases any acquired resources. Call it when done with the object.

| Exceptions ||
|-----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | When an [IOException](../java/io/IOException.md) is thrown while closing a [MediaDataSource](../android/media/MediaDataSource.md) passed to [setDataSource(android.media.MediaDataSource)](../android/media/MediaMetadataRetriever.md)). This throws clause exists since API [android.os.Build.VERSION_CODES#TIRAMISU](../android/os/Build.VERSION_CODES.md), but this method can throw in earlier API versions where the exception is not declared. |

### setDataSource

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDataSource(
    context: Context!, 
    uri: Uri!
): Unit
```

Sets the data source as a content Uri. Call this method before the rest of the methods in this class. This method may be time-consuming.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md)!:the Context to use when resolving the Uri |
| `uri` | [Uri](../android/net/Uri.md)!:the Content URI of the data you want to play |

| Exceptions ||
|--------------------------------------|------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the Uri is invalid |
| `java.lang.SecurityException` | if the Uri cannot be used due to lack of permission. |

### setDataSource

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDataSource(dataSource: MediaDataSource!): Unit
```

Sets the data source (MediaDataSource) to use.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `dataSource` | [MediaDataSource](../android/media/MediaDataSource.md)!:the MediaDataSource for the media you want to play |

### setDataSource

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDataSource(fd: FileDescriptor!): Unit
```

Sets the data source (FileDescriptor) to use. It is the caller's responsibility to close the file descriptor. It is safe to do so as soon as this call returns. Call this method before the rest of the methods in this class. This method may be time-consuming.

| Parameters ||
|------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `fd` | [FileDescriptor](../java/io/FileDescriptor.md)!:the FileDescriptor for the file you want to play |

| Exceptions ||
|--------------------------------------|----------------------------------|
| `java.lang.IllegalArgumentException` | if the FileDescriptor is invalid |

### setDataSource

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDataSource(
    fd: FileDescriptor!, 
    offset: Long, 
    length: Long
): Unit
```

Sets the data source (FileDescriptor) to use. It is the caller's responsibility to close the file descriptor. It is safe to do so as soon as this call returns. Call this method before the rest of the methods in this class. This method may be time-consuming.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fd` | [FileDescriptor](../java/io/FileDescriptor.md)!:the FileDescriptor for the file you want to play |
| `offset` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the offset into the file where the data to be played starts, in bytes. It must be non-negative |
| `length` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the length in bytes of the data to be played. It must be non-negative. |
| --- | --- |

| Exceptions ||
|--------------------------------------|------------------------------|
| `java.lang.IllegalArgumentException` | if the arguments are invalid |

### setDataSource

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDataSource(path: String!): Unit
```

Sets the data source (file pathname) to use. Call this method before the rest of the methods in this class. This method may be time-consuming.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `path` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The path, or the URI (doesn't support streaming source currently) of the input media file. |

| Exceptions ||
|--------------------------------------|-------------------------|
| `java.lang.IllegalArgumentException` | If the path is invalid. |

### setDataSource

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDataSource(
    uri: String!, 
    headers: MutableMap<String!, String!>!
): Unit
```

Sets the data source (URI) to use. Call this method before the rest of the methods in this class. This method may be time-consuming.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The URI of the input media. |
| `headers` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:the headers to be sent together with the request for the data |

| Exceptions ||
|--------------------------------------|------------------------|
| `java.lang.IllegalArgumentException` | If the URI is invalid. |

## Protected methods

### finalize

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun finalize(): Unit
```

| Exceptions ||
|-----------------------|-------------------------------------|
| `java.lang.Throwable` | the`Exception`raised by this method |
