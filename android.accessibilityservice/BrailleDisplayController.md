# BrailleDisplayController

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BrailleDisplayController

Kotlin| [Java](../android/accessibilityservice/BrailleDisplayController.md) 
| --- | --- |

```
interface BrailleDisplayController
```

| [android.accessibilityservice.BrailleDisplayController](../android/accessibilityservice/BrailleDisplayController.md) |

Used to communicate with a Braille display that supports the Braille display HID standard (usage page 0x41).

Only one Braille display may be connected at a time.

## Summary

| Nested classes ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [BrailleDisplayCallback](../android/accessibilityservice/BrailleDisplayController.BrailleDisplayCallback.md) Interface provided to [BrailleDisplayController](../android/accessibilityservice/BrailleDisplayController.md) connection methods to receive callbacks from the system. |

| Public methods ||
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [connect](../android/accessibilityservice/BrailleDisplayController.md))`(`bluetoothDevice:` ` [BluetoothDevice](../android/bluetooth/BluetoothDevice.md)`, `callback:` ` [BrailleDisplayController.BrailleDisplayCallback](../android/accessibilityservice/BrailleDisplayController.BrailleDisplayCallback.md)`)` Connects to the requested bluetooth Braille display using the Braille display HID standard (usage page 0x41). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [connect](../android/accessibilityservice/BrailleDisplayController.md))`(`bluetoothDevice:` ` [BluetoothDevice](../android/bluetooth/BluetoothDevice.md)`, `callbackExecutor:` ` [Executor](../java/util/concurrent/Executor.md)`, `callback:` ` [BrailleDisplayController.BrailleDisplayCallback](../android/accessibilityservice/BrailleDisplayController.BrailleDisplayCallback.md)`)` Connects to the requested bluetooth Braille display using the Braille display HID standard (usage page 0x41). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [connect](../android/accessibilityservice/BrailleDisplayController.md))`(`usbDevice:` ` [UsbDevice](../android/hardware/usb/UsbDevice.md)`, `callback:` ` [BrailleDisplayController.BrailleDisplayCallback](../android/accessibilityservice/BrailleDisplayController.BrailleDisplayCallback.md)`)` Connects to the requested USB Braille display using the Braille display HID standard (usage page 0x41). |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [connect](../android/accessibilityservice/BrailleDisplayController.md))`(`usbDevice:` ` [UsbDevice](../android/hardware/usb/UsbDevice.md)`, `callbackExecutor:` ` [Executor](../java/util/concurrent/Executor.md)`, `callback:` ` [BrailleDisplayController.BrailleDisplayCallback](../android/accessibilityservice/BrailleDisplayController.BrailleDisplayCallback.md)`)` Connects to the requested USB Braille display using the Braille display HID standard (usage page 0x41). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [disconnect](../android/accessibilityservice/BrailleDisplayController.md))`()` Disconnects from the currently connected Braille display. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isConnected](../android/accessibilityservice/BrailleDisplayController.md))`()` Returns true if a Braille display is currently connected, otherwise false. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](../android/accessibilityservice/BrailleDisplayController.md))`(`buffer:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`)` Writes a HID report to the currently connected Braille display. |

## Public methods

