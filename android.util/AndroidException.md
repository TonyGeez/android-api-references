# AndroidException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AndroidException

Kotlin| [Java](https://developer.android.com/reference/android/util/AndroidException "View this page in Java") 

```
open class AndroidException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||
| | | ↳ | [android.util.AndroidException](https://developer.android.com/reference/kotlin/android/util/AndroidException#) |

| Known Direct Subclasses [CameraAccessException](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraAccessException.html#), [IntentFilter.MalformedMimeTypeException](https://developer.android.com/reference/kotlin/android/content/IntentFilter.MalformedMimeTypeException.html#), [IntentSender.SendIntentException](https://developer.android.com/reference/kotlin/android/content/IntentSender.SendIntentException.html#), [IpSecManager.ResourceUnavailableException](https://developer.android.com/reference/kotlin/android/net/IpSecManager.ResourceUnavailableException.html#), [IpSecManager.SpiUnavailableException](https://developer.android.com/reference/kotlin/android/net/IpSecManager.SpiUnavailableException.html#), [PackageManager.NameNotFoundException](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.NameNotFoundException.html#), [PendingIntent.CanceledException](https://developer.android.com/reference/kotlin/android/app/PendingIntent.CanceledException.html#), [RemoteException](https://developer.android.com/reference/kotlin/android/os/RemoteException.html#), [Settings.SettingNotFoundException](https://developer.android.com/reference/kotlin/android/provider/Settings.SettingNotFoundException.html#) |---------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [CameraAccessException](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraAccessException.html#) | `CameraAccessException`is thrown if a camera device could not be queried or opened by the [CameraManager](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraManager.html#), or if the connection to an opened [CameraDevice](https://developer.android.com/reference/kotlin/android/hardware/camera2/CameraDevice.html#) is no longer valid. | | [IntentFilter.MalformedMimeTypeException](https://developer.android.com/reference/kotlin/android/content/IntentFilter.MalformedMimeTypeException.html#) | This exception is thrown when a given MIME type does not have a valid syntax. | | [IntentSender.SendIntentException](https://developer.android.com/reference/kotlin/android/content/IntentSender.SendIntentException.html#) | Exception thrown when trying to send through a PendingIntent that has been canceled or is otherwise no longer able to execute the request. | | [IpSecManager.ResourceUnavailableException](https://developer.android.com/reference/kotlin/android/net/IpSecManager.ResourceUnavailableException.html#) | Thrown to indicate that an IPsec resource is unavailable. | | [IpSecManager.SpiUnavailableException](https://developer.android.com/reference/kotlin/android/net/IpSecManager.SpiUnavailableException.html#) | Thrown to indicate that a requested SPI is in use. | | [PackageManager.NameNotFoundException](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.NameNotFoundException.html#) | This exception is thrown when a given package, application, or component name cannot be found. | | [PendingIntent.CanceledException](https://developer.android.com/reference/kotlin/android/app/PendingIntent.CanceledException.html#) | Exception thrown when trying to send through a PendingIntent that has been canceled or is otherwise no longer able to execute the request. | | [RemoteException](https://developer.android.com/reference/kotlin/android/os/RemoteException.html#) | Parent exception for all Binder remote-invocation errors Note: not all exceptions from binder services will be subclasses of this. | | [Settings.SettingNotFoundException](https://developer.android.com/reference/kotlin/android/provider/Settings.SettingNotFoundException.html#) | <br /> | |

| Known Indirect Subclasses [DeadObjectException](https://developer.android.com/reference/kotlin/android/os/DeadObjectException.html#), [DeadSystemException](https://developer.android.com/reference/kotlin/android/os/DeadSystemException.html#), [TransactionTooLargeException](https://developer.android.com/reference/kotlin/android/os/TransactionTooLargeException.html#) |------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------| | [DeadObjectException](https://developer.android.com/reference/kotlin/android/os/DeadObjectException.html#) | The object you are calling has died, because its hosting process no longer exists, or there has been a low-level binder error. | | [DeadSystemException](https://developer.android.com/reference/kotlin/android/os/DeadSystemException.html#) | The core Android system has died and is going through a runtime restart. | | [TransactionTooLargeException](https://developer.android.com/reference/kotlin/android/os/TransactionTooLargeException.html#) | The Binder transaction failed because it was too large. | |

Base class for all checked exceptions thrown by the Android frameworks.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AndroidException](https://developer.android.com/reference/kotlin/android/util/AndroidException#AndroidException())`()` <br /> |
| [AndroidException](https://developer.android.com/reference/kotlin/android/util/AndroidException#AndroidException(java.lang.Exception))`(`cause:` ` [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!`)` <br /> |
| [AndroidException](https://developer.android.com/reference/kotlin/android/util/AndroidException#AndroidException(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| [AndroidException](https://developer.android.com/reference/kotlin/android/util/AndroidException#AndroidException(kotlin.String,%20kotlin.Throwable))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` <br /> |

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
