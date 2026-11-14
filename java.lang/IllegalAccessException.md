# IllegalAccessException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IllegalAccessException

```
open class IllegalAccessException : ReflectiveOperationException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](Exception.md) |||
| | | ↳ | [java.lang.ReflectiveOperationException](ReflectiveOperationException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.IllegalAccessException](IllegalAccessException.md) |

An IllegalAccessException is thrown when an application tries to reflectively create an instance (other than an array), set or get a field, or invoke a method, but the currently executing method does not have access to the definition of the specified class, field, method or constructor.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [IllegalAccessException](IllegalAccessException.md))`()` Constructs an`IllegalAccessException`without a detail message. |
| [IllegalAccessException](IllegalAccessException.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an`IllegalAccessException`with a detail message. |

## Public constructors

### IllegalAccessException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
IllegalAccessException()
```

Constructs an`IllegalAccessException`without a detail message. 

### IllegalAccessException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
IllegalAccessException(s: String!)
```

Constructs an`IllegalAccessException`with a detail message.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. |
