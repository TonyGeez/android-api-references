# MalformedParameterizedTypeException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MalformedParameterizedTypeException

```
open class MalformedParameterizedTypeException : RuntimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) |||
| | | ↳ | [java.lang.RuntimeException](../java.lang/RuntimeException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.reflect.MalformedParameterizedTypeException](MalformedParameterizedTypeException.md) |

Thrown when a semantically malformed parameterized type is encountered by a reflective method that needs to instantiate it. For example, if the number of type arguments to a parameterized type is wrong.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [MalformedParameterizedTypeException](MalformedParameterizedTypeException.md))`()` Constructs a`MalformedParameterizedTypeException`with no detail message. |
| [MalformedParameterizedTypeException](MalformedParameterizedTypeException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a`MalformedParameterizedTypeException`with the given detail message. |

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
