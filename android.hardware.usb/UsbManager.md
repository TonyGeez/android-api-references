# UsbManager

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UsbManager

Kotlin| [Java](UsbManager.md) 
| --- | --- |

```
open class UsbManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.hardware.usb.UsbManager](UsbManager.md) |

This class allows you to access the state of USB and communicate with USB devices. Currently only host mode is supported in the public API.
|
| ### Developer Guides
|
| For more information about communicating with USB hardware, read the [USB developer guide](https://developer.android.com/guide/topics/connectivity/usb/index.html).

Restricted for SDK Runtime environment in API level 34.

<br />

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_USB_ACCESSORY_ATTACHED](UsbManager.md) Activity intent sent when user attaches a USB accessory. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_USB_ACCESSORY_DETACHED](UsbManager.md) Broadcast Action: A broadcast for USB accessory detached event. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_USB_DEVICE_ATTACHED](UsbManager.md) Activity intent sent when user attaches a USB device. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_USB_DEVICE_DETACHED](UsbManager.md) Broadcast Action: A broadcast for USB device detached event. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_ACCESSORY](UsbManager.md) Name of extra for [ACTION_USB_ACCESSORY_ATTACHED](UsbManager.md) and [ACTION_USB_ACCESSORY_DETACHED](UsbManager.md) broadcasts containing the [UsbAccessory](UsbAccessory.md) object for the accessory. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_DEVICE](UsbManager.md) Name of extra for [ACTION_USB_DEVICE_ATTACHED](UsbManager.md) and [ACTION_USB_DEVICE_DETACHED](UsbManager.md) broadcasts containing the [UsbDevice](UsbDevice.md) object for the device. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_PERMISSION_GRANTED](UsbManager.md) Name of extra added to the [android.app.PendingIntent](../android.app/PendingIntent.md) passed into [requestPermission(android.hardware.usb.UsbDevice,android.app.PendingIntent)](UsbManager.md))or [requestPermission(android.hardware.usb.UsbAccessory,android.app.PendingIntent)](UsbManager.md))containing a boolean value indicating whether the user granted permission or not. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [UsbAccessory](UsbAccessory.md)!\>! | [getAccessoryList](UsbManager.md))`()` Returns a list of currently attached USB accessories. |
| open [HashMap](../java.util/HashMap.md)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [UsbDevice](UsbDevice.md)!\>! | [getDeviceList](UsbManager.md))`()` Returns a HashMap containing all USB devices currently attached. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasPermission](UsbManager.md))`(`accessory:` ` [UsbAccessory](UsbAccessory.md)!`)` Returns true if the caller has permission to access the accessory. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasPermission](UsbManager.md))`(`device:` ` [UsbDevice](UsbDevice.md)!`)` Returns true if the caller has permission to access the device. |
| open [ParcelFileDescriptor](../android.os/ParcelFileDescriptor.md)! | [openAccessory](UsbManager.md))`(`accessory:` ` [UsbAccessory](UsbAccessory.md)!`)` Opens a file descriptor for reading and writing data to the USB accessory. |
| open [InputStream](../java.io/InputStream.md) | [openAccessoryInputStream](UsbManager.md))`(`accessory:` ` [UsbAccessory](UsbAccessory.md)`)` Opens an input stream for reading from the USB accessory. |
| --- | --- |
| open [OutputStream](../java.io/OutputStream.md) | [openAccessoryOutputStream](UsbManager.md))`(`accessory:` ` [UsbAccessory](UsbAccessory.md)`)` Opens an output stream for writing to the USB accessory. |
| open [UsbDeviceConnection](UsbDeviceConnection.md)! | [openDevice](UsbManager.md))`(`device:` ` [UsbDevice](UsbDevice.md)!`)` Opens the device so it can be used to send and receive data using [android.hardware.usb.UsbRequest](UsbRequest.md). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestPermission](UsbManager.md))`(`accessory:` ` [UsbAccessory](UsbAccessory.md)!`, `pi:` ` [PendingIntent](../android.app/PendingIntent.md)!`)` Requests temporary permission for the given package to access the accessory. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestPermission](UsbManager.md))`(`device:` ` [UsbDevice](UsbDevice.md)!`, `pi:` ` [PendingIntent](../android.app/PendingIntent.md)!`)` Requests temporary permission for the given package to access the device. |

## Constants

### ACTION_USB_ACCESSORY_ATTACHED

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_USB_ACCESSORY_ATTACHED: String
```

