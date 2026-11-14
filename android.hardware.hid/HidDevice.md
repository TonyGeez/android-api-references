Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# HidDevice

```
class HidDevice : AutoCloseable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.hardware.hid.HidDevice](HidDevice.md) |

Represents a Human Interface Device (HID) connected to the system.

HIDs are devices like keyboards, mice, game controllers, and other peripherals that follow the HID specification for communication over various transports (USB, Bluetooth, etc.).

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/hid/HidDevice#TRANSPORT_BLUETOOTH:kotlin.Int` Transport type is Bluetooth. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/hid/HidDevice#TRANSPORT_I2C:kotlin.Int` Transport type is I2C. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/hid/HidDevice#TRANSPORT_SPI:kotlin.Int` Transport type is SPI. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/hid/HidDevice#TRANSPORT_UNKNOWN:kotlin.Int` Transport type is unknown. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/hid/HidDevice#TRANSPORT_USB:kotlin.Int` Transport type is USB. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/hid/HidDevice#TRANSPORT_VIRTUAL:kotlin.Int` Transport type is Virtual. |
| --- | --- |

| Public methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/hid/HidDevice#close()()` Releases all system resources and closes the connection to the HID device. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/hid/HidDevice#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/hid/HidDevice#getFeatureReport(kotlin.Int,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)(reportId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://developer.android.com/reference/kotlin/android/hardware/hid/Report!, https://developer.android.com/reference/kotlin/java/lang/Exception.html#!>)` Get a feature report from the HID device. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/hid/HidDevice#getName()()` The human-readable name of the HID device. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/hid/HidDevice#getPhysicalAddress()()` The physical address of the device, representing its connection path through the system's device tree (e.g., the USB hub and port path). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/hid/HidDevice#getProductId()()` The product ID for this device. |
| --- | --- |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/hid/HidDevice#getReportDescriptor()()` The raw HID report descriptor for the device. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/hid/HidDevice#getTransport()()` The transport type used by this device. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/hid/HidDevice#getUniqueId()()` A unique identifier for this device instance. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/hid/HidDevice#getVendorId()()` The vendor ID for this device. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/hid/HidDevice#hashCode()()` Returns a hash code value for the object. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/hid/HidDevice#isOpen()()` Returns whether the HID device is currently open and ready for communication. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/hid/HidDevice#open(java.util.concurrent.Executor,%20android.os.OutcomeReceiver)(executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://developer.android.com/reference/kotlin/android/hardware/hid/HidDevice#!, https://developer.android.com/reference/kotlin/java/lang/Exception.html#!>)` Opens the HID device so that it can be used to send and receive HID reports. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/hid/HidDevice#registerEventListener(java.util.concurrent.Executor,%20android.hardware.hid.HidEventListener)(executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, listener: https://developer.android.com/reference/kotlin/android/hardware/hid/HidEventListener)` Registers a listener to receive real-time input reports and hotplug events for this HID device. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/hid/HidDevice#sendFeatureReport(android.hardware.hid.Report,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)(report: https://developer.android.com/reference/kotlin/android/hardware/hid/Report, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://developer.android.com/reference/kotlin/java/lang/Void.html#!, https://developer.android.com/reference/kotlin/java/lang/Exception.html#!>)` Send a feature report to the HID device. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/hid/HidDevice#sendOutputReport(android.hardware.hid.Report,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)(report: https://developer.android.com/reference/kotlin/android/hardware/hid/Report, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://developer.android.com/reference/kotlin/java/lang/Void.html#!, https://developer.android.com/reference/kotlin/java/lang/Exception.html#!>)` Send an output report to the HID device. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/hid/HidDevice#toString()()` Returns a string representation of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/hid/HidDevice#unregisterEventListener(android.hardware.hid.HidEventListener)(listener: https://developer.android.com/reference/kotlin/android/hardware/hid/HidEventListener)` Unregisters an active listener from receiving input reports. |
| --- | --- |

## Constants

### TRANSPORT_BLUETOOTH

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TRANSPORT_BLUETOOTH: Int
```

Transport type is Bluetooth.

 Value: 5

### TRANSPORT_I2C

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TRANSPORT_I2C: Int
```

Transport type is I2C.

 Value: 24

### TRANSPORT_SPI

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TRANSPORT_SPI: Int
```

Transport type is SPI.

 Value: 28

### TRANSPORT_UNKNOWN

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TRANSPORT_UNKNOWN: Int
```

Transport type is unknown.

 Value: 0

