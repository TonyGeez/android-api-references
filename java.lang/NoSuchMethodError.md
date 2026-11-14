# NoSuchMethodError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NoSuchMethodError

```
open class NoSuchMethodError : IncompatibleClassChangeError
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Error](https://developer.android.com/reference/kotlin/java/lang/Error) ||||
| | | ↳ | [java.lang.LinkageError](https://developer.android.com/reference/kotlin/java/lang/LinkageError) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.IncompatibleClassChangeError](https://developer.android.com/reference/kotlin/java/lang/IncompatibleClassChangeError) ||
| | | | | ↳ | [java.lang.NoSuchMethodError](https://developer.android.com/reference/kotlin/java/lang/NoSuchMethodError#) |

Thrown if an application tries to call a specified method of a class (either static or instance), and that class no longer has a definition of that method.

Normally, this error is caught by the compiler; this error can only occur at run time if the definition of a class has incompatibly changed.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [NoSuchMethodError](https://developer.android.com/reference/kotlin/java/lang/NoSuchMethodError#NoSuchMethodError())`()` Constructs a `NoSuchMethodError` with no detail message. |
| [NoSuchMethodError](https://developer.android.com/reference/kotlin/java/lang/NoSuchMethodError#NoSuchMethodError(kotlin.String))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a `NoSuchMethodError` with the specified detail message. |

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
