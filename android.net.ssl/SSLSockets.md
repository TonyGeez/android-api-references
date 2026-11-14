Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SSLSockets

```
open class SSLSockets
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.ssl.SSLSockets](SSLSockets.md) |

Static utility methods for accessing additional functionality of supported instances of `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket.html#`. Sockets from the platform TLS provider will be compatible with all methods in this class.

## Summary

| Public methods ||
|---|---|
| open static [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | `https://developer.android.com/reference/kotlin/android/net/ssl/SSLSockets#exportKeyingMaterial(javax.net.ssl.SSLSocket,%20kotlin.String,%20kotlin.ByteArray,%20kotlin.Int)(socket: https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket.html#, label: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, context: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html?, length: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Exports a value derived from the TLS master secret as described in RFC 5705. |
| open static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/ssl/SSLSockets#isSupportedSocket(javax.net.ssl.SSLSocket)(socket: https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket.html#)` Returns whether the given socket can be used with the methods in this class. |
| open static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/ssl/SSLSockets#setEchConfigList(javax.net.ssl.SSLSocket,%20android.net.ssl.EchConfigList)(socket: https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket.html#, echConfigList: https://developer.android.com/reference/kotlin/android/net/ssl/EchConfigList)` Sets an EchConfigList to be used to establish ECH on the TLS handshake. |
| --- | --- |
| open static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/ssl/SSLSockets#setUseSessionTickets(javax.net.ssl.SSLSocket,%20kotlin.Boolean)(socket: https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocket.html#, useSessionTickets: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Enables or disables the use of session tickets. |

## Public methods

### exportKeyingMaterial

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun exportKeyingMaterial(
    socket: SSLSocket, 
    label: String, 
    context: ByteArray?, 
    length: Int
): ByteArray?
```

Exports a value derived from the TLS master secret as described in RFC 5705. A number of protocols leverage Transport Layer Security (TLS) to perform key establishment but then use some of the keying material for their own purposes. This method allows an application to export keying material from a TLS connection. The exported material will be the same on the client and server if they pass in the same values for `label` and `context`. See RFC 5705 for further details.

| Parameters ||
|---|---|
| `socket` | [SSLSocket](../javax.net.ssl/SSLSocket.md): the socket to use for exporting keying material. This value cannot be `null`. |
| `label` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): the label to use in calculating the exported value. This must be an ASCII-only string. This value cannot be `null`. |
| `context` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?: the application-specific context value to use in calculating the exported value. This may be `null` to use no application context, which is treated differently than an empty byte array. |
| --- | --- |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the number of bytes of keying material to return. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html?` | a value of the specified length, or `null` if the handshake has not yet completed or the connection has been closed. |

| Exceptions ||
|---|---|
| `javax.net.ssl.SSLException` | if the value could not be exported. |

### isSupportedSocket

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun isSupportedSocket(socket: SSLSocket): Boolean
```

Returns whether the given socket can be used with the methods in this class. In general, only sockets from the platform TLS provider are supported.

| Parameters ||
|---|---|
| `socket` | [SSLSocket](../javax.net.ssl/SSLSocket.md): This value cannot be `null`. |

### setEchConfigList

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [C Extensions 22](https://developer.android.com/sdkExtensions)

```
open static fun setEchConfigList(
    socket: SSLSocket, 
    echConfigList: EchConfigList
): Unit
```

Sets an EchConfigList to be used to establish ECH on the TLS handshake.

This function must be called before the handshake is started or it will have no effect.

| Parameters ||
|---|---|
| `socket` | [SSLSocket](../javax.net.ssl/SSLSocket.md): the socket. This value cannot be `null`. |
| `echConfigList` | [EchConfigList](../android/net/ssl/EchConfigList.md): the ECH config data to be used in the handshake. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the given socket is not a platform socket |

### setUseSessionTickets

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun setUseSessionTickets(
    socket: SSLSocket, 
    useSessionTickets: Boolean
): Unit
```

Enables or disables the use of session tickets.

This function must be called before the handshake is started or it will have no effect.

| Parameters ||
|---|---|
| `socket` | [SSLSocket](../javax.net.ssl/SSLSocket.md): the socket. This value cannot be `null`. |
| `useSessionTickets` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): whether to enable or disable the use of session tickets |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the given socket is not a platform socket |
