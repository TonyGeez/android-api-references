# InvalidObjectException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InvalidObjectException

```
open class InvalidObjectException : ObjectStreamException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||||
| | | ↳ | [java.io.IOException](https://developer.android.com/reference/kotlin/java/io/IOException) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.io.ObjectStreamException](https://developer.android.com/reference/kotlin/java/io/ObjectStreamException) ||
| | | | | ↳ | [java.io.InvalidObjectException](https://developer.android.com/reference/kotlin/java/io/InvalidObjectException#) |

Indicates that one or more deserialized objects failed validation tests. The argument should provide the reason for the failure.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [InvalidObjectException](https://developer.android.com/reference/kotlin/java/io/InvalidObjectException#InvalidObjectException(kotlin.String))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an `InvalidObjectException`. |

## Public constructors

### InvalidObjectException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
InvalidObjectException(reason: String!)
```

Constructs an `InvalidObjectException`.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: Detailed message explaining the reason for the failure. |

**See Also**

- [java.io.ObjectInputValidation](https://developer.android.com/reference/kotlin/java/io/ObjectInputValidation)
