Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MediaFormat

```
class MediaFormat
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.MediaFormat](MediaFormat.md) |

Encapsulates the information describing the format of media data, be it audio or video, as well as optional feature metadata.

The format of the media data is specified as key/value pairs. Keys are strings. Values can be integer, long, float, String or ByteBuffer.

The feature metadata is specified as string/boolean pairs.

Keys common to all audio/video formats, **all keys not marked optional are mandatory**:

| Name | Value Type | Description |
|---|---|---|
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_MIME:kotlin.String` | String | The type of the format. |
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_CODECS_STRING:kotlin.String` | String | optional, the RFC 6381 codecs string of the MediaFormat |
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_MAX_INPUT_SIZE:kotlin.String` | Integer | optional, maximum size of a buffer of input data |
| --- | --- | --- |
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_PIXEL_ASPECT_RATIO_WIDTH:kotlin.String` | Integer | optional, the pixel aspect ratio width |
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_PIXEL_ASPECT_RATIO_HEIGHT:kotlin.String` | Integer | optional, the pixel aspect ratio height |
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_BIT_RATE:kotlin.String` | Integer | **encoder-only**, desired bitrate in bits/second |
| --- | --- | --- |
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_DURATION:kotlin.String` | long | the duration of the content (in microseconds) |
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_I_FRAME_INTERVAL:kotlin.String` | Integer (or Float) | **encoder-only** , optional for audio encoders, time-interval between key frames. Float support added in `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#N_MR1:kotlin.Int` |

Video formats have the following keys:

| Name | Value Type | Description |
|---|---|---|
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_WIDTH:kotlin.String` | Integer | |
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_HEIGHT:kotlin.String` | Integer | |
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_COLOR_FORMAT:kotlin.String` | Integer | set by the user for encoders, readable in the output format of decoders |
| --- | --- | --- |
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_FRAME_RATE:kotlin.String` | Integer or Float | required for **encoders** , optional for **decoders** |
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_CAPTURE_RATE:kotlin.String` | Integer | |
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_INTRA_REFRESH_PERIOD:kotlin.String` | Integer | **encoder-only**, optional |
| --- | --- | --- |
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_LATENCY:kotlin.String` | Integer | **encoder-only**, optional |
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_MAX_WIDTH:kotlin.String` | Integer | **decoder-only**, optional, max-resolution width |
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_MAX_HEIGHT:kotlin.String` | Integer | **decoder-only**, optional, max-resolution height |
| --- | --- | --- |
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_REPEAT_PREVIOUS_FRAME_AFTER:kotlin.String` | Long | **encoder in surface-mode only**, optional |
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_PUSH_BLANK_BUFFERS_ON_STOP:kotlin.String` | Integer(1) | **decoder rendering to a surface only**, optional |
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_TEMPORAL_LAYERING:kotlin.String` | String | **encoder only**, optional, temporal-layering schema |
| --- | --- | --- |
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_VIDEO_BITRATE_LAYERING:kotlin.String` | String | **encoder only**, optional, layering bitrate ratios |
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_TEMPORAL_LAYER_ID:kotlin.String` | String | **encoder only**, optional, temporal layer id |
| KEY_HORIZONTAL_FLIP | Integer | , optional, Set to true to horizontally flip the content |
| --- | --- | --- |

Specify both `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_MAX_WIDTH:kotlin.String` and `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_MAX_HEIGHT:kotlin.String` to enable adaptive playback (seamless resolution change) for a video decoder that supports it (`https://developer.android.com/reference/kotlin/android/media/MediaCodecInfo.CodecCapabilities#FEATURE_AdaptivePlayback:kotlin.String`). The values are used as hints for the codec: they are the maximum expected resolution to prepare for. Depending on codec support, preparing for larger maximum resolution may require more memory even if that resolution is never reached. These fields have no effect for codecs that do not support adaptive playback. 

Audio formats have the following keys:

| Name | Value Type | Description |
|---|---|---|
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_CHANNEL_COUNT:kotlin.String` | Integer | |
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_SAMPLE_RATE:kotlin.String` | Integer | |
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_PCM_ENCODING:kotlin.String` | Integer | optional |
| --- | --- | --- |
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_IS_ADTS:kotlin.String` | Integer | optional, if *decoding* AAC audio content, setting this key to 1 indicates that each audio frame is prefixed by the ADTS header. |
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_AAC_PROFILE:kotlin.String` | Integer | **encoder-only**, optional, if content is AAC audio, specifies the desired profile. |
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_AAC_SBR_MODE:kotlin.String` | Integer | **encoder-only**, optional, if content is AAC audio, specifies the desired SBR mode. |
| --- | --- | --- |
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_AAC_DRC_TARGET_REFERENCE_LEVEL:kotlin.String` | Integer | **decoder-only**, optional, if content is AAC audio, specifies the target reference level. |
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_AAC_ENCODED_TARGET_LEVEL:kotlin.String` | Integer | **decoder-only**, optional, if content is AAC audio, specifies the target reference level used at encoder. |
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_AAC_DRC_BOOST_FACTOR:kotlin.String` | Integer | **decoder-only**, optional, if content is AAC audio, specifies the DRC boost factor. |
| --- | --- | --- |
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_AAC_DRC_ATTENUATION_FACTOR:kotlin.String` | Integer | **decoder-only**, optional, if content is AAC audio, specifies the DRC attenuation factor. |
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_AAC_DRC_HEAVY_COMPRESSION:kotlin.String` | Integer | **decoder-only**, optional, if content is AAC audio, specifies whether to use heavy compression. |
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_AAC_MAX_OUTPUT_CHANNEL_COUNT:kotlin.String` | Integer | **decoder-only**, optional, if content is AAC audio, specifies the maximum number of channels the decoder outputs. |
| --- | --- | --- |
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_AAC_DRC_EFFECT_TYPE:kotlin.String` | Integer | **decoder-only**, optional, if content is AAC audio, specifies the MPEG-D DRC effect type to use. |
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_AAC_DRC_OUTPUT_LOUDNESS:kotlin.String` | Integer | **decoder-only**, optional, if content is AAC audio, returns the DRC output loudness. |
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_AAC_DRC_ALBUM_MODE:kotlin.String` | Integer | **decoder-only**, optional, if content is AAC audio, specifies the whether MPEG-D DRC Album Mode is active or not. |
| --- | --- | --- |
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_CHANNEL_MASK:kotlin.String` | Integer | optional, a mask of audio channel assignments |
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_ENCODER_DELAY:kotlin.String` | Integer | optional, the number of frames to trim from the start of the decoded audio stream. |
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_ENCODER_PADDING:kotlin.String` | Integer | optional, the number of frames to trim from the end of the decoded audio stream. |
| --- | --- | --- |
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_FLAC_COMPRESSION_LEVEL:kotlin.String` | Integer | **encoder-only**, optional, if content is FLAC audio, specifies the desired compression level. |
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_MPEGH_PROFILE_LEVEL_INDICATION:kotlin.String` | Integer | **decoder-only**, optional, if content is MPEG-H audio, specifies the profile and level of the stream. |
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_MPEGH_COMPATIBLE_SETS:kotlin.String` | ByteBuffer | **decoder-only**, optional, if content is MPEG-H audio, specifies the compatible sets (profile and level) of the stream. |
| --- | --- | --- |
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_MPEGH_REFERENCE_CHANNEL_LAYOUT:kotlin.String` | Integer | **decoder-only**, optional, if content is MPEG-H audio, specifies the preferred reference channel layout of the stream. |
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_BUFFER_BATCH_MAX_OUTPUT_SIZE:kotlin.String` | Integer | optional, used with large audio frame support, specifies max size of output buffer in bytes. |
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_BUFFER_BATCH_THRESHOLD_OUTPUT_SIZE:kotlin.String` | Integer | optional, used with large audio frame support, specifies threshold output size in bytes. |
| --- | --- | --- |
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_AUDIO_PRESENTATION_ID:kotlin.String` | long | optional, The ID of an AudioPresentation, MixPresentation, or similar audio decoder concept. |

Subtitle formats have the following keys:

| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_MIME:kotlin.String` | String | The type of the format. |
| --- | --- | --- |
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_LANGUAGE:kotlin.String` | String | The language of the content. |
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_CAPTION_SERVICE_NUMBER:kotlin.String` | int | optional, the closed-caption service or channel number. |

Image formats have the following keys:

| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_MIME:kotlin.String` | String | The type of the format. |
| --- | --- | --- |
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_WIDTH:kotlin.String` | Integer | |
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_HEIGHT:kotlin.String` | Integer | |
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_COLOR_FORMAT:kotlin.String` | Integer | set by the user for encoders, readable in the output format of decoders |
| --- | --- | --- |
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_TILE_WIDTH:kotlin.String` | Integer | required if the image has grid |
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_TILE_HEIGHT:kotlin.String` | Integer | required if the image has grid |
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_GRID_ROWS:kotlin.String` | Integer | required if the image has grid |
| --- | --- | --- |
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_GRID_COLUMNS:kotlin.String` | Integer | required if the image has grid |

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/media/MediaFormat.QpOffsetRect` QpOffsetRect constitutes the metadata required for encoding a region of interest in an image or a video frame. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#COLOR_RANGE_FULL:kotlin.Int` Full range. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#COLOR_RANGE_LIMITED:kotlin.Int` Limited range. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#COLOR_STANDARD_BT2020:kotlin.Int` BT. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#COLOR_STANDARD_BT601_NTSC:kotlin.Int` BT. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#COLOR_STANDARD_BT601_PAL:kotlin.Int` BT. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#COLOR_STANDARD_BT709:kotlin.Int` BT. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#COLOR_TRANSFER_HLG:kotlin.Int` ARIB STD-B67 hybrid-log-gamma transfer function. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#COLOR_TRANSFER_LINEAR:kotlin.Int` Linear transfer characteristic curve. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#COLOR_TRANSFER_SDR_VIDEO:kotlin.Int` SMPTE 170M transfer characteristic curve used by BT. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#COLOR_TRANSFER_ST2084:kotlin.Int` SMPTE ST 2084 transfer function. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#FLAG_SECURITY_MODEL_MEMORY_SAFE:kotlin.Int` Flag for `https://developer.android.com/reference/kotlin/android/media/MediaCodecInfo#SECURITY_MODEL_MEMORY_SAFE:kotlin.Int`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#FLAG_SECURITY_MODEL_SANDBOXED:kotlin.Int` Flag for `https://developer.android.com/reference/kotlin/android/media/MediaCodecInfo#SECURITY_MODEL_SANDBOXED:kotlin.Int`. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_AAC_DRC_ALBUM_MODE:kotlin.String` A key describing the album mode for MPEG-D DRC as defined in ISO/IEC 23003-4. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_AAC_DRC_ATTENUATION_FACTOR:kotlin.String` A key describing the attenuation factor allowing to adapt the dynamics of the output to the actual listening requirements. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_AAC_DRC_BOOST_FACTOR:kotlin.String` A key describing the boost factor allowing to adapt the dynamics of the output to the actual listening requirements. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_AAC_DRC_EFFECT_TYPE:kotlin.String` A key describing for selecting the DRC effect type for MPEG-D DRC. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_AAC_DRC_HEAVY_COMPRESSION:kotlin.String` A key describing the selection of the heavy compression profile for MPEG-4 DRC. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_AAC_DRC_OUTPUT_LOUDNESS:kotlin.String` A key to retrieve the output loudness of a decoded bitstream. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_AAC_DRC_TARGET_REFERENCE_LEVEL:kotlin.String` A key describing the Target Reference Level (Target Loudness). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_AAC_ENCODED_TARGET_LEVEL:kotlin.String` A key describing the target reference level that was assumed at the encoder for calculation of attenuation gains for clipping prevention. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_AAC_MAX_OUTPUT_CHANNEL_COUNT:kotlin.String` A key describing the maximum number of channels that can be output by the AAC decoder. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_AAC_PROFILE:kotlin.String` A key describing the AAC profile to be used (AAC audio formats only). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_AAC_SBR_MODE:kotlin.String` A key describing the AAC SBR mode to be used (AAC audio formats only). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_ALLOW_FRAME_DROP:kotlin.String` A key for applications to opt out of allowing a Surface to discard undisplayed/unconsumed frames as means to catch up after falling behind. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_AUDIO_PRESENTATION_ID:kotlin.String` A key identifying an audio or mix presentation or similar concept. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_AUDIO_SESSION_ID:kotlin.String` A key describing the audio session ID of the AudioTrack associated to a tunneled video codec. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_BITRATE_MODE:kotlin.String` A key describing the desired bitrate mode to be used by an encoder. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_BIT_RATE:kotlin.String` A key describing the average bitrate in bits/sec. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_BUFFER_BATCH_MAX_OUTPUT_SIZE:kotlin.String` A key describing the maximum output buffer size in bytes when using large buffer mode containing multiple access units. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_BUFFER_BATCH_THRESHOLD_OUTPUT_SIZE:kotlin.String` A key describing the threshold output size in bytes when using large buffer mode containing multiple access units. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_CAPTION_SERVICE_NUMBER:kotlin.String` A key describing the closed caption service number. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_CAPTURE_RATE:kotlin.String` A key describing the capture rate of a video format in frames/sec. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_CHANNEL_COUNT:kotlin.String` A key describing the number of channels in an audio format. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_CHANNEL_MASK:kotlin.String` A key describing the channel composition of audio content. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_CODECS_STRING:kotlin.String` A key describing the codecs string of the MediaFormat. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_COLOR_FORMAT:kotlin.String` A key describing the color format of the content in a video format. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_COLOR_RANGE:kotlin.String` An optional key describing the range of the component values of the video content. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_COLOR_STANDARD:kotlin.String` An optional key describing the color primaries, white point and luminance factors for video content. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_COLOR_TRANSFER:kotlin.String` An optional key describing the opto-electronic transfer function used for the video content. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_COLOR_TRANSFER_REQUEST:kotlin.String` An optional key describing the opto-electronic transfer function requested for the output video content. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_COMPLEXITY:kotlin.String` A key describing the encoding complexity. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_CREATE_INPUT_SURFACE_SUSPENDED:kotlin.String` If specified when configuring a video encoder that's in "surface-input" mode, it will instruct the encoder to put the surface source in suspended state when it's connected. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_CROP_BOTTOM:kotlin.String` A key describing the bottom-coordinate (y) of the crop rectangle. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_CROP_LEFT:kotlin.String` A key describing the left-coordinate (x) of the crop rectangle. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_CROP_RIGHT:kotlin.String` A key describing the right-coordinate (x) of the crop rectangle. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_CROP_TOP:kotlin.String` A key describing the top-coordinate (y) of the crop rectangle. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_DURATION:kotlin.String` A key describing the duration (in microseconds) of the content. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_ENCODER_DELAY:kotlin.String` A key describing the number of frames to trim from the start of the decoded audio stream. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_ENCODER_PADDING:kotlin.String` A key describing the number of frames to trim from the end of the decoded audio stream. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_FLAC_COMPRESSION_LEVEL:kotlin.String` A key describing the FLAC compression level to be used (FLAC audio format only). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_FRAME_RATE:kotlin.String` A key describing the frame rate of a video format in frames/sec. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_GRID_COLUMNS:kotlin.String` A key describing the number of grid columns in the content in a `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_IMAGE_ANDROID_HEIC:kotlin.String` / `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_IMAGE_AVIF:kotlin.String` track. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_GRID_ROWS:kotlin.String` A key describing the number of grid rows in the content in a `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_IMAGE_ANDROID_HEIC:kotlin.String` / `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_IMAGE_AVIF:kotlin.String` track. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_HAPTIC_CHANNEL_COUNT:kotlin.String` A key describing the number of haptic channels in an audio format. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_HARDWARE_AV_SYNC_ID:kotlin.String` A key describing the hardware AV sync id. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_HDR10_PLUS_INFO:kotlin.String` An optional key describing the HDR10+ metadata of the video content. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_HDR_ST2094_50_INFO:kotlin.String` An optional key describing the SMPTE ST 2094-50 metadata of the video content. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_HDR_STATIC_INFO:kotlin.String` An optional key describing the static metadata of HDR (high-dynamic-range) video content. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_HEIGHT:kotlin.String` A key describing the height of the content in a video format. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_IMPORTANCE:kotlin.String` A key describing the desired codec importance for the application. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_INTRA_REFRESH_PERIOD:kotlin.String` An optional key describing the period of intra refresh in frames. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_IS_ADTS:kotlin.String` A key mapping to a value of 1 if the content is AAC audio and audio frames are prefixed with an ADTS header. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_IS_AUTOSELECT:kotlin.String` A key for boolean AUTOSELECT behavior for the track. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_IS_DEFAULT:kotlin.String` A key for boolean DEFAULT behavior for the track. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_IS_FORCED_SUBTITLE:kotlin.String` A key for the FORCED field for subtitle tracks. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_I_FRAME_INTERVAL:kotlin.String` A key describing the frequency of key frames expressed in seconds between key frames. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_LANGUAGE:kotlin.String` A key describing the language of the content, using either ISO 639-1 or 639-2/T codes. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_LATENCY:kotlin.String` An optional key describing the desired encoder latency in frames. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_LEVEL:kotlin.String` A key describing the desired profile to be used by an encoder. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_LOW_LATENCY:kotlin.String` An optional key describing the low latency decoding mode. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_MAX_B_FRAMES:kotlin.String` A key describing the maximum number of B frames between I or P frames, to be used by a video encoder. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_MAX_FPS_TO_ENCODER:kotlin.String` Instruct the video encoder in "surface-input" mode to drop excessive frames from the source, so that the input frame rate to the encoder does not exceed the specified fps. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_MAX_HEIGHT:kotlin.String` A key describing the maximum expected height of the content in a video decoder format, in case there are resolution changes in the video content. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_MAX_INPUT_SIZE:kotlin.String` A key describing the maximum size in bytes of a buffer of data described by this MediaFormat. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_MAX_OUTPUT_CHANNEL_COUNT:kotlin.String` A key describing the maximum number of channels that can be output by an audio decoder. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_MAX_PTS_GAP_TO_ENCODER:kotlin.String` Instruct the video encoder in "surface-input" mode to limit the gap of timestamp between any two adjacent frames fed to the encoder to the specified amount (in micro-second). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_MAX_WIDTH:kotlin.String` A key describing the maximum expected width of the content in a video decoder format, in case there are resolution changes in the video content. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_MIME:kotlin.String` A key describing the mime type of the MediaFormat. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_MPEGH_COMPATIBLE_SETS:kotlin.String` A key describing the MPEG-H stream compatible sets. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_MPEGH_PROFILE_LEVEL_INDICATION:kotlin.String` A key describing the MPEG-H stream profile-level indication. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_MPEGH_REFERENCE_CHANNEL_LAYOUT:kotlin.String` A key describing the MPEG-H stream reference channel layout. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_NUM_SLOTS:kotlin.String` A key describing the number of slots used in the codec. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_OPERATING_RATE:kotlin.String` A key describing the desired operating frame rate for video or sample rate for audio that the codec will need to operate at. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_OUTPUT_REORDER_DEPTH:kotlin.String` An optional key describing the maximum number of non-display-order coded frames. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_PCM_ENCODING:kotlin.String` A key describing the raw audio sample encoding/format. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_PICTURE_PROFILE_ID:kotlin.String` A key describing the picture profile ID to be applied to `https://developer.android.com/reference/kotlin/android/media/MediaCodec`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_PICTURE_PROFILE_INSTANCE:kotlin.String` A key describing the picture profile instance to be applied to `https://developer.android.com/reference/kotlin/android/media/MediaCodec`. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_PICTURE_TYPE:kotlin.String` A key describing the picture type of the encoded frame. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_PIXEL_ASPECT_RATIO_HEIGHT:kotlin.String` A key describing the pixel aspect ratio height. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_PIXEL_ASPECT_RATIO_WIDTH:kotlin.String` A key describing the pixel aspect ratio width. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_PREPEND_HEADER_TO_SYNC_FRAMES:kotlin.String` An optional key describing whether encoders prepend headers to sync frames (e.g. SPS and PPS to IDR frames for H.264). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_PRIORITY:kotlin.String` A key describing the desired codec priority. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_PROFILE:kotlin.String` A key describing the desired profile to be used by an encoder. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_PUSH_BLANK_BUFFERS_ON_STOP:kotlin.String` If specified when configuring a video decoder rendering to a surface, causes the decoder to output "blank", i. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_QUALITY:kotlin.String` A key describing the desired encoding quality. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_REPEAT_PREVIOUS_FRAME_AFTER:kotlin.String` Applies only when configuring a video encoder in "surface-input" mode. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_ROTATION:kotlin.String` A key describing the desired clockwise rotation on an output surface. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_SAMPLE_RATE:kotlin.String` A key describing the sample rate of an audio format. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_SECURITY_MODEL:kotlin.String` A key describing the requested security model as flags. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_SLICE_HEIGHT:kotlin.String` A key describing the plane height of a multi-planar (YUV) video bytebuffer layout. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_SLOW_MOTION_MARKERS:kotlin.String` A key for retrieving the slow-motion marker information associated with a video track. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_STRIDE:kotlin.String` A key describing the stride of the video bytebuffer layout. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_TEMPORAL_LAYERING:kotlin.String` A key describing the temporal layering schema. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_TEMPORAL_LAYER_ID:kotlin.String` A key describing the index of the temporal layer of the output buffer. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_TILE_HEIGHT:kotlin.String` A key describing the height (in pixels) of each tile of the content in a `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_IMAGE_ANDROID_HEIC:kotlin.String` / `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_IMAGE_AVIF:kotlin.String` track. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_TILE_WIDTH:kotlin.String` A key describing the width (in pixels) of each tile of the content in a `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_IMAGE_ANDROID_HEIC:kotlin.String` / `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_IMAGE_AVIF:kotlin.String` track. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_TRACK_ID:kotlin.String` A key describing a unique ID for the content of a media track. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_VIDEO_BITRATE_LAYERING:kotlin.String` Set the bitrate distributions for temporal layering. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_VIDEO_ENCODING_STATISTICS_LEVEL:kotlin.String` A key describing the level of encoding statistics information emitted from video encoder. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_VIDEO_QP_AVERAGE:kotlin.String` A key describing the per-frame average block QP (Quantization Parameter). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_VIDEO_QP_B_MAX:kotlin.String` A key describing the maximum Quantization Parameter allowed for encoding video. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_VIDEO_QP_B_MIN:kotlin.String` A key describing the minimum Quantization Parameter allowed for encoding video. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_VIDEO_QP_I_MAX:kotlin.String` A key describing the maximum Quantization Parameter allowed for encoding video. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_VIDEO_QP_I_MIN:kotlin.String` A key describing the minimum Quantization Parameter allowed for encoding video. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_VIDEO_QP_MAX:kotlin.String` A key describing the maximum Quantization Parameter allowed for encoding video. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_VIDEO_QP_MIN:kotlin.String` A key describing the minimum Quantization Parameter allowed for encoding video. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_VIDEO_QP_P_MAX:kotlin.String` A key describing the maximum Quantization Parameter allowed for encoding video. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_VIDEO_QP_P_MIN:kotlin.String` A key describing the minimum Quantization Parameter allowed for encoding video. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_WIDTH:kotlin.String` A key describing the width of the content in a video format. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#LOG_SESSION_ID:kotlin.String` A key describing the log session ID for MediaCodec. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_AUDIO_AAC:kotlin.String` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_AUDIO_AAC_ELD:kotlin.String` MIME type for AAC Enhanced Low Delay (ELD) audio stream. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_AUDIO_AAC_HE_V1:kotlin.String` MIME type for HE-AAC v1 (LC + SBR) audio stream. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_AUDIO_AAC_HE_V2:kotlin.String` MIME type for HE-AAC v2 (LC + SBR + PS) audio stream. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_AUDIO_AAC_LC:kotlin.String` MIME type for AAC Low Complexity (LC) audio stream. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_AUDIO_AAC_XHE:kotlin.String` MIME type for AAC XHE audio stream. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_AUDIO_AC3:kotlin.String` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_AUDIO_AC4:kotlin.String` MIME type for AC-4 sync frame transport format audio stream. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_AUDIO_AMR_NB:kotlin.String` <br /> |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_AUDIO_AMR_WB:kotlin.String` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_AUDIO_DOLBY_MAT:kotlin.String` MIME type for Dolby Metadata-enhanced Audio Transmission (MAT) audio stream. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_AUDIO_DOLBY_TRUEHD:kotlin.String` MIME type for Dolby TrueHD audio format, based on Meridian Lossless Packing (MLP). |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_AUDIO_DRA:kotlin.String` MIME type for Dynamic Resolution Adaptation (DRA) audio stream. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_AUDIO_DTS:kotlin.String` MIME type for DTS Digital Surround (up to 5.1 channels) audio stream, aka DTS-CA. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_AUDIO_DTS_HD:kotlin.String` MIME type for DTS HD (up to 7.1 channels) audio stream. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_AUDIO_DTS_UHD:kotlin.String` MIME type for DTS UHD (object-based) audio stream, aka DTS:X. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_AUDIO_EAC3:kotlin.String` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_AUDIO_EAC3_JOC:kotlin.String` <br /> |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_AUDIO_FLAC:kotlin.String` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_AUDIO_G711_ALAW:kotlin.String` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_AUDIO_G711_MLAW:kotlin.String` <br /> |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_AUDIO_IAMF:kotlin.String` MIME type for IAMF audio stream |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_AUDIO_IEC61937:kotlin.String` MIME type for the IEC61937 audio stream encapsulation. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_AUDIO_MPEG:kotlin.String` <br /> |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_AUDIO_MPEGH_BL_L3:kotlin.String` MIME type for MPEG-H Baseline (BL) Profile L3 audio stream. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_AUDIO_MPEGH_BL_L4:kotlin.String` MIME type for MPEG-H Baseline (BL) Profile L4 audio stream. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_AUDIO_MPEGH_LC_L3:kotlin.String` MIME type for MPEG-H Low Complexity (LC) L3 audio stream. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_AUDIO_MPEGH_LC_L4:kotlin.String` MIME type for MPEG-H Low Complexity (LC) L4 audio stream. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_AUDIO_MPEGH_MHA1:kotlin.String` MIME type for MPEG-H Audio single stream |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_AUDIO_MPEGH_MHM1:kotlin.String` MIME type for MPEG-H Audio single stream, encapsulated in MHAS |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_AUDIO_MSGSM:kotlin.String` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_AUDIO_OPUS:kotlin.String` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_AUDIO_QCELP:kotlin.String` <br /> |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_AUDIO_RAW:kotlin.String` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_AUDIO_SCRAMBLED:kotlin.String` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_AUDIO_VORBIS:kotlin.String` <br /> |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_IMAGE_ANDROID_HEIC:kotlin.String` MIME type for HEIF still image data encoded in HEVC. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_IMAGE_AVIF:kotlin.String` MIME type for AVIF still image data encoded in AV1. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_TEXT_CEA_608:kotlin.String` MIME type for CEA-608 closed caption data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_TEXT_CEA_708:kotlin.String` MIME type for CEA-708 closed caption data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_TEXT_SUBRIP:kotlin.String` MIME type for SubRip (SRT) container. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_TEXT_VTT:kotlin.String` MIME type for WebVTT subtitle data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_VIDEO_APV:kotlin.String` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_VIDEO_AV1:kotlin.String` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_VIDEO_AVC:kotlin.String` <br /> |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_VIDEO_DOLBY_VISION:kotlin.String` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_VIDEO_H263:kotlin.String` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_VIDEO_HEVC:kotlin.String` <br /> |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_VIDEO_MPEG2:kotlin.String` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_VIDEO_MPEG4:kotlin.String` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_VIDEO_RAW:kotlin.String` <br /> |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_VIDEO_SCRAMBLED:kotlin.String` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_VIDEO_VP8:kotlin.String` <br /> |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_VIDEO_VP9:kotlin.String` <br /> |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_VIDEO_VVC:kotlin.String` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#PICTURE_TYPE_B:kotlin.Int` Picture Type is B Frame. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#PICTURE_TYPE_I:kotlin.Int` Picture Type is I Frame. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#PICTURE_TYPE_P:kotlin.Int` Picture Type is P Frame. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#PICTURE_TYPE_UNKNOWN:kotlin.Int` Picture Type is unknown. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#TYPE_BYTE_BUFFER:kotlin.Int` <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#TYPE_FLOAT:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#TYPE_INTEGER:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#TYPE_LONG:kotlin.Int` <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#TYPE_NULL:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#TYPE_STRING:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#VIDEO_ENCODING_STATISTICS_LEVEL_1:kotlin.Int` Encoding Statistics Level 1. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#VIDEO_ENCODING_STATISTICS_LEVEL_NONE:kotlin.Int` Encoding Statistics Level None. |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MediaFormat()()` Creates an empty MediaFormat |
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MediaFormat(android.media.MediaFormat)(other: https://developer.android.com/reference/kotlin/android/media/MediaFormat#)` Create a copy of a media format object. |

| Public methods ||
|---|---|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#containsFeature(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Returns true iff a feature of the given name exists in the format. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#containsKey(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Returns true iff a key of the given name exists in the format. |
| static [MediaFormat](MediaFormat.md) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#createAudioFormat(kotlin.String,%20kotlin.Int,%20kotlin.Int)(mime: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, sampleRate: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, channelCount: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Creates a minimal audio format. |
| --- | --- |
| static [MediaFormat](MediaFormat.md) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#createSubtitleFormat(kotlin.String,%20kotlin.String)(mime: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, language: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Creates a minimal subtitle format. |
| static [MediaFormat](MediaFormat.md) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#createVideoFormat(kotlin.String,%20kotlin.Int,%20kotlin.Int)(mime: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, width: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, height: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Creates a minimal video format. |
| [ByteBuffer](../java.nio/ByteBuffer.md)? | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#getByteBuffer(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Returns the value of a ByteBuffer key. |
| --- | --- |
| [ByteBuffer](../java.nio/ByteBuffer.md) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#getByteBuffer(kotlin.String,%20java.nio.ByteBuffer)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, defaultValue: https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)` Returns the value of a ByteBuffer key, or the default value if the key is missing. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#getFeatureEnabled(kotlin.String)(feature: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Returns whether a feature is to be enabled (`true`) or disabled (`false`). |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#getFeatures()()` Returns a `https://developer.android.com/reference/kotlin/java/util/Set.html#` view of the features contained in this MediaFormat. |
| --- | --- |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#getFloat(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Returns the value of a float key. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#getFloat(kotlin.String,%20kotlin.Float)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, defaultValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Returns the value of a float key, or the default value if the key is missing. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#getInteger(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Returns the value of an integer key. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#getInteger(kotlin.String,%20kotlin.Int)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, defaultValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the value of an integer key, or the default value if the key is missing. |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#getKeys()()` Returns a `https://developer.android.com/reference/kotlin/java/util/Set.html#` view of the keys contained in this MediaFormat. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#getLong(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Returns the value of a long key. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#getLong(kotlin.String,%20kotlin.Long)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, defaultValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns the value of a long key, or the default value if the key is missing. |
| [Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html)? | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#getNumber(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Returns the value of a numeric key. |
| [Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#getNumber(kotlin.String,%20kotlin.Number)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, defaultValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html)` Returns the value of a numeric key, or the default value if the key is missing. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#getString(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Returns the value of a string key. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#getString(kotlin.String,%20kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, defaultValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Returns the value of a string key, or the default value if the key is missing. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#getValueTypeForKey(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Returns the value type for a key. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#removeFeature(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Removes a given feature setting if present. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#removeKey(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Removes a value of a given key if present. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#setByteBuffer(kotlin.String,%20java.nio.ByteBuffer)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, bytes: https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#?)` Sets the value of a ByteBuffer key. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#setFeatureEnabled(kotlin.String,%20kotlin.Boolean)(feature: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, enabled: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets whether a feature is to be enabled (`true`) or disabled (`false`). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#setFloat(kotlin.String,%20kotlin.Float)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Sets the value of a float key. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#setInteger(kotlin.String,%20kotlin.Int)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the value of an integer key. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#setLong(kotlin.String,%20kotlin.Long)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Sets the value of a long key. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#setString(kotlin.String,%20kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Sets the value of a string key. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/MediaFormat#toString()()` Returns a string representation of the object. |
| --- | --- |

## Constants

### COLOR_RANGE_FULL

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val COLOR_RANGE_FULL: Int
```

Full range. Y, Cr and Cb component values range from 0 to 255 for 8-bit content.

 Value: 1

### COLOR_RANGE_LIMITED

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val COLOR_RANGE_LIMITED: Int
```

Limited range. Y component values range from 16 to 235 for 8-bit content. Cr, Cy values range from 16 to 240 for 8-bit content. This is the default for video content.

 Value: 2

### COLOR_STANDARD_BT2020

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val COLOR_STANDARD_BT2020: Int
```

BT.2020 color chromaticity coordinates with KR = 0.2627, KB = 0.0593.

 Value: 6

### COLOR_STANDARD_BT601_NTSC

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val COLOR_STANDARD_BT601_NTSC: Int
```

BT.601 525 color chromaticity coordinates with KR = 0.299, KB = 0.114.

 Value: 4

### COLOR_STANDARD_BT601_PAL

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val COLOR_STANDARD_BT601_PAL: Int
```

BT.601 625 color chromaticity coordinates with KR = 0.299, KB = 0.114.

 Value: 2

### COLOR_STANDARD_BT709

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val COLOR_STANDARD_BT709: Int
```

BT.709 color chromaticity coordinates with KR = 0.2126, KB = 0.0722.

 Value: 1

### COLOR_TRANSFER_HLG

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val COLOR_TRANSFER_HLG: Int
```

ARIB STD-B67 hybrid-log-gamma transfer function. This is used by some HDR video content.

 Value: 7

### COLOR_TRANSFER_LINEAR

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val COLOR_TRANSFER_LINEAR: Int
```

Linear transfer characteristic curve.

 Value: 1

### COLOR_TRANSFER_SDR_VIDEO

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val COLOR_TRANSFER_SDR_VIDEO: Int
```

SMPTE 170M transfer characteristic curve used by BT.601/BT.709/BT.2020. This is the curve used by most non-HDR video content.

 Value: 3

### COLOR_TRANSFER_ST2084

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val COLOR_TRANSFER_ST2084: Int
```

SMPTE ST 2084 transfer function. This is used by some HDR video content.

 Value: 6

### FLAG_SECURITY_MODEL_MEMORY_SAFE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_SECURITY_MODEL_MEMORY_SAFE: Int
```

Flag for `https://developer.android.com/reference/kotlin/android/media/MediaCodecInfo#SECURITY_MODEL_MEMORY_SAFE:kotlin.Int`.

 Value: 2

### FLAG_SECURITY_MODEL_SANDBOXED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_SECURITY_MODEL_SANDBOXED: Int
```

Flag for `https://developer.android.com/reference/kotlin/android/media/MediaCodecInfo#SECURITY_MODEL_SANDBOXED:kotlin.Int`.

 Value: 1

### KEY_AAC_DRC_ALBUM_MODE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_AAC_DRC_ALBUM_MODE: String
```

A key describing the album mode for MPEG-D DRC as defined in ISO/IEC 23003-4.

The associated value is an integer and can be set to following values:

| Value | Album Mode |
| --- | --- |
| 0 | disabled |
| 1 | enabled |
|---|---|

Disabled album mode leads to application of gain sequences for fading in and out, if provided in the bitstream. Enabled album mode makes use of dedicated album loudness information, if provided in the bitstream.

The default value is 0 (album mode disabled).

This key is only used during decoding.

 Value: "aac-drc-album-mode"

### KEY_AAC_DRC_ATTENUATION_FACTOR

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_AAC_DRC_ATTENUATION_FACTOR: String
```

A key describing the attenuation factor allowing to adapt the dynamics of the output to the actual listening requirements. See `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_AAC_DRC_BOOST_FACTOR:kotlin.String` for a description of the role of this attenuation factor and the value range.

The default value is 127 (fully apply attenuation DRC gains).

This key is only used during decoding.

 Value: "aac-drc-cut-level"

### KEY_AAC_DRC_BOOST_FACTOR

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_AAC_DRC_BOOST_FACTOR: String
```

A key describing the boost factor allowing to adapt the dynamics of the output to the actual listening requirements. This relies on DRC gain sequences that can be transmitted in the encoded bitstream to be able to reduce the dynamics of the output signal upon request. This factor enables the user to select how much of the gains are applied.

Positive gains (boost) and negative gains (attenuation, see `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_AAC_DRC_ATTENUATION_FACTOR:kotlin.String`) can be controlled separately for a better match to different use-cases.

Typically, attenuation gains are sent for loud signal segments, and boost gains are sent for soft signal segments. If the output is listened to in a noisy environment, for example, the boost factor is used to enable the positive gains, i.e. to amplify soft signal segments beyond the noise floor. But for listening late at night, the attenuation factor is used to enable the negative gains, to prevent loud signal from surprising the listener. In applications which generally need a low dynamic range, both the boost factor and the attenuation factor are used in order to enable all DRC gains.

In order to prevent clipping, it is also recommended to apply the attenuation gains in case of a downmix and/or loudness normalization to high target reference levels.

Both the boost and the attenuation factor parameters are given as integer values between 0 and 127, representing the range of the factor of 0 (i.e. don't apply) to 1 (i.e. fully apply boost/attenuation gains respectively).

The default value is 127 (fully apply boost DRC gains).

This key is only used during decoding.

 Value: "aac-drc-boost-level"

### KEY_AAC_DRC_EFFECT_TYPE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_AAC_DRC_EFFECT_TYPE: String
```

A key describing for selecting the DRC effect type for MPEG-D DRC. The supported values are defined in ISO/IEC 23003-4:2015 and are described as follows:

| Value | Effect |
| --- | --- |
| -1 | Off |
| 0 | None |
| 1 | Late night |
| --- | --- |
| 2 | Noisy environment |
| 3 | Limited playback range |
| 4 | Low playback level |
| --- | --- |
| 5 | Dialog enhancement |
| 6 | General compression |
|---|---|

<br />

The value -1 (Off) disables DRC processing, while loudness normalization may still be active and dependent on `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_AAC_DRC_TARGET_REFERENCE_LEVEL:kotlin.String`. 
The value 0 (None) automatically enables DRC processing if necessary to prevent signal clipping 
The value 6 (General compression) can be used for enabling MPEG-D DRC without particular DRC effect type request. 
The default DRC effect type is 3 ("Limited playback range") on mobile devices.

This key is only used during decoding.

 Value: "aac-drc-effect-type"

### KEY_AAC_DRC_HEAVY_COMPRESSION

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_AAC_DRC_HEAVY_COMPRESSION: String
```

A key describing the selection of the heavy compression profile for MPEG-4 DRC.

Two separate DRC gain sequences can be transmitted in one bitstream: light compression and heavy compression. When selecting the application of the heavy compression, one of the sequences is selected:

- 0 enables light compression,
- 1 enables heavy compression instead.

Note that heavy compression doesn't offer the features of scaling of DRC gains (see `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_AAC_DRC_BOOST_FACTOR:kotlin.String` and `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_AAC_DRC_ATTENUATION_FACTOR:kotlin.String` for the boost and attenuation factors), and frequency-selective (multiband) DRC. Light compression usually contains clipping prevention for stereo downmixing while heavy compression, if additionally provided in the bitstream, is usually stronger, and contains clipping prevention for stereo and mono downmixing.

The default is 1 (heavy compression).

This key is only used during decoding.

 Value: "aac-drc-heavy-compression"

### KEY_AAC_DRC_OUTPUT_LOUDNESS

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_AAC_DRC_OUTPUT_LOUDNESS: String
```

A key to retrieve the output loudness of a decoded bitstream.

If loudness normalization is active, the value corresponds to the Target Reference Level (see `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_AAC_DRC_TARGET_REFERENCE_LEVEL:kotlin.String`). 
If loudness normalization is not active, the value corresponds to the loudness metadata given in the bitstream.

The value is retrieved with getInteger() and is given as an integer value between 0 and 231. It is calculated as -4 \* Output Loudness in LKFS. Therefore, it represents the range of 0 to -57.75 LKFS.

A value of -1 indicates that no loudness metadata is present in the bitstream.

Loudness metadata can originate from MPEG-4 DRC or MPEG-D DRC.

This key is only used during decoding.

 Value: "aac-drc-output-loudness"

### KEY_AAC_DRC_TARGET_REFERENCE_LEVEL

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_AAC_DRC_TARGET_REFERENCE_LEVEL: String
```

A key describing the Target Reference Level (Target Loudness).

For normalizing loudness across program items, a gain is applied to the audio output so that the output loudness matches the Target Reference Level. The gain is derived as the difference between the Target Reference Level and the Program Reference Level (Program Loudness). The latter can be given in the bitstream and indicates the actual loudness value of the program item.

The Target Reference Level controls loudness normalization for both MPEG-4 DRC and MPEG-D DRC.

The value is given as an integer value between 40 and 127, and is calculated as -4 \* Target Reference Level in LKFS. Therefore, it represents the range of -10 to -31.75 LKFS.

For MPEG-4 DRC, a value of -1 switches off loudness normalization and DRC processing.

For MPEG-D DRC, a value of -1 switches off loudness normalization only. For DRC processing options of MPEG-D DRC, see `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_AAC_DRC_EFFECT_TYPE:kotlin.String`

The default value on mobile devices is 64 (-16 LKFS).

This key is only used during decoding.

 Value: "aac-target-ref-level"

### KEY_AAC_ENCODED_TARGET_LEVEL

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_AAC_ENCODED_TARGET_LEVEL: String
```

A key describing the target reference level that was assumed at the encoder for calculation of attenuation gains for clipping prevention.

If it is known, this information can be provided as an integer value between 0 and 127, which is calculated as -4 \* Encoded Target Level in LKFS. If the Encoded Target Level is unknown, the value can be set to -1.

The default value is -1 (unknown).

The value is ignored when heavy compression (see `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_AAC_DRC_HEAVY_COMPRESSION:kotlin.String`) or MPEG-D DRC is used.

This key is only used during decoding.

 Value: "aac-encoded-target-level"

### KEY_AAC_MAX_OUTPUT_CHANNEL_COUNT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_AAC_MAX_OUTPUT_CHANNEL_COUNT: String
```

**Deprecated:** *Use the non-AAC-specific key `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_MAX_OUTPUT_CHANNEL_COUNT:kotlin.String` instead*

A key describing the maximum number of channels that can be output by the AAC decoder. By default, the decoder will output the same number of channels as present in the encoded stream, if supported. Set this value to limit the number of output channels, and use the downmix information in the stream, if available.

Values larger than the number of channels in the content to decode behave just like the actual channel count of the content (e.g. passing 99 for the decoding of 5.1 content will behave like using 6).

This key is only used during decoding.

 Value: "aac-max-output-channel_count"

### KEY_AAC_PROFILE

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_AAC_PROFILE: String
```

A key describing the AAC profile to be used (AAC audio formats only). Constants are declared in `https://developer.android.com/reference/kotlin/android/media/MediaCodecInfo.CodecProfileLevel`.

 Value: "aac-profile"

### KEY_AAC_SBR_MODE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_AAC_SBR_MODE: String
```

A key describing the AAC SBR mode to be used (AAC audio formats only). The associated value is an integer and can be set to following values:

- 0 - no SBR should be applied
- 1 - single rate SBR
- 2 - double rate SBR

Note: If this key is not defined the default SBR mode for the desired AAC profile will be used.

<br />

This key is only used during encoding.

 Value: "aac-sbr-mode"

### KEY_ALLOW_FRAME_DROP

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_ALLOW_FRAME_DROP: String
```

A key for applications to opt out of allowing a Surface to discard undisplayed/unconsumed frames as means to catch up after falling behind. This value is an integer. The value 0 indicates the surface is not allowed to drop frames. The value 1 indicates the surface is allowed to drop frames. `https://developer.android.com/reference/kotlin/android/media/MediaCodec` describes the semantics.

 Value: "allow-frame-drop"

### KEY_AUDIO_PRESENTATION_ID

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_AUDIO_PRESENTATION_ID: String
```

A key identifying an audio or mix presentation or similar concept.

For audio stream encodings and associated decoders that support the concept of different creator-defined mixes within a file, this key can be used to provide the decoder with the selected mix.

The associated value is a long.

<br />

 Value: "audio-presentation-id"

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/AudioPresentation`

### KEY_AUDIO_SESSION_ID

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_AUDIO_SESSION_ID: String
```

A key describing the audio session ID of the AudioTrack associated to a tunneled video codec. The associated value is an integer.

 Value: "audio-session-id"

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/MediaCodecInfo.CodecCapabilities#FEATURE_TunneledPlayback:kotlin.String`

### KEY_BITRATE_MODE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_BITRATE_MODE: String
```

A key describing the desired bitrate mode to be used by an encoder. Constants are declared in `https://developer.android.com/reference/kotlin/android/media/MediaCodecInfo.EncoderCapabilities`.

 Value: "bitrate-mode"

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/MediaCodecInfo.EncoderCapabilities#isBitrateModeSupported(kotlin.Int)`

### KEY_BIT_RATE

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_BIT_RATE: String
```

A key describing the average bitrate in bits/sec. The associated value is an integer

 Value: "bitrate"

### KEY_BUFFER_BATCH_MAX_OUTPUT_SIZE

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_BUFFER_BATCH_MAX_OUTPUT_SIZE: String
```

A key describing the maximum output buffer size in bytes when using large buffer mode containing multiple access units.

When not-set - codec functions with one access-unit per frame. When set less than the size of two access-units - will make codec operate in single access-unit per output frame. When set to a value too big - The component or the framework will override this value to a reasonable max size not exceeding typical 10 seconds of data (device dependent) when set to a value larger than that. The value final value used will be returned in the output format.

The associated value is an integer

 Value: "buffer-batch-max-output-size"

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/MediaCodecInfo.CodecCapabilities#FEATURE_MultipleFrames:kotlin.String`

### KEY_BUFFER_BATCH_THRESHOLD_OUTPUT_SIZE

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_BUFFER_BATCH_THRESHOLD_OUTPUT_SIZE: String
```

A key describing the threshold output size in bytes when using large buffer mode containing multiple access units.

This is an optional parameter.

If not set - the component can set this to a reasonable value. If set larger than max size, the components will clip this setting to maximum buffer batching output size.

The component will return a partial output buffer if the output buffer reaches or surpass this limit.

Threshold size should be always less or equal to `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_BUFFER_BATCH_MAX_OUTPUT_SIZE:kotlin.String`. The final setting of this value as determined by the component will be returned in the output format

The associated value is an integer

 Value: "buffer-batch-threshold-output-size"

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/MediaCodecInfo.CodecCapabilities#FEATURE_MultipleFrames:kotlin.String`

### KEY_CAPTION_SERVICE_NUMBER

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CAPTION_SERVICE_NUMBER: String
```

A key describing the closed caption service number. For CEA-608 caption tracks, holds the channel number. For CEA-708, holds the service number. The associated value is an int.

 Value: "caption-service-number"

### KEY_CAPTURE_RATE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CAPTURE_RATE: String
```

A key describing the capture rate of a video format in frames/sec.

When capture rate is different than the frame rate, it means that the video is acquired at a different rate than the playback, which produces slow motion or timelapse effect during playback. Application can use the value of this key to set a capture rate that differs from the playback rate. If unspecified, the system uses the playback frame rate as the capture rate (e.g. normal speed).

However, Specifying capture rates that are nearly equal to the frame rate are at risk of causing frame drops and other visual artifacts in the output. To avoid such artifacts, the capture rate should be at least a factor of 2 away from the frame rate. `GraphicBufferSource#calculateCodecTimestamp_l`

The associated value is an integer or a float.

 Value: "capture-rate"

### KEY_CHANNEL_COUNT

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CHANNEL_COUNT: String
```

A key describing the number of channels in an audio format. The associated value is an integer

 Value: "channel-count"

### KEY_CHANNEL_MASK

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CHANNEL_MASK: String
```

A key describing the channel composition of audio content. This mask is composed of bits drawn from channel mask definitions in `https://developer.android.com/reference/kotlin/android/media/AudioFormat`. The associated value is an integer.

 Value: "channel-mask"

### KEY_CODECS_STRING

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CODECS_STRING: String
```

A key describing the codecs string of the MediaFormat. See RFC 6381 section 3.2 for the syntax of the value. The value does not hold `https://developer.android.com/reference/kotlin/android/media/MediaCodec`-exposed codec names. The associated value is a string.

 Value: "codecs-string"

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/MediaParser.TrackData#mediaFormat:android.media.MediaFormat`

### KEY_COLOR_FORMAT

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_COLOR_FORMAT: String
```

A key describing the color format of the content in a video format. Constants are declared in `https://developer.android.com/reference/kotlin/android/media/MediaCodecInfo.CodecCapabilities`.

 Value: "color-format"

### KEY_COLOR_RANGE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_COLOR_RANGE: String
```

An optional key describing the range of the component values of the video content. The associated value is an integer: 0 if unspecified, or one of the COLOR_RANGE_ values.

 Value: "color-range"

### KEY_COLOR_STANDARD

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_COLOR_STANDARD: String
```

An optional key describing the color primaries, white point and luminance factors for video content. The associated value is an integer: 0 if unspecified, or one of the COLOR_STANDARD_ values.

 Value: "color-standard"

### KEY_COLOR_TRANSFER

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_COLOR_TRANSFER: String
```

An optional key describing the opto-electronic transfer function used for the video content. The associated value is an integer: 0 if unspecified, or one of the COLOR_TRANSFER_ values.

 Value: "color-transfer"

### KEY_COLOR_TRANSFER_REQUEST

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_COLOR_TRANSFER_REQUEST: String
```

An optional key describing the opto-electronic transfer function requested for the output video content. The associated value is an integer: 0 if unspecified, or one of the COLOR_TRANSFER_ values. When unspecified the component will not touch the video content; otherwise the component will tone-map the raw video frame to match the requested transfer function. After configure, component's input format will contain this key to note whether the request is supported or not. If the value in the input format is the same as the requested value, the request is supported. The value is set to 0 if unsupported.

 Value: "color-transfer-request"

### KEY_COMPLEXITY

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_COMPLEXITY: String
```

A key describing the encoding complexity. The associated value is an integer. These values are device and codec specific, but lower values generally result in faster and/or less power-hungry encoding.

 Value: "complexity"

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/MediaCodecInfo.EncoderCapabilities#getComplexityRange()`

### KEY_CREATE_INPUT_SURFACE_SUSPENDED

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CREATE_INPUT_SURFACE_SUSPENDED: String
```

If specified when configuring a video encoder that's in "surface-input" mode, it will instruct the encoder to put the surface source in suspended state when it's connected. No video frames will be accepted until a resume operation (see `https://developer.android.com/reference/kotlin/android/media/MediaCodec#PARAMETER_KEY_SUSPEND:kotlin.String`), optionally with timestamp specified via `https://developer.android.com/reference/kotlin/android/media/MediaCodec#PARAMETER_KEY_SUSPEND_TIME:kotlin.String`, is received. The value is an integer, with 1 indicating to create with the surface source suspended, or 0 otherwise. The default value is 0. If this key is not set or set to 0, the surface source will accept buffers as soon as it's connected to the encoder (although they may not be encoded immediately). This key can be used when the client wants to prepare the encoder session in advance, but do not want to accept buffers immediately.

 Value: "create-input-buffers-suspended"

### KEY_CROP_BOTTOM

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CROP_BOTTOM: String
```

A key describing the bottom-coordinate (y) of the crop rectangle. This is the bottom-most row included in the crop frame, where row indices start at 0. Additional information on the crop rectangle semantics can be found at `https://developer.android.com/reference/kotlin/android/media/MediaCodec`.

 Value: "crop-bottom"

### KEY_CROP_LEFT

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CROP_LEFT: String
```

A key describing the left-coordinate (x) of the crop rectangle. This is the left-most column included in the crop frame, where column indices start at 0. Additional information on the crop rectangle semantics can be found at `https://developer.android.com/reference/kotlin/android/media/MediaCodec`.

 Value: "crop-left"

### KEY_CROP_RIGHT

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CROP_RIGHT: String
```

A key describing the right-coordinate (x) of the crop rectangle. This is the right-most column included in the crop frame, where column indices start at 0. Additional information on the crop rectangle semantics can be found at `https://developer.android.com/reference/kotlin/android/media/MediaCodec`.

 Value: "crop-right"

### KEY_CROP_TOP

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_CROP_TOP: String
```

A key describing the top-coordinate (y) of the crop rectangle. This is the top-most row included in the crop frame, where row indices start at 0. Additional information on the crop rectangle semantics can be found at `https://developer.android.com/reference/kotlin/android/media/MediaCodec`.

 Value: "crop-top"

### KEY_DURATION

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_DURATION: String
```

A key describing the duration (in microseconds) of the content. The associated value is a long.

 Value: "durationUs"

### KEY_ENCODER_DELAY

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_ENCODER_DELAY: String
```

A key describing the number of frames to trim from the start of the decoded audio stream. The associated value is an integer.

 Value: "encoder-delay"

### KEY_ENCODER_PADDING

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_ENCODER_PADDING: String
```

A key describing the number of frames to trim from the end of the decoded audio stream. The associated value is an integer.

 Value: "encoder-padding"

### KEY_FLAC_COMPRESSION_LEVEL

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_FLAC_COMPRESSION_LEVEL: String
```

A key describing the FLAC compression level to be used (FLAC audio format only). The associated value is an integer ranging from 0 (fastest, least compression) to 8 (slowest, most compression).

 Value: "flac-compression-level"

### KEY_FRAME_RATE

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_FRAME_RATE: String
```

A key describing the frame rate of a video format in frames/sec.

The associated value is normally an integer when the value is used by the platform, but video codecs also accept float configuration values. Specifically, `https://developer.android.com/reference/kotlin/android/media/MediaExtractor#getTrackFormat(kotlin.Int)` provides an integer value corresponding to the frame rate information of the track if specified and non-zero. Otherwise, this key is not present. android.media.MediaCodec#configure accepts both float and integer values.

This represents the desired operating frame rate if the `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_OPERATING_RATE:kotlin.String` is not present and `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_PRIORITY:kotlin.String` is `0` (realtime). Otherwise, this is just informational.

For video encoders this value corresponds to the intended frame rate (the rate at which the application intends to send frames to the encoder, as calculated by the buffer timestamps, and not from the actual real-time rate that the frames are sent to the encoder). Encoders use this hint for rate control, specifically for the initial frames, as encoders are expected to support variable frame rate (for rate control) based on the actual `https://developer.android.com/reference/kotlin/android/media/MediaCodec.BufferInfo#presentationTimeUs:kotlin.Long` of subsequent frames.

This key is not used in the `MediaCodec` `https://developer.android.com/reference/kotlin/android/media/MediaCodec#getInputFormat()`/android.media.MediaCodec#getOutputFormat formats, nor by `https://developer.android.com/reference/kotlin/android/media/MediaMuxer#addTrack(android.media.MediaFormat)`.

 Value: "frame-rate"

### KEY_GRID_COLUMNS

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_GRID_COLUMNS: String
```

A key describing the number of grid columns in the content in a `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_IMAGE_ANDROID_HEIC:kotlin.String` / `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_IMAGE_AVIF:kotlin.String` track. The associated value is an integer. Refer to `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_IMAGE_ANDROID_HEIC:kotlin.String` / `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_IMAGE_AVIF:kotlin.String` on decoding instructions of such tracks.

 Value: "grid-cols"

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_TILE_WIDTH:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_TILE_HEIGHT:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_GRID_ROWS:kotlin.String`

### KEY_GRID_ROWS

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_GRID_ROWS: String
```

A key describing the number of grid rows in the content in a `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_IMAGE_ANDROID_HEIC:kotlin.String` / `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_IMAGE_AVIF:kotlin.String` track. The associated value is an integer. Refer to `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_IMAGE_ANDROID_HEIC:kotlin.String` / `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_IMAGE_AVIF:kotlin.String` on decoding instructions of such tracks.

 Value: "grid-rows"

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_TILE_WIDTH:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_TILE_HEIGHT:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_GRID_COLUMNS:kotlin.String`

### KEY_HAPTIC_CHANNEL_COUNT

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_HAPTIC_CHANNEL_COUNT: String
```

A key describing the number of haptic channels in an audio format. The associated value is an integer.

 Value: "haptic-channel-count"

### KEY_HARDWARE_AV_SYNC_ID

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_HARDWARE_AV_SYNC_ID: String
```

A key describing the hardware AV sync id. The associated value is an integer

 Value: "hw-av-sync-id"

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/MediaFormat#`

### KEY_HDR10_PLUS_INFO

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_HDR10_PLUS_INFO: String
```

An optional key describing the HDR10+ metadata of the video content. The associated value is a ByteBuffer containing HDR10+ metadata conforming to the user_data_registered_itu_t_t35() syntax of SEI message for ST 2094-40. This key will be present on:

- The formats of output buffers of a decoder configured for HDR10+ profiles (such as `https://developer.android.com/reference/kotlin/android/media/MediaCodecInfo.CodecProfileLevel#VP9Profile2HDR10Plus:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/MediaCodecInfo.CodecProfileLevel#VP9Profile3HDR10Plus:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/media/MediaCodecInfo.CodecProfileLevel#HEVCProfileMain10HDR10Plus:kotlin.Int`), or

- The formats of output buffers of an encoder configured for an HDR10+ profiles that uses out-of-band metadata (such as `https://developer.android.com/reference/kotlin/android/media/MediaCodecInfo.CodecProfileLevel#VP9Profile2HDR10Plus:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/media/MediaCodecInfo.CodecProfileLevel#VP9Profile3HDR10Plus:kotlin.Int`).

 Value: "hdr10-plus-info"

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/MediaCodec#PARAMETER_KEY_HDR10_PLUS_INFO:kotlin.String`

### KEY_HDR_ST2094_50_INFO

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_HDR_ST2094_50_INFO: String
```

An optional key describing the SMPTE ST 2094-50 metadata of the video content. The associated value is a ByteBuffer containing the user_data_payload segment of an ITU-T T.35 SEI message, specifically for SMPTE ST 2094-50. The buffer's contents must conform to the syntax defined in SMPTE ST 2094-50, and must not include the initial 5-byte ITU-T T.35 header.

 Value: "hdr-st2094-50-info"

### KEY_HDR_STATIC_INFO

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_HDR_STATIC_INFO: String
```

An optional key describing the static metadata of HDR (high-dynamic-range) video content. The associated value is a ByteBuffer. This buffer contains the raw contents of the Static Metadata Descriptor (including the descriptor ID) of an HDMI Dynamic Range and Mastering InfoFrame as defined by CTA-861.3. This key must be provided to video decoders for HDR video content unless this information is contained in the bitstream and the video decoder supports an HDR-capable profile. This key must be provided to video encoders for HDR video content.

 Value: "hdr-static-info"

### KEY_HEIGHT

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_HEIGHT: String
```

A key describing the height of the content in a video format. The associated value is an integer

 Value: "height"

### KEY_IMPORTANCE

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_IMPORTANCE: String
```

A key describing the desired codec importance for the application.

The associated value is a positive integer including zero. Higher value means lesser importance.

The resource manager may use the codec importance, along with other factors when reclaiming codecs from an application. The specifics of reclaim policy is device dependent, but specifying the codec importance, will allow the resource manager to prioritize reclaiming less important codecs (assigned higher values) from the (reclaim) requesting application first. So, the codec importance is only relevant within the context of that application.

The codec importance can be set:

- through android.media.MediaCodec#configure.
- through `https://developer.android.com/reference/kotlin/android/media/MediaCodec#setParameters(android.os.Bundle)` if the codec has been configured already, which allows the users to change the codec importance multiple times.

Any change/update in codec importance is guaranteed upon the completion of the function call that sets the codec importance. So, in case of concurrent codec operations, make sure to wait for the change in codec importance, before using another codec. Note that unless specified, by default the codecs will have highest importance (of value 0).

 Value: "importance"

### KEY_INTRA_REFRESH_PERIOD

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_INTRA_REFRESH_PERIOD: String
```

An optional key describing the period of intra refresh in frames. This is an optional parameter that applies only to video encoders. If encoder supports it (`https://developer.android.com/reference/kotlin/android/media/MediaCodecInfo.CodecCapabilities#FEATURE_IntraRefresh:kotlin.String`), the whole frame is completely refreshed after the specified period. Also for each frame, a fix subset of macroblocks must be intra coded which leads to more constant bitrate than inserting a key frame. This key is recommended for video streaming applications as it provides low-delay and good error-resilience. This key is ignored if the video encoder does not support the intra refresh feature. Use the output format to verify that this feature was enabled. The associated value is an integer.

 Value: "intra-refresh-period"

### KEY_IS_ADTS

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_IS_ADTS: String
```

A key mapping to a value of 1 if the content is AAC audio and audio frames are prefixed with an ADTS header. The associated value is an integer (0 or 1). This key is only supported when _decoding_ content, it cannot be used to configure an encoder to emit ADTS output.

 Value: "is-adts"

### KEY_IS_AUTOSELECT

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_IS_AUTOSELECT: String
```

A key for boolean AUTOSELECT behavior for the track. Tracks with AUTOSELECT=true are considered when automatically selecting a track without specific user choice, based on the current locale. This is currently only used for subtitle tracks, when the user selected 'Default' for the captioning locale. The associated value is an integer, where non-0 means TRUE. This is an optional field; if not specified, AUTOSELECT defaults to TRUE.

 Value: "is-autoselect"

### KEY_IS_DEFAULT

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_IS_DEFAULT: String
```

A key for boolean DEFAULT behavior for the track. The track with DEFAULT=true is selected in the absence of a specific user choice. This is currently used in two scenarios: 1) for subtitle tracks, when the user selected 'Default' for the captioning locale. 2) for a `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_IMAGE_ANDROID_HEIC:kotlin.String` / `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_IMAGE_AVIF:kotlin.String` track, indicating the image is the primary item in the file. The associated value is an integer, where non-0 means TRUE. This is an optional field; if not specified, DEFAULT is considered to be FALSE.

 Value: "is-default"

### KEY_IS_FORCED_SUBTITLE

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_IS_FORCED_SUBTITLE: String
```

A key for the FORCED field for subtitle tracks. True if it is a forced subtitle track. Forced subtitle tracks are essential for the content and are shown even when the user turns off Captions. They are used for example to translate foreign/alien dialogs or signs. The associated value is an integer, where non-0 means TRUE. This is an optional field; if not specified, FORCED defaults to FALSE.

 Value: "is-forced-subtitle"

### KEY_I_FRAME_INTERVAL

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_I_FRAME_INTERVAL: String
```

A key describing the frequency of key frames expressed in seconds between key frames.

This key is used by encoders. A negative value means no key frames are requested after the first frame. A zero value means a stream containing all key frames is requested.

Most encoders will convert this value of the number of non-key-frames between key-frames, using the [frame rate](MediaFormat.md) information; therefore, if the actual frame rate differs (e.g. input frames are dropped or the frame rate changes), the **time interval** between key frames will not be the configured value.

The associated value is an integer (or float since `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#N_MR1:kotlin.Int`).

 Value: "i-frame-interval"

### KEY_LANGUAGE

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_LANGUAGE: String
```

A key describing the language of the content, using either ISO 639-1 or 639-2/T codes. The associated value is a string.

 Value: "language"

### KEY_LATENCY

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_LATENCY: String
```

An optional key describing the desired encoder latency in frames. This is an optional parameter that applies only to video encoders. If encoder supports it, it should output at least one output frame after being queued the specified number of frames. This key is ignored if the video encoder does not support the latency feature. Use the output format to verify that this feature was enabled and the actual value used by the encoder.

If the key is not specified, the default latency will be implementation specific. The associated value is an integer.

 Value: "latency"

### KEY_LEVEL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_LEVEL: String
```

A key describing the desired profile to be used by an encoder.

The associated value is an integer. Constants are declared in `https://developer.android.com/reference/kotlin/android/media/MediaCodecInfo.CodecProfileLevel`. This key is used as a further hint when specifying a desired profile, and is only supported for codecs that specify a level.

This key is ignored if the `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_PROFILE:kotlin.String` is not specified. Otherwise, the value should be a level compatible with the configured encoding parameters.

**Note:** This key cannot be used to constrain the encoder's output to a maximum encoding level. Encoders are free to target a different level if the configured encoding parameters dictate it. Nevertheless, encoders shall use (and encode) a level sufficient to decode the generated bitstream, though they may exceed the (Video) Buffering Verifier limits for that encoded level.

 Value: "level"

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/MediaCodecInfo.CodecCapabilities#profileLevels:kotlin.Array`

### KEY_LOW_LATENCY

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_LOW_LATENCY: String
```

An optional key describing the low latency decoding mode. This is an optional parameter that applies only to decoders. If enabled, the decoder doesn't hold input and output data more than required by the codec standards. The associated value is an integer (0 or 1): 1 when low-latency decoding is enabled, 0 otherwise. The default value is 0.

 Value: "low-latency"

### KEY_MAX_B_FRAMES

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_MAX_B_FRAMES: String
```

A key describing the maximum number of B frames between I or P frames, to be used by a video encoder. The associated value is an integer. The default value is 0, which means that no B frames are allowed. Note that non-zero value does not guarantee B frames; it's up to the encoder to decide.

 Value: "max-bframes"

### KEY_MAX_FPS_TO_ENCODER

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_MAX_FPS_TO_ENCODER: String
```

Instruct the video encoder in "surface-input" mode to drop excessive frames from the source, so that the input frame rate to the encoder does not exceed the specified fps. The associated value is a float, representing the max frame rate to feed the encoder at.

 Value: "max-fps-to-encoder"

### KEY_MAX_HEIGHT

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_MAX_HEIGHT: String
```

A key describing the maximum expected height of the content in a video decoder format, in case there are resolution changes in the video content. The associated value is an integer

 Value: "max-height"

### KEY_MAX_INPUT_SIZE

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_MAX_INPUT_SIZE: String
```

A key describing the maximum size in bytes of a buffer of data described by this MediaFormat. The associated value is an integer

 Value: "max-input-size"

### KEY_MAX_OUTPUT_CHANNEL_COUNT

Added in [API level 32](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_MAX_OUTPUT_CHANNEL_COUNT: String
```

A key describing the maximum number of channels that can be output by an audio decoder. By default, the decoder will output the same number of channels as present in the encoded stream, if supported. Set this value to limit the number of output channels, and use the downmix information in the stream, if available.

Values larger than the number of channels in the content to decode behave like the number of channels in the content (if applicable), for instance passing 99 for a 5.1 audio stream behaves like passing 6.

This key is only used during decoding.

 Value: "max-output-channel-count"

### KEY_MAX_PTS_GAP_TO_ENCODER

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_MAX_PTS_GAP_TO_ENCODER: String
```

Instruct the video encoder in "surface-input" mode to limit the gap of timestamp between any two adjacent frames fed to the encoder to the specified amount (in micro-second). The associated value is a long int. When positive, it represents the max timestamp gap between two adjacent frames fed to the encoder. When negative, the absolute value represents a fixed timestamp gap between any two adjacent frames fed to the encoder. Note that this will also apply even when the original timestamp goes backward in time. Under normal conditions, such frames would be dropped and not sent to the encoder. The output timestamp will be restored to the original timestamp and will not be affected. This is used in some special scenarios where input frames arrive sparingly but it's undesirable to allocate more bits to any single frame, or when it's important to ensure all frames are captured (rather than captured in the correct order).

 Value: "max-pts-gap-to-encoder"

### KEY_MAX_WIDTH

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_MAX_WIDTH: String
```

A key describing the maximum expected width of the content in a video decoder format, in case there are resolution changes in the video content. The associated value is an integer

 Value: "max-width"

### KEY_MIME

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_MIME: String
```

A key describing the mime type of the MediaFormat. The associated value is a string.

 Value: "mime"

### KEY_MPEGH_COMPATIBLE_SETS

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_MPEGH_COMPATIBLE_SETS: String
```

A key describing the MPEG-H stream compatible sets. See FDAmd_2 of ISO_IEC_23008-3;2019 MHAProfileAndLevelCompatibilitySetBox.

 Value: "mpegh-compatible-sets"

### KEY_MPEGH_PROFILE_LEVEL_INDICATION

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_MPEGH_PROFILE_LEVEL_INDICATION: String
```

A key describing the MPEG-H stream profile-level indication. See ISO_IEC_23008-3;2019 MHADecoderConfigurationRecord mpegh3daProfileLevelIndication.

 Value: "mpegh-profile-level-indication"

### KEY_MPEGH_REFERENCE_CHANNEL_LAYOUT

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_MPEGH_REFERENCE_CHANNEL_LAYOUT: String
```

A key describing the MPEG-H stream reference channel layout. See ISO_IEC_23008-3;2019 MHADecoderConfigurationRecord referenceChannelLayout and ISO_IEC_23001‐8 ChannelConfiguration value.

 Value: "mpegh-reference-channel-layout"

### KEY_NUM_SLOTS

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_NUM_SLOTS: String
```

A key describing the number of slots used in the codec. When present in input format, the associated value indicates the number of input slots. The entry is set by the codec if configured with (@link MediaCodec#CONFIGURE_FLAG_BLOCK_MODEL), and will be ignored if set by the application.

The associated value is an integer.

 Value: "num-slots"

### KEY_OPERATING_RATE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_OPERATING_RATE: String
```

A key describing the desired operating frame rate for video or sample rate for audio that the codec will need to operate at.

The associated value is an integer or a float representing frames-per-second or samples-per-second

This is used for cases like high-speed/slow-motion video capture, where the video encoder format contains the target playback rate (e.g. 30fps), but the component must be able to handle the high operating capture rate (e.g. 240fps).

This rate will be used by codec for resource planning and setting the operating points.

 Value: "operating-rate"

### KEY_OUTPUT_REORDER_DEPTH

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_OUTPUT_REORDER_DEPTH: String
```

An optional key describing the maximum number of non-display-order coded frames. This is an optional parameter that applies only to video encoders. Application should check the value for this key in the output format to see if codec will produce non-display-order coded frames. If encoder supports it, the output frames' order will be different from the display order and each frame's display order could be retrived from `https://developer.android.com/reference/kotlin/android/media/MediaCodec.BufferInfo#presentationTimeUs:kotlin.Long`. Before API level 27, application may receive non-display-order coded frames even though the application did not request it. Note: Application should not rearrange the frames to display order before feeding them to `https://developer.android.com/reference/kotlin/android/media/MediaMuxer#writeSampleData(kotlin.Int,%20java.nio.ByteBuffer,%20android.media.MediaCodec.BufferInfo)`.

The default value is 0.

 Value: "output-reorder-depth"

### KEY_PCM_ENCODING

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_PCM_ENCODING: String
```

A key describing the raw audio sample encoding/format.

The associated value is an integer, using one of the `https://developer.android.com/reference/kotlin/android/media/AudioFormat`.ENCODING_PCM_ values.

This is an optional key for audio decoders and encoders specifying the desired raw audio sample format during android.media.MediaCodec#configure call. Use `https://developer.android.com/reference/kotlin/android/media/MediaCodec#getInputFormat()`/android.media.MediaCodec#getOutputFormat to confirm the actual format. For the PCM decoder this key specifies both input and output sample encodings.

This key is also used by `https://developer.android.com/reference/kotlin/android/media/MediaExtractor` to specify the sample format of audio data, if it is specified.

If this key is missing, the raw audio sample format is signed 16-bit short.

 Value: "pcm-encoding"

### KEY_PICTURE_PROFILE_ID

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_PICTURE_PROFILE_ID: String
```

A key describing the picture profile ID to be applied to `https://developer.android.com/reference/kotlin/android/media/MediaCodec`.

The associated value is a string.

<br />

 Value: "picture-profile-id"

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/quality/PictureProfile`
- `https://developer.android.com/reference/kotlin/android/media/quality/PictureProfile#getProfileId()`

### KEY_PICTURE_PROFILE_INSTANCE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_PICTURE_PROFILE_INSTANCE: String
```

A key describing the picture profile instance to be applied to `https://developer.android.com/reference/kotlin/android/media/MediaCodec`.

The associated value is an instance of `https://developer.android.com/reference/kotlin/android/media/quality/PictureProfile`.

<br />

 Value: "picture-profile-instance"

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/quality/PictureProfile`

### KEY_PICTURE_TYPE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_PICTURE_TYPE: String
```

A key describing the picture type of the encoded frame. This is a part of a video 'Encoding Statistics' export feature. This value is emitted from video encoder for a video frame. The associated value is an integer.

 Value: "picture-type"

### KEY_PIXEL_ASPECT_RATIO_HEIGHT

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_PIXEL_ASPECT_RATIO_HEIGHT: String
```

A key describing the pixel aspect ratio height. The associated value is an integer

 Value: "sar-height"

### KEY_PIXEL_ASPECT_RATIO_WIDTH

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_PIXEL_ASPECT_RATIO_WIDTH: String
```

A key describing the pixel aspect ratio width. The associated value is an integer

 Value: "sar-width"

### KEY_PREPEND_HEADER_TO_SYNC_FRAMES

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_PREPEND_HEADER_TO_SYNC_FRAMES: String
```

An optional key describing whether encoders prepend headers to sync frames (e.g. SPS and PPS to IDR frames for H.264). This is an optional parameter that applies only to video encoders. A video encoder may not support this feature; the component will fail to configure in that case. For other components, this key is ignored. The value is an integer, with 1 indicating to prepend headers to every sync frames, or 0 otherwise. The default value is 0.

 Value: "prepend-sps-pps-to-idr-frames"

### KEY_PRIORITY

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_PRIORITY: String
```

A key describing the desired codec priority.

The associated value is an integer. Higher value means lower priority.

Currently, only two levels are supported: 
0: realtime priority - meaning that the codec shall support the given performance configuration (e.g. framerate) at realtime. This should only be used by media playback, capture, and possibly by realtime communication scenarios if best effort performance is not suitable. 
1: non-realtime priority (best effort).

This is a hint used at codec configuration and resource planning - to understand the realtime requirements of the application; however, due to the nature of media components, performance is not guaranteed.

 Value: "priority"

### KEY_PROFILE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_PROFILE: String
```

A key describing the desired profile to be used by an encoder.

The associated value is an integer. Constants are declared in `https://developer.android.com/reference/kotlin/android/media/MediaCodecInfo.CodecProfileLevel`. This key is used as a hint, and is only supported for codecs that specify a profile. When configuring profile, encoder configuration may fail if other parameters are not compatible with the desired profile or if the desired profile is not supported, but it may also fail silently (where the encoder ends up using a different, compatible profile.)

It is recommended that the profile is set for all encoders. For more information, see the *Encoder Profiles* section of the `https://developer.android.com/reference/kotlin/android/media/MediaCodec` API reference.

**Note:** Codecs are free to use all the available coding tools at the specified profile, but may ultimately choose to not do so.

**Note:** When configuring video encoders, profile (if set) must be set together with `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_LEVEL:kotlin.String`.

 Value: "profile"

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/MediaCodecInfo.CodecCapabilities#profileLevels:kotlin.Array`

### KEY_PUSH_BLANK_BUFFERS_ON_STOP

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_PUSH_BLANK_BUFFERS_ON_STOP: String
```

If specified when configuring a video decoder rendering to a surface, causes the decoder to output "blank", i.e. black frames to the surface when stopped to clear out any previously displayed contents. The associated value is an integer of value 1.

 Value: "push-blank-buffers-on-shutdown"

### KEY_QUALITY

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_QUALITY: String
```

A key describing the desired encoding quality. The associated value is an integer. This key is only supported for encoders that are configured in constant-quality mode. These values are device and codec specific, but lower values generally result in more efficient (smaller-sized) encoding.

 Value: "quality"

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/MediaCodecInfo.EncoderCapabilities#getQualityRange()`

### KEY_REPEAT_PREVIOUS_FRAME_AFTER

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_REPEAT_PREVIOUS_FRAME_AFTER: String
```

Applies only when configuring a video encoder in "surface-input" mode. The associated value is a long and gives the time in microseconds after which the frame previously submitted to the encoder will be repeated (once) if no new frame became available since.

 Value: "repeat-previous-frame-after"

### KEY_ROTATION

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_ROTATION: String
```

A key describing the desired clockwise rotation on an output surface. This key is only used when the codec is configured using an output surface. The associated value is an integer, representing degrees. Supported values are 0, 90, 180 or 270. This is an optional field; if not specified, rotation defaults to 0. Note that if #KEY_HORIZONTAL_FLIP is also set, the rotation will be applied after the flip.

 Value: "rotation-degrees"

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/MediaCodecInfo.CodecCapabilities#profileLevels:kotlin.Array`

### KEY_SAMPLE_RATE

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SAMPLE_RATE: String
```

A key describing the sample rate of an audio format. The associated value is an integer

 Value: "sample-rate"

### KEY_SECURITY_MODEL

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SECURITY_MODEL: String
```

A key describing the requested security model as flags.

The associated value is a flag of the following values: `https://developer.android.com/reference/kotlin/android/media/MediaFormat#FLAG_SECURITY_MODEL_SANDBOXED:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/media/MediaFormat#FLAG_SECURITY_MODEL_MEMORY_SAFE:kotlin.Int`. The default value is `https://developer.android.com/reference/kotlin/android/media/MediaFormat#FLAG_SECURITY_MODEL_SANDBOXED:kotlin.Int`.

When passed to `https://developer.android.com/reference/kotlin/android/media/MediaCodecList#findDecoderForFormat(android.media.MediaFormat)` or `https://developer.android.com/reference/kotlin/android/media/MediaCodecList#findEncoderForFormat(android.media.MediaFormat)`, MediaCodecList filters the security model of the codecs according to this flag value.

When passed to android.media.MediaCodec#configure, MediaCodec verifies the security model matches the flag value passed, and throws `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#` if the model does not match.

<br />

 Value: "security-model"

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/MediaCodecInfo#getSecurityModel()`
- `https://developer.android.com/reference/kotlin/android/media/MediaCodecList#findDecoderForFormat(android.media.MediaFormat)`
- `https://developer.android.com/reference/kotlin/android/media/MediaCodecList#findEncoderForFormat(android.media.MediaFormat)`

### KEY_SLICE_HEIGHT

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SLICE_HEIGHT: String
```

A key describing the plane height of a multi-planar (YUV) video bytebuffer layout. Slice height (or plane height/vertical stride) is the number of rows that must be skipped to get from the top of the Y plane to the top of the U plane in the bytebuffer. In essence the offset of the U plane is sliceHeight \* stride. The height of the U/V planes can be calculated based on the color format, though it is generally undefined and depends on the device and release. The associated value is an integer, representing number of rows.

 Value: "slice-height"

### KEY_SLOW_MOTION_MARKERS

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_SLOW_MOTION_MARKERS: String
```

A key for retrieving the slow-motion marker information associated with a video track.

The associated value is a ByteBuffer in `https://developer.android.com/reference/kotlin/java/nio/ByteOrder.html#BIG_ENDIAN:java.nio.ByteOrder` (networking order) of the following format:

```kotlin
float(32) playbackRate;
      unsigned int(32) numMarkers;
      for (i = 0;i < numMarkers; i++) {
          int(64) timestampUs;
          float(32) speedRatio;
      }
```
The meaning of each field is as follows:

| playbackRate | The frame rate at which the playback should happen (or the flattened clip should be). |
| --- | --- |
| numMarkers | The number of slow-motion markers that follows. |
| timestampUs | The starting point of a new segment. |
| speedRatio | The playback speed for that segment. The playback speed is a floating point number, indicating how fast the time progresses relative to that written in the container. (Eg. 4.0 means time goes 4x as fast, which makes 30fps become 120fps.) |
| --- | --- |

The following constraints apply to the timestampUs of the markers:
- The timestampUs shall be monotonically increasing.
- The timestampUs shall fall within the time span of the video track.
- The first timestampUs should match that of the first video sample.

 Value: "slow-motion-markers"

### KEY_STRIDE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_STRIDE: String
```

A key describing the stride of the video bytebuffer layout. Stride (or row increment) is the difference between the index of a pixel and that of the pixel directly underneath. For YUV 420 formats, the stride corresponds to the Y plane; the stride of the U and V planes can be calculated based on the color format, though it is generally undefined and depends on the device and release. The associated value is an integer, representing number of bytes.

 Value: "stride"

### KEY_TEMPORAL_LAYERING

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_TEMPORAL_LAYERING: String
```

A key describing the temporal layering schema. This is an optional parameter that applies only to video encoders. Use android.media.MediaCodec#getOutputFormat after android.media.MediaCodec#configure to query if the encoder supports the desired schema. Supported values are `webrtc.vp8.N-layer`, `android.generic.N`, `android.generic.N+M`, `webrtc.svc.l1tN` and `none`, where `N` denotes the total number of non-bidirectional layers (which must be at least 1) and `M` denotes the total number of bidirectional layers (which must be non-negative). The video encoder for `webrtc.svc.* ` schema must produce the layer structure that is compliant with [WebRTC-SVC](https://www.w3.org/TR/webrtc-svc).

`android.generic.*` schemas have been added in `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#N_MR1:kotlin.Int`.

`webrtc.svc.l1t*` schemas have been added in `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#CINNAMON_BUN:kotlin.Int`.

The encoder may support fewer temporal layers, in which case the output format will contain the configured schema. If the encoder does not support temporal layering, the output format will not have an entry with this key. The associated value is a string.

 Value: "ts-schema"

### KEY_TEMPORAL_LAYER_ID

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_TEMPORAL_LAYER_ID: String
```

A key describing the index of the temporal layer of the output buffer. This is an optional parameter that applies only to video encoders. The key is present in every output buffer only if `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_TEMPORAL_LAYERING:kotlin.String` is "webrtc.svc.\*" and `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_TEMPORAL_LAYER_ID:kotlin.String` is configured at android.media.MediaCodec#configure and the encoder is producing temporal layer encoding. The associated value is an integer and 0-based. The value 0 represents the base layer and 1 is the second layer, and thus the value must be less than the number of layers specified by `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_TEMPORAL_LAYERING:kotlin.String` configured at android.media.MediaCodec#configure.

 Value: "temporal-layer-id"

### KEY_TILE_HEIGHT

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_TILE_HEIGHT: String
```

A key describing the height (in pixels) of each tile of the content in a `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_IMAGE_ANDROID_HEIC:kotlin.String` / `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_IMAGE_AVIF:kotlin.String` track. The associated value is an integer. Refer to `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_IMAGE_ANDROID_HEIC:kotlin.String` / `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_IMAGE_AVIF:kotlin.String` on decoding instructions of such tracks.

 Value: "tile-height"

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_TILE_WIDTH:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_GRID_ROWS:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_GRID_COLUMNS:kotlin.String`

### KEY_TILE_WIDTH

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_TILE_WIDTH: String
```

A key describing the width (in pixels) of each tile of the content in a `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_IMAGE_ANDROID_HEIC:kotlin.String` / `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_IMAGE_AVIF:kotlin.String` track. The associated value is an integer. Refer to `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_IMAGE_ANDROID_HEIC:kotlin.String` / `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_IMAGE_AVIF:kotlin.String` on decoding instructions of such tracks.

 Value: "tile-width"

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_TILE_HEIGHT:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_GRID_ROWS:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_GRID_COLUMNS:kotlin.String`

### KEY_TRACK_ID

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_TRACK_ID: String
```

A key describing a unique ID for the content of a media track.

This key is used by `https://developer.android.com/reference/kotlin/android/media/MediaExtractor`. Some extractors provide multiple encodings of the same track (e.g. float audio tracks for FLAC and WAV may be expressed as two tracks via MediaExtractor: a normal PCM track for backward compatibility, and a float PCM track for added fidelity. Similarly, Dolby Vision extractor may provide a baseline SDR version of a DV track.) This key can be used to identify which MediaExtractor tracks refer to the same underlying content.
The associated value is an integer.

 Value: "track-id"

### KEY_VIDEO_BITRATE_LAYERING

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_VIDEO_BITRATE_LAYERING: String
```

Set the bitrate distributions for temporal layering.

The associated value is a String in the format "ratio1;ratio2;...;ratioN", where N is the number of temporal layers - 1. Each ratio represents the bitrate allocation for the current layer and all lower layers combined, as a fraction of the total bitrate. There is no value for the highest temporal layer because it is always 1.0.

For example, if there are 3 temporal layers and the total bitrate is 1000kbps, a value of "0.3;0.6" would mean:

- Layer 0 (base layer): 30% of total bitrate (300kbps)
- Layer 0 + Layer 1: 60% of total bitrate (600kbps), so Layer 1 gets 30% (300kbps)
- Layer 0 + Layer 1 + Layer 2: 100% of total bitrate (1000kbps), so Layer 2 gets 40% (400kbps)

The ratios must be monotonically increasing. See `https://developer.android.com/reference/kotlin/android/media/MediaCodec#setParameters(android.os.Bundle)`

 Value: "video-bitrate-layering"

### KEY_VIDEO_ENCODING_STATISTICS_LEVEL

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_VIDEO_ENCODING_STATISTICS_LEVEL: String
```

A key describing the level of encoding statistics information emitted from video encoder. The associated value is an integer.

 Value: "video-encoding-statistics-level"

### KEY_VIDEO_QP_AVERAGE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_VIDEO_QP_AVERAGE: String
```

A key describing the per-frame average block QP (Quantization Parameter). This is a part of a video 'Encoding Statistics' export feature. This value is emitted from video encoder for a video frame. The average value is rounded to the nearest integer value. The associated value is an integer.

 Value: "video-qp-average"

### KEY_VIDEO_QP_B_MAX

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_VIDEO_QP_B_MAX: String
```

A key describing the maximum Quantization Parameter allowed for encoding video. This value applies to video B-frames. The associated value is an integer.

 Value: "video-qp-b-max"

### KEY_VIDEO_QP_B_MIN

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_VIDEO_QP_B_MIN: String
```

A key describing the minimum Quantization Parameter allowed for encoding video. This value applies to video B-frames. The associated value is an integer.

 Value: "video-qp-b-min"

### KEY_VIDEO_QP_I_MAX

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_VIDEO_QP_I_MAX: String
```

A key describing the maximum Quantization Parameter allowed for encoding video. This value applies to video I-frames. The associated value is an integer.

 Value: "video-qp-i-max"

### KEY_VIDEO_QP_I_MIN

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_VIDEO_QP_I_MIN: String
```

A key describing the minimum Quantization Parameter allowed for encoding video. This value applies to video I-frames. The associated value is an integer.

 Value: "video-qp-i-min"

### KEY_VIDEO_QP_MAX

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_VIDEO_QP_MAX: String
```

A key describing the maximum Quantization Parameter allowed for encoding video. This key applies to all three video picture types (I, P, and B). The value is used directly for picture type I; a per-mime formula is used to calculate the value for the remaining picture types. This calculation can be avoided by directly specifying values for each picture type using the type-specific keys `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_VIDEO_QP_I_MAX:kotlin.String`, `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_VIDEO_QP_P_MAX:kotlin.String`, and `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_VIDEO_QP_B_MAX:kotlin.String`. The associated value is an integer.

 Value: "video-qp-max"

### KEY_VIDEO_QP_MIN

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_VIDEO_QP_MIN: String
```

A key describing the minimum Quantization Parameter allowed for encoding video. This key applies to all three video frame types (I, P, and B). The value is used directly for picture type I; a per-mime formula is used to calculate the value for the remaining picture types. This calculation can be avoided by directly specifying values for each picture type using the type-specific keys `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_VIDEO_QP_I_MIN:kotlin.String`, `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_VIDEO_QP_P_MIN:kotlin.String`, and `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_VIDEO_QP_B_MIN:kotlin.String`. The associated value is an integer.

 Value: "video-qp-min"

### KEY_VIDEO_QP_P_MAX

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_VIDEO_QP_P_MAX: String
```

A key describing the maximum Quantization Parameter allowed for encoding video. This value applies to video P-frames. The associated value is an integer.

 Value: "video-qp-p-max"

### KEY_VIDEO_QP_P_MIN

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_VIDEO_QP_P_MIN: String
```

A key describing the minimum Quantization Parameter allowed for encoding video. This value applies to video P-frames. The associated value is an integer.

 Value: "video-qp-p-min"

### KEY_WIDTH

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val KEY_WIDTH: String
```

A key describing the width of the content in a video format. The associated value is an integer

 Value: "width"

### LOG_SESSION_ID

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LOG_SESSION_ID: String
```

A key describing the log session ID for MediaCodec. The log session ID is a random 32-byte hexadecimal string that is used to associate metrics from multiple media codec instances to the same playback or recording session. The value is created as `https://developer.android.com/reference/kotlin/android/media/metrics/LogSessionId`. Sessions are created in `https://developer.android.com/reference/kotlin/android/media/metrics/MediaMetricsManager`. The associated value is a string.

 Value: "log-session-id"

### MIMETYPE_AUDIO_AAC

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIMETYPE_AUDIO_AAC: String
```

 Value: "audio/mp4a-latm"

### MIMETYPE_AUDIO_AAC_ELD

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIMETYPE_AUDIO_AAC_ELD: String
```

MIME type for AAC Enhanced Low Delay (ELD) audio stream. Uses the scheme defined by RFC 6381 with OTI of MPEG-4 (40) and AOT of ELD (39) from ISO/IEC 14496-3.

 Value: "audio/mp4a.40.39"

### MIMETYPE_AUDIO_AAC_HE_V1

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIMETYPE_AUDIO_AAC_HE_V1: String
```

MIME type for HE-AAC v1 (LC + SBR) audio stream. Uses the scheme defined by RFC 6381 with OTI of MPEG-4 (40) and AOT of AAC SBR (5) from ISO/IEC 14496-3.

 Value: "audio/mp4a.40.05"

### MIMETYPE_AUDIO_AAC_HE_V2

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIMETYPE_AUDIO_AAC_HE_V2: String
```

MIME type for HE-AAC v2 (LC + SBR + PS) audio stream. Uses the scheme defined by RFC 6381 with OTI of MPEG-4 (40) and AOT of PS (29) from ISO/IEC 14496-3.

 Value: "audio/mp4a.40.29"

### MIMETYPE_AUDIO_AAC_LC

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIMETYPE_AUDIO_AAC_LC: String
```

MIME type for AAC Low Complexity (LC) audio stream. Uses the scheme defined by RFC 6381 with OTI of MPEG-4 (40) and AOT of AAC LC (2) from ISO/IEC 14496-3.

 Value: "audio/mp4a.40.02"

### MIMETYPE_AUDIO_AAC_XHE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIMETYPE_AUDIO_AAC_XHE: String
```

MIME type for AAC XHE audio stream. Uses the scheme defined by RFC 6381 with OTI of MPEG-4 (40) and AOT of USAC (42) from ISO/IEC 14496-3.

When encoding xHE-AAC, `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_AUDIO_PRESENTATION_ID:kotlin.String` can be used for audio encoders to differentiate between different streams with different encoding settings, and `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_I_FRAME_INTERVAL:kotlin.String` can be used to specify key frames.

 Value: "audio/mp4a.40.42"

### MIMETYPE_AUDIO_AC3

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIMETYPE_AUDIO_AC3: String
```

 Value: "audio/ac3"

### MIMETYPE_AUDIO_AC4

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIMETYPE_AUDIO_AC4: String
```

MIME type for AC-4 sync frame transport format audio stream.

 Value: "audio/ac4"

### MIMETYPE_AUDIO_AMR_NB

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIMETYPE_AUDIO_AMR_NB: String
```

 Value: "audio/3gpp"

### MIMETYPE_AUDIO_AMR_WB

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIMETYPE_AUDIO_AMR_WB: String
```

 Value: "audio/amr-wb"

### MIMETYPE_AUDIO_DOLBY_MAT

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIMETYPE_AUDIO_DOLBY_MAT: String
```

MIME type for Dolby Metadata-enhanced Audio Transmission (MAT) audio stream.

 Value: "audio/vnd.dolby.mat"

### MIMETYPE_AUDIO_DOLBY_TRUEHD

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIMETYPE_AUDIO_DOLBY_TRUEHD: String
```

MIME type for Dolby TrueHD audio format, based on Meridian Lossless Packing (MLP).

 Value: "audio/vnd.dolby.mlp"

### MIMETYPE_AUDIO_DRA

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIMETYPE_AUDIO_DRA: String
```

MIME type for Dynamic Resolution Adaptation (DRA) audio stream.

 Value: "audio/vnd.dra"

### MIMETYPE_AUDIO_DTS

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIMETYPE_AUDIO_DTS: String
```

MIME type for DTS Digital Surround (up to 5.1 channels) audio stream, aka DTS-CA.

 Value: "audio/vnd.dts"

### MIMETYPE_AUDIO_DTS_HD

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIMETYPE_AUDIO_DTS_HD: String
```

MIME type for DTS HD (up to 7.1 channels) audio stream. With codec profile DTS_HDProfileHRA represents DTS HD High Resolution Audio. With codec profile DTS_HDProfileMA represents DTS HD Master Audio. With codec profile DTS_HDProfileLBR represents DTS Express.

 Value: "audio/vnd.dts.hd"

### MIMETYPE_AUDIO_DTS_UHD

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIMETYPE_AUDIO_DTS_UHD: String
```

MIME type for DTS UHD (object-based) audio stream, aka DTS:X. With codec profile DTS_UHDProfileP1 represents DTS-UHD P1. With codec profile DTS_UHDProfileP2 represents DTS-UHD P2.

 Value: "audio/vnd.dts.uhd"

### MIMETYPE_AUDIO_EAC3

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIMETYPE_AUDIO_EAC3: String
```

 Value: "audio/eac3"

### MIMETYPE_AUDIO_EAC3_JOC

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIMETYPE_AUDIO_EAC3_JOC: String
```

 Value: "audio/eac3-joc"

### MIMETYPE_AUDIO_FLAC

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIMETYPE_AUDIO_FLAC: String
```

 Value: "audio/flac"

### MIMETYPE_AUDIO_G711_ALAW

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIMETYPE_AUDIO_G711_ALAW: String
```

 Value: "audio/g711-alaw"

### MIMETYPE_AUDIO_G711_MLAW

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIMETYPE_AUDIO_G711_MLAW: String
```

 Value: "audio/g711-mlaw"

### MIMETYPE_AUDIO_IAMF

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIMETYPE_AUDIO_IAMF: String
```

MIME type for IAMF audio stream

 Value: "audio/iamf"

### MIMETYPE_AUDIO_IEC61937

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIMETYPE_AUDIO_IEC61937: String
```

MIME type for the IEC61937 audio stream encapsulation. This type isn't defined by IANA.

 Value: "audio/x-iec61937"

### MIMETYPE_AUDIO_MPEG

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIMETYPE_AUDIO_MPEG: String
```

 Value: "audio/mpeg"

### MIMETYPE_AUDIO_MPEGH_BL_L3

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIMETYPE_AUDIO_MPEGH_BL_L3: String
```

MIME type for MPEG-H Baseline (BL) Profile L3 audio stream. Uses the scheme defined by RFC 6381 with mpegh3daProfileLevelIndication for main profile/L3 (0x3) from ISO/IEC 23008-3.

 Value: "audio/mhm1.03"

### MIMETYPE_AUDIO_MPEGH_BL_L4

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIMETYPE_AUDIO_MPEGH_BL_L4: String
```

MIME type for MPEG-H Baseline (BL) Profile L4 audio stream. Uses the scheme defined by RFC 6381 with mpegh3daProfileLevelIndication for main profile/L4 (0x4) from ISO/IEC 23008-3.

 Value: "audio/mhm1.04"

### MIMETYPE_AUDIO_MPEGH_LC_L3

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIMETYPE_AUDIO_MPEGH_LC_L3: String
```

MIME type for MPEG-H Low Complexity (LC) L3 audio stream. Uses the scheme defined by RFC 6381 with mpegh3daProfileLevelIndication for LC profile/L3 (0xD) from ISO/IEC 23008-3.

 Value: "audio/mhm1.0d"

### MIMETYPE_AUDIO_MPEGH_LC_L4

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIMETYPE_AUDIO_MPEGH_LC_L4: String
```

MIME type for MPEG-H Low Complexity (LC) L4 audio stream. Uses the scheme defined by RFC 6381 with mpegh3daProfileLevelIndication for LC profile/L4 (0xE) from ISO/IEC 23008-3.

 Value: "audio/mhm1.0e"

### MIMETYPE_AUDIO_MPEGH_MHA1

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIMETYPE_AUDIO_MPEGH_MHA1: String
```

MIME type for MPEG-H Audio single stream

 Value: "audio/mha1"

### MIMETYPE_AUDIO_MPEGH_MHM1

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIMETYPE_AUDIO_MPEGH_MHM1: String
```

MIME type for MPEG-H Audio single stream, encapsulated in MHAS

 Value: "audio/mhm1"

### MIMETYPE_AUDIO_MSGSM

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIMETYPE_AUDIO_MSGSM: String
```

 Value: "audio/gsm"

### MIMETYPE_AUDIO_OPUS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIMETYPE_AUDIO_OPUS: String
```

 Value: "audio/opus"

### MIMETYPE_AUDIO_QCELP

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIMETYPE_AUDIO_QCELP: String
```

 Value: "audio/qcelp"

### MIMETYPE_AUDIO_RAW

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIMETYPE_AUDIO_RAW: String
```

 Value: "audio/raw"

### MIMETYPE_AUDIO_SCRAMBLED

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIMETYPE_AUDIO_SCRAMBLED: String
```

 Value: "audio/scrambled"

### MIMETYPE_AUDIO_VORBIS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIMETYPE_AUDIO_VORBIS: String
```

 Value: "audio/vorbis"

### MIMETYPE_IMAGE_ANDROID_HEIC

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIMETYPE_IMAGE_ANDROID_HEIC: String
```

MIME type for HEIF still image data encoded in HEVC. To decode such an image, `https://developer.android.com/reference/kotlin/android/media/MediaCodec` decoder for `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_VIDEO_HEVC:kotlin.String` shall be used. The client needs to form the correct #MediaFormat based on additional information in the track format (shown in the next paragraph), and send it to android.media.MediaCodec#configure. The track's MediaFormat will come with `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_WIDTH:kotlin.String` and `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_HEIGHT:kotlin.String` keys, which describes the width and height of the image. If the image doesn't contain grid (i.e. none of `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_TILE_WIDTH:kotlin.String`, `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_TILE_HEIGHT:kotlin.String`, `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_GRID_ROWS:kotlin.String`, `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_GRID_COLUMNS:kotlin.String` are present), the track will contain a single sample of coded data for the entire image, and the image width and height should be used to set up the decoder. If the image does come with grid, each sample from the track will contain one tile in the grid, of which the size is described by `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_TILE_WIDTH:kotlin.String` and `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_TILE_HEIGHT:kotlin.String`. This size (instead of `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_WIDTH:kotlin.String` and `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_HEIGHT:kotlin.String`) should be used to set up the decoder. The track contains `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_GRID_ROWS:kotlin.String` by `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_GRID_COLUMNS:kotlin.String` samples in row-major, top-row first, left-to-right order. The output image should be reconstructed by first tiling the decoding results of the tiles in the correct order, then trimming (before rotation is applied) on the bottom and right side, if the tiled area is larger than the image width and height.

 Value: "image/vnd.android.heic"

### MIMETYPE_IMAGE_AVIF

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIMETYPE_IMAGE_AVIF: String
```

MIME type for AVIF still image data encoded in AV1. To decode such an image, `https://developer.android.com/reference/kotlin/android/media/MediaCodec` decoder for `https://developer.android.com/reference/kotlin/android/media/MediaFormat#MIMETYPE_VIDEO_AV1:kotlin.String` shall be used. The client needs to form the correct #MediaFormat based on additional information in the track format (shown in the next paragraph), and send it to android.media.MediaCodec#configure. The track's MediaFormat will come with `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_WIDTH:kotlin.String` and `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_HEIGHT:kotlin.String` keys, which describes the width and height of the image. If the image doesn't contain grid (i.e. none of `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_TILE_WIDTH:kotlin.String`, `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_TILE_HEIGHT:kotlin.String`, `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_GRID_ROWS:kotlin.String`, `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_GRID_COLUMNS:kotlin.String` are present), the track will contain a single sample of coded data for the entire image, and the image width and height should be used to set up the decoder. If the image does come with grid, each sample from the track will contain one tile in the grid, of which the size is described by `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_TILE_WIDTH:kotlin.String` and `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_TILE_HEIGHT:kotlin.String`. This size (instead of `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_WIDTH:kotlin.String` and `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_HEIGHT:kotlin.String`) should be used to set up the decoder. The track contains `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_GRID_ROWS:kotlin.String` by `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_GRID_COLUMNS:kotlin.String` samples in row-major, top-row first, left-to-right order. The output image should be reconstructed by first tiling the decoding results of the tiles in the correct order, then trimming (before rotation is applied) on the bottom and right side, if the tiled area is larger than the image width and height.

 Value: "image/avif"

### MIMETYPE_TEXT_CEA_608

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIMETYPE_TEXT_CEA_608: String
```

MIME type for CEA-608 closed caption data.

 Value: "text/cea-608"

### MIMETYPE_TEXT_CEA_708

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIMETYPE_TEXT_CEA_708: String
```

MIME type for CEA-708 closed caption data.

 Value: "text/cea-708"

### MIMETYPE_TEXT_SUBRIP

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIMETYPE_TEXT_SUBRIP: String
```

MIME type for SubRip (SRT) container.

 Value: "application/x-subrip"

### MIMETYPE_TEXT_VTT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIMETYPE_TEXT_VTT: String
```

MIME type for WebVTT subtitle data.

 Value: "text/vtt"

### MIMETYPE_VIDEO_APV

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIMETYPE_VIDEO_APV: String
```

 Value: "video/apv"

### MIMETYPE_VIDEO_AV1

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIMETYPE_VIDEO_AV1: String
```

 Value: "video/av01"

### MIMETYPE_VIDEO_AVC

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIMETYPE_VIDEO_AVC: String
```

 Value: "video/avc"

### MIMETYPE_VIDEO_DOLBY_VISION

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIMETYPE_VIDEO_DOLBY_VISION: String
```

 Value: "video/dolby-vision"

### MIMETYPE_VIDEO_H263

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIMETYPE_VIDEO_H263: String
```

 Value: "video/3gpp"

### MIMETYPE_VIDEO_HEVC

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIMETYPE_VIDEO_HEVC: String
```

 Value: "video/hevc"

### MIMETYPE_VIDEO_MPEG2

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIMETYPE_VIDEO_MPEG2: String
```

 Value: "video/mpeg2"

### MIMETYPE_VIDEO_MPEG4

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIMETYPE_VIDEO_MPEG4: String
```

 Value: "video/mp4v-es"

### MIMETYPE_VIDEO_RAW

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIMETYPE_VIDEO_RAW: String
```

 Value: "video/raw"

### MIMETYPE_VIDEO_SCRAMBLED

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIMETYPE_VIDEO_SCRAMBLED: String
```

 Value: "video/scrambled"

### MIMETYPE_VIDEO_VP8

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIMETYPE_VIDEO_VP8: String
```

 Value: "video/x-vnd.on2.vp8"

### MIMETYPE_VIDEO_VP9

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIMETYPE_VIDEO_VP9: String
```

 Value: "video/x-vnd.on2.vp9"

### MIMETYPE_VIDEO_VVC

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIMETYPE_VIDEO_VVC: String
```

 Value: "video/vvc"

### PICTURE_TYPE_B

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PICTURE_TYPE_B: Int
```

Picture Type is B Frame.

 Value: 3

### PICTURE_TYPE_I

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PICTURE_TYPE_I: Int
```

Picture Type is I Frame.

 Value: 1

### PICTURE_TYPE_P

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PICTURE_TYPE_P: Int
```

Picture Type is P Frame.

 Value: 2

### PICTURE_TYPE_UNKNOWN

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PICTURE_TYPE_UNKNOWN: Int
```

Picture Type is unknown.

 Value: 0

### TYPE_BYTE_BUFFER

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_BYTE_BUFFER: Int
```

 Value: 5

### TYPE_FLOAT

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_FLOAT: Int
```

 Value: 3

### TYPE_INTEGER

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_INTEGER: Int
```

 Value: 1

### TYPE_LONG

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_LONG: Int
```

 Value: 2

### TYPE_NULL

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_NULL: Int
```

 Value: 0

### TYPE_STRING

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TYPE_STRING: Int
```

 Value: 4

### VIDEO_ENCODING_STATISTICS_LEVEL_1

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val VIDEO_ENCODING_STATISTICS_LEVEL_1: Int
```

Encoding Statistics Level 1. Encoder generates `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_PICTURE_TYPE:kotlin.String` and `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_VIDEO_QP_AVERAGE:kotlin.String` for each frame.

 Value: 1

### VIDEO_ENCODING_STATISTICS_LEVEL_NONE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val VIDEO_ENCODING_STATISTICS_LEVEL_NONE: Int
```

Encoding Statistics Level None. Encoder generates no information about Encoding statistics.

 Value: 0

## Public constructors

### MediaFormat

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
MediaFormat()
```

Creates an empty MediaFormat

### MediaFormat

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
MediaFormat(other: MediaFormat)
```

Create a copy of a media format object.

| Parameters ||
|---|---|
| `other` | [MediaFormat](MediaFormat.md): This value cannot be `null`. |

## Public methods

### containsFeature

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun containsFeature(name: String): Boolean
```

Returns true iff a feature of the given name exists in the format.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

### containsKey

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun containsKey(name: String): Boolean
```

Returns true iff a key of the given name exists in the format.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

### createAudioFormat

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createAudioFormat(
    mime: String, 
    sampleRate: Int, 
    channelCount: Int
): MediaFormat
```

Creates a minimal audio format.

| Parameters ||
|---|---|
| `mime` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The mime type of the content. This value cannot be `null`. |
| `sampleRate` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The sampling rate of the content. |
| `channelCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of audio channels in the content. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#` | This value cannot be `null`. |

### createSubtitleFormat

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createSubtitleFormat(
    mime: String, 
    language: String!
): MediaFormat
```

Creates a minimal subtitle format.

| Parameters ||
|---|---|
| `mime` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The mime type of the content. This value cannot be `null`. |
| `language` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The language of the content, using either ISO 639-1 or 639-2/T codes. Specify null or "und" if language information is only included in the content. (This will also work if there are multiple language tracks in the content.) |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#` | This value cannot be `null`. |

### createVideoFormat

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun createVideoFormat(
    mime: String, 
    width: Int, 
    height: Int
): MediaFormat
```

Creates a minimal video format.

| Parameters ||
|---|---|
| `mime` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The mime type of the content. This value cannot be `null`. |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The width of the content (in pixels) |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The height of the content (in pixels) |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/media/MediaFormat#` | This value cannot be `null`. |

### getByteBuffer

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getByteBuffer(name: String): ByteBuffer?
```

Returns the value of a ByteBuffer key.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#?` | null if the key does not exist or the stored value for the key is null |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the stored value for the key is int, long, float or String |

### getByteBuffer

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getByteBuffer(
    name: String, 
    defaultValue: ByteBuffer
): ByteBuffer
```

Returns the value of a ByteBuffer key, or the default value if the key is missing.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `defaultValue` | [ByteBuffer](../java.nio/ByteBuffer.md): This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#` | defaultValue if the key does not exist or the stored value for the key is null |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the stored value for the key is int, long, float or String |

### getFeatureEnabled

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getFeatureEnabled(feature: String): Boolean
```

Returns whether a feature is to be enabled (`true`) or disabled (`false`).

| Parameters ||
|---|---|
| `feature` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the name of a `https://developer.android.com/reference/kotlin/android/media/MediaCodecInfo.CodecCapabilities` feature. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the feature was neither set to be enabled nor to be disabled. |

### getFeatures

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getFeatures(): MutableSet<String!>
```

Returns a `https://developer.android.com/reference/kotlin/java/util/Set.html#` view of the features contained in this MediaFormat. The set is backed by the MediaFormat object, so changes to the format are reflected in the set, and vice-versa. If the format is modified while an iteration over the set is in progress (except through the iterator's own remove operation), the results of the iteration are undefined. The set supports element removal, which removes the corresponding mapping from the format, via the Iterator.remove, Set.remove, removeAll, retainAll, and clear operations. It does not support the add or addAll operations.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>` | This value cannot be `null`. |

### getFloat

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getFloat(name: String): Float
```

Returns the value of a float key.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the stored value for the key is int, long, ByteBuffer or String |
| `java.lang.NullPointerException` | if the key does not exist or the stored value for the key is null |

### getFloat

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getFloat(
    name: String, 
    defaultValue: Float
): Float
```

Returns the value of a float key, or the default value if the key is missing.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | defaultValue if the key does not exist or the stored value for the key is null |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the stored value for the key is int, long, ByteBuffer or String |

### getInteger

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getInteger(name: String): Int
```

Returns the value of an integer key.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the stored value for the key is long, float, ByteBuffer or String |
| `java.lang.NullPointerException` | if the key does not exist or the stored value for the key is null |

### getInteger

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getInteger(
    name: String, 
    defaultValue: Int
): Int
```

Returns the value of an integer key, or the default value if the key is missing.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | defaultValue if the key does not exist or the stored value for the key is null |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the stored value for the key is long, float, ByteBuffer or String |

### getKeys

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getKeys(): MutableSet<String!>
```

Returns a `https://developer.android.com/reference/kotlin/java/util/Set.html#` view of the keys contained in this MediaFormat. The set is backed by the MediaFormat object, so changes to the format are reflected in the set, and vice-versa. If the format is modified while an iteration over the set is in progress (except through the iterator's own remove operation), the results of the iteration are undefined. The set supports element removal, which removes the corresponding mapping from the format, via the Iterator.remove, Set.remove, removeAll, retainAll, and clear operations. It does not support the add or addAll operations.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>` | This value cannot be `null`. |

### getLong

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getLong(name: String): Long
```

Returns the value of a long key.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the stored value for the key is int, float, ByteBuffer or String |
| `java.lang.NullPointerException` | if the key does not exist or the stored value for the key is null |

### getLong

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getLong(
    name: String, 
    defaultValue: Long
): Long
```

Returns the value of a long key, or the default value if the key is missing.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | defaultValue if the key does not exist or the stored value for the key is null |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the stored value for the key is int, float, ByteBuffer or String |

### getNumber

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getNumber(name: String): Number?
```

Returns the value of a numeric key. This is provided as a convenience method for keys that may take multiple numeric types, such as `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_FRAME_RATE:kotlin.String`, or `https://developer.android.com/reference/kotlin/android/media/MediaFormat#KEY_I_FRAME_INTERVAL:kotlin.String`.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html?` | null if the key does not exist or the stored value for the key is null |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the stored value for the key is ByteBuffer or String |

### getNumber

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getNumber(
    name: String, 
    defaultValue: Number
): Number
```

Returns the value of a numeric key, or the default value if the key is missing.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `defaultValue` | [Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html` | defaultValue if the key does not exist or the stored value for the key is null |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the stored value for the key is ByteBuffer or String |

### getString

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getString(name: String): String?
```

Returns the value of a string key.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | null if the key does not exist or the stored value for the key is null |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the stored value for the key is int, long, float or ByteBuffer |

### getString

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getString(
    name: String, 
    defaultValue: String
): String
```

Returns the value of a string key, or the default value if the key is missing.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `defaultValue` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | defaultValue if the key does not exist or the stored value for the key is null |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the stored value for the key is int, long, float or ByteBuffer |

### getValueTypeForKey

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getValueTypeForKey(name: String): Int
```

Returns the value type for a key. If the key does not exist, it returns TYPE_NULL.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/media/MediaFormat#TYPE_NULL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/MediaFormat#TYPE_INTEGER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/MediaFormat#TYPE_LONG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/MediaFormat#TYPE_FLOAT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/MediaFormat#TYPE_STRING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/MediaFormat#TYPE_BYTE_BUFFER:kotlin.Int` |

### removeFeature

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun removeFeature(name: String): Unit
```

Removes a given feature setting if present. Has no effect if the feature setting is not present.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

### removeKey

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun removeKey(name: String): Unit
```

Removes a value of a given key if present. Has no effect if the key is not present.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

### setByteBuffer

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setByteBuffer(
    name: String, 
    bytes: ByteBuffer?
): Unit
```

Sets the value of a ByteBuffer key.

If value is `null`, it sets a null value that behaves similarly to a missing key. This could be used prior to API level `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int` to effectively remove a key.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `bytes` | [ByteBuffer](../java.nio/ByteBuffer.md)?: This value may be `null`. |

### setFeatureEnabled

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setFeatureEnabled(
    feature: String, 
    enabled: Boolean
): Unit
```

Sets whether a feature is to be enabled (`true`) or disabled (`false`). If `enabled` is `true`, the feature is requested to be present. Otherwise, the feature is requested to be not present.

| Parameters ||
|---|---|
| `feature` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the name of a `https://developer.android.com/reference/kotlin/android/media/MediaCodecInfo.CodecCapabilities` feature. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/MediaCodecList#findDecoderForFormat(android.media.MediaFormat)`
- `https://developer.android.com/reference/kotlin/android/media/MediaCodecList#findEncoderForFormat(android.media.MediaFormat)`
- `https://developer.android.com/reference/kotlin/android/media/MediaCodecInfo.CodecCapabilities#isFormatSupported(android.media.MediaFormat)`

### setFloat

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setFloat(
    name: String, 
    value: Float
): Unit
```

Sets the value of a float key.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

### setInteger

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setInteger(
    name: String, 
    value: Int
): Unit
```

Sets the value of an integer key.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

### setLong

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setLong(
    name: String, 
    value: Long
): Unit
```

Sets the value of a long key.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

### setString

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setString(
    name: String, 
    value: String?
): Unit
```

Sets the value of a string key.

If value is `null`, it sets a null value that behaves similarly to a missing key. This could be used prior to API level `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int` to effectively remove a key.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `value` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |

### toString

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | This value cannot be `null`. |
