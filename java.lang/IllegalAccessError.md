# IllegalAccessError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IllegalAccessError

```
open class IllegalAccessError : IncompatibleClassChangeError
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Error](../java/lang/Error.md) ||||
| | | ↳ | [java.lang.LinkageError](../java/lang/LinkageError.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.IncompatibleClassChangeError](../java/lang/IncompatibleClassChangeError.md) ||
| | | | | ↳ | [java.lang.IllegalAccessError](../java/lang/IllegalAccessError.md) |

Thrown if an application attempts to access or modify a field, or to call a method that it does not have access to.

Normally, this error is caught by the compiler; this error can only occur at run time if the definition of a class has incompatibly changed.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [IllegalAccessError](../java/lang/IllegalAccessError.md))`()` Constructs an`IllegalAccessError`with no detail message. |
| [IllegalAccessError](../java/lang/IllegalAccessError.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an`IllegalAccessError`with the specified detail message. |

## Public constructors

### IllegalAccessError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
IllegalAccessError()
```

Constructs an`IllegalAccessError`with no detail message. 

### IllegalAccessError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
IllegalAccessError(s: String!)
```

Constructs an`IllegalAccessError`with the specified detail message.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. |
