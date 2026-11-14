# IncompatibleClassChangeError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IncompatibleClassChangeError

```
open class IncompatibleClassChangeError : LinkageError
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Error](Error.md) |||
| | | ↳ | [java.lang.LinkageError](LinkageError.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.IncompatibleClassChangeError](IncompatibleClassChangeError.md) |

| Known Direct Subclasses [AbstractMethodError](AbstractMethodError.md), [IllegalAccessError](IllegalAccessError.md), [InstantiationError](InstantiationError.md), [NoSuchFieldError](NoSuchFieldError.md), [NoSuchMethodError](NoSuchMethodError.md) |-----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AbstractMethodError](AbstractMethodError.md) | Thrown when an application tries to call an abstract method. | | [IllegalAccessError](IllegalAccessError.md) | Thrown if an application attempts to access or modify a field, or to call a method that it does not have access to. | | [InstantiationError](InstantiationError.md) | Thrown when an application tries to use the Java`new`construct to instantiate an abstract class or an interface. | | [NoSuchFieldError](NoSuchFieldError.md) | Thrown if an application tries to access or modify a specified field of an object, and that object no longer has that field. | | [NoSuchMethodError](NoSuchMethodError.md) | Thrown if an application tries to call a specified method of a class (either static or instance), and that class no longer has a definition of that method. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Thrown when an incompatible class change has occurred to some class definition. The definition of some class, on which the currently executing method depends, has since changed.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [IncompatibleClassChangeError](IncompatibleClassChangeError.md))`()` Constructs an`IncompatibleClassChangeError`with no detail message. |
| [IncompatibleClassChangeError](IncompatibleClassChangeError.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an`IncompatibleClassChangeError`with the specified detail message. |

## Public constructors

### IncompatibleClassChangeError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
IncompatibleClassChangeError()
```

Constructs an`IncompatibleClassChangeError`with no detail message. 

### IncompatibleClassChangeError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
IncompatibleClassChangeError(s: String!)
```

Constructs an`IncompatibleClassChangeError`with the specified detail message.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. |
