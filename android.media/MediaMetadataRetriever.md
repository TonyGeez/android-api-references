# MediaMetadataRetriever

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MediaMetadataRetriever

Kotlin| [Java](https://developer.android.com/reference/android/media/MediaMetadataRetriever "View this page in Java") 
| --- | --- |

```
open class MediaMetadataRetriever : AutoCloseable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.MediaMetadataRetriever](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#) |

MediaMetadataRetriever class provides a unified interface for retrieving frame and meta data from an input media file.

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------------------------|
| | [BitmapParams](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever.BitmapParams) <br /> |

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_ALBUM](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#METADATA_KEY_ALBUM:kotlin.Int) The metadata key to retrieve the information about the album title of the data source. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_ALBUMARTIST](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#METADATA_KEY_ALBUMARTIST:kotlin.Int) The metadata key to retrieve the information about the performers or artist associated with the data source. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_ARTIST](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#METADATA_KEY_ARTIST:kotlin.Int) The metadata key to retrieve the information about the artist of the data source. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_AUTHOR](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#METADATA_KEY_AUTHOR:kotlin.Int) The metadata key to retrieve the information about the author of the data source. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_BITRATE](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#METADATA_KEY_BITRATE:kotlin.Int) This key retrieves the average bitrate (in bits/sec), if available. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_BITS_PER_SAMPLE](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#METADATA_KEY_BITS_PER_SAMPLE:kotlin.Int) This key retrieves the bits per sample in numbers of bits, if available. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_CAPTURE_FRAMERATE](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#METADATA_KEY_CAPTURE_FRAMERATE:kotlin.Int) This key retrieves the original capture framerate, if it's available. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_CD_TRACK_NUMBER](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#METADATA_KEY_CD_TRACK_NUMBER:kotlin.Int) The metadata key to retrieve the numeric string describing the order of the audio data source on its original recording. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_COLOR_RANGE](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#METADATA_KEY_COLOR_RANGE:kotlin.Int) This key retrieves the color range, if available. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_COLOR_STANDARD](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#METADATA_KEY_COLOR_STANDARD:kotlin.Int) This key retrieves the color standard, if available. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_COLOR_TRANSFER](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#METADATA_KEY_COLOR_TRANSFER:kotlin.Int) This key retrieves the color transfer, if available. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_COMPILATION](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#METADATA_KEY_COMPILATION:kotlin.Int) The metadata key to retrieve the music album compilation status. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_COMPOSER](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#METADATA_KEY_COMPOSER:kotlin.Int) The metadata key to retrieve the information about the composer of the data source. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_DATE](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#METADATA_KEY_DATE:kotlin.Int) The metadata key to retrieve the date when the data source was created or modified. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_DISC_NUMBER](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#METADATA_KEY_DISC_NUMBER:kotlin.Int) The metadata key to retrieve the numberic string that describes which part of a set the audio data source comes from. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_DURATION](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#METADATA_KEY_DURATION:kotlin.Int) The metadata key to retrieve the playback duration (in ms) of the data source. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_EXIF_LENGTH](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#METADATA_KEY_EXIF_LENGTH:kotlin.Int) If the media contains EXIF data, this key retrieves the length (in bytes) of the data. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_EXIF_OFFSET](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#METADATA_KEY_EXIF_OFFSET:kotlin.Int) If the media contains EXIF data, this key retrieves the offset (in bytes) of the data. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_GENRE](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#METADATA_KEY_GENRE:kotlin.Int) The metadata key to retrieve the content type or genre of the data source. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_HAS_AUDIO](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#METADATA_KEY_HAS_AUDIO:kotlin.Int) If this key exists the media contains audio content. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_HAS_IMAGE](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#METADATA_KEY_HAS_IMAGE:kotlin.Int) If this key exists the media contains still image content. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_HAS_VIDEO](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#METADATA_KEY_HAS_VIDEO:kotlin.Int) If this key exists the media contains video content. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_IMAGE_COUNT](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#METADATA_KEY_IMAGE_COUNT:kotlin.Int) If the media contains still images, this key retrieves the number of still images. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_IMAGE_HEIGHT](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#METADATA_KEY_IMAGE_HEIGHT:kotlin.Int) If the media contains still images, this key retrieves the height of the primary image. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_IMAGE_PRIMARY](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#METADATA_KEY_IMAGE_PRIMARY:kotlin.Int) If the media contains still images, this key retrieves the image index of the primary image. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_IMAGE_ROTATION](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#METADATA_KEY_IMAGE_ROTATION:kotlin.Int) If the media contains still images, this key retrieves the rotation angle (in degrees clockwise) of the primary image. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_IMAGE_WIDTH](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#METADATA_KEY_IMAGE_WIDTH:kotlin.Int) If the media contains still images, this key retrieves the width of the primary image. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_LOCATION](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#METADATA_KEY_LOCATION:kotlin.Int) This key retrieves the location information, if available. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_MIMETYPE](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#METADATA_KEY_MIMETYPE:kotlin.Int) The metadata key to retrieve the mime type of the data source. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_NUM_TRACKS](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#METADATA_KEY_NUM_TRACKS:kotlin.Int) The metadata key to retrieve the number of tracks, such as audio, video, text, in the data source, such as a mp4 or 3gpp file. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_SAMPLERATE](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#METADATA_KEY_SAMPLERATE:kotlin.Int) This key retrieves the sample rate in Hz, if available. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_TITLE](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#METADATA_KEY_TITLE:kotlin.Int) The metadata key to retrieve the data source title. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_VIDEO_FRAME_COUNT](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#METADATA_KEY_VIDEO_FRAME_COUNT:kotlin.Int) If the media contains video and this key exists, it retrieves the total number of frames in the video sequence. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_VIDEO_HEIGHT](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#METADATA_KEY_VIDEO_HEIGHT:kotlin.Int) If the media contains video, this key retrieves its height. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_VIDEO_ROTATION](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#METADATA_KEY_VIDEO_ROTATION:kotlin.Int) This key retrieves the video rotation angle in degrees, if available. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_VIDEO_WIDTH](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#METADATA_KEY_VIDEO_WIDTH:kotlin.Int) If the media contains video, this key retrieves its width. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_WRITER](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#METADATA_KEY_WRITER:kotlin.Int) The metadata key to retrieve the information of the writer (such as lyricist) of the data source. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_XMP_LENGTH](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#METADATA_KEY_XMP_LENGTH:kotlin.Int) If the media contains XMP data, this key retrieves the length (in bytes) of the data. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_XMP_OFFSET](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#METADATA_KEY_XMP_OFFSET:kotlin.Int) If the media contains XMP data, this key retrieves the offset (in bytes) of the data. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [METADATA_KEY_YEAR](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#METADATA_KEY_YEAR:kotlin.Int) The metadata key to retrieve the year when the data source was created or modified. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [OPTION_CLOSEST](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#OPTION_CLOSEST:kotlin.Int) This option is used with [getFrameAtTime(long,int)](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getFrameAtTime(kotlin.Long,%20kotlin.Int))to retrieve a frame (not necessarily a key frame) associated with a data source that is located closest to or at the given time. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [OPTION_CLOSEST_SYNC](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#OPTION_CLOSEST_SYNC:kotlin.Int) This option is used with [getFrameAtTime(long,int)](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getFrameAtTime(kotlin.Long,%20kotlin.Int))to retrieve a sync (or key) frame associated with a data source that is located closest to (in time) or at the given time. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [OPTION_NEXT_SYNC](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#OPTION_NEXT_SYNC:kotlin.Int) This option is used with [getFrameAtTime(long,int)](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getFrameAtTime(kotlin.Long,%20kotlin.Int))to retrieve a sync (or key) frame associated with a data source that is located right after or at the given time. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [OPTION_PREVIOUS_SYNC](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#OPTION_PREVIOUS_SYNC:kotlin.Int) This option is used with [getFrameAtTime(long,int)](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getFrameAtTime(kotlin.Long,%20kotlin.Int))to retrieve a sync (or key) frame associated with a data source that is located right before or at the given time. |

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [MediaMetadataRetriever](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#MediaMetadataRetriever())`()` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#close())`()` Releases any acquired resources. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [extractMetadata](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#extractMetadata(kotlin.Int))`(`keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Call this method after setDataSource(). |
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | [getEmbeddedPicture](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getEmbeddedPicture())`()` Call this method after setDataSource(). |
| --- | --- |
| open [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)? | [getFrameAtIndex](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getFrameAtIndex(kotlin.Int))`(`frameIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` This method is similar to [getFrameAtIndex(int,android.media.MediaMetadataRetriever.BitmapParams)](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getFrameAtIndex(kotlin.Int,%20android.media.MediaMetadataRetriever.BitmapParams))except that the default for [BitmapParams](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever.BitmapParams) will be used. |
| open [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)? | [getFrameAtIndex](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getFrameAtIndex(kotlin.Int,%20android.media.MediaMetadataRetriever.BitmapParams))`(`frameIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `params:` ` [MediaMetadataRetriever.BitmapParams](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever.BitmapParams)`)` This method retrieves a video frame by its index. |
| open [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)? | [getFrameAtTime](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getFrameAtTime())`()` Call this method after setDataSource(). |
| --- | --- |
| open [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)? | [getFrameAtTime](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getFrameAtTime(kotlin.Long))`(`timeUs:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Call this method after setDataSource(). |
| open [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)? | [getFrameAtTime](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getFrameAtTime(kotlin.Long,%20kotlin.Int))`(`timeUs:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `option:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` This method is similar to [getFrameAtTime(long,int,android.media.MediaMetadataRetriever.BitmapParams)](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getFrameAtTime(kotlin.Long,%20kotlin.Int,%20android.media.MediaMetadataRetriever.BitmapParams))except that the device will choose the actual [Bitmap.Config](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config.html#) to use. |
| open [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)? | [getFrameAtTime](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getFrameAtTime(kotlin.Long,%20kotlin.Int,%20android.media.MediaMetadataRetriever.BitmapParams))`(`timeUs:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `option:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `params:` ` [MediaMetadataRetriever.BitmapParams](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever.BitmapParams)`)` Call this method after setDataSource(). |
| --- | --- |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)!\> | [getFramesAtIndex](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getFramesAtIndex(kotlin.Int,%20kotlin.Int))`(`frameIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `numFrames:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` This method is similar to [getFramesAtIndex(int,int,android.media.MediaMetadataRetriever.BitmapParams)](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getFramesAtIndex(kotlin.Int,%20kotlin.Int,%20android.media.MediaMetadataRetriever.BitmapParams))except that the default for [BitmapParams](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever.BitmapParams) will be used. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)!\> | [getFramesAtIndex](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getFramesAtIndex(kotlin.Int,%20kotlin.Int,%20android.media.MediaMetadataRetriever.BitmapParams))`(`frameIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `numFrames:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `params:` ` [MediaMetadataRetriever.BitmapParams](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever.BitmapParams)`)` This method retrieves a consecutive set of video frames starting at the specified index. |
| open [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)? | [getImageAtIndex](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getImageAtIndex(kotlin.Int))`(`imageIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` This method is similar to [getImageAtIndex(int,android.media.MediaMetadataRetriever.BitmapParams)](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getImageAtIndex(kotlin.Int,%20android.media.MediaMetadataRetriever.BitmapParams))except that the default for [BitmapParams](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever.BitmapParams) will be used. |
| --- | --- |
| open [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)? | [getImageAtIndex](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getImageAtIndex(kotlin.Int,%20android.media.MediaMetadataRetriever.BitmapParams))`(`imageIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `params:` ` [MediaMetadataRetriever.BitmapParams](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever.BitmapParams)`)` This method retrieves a still image by its index. |
| open [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)? | [getPrimaryImage](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getPrimaryImage())`()` This method is similar to [getPrimaryImage(android.media.MediaMetadataRetriever.BitmapParams)](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getPrimaryImage(android.media.MediaMetadataRetriever.BitmapParams))except that the default for [BitmapParams](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever.BitmapParams) will be used. |
| open [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)? | [getPrimaryImage](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getPrimaryImage(android.media.MediaMetadataRetriever.BitmapParams))`(`params:` ` [MediaMetadataRetriever.BitmapParams](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever.BitmapParams)`)` This method retrieves the primary image of the media content. |
| --- | --- |
| open [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)? | [getScaledFrameAtTime](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getScaledFrameAtTime(kotlin.Long,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`timeUs:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `option:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dstWidth:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dstHeight:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` This method is similar to [getScaledFrameAtTime(long,int,int,int,android.media.MediaMetadataRetriever.BitmapParams)](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getScaledFrameAtTime(kotlin.Long,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20android.media.MediaMetadataRetriever.BitmapParams))except that the device will choose the actual [Bitmap.Config](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config.html#) to use. |
| open [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)? | [getScaledFrameAtTime](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getScaledFrameAtTime(kotlin.Long,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20android.media.MediaMetadataRetriever.BitmapParams))`(`timeUs:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `option:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dstWidth:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dstHeight:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `params:` ` [MediaMetadataRetriever.BitmapParams](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever.BitmapParams)`)` Retrieve a video frame near a given timestamp scaled to a desired size. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [release](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#release())`()` Releases any acquired resources. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDataSource](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#setDataSource(android.content.Context,%20android.net.Uri))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!`)` Sets the data source as a content Uri. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDataSource](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#setDataSource(android.media.MediaDataSource))`(`dataSource:` ` [MediaDataSource](https://developer.android.com/reference/kotlin/android/media/MediaDataSource)!`)` Sets the data source (MediaDataSource) to use. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDataSource](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#setDataSource(java.io.FileDescriptor))`(`fd:` ` [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#)!`)` Sets the data source (FileDescriptor) to use. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDataSource](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#setDataSource(java.io.FileDescriptor,%20kotlin.Long,%20kotlin.Long))`(`fd:` ` [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#)!`, `offset:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `length:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the data source (FileDescriptor) to use. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDataSource](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#setDataSource(kotlin.String))`(`path:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the data source (file pathname) to use. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDataSource](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#setDataSource(kotlin.String,%20kotlin.collections.MutableMap))`(`uri:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `headers:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Sets the data source (URI) to use. |
| --- | --- |

| Protected methods ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#finalize())`()` <br /> |

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

- [android.media.MediaFormat#COLOR_RANGE_LIMITED](https://developer.android.com/reference/kotlin/android/media/MediaFormat#COLOR_RANGE_LIMITED:kotlin.Int)
- [android.media.MediaFormat#COLOR_RANGE_FULL](https://developer.android.com/reference/kotlin/android/media/MediaFormat#COLOR_RANGE_FULL:kotlin.Int) 

### METADATA_KEY_COLOR_STANDARD

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val METADATA_KEY_COLOR_STANDARD: Int
```

This key retrieves the color standard, if available. 

 Value: 35

**See Also**

- [android.media.MediaFormat#COLOR_STANDARD_BT709](https://developer.android.com/reference/kotlin/android/media/MediaFormat#COLOR_STANDARD_BT709:kotlin.Int)
- [android.media.MediaFormat#COLOR_STANDARD_BT601_PAL](https://developer.android.com/reference/kotlin/android/media/MediaFormat#COLOR_STANDARD_BT601_PAL:kotlin.Int)
- [android.media.MediaFormat#COLOR_STANDARD_BT601_NTSC](https://developer.android.com/reference/kotlin/android/media/MediaFormat#COLOR_STANDARD_BT601_NTSC:kotlin.Int)
- [android.media.MediaFormat#COLOR_STANDARD_BT2020](https://developer.android.com/reference/kotlin/android/media/MediaFormat#COLOR_STANDARD_BT2020:kotlin.Int) 

### METADATA_KEY_COLOR_TRANSFER

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val METADATA_KEY_COLOR_TRANSFER: Int
```

This key retrieves the color transfer, if available. 

 Value: 36

**See Also**

- [android.media.MediaFormat#COLOR_TRANSFER_LINEAR](https://developer.android.com/reference/kotlin/android/media/MediaFormat#COLOR_TRANSFER_LINEAR:kotlin.Int)
- [android.media.MediaFormat#COLOR_TRANSFER_SDR_VIDEO](https://developer.android.com/reference/kotlin/android/media/MediaFormat#COLOR_TRANSFER_SDR_VIDEO:kotlin.Int)
- [android.media.MediaFormat#COLOR_TRANSFER_ST2084](https://developer.android.com/reference/kotlin/android/media/MediaFormat#COLOR_TRANSFER_ST2084:kotlin.Int)
- [android.media.MediaFormat#COLOR_TRANSFER_HLG](https://developer.android.com/reference/kotlin/android/media/MediaFormat#COLOR_TRANSFER_HLG:kotlin.Int) 

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

This option is used with [getFrameAtTime(long,int)](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getFrameAtTime(kotlin.Long,%20kotlin.Int))to retrieve a frame (not necessarily a key frame) associated with a data source that is located closest to or at the given time. 

 Value: 3

**See Also**

- [#getFrameAtTime(long, int)](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getFrameAtTime(kotlin.Long,%20kotlin.Int)) 

### OPTION_CLOSEST_SYNC

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OPTION_CLOSEST_SYNC: Int
```

This option is used with [getFrameAtTime(long,int)](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getFrameAtTime(kotlin.Long,%20kotlin.Int))to retrieve a sync (or key) frame associated with a data source that is located closest to (in time) or at the given time. 

 Value: 2

**See Also**

- [#getFrameAtTime(long, int)](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getFrameAtTime(kotlin.Long,%20kotlin.Int)) 

### OPTION_NEXT_SYNC

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OPTION_NEXT_SYNC: Int
```

This option is used with [getFrameAtTime(long,int)](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getFrameAtTime(kotlin.Long,%20kotlin.Int))to retrieve a sync (or key) frame associated with a data source that is located right after or at the given time. 

 Value: 1

**See Also**

- [#getFrameAtTime(long, int)](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getFrameAtTime(kotlin.Long,%20kotlin.Int)) 

### OPTION_PREVIOUS_SYNC

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OPTION_PREVIOUS_SYNC: Int
```

This option is used with [getFrameAtTime(long,int)](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getFrameAtTime(kotlin.Long,%20kotlin.Int))to retrieve a sync (or key) frame associated with a data source that is located right before or at the given time. 

 Value: 0

**See Also**

- [#getFrameAtTime(long, int)](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getFrameAtTime(kotlin.Long,%20kotlin.Int))

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
| `java.io.IOException` | When an [IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#) is thrown while closing a [MediaDataSource](https://developer.android.com/reference/kotlin/android/media/MediaDataSource) passed to [setDataSource(android.media.MediaDataSource)](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#setDataSource(android.media.MediaDataSource)). This throws clause exists since API [android.os.Build.VERSION_CODES#TIRAMISU](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int), but this method can throw in earlier API versions where the exception is not declared. |

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

This method is similar to [getFrameAtIndex(int,android.media.MediaMetadataRetriever.BitmapParams)](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getFrameAtIndex(kotlin.Int,%20android.media.MediaMetadataRetriever.BitmapParams))except that the default for [BitmapParams](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever.BitmapParams) will be used.

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `frameIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):0-based index of the video frame. The frame index must be that of a valid frame. The total number of frames available for retrieval can be queried via the [METADATA_KEY_VIDEO_FRAME_COUNT](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#METADATA_KEY_VIDEO_FRAME_COUNT:kotlin.Int) key. |

| Return ||
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)? | A Bitmap containing the requested video frame, or null if the retrieval fails. |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------|
| `java.lang.IllegalStateException` | if the container doesn't contain video or image sequences. |
| `java.lang.IllegalArgumentException` | if the requested frame index does not exist. |

**See Also**

- [#getFrameAtIndex(int, BitmapParams)](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getFrameAtIndex(kotlin.Int,%20android.media.MediaMetadataRetriever.BitmapParams))
- [#getFramesAtIndex(int, int, BitmapParams)](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getFramesAtIndex(kotlin.Int,%20kotlin.Int,%20android.media.MediaMetadataRetriever.BitmapParams))
- [#getFramesAtIndex(int, int)](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getFramesAtIndex(kotlin.Int,%20kotlin.Int)) 

### getFrameAtIndex

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFrameAtIndex(
    frameIndex: Int, 
    params: MediaMetadataRetriever.BitmapParams
): Bitmap?
```

This method retrieves a video frame by its index. It should only be called after #setDataSource. After the bitmap is returned, you can query the actual parameters that were used to create the bitmap from the`BitmapParams`argument, for instance to query the bitmap config used for the bitmap with [BitmapParams.getActualConfig](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever.BitmapParams#getActualConfig()).

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `frameIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):0-based index of the video frame. The frame index must be that of a valid frame. The total number of frames available for retrieval can be queried via the [METADATA_KEY_VIDEO_FRAME_COUNT](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#METADATA_KEY_VIDEO_FRAME_COUNT:kotlin.Int) key. |
| `params` | [MediaMetadataRetriever.BitmapParams](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever.BitmapParams):BitmapParams that controls the returned bitmap config (such as pixel formats). This value cannot be`null`. |

| Return ||
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)? | A Bitmap containing the requested video frame, or null if the retrieval fails. |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------|
| `java.lang.IllegalStateException` | if the container doesn't contain video or image sequences. |
| `java.lang.IllegalArgumentException` | if the requested frame index does not exist. |

**See Also**

- [#getFrameAtIndex(int)](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getFrameAtIndex(kotlin.Int))
- [#getFramesAtIndex(int, int, BitmapParams)](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getFramesAtIndex(kotlin.Int,%20kotlin.Int,%20android.media.MediaMetadataRetriever.BitmapParams))
- [#getFramesAtIndex(int, int)](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getFramesAtIndex(kotlin.Int,%20kotlin.Int)) 

### getFrameAtTime

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFrameAtTime(): Bitmap?
```

Call this method after setDataSource(). This method finds a representative frame at any time position if possible, and returns it as a bitmap. Call this method if one does not care about where the frame is located; otherwise, please call [getFrameAtTime(long)](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getFrameAtTime(kotlin.Long))or [getFrameAtTime(long,int)](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getFrameAtTime(kotlin.Long,%20kotlin.Int))

If you don't need a full-resolution frame (for example, because you need a thumbnail image), use #getScaledFrameAtTime instead of this method.

| Return ||
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)? | A Bitmap containing a representative video frame, which can be null, if such a frame cannot be retrieved. |

**See Also**

- [#getFrameAtTime(long)](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getFrameAtTime(kotlin.Long))
- [#getFrameAtTime(long, int)](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getFrameAtTime(kotlin.Long,%20kotlin.Int)) 

### getFrameAtTime

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFrameAtTime(timeUs: Long): Bitmap?
```

Call this method after setDataSource(). This method finds a representative frame close to the given time position if possible, and returns it as a bitmap. Call this method if one does not care how the frame is found as long as it is close to the given time; otherwise, please call [getFrameAtTime(long,int)](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getFrameAtTime(kotlin.Long,%20kotlin.Int)).

If you don't need a full-resolution frame (for example, because you need a thumbnail image), use #getScaledFrameAtTime instead of this method.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `timeUs` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The time position where the frame will be retrieved. When retrieving the frame at the given time position, there is no guarentee that the data source has a frame located at the position. When this happens, a frame nearby will be returned. If timeUs is negative, time position and option will ignored, and any frame that the implementation considers as representative may be returned. |

| Return ||
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)? | A Bitmap of size dst_widthxdst_height containing a representative video frame, which can be null, if such a frame cannot be retrieved. |

**See Also**

- [#getFrameAtTime(long, int)](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getFrameAtTime(kotlin.Long,%20kotlin.Int)) 

### getFrameAtTime

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFrameAtTime(
    timeUs: Long, 
    option: Int
): Bitmap?
```

This method is similar to [getFrameAtTime(long,int,android.media.MediaMetadataRetriever.BitmapParams)](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getFrameAtTime(kotlin.Long,%20kotlin.Int,%20android.media.MediaMetadataRetriever.BitmapParams))except that the device will choose the actual [Bitmap.Config](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config.html#) to use.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `timeUs` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The time position where the frame will be retrieved. When retrieving the frame at the given time position, there is no guarantee that the data source has a frame located at the position. When this happens, a frame nearby will be returned. If timeUs is negative, time position and option will ignored, and any frame that the implementation considers as representative may be returned. |
| `option` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a hint on how the frame is found. Use [OPTION_PREVIOUS_SYNC](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#OPTION_PREVIOUS_SYNC:kotlin.Int) if one wants to retrieve a sync frame that has a timestamp earlier than or the same as timeUs. Use [OPTION_NEXT_SYNC](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#OPTION_NEXT_SYNC:kotlin.Int) if one wants to retrieve a sync frame that has a timestamp later than or the same as timeUs. Use [OPTION_CLOSEST_SYNC](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#OPTION_CLOSEST_SYNC:kotlin.Int) if one wants to retrieve a sync frame that has a timestamp closest to or the same as timeUs. Use [OPTION_CLOSEST](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#OPTION_CLOSEST:kotlin.Int) if one wants to retrieve a frame that may or may not be a sync frame but is closest to or the same as timeUs. [OPTION_CLOSEST](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#OPTION_CLOSEST:kotlin.Int) often has larger performance overhead compared to the other options if there is no sync frame located at timeUs. Value is [android.media.MediaMetadataRetriever#OPTION_PREVIOUS_SYNC](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#OPTION_PREVIOUS_SYNC:kotlin.Int), [android.media.MediaMetadataRetriever#OPTION_NEXT_SYNC](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#OPTION_NEXT_SYNC:kotlin.Int), [android.media.MediaMetadataRetriever#OPTION_CLOSEST_SYNC](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#OPTION_CLOSEST_SYNC:kotlin.Int), or [android.media.MediaMetadataRetriever#OPTION_CLOSEST](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#OPTION_CLOSEST:kotlin.Int) |

| Return ||
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)? | A Bitmap containing a representative video frame, which can be null, if such a frame cannot be retrieved. [Bitmap.getConfig()](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#getConfig())can be used to query the actual [Bitmap.Config](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config.html#). |

**See Also**

- [#getFrameAtTime(long, int, BitmapParams)](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getFrameAtTime(kotlin.Long,%20kotlin.Int,%20android.media.MediaMetadataRetriever.BitmapParams)) 

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
| `option` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a hint on how the frame is found. Use [OPTION_PREVIOUS_SYNC](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#OPTION_PREVIOUS_SYNC:kotlin.Int) if one wants to retrieve a sync frame that has a timestamp earlier than or the same as timeUs. Use [OPTION_NEXT_SYNC](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#OPTION_NEXT_SYNC:kotlin.Int) if one wants to retrieve a sync frame that has a timestamp later than or the same as timeUs. Use [OPTION_CLOSEST_SYNC](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#OPTION_CLOSEST_SYNC:kotlin.Int) if one wants to retrieve a sync frame that has a timestamp closest to or the same as timeUs. Use [OPTION_CLOSEST](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#OPTION_CLOSEST:kotlin.Int) if one wants to retrieve a frame that may or may not be a sync frame but is closest to or the same as timeUs. [OPTION_CLOSEST](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#OPTION_CLOSEST:kotlin.Int) often has larger performance overhead compared to the other options if there is no sync frame located at timeUs. Value is [android.media.MediaMetadataRetriever#OPTION_PREVIOUS_SYNC](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#OPTION_PREVIOUS_SYNC:kotlin.Int), [android.media.MediaMetadataRetriever#OPTION_NEXT_SYNC](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#OPTION_NEXT_SYNC:kotlin.Int), [android.media.MediaMetadataRetriever#OPTION_CLOSEST_SYNC](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#OPTION_CLOSEST_SYNC:kotlin.Int), or [android.media.MediaMetadataRetriever#OPTION_CLOSEST](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#OPTION_CLOSEST:kotlin.Int) |
| `params` | [MediaMetadataRetriever.BitmapParams](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever.BitmapParams):BitmapParams that controls the returned bitmap config (such as pixel formats). This value cannot be`null`. |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)? | A Bitmap containing a representative video frame, which can be null, if such a frame cannot be retrieved. |

**See Also**

- [#getFrameAtTime(long, int)](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getFrameAtTime(kotlin.Long,%20kotlin.Int)) 

### getFramesAtIndex

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFramesAtIndex(
    frameIndex: Int, 
    numFrames: Int
): MutableList<Bitmap!>
```

This method is similar to [getFramesAtIndex(int,int,android.media.MediaMetadataRetriever.BitmapParams)](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getFramesAtIndex(kotlin.Int,%20kotlin.Int,%20android.media.MediaMetadataRetriever.BitmapParams))except that the default for [BitmapParams](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever.BitmapParams) will be used.

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `frameIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):0-based index of the first video frame to retrieve. The frame index must be that of a valid frame. The total number of frames available for retrieval can be queried via the [METADATA_KEY_VIDEO_FRAME_COUNT](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#METADATA_KEY_VIDEO_FRAME_COUNT:kotlin.Int) key. |
| `numFrames` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):number of consecutive video frames to retrieve. Must be a positive value. The stream must contain at least numFrames frames starting at frameIndex. |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)!> | An list of Bitmaps containing the requested video frames. The returned array could contain less frames than requested if the retrieval fails. This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if the container doesn't contain video or image sequences. |
| `java.lang.IllegalArgumentException` | if the frameIndex or numFrames is invalid, or the stream doesn't contain at least numFrames starting at frameIndex. |

**See Also**

- [#getFrameAtIndex(int, BitmapParams)](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getFrameAtIndex(kotlin.Int,%20android.media.MediaMetadataRetriever.BitmapParams))
- [#getFrameAtIndex(int)](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getFrameAtIndex(kotlin.Int))
- [#getFramesAtIndex(int, int, BitmapParams)](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getFramesAtIndex(kotlin.Int,%20kotlin.Int,%20android.media.MediaMetadataRetriever.BitmapParams)) 

### getFramesAtIndex

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFramesAtIndex(
    frameIndex: Int, 
    numFrames: Int, 
    params: MediaMetadataRetriever.BitmapParams
): MutableList<Bitmap!>
```

This method retrieves a consecutive set of video frames starting at the specified index. It should only be called after #setDataSource. If the caller intends to retrieve more than one consecutive video frames, this method is preferred over [getFrameAtIndex(int,android.media.MediaMetadataRetriever.BitmapParams)](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getFrameAtIndex(kotlin.Int,%20android.media.MediaMetadataRetriever.BitmapParams))for efficiency. After the bitmaps are returned, you can query the actual parameters that were used to create the bitmaps from the`BitmapParams`argument, for instance to query the bitmap config used for the bitmaps with [BitmapParams.getActualConfig](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever.BitmapParams#getActualConfig()).

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `frameIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):0-based index of the first video frame to retrieve. The frame index must be that of a valid frame. The total number of frames available for retrieval can be queried via the [METADATA_KEY_VIDEO_FRAME_COUNT](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#METADATA_KEY_VIDEO_FRAME_COUNT:kotlin.Int) key. |
| `numFrames` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):number of consecutive video frames to retrieve. Must be a positive value. The stream must contain at least numFrames frames starting at frameIndex. |
| `params` | [MediaMetadataRetriever.BitmapParams](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever.BitmapParams):BitmapParams that controls the returned bitmap config (such as pixel formats). This value cannot be`null`. |
| --- | --- |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)!> | An list of Bitmaps containing the requested video frames. The returned array could contain less frames than requested if the retrieval fails. This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if the container doesn't contain video or image sequences. |
| `java.lang.IllegalArgumentException` | if the frameIndex or numFrames is invalid, or the stream doesn't contain at least numFrames starting at frameIndex. |

**See Also**

- [#getFrameAtIndex(int, BitmapParams)](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getFrameAtIndex(kotlin.Int,%20android.media.MediaMetadataRetriever.BitmapParams))
- [#getFrameAtIndex(int)](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getFrameAtIndex(kotlin.Int))
- [#getFramesAtIndex(int, int)](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getFramesAtIndex(kotlin.Int,%20kotlin.Int)) 

### getImageAtIndex

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getImageAtIndex(imageIndex: Int): Bitmap?
```

This method is similar to [getImageAtIndex(int,android.media.MediaMetadataRetriever.BitmapParams)](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getImageAtIndex(kotlin.Int,%20android.media.MediaMetadataRetriever.BitmapParams))except that the default for [BitmapParams](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever.BitmapParams) will be used.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------|
| `imageIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):0-based index of the image. |

| Return ||
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)? | the requested still image, or null if the image cannot be retrieved. |

| Exceptions ||
|--------------------------------------|------------------------------------------------|
| `java.lang.IllegalStateException` | if the container doesn't contain still images. |
| `java.lang.IllegalArgumentException` | if the requested image does not exist. |

**See Also**

- [#getImageAtIndex(int, BitmapParams)](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getImageAtIndex(kotlin.Int,%20android.media.MediaMetadataRetriever.BitmapParams))
- [#getPrimaryImage(BitmapParams)](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getPrimaryImage(android.media.MediaMetadataRetriever.BitmapParams))
- <https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getPrimaryImage()> 

### getImageAtIndex

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getImageAtIndex(
    imageIndex: Int, 
    params: MediaMetadataRetriever.BitmapParams
): Bitmap?
```

This method retrieves a still image by its index. It should only be called after #setDataSource. After the bitmap is returned, you can query the actual parameters that were used to create the bitmap from the`BitmapParams`argument, for instance to query the bitmap config used for the bitmap with [BitmapParams.getActualConfig](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever.BitmapParams#getActualConfig()).

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `imageIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):0-based index of the image. |
| `params` | [MediaMetadataRetriever.BitmapParams](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever.BitmapParams):BitmapParams that controls the returned bitmap config (such as pixel formats). This value cannot be`null`. |

| Return ||
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)? | the requested still image, or null if the image cannot be retrieved. |

| Exceptions ||
|--------------------------------------|------------------------------------------------|
| `java.lang.IllegalStateException` | if the container doesn't contain still images. |
| `java.lang.IllegalArgumentException` | if the requested image does not exist. |

**See Also**

- [#getImageAtIndex(int)](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getImageAtIndex(kotlin.Int))
- [#getPrimaryImage(BitmapParams)](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getPrimaryImage(android.media.MediaMetadataRetriever.BitmapParams))
- <https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getPrimaryImage()> 

### getPrimaryImage

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPrimaryImage(): Bitmap?
```

This method is similar to [getPrimaryImage(android.media.MediaMetadataRetriever.BitmapParams)](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getPrimaryImage(android.media.MediaMetadataRetriever.BitmapParams))except that the default for [BitmapParams](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever.BitmapParams) will be used.

| Return ||
|-----------------------------------------------------------------------------------------|-------------------------------------------------------|
| [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)? | the primary image, or null if it cannot be retrieved. |

| Exceptions ||
|-----------------------------------|------------------------------------------------|
| `java.lang.IllegalStateException` | if the container doesn't contain still images. |

**See Also**

- [#getImageAtIndex(int, BitmapParams)](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getImageAtIndex(kotlin.Int,%20android.media.MediaMetadataRetriever.BitmapParams))
- [#getImageAtIndex(int)](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getImageAtIndex(kotlin.Int))
- [#getPrimaryImage(BitmapParams)](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getPrimaryImage(android.media.MediaMetadataRetriever.BitmapParams)) 

### getPrimaryImage

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPrimaryImage(params: MediaMetadataRetriever.BitmapParams): Bitmap?
```

This method retrieves the primary image of the media content. It should only be called after #setDataSource. After the bitmap is returned, you can query the actual parameters that were used to create the bitmap from the`BitmapParams`argument, for instance to query the bitmap config used for the bitmap with [BitmapParams.getActualConfig](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever.BitmapParams#getActualConfig()).

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `params` | [MediaMetadataRetriever.BitmapParams](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever.BitmapParams):BitmapParams that controls the returned bitmap config (such as pixel formats). This value cannot be`null`. |

| Return ||
|-----------------------------------------------------------------------------------------|-------------------------------------------------------|
| [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)? | the primary image, or null if it cannot be retrieved. |

| Exceptions ||
|-----------------------------------|------------------------------------------------|
| `java.lang.IllegalStateException` | if the container doesn't contain still images. |

**See Also**

- [#getImageAtIndex(int, BitmapParams)](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getImageAtIndex(kotlin.Int,%20android.media.MediaMetadataRetriever.BitmapParams))
- [#getImageAtIndex(int)](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getImageAtIndex(kotlin.Int))
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

This method is similar to [getScaledFrameAtTime(long,int,int,int,android.media.MediaMetadataRetriever.BitmapParams)](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getScaledFrameAtTime(kotlin.Long,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20android.media.MediaMetadataRetriever.BitmapParams))except that the device will choose the actual [Bitmap.Config](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config.html#) to use.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `timeUs` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The time position in microseconds where the frame will be retrieved. When retrieving the frame at the given time position, there is no guarantee that the data source has a frame located at the position. When this happens, a frame nearby will be returned. If timeUs is negative, time position and option will ignored, and any frame that the implementation considers as representative may be returned. |
| `option` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a hint on how the frame is found. Use [OPTION_PREVIOUS_SYNC](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#OPTION_PREVIOUS_SYNC:kotlin.Int) if one wants to retrieve a sync frame that has a timestamp earlier than or the same as timeUs. Use [OPTION_NEXT_SYNC](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#OPTION_NEXT_SYNC:kotlin.Int) if one wants to retrieve a sync frame that has a timestamp later than or the same as timeUs. Use [OPTION_CLOSEST_SYNC](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#OPTION_CLOSEST_SYNC:kotlin.Int) if one wants to retrieve a sync frame that has a timestamp closest to or the same as timeUs. Use [OPTION_CLOSEST](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#OPTION_CLOSEST:kotlin.Int) if one wants to retrieve a frame that may or may not be a sync frame but is closest to or the same as timeUs. [OPTION_CLOSEST](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#OPTION_CLOSEST:kotlin.Int) often has larger performance overhead compared to the other options if there is no sync frame located at timeUs. Value is [android.media.MediaMetadataRetriever#OPTION_PREVIOUS_SYNC](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#OPTION_PREVIOUS_SYNC:kotlin.Int), [android.media.MediaMetadataRetriever#OPTION_NEXT_SYNC](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#OPTION_NEXT_SYNC:kotlin.Int), [android.media.MediaMetadataRetriever#OPTION_CLOSEST_SYNC](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#OPTION_CLOSEST_SYNC:kotlin.Int), or [android.media.MediaMetadataRetriever#OPTION_CLOSEST](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#OPTION_CLOSEST:kotlin.Int) |
| `dstWidth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):expected output bitmap width Value is 1 or greater |
| --- | --- |
| `dstHeight` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):expected output bitmap height Value is 1 or greater |

| Return ||
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)? | A Bitmap containing a representative video frame, which can be null, if such a frame cannot be retrieved. [Bitmap.getConfig()](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#getConfig())can be used to query the actual [Bitmap.Config](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.Config.html#). |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if passed in invalid option or width by height is less than or equal to 0. |

**See Also**

- [#getScaledFrameAtTime(long, int, int, int, BitmapParams)](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getScaledFrameAtTime(kotlin.Long,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20android.media.MediaMetadataRetriever.BitmapParams)) 

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
| `option` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a hint on how the frame is found. Use [OPTION_PREVIOUS_SYNC](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#OPTION_PREVIOUS_SYNC:kotlin.Int) if one wants to retrieve a sync frame that has a timestamp earlier than or the same as timeUs. Use [OPTION_NEXT_SYNC](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#OPTION_NEXT_SYNC:kotlin.Int) if one wants to retrieve a sync frame that has a timestamp later than or the same as timeUs. Use [OPTION_CLOSEST_SYNC](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#OPTION_CLOSEST_SYNC:kotlin.Int) if one wants to retrieve a sync frame that has a timestamp closest to or the same as timeUs. Use [OPTION_CLOSEST](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#OPTION_CLOSEST:kotlin.Int) if one wants to retrieve a frame that may or may not be a sync frame but is closest to or the same as timeUs. [OPTION_CLOSEST](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#OPTION_CLOSEST:kotlin.Int) often has larger performance overhead compared to the other options if there is no sync frame located at timeUs. Value is [android.media.MediaMetadataRetriever#OPTION_PREVIOUS_SYNC](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#OPTION_PREVIOUS_SYNC:kotlin.Int), [android.media.MediaMetadataRetriever#OPTION_NEXT_SYNC](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#OPTION_NEXT_SYNC:kotlin.Int), [android.media.MediaMetadataRetriever#OPTION_CLOSEST_SYNC](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#OPTION_CLOSEST_SYNC:kotlin.Int), or [android.media.MediaMetadataRetriever#OPTION_CLOSEST](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#OPTION_CLOSEST:kotlin.Int) |
| `dstWidth` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):expected output bitmap width Value is 1 or greater |
| --- | --- |
| `dstHeight` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):expected output bitmap height Value is 1 or greater |
| `params` | [MediaMetadataRetriever.BitmapParams](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever.BitmapParams):BitmapParams that controls the returned bitmap config (such as pixel formats). This value cannot be`null`. |

| Return ||
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)? | A Bitmap of size not larger than dstWidth by dstHeight containing a scaled video frame, which can be null, if such a frame cannot be retrieved. |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if passed in invalid option or width by height is less than or equal to 0. |

**See Also**

- [#getScaledFrameAtTime(long, int, int, int)](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#getScaledFrameAtTime(kotlin.Long,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)) 

### release

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun release(): Unit
```

Releases any acquired resources. Call it when done with the object.

| Exceptions ||
|-----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | When an [IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#) is thrown while closing a [MediaDataSource](https://developer.android.com/reference/kotlin/android/media/MediaDataSource) passed to [setDataSource(android.media.MediaDataSource)](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#setDataSource(android.media.MediaDataSource)). This throws clause exists since API [android.os.Build.VERSION_CODES#TIRAMISU](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int), but this method can throw in earlier API versions where the exception is not declared. |

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
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:the Context to use when resolving the Uri |
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!:the Content URI of the data you want to play |

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
| `dataSource` | [MediaDataSource](https://developer.android.com/reference/kotlin/android/media/MediaDataSource)!:the MediaDataSource for the media you want to play |

### setDataSource

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDataSource(fd: FileDescriptor!): Unit
```

Sets the data source (FileDescriptor) to use. It is the caller's responsibility to close the file descriptor. It is safe to do so as soon as this call returns. Call this method before the rest of the methods in this class. This method may be time-consuming.

| Parameters ||
|------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `fd` | [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#)!:the FileDescriptor for the file you want to play |

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
| `fd` | [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#)!:the FileDescriptor for the file you want to play |
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
