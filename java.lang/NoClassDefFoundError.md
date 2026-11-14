# NoClassDefFoundError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NoClassDefFoundError

```
open class NoClassDefFoundError : LinkageError
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Error](../java/lang/Error.md) |||
| | | ↳ | [java.lang.LinkageError](../java/lang/LinkageError.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.NoClassDefFoundError](../java/lang/NoClassDefFoundError.md) |

Thrown if the Java Virtual Machine or a`ClassLoader`instance tries to load in the definition of a class (as part of a normal method call or as part of creating a new instance using the`new`expression) and no definition of the class could be found.

The searched-for class definition existed when the currently executing class was compiled, but the definition can no longer be found.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [NoClassDefFoundError](../java/lang/NoClassDefFoundError.md))`()` Constructs a`NoClassDefFoundError`with no detail message. |
| [NoClassDefFoundError](../java/lang/NoClassDefFoundError.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a`NoClassDefFoundError`with the specified detail message. |

## Public constructors

### NoClassDefFoundError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
NoClassDefFoundError()
```

Constructs a`NoClassDefFoundError`with no detail message. 

### NoClassDefFoundError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
NoClassDefFoundError(s: String!)
```

Constructs a`NoClassDefFoundError`with the specified detail message.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. |