Activity intent sent when user attaches a USB accessory.

- [EXTRA_ACCESSORY](UsbManager.md) containing the [android.hardware.usb.UsbAccessory](UsbAccessory.md) for the attached accessory

<br />

 Value: "android.hardware.usb.action.USB_ACCESSORY_ATTACHED"

### ACTION_USB_ACCESSORY_DETACHED

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_USB_ACCESSORY_DETACHED: String
```

Broadcast Action: A broadcast for USB accessory detached event. This intent is sent when a USB accessory is detached.

- [EXTRA_ACCESSORY](UsbManager.md) containing the [UsbAccessory](UsbAccessory.md) for the attached accessory that was detached

<br />

 Value: "android.hardware.usb.action.USB_ACCESSORY_DETACHED"

### ACTION_USB_DEVICE_ATTACHED

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_USB_DEVICE_ATTACHED: String
```

Activity intent sent when user attaches a USB device. This intent is sent when a USB device is attached to the USB bus when in host mode.

- [EXTRA_DEVICE](UsbManager.md) containing the [android.hardware.usb.UsbDevice](UsbDevice.md) for the attached device

<br />

 Value: "android.hardware.usb.action.USB_DEVICE_ATTACHED"

### ACTION_USB_DEVICE_DETACHED

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_USB_DEVICE_DETACHED: String
```

Broadcast Action: A broadcast for USB device detached event. This intent is sent when a USB device is detached from the USB bus when in host mode.

- [EXTRA_DEVICE](UsbManager.md) containing the [android.hardware.usb.UsbDevice](UsbDevice.md) for the detached device

<br />

 Value: "android.hardware.usb.action.USB_DEVICE_DETACHED"

### EXTRA_ACCESSORY

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_ACCESSORY: String
```

Name of extra for [ACTION_USB_ACCESSORY_ATTACHED](UsbManager.md) and [ACTION_USB_ACCESSORY_DETACHED](UsbManager.md) broadcasts containing the [UsbAccessory](UsbAccessory.md) object for the accessory. 

 Value: "accessory"

### EXTRA_DEVICE

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_DEVICE: String
```

Name of extra for [ACTION_USB_DEVICE_ATTACHED](UsbManager.md) and [ACTION_USB_DEVICE_DETACHED](UsbManager.md) broadcasts containing the [UsbDevice](UsbDevice.md) object for the device. 

 Value: "device"

### EXTRA_PERMISSION_GRANTED

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_PERMISSION_GRANTED: String
```

Name of extra added to the [android.app.PendingIntent](../android.app/PendingIntent.md) passed into [requestPermission(android.hardware.usb.UsbDevice,android.app.PendingIntent)](UsbManager.md))or [requestPermission(android.hardware.usb.UsbAccessory,android.app.PendingIntent)](UsbManager.md))containing a boolean value indicating whether the user granted permission or not. 

 Value: "permission"

## Public methods

### getAccessoryList

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAccessoryList(): Array<UsbAccessory!>!
```

Returns a list of currently attached USB accessories. (in the current implementation there can be at most one) 
Requires the [PackageManager#FEATURE_USB_ACCESSORY](../android.content.pm/PackageManager.md) feature which can be detected using [PackageManager.hasSystemFeature(String)](../android.content.pm/PackageManager.md)).

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [UsbAccessory](UsbAccessory.md)!>! | list of USB accessories, or null if none are attached. |

### getDeviceList

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDeviceList(): HashMap<String!, UsbDevice!>!
```

