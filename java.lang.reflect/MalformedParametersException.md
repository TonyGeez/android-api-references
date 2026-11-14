# MalformedParametersException

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MalformedParametersException

```
open class MalformedParametersException : RuntimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) |||
| | | ↳ | [java.lang.RuntimeException](../java.lang/RuntimeException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.reflect.MalformedParametersException](MalformedParametersException.md) |

Thrown when [the](Executable.md))attempts to read method parameters from a class file and determines that one or more parameters are malformed.

The following is a list of conditions under which this exception can be thrown:

- The number of parameters (parameter_count) is wrong for the method
- A constant pool index is out of bounds.
- A constant pool index does not refer to a UTF-8 entry
- A parameter's name is "", or contains an illegal character
- The flags field contains an illegal flag (something other than FINAL, SYNTHETIC, or MANDATED)

See [java.lang.reflect.Executable#getParameters](Executable.md))for more information.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [MalformedParametersException](MalformedParametersException.md))`()` Create a`MalformedParametersException`with an empty reason. |
| [MalformedParametersException](MalformedParametersException.md))`(`reason:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Create a`MalformedParametersException`. |

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
