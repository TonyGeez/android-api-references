Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MediaParser

```
class MediaParser
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.MediaParser](https://developer.android.com/reference/kotlin/android/media/MediaParser#) |

Parses media container formats and extracts contained media samples and metadata.

This class provides access to a battery of low-level media container parsers. Each instance of this class is associated to a specific media parser implementation which is suitable for extraction from a specific media container format. The media parser implementation assignment depends on the factory method (see `https://developer.android.com/reference/kotlin/android/media/MediaParser#create(android.media.MediaParser.OutputConsumer,%20kotlin.String)` and `https://developer.android.com/reference/kotlin/android/media/MediaParser#createByName(kotlin.String,%20android.media.MediaParser.OutputConsumer)`) used to create the instance.

Users must implement the following to use this class.

- `https://developer.android.com/reference/kotlin/android/media/MediaParser.InputReader`: Provides the media container's bytes to parse.
- `https://developer.android.com/reference/kotlin/android/media/MediaParser.OutputConsumer`: Provides a sink for all extracted data and metadata.

The following code snippet includes a usage example:

```kotlin
MyOutputConsumer myOutputConsumer = new MyOutputConsumer();
  MyInputReader myInputReader = new MyInputReader("www.example.com");
  MediaParser mediaParser = MediaParser.create(myOutputConsumer);
 
  while (mediaParser.advance(myInputReader)) {}
 
  mediaParser.release();
  mediaParser = null;
  
```

The following code snippet provides a rudimentary `https://developer.android.com/reference/kotlin/android/media/MediaParser.OutputConsumer` sample implementation which extracts and publishes all video samples:

```kotlin
class VideoOutputConsumer implements MediaParser.OutputConsumer {
 
      private byte[] sampleDataBuffer = new byte[4096];
      private byte[] discardedDataBuffer = new byte[4096];
      private int videoTrackIndex = -1;
      private int bytesWrittenCount = 0;
 
      @Override
      public void onSeekMapFound(int i, @NonNull SeekMap seekMap) {
        // Do nothing.
      }
 
      @Override
      public void onTrackDataFound(int i, @NonNull TrackData trackData) {
        MediaFormat mediaFormat = trackData.mediaFormat;
        if (videoTrackIndex == -1 &&
            mediaFormat
                .getString(MediaFormat.KEY_MIME, /* defaultValue= */ "")
                .startsWith("video/")) {
          videoTrackIndex = i;
        }
      }
 
      @Override
      public void onSampleDataFound(int trackIndex, @NonNull InputReader inputReader)
          throws IOException {
        int numberOfBytesToRead = (int) inputReader.getLength();
        if (videoTrackIndex != trackIndex) {
          // Discard contents.
          inputReader.read(
              discardedDataBuffer,
              /* offset= */ 0,
              Math.min(discardDataBuffer.length, numberOfBytesToRead));
        } else {
          ensureSpaceInBuffer(numberOfBytesToRead);
          int bytesRead = inputReader.read(
              sampleDataBuffer, bytesWrittenCount, numberOfBytesToRead);
          bytesWrittenCount += bytesRead;
        }
      }
 
      @Override
      public void onSampleCompleted(
          int trackIndex,
          long timeMicros,
          int flags,
          int size,
          int offset,
          @Nullable CryptoInfo cryptoData) {
        if (videoTrackIndex != trackIndex) {
          return; // It's not the video track. Ignore.
        }
        byte[] sampleData = new byte[size];
        int sampleStartOffset = bytesWrittenCount - size - offset;
        System.arraycopy(
            sampleDataBuffer,
            sampleStartOffset,
            sampleData,
            /* destPos= */ 0,
            size);
        // Place trailing bytes at the start of the buffer.
        System.arraycopy(
            sampleDataBuffer,
            bytesWrittenCount - offset,
            sampleDataBuffer,
            /* destPos= */ 0,
            /* size= */ offset);
        bytesWrittenCount = bytesWrittenCount - offset;
        publishSample(sampleData, timeMicros, flags);
      }
 
     private void ensureSpaceInBuffer(int numberOfBytesToRead) {
       int requiredLength = bytesWrittenCount + numberOfBytesToRead;
       if (requiredLength > sampleDataBuffer.length) {
         sampleDataBuffer = Arrays.copyOf(sampleDataBuffer, requiredLength);
       }
     }
 
    }
 
  
```

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/media/MediaParser.InputReader` Provides input data to `https://developer.android.com/reference/kotlin/android/media/MediaParser#`. |
| abstract | `https://developer.android.com/reference/kotlin/android/media/MediaParser.OutputConsumer` Receives extracted media sample data and metadata from `https://developer.android.com/reference/kotlin/android/media/MediaParser#`. |
| | `https://developer.android.com/reference/kotlin/android/media/MediaParser.ParsingException` Thrown when an error occurs while parsing a media stream. |
| --- | --- |
| | `https://developer.android.com/reference/kotlin/android/media/MediaParser.SeekMap` Maps seek positions to `https://developer.android.com/reference/kotlin/android/media/MediaParser.SeekPoint` in the stream. |
| | `https://developer.android.com/reference/kotlin/android/media/MediaParser.SeekPoint` Defines a seek point in a media stream. |
| abstract | `https://developer.android.com/reference/kotlin/android/media/MediaParser.SeekableInputReader` `https://developer.android.com/reference/kotlin/android/media/MediaParser.InputReader` that allows setting the read position. |
| --- | --- |
| | `https://developer.android.com/reference/kotlin/android/media/MediaParser.TrackData` Holds information associated with a track. |
| | `https://developer.android.com/reference/kotlin/android/media/MediaParser.UnrecognizedInputFormatException` Thrown if all parser implementations provided to `https://developer.android.com/reference/kotlin/android/media/MediaParser#create(android.media.MediaParser.OutputConsumer,%20kotlin.String)` failed to sniff the input content. |

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARAMETER_ADTS_ENABLE_CBR_SEEKING:kotlin.String` Sets whether constant bitrate seeking should be enabled for ADTS parsing. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARAMETER_AMR_ENABLE_CBR_SEEKING:kotlin.String` Sets whether constant bitrate seeking should be enabled for AMR. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARAMETER_FLAC_DISABLE_ID3:kotlin.String` Sets whether the ID3 track should be disabled for FLAC. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARAMETER_MATROSKA_DISABLE_CUES_SEEKING:kotlin.String` Sets whether Matroska parsing should avoid seeking to the cues element. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARAMETER_MP3_DISABLE_ID3:kotlin.String` Sets whether the ID3 track should be disabled for MP3. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARAMETER_MP3_ENABLE_CBR_SEEKING:kotlin.String` Sets whether constant bitrate seeking should be enabled for MP3. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARAMETER_MP3_ENABLE_INDEX_SEEKING:kotlin.String` Sets whether MP3 parsing should generate a time-to-byte mapping. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARAMETER_MP4_IGNORE_EDIT_LISTS:kotlin.String` Sets whether MP4 parsing should ignore edit lists. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARAMETER_MP4_IGNORE_TFDT_BOX:kotlin.String` Sets whether MP4 parsing should ignore the tfdt box. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARAMETER_MP4_TREAT_VIDEO_FRAMES_AS_KEYFRAMES:kotlin.String` Sets whether MP4 parsing should treat all video frames as key frames. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARAMETER_TS_ALLOW_NON_IDR_AVC_KEYFRAMES:kotlin.String` Sets whether TS should treat samples consisting of non-IDR I slices as synchronization samples (key-frames). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARAMETER_TS_DETECT_ACCESS_UNITS:kotlin.String` Sets whether TS parsing should split AVC stream into access units based on slice headers. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARAMETER_TS_ENABLE_HDMV_DTS_AUDIO_STREAMS:kotlin.String` Sets whether TS parsing should handle HDMV DTS audio streams. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARAMETER_TS_IGNORE_AAC_STREAM:kotlin.String` Sets whether TS parsing should ignore AAC elementary streams. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARAMETER_TS_IGNORE_AVC_STREAM:kotlin.String` Sets whether TS parsing should ignore AVC elementary streams. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARAMETER_TS_IGNORE_SPLICE_INFO_STREAM:kotlin.String` Sets whether TS parsing should ignore splice information streams. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARAMETER_TS_MODE:kotlin.String` Sets the operation mode for TS parsing. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_AC3:kotlin.String` Parser for the AC-3 container format, as defined in Digital Audio Compression Standard (AC-3). |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_AC4:kotlin.String` Parser for the AC-4 container format, as defined by Dolby AC-4: Audio delivery for Next-Generation Entertainment Services. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_ADTS:kotlin.String` Parser for the ADTS container format, as defined in ISO/IEC 13818-7. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_AMR:kotlin.String` Parser for the AMR container format, as defined in RFC 4867. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_FLAC:kotlin.String` Parser for the FLAC container format, as defined in the [spec](https://xiph.org/flac/). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_FLV:kotlin.String` Parser for the FLV container format, as defined in Adobe Flash Video File Format Specification. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_FMP4:kotlin.String` Parser for fragmented files using the MP4 container format, as defined in ISO/IEC 14496-12. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_MATROSKA:kotlin.String` Parser for the Matroska container format, as defined in the [spec](https://matroska.org/technical/specs/). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_MP3:kotlin.String` Parser for the MP3 container format, as defined in ISO/IEC 11172-3. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_MP4:kotlin.String` Parser for non-fragmented files using the MP4 container format, as defined in ISO/IEC 14496-12. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_OGG:kotlin.String` Parser for the OGG container format, as defined in RFC 3533. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_PS:kotlin.String` Parser for the PS container format, as defined in ISO/IEC 11172-1. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_TS:kotlin.String` Parser for the TS container format, as defined in ISO/IEC 13818-1. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_UNKNOWN:kotlin.String` Parser name returned by `https://developer.android.com/reference/kotlin/android/media/MediaParser#getParserName()` when no parser has been selected yet. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_WAV:kotlin.String` Parser for the WAV container format, as defined in Multimedia Programming Interface and Data Specifications. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaParser#SAMPLE_FLAG_DECODE_ONLY:kotlin.Int` Indicates that the sample should be decoded but not rendered. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaParser#SAMPLE_FLAG_ENCRYPTED:kotlin.Int` Indicates that the sample is (at least partially) encrypted. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaParser#SAMPLE_FLAG_HAS_SUPPLEMENTAL_DATA:kotlin.Int` Indicates that the sample has supplemental data. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaParser#SAMPLE_FLAG_KEY_FRAME:kotlin.Int` Indicates that the sample holds a synchronization sample. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaParser#SAMPLE_FLAG_LAST_SAMPLE:kotlin.Int` Indicates that the sample is known to contain the last media sample of the stream. |

| Public methods ||
|---|---|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaParser#advance(android.media.MediaParser.SeekableInputReader)(seekableInputReader: https://developer.android.com/reference/kotlin/android/media/MediaParser.SeekableInputReader)` Makes progress in the extraction of the input media stream, unless the end of the input has been reached. |
| static [MediaParser](https://developer.android.com/reference/kotlin/android/media/MediaParser#) | `https://developer.android.com/reference/kotlin/android/media/MediaParser#create(android.media.MediaParser.OutputConsumer,%20kotlin.String)(outputConsumer: https://developer.android.com/reference/kotlin/android/media/MediaParser.OutputConsumer, vararg parserNames: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Creates an instance whose backing parser will be selected by sniffing the content during the first `https://developer.android.com/reference/kotlin/android/media/MediaParser#advance(android.media.MediaParser.SeekableInputReader)` call. |
| static [MediaParser](https://developer.android.com/reference/kotlin/android/media/MediaParser#) | `https://developer.android.com/reference/kotlin/android/media/MediaParser#createByName(kotlin.String,%20android.media.MediaParser.OutputConsumer)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, outputConsumer: https://developer.android.com/reference/kotlin/android/media/MediaParser.OutputConsumer)` Creates an instance backed by the parser with the given `name`. |
| --- | --- |
| [LogSessionId](https://developer.android.com/reference/kotlin/android/media/metrics/LogSessionId) | `https://developer.android.com/reference/kotlin/android/media/MediaParser#getLogSessionId()()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaParser#getParserName()()` Returns the name of the backing parser implementation. |
| static [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | `https://developer.android.com/reference/kotlin/android/media/MediaParser#getParserNames(android.media.MediaFormat)(mediaFormat: https://developer.android.com/reference/kotlin/android/media/MediaFormat)` Returns an immutable list with the names of the parsers that are suitable for container formats with the given `https://developer.android.com/reference/kotlin/android/media/MediaFormat`. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaParser#release()()` Releases any acquired resources. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaParser#seek(android.media.MediaParser.SeekPoint)(seekPoint: https://developer.android.com/reference/kotlin/android/media/MediaParser.SeekPoint)` Seeks within the media container being extracted. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaParser#setLogSessionId(android.media.metrics.LogSessionId)(logSessionId: https://developer.android.com/reference/kotlin/android/media/metrics/LogSessionId)` <br /> |
| --- | --- |
| [MediaParser](https://developer.android.com/reference/kotlin/android/media/MediaParser#) | `https://developer.android.com/reference/kotlin/android/media/MediaParser#setParameter(kotlin.String,%20kotlin.Any)(parameterName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)` Sets parser-specific parameters which allow customizing behavior. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaParser#supportsParameter(kotlin.String)(parameterName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Returns whether the given `parameterName` is supported by this parser. |

## Constants

### PARAMETER_ADTS_ENABLE_CBR_SEEKING

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PARAMETER_ADTS_ENABLE_CBR_SEEKING: String
```

Sets whether constant bitrate seeking should be enabled for ADTS parsing. `boolean` expected. Default value is `false`.

 Value: "android.media.mediaparser.adts.enableCbrSeeking"

### PARAMETER_AMR_ENABLE_CBR_SEEKING

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PARAMETER_AMR_ENABLE_CBR_SEEKING: String
```

Sets whether constant bitrate seeking should be enabled for AMR. `boolean` expected. Default value is `false`.

 Value: "android.media.mediaparser.amr.enableCbrSeeking"

### PARAMETER_FLAC_DISABLE_ID3

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PARAMETER_FLAC_DISABLE_ID3: String
```

Sets whether the ID3 track should be disabled for FLAC. `boolean` expected. Default value is `false`.

 Value: "android.media.mediaparser.flac.disableId3"

### PARAMETER_MATROSKA_DISABLE_CUES_SEEKING

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PARAMETER_MATROSKA_DISABLE_CUES_SEEKING: String
```

Sets whether Matroska parsing should avoid seeking to the cues element. `boolean` expected. Default value is `false`.

If this flag is enabled and the cues element occurs after the first cluster, then the media is treated as unseekable.

 Value: "android.media.mediaparser.matroska.disableCuesSeeking"

### PARAMETER_MP3_DISABLE_ID3

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PARAMETER_MP3_DISABLE_ID3: String
```

Sets whether the ID3 track should be disabled for MP3. `boolean` expected. Default value is `false`.

 Value: "android.media.mediaparser.mp3.disableId3"

### PARAMETER_MP3_ENABLE_CBR_SEEKING

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PARAMETER_MP3_ENABLE_CBR_SEEKING: String
```

Sets whether constant bitrate seeking should be enabled for MP3. `boolean` expected. Default value is `false`.

 Value: "android.media.mediaparser.mp3.enableCbrSeeking"

### PARAMETER_MP3_ENABLE_INDEX_SEEKING

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PARAMETER_MP3_ENABLE_INDEX_SEEKING: String
```

Sets whether MP3 parsing should generate a time-to-byte mapping. `boolean` expected. Default value is `false`.

Enabling this flag may require to scan a significant portion of the file to compute a seek point. Therefore, it should only be used if:

- the file is small, or
- the bitrate is variable (or the type of bitrate is unknown) and the seeking metadata provided in the file is not precise enough (or is not present).

 Value: "android.media.mediaparser.mp3.enableIndexSeeking"

### PARAMETER_MP4_IGNORE_EDIT_LISTS

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PARAMETER_MP4_IGNORE_EDIT_LISTS: String
```

Sets whether MP4 parsing should ignore edit lists. `boolean` expected. Default value is `false`.

 Value: "android.media.mediaparser.mp4.ignoreEditLists"

### PARAMETER_MP4_IGNORE_TFDT_BOX

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PARAMETER_MP4_IGNORE_TFDT_BOX: String
```

Sets whether MP4 parsing should ignore the tfdt box. `boolean` expected. Default value is `false`.

 Value: "android.media.mediaparser.mp4.ignoreTfdtBox"

### PARAMETER_MP4_TREAT_VIDEO_FRAMES_AS_KEYFRAMES

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PARAMETER_MP4_TREAT_VIDEO_FRAMES_AS_KEYFRAMES: String
```

Sets whether MP4 parsing should treat all video frames as key frames. `boolean` expected. Default value is `false`.

 Value: "android.media.mediaparser.mp4.treatVideoFramesAsKeyframes"

### PARAMETER_TS_ALLOW_NON_IDR_AVC_KEYFRAMES

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PARAMETER_TS_ALLOW_NON_IDR_AVC_KEYFRAMES: String
```

Sets whether TS should treat samples consisting of non-IDR I slices as synchronization samples (key-frames). `boolean` expected. Default value is `false`.

 Value: "android.media.mediaparser.ts.allowNonIdrAvcKeyframes"

### PARAMETER_TS_DETECT_ACCESS_UNITS

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PARAMETER_TS_DETECT_ACCESS_UNITS: String
```

Sets whether TS parsing should split AVC stream into access units based on slice headers. `boolean` expected. Default value is `false`.

This flag should be left disabled if the stream contains access units delimiters in order to avoid unnecessary computational costs.

 Value: "android.media.mediaparser.ts.ignoreDetectAccessUnits"

### PARAMETER_TS_ENABLE_HDMV_DTS_AUDIO_STREAMS

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PARAMETER_TS_ENABLE_HDMV_DTS_AUDIO_STREAMS: String
```

Sets whether TS parsing should handle HDMV DTS audio streams. `boolean` expected. Default value is `false`.

Enabling this flag will disable the detection of SCTE subtitles.

 Value: "android.media.mediaparser.ts.enableHdmvDtsAudioStreams"

### PARAMETER_TS_IGNORE_AAC_STREAM

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PARAMETER_TS_IGNORE_AAC_STREAM: String
```

Sets whether TS parsing should ignore AAC elementary streams. `boolean` expected. Default value is `false`.

 Value: "android.media.mediaparser.ts.ignoreAacStream"

### PARAMETER_TS_IGNORE_AVC_STREAM

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PARAMETER_TS_IGNORE_AVC_STREAM: String
```

Sets whether TS parsing should ignore AVC elementary streams. `boolean` expected. Default value is `false`.

 Value: "android.media.mediaparser.ts.ignoreAvcStream"

### PARAMETER_TS_IGNORE_SPLICE_INFO_STREAM

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PARAMETER_TS_IGNORE_SPLICE_INFO_STREAM: String
```

Sets whether TS parsing should ignore splice information streams. `boolean` expected. Default value is `false`.

 Value: "android.media.mediaparser.ts.ignoreSpliceInfoStream"

### PARAMETER_TS_MODE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PARAMETER_TS_MODE: String
```

Sets the operation mode for TS parsing. `String` expected. Valid values are `"single_pmt"`, `"multi_pmt"`, and `"hls"`. Default value is `"single_pmt"`.

The operation modes alter the way TS behaves so that it can handle certain kinds of commonly-occurring malformed media.

- `"single_pmt"`: Only the first found PMT is parsed. Others are ignored, even if more PMTs are declared in the PAT.
- `"multi_pmt"`: Behave as described in ISO/IEC 13818-1.
- `"hls"`: Enable `"single_pmt"` mode, and ignore continuity counters.

 Value: "android.media.mediaparser.ts.mode"

### PARSER_NAME_AC3

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PARSER_NAME_AC3: String
```

Parser for the AC-3 container format, as defined in Digital Audio Compression Standard (AC-3).

 Value: "android.media.mediaparser.Ac3Parser"

### PARSER_NAME_AC4

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PARSER_NAME_AC4: String
```

Parser for the AC-4 container format, as defined by Dolby AC-4: Audio delivery for Next-Generation Entertainment Services.

 Value: "android.media.mediaparser.Ac4Parser"

### PARSER_NAME_ADTS

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PARSER_NAME_ADTS: String
```

Parser for the ADTS container format, as defined in ISO/IEC 13818-7.

 Value: "android.media.mediaparser.AdtsParser"

### PARSER_NAME_AMR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PARSER_NAME_AMR: String
```

Parser for the AMR container format, as defined in RFC 4867.

 Value: "android.media.mediaparser.AmrParser"

### PARSER_NAME_FLAC

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PARSER_NAME_FLAC: String
```

Parser for the FLAC container format, as defined in the [spec](https://xiph.org/flac/).

 Value: "android.media.mediaparser.FlacParser"

### PARSER_NAME_FLV

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PARSER_NAME_FLV: String
```

Parser for the FLV container format, as defined in Adobe Flash Video File Format Specification.

 Value: "android.media.mediaparser.FlvParser"

### PARSER_NAME_FMP4

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PARSER_NAME_FMP4: String
```

Parser for fragmented files using the MP4 container format, as defined in ISO/IEC 14496-12.

 Value: "android.media.mediaparser.FragmentedMp4Parser"

### PARSER_NAME_MATROSKA

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PARSER_NAME_MATROSKA: String
```

Parser for the Matroska container format, as defined in the [spec](https://matroska.org/technical/specs/).

 Value: "android.media.mediaparser.MatroskaParser"

### PARSER_NAME_MP3

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PARSER_NAME_MP3: String
```

Parser for the MP3 container format, as defined in ISO/IEC 11172-3.

 Value: "android.media.mediaparser.Mp3Parser"

### PARSER_NAME_MP4

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PARSER_NAME_MP4: String
```

Parser for non-fragmented files using the MP4 container format, as defined in ISO/IEC 14496-12.

 Value: "android.media.mediaparser.Mp4Parser"

### PARSER_NAME_OGG

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PARSER_NAME_OGG: String
```

Parser for the OGG container format, as defined in RFC 3533.

 Value: "android.media.mediaparser.OggParser"

### PARSER_NAME_PS

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PARSER_NAME_PS: String
```

Parser for the PS container format, as defined in ISO/IEC 11172-1.

 Value: "android.media.mediaparser.PsParser"

### PARSER_NAME_TS

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PARSER_NAME_TS: String
```

Parser for the TS container format, as defined in ISO/IEC 13818-1.

 Value: "android.media.mediaparser.TsParser"

### PARSER_NAME_UNKNOWN

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PARSER_NAME_UNKNOWN: String
```

Parser name returned by `https://developer.android.com/reference/kotlin/android/media/MediaParser#getParserName()` when no parser has been selected yet.

 Value: "android.media.mediaparser.UNKNOWN"

### PARSER_NAME_WAV

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PARSER_NAME_WAV: String
```

Parser for the WAV container format, as defined in Multimedia Programming Interface and Data Specifications.

 Value: "android.media.mediaparser.WavParser"

### SAMPLE_FLAG_DECODE_ONLY

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SAMPLE_FLAG_DECODE_ONLY: Int
```

**Deprecated:** *This flag is no longer supported and will be ignored.*

Indicates that the sample should be decoded but not rendered.

 Value: -2147483648

### SAMPLE_FLAG_ENCRYPTED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SAMPLE_FLAG_ENCRYPTED: Int
```

Indicates that the sample is (at least partially) encrypted.

 Value: 1073741824

### SAMPLE_FLAG_HAS_SUPPLEMENTAL_DATA

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SAMPLE_FLAG_HAS_SUPPLEMENTAL_DATA: Int
```

Indicates that the sample has supplemental data.

Samples will not have this flag set unless the `"android.media.mediaparser.includeSupplementalData"` parameter is set to `true` via `https://developer.android.com/reference/kotlin/android/media/MediaParser#setParameter(kotlin.String,%20kotlin.Any)`.

Samples with supplemental data have the following sample data format:

- If the `"android.media.mediaparser.inBandCryptoInfo"` parameter is set, all encryption information.
- (4 bytes) `sample_data_size`: The size of the actual sample data, not including supplemental data or encryption information.
- (`sample_data_size` bytes): The media sample data.
- (remaining bytes) The supplemental data.

 Value: 268435456

### SAMPLE_FLAG_KEY_FRAME

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SAMPLE_FLAG_KEY_FRAME: Int
```

Indicates that the sample holds a synchronization sample.

 Value: 1

### SAMPLE_FLAG_LAST_SAMPLE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SAMPLE_FLAG_LAST_SAMPLE: Int
```

Indicates that the sample is known to contain the last media sample of the stream.

 Value: 536870912

## Public methods

### advance

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun advance(seekableInputReader: MediaParser.SeekableInputReader): Boolean
```

Makes progress in the extraction of the input media stream, unless the end of the input has been reached.

This method will block until some progress has been made.

If this instance was created using `https://developer.android.com/reference/kotlin/android/media/MediaParser#create(android.media.MediaParser.OutputConsumer,%20kotlin.String)`, the first call to this method will sniff the content using the selected parser implementations.

| Parameters ||
|---|---|
| `seekableInputReader` | [MediaParser.SeekableInputReader](https://developer.android.com/reference/kotlin/android/media/MediaParser.SeekableInputReader): The `https://developer.android.com/reference/kotlin/android/media/MediaParser.SeekableInputReader` from which to obtain the media container data. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Whether there is any data left to extract. Returns false if the end of input has been reached. |

| Exceptions ||
|---|---|
| `android.media.MediaParser.UnrecognizedInputFormatException` | If the format cannot be recognized by any of the underlying parser implementations. |
| `java.io.IOException` | If an error occurs while reading from the `https://developer.android.com/reference/kotlin/android/media/MediaParser.SeekableInputReader`. |

### create

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun create(
    outputConsumer: MediaParser.OutputConsumer, 
    vararg parserNames: String!
): MediaParser
```

Creates an instance whose backing parser will be selected by sniffing the content during the first `https://developer.android.com/reference/kotlin/android/media/MediaParser#advance(android.media.MediaParser.SeekableInputReader)` call. Parser implementations will sniff the content in order of appearance in `parserNames`.

| Parameters ||
|---|---|
| `outputConsumer` | [MediaParser.OutputConsumer](https://developer.android.com/reference/kotlin/android/media/MediaParser.OutputConsumer): The `https://developer.android.com/reference/kotlin/android/media/MediaParser.OutputConsumer` to which extracted data is output. This value cannot be `null`. |
| `parserNames` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The names of the parsers to sniff the content with. If empty, a default array of names is used. This value cannot be `null`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_UNKNOWN:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_MATROSKA:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_FMP4:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_MP4:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_MP3:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_ADTS:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_AC3:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_TS:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_FLV:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_OGG:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_PS:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_WAV:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_AMR:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_AC4:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_FLAC:kotlin.String` |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/media/MediaParser#` | A new instance. This value cannot be `null`. |

### createByName

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createByName(
    name: String, 
    outputConsumer: MediaParser.OutputConsumer
): MediaParser
```

Creates an instance backed by the parser with the given `name`. The returned instance will attempt parsing without sniffing the content.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The name of the parser that will be associated with the created instance. This value cannot be `null`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_UNKNOWN:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_MATROSKA:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_FMP4:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_MP4:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_MP3:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_ADTS:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_AC3:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_TS:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_FLV:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_OGG:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_PS:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_WAV:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_AMR:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_AC4:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_FLAC:kotlin.String` |
| `outputConsumer` | [MediaParser.OutputConsumer](https://developer.android.com/reference/kotlin/android/media/MediaParser.OutputConsumer): The `https://developer.android.com/reference/kotlin/android/media/MediaParser.OutputConsumer` to which track data and samples are pushed. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/media/MediaParser#` | A new instance. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If an invalid name is provided. |

### getLogSessionId

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getLogSessionId(): LogSessionId
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/media/metrics/LogSessionId` | This value cannot be `null`. |

### getParserName

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getParserName(): String
```

Returns the name of the backing parser implementation.

If this instance was creating using `https://developer.android.com/reference/kotlin/android/media/MediaParser#createByName(kotlin.String,%20android.media.MediaParser.OutputConsumer)`, the provided name is returned. If this instance was created using `https://developer.android.com/reference/kotlin/android/media/MediaParser#create(android.media.MediaParser.OutputConsumer,%20kotlin.String)`, this method will return `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_UNKNOWN:kotlin.String` until the first call to `https://developer.android.com/reference/kotlin/android/media/MediaParser#advance(android.media.MediaParser.SeekableInputReader)`, after which the name of the backing parser implementation is returned.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | The name of the backing parser implementation, or null if the backing parser implementation has not yet been selected. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_UNKNOWN:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_MATROSKA:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_FMP4:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_MP4:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_MP3:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_ADTS:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_AC3:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_TS:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_FLV:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_OGG:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_PS:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_WAV:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_AMR:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_AC4:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_FLAC:kotlin.String` |

### getParserNames

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getParserNames(mediaFormat: MediaFormat): MutableList<String!>
```

Returns an immutable list with the names of the parsers that are suitable for container formats with the given `https://developer.android.com/reference/kotlin/android/media/MediaFormat`.

A parser supports a `https://developer.android.com/reference/kotlin/android/media/MediaFormat` if the mime type associated with `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_MIME:kotlin.String` corresponds to the supported container format.

| Parameters ||
|---|---|
| `mediaFormat` | [MediaFormat](https://developer.android.com/reference/kotlin/android/media/MediaFormat): The `https://developer.android.com/reference/kotlin/android/media/MediaFormat` to check support for. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>` | The parser names that support the given `mediaFormat`, or the list of all parsers available if no container specific format information is provided. This value cannot be `null`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_UNKNOWN:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_MATROSKA:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_FMP4:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_MP4:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_MP3:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_ADTS:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_AC3:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_TS:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_FLV:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_OGG:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_PS:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_WAV:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_AMR:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_AC4:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARSER_NAME_FLAC:kotlin.String` |

### release

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun release(): Unit
```

Releases any acquired resources.

After calling this method, this instance becomes unusable and no other methods should be invoked.

### seek

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun seek(seekPoint: MediaParser.SeekPoint): Unit
```

Seeks within the media container being extracted.

`https://developer.android.com/reference/kotlin/android/media/MediaParser.SeekPoint` can be obtained from the `https://developer.android.com/reference/kotlin/android/media/MediaParser.SeekMap` passed to `https://developer.android.com/reference/kotlin/android/media/MediaParser.OutputConsumer#onSeekMapFound(android.media.MediaParser.SeekMap)`.

Following a call to this method, the `https://developer.android.com/reference/kotlin/android/media/MediaParser.InputReader` passed to the next invocation of `https://developer.android.com/reference/kotlin/android/media/MediaParser#advance(android.media.MediaParser.SeekableInputReader)` must provide data starting from `https://developer.android.com/reference/kotlin/android/media/MediaParser.SeekPoint#position:kotlin.Long` in the stream.

| Parameters ||
|---|---|
| `seekPoint` | [MediaParser.SeekPoint](https://developer.android.com/reference/kotlin/android/media/MediaParser.SeekPoint): The `https://developer.android.com/reference/kotlin/android/media/MediaParser.SeekPoint` to seek to. This value cannot be `null`. |

### setLogSessionId

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setLogSessionId(logSessionId: LogSessionId): Unit
```

| Parameters ||
|---|---|
| `logSessionId` | [LogSessionId](https://developer.android.com/reference/kotlin/android/media/metrics/LogSessionId): This value cannot be `null`. |

### setParameter

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setParameter(
    parameterName: String, 
    value: Any
): MediaParser
```

Sets parser-specific parameters which allow customizing behavior.

Must be called before the first call to `https://developer.android.com/reference/kotlin/android/media/MediaParser#advance(android.media.MediaParser.SeekableInputReader)`.

| Parameters ||
|---|---|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The name of the parameter to set. See `PARAMETER_*` constants for documentation on possible values. This value cannot be `null`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARAMETER_ADTS_ENABLE_CBR_SEEKING:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARAMETER_AMR_ENABLE_CBR_SEEKING:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARAMETER_FLAC_DISABLE_ID3:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARAMETER_MP4_IGNORE_EDIT_LISTS:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARAMETER_MP4_IGNORE_TFDT_BOX:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARAMETER_MP4_TREAT_VIDEO_FRAMES_AS_KEYFRAMES:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARAMETER_MATROSKA_DISABLE_CUES_SEEKING:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARAMETER_MP3_DISABLE_ID3:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARAMETER_MP3_ENABLE_CBR_SEEKING:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARAMETER_MP3_ENABLE_INDEX_SEEKING:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARAMETER_TS_MODE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARAMETER_TS_ALLOW_NON_IDR_AVC_KEYFRAMES:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARAMETER_TS_IGNORE_AAC_STREAM:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARAMETER_TS_IGNORE_AVC_STREAM:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARAMETER_TS_IGNORE_SPLICE_INFO_STREAM:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARAMETER_TS_DETECT_ACCESS_UNITS:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARAMETER_TS_ENABLE_HDMV_DTS_AUDIO_STREAMS:kotlin.String` |
| `value` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html): The value to set for the given `parameterName`. See `PARAMETER_*` constants for documentation on the expected types. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/media/MediaParser#` | This instance, for convenience. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If called after calling `https://developer.android.com/reference/kotlin/android/media/MediaParser#advance(android.media.MediaParser.SeekableInputReader)` on the same instance. |

### supportsParameter

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun supportsParameter(parameterName: String): Boolean
```

Returns whether the given `parameterName` is supported by this parser.

| Parameters ||
|---|---|
| `parameterName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The parameter name to check support for. One of the `PARAMETER_*` constants. This value cannot be `null`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARAMETER_ADTS_ENABLE_CBR_SEEKING:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARAMETER_AMR_ENABLE_CBR_SEEKING:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARAMETER_FLAC_DISABLE_ID3:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARAMETER_MP4_IGNORE_EDIT_LISTS:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARAMETER_MP4_IGNORE_TFDT_BOX:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARAMETER_MP4_TREAT_VIDEO_FRAMES_AS_KEYFRAMES:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARAMETER_MATROSKA_DISABLE_CUES_SEEKING:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARAMETER_MP3_DISABLE_ID3:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARAMETER_MP3_ENABLE_CBR_SEEKING:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARAMETER_MP3_ENABLE_INDEX_SEEKING:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARAMETER_TS_MODE:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARAMETER_TS_ALLOW_NON_IDR_AVC_KEYFRAMES:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARAMETER_TS_IGNORE_AAC_STREAM:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARAMETER_TS_IGNORE_AVC_STREAM:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARAMETER_TS_IGNORE_SPLICE_INFO_STREAM:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARAMETER_TS_DETECT_ACCESS_UNITS:kotlin.String` - `https://developer.android.com/reference/kotlin/android/media/MediaParser#PARAMETER_TS_ENABLE_HDMV_DTS_AUDIO_STREAMS:kotlin.String` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Whether the given `parameterName` is supported. |
