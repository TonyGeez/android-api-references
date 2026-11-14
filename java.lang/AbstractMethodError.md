# AbstractMethodError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AbstractMethodError

```
open class AbstractMethodError : IncompatibleClassChangeError
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Error](Error.md) ||||
| | | ↳ | [java.lang.LinkageError](LinkageError.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.IncompatibleClassChangeError](IncompatibleClassChangeError.md) ||
| | | | | ↳ | [java.lang.AbstractMethodError](AbstractMethodError.md) |

Thrown when an application tries to call an abstract method. Normally, this error is caught by the compiler; this error can only occur at run time if the definition of some class has incompatibly changed since the currently executing method was last compiled.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AbstractMethodError](AbstractMethodError.md))`()` Constructs an`AbstractMethodError`with no detail message. |
| [AbstractMethodError](AbstractMethodError.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an`AbstractMethodError`with the specified detail message. |

## Public constructors

### AbstractMethodError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AbstractMethodError()
```

Constructs an`AbstractMethodError`with no detail message. 

### AbstractMethodError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AbstractMethodError(s: String!)
```

Constructs an`AbstractMethodError`with the specified detail message.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. |
