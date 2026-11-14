# UsbRequest

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UsbRequest

Kotlin| [Java](https://developer.android.com/reference/android/hardware/usb/UsbRequest "View this page in Java") 
| --- | --- |

```
open class UsbRequest
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.hardware.usb.UsbRequest](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbRequest#) |

A class representing USB request packet. This can be used for both reading and writing data to or from a [android.hardware.usb.UsbDeviceConnection](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbDeviceConnection). UsbRequests can be used to transfer data on bulk and interrupt endpoints. Requests on bulk endpoints can be sent synchronously via android.hardware.usb.UsbDeviceConnection#bulkTransfer or asynchronously via #queue and android.hardware.usb.UsbDeviceConnection#requestWait. Requests on interrupt endpoints are only send and received asynchronously.

Requests on endpoint zero are not supported by this class; use android.hardware.usb.UsbDeviceConnection#controlTransfer for endpoint zero requests instead.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------|---|
| [UsbRequest](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbRequest#UsbRequest())`()` <br /> |

| Public methods ||
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [cancel](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbRequest#cancel())`()` Cancels a pending queue operation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbRequest#close())`()` Releases all resources related to this request. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getClientData](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbRequest#getClientData())`()` Returns the client data for the request. |
| --- | --- |
| open [UsbEndpoint](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbEndpoint)! | [getEndpoint](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbRequest#getEndpoint())`()` Returns the endpoint for the request, or null if the request is not opened. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [initialize](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbRequest#initialize(android.hardware.usb.UsbDeviceConnection,%20android.hardware.usb.UsbEndpoint))`(`connection:` ` [UsbDeviceConnection](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbDeviceConnection)!`, `endpoint:` ` [UsbEndpoint](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbEndpoint)!`)` Initializes the request so it can read or write data on the given endpoint. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [queue](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbRequest#queue(java.nio.ByteBuffer))`(`buffer:` ` [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)?`)` Queues the request to send or receive data on its endpoint. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [queue](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbRequest#queue(java.nio.ByteBuffer,%20kotlin.Int))`(`buffer:` ` [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Queues the request to send or receive data on its endpoint. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setClientData](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbRequest#setClientData(kotlin.Any))`(`data:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Sets the client data for the request. |

| Protected methods ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbRequest#finalize())`()` <br /> |

## Public constructors

### UsbRequest

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
UsbRequest()
```

## Public methods

### cancel

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun cancel(): Boolean
```

Cancels a pending queue operation.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if cancelling succeeded |

### close

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

Releases all resources related to this request. 

### getClientData

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getClientData(): Any!
```

Returns the client data for the request. This can be used in conjunction with [setClientData](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbRequest#setClientData(kotlin.Any))to associate another object with this request, which can be useful for maintaining state between calls to #queue and android.hardware.usb.UsbDeviceConnection#requestWait

| Return ||
|-----------------------------------------------------------------------------|---------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | the client data for the request |

### getEndpoint

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEndpoint(): UsbEndpoint!
```

Returns the endpoint for the request, or null if the request is not opened.

| Return ||
|-------------------------------------------------------------------------------------------------|------------------------|
| [UsbEndpoint](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbEndpoint)! | the request's endpoint |

### initialize

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun initialize(
    connection: UsbDeviceConnection!, 
    endpoint: UsbEndpoint!
): Boolean
```

Initializes the request so it can read or write data on the given endpoint. Whether the request allows reading or writing depends on the direction of the endpoint.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `endpoint` | [UsbEndpoint](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbEndpoint)!:the endpoint to be used for this request. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the request was successfully opened. |

### queue

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun queue(buffer: ByteBuffer?): Boolean
```

Queues the request to send or receive data on its endpoint.

For OUT endpoints, the remaining bytes of the buffer will be sent on the endpoint. For IN endpoints, the endpoint will attempt to fill the remaining bytes of the buffer. If the queueing operation is successful, return true. The result will be returned via android.hardware.usb.UsbDeviceConnection#requestWait

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `buffer` | [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)?:the buffer containing the bytes to send, or the buffer to fill. The state of the buffer is undefined until the request is returned by android.hardware.usb.UsbDeviceConnection#requestWait. If the request failed the buffer will be unchanged; if the request succeeded the position of the buffer is incremented by the number of bytes sent/received. Before {@value android.os.Build.VERSION_CODES#P Build.VERSION_CODES.P}, a buffer of length larger than 16384 bytes would throw IllegalArgumentException. In API {@value android.os.Build.VERSION_CODES#P Build.VERSION_CODES.P} and after, any size buffer is valid. This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the queueing operation succeeded |

### queue

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun queue(
    buffer: ByteBuffer!, 
    length: Int
): Boolean
```

**Deprecated:** *Use [queue(java.nio.ByteBuffer)](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbRequest#queue(java.nio.ByteBuffer))instead.*

Queues the request to send or receive data on its endpoint.

For OUT endpoints, the given buffer data will be sent on the endpoint. For IN endpoints, the endpoint will attempt to read the given number of bytes into the specified buffer. If the queueing operation is successful, return true. The result will be returned via android.hardware.usb.UsbDeviceConnection#requestWait

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `buffer` | [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!:the buffer containing the bytes to write, or location to store the results of a read. Position and array offset will be ignored and assumed to be 0. Limit and capacity will be ignored. Once the request [is processed](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbDeviceConnection#requestWait())the position will be set to the number of bytes read/written. |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):number of bytes to read or write. Before {@value android.os.Build.VERSION_CODES#P Build.VERSION_CODES.P}, a value larger than 16384 bytes would be truncated down to 16384. In API {@value android.os.Build.VERSION_CODES#P Build.VERSION_CODES.P} and after, any value of length is valid. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the queueing operation succeeded |

### setClientData

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setClientData(data: Any!): Unit
```

Sets the client data for the request. This can be used in conjunction with [getClientData](https://developer.android.com/reference/kotlin/android/hardware/usb/UsbRequest#getClientData())to associate another object with this request, which can be useful for maintaining state between calls to #queue and android.hardware.usb.UsbDeviceConnection#requestWait

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------|
| `data` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the client data for the request |

## Protected methods

### finalize

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun finalize(): Unit
```

| Exceptions ||
|-----------------------|-------------------------------------|
| `java.lang.Throwable` | the`Exception`raised by this method |