### connect

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun connect(
    bluetoothDevice: BluetoothDevice, 
    callback: BrailleDisplayController.BrailleDisplayCallback
): Unit
```

Connects to the requested bluetooth Braille display using the Braille display HID standard (usage page 0x41).

If successful then the HID report descriptor will be provided to [BrailleDisplayCallback.onConnected](../android/accessibilityservice/BrailleDisplayController.BrailleDisplayCallback.md))and the Braille display will start sending incoming input bytes to [BrailleDisplayCallback.onInput](../android/accessibilityservice/BrailleDisplayController.BrailleDisplayCallback.md)). If there is an error in reading input then the system will disconnect the Braille display.

Note that the callbacks will be executed on the main thread using [AccessibilityService.getMainExecutor()](../android/content/ContextWrapper.md)). To specify the execution thread, use [connect(android.bluetooth.BluetoothDevice,java.util.concurrent.Executor,android.accessibilityservice.BrailleDisplayController.BrailleDisplayCallback)](../android/accessibilityservice/BrailleDisplayController.md)). 
Requires [android.Manifest.permission#BLUETOOTH_CONNECT](../android/Manifest.permission.md)

| Parameters ||
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `bluetoothDevice` | [BluetoothDevice](../android/bluetooth/BluetoothDevice.md):The Braille display device. This value cannot be`null`. |
| `callback` | [BrailleDisplayController.BrailleDisplayCallback](../android/accessibilityservice/BrailleDisplayController.BrailleDisplayCallback.md):Callbacks used to provide connection results. This value cannot be`null`. |

| Exceptions ||
|-----------------------------------|---------------------------------------------------------------|
| `java.lang.IllegalStateException` | if a Braille display is already connected to this controller. |

**See Also**

- [android.accessibilityservice.BrailleDisplayController.BrailleDisplayCallback#onConnected](../android/accessibilityservice/BrailleDisplayController.BrailleDisplayCallback.md))
- [android.accessibilityservice.BrailleDisplayController.BrailleDisplayCallback#onConnectionFailed](../android/accessibilityservice/BrailleDisplayController.BrailleDisplayCallback.md)) 

### connect

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun connect(
    bluetoothDevice: BluetoothDevice, 
    callbackExecutor: Executor, 
    callback: BrailleDisplayController.BrailleDisplayCallback
): Unit
```

Connects to the requested bluetooth Braille display using the Braille display HID standard (usage page 0x41).

If successful then the HID report descriptor will be provided to [BrailleDisplayCallback.onConnected](../android/accessibilityservice/BrailleDisplayController.BrailleDisplayCallback.md))and the Braille display will start sending incoming input bytes to [BrailleDisplayCallback.onInput](../android/accessibilityservice/BrailleDisplayController.BrailleDisplayCallback.md)). If there is an error in reading input then the system will disconnect the Braille display. 
Requires [android.Manifest.permission#BLUETOOTH_CONNECT](../android/Manifest.permission.md)

| Parameters ||
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `bluetoothDevice` | [BluetoothDevice](../android/bluetooth/BluetoothDevice.md):The Braille display device. This value cannot be`null`. |
| `callbackExecutor` | [Executor](../java/util/concurrent/Executor.md):Executor for executing the provided callbacks. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](../java/util/concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android/content/Context.md)). Otherwise, provide an [Executor](../java/util/concurrent/Executor.md) that dispatches to an appropriate thread. |
| `callback` | [BrailleDisplayController.BrailleDisplayCallback](../android/accessibilityservice/BrailleDisplayController.BrailleDisplayCallback.md):Callbacks used to provide connection results. This value cannot be`null`. |
| --- | --- |

| Exceptions ||
|-----------------------------------|---------------------------------------------------------------|
| `java.lang.IllegalStateException` | if a Braille display is already connected to this controller. |

**See Also**

