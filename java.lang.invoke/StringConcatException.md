# StringConcatException

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StringConcatException

```
open class StringConcatException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) ||
| | | ↳ | [java.lang.invoke.StringConcatException](StringConcatException.md) |
| --- | --- | --- | --- |

StringConcatException is thrown by [StringConcatFactory](StringConcatException.md) when linkage invariants are violated.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [StringConcatException](StringConcatException.md))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an exception with a message |
| [StringConcatException](StringConcatException.md))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs an exception with a message and a linked throwable |

## Public constructors

### StringConcatException

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
StringConcatException(msg: String!)
```

Constructs an exception with a message

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------|
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:exception message |

### StringConcatException

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
StringConcatException(
    msg: String!, 
    cause: Throwable!)
```

Constructs an exception with a message and a linked throwable

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------|
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:exception message |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:throwable cause |
