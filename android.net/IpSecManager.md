Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IpSecManager

Kotlin | [Java](https://developer.android.com/reference/android/net/IpSecManager "View this page in Java")
| --- | --- |

```
open class IpSecManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.IpSecManager](https://developer.android.com/reference/kotlin/android/net/IpSecManager#) |

This class contains methods for managing IPsec sessions. Once configured, the kernel will apply confidentiality (encryption) and integrity (authentication) to IP traffic.

Note that not all aspects of IPsec are permitted by this API. Applications may create transport mode security associations and apply them to individual sockets. Applications looking to create an IPsec VPN should use `https://developer.android.com/reference/kotlin/android/net/VpnManager` and `https://developer.android.com/reference/kotlin/android/net/Ikev2VpnProfile`.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/net/IpSecManager.ResourceUnavailableException` Thrown to indicate that an IPsec resource is unavailable. |
| | `https://developer.android.com/reference/kotlin/android/net/IpSecManager.SecurityParameterIndex` This class represents a reserved SPI. |
| | `https://developer.android.com/reference/kotlin/android/net/IpSecManager.SpiUnavailableException` Thrown to indicate that a requested SPI is in use. |
| --- | --- |
| | `https://developer.android.com/reference/kotlin/android/net/IpSecManager.UdpEncapsulationSocket` This class provides access to a UDP encapsulation Socket. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/IpSecManager#DIRECTION_IN:kotlin.Int` Used when applying a transform to direct traffic through an `https://developer.android.com/reference/kotlin/android/net/IpSecTransform` towards the host. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/IpSecManager#DIRECTION_OUT:kotlin.Int` Used when applying a transform to direct traffic through an `https://developer.android.com/reference/kotlin/android/net/IpSecTransform` away from the host. |

| Public methods ||
|---|---|
| open [IpSecManager.SecurityParameterIndex](https://developer.android.com/reference/kotlin/android/net/IpSecManager.SecurityParameterIndex) | `https://developer.android.com/reference/kotlin/android/net/IpSecManager#allocateSecurityParameterIndex(java.net.InetAddress)(destinationAddress: https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)` Reserve a random SPI for traffic bound to or from the specified destination address. |
| open [IpSecManager.SecurityParameterIndex](https://developer.android.com/reference/kotlin/android/net/IpSecManager.SecurityParameterIndex) | `https://developer.android.com/reference/kotlin/android/net/IpSecManager#allocateSecurityParameterIndex(java.net.InetAddress,%20kotlin.Int)(destinationAddress: https://developer.android.com/reference/kotlin/java/net/InetAddress.html#, requestedSpi: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Reserve the requested SPI for traffic bound to or from the specified destination address. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/IpSecManager#applyTransportModeTransform(java.io.FileDescriptor,%20kotlin.Int,%20android.net.IpSecTransform)(socket: https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#, direction: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, transform: https://developer.android.com/reference/kotlin/android/net/IpSecTransform)` Apply an IPsec transform to a socket. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/IpSecManager#applyTransportModeTransform(java.net.DatagramSocket,%20kotlin.Int,%20android.net.IpSecTransform)(socket: https://developer.android.com/reference/kotlin/java/net/DatagramSocket.html#, direction: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, transform: https://developer.android.com/reference/kotlin/android/net/IpSecTransform)` Apply an IPsec transform to a datagram socket. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/IpSecManager#applyTransportModeTransform(java.net.Socket,%20kotlin.Int,%20android.net.IpSecTransform)(socket: https://developer.android.com/reference/kotlin/java/net/Socket.html#, direction: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, transform: https://developer.android.com/reference/kotlin/android/net/IpSecTransform)` Apply an IPsec transform to a stream socket. |
| open [IpSecManager.UdpEncapsulationSocket](https://developer.android.com/reference/kotlin/android/net/IpSecManager.UdpEncapsulationSocket) | `https://developer.android.com/reference/kotlin/android/net/IpSecManager#openUdpEncapsulationSocket()()` Open a socket for UDP encapsulation. |
| --- | --- |
| open [IpSecManager.UdpEncapsulationSocket](https://developer.android.com/reference/kotlin/android/net/IpSecManager.UdpEncapsulationSocket) | `https://developer.android.com/reference/kotlin/android/net/IpSecManager#openUdpEncapsulationSocket(kotlin.Int)(port: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Open a socket for UDP encapsulation and bind to the given port. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/IpSecManager#removeTransportModeTransforms(java.io.FileDescriptor)(socket: https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#)` Remove an IPsec transform from a socket. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/IpSecManager#removeTransportModeTransforms(java.net.DatagramSocket)(socket: https://developer.android.com/reference/kotlin/java/net/DatagramSocket.html#)` Remove an IPsec transform from a datagram socket. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/IpSecManager#removeTransportModeTransforms(java.net.Socket)(socket: https://developer.android.com/reference/kotlin/java/net/Socket.html#)` Remove an IPsec transform from a stream socket. |

## Constants

### DIRECTION_IN

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DIRECTION_IN: Int
```

Used when applying a transform to direct traffic through an `https://developer.android.com/reference/kotlin/android/net/IpSecTransform` towards the host.

See `https://developer.android.com/reference/kotlin/android/net/IpSecManager#applyTransportModeTransform(java.net.Socket,%20kotlin.Int,%20android.net.IpSecTransform)`.

 Value: 0

### DIRECTION_OUT

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DIRECTION_OUT: Int
```

Used when applying a transform to direct traffic through an `https://developer.android.com/reference/kotlin/android/net/IpSecTransform` away from the host.

See `https://developer.android.com/reference/kotlin/android/net/IpSecManager#applyTransportModeTransform(java.net.Socket,%20kotlin.Int,%20android.net.IpSecTransform)`.

 Value: 1

## Public methods

### allocateSecurityParameterIndex

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun allocateSecurityParameterIndex(destinationAddress: InetAddress): IpSecManager.SecurityParameterIndex
```

Reserve a random SPI for traffic bound to or from the specified destination address.

If successful, this SPI is guaranteed available until released by a call to `https://developer.android.com/reference/kotlin/android/net/IpSecManager.SecurityParameterIndex#close()`.

| Parameters ||
|---|---|
| `destinationAddress` | [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#): the destination address for traffic bearing the requested SPI. For inbound traffic, the destination should be an address currently assigned on-device. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/IpSecManager.SecurityParameterIndex` | the reserved SecurityParameterIndex. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.net.IpSecManager.ResourceUnavailableException` | indicating that too many SPIs are currently allocated for this user |

### allocateSecurityParameterIndex

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun allocateSecurityParameterIndex(
    destinationAddress: InetAddress, 
    requestedSpi: Int
): IpSecManager.SecurityParameterIndex
```

Reserve the requested SPI for traffic bound to or from the specified destination address.

If successful, this SPI is guaranteed available until released by a call to `https://developer.android.com/reference/kotlin/android/net/IpSecManager.SecurityParameterIndex#close()`.

| Parameters ||
|---|---|
| `destinationAddress` | [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#): the destination address for traffic bearing the requested SPI. For inbound traffic, the destination should be an address currently assigned on-device. This value cannot be `null`. |
| `requestedSpi` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the requested SPI. The range 1-255 is reserved and may not be used. See RFC 4303 Section 2.1. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/IpSecManager.SecurityParameterIndex` | the reserved SecurityParameterIndex. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.net.IpSecManager.ResourceUnavailableException` | indicating that too many SPIs are currently allocated for this user |
| `android.net.IpSecManager.SpiUnavailableException` | indicating that the requested SPI could not be reserved |

### applyTransportModeTransform

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun applyTransportModeTransform(
    socket: FileDescriptor, 
    direction: Int, 
    transform: IpSecTransform
): Unit
```

Apply an IPsec transform to a socket.

This applies transport mode encapsulation to the given socket. Once applied, I/O on the socket will be encapsulated according to the parameters of the `IpSecTransform`. When the transform is removed from the socket by calling #removeTransportModeTransforms, unprotected traffic can resume on that socket.

For security reasons, the destination address of any traffic on the socket must match the remote `InetAddress` of the `IpSecTransform`. Attempts to send traffic to any other IP address will result in an IOException. In addition, reads and writes on the socket will throw IOException if the user deactivates the transform (by calling `https://developer.android.com/reference/kotlin/android/net/IpSecTransform#close()`) without calling #removeTransportModeTransforms.

Note that when applied to TCP sockets, calling `https://developer.android.com/reference/kotlin/android/net/IpSecTransform#close()` on an applied transform before completion of graceful shutdown may result in the shutdown sequence failing to complete. As such, applications requiring graceful shutdown MUST close the socket prior to deactivating the applied transform. Socket closure may be performed asynchronously (in batches), so the returning of a close function does not guarantee shutdown of a socket. Setting an SO_LINGER timeout results in socket closure being performed synchronously, and is sufficient to ensure shutdown. Specifically, if the transform is deactivated (by calling `https://developer.android.com/reference/kotlin/android/net/IpSecTransform#close()`), prior to the socket being closed, the standard \[FIN - FIN/ACK - ACK\], or the reset \[RST\] packets are dropped due to the lack of a valid Transform. Similarly, if a socket without the SO_LINGER option set is closed, the delayed/batched FIN packets may be dropped.

#### Rekey Procedure

When applying a new tranform to a socket in the outbound direction, the previous transform will be removed and the new transform will take effect immediately, sending all traffic on the new transform; however, when applying a transform in the inbound direction, traffic on the old transform will continue to be decrypted and delivered until that transform is deallocated by calling `https://developer.android.com/reference/kotlin/android/net/IpSecTransform#close()`. This overlap allows lossless rekey procedures where both transforms are valid until both endpoints are using the new transform and all in-flight packets have been received.

| Parameters ||
|---|---|
| `socket` | [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#): a socket file descriptor. This value cannot be `null`. |
| `direction` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the direction in which the transform should be applied. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/net/IpSecManager#DIRECTION_IN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/IpSecManager#DIRECTION_OUT:kotlin.Int` |
| `transform` | [IpSecTransform](https://developer.android.com/reference/kotlin/android/net/IpSecTransform): a transport mode `IpSecTransform` This value cannot be `null`. |
| --- | --- |

| Exceptions ||
|---|---|
| `java.io.IOException` | indicating that the transform could not be applied |

### applyTransportModeTransform

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun applyTransportModeTransform(
    socket: DatagramSocket, 
    direction: Int, 
    transform: IpSecTransform
): Unit
```

Apply an IPsec transform to a datagram socket.

This applies transport mode encapsulation to the given socket. Once applied, I/O on the socket will be encapsulated according to the parameters of the `IpSecTransform`. When the transform is removed from the socket by calling #removeTransportModeTransforms, unprotected traffic can resume on that socket.

For security reasons, the destination address of any traffic on the socket must match the remote `InetAddress` of the `IpSecTransform`. Attempts to send traffic to any other IP address will result in an IOException. In addition, reads and writes on the socket will throw IOException if the user deactivates the transform (by calling `https://developer.android.com/reference/kotlin/android/net/IpSecTransform#close()`) without calling #removeTransportModeTransforms.

#### Rekey Procedure

When applying a new tranform to a socket in the outbound direction, the previous transform will be removed and the new transform will take effect immediately, sending all traffic on the new transform; however, when applying a transform in the inbound direction, traffic on the old transform will continue to be decrypted and delivered until that transform is deallocated by calling `https://developer.android.com/reference/kotlin/android/net/IpSecTransform#close()`. This overlap allows lossless rekey procedures where both transforms are valid until both endpoints are using the new transform and all in-flight packets have been received.

| Parameters ||
|---|---|
| `socket` | [DatagramSocket](https://developer.android.com/reference/kotlin/java/net/DatagramSocket.html#): a datagram socket. This value cannot be `null`. |
| `direction` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the direction in which the transform should be applied. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/net/IpSecManager#DIRECTION_IN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/IpSecManager#DIRECTION_OUT:kotlin.Int` |
| `transform` | [IpSecTransform](https://developer.android.com/reference/kotlin/android/net/IpSecTransform): a transport mode `IpSecTransform` This value cannot be `null`. |
| --- | --- |

| Exceptions ||
|---|---|
| `java.io.IOException` | indicating that the transform could not be applied |

### applyTransportModeTransform

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun applyTransportModeTransform(
    socket: Socket, 
    direction: Int, 
    transform: IpSecTransform
): Unit
```

Apply an IPsec transform to a stream socket.

This applies transport mode encapsulation to the given socket. Once applied, I/O on the socket will be encapsulated according to the parameters of the `IpSecTransform`. When the transform is removed from the socket by calling #removeTransportModeTransforms, unprotected traffic can resume on that socket.

For security reasons, the destination address of any traffic on the socket must match the remote `InetAddress` of the `IpSecTransform`. Attempts to send traffic to any other IP address will result in an IOException. In addition, reads and writes on the socket will throw IOException if the user deactivates the transform (by calling `https://developer.android.com/reference/kotlin/android/net/IpSecTransform#close()`) without calling #removeTransportModeTransforms.

Note that when applied to TCP sockets, calling `https://developer.android.com/reference/kotlin/android/net/IpSecTransform#close()` on an applied transform before completion of graceful shutdown may result in the shutdown sequence failing to complete. As such, applications requiring graceful shutdown MUST close the socket prior to deactivating the applied transform. Socket closure may be performed asynchronously (in batches), so the returning of a close function does not guarantee shutdown of a socket. Setting an SO_LINGER timeout results in socket closure being performed synchronously, and is sufficient to ensure shutdown. Specifically, if the transform is deactivated (by calling `https://developer.android.com/reference/kotlin/android/net/IpSecTransform#close()`), prior to the socket being closed, the standard \[FIN - FIN/ACK - ACK\], or the reset \[RST\] packets are dropped due to the lack of a valid Transform. Similarly, if a socket without the SO_LINGER option set is closed, the delayed/batched FIN packets may be dropped.

#### Rekey Procedure

When applying a new tranform to a socket in the outbound direction, the previous transform will be removed and the new transform will take effect immediately, sending all traffic on the new transform; however, when applying a transform in the inbound direction, traffic on the old transform will continue to be decrypted and delivered until that transform is deallocated by calling `https://developer.android.com/reference/kotlin/android/net/IpSecTransform#close()`. This overlap allows lossless rekey procedures where both transforms are valid until both endpoints are using the new transform and all in-flight packets have been received.

| Parameters ||
|---|---|
| `socket` | [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#): a stream socket. This value cannot be `null`. |
| `direction` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the direction in which the transform should be applied. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/net/IpSecManager#DIRECTION_IN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/IpSecManager#DIRECTION_OUT:kotlin.Int` |
| `transform` | [IpSecTransform](https://developer.android.com/reference/kotlin/android/net/IpSecTransform): a transport mode `IpSecTransform` This value cannot be `null`. |
| --- | --- |

| Exceptions ||
|---|---|
| `java.io.IOException` | indicating that the transform could not be applied |

### openUdpEncapsulationSocket

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun openUdpEncapsulationSocket(): IpSecManager.UdpEncapsulationSocket
```

Open a socket for UDP encapsulation.

See `https://developer.android.com/reference/kotlin/android/net/IpSecManager.UdpEncapsulationSocket` for the proper way to close the returned socket.

The local port of the returned socket can be obtained by calling `https://developer.android.com/reference/kotlin/android/net/IpSecManager.UdpEncapsulationSocket#getPort()`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/IpSecManager.UdpEncapsulationSocket` | a socket that is bound to a local port. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.net.IpSecManager.ResourceUnavailableException` | indicating that too many encapsulation sockets are open |
| `java.io.IOException` | indicating that the socket could not be opened or bound |

### openUdpEncapsulationSocket

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun openUdpEncapsulationSocket(port: Int): IpSecManager.UdpEncapsulationSocket
```

Open a socket for UDP encapsulation and bind to the given port.

See `https://developer.android.com/reference/kotlin/android/net/IpSecManager.UdpEncapsulationSocket` for the proper way to close the returned socket.

| Parameters ||
|---|---|
| `port` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): a local UDP port |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/IpSecManager.UdpEncapsulationSocket` | a socket that is bound to the given port. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.net.IpSecManager.ResourceUnavailableException` | indicating that too many encapsulation sockets are open |
| `java.io.IOException` | indicating that the socket could not be opened or bound |

### removeTransportModeTransforms

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeTransportModeTransforms(socket: FileDescriptor): Unit
```

Remove an IPsec transform from a socket.

Once removed, traffic on the socket will not be encrypted. Removing transforms from a socket allows the socket to be reused for communication in the clear.

If an `IpSecTransform` object applied to this socket was deallocated by calling `https://developer.android.com/reference/kotlin/android/net/IpSecTransform#close()`, then communication on the socket will fail until this method is called.

| Parameters ||
|---|---|
| `socket` | [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#): a socket that previously had a transform applied to it. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.io.IOException` | indicating that the transform could not be removed from the socket |

### removeTransportModeTransforms

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeTransportModeTransforms(socket: DatagramSocket): Unit
```

Remove an IPsec transform from a datagram socket.

Once removed, traffic on the socket will not be encrypted. Removing transforms from a socket allows the socket to be reused for communication in the clear.

If an `IpSecTransform` object applied to this socket was deallocated by calling `https://developer.android.com/reference/kotlin/android/net/IpSecTransform#close()`, then communication on the socket will fail until this method is called.

| Parameters ||
|---|---|
| `socket` | [DatagramSocket](https://developer.android.com/reference/kotlin/java/net/DatagramSocket.html#): a socket that previously had a transform applied to it. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.io.IOException` | indicating that the transform could not be removed from the socket |

### removeTransportModeTransforms

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeTransportModeTransforms(socket: Socket): Unit
```

Remove an IPsec transform from a stream socket.

Once removed, traffic on the socket will not be encrypted. Removing transforms from a socket allows the socket to be reused for communication in the clear.

If an `IpSecTransform` object applied to this socket was deallocated by calling `https://developer.android.com/reference/kotlin/android/net/IpSecTransform#close()`, then communication on the socket will fail until this method is called.

| Parameters ||
|---|---|
| `socket` | [Socket](https://developer.android.com/reference/kotlin/java/net/Socket.html#): a socket that previously had a transform applied to it. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.io.IOException` | indicating that the transform could not be removed from the socket |
