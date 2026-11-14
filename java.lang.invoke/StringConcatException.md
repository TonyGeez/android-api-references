# StringConcatException

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StringConcatException

```
open class StringConcatException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||
| | | ↳ | [java.lang.invoke.StringConcatException](https://developer.android.com/reference/kotlin/java/lang/invoke/StringConcatException#) |
| --- | --- | --- | --- |

StringConcatException is thrown by [StringConcatFactory](https://developer.android.com/reference/kotlin/java/lang/invoke/StringConcatException#) when linkage invariants are violated.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [StringConcatException](https://developer.android.com/reference/kotlin/java/lang/invoke/StringConcatException#StringConcatException(kotlin.String))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an exception with a message |
| [StringConcatException](https://developer.android.com/reference/kotlin/java/lang/invoke/StringConcatException#StringConcatException(kotlin.String,%20kotlin.Throwable))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs an exception with a message and a linked throwable |

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
