# IllformedLocaleException

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IllformedLocaleException

```
open class IllformedLocaleException : RuntimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.util.IllformedLocaleException](https://developer.android.com/reference/kotlin/java/util/IllformedLocaleException#) |

Thrown by methods in [Locale](https://developer.android.com/reference/kotlin/java/util/Locale) and [Locale.Builder](https://developer.android.com/reference/kotlin/java/util/Locale.Builder) to indicate that an argument is not a well-formed BCP 47 tag.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [IllformedLocaleException](https://developer.android.com/reference/kotlin/java/util/IllformedLocaleException#IllformedLocaleException())`()` Constructs a new`IllformedLocaleException`with no detail message and -1 as the error index. |
| [IllformedLocaleException](https://developer.android.com/reference/kotlin/java/util/IllformedLocaleException#IllformedLocaleException(kotlin.String))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a new`IllformedLocaleException`with the given message and -1 as the error index. |
| [IllformedLocaleException](https://developer.android.com/reference/kotlin/java/util/IllformedLocaleException#IllformedLocaleException(kotlin.String,%20kotlin.Int))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `errorIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs a new`IllformedLocaleException`with the given message and the error index. |

| Public methods ||
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getErrorIndex](https://developer.android.com/reference/kotlin/java/util/IllformedLocaleException#getErrorIndex())`()` Returns the index where the error was found. |

## Public constructors

### IllformedLocaleException

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
IllformedLocaleException()
```

Constructs a new`IllformedLocaleException`with no detail message and -1 as the error index. 

### IllformedLocaleException

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
IllformedLocaleException(message: String!)
```

Constructs a new`IllformedLocaleException`with the given message and -1 as the error index.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the message |

### IllformedLocaleException

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
IllformedLocaleException(
    message: String!, 
    errorIndex: Int)
```

Constructs a new`IllformedLocaleException`with the given message and the error index. The error index is the approximate offset from the start of the ill-formed value to the point where the parse first detected an error. A negative error index value indicates either the error index is not applicable or unknown.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the message |
| `errorIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index |

## Public methods

### getErrorIndex

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getErrorIndex(): Int
```

Returns the index where the error was found. A negative value indicates either the error index is not applicable or unknown.

| Return ||
|----------------------------------------------------------------------------|-----------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the error index |
