# StreamingServiceCallback

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StreamingServiceCallback

Kotlin| [Java](https://developer.android.com/reference/android/telephony/mbms/StreamingServiceCallback "View this page in Java") 

```
open class StreamingServiceCallback
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.telephony.mbms.StreamingServiceCallback](https://developer.android.com/reference/kotlin/android/telephony/mbms/StreamingServiceCallback#) |

A callback class for use when the application is actively streaming content. The middleware will provide updates on the status of the stream via this callback.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SIGNAL_STRENGTH_UNAVAILABLE](https://developer.android.com/reference/kotlin/android/telephony/mbms/StreamingServiceCallback#SIGNAL_STRENGTH_UNAVAILABLE:kotlin.Int) Indicates broadcast signal strength is not available for this service. |

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [StreamingServiceCallback](https://developer.android.com/reference/kotlin/android/telephony/mbms/StreamingServiceCallback#StreamingServiceCallback())`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onBroadcastSignalStrengthUpdated](https://developer.android.com/reference/kotlin/android/telephony/mbms/StreamingServiceCallback#onBroadcastSignalStrengthUpdated(kotlin.Int))`(`signalStrength:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Broadcast Signal Strength updated. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onError](https://developer.android.com/reference/kotlin/android/telephony/mbms/StreamingServiceCallback#onError(kotlin.Int,%20kotlin.String))`(`errorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Called by the middleware when it has detected an error condition in this stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onMediaDescriptionUpdated](https://developer.android.com/reference/kotlin/android/telephony/mbms/StreamingServiceCallback#onMediaDescriptionUpdated())`()` Called to indicate the mpd of a the stream has changed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStreamMethodUpdated](https://developer.android.com/reference/kotlin/android/telephony/mbms/StreamingServiceCallback#onStreamMethodUpdated(kotlin.Int))`(`methodType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Notify of bcast/unicast method being used. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStreamStateUpdated](https://developer.android.com/reference/kotlin/android/telephony/mbms/StreamingServiceCallback#onStreamStateUpdated(kotlin.Int,%20kotlin.Int))`(`state:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `reason:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called to indicate this stream has changed state. |

## Constants

### SIGNAL_STRENGTH_UNAVAILABLE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SIGNAL_STRENGTH_UNAVAILABLE: Int
```

Indicates broadcast signal strength is not available for this service. This may be due to the service no longer being available due to geography or timing (end of service) or because lack of demand has caused the service to be delivered via unicast. 

 Value: -1

## Public constructors

### StreamingServiceCallback

```
StreamingServiceCallback()
```

## Public methods

### onBroadcastSignalStrengthUpdated

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onBroadcastSignalStrengthUpdated(signalStrength: Int): Unit
```

Broadcast Signal Strength updated. This signal strength is the BROADCAST signal strength which, depending on technology in play and it's deployment, may be stronger or weaker than the traditional UNICAST signal strength. It a simple int from 0-4 for valid levels or [SIGNAL_STRENGTH_UNAVAILABLE](https://developer.android.com/reference/kotlin/android/telephony/mbms/StreamingServiceCallback#SIGNAL_STRENGTH_UNAVAILABLE:kotlin.Int) if broadcast is not available for this service due to timing, geography or popularity. 

### onError

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onError(
    errorCode: Int, 
    message: String?
): Unit
```

Called by the middleware when it has detected an error condition in this stream. The possible error codes are listed in [MbmsErrors](https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsErrors).

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `errorCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The error code. Value is [android.telephony.mbms.MbmsErrors#ERROR_NO_UNIQUE_MIDDLEWARE](https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsErrors#ERROR_NO_UNIQUE_MIDDLEWARE:kotlin.Int), [android.telephony.mbms.MbmsErrors#ERROR_MIDDLEWARE_LOST](https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsErrors#ERROR_MIDDLEWARE_LOST:kotlin.Int), [android.telephony.mbms.MbmsErrors#ERROR_MIDDLEWARE_NOT_BOUND](https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsErrors#ERROR_MIDDLEWARE_NOT_BOUND:kotlin.Int), [android.telephony.mbms.MbmsErrors.GeneralErrors#ERROR_MIDDLEWARE_NOT_YET_READY](https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsErrors.GeneralErrors#ERROR_MIDDLEWARE_NOT_YET_READY:kotlin.Int), [android.telephony.mbms.MbmsErrors.GeneralErrors#ERROR_OUT_OF_MEMORY](https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsErrors.GeneralErrors#ERROR_OUT_OF_MEMORY:kotlin.Int), [android.telephony.mbms.MbmsErrors.GeneralErrors#ERROR_MIDDLEWARE_TEMPORARILY_UNAVAILABLE](https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsErrors.GeneralErrors#ERROR_MIDDLEWARE_TEMPORARILY_UNAVAILABLE:kotlin.Int), [android.telephony.mbms.MbmsErrors.GeneralErrors#ERROR_IN_E911](https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsErrors.GeneralErrors#ERROR_IN_E911:kotlin.Int), [android.telephony.mbms.MbmsErrors.GeneralErrors#ERROR_NOT_CONNECTED_TO_HOME_CARRIER_LTE](https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsErrors.GeneralErrors#ERROR_NOT_CONNECTED_TO_HOME_CARRIER_LTE:kotlin.Int), [android.telephony.mbms.MbmsErrors.GeneralErrors#ERROR_UNABLE_TO_READ_SIM](https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsErrors.GeneralErrors#ERROR_UNABLE_TO_READ_SIM:kotlin.Int), [android.telephony.mbms.MbmsErrors.GeneralErrors#ERROR_CARRIER_CHANGE_NOT_ALLOWED](https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsErrors.GeneralErrors#ERROR_CARRIER_CHANGE_NOT_ALLOWED:kotlin.Int), [android.telephony.mbms.MbmsErrors.StreamingErrors#ERROR_CONCURRENT_SERVICE_LIMIT_REACHED](https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsErrors.StreamingErrors#ERROR_CONCURRENT_SERVICE_LIMIT_REACHED:kotlin.Int), [android.telephony.mbms.MbmsErrors.StreamingErrors#ERROR_UNABLE_TO_START_SERVICE](https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsErrors.StreamingErrors#ERROR_UNABLE_TO_START_SERVICE:kotlin.Int), or [android.telephony.mbms.MbmsErrors.StreamingErrors#ERROR_DUPLICATE_START_STREAM](https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsErrors.StreamingErrors#ERROR_DUPLICATE_START_STREAM:kotlin.Int) |
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:A human-readable message generated by the middleware for debugging purposes. This value may be`null`. |

### onMediaDescriptionUpdated

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onMediaDescriptionUpdated(): Unit
```

Called to indicate the mpd of a the stream has changed. Depending on the Dash Client it may need to be either reset (less drastic, but original spec didn't allow mpd to change so not always supported) or restarted. This may be called when a looping stream hits the end or when parameters have changed to account for time drift. 

### onStreamMethodUpdated

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onStreamMethodUpdated(methodType: Int): Unit
```

Notify of bcast/unicast method being used. This is intended to be informational. Indicates whether we're able to use cell broadcast or have had to fallback to unicast for this stream. This must be called once at the beginning of the stream around the same time as we change to STATE_STARTED, but strict ordering is not specified. It must be called again if we change modes, but if that doesn't happen the callback won't be used again. See [StreamingService.BROADCAST_METHOD](https://developer.android.com/reference/kotlin/android/telephony/mbms/StreamingService#BROADCAST_METHOD:kotlin.Int) and [StreamingService.UNICAST_METHOD](https://developer.android.com/reference/kotlin/android/telephony/mbms/StreamingService#UNICAST_METHOD:kotlin.Int) 

### onStreamStateUpdated

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onStreamStateUpdated(
    state: Int, 
    reason: Int
): Unit
```

Called to indicate this stream has changed state. See [StreamingService.STATE_STOPPED](https://developer.android.com/reference/kotlin/android/telephony/mbms/StreamingService#STATE_STOPPED:kotlin.Int), [StreamingService.STATE_STARTED](https://developer.android.com/reference/kotlin/android/telephony/mbms/StreamingService#STATE_STARTED:kotlin.Int) and [StreamingService.STATE_STALLED](https://developer.android.com/reference/kotlin/android/telephony/mbms/StreamingService#STATE_STALLED:kotlin.Int).

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `state` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.telephony.mbms.StreamingService#STATE_STOPPED](https://developer.android.com/reference/kotlin/android/telephony/mbms/StreamingService#STATE_STOPPED:kotlin.Int), [android.telephony.mbms.StreamingService#STATE_STARTED](https://developer.android.com/reference/kotlin/android/telephony/mbms/StreamingService#STATE_STARTED:kotlin.Int), or [android.telephony.mbms.StreamingService#STATE_STALLED](https://developer.android.com/reference/kotlin/android/telephony/mbms/StreamingService#STATE_STALLED:kotlin.Int) |
| `reason` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.telephony.mbms.StreamingService#REASON_BY_USER_REQUEST](https://developer.android.com/reference/kotlin/android/telephony/mbms/StreamingService#REASON_BY_USER_REQUEST:kotlin.Int), [android.telephony.mbms.StreamingService#REASON_END_OF_SESSION](https://developer.android.com/reference/kotlin/android/telephony/mbms/StreamingService#REASON_END_OF_SESSION:kotlin.Int), [android.telephony.mbms.StreamingService#REASON_FREQUENCY_CONFLICT](https://developer.android.com/reference/kotlin/android/telephony/mbms/StreamingService#REASON_FREQUENCY_CONFLICT:kotlin.Int), [android.telephony.mbms.StreamingService#REASON_OUT_OF_MEMORY](https://developer.android.com/reference/kotlin/android/telephony/mbms/StreamingService#REASON_OUT_OF_MEMORY:kotlin.Int), [android.telephony.mbms.StreamingService#REASON_NOT_CONNECTED_TO_HOMECARRIER_LTE](https://developer.android.com/reference/kotlin/android/telephony/mbms/StreamingService#REASON_NOT_CONNECTED_TO_HOMECARRIER_LTE:kotlin.Int), [android.telephony.mbms.StreamingService#REASON_LEFT_MBMS_BROADCAST_AREA](https://developer.android.com/reference/kotlin/android/telephony/mbms/StreamingService#REASON_LEFT_MBMS_BROADCAST_AREA:kotlin.Int), or [android.telephony.mbms.StreamingService#REASON_NONE](https://developer.android.com/reference/kotlin/android/telephony/mbms/StreamingService#REASON_NONE:kotlin.Int) |
