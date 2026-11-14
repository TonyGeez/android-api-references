Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MediaMuxer

Kotlin | [Java](https://developer.android.com/reference/android/media/MediaMuxer "View this page in Java")

```
class MediaMuxer
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.media.MediaMuxer](https://developer.android.com/reference/kotlin/android/media/MediaMuxer#) |

MediaMuxer facilitates muxing elementary streams. Currently MediaMuxer supports MP4, Webm and 3GP file as the output. It also supports muxing B-frames in MP4 since Android Nougat MR1.

It is generally used like this:

```kotlin
MediaMuxer muxer = new MediaMuxer("temp.mp4", OutputFormat.MUXER_OUTPUT_MPEG_4);
  // More often, the MediaFormat will be retrieved from MediaCodec.getOutputFormat()
  // or MediaExtractor.getTrackFormat().
  MediaFormat audioFormat = new MediaFormat(...);
  MediaFormat videoFormat = new MediaFormat(...);
  int audioTrackIndex = muxer.addTrack(audioFormat);
  int videoTrackIndex = muxer.addTrack(videoFormat);
  ByteBuffer inputBuffer = ByteBuffer.allocate(bufferSize);
  boolean finished = false;
  BufferInfo bufferInfo = new BufferInfo();
 
  muxer.start();
  while(!finished) {
    // getInputBuffer() will fill the inputBuffer with one frame of encoded
    // sample from either MediaCodec or MediaExtractor, set isAudioSample to
    // true when the sample is audio data, set up all the fields of bufferInfo,
    // and return true if there are no more samples.
    finished = getInputBuffer(inputBuffer, isAudioSample, bufferInfo);
    if (!finished) {
      int currentTrackIndex = isAudioSample ? audioTrackIndex : videoTrackIndex;
      muxer.writeSampleData(currentTrackIndex, inputBuffer, bufferInfo);
    }
  };
  muxer.stop();
  muxer.release();
  
```

#### Metadata Track

Per-frame metadata carries information that correlates with video or audio to facilitate offline processing. For example, gyro signals from the sensor can help video stabilization when doing offline processing. Metadata tracks are only supported when multiplexing to the MP4 container format. When adding a new metadata track, the MIME type format must start with prefix "application/" (for example, "application/gyro"). The format of the metadata is application-defined. Metadata timestamps must be in the same time base as video and audio timestamps. The generated MP4 file uses TextMetaDataSampleEntry (defined in section 12.3.3.2 of the ISOBMFF specification) to signal the metadata's MIME type.

```kotlin
MediaMuxer muxer = new MediaMuxer("temp.mp4", OutputFormat.MUXER_OUTPUT_MPEG_4);
    // SetUp Video/Audio Tracks.
    MediaFormat audioFormat = new MediaFormat(...);
    MediaFormat videoFormat = new MediaFormat(...);
    int audioTrackIndex = muxer.addTrack(audioFormat);
    int videoTrackIndex = muxer.addTrack(videoFormat);
 
    // Setup Metadata Track
    MediaFormat metadataFormat = new MediaFormat(...);
    metadataFormat.setString(KEY_MIME, "application/gyro");
    int metadataTrackIndex = muxer.addTrack(metadataFormat);
 
    muxer.start();
    while(..) {
        // Allocate bytebuffer and write gyro data(x,y,z) into it.
        ByteBuffer metaData = ByteBuffer.allocate(bufferSize);
        metaData.putFloat(x);
        metaData.putFloat(y);
        metaData.putFloat(z);
        BufferInfo metaInfo = new BufferInfo();
        // Associate this metadata with the video frame by setting
        // the same timestamp as the video frame.
        metaInfo.presentationTimeUs = currentVideoTrackTimeUs;
        metaInfo.offset = 0;
        metaInfo.flags = 0;
        metaInfo.size = bufferSize;
        muxer.writeSampleData(metadataTrackIndex, metaData, metaInfo);
    };
    muxer.stop();
    muxer.release();
  }
```

## Features and API History

The following table summarizes the feature support in different API version and containers. For API version numbers, see `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#`.

| Symbol | Meaning |
|---|---|
| ● | Supported |
| ○ | Not supported |
| ▧ | Supported in MP4/WebM/3GP |
| ⁕ | Only Supported in MP4 |

