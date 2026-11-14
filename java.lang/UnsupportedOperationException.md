Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UnsupportedOperationException

```
open class UnsupportedOperationException : RuntimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception) |||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException) ||
| | | | ↳ | [java.lang.UnsupportedOperationException](https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException#) |

| Known Direct Subclasses [ReadOnlyBufferException](https://developer.android.com/reference/kotlin/java/nio/ReadOnlyBufferException.html#), [ReadOnlyFileSystemException](https://developer.android.com/reference/kotlin/java/nio/file/ReadOnlyFileSystemException.html#) |---|---| | [ReadOnlyBufferException](https://developer.android.com/reference/kotlin/java/nio/ReadOnlyBufferException.html#) | Unchecked exception thrown when a content-mutation method such as put or compact is invoked upon a read-only buffer. | | [ReadOnlyFileSystemException](https://developer.android.com/reference/kotlin/java/nio/file/ReadOnlyFileSystemException.html#) | Unchecked exception thrown when an attempt is made to update an object associated with a `https://developer.android.com/reference/kotlin/java/nio/file/FileSystem.html#isReadOnly()` `FileSystem`. | |

Thrown to indicate that the requested operation is not supported.

This class is a member of the [Java Collections Framework](https://developer.android.com//reference/java/util/package-summary.html#CollectionsFramework).

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException#UnsupportedOperationException()()` Constructs an UnsupportedOperationException with no detail message. |
| `https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException#UnsupportedOperationException(kotlin.String)(message: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Constructs an UnsupportedOperationException with the specified detail message. |
| `https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException#UnsupportedOperationException(kotlin.String,%20kotlin.Throwable)(message: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, cause: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html!)` Constructs a new exception with the specified detail message and cause. |
| `https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException#UnsupportedOperationException(kotlin.Throwable)(cause: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html!)` Constructs a new exception with the specified cause and a detail message of `(cause==null ? null : cause.toString())` (which typically contains the class and detail message of `cause`). |

## Public constructors

### UnsupportedOperationException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
UnsupportedOperationException()
```

Constructs an UnsupportedOperationException with no detail message.

### UnsupportedOperationException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
UnsupportedOperationException(message: String!)
```

Constructs an UnsupportedOperationException with the specified detail message.

| Parameters ||
|---|---|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the detail message |

### UnsupportedOperationException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
UnsupportedOperationException(
    message: String!, 
    cause: Throwable!)
```

Constructs a new exception with the specified detail message and cause.

Note that the detail message associated with `cause` is *not* automatically incorporated in this exception's detail message.

| Parameters ||
|---|---|
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the detail message (which is saved for later retrieval by the `https://developer.android.com/reference/kotlin/java/lang/Throwable#getMessage()` method). |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!: the cause (which is saved for later retrieval by the `https://developer.android.com/reference/kotlin/java/lang/Throwable#getCause()` method). (A `null` value is permitted, and indicates that the cause is nonexistent or unknown.) |

### UnsupportedOperationException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
UnsupportedOperationException(cause: Throwable!)
```

Constructs a new exception with the specified cause and a detail message of `(cause==null ? null : cause.toString())` (which typically contains the class and detail message of `cause`). This constructor is useful for exceptions that are little more than wrappers for other throwables (for example, `https://developer.android.com/reference/kotlin/java/security/PrivilegedActionException.html#`).

| Parameters ||
|---|---|
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!: the cause (which is saved for later retrieval by the `https://developer.android.com/reference/kotlin/java/lang/Throwable#getCause()` method). (A `null` value is permitted, and indicates that the cause is nonexistent or unknown.) |
