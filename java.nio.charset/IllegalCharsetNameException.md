# IllegalCharsetNameException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IllegalCharsetNameException

```
open class IllegalCharsetNameException : IllegalArgumentException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.IllegalArgumentException](https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#) ||
| | | | | ↳ | [java.nio.charset.IllegalCharsetNameException](https://developer.android.com/reference/kotlin/java/nio/charset/IllegalCharsetNameException#) |

Unchecked exception thrown when a string that is not a [legal charset name](https://developer.android.com/reference/kotlin/java/nio/charset/Charset#names) is used as such.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [IllegalCharsetNameException](https://developer.android.com/reference/kotlin/java/nio/charset/IllegalCharsetNameException#IllegalCharsetNameException(kotlin.String))`(`charsetName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an instance of this class. |

| Public methods ||
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getCharsetName](https://developer.android.com/reference/kotlin/java/nio/charset/IllegalCharsetNameException#getCharsetName())`()` Retrieves the illegal charset name. |

## Public constructors

### IllegalCharsetNameException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
IllegalCharsetNameException(charsetName: String!)
```

Constructs an instance of this class.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------|
| `charsetName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The illegal charset name |

## Public methods

### getCharsetName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCharsetName(): String!
```

Retrieves the illegal charset name.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The illegal charset name |
