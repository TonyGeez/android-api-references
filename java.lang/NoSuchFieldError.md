# NoSuchFieldError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NoSuchFieldError

```
open class NoSuchFieldError : IncompatibleClassChangeError
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Error](../java/lang/Error.md) ||||
| | | ↳ | [java.lang.LinkageError](../java/lang/LinkageError.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.IncompatibleClassChangeError](../java/lang/IncompatibleClassChangeError.md) ||
| | | | | ↳ | [java.lang.NoSuchFieldError](../java/lang/NoSuchFieldError.md) |

Thrown if an application tries to access or modify a specified field of an object, and that object no longer has that field.

Normally, this error is caught by the compiler; this error can only occur at run time if the definition of a class has incompatibly changed.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [NoSuchFieldError](../java/lang/NoSuchFieldError.md))`()` Constructs a`NoSuchFieldError`with no detail message. |
| [NoSuchFieldError](../java/lang/NoSuchFieldError.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a`NoSuchFieldError`with the specified detail message. |

## Public constructors

### NoSuchFieldError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
NoSuchFieldError()
```

Constructs a`NoSuchFieldError`with no detail message. 

### NoSuchFieldError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
NoSuchFieldError(s: String!)
```

Constructs a`NoSuchFieldError`with the specified detail message.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. |
