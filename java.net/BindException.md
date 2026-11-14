# BindException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BindException

```
open class BindException : SocketException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||||
| | | ↳ | [java.io.IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.net.SocketException](https://developer.android.com/reference/kotlin/java/net/SocketException) ||
| | | | | ↳ | [java.net.BindException](https://developer.android.com/reference/kotlin/java/net/BindException#) |

Signals that an error occurred while attempting to bind a socket to a local address and port. Typically, the port is in use, or the requested local address could not be assigned.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [BindException](https://developer.android.com/reference/kotlin/java/net/BindException#BindException())`()` Construct a new BindException with no detailed message. |
| [BindException](https://developer.android.com/reference/kotlin/java/net/BindException#BindException(kotlin.String))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a new BindException with the specified detail message as to why the bind error occurred. |

## Public constructors

### BindException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BindException()
```

Construct a new BindException with no detailed message. 

### BindException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BindException(msg: String!)
```

Constructs a new BindException with the specified detail message as to why the bind error occurred. A detail message is a String that gives a specific description of this error.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------|
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message |
