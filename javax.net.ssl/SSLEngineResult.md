# SSLEngineResult

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SSLEngineResult

```
open class SSLEngineResult
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.net.ssl.SSLEngineResult](../javax/net/ssl/SSLEngineResult.md) |

An encapsulation of the result state produced by`SSLEngine`I/O calls.

A`SSLEngine`provides a means for establishing secure communication sessions between two peers.`SSLEngine`operations typically consume bytes from an input buffer and produce bytes in an output buffer. This class provides operational result values describing the state of the`SSLEngine`, including indications of what operations are needed to finish an ongoing handshake. Lastly, it reports the number of bytes consumed and produced as a result of this operation.

## Summary

| Nested classes ||
|---|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [HandshakeStatus](../javax/net/ssl/SSLEngineResult.HandshakeStatus.md) An`SSLEngineResult`enum describing the current handshaking state of this`SSLEngine`. |
| | [Status](../javax/net/ssl/SSLEngineResult.Status.md) An`SSLEngineResult`enum describing the overall result of the`SSLEngine`operation. |

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SSLEngineResult](../javax/net/ssl/SSLEngineResult.md))`(`status:` ` [SSLEngineResult.Status](../javax/net/ssl/SSLEngineResult.Status.md)!`, `handshakeStatus:` ` [SSLEngineResult.HandshakeStatus](../javax/net/ssl/SSLEngineResult.HandshakeStatus.md)!`, `bytesConsumed:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bytesProduced:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Initializes a new instance of this class. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [bytesConsumed](../javax/net/ssl/SSLEngineResult.md))`()` Returns the number of bytes consumed from the input buffer. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [bytesProduced](../javax/net/ssl/SSLEngineResult.md))`()` Returns the number of bytes written to the output buffer. |
| [SSLEngineResult.HandshakeStatus](../javax/net/ssl/SSLEngineResult.HandshakeStatus.md)! | [getHandshakeStatus](../javax/net/ssl/SSLEngineResult.md))`()` Gets the handshake status of this`SSLEngine`operation. |
| --- | --- |
| [SSLEngineResult.Status](../javax/net/ssl/SSLEngineResult.Status.md)! | [getStatus](../javax/net/ssl/SSLEngineResult.md))`()` Gets the return value of this`SSLEngine`operation. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../javax/net/ssl/SSLEngineResult.md))`()` Returns a String representation of this object. |

## Public constructors

### SSLEngineResult

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SSLEngineResult(
    status: SSLEngineResult.Status!, 
    handshakeStatus: SSLEngineResult.HandshakeStatus!, 
    bytesConsumed: Int, 
    bytesProduced: Int)
```

Initializes a new instance of this class.

| Parameters ||
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `status` | [SSLEngineResult.Status](../javax/net/ssl/SSLEngineResult.Status.md)!:the return value of the operation. |
| `handshakeStatus` | [SSLEngineResult.HandshakeStatus](../javax/net/ssl/SSLEngineResult.HandshakeStatus.md)!:the current handshaking status. |
| `bytesConsumed` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of bytes consumed from the source ByteBuffer |
| --- | --- |
| `bytesProduced` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of bytes placed into the destination ByteBuffer |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the`status`or`handshakeStatus`arguments are null, or if`bytesConsumed`or`bytesProduced`is negative. |

## Public methods

### bytesConsumed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun bytesConsumed(): Int
```

Returns the number of bytes consumed from the input buffer.

| Return ||
|----------------------------------------------------------------------------|-------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of bytes consumed. |

### bytesProduced

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun bytesProduced(): Int
```

Returns the number of bytes written to the output buffer.

| Return ||
|----------------------------------------------------------------------------|------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of bytes produced |

### getHandshakeStatus

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getHandshakeStatus(): SSLEngineResult.HandshakeStatus!
```

Gets the handshake status of this`SSLEngine`operation.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------|----------------------|
| [SSLEngineResult.HandshakeStatus](../javax/net/ssl/SSLEngineResult.HandshakeStatus.md)! | the handshake status |

### getStatus

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getStatus(): SSLEngineResult.Status!
```

Gets the return value of this`SSLEngine`operation.

| Return ||
|----------------------------------------------------------------------------------------------------------------|------------------|
| [SSLEngineResult.Status](../javax/net/ssl/SSLEngineResult.Status.md)! | the return value |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Returns a String representation of this object.

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |
