# BluetoothServerSocket

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BluetoothServerSocket

Kotlin| [Java](https://developer.android.com/reference/android/bluetooth/BluetoothServerSocket "View this page in Java") 
| --- | --- |

```
class BluetoothServerSocket : Closeable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.bluetooth.BluetoothServerSocket](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothServerSocket#) |

A listening Bluetooth socket.

The interface for Bluetooth Sockets is similar to that of TCP sockets: [java.net.Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#) and [java.net.ServerSocket](https://developer.android.com/reference/kotlin/java/net/ServerSocket.html#). On the server side, use a [BluetoothServerSocket](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothServerSocket#) to create a listening server socket. When a connection is accepted by the [BluetoothServerSocket](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothServerSocket#), it will return a new [BluetoothSocket](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket) to manage the connection. On the client side, use a single [BluetoothSocket](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket) to both initiate an outgoing connection and to manage the connection.

For Bluetooth BR/EDR, the most common type of socket is RFCOMM, which is the type supported by the Android APIs. RFCOMM is a connection-oriented, streaming transport over Bluetooth BR/EDR. It is also known as the Serial Port Profile (SPP). To create a listening [BluetoothServerSocket](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothServerSocket#) that's ready for incoming Bluetooth BR/EDR connections, use [BluetoothAdapter.listenUsingRfcommWithServiceRecord()](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#listenUsingRfcommWithServiceRecord(kotlin.String,%20java.util.UUID)).

For Bluetooth LE, the socket uses LE Connection-oriented Channel (CoC). LE CoC is a connection-oriented, streaming transport over Bluetooth LE and has a credit-based flow control. Correspondingly, use [BluetoothAdapter.listenUsingL2capChannel()](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#listenUsingL2capChannel())to create a listening [BluetoothServerSocket](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothServerSocket#) that's ready for incoming Bluetooth LE CoC connections. For LE CoC, you can use [getPsm()](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothServerSocket#getPsm())to get the protocol/service multiplexer (PSM) value that the peer needs to use to connect to your socket.

After the listening [BluetoothServerSocket](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothServerSocket#) is created, call [accept()](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothServerSocket#accept())to listen for incoming connection requests. This call will block until a connection is established, at which point, it will return a [BluetoothSocket](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket) to manage the connection. Once the [BluetoothSocket](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket) is acquired, it's a good idea to call #close() on the [BluetoothServerSocket](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothServerSocket#) when it's no longer needed for accepting connections. Closing the [BluetoothServerSocket](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothServerSocket#) will*not* close the returned [BluetoothSocket](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket).

[BluetoothServerSocket](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothServerSocket#) is thread safe. In particular, #close will always immediately abort ongoing operations and close the server socket.

<br />

| ### Developer Guides
|
| For more information about using Bluetooth, read the [Bluetooth](https://developer.android.com/guide/topics/connectivity/bluetooth.html) developer guide.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [BluetoothSocket](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket)! | [accept](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothServerSocket#accept())`()` Block until a connection is established. |
| [BluetoothSocket](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket)! | [accept](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothServerSocket#accept(kotlin.Int))`(`timeout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Block until a connection is established, with timeout. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothServerSocket#close())`()` Immediately close this socket, and release all associated resources. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPsm](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothServerSocket#getPsm())`()` Returns the assigned dynamic protocol/service multiplexer (PSM) value for the listening L2CAP Connection-oriented Channel (CoC) server socket. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothServerSocket#toString())`()` <br /> |

## Public methods

### accept

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun accept(): BluetoothSocket!
```

Block until a connection is established.

Returns a connected [BluetoothSocket](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket) on successful connection.

Once this call returns, it can be called again to accept subsequent incoming connections.

close can be used to abort this call from another thread.

| Return ||
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [BluetoothSocket](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket)! | a connected [BluetoothSocket](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket) |

| Exceptions ||
|-----------------------|---------------------------------------------------------|
| `java.io.IOException` | on error, for example this call was aborted, or timeout |

### accept

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun accept(timeout: Int): BluetoothSocket!
```

Block until a connection is established, with timeout.

Returns a connected [BluetoothSocket](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket) on successful connection.

Once this call returns, it can be called again to accept subsequent incoming connections.

close can be used to abort this call from another thread.

| Return ||
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [BluetoothSocket](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket)! | a connected [BluetoothSocket](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket) |

| Exceptions ||
|-----------------------|---------------------------------------------------------|
| `java.io.IOException` | on error, for example this call was aborted, or timeout |

### close

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun close(): Unit
```

Immediately close this socket, and release all associated resources.

Causes blocked calls on this socket in other threads to immediately throw an IOException.

Closing the [BluetoothServerSocket](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothServerSocket#) will*not* close any [BluetoothSocket](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket) received from [accept()](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothServerSocket#accept()).

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | if an I/O error occurs |

### getPsm

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPsm(): Int
```

Returns the assigned dynamic protocol/service multiplexer (PSM) value for the listening L2CAP Connection-oriented Channel (CoC) server socket. This server socket must be returned by the [BluetoothAdapter.listenUsingL2capChannel()](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#listenUsingL2capChannel())or [android.bluetooth.BluetoothAdapter#listenUsingInsecureL2capChannel()](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#listenUsingInsecureL2capChannel()). The returned value is undefined if this method is called on non-L2CAP server sockets.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the assigned PSM or LE_PSM value depending on transport |

### toString

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |
