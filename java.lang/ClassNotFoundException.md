# ClassNotFoundException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ClassNotFoundException

```
open class ClassNotFoundException : ReflectiveOperationException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](Exception.md) |||
| | | ↳ | [java.lang.ReflectiveOperationException](ReflectiveOperationException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.ClassNotFoundException](ClassNotFoundException.md) |

Thrown when an application tries to load in a class through its string name using:

- The`forName`method in class`Class`.
- The`findSystemClass`method in class`ClassLoader`.
- The`loadClass`method in class`ClassLoader`.

<br />

but no definition for the class with the specified name could be found.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ClassNotFoundException](ClassNotFoundException.md))`()` Constructs a`ClassNotFoundException`with no detail message. |
| [ClassNotFoundException](ClassNotFoundException.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a`ClassNotFoundException`with the specified detail message. |
| [ClassNotFoundException](ClassNotFoundException.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `ex:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a`ClassNotFoundException`with the specified detail message and optional exception that was raised while loading the class. |

| Public methods ||
|---------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)! | [getException](ClassNotFoundException.md))`()` Returns the exception that was raised if an error occurred while attempting to load the class. |

## Public constructors

### ClassNotFoundException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ClassNotFoundException()
```

Constructs a`ClassNotFoundException`with no detail message. 

### ClassNotFoundException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ClassNotFoundException(s: String!)
```

Constructs a`ClassNotFoundException`with the specified detail message.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. |

### ClassNotFoundException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ClassNotFoundException(
    s: String!, 
    ex: Throwable!)
```

Constructs a`ClassNotFoundException`with the specified detail message and optional exception that was raised while loading the class.

| Parameters ||
|------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message |
| `ex` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the exception that was raised while loading the class |

## Public methods

### getException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getException(): Throwable!
```

Returns the exception that was raised if an error occurred while attempting to load the class. Otherwise, returns`null`.

| Return ||
|-----------------------------------------------------------------------------------------|-----------------------------------------------------|
| [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)! | the`Exception`that was raised while loading a class |
