# UsbManager

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UsbManager

Kotlin| [Java](https://developer.android.com/reference/android/hardware/usb/UsbManager "View this page in Java") 
| --- | --- |

```
open class UsbManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.hardware.usb.UsbManager](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbManager#) |

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
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_USB_ACCESSORY_ATTACHED](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbManager#ACTION_USB_ACCESSORY_ATTACHED:kotlin.String) Activity intent sent when user attaches a USB accessory. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_USB_ACCESSORY_DETACHED](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbManager#ACTION_USB_ACCESSORY_DETACHED:kotlin.String) Broadcast Action: A broadcast for USB accessory detached event. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_USB_DEVICE_ATTACHED](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbManager#ACTION_USB_DEVICE_ATTACHED:kotlin.String) Activity intent sent when user attaches a USB device. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_USB_DEVICE_DETACHED](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbManager#ACTION_USB_DEVICE_DETACHED:kotlin.String) Broadcast Action: A broadcast for USB device detached event. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_ACCESSORY](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbManager#EXTRA_ACCESSORY:kotlin.String) Name of extra for [ACTION_USB_ACCESSORY_ATTACHED](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbManager#ACTION_USB_ACCESSORY_ATTACHED:kotlin.String) and [ACTION_USB_ACCESSORY_DETACHED](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbManager#ACTION_USB_ACCESSORY_DETACHED:kotlin.String) broadcasts containing the [UsbAccessory](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbAccessory) object for the accessory. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_DEVICE](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbManager#EXTRA_DEVICE:kotlin.String) Name of extra for [ACTION_USB_DEVICE_ATTACHED](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbManager#ACTION_USB_DEVICE_ATTACHED:kotlin.String) and [ACTION_USB_DEVICE_DETACHED](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbManager#ACTION_USB_DEVICE_DETACHED:kotlin.String) broadcasts containing the [UsbDevice](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbDevice) object for the device. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_PERMISSION_GRANTED](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbManager#EXTRA_PERMISSION_GRANTED:kotlin.String) Name of extra added to the [android.app.PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#) passed into [requestPermission(android.hardware.usb.UsbDevice,android.app.PendingIntent)](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbManager#requestPermission(android.hardware.usb.UsbDevice,%20android.app.PendingIntent))or [requestPermission(android.hardware.usb.UsbAccessory,android.app.PendingIntent)](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbManager#requestPermission(android.hardware.usb.UsbAccessory,%20android.app.PendingIntent))containing a boolean value indicating whether the user granted permission or not. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [UsbAccessory](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbAccessory)!\>! | [getAccessoryList](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbManager#getAccessoryList())`()` Returns a list of currently attached USB accessories. |
| open [HashMap](https://developer.android.com/reference/kotlin/java/util/HashMap.html#)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [UsbDevice](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbDevice)!\>! | [getDeviceList](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbManager#getDeviceList())`()` Returns a HashMap containing all USB devices currently attached. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasPermission](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbManager#hasPermission(android.hardware.usb.UsbAccessory))`(`accessory:` ` [UsbAccessory](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbAccessory)!`)` Returns true if the caller has permission to access the accessory. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasPermission](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbManager#hasPermission(android.hardware.usb.UsbDevice))`(`device:` ` [UsbDevice](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbDevice)!`)` Returns true if the caller has permission to access the device. |
| open [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#)! | [openAccessory](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbManager#openAccessory(android.hardware.usb.UsbAccessory))`(`accessory:` ` [UsbAccessory](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbAccessory)!`)` Opens a file descriptor for reading and writing data to the USB accessory. |
| open [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#) | [openAccessoryInputStream](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbManager#openAccessoryInputStream(android.hardware.usb.UsbAccessory))`(`accessory:` ` [UsbAccessory](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbAccessory)`)` Opens an input stream for reading from the USB accessory. |
| --- | --- |
| open [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#) | [openAccessoryOutputStream](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbManager#openAccessoryOutputStream(android.hardware.usb.UsbAccessory))`(`accessory:` ` [UsbAccessory](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbAccessory)`)` Opens an output stream for writing to the USB accessory. |
| open [UsbDeviceConnection](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbDeviceConnection)! | [openDevice](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbManager#openDevice(android.hardware.usb.UsbDevice))`(`device:` ` [UsbDevice](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbDevice)!`)` Opens the device so it can be used to send and receive data using [android.hardware.usb.UsbRequest](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbRequest). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestPermission](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbManager#requestPermission(android.hardware.usb.UsbAccessory,%20android.app.PendingIntent))`(`accessory:` ` [UsbAccessory](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbAccessory)!`, `pi:` ` [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#)!`)` Requests temporary permission for the given package to access the accessory. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [requestPermission](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbManager#requestPermission(android.hardware.usb.UsbDevice,%20android.app.PendingIntent))`(`device:` ` [UsbDevice](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbDevice)!`, `pi:` ` [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#)!`)` Requests temporary permission for the given package to access the device. |

## Constants

### ACTION_USB_ACCESSORY_ATTACHED

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_USB_ACCESSORY_ATTACHED: String
```

Activity intent sent when user attaches a USB accessory.

- [EXTRA_ACCESSORY](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbManager#EXTRA_ACCESSORY:kotlin.String) containing the [android.hardware.usb.UsbAccessory](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbAccessory) for the attached accessory

<br />

 Value: "android.hardware.usb.action.USB_ACCESSORY_ATTACHED"

### ACTION_USB_ACCESSORY_DETACHED

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_USB_ACCESSORY_DETACHED: String
```

Broadcast Action: A broadcast for USB accessory detached event. This intent is sent when a USB accessory is detached.

- [EXTRA_ACCESSORY](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbManager#EXTRA_ACCESSORY:kotlin.String) containing the [UsbAccessory](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbAccessory) for the attached accessory that was detached

<br />

 Value: "android.hardware.usb.action.USB_ACCESSORY_DETACHED"

### ACTION_USB_DEVICE_ATTACHED

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_USB_DEVICE_ATTACHED: String
```

Activity intent sent when user attaches a USB device. This intent is sent when a USB device is attached to the USB bus when in host mode.

- [EXTRA_DEVICE](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbManager#EXTRA_DEVICE:kotlin.String) containing the [android.hardware.usb.UsbDevice](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbDevice) for the attached device

<br />

 Value: "android.hardware.usb.action.USB_DEVICE_ATTACHED"

### ACTION_USB_DEVICE_DETACHED

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_USB_DEVICE_DETACHED: String
```

Broadcast Action: A broadcast for USB device detached event. This intent is sent when a USB device is detached from the USB bus when in host mode.

- [EXTRA_DEVICE](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbManager#EXTRA_DEVICE:kotlin.String) containing the [android.hardware.usb.UsbDevice](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbDevice) for the detached device

<br />

 Value: "android.hardware.usb.action.USB_DEVICE_DETACHED"

### EXTRA_ACCESSORY

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_ACCESSORY: String
```

Name of extra for [ACTION_USB_ACCESSORY_ATTACHED](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbManager#ACTION_USB_ACCESSORY_ATTACHED:kotlin.String) and [ACTION_USB_ACCESSORY_DETACHED](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbManager#ACTION_USB_ACCESSORY_DETACHED:kotlin.String) broadcasts containing the [UsbAccessory](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbAccessory) object for the accessory. 

 Value: "accessory"

### EXTRA_DEVICE

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_DEVICE: String
```

Name of extra for [ACTION_USB_DEVICE_ATTACHED](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbManager#ACTION_USB_DEVICE_ATTACHED:kotlin.String) and [ACTION_USB_DEVICE_DETACHED](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbManager#ACTION_USB_DEVICE_DETACHED:kotlin.String) broadcasts containing the [UsbDevice](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbDevice) object for the device. 

 Value: "device"

### EXTRA_PERMISSION_GRANTED

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_PERMISSION_GRANTED: String
```

Name of extra added to the [android.app.PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#) passed into [requestPermission(android.hardware.usb.UsbDevice,android.app.PendingIntent)](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbManager#requestPermission(android.hardware.usb.UsbDevice,%20android.app.PendingIntent))or [requestPermission(android.hardware.usb.UsbAccessory,android.app.PendingIntent)](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbManager#requestPermission(android.hardware.usb.UsbAccessory,%20android.app.PendingIntent))containing a boolean value indicating whether the user granted permission or not. 

 Value: "permission"

## Public methods

### getAccessoryList

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAccessoryList(): Array<UsbAccessory!>!
```

Returns a list of currently attached USB accessories. (in the current implementation there can be at most one) 
Requires the [PackageManager#FEATURE_USB_ACCESSORY](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_USB_ACCESSORY:kotlin.String) feature which can be detected using [PackageManager.hasSystemFeature(String)](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#hasSystemFeature(kotlin.String)).

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [UsbAccessory](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbAccessory)!>! | list of USB accessories, or null if none are attached. |

### getDeviceList

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDeviceList(): HashMap<String!, UsbDevice!>!
```

Returns a HashMap containing all USB devices currently attached. USB device name is the key for the returned HashMap. The result will be empty if no devices are attached, or if USB host mode is inactive or unsupported. 
Requires the [PackageManager#FEATURE_USB_HOST](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_USB_HOST:kotlin.String) feature which can be detected using [PackageManager.hasSystemFeature(String)](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#hasSystemFeature(kotlin.String)).

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [HashMap](https://developer.android.com/reference/kotlin/java/util/HashMap.html#)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [UsbDevice](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbDevice)!>! | HashMap containing all connected USB devices. |

### hasPermission

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasPermission(accessory: UsbAccessory!): Boolean
```

Returns true if the caller has permission to access the accessory. Permission might have been granted temporarily via [requestPermission(android.hardware.usb.UsbAccessory,android.app.PendingIntent)](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbManager#requestPermission(android.hardware.usb.UsbAccessory,%20android.app.PendingIntent))or by the user choosing the caller as the default application for the accessory. 
Requires the [PackageManager#FEATURE_USB_ACCESSORY](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_USB_ACCESSORY:kotlin.String) feature which can be detected using [PackageManager.hasSystemFeature(String)](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#hasSystemFeature(kotlin.String)).

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------|
| `accessory` | [UsbAccessory](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbAccessory)!:to check permissions for |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if caller has permission |

### hasPermission

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasPermission(device: UsbDevice!): Boolean
```

Returns true if the caller has permission to access the device. Permission might have been granted temporarily via [requestPermission(android.hardware.usb.UsbDevice,android.app.PendingIntent)](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbManager#requestPermission(android.hardware.usb.UsbDevice,%20android.app.PendingIntent))or by the user choosing the caller as the default application for the device. Permission for USB devices of class [UsbConstants.USB_CLASS_VIDEO](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbConstants#USB_CLASS_VIDEO:kotlin.Int) for clients that target SDK [android.os.Build.VERSION_CODES#P](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#P:kotlin.Int) and above can be granted only if they have additionally the [android.Manifest.permission#CAMERA](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#CAMERA:kotlin.String) permission. 
Requires the [PackageManager#FEATURE_USB_HOST](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_USB_HOST:kotlin.String) feature which can be detected using [PackageManager.hasSystemFeature(String)](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#hasSystemFeature(kotlin.String)).

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------|
| `device` | [UsbDevice](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbDevice)!:to check permissions for |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if caller has permission |

### openAccessory

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun openAccessory(accessory: UsbAccessory!): ParcelFileDescriptor!
```

Opens a file descriptor for reading and writing data to the USB accessory.

If data is read from the [java.io.InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#) created from this file descriptor all data of a USB transfer should be read at once. If only a partial request is read the rest of the transfer is dropped.

It is strongly recommended to use newer methods instead of this method, since this method may provide sub-optimal performance on some devices. This method could potentially face interim performance degradation as well. 
Requires the [PackageManager#FEATURE_USB_ACCESSORY](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_USB_ACCESSORY:kotlin.String) feature which can be detected using [PackageManager.hasSystemFeature(String)](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#hasSystemFeature(kotlin.String)).

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------|
| `accessory` | [UsbAccessory](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbAccessory)!:the USB accessory to open |

| Return ||
|---------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#)! | file descriptor, or null if the accessory could not be opened. |

### openAccessoryInputStream

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun openAccessoryInputStream(accessory: UsbAccessory): InputStream
```

Opens an input stream for reading from the USB accessory. If accessory is not open at this point, accessory will first be opened.

If data is read from the created [java.io.InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#) all data of a USB transfer should be read at once. If only a partial request is read, the rest of the transfer is dropped.

The caller is responsible for ensuring that the returned stream is closed. 
Requires the [PackageManager#FEATURE_USB_ACCESSORY](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_USB_ACCESSORY:kotlin.String) feature which can be detected using [PackageManager.hasSystemFeature(String)](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#hasSystemFeature(kotlin.String)).

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `accessory` | [UsbAccessory](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbAccessory):the USB accessory to open an input stream for This value cannot be`null`. |

| Return ||
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#) | input stream to read from given USB accessory This value cannot be`null`. |

### openAccessoryOutputStream

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun openAccessoryOutputStream(accessory: UsbAccessory): OutputStream
```

Opens an output stream for writing to the USB accessory. If accessory is not open at this point, accessory will first be opened.

The caller is responsible for ensuring that the returned stream is closed. 
Requires the [PackageManager#FEATURE_USB_ACCESSORY](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_USB_ACCESSORY:kotlin.String) feature which can be detected using [PackageManager.hasSystemFeature(String)](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#hasSystemFeature(kotlin.String)).

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `accessory` | [UsbAccessory](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbAccessory):the USB accessory to open an output stream for This value cannot be`null`. |

| Return ||
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#) | output stream to write to given USB accessory This value cannot be`null`. |

### openDevice

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun openDevice(device: UsbDevice!): UsbDeviceConnection!
```

Opens the device so it can be used to send and receive data using [android.hardware.usb.UsbRequest](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbRequest). 
Requires the [PackageManager#FEATURE_USB_HOST](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_USB_HOST:kotlin.String) feature which can be detected using [PackageManager.hasSystemFeature(String)](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#hasSystemFeature(kotlin.String)).

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------|
| `device` | [UsbDevice](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbDevice)!:the device to open |

| Return ||
|-----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [UsbDeviceConnection](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbDeviceConnection)! | a [UsbDeviceConnection](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbDeviceConnection), or`null`if open failed |

### requestPermission

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun requestPermission(
    accessory: UsbAccessory!, 
    pi: PendingIntent!
): Unit
```

Requests temporary permission for the given package to access the accessory. This may result in a system dialog being displayed to the user if permission had not already been granted. Success or failure is returned via the [android.app.PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#) pi. If successful, this grants the caller permission to access the accessory only until the device is disconnected. The following extras will be added to pi:

- [EXTRA_ACCESSORY](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbManager#EXTRA_ACCESSORY:kotlin.String) containing the accessory passed into this call
- [EXTRA_PERMISSION_GRANTED](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbManager#EXTRA_PERMISSION_GRANTED:kotlin.String) containing boolean indicating whether permission was granted by the user

<br />

Requires the [PackageManager#FEATURE_USB_ACCESSORY](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_USB_ACCESSORY:kotlin.String) feature which can be detected using [PackageManager.hasSystemFeature(String)](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#hasSystemFeature(kotlin.String)).

<br />

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------|
| `accessory` | [UsbAccessory](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbAccessory)!:to request permissions for |
| `pi` | [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#)!:PendingIntent for returning result |

### requestPermission

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun requestPermission(
    device: UsbDevice!, 
    pi: PendingIntent!
): Unit
```

Requests temporary permission for the given package to access the device. This may result in a system dialog being displayed to the user if permission had not already been granted. Success or failure is returned via the [android.app.PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#) pi. If successful, this grants the caller permission to access the device only until the device is disconnected. The following extras will be added to pi:

- [EXTRA_DEVICE](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbManager#EXTRA_DEVICE:kotlin.String) containing the device passed into this call
- [EXTRA_PERMISSION_GRANTED](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbManager#EXTRA_PERMISSION_GRANTED:kotlin.String) containing boolean indicating whether permission was granted by the user

Permission for USB devices of class [UsbConstants.USB_CLASS_VIDEO](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbConstants#USB_CLASS_VIDEO:kotlin.Int) for clients that target SDK [android.os.Build.VERSION_CODES#P](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#P:kotlin.Int) and above can be granted only if they have additionally the [android.Manifest.permission#CAMERA](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#CAMERA:kotlin.String) permission. 
Requires the [PackageManager#FEATURE_USB_HOST](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_USB_HOST:kotlin.String) feature which can be detected using [PackageManager.hasSystemFeature(String)](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#hasSystemFeature(kotlin.String)).

<br />

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------|
| `device` | [UsbDevice](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbDevice)!:to request permissions for |
| `pi` | [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#)!:PendingIntent for returning result |
