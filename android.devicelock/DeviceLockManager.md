# DeviceLockManager

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DeviceLockManager

Kotlin| [Java](https://developer.android.com/reference/android/devicelock/DeviceLockManager "View this page in Java") 

```
class DeviceLockManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.devicelock.DeviceLockManager](https://developer.android.com/reference/kotlin/android/devicelock/DeviceLockManager#) |

Manager used to interact with the system device lock service. The device lock feature is used by special applications ('kiosk apps', downloaded and installed by the device lock solution) to lock and unlock a device. A typical use case is a financed device, where the financing entity has the capability to lock the device in case of a missed payment. When a device is locked, only a limited set of interactions with the device is allowed (for example, placing emergency calls).

Use [android.content.Context#getSystemService(java.lang.String)](https://developer.android.com/reference/kotlin/android/content/Context.html#getSystemService(kotlin.String))with [Context.DEVICE_LOCK_SERVICE](https://developer.android.com/reference/kotlin/android/content/Context.html#DEVICE_LOCK_SERVICE:kotlin.String) to create a [DeviceLockManager](https://developer.android.com/reference/kotlin/android/devicelock/DeviceLockManager#).

Requires the [PackageManager#FEATURE_DEVICE_LOCK](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_DEVICE_LOCK:kotlin.String) feature which can be detected using [PackageManager.hasSystemFeature(String)](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#hasSystemFeature(kotlin.String)).

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEVICE_LOCK_ROLE_FINANCING](https://developer.android.com/reference/kotlin/android/devicelock/DeviceLockManager#DEVICE_LOCK_ROLE_FINANCING:kotlin.Int) Constant representing a financed device role, returned by [getKioskApps](https://developer.android.com/reference/kotlin/android/devicelock/DeviceLockManager#getKioskApps(java.util.concurrent.Executor,%20android.os.OutcomeReceiver)). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_DEVICE_LOCK_VERSION](https://developer.android.com/reference/kotlin/android/devicelock/DeviceLockManager#EXTRA_DEVICE_LOCK_VERSION:kotlin.String) Extra passed to the kiosk setup activity containing the version of the Device Lock solution that started the activity. |

| Public methods ||
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearDeviceRestrictions](https://developer.android.com/reference/kotlin/android/devicelock/DeviceLockManager#clearDeviceRestrictions(java.util.concurrent.Executor,%20android.os.OutcomeReceiver))`(`executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `callback:` ` [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)< [Void](https://developer.android.com/reference/kotlin/java/lang/Void.html#)!,` ` [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!>`)` Clear device restrictions. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getDeviceId](https://developer.android.com/reference/kotlin/android/devicelock/DeviceLockManager#getDeviceId(java.util.concurrent.Executor,%20android.os.OutcomeReceiver))`(`executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `callback:` ` [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)< [DeviceId](https://developer.android.com/reference/kotlin/android/devicelock/DeviceId)!,` ` [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!>`)` Gets the device id. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getKioskApps](https://developer.android.com/reference/kotlin/android/devicelock/DeviceLockManager#getKioskApps(java.util.concurrent.Executor,%20android.os.OutcomeReceiver))`(`executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `callback:` ` [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)< [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!,` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!,` ` [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!>`)` Get the kiosk app roles and packages. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [isDeviceLocked](https://developer.android.com/reference/kotlin/android/devicelock/DeviceLockManager#isDeviceLocked(java.util.concurrent.Executor,%20android.os.OutcomeReceiver))`(`executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `callback:` ` [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)< [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)!,` ` [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!>`)` Checks if the device is locked or not. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [lockDevice](https://developer.android.com/reference/kotlin/android/devicelock/DeviceLockManager#lockDevice(java.util.concurrent.Executor,%20android.os.OutcomeReceiver))`(`executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `callback:` ` [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)< [Void](https://developer.android.com/reference/kotlin/java/lang/Void.html#)!,` ` [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!>`)` Locks the device. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyKioskSetupFinished](https://developer.android.com/reference/kotlin/android/devicelock/DeviceLockManager#notifyKioskSetupFinished(java.util.concurrent.Executor,%20android.os.OutcomeReceiver))`(`executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `callback:` ` [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)< [Void](https://developer.android.com/reference/kotlin/java/lang/Void.html#)!,` ` [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!>`)` Notifies DLC that kiosk set-up has finished and we no longer need to lock to the set-up activity. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unlockDevice](https://developer.android.com/reference/kotlin/android/devicelock/DeviceLockManager#unlockDevice(java.util.concurrent.Executor,%20android.os.OutcomeReceiver))`(`executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `callback:` ` [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)< [Void](https://developer.android.com/reference/kotlin/java/lang/Void.html#)!,` ` [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!>`)` Unlocks the device. |

## Constants

### DEVICE_LOCK_ROLE_FINANCING

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEVICE_LOCK_ROLE_FINANCING: Int
```

Constant representing a financed device role, returned by [getKioskApps](https://developer.android.com/reference/kotlin/android/devicelock/DeviceLockManager#getKioskApps(java.util.concurrent.Executor,%20android.os.OutcomeReceiver)). 

 Value: 0

### EXTRA_DEVICE_LOCK_VERSION

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_DEVICE_LOCK_VERSION: String
```

Extra passed to the kiosk setup activity containing the version of the Device Lock solution that started the activity. The kiosk setup activity can retrieve the version by calling getIntent().getIntExtra(DeviceLockManager.EXTRA_DEVICE_LOCK_VERSION, 1) This is meant to be used by kiosk apps sharing the same setup activity between the legacy Device Owner(DO) based DeviceLock solution (version 1) and successive versions. 

 Value: "android.devicelock.extra.DEVICE_LOCK_VERSION"

## Public methods

### clearDeviceRestrictions

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun clearDeviceRestrictions(
    executor: Executor, 
    callback: OutcomeReceiver<Void!, Exception!>
): Unit
```

Clear device restrictions.

After a device determines that it's part of a program (e.g. financing) by checking in with the device lock backend, it will go though a provisioning flow and install a kiosk app.

At this point, the device is "restricted" and the creditor kiosk app is able to lock the device. For example, a creditor kiosk app in a financing use case may lock the device (using [lockDevice](https://developer.android.com/reference/kotlin/android/devicelock/DeviceLockManager#lockDevice(java.util.concurrent.Executor,%20android.os.OutcomeReceiver))) if payments are missed and unlock (using [unlockDevice](https://developer.android.com/reference/kotlin/android/devicelock/DeviceLockManager#unlockDevice(java.util.concurrent.Executor,%20android.os.OutcomeReceiver)))) once they are resumed.

The Device Lock solution will also put in place some additional restrictions when a device is enrolled in the program, namely:

- Disable debugging features ([android.os.UserManager#DISALLOW_DEBUGGING_FEATURES](https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_DEBUGGING_FEATURES:kotlin.String))
- Disable installing from unknown sources ([android.os.UserManager#DISALLOW_INSTALL_UNKNOWN_SOURCES](https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_INSTALL_UNKNOWN_SOURCES:kotlin.String), when configured in the backend)
- Disable outgoing calls ([android.os.UserManager#DISALLOW_OUTGOING_CALLS](https://developer.android.com/reference/kotlin/android/os/UserManager.html#DISALLOW_OUTGOING_CALLS:kotlin.String), when configured in the backend and the device is locked)

Once the program is completed (e.g. the device has been fully paid off), the kiosk app can use the [clearDeviceRestrictions](https://developer.android.com/reference/kotlin/android/devicelock/DeviceLockManager#clearDeviceRestrictions(java.util.concurrent.Executor,%20android.os.OutcomeReceiver))API to lift the above restrictions.

At this point, the kiosk app has relinquished its ability to lock the device.

Exceptions that can be returned through the ParcelableException on the callback's`onError`method:

- [SecurityException](https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#) if the caller is missing the android.android.Manifest.permission.MANAGE_DEVICE_LOCK_STATE permission.
- [IllegalStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#) if the device has already been cleared or if policies could not be enforced for the clear state.
- [java.util.concurrent.TimeoutException](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeoutException.html#) if the response from the underlying binder call is not received within the specified duration (10 seconds).

<br />

Requires [android.Manifest.permission#MANAGE_DEVICE_LOCK_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DEVICE_LOCK_STATE:kotlin.String)

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):the [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) on which to invoke the callback. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| `callback` | [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)\< [Void](https://developer.android.com/reference/kotlin/java/lang/Void.html#)!, [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!\>:this returns either success or an exception. This value cannot be`null`. |

| Exceptions ||
|------------------------------|-------------------------------------------|
| `java.lang.RuntimeException` | if there are binder communications errors |

### getDeviceId

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDeviceId(
    executor: Executor, 
    callback: OutcomeReceiver<DeviceId!, Exception!>
): Unit
```

Gets the device id.

Exceptions that can be returned through the ParcelableException on the callback's`onError`method:

- [SecurityException](https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#) if the caller is missing the android.android.Manifest.permission.MANAGE_DEVICE_LOCK_STATE permission.
- [IllegalStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#) if no registered Device ID is found.
- [java.util.concurrent.TimeoutException](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeoutException.html#) if the response from the underlying binder call is not received within the specified duration (10 seconds).

<br />

Requires [android.Manifest.permission#MANAGE_DEVICE_LOCK_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DEVICE_LOCK_STATE:kotlin.String)

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):the [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) on which to invoke the callback. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| `callback` | [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)\< [DeviceId](https://developer.android.com/reference/kotlin/android/devicelock/DeviceId)!, [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!\>:this returns either the [DeviceId](https://developer.android.com/reference/kotlin/android/devicelock/DeviceId) or an exception. This value cannot be`null`. |

| Exceptions ||
|------------------------------|-------------------------------------------|
| `java.lang.RuntimeException` | if there are binder communications errors |

### getKioskApps

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getKioskApps(
    executor: Executor, 
    callback: OutcomeReceiver<MutableMap<Int!, String!>!, Exception!>
): Unit
```

Get the kiosk app roles and packages.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):the [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) on which to invoke the callback. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| `callback` | [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)\< [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!, [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!, [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!\>:this returns either a [Map](https://developer.android.com/reference/kotlin/java/util/Map.html#) of device roles/package names, or an exception. The Integer in the map represent the device lock role (at this moment, the only supported role is {@value #DEVICE_LOCK_ROLE_FINANCING}. The String represents the package name of the kiosk app for that role. This value cannot be`null`. |

| Exceptions ||
|------------------------------|-------------------------------------------|
| `java.lang.RuntimeException` | if there are binder communications errors |

### isDeviceLocked

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isDeviceLocked(
    executor: Executor, 
    callback: OutcomeReceiver<Boolean!, Exception!>
): Unit
```

Checks if the device is locked or not.

Exceptions that can be returned through the ParcelableException on the callback's`onError`method:

- [SecurityException](https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#) if the caller is missing the android.android.Manifest.permission.MANAGE_DEVICE_LOCK_STATE permission.
- [IllegalStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#) if called before setting the locked state of the device through [lockDevice](https://developer.android.com/reference/kotlin/android/devicelock/DeviceLockManager#lockDevice(java.util.concurrent.Executor,%20android.os.OutcomeReceiver))or [unlockDevice](https://developer.android.com/reference/kotlin/android/devicelock/DeviceLockManager#unlockDevice(java.util.concurrent.Executor,%20android.os.OutcomeReceiver)).
- [java.util.concurrent.TimeoutException](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeoutException.html#) if the response from the underlying binder call is not received within the specified duration (10 seconds).

<br />

Requires [android.Manifest.permission#MANAGE_DEVICE_LOCK_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DEVICE_LOCK_STATE:kotlin.String)

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):the [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) on which to invoke the callback. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| `callback` | [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)\< [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)!, [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!\>:this returns either the lock status or an exception. This value cannot be`null`. |

| Exceptions ||
|------------------------------|-------------------------------------------|
| `java.lang.RuntimeException` | if there are binder communications errors |

### lockDevice

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun lockDevice(
    executor: Executor, 
    callback: OutcomeReceiver<Void!, Exception!>
): Unit
```

Locks the device.

Exceptions that can be returned through the ParcelableException on the callback's`onError`method:

- [SecurityException](https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#) if the caller is missing the android.android.Manifest.permission.MANAGE_DEVICE_LOCK_STATE permission.
- [IllegalStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#) if the device has already been cleared or if policies could not be enforced for the lock state.
- [java.util.concurrent.TimeoutException](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeoutException.html#) if the response from the underlying binder call is not received within the specified duration (10 seconds).

<br />

Requires [android.Manifest.permission#MANAGE_DEVICE_LOCK_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DEVICE_LOCK_STATE:kotlin.String)

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):the [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) on which to invoke the callback. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| `callback` | [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)\< [Void](https://developer.android.com/reference/kotlin/java/lang/Void.html#)!, [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!\>:this returns either success or an exception. This value cannot be`null`. |

| Exceptions ||
|------------------------------|-------------------------------------------|
| `java.lang.RuntimeException` | if there are binder communications errors |

### notifyKioskSetupFinished

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun notifyKioskSetupFinished(
    executor: Executor, 
    callback: OutcomeReceiver<Void!, Exception!>
): Unit
```

Notifies DLC that kiosk set-up has finished and we no longer need to lock to the set-up activity. This will close the set-up activity as specified through a callback and then respect the current device lock state. If the device has never been locked or unlocked by the kiosk, it will unlock the device. Invoking [lockDevice](https://developer.android.com/reference/kotlin/android/devicelock/DeviceLockManager#lockDevice(java.util.concurrent.Executor,%20android.os.OutcomeReceiver))or [unlockDevice](https://developer.android.com/reference/kotlin/android/devicelock/DeviceLockManager#unlockDevice(java.util.concurrent.Executor,%20android.os.OutcomeReceiver))will also result in the device provision state moving from kiosk_provisioned to provision_success.

Exceptions that can be returned through the ParcelableException on the callback's`onError`method:

- [SecurityException](https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#) if the caller is missing the android.android.Manifest.permission.MANAGE_DEVICE_LOCK_STATE permission.
- [IllegalStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#) if the device has already been cleared or if policies could not be enforced for the lock or unlock state.
- [java.util.concurrent.TimeoutException](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeoutException.html#) if the response from the underlying binder call is not received within the specified duration (10 seconds).

<br />

Requires [android.Manifest.permission#MANAGE_DEVICE_LOCK_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DEVICE_LOCK_STATE:kotlin.String)

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):the [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) on which to invoke the callback. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| `callback` | [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)\< [Void](https://developer.android.com/reference/kotlin/java/lang/Void.html#)!, [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!\>:this returns either success or an exception. This value cannot be`null`. |

| Exceptions ||
|------------------------------|-------------------------------------------|
| `java.lang.RuntimeException` | if there are binder communications errors |

### unlockDevice

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun unlockDevice(
    executor: Executor, 
    callback: OutcomeReceiver<Void!, Exception!>
): Unit
```

Unlocks the device.

Exceptions that can be returned through the ParcelableException on the callback's`onError`method:

- [SecurityException](https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#) if the caller is missing the android.android.Manifest.permission.MANAGE_DEVICE_LOCK_STATE permission.
- [IllegalStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#) if the device has already been cleared or if policies could not be enforced for the unlock state.
- [java.util.concurrent.TimeoutException](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeoutException.html#) If the response from the underlying binder call is not received within the specified duration (10 seconds).

<br />

Requires [android.Manifest.permission#MANAGE_DEVICE_LOCK_STATE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MANAGE_DEVICE_LOCK_STATE:kotlin.String)

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):the [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) on which to invoke the callback. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| `callback` | [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)\< [Void](https://developer.android.com/reference/kotlin/java/lang/Void.html#)!, [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)!\>:this returns either success or an exception. This value cannot be`null`. |

| Exceptions ||
|------------------------------|-------------------------------------------|
| `java.lang.RuntimeException` | if there are binder communications errors |
