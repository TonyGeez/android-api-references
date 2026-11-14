# BluetoothSocket

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BluetoothSocket

Kotlin| [Java](https://developer.android.com/reference/android/bluetooth/BluetoothSocket "View this page in Java") 

```
class BluetoothSocket : Closeable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.bluetooth.BluetoothSocket](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket#) |

A connected or connecting Bluetooth socket.

The interface for Bluetooth Sockets is similar to that of TCP sockets: [java.net.Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#) and [java.net.ServerSocket](https://developer.android.com/reference/kotlin/java/net/ServerSocket.html#). On the server side, use a [BluetoothServerSocket](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothServerSocket) to create a listening server socket. When a connection is accepted by the [BluetoothServerSocket](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothServerSocket), it will return a new [BluetoothSocket](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket#) to manage the connection. On the client side, use a single [BluetoothSocket](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket#) to both initiate an outgoing connection and to manage the connection.

The most common type of Bluetooth socket is RFCOMM, which is the type supported by the Android APIs. RFCOMM is a connection-oriented, streaming transport over Bluetooth. It is also known as the Serial Port Profile (SPP).

To create a [BluetoothSocket](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket#) for connecting to a known device, use [BluetoothDevice.createRfcommSocketToServiceRecord()](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#createRfcommSocketToServiceRecord(java.util.UUID)). Then call [connect()](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket#connect())to attempt a connection to the remote device. This call will block until a connection is established or the connection fails.

To create a [BluetoothSocket](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket#) as a server (or "host"), see the [BluetoothServerSocket](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothServerSocket) documentation.

Once the socket is connected, whether initiated as a client or accepted as a server, open the IO streams by calling [getInputStream](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket#getInputStream())and [getOutputStream](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket#getOutputStream())in order to retrieve [java.io.InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#) and [java.io.OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#) objects, respectively, which are automatically connected to the socket.

[BluetoothSocket](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket#) is thread safe. In particular, #close will always immediately abort ongoing operations and close the socket.

<br />

| ### Developer Guides
|
| For more information about using Bluetooth, read the [Bluetooth](https://developer.android.com/guide/topics/connectivity/bluetooth.html) developer guide.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_L2CAP](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket#TYPE_L2CAP:kotlin.Int) L2CAP socket |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_LE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket#TYPE_LE:kotlin.Int) L2CAP socket on LE transport |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_RFCOMM](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket#TYPE_RFCOMM:kotlin.Int) RFCOMM socket |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_SCO](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket#TYPE_SCO:kotlin.Int) SCO socket |

| Public methods ||
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket#close())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [connect](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket#connect())`()` Attempt to connect to a remote device. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getConnectionType](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket#getConnectionType())`()` Get the type of the underlying connection. |
| [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)! | [getInputStream](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket#getInputStream())`()` Get the input stream associated with this socket. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxReceivePacketSize](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket#getMaxReceivePacketSize())`()` Get the maximum supported Receive packet size for the underlying transport. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxTransmitPacketSize](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket#getMaxTransmitPacketSize())`()` Get the maximum supported Transmit packet size for the underlying transport. |
| [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)! | [getOutputStream](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket#getOutputStream())`()` Get the output stream associated with this socket. |
| [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice)! | [getRemoteDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket#getRemoteDevice())`()` Get the remote device this socket is connecting, or connected, to. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isConnected](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket#isConnected())`()` Get the connection status of this socket, ie, whether there is an active connection with remote device. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket#toString())`()` <br /> |

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

Creating new connections to remote Bluetooth devices should not be attempted while device discovery is in progress. Device discovery is a heavyweight procedure on the Bluetooth adapter and will significantly slow a device connection. Use [android.bluetooth.BluetoothAdapter#cancelDiscovery()](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#cancelDiscovery())to cancel an ongoing discovery. Discovery is not managed by the Activity, but is run as a system service, so an application should always call [android.bluetooth.BluetoothAdapter#cancelDiscovery()](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#cancelDiscovery())even if it did not directly request a discovery, just to be sure.

close can be used to abort this call from another thread.

Requires the [android.Manifest.permission#BLUETOOTH_PRIVILEGED](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_PRIVILEGED:kotlin.String) permission only when`mDataPath`is different from android.bluetooth.BluetoothSocketSettings#DATA_PATH_NO_OFFLOAD. 
For apps targeting [Build.VERSION_CODES.S](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int) or or higher, this requires the [Manifest.permission.BLUETOOTH_CONNECT](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String) permission which can be gained with[android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)).

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | one of [TYPE_RFCOMM](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket#TYPE_RFCOMM:kotlin.Int), [TYPE_SCO](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket#TYPE_SCO:kotlin.Int) or [TYPE_L2CAP](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket#TYPE_L2CAP:kotlin.Int) |

### getInputStream

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getInputStream(): InputStream!
```

Get the input stream associated with this socket.

The input stream will be returned even if the socket is not yet connected, but operations on that stream will throw IOException until the associated socket is connected.

| Return ||
|------------------------------------------------------------------------------------------|-------------|
| [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)! | InputStream |

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
| [OutputStream](https://developer.android.com/reference/kotlin/java/io/OutputStream.html#)! | OutputStream |

### getRemoteDevice

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRemoteDevice(): BluetoothDevice!
```

Get the remote device this socket is connecting, or connected, to.

| Return ||
|------------------------------------------------------------------------------------------------------|---------------|
| [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice)! | remote device |

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
