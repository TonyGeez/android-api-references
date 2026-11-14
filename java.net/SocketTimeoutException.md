# SocketTimeoutException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SocketTimeoutException

```
open class SocketTimeoutException : InterruptedIOException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||||
| | | ↳ | [java.io.IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.io.InterruptedIOException](https://developer.android.com/reference/kotlin/java/io/InterruptedIOException.html#) ||
| | | | | ↳ | [java.net.SocketTimeoutException](https://developer.android.com/reference/kotlin/java/net/SocketTimeoutException#) |

Signals that a timeout has occurred on a socket read or accept.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SocketTimeoutException](https://developer.android.com/reference/kotlin/java/net/SocketTimeoutException#SocketTimeoutException())`()` Construct a new SocketTimeoutException with no detailed message. |
| [SocketTimeoutException](https://developer.android.com/reference/kotlin/java/net/SocketTimeoutException#SocketTimeoutException(kotlin.String))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a new SocketTimeoutException with a detail message. |

| Inherited properties ||
|---|---|
| From class [InterruptedIOException](https://developer.android.com/reference/kotlin/java/io/InterruptedIOException.html#) |----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [bytesTransferred](https://developer.android.com/reference/kotlin/java/io/InterruptedIOException.html#bytesTransferred:kotlin.Int) <br /> Reports how many bytes had been transferred as part of the I/O operation before it was interrupted. <br /> | ||

## Public constructors

### SocketTimeoutException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SocketTimeoutException()
```

Construct a new SocketTimeoutException with no detailed message. 

### SocketTimeoutException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SocketTimeoutException(msg: String!)
```

Constructs a new SocketTimeoutException with a detail message.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------|
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message |
