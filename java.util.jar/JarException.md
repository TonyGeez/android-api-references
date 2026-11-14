# JarException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# JarException

```
open class JarException : ZipException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||||
| | | ↳ | [java.io.IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.util.zip.ZipException](https://developer.android.com/reference/kotlin/java/util/zip/ZipException.html#) ||
| | | | | ↳ | [java.util.jar.JarException](https://developer.android.com/reference/kotlin/java/util/jar/JarException#) |

Signals that an error of some sort has occurred while reading from or writing to a JAR file.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [JarException](https://developer.android.com/reference/kotlin/java/util/jar/JarException#JarException())`()` Constructs a JarException with no detail message. |
| [JarException](https://developer.android.com/reference/kotlin/java/util/jar/JarException#JarException(kotlin.String))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a JarException with the specified detail message. |

## Public constructors

### JarException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
JarException()
```

Constructs a JarException with no detail message. 

### JarException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
JarException(s: String!)
```

Constructs a JarException with the specified detail message.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message |
