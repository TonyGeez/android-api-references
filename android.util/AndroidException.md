# AndroidException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AndroidException

Kotlin| [Java](../android/util/AndroidException.md) 
| --- | --- |

```
open class AndroidException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) ||
| | | ↳ | [android.util.AndroidException](../android/util/AndroidException.md) |
| --- | --- | --- | --- |

| Known Direct Subclasses [CameraAccessException](../android/hardware/camera2/CameraAccessException.md), [IntentFilter.MalformedMimeTypeException](../android/content/IntentFilter.MalformedMimeTypeException.md), [IntentSender.SendIntentException](../android/content/IntentSender.SendIntentException.md), [IpSecManager.ResourceUnavailableException](../android/net/IpSecManager.ResourceUnavailableException.md), [IpSecManager.SpiUnavailableException](../android/net/IpSecManager.SpiUnavailableException.md), [PackageManager.NameNotFoundException](../android/content/pm/PackageManager.NameNotFoundException.md), [PendingIntent.CanceledException](../android/app/PendingIntent.CanceledException.md), [RemoteException](../android/os/RemoteException.md), [Settings.SettingNotFoundException](../android/provider/Settings.SettingNotFoundException.md) |---------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [CameraAccessException](../android/hardware/camera2/CameraAccessException.md) | `CameraAccessException`is thrown if a camera device could not be queried or opened by the [CameraManager](../android/hardware/camera2/CameraManager.md), or if the connection to an opened [CameraDevice](../android/hardware/camera2/CameraDevice.md) is no longer valid. | | [IntentFilter.MalformedMimeTypeException](../android/content/IntentFilter.MalformedMimeTypeException.md) | This exception is thrown when a given MIME type does not have a valid syntax. | | [IntentSender.SendIntentException](../android/content/IntentSender.SendIntentException.md) | Exception thrown when trying to send through a PendingIntent that has been canceled or is otherwise no longer able to execute the request. | | [IpSecManager.ResourceUnavailableException](../android/net/IpSecManager.ResourceUnavailableException.md) | Thrown to indicate that an IPsec resource is unavailable. | | [IpSecManager.SpiUnavailableException](../android/net/IpSecManager.SpiUnavailableException.md) | Thrown to indicate that a requested SPI is in use. | | [PackageManager.NameNotFoundException](../android/content/pm/PackageManager.NameNotFoundException.md) | This exception is thrown when a given package, application, or component name cannot be found. | | [PendingIntent.CanceledException](../android/app/PendingIntent.CanceledException.md) | Exception thrown when trying to send through a PendingIntent that has been canceled or is otherwise no longer able to execute the request. | | [RemoteException](../android/os/RemoteException.md) | Parent exception for all Binder remote-invocation errors Note: not all exceptions from binder services will be subclasses of this. | | [Settings.SettingNotFoundException](../android/provider/Settings.SettingNotFoundException.md) | <br /> | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [DeadObjectException](../android/os/DeadObjectException.md), [DeadSystemException](../android/os/DeadSystemException.md), [TransactionTooLargeException](../android/os/TransactionTooLargeException.md) |------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------| | [DeadObjectException](../android/os/DeadObjectException.md) | The object you are calling has died, because its hosting process no longer exists, or there has been a low-level binder error. | | [DeadSystemException](../android/os/DeadSystemException.md) | The core Android system has died and is going through a runtime restart. | | [TransactionTooLargeException](../android/os/TransactionTooLargeException.md) | The Binder transaction failed because it was too large. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Base class for all checked exceptions thrown by the Android frameworks.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AndroidException](../android/util/AndroidException.md))`()` <br /> |
| [AndroidException](../android/util/AndroidException.md))`(`cause:` ` [Exception](../java/lang/Exception.md)!`)` <br /> |
| [AndroidException](../android/util/AndroidException.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| [AndroidException](../android/util/AndroidException.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` <br /> |

## Public constructors

### AndroidException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AndroidException()
```  

### AndroidException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AndroidException(cause: Exception!)
```  

### AndroidException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AndroidException(name: String!)
```  

### AndroidException

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AndroidException(
    name: String!, 
    cause: Throwable!)
```
