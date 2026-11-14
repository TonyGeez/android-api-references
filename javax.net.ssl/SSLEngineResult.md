# SSLEngineResult

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SSLEngineResult

```
open class SSLEngineResult
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [javax.net.ssl.SSLEngineResult](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngineResult#) |

An encapsulation of the result state produced by`SSLEngine`I/O calls.

A`SSLEngine`provides a means for establishing secure communication sessions between two peers.`SSLEngine`operations typically consume bytes from an input buffer and produce bytes in an output buffer. This class provides operational result values describing the state of the`SSLEngine`, including indications of what operations are needed to finish an ongoing handshake. Lastly, it reports the number of bytes consumed and produced as a result of this operation.

## Summary

| Nested classes ||
|---|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [HandshakeStatus](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngineResult.HandshakeStatus) An`SSLEngineResult`enum describing the current handshaking state of this`SSLEngine`. |
| | [Status](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngineResult.Status) An`SSLEngineResult`enum describing the overall result of the`SSLEngine`operation. |

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SSLEngineResult](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngineResult#SSLEngineResult(javax.net.ssl.SSLEngineResult.Status,%20javax.net.ssl.SSLEngineResult.HandshakeStatus,%20kotlin.Int,%20kotlin.Int))`(`status:` ` [SSLEngineResult.Status](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngineResult.Status)!`, `handshakeStatus:` ` [SSLEngineResult.HandshakeStatus](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngineResult.HandshakeStatus)!`, `bytesConsumed:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bytesProduced:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Initializes a new instance of this class. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [bytesConsumed](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngineResult#bytesConsumed())`()` Returns the number of bytes consumed from the input buffer. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [bytesProduced](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngineResult#bytesProduced())`()` Returns the number of bytes written to the output buffer. |
| [SSLEngineResult.HandshakeStatus](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngineResult.HandshakeStatus)! | [getHandshakeStatus](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngineResult#getHandshakeStatus())`()` Gets the handshake status of this`SSLEngine`operation. |
| --- | --- |
| [SSLEngineResult.Status](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngineResult.Status)! | [getStatus](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngineResult#getStatus())`()` Gets the return value of this`SSLEngine`operation. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngineResult#toString())`()` Returns a String representation of this object. |

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
| `status` | [SSLEngineResult.Status](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngineResult.Status)!:the return value of the operation. |
| `handshakeStatus` | [SSLEngineResult.HandshakeStatus](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngineResult.HandshakeStatus)!:the current handshaking status. |
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
| [SSLEngineResult.HandshakeStatus](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngineResult.HandshakeStatus)! | the handshake status |

### getStatus

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getStatus(): SSLEngineResult.Status!
```

Gets the return value of this`SSLEngine`operation.

| Return ||
|----------------------------------------------------------------------------------------------------------------|------------------|
| [SSLEngineResult.Status](https://developer.android.com/reference/kotlin/javax/net/ssl/SSLEngineResult.Status)! | the return value |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Returns a String representation of this object.

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |
