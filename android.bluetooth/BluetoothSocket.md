# BluetoothSocket

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BluetoothSocket

Kotlin| [Java](../android/bluetooth/BluetoothSocket.md) 
| --- | --- |

```
class BluetoothSocket : Closeable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.bluetooth.BluetoothSocket](../android/bluetooth/BluetoothSocket.md) |

A connected or connecting Bluetooth socket.

The interface for Bluetooth Sockets is similar to that of TCP sockets: [java.net.Socket](../java/net/Socket.md) and [java.net.ServerSocket](../java/net/ServerSocket.md). On the server side, use a [BluetoothServerSocket](../android/bluetooth/BluetoothServerSocket.md) to create a listening server socket. When a connection is accepted by the [BluetoothServerSocket](../android/bluetooth/BluetoothServerSocket.md), it will return a new [BluetoothSocket](../android/bluetooth/BluetoothSocket.md) to manage the connection. On the client side, use a single [BluetoothSocket](../android/bluetooth/BluetoothSocket.md) to both initiate an outgoing connection and to manage the connection.

The most common type of Bluetooth socket is RFCOMM, which is the type supported by the Android APIs. RFCOMM is a connection-oriented, streaming transport over Bluetooth. It is also known as the Serial Port Profile (SPP).

To create a [BluetoothSocket](../android/bluetooth/BluetoothSocket.md) for connecting to a known device, use [BluetoothDevice.createRfcommSocketToServiceRecord()](../android/bluetooth/BluetoothDevice.md)). Then call [connect()](../android/bluetooth/BluetoothSocket.md))to attempt a connection to the remote device. This call will block until a connection is established or the connection fails.

To create a [BluetoothSocket](../android/bluetooth/BluetoothSocket.md) as a server (or "host"), see the [BluetoothServerSocket](../android/bluetooth/BluetoothServerSocket.md) documentation.

Once the socket is connected, whether initiated as a client or accepted as a server, open the IO streams by calling [getInputStream](../android/bluetooth/BluetoothSocket.md))and [getOutputStream](../android/bluetooth/BluetoothSocket.md))in order to retrieve [java.io.InputStream](../java/io/InputStream.md) and [java.io.OutputStream](../java/io/OutputStream.md) objects, respectively, which are automatically connected to the socket.

[BluetoothSocket](../android/bluetooth/BluetoothSocket.md) is thread safe. In particular, #close will always immediately abort ongoing operations and close the socket.

<br />

| ### Developer Guides
|
| For more information about using Bluetooth, read the [Bluetooth](https://developer.android.com/guide/topics/connectivity/bluetooth.html) developer guide.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_L2CAP](../android/bluetooth/BluetoothSocket.md) L2CAP socket |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_LE](../android/bluetooth/BluetoothSocket.md) L2CAP socket on LE transport |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_RFCOMM](../android/bluetooth/BluetoothSocket.md) RFCOMM socket |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_SCO](../android/bluetooth/BluetoothSocket.md) SCO socket |

| Public methods ||
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](../android/bluetooth/BluetoothSocket.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [connect](../android/bluetooth/BluetoothSocket.md))`()` Attempt to connect to a remote device. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getConnectionType](../android/bluetooth/BluetoothSocket.md))`()` Get the type of the underlying connection. |
| --- | --- |
| [InputStream](../java/io/InputStream.md)! | [getInputStream](../android/bluetooth/BluetoothSocket.md))`()` Get the input stream associated with this socket. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxReceivePacketSize](../android/bluetooth/BluetoothSocket.md))`()` Get the maximum supported Receive packet size for the underlying transport. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxTransmitPacketSize](../android/bluetooth/BluetoothSocket.md))`()` Get the maximum supported Transmit packet size for the underlying transport. |
| --- | --- |
| [OutputStream](../java/io/OutputStream.md)! | [getOutputStream](../android/bluetooth/BluetoothSocket.md))`()` Get the output stream associated with this socket. |
| [BluetoothDevice](../android/bluetooth/BluetoothDevice.md)! | [getRemoteDevice](../android/bluetooth/BluetoothSocket.md))`()` Get the remote device this socket is connecting, or connected, to. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isConnected](../android/bluetooth/BluetoothSocket.md))`()` Get the connection status of this socket, ie, whether there is an active connection with remote device. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/bluetooth/BluetoothSocket.md))`()` <br /> |

## Constants

### TYPE_L2CAP

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_L2CAP: Int
```

L2CAP socket 

 Value: 3

### TYPE_LE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_LE: Int
```

L2CAP socket on LE transport 

 Value: 4

### TYPE_RFCOMM

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_RFCOMM: Int
```

RFCOMM socket 

 Value: 1

### TYPE_SCO

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_SCO: Int
```

SCO socket 

 Value: 2

## Public methods

### close

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun close(): Unit
```

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | if an I/O error occurs |

### connect

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun connect(): Unit
```

Attempt to connect to a remote device.

This method will block until a connection is made or the connection fails. If this method returns without an exception then this socket is now connected.

Creating new connections to remote Bluetooth devices should not be attempted while device discovery is in progress. Device discovery is a heavyweight procedure on the Bluetooth adapter and will significantly slow a device connection. Use [android.bluetooth.BluetoothAdapter#cancelDiscovery()](../android/bluetooth/BluetoothAdapter.md))to cancel an ongoing discovery. Discovery is not managed by the Activity, but is run as a system service, so an application should always call [android.bluetooth.BluetoothAdapter#cancelDiscovery()](../android/bluetooth/BluetoothAdapter.md))even if it did not directly request a discovery, just to be sure.

close can be used to abort this call from another thread.

Requires the [android.Manifest.permission#BLUETOOTH_PRIVILEGED](../android/Manifest.permission.md) permission only when`mDataPath`is different from android.bluetooth.BluetoothSocketSettings#DATA_PATH_NO_OFFLOAD. 
For apps targeting [Build.VERSION_CODES.S](../android/os/Build.VERSION_CODES.md) or or higher, this requires the [Manifest.permission.BLUETOOTH_CONNECT](../android/Manifest.permission.md) permission which can be gained with[android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)).

| Exceptions ||
|----------------------------------------------|--------------------------------------------------------|
| `android.bluetooth.BluetoothSocketException` | in case of failure, with the corresponding error code. |
| `java.io.IOException` | for other errors (eg: InputStream read failures etc.). |

### getConnectionType

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getConnectionType(): Int
```

Get the type of the underlying connection.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | one of [TYPE_RFCOMM](../android/bluetooth/BluetoothSocket.md), [TYPE_SCO](../android/bluetooth/BluetoothSocket.md) or [TYPE_L2CAP](../android/bluetooth/BluetoothSocket.md) |

### getInputStream

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getInputStream(): InputStream!
```

Get the input stream associated with this socket.

The input stream will be returned even if the socket is not yet connected, but operations on that stream will throw IOException until the associated socket is connected.

| Return ||
|------------------------------------------------------------------------------------------|-------------|
| [InputStream](../java/io/InputStream.md)! | InputStream |

### getMaxReceivePacketSize

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMaxReceivePacketSize(): Int
```

Get the maximum supported Receive packet size for the underlying transport. Use this to optimize the reads done on the input stream, as any call to read will return a maximum of this amount of bytes - or for some transports a multiple of this value.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the maximum supported Receive packet size for the underlying transport. |

### getMaxTransmitPacketSize

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMaxTransmitPacketSize(): Int
```

Get the maximum supported Transmit packet size for the underlying transport. Use this to optimize the writes done to the output socket, to avoid sending half full packets.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the maximum supported Transmit packet size for the underlying transport. |

### getOutputStream

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getOutputStream(): OutputStream!
```

Get the output stream associated with this socket.

The output stream will be returned even if the socket is not yet connected, but operations on that stream will throw IOException until the associated socket is connected.

| Return ||
|--------------------------------------------------------------------------------------------|--------------|
| [OutputStream](../java/io/OutputStream.md)! | OutputStream |

### getRemoteDevice

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRemoteDevice(): BluetoothDevice!
```

Get the remote device this socket is connecting, or connected, to.

| Return ||
|------------------------------------------------------------------------------------------------------|---------------|
| [BluetoothDevice](../android/bluetooth/BluetoothDevice.md)! | remote device |

### isConnected

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isConnected(): Boolean
```

Get the connection status of this socket, ie, whether there is an active connection with remote device.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if connected false if not connected |

### toString

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |
