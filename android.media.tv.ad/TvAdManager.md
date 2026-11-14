Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TvAdManager

Kotlin | [Java](TvAdManager.md)
| --- | --- |

```
class TvAdManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.tv.ad.TvAdManager](TvAdManager.md) |

Central system API to the overall client-side TV AD architecture, which arbitrates interaction between applications and AD services.

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdManager.TvAdServiceCallback` Callback used to monitor status of the TV advertisement service. |

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdManager#ACTION_APP_LINK_COMMAND:kotlin.String` Broadcast intent action to send app command to TV app. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdManager#APP_LINK_KEY_BACK_URI:kotlin.String` Key for back URI in app link command. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdManager#APP_LINK_KEY_CLASS_NAME:kotlin.String` Key for class name in app link. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdManager#APP_LINK_KEY_COMMAND_TYPE:kotlin.String` Key for command type in app link command. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdManager#APP_LINK_KEY_PACKAGE_NAME:kotlin.String` Key for package name in app link. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdManager#APP_LINK_KEY_SERVICE_ID:kotlin.String` Key for service ID in app link command. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdManager#ERROR_BLOCKED:kotlin.Int` Error code for blocked contents. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdManager#ERROR_ENCRYPTED:kotlin.Int` Error code when the key or module is missing for the encrypted channel. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdManager#ERROR_NONE:kotlin.Int` No error. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdManager#ERROR_NOT_SUPPORTED:kotlin.Int` Error code for an unsupported channel. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdManager#ERROR_RESOURCE_UNAVAILABLE:kotlin.Int` Error code when resource (e.g. tuner) is unavailable. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdManager#ERROR_UNKNOWN:kotlin.Int` Unknown error code. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdManager#ERROR_UNKNOWN_CHANNEL:kotlin.Int` Error code when the current channel is an unknown channel. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdManager#ERROR_WEAK_SIGNAL:kotlin.Int` Error code for weak signal. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdManager#INTENT_KEY_AD_SERVICE_ID:kotlin.String` Intent key for TV AD service ID. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdManager#INTENT_KEY_CHANNEL_URI:kotlin.String` Intent key for TV channel URI. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdManager#INTENT_KEY_COMMAND_TYPE:kotlin.String` Intent key for command type. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdManager#INTENT_KEY_TV_INPUT_ID:kotlin.String` Intent key for TV input ID. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdManager#SESSION_DATA_KEY_AD_BUFFER:kotlin.String` An object of `https://developer.android.com/reference/kotlin/android/media/tv/AdBuffer.html#`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdManager#SESSION_DATA_KEY_AD_REQUEST:kotlin.String` An object of `https://developer.android.com/reference/kotlin/android/media/tv/AdRequest.html#`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdManager#SESSION_DATA_KEY_BROADCAST_INFO_REQUEST:kotlin.String` An object of `https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoRequest.html#`. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdManager#SESSION_DATA_KEY_REQUEST_ID:kotlin.String` The ID of `https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoRequest.html#`. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdManager#SESSION_DATA_TYPE_AD_BUFFER_READY:kotlin.String` Notifies the advertisement buffer is ready. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdManager#SESSION_DATA_TYPE_AD_REQUEST:kotlin.String` Sends an advertisement request to be processed by the related TV input. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdManager#SESSION_DATA_TYPE_BROADCAST_INFO_REQUEST:kotlin.String` Sends request for broadcast info. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdManager#SESSION_DATA_TYPE_REMOVE_BROADCAST_INFO_REQUEST:kotlin.String` Removes request for broadcast info. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdManager#SESSION_STATE_ERROR:kotlin.Int` Error state of AD service session. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdManager#SESSION_STATE_RUNNING:kotlin.Int` Running state of AD service session. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdManager#SESSION_STATE_STOPPED:kotlin.Int` Stopped (or not started) state of AD service session. |

| Public methods ||
|---|---|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [TvAdServiceInfo](TvAdServiceInfo.md)!\> | `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdManager#getTvAdServiceList()()` Returns the complete list of TV AD services on the system. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdManager#registerCallback(java.util.concurrent.Executor,%20android.media.tv.ad.TvAdManager.TvAdServiceCallback)(executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdManager.TvAdServiceCallback)` Registers a `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdManager.TvAdServiceCallback`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdManager#sendAppLinkCommand(kotlin.String,%20android.os.Bundle)(serviceId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, command: https://developer.android.com/reference/kotlin/android/os/Bundle.html#)` Sends app link command. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdManager#unregisterCallback(android.media.tv.ad.TvAdManager.TvAdServiceCallback)(callback: https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdManager.TvAdServiceCallback)` Unregisters the existing `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdManager.TvAdServiceCallback`. |

## Constants

### ACTION_APP_LINK_COMMAND

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_APP_LINK_COMMAND: String
```

Broadcast intent action to send app command to TV app.

 Value: "android.media.tv.ad.action.APP_LINK_COMMAND"

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdManager#sendAppLinkCommand(kotlin.String,%20android.os.Bundle)`

