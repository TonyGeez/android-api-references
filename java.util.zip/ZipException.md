# ZipException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ZipException

```
open class ZipException : IOException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) |||
| | | ↳ | [java.io.IOException](../java.io/IOException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.util.zip.ZipException](ZipException.md) |

| Known Direct Subclasses [JarException](../java.util.jar/JarException.md) |-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------| | [JarException](../java.util.jar/JarException.md) | Signals that an error of some sort has occurred while reading from or writing to a JAR file. | |
| --- | --- | --- | --- | --- | --- | --- |

Signals that a Zip exception of some sort has occurred.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ZipException](ZipException.md))`()` Constructs a`ZipException`with`null`as its error detail message. |
| [ZipException](ZipException.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a`ZipException`with the specified detail message. |

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
