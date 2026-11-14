# CallLog

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CallLog

Kotlin| [Java](https://developer.android.com/reference/android/provider/CallLog "View this page in Java") 

```
open class CallLog
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.provider.CallLog](https://developer.android.com/reference/kotlin/android/provider/CallLog#) |

The CallLog provider contains information about placed and received calls.

## Summary

| Nested classes ||
|------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [Calls](https://developer.android.com/reference/kotlin/android/provider/CallLog.Calls) Contains the recent calls. |
| open | [Locations](https://developer.android.com/reference/kotlin/android/provider/CallLog.Locations) Table that contains information on location data sent via call composer. |

| Constants ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [AUTHORITY](https://developer.android.com/reference/kotlin/android/provider/CallLog#AUTHORITY:kotlin.String) <br /> |

| Public constructors ||
|---------------------------------------------------------------------------------------------------------|---|
| [CallLog](https://developer.android.com/reference/kotlin/android/provider/CallLog#CallLog())`()` <br /> |

| Properties ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)! | [CONTENT_URI](https://developer.android.com/reference/kotlin/android/provider/CallLog#CONTENT_URI:android.net.Uri) The content:// style URL for this provider |

## Constants

### AUTHORITY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AUTHORITY: String
```  

 Value: "call_log"

## Public constructors

### CallLog

```
CallLog()
```

## Properties

### CONTENT_URI

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTENT_URI: Uri!
```

The content:// style URL for this provider
