# DeviceLockManager

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DeviceLockManager

Kotlin| [Java](../android/devicelock/DeviceLockManager.md) 
| --- | --- |

```
class DeviceLockManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.devicelock.DeviceLockManager](../android/devicelock/DeviceLockManager.md) |

Manager used to interact with the system device lock service. The device lock feature is used by special applications ('kiosk apps', downloaded and installed by the device lock solution) to lock and unlock a device. A typical use case is a financed device, where the financing entity has the capability to lock the device in case of a missed payment. When a device is locked, only a limited set of interactions with the device is allowed (for example, placing emergency calls).

Use [android.content.Context#getSystemService(java.lang.String)](../android/content/Context.md))with [Context.DEVICE_LOCK_SERVICE](../android/content/Context.md) to create a [DeviceLockManager](../android/devicelock/DeviceLockManager.md).

Requires the [PackageManager#FEATURE_DEVICE_LOCK](../android/content/pm/PackageManager.md) feature which can be detected using [PackageManager.hasSystemFeature(String)](../android/content/pm/PackageManager.md)).

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEVICE_LOCK_ROLE_FINANCING](../android/devicelock/DeviceLockManager.md) Constant representing a financed device role, returned by [getKioskApps](../android/devicelock/DeviceLockManager.md)). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_DEVICE_LOCK_VERSION](../android/devicelock/DeviceLockManager.md) Extra passed to the kiosk setup activity containing the version of the Device Lock solution that started the activity. |

| Public methods ||
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearDeviceRestrictions](../android/devicelock/DeviceLockManager.md))`(`executor:` ` [Executor](../java/util/concurrent/Executor.md)`, `callback:` ` [OutcomeReceiver](../android/os/OutcomeReceiver.md)< [Void](../java/lang/Void.md)!,` ` [Exception](../java/lang/Exception.md)!>`)` Clear device restrictions. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getDeviceId](../android/devicelock/DeviceLockManager.md))`(`executor:` ` [Executor](../java/util/concurrent/Executor.md)`, `callback:` ` [OutcomeReceiver](../android/os/OutcomeReceiver.md)< [DeviceId](../android/devicelock/DeviceId.md)!,` ` [Exception](../java/lang/Exception.md)!>`)` Gets the device id. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getKioskApps](../android/devicelock/DeviceLockManager.md))`(`executor:` ` [Executor](../java/util/concurrent/Executor.md)`, `callback:` ` [OutcomeReceiver](../android/os/OutcomeReceiver.md)< [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!,` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!,` ` [Exception](../java/lang/Exception.md)!>`)` Get the kiosk app roles and packages. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [isDeviceLocked](../android/devicelock/DeviceLockManager.md))`(`executor:` ` [Executor](../java/util/concurrent/Executor.md)`, `callback:` ` [OutcomeReceiver](../android/os/OutcomeReceiver.md)< [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)!,` ` [Exception](../java/lang/Exception.md)!>`)` Checks if the device is locked or not. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [lockDevice](../android/devicelock/DeviceLockManager.md))`(`executor:` ` [Executor](../java/util/concurrent/Executor.md)`, `callback:` ` [OutcomeReceiver](../android/os/OutcomeReceiver.md)< [Void](../java/lang/Void.md)!,` ` [Exception](../java/lang/Exception.md)!>`)` Locks the device. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyKioskSetupFinished](../android/devicelock/DeviceLockManager.md))`(`executor:` ` [Executor](../java/util/concurrent/Executor.md)`, `callback:` ` [OutcomeReceiver](../android/os/OutcomeReceiver.md)< [Void](../java/lang/Void.md)!,` ` [Exception](../java/lang/Exception.md)!>`)` Notifies DLC that kiosk set-up has finished and we no longer need to lock to the set-up activity. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unlockDevice](../android/devicelock/DeviceLockManager.md))`(`executor:` ` [Executor](../java/util/concurrent/Executor.md)`, `callback:` ` [OutcomeReceiver](../android/os/OutcomeReceiver.md)< [Void](../java/lang/Void.md)!,` ` [Exception](../java/lang/Exception.md)!>`)` Unlocks the device. |

## Constants

