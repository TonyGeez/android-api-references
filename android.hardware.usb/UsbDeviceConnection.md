# UsbDeviceConnection

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UsbDeviceConnection

Kotlin| [Java](../android/hardware/usb/UsbDeviceConnection.md) 
| --- | --- |

```
open class UsbDeviceConnection
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.hardware.usb.UsbDeviceConnection](../android/hardware/usb/UsbDeviceConnection.md) |

This class is used for sending and receiving data and control messages to a USB device. Instances of this class are created by [UsbManager.openDevice](../android/hardware/usb/UsbManager.md)).

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [bulkTransfer](../android/hardware/usb/UsbDeviceConnection.md))`(`endpoint:` ` [UsbEndpoint](../android/hardware/usb/UsbEndpoint.md)!`, `buffer:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `timeout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Performs a bulk transaction on the given endpoint. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [bulkTransfer](../android/hardware/usb/UsbDeviceConnection.md))`(`endpoint:` ` [UsbEndpoint](../android/hardware/usb/UsbEndpoint.md)!`, `buffer:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `timeout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Performs a bulk transaction on the given endpoint. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [claimInterface](../android/hardware/usb/UsbDeviceConnection.md))`(`intf:` ` [UsbInterface](../android/hardware/usb/UsbInterface.md)!`, `force:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Claims exclusive access to a [android.hardware.usb.UsbInterface](../android/hardware/usb/UsbInterface.md). |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](../android/hardware/usb/UsbDeviceConnection.md))`()` Releases all system resources related to the device. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [controlTransfer](../android/hardware/usb/UsbDeviceConnection.md))`(`requestType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `request:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `buffer:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `timeout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Performs a control transaction on endpoint zero for this device. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [controlTransfer](../android/hardware/usb/UsbDeviceConnection.md))`(`requestType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `request:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `buffer:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `timeout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Performs a control transaction on endpoint zero for this device. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getFileDescriptor](../android/hardware/usb/UsbDeviceConnection.md))`()` Returns the native file descriptor for the device, or -1 if the device is not opened. |
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getRawDescriptors](../android/hardware/usb/UsbDeviceConnection.md))`()` Returns the raw USB descriptors for the device. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSerial](../android/hardware/usb/UsbDeviceConnection.md))`()` Returns the serial number for the device. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [releaseInterface](../android/hardware/usb/UsbDeviceConnection.md))`(`intf:` ` [UsbInterface](../android/hardware/usb/UsbInterface.md)!`)` Releases exclusive access to a [android.hardware.usb.UsbInterface](../android/hardware/usb/UsbInterface.md). |
| open [UsbRequest](../android/hardware/usb/UsbRequest.md)! | [requestWait](../android/hardware/usb/UsbDeviceConnection.md))`()` Waits for the result of a android. |
| open [UsbRequest](../android/hardware/usb/UsbRequest.md)! | [requestWait](../android/hardware/usb/UsbDeviceConnection.md))`(`timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Waits for the result of a android. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setConfiguration](../android/hardware/usb/UsbDeviceConnection.md))`(`configuration:` ` [UsbConfiguration](../android/hardware/usb/UsbConfiguration.md)!`)` Sets the device's current [android.hardware.usb.UsbConfiguration](../android/hardware/usb/UsbConfiguration.md). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setInterface](../android/hardware/usb/UsbDeviceConnection.md))`(`intf:` ` [UsbInterface](../android/hardware/usb/UsbInterface.md)!`)` Sets the current [android.hardware.usb.UsbInterface](../android/hardware/usb/UsbInterface.md). |

| Protected methods ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](../android/hardware/usb/UsbDeviceConnection.md))`()` <br /> |

## Public methods

### bulkTransfer

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun bulkTransfer(
    endpoint: UsbEndpoint!, 
    buffer: ByteArray!, 
    length: Int, 
    timeout: Int
): Int
```

Performs a bulk transaction on the given endpoint. The direction of the transfer is determined by the direction of the endpoint.

This method transfers data starting from index 0 in the buffer. To specify a different offset, use[bulkTransfer(android.hardware.usb.UsbEndpoint,byte[],int,int,int)](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbDeviceConnection#bulkTransfer(android.hardware.usb.UsbEndpoint,%20kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)).

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `endpoint` | [UsbEndpoint](../android/hardware/usb/UsbEndpoint.md)!:the endpoint for this transaction |
| `buffer` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:buffer for data to send or receive; can be`null`to wait for next transaction without reading data |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the length of the data to send or receive. Before {@value android.os.Build.VERSION_CODES#P Build.VERSION_CODES.P}, a value larger than 16384 bytes would be truncated down to 16384. In API {@value android.os.Build.VERSION_CODES#P Build.VERSION_CODES.P} and after, any value of length is valid. |
| --- | --- |
| `timeout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):in milliseconds, 0 is infinite |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | length of data transferred (or zero) for success, or negative value for failure |

### bulkTransfer

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun bulkTransfer(
    endpoint: UsbEndpoint!, 
    buffer: ByteArray!, 
    offset: Int, 
    length: Int, 
    timeout: Int
): Int
```

Performs a bulk transaction on the given endpoint. The direction of the transfer is determined by the direction of the endpoint.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `endpoint` | [UsbEndpoint](../android/hardware/usb/UsbEndpoint.md)!:the endpoint for this transaction |
| `buffer` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:buffer for data to send or receive |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index of the first byte in the buffer to send or receive |
| --- | --- |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the length of the data to send or receive. Before {@value android.os.Build.VERSION_CODES#P Build.VERSION_CODES.P}, a value larger than 16384 bytes would be truncated down to 16384. In API {@value android.os.Build.VERSION_CODES#P Build.VERSION_CODES.P} and after, any value of length is valid. |
| `timeout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):in milliseconds, 0 is infinite |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | length of data transferred (or zero) for success, or negative value for failure |

### claimInterface

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun claimInterface(
    intf: UsbInterface!, 
    force: Boolean
): Boolean
```

Claims exclusive access to a [android.hardware.usb.UsbInterface](../android/hardware/usb/UsbInterface.md). This must be done before sending or receiving data on any [android.hardware.usb.UsbEndpoint](../android/hardware/usb/UsbEndpoint.md) s belonging to the interface.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------|
| `intf` | [UsbInterface](../android/hardware/usb/UsbInterface.md)!:the interface to claim |
| `force` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true to disconnect kernel driver if necessary |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the interface was successfully claimed |

### close

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

Releases all system resources related to the device. Once the object is closed it cannot be used again. The client must call [UsbManager.openDevice](../android/hardware/usb/UsbManager.md))again to retrieve a new instance to reestablish communication with the device. 

### controlTransfer

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun controlTransfer(
    requestType: Int, 
    request: Int, 
    value: Int, 
    index: Int, 
    buffer: ByteArray?, 
    length: Int, 
    timeout: Int
): Int
```

Performs a control transaction on endpoint zero for this device. The direction of the transfer is determined by the request type. If requestType \& [UsbConstants.USB_ENDPOINT_DIR_MASK](../android/hardware/usb/UsbConstants.md) is [UsbConstants.USB_DIR_OUT](../android/hardware/usb/UsbConstants.md), then the transfer is a write, and if it is [UsbConstants.USB_DIR_IN](../android/hardware/usb/UsbConstants.md), then the transfer is a read.

This method transfers data starting from index 0 in the buffer. To specify a different offset, use[controlTransfer(int,int,int,int,byte[],int,int,int)](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbDeviceConnection#controlTransfer(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)).

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `requestType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):request type for this transaction |
| `request` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):request ID for this transaction |
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):value field for this transaction |
| --- | --- |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index field for this transaction |
| `buffer` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?:buffer for data portion of transaction, or null if no data needs to be sent or received |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the length of the data to send or receive |
| --- | --- |
| `timeout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):in milliseconds |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | length of data transferred (or zero) for success, or negative value for failure |

### controlTransfer

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun controlTransfer(
    requestType: Int, 
    request: Int, 
    value: Int, 
    index: Int, 
    buffer: ByteArray?, 
    offset: Int, 
    length: Int, 
    timeout: Int
): Int
```

Performs a control transaction on endpoint zero for this device. The direction of the transfer is determined by the request type. If requestType \& [UsbConstants.USB_ENDPOINT_DIR_MASK](../android/hardware/usb/UsbConstants.md) is [UsbConstants.USB_DIR_OUT](../android/hardware/usb/UsbConstants.md), then the transfer is a write, and if it is [UsbConstants.USB_DIR_IN](../android/hardware/usb/UsbConstants.md), then the transfer is a read.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `requestType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):request type for this transaction |
| `request` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):request ID for this transaction |
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):value field for this transaction |
| --- | --- |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index field for this transaction |
| `buffer` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?:buffer for data portion of transaction, or null if no data needs to be sent or received |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index of the first byte in the buffer to send or receive |
| --- | --- |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the length of the data to send or receive |
| `timeout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):in milliseconds |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | length of data transferred (or zero) for success, or negative value for failure |

### getFileDescriptor

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFileDescriptor(): Int
```

Returns the native file descriptor for the device, or -1 if the device is not opened. This is intended for passing to native code to access the device.

| Return ||
|----------------------------------------------------------------------------|----------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the native file descriptor |

### getRawDescriptors

Added in [API level 13](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRawDescriptors(): ByteArray!
```

Returns the raw USB descriptors for the device. This can be used to access descriptors not supported directly via the higher level APIs.

| Return ||
|------------------------------------------------------------------------------------------|---------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | raw USB descriptors |

### getSerial

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSerial(): String!
```

Returns the serial number for the device. This will return null if the device has not been opened.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the device serial number |

### releaseInterface

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun releaseInterface(intf: UsbInterface!): Boolean
```

Releases exclusive access to a [android.hardware.usb.UsbInterface](../android/hardware/usb/UsbInterface.md).

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the interface was successfully released |

### requestWait

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun requestWait(): UsbRequest!
```

Waits for the result of a android.hardware.usb.UsbRequest#queue operation

Note that this may return requests queued on multiple [android.hardware.usb.UsbEndpoint](../android/hardware/usb/UsbEndpoint.md) s. When multiple endpoints are in use, [android.hardware.usb.UsbRequest#getEndpoint](../android/hardware/usb/UsbRequest.md))and [android.hardware.usb.UsbRequest#getClientData](../android/hardware/usb/UsbRequest.md))can be useful in determining how to process the result of this function.

| Return ||
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------|
| [UsbRequest](../android/hardware/usb/UsbRequest.md)! | a completed USB request, or null if an error occurred |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | Before API {@value android.os.Build.VERSION_CODES#O Build.VERSION_CODES.O}: if the number of bytes read or written is more than the limit of the request's buffer. The number of bytes is determined by the`length`parameter of [UsbRequest.queue(ByteBuffer, int)](../android/hardware/usb/UsbRequest.md)) |
| `java.nio.BufferOverflowException` | In API {@value android.os.Build.VERSION_CODES#O Build.VERSION_CODES.O} and after: if the number of bytes read or written is more than the limit of the request's buffer. The number of bytes is determined by the`length`parameter of [UsbRequest.queue(ByteBuffer, int)](../android/hardware/usb/UsbRequest.md)) |

### requestWait

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun requestWait(timeout: Long): UsbRequest!
```

