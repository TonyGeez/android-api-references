# ZipException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ZipException

```
open class ZipException : IOException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [java.io.IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#) ||
| | | | ↳ | [java.util.zip.ZipException](https://developer.android.com/reference/kotlin/java/util/zip/ZipException#) |

| Known Direct Subclasses [JarException](https://developer.android.com/reference/kotlin/java/util/jar/JarException.html#) |-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------| | [JarException](https://developer.android.com/reference/kotlin/java/util/jar/JarException.html#) | Signals that an error of some sort has occurred while reading from or writing to a JAR file. | |

Signals that a Zip exception of some sort has occurred.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ZipException](https://developer.android.com/reference/kotlin/java/util/zip/ZipException#ZipException())`()` Constructs a`ZipException`with`null`as its error detail message. |
| [ZipException](https://developer.android.com/reference/kotlin/java/util/zip/ZipException#ZipException(kotlin.String))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a`ZipException`with the specified detail message. |

## Public constructors

### ZipException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ZipException()
```

Constructs a`ZipException`with`null`as its error detail message. 

### ZipException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ZipException(s: String!)
```

Constructs a`ZipException`with the specified detail message.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. |