### TRANSPORT_USB

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TRANSPORT_USB: Int
```

Transport type is USB.

 Value: 3

### TRANSPORT_VIRTUAL

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TRANSPORT_VIRTUAL: Int
```

Transport type is Virtual.

 Value: 6

## Public methods

### close

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun close(): Unit
```

Releases all system resources and closes the connection to the HID device.

This method is synchronous and idempotent; calling it on an already closed device has no effect. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_HID:kotlin.String`

| Exceptions ||
|---|---|
| `java.lang.Exception` | if this resource cannot be closed |

### equals

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The `equals` method implements an equivalence relation on non-null object references:

- It is *reflexive* : for any non-null reference value `x`, `x.equals(x)` should return `true`.
- It is *symmetric* : for any non-null reference values `x` and `y`, `x.equals(y)` should return `true` if and only if `y.equals(x)` returns `true`.
- It is *transitive* : for any non-null reference values `x`, `y`, and `z`, if `x.equals(y)` returns `true` and `y.equals(z)` returns `true`, then `x.equals(z)` should return `true`.
- It is *consistent* : for any non-null reference values `x` and `y`, multiple invocations of `x.equals(y)` consistently return `true` or consistently return `false`, provided no information used in `equals` comparisons on the objects is modified.
- For any non-null reference value `x`, `x.equals(null)` should return `false`.

An equivalence relation partitions the elements it operates on into *equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |
| `o` | This value may be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

### getFeatureReport

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getFeatureReport(
    reportId: Int, 
    executor: Executor, 
    callback: OutcomeReceiver<Report!, Exception!>
): Unit
```

Get a feature report from the HID device.

The device must be opened first before calling this method.

On success, `callback.onResult` is called with the retrieved `https://developer.android.com/reference/kotlin/android/hardware/hid/Report`. On failure, `callback.onError` is called with one of the following:

- `https://developer.android.com/reference/kotlin/java/io/IOException.html#`: If the underlying hardware device could not be accessed or the system service returned a failure.
- `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#`: If the caller lacks the required permission.

. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_HID:kotlin.String`

| Parameters ||
|---|---|
| `reportId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the feature report to get. |
| `executor` | [Executor](../java.util.concurrent/Executor.md): the executor on which the callback will be invoked. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [OutcomeReceiver](../android.os/OutcomeReceiver.md)\< [Report](Report.md)!, [Exception](../java.lang/Exception.md)!\>: the callback object to be used to notify of the report or an error. This value cannot be `null`. |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if the device is not open. |

### getName

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getName(): String
```

The human-readable name of the HID device.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | This value cannot be `null`. |

### getPhysicalAddress

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPhysicalAddress(): String
```

The physical address of the device, representing its connection path through the system's device tree (e.g., the USB hub and port path).

This value is unique to the device's physical connection point on the current system.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | This value cannot be `null`. |

### getProductId

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getProductId(): Int
```

The product ID for this device.

A product ID uniquely identifies which product within the address space of a given vendor, identified by the device's vendor ID. A value of 0 will be assigned where a product ID is not available.

### getReportDescriptor

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getReportDescriptor(): ByteArray
```

The raw HID report descriptor for the device.

This descriptor defines the format and meaning of the reports sent and received by the device, following the HID specification.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html` | This value cannot be `null`. |

### getTransport

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTransport(): Int
```

The transport type used by this device.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/hardware/hid/HidDevice#TRANSPORT_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/hid/HidDevice#TRANSPORT_USB:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/hid/HidDevice#TRANSPORT_BLUETOOTH:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/hid/HidDevice#TRANSPORT_SPI:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/hid/HidDevice#TRANSPORT_I2C:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/hid/HidDevice#TRANSPORT_VIRTUAL:kotlin.Int` |

### getUniqueId

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getUniqueId(): String
```

A unique identifier for this device instance.

This value is typically the device's serial number if available, or a system-generated unique ID. This ID is unique among all currently connected HID devices.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | This value cannot be `null`. |

### getVendorId

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getVendorId(): Int
```

The vendor ID for this device.

A vendor ID uniquely identifies the company who manufactured the device. A value of 0 will be assigned where a vendor ID is not available.

### hashCode

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by `https://developer.android.com/reference/kotlin/java/util/HashMap.html#`.

The general contract of `hashCode` is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the `hashCode` method must consistently return the same integer, provided no information used in `equals` comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce the same integer result.
- It is *not* required that if two objects are unequal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

### isOpen

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isOpen(): Boolean
```

Returns whether the HID device is currently open and ready for communication.

Note: This method returns `false` while the device is in the process of opening. It only returns `true` after the `https://developer.android.com/reference/kotlin/android/hardware/hid/HidDevice#open(java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` operation has successfully completed.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the device is fully opened; `false` otherwise. |

