# BrailleDisplayController

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BrailleDisplayController

Kotlin| [Java](https://developer.android.com/reference/android/accessibilityservice/BrailleDisplayController "View this page in Java") 

```
interface BrailleDisplayController
```

| [android.accessibilityservice.BrailleDisplayController](https://developer.android.com/reference/kotlin/android/accessibilityservice/BrailleDisplayController#) |

Used to communicate with a Braille display that supports the Braille display HID standard (usage page 0x41).

Only one Braille display may be connected at a time.

## Summary

| Nested classes ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [BrailleDisplayCallback](https://developer.android.com/reference/kotlin/android/accessibilityservice/BrailleDisplayController.BrailleDisplayCallback) Interface provided to [BrailleDisplayController](https://developer.android.com/reference/kotlin/android/accessibilityservice/BrailleDisplayController#) connection methods to receive callbacks from the system. |

| Public methods ||
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [connect](https://developer.android.com/reference/kotlin/android/accessibilityservice/BrailleDisplayController#connect(android.bluetooth.BluetoothDevice,%20android.accessibilityservice.BrailleDisplayController.BrailleDisplayCallback))`(`bluetoothDevice:` ` [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice.html#)`, `callback:` ` [BrailleDisplayController.BrailleDisplayCallback](https://developer.android.com/reference/kotlin/android/accessibilityservice/BrailleDisplayController.BrailleDisplayCallback)`)` Connects to the requested bluetooth Braille display using the Braille display HID standard (usage page 0x41). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [connect](https://developer.android.com/reference/kotlin/android/accessibilityservice/BrailleDisplayController#connect(android.bluetooth.BluetoothDevice,%20java.util.concurrent.Executor,%20android.accessibilityservice.BrailleDisplayController.BrailleDisplayCallback))`(`bluetoothDevice:` ` [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice.html#)`, `callbackExecutor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `callback:` ` [BrailleDisplayController.BrailleDisplayCallback](https://developer.android.com/reference/kotlin/android/accessibilityservice/BrailleDisplayController.BrailleDisplayCallback)`)` Connects to the requested bluetooth Braille display using the Braille display HID standard (usage page 0x41). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [connect](https://developer.android.com/reference/kotlin/android/accessibilityservice/BrailleDisplayController#connect(android.hardware.usb.UsbDevice,%20android.accessibilityservice.BrailleDisplayController.BrailleDisplayCallback))`(`usbDevice:` ` [UsbDevice](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbDevice.html#)`, `callback:` ` [BrailleDisplayController.BrailleDisplayCallback](https://developer.android.com/reference/kotlin/android/accessibilityservice/BrailleDisplayController.BrailleDisplayCallback)`)` Connects to the requested USB Braille display using the Braille display HID standard (usage page 0x41). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [connect](https://developer.android.com/reference/kotlin/android/accessibilityservice/BrailleDisplayController#connect(android.hardware.usb.UsbDevice,%20java.util.concurrent.Executor,%20android.accessibilityservice.BrailleDisplayController.BrailleDisplayCallback))`(`usbDevice:` ` [UsbDevice](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbDevice.html#)`, `callbackExecutor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `callback:` ` [BrailleDisplayController.BrailleDisplayCallback](https://developer.android.com/reference/kotlin/android/accessibilityservice/BrailleDisplayController.BrailleDisplayCallback)`)` Connects to the requested USB Braille display using the Braille display HID standard (usage page 0x41). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [disconnect](https://developer.android.com/reference/kotlin/android/accessibilityservice/BrailleDisplayController#disconnect())`()` Disconnects from the currently connected Braille display. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isConnected](https://developer.android.com/reference/kotlin/android/accessibilityservice/BrailleDisplayController#isConnected())`()` Returns true if a Braille display is currently connected, otherwise false. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [write](https://developer.android.com/reference/kotlin/android/accessibilityservice/BrailleDisplayController#write(kotlin.ByteArray))`(`buffer:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`)` Writes a HID report to the currently connected Braille display. |

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

If successful then the HID report descriptor will be provided to [BrailleDisplayCallback.onConnected](https://developer.android.com/reference/kotlin/android/accessibilityservice/BrailleDisplayController.BrailleDisplayCallback#onConnected(kotlin.ByteArray))and the Braille display will start sending incoming input bytes to [BrailleDisplayCallback.onInput](https://developer.android.com/reference/kotlin/android/accessibilityservice/BrailleDisplayController.BrailleDisplayCallback#onInput(kotlin.ByteArray)). If there is an error in reading input then the system will disconnect the Braille display.

Note that the callbacks will be executed on the main thread using [AccessibilityService.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getMainExecutor()). To specify the execution thread, use [connect(android.bluetooth.BluetoothDevice,java.util.concurrent.Executor,android.accessibilityservice.BrailleDisplayController.BrailleDisplayCallback)](https://developer.android.com/reference/kotlin/android/accessibilityservice/BrailleDisplayController#connect(android.bluetooth.BluetoothDevice,%20java.util.concurrent.Executor,%20android.accessibilityservice.BrailleDisplayController.BrailleDisplayCallback)). 
Requires [android.Manifest.permission#BLUETOOTH_CONNECT](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String)

| Parameters ||
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `bluetoothDevice` | [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice.html#):The Braille display device. This value cannot be`null`. |
| `callback` | [BrailleDisplayController.BrailleDisplayCallback](https://developer.android.com/reference/kotlin/android/accessibilityservice/BrailleDisplayController.BrailleDisplayCallback):Callbacks used to provide connection results. This value cannot be`null`. |

| Exceptions ||
|-----------------------------------|---------------------------------------------------------------|
| `java.lang.IllegalStateException` | if a Braille display is already connected to this controller. |

**See Also**

- [android.accessibilityservice.BrailleDisplayController.BrailleDisplayCallback#onConnected](https://developer.android.com/reference/kotlin/android/accessibilityservice/BrailleDisplayController.BrailleDisplayCallback#onConnected(kotlin.ByteArray))
- [android.accessibilityservice.BrailleDisplayController.BrailleDisplayCallback#onConnectionFailed](https://developer.android.com/reference/kotlin/android/accessibilityservice/BrailleDisplayController.BrailleDisplayCallback#onConnectionFailed(kotlin.Int)) 

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

If successful then the HID report descriptor will be provided to [BrailleDisplayCallback.onConnected](https://developer.android.com/reference/kotlin/android/accessibilityservice/BrailleDisplayController.BrailleDisplayCallback#onConnected(kotlin.ByteArray))and the Braille display will start sending incoming input bytes to [BrailleDisplayCallback.onInput](https://developer.android.com/reference/kotlin/android/accessibilityservice/BrailleDisplayController.BrailleDisplayCallback#onInput(kotlin.ByteArray)). If there is an error in reading input then the system will disconnect the Braille display. 
Requires [android.Manifest.permission#BLUETOOTH_CONNECT](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String)

| Parameters ||
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `bluetoothDevice` | [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice.html#):The Braille display device. This value cannot be`null`. |
| `callbackExecutor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):Executor for executing the provided callbacks. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| `callback` | [BrailleDisplayController.BrailleDisplayCallback](https://developer.android.com/reference/kotlin/android/accessibilityservice/BrailleDisplayController.BrailleDisplayCallback):Callbacks used to provide connection results. This value cannot be`null`. |

| Exceptions ||
|-----------------------------------|---------------------------------------------------------------|
| `java.lang.IllegalStateException` | if a Braille display is already connected to this controller. |

**See Also**

- [android.accessibilityservice.BrailleDisplayController.BrailleDisplayCallback#onConnected](https://developer.android.com/reference/kotlin/android/accessibilityservice/BrailleDisplayController.BrailleDisplayCallback#onConnected(kotlin.ByteArray))
- [android.accessibilityservice.BrailleDisplayController.BrailleDisplayCallback#onConnectionFailed](https://developer.android.com/reference/kotlin/android/accessibilityservice/BrailleDisplayController.BrailleDisplayCallback#onConnectionFailed(kotlin.Int)) 

### connect

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun connect(
    usbDevice: UsbDevice, 
    callback: BrailleDisplayController.BrailleDisplayCallback
): Unit
```

Connects to the requested USB Braille display using the Braille display HID standard (usage page 0x41).

If successful then the HID report descriptor will be provided to [BrailleDisplayCallback.onConnected](https://developer.android.com/reference/kotlin/android/accessibilityservice/BrailleDisplayController.BrailleDisplayCallback#onConnected(kotlin.ByteArray))and the Braille display will start sending incoming input bytes to [BrailleDisplayCallback.onInput](https://developer.android.com/reference/kotlin/android/accessibilityservice/BrailleDisplayController.BrailleDisplayCallback#onInput(kotlin.ByteArray)). If there is an error in reading input then the system will disconnect the Braille display.

The accessibility service app must already have approval to access the USB device from the standard [android.hardware.usb.UsbManager](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbManager.html#) access approval process.

Note that the callbacks will be executed on the main thread using [AccessibilityService.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/ContextWrapper.html#getMainExecutor()). To specify the execution thread, use [connect(android.hardware.usb.UsbDevice,java.util.concurrent.Executor,android.accessibilityservice.BrailleDisplayController.BrailleDisplayCallback)](https://developer.android.com/reference/kotlin/android/accessibilityservice/BrailleDisplayController#connect(android.hardware.usb.UsbDevice,%20java.util.concurrent.Executor,%20android.accessibilityservice.BrailleDisplayController.BrailleDisplayCallback)).

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `usbDevice` | [UsbDevice](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbDevice.html#):The Braille display device. This value cannot be`null`. |
| `callback` | [BrailleDisplayController.BrailleDisplayCallback](https://developer.android.com/reference/kotlin/android/accessibilityservice/BrailleDisplayController.BrailleDisplayCallback):Callbacks used to provide connection results. This value cannot be`null`. |

| Exceptions ||
|-----------------------------------|---------------------------------------------------------------|
| `java.lang.SecurityException` | if the caller does not have USB device approval. |
| `java.lang.IllegalStateException` | if a Braille display is already connected to this controller. |

**See Also**

- [android.accessibilityservice.BrailleDisplayController.BrailleDisplayCallback#onConnected](https://developer.android.com/reference/kotlin/android/accessibilityservice/BrailleDisplayController.BrailleDisplayCallback#onConnected(kotlin.ByteArray))
- [android.accessibilityservice.BrailleDisplayController.BrailleDisplayCallback#onConnectionFailed](https://developer.android.com/reference/kotlin/android/accessibilityservice/BrailleDisplayController.BrailleDisplayCallback#onConnectionFailed(kotlin.Int)) 

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

If successful then the HID report descriptor will be provided to [BrailleDisplayCallback.onConnected](https://developer.android.com/reference/kotlin/android/accessibilityservice/BrailleDisplayController.BrailleDisplayCallback#onConnected(kotlin.ByteArray))and the Braille display will start sending incoming input bytes to [BrailleDisplayCallback.onInput](https://developer.android.com/reference/kotlin/android/accessibilityservice/BrailleDisplayController.BrailleDisplayCallback#onInput(kotlin.ByteArray)). If there is an error in reading input then the system will disconnect the Braille display.

The accessibility service app must already have approval to access the USB device from the standard [android.hardware.usb.UsbManager](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbManager.html#) access approval process.

| Parameters ||
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `usbDevice` | [UsbDevice](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbDevice.html#):The Braille display device. This value cannot be`null`. |
| `callbackExecutor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):Executor for executing the provided callbacks. This value cannot be`null`. Callback and listener events are dispatched through this [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#), providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use [Context.getMainExecutor()](https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()). Otherwise, provide an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that dispatches to an appropriate thread. |
| `callback` | [BrailleDisplayController.BrailleDisplayCallback](https://developer.android.com/reference/kotlin/android/accessibilityservice/BrailleDisplayController.BrailleDisplayCallback):Callbacks used to provide connection results. This value cannot be`null`. |

| Exceptions ||
|-----------------------------------|---------------------------------------------------------------|
| `java.lang.SecurityException` | if the caller does not have USB device approval. |
| `java.lang.IllegalStateException` | if a Braille display is already connected to this controller. |

**See Also**

- [android.accessibilityservice.BrailleDisplayController.BrailleDisplayCallback#onConnected](https://developer.android.com/reference/kotlin/android/accessibilityservice/BrailleDisplayController.BrailleDisplayCallback#onConnected(kotlin.ByteArray))
- [android.accessibilityservice.BrailleDisplayController.BrailleDisplayCallback#onConnectionFailed](https://developer.android.com/reference/kotlin/android/accessibilityservice/BrailleDisplayController.BrailleDisplayCallback#onConnectionFailed(kotlin.Int)) 

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

This method returns immediately after dispatching the write request to the system. If the system experiences an error in writing output (e.g. the Braille display is unplugged after the system receives the write request but before writing the bytes to the Braille display) then the system will disconnect the Braille display, which calls [BrailleDisplayCallback.onDisconnected()](https://developer.android.com/reference/kotlin/android/accessibilityservice/BrailleDisplayController.BrailleDisplayCallback#onDisconnected()).

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `buffer` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html):The bytes to write to the Braille display. These bytes should be formatted according to the HID report descriptor and the HIDRAW kernel driver. This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if there is no currently connected Braille display. |
| `java.lang.IllegalArgumentException` | if the buffer exceeds the maximum safe payload size for binder transactions of [IBinder.getSuggestedMaxIpcSizeBytes()](https://developer.android.com/reference/kotlin/android/os/IBinder.html#getSuggestedMaxIpcSizeBytes()) |
