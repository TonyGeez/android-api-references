# MidiDeviceInfo

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MidiDeviceInfo

Kotlin| [Java](https://developer.android.com/reference/android/media/midi/MidiDeviceInfo "View this page in Java") 

```
class MidiDeviceInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.media.midi.MidiDeviceInfo](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo#) |

This class contains information to describe a MIDI device. For now we only have information that can be retrieved easily for USB devices, but we will probably expand this in the future. This class is just an immutable object to encapsulate the MIDI device description. Use the MidiDevice class to actually communicate with devices.

## Summary

| Nested classes ||
|---|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [PortInfo](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo.PortInfo) Contains information about an input or output port. |

| Constants ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PROPERTY_BLUETOOTH_DEVICE](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo#PROPERTY_BLUETOOTH_DEVICE:kotlin.String) Bundle key for the device's corresponding Bluetooth device. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PROPERTY_MANUFACTURER](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo#PROPERTY_MANUFACTURER:kotlin.String) Bundle key for the device's manufacturer name property. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PROPERTY_NAME](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo#PROPERTY_NAME:kotlin.String) Bundle key for the device's user visible name property. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PROPERTY_PRODUCT](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo#PROPERTY_PRODUCT:kotlin.String) Bundle key for the device's product name property. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PROPERTY_SERIAL_NUMBER](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo#PROPERTY_SERIAL_NUMBER:kotlin.String) Bundle key for the device's serial number property. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PROPERTY_USB_DEVICE](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo#PROPERTY_USB_DEVICE:kotlin.String) Bundle key for the device's corresponding USB device. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [PROPERTY_VERSION](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo#PROPERTY_VERSION:kotlin.String) Bundle key for the device's version property. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PROTOCOL_UMP_MIDI_1_0_UP_TO_128_BITS](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo#PROTOCOL_UMP_MIDI_1_0_UP_TO_128_BITS:kotlin.Int) Constant representing a default protocol with Universal MIDI Packets (UMP). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PROTOCOL_UMP_MIDI_1_0_UP_TO_128_BITS_AND_JRTS](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo#PROTOCOL_UMP_MIDI_1_0_UP_TO_128_BITS_AND_JRTS:kotlin.Int) Constant representing a default protocol with Universal MIDI Packets (UMP). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PROTOCOL_UMP_MIDI_1_0_UP_TO_64_BITS](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo#PROTOCOL_UMP_MIDI_1_0_UP_TO_64_BITS:kotlin.Int) Constant representing a default protocol with Universal MIDI Packets (UMP). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PROTOCOL_UMP_MIDI_1_0_UP_TO_64_BITS_AND_JRTS](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo#PROTOCOL_UMP_MIDI_1_0_UP_TO_64_BITS_AND_JRTS:kotlin.Int) Constant representing a default protocol with Universal MIDI Packets (UMP). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PROTOCOL_UMP_MIDI_2_0](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo#PROTOCOL_UMP_MIDI_2_0:kotlin.Int) Constant representing a default protocol with Universal MIDI Packets (UMP). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PROTOCOL_UMP_MIDI_2_0_AND_JRTS](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo#PROTOCOL_UMP_MIDI_2_0_AND_JRTS:kotlin.Int) Constant representing a default protocol with Universal MIDI Packets (UMP). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PROTOCOL_UMP_USE_MIDI_CI](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo#PROTOCOL_UMP_USE_MIDI_CI:kotlin.Int) Constant representing a default protocol with Universal MIDI Packets (UMP). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PROTOCOL_UNKNOWN](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo#PROTOCOL_UNKNOWN:kotlin.Int) Constant representing a device with an unknown default protocol. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_BLUETOOTH](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo#TYPE_BLUETOOTH:kotlin.Int) Constant representing Bluetooth MIDI devices for [getType](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo#getType()) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_USB](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo#TYPE_USB:kotlin.Int) Constant representing USB MIDI devices for [getType](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo#getType()) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_VIRTUAL](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo#TYPE_VIRTUAL:kotlin.Int) Constant representing virtual (software based) MIDI devices for [getType](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo#getType()) |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDefaultProtocol](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo#getDefaultProtocol())`()` Returns the default protocol. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getId](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo#getId())`()` Returns the ID of the device. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getInputPortCount](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo#getInputPortCount())`()` Returns the device's number of input ports. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOutputPortCount](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo#getOutputPortCount())`()` Returns the device's number of output ports. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [MidiDeviceInfo.PortInfo](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo.PortInfo)!\>! | [getPorts](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo#getPorts())`()` Returns information about the device's ports. |
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)! | [getProperties](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo#getProperties())`()` Returns the [android.os.Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) containing the device's properties. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo#getType())`()` Returns the type of the device. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo#hashCode())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPrivate](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo#isPrivate())`()` Returns true if the device is private. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`parcel:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [MidiDeviceInfo](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### PROPERTY_BLUETOOTH_DEVICE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PROPERTY_BLUETOOTH_DEVICE: String
```

Bundle key for the device's corresponding Bluetooth device. The value for this property is of type [android.bluetooth.BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice.html#). Only set for Bluetooth MIDI devices. Used with the [android.os.Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) returned by [getProperties](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo#getProperties()) 

 Value: "bluetooth_device"

### PROPERTY_MANUFACTURER

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PROPERTY_MANUFACTURER: String
```

Bundle key for the device's manufacturer name property. The value for this property is of type [java.lang.String](https://developer.android.com/reference/kotlin/java/lang/String.html#). Used with the [android.os.Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) returned by [getProperties](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo#getProperties()). Matches the USB device manufacturer name string for USB MIDI devices. 

 Value: "manufacturer"

### PROPERTY_NAME

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PROPERTY_NAME: String
```

Bundle key for the device's user visible name property. The value for this property is of type [java.lang.String](https://developer.android.com/reference/kotlin/java/lang/String.html#). Used with the [android.os.Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) returned by [getProperties](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo#getProperties()). For USB devices, this is a concatenation of the manufacturer and product names. 

 Value: "name"

### PROPERTY_PRODUCT

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PROPERTY_PRODUCT: String
```

Bundle key for the device's product name property. The value for this property is of type [java.lang.String](https://developer.android.com/reference/kotlin/java/lang/String.html#). Used with the [android.os.Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) returned by [getProperties](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo#getProperties())Matches the USB device product name string for USB MIDI devices. 

 Value: "product"

### PROPERTY_SERIAL_NUMBER

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PROPERTY_SERIAL_NUMBER: String
```

Bundle key for the device's serial number property. The value for this property is of type [java.lang.String](https://developer.android.com/reference/kotlin/java/lang/String.html#). Used with the [android.os.Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) returned by [getProperties](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo#getProperties())Matches the USB device serial number for USB MIDI devices. 

 Value: "serial_number"

### PROPERTY_USB_DEVICE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PROPERTY_USB_DEVICE: String
```

Bundle key for the device's corresponding USB device. The value for this property is of type [android.hardware.usb.UsbDevice](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbDevice.html#). Only set for USB MIDI devices. Used with the [android.os.Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) returned by [getProperties](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo#getProperties()) 

 Value: "usb_device"

### PROPERTY_VERSION

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PROPERTY_VERSION: String
```

Bundle key for the device's version property. The value for this property is of type [java.lang.String](https://developer.android.com/reference/kotlin/java/lang/String.html#). Used with the [android.os.Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) returned by [getProperties](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo#getProperties())Matches the USB device version number for USB MIDI devices. 

 Value: "version"

### PROTOCOL_UMP_MIDI_1_0_UP_TO_128_BITS

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PROTOCOL_UMP_MIDI_1_0_UP_TO_128_BITS: Int
```

Constant representing a default protocol with Universal MIDI Packets (UMP). UMP is defined in "Universal MIDI Packet (UMP) Format and MIDI 2.0 Protocol" spec. All UMP data should be a multiple of 4 bytes. Use MIDI 1.0 through UMP with packet sizes up to 128 bits. Call [MidiManager.getDevicesForTransport](https://developer.android.com/reference/kotlin/android/media/midi/MidiManager#getDevicesForTransport(kotlin.Int))with parameter [MidiManager.TRANSPORT_UNIVERSAL_MIDI_PACKETS](https://developer.android.com/reference/kotlin/android/media/midi/MidiManager#TRANSPORT_UNIVERSAL_MIDI_PACKETS:kotlin.Int) to get devices with this transport. 

 Value: 3

**See Also**

- [android.media.midi.MidiDeviceInfo#getDefaultProtocol](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo#getDefaultProtocol()) 

### PROTOCOL_UMP_MIDI_1_0_UP_TO_128_BITS_AND_JRTS

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PROTOCOL_UMP_MIDI_1_0_UP_TO_128_BITS_AND_JRTS: Int
```

Constant representing a default protocol with Universal MIDI Packets (UMP). UMP is defined in "Universal MIDI Packet (UMP) Format and MIDI 2.0 Protocol" spec. All UMP data should be a multiple of 4 bytes. Use MIDI 1.0 through UMP with packet sizes up to 128 bits and jitter reduction timestamps. Call [MidiManager.getDevicesForTransport](https://developer.android.com/reference/kotlin/android/media/midi/MidiManager#getDevicesForTransport(kotlin.Int))with parameter [MidiManager.TRANSPORT_UNIVERSAL_MIDI_PACKETS](https://developer.android.com/reference/kotlin/android/media/midi/MidiManager#TRANSPORT_UNIVERSAL_MIDI_PACKETS:kotlin.Int) to get devices with this transport. 

 Value: 4

**See Also**

- [android.media.midi.MidiDeviceInfo#getDefaultProtocol](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo#getDefaultProtocol()) 

### PROTOCOL_UMP_MIDI_1_0_UP_TO_64_BITS

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PROTOCOL_UMP_MIDI_1_0_UP_TO_64_BITS: Int
```

Constant representing a default protocol with Universal MIDI Packets (UMP). UMP is defined in "Universal MIDI Packet (UMP) Format and MIDI 2.0 Protocol" spec. All UMP data should be a multiple of 4 bytes. Use MIDI 1.0 through UMP with packet sizes up to 64 bits. Call [MidiManager.getDevicesForTransport](https://developer.android.com/reference/kotlin/android/media/midi/MidiManager#getDevicesForTransport(kotlin.Int))with parameter [MidiManager.TRANSPORT_UNIVERSAL_MIDI_PACKETS](https://developer.android.com/reference/kotlin/android/media/midi/MidiManager#TRANSPORT_UNIVERSAL_MIDI_PACKETS:kotlin.Int) to get devices with this transport. 

 Value: 1

**See Also**

- [android.media.midi.MidiDeviceInfo#getDefaultProtocol](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo#getDefaultProtocol()) 

### PROTOCOL_UMP_MIDI_1_0_UP_TO_64_BITS_AND_JRTS

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PROTOCOL_UMP_MIDI_1_0_UP_TO_64_BITS_AND_JRTS: Int
```

Constant representing a default protocol with Universal MIDI Packets (UMP). UMP is defined in "Universal MIDI Packet (UMP) Format and MIDI 2.0 Protocol" spec. All UMP data should be a multiple of 4 bytes. Use MIDI 1.0 through UMP with packet sizes up to 64 bits and jitter reduction timestamps. Call [MidiManager.getDevicesForTransport](https://developer.android.com/reference/kotlin/android/media/midi/MidiManager#getDevicesForTransport(kotlin.Int))with parameter [MidiManager.TRANSPORT_UNIVERSAL_MIDI_PACKETS](https://developer.android.com/reference/kotlin/android/media/midi/MidiManager#TRANSPORT_UNIVERSAL_MIDI_PACKETS:kotlin.Int) to get devices with this transport. 

 Value: 2

**See Also**

- [android.media.midi.MidiDeviceInfo#getDefaultProtocol](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo#getDefaultProtocol()) 

### PROTOCOL_UMP_MIDI_2_0

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PROTOCOL_UMP_MIDI_2_0: Int
```

Constant representing a default protocol with Universal MIDI Packets (UMP). UMP is defined in "Universal MIDI Packet (UMP) Format and MIDI 2.0 Protocol" spec. All UMP data should be a multiple of 4 bytes. Use MIDI 2.0 through UMP. Call [MidiManager.getDevicesForTransport](https://developer.android.com/reference/kotlin/android/media/midi/MidiManager#getDevicesForTransport(kotlin.Int))with parameter [MidiManager.TRANSPORT_UNIVERSAL_MIDI_PACKETS](https://developer.android.com/reference/kotlin/android/media/midi/MidiManager#TRANSPORT_UNIVERSAL_MIDI_PACKETS:kotlin.Int) to get devices with this transport. 

 Value: 17

**See Also**

- [android.media.midi.MidiDeviceInfo#getDefaultProtocol](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo#getDefaultProtocol()) 

### PROTOCOL_UMP_MIDI_2_0_AND_JRTS

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PROTOCOL_UMP_MIDI_2_0_AND_JRTS: Int
```

Constant representing a default protocol with Universal MIDI Packets (UMP). UMP is defined in "Universal MIDI Packet (UMP) Format and MIDI 2.0 Protocol" spec. All UMP data should be a multiple of 4 bytes. Use MIDI 2.0 through UMP and jitter reduction timestamps. Call [MidiManager.getDevicesForTransport](https://developer.android.com/reference/kotlin/android/media/midi/MidiManager#getDevicesForTransport(kotlin.Int))with parameter [MidiManager.TRANSPORT_UNIVERSAL_MIDI_PACKETS](https://developer.android.com/reference/kotlin/android/media/midi/MidiManager#TRANSPORT_UNIVERSAL_MIDI_PACKETS:kotlin.Int) to get devices with this transport. 

 Value: 18

**See Also**

- [android.media.midi.MidiDeviceInfo#getDefaultProtocol](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo#getDefaultProtocol()) 

### PROTOCOL_UMP_USE_MIDI_CI

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PROTOCOL_UMP_USE_MIDI_CI: Int
```

Constant representing a default protocol with Universal MIDI Packets (UMP). UMP is defined in "Universal MIDI Packet (UMP) Format and MIDI 2.0 Protocol" spec. All UMP data should be a multiple of 4 bytes. Use UMP to negotiate with the device with MIDI-CI. MIDI-CI is defined in "MIDI Capability Inquiry (MIDI-CI)" spec. Call [MidiManager.getDevicesForTransport](https://developer.android.com/reference/kotlin/android/media/midi/MidiManager#getDevicesForTransport(kotlin.Int))with parameter [MidiManager.TRANSPORT_UNIVERSAL_MIDI_PACKETS](https://developer.android.com/reference/kotlin/android/media/midi/MidiManager#TRANSPORT_UNIVERSAL_MIDI_PACKETS:kotlin.Int) to get devices with this transport. 

 Value: 0

**See Also**

- [android.media.midi.MidiDeviceInfo#getDefaultProtocol](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo#getDefaultProtocol()) 

### PROTOCOL_UNKNOWN

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PROTOCOL_UNKNOWN: Int
```

Constant representing a device with an unknown default protocol. If Universal MIDI Packets (UMP) are needed, use MIDI-CI through MIDI 1.0. UMP is defined in "Universal MIDI Packet (UMP) Format and MIDI 2.0 Protocol" spec. MIDI-CI is defined in "MIDI Capability Inquiry (MIDI-CI)" spec. 

 Value: -1

**See Also**

- [android.media.midi.MidiDeviceInfo#getDefaultProtocol](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo#getDefaultProtocol()) 

### TYPE_BLUETOOTH

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_BLUETOOTH: Int
```

Constant representing Bluetooth MIDI devices for [getType](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo#getType()) 

 Value: 3

### TYPE_USB

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_USB: Int
```

Constant representing USB MIDI devices for [getType](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo#getType()) 

 Value: 1

### TYPE_VIRTUAL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_VIRTUAL: Int
```

Constant representing virtual (software based) MIDI devices for [getType](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo#getType()) 

 Value: 2

## Public methods

### describeContents

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### equals

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getDefaultProtocol

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDefaultProtocol(): Int
```

Returns the default protocol. For most devices, this will be [PROTOCOL_UNKNOWN](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo#PROTOCOL_UNKNOWN:kotlin.Int). Returning [PROTOCOL_UNKNOWN](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo#PROTOCOL_UNKNOWN:kotlin.Int) is not an error; the device just doesn't support Universal MIDI Packets by default.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the device's default protocol. Value is [android.media.midi.MidiDeviceInfo#PROTOCOL_UMP_USE_MIDI_CI](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo#PROTOCOL_UMP_USE_MIDI_CI:kotlin.Int), [android.media.midi.MidiDeviceInfo#PROTOCOL_UMP_MIDI_1_0_UP_TO_64_BITS](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo#PROTOCOL_UMP_MIDI_1_0_UP_TO_64_BITS:kotlin.Int), [android.media.midi.MidiDeviceInfo#PROTOCOL_UMP_MIDI_1_0_UP_TO_64_BITS_AND_JRTS](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo#PROTOCOL_UMP_MIDI_1_0_UP_TO_64_BITS_AND_JRTS:kotlin.Int), [android.media.midi.MidiDeviceInfo#PROTOCOL_UMP_MIDI_1_0_UP_TO_128_BITS](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo#PROTOCOL_UMP_MIDI_1_0_UP_TO_128_BITS:kotlin.Int), [android.media.midi.MidiDeviceInfo#PROTOCOL_UMP_MIDI_1_0_UP_TO_128_BITS_AND_JRTS](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo#PROTOCOL_UMP_MIDI_1_0_UP_TO_128_BITS_AND_JRTS:kotlin.Int), [android.media.midi.MidiDeviceInfo#PROTOCOL_UMP_MIDI_2_0](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo#PROTOCOL_UMP_MIDI_2_0:kotlin.Int), [android.media.midi.MidiDeviceInfo#PROTOCOL_UMP_MIDI_2_0_AND_JRTS](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo#PROTOCOL_UMP_MIDI_2_0_AND_JRTS:kotlin.Int), or [android.media.midi.MidiDeviceInfo#PROTOCOL_UNKNOWN](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo#PROTOCOL_UNKNOWN:kotlin.Int) |

### getId

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getId(): Int
```

Returns the ID of the device. This ID is generated by the MIDI service and is not persistent across device unplugs.

| Return ||
|----------------------------------------------------------------------------|-----------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the device's ID |

### getInputPortCount

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getInputPortCount(): Int
```

Returns the device's number of input ports.

| Return ||
|----------------------------------------------------------------------------|---------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of input ports |

### getOutputPortCount

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getOutputPortCount(): Int
```

Returns the device's number of output ports.

| Return ||
|----------------------------------------------------------------------------|----------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of output ports |

### getPorts

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPorts(): Array<MidiDeviceInfo.PortInfo!>!
```

Returns information about the device's ports. The ports are in unspecified order.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [MidiDeviceInfo.PortInfo](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo.PortInfo)!>! | array of [PortInfo](https://developer.android.com/reference/kotlin/android/media/midi/MidiDeviceInfo.PortInfo) |

### getProperties

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getProperties(): Bundle!
```

Returns the [android.os.Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) containing the device's properties.

| Return ||
|-----------------------------------------------------------------------------------|-------------------------|
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)! | the device's properties |

### getType

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getType(): Int
```

Returns the type of the device.

| Return ||
|----------------------------------------------------------------------------|-------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the device's type |

### hashCode

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### isPrivate

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isPrivate(): Boolean
```

Returns true if the device is private. Private devices are only visible and accessible to clients with the same UID as the application that is hosting the device.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the device is private |

### toString

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    parcel: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<MidiDeviceInfo!>
```
