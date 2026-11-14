# UsbConstants

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UsbConstants

Kotlin| [Java](https://developer.android.com/reference/android/hardware/usb/UsbConstants "View this page in Java") 

```
class UsbConstants
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.hardware.usb.UsbConstants](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbConstants#) |

Contains constants for the USB protocol. These constants correspond to definitions in linux/usb/ch9.h in the linux kernel.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [USB_CLASS_APP_SPEC](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbConstants#USB_CLASS_APP_SPEC:kotlin.Int) Application specific USB class. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [USB_CLASS_AUDIO](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbConstants#USB_CLASS_AUDIO:kotlin.Int) USB class for audio devices. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [USB_CLASS_CDC_DATA](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbConstants#USB_CLASS_CDC_DATA:kotlin.Int) USB class for CDC devices (communications device class). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [USB_CLASS_COMM](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbConstants#USB_CLASS_COMM:kotlin.Int) USB class for communication devices. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [USB_CLASS_CONTENT_SEC](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbConstants#USB_CLASS_CONTENT_SEC:kotlin.Int) USB class for content security devices. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [USB_CLASS_CSCID](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbConstants#USB_CLASS_CSCID:kotlin.Int) USB class for content smart card devices. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [USB_CLASS_HID](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbConstants#USB_CLASS_HID:kotlin.Int) USB class for human interface devices (for example, mice and keyboards). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [USB_CLASS_HUB](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbConstants#USB_CLASS_HUB:kotlin.Int) USB class for USB hubs. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [USB_CLASS_MASS_STORAGE](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbConstants#USB_CLASS_MASS_STORAGE:kotlin.Int) USB class for mass storage devices. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [USB_CLASS_MISC](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbConstants#USB_CLASS_MISC:kotlin.Int) USB class for wireless miscellaneous devices. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [USB_CLASS_PER_INTERFACE](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbConstants#USB_CLASS_PER_INTERFACE:kotlin.Int) USB class indicating that the class is determined on a per-interface basis. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [USB_CLASS_PHYSICA](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbConstants#USB_CLASS_PHYSICA:kotlin.Int) USB class for physical devices. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [USB_CLASS_PRINTER](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbConstants#USB_CLASS_PRINTER:kotlin.Int) USB class for printers. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [USB_CLASS_STILL_IMAGE](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbConstants#USB_CLASS_STILL_IMAGE:kotlin.Int) USB class for still image devices (digital cameras). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [USB_CLASS_VENDOR_SPEC](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbConstants#USB_CLASS_VENDOR_SPEC:kotlin.Int) Vendor specific USB class. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [USB_CLASS_VIDEO](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbConstants#USB_CLASS_VIDEO:kotlin.Int) USB class for video devices. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [USB_CLASS_WIRELESS_CONTROLLER](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbConstants#USB_CLASS_WIRELESS_CONTROLLER:kotlin.Int) USB class for wireless controller devices. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [USB_DIR_IN](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbConstants#USB_DIR_IN:kotlin.Int) Used to signify direction of data for a [UsbEndpoint](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbEndpoint) is IN (device to host) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [USB_DIR_OUT](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbConstants#USB_DIR_OUT:kotlin.Int) Used to signify direction of data for a [UsbEndpoint](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbEndpoint) is OUT (host to device) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [USB_ENDPOINT_DIR_MASK](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbConstants#USB_ENDPOINT_DIR_MASK:kotlin.Int) Bitmask used for extracting the [UsbEndpoint](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbEndpoint) direction from its address field. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [USB_ENDPOINT_NUMBER_MASK](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbConstants#USB_ENDPOINT_NUMBER_MASK:kotlin.Int) Bitmask used for extracting the [UsbEndpoint](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbEndpoint) number its address field. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [USB_ENDPOINT_XFERTYPE_MASK](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbConstants#USB_ENDPOINT_XFERTYPE_MASK:kotlin.Int) Bitmask used for extracting the [UsbEndpoint](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbEndpoint) type from its address field. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [USB_ENDPOINT_XFER_BULK](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbConstants#USB_ENDPOINT_XFER_BULK:kotlin.Int) Bulk endpoint type |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [USB_ENDPOINT_XFER_CONTROL](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbConstants#USB_ENDPOINT_XFER_CONTROL:kotlin.Int) Control endpoint type (endpoint zero) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [USB_ENDPOINT_XFER_INT](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbConstants#USB_ENDPOINT_XFER_INT:kotlin.Int) Interrupt endpoint type |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [USB_ENDPOINT_XFER_ISOC](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbConstants#USB_ENDPOINT_XFER_ISOC:kotlin.Int) Isochronous endpoint type (currently not supported) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [USB_INTERFACE_SUBCLASS_BOOT](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbConstants#USB_INTERFACE_SUBCLASS_BOOT:kotlin.Int) Boot subclass for HID devices. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [USB_SUBCLASS_VENDOR_SPEC](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbConstants#USB_SUBCLASS_VENDOR_SPEC:kotlin.Int) Vendor specific USB subclass. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [USB_TYPE_CLASS](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbConstants#USB_TYPE_CLASS:kotlin.Int) Used to specify that an endpoint zero control request is a class specific request. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [USB_TYPE_MASK](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbConstants#USB_TYPE_MASK:kotlin.Int) Bitmask used for encoding the request type for a control request on endpoint zero. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [USB_TYPE_RESERVED](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbConstants#USB_TYPE_RESERVED:kotlin.Int) Reserved endpoint zero control request type (currently unused). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [USB_TYPE_STANDARD](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbConstants#USB_TYPE_STANDARD:kotlin.Int) Used to specify that an endpoint zero control request is a standard request. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [USB_TYPE_VENDOR](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbConstants#USB_TYPE_VENDOR:kotlin.Int) Used to specify that an endpoint zero control request is a vendor specific request. |

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------|---|
| [UsbConstants](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbConstants#UsbConstants())`()` <br /> |

## Constants

### USB_CLASS_APP_SPEC

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USB_CLASS_APP_SPEC: Int
```

Application specific USB class. 

 Value: 254

### USB_CLASS_AUDIO

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USB_CLASS_AUDIO: Int
```

USB class for audio devices. 

 Value: 1

### USB_CLASS_CDC_DATA

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USB_CLASS_CDC_DATA: Int
```

USB class for CDC devices (communications device class). 

 Value: 10

### USB_CLASS_COMM

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USB_CLASS_COMM: Int
```

USB class for communication devices. 

 Value: 2

### USB_CLASS_CONTENT_SEC

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USB_CLASS_CONTENT_SEC: Int
```

USB class for content security devices. 

 Value: 13

### USB_CLASS_CSCID

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USB_CLASS_CSCID: Int
```

USB class for content smart card devices. 

 Value: 11

### USB_CLASS_HID

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USB_CLASS_HID: Int
```

USB class for human interface devices (for example, mice and keyboards). 

 Value: 3

### USB_CLASS_HUB

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USB_CLASS_HUB: Int
```

USB class for USB hubs. 

 Value: 9

### USB_CLASS_MASS_STORAGE

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USB_CLASS_MASS_STORAGE: Int
```

USB class for mass storage devices. 

 Value: 8

### USB_CLASS_MISC

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USB_CLASS_MISC: Int
```

USB class for wireless miscellaneous devices. 

 Value: 239

### USB_CLASS_PER_INTERFACE

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USB_CLASS_PER_INTERFACE: Int
```

USB class indicating that the class is determined on a per-interface basis. 

 Value: 0

### USB_CLASS_PHYSICA

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USB_CLASS_PHYSICA: Int
```

USB class for physical devices. 

 Value: 5

### USB_CLASS_PRINTER

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USB_CLASS_PRINTER: Int
```

USB class for printers. 

 Value: 7

### USB_CLASS_STILL_IMAGE

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USB_CLASS_STILL_IMAGE: Int
```

USB class for still image devices (digital cameras). 

 Value: 6

### USB_CLASS_VENDOR_SPEC

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USB_CLASS_VENDOR_SPEC: Int
```

Vendor specific USB class. 

 Value: 255

### USB_CLASS_VIDEO

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USB_CLASS_VIDEO: Int
```

USB class for video devices. 

 Value: 14

### USB_CLASS_WIRELESS_CONTROLLER

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USB_CLASS_WIRELESS_CONTROLLER: Int
```

USB class for wireless controller devices. 

 Value: 224

### USB_DIR_IN

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USB_DIR_IN: Int
```

Used to signify direction of data for a [UsbEndpoint](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbEndpoint) is IN (device to host) 

 Value: 128

**See Also**

- [android.hardware.usb.UsbEndpoint#getDirection](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbEndpoint#getDirection()) 

### USB_DIR_OUT

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USB_DIR_OUT: Int
```

Used to signify direction of data for a [UsbEndpoint](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbEndpoint) is OUT (host to device) 

 Value: 0

**See Also**

- [android.hardware.usb.UsbEndpoint#getDirection](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbEndpoint#getDirection()) 

### USB_ENDPOINT_DIR_MASK

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USB_ENDPOINT_DIR_MASK: Int
```

Bitmask used for extracting the [UsbEndpoint](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbEndpoint) direction from its address field. 

 Value: 128

**See Also**

- [android.hardware.usb.UsbEndpoint#getAddress](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbEndpoint#getAddress())
- [android.hardware.usb.UsbEndpoint#getDirection](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbEndpoint#getDirection())
- [#USB_DIR_OUT](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbConstants#USB_DIR_OUT:kotlin.Int)
- [#USB_DIR_IN](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbConstants#USB_DIR_IN:kotlin.Int) 

### USB_ENDPOINT_NUMBER_MASK

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USB_ENDPOINT_NUMBER_MASK: Int
```

Bitmask used for extracting the [UsbEndpoint](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbEndpoint) number its address field. 

 Value: 15

**See Also**

- [android.hardware.usb.UsbEndpoint#getAddress](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbEndpoint#getAddress())
- [android.hardware.usb.UsbEndpoint#getEndpointNumber](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbEndpoint#getEndpointNumber()) 

### USB_ENDPOINT_XFERTYPE_MASK

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USB_ENDPOINT_XFERTYPE_MASK: Int
```

Bitmask used for extracting the [UsbEndpoint](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbEndpoint) type from its address field. 

 Value: 3

**See Also**

- [android.hardware.usb.UsbEndpoint#getAddress](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbEndpoint#getAddress())
- [android.hardware.usb.UsbEndpoint#getType](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbEndpoint#getType())
- [#USB_ENDPOINT_XFER_CONTROL](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbConstants#USB_ENDPOINT_XFER_CONTROL:kotlin.Int)
- [#USB_ENDPOINT_XFER_ISOC](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbConstants#USB_ENDPOINT_XFER_ISOC:kotlin.Int)
- [#USB_ENDPOINT_XFER_BULK](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbConstants#USB_ENDPOINT_XFER_BULK:kotlin.Int)
- [#USB_ENDPOINT_XFER_INT](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbConstants#USB_ENDPOINT_XFER_INT:kotlin.Int) 

### USB_ENDPOINT_XFER_BULK

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USB_ENDPOINT_XFER_BULK: Int
```

Bulk endpoint type 

 Value: 2

**See Also**

- [android.hardware.usb.UsbEndpoint#getType](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbEndpoint#getType()) 

### USB_ENDPOINT_XFER_CONTROL

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USB_ENDPOINT_XFER_CONTROL: Int
```

Control endpoint type (endpoint zero) 

 Value: 0

**See Also**

- [android.hardware.usb.UsbEndpoint#getType](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbEndpoint#getType()) 

### USB_ENDPOINT_XFER_INT

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USB_ENDPOINT_XFER_INT: Int
```

Interrupt endpoint type 

 Value: 3

**See Also**

- [android.hardware.usb.UsbEndpoint#getType](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbEndpoint#getType()) 

### USB_ENDPOINT_XFER_ISOC

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USB_ENDPOINT_XFER_ISOC: Int
```

Isochronous endpoint type (currently not supported) 

 Value: 1

**See Also**

- [android.hardware.usb.UsbEndpoint#getType](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbEndpoint#getType()) 

### USB_INTERFACE_SUBCLASS_BOOT

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USB_INTERFACE_SUBCLASS_BOOT: Int
```

Boot subclass for HID devices. 

 Value: 1

### USB_SUBCLASS_VENDOR_SPEC

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USB_SUBCLASS_VENDOR_SPEC: Int
```

Vendor specific USB subclass. 

 Value: 255

### USB_TYPE_CLASS

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USB_TYPE_CLASS: Int
```

Used to specify that an endpoint zero control request is a class specific request. 

 Value: 32

### USB_TYPE_MASK

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USB_TYPE_MASK: Int
```

Bitmask used for encoding the request type for a control request on endpoint zero. 

 Value: 96

### USB_TYPE_RESERVED

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USB_TYPE_RESERVED: Int
```

Reserved endpoint zero control request type (currently unused). 

 Value: 96

### USB_TYPE_STANDARD

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USB_TYPE_STANDARD: Int
```

Used to specify that an endpoint zero control request is a standard request. 

 Value: 0

### USB_TYPE_VENDOR

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val USB_TYPE_VENDOR: Int
```

Used to specify that an endpoint zero control request is a vendor specific request. 

 Value: 64

## Public constructors

### UsbConstants

```
UsbConstants()
```
