# MbmsGroupCallSessionCallback

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MbmsGroupCallSessionCallback

Kotlin| [Java](MbmsGroupCallSessionCallback.md) 
| --- | --- |

```
interface MbmsGroupCallSessionCallback
```

| [android.telephony.mbms.MbmsGroupCallSessionCallback](MbmsGroupCallSessionCallback.md) |

A callback class that is used to receive information from the middleware on MBMS group-call services. An instance of this object should be passed into [MbmsGroupCallSession.create(Context, int, Executor, MbmsGroupCallSessionCallback)](../android.telephony/MbmsGroupCallSession.md)).

## Summary

| Public methods ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAvailableSaisUpdated](MbmsGroupCallSessionCallback.md))`(`currentSais:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!>`, `availableSais:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!>!>`)` Indicates that the list of currently available SAIs has been updated. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onError](MbmsGroupCallSessionCallback.md))`(`errorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Called by the middleware when it has detected an error condition. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onMiddlewareReady](MbmsGroupCallSessionCallback.md))`()` Called to indicate that the middleware has been initialized and is ready. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onServiceInterfaceAvailable](MbmsGroupCallSessionCallback.md))`(`interfaceName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called soon after the app calls android. |

## Public methods

### onAvailableSaisUpdated

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onAvailableSaisUpdated(
    currentSais: MutableList<Int!>, 
    availableSais: MutableList<MutableList<Int!>!>
): Unit
```

Indicates that the list of currently available SAIs has been updated. The app may use this information to filter the list of group calls when displaying available group calls to the user by matching the SAIs with a list of group calls separately negotiated with the carrier. The app may also report the aggregate list of SAIs to the group call application server so that a network entity can determine when, and where to activate the broadcast of particular group calls.

| Parameters ||
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `currentSais` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\>:The available SAIs on the current cell. This value cannot be`null`. |
| `availableSais` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\>!\>:A list of lists of available SAIS in neighboring cells, where each list contains the available SAIs in an individual cell. This value cannot be`null`. |

### onError

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onError(
    errorCode: Int, 
    message: String?
): Unit
```

Called by the middleware when it has detected an error condition. The possible error codes are listed in [MbmsErrors](MbmsErrors.md).

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `errorCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The error code. Value is [android.telephony.mbms.MbmsErrors#ERROR_NO_UNIQUE_MIDDLEWARE](MbmsErrors.md), [android.telephony.mbms.MbmsErrors#ERROR_MIDDLEWARE_LOST](MbmsErrors.md), [android.telephony.mbms.MbmsErrors#ERROR_MIDDLEWARE_NOT_BOUND](MbmsErrors.md), [android.telephony.mbms.MbmsErrors.InitializationErrors#ERROR_APP_PERMISSIONS_NOT_GRANTED](../android/telephony/mbms/MbmsErrors.InitializationErrors.md), [android.telephony.mbms.MbmsErrors.InitializationErrors#ERROR_DUPLICATE_INITIALIZE](../android/telephony/mbms/MbmsErrors.InitializationErrors.md), [android.telephony.mbms.MbmsErrors.InitializationErrors#ERROR_UNABLE_TO_INITIALIZE](../android/telephony/mbms/MbmsErrors.InitializationErrors.md), [android.telephony.mbms.MbmsErrors.GeneralErrors#ERROR_MIDDLEWARE_NOT_YET_READY](../android/telephony/mbms/MbmsErrors.GeneralErrors.md), [android.telephony.mbms.MbmsErrors.GeneralErrors#ERROR_OUT_OF_MEMORY](../android/telephony/mbms/MbmsErrors.GeneralErrors.md), [android.telephony.mbms.MbmsErrors.GeneralErrors#ERROR_MIDDLEWARE_TEMPORARILY_UNAVAILABLE](../android/telephony/mbms/MbmsErrors.GeneralErrors.md), [android.telephony.mbms.MbmsErrors.GeneralErrors#ERROR_IN_E911](../android/telephony/mbms/MbmsErrors.GeneralErrors.md), [android.telephony.mbms.MbmsErrors.GeneralErrors#ERROR_NOT_CONNECTED_TO_HOME_CARRIER_LTE](../android/telephony/mbms/MbmsErrors.GeneralErrors.md), [android.telephony.mbms.MbmsErrors.GeneralErrors#ERROR_UNABLE_TO_READ_SIM](../android/telephony/mbms/MbmsErrors.GeneralErrors.md), or [android.telephony.mbms.MbmsErrors.GeneralErrors#ERROR_CARRIER_CHANGE_NOT_ALLOWED](../android/telephony/mbms/MbmsErrors.GeneralErrors.md) |
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:A human-readable message generated by the middleware for debugging purposes. This value may be`null`. |

### onMiddlewareReady

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onMiddlewareReady(): Unit
```

Called to indicate that the middleware has been initialized and is ready. Before this method is called, calling any method on an instance of [MbmsGroupCallSession](../android.telephony/MbmsGroupCallSession.md) will result in an [IllegalStateException](../java.lang/IllegalStateException.md) or an error delivered via [onError(int,java.lang.String)](MbmsGroupCallSessionCallback.md))with error code [MbmsErrors.GeneralErrors.ERROR_MIDDLEWARE_NOT_YET_READY](../android/telephony/mbms/MbmsErrors.GeneralErrors.md). 

### onServiceInterfaceAvailable

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onServiceInterfaceAvailable(
    interfaceName: String, 
    index: Int
): Unit
```

Called soon after the app calls android.telephony.MbmsGroupCallSession#create. The information supplied via this callback may be used to establish a data-link interface with the modem. In order to establish the data-link interface, the multicast IP and port must be obtained out-of-band from the carrier. A [java.net.MulticastSocket](../java.net/MulticastSocket.md) may then be constructed using a [java.net.NetworkInterface](../java.net/NetworkInterface.md) with the name and interface supplied by this callback.

| Parameters ||
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `interfaceName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The interface name for the data link. This value cannot be`null`. |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index for the data link. |