| Feature | SDK Version ||||||||||||||||||||||||
| Feature | 18 | 19 | 20 | 21 | 22 | 23 | 24 | 25 | 26+ |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| MP4 container | ● | ● | ● | ● | ● | ● | ● | ● | ● |
| WebM container | ○ | ○ | ○ | ● | ● | ● | ● | ● | ● |
| 3GP container | ○ | ○ | ○ | ○ | ○ | ○ | ○ | ○ | ● |
| Muxing B-Frames (bi-directional predicted frames) | ○ | ○ | ○ | ○ | ○ | ○ | ○ | ⁕ | ⁕ |
| Muxing Single Video/Audio Track | ▧ | ▧ | ▧ | ▧ | ▧ | ▧ | ▧ | ▧ | ▧ |
| Muxing Multiple Video/Audio Tracks | ○ | ○ | ○ | ○ | ○ | ○ | ○ | ○ | ⁕ |
| Muxing Metadata Tracks | ○ | ○ | ○ | ○ | ○ | ○ | ○ | ○ | ⁕ |

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/media/MediaMuxer.OutputFormat` Defines the output format. |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/media/MediaMuxer#MediaMuxer(java.io.FileDescriptor,%20kotlin.Int)(fd: https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#, format: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Creates a media muxer that writes to the specified FileDescriptor. |
| `https://developer.android.com/reference/kotlin/android/media/MediaMuxer#MediaMuxer(kotlin.String,%20kotlin.Int)(path: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, format: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Creates a media muxer that writes to the specified path. |

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaMuxer#addTrack(android.media.MediaFormat)(format: https://developer.android.com/reference/kotlin/android/media/MediaFormat)` Adds a track with the specified format. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaMuxer#release()()` Make sure you call this when you're done to free up any resources instead of relying on the garbage collector to do this for you at some point in the future. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaMuxer#setLocation(kotlin.Float,%20kotlin.Float)(latitude: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, longitude: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Set and store the geodata (latitude and longitude) in the output file. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaMuxer#setOrientationHint(kotlin.Int)(degrees: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the orientation hint for output video playback. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaMuxer#start()()` Starts the muxer. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaMuxer#stop()()` Stops the muxer. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaMuxer#writeSampleData(kotlin.Int,%20java.nio.ByteBuffer,%20android.media.MediaCodec.BufferInfo)(trackIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, byteBuf: https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#, bufferInfo: https://developer.android.com/reference/kotlin/android/media/MediaCodec.BufferInfo)` Writes an encoded sample into the muxer. |

| Protected methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaMuxer#finalize()()` Called by the garbage collector on an object when garbage collection determines that there are no more references to the object. |

## Public constructors

### MediaMuxer

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
MediaMuxer(
    fd: FileDescriptor, 
    format: Int)
```

Creates a media muxer that writes to the specified FileDescriptor.

The caller must not use the file referenced by the specified `fd` before calling `https://developer.android.com/reference/kotlin/android/media/MediaMuxer#stop()`.

It is the caller's responsibility to close the file descriptor, which is safe to do so as soon as this call returns.

