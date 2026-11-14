Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# VirtualDeviceManager

```
class VirtualDeviceManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.companion.virtual.VirtualDeviceManager](https://developer.android.com/reference/kotlin/android/companion/virtual/VirtualDeviceManager#) |

System level service for creation and management of virtual devices.

VirtualDeviceManager enables interactive sharing of capabilities between the host Android device and a remote device.

A device only supports VirtualDeviceManager if it enables it via `config_enableVirtualDeviceManager`. Otherwise `Context#getSystemService (VirtualDeviceManager.class)` will return `null`.

VirtualDeviceManager provides support for the ComputerControl feature in Android. For a device to support the ComputerControl feature, the device needs to:

- Enable support for feature `android.software.activities_on_secondary_displays`
- Enable support for VirtualDeviceManager `config_enableVirtualDeviceManager`
- Preload the ComputerControl extensions library `com.android.extensions .computercontrol`
- Preload the platform application `VirtualDeviceManager`

Devices that support the ComputerControl feature:

- MUST only allow applications to use the Computer Controls API if it is listed in the latest version of the agent allowlist.
- MUST NOT allow a Computer Controls Agent to automate any target applications that:
 - Are not included in the latest version of the allowlist OR
 - Are included in the latest version of the Computer Controls denylist OR
 - Do not have explicit opt-in user consent for automation by the requesting Computer Controls Agent
- MAY remove applications from the Computer Controls allowlist, or MAY add applications to the Computer Controls denylist, provided it results in a more restrictive set of automatable applications
- MUST support the per-app consent dialog UI and consent settings UI to allow users to manage consent for each target application per Computer Controls Agent

ComputerControl may only be used by agent applications holding the android.Manifest.permission#ACCESS_COMPUTER_CONTROL permission and meeting the relevant policy requirements. Only the current ASSISTANT role holder can use ComputerControl.

Not to be confused with the Android Studio's Virtual Device Manager, which allows for device emulation. 
Restricted for SDK Runtime environment in API level 34.

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/companion/virtual/VirtualDeviceManager.VirtualDeviceListener` Listener for changes in the available virtual devices. |

| Public methods ||
|---|---|
| [VirtualDevice](https://developer.android.com/reference/kotlin/android/companion/virtual/VirtualDevice)? | `https://developer.android.com/reference/kotlin/android/companion/virtual/VirtualDeviceManager#getVirtualDevice(kotlin.Int)(deviceId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the details of the virtual device with the given ID, if any. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [VirtualDevice](https://developer.android.com/reference/kotlin/android/companion/virtual/VirtualDevice)!\> | `https://developer.android.com/reference/kotlin/android/companion/virtual/VirtualDeviceManager#getVirtualDevices()()` Returns the details of all available virtual devices. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/companion/virtual/VirtualDeviceManager#isVirtualCameraSupported()()` Returns true if virtual cameras can be added to virtual devices on this device. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/companion/virtual/VirtualDeviceManager#registerVirtualDeviceListener(java.util.concurrent.Executor,%20android.companion.virtual.VirtualDeviceManager.VirtualDeviceListener)(executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, listener: https://developer.android.com/reference/kotlin/android/companion/virtual/VirtualDeviceManager.VirtualDeviceListener)` Registers a virtual device listener to receive notifications when virtual devices are created or closed. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/companion/virtual/VirtualDeviceManager#unregisterVirtualDeviceListener(android.companion.virtual.VirtualDeviceManager.VirtualDeviceListener)(listener: https://developer.android.com/reference/kotlin/android/companion/virtual/VirtualDeviceManager.VirtualDeviceListener)` Unregisters a virtual device listener previously registered with `https://developer.android.com/reference/kotlin/android/companion/virtual/VirtualDeviceManager#registerVirtualDeviceListener(java.util.concurrent.Executor,%20android.companion.virtual.VirtualDeviceManager.VirtualDeviceListener)`. |

## Public methods

### getVirtualDevice

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getVirtualDevice(deviceId: Int): VirtualDevice?
```

Returns the details of the virtual device with the given ID, if any.

The returned object is a read-only representation of the virtual device that expose its properties.

Note that if the virtual device is closed and becomes invalid, the returned object will not be updated and may contain stale values. Use a `https://developer.android.com/reference/kotlin/android/companion/virtual/VirtualDeviceManager.VirtualDeviceListener` for real time updates of the availability of virtual devices.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/companion/virtual/VirtualDevice?` | the virtual device with the requested ID, or `null` if no such device exists or it has already been closed. |

### getVirtualDevices

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getVirtualDevices(): MutableList<VirtualDevice!>
```

Returns the details of all available virtual devices.

The returned objects are read-only representations that expose the properties of all existing virtual devices.

Note that if a virtual device is closed and becomes invalid, the returned objects will not be updated and may contain stale values. Use a `https://developer.android.com/reference/kotlin/android/companion/virtual/VirtualDeviceManager.VirtualDeviceListener` for real time updates of the availability of virtual devices.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/companion/virtual/VirtualDevice!>` | This value cannot be `null`. |

### isVirtualCameraSupported

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun isVirtualCameraSupported(): Boolean
```

Returns true if virtual cameras can be added to virtual devices on this device.

### registerVirtualDeviceListener

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun registerVirtualDeviceListener(
    executor: Executor, 
    listener: VirtualDeviceManager.VirtualDeviceListener
): Unit
```

Registers a virtual device listener to receive notifications when virtual devices are created or closed.

| Parameters ||
|---|---|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): The executor where the listener is executed on. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `listener` | [VirtualDeviceManager.VirtualDeviceListener](https://developer.android.com/reference/kotlin/android/companion/virtual/VirtualDeviceManager.VirtualDeviceListener): The listener to add. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/companion/virtual/VirtualDeviceManager#unregisterVirtualDeviceListener(android.companion.virtual.VirtualDeviceManager.VirtualDeviceListener)`

### unregisterVirtualDeviceListener

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun unregisterVirtualDeviceListener(listener: VirtualDeviceManager.VirtualDeviceListener): Unit
```

Unregisters a virtual device listener previously registered with `https://developer.android.com/reference/kotlin/android/companion/virtual/VirtualDeviceManager#registerVirtualDeviceListener(java.util.concurrent.Executor,%20android.companion.virtual.VirtualDeviceManager.VirtualDeviceListener)`.

| Parameters ||
|---|---|
| `listener` | [VirtualDeviceManager.VirtualDeviceListener](https://developer.android.com/reference/kotlin/android/companion/virtual/VirtualDeviceManager.VirtualDeviceListener): The listener to unregister. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/companion/virtual/VirtualDeviceManager#registerVirtualDeviceListener(java.util.concurrent.Executor,%20android.companion.virtual.VirtualDeviceManager.VirtualDeviceListener)`
