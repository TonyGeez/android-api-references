# TvInteractiveAppManager

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TvInteractiveAppManager

Kotlin| [Java](../android/media/tv/interactive/TvInteractiveAppManager.md) 
| --- | --- |

```
class TvInteractiveAppManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.tv.interactive.TvInteractiveAppManager](../android/media/tv/interactive/TvInteractiveAppManager.md) |

Central system API to the overall TV interactive application framework (TIAF) architecture, which arbitrates interaction between Android applications and TV interactive apps.

## Summary

| Nested classes ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [TvInteractiveAppCallback](../android/media/tv/interactive/TvInteractiveAppManager.TvInteractiveAppCallback.md) Callback used to monitor status of the TV Interactive App. |

| Constants ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_APP_LINK_COMMAND](../android/media/tv/interactive/TvInteractiveAppManager.md) Broadcast intent action to send app command to TV app. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [APP_LINK_KEY_BACK_URI](../android/media/tv/interactive/TvInteractiveAppManager.md) Key for back URI in app link command. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [APP_LINK_KEY_CLASS_NAME](../android/media/tv/interactive/TvInteractiveAppManager.md) Key for class name in app link. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [APP_LINK_KEY_COMMAND_TYPE](../android/media/tv/interactive/TvInteractiveAppManager.md) Key for command type in app link command. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [APP_LINK_KEY_PACKAGE_NAME](../android/media/tv/interactive/TvInteractiveAppManager.md) Key for package name in app link. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [APP_LINK_KEY_SERVICE_ID](../android/media/tv/interactive/TvInteractiveAppManager.md) Key for service ID in app link command. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_BLOCKED](../android/media/tv/interactive/TvInteractiveAppManager.md) Error code for blocked contents. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_ENCRYPTED](../android/media/tv/interactive/TvInteractiveAppManager.md) Error code when the key or module is missing for the encrypted channel. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_NONE](../android/media/tv/interactive/TvInteractiveAppManager.md) No error. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_NOT_SUPPORTED](../android/media/tv/interactive/TvInteractiveAppManager.md) Error code for an unsupported channel. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_RESOURCE_UNAVAILABLE](../android/media/tv/interactive/TvInteractiveAppManager.md) Error code when resource (e.g. tuner) is unavailable. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_UNKNOWN](../android/media/tv/interactive/TvInteractiveAppManager.md) Unknown error code. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_UNKNOWN_CHANNEL](../android/media/tv/interactive/TvInteractiveAppManager.md) Error code when the current channel is an unknown channel. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_WEAK_SIGNAL](../android/media/tv/interactive/TvInteractiveAppManager.md) Error code for weak signal. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [INTENT_KEY_BI_INTERACTIVE_APP_TYPE](../android/media/tv/interactive/TvInteractiveAppManager.md) Intent key for broadcast-independent(BI) interactive app type. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [INTENT_KEY_BI_INTERACTIVE_APP_URI](../android/media/tv/interactive/TvInteractiveAppManager.md) Intent key for broadcast-independent(BI) interactive app URI. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [INTENT_KEY_CHANNEL_URI](../android/media/tv/interactive/TvInteractiveAppManager.md) Intent key for TV channel URI. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [INTENT_KEY_COMMAND_TYPE](../android/media/tv/interactive/TvInteractiveAppManager.md) Intent key for command type. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [INTENT_KEY_INTERACTIVE_APP_SERVICE_ID](../android/media/tv/interactive/TvInteractiveAppManager.md) Intent key for TV interactive app ID. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [INTENT_KEY_TV_INPUT_ID](../android/media/tv/interactive/TvInteractiveAppManager.md) Intent key for TV input ID. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INTERACTIVE_APP_STATE_ERROR](../android/media/tv/interactive/TvInteractiveAppManager.md) Error state of interactive application. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INTERACTIVE_APP_STATE_RUNNING](../android/media/tv/interactive/TvInteractiveAppManager.md) Running state of interactive application. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INTERACTIVE_APP_STATE_STOPPED](../android/media/tv/interactive/TvInteractiveAppManager.md) Stopped (or not started) state of interactive application. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SERVICE_STATE_ERROR](../android/media/tv/interactive/TvInteractiveAppManager.md) Error state of interactive app service. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SERVICE_STATE_PREPARING](../android/media/tv/interactive/TvInteractiveAppManager.md) Preparing state of interactive app service. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SERVICE_STATE_READY](../android/media/tv/interactive/TvInteractiveAppManager.md) Ready state of interactive app service. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SERVICE_STATE_UNREALIZED](../android/media/tv/interactive/TvInteractiveAppManager.md) Unrealized state of interactive app service. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TELETEXT_APP_STATE_ERROR](../android/media/tv/interactive/TvInteractiveAppManager.md) State of Teletext app: error |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TELETEXT_APP_STATE_HIDE](../android/media/tv/interactive/TvInteractiveAppManager.md) State of Teletext app: hide |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TELETEXT_APP_STATE_SHOW](../android/media/tv/interactive/TvInteractiveAppManager.md) State of Teletext app: show |
| --- | --- |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [AppLinkInfo](../android/media/tv/interactive/AppLinkInfo.md)!\> | [getAppLinkInfoList](../android/media/tv/interactive/TvInteractiveAppManager.md))`()` Returns a list of available app link information. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [TvInteractiveAppServiceInfo](../android/media/tv/interactive/TvInteractiveAppServiceInfo.md)!\> | [getTvInteractiveAppServiceList](../android/media/tv/interactive/TvInteractiveAppManager.md))`()` Returns the complete list of TV Interactive App service on the system. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerAppLinkInfo](../android/media/tv/interactive/TvInteractiveAppManager.md))`(`tvIAppServiceId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `appLinkInfo:` ` [AppLinkInfo](../android/media/tv/interactive/AppLinkInfo.md)`)` Registers an Android application link info record which can be used to launch the specific Android application by TV interactive App RTE. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerCallback](../android/media/tv/interactive/TvInteractiveAppManager.md))`(`executor:` ` [Executor](../java/util/concurrent/Executor.md)`, `callback:` ` [TvInteractiveAppManager.TvInteractiveAppCallback](../android/media/tv/interactive/TvInteractiveAppManager.TvInteractiveAppCallback.md)`)` Registers a [TvInteractiveAppCallback](../android/media/tv/interactive/TvInteractiveAppManager.TvInteractiveAppCallback.md). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendAppLinkCommand](../android/media/tv/interactive/TvInteractiveAppManager.md))`(`tvIAppServiceId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `command:` ` [Bundle](../android/os/Bundle.md)`)` Sends app link command. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterAppLinkInfo](../android/media/tv/interactive/TvInteractiveAppManager.md))`(`tvIAppServiceId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `appLinkInfo:` ` [AppLinkInfo](../android/media/tv/interactive/AppLinkInfo.md)`)` Unregisters an Android application link info record which can be used to launch the specific Android application by TV interactive App RTE. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterCallback](../android/media/tv/interactive/TvInteractiveAppManager.md))`(`callback:` ` [TvInteractiveAppManager.TvInteractiveAppCallback](../android/media/tv/interactive/TvInteractiveAppManager.TvInteractiveAppCallback.md)`)` Unregisters the existing [TvInteractiveAppCallback](../android/media/tv/interactive/TvInteractiveAppManager.TvInteractiveAppCallback.md). |

## Constants

### ACTION_APP_LINK_COMMAND

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_APP_LINK_COMMAND: String
```

Broadcast intent action to send app command to TV app. 

 Value: "android.media.tv.interactive.action.APP_LINK_COMMAND"

**See Also**

- [#sendAppLinkCommand(String, Bundle)](../android/media/tv/interactive/TvInteractiveAppManager.md)) 

### APP_LINK_KEY_BACK_URI

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val APP_LINK_KEY_BACK_URI: String
```

Key for back URI in app link command.

Type: String 

 Value: "back_uri"

**See Also**

- [#sendAppLinkCommand(String, Bundle)](../android/media/tv/interactive/TvInteractiveAppManager.md)) 

### APP_LINK_KEY_CLASS_NAME

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val APP_LINK_KEY_CLASS_NAME: String
```

Key for class name in app link.

Type: String 

 Value: "class_name"

**See Also**

- [#sendAppLinkCommand(String, Bundle)](../android/media/tv/interactive/TvInteractiveAppManager.md)) 

### APP_LINK_KEY_COMMAND_TYPE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val APP_LINK_KEY_COMMAND_TYPE: String
```

Key for command type in app link command.

Type: String 

 Value: "command_type"

**See Also**

- [#sendAppLinkCommand(String, Bundle)](../android/media/tv/interactive/TvInteractiveAppManager.md)) 

### APP_LINK_KEY_PACKAGE_NAME

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val APP_LINK_KEY_PACKAGE_NAME: String
```

Key for package name in app link.

Type: String 

 Value: "package_name"

**See Also**

- [#sendAppLinkCommand(String, Bundle)](../android/media/tv/interactive/TvInteractiveAppManager.md)) 

### APP_LINK_KEY_SERVICE_ID

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val APP_LINK_KEY_SERVICE_ID: String
```

Key for service ID in app link command.

Type: String 

 Value: "service_id"

**See Also**

- [#sendAppLinkCommand(String, Bundle)](../android/media/tv/interactive/TvInteractiveAppManager.md)) 

### ERROR_BLOCKED

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_BLOCKED: Int
```

Error code for blocked contents. 

 Value: 5

### ERROR_ENCRYPTED

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_ENCRYPTED: Int
```

Error code when the key or module is missing for the encrypted channel. 

 Value: 6

### ERROR_NONE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_NONE: Int
```

No error. 

 Value: 0

### ERROR_NOT_SUPPORTED

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_NOT_SUPPORTED: Int
```

Error code for an unsupported channel. 

 Value: 2

### ERROR_RESOURCE_UNAVAILABLE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_RESOURCE_UNAVAILABLE: Int
```

Error code when resource (e.g. tuner) is unavailable. 

 Value: 4

### ERROR_UNKNOWN

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_UNKNOWN: Int
```

Unknown error code. 

 Value: 1

### ERROR_UNKNOWN_CHANNEL

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_UNKNOWN_CHANNEL: Int
```

Error code when the current channel is an unknown channel. 

 Value: 7

### ERROR_WEAK_SIGNAL

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_WEAK_SIGNAL: Int
```

Error code for weak signal. 

 Value: 3

### INTENT_KEY_BI_INTERACTIVE_APP_TYPE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INTENT_KEY_BI_INTERACTIVE_APP_TYPE: String
```

Intent key for broadcast-independent(BI) interactive app type. It's used to send app command to TV app.

Type: int 

 Value: "bi_interactive_app_type"

**See Also**

- [#sendAppLinkCommand(String, Bundle)](../android/media/tv/interactive/TvInteractiveAppManager.md))
- [#ACTION_APP_LINK_COMMAND](../android/media/tv/interactive/TvInteractiveAppManager.md)
- [android.media.tv.interactive.TvInteractiveAppServiceInfo#getSupportedTypes()](../android/media/tv/interactive/TvInteractiveAppServiceInfo.md))
- [android.media.tv.interactive.TvInteractiveAppView#createBiInteractiveApp(Uri, Bundle)](../android/media/tv/interactive/TvInteractiveAppView.md)) 

### INTENT_KEY_BI_INTERACTIVE_APP_URI

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INTENT_KEY_BI_INTERACTIVE_APP_URI: String
```

Intent key for broadcast-independent(BI) interactive app URI. It's used to send app command to TV app.

Type: android.net.Uri 

 Value: "bi_interactive_app_uri"

**See Also**

- [#sendAppLinkCommand(String, Bundle)](../android/media/tv/interactive/TvInteractiveAppManager.md))
- [#ACTION_APP_LINK_COMMAND](../android/media/tv/interactive/TvInteractiveAppManager.md)
- [android.media.tv.interactive.TvInteractiveAppView#createBiInteractiveApp(Uri, Bundle)](../android/media/tv/interactive/TvInteractiveAppView.md)) 

### INTENT_KEY_CHANNEL_URI

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INTENT_KEY_CHANNEL_URI: String
```

Intent key for TV channel URI. It's used to send app command to TV app.

Type: android.net.Uri 

 Value: "channel_uri"

**See Also**

- [#sendAppLinkCommand(String, Bundle)](../android/media/tv/interactive/TvInteractiveAppManager.md))
- [#ACTION_APP_LINK_COMMAND](../android/media/tv/interactive/TvInteractiveAppManager.md) 

### INTENT_KEY_COMMAND_TYPE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INTENT_KEY_COMMAND_TYPE: String
```

Intent key for command type. It's used to send app command to TV app. The value of this key could vary according to TV apps.

Type: String 

 Value: "command_type"

**See Also**

- [#sendAppLinkCommand(String, Bundle)](../android/media/tv/interactive/TvInteractiveAppManager.md))
- [#ACTION_APP_LINK_COMMAND](../android/media/tv/interactive/TvInteractiveAppManager.md) 

### INTENT_KEY_INTERACTIVE_APP_SERVICE_ID

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INTENT_KEY_INTERACTIVE_APP_SERVICE_ID: String
```

Intent key for TV interactive app ID. It's used to send app command to TV app.

Type: String 

 Value: "interactive_app_id"

**See Also**

- [#sendAppLinkCommand(String, Bundle)](../android/media/tv/interactive/TvInteractiveAppManager.md))
- [#ACTION_APP_LINK_COMMAND](../android/media/tv/interactive/TvInteractiveAppManager.md)
- [android.media.tv.interactive.TvInteractiveAppServiceInfo#getId()](../android/media/tv/interactive/TvInteractiveAppServiceInfo.md)) 

### INTENT_KEY_TV_INPUT_ID

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INTENT_KEY_TV_INPUT_ID: String
```

Intent key for TV input ID. It's used to send app command to TV app.

Type: String 

 Value: "tv_input_id"

**See Also**

- [#sendAppLinkCommand(String, Bundle)](../android/media/tv/interactive/TvInteractiveAppManager.md))
- [#ACTION_APP_LINK_COMMAND](../android/media/tv/interactive/TvInteractiveAppManager.md) 

### INTERACTIVE_APP_STATE_ERROR

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INTERACTIVE_APP_STATE_ERROR: Int
```

Error state of interactive application. 

 Value: 3

### INTERACTIVE_APP_STATE_RUNNING

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INTERACTIVE_APP_STATE_RUNNING: Int
```

Running state of interactive application. 

 Value: 2

### INTERACTIVE_APP_STATE_STOPPED

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INTERACTIVE_APP_STATE_STOPPED: Int
```

Stopped (or not started) state of interactive application. 

 Value: 1

### SERVICE_STATE_ERROR

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SERVICE_STATE_ERROR: Int
```

Error state of interactive app service. 

 Value: 4

### SERVICE_STATE_PREPARING

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SERVICE_STATE_PREPARING: Int
```

Preparing state of interactive app service. 

 Value: 2

### SERVICE_STATE_READY

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SERVICE_STATE_READY: Int
```

Ready state of interactive app service.

In this state, the interactive app service is ready, and interactive apps can be started. 

 Value: 3

**See Also**

- [android.media.tv.interactive.TvInteractiveAppView#startInteractiveApp()](../android/media/tv/interactive/TvInteractiveAppView.md)) 

### SERVICE_STATE_UNREALIZED

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SERVICE_STATE_UNREALIZED: Int
```

Unrealized state of interactive app service. 

 Value: 1

### TELETEXT_APP_STATE_ERROR

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TELETEXT_APP_STATE_ERROR: Int
```

State of Teletext app: error 

 Value: 3

### TELETEXT_APP_STATE_HIDE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TELETEXT_APP_STATE_HIDE: Int
```

State of Teletext app: hide 

 Value: 2

### TELETEXT_APP_STATE_SHOW

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TELETEXT_APP_STATE_SHOW: Int
```

State of Teletext app: show 

 Value: 1

## Public methods

### getAppLinkInfoList

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAppLinkInfoList(): MutableList<AppLinkInfo!>
```

Returns a list of available app link information.

A package must declare its app link info in its manifest using meta-data tag, so the info can be detected by the system.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [AppLinkInfo](../android/media/tv/interactive/AppLinkInfo.md)!> | List of [AppLinkInfo](../android/media/tv/interactive/AppLinkInfo.md) for each package that deslares its app link information. This value cannot be`null`. |

### getTvInteractiveAppServiceList

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTvInteractiveAppServiceList(): MutableList<TvInteractiveAppServiceInfo!>
```

Returns the complete list of TV Interactive App service on the system.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [TvInteractiveAppServiceInfo](../android/media/tv/interactive/TvInteractiveAppServiceInfo.md)!> | List of [TvInteractiveAppServiceInfo](../android/media/tv/interactive/TvInteractiveAppServiceInfo.md) for each TV Interactive App service that describes its meta information. This value cannot be`null`. |

### registerAppLinkInfo

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun registerAppLinkInfo(
    tvIAppServiceId: String, 
    appLinkInfo: AppLinkInfo
): Unit
```

Registers an Android application link info record which can be used to launch the specific Android application by TV interactive App RTE.

| Parameters ||
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tvIAppServiceId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The ID of TV interactive service which the command to be sent to. The ID can be found in [TvInteractiveAppServiceInfo.getId()](../android/media/tv/interactive/TvInteractiveAppServiceInfo.md)). This value cannot be`null`. |
| `appLinkInfo` | [AppLinkInfo](../android/media/tv/interactive/AppLinkInfo.md):The Android application link info record to be registered. This value cannot be`null`. |

### registerCallback

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun registerCallback(
    executor: Executor, 
    callback: TvInteractiveAppManager.TvInteractiveAppCallback
): Unit
```

Registers a [TvInteractiveAppCallback](../android/media/tv/interactive/TvInteractiveAppManager.TvInteractiveAppCallback.md).

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [TvInteractiveAppManager.TvInteractiveAppCallback](../android/media/tv/interactive/TvInteractiveAppManager.TvInteractiveAppCallback.md):A callback used to monitor status of the TV Interactive App services. This value cannot be`null`. |
| `executor` | [Executor](../java/util/concurrent/Executor.md):A [Executor](../java/util/concurrent/Executor.md) that the status change will be delivered to. Callback and listener events are dispatched through this [Executor](../java/util/concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android/content/Context.md)). Otherwise, provide an [Executor](../java/util/concurrent/Executor.md) that dispatches to an appropriate thread. This value cannot be`null`. |

### sendAppLinkCommand

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun sendAppLinkCommand(
    tvIAppServiceId: String, 
    command: Bundle
): Unit
```

Sends app link command.

| Parameters ||
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tvIAppServiceId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The ID of TV interactive service which the command to be sent to. The ID can be found in [TvInteractiveAppServiceInfo.getId()](../android/media/tv/interactive/TvInteractiveAppServiceInfo.md)). This value cannot be`null`. |
| `command` | [Bundle](../android/os/Bundle.md):The command to be sent. This value cannot be`null`. |

### unregisterAppLinkInfo

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun unregisterAppLinkInfo(
    tvIAppServiceId: String, 
    appLinkInfo: AppLinkInfo
): Unit
```

Unregisters an Android application link info record which can be used to launch the specific Android application by TV interactive App RTE.

| Parameters ||
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tvIAppServiceId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The ID of TV interactive service which the command to be sent to. The ID can be found in [TvInteractiveAppServiceInfo.getId()](../android/media/tv/interactive/TvInteractiveAppServiceInfo.md)). This value cannot be`null`. |
| `appLinkInfo` | [AppLinkInfo](../android/media/tv/interactive/AppLinkInfo.md):The Android application link info record to be unregistered. This value cannot be`null`. |

### unregisterCallback

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun unregisterCallback(callback: TvInteractiveAppManager.TvInteractiveAppCallback): Unit
```

Unregisters the existing [TvInteractiveAppCallback](../android/media/tv/interactive/TvInteractiveAppManager.TvInteractiveAppCallback.md).

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [TvInteractiveAppManager.TvInteractiveAppCallback](../android/media/tv/interactive/TvInteractiveAppManager.TvInteractiveAppCallback.md):The existing callback to remove. This value cannot be`null`. |