- [android.accessibilityservice.BrailleDisplayController.BrailleDisplayCallback#onConnected](../android/accessibilityservice/BrailleDisplayController.BrailleDisplayCallback.md))
- [android.accessibilityservice.BrailleDisplayController.BrailleDisplayCallback#onConnectionFailed](../android/accessibilityservice/BrailleDisplayController.BrailleDisplayCallback.md)) 

### connect

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun connect(
    usbDevice: UsbDevice, 
    callback: BrailleDisplayController.BrailleDisplayCallback
): Unit
```

Connects to the requested USB Braille display using the Braille display HID standard (usage page 0x41).

If successful then the HID report descriptor will be provided to [BrailleDisplayCallback.onConnected](../android/accessibilityservice/BrailleDisplayController.BrailleDisplayCallback.md))and the Braille display will start sending incoming input bytes to [BrailleDisplayCallback.onInput](../android/accessibilityservice/BrailleDisplayController.BrailleDisplayCallback.md)). If there is an error in reading input then the system will disconnect the Braille display.

The accessibility service app must already have approval to access the USB device from the standard [android.hardware.usb.UsbManager](../android/hardware/usb/UsbManager.md) access approval process.

Note that the callbacks will be executed on the main thread using [AccessibilityService.getMainExecutor()](../android/content/ContextWrapper.md)). To specify the execution thread, use [connect(android.hardware.usb.UsbDevice,java.util.concurrent.Executor,android.accessibilityservice.BrailleDisplayController.BrailleDisplayCallback)](../android/accessibilityservice/BrailleDisplayController.md)).

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `usbDevice` | [UsbDevice](../android/hardware/usb/UsbDevice.md):The Braille display device. This value cannot be`null`. |
| `callback` | [BrailleDisplayController.BrailleDisplayCallback](../android/accessibilityservice/BrailleDisplayController.BrailleDisplayCallback.md):Callbacks used to provide connection results. This value cannot be`null`. |

| Exceptions ||
|-----------------------------------|---------------------------------------------------------------|
| `java.lang.SecurityException` | if the caller does not have USB device approval. |
| `java.lang.IllegalStateException` | if a Braille display is already connected to this controller. |

**See Also**

- [android.accessibilityservice.BrailleDisplayController.BrailleDisplayCallback#onConnected](../android/accessibilityservice/BrailleDisplayController.BrailleDisplayCallback.md))
- [android.accessibilityservice.BrailleDisplayController.BrailleDisplayCallback#onConnectionFailed](../android/accessibilityservice/BrailleDisplayController.BrailleDisplayCallback.md)) 

### connect

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun connect(
    usbDevice: UsbDevice, 
    callbackExecutor: Executor, 
    callback: BrailleDisplayController.BrailleDisplayCallback
): Unit
```

Connects to the requested USB Braille display using the Braille display HID standard (usage page 0x41).

If successful then the HID report descriptor will be provided to [BrailleDisplayCallback.onConnected](../android/accessibilityservice/BrailleDisplayController.BrailleDisplayCallback.md))and the Braille display will start sending incoming input bytes to [BrailleDisplayCallback.onInput](../android/accessibilityservice/BrailleDisplayController.BrailleDisplayCallback.md)). If there is an error in reading input then the system will disconnect the Braille display.

The accessibility service app must already have approval to access the USB device from the standard [android.hardware.usb.UsbManager](../android/hardware/usb/UsbManager.md) access approval process.

| Parameters ||
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `usbDevice` | [UsbDevice](../android/hardware/usb/UsbDevice.md):The Braille display device. This value cannot be`null`. |
| `callbackExecutor` | [Executor](../java/util/concurrent/Executor.md):Executor for executing the provided callbacks. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](../java/util/concurrent/Executor.md), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](../android/content/Context.md)). Otherwise, provide an [Executor](../java/util/concurrent/Executor.md) that dispatches to an appropriate thread. |
| `callback` | [BrailleDisplayController.BrailleDisplayCallback](../android/accessibilityservice/BrailleDisplayController.BrailleDisplayCallback.md):Callbacks used to provide connection results. This value cannot be`null`. |
| --- | --- |

| Exceptions ||
|-----------------------------------|---------------------------------------------------------------|
| `java.lang.SecurityException` | if the caller does not have USB device approval. |
| `java.lang.IllegalStateException` | if a Braille display is already connected to this controller. |

**See Also**

- [android.accessibilityservice.BrailleDisplayController.BrailleDisplayCallback#onConnected](../android/accessibilityservice/BrailleDisplayController.BrailleDisplayCallback.md))
- [android.accessibilityservice.BrailleDisplayController.BrailleDisplayCallback#onConnectionFailed](../android/accessibilityservice/BrailleDisplayController.BrailleDisplayCallback.md)) 

### disconnect

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun disconnect(): Unit
```

Disconnects from the currently connected Braille display. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/accessibilityservice/BrailleDisplayController#isConnected()> 

### isConnected

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isConnected(): Boolean
```

Returns true if a Braille display is currently connected, otherwise false. 
**See Also**

### write

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun write(buffer: ByteArray): Unit
```

Writes a HID report to the currently connected Braille display.

This method returns immediately after dispatching the write request to the system. If the system experiences an error in writing output (e.g. the Braille display is unplugged after the system receives the write request but before writing the bytes to the Braille display) then the system will disconnect the Braille display, which calls [BrailleDisplayCallback.onDisconnected()](../android/accessibilityservice/BrailleDisplayController.BrailleDisplayCallback.md)).

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `buffer` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html):The bytes to write to the Braille display. These bytes should be formatted according to the HID report descriptor and the HIDRAW kernel driver. This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if there is no currently connected Braille display. |
| `java.lang.IllegalArgumentException` | if the buffer exceeds the maximum safe payload size for binder transactions of [IBinder.getSuggestedMaxIpcSizeBytes()](../android/os/IBinder.md)) |
