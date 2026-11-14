# InstantiationException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InstantiationException

```
open class InstantiationException : ReflectiveOperationException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception) |||
| | | ↳ | [java.lang.ReflectiveOperationException](https://developer.android.com/reference/kotlin/java/lang/ReflectiveOperationException) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.InstantiationException](https://developer.android.com/reference/kotlin/java/lang/InstantiationException#) |

Thrown when an application tries to create an instance of a class using the`newInstance`method in class`Class`, but the specified class object cannot be instantiated. The instantiation can fail for a variety of reasons including but not limited to:

- the class object represents an abstract class, an interface, an array class, a primitive type, or`void`
- the class has no nullary constructor

<br />

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [InstantiationException](https://developer.android.com/reference/kotlin/java/lang/InstantiationException#InstantiationException())`()` Constructs an`InstantiationException`with no detail message. |
| [InstantiationException](https://developer.android.com/reference/kotlin/java/lang/InstantiationException#InstantiationException(kotlin.String))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an`InstantiationException`with the specified detail message. |

## Public constructors

### InstantiationException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
InstantiationException()
```

Constructs an`InstantiationException`with no detail message. 

### InstantiationException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
InstantiationException(s: String!)
```

Constructs an`InstantiationException`with the specified detail message.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. |
