# MidiManager

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MidiManager

Kotlin| [Java](https://developer.android.com/reference/android/media/midi/MidiManager "View this page in Java") 
| --- | --- |

```
class MidiManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.midi.MidiManager](https://developer.android.com/reference/kotlin/android/media/midi/MidiManager#) |

This class is the public application interface to the MIDI service. 
Requires the [PackageManager#FEATURE_MIDI](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_MIDI:kotlin.String) feature which can be detected using [PackageManager.hasSystemFeature(String)](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#hasSystemFeature(kotlin.String)).

## Summary

| Nested classes ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [DeviceCallback](https://developer.android.com/reference/kotlin/android/media/midi/MidiManager.DeviceCallback) Callback class used for clients to receive MIDI device added and removed notifications |
| abstract | [OnDeviceOpenedListener](https://developer.android.com/reference/kotlin/android/media/midi/MidiManager.OnDeviceOpenedListener) Listener class used for receiving the results of [openDevice](https://developer.android.com/reference/kotlin/android/media/midi/MidiManager#openDevice(android.media.midi.MidiDeviceInfo,%20android.media.midi.MidiManager.OnDeviceOpenedListener,%20android.os.Handler))and [openBluetoothDevice](https://developer.android.com/reference/kotlin/android/media/midi/MidiManager#openBluetoothDevice(android.bluetooth.BluetoothDevice,%20android.media.midi.MidiManager.OnDeviceOpenedListener,%20android.os.Handler)) |

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRANSPORT_MIDI_BYTE_STREAM](https://developer.android.com/reference/kotlin/android/media/midi/MidiManager#TRANSPORT_MIDI_BYTE_STREAM:kotlin.Int) Constant representing MIDI devices. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRANSPORT_UNIVERSAL_MIDI_PACKETS](https://developer.android.com/reference/kotlin/android/media/midi/MidiManager#TRANSPORT_UNIVERSAL_MIDI_PACKETS:kotlin.Int) Constant representing Universal MIDI devices. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [MidiDeviceInfo](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo)!\>! | [getDevices](https://developer.android.com/reference/kotlin/android/media/midi/MidiManager#getDevices())`()` Gets a list of connected MIDI devices. |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [MidiDeviceInfo](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo)!\> | [getDevicesForTransport](https://developer.android.com/reference/kotlin/android/media/midi/MidiManager#getDevicesForTransport(kotlin.Int))`(`transport:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Gets a list of connected MIDI devices by transport. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [openBluetoothDevice](https://developer.android.com/reference/kotlin/android/media/midi/MidiManager#openBluetoothDevice(android.bluetooth.BluetoothDevice,%20android.media.midi.MidiManager.OnDeviceOpenedListener,%20android.os.Handler))`(`bluetoothDevice:` ` [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice.html#)!`, `listener:` ` [MidiManager.OnDeviceOpenedListener](https://developer.android.com/reference/kotlin/android/media/midi/MidiManager.OnDeviceOpenedListener)!`, `handler:` ` [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)!`)` Opens a Bluetooth MIDI device for reading and writing. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [openDevice](https://developer.android.com/reference/kotlin/android/media/midi/MidiManager#openDevice(android.media.midi.MidiDeviceInfo,%20android.media.midi.MidiManager.OnDeviceOpenedListener,%20android.os.Handler))`(`deviceInfo:` ` [MidiDeviceInfo](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo)!`, `listener:` ` [MidiManager.OnDeviceOpenedListener](https://developer.android.com/reference/kotlin/android/media/midi/MidiManager.OnDeviceOpenedListener)!`, `handler:` ` [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)!`)` Opens a MIDI device for reading and writing. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerDeviceCallback](https://developer.android.com/reference/kotlin/android/media/midi/MidiManager#registerDeviceCallback(android.media.midi.MidiManager.DeviceCallback,%20android.os.Handler))`(`callback:` ` [MidiManager.DeviceCallback](https://developer.android.com/reference/kotlin/android/media/midi/MidiManager.DeviceCallback)!`, `handler:` ` [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)!`)` Registers a callback to receive notifications when MIDI 1. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerDeviceCallback](https://developer.android.com/reference/kotlin/android/media/midi/MidiManager#registerDeviceCallback(kotlin.Int,%20java.util.concurrent.Executor,%20android.media.midi.MidiManager.DeviceCallback))`(`transport:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `callback:` ` [MidiManager.DeviceCallback](https://developer.android.com/reference/kotlin/android/media/midi/MidiManager.DeviceCallback)`)` Registers a callback to receive notifications when MIDI devices are added and removed for a specific transport type. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterDeviceCallback](https://developer.android.com/reference/kotlin/android/media/midi/MidiManager#unregisterDeviceCallback(android.media.midi.MidiManager.DeviceCallback))`(`callback:` ` [MidiManager.DeviceCallback](https://developer.android.com/reference/kotlin/android/media/midi/MidiManager.DeviceCallback)!`)` Unregisters a [DeviceCallback](https://developer.android.com/reference/kotlin/android/media/midi/MidiManager.DeviceCallback). |

## Constants

### TRANSPORT_MIDI_BYTE_STREAM

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TRANSPORT_MIDI_BYTE_STREAM: Int
```

Constant representing MIDI devices. These devices do NOT support Universal MIDI Packets by default. These support the original MIDI 1.0 byte stream. When communicating to a USB device, a raw byte stream will be padded for USB. Likewise, for a Bluetooth device, the raw bytes will be converted for Bluetooth. For virtual devices, the byte stream will be passed directly. If Universal MIDI Packets are needed, please use MIDI-CI. 

 Value: 1

**See Also**

- [android.media.midi.MidiManager#getDevicesForTransport](https://developer.android.com/reference/kotlin/android/media/midi/MidiManager#getDevicesForTransport(kotlin.Int)) 

### TRANSPORT_UNIVERSAL_MIDI_PACKETS

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TRANSPORT_UNIVERSAL_MIDI_PACKETS: Int
```

Constant representing Universal MIDI devices. These devices do support Universal MIDI Packets (UMP) by default. When sending data to these devices, please send UMP. Packets should always be a multiple of 4 bytes. UMP is defined in the USB MIDI 2.0 spec. Please read the standard for more info. 

 Value: 2

**See Also**

- [android.media.midi.MidiManager#getDevicesForTransport](https://developer.android.com/reference/kotlin/android/media/midi/MidiManager#getDevicesForTransport(kotlin.Int))

## Public methods

### getDevices

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDevices(): Array<MidiDeviceInfo!>!
```

**Deprecated:** *Use [getDevicesForTransport](https://developer.android.com/reference/kotlin/android/media/midi/MidiManager#getDevicesForTransport(kotlin.Int))instead.*

Gets a list of connected MIDI devices. This returns all devices that do not default to Universal MIDI Packets. To get those instead, please call [getDevicesForTransport](https://developer.android.com/reference/kotlin/android/media/midi/MidiManager#getDevicesForTransport(kotlin.Int))instead.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [MidiDeviceInfo](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo)!>! | an array of MIDI devices |

### getDevicesForTransport

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDevicesForTransport(transport: Int): MutableSet<MidiDeviceInfo!>
```

Gets a list of connected MIDI devices by transport. TRANSPORT_MIDI_BYTE_STREAM is used for MIDI 1.0 and is the most common. For devices with built in Universal MIDI Packet support, use TRANSPORT_UNIVERSAL_MIDI_PACKETS instead.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `transport` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The transport to be used. This is either TRANSPORT_MIDI_BYTE_STREAM or TRANSPORT_UNIVERSAL_MIDI_PACKETS. Value is [android.media.midi.MidiManager#TRANSPORT_MIDI_BYTE_STREAM](https://developer.android.com/reference/kotlin/android/media/midi/MidiManager#TRANSPORT_MIDI_BYTE_STREAM:kotlin.Int), or [android.media.midi.MidiManager#TRANSPORT_UNIVERSAL_MIDI_PACKETS](https://developer.android.com/reference/kotlin/android/media/midi/MidiManager#TRANSPORT_UNIVERSAL_MIDI_PACKETS:kotlin.Int) |

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [MidiDeviceInfo](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo)!> | a collection of MIDI devices This value cannot be`null`. |

### openBluetoothDevice

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun openBluetoothDevice(
    bluetoothDevice: BluetoothDevice!, 
    listener: MidiManager.OnDeviceOpenedListener!, 
    handler: Handler!
): Unit
```

Opens a Bluetooth MIDI device for reading and writing. Bluetooth MIDI devices are only available after openBluetoothDevice() is called. Once that happens anywhere in the system, then the BLE-MIDI device will appear as just another MidiDevice to other apps. If the device opened using openBluetoothDevice() is closed, then it will no longer be available. To other apps, it will appear as if the BLE MidiDevice had been unplugged. If a MidiDevice is garbage collected then it will be closed automatically. If you want the BLE-MIDI device to remain available you should keep the object alive. You may close the device with MidiDevice.close().

| Parameters ||
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `bluetoothDevice` | [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice.html#)!:a [android.bluetooth.BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice.html#) to open as a MIDI device |
| `listener` | [MidiManager.OnDeviceOpenedListener](https://developer.android.com/reference/kotlin/android/media/midi/MidiManager.OnDeviceOpenedListener)!:a [MidiManager.OnDeviceOpenedListener](https://developer.android.com/reference/kotlin/android/media/midi/MidiManager.OnDeviceOpenedListener) to be called to receive the result |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)!:the [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#) that will be used for delivering the result. If handler is null, then the thread used for the listener is unspecified. |
| --- | --- |

### openDevice

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun openDevice(
    deviceInfo: MidiDeviceInfo!, 
    listener: MidiManager.OnDeviceOpenedListener!, 
    handler: Handler!
): Unit
```

Opens a MIDI device for reading and writing.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `deviceInfo` | [MidiDeviceInfo](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo)!:a [android.media.midi.MidiDeviceInfo](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo) to open |
| `listener` | [MidiManager.OnDeviceOpenedListener](https://developer.android.com/reference/kotlin/android/media/midi/MidiManager.OnDeviceOpenedListener)!:a [MidiManager.OnDeviceOpenedListener](https://developer.android.com/reference/kotlin/android/media/midi/MidiManager.OnDeviceOpenedListener) to be called to receive the result |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)!:the [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#) that will be used for delivering the result. If handler is null, then the thread used for the listener is unspecified. |
| --- | --- |

### registerDeviceCallback

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun registerDeviceCallback(
    callback: MidiManager.DeviceCallback!, 
    handler: Handler!
): Unit
```

**Deprecated:** *Use [registerDeviceCallback(int,java.util.concurrent.Executor,android.media.midi.MidiManager.DeviceCallback)](https://developer.android.com/reference/kotlin/android/media/midi/MidiManager#registerDeviceCallback(kotlin.Int,%20java.util.concurrent.Executor,%20android.media.midi.MidiManager.DeviceCallback))instead.*

Registers a callback to receive notifications when MIDI 1.0 devices are added and removed. These are devices that do not default to Universal MIDI Packets. To register for a callback for those, call #registerDeviceCallback instead. The [DeviceCallback.onDeviceStatusChanged](https://developer.android.com/reference/kotlin/android/media/midi/MidiManager.DeviceCallback#onDeviceStatusChanged(android.media.midi.MidiDeviceStatus))method will be called immediately for any devices that have open ports. This allows applications to know which input ports are already in use and, therefore, unavailable. Applications should call [getDevices](https://developer.android.com/reference/kotlin/android/media/midi/MidiManager#getDevices())before registering the callback to get a list of devices already added.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [MidiManager.DeviceCallback](https://developer.android.com/reference/kotlin/android/media/midi/MidiManager.DeviceCallback)!:a [DeviceCallback](https://developer.android.com/reference/kotlin/android/media/midi/MidiManager.DeviceCallback) for MIDI device notifications |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)!:The [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#) that will be used for delivering the device notifications. If handler is null, then the thread used for the callback is unspecified. |

### registerDeviceCallback

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun registerDeviceCallback(
    transport: Int, 
    executor: Executor, 
    callback: MidiManager.DeviceCallback
): Unit
```

Registers a callback to receive notifications when MIDI devices are added and removed for a specific transport type. The [DeviceCallback.onDeviceStatusChanged](https://developer.android.com/reference/kotlin/android/media/midi/MidiManager.DeviceCallback#onDeviceStatusChanged(android.media.midi.MidiDeviceStatus))method will be called immediately for any devices that have open ports. This allows applications to know which input ports are already in use and, therefore, unavailable. Applications should call [getDevicesForTransport](https://developer.android.com/reference/kotlin/android/media/midi/MidiManager#getDevicesForTransport(kotlin.Int))before registering the callback to get a list of devices already added.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `transport` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The transport to be used. This is either TRANSPORT_MIDI_BYTE_STREAM or TRANSPORT_UNIVERSAL_MIDI_PACKETS. Value is [android.media.midi.MidiManager#TRANSPORT_MIDI_BYTE_STREAM](https://developer.android.com/reference/kotlin/android/media/midi/MidiManager#TRANSPORT_MIDI_BYTE_STREAM:kotlin.Int), or [android.media.midi.MidiManager#TRANSPORT_UNIVERSAL_MIDI_PACKETS](https://developer.android.com/reference/kotlin/android/media/midi/MidiManager#TRANSPORT_UNIVERSAL_MIDI_PACKETS:kotlin.Int) |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):The [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) that will be used for delivering the device notifications. This value cannot be`null`. |
| `callback` | [MidiManager.DeviceCallback](https://developer.android.com/reference/kotlin/android/media/midi/MidiManager.DeviceCallback):a [DeviceCallback](https://developer.android.com/reference/kotlin/android/media/midi/MidiManager.DeviceCallback) for MIDI device notifications This value cannot be`null`. |
| --- | --- |

### unregisterDeviceCallback

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun unregisterDeviceCallback(callback: MidiManager.DeviceCallback!): Unit
```

Unregisters a [DeviceCallback](https://developer.android.com/reference/kotlin/android/media/midi/MidiManager.DeviceCallback).

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [MidiManager.DeviceCallback](https://developer.android.com/reference/kotlin/android/media/midi/MidiManager.DeviceCallback)!:a [DeviceCallback](https://developer.android.com/reference/kotlin/android/media/midi/MidiManager.DeviceCallback) to unregister |
