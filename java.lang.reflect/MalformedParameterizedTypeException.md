# MalformedParameterizedTypeException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MalformedParameterizedTypeException

```
open class MalformedParameterizedTypeException : RuntimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.reflect.MalformedParameterizedTypeException](https://developer.android.com/reference/kotlin/java/lang/reflect/MalformedParameterizedTypeException#) |

Thrown when a semantically malformed parameterized type is encountered by a reflective method that needs to instantiate it. For example, if the number of type arguments to a parameterized type is wrong.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [MalformedParameterizedTypeException](https://developer.android.com/reference/kotlin/java/lang/reflect/MalformedParameterizedTypeException#MalformedParameterizedTypeException())`()` Constructs a`MalformedParameterizedTypeException`with no detail message. |
| [MalformedParameterizedTypeException](https://developer.android.com/reference/kotlin/java/lang/reflect/MalformedParameterizedTypeException#MalformedParameterizedTypeException(kotlin.String))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a`MalformedParameterizedTypeException`with the given detail message. |

## Public constructors

### MalformedParameterizedTypeException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
MalformedParameterizedTypeException()
```

Constructs a`MalformedParameterizedTypeException`with no detail message. 

### MalformedParameterizedTypeException

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
MalformedParameterizedTypeException(message: String!)
```

Constructs a`MalformedParameterizedTypeException`with the given detail message.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message; may be`null` |