Waits for the result of a android.hardware.usb.UsbRequest#queue operation

Note that this may return requests queued on multiple [android.hardware.usb.UsbEndpoint](../android/hardware/usb/UsbEndpoint.md) s. When multiple endpoints are in use, [android.hardware.usb.UsbRequest#getEndpoint](../android/hardware/usb/UsbRequest.md))and [android.hardware.usb.UsbRequest#getClientData](../android/hardware/usb/UsbRequest.md))can be useful in determining how to process the result of this function.

Android processes [UsbRequests](../android/hardware/usb/UsbRequest.md) asynchronously. Hence it is not guaranteed that [requestWait(0)](../android/hardware/usb/UsbDeviceConnection.md))returns a request that has been queued right before even if the request could have been processed immediately.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------|
| `timeout` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):timeout in milliseconds. If 0 this method does not wait. |

| Return ||
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------|
| [UsbRequest](../android/hardware/usb/UsbRequest.md)! | a completed USB request, or`null`if an error occurred |

| Exceptions ||
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.nio.BufferOverflowException` | if the number of bytes read or written is more than the limit of the request's buffer. The number of bytes is determined by the`length`parameter of [UsbRequest.queue(ByteBuffer, int)](../android/hardware/usb/UsbRequest.md)) |
| `java.util.concurrent.TimeoutException` | if no request was received in`timeout`milliseconds. |

### setConfiguration

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setConfiguration(configuration: UsbConfiguration!): Boolean
```

Sets the device's current [android.hardware.usb.UsbConfiguration](../android/hardware/usb/UsbConfiguration.md).

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the configuration was successfully set |

### setInterface

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setInterface(intf: UsbInterface!): Boolean
```

Sets the current [android.hardware.usb.UsbInterface](../android/hardware/usb/UsbInterface.md). Used to select between two interfaces with the same ID but different alternate setting.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the interface was successfully selected |

## Protected methods

### finalize

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun finalize(): Unit
```

| Exceptions ||
|-----------------------|-------------------------------------|
| `java.lang.Throwable` | the`Exception`raised by this method |
