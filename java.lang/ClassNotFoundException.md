# ClassNotFoundException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ClassNotFoundException

```
open class ClassNotFoundException : ReflectiveOperationException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception) |||
| | | ↳ | [java.lang.ReflectiveOperationException](https://developer.android.com/reference/kotlin/java/lang/ReflectiveOperationException) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.ClassNotFoundException](https://developer.android.com/reference/kotlin/java/lang/ClassNotFoundException#) |

Thrown when an application tries to load in a class through its string name using:

- The`forName`method in class`Class`.
- The`findSystemClass`method in class`ClassLoader`.
- The`loadClass`method in class`ClassLoader`.

<br />

but no definition for the class with the specified name could be found.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ClassNotFoundException](https://developer.android.com/reference/kotlin/java/lang/ClassNotFoundException#ClassNotFoundException())`()` Constructs a`ClassNotFoundException`with no detail message. |
| [ClassNotFoundException](https://developer.android.com/reference/kotlin/java/lang/ClassNotFoundException#ClassNotFoundException(kotlin.String))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a`ClassNotFoundException`with the specified detail message. |
| [ClassNotFoundException](https://developer.android.com/reference/kotlin/java/lang/ClassNotFoundException#ClassNotFoundException(kotlin.String,%20kotlin.Throwable))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `ex:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a`ClassNotFoundException`with the specified detail message and optional exception that was raised while loading the class. |

| Public methods ||
|---------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)! | [getException](https://developer.android.com/reference/kotlin/java/lang/ClassNotFoundException#getException())`()` Returns the exception that was raised if an error occurred while attempting to load the class. |

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
