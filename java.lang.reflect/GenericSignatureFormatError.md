# GenericSignatureFormatError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GenericSignatureFormatError

```
open class GenericSignatureFormatError : ClassFormatError
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Error](https://developer.android.com/reference/kotlin/java/lang/Error.html#) ||||
| | | ↳ | [java.lang.LinkageError](https://developer.android.com/reference/kotlin/java/lang/LinkageError.html#) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.ClassFormatError](https://developer.android.com/reference/kotlin/java/lang/ClassFormatError.html#) ||
| | | | | ↳ | [java.lang.reflect.GenericSignatureFormatError](https://developer.android.com/reference/kotlin/java/lang/reflect/GenericSignatureFormatError#) |

Thrown when a syntactically malformed signature attribute is encountered by a reflective method that needs to interpret the generic signature information for a type, method or constructor.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [GenericSignatureFormatError](https://developer.android.com/reference/kotlin/java/lang/reflect/GenericSignatureFormatError#GenericSignatureFormatError())`()` Constructs a new `GenericSignatureFormatError`. |
| [GenericSignatureFormatError](https://developer.android.com/reference/kotlin/java/lang/reflect/GenericSignatureFormatError#GenericSignatureFormatError(kotlin.String))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a new `GenericSignatureFormatError` with the specified message. |

## Public constructors

### GenericSignatureFormatError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
GenericSignatureFormatError()
```

Constructs a new `GenericSignatureFormatError`. 

### GenericSignatureFormatError

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
GenericSignatureFormatError(message: String!)
```

Constructs a new `GenericSignatureFormatError` with the specified message.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the detail message, may be `null` |