| Parameters ||
|---|---|
| `fd` | [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#): The FileDescriptor of the output media file. If `format` is `https://developer.android.com/reference/kotlin/android/media/MediaMuxer.OutputFormat#MUXER_OUTPUT_WEBM:kotlin.Int`, `fd` must be open in read-write mode. Otherwise, write mode is sufficient, but read-write is also accepted. This value cannot be `null`. |
| `format` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The format of the output media file. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/media/MediaMuxer.OutputFormat#MUXER_OUTPUT_MPEG_4:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/MediaMuxer.OutputFormat#MUXER_OUTPUT_WEBM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/MediaMuxer.OutputFormat#MUXER_OUTPUT_3GPP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/MediaMuxer.OutputFormat#MUXER_OUTPUT_HEIF:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/MediaMuxer.OutputFormat#MUXER_OUTPUT_OGG:kotlin.Int` |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an error occurs while performing an IO operation. |
| `java.lang.IllegalArgumentException` | if `format` is not supported, or if `fd` is not open in the expected mode. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/MediaMuxer.OutputFormat`

### MediaMuxer

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
MediaMuxer(
    path: String, 
    format: Int)
```

Creates a media muxer that writes to the specified path.

The caller must not use the file `path` before calling `https://developer.android.com/reference/kotlin/android/media/MediaMuxer#stop()`.

| Parameters ||
|---|---|
| `path` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The path of the output media file. This value cannot be `null`. |
| `format` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The format of the output media file. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/media/MediaMuxer.OutputFormat#MUXER_OUTPUT_MPEG_4:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/MediaMuxer.OutputFormat#MUXER_OUTPUT_WEBM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/MediaMuxer.OutputFormat#MUXER_OUTPUT_3GPP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/MediaMuxer.OutputFormat#MUXER_OUTPUT_HEIF:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/MediaMuxer.OutputFormat#MUXER_OUTPUT_OGG:kotlin.Int` |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an error occurs while opening or creating the output file. |
| `java.lang.IllegalArgumentException` | if path is invalid or format is not supported. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/MediaMuxer.OutputFormat`

## Public methods

### addTrack

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun addTrack(format: MediaFormat): Int
```

Adds a track with the specified format.

The following table summarizes support for specific format keys across android releases. Keys marked with '+:' are required.

| OS Version(s) | `MediaFormat` keys used for |||
| OS Version(s) | All Tracks | Audio Tracks | Video Tracks |
|---|---|---|---|
| `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#JELLY_BEAN_MR2:kotlin.Int` | +: `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_MIME:kotlin.String` | +: `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_SAMPLE_RATE:kotlin.String`, +: `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_CHANNEL_COUNT:kotlin.String`, +: **codec-specific dataAAC** | +: `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_WIDTH:kotlin.String`, +: `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_HEIGHT:kotlin.String`, no `KEY_ROTATION`, use `https://developer.android.com/reference/kotlin/android/media/MediaMuxer#setOrientationHint(kotlin.Int)`.mp4, +: **codec-specific dataAVC, MPEG4** |
| `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#KITKAT:kotlin.Int` | +: `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_MIME:kotlin.String` | +: `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_SAMPLE_RATE:kotlin.String`, +: `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_CHANNEL_COUNT:kotlin.String`, +: **codec-specific dataAAC** | +: `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_WIDTH:kotlin.String`, +: `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_HEIGHT:kotlin.String`, no `KEY_ROTATION`, use `https://developer.android.com/reference/kotlin/android/media/MediaMuxer#setOrientationHint(kotlin.Int)`.mp4, +: **codec-specific dataAVC, MPEG4** |
| `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#KITKAT_WATCH:kotlin.Int` | +: `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_MIME:kotlin.String` | +: `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_SAMPLE_RATE:kotlin.String`, +: `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_CHANNEL_COUNT:kotlin.String`, +: **codec-specific dataAAC** | +: `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_WIDTH:kotlin.String`, +: `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_HEIGHT:kotlin.String`, no `KEY_ROTATION`, use `https://developer.android.com/reference/kotlin/android/media/MediaMuxer#setOrientationHint(kotlin.Int)`.mp4, +: **codec-specific dataAVC, MPEG4** |
| `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#LOLLIPOP:kotlin.Int` | +: `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_MIME:kotlin.String` | as above, plus +: **codec-specific dataVorbis \& .webm** | +: `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_WIDTH:kotlin.String`, +: `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_HEIGHT:kotlin.String`, no `KEY_ROTATION`, use `https://developer.android.com/reference/kotlin/android/media/MediaMuxer#setOrientationHint(kotlin.Int)`.mp4, +: **codec-specific dataAVC, MPEG4** |
| `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#LOLLIPOP_MR1:kotlin.Int` | +: `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_MIME:kotlin.String` | as above, plus +: **codec-specific dataVorbis \& .webm** | +: `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_WIDTH:kotlin.String`, +: `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_HEIGHT:kotlin.String`, no `KEY_ROTATION`, use `https://developer.android.com/reference/kotlin/android/media/MediaMuxer#setOrientationHint(kotlin.Int)`.mp4, +: **codec-specific dataAVC, MPEG4** |
| `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#M:kotlin.Int` | +: `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_MIME:kotlin.String` | as above, plus +: **codec-specific dataVorbis \& .webm** | as above, plus `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_BIT_RATE:kotlin.String`AAC |
| `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#N:kotlin.Int` | +: `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_MIME:kotlin.String` | as above, plus +: **codec-specific dataVorbis \& .webm** | as above, plus `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_BIT_RATE:kotlin.String`MPEG4, `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_HDR_STATIC_INFO:kotlin.String`, .webm, `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_COLOR_STANDARD:kotlin.String`, `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_COLOR_TRANSFER:kotlin.String`, `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_COLOR_RANGE:kotlin.String`, +: **codec-specific dataHEVC** , codec-specific dataVP9 |
| **Notes:** #: storing into container metadata. .mp4, .webm...: for listed containers MPEG4, AAC...: for listed codecs ||||
| Note that the codec-specific data for the track must be specified using this method. Furthermore, codec-specific data must not be passed/specified via the `https://developer.android.com/reference/kotlin/android/media/MediaMuxer#writeSampleData(kotlin.Int,%20java.nio.ByteBuffer,%20android.media.MediaCodec.BufferInfo)` call. ||||

The following table summarizes codec support for containers across android releases:

| Codec | [MP4](https://developer.android.com/reference/kotlin/android/media/MediaMuxer.OutputFormat#MUXER_OUTPUT_MPEG_4:kotlin.Int) | [WEBM](https://developer.android.com/reference/kotlin/android/media/MediaMuxer.OutputFormat#MUXER_OUTPUT_WEBM:kotlin.Int) | [OGG](https://developer.android.com/reference/kotlin/android/media/MediaMuxer.OutputFormat#MUXER_OUTPUT_OGG:kotlin.Int) | Supported From SDK version |
|---|---|---|---|---|
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_AUDIO_AAC:kotlin.String` | ✓ | | | 16 |
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_AUDIO_AMR_NB:kotlin.String` | ✓ | | | 16 |
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_AUDIO_AMR_WB:kotlin.String` | ✓ | | | 16 |
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_VIDEO_H263:kotlin.String` | ✓ | | | 16 |
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_VIDEO_MPEG4:kotlin.String` | ✓ | | | 16 |
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_VIDEO_AVC:kotlin.String` (H.264) | ✓ | | | 16 |
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_AUDIO_VORBIS:kotlin.String` | | ✓ | | 21 |
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_VIDEO_VP8:kotlin.String` | | ✓ | | 21 |
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_VIDEO_VP9:kotlin.String` | | ✓ | | 24 |
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_VIDEO_HEVC:kotlin.String` (H.265) | ✓ | | | 24 |
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_AUDIO_OPUS:kotlin.String` | | ✓ | ✓ | 29 |
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_VIDEO_DOLBY_VISION:kotlin.String` | ✓ | | | 33 |
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_VIDEO_AV1:kotlin.String` | ✓ | | | 34 |
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_VIDEO_APV:kotlin.String` | ✓ | | | 36 |

| Parameters ||
|---|---|
| `format` | [MediaFormat](https://developer.android.com/reference/kotlin/android/media/MediaFormat): The media format for the track. This must not be an empty MediaFormat. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The track index for this newly added track, and it should be used in the `https://developer.android.com/reference/kotlin/android/media/MediaMuxer#writeSampleData(kotlin.Int,%20java.nio.ByteBuffer,%20android.media.MediaCodec.BufferInfo)`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if format is invalid. |
| `java.lang.IllegalStateException` | if muxer is in the wrong state. |

### release

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun release(): Unit
```

Make sure you call this when you're done to free up any resources instead of relying on the garbage collector to do this for you at some point in the future.

### setLocation

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setLocation(
    latitude: Float, 
    longitude: Float
): Unit
```

Set and store the geodata (latitude and longitude) in the output file. This method should be called before `https://developer.android.com/reference/kotlin/android/media/MediaMuxer#start()`. The geodata is stored in udta box if the output format is `https://developer.android.com/reference/kotlin/android/media/MediaMuxer.OutputFormat#MUXER_OUTPUT_MPEG_4:kotlin.Int`, and is ignored for other output formats. The geodata is stored according to ISO-6709 standard.

| Parameters ||
|---|---|
| `latitude` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): Latitude in degrees. Its value must be in the range \[-90, 90\]. |
| `longitude` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): Longitude in degrees. Its value must be in the range \[-180, 180\]. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If the given latitude or longitude is out of range. |
| `java.lang.IllegalStateException` | If this method is called after `https://developer.android.com/reference/kotlin/android/media/MediaMuxer#start()`. |

### setOrientationHint

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setOrientationHint(degrees: Int): Unit
```

Sets the orientation hint for output video playback.

This method should be called before `https://developer.android.com/reference/kotlin/android/media/MediaMuxer#start()`. Calling this method will not rotate the video frame when muxer is generating the file, but add a composition matrix containing the rotation angle in the output video if the output format is `https://developer.android.com/reference/kotlin/android/media/MediaMuxer.OutputFormat#MUXER_OUTPUT_MPEG_4:kotlin.Int` so that a video player can choose the proper orientation for playback. Note that some video players may choose to ignore the composition matrix in a video during playback. By default, the rotation degree is 0.

| Parameters ||
|---|---|
| `degrees` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the angle to be rotated clockwise in degrees. The supported angles are 0, 90, 180, and 270 degrees. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if degree is not supported. |
| `java.lang.IllegalStateException` | If this method is called after `https://developer.android.com/reference/kotlin/android/media/MediaMuxer#start()`. |

### start

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun start(): Unit
```

Starts the muxer.

Make sure this is called after `https://developer.android.com/reference/kotlin/android/media/MediaMuxer#addTrack(android.media.MediaFormat)` and before `https://developer.android.com/reference/kotlin/android/media/MediaMuxer#writeSampleData(kotlin.Int,%20java.nio.ByteBuffer,%20android.media.MediaCodec.BufferInfo)`.

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If this method is called after `https://developer.android.com/reference/kotlin/android/media/MediaMuxer#start()` or Muxer is released |

### stop

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun stop(): Unit
```

Stops the muxer.

Once the muxer stops, it can not be restarted.

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if muxer is in the wrong state. |

### writeSampleData

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeSampleData(
    trackIndex: Int, 
    byteBuf: ByteBuffer, 
    bufferInfo: MediaCodec.BufferInfo
): Unit
```

Writes an encoded sample into the muxer.

The application needs to make sure that the samples are written into the right tracks. Also, it needs to make sure the samples for each track are written in chronological order (e.g. in the order they are provided by the encoder.)

For MPEG4 media format, the duration of the last sample in a track can be set by passing an additional empty buffer(bufferInfo.size = 0) with MediaCodec.BUFFER_FLAG_END_OF_STREAM flag and a suitable presentation timestamp set in bufferInfo parameter as the last sample of that track. This last sample's presentation timestamp shall be a sum of the presentation timestamp and the duration preferred for the original last sample. If no explicit END_OF_STREAM sample was passed, then the duration of the last sample would be the same as that of the sample before that.

| Parameters ||
|---|---|
| `trackIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The track index for this sample. |
| `byteBuf` | [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#): The encoded sample. This value cannot be `null`. |
| `bufferInfo` | [MediaCodec.BufferInfo](https://developer.android.com/reference/kotlin/android/media/MediaCodec.BufferInfo): The buffer information related to this sample. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if trackIndex, byteBuf or bufferInfo is invalid. |
| `java.lang.IllegalStateException` | if muxer is in wrong state. MediaMuxer uses the flags provided in `https://developer.android.com/reference/kotlin/android/media/MediaCodec.BufferInfo`, to signal sync frames. |

## Protected methods

### finalize

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected fun finalize(): Unit
```

Called by the garbage collector on an object when garbage collection determines that there are no more references to the object. A subclass overrides the `finalize` method to dispose of system resources or to perform other cleanup.

The general contract of `finalize` is that it is invoked if and when the Java virtual machine has determined that there is no longer any means by which this object can be accessed by any thread that has not yet died, except as a result of an action taken by the finalization of some other object or class which is ready to be finalized. The `finalize` method may take any action, including making this object available again to other threads; the usual purpose of `finalize`, however, is to perform cleanup actions before the object is irrevocably discarded. For example, the finalize method for an object that represents an input/output connection might perform explicit I/O transactions to break the connection before the object is permanently discarded.

The `finalize` method of class `Object` performs no special action; it simply returns normally. Subclasses of `Object` may override this definition.

The Java programming language does not guarantee which thread will invoke the `finalize` method for any given object. It is guaranteed, however, that the thread that invokes finalize will not be holding any user-visible synchronization locks when finalize is invoked. If an uncaught exception is thrown by the finalize method, the exception is ignored and finalization of that object terminates.

After the `finalize` method has been invoked for an object, no further action is taken until the Java virtual machine has again determined that there is no longer any means by which this object can be accessed by any thread that has not yet died, including possible actions by other objects or classes which are ready to be finalized, at which point the object may be discarded.

The `finalize` method is never invoked more than once by a Java virtual machine for any given object.

Any exception thrown by the `finalize` method causes the finalization of this object to be halted, but is otherwise ignored.

| Exceptions ||
|---|---|
| `java.lang.Throwable` | the `Exception` raised by this method |
