# InstantiationError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InstantiationError

```
open class InstantiationError : IncompatibleClassChangeError
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Error](../java/lang/Error.md) ||||
| | | ↳ | [java.lang.LinkageError](../java/lang/LinkageError.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.IncompatibleClassChangeError](../java/lang/IncompatibleClassChangeError.md) ||
| | | | | ↳ | [java.lang.InstantiationError](../java/lang/InstantiationError.md) |

Thrown when an application tries to use the Java `new` construct to instantiate an abstract class or an interface.

Normally, this error is caught by the compiler; this error can only occur at run time if the definition of a class has incompatibly changed.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [InstantiationError](../java/lang/InstantiationError.md))`()` Constructs an `InstantiationError` with no detail message. |
| [InstantiationError](../java/lang/InstantiationError.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an `InstantiationError` with the specified detail message. |

## Public constructors

### InstantiationError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
InstantiationError()
```

Constructs an `InstantiationError` with no detail message. 

### InstantiationError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
InstantiationError(s: String!)
```

Constructs an `InstantiationError` with the specified detail message.

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the detail message. |