### DEVICE_LOCK_ROLE_FINANCING

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEVICE_LOCK_ROLE_FINANCING: Int
```

Constant representing a financed device role, returned by [getKioskApps](../android/devicelock/DeviceLockManager.md)). 

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

At this point, the device is "restricted" and the creditor kiosk app is able to lock the device. For example, a creditor kiosk app in a financing use case may lock the device (using [lockDevice](../android/devicelock/DeviceLockManager.md))) if payments are missed and unlock (using [unlockDevice](../android/devicelock/DeviceLockManager.md)))) once they are resumed.

The Device Lock solution will also put in place some additional restrictions when a device is enrolled in the program, namely:

- Disable debugging features ([android.os.UserManager#DISALLOW_DEBUGGING_FEATURES](../android/os/UserManager.md))
- Disable installing from unknown sources ([android.os.UserManager#DISALLOW_INSTALL_UNKNOWN_SOURCES](../android/os/UserManager.md), when configured in the backend)
- Disable outgoing calls ([android.os.UserManager#DISALLOW_OUTGOING_CALLS](../android/os/UserManager.md), when configured in the backend and the device is locked)

Once the program is completed (e.g. the device has been fully paid off), the kiosk app can use the [clearDeviceRestrictions](../android/devicelock/DeviceLockManager.md))API to lift the above restrictions.

At this point, the kiosk app has relinquished its ability to lock the device.

Exceptions that can be returned through the ParcelableException on the callback's`onError`method:

- [SecurityException](../java/lang/SecurityException.md) if the caller is missing the android.android.Manifest.permission.MANAGE_DEVICE_LOCK_STATE permission.
- [IllegalStateException](../java/lang/IllegalStateException.md) if the device has already been cleared or if policies could not be enforced for the clear state.
- [java.util.concurrent.TimeoutException](../java/util/concurrent/TimeoutException.md) if the response from the underlying binder call is not received within the specified duration (10 seconds).

<br />

Requires [android.Manifest.permission#MANAGE_DEVICE_LOCK_STATE](../android/Manifest.permission.md)

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](../java/util/concurrent/Executor.md):the [Executor](../java/util/concurrent/Executor.md) on which to invoke the callback. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](../java/util/concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android/content/Context.md)). Otherwise, provide an [Executor](../java/util/concurrent/Executor.md) that dispatches to an appropriate thread. |
| `callback` | [OutcomeReceiver](../android/os/OutcomeReceiver.md)\< [Void](../java/lang/Void.md)!, [Exception](../java/lang/Exception.md)!\>:this returns either success or an exception. This value cannot be`null`. |

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

- [SecurityException](../java/lang/SecurityException.md) if the caller is missing the android.android.Manifest.permission.MANAGE_DEVICE_LOCK_STATE permission.
- [IllegalStateException](../java/lang/IllegalStateException.md) if no registered Device ID is found.
- [java.util.concurrent.TimeoutException](../java/util/concurrent/TimeoutException.md) if the response from the underlying binder call is not received within the specified duration (10 seconds).

<br />

Requires [android.Manifest.permission#MANAGE_DEVICE_LOCK_STATE](../android/Manifest.permission.md)

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](../java/util/concurrent/Executor.md):the [Executor](../java/util/concurrent/Executor.md) on which to invoke the callback. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](../java/util/concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android/content/Context.md)). Otherwise, provide an [Executor](../java/util/concurrent/Executor.md) that dispatches to an appropriate thread. |
| `callback` | [OutcomeReceiver](../android/os/OutcomeReceiver.md)\< [DeviceId](../android/devicelock/DeviceId.md)!, [Exception](../java/lang/Exception.md)!\>:this returns either the [DeviceId](../android/devicelock/DeviceId.md) or an exception. This value cannot be`null`. |

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
| `executor` | [Executor](../java/util/concurrent/Executor.md):the [Executor](../java/util/concurrent/Executor.md) on which to invoke the callback. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](../java/util/concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android/content/Context.md)). Otherwise, provide an [Executor](../java/util/concurrent/Executor.md) that dispatches to an appropriate thread. |
| `callback` | [OutcomeReceiver](../android/os/OutcomeReceiver.md)\< [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!, [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!, [Exception](../java/lang/Exception.md)!\>:this returns either a [Map](../java/util/Map.md) of device roles/package names, or an exception. The Integer in the map represent the device lock role (at this moment, the only supported role is {@value #DEVICE_LOCK_ROLE_FINANCING}. The String represents the package name of the kiosk app for that role. This value cannot be`null`. |

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

- [SecurityException](../java/lang/SecurityException.md) if the caller is missing the android.android.Manifest.permission.MANAGE_DEVICE_LOCK_STATE permission.
- [IllegalStateException](../java/lang/IllegalStateException.md) if called before setting the locked state of the device through [lockDevice](../android/devicelock/DeviceLockManager.md))or [unlockDevice](../android/devicelock/DeviceLockManager.md)).
- [java.util.concurrent.TimeoutException](../java/util/concurrent/TimeoutException.md) if the response from the underlying binder call is not received within the specified duration (10 seconds).

<br />

Requires [android.Manifest.permission#MANAGE_DEVICE_LOCK_STATE](../android/Manifest.permission.md)

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](../java/util/concurrent/Executor.md):the [Executor](../java/util/concurrent/Executor.md) on which to invoke the callback. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](../java/util/concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android/content/Context.md)). Otherwise, provide an [Executor](../java/util/concurrent/Executor.md) that dispatches to an appropriate thread. |
| `callback` | [OutcomeReceiver](../android/os/OutcomeReceiver.md)\< [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)!, [Exception](../java/lang/Exception.md)!\>:this returns either the lock status or an exception. This value cannot be`null`. |

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

- [SecurityException](../java/lang/SecurityException.md) if the caller is missing the android.android.Manifest.permission.MANAGE_DEVICE_LOCK_STATE permission.
- [IllegalStateException](../java/lang/IllegalStateException.md) if the device has already been cleared or if policies could not be enforced for the lock state.
- [java.util.concurrent.TimeoutException](../java/util/concurrent/TimeoutException.md) if the response from the underlying binder call is not received within the specified duration (10 seconds).

<br />

Requires [android.Manifest.permission#MANAGE_DEVICE_LOCK_STATE](../android/Manifest.permission.md)

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](../java/util/concurrent/Executor.md):the [Executor](../java/util/concurrent/Executor.md) on which to invoke the callback. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](../java/util/concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android/content/Context.md)). Otherwise, provide an [Executor](../java/util/concurrent/Executor.md) that dispatches to an appropriate thread. |
| `callback` | [OutcomeReceiver](../android/os/OutcomeReceiver.md)\< [Void](../java/lang/Void.md)!, [Exception](../java/lang/Exception.md)!\>:this returns either success or an exception. This value cannot be`null`. |

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

Notifies DLC that kiosk set-up has finished and we no longer need to lock to the set-up activity. This will close the set-up activity as specified through a callback and then respect the current device lock state. If the device has never been locked or unlocked by the kiosk, it will unlock the device. Invoking [lockDevice](../android/devicelock/DeviceLockManager.md))or [unlockDevice](../android/devicelock/DeviceLockManager.md))will also result in the device provision state moving from kiosk_provisioned to provision_success.

Exceptions that can be returned through the ParcelableException on the callback's`onError`method:

- [SecurityException](../java/lang/SecurityException.md) if the caller is missing the android.android.Manifest.permission.MANAGE_DEVICE_LOCK_STATE permission.
- [IllegalStateException](../java/lang/IllegalStateException.md) if the device has already been cleared or if policies could not be enforced for the lock or unlock state.
- [java.util.concurrent.TimeoutException](../java/util/concurrent/TimeoutException.md) if the response from the underlying binder call is not received within the specified duration (10 seconds).

<br />

Requires [android.Manifest.permission#MANAGE_DEVICE_LOCK_STATE](../android/Manifest.permission.md)

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](../java/util/concurrent/Executor.md):the [Executor](../java/util/concurrent/Executor.md) on which to invoke the callback. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](../java/util/concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android/content/Context.md)). Otherwise, provide an [Executor](../java/util/concurrent/Executor.md) that dispatches to an appropriate thread. |
| `callback` | [OutcomeReceiver](../android/os/OutcomeReceiver.md)\< [Void](../java/lang/Void.md)!, [Exception](../java/lang/Exception.md)!\>:this returns either success or an exception. This value cannot be`null`. |

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

- [SecurityException](../java/lang/SecurityException.md) if the caller is missing the android.android.Manifest.permission.MANAGE_DEVICE_LOCK_STATE permission.
- [IllegalStateException](../java/lang/IllegalStateException.md) if the device has already been cleared or if policies could not be enforced for the unlock state.
- [java.util.concurrent.TimeoutException](../java/util/concurrent/TimeoutException.md) If the response from the underlying binder call is not received within the specified duration (10 seconds).

<br />

Requires [android.Manifest.permission#MANAGE_DEVICE_LOCK_STATE](../android/Manifest.permission.md)

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](../java/util/concurrent/Executor.md):the [Executor](../java/util/concurrent/Executor.md) on which to invoke the callback. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](../java/util/concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android/content/Context.md)). Otherwise, provide an [Executor](../java/util/concurrent/Executor.md) that dispatches to an appropriate thread. |
| `callback` | [OutcomeReceiver](../android/os/OutcomeReceiver.md)\< [Void](../java/lang/Void.md)!, [Exception](../java/lang/Exception.md)!\>:this returns either success or an exception. This value cannot be`null`. |

| Exceptions ||
|------------------------------|-------------------------------------------|
| `java.lang.RuntimeException` | if there are binder communications errors |
