# MbmsErrors

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MbmsErrors

Kotlin| [Java](https://developer.android.com/reference/android/telephony/mbms/MbmsErrors "View this page in Java") 
| --- | --- |

```
open class MbmsErrors
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telephony.mbms.MbmsErrors](https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsErrors#) |

## Summary

| Nested classes ||
|------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [DownloadErrors](https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsErrors.DownloadErrors) Indicates the errors that are applicable only to the file-download use-case |
| open | [GeneralErrors](https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsErrors.GeneralErrors) Indicates the errors that may occur at any point and are applicable to both streaming and file-download. |
| open | [GroupCallErrors](https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsErrors.GroupCallErrors) Indicates the errors that are applicable only to the group call use-case. |
| --- | --- |
| open | [InitializationErrors](https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsErrors.InitializationErrors) Indicates errors that may be generated during initialization by the middleware. |
| open | [StreamingErrors](https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsErrors.StreamingErrors) Indicates the errors that are applicable only to the streaming use-case |

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_MIDDLEWARE_LOST](https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsErrors#ERROR_MIDDLEWARE_LOST:kotlin.Int) Indicates that the middleware has died and the requested operation was not completed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_MIDDLEWARE_NOT_BOUND](https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsErrors#ERROR_MIDDLEWARE_NOT_BOUND:kotlin.Int) Indicates that the app attempted to perform an operation on an instance of [android.telephony.MbmsDownloadSession](https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession.html#) or [MbmsStreamingSession](https://developer.android.com/reference/kotlin/android/telephony/MbmsStreamingSession.html#) without being bound to the middleware. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_NO_UNIQUE_MIDDLEWARE](https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsErrors#ERROR_NO_UNIQUE_MIDDLEWARE:kotlin.Int) Indicates that either no MBMS middleware app is installed on the device or multiple middleware apps are installed on the device. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SUCCESS](https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsErrors#SUCCESS:kotlin.Int) Indicates that the operation was successful. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UNKNOWN](https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsErrors#UNKNOWN:kotlin.Int) Indicates that the middleware has sent an error code that is not defined in the version of the SDK targeted by your app. |

## Constants

### ERROR_MIDDLEWARE_LOST

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_MIDDLEWARE_LOST: Int
```

Indicates that the middleware has died and the requested operation was not completed. 

 Value: 3

### ERROR_MIDDLEWARE_NOT_BOUND

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_MIDDLEWARE_NOT_BOUND: Int
```

Indicates that the app attempted to perform an operation on an instance of [android.telephony.MbmsDownloadSession](https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession.html#) or [MbmsStreamingSession](https://developer.android.com/reference/kotlin/android/telephony/MbmsStreamingSession.html#) without being bound to the middleware. 

 Value: 2

### ERROR_NO_UNIQUE_MIDDLEWARE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_NO_UNIQUE_MIDDLEWARE: Int
```

Indicates that either no MBMS middleware app is installed on the device or multiple middleware apps are installed on the device. 

 Value: 1

### SUCCESS

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUCCESS: Int
```

Indicates that the operation was successful. 

 Value: 0

### UNKNOWN

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UNKNOWN: Int
```

Indicates that the middleware has sent an error code that is not defined in the version of the SDK targeted by your app. This is an illegal value for the middleware to return -- it should only ever be generated by the framework. 

 Value: -1