### open

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun open(
    executor: Executor, 
    callback: OutcomeReceiver<HidDevice!, Exception!>
): Unit
```

Opens the HID device so that it can be used to send and receive HID reports.

This is an asynchronous operation. If an open operation is already in progress, the provided callback is queued and will be notified once the underlying operation completes. The state transitions are as follows:

- If the device is already **opened** , `callback.onResult` is invoked immediately.
- If the device is currently **opening** , the request is queued and `callback` will be notified when the existing operation finishes.
- If the device is **closed**, it transitions to an opening state and attempts to establish a connection via the system service.

On success, `callback.onResult` is called with this `https://developer.android.com/reference/kotlin/android/hardware/hid/HidDevice#` instance. On failure, `callback.onError` is called with one of the following:

- `https://developer.android.com/reference/kotlin/java/io/IOException.html#`: If the underlying hardware device (e.g., hidraw node) could not be accessed or the system service returned a failure.
- `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#`: If the caller lacks the required permission, or the user has rejected access to the device.
- `https://developer.android.com/reference/kotlin/android/os/RemoteException.html#`: If the HID system service is unreachable.

. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_HID:kotlin.String`

| Parameters ||
|---|---|
| `executor` | [Executor](../java.util.concurrent/Executor.md): The executor on which the callback will be invoked. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [OutcomeReceiver](../android.os/OutcomeReceiver.md)\< [HidDevice](HidDevice.md)!, [Exception](../java.lang/Exception.md)!\>: The object to be notified of success or failure. This value cannot be `null`. |

### registerEventListener

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun registerEventListener(
    executor: Executor, 
    listener: HidEventListener
): Unit
```

Registers a listener to receive real-time input reports and hotplug events for this HID device. If the listener is already registered, this call does nothing. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_HID:kotlin.String`

| Parameters ||
|---|---|
| `executor` | [Executor](../java.util.concurrent/Executor.md): The executor on which callback events will be executed. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `listener` | [HidEventListener](HidEventListener.md): The callback listener to register. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If the device is not open or FMQ session establishment fails. |

### sendFeatureReport

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun sendFeatureReport(
    report: Report, 
    executor: Executor, 
    callback: OutcomeReceiver<Void!, Exception!>
): Unit
```

Send a feature report to the HID device.

The device must be opened first before calling this method.

On success, `callback.onResult` is called with `null`. On failure, `callback.onError` is called with one of the following:

- `https://developer.android.com/reference/kotlin/java/io/IOException.html#`: If the underlying hardware device could not be accessed or the system service returned a failure.
- `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#`: If the caller lacks the required permission.

. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_HID:kotlin.String`

| Parameters ||
|---|---|
| `report` | [Report](Report.md): the feature report to send. This value cannot be `null`. |
| `executor` | [Executor](../java.util.concurrent/Executor.md): the executor on which the callback will be invoked. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [OutcomeReceiver](../android.os/OutcomeReceiver.md)\< [Void](../java.lang/Void.md)!, [Exception](../java.lang/Exception.md)!\>: the callback object to be used to notify of an error. This value cannot be `null`. |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if the device is not open. |

### sendOutputReport

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun sendOutputReport(
    report: Report, 
    executor: Executor, 
    callback: OutcomeReceiver<Void!, Exception!>
): Unit
```

Send an output report to the HID device.

The device must be opened first before calling this method.

On success, `callback.onResult` is called with `null`. On failure, `callback.onError` is called with one of the following:

- `https://developer.android.com/reference/kotlin/java/io/IOException.html#`: If the underlying hardware device could not be accessed or the system service returned a failure.
- `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#`: If the caller lacks the required permission.

. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_HID:kotlin.String`

| Parameters ||
|---|---|
| `report` | [Report](Report.md): the output report to send. This value cannot be `null`. |
| `executor` | [Executor](../java.util.concurrent/Executor.md): the executor on which the callback will be invoked. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [OutcomeReceiver](../android.os/OutcomeReceiver.md)\< [Void](../java.lang/Void.md)!, [Exception](../java.lang/Exception.md)!\>: the callback object to be used to notify of an error. This value cannot be `null`. |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if the device is not open. |

### toString

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### unregisterEventListener

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun unregisterEventListener(listener: HidEventListener): Unit
```

Unregisters an active listener from receiving input reports.

| Parameters ||
|---|---|
| `listener` | [HidEventListener](HidEventListener.md): The callback listener to unregister. This value cannot be `null`. |
