# StreamingServiceCallback

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StreamingServiceCallback

Kotlin| [Java](../android/telephony/mbms/StreamingServiceCallback.md) 
| --- | --- |

```
open class StreamingServiceCallback
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telephony.mbms.StreamingServiceCallback](../android/telephony/mbms/StreamingServiceCallback.md) |

A callback class for use when the application is actively streaming content. The middleware will provide updates on the status of the stream via this callback.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SIGNAL_STRENGTH_UNAVAILABLE](../android/telephony/mbms/StreamingServiceCallback.md) Indicates broadcast signal strength is not available for this service. |

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [StreamingServiceCallback](../android/telephony/mbms/StreamingServiceCallback.md))`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onBroadcastSignalStrengthUpdated](../android/telephony/mbms/StreamingServiceCallback.md))`(`signalStrength:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Broadcast Signal Strength updated. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onError](../android/telephony/mbms/StreamingServiceCallback.md))`(`errorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Called by the middleware when it has detected an error condition in this stream. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onMediaDescriptionUpdated](../android/telephony/mbms/StreamingServiceCallback.md))`()` Called to indicate the mpd of a the stream has changed. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStreamMethodUpdated](../android/telephony/mbms/StreamingServiceCallback.md))`(`methodType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Notify of bcast/unicast method being used. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStreamStateUpdated](../android/telephony/mbms/StreamingServiceCallback.md))`(`state:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `reason:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called to indicate this stream has changed state. |

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

Broadcast Signal Strength updated. This signal strength is the BROADCAST signal strength which, depending on technology in play and it's deployment, may be stronger or weaker than the traditional UNICAST signal strength. It a simple int from 0-4 for valid levels or [SIGNAL_STRENGTH_UNAVAILABLE](../android/telephony/mbms/StreamingServiceCallback.md) if broadcast is not available for this service due to timing, geography or popularity. 

### onError

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onError(
    errorCode: Int, 
    message: String?
): Unit
```

Called by the middleware when it has detected an error condition in this stream. The possible error codes are listed in [MbmsErrors](../android/telephony/mbms/MbmsErrors.md).

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `errorCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The error code. Value is [android.telephony.mbms.MbmsErrors#ERROR_NO_UNIQUE_MIDDLEWARE](../android/telephony/mbms/MbmsErrors.md), [android.telephony.mbms.MbmsErrors#ERROR_MIDDLEWARE_LOST](../android/telephony/mbms/MbmsErrors.md), [android.telephony.mbms.MbmsErrors#ERROR_MIDDLEWARE_NOT_BOUND](../android/telephony/mbms/MbmsErrors.md), [android.telephony.mbms.MbmsErrors.GeneralErrors#ERROR_MIDDLEWARE_NOT_YET_READY](../android/telephony/mbms/MbmsErrors.GeneralErrors.md), [android.telephony.mbms.MbmsErrors.GeneralErrors#ERROR_OUT_OF_MEMORY](../android/telephony/mbms/MbmsErrors.GeneralErrors.md), [android.telephony.mbms.MbmsErrors.GeneralErrors#ERROR_MIDDLEWARE_TEMPORARILY_UNAVAILABLE](../android/telephony/mbms/MbmsErrors.GeneralErrors.md), [android.telephony.mbms.MbmsErrors.GeneralErrors#ERROR_IN_E911](../android/telephony/mbms/MbmsErrors.GeneralErrors.md), [android.telephony.mbms.MbmsErrors.GeneralErrors#ERROR_NOT_CONNECTED_TO_HOME_CARRIER_LTE](../android/telephony/mbms/MbmsErrors.GeneralErrors.md), [android.telephony.mbms.MbmsErrors.GeneralErrors#ERROR_UNABLE_TO_READ_SIM](../android/telephony/mbms/MbmsErrors.GeneralErrors.md), [android.telephony.mbms.MbmsErrors.GeneralErrors#ERROR_CARRIER_CHANGE_NOT_ALLOWED](../android/telephony/mbms/MbmsErrors.GeneralErrors.md), [android.telephony.mbms.MbmsErrors.StreamingErrors#ERROR_CONCURRENT_SERVICE_LIMIT_REACHED](../android/telephony/mbms/MbmsErrors.StreamingErrors.md), [android.telephony.mbms.MbmsErrors.StreamingErrors#ERROR_UNABLE_TO_START_SERVICE](../android/telephony/mbms/MbmsErrors.StreamingErrors.md), or [android.telephony.mbms.MbmsErrors.StreamingErrors#ERROR_DUPLICATE_START_STREAM](../android/telephony/mbms/MbmsErrors.StreamingErrors.md) |
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

Notify of bcast/unicast method being used. This is intended to be informational. Indicates whether we're able to use cell broadcast or have had to fallback to unicast for this stream. This must be called once at the beginning of the stream around the same time as we change to STATE_STARTED, but strict ordering is not specified. It must be called again if we change modes, but if that doesn't happen the callback won't be used again. See [StreamingService.BROADCAST_METHOD](../android/telephony/mbms/StreamingService.md) and [StreamingService.UNICAST_METHOD](../android/telephony/mbms/StreamingService.md) 

### onStreamStateUpdated

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onStreamStateUpdated(
    state: Int, 
    reason: Int
): Unit
```

Called to indicate this stream has changed state. See [StreamingService.STATE_STOPPED](../android/telephony/mbms/StreamingService.md), [StreamingService.STATE_STARTED](../android/telephony/mbms/StreamingService.md) and [StreamingService.STATE_STALLED](../android/telephony/mbms/StreamingService.md).

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `state` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.telephony.mbms.StreamingService#STATE_STOPPED](../android/telephony/mbms/StreamingService.md), [android.telephony.mbms.StreamingService#STATE_STARTED](../android/telephony/mbms/StreamingService.md), or [android.telephony.mbms.StreamingService#STATE_STALLED](../android/telephony/mbms/StreamingService.md) |
| `reason` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.telephony.mbms.StreamingService#REASON_BY_USER_REQUEST](../android/telephony/mbms/StreamingService.md), [android.telephony.mbms.StreamingService#REASON_END_OF_SESSION](../android/telephony/mbms/StreamingService.md), [android.telephony.mbms.StreamingService#REASON_FREQUENCY_CONFLICT](../android/telephony/mbms/StreamingService.md), [android.telephony.mbms.StreamingService#REASON_OUT_OF_MEMORY](../android/telephony/mbms/StreamingService.md), [android.telephony.mbms.StreamingService#REASON_NOT_CONNECTED_TO_HOMECARRIER_LTE](../android/telephony/mbms/StreamingService.md), [android.telephony.mbms.StreamingService#REASON_LEFT_MBMS_BROADCAST_AREA](../android/telephony/mbms/StreamingService.md), or [android.telephony.mbms.StreamingService#REASON_NONE](../android/telephony/mbms/StreamingService.md) |