Returns a HashMap containing all USB devices currently attached. USB device name is the key for the returned HashMap. The result will be empty if no devices are attached, or if USB host mode is inactive or unsupported. 
Requires the [PackageManager#FEATURE_USB_HOST](../android.content.pm/PackageManager.md) feature which can be detected using [PackageManager.hasSystemFeature(String)](../android.content.pm/PackageManager.md)).

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [HashMap](../java.util/HashMap.md)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [UsbDevice](UsbDevice.md)!>! | HashMap containing all connected USB devices. |

### hasPermission

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasPermission(accessory: UsbAccessory!): Boolean
```

Returns true if the caller has permission to access the accessory. Permission might have been granted temporarily via [requestPermission(android.hardware.usb.UsbAccessory,android.app.PendingIntent)](UsbManager.md))or by the user choosing the caller as the default application for the accessory. 
Requires the [PackageManager#FEATURE_USB_ACCESSORY](../android.content.pm/PackageManager.md) feature which can be detected using [PackageManager.hasSystemFeature(String)](../android.content.pm/PackageManager.md)).

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------|
| `accessory` | [UsbAccessory](UsbAccessory.md)!:to check permissions for |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if caller has permission |

### hasPermission

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasPermission(device: UsbDevice!): Boolean
```

Returns true if the caller has permission to access the device. Permission might have been granted temporarily via [requestPermission(android.hardware.usb.UsbDevice,android.app.PendingIntent)](UsbManager.md))or by the user choosing the caller as the default application for the device. Permission for USB devices of class [UsbConstants.USB_CLASS_VIDEO](UsbConstants.md) for clients that target SDK [android.os.Build.VERSION_CODES#P](../android/os/Build.VERSION_CODES.md) and above can be granted only if they have additionally the [android.Manifest.permission#CAMERA](../android/Manifest.permission.md) permission. 
Requires the [PackageManager#FEATURE_USB_HOST](../android.content.pm/PackageManager.md) feature which can be detected using [PackageManager.hasSystemFeature(String)](../android.content.pm/PackageManager.md)).

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------|
| `device` | [UsbDevice](UsbDevice.md)!:to check permissions for |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if caller has permission |

### openAccessory

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun openAccessory(accessory: UsbAccessory!): ParcelFileDescriptor!
```

Opens a file descriptor for reading and writing data to the USB accessory.

If data is read from the [java.io.InputStream](../java.io/InputStream.md) created from this file descriptor all data of a USB transfer should be read at once. If only a partial request is read the rest of the transfer is dropped.

It is strongly recommended to use newer methods instead of this method, since this method may provide sub-optimal performance on some devices. This method could potentially face interim performance degradation as well. 
Requires the [PackageManager#FEATURE_USB_ACCESSORY](../android.content.pm/PackageManager.md) feature which can be detected using [PackageManager.hasSystemFeature(String)](../android.content.pm/PackageManager.md)).

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------|
| `accessory` | [UsbAccessory](UsbAccessory.md)!:the USB accessory to open |

| Return ||
|---------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [ParcelFileDescriptor](../android.os/ParcelFileDescriptor.md)! | file descriptor, or null if the accessory could not be opened. |

### openAccessoryInputStream

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun openAccessoryInputStream(accessory: UsbAccessory): InputStream
```

Opens an input stream for reading from the USB accessory. If accessory is not open at this point, accessory will first be opened.

If data is read from the created [java.io.InputStream](../java.io/InputStream.md) all data of a USB transfer should be read at once. If only a partial request is read, the rest of the transfer is dropped.

The caller is responsible for ensuring that the returned stream is closed. 
Requires the [PackageManager#FEATURE_USB_ACCESSORY](../android.content.pm/PackageManager.md) feature which can be detected using [PackageManager.hasSystemFeature(String)](../android.content.pm/PackageManager.md)).

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `accessory` | [UsbAccessory](UsbAccessory.md):the USB accessory to open an input stream for This value cannot be`null`. |

| Return ||
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [InputStream](../java.io/InputStream.md) | input stream to read from given USB accessory This value cannot be`null`. |

### openAccessoryOutputStream

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun openAccessoryOutputStream(accessory: UsbAccessory): OutputStream
```

Opens an output stream for writing to the USB accessory. If accessory is not open at this point, accessory will first be opened.

The caller is responsible for ensuring that the returned stream is closed. 
Requires the [PackageManager#FEATURE_USB_ACCESSORY](../android.content.pm/PackageManager.md) feature which can be detected using [PackageManager.hasSystemFeature(String)](../android.content.pm/PackageManager.md)).

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `accessory` | [UsbAccessory](UsbAccessory.md):the USB accessory to open an output stream for This value cannot be`null`. |

| Return ||
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [OutputStream](../java.io/OutputStream.md) | output stream to write to given USB accessory This value cannot be`null`. |

### openDevice

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun openDevice(device: UsbDevice!): UsbDeviceConnection!
```

Opens the device so it can be used to send and receive data using [android.hardware.usb.UsbRequest](UsbRequest.md). 
Requires the [PackageManager#FEATURE_USB_HOST](../android.content.pm/PackageManager.md) feature which can be detected using [PackageManager.hasSystemFeature(String)](../android.content.pm/PackageManager.md)).

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------|
| `device` | [UsbDevice](UsbDevice.md)!:the device to open |

| Return ||
|-----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [UsbDeviceConnection](UsbDeviceConnection.md)! | a [UsbDeviceConnection](UsbDeviceConnection.md), or`null`if open failed |

### requestPermission

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun requestPermission(
    accessory: UsbAccessory!, 
    pi: PendingIntent!
): Unit
```

Requests temporary permission for the given package to access the accessory. This may result in a system dialog being displayed to the user if permission had not already been granted. Success or failure is returned via the [android.app.PendingIntent](../android.app/PendingIntent.md) pi. If successful, this grants the caller permission to access the accessory only until the device is disconnected. The following extras will be added to pi:

- [EXTRA_ACCESSORY](UsbManager.md) containing the accessory passed into this call
- [EXTRA_PERMISSION_GRANTED](UsbManager.md) containing boolean indicating whether permission was granted by the user

<br />

Requires the [PackageManager#FEATURE_USB_ACCESSORY](../android.content.pm/PackageManager.md) feature which can be detected using [PackageManager.hasSystemFeature(String)](../android.content.pm/PackageManager.md)).

<br />

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------|
| `accessory` | [UsbAccessory](UsbAccessory.md)!:to request permissions for |
| `pi` | [PendingIntent](../android.app/PendingIntent.md)!:PendingIntent for returning result |

### requestPermission

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun requestPermission(
    device: UsbDevice!, 
    pi: PendingIntent!
): Unit
```

Requests temporary permission for the given package to access the device. This may result in a system dialog being displayed to the user if permission had not already been granted. Success or failure is returned via the [android.app.PendingIntent](../android.app/PendingIntent.md) pi. If successful, this grants the caller permission to access the device only until the device is disconnected. The following extras will be added to pi:

- [EXTRA_DEVICE](UsbManager.md) containing the device passed into this call
- [EXTRA_PERMISSION_GRANTED](UsbManager.md) containing boolean indicating whether permission was granted by the user

Permission for USB devices of class [UsbConstants.USB_CLASS_VIDEO](UsbConstants.md) for clients that target SDK [android.os.Build.VERSION_CODES#P](../android/os/Build.VERSION_CODES.md) and above can be granted only if they have additionally the [android.Manifest.permission#CAMERA](../android/Manifest.permission.md) permission. 
Requires the [PackageManager#FEATURE_USB_HOST](../android.content.pm/PackageManager.md) feature which can be detected using [PackageManager.hasSystemFeature(String)](../android.content.pm/PackageManager.md)).

<br />

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------|
| `device` | [UsbDevice](UsbDevice.md)!:to request permissions for |
| `pi` | [PendingIntent](../android.app/PendingIntent.md)!:PendingIntent for returning result |
