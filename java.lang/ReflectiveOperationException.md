# ReflectiveOperationException

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ReflectiveOperationException

```
open class ReflectiveOperationException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) ||
| | | ↳ | [java.lang.ReflectiveOperationException](../java/lang/ReflectiveOperationException.md) |
| --- | --- | --- | --- |

| Known Direct Subclasses [ClassNotFoundException](../java/lang/ClassNotFoundException.md), [IllegalAccessException](../java/lang/IllegalAccessException.md), [InstantiationException](../java/lang/InstantiationException.md), [InvocationTargetException](../java/lang/reflect/InvocationTargetException.md), [NoSuchFieldException](../java/lang/NoSuchFieldException.md), [NoSuchMethodException](../java/lang/NoSuchMethodException.md) |-------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ClassNotFoundException](../java/lang/ClassNotFoundException.md) | Thrown when an application tries to load in a class through its string name using: - The`forName`method in class`Class`. - The`findSystemClass`method in class`ClassLoader`. - The`loadClass`method in class`ClassLoader`. <br /> | | [IllegalAccessException](../java/lang/IllegalAccessException.md) | An IllegalAccessException is thrown when an application tries to reflectively create an instance (other than an array), set or get a field, or invoke a method, but the currently executing method does not have access to the definition of the specified class, field, method or constructor. | | [InstantiationException](../java/lang/InstantiationException.md) | Thrown when an application tries to create an instance of a class using the`newInstance`method in class`Class`, but the specified class object cannot be instantiated. | | [InvocationTargetException](../java/lang/reflect/InvocationTargetException.md) | InvocationTargetException is a checked exception that wraps an exception thrown by an invoked method or constructor. | | [NoSuchFieldException](../java/lang/NoSuchFieldException.md) | Signals that the class doesn't have a field of a specified name. | | [NoSuchMethodException](../java/lang/NoSuchMethodException.md) | Thrown when a particular method cannot be found. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Common superclass of exceptions thrown by reflective operations in core reflection.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ReflectiveOperationException](../java/lang/ReflectiveOperationException.md))`()` Constructs a new exception with`null`as its detail message. |
| [ReflectiveOperationException](../java/lang/ReflectiveOperationException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a new exception with the specified detail message. |
| [ReflectiveOperationException](../java/lang/ReflectiveOperationException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a new exception with the specified detail message and cause. |
| [ReflectiveOperationException](../java/lang/ReflectiveOperationException.md))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs a new exception with the specified cause and a detail message of`(cause==null ? null : cause.toString())`(which typically contains the class and detail message of`cause`). |

## Public constructors

### ReflectiveOperationException

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ReflectiveOperationException()
```

Constructs a new exception with`null`as its detail message. The cause is not initialized, and may subsequently be initialized by a call to [initCause](../java/lang/Throwable.md)). 

### ReflectiveOperationException

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ReflectiveOperationException(message: String!)
```

Constructs a new exception with the specified detail message. The cause is not initialized, and may subsequently be initialized by a call to [initCause](../java/lang/Throwable.md)).

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message. The detail message is saved for later retrieval by the [getMessage()](../java/lang/Throwable.md))method. |

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
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the detail message (which is saved for later retrieval by the [getMessage()](../java/lang/Throwable.md))method). |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause (which is saved for later retrieval by the [getCause()](../java/lang/Throwable.md))method). (A`null`value is permitted, and indicates that the cause is nonexistent or unknown.) |

### ReflectiveOperationException

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ReflectiveOperationException(cause: Throwable!)
```

Constructs a new exception with the specified cause and a detail message of`(cause==null ? null : cause.toString())`(which typically contains the class and detail message of`cause`).

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the cause (which is saved for later retrieval by the [getCause()](../java/lang/Throwable.md))method). (A`null`value is permitted, and indicates that the cause is nonexistent or unknown.) |
