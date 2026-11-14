# IllformedLocaleException

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IllformedLocaleException

```
open class IllformedLocaleException : RuntimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) |||
| | | ↳ | [java.lang.RuntimeException](../java.lang/RuntimeException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.util.IllformedLocaleException](IllformedLocaleException.md) |

Thrown by methods in [Locale](Locale.md) and [Locale.Builder](../java/util/Locale.Builder.md) to indicate that an argument is not a well-formed BCP 47 tag.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [IllformedLocaleException](IllformedLocaleException.md))`()` Constructs a new`IllformedLocaleException`with no detail message and -1 as the error index. |
| [IllformedLocaleException](IllformedLocaleException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a new`IllformedLocaleException`with the given message and -1 as the error index. |
| [IllformedLocaleException](IllformedLocaleException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `errorIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs a new`IllformedLocaleException`with the given message and the error index. |

| Public methods ||
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getErrorIndex](IllformedLocaleException.md))`()` Returns the index where the error was found. |

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
