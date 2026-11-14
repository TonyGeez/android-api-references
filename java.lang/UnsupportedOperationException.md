Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UnsupportedOperationException

```
open class UnsupportedOperationException : RuntimeException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](Exception.md) |||
| | | ↳ | [java.lang.RuntimeException](RuntimeException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.UnsupportedOperationException](UnsupportedOperationException.md) |

| Known Direct Subclasses [ReadOnlyBufferException](../java.nio/ReadOnlyBufferException.md), [ReadOnlyFileSystemException](../java.nio.file/ReadOnlyFileSystemException.md) |---|---| | [ReadOnlyBufferException](../java.nio/ReadOnlyBufferException.md) | Unchecked exception thrown when a content-mutation method such as put or compact is invoked upon a read-only buffer. | | [ReadOnlyFileSystemException](../java.nio.file/ReadOnlyFileSystemException.md) | Unchecked exception thrown when an attempt is made to update an object associated with a isReadOnly `FileSystem`. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Thrown to indicate that the requested operation is not supported.

This class is a member of the [Java Collections Framework](https://developer.android.com//reference/java/util/package-summary.html#CollectionsFramework).

## Summary

| Public constructors ||
|---|---|
| UnsupportedOperationException Constructs an UnsupportedOperationException with no detail message. |
| UnsupportedOperationException Constructs an UnsupportedOperationException with the specified detail message. |
| UnsupportedOperationException Constructs a new exception with the specified detail message and cause. |
| UnsupportedOperationException Constructs a new exception with the specified cause and a detail message of `(cause==null ? null : cause.toString())` (which typically contains the class and detail message of `cause`). |

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
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the detail message (which is saved for later retrieval by the getMessage method). |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!: the cause (which is saved for later retrieval by the getCause method). (A `null` value is permitted, and indicates that the cause is nonexistent or unknown.) |

### UnsupportedOperationException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
UnsupportedOperationException(cause: Throwable!)
```

Constructs a new exception with the specified cause and a detail message of `(cause==null ? null : cause.toString())` (which typically contains the class and detail message of `cause`). This constructor is useful for exceptions that are little more than wrappers for other throwables (for example, `https://developer.android.com/reference/kotlin/java/security/PrivilegedActionException.html#`).

| Parameters ||
|---|---|
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!: the cause (which is saved for later retrieval by the getCause method). (A `null` value is permitted, and indicates that the cause is nonexistent or unknown.) |
