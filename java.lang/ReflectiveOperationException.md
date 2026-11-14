# ReflectiveOperationException

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ReflectiveOperationException

```
open class ReflectiveOperationException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception) ||
| | | ↳ | [java.lang.ReflectiveOperationException](https://developer.android.com/reference/kotlin/java/lang/ReflectiveOperationException#) |

| Known Direct Subclasses [ClassNotFoundException](https://developer.android.com/reference/kotlin/java/lang/ClassNotFoundException), [IllegalAccessException](https://developer.android.com/reference/kotlin/java/lang/IllegalAccessException), [InstantiationException](https://developer.android.com/reference/kotlin/java/lang/InstantiationException), [InvocationTargetException](https://developer.android.com/reference/kotlin/java/lang/reflect/InvocationTargetException), [NoSuchFieldException](https://developer.android.com/reference/kotlin/java/lang/NoSuchFieldException), [NoSuchMethodException](https://developer.android.com/reference/kotlin/java/lang/NoSuchMethodException) |-------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ClassNotFoundException](https://developer.android.com/reference/kotlin/java/lang/ClassNotFoundException) | Thrown when an application tries to load in a class through its string name using: - The`forName`method in class`Class`. - The`findSystemClass`method in class`ClassLoader`. - The`loadClass`method in class`ClassLoader`. <br /> | | [IllegalAccessException](https://developer.android.com/reference/kotlin/java/lang/IllegalAccessException) | An IllegalAccessException is thrown when an application tries to reflectively create an instance (other than an array), set or get a field, or invoke a method, but the currently executing method does not have access to the definition of the specified class, field, method or constructor. | | [InstantiationException](https://developer.android.com/reference/kotlin/java/lang/InstantiationException) | Thrown when an application tries to create an instance of a class using the`newInstance`method in class`Class`, but the specified class object cannot be instantiated. | | [InvocationTargetException](https://developer.android.com/reference/kotlin/java/lang/reflect/InvocationTargetException) | InvocationTargetException is a checked exception that wraps an exception thrown by an invoked method or constructor. | | [NoSuchFieldException](https://developer.android.com/reference/kotlin/java/lang/NoSuchFieldException) | Signals that the class doesn't have a field of a specified name. | | [NoSuchMethodException](https://developer.android.com/reference/kotlin/java/lang/NoSuchMethodException) | Thrown when a particular method cannot be found. | |

Common superclass of exceptions thrown by reflective operations in core reflection.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ReflectiveOperationException](https://developer.android.com/reference/kotlin/java/lang/ReflectiveOperationException#ReflectiveOperationException())`()` Constructs a new exception with`null`as its detail message. |
| [ReflectiveOperationException](https://developer.android.com/reference/kotlin/java/lang/ReflectiveOperationException#ReflectiveOperationException(kotlin.String))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a new exception with the specified detail message. |
| [ReflectiveOperationException](https://developer.android.com/reference/kotlin/java/lang/ReflectiveOperationException#ReflectiveOperationException(kotlin.String,%20kotlin.Throwable))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a new exception with the specified detail message and cause. |
| [ReflectiveOperationException](https://developer.android.com/reference/kotlin/java/lang/ReflectiveOperationException#ReflectiveOperationException(kotlin.Throwable))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a new exception with the specified cause and a detail message of`(cause==null ? null : cause.toString())`(which typically contains the class and detail message of`cause`). |

## Public constructors

### ReflectiveOperationException

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ReflectiveOperationException()
```

Constructs a new exception with`null`as its detail message. The cause is not initialized, and may subsequently be initialized by a call to [initCause](https://developer.android.com/reference/kotlin/java/lang/Throwable#initCause(kotlin.Throwable)). 

### ReflectiveOperationException

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ReflectiveOperationException(message: String!)
```

Constructs a new exception with the specified detail message. The cause is not initialized, and may subsequently be initialized by a call to [initCause](https://developer.android.com/reference/kotlin/java/lang/Throwable#initCause(kotlin.Throwable)).

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. The detail message is saved for later retrieval by the [getMessage()](https://developer.android.com/reference/kotlin/java/lang/Throwable#getMessage())method. |

### ReflectiveOperationException

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ReflectiveOperationException(
    message: String!, 
    cause: Throwable!)
```

Constructs a new exception with the specified detail message and cause.

Note that the detail message associated with`cause`is*not*automatically incorporated in this exception's detail message.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message (which is saved for later retrieval by the [getMessage()](https://developer.android.com/reference/kotlin/java/lang/Throwable#getMessage())method). |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause (which is saved for later retrieval by the [getCause()](https://developer.android.com/reference/kotlin/java/lang/Throwable#getCause())method). (A`null`value is permitted, and indicates that the cause is nonexistent or unknown.) |

### ReflectiveOperationException

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ReflectiveOperationException(cause: Throwable!)
```

Constructs a new exception with the specified cause and a detail message of`(cause==null ? null : cause.toString())`(which typically contains the class and detail message of`cause`).

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause (which is saved for later retrieval by the [getCause()](https://developer.android.com/reference/kotlin/java/lang/Throwable#getCause())method). (A`null`value is permitted, and indicates that the cause is nonexistent or unknown.) |
