# MidiManager

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MidiManager

Kotlin| [Java](../android/media/midi/MidiManager.md) 
| --- | --- |

```
class MidiManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.midi.MidiManager](../android/media/midi/MidiManager.md) |

This class is the public application interface to the MIDI service. 
Requires the [PackageManager#FEATURE_MIDI](../android/content/pm/PackageManager.md) feature which can be detected using [PackageManager.hasSystemFeature(String)](../android/content/pm/PackageManager.md)).

## Summary

| Nested classes ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [DeviceCallback](../android/media/midi/MidiManager.DeviceCallback.md) Callback class used for clients to receive MIDI device added and removed notifications |
| abstract | [OnDeviceOpenedListener](../android/media/midi/MidiManager.OnDeviceOpenedListener.md) Listener class used for receiving the results of [openDevice](../android/media/midi/MidiManager.md))and [openBluetoothDevice](../android/media/midi/MidiManager.md)) |

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRANSPORT_MIDI_BYTE_STREAM](../android/media/midi/MidiManager.md) Constant representing MIDI devices. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRANSPORT_UNIVERSAL_MIDI_PACKETS](../android/media/midi/MidiManager.md) Constant representing Universal MIDI devices. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [MidiDeviceInfo](../android/media/midi/MidiDeviceInfo.md)!\>! | [getDevices](../android/media/midi/MidiManager.md))`()` Gets a list of connected MIDI devices. |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [MidiDeviceInfo](../android/media/midi/MidiDeviceInfo.md)!\> | [getDevicesForTransport](../android/media/midi/MidiManager.md))`(`transport:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Gets a list of connected MIDI devices by transport. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [openBluetoothDevice](../android/media/midi/MidiManager.md))`(`bluetoothDevice:` ` [BluetoothDevice](../android/bluetooth/BluetoothDevice.md)!`, `listener:` ` [MidiManager.OnDeviceOpenedListener](../android/media/midi/MidiManager.OnDeviceOpenedListener.md)!`, `handler:` ` [Handler](../android/os/Handler.md)!`)` Opens a Bluetooth MIDI device for reading and writing. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [openDevice](../android/media/midi/MidiManager.md))`(`deviceInfo:` ` [MidiDeviceInfo](../android/media/midi/MidiDeviceInfo.md)!`, `listener:` ` [MidiManager.OnDeviceOpenedListener](../android/media/midi/MidiManager.OnDeviceOpenedListener.md)!`, `handler:` ` [Handler](../android/os/Handler.md)!`)` Opens a MIDI device for reading and writing. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerDeviceCallback](../android/media/midi/MidiManager.md))`(`callback:` ` [MidiManager.DeviceCallback](../android/media/midi/MidiManager.DeviceCallback.md)!`, `handler:` ` [Handler](../android/os/Handler.md)!`)` Registers a callback to receive notifications when MIDI 1. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerDeviceCallback](../android/media/midi/MidiManager.md))`(`transport:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `executor:` ` [Executor](../java/util/concurrent/Executor.md)`, `callback:` ` [MidiManager.DeviceCallback](../android/media/midi/MidiManager.DeviceCallback.md)`)` Registers a callback to receive notifications when MIDI devices are added and removed for a specific transport type. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterDeviceCallback](../android/media/midi/MidiManager.md))`(`callback:` ` [MidiManager.DeviceCallback](../android/media/midi/MidiManager.DeviceCallback.md)!`)` Unregisters a [DeviceCallback](../android/media/midi/MidiManager.DeviceCallback.md). |

## Constants

### TRANSPORT_MIDI_BYTE_STREAM

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TRANSPORT_MIDI_BYTE_STREAM: Int
```

Constant representing MIDI devices. These devices do NOT support Universal MIDI Packets by default. These support the original MIDI 1.0 byte stream. When communicating to a USB device, a raw byte stream will be padded for USB. Likewise, for a Bluetooth device, the raw bytes will be converted for Bluetooth. For virtual devices, the byte stream will be passed directly. If Universal MIDI Packets are needed, please use MIDI-CI. 

 Value: 1

**See Also**

- [android.media.midi.MidiManager#getDevicesForTransport](../android/media/midi/MidiManager.md)) 

### TRANSPORT_UNIVERSAL_MIDI_PACKETS

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TRANSPORT_UNIVERSAL_MIDI_PACKETS: Int
```

Constant representing Universal MIDI devices. These devices do support Universal MIDI Packets (UMP) by default. When sending data to these devices, please send UMP. Packets should always be a multiple of 4 bytes. UMP is defined in the USB MIDI 2.0 spec. Please read the standard for more info. 

 Value: 2

**See Also**

