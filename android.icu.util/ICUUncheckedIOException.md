# ICUUncheckedIOException

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ICUUncheckedIOException

Kotlin| [Java](ICUUncheckedIOException.md) 
| --- | --- |

```
open class ICUUncheckedIOException : RuntimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) |||
| | | ↳ | [java.lang.RuntimeException](../java.lang/RuntimeException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [android.icu.util.ICUUncheckedIOException](ICUUncheckedIOException.md) |

Unchecked version of [java.io.IOException](../java.io/IOException.md). Some ICU APIs do not throw the standard exception but instead wrap it into this unchecked version.

This currently extends [RuntimeException](../java.lang/RuntimeException.md), but when ICU can rely on Java 8 this class should be changed to extend java.io.UncheckedIOException instead.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ICUUncheckedIOException](ICUUncheckedIOException.md))`()` Default constructor. |
| [ICUUncheckedIOException](ICUUncheckedIOException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructor. |
| [ICUUncheckedIOException](ICUUncheckedIOException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructor. |
| [ICUUncheckedIOException](ICUUncheckedIOException.md))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructor. |

## Public constructors

### ICUUncheckedIOException

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ICUUncheckedIOException()
```

Default constructor. 

### ICUUncheckedIOException

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ICUUncheckedIOException(message: String!)
```

Constructor.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:exception message string |

### ICUUncheckedIOException

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ICUUncheckedIOException(
    message: String!, 
    cause: Throwable!)
```

Constructor.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:exception message string |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:original exception (normally a [java.io.IOException](../java.io/IOException.md)) |

### ICUUncheckedIOException

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ICUUncheckedIOException(cause: Throwable!)
```

Constructor.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:original exception (normally a [java.io.IOException](../java.io/IOException.md)) |
