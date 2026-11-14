# CallLog

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CallLog

Kotlin| [Java](../android/provider/CallLog.md) 
| --- | --- |

```
open class CallLog
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.provider.CallLog](../android/provider/CallLog.md) |

The CallLog provider contains information about placed and received calls.

## Summary

| Nested classes ||
|------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [Calls](../android/provider/CallLog.Calls.md) Contains the recent calls. |
| open | [Locations](../android/provider/CallLog.Locations.md) Table that contains information on location data sent via call composer. |

| Constants ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [AUTHORITY](../android/provider/CallLog.md) <br /> |

| Public constructors ||
|---------------------------------------------------------------------------------------------------------|---|
| [CallLog](../android/provider/CallLog.md))`()` <br /> |

| Properties ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Uri](../android/net/Uri.md)! | [CONTENT_URI](../android/provider/CallLog.md) The content:// style URL for this provider |

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
