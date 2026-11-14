# MtpDevice

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MtpDevice

Kotlin | [Java](MtpDevice.md) 
| --- | --- |

```
class MtpDevice
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.mtp.MtpDevice](MtpDevice.md) |

This class represents an MTP or PTP device connected on the USB host bus. An application can instantiate an object of this type, by referencing an attached and then use methods in this class to get information about the device and objects stored on it, as well as open the connection and transfer data.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [MtpDevice](MtpDevice.md))`(`device:` ` [UsbDevice](../android.hardware.usb/UsbDevice.md)`)` MtpClient constructor |

| Public methods ||
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](MtpDevice.md))`()` Closes all resources related to the MtpDevice object. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [deleteObject](MtpDevice.md))`(`objectHandle:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Deletes an object on the device. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDeviceId](MtpDevice.md))`()` Returns the USB ID of the USB device. |
| --- | --- |
| [MtpDeviceInfo](MtpDeviceInfo.md)? | [getDeviceInfo](MtpDevice.md))`()` Returns the [MtpDeviceInfo](MtpDeviceInfo.md) for this device |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getDeviceName](MtpDevice.md))`()` Returns the name of the USB device This returns the same value as android. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | [getObject](MtpDevice.md))`(`objectHandle:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `objectSize:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the data for an object as a byte array. |
| --- | --- |
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)? | [getObjectHandles](MtpDevice.md))`(`storageId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `format:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `objectHandle:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the list of object handles for all objects on the given storage unit, with the given format and parent. |
| [MtpObjectInfo](MtpObjectInfo.md)? | [getObjectInfo](MtpDevice.md))`(`objectHandle:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves the [MtpObjectInfo](MtpObjectInfo.md) for an object. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getParent](MtpDevice.md))`(`objectHandle:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves the object handle for the parent of an object on the device. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getPartialObject](MtpDevice.md))`(`objectHandle:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `offset:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `size:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `buffer:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`)` Obtains object bytes in the specified range and writes it to an array. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getPartialObject64](MtpDevice.md))`(`objectHandle:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `offset:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `size:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `buffer:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`)` Obtains object bytes in the specified range and writes it to an array. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getStorageId](MtpDevice.md))`(`objectHandle:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves the ID of the storage unit containing the given object on the device. |
| --- | --- |
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)? | [getStorageIds](MtpDevice.md))`()` Returns the list of IDs for all storage units on this device Information about each storage unit can be accessed via [getStorageInfo](MtpDevice.md)). |
| [MtpStorageInfo](MtpStorageInfo.md)? | [getStorageInfo](MtpDevice.md))`(`storageId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieves the [MtpStorageInfo](MtpStorageInfo.md) for a storage unit. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | [getThumbnail](MtpDevice.md))`(`objectHandle:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the thumbnail data for an object as a byte array. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [importFile](MtpDevice.md))`(`objectHandle:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `descriptor:` ` [ParcelFileDescriptor](../android.os/ParcelFileDescriptor.md)`)` Copies the data for an object to a file descriptor. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [importFile](MtpDevice.md))`(`objectHandle:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `destPath:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Copies the data for an object to a file in external storage. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [open](MtpDevice.md))`(`connection:` ` [UsbDeviceConnection](../android.hardware.usb/UsbDeviceConnection.md)`)` Opens the MTP device. |
| --- | --- |
| [MtpEvent](MtpEvent.md) | [readEvent](MtpDevice.md))`(`signal:` ` [CancellationSignal](../android.os/CancellationSignal.md)?`)` Reads an event from the device. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [sendObject](MtpDevice.md))`(`objectHandle:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `size:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `descriptor:` ` [ParcelFileDescriptor](../android.os/ParcelFileDescriptor.md)`)` Copies the data for an object from a file descriptor. |
| [MtpObjectInfo](MtpObjectInfo.md)? | [sendObjectInfo](MtpDevice.md))`(`info:` ` [MtpObjectInfo](MtpObjectInfo.md)`)` Uploads an object metadata for a new entry. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](MtpDevice.md))`()` Returns a string representation of the object. |

| Protected methods ||
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](MtpDevice.md))`()` <br /> |

## Public constructors

### MtpDevice

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
MtpDevice(device: UsbDevice)
```

MtpClient constructor

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `device` | [UsbDevice](../android.hardware.usb/UsbDevice.md): the [android.hardware.usb.UsbDevice](../android.hardware.usb/UsbDevice.md) for the MTP or PTP device This value cannot be `null`. |

## Public methods

### close

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun close(): Unit
```

Closes all resources related to the MtpDevice object. After this is called, the object can not be used until [open](MtpDevice.md)) is called again with a new [android.hardware.usb.UsbDeviceConnection](../android.hardware.usb/UsbDeviceConnection.md). 

### deleteObject

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun deleteObject(objectHandle: Int): Boolean
```

Deletes an object on the device. This call may block, since deleting a directory containing many files may take a long time on some devices.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------|
| `objectHandle` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): handle of the object to delete |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the deletion succeeds |

### getDeviceId

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDeviceId(): Int
```

