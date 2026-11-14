# MbmsDownloadSessionCallback

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MbmsDownloadSessionCallback

Kotlin| [Java](MbmsDownloadSessionCallback.md) 
| --- | --- |

```
open class MbmsDownloadSessionCallback
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telephony.mbms.MbmsDownloadSessionCallback](MbmsDownloadSessionCallback.md) |

A callback class that apps should use to receive information on file downloads over cell-broadcast.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [MbmsDownloadSessionCallback](MbmsDownloadSessionCallback.md))`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onError](MbmsDownloadSessionCallback.md))`(`errorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Indicates that the middleware has encountered an asynchronous error. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onFileServicesUpdated](MbmsDownloadSessionCallback.md))`(`services:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [FileServiceInfo](FileServiceInfo.md)!>!`)` Called to indicate published File Services have changed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onMiddlewareReady](MbmsDownloadSessionCallback.md))`()` Called to indicate that the middleware has been initialized and is ready. |
| --- | --- |

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
| `errorCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Any error code listed in [MbmsErrors](MbmsErrors.md) Value is [android.telephony.mbms.MbmsErrors#ERROR_NO_UNIQUE_MIDDLEWARE](MbmsErrors.md), [android.telephony.mbms.MbmsErrors#ERROR_MIDDLEWARE_LOST](MbmsErrors.md), [android.telephony.mbms.MbmsErrors#ERROR_MIDDLEWARE_NOT_BOUND](MbmsErrors.md), [android.telephony.mbms.MbmsErrors.InitializationErrors#ERROR_APP_PERMISSIONS_NOT_GRANTED](../android/telephony/mbms/MbmsErrors.InitializationErrors.md), [android.telephony.mbms.MbmsErrors.InitializationErrors#ERROR_DUPLICATE_INITIALIZE](../android/telephony/mbms/MbmsErrors.InitializationErrors.md), [android.telephony.mbms.MbmsErrors.InitializationErrors#ERROR_UNABLE_TO_INITIALIZE](../android/telephony/mbms/MbmsErrors.InitializationErrors.md), [android.telephony.mbms.MbmsErrors.GeneralErrors#ERROR_MIDDLEWARE_NOT_YET_READY](../android/telephony/mbms/MbmsErrors.GeneralErrors.md), [android.telephony.mbms.MbmsErrors.GeneralErrors#ERROR_OUT_OF_MEMORY](../android/telephony/mbms/MbmsErrors.GeneralErrors.md), [android.telephony.mbms.MbmsErrors.GeneralErrors#ERROR_MIDDLEWARE_TEMPORARILY_UNAVAILABLE](../android/telephony/mbms/MbmsErrors.GeneralErrors.md), [android.telephony.mbms.MbmsErrors.GeneralErrors#ERROR_IN_E911](../android/telephony/mbms/MbmsErrors.GeneralErrors.md), [android.telephony.mbms.MbmsErrors.GeneralErrors#ERROR_NOT_CONNECTED_TO_HOME_CARRIER_LTE](../android/telephony/mbms/MbmsErrors.GeneralErrors.md), [android.telephony.mbms.MbmsErrors.GeneralErrors#ERROR_UNABLE_TO_READ_SIM](../android/telephony/mbms/MbmsErrors.GeneralErrors.md), [android.telephony.mbms.MbmsErrors.GeneralErrors#ERROR_CARRIER_CHANGE_NOT_ALLOWED](../android/telephony/mbms/MbmsErrors.GeneralErrors.md), [android.telephony.mbms.MbmsErrors.DownloadErrors#ERROR_CANNOT_CHANGE_TEMP_FILE_ROOT](../android/telephony/mbms/MbmsErrors.DownloadErrors.md), [android.telephony.mbms.MbmsErrors.DownloadErrors#ERROR_UNKNOWN_DOWNLOAD_REQUEST](../android/telephony/mbms/MbmsErrors.DownloadErrors.md), or [android.telephony.mbms.MbmsErrors.DownloadErrors#ERROR_UNKNOWN_FILE_INFO](../android/telephony/mbms/MbmsErrors.DownloadErrors.md) |
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:A message, intended for debugging purposes, describing the error in further detail. |

### onFileServicesUpdated

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onFileServicesUpdated(services: MutableList<FileServiceInfo!>!): Unit
```

Called to indicate published File Services have changed. This will only be called after the application has requested a list of file services and specified a service class list of interest via [MbmsDownloadSession.requestUpdateFileServices(List)](../android.telephony/MbmsDownloadSession.md)). If there are subsequent calls to [MbmsDownloadSession.requestUpdateFileServices(List)](../android.telephony/MbmsDownloadSession.md)), this method may not be called again if the list of service classes would remain the same.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `services` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [FileServiceInfo](FileServiceInfo.md)!\>!:The most recently updated list of available file services. |

### onMiddlewareReady

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onMiddlewareReady(): Unit
```

Called to indicate that the middleware has been initialized and is ready. Before this method is called, calling any method on an instance of [MbmsDownloadSession](../android.telephony/MbmsDownloadSession.md) will result in an [IllegalStateException](../java.lang/IllegalStateException.md) being thrown or [onError(int,java.lang.String)](MbmsDownloadSessionCallback.md))being called with error code [MbmsErrors.GeneralErrors.ERROR_MIDDLEWARE_NOT_YET_READY](../android/telephony/mbms/MbmsErrors.GeneralErrors.md)