### APP_LINK_KEY_BACK_URI

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val APP_LINK_KEY_BACK_URI: String
```

Key for back URI in app link command.

Type: String

 Value: "back_uri"

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdManager#sendAppLinkCommand(kotlin.String,%20android.os.Bundle)`

### APP_LINK_KEY_CLASS_NAME

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val APP_LINK_KEY_CLASS_NAME: String
```

Key for class name in app link.

Type: String

 Value: "class_name"

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdManager#sendAppLinkCommand(kotlin.String,%20android.os.Bundle)`

### APP_LINK_KEY_COMMAND_TYPE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val APP_LINK_KEY_COMMAND_TYPE: String
```

Key for command type in app link command.

Type: String

 Value: "command_type"

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdManager#sendAppLinkCommand(kotlin.String,%20android.os.Bundle)`

### APP_LINK_KEY_PACKAGE_NAME

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val APP_LINK_KEY_PACKAGE_NAME: String
```

Key for package name in app link.

Type: String

 Value: "package_name"

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdManager#sendAppLinkCommand(kotlin.String,%20android.os.Bundle)`

### APP_LINK_KEY_SERVICE_ID

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val APP_LINK_KEY_SERVICE_ID: String
```

Key for service ID in app link command.

Type: String

 Value: "service_id"

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdManager#sendAppLinkCommand(kotlin.String,%20android.os.Bundle)`

### ERROR_BLOCKED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_BLOCKED: Int
```

Error code for blocked contents.

 Value: 5

### ERROR_ENCRYPTED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_ENCRYPTED: Int
```

Error code when the key or module is missing for the encrypted channel.

 Value: 6

### ERROR_NONE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_NONE: Int
```

No error.

 Value: 0

### ERROR_NOT_SUPPORTED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_NOT_SUPPORTED: Int
```

Error code for an unsupported channel.

 Value: 2

### ERROR_RESOURCE_UNAVAILABLE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_RESOURCE_UNAVAILABLE: Int
```

Error code when resource (e.g. tuner) is unavailable.

 Value: 4

### ERROR_UNKNOWN

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_UNKNOWN: Int
```

Unknown error code.

 Value: 1

### ERROR_UNKNOWN_CHANNEL

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_UNKNOWN_CHANNEL: Int
```

Error code when the current channel is an unknown channel.

 Value: 7

### ERROR_WEAK_SIGNAL

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_WEAK_SIGNAL: Int
```

Error code for weak signal.

 Value: 3

### INTENT_KEY_AD_SERVICE_ID

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INTENT_KEY_AD_SERVICE_ID: String
```

Intent key for TV AD service ID. It's used to send app command to TV app.

Type: String

 Value: "ad_service_id"

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdManager#sendAppLinkCommand(kotlin.String,%20android.os.Bundle)`
- `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdManager#ACTION_APP_LINK_COMMAND:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdServiceInfo#getId()`

### INTENT_KEY_CHANNEL_URI

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INTENT_KEY_CHANNEL_URI: String
```

Intent key for TV channel URI. It's used to send app command to TV app.

Type: android.net.Uri

 Value: "channel_uri"

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdManager#sendAppLinkCommand(kotlin.String,%20android.os.Bundle)`
- `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdManager#ACTION_APP_LINK_COMMAND:kotlin.String`

### INTENT_KEY_COMMAND_TYPE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INTENT_KEY_COMMAND_TYPE: String
```

Intent key for command type. It's used to send app command to TV app. The value of this key could vary according to TV apps.

Type: String

 Value: "command_type"

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdManager#sendAppLinkCommand(kotlin.String,%20android.os.Bundle)`
- `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdManager#ACTION_APP_LINK_COMMAND:kotlin.String`

### INTENT_KEY_TV_INPUT_ID

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INTENT_KEY_TV_INPUT_ID: String
```

Intent key for TV input ID. It's used to send app command to TV app.

Type: String

 Value: "tv_input_id"

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdManager#sendAppLinkCommand(kotlin.String,%20android.os.Bundle)`
- `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdManager#ACTION_APP_LINK_COMMAND:kotlin.String`

### SESSION_DATA_KEY_AD_BUFFER

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SESSION_DATA_KEY_AD_BUFFER: String
```

An object of `https://developer.android.com/reference/kotlin/android/media/tv/AdBuffer.html#`.

Type: android.media.tv.AdBuffer

 Value: "ad_buffer"

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdService.Session#sendTvAdSessionData(kotlin.String,%20android.os.Bundle)`

### SESSION_DATA_KEY_AD_REQUEST

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SESSION_DATA_KEY_AD_REQUEST: String
```

An object of `https://developer.android.com/reference/kotlin/android/media/tv/AdRequest.html#`.

Type: android.media.tv.AdRequest

 Value: "ad_request"

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdService.Session#sendTvAdSessionData(kotlin.String,%20android.os.Bundle)`

### SESSION_DATA_KEY_BROADCAST_INFO_REQUEST

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SESSION_DATA_KEY_BROADCAST_INFO_REQUEST: String
```

An object of `https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoRequest.html#`.

Type: android.media.tv.BroadcastInfoRequest

 Value: "broadcast_info_request"

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdService.Session#sendTvAdSessionData(kotlin.String,%20android.os.Bundle)`

### SESSION_DATA_KEY_REQUEST_ID

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SESSION_DATA_KEY_REQUEST_ID: String
```

The ID of `https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoRequest.html#`.

Type: Integer

 Value: "request_id"

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdService.Session#sendTvAdSessionData(kotlin.String,%20android.os.Bundle)`

### SESSION_DATA_TYPE_AD_BUFFER_READY

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SESSION_DATA_TYPE_AD_BUFFER_READY: String
```

Notifies the advertisement buffer is ready.

 Value: "ad_buffer_ready"

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdService.Session#sendTvAdSessionData(kotlin.String,%20android.os.Bundle)`
- `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdManager#SESSION_DATA_KEY_AD_BUFFER:kotlin.String`

### SESSION_DATA_TYPE_AD_REQUEST

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SESSION_DATA_TYPE_AD_REQUEST: String
```

Sends an advertisement request to be processed by the related TV input.

 Value: "ad_request"

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdService.Session#sendTvAdSessionData(kotlin.String,%20android.os.Bundle)`
- `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdManager#SESSION_DATA_KEY_AD_REQUEST:kotlin.String`

### SESSION_DATA_TYPE_BROADCAST_INFO_REQUEST

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SESSION_DATA_TYPE_BROADCAST_INFO_REQUEST: String
```

Sends request for broadcast info.

 Value: "broadcast_info_request"

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdService.Session#sendTvAdSessionData(kotlin.String,%20android.os.Bundle)`

### SESSION_DATA_TYPE_REMOVE_BROADCAST_INFO_REQUEST

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SESSION_DATA_TYPE_REMOVE_BROADCAST_INFO_REQUEST: String
```

Removes request for broadcast info.

 Value: "remove_broadcast_info_request"

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdService.Session#sendTvAdSessionData(kotlin.String,%20android.os.Bundle)`

### SESSION_STATE_ERROR

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SESSION_STATE_ERROR: Int
```

Error state of AD service session.

 Value: 3

### SESSION_STATE_RUNNING

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SESSION_STATE_RUNNING: Int
```

Running state of AD service session.

 Value: 2

### SESSION_STATE_STOPPED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SESSION_STATE_STOPPED: Int
```

Stopped (or not started) state of AD service session.

 Value: 1

## Public methods

### getTvAdServiceList

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTvAdServiceList(): MutableList<TvAdServiceInfo!>
```

Returns the complete list of TV AD services on the system.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdServiceInfo!>` | List of `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdServiceInfo` for each TV AD service that describes its meta information. This value cannot be `null`. |

### registerCallback

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun registerCallback(
    executor: Executor, 
    callback: TvAdManager.TvAdServiceCallback
): Unit
```

Registers a `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdManager.TvAdServiceCallback`.

| Parameters ||
|---|---|
| `executor` | [Executor](../java.util.concurrent/Executor.md): A `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that the status change will be delivered to. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. This value cannot be `null`. |
| `callback` | [TvAdManager.TvAdServiceCallback](../android/media/tv/ad/TvAdManager.TvAdServiceCallback.md): A callback used to monitor status of the TV AD services. This value cannot be `null`. |

### sendAppLinkCommand

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun sendAppLinkCommand(
    serviceId: String, 
    command: Bundle
): Unit
```

Sends app link command.

| Parameters ||
|---|---|
| `serviceId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The ID of TV AD service which the command to be sent to. The ID can be found in `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdServiceInfo#getId()`. This value cannot be `null`. |
| `command` | [Bundle](../android.os/Bundle.md): The command to be sent. The command is a bundle with the following keys: - `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdManager#APP_LINK_KEY_PACKAGE_NAME:kotlin.String`: The package name of the app to be launched. - `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdManager#APP_LINK_KEY_CLASS_NAME:kotlin.String`: The class name of the app to be launched. - `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdManager#APP_LINK_KEY_COMMAND_TYPE:kotlin.String`: The command type. - `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdManager#APP_LINK_KEY_SERVICE_ID:kotlin.String`: The ID of the TV AD service. - `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdManager#APP_LINK_KEY_BACK_URI:kotlin.String`: The URI to be used to return to the previous app. . This value cannot be `null`. |

### unregisterCallback

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun unregisterCallback(callback: TvAdManager.TvAdServiceCallback): Unit
```

Unregisters the existing `https://developer.android.com/reference/kotlin/android/media/tv/ad/TvAdManager.TvAdServiceCallback`.

| Parameters ||
|---|---|
| `callback` | [TvAdManager.TvAdServiceCallback](../android/media/tv/ad/TvAdManager.TvAdServiceCallback.md): The existing callback to remove. This value cannot be `null`. |
