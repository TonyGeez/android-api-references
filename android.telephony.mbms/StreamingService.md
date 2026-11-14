Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StreamingService

Kotlin | [Java](../android/telephony/mbms/StreamingService.md)
| --- | --- |

```
open class StreamingService : AutoCloseable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telephony.mbms.StreamingService](../android/telephony/mbms/StreamingService.md) |

Class used to represent a single MBMS stream. After a stream has been started with `https://developer.android.com/reference/kotlin/android/telephony/MbmsStreamingSession.html#startStreaming(android.telephony.mbms.StreamingServiceInfo,%20java.util.concurrent.Executor,%20android.telephony.mbms.StreamingServiceCallback)`, this class is used to hold information about the stream and control it.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/mbms/StreamingService#BROADCAST_METHOD:kotlin.Int` The method of transmission currently used for a stream, reported via `https://developer.android.com/reference/kotlin/android/telephony/mbms/StreamingServiceCallback#onStreamMethodUpdated(kotlin.Int)` |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/mbms/StreamingService#REASON_BY_USER_REQUEST:kotlin.Int` State changed due to a call to `https://developer.android.com/reference/kotlin/android/telephony/mbms/StreamingService#close()` or `https://developer.android.com/reference/kotlin/android/telephony/MbmsStreamingSession.html#startStreaming(android.telephony.mbms.StreamingServiceInfo,%20java.util.concurrent.Executor,%20android.telephony.mbms.StreamingServiceCallback)` |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/mbms/StreamingService#REASON_END_OF_SESSION:kotlin.Int` State changed due to the streaming session ending at the carrier. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/mbms/StreamingService#REASON_FREQUENCY_CONFLICT:kotlin.Int` State changed due to a frequency conflict with another requested stream. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/mbms/StreamingService#REASON_LEFT_MBMS_BROADCAST_AREA:kotlin.Int` State changed due to the device leaving the where this stream is being broadcast. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/mbms/StreamingService#REASON_NONE:kotlin.Int` Indicates that the middleware does not have a reason to provide for the state change. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/mbms/StreamingService#REASON_NOT_CONNECTED_TO_HOMECARRIER_LTE:kotlin.Int` State changed due to the device leaving the home carrier's LTE network. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/mbms/StreamingService#REASON_OUT_OF_MEMORY:kotlin.Int` State changed due to the middleware running out of memory |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/mbms/StreamingService#STATE_STALLED:kotlin.Int` <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/mbms/StreamingService#STATE_STARTED:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/mbms/StreamingService#STATE_STOPPED:kotlin.Int` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/mbms/StreamingService#UNICAST_METHOD:kotlin.Int` <br /> |
| --- | --- |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/mbms/StreamingService#close()()` Stop streaming this service. |
| open [StreamingServiceInfo](../android/telephony/mbms/StreamingServiceInfo.md)! | `https://developer.android.com/reference/kotlin/android/telephony/mbms/StreamingService#getInfo()()` Retrieve the `https://developer.android.com/reference/kotlin/android/telephony/mbms/StreamingServiceInfo` corresponding to this stream. |
| open [Uri](../android/net/Uri.md)? | `https://developer.android.com/reference/kotlin/android/telephony/mbms/StreamingService#getPlaybackUri()()` Retrieve the Uri used to play this stream. |
| --- | --- |

## Constants

### BROADCAST_METHOD

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BROADCAST_METHOD: Int
```

The method of transmission currently used for a stream, reported via `https://developer.android.com/reference/kotlin/android/telephony/mbms/StreamingServiceCallback#onStreamMethodUpdated(kotlin.Int)`

 Value: 1

### REASON_BY_USER_REQUEST

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REASON_BY_USER_REQUEST: Int
```

State changed due to a call to `https://developer.android.com/reference/kotlin/android/telephony/mbms/StreamingService#close()` or `https://developer.android.com/reference/kotlin/android/telephony/MbmsStreamingSession.html#startStreaming(android.telephony.mbms.StreamingServiceInfo,%20java.util.concurrent.Executor,%20android.telephony.mbms.StreamingServiceCallback)`

 Value: 1

### REASON_END_OF_SESSION

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REASON_END_OF_SESSION: Int
```

State changed due to the streaming session ending at the carrier.

 Value: 2

### REASON_FREQUENCY_CONFLICT

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REASON_FREQUENCY_CONFLICT: Int
```

State changed due to a frequency conflict with another requested stream.

 Value: 3

### REASON_LEFT_MBMS_BROADCAST_AREA

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REASON_LEFT_MBMS_BROADCAST_AREA: Int
```

State changed due to the device leaving the where this stream is being broadcast.

 Value: 6

### REASON_NONE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REASON_NONE: Int
```

Indicates that the middleware does not have a reason to provide for the state change.

 Value: 0

### REASON_NOT_CONNECTED_TO_HOMECARRIER_LTE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REASON_NOT_CONNECTED_TO_HOMECARRIER_LTE: Int
```

State changed due to the device leaving the home carrier's LTE network.

 Value: 5

### REASON_OUT_OF_MEMORY

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REASON_OUT_OF_MEMORY: Int
```

State changed due to the middleware running out of memory

 Value: 4

### STATE_STALLED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATE_STALLED: Int
```

 Value: 3

### STATE_STARTED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATE_STARTED: Int
```

 Value: 2

### STATE_STOPPED

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATE_STOPPED: Int
```

 Value: 1

### UNICAST_METHOD

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UNICAST_METHOD: Int
```

 Value: 2

## Public methods

### close

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun close(): Unit
```

Stop streaming this service. Further operations on this object will fail with an `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#`. May throw an `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#` or an `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#`

| Exceptions ||
|---|---|
| `java.lang.Exception` | if this resource cannot be closed |

### getInfo

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getInfo(): StreamingServiceInfo!
```

Retrieve the `https://developer.android.com/reference/kotlin/android/telephony/mbms/StreamingServiceInfo` corresponding to this stream.

### getPlaybackUri

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPlaybackUri(): Uri?
```

Retrieve the Uri used to play this stream. May throw an `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#` or an `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/Uri.html#?` | The `https://developer.android.com/reference/kotlin/android/net/Uri.html#` to pass to the streaming client, or `null` if an error occurred. |