- [android.media.midi.MidiManager#getDevicesForTransport](../android/media/midi/MidiManager.md))

## Public methods

### getDevices

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDevices(): Array<MidiDeviceInfo!>!
```

**Deprecated:** *Use [getDevicesForTransport](../android/media/midi/MidiManager.md))instead.*

Gets a list of connected MIDI devices. This returns all devices that do not default to Universal MIDI Packets. To get those instead, please call [getDevicesForTransport](../android/media/midi/MidiManager.md))instead.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [MidiDeviceInfo](../android/media/midi/MidiDeviceInfo.md)!>! | an array of MIDI devices |

### getDevicesForTransport

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDevicesForTransport(transport: Int): MutableSet<MidiDeviceInfo!>
```

Gets a list of connected MIDI devices by transport. TRANSPORT_MIDI_BYTE_STREAM is used for MIDI 1.0 and is the most common. For devices with built in Universal MIDI Packet support, use TRANSPORT_UNIVERSAL_MIDI_PACKETS instead.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `transport` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The transport to be used. This is either TRANSPORT_MIDI_BYTE_STREAM or TRANSPORT_UNIVERSAL_MIDI_PACKETS. Value is [android.media.midi.MidiManager#TRANSPORT_MIDI_BYTE_STREAM](../android/media/midi/MidiManager.md), or [android.media.midi.MidiManager#TRANSPORT_UNIVERSAL_MIDI_PACKETS](../android/media/midi/MidiManager.md) |

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [MidiDeviceInfo](../android/media/midi/MidiDeviceInfo.md)!> | a collection of MIDI devices This value cannot be`null`. |

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
| `bluetoothDevice` | [BluetoothDevice](../android/bluetooth/BluetoothDevice.md)!:a [android.bluetooth.BluetoothDevice](../android/bluetooth/BluetoothDevice.md) to open as a MIDI device |
| `listener` | [MidiManager.OnDeviceOpenedListener](../android/media/midi/MidiManager.OnDeviceOpenedListener.md)!:a [MidiManager.OnDeviceOpenedListener](../android/media/midi/MidiManager.OnDeviceOpenedListener.md) to be called to receive the result |
| `handler` | [Handler](../android/os/Handler.md)!:the [Handler](../android/os/Handler.md) that will be used for delivering the result. If handler is null, then the thread used for the listener is unspecified. |
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
| `deviceInfo` | [MidiDeviceInfo](../android/media/midi/MidiDeviceInfo.md)!:a [android.media.midi.MidiDeviceInfo](../android/media/midi/MidiDeviceInfo.md) to open |
| `listener` | [MidiManager.OnDeviceOpenedListener](../android/media/midi/MidiManager.OnDeviceOpenedListener.md)!:a [MidiManager.OnDeviceOpenedListener](../android/media/midi/MidiManager.OnDeviceOpenedListener.md) to be called to receive the result |
| `handler` | [Handler](../android/os/Handler.md)!:the [Handler](../android/os/Handler.md) that will be used for delivering the result. If handler is null, then the thread used for the listener is unspecified. |
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

**Deprecated:** *Use [registerDeviceCallback(int,java.util.concurrent.Executor,android.media.midi.MidiManager.DeviceCallback)](../android/media/midi/MidiManager.md))instead.*

Registers a callback to receive notifications when MIDI 1.0 devices are added and removed. These are devices that do not default to Universal MIDI Packets. To register for a callback for those, call #registerDeviceCallback instead. The [DeviceCallback.onDeviceStatusChanged](../android/media/midi/MidiManager.DeviceCallback.md))method will be called immediately for any devices that have open ports. This allows applications to know which input ports are already in use and, therefore, unavailable. Applications should call [getDevices](../android/media/midi/MidiManager.md))before registering the callback to get a list of devices already added.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [MidiManager.DeviceCallback](../android/media/midi/MidiManager.DeviceCallback.md)!:a [DeviceCallback](../android/media/midi/MidiManager.DeviceCallback.md) for MIDI device notifications |
| `handler` | [Handler](../android/os/Handler.md)!:The [Handler](../android/os/Handler.md) that will be used for delivering the device notifications. If handler is null, then the thread used for the callback is unspecified. |

### registerDeviceCallback

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun registerDeviceCallback(
    transport: Int, 
    executor: Executor, 
    callback: MidiManager.DeviceCallback
): Unit
```

Registers a callback to receive notifications when MIDI devices are added and removed for a specific transport type. The [DeviceCallback.onDeviceStatusChanged](../android/media/midi/MidiManager.DeviceCallback.md))method will be called immediately for any devices that have open ports. This allows applications to know which input ports are already in use and, therefore, unavailable. Applications should call [getDevicesForTransport](../android/media/midi/MidiManager.md))before registering the callback to get a list of devices already added.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `transport` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The transport to be used. This is either TRANSPORT_MIDI_BYTE_STREAM or TRANSPORT_UNIVERSAL_MIDI_PACKETS. Value is [android.media.midi.MidiManager#TRANSPORT_MIDI_BYTE_STREAM](../android/media/midi/MidiManager.md), or [android.media.midi.MidiManager#TRANSPORT_UNIVERSAL_MIDI_PACKETS](../android/media/midi/MidiManager.md) |
| `executor` | [Executor](../java/util/concurrent/Executor.md):The [Executor](../java/util/concurrent/Executor.md) that will be used for delivering the device notifications. This value cannot be`null`. |
| `callback` | [MidiManager.DeviceCallback](../android/media/midi/MidiManager.DeviceCallback.md):a [DeviceCallback](../android/media/midi/MidiManager.DeviceCallback.md) for MIDI device notifications This value cannot be`null`. |
| --- | --- |

### unregisterDeviceCallback

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun unregisterDeviceCallback(callback: MidiManager.DeviceCallback!): Unit
```

Unregisters a [DeviceCallback](../android/media/midi/MidiManager.DeviceCallback.md).

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [MidiManager.DeviceCallback](../android/media/midi/MidiManager.DeviceCallback.md)!:a [DeviceCallback](../android/media/midi/MidiManager.DeviceCallback.md) to unregister |
