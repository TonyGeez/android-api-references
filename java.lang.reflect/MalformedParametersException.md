# MalformedParametersException

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MalformedParametersException

```
open class MalformedParametersException : RuntimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#) ||
| | | | ↳ | [java.lang.reflect.MalformedParametersException](https://developer.android.com/reference/kotlin/java/lang/reflect/MalformedParametersException#) |

Thrown when [the](https://developer.android.com/reference/kotlin/java/lang/reflect/Executable#getParameters())attempts to read method parameters from a class file and determines that one or more parameters are malformed.

The following is a list of conditions under which this exception can be thrown:

- The number of parameters (parameter_count) is wrong for the method
- A constant pool index is out of bounds.
- A constant pool index does not refer to a UTF-8 entry
- A parameter's name is "", or contains an illegal character
- The flags field contains an illegal flag (something other than FINAL, SYNTHETIC, or MANDATED)

See [java.lang.reflect.Executable#getParameters](https://developer.android.com/reference/kotlin/java/lang/reflect/Executable#getParameters())for more information.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [MalformedParametersException](https://developer.android.com/reference/kotlin/java/lang/reflect/MalformedParametersException#MalformedParametersException())`()` Create a`MalformedParametersException`with an empty reason. |
| [MalformedParametersException](https://developer.android.com/reference/kotlin/java/lang/reflect/MalformedParametersException#MalformedParametersException(kotlin.String))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Create a`MalformedParametersException`. |

## Public constructors

### MalformedParametersException

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
MalformedParametersException()
```

Create a`MalformedParametersException`with an empty reason. 

### MalformedParametersException

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
MalformedParametersException(reason: String!)
```

Create a`MalformedParametersException`.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------|
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The reason for the exception. |
