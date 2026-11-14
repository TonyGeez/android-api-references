Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IkeIOException

```
class IkeIOException : IkeNonProtocolException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||||
| | | ↳ | [android.net.ipsec.ike.exceptions.IkeException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeException) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [android.net.ipsec.ike.exceptions.IkeNonProtocolException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeNonProtocolException) ||
| | | | | ↳ | [android.net.ipsec.ike.exceptions.IkeIOException](https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeIOException#) |

Wrapper for I/O exceptions encountered during IKE operations.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeIOException#IkeIOException(java.io.IOException)(cause: https://developer.android.com/reference/kotlin/java/io/IOException.html#)` Constructs a new exception with the specified cause. |

| Public methods ||
|---|---|
| [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeIOException#initCause(kotlin.Throwable)(cause: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html?)` Initializes the *cause* of this throwable to the specified value. |

| Properties ||
|---|---|
| [IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#) | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeIOException#cause:java.io.IOException` Returns the cause of this IkeIOException. |

## Public constructors

### IkeIOException

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
IkeIOException(cause: IOException)
```

Constructs a new exception with the specified cause.

Callers are not generally expected to instantiate this object themselves, except for testing. A reference is passed via `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionCallback.html#` or `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/ChildSessionCallback.html#`.

| Parameters ||
|---|---|
| `cause` | [IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#): the cause (which is saved for later retrieval by the `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeIOException#cause:java.io.IOException` method). This value cannot be `null`. |

## Public methods

### initCause

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun initCause(cause: Throwable?): Throwable
```

Initializes the *cause* of this throwable to the specified value. (The cause is the throwable that caused this throwable to get thrown.)

This method can be called at most once. It is generally called from within the constructor, or immediately after creating the throwable. If this throwable was created with `https://developer.android.com/reference/kotlin/java/lang/Throwable.html#Throwable(kotlin.Throwable)` or `https://developer.android.com/reference/kotlin/java/lang/Throwable.html#Throwable(kotlin.String,%20kotlin.Throwable)`, this method cannot be called even once.

An example of using this method on a legacy throwable type without other support for setting the cause is:

```kotlin
try {
      lowLevelOp();
  } catch (LowLevelException le) {
      throw (HighLevelException)
            new HighLevelException().initCause(le); // Legacy constructor
  }
  
```

| Parameters ||
|---|---|
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?: the cause (which is saved for later retrieval by the `https://developer.android.com/reference/kotlin/java/lang/Throwable.html#getCause()` method). (A `null` value is permitted, and indicates that the cause is nonexistent or unknown.) |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html` | a reference to this `Throwable` instance. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `cause` is this throwable. (A throwable cannot be its own cause.) |
| `java.lang.IllegalStateException` | if this throwable was created with `https://developer.android.com/reference/kotlin/java/lang/Throwable.html#Throwable(kotlin.Throwable)` or `https://developer.android.com/reference/kotlin/java/lang/Throwable.html#Throwable(kotlin.String,%20kotlin.Throwable)`, or this method has already been called on this throwable. |

## Properties

### cause

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
val cause: IOException
```

Returns the cause of this IkeIOException.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/io/IOException.html#` | the cause of this IkeIOException. It might be a subclass of IOException that represents a specific type of I/O issue. For example, `https://developer.android.com/reference/kotlin/java/net/UnknownHostException.html#` and `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/exceptions/IkeTimeoutException`. This value cannot be `null`. |
