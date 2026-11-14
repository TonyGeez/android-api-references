# ErrnoException

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ErrnoException

Kotlin| [Java](../android/system/ErrnoException.md) 
| --- | --- |

```
class ErrnoException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) ||
| | | ↳ | [android.system.ErrnoException](../android/system/ErrnoException.md) |
| --- | --- | --- | --- |

A checked exception thrown when [Os](../android/system/Os.md) methods fail. This exception contains the native errno value, for comparison against the constants in [OsConstants](../android/system/OsConstants.md), should sophisticated callers need to adjust their behavior based on the exact failure.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ErrnoException](../android/system/ErrnoException.md))`(`functionName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `errno:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs an instance with the given function name and errno value. |
| [ErrnoException](../android/system/ErrnoException.md))`(`functionName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `errno:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs an instance with the given function name, errno value, and cause. |

| Public methods ||
|--------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IOException](../java/io/IOException.md) | [rethrowAsIOException](../android/system/ErrnoException.md))`()` Throws an [IOException](../java/io/IOException.md) with a message based on [getMessage()](../android/system/ErrnoException.md) and with this instance as the cause. |
| [SocketException](../java/net/SocketException.md) | [rethrowAsSocketException](../android/system/ErrnoException.md))`()` Throws a [SocketException](../java/net/SocketException.md) with a message based on [getMessage()](../android/system/ErrnoException.md) and with this instance as the cause. |

| Properties ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [errno](../android/system/ErrnoException.md) The errno value, for comparison with the`E`constants in [OsConstants](../android/system/OsConstants.md). |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [message](../android/system/ErrnoException.md) Converts the stashed function name and errno value to a human-readable string. |

## Public constructors

### ErrnoException

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ErrnoException(
    functionName: String!, 
    errno: Int)
```

Constructs an instance with the given function name and errno value. 

### ErrnoException

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ErrnoException(
    functionName: String!, 
    errno: Int, 
    cause: Throwable!)
```

Constructs an instance with the given function name, errno value, and cause.

## Public methods

### rethrowAsIOException

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun rethrowAsIOException(): IOException
```

Throws an [IOException](../java/io/IOException.md) with a message based on [getMessage()](../android/system/ErrnoException.md) and with this instance as the cause.

This method always terminates by throwing the exception. Callers can write`throw e.rethrowAsIOException()`to make that clear to the compiler.

| Return ||
|-----------------------------------------------------------------------------------------|-----------------------------|
| [IOException](../java/io/IOException.md) | This value cannot be`null`. |

### rethrowAsSocketException

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun rethrowAsSocketException(): SocketException
```

Throws a [SocketException](../java/net/SocketException.md) with a message based on [getMessage()](../android/system/ErrnoException.md) and with this instance as the cause.

This method always terminates by throwing the exception. Callers can write`throw e.rethrowAsIOException()`to make that clear to the compiler.

| Return ||
|--------------------------------------------------------------------------------------------------|-----------------------------|
| [SocketException](../java/net/SocketException.md) | This value cannot be`null`. |

## Properties

### errno

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val errno: Int
```

The errno value, for comparison with the`E`constants in [OsConstants](../android/system/OsConstants.md). 

### message

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val message: String?
```

Converts the stashed function name and errno value to a human-readable string. We do this here rather than in the constructor so that callers only pay for this if they need it.

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | the detail message string of this`Throwable`instance (which may be`null`). |
