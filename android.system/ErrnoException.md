# ErrnoException

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ErrnoException

Kotlin| [Java](https://developer.android.com/reference/android/system/ErrnoException "View this page in Java") 
| --- | --- |

```
class ErrnoException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||
| | | ↳ | [android.system.ErrnoException](https://developer.android.com/reference/kotlin/android/system/ErrnoException#) |
| --- | --- | --- | --- |

A checked exception thrown when [Os](https://developer.android.com/reference/kotlin/android/system/Os) methods fail. This exception contains the native errno value, for comparison against the constants in [OsConstants](https://developer.android.com/reference/kotlin/android/system/OsConstants), should sophisticated callers need to adjust their behavior based on the exact failure.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ErrnoException](https://developer.android.com/reference/kotlin/android/system/ErrnoException#ErrnoException(kotlin.String,%20kotlin.Int))`(`functionName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `errno:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs an instance with the given function name and errno value. |
| [ErrnoException](https://developer.android.com/reference/kotlin/android/system/ErrnoException#ErrnoException(kotlin.String,%20kotlin.Int,%20kotlin.Throwable))`(`functionName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `errno:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Constructs an instance with the given function name, errno value, and cause. |

| Public methods ||
|--------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#) | [rethrowAsIOException](https://developer.android.com/reference/kotlin/android/system/ErrnoException#rethrowAsIOException())`()` Throws an [IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#) with a message based on [getMessage()](https://developer.android.com/reference/kotlin/android/system/ErrnoException#message:kotlin.String) and with this instance as the cause. |
| [SocketException](https://developer.android.com/reference/kotlin/java/net/SocketException.html#) | [rethrowAsSocketException](https://developer.android.com/reference/kotlin/android/system/ErrnoException#rethrowAsSocketException())`()` Throws a [SocketException](https://developer.android.com/reference/kotlin/java/net/SocketException.html#) with a message based on [getMessage()](https://developer.android.com/reference/kotlin/android/system/ErrnoException#message:kotlin.String) and with this instance as the cause. |

| Properties ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [errno](https://developer.android.com/reference/kotlin/android/system/ErrnoException#errno:kotlin.Int) The errno value, for comparison with the`E`constants in [OsConstants](https://developer.android.com/reference/kotlin/android/system/OsConstants). |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [message](https://developer.android.com/reference/kotlin/android/system/ErrnoException#message:kotlin.String) Converts the stashed function name and errno value to a human-readable string. |

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

Throws an [IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#) with a message based on [getMessage()](https://developer.android.com/reference/kotlin/android/system/ErrnoException#message:kotlin.String) and with this instance as the cause.

This method always terminates by throwing the exception. Callers can write`throw e.rethrowAsIOException()`to make that clear to the compiler.

| Return ||
|-----------------------------------------------------------------------------------------|-----------------------------|
| [IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#) | This value cannot be`null`. |

### rethrowAsSocketException

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun rethrowAsSocketException(): SocketException
```

Throws a [SocketException](https://developer.android.com/reference/kotlin/java/net/SocketException.html#) with a message based on [getMessage()](https://developer.android.com/reference/kotlin/android/system/ErrnoException#message:kotlin.String) and with this instance as the cause.

This method always terminates by throwing the exception. Callers can write`throw e.rethrowAsIOException()`to make that clear to the compiler.

| Return ||
|--------------------------------------------------------------------------------------------------|-----------------------------|
| [SocketException](https://developer.android.com/reference/kotlin/java/net/SocketException.html#) | This value cannot be`null`. |

## Properties

### errno

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val errno: Int
```

The errno value, for comparison with the`E`constants in [OsConstants](https://developer.android.com/reference/kotlin/android/system/OsConstants). 

### message

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val message: String?
```

Converts the stashed function name and errno value to a human-readable string. We do this here rather than in the constructor so that callers only pay for this if they need it.

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | the detail message string of this`Throwable`instance (which may be`null`). |
