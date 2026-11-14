# ICUUncheckedIOException

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ICUUncheckedIOException

Kotlin| [Java](https://developer.android.com/reference/android/icu/util/ICUUncheckedIOException "View this page in Java") 
| --- | --- |

```
open class ICUUncheckedIOException : RuntimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [android.icu.util.ICUUncheckedIOException](https://developer.android.com/reference/kotlin/android/icu/util/ICUUncheckedIOException#) |

Unchecked version of [java.io.IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#). Some ICU APIs do not throw the standard exception but instead wrap it into this unchecked version.

This currently extends [RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#), but when ICU can rely on Java 8 this class should be changed to extend java.io.UncheckedIOException instead.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ICUUncheckedIOException](https://developer.android.com/reference/kotlin/android/icu/util/ICUUncheckedIOException#ICUUncheckedIOException())`()` Default constructor. |
| [ICUUncheckedIOException](https://developer.android.com/reference/kotlin/android/icu/util/ICUUncheckedIOException#ICUUncheckedIOException(kotlin.String))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructor. |
| [ICUUncheckedIOException](https://developer.android.com/reference/kotlin/android/icu/util/ICUUncheckedIOException#ICUUncheckedIOException(kotlin.String,%20kotlin.Throwable))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructor. |
| [ICUUncheckedIOException](https://developer.android.com/reference/kotlin/android/icu/util/ICUUncheckedIOException#ICUUncheckedIOException(kotlin.Throwable))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructor. |

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
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:original exception (normally a [java.io.IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#)) |

### ICUUncheckedIOException

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ICUUncheckedIOException(cause: Throwable!)
```

Constructor.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:original exception (normally a [java.io.IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#)) |
