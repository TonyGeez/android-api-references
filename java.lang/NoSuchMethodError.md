# NoSuchMethodError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NoSuchMethodError

```
open class NoSuchMethodError : IncompatibleClassChangeError
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Error](../java/lang/Error.md) ||||
| | | ↳ | [java.lang.LinkageError](../java/lang/LinkageError.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.IncompatibleClassChangeError](../java/lang/IncompatibleClassChangeError.md) ||
| | | | | ↳ | [java.lang.NoSuchMethodError](../java/lang/NoSuchMethodError.md) |

Thrown if an application tries to call a specified method of a class (either static or instance), and that class no longer has a definition of that method.

Normally, this error is caught by the compiler; this error can only occur at run time if the definition of a class has incompatibly changed.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [NoSuchMethodError](../java/lang/NoSuchMethodError.md))`()` Constructs a `NoSuchMethodError` with no detail message. |
| [NoSuchMethodError](../java/lang/NoSuchMethodError.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a `NoSuchMethodError` with the specified detail message. |

## Public constructors

### NoSuchMethodError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
NoSuchMethodError()
```

Constructs a `NoSuchMethodError` with no detail message. 

### NoSuchMethodError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
NoSuchMethodError(s: String!)
```

Constructs a `NoSuchMethodError` with the specified detail message.

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the detail message. |
