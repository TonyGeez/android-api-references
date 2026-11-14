# UnsupportedCharsetException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UnsupportedCharsetException

```
open class UnsupportedCharsetException : IllegalArgumentException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.IllegalArgumentException](https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#) ||
| | | | | ↳ | [java.nio.charset.UnsupportedCharsetException](https://developer.android.com/reference/kotlin/java/nio/charset/UnsupportedCharsetException#) |

Unchecked exception thrown when no support is available for a requested charset.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [UnsupportedCharsetException](https://developer.android.com/reference/kotlin/java/nio/charset/UnsupportedCharsetException#UnsupportedCharsetException(kotlin.String))`(`charsetName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an instance of this class. |

| Public methods ||
|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getCharsetName](https://developer.android.com/reference/kotlin/java/nio/charset/UnsupportedCharsetException#getCharsetName())`()` Retrieves the name of the unsupported charset. |

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
