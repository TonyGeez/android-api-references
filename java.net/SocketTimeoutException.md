# SocketTimeoutException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SocketTimeoutException

```
open class SocketTimeoutException : InterruptedIOException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) ||||
| | | ↳ | [java.io.IOException](../java.io/IOException.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.io.InterruptedIOException](../java.io/InterruptedIOException.md) ||
| | | | | ↳ | [java.net.SocketTimeoutException](SocketTimeoutException.md) |

Signals that a timeout has occurred on a socket read or accept.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SocketTimeoutException](SocketTimeoutException.md))`()` Construct a new SocketTimeoutException with no detailed message. |
| [SocketTimeoutException](SocketTimeoutException.md))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a new SocketTimeoutException with a detail message. |

| Inherited properties ||
|---|---|
| From class [InterruptedIOException](../java.io/InterruptedIOException.md) |----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [bytesTransferred](../java.io/InterruptedIOException.md) <br /> Reports how many bytes had been transferred as part of the I/O operation before it was interrupted. <br /> | ||

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
