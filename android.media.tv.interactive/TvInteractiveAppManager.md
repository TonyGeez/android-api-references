# TvInteractiveAppManager

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TvInteractiveAppManager

Kotlin| [Java](https://developer.android.com/reference/android/media/tv/interactive/TvInteractiveAppManager "View this page in Java") 
| --- | --- |

```
class TvInteractiveAppManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.tv.interactive.TvInteractiveAppManager](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppManager#) |

Central system API to the overall TV interactive application framework (TIAF) architecture, which arbitrates interaction between Android applications and TV interactive apps.

## Summary

| Nested classes ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [TvInteractiveAppCallback](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppManager.TvInteractiveAppCallback) Callback used to monitor status of the TV Interactive App. |

| Constants ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_APP_LINK_COMMAND](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppManager#ACTION_APP_LINK_COMMAND:kotlin.String) Broadcast intent action to send app command to TV app. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [APP_LINK_KEY_BACK_URI](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppManager#APP_LINK_KEY_BACK_URI:kotlin.String) Key for back URI in app link command. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [APP_LINK_KEY_CLASS_NAME](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppManager#APP_LINK_KEY_CLASS_NAME:kotlin.String) Key for class name in app link. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [APP_LINK_KEY_COMMAND_TYPE](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppManager#APP_LINK_KEY_COMMAND_TYPE:kotlin.String) Key for command type in app link command. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [APP_LINK_KEY_PACKAGE_NAME](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppManager#APP_LINK_KEY_PACKAGE_NAME:kotlin.String) Key for package name in app link. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [APP_LINK_KEY_SERVICE_ID](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppManager#APP_LINK_KEY_SERVICE_ID:kotlin.String) Key for service ID in app link command. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_BLOCKED](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppManager#ERROR_BLOCKED:kotlin.Int) Error code for blocked contents. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_ENCRYPTED](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppManager#ERROR_ENCRYPTED:kotlin.Int) Error code when the key or module is missing for the encrypted channel. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_NONE](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppManager#ERROR_NONE:kotlin.Int) No error. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_NOT_SUPPORTED](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppManager#ERROR_NOT_SUPPORTED:kotlin.Int) Error code for an unsupported channel. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_RESOURCE_UNAVAILABLE](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppManager#ERROR_RESOURCE_UNAVAILABLE:kotlin.Int) Error code when resource (e.g. tuner) is unavailable. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_UNKNOWN](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppManager#ERROR_UNKNOWN:kotlin.Int) Unknown error code. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_UNKNOWN_CHANNEL](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppManager#ERROR_UNKNOWN_CHANNEL:kotlin.Int) Error code when the current channel is an unknown channel. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_WEAK_SIGNAL](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppManager#ERROR_WEAK_SIGNAL:kotlin.Int) Error code for weak signal. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [INTENT_KEY_BI_INTERACTIVE_APP_TYPE](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppManager#INTENT_KEY_BI_INTERACTIVE_APP_TYPE:kotlin.String) Intent key for broadcast-independent(BI) interactive app type. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [INTENT_KEY_BI_INTERACTIVE_APP_URI](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppManager#INTENT_KEY_BI_INTERACTIVE_APP_URI:kotlin.String) Intent key for broadcast-independent(BI) interactive app URI. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [INTENT_KEY_CHANNEL_URI](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppManager#INTENT_KEY_CHANNEL_URI:kotlin.String) Intent key for TV channel URI. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [INTENT_KEY_COMMAND_TYPE](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppManager#INTENT_KEY_COMMAND_TYPE:kotlin.String) Intent key for command type. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [INTENT_KEY_INTERACTIVE_APP_SERVICE_ID](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppManager#INTENT_KEY_INTERACTIVE_APP_SERVICE_ID:kotlin.String) Intent key for TV interactive app ID. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [INTENT_KEY_TV_INPUT_ID](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppManager#INTENT_KEY_TV_INPUT_ID:kotlin.String) Intent key for TV input ID. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INTERACTIVE_APP_STATE_ERROR](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppManager#INTERACTIVE_APP_STATE_ERROR:kotlin.Int) Error state of interactive application. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INTERACTIVE_APP_STATE_RUNNING](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppManager#INTERACTIVE_APP_STATE_RUNNING:kotlin.Int) Running state of interactive application. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INTERACTIVE_APP_STATE_STOPPED](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppManager#INTERACTIVE_APP_STATE_STOPPED:kotlin.Int) Stopped (or not started) state of interactive application. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SERVICE_STATE_ERROR](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppManager#SERVICE_STATE_ERROR:kotlin.Int) Error state of interactive app service. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SERVICE_STATE_PREPARING](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppManager#SERVICE_STATE_PREPARING:kotlin.Int) Preparing state of interactive app service. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SERVICE_STATE_READY](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppManager#SERVICE_STATE_READY:kotlin.Int) Ready state of interactive app service. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SERVICE_STATE_UNREALIZED](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppManager#SERVICE_STATE_UNREALIZED:kotlin.Int) Unrealized state of interactive app service. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TELETEXT_APP_STATE_ERROR](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppManager#TELETEXT_APP_STATE_ERROR:kotlin.Int) State of Teletext app: error |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TELETEXT_APP_STATE_HIDE](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppManager#TELETEXT_APP_STATE_HIDE:kotlin.Int) State of Teletext app: hide |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TELETEXT_APP_STATE_SHOW](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppManager#TELETEXT_APP_STATE_SHOW:kotlin.Int) State of Teletext app: show |
| --- | --- |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [AppLinkInfo](https://developer.android.com/reference/kotlin/android/media/tv/interactive/AppLinkInfo)!\> | [getAppLinkInfoList](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppManager#getAppLinkInfoList())`()` Returns a list of available app link information. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [TvInteractiveAppServiceInfo](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppServiceInfo)!\> | [getTvInteractiveAppServiceList](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppManager#getTvInteractiveAppServiceList())`()` Returns the complete list of TV Interactive App service on the system. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerAppLinkInfo](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppManager#registerAppLinkInfo(kotlin.String,%20android.media.tv.interactive.AppLinkInfo))`(`tvIAppServiceId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `appLinkInfo:` ` [AppLinkInfo](https://developer.android.com/reference/kotlin/android/media/tv/interactive/AppLinkInfo)`)` Registers an Android application link info record which can be used to launch the specific Android application by TV interactive App RTE. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerCallback](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppManager#registerCallback(java.util.concurrent.Executor,%20android.media.tv.interactive.TvInteractiveAppManager.TvInteractiveAppCallback))`(`executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `callback:` ` [TvInteractiveAppManager.TvInteractiveAppCallback](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppManager.TvInteractiveAppCallback)`)` Registers a [TvInteractiveAppCallback](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppManager.TvInteractiveAppCallback). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendAppLinkCommand](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppManager#sendAppLinkCommand(kotlin.String,%20android.os.Bundle))`(`tvIAppServiceId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `command:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)`)` Sends app link command. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterAppLinkInfo](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppManager#unregisterAppLinkInfo(kotlin.String,%20android.media.tv.interactive.AppLinkInfo))`(`tvIAppServiceId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `appLinkInfo:` ` [AppLinkInfo](https://developer.android.com/reference/kotlin/android/media/tv/interactive/AppLinkInfo)`)` Unregisters an Android application link info record which can be used to launch the specific Android application by TV interactive App RTE. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterCallback](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppManager#unregisterCallback(android.media.tv.interactive.TvInteractiveAppManager.TvInteractiveAppCallback))`(`callback:` ` [TvInteractiveAppManager.TvInteractiveAppCallback](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppManager.TvInteractiveAppCallback)`)` Unregisters the existing [TvInteractiveAppCallback](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppManager.TvInteractiveAppCallback). |

## Constants

### ACTION_APP_LINK_COMMAND

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_APP_LINK_COMMAND: String
```

Broadcast intent action to send app command to TV app. 

 Value: "android.media.tv.interactive.action.APP_LINK_COMMAND"

**See Also**

- [#sendAppLinkCommand(String, Bundle)](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppManager#sendAppLinkCommand(kotlin.String,%20android.os.Bundle)) 

### APP_LINK_KEY_BACK_URI

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val APP_LINK_KEY_BACK_URI: String
```

Key for back URI in app link command.

Type: String 

 Value: "back_uri"

**See Also**

- [#sendAppLinkCommand(String, Bundle)](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppManager#sendAppLinkCommand(kotlin.String,%20android.os.Bundle)) 

### APP_LINK_KEY_CLASS_NAME

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val APP_LINK_KEY_CLASS_NAME: String
```

Key for class name in app link.

Type: String 

 Value: "class_name"

**See Also**

- [#sendAppLinkCommand(String, Bundle)](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppManager#sendAppLinkCommand(kotlin.String,%20android.os.Bundle)) 

### APP_LINK_KEY_COMMAND_TYPE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val APP_LINK_KEY_COMMAND_TYPE: String
```

Key for command type in app link command.

Type: String 

 Value: "command_type"

**See Also**

- [#sendAppLinkCommand(String, Bundle)](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppManager#sendAppLinkCommand(kotlin.String,%20android.os.Bundle)) 

### APP_LINK_KEY_PACKAGE_NAME

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val APP_LINK_KEY_PACKAGE_NAME: String
```

Key for package name in app link.

Type: String 

 Value: "package_name"

**See Also**

- [#sendAppLinkCommand(String, Bundle)](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppManager#sendAppLinkCommand(kotlin.String,%20android.os.Bundle)) 

### APP_LINK_KEY_SERVICE_ID

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val APP_LINK_KEY_SERVICE_ID: String
```

Key for service ID in app link command.

Type: String 

 Value: "service_id"

**See Also**

- [#sendAppLinkCommand(String, Bundle)](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppManager#sendAppLinkCommand(kotlin.String,%20android.os.Bundle)) 

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

- [#sendAppLinkCommand(String, Bundle)](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppManager#sendAppLinkCommand(kotlin.String,%20android.os.Bundle))
- [#ACTION_APP_LINK_COMMAND](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppManager#ACTION_APP_LINK_COMMAND:kotlin.String)
- [android.media.tv.interactive.TvInteractiveAppServiceInfo#getSupportedTypes()](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppServiceInfo#getSupportedTypes())
- [android.media.tv.interactive.TvInteractiveAppView#createBiInteractiveApp(Uri, Bundle)](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppView#createBiInteractiveApp(android.net.Uri,%20android.os.Bundle)) 

### INTENT_KEY_BI_INTERACTIVE_APP_URI

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INTENT_KEY_BI_INTERACTIVE_APP_URI: String
```

Intent key for broadcast-independent(BI) interactive app URI. It's used to send app command to TV app.

Type: android.net.Uri 

 Value: "bi_interactive_app_uri"

**See Also**

- [#sendAppLinkCommand(String, Bundle)](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppManager#sendAppLinkCommand(kotlin.String,%20android.os.Bundle))
- [#ACTION_APP_LINK_COMMAND](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppManager#ACTION_APP_LINK_COMMAND:kotlin.String)
- [android.media.tv.interactive.TvInteractiveAppView#createBiInteractiveApp(Uri, Bundle)](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppView#createBiInteractiveApp(android.net.Uri,%20android.os.Bundle)) 

### INTENT_KEY_CHANNEL_URI

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INTENT_KEY_CHANNEL_URI: String
```

Intent key for TV channel URI. It's used to send app command to TV app.

Type: android.net.Uri 

 Value: "channel_uri"

**See Also**

- [#sendAppLinkCommand(String, Bundle)](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppManager#sendAppLinkCommand(kotlin.String,%20android.os.Bundle))
- [#ACTION_APP_LINK_COMMAND](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppManager#ACTION_APP_LINK_COMMAND:kotlin.String) 

### INTENT_KEY_COMMAND_TYPE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INTENT_KEY_COMMAND_TYPE: String
```

Intent key for command type. It's used to send app command to TV app. The value of this key could vary according to TV apps.

Type: String 

 Value: "command_type"

**See Also**

- [#sendAppLinkCommand(String, Bundle)](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppManager#sendAppLinkCommand(kotlin.String,%20android.os.Bundle))
- [#ACTION_APP_LINK_COMMAND](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppManager#ACTION_APP_LINK_COMMAND:kotlin.String) 

### INTENT_KEY_INTERACTIVE_APP_SERVICE_ID

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INTENT_KEY_INTERACTIVE_APP_SERVICE_ID: String
```

Intent key for TV interactive app ID. It's used to send app command to TV app.

Type: String 

 Value: "interactive_app_id"

**See Also**

- [#sendAppLinkCommand(String, Bundle)](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppManager#sendAppLinkCommand(kotlin.String,%20android.os.Bundle))
- [#ACTION_APP_LINK_COMMAND](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppManager#ACTION_APP_LINK_COMMAND:kotlin.String)
- [android.media.tv.interactive.TvInteractiveAppServiceInfo#getId()](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppServiceInfo#getId()) 

### INTENT_KEY_TV_INPUT_ID

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INTENT_KEY_TV_INPUT_ID: String
```

Intent key for TV input ID. It's used to send app command to TV app.

Type: String 

 Value: "tv_input_id"

**See Also**

- [#sendAppLinkCommand(String, Bundle)](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppManager#sendAppLinkCommand(kotlin.String,%20android.os.Bundle))
- [#ACTION_APP_LINK_COMMAND](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppManager#ACTION_APP_LINK_COMMAND:kotlin.String) 

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

- [android.media.tv.interactive.TvInteractiveAppView#startInteractiveApp()](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppView#startInteractiveApp()) 

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
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [AppLinkInfo](https://developer.android.com/reference/kotlin/android/media/tv/interactive/AppLinkInfo)!> | List of [AppLinkInfo](https://developer.android.com/reference/kotlin/android/media/tv/interactive/AppLinkInfo) for each package that deslares its app link information. This value cannot be`null`. |

### getTvInteractiveAppServiceList

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTvInteractiveAppServiceList(): MutableList<TvInteractiveAppServiceInfo!>
```

Returns the complete list of TV Interactive App service on the system.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [TvInteractiveAppServiceInfo](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppServiceInfo)!> | List of [TvInteractiveAppServiceInfo](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppServiceInfo) for each TV Interactive App service that describes its meta information. This value cannot be`null`. |

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
| `tvIAppServiceId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The ID of TV interactive service which the command to be sent to. The ID can be found in [TvInteractiveAppServiceInfo.getId()](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppServiceInfo#getId()). This value cannot be`null`. |
| `appLinkInfo` | [AppLinkInfo](https://developer.android.com/reference/kotlin/android/media/tv/interactive/AppLinkInfo):The Android application link info record to be registered. This value cannot be`null`. |

### registerCallback

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun registerCallback(
    executor: Executor, 
    callback: TvInteractiveAppManager.TvInteractiveAppCallback
): Unit
```

Registers a [TvInteractiveAppCallback](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppManager.TvInteractiveAppCallback).

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [TvInteractiveAppManager.TvInteractiveAppCallback](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppManager.TvInteractiveAppCallback):A callback used to monitor status of the TV Interactive App services. This value cannot be`null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):A [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that the status change will be delivered to. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. This value cannot be`null`. |

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
| `tvIAppServiceId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The ID of TV interactive service which the command to be sent to. The ID can be found in [TvInteractiveAppServiceInfo.getId()](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppServiceInfo#getId()). This value cannot be`null`. |
| `command` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#):The command to be sent. This value cannot be`null`. |

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
| `tvIAppServiceId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The ID of TV interactive service which the command to be sent to. The ID can be found in [TvInteractiveAppServiceInfo.getId()](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppServiceInfo#getId()). This value cannot be`null`. |
| `appLinkInfo` | [AppLinkInfo](https://developer.android.com/reference/kotlin/android/media/tv/interactive/AppLinkInfo):The Android application link info record to be unregistered. This value cannot be`null`. |

### unregisterCallback

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun unregisterCallback(callback: TvInteractiveAppManager.TvInteractiveAppCallback): Unit
```

Unregisters the existing [TvInteractiveAppCallback](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppManager.TvInteractiveAppCallback).

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [TvInteractiveAppManager.TvInteractiveAppCallback](https://developer.android.com/reference/kotlin/android/media/tv/interactive/TvInteractiveAppManager.TvInteractiveAppCallback):The existing callback to remove. This value cannot be`null`. |
