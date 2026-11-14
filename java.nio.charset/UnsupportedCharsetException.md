# UnsupportedCharsetException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UnsupportedCharsetException

```
open class UnsupportedCharsetException : IllegalArgumentException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) ||||
| | | ↳ | [java.lang.RuntimeException](../java.lang/RuntimeException.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.IllegalArgumentException](../java.lang/IllegalArgumentException.md) ||
| | | | | ↳ | [java.nio.charset.UnsupportedCharsetException](UnsupportedCharsetException.md) |

Unchecked exception thrown when no support is available for a requested charset.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [UnsupportedCharsetException](UnsupportedCharsetException.md))`(`charsetName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an instance of this class. |

| Public methods ||
|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getCharsetName](UnsupportedCharsetException.md))`()` Retrieves the name of the unsupported charset. |

## Public constructors

### UnsupportedCharsetException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
UnsupportedCharsetException(charsetName: String!)
```

Constructs an instance of this class.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------|
| `charsetName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the unsupported charset |

## Public methods

### getCharsetName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCharsetName(): String!
```

Retrieves the name of the unsupported charset.

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The name of the unsupported charset |
