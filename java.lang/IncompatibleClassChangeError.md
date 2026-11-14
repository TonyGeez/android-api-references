# IncompatibleClassChangeError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IncompatibleClassChangeError

```
open class IncompatibleClassChangeError : LinkageError
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Error](https://developer.android.com/reference/kotlin/java/lang/Error) |||
| | | ↳ | [java.lang.LinkageError](https://developer.android.com/reference/kotlin/java/lang/LinkageError) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.IncompatibleClassChangeError](https://developer.android.com/reference/kotlin/java/lang/IncompatibleClassChangeError#) |

| Known Direct Subclasses [AbstractMethodError](https://developer.android.com/reference/kotlin/java/lang/AbstractMethodError), [IllegalAccessError](https://developer.android.com/reference/kotlin/java/lang/IllegalAccessError), [InstantiationError](https://developer.android.com/reference/kotlin/java/lang/InstantiationError), [NoSuchFieldError](https://developer.android.com/reference/kotlin/java/lang/NoSuchFieldError), [NoSuchMethodError](https://developer.android.com/reference/kotlin/java/lang/NoSuchMethodError) |-----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AbstractMethodError](https://developer.android.com/reference/kotlin/java/lang/AbstractMethodError) | Thrown when an application tries to call an abstract method. | | [IllegalAccessError](https://developer.android.com/reference/kotlin/java/lang/IllegalAccessError) | Thrown if an application attempts to access or modify a field, or to call a method that it does not have access to. | | [InstantiationError](https://developer.android.com/reference/kotlin/java/lang/InstantiationError) | Thrown when an application tries to use the Java`new`construct to instantiate an abstract class or an interface. | | [NoSuchFieldError](https://developer.android.com/reference/kotlin/java/lang/NoSuchFieldError) | Thrown if an application tries to access or modify a specified field of an object, and that object no longer has that field. | | [NoSuchMethodError](https://developer.android.com/reference/kotlin/java/lang/NoSuchMethodError) | Thrown if an application tries to call a specified method of a class (either static or instance), and that class no longer has a definition of that method. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Thrown when an incompatible class change has occurred to some class definition. The definition of some class, on which the currently executing method depends, has since changed.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [IncompatibleClassChangeError](https://developer.android.com/reference/kotlin/java/lang/IncompatibleClassChangeError#IncompatibleClassChangeError())`()` Constructs an`IncompatibleClassChangeError`with no detail message. |
| [IncompatibleClassChangeError](https://developer.android.com/reference/kotlin/java/lang/IncompatibleClassChangeError#IncompatibleClassChangeError(kotlin.String))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs an`IncompatibleClassChangeError`with the specified detail message. |

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
