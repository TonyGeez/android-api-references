# MbmsDownloadSessionCallback

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MbmsDownloadSessionCallback

Kotlin| [Java](https://developer.android.com/reference/android/telephony/mbms/MbmsDownloadSessionCallback "View this page in Java") 

```
open class MbmsDownloadSessionCallback
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.telephony.mbms.MbmsDownloadSessionCallback](https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsDownloadSessionCallback#) |

A callback class that apps should use to receive information on file downloads over cell-broadcast.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [MbmsDownloadSessionCallback](https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsDownloadSessionCallback#MbmsDownloadSessionCallback())`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onError](https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsDownloadSessionCallback#onError(kotlin.Int,%20kotlin.String))`(`errorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Indicates that the middleware has encountered an asynchronous error. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onFileServicesUpdated](https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsDownloadSessionCallback#onFileServicesUpdated(kotlin.collections.MutableList))`(`services:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [FileServiceInfo](https://developer.android.com/reference/kotlin/android/telephony/mbms/FileServiceInfo)!>!`)` Called to indicate published File Services have changed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onMiddlewareReady](https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsDownloadSessionCallback#onMiddlewareReady())`()` Called to indicate that the middleware has been initialized and is ready. |

## Public constructors

### MbmsDownloadSessionCallback

```
MbmsDownloadSessionCallback()
```

## Public methods

### onError

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onError(
    errorCode: Int, 
    message: String!
): Unit
```

Indicates that the middleware has encountered an asynchronous error.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `errorCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Any error code listed in [MbmsErrors](https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsErrors) Value is [android.telephony.mbms.MbmsErrors#ERROR_NO_UNIQUE_MIDDLEWARE](https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsErrors#ERROR_NO_UNIQUE_MIDDLEWARE:kotlin.Int), [android.telephony.mbms.MbmsErrors#ERROR_MIDDLEWARE_LOST](https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsErrors#ERROR_MIDDLEWARE_LOST:kotlin.Int), [android.telephony.mbms.MbmsErrors#ERROR_MIDDLEWARE_NOT_BOUND](https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsErrors#ERROR_MIDDLEWARE_NOT_BOUND:kotlin.Int), [android.telephony.mbms.MbmsErrors.InitializationErrors#ERROR_APP_PERMISSIONS_NOT_GRANTED](https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsErrors.InitializationErrors#ERROR_APP_PERMISSIONS_NOT_GRANTED:kotlin.Int), [android.telephony.mbms.MbmsErrors.InitializationErrors#ERROR_DUPLICATE_INITIALIZE](https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsErrors.InitializationErrors#ERROR_DUPLICATE_INITIALIZE:kotlin.Int), [android.telephony.mbms.MbmsErrors.InitializationErrors#ERROR_UNABLE_TO_INITIALIZE](https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsErrors.InitializationErrors#ERROR_UNABLE_TO_INITIALIZE:kotlin.Int), [android.telephony.mbms.MbmsErrors.GeneralErrors#ERROR_MIDDLEWARE_NOT_YET_READY](https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsErrors.GeneralErrors#ERROR_MIDDLEWARE_NOT_YET_READY:kotlin.Int), [android.telephony.mbms.MbmsErrors.GeneralErrors#ERROR_OUT_OF_MEMORY](https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsErrors.GeneralErrors#ERROR_OUT_OF_MEMORY:kotlin.Int), [android.telephony.mbms.MbmsErrors.GeneralErrors#ERROR_MIDDLEWARE_TEMPORARILY_UNAVAILABLE](https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsErrors.GeneralErrors#ERROR_MIDDLEWARE_TEMPORARILY_UNAVAILABLE:kotlin.Int), [android.telephony.mbms.MbmsErrors.GeneralErrors#ERROR_IN_E911](https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsErrors.GeneralErrors#ERROR_IN_E911:kotlin.Int), [android.telephony.mbms.MbmsErrors.GeneralErrors#ERROR_NOT_CONNECTED_TO_HOME_CARRIER_LTE](https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsErrors.GeneralErrors#ERROR_NOT_CONNECTED_TO_HOME_CARRIER_LTE:kotlin.Int), [android.telephony.mbms.MbmsErrors.GeneralErrors#ERROR_UNABLE_TO_READ_SIM](https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsErrors.GeneralErrors#ERROR_UNABLE_TO_READ_SIM:kotlin.Int), [android.telephony.mbms.MbmsErrors.GeneralErrors#ERROR_CARRIER_CHANGE_NOT_ALLOWED](https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsErrors.GeneralErrors#ERROR_CARRIER_CHANGE_NOT_ALLOWED:kotlin.Int), [android.telephony.mbms.MbmsErrors.DownloadErrors#ERROR_CANNOT_CHANGE_TEMP_FILE_ROOT](https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsErrors.DownloadErrors#ERROR_CANNOT_CHANGE_TEMP_FILE_ROOT:kotlin.Int), [android.telephony.mbms.MbmsErrors.DownloadErrors#ERROR_UNKNOWN_DOWNLOAD_REQUEST](https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsErrors.DownloadErrors#ERROR_UNKNOWN_DOWNLOAD_REQUEST:kotlin.Int), or [android.telephony.mbms.MbmsErrors.DownloadErrors#ERROR_UNKNOWN_FILE_INFO](https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsErrors.DownloadErrors#ERROR_UNKNOWN_FILE_INFO:kotlin.Int) |
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A message, intended for debugging purposes, describing the error in further detail. |

### onFileServicesUpdated

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onFileServicesUpdated(services: MutableList<FileServiceInfo!>!): Unit
```

Called to indicate published File Services have changed. This will only be called after the application has requested a list of file services and specified a service class list of interest via [MbmsDownloadSession.requestUpdateFileServices(List)](https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession.html#requestUpdateFileServices(kotlin.collections.MutableList)). If there are subsequent calls to [MbmsDownloadSession.requestUpdateFileServices(List)](https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession.html#requestUpdateFileServices(kotlin.collections.MutableList)), this method may not be called again if the list of service classes would remain the same.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `services` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [FileServiceInfo](https://developer.android.com/reference/kotlin/android/telephony/mbms/FileServiceInfo)!\>!:The most recently updated list of available file services. |

### onMiddlewareReady

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onMiddlewareReady(): Unit
```

Called to indicate that the middleware has been initialized and is ready. Before this method is called, calling any method on an instance of [MbmsDownloadSession](https://developer.android.com/reference/kotlin/android/telephony/MbmsDownloadSession.html#) will result in an [IllegalStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#) being thrown or [onError(int,java.lang.String)](https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsDownloadSessionCallback#onError(kotlin.Int,%20kotlin.String))being called with error code [MbmsErrors.GeneralErrors.ERROR_MIDDLEWARE_NOT_YET_READY](https://developer.android.com/reference/kotlin/android/telephony/mbms/MbmsErrors.GeneralErrors#ERROR_MIDDLEWARE_NOT_YET_READY:kotlin.Int)