Returns the USB ID of the USB device. This returns the same value as android.hardware.usb.UsbDevice#getDeviceId for the device's [android.hardware.usb.UsbDevice](../android.hardware.usb/UsbDevice.md)

| Return ||
|----------------------------------------------------------------------------|---------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the device ID |

### getDeviceInfo

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDeviceInfo(): MtpDeviceInfo?
```

Returns the [MtpDeviceInfo](MtpDeviceInfo.md) for this device

| Return ||
|--------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [MtpDeviceInfo](MtpDeviceInfo.md)? | the device info, or null if fetching device info fails |

### getDeviceName

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDeviceName(): String
```

Returns the name of the USB device This returns the same value as android.hardware.usb.UsbDevice#getDeviceName for the device's [android.hardware.usb.UsbDevice](../android.hardware.usb/UsbDevice.md)

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the device name This value cannot be `null`. |

### getObject

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getObject(
    objectHandle: Int, 
    objectSize: Int
): ByteArray?
```

Returns the data for an object as a byte array. This call may block for an arbitrary amount of time depending on the size of the data and speed of the devices.

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `objectHandle` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): handle of the object to read |
| `objectSize` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the size of the object (this should match [MtpObjectInfo.getCompressedSize](MtpObjectInfo.md))) |

| Return ||
|------------------------------------------------------------------------------------------|---------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | the object's data, or null if reading fails |

### getObjectHandles

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getObjectHandles(
    storageId: Int, 
    format: Int, 
    objectHandle: Int
): IntArray?
```

Returns the list of object handles for all objects on the given storage unit, with the given format and parent. Information about each object can be accessed via [getObjectInfo](MtpDevice.md)).

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `storageId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the storage unit to query |
| `format` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the format of the object to return, or zero for all formats |
| `objectHandle` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the parent object to query, -1 for the storage root, or zero for all objects |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)? | the object handles, or null if fetching object handles fails |

### getObjectInfo

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getObjectInfo(objectHandle: Int): MtpObjectInfo?
```

Retrieves the [MtpObjectInfo](MtpObjectInfo.md) for an object.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------|
| `objectHandle` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the handle of the object |

| Return ||
|--------------------------------------------------------------------------------------------|----------------------------------------------------------|
| [MtpObjectInfo](MtpObjectInfo.md)? | the MtpObjectInfo, or null if fetching object info fails |

### getParent

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getParent(objectHandle: Int): Long
```

Retrieves the object handle for the parent of an object on the device.

| Parameters ||
|----------------|-----------------------------------------------------------------------------------------------------------|
| `objectHandle` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): handle of the object to query |

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the parent's handle, or zero if it is in the root of the storage |

### getPartialObject

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPartialObject(
    objectHandle: Int, 
    offset: Long, 
    size: Long, 
    buffer: ByteArray
): Long
```

Obtains object bytes in the specified range and writes it to an array. This call may block for an arbitrary amount of time depending on the size of the data and speed of the devices.

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `objectHandle` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): handle of the object to read |
| `offset` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): Start index of reading range. It must be a non-negative value at most 0xffffffff. |
| `size` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): Size of reading range. It must be a non-negative value at most Integer.MAX_VALUE or 0xffffffff. If 0xffffffff is specified, the method obtains the full bytes of object. |
| --- | --- |
| `buffer` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): Array to write data. This value cannot be `null`. |

| Return ||
|------------------------------------------------------------------------------|---------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | Size of bytes that are actually read. |

### getPartialObject64

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPartialObject64(
    objectHandle: Int, 
    offset: Long, 
    size: Long, 
    buffer: ByteArray
): Long
```

Obtains object bytes in the specified range and writes it to an array. This call may block for an arbitrary amount of time depending on the size of the data and speed of the devices. This is a vender-extended operation supported by Android that enables us to pass unsigned 64-bit offset. Check if the MTP device supports the operation by using [MtpDeviceInfo.getOperationsSupported()](MtpDeviceInfo.md)).

| Parameters ||
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `objectHandle` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): handle of the object to read |
| `offset` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): Start index of reading range. It must be a non-negative value. |
| `size` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): Size of reading range. It must be a non-negative value at most Integer.MAX_VALUE. |
| --- | --- |
| `buffer` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): Array to write data. This value cannot be `null`. |

| Return ||
|------------------------------------------------------------------------------|---------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | Size of bytes that are actually read. |

**See Also**

- [android.mtp.MtpConstants#OPERATION_GET_PARTIAL_OBJECT_64](MtpConstants.md) 

### getStorageId

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getStorageId(objectHandle: Int): Long
```

Retrieves the ID of the storage unit containing the given object on the device.

| Parameters ||
|----------------|-----------------------------------------------------------------------------------------------------------|
| `objectHandle` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): handle of the object to query |

| Return ||
|------------------------------------------------------------------------------|------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the object's storage unit ID |

### getStorageIds

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getStorageIds(): IntArray?
```

Returns the list of IDs for all storage units on this device Information about each storage unit can be accessed via [getStorageInfo](MtpDevice.md)).

| Return ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)? | the list of storage IDs, or null if fetching storage IDs fails |

### getStorageInfo

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getStorageInfo(storageId: Int): MtpStorageInfo?
```

Retrieves the [MtpStorageInfo](MtpStorageInfo.md) for a storage unit.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------|
| `storageId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the ID of the storage unit |

| Return ||
|----------------------------------------------------------------------------------------------|------------------------------------------------------------|
| [MtpStorageInfo](MtpStorageInfo.md)? | the MtpStorageInfo, or null if fetching storage info fails |

### getThumbnail

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getThumbnail(objectHandle: Int): ByteArray?
```

Returns the thumbnail data for an object as a byte array. The size and format of the thumbnail data can be determined via [MtpObjectInfo.getThumbCompressedSize](MtpObjectInfo.md)) and [MtpObjectInfo.getThumbFormat](MtpObjectInfo.md)). For typical devices the format is JPEG.

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------|
| `objectHandle` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): handle of the object to read |

| Return ||
|------------------------------------------------------------------------------------------|--------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | the object's thumbnail, or null if reading fails |

### importFile

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun importFile(
    objectHandle: Int, 
    descriptor: ParcelFileDescriptor
): Boolean
```

Copies the data for an object to a file descriptor. This call may block for an arbitrary amount of time depending on the size of the data and speed of the devices. The file descriptor is not closed on completion, and must be done by the caller.

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `objectHandle` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): handle of the object to read |
| `descriptor` | [ParcelFileDescriptor](../android.os/ParcelFileDescriptor.md): file descriptor to write the data to for the file transfer. This value cannot be `null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the file transfer succeeds |

### importFile

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun importFile(
    objectHandle: Int, 
    destPath: String
): Boolean
```

Copies the data for an object to a file in external storage. This call may block for an arbitrary amount of time depending on the size of the data and speed of the devices.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `objectHandle` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): handle of the object to read |
| `destPath` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): path to destination for the file transfer. This path should be in the external storage as defined by [android.os.Environment#getExternalStorageDirectory](../android.os/Environment.md)) This value cannot be `null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the file transfer succeeds |

### open

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun open(connection: UsbDeviceConnection): Boolean
```

Opens the MTP device. Once the device is open it takes ownership of the [android.hardware.usb.UsbDeviceConnection](../android.hardware.usb/UsbDeviceConnection.md). The connection will be closed when you call [close()](MtpDevice.md)) The connection will also be closed if this method fails.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `connection` | [UsbDeviceConnection](../android.hardware.usb/UsbDeviceConnection.md): an open [android.hardware.usb.UsbDeviceConnection](../android.hardware.usb/UsbDeviceConnection.md) for the device This value cannot be `null`. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the device was successfully opened. |

### readEvent

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun readEvent(signal: CancellationSignal?): MtpEvent
```

Reads an event from the device. It blocks the current thread until it gets an event. It throws OperationCanceledException if it is cancelled by signal.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `signal` | [CancellationSignal](../android.os/CancellationSignal.md)?: signal for cancellation This value may be `null`. |

| Return ||
|---------------------------------------------------------------------------------|---------------------------------------------|
| [MtpEvent](MtpEvent.md) | obtained event This value cannot be `null`. |

| Exceptions ||
|-----------------------|---|
| `java.io.IOException` | |

### sendObject

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun sendObject(
    objectHandle: Int, 
    size: Long, 
    descriptor: ParcelFileDescriptor
): Boolean
```

Copies the data for an object from a file descriptor. This call may block for an arbitrary amount of time depending on the size of the data and speed of the devices. The file descriptor is not closed on completion, and must be done by the caller.

| Parameters ||
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `objectHandle` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): handle of the target file |
| `size` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): size of the file in bytes |
| `descriptor` | [ParcelFileDescriptor](../android.os/ParcelFileDescriptor.md): file descriptor to read the data from. This value cannot be `null`. |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the file transfer succeeds |

### sendObjectInfo

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun sendObjectInfo(info: MtpObjectInfo): MtpObjectInfo?
```

Uploads an object metadata for a new entry. The [MtpObjectInfo](MtpObjectInfo.md) can be created with the [MtpObjectInfo.Builder](../android/mtp/MtpObjectInfo.Builder.md) class. The returned [MtpObjectInfo](MtpObjectInfo.md) has the new object handle field filled in.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `info` | [MtpObjectInfo](MtpObjectInfo.md): metadata of the entry This value cannot be `null`. |

| Return ||
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [MtpObjectInfo](MtpObjectInfo.md)? | object info of the created entry, or null if sending object info fails |

### toString

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|----------------------------------------------------------------------------------|------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be `null`. |

## Protected methods

### finalize

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected fun finalize(): Unit
```

| Exceptions ||
|-----------------------|---------------------------------------|
| `java.lang.Throwable` | the `Exception` raised by this method |
