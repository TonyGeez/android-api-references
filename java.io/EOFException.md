# EOFException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EOFException

```
open class EOFException : IOException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [java.io.IOException](https://developer.android.com/reference/kotlin/java/io/IOException) ||
| | | | ↳ | [java.io.EOFException](https://developer.android.com/reference/kotlin/java/io/EOFException#) |

Signals that an end of file or end of stream has been reached unexpectedly during input.

This exception is mainly used by data input streams to signal end of stream. Note that many other input operations return a special value on end of stream rather than throwing an exception.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [EOFException](https://developer.android.com/reference/kotlin/java/io/EOFException#EOFException())`()` Constructs an`EOFException`with`null`as its error detail message. |
| [EOFException](https://developer.android.com/reference/kotlin/java/io/EOFException#EOFException(kotlin.String))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an`EOFException`with the specified detail message. |

## Public constructors

### EOFException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
EOFException()
```

Constructs an`EOFException`with`null`as its error detail message. 

### EOFException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
EOFException(s: String!)
```

Constructs an`EOFException`with the specified detail message. The string`s`may later be retrieved by the [java.lang.Throwable#getMessage](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#getMessage())method of class`java.lang.Throwable`.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. |
