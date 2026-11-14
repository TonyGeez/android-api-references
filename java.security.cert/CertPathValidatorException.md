Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CertPathValidatorException

```
open class CertPathValidatorException : GeneralSecurityException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) |||
| | | ↳ | [java.security.GeneralSecurityException](https://developer.android.com/reference/kotlin/java/security/GeneralSecurityException.html#) ||
| | | | ↳ | [java.security.cert.CertPathValidatorException](https://developer.android.com/reference/kotlin/java/security/cert/CertPathValidatorException#) |

An exception indicating one of a variety of problems encountered when validating a certification path.

A `CertPathValidatorException` provides support for wrapping exceptions. The `https://developer.android.com/reference/kotlin/java/lang/Throwable.html#getCause()` method returns the throwable, if any, that caused this exception to be thrown.

A `CertPathValidatorException` may also include the certification path that was being validated when the exception was thrown, the index of the certificate in the certification path that caused the exception to be thrown, and the reason that caused the failure. Use the `https://developer.android.com/reference/kotlin/java/security/cert/CertPathValidatorException#getCertPath()`, `https://developer.android.com/reference/kotlin/java/security/cert/CertPathValidatorException#getIndex()`, and `https://developer.android.com/reference/kotlin/java/security/cert/CertPathValidatorException#getReason()` methods to retrieve this information.

**Concurrent Access**

Unless otherwise specified, the methods defined in this class are not thread-safe. Multiple threads that need to access a single object concurrently should synchronize amongst themselves and provide the necessary locking. Multiple threads each manipulating separate objects need not synchronize.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/java/security/cert/CertPathValidatorException.BasicReason` The BasicReason enumerates the potential reasons that a certification path of any type may be invalid. |
| abstract | `https://developer.android.com/reference/kotlin/java/security/cert/CertPathValidatorException.Reason` The reason the validation algorithm failed. |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/security/cert/CertPathValidatorException#CertPathValidatorException()()` Creates a `CertPathValidatorException` with no detail message. |
| `https://developer.android.com/reference/kotlin/java/security/cert/CertPathValidatorException#CertPathValidatorException(kotlin.String)(msg: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Creates a `CertPathValidatorException` with the given detail message. |
| `https://developer.android.com/reference/kotlin/java/security/cert/CertPathValidatorException#CertPathValidatorException(kotlin.String,%20kotlin.Throwable)(msg: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, cause: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html!)` Creates a `CertPathValidatorException` with the specified detail message and cause. |
| `https://developer.android.com/reference/kotlin/java/security/cert/CertPathValidatorException#CertPathValidatorException(kotlin.String,%20kotlin.Throwable,%20java.security.cert.CertPath,%20kotlin.Int)(msg: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, cause: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html!, certPath: https://developer.android.com/reference/kotlin/java/security/cert/CertPath!, index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Creates a `CertPathValidatorException` with the specified detail message, cause, certification path, and index. |
| `https://developer.android.com/reference/kotlin/java/security/cert/CertPathValidatorException#CertPathValidatorException(kotlin.String,%20kotlin.Throwable,%20java.security.cert.CertPath,%20kotlin.Int,%20java.security.cert.CertPathValidatorException.Reason)(msg: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, cause: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html!, certPath: https://developer.android.com/reference/kotlin/java/security/cert/CertPath!, index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, reason: https://developer.android.com/reference/kotlin/java/security/cert/CertPathValidatorException.Reason!)` Creates a `CertPathValidatorException` with the specified detail message, cause, certification path, index, and reason. |
| `https://developer.android.com/reference/kotlin/java/security/cert/CertPathValidatorException#CertPathValidatorException(kotlin.Throwable)(cause: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html!)` Creates a `CertPathValidatorException` that wraps the specified throwable. |

| Public methods ||
|---|---|
| open [CertPath](https://developer.android.com/reference/kotlin/java/security/cert/CertPath)! | `https://developer.android.com/reference/kotlin/java/security/cert/CertPathValidatorException#getCertPath()()` Returns the certification path that was being validated when the exception was thrown. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/security/cert/CertPathValidatorException#getIndex()()` Returns the index of the certificate in the certification path that caused the exception to be thrown. |
| open [CertPathValidatorException.Reason](https://developer.android.com/reference/kotlin/java/security/cert/CertPathValidatorException.Reason)! | `https://developer.android.com/reference/kotlin/java/security/cert/CertPathValidatorException#getReason()()` Returns the reason that the validation failed. |

## Public constructors

### CertPathValidatorException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
CertPathValidatorException()
```

Creates a `CertPathValidatorException` with no detail message.

### CertPathValidatorException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
CertPathValidatorException(msg: String!)
```

Creates a `CertPathValidatorException` with the given detail message. A detail message is a `String` that describes this particular exception.

| Parameters ||
|---|---|
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the detail message |

### CertPathValidatorException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
CertPathValidatorException(
    msg: String!, 
    cause: Throwable!)
```

Creates a `CertPathValidatorException` with the specified detail message and cause.

| Parameters ||
|---|---|
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the detail message |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!: the cause (which is saved for later retrieval by the `https://developer.android.com/reference/kotlin/java/lang/Throwable.html#getCause()` method). (A `null` value is permitted, and indicates that the cause is nonexistent or unknown.) |

### CertPathValidatorException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
CertPathValidatorException(
    msg: String!, 
    cause: Throwable!, 
    certPath: CertPath!, 
    index: Int)
```

Creates a `CertPathValidatorException` with the specified detail message, cause, certification path, and index.

| Parameters ||
|---|---|
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the detail message (or `null` if none) |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!: the cause (or `null` if none) |
| `certPath` | [CertPath](https://developer.android.com/reference/kotlin/java/security/cert/CertPath)!: the certification path that was in the process of being validated when the error was encountered |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the certificate in the certification path that caused the error (or -1 if not applicable). Note that the list of certificates in a `CertPath` is zero based. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `certPath` is `null` and `index` is not -1 |
| `java.lang.IndexOutOfBoundsException` | if the index is out of range `(index < -1 || (certPath != null && index >= certPath.getCertificates().size()) ` |

### CertPathValidatorException

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
CertPathValidatorException(
    msg: String!, 
    cause: Throwable!, 
    certPath: CertPath!, 
    index: Int, 
    reason: CertPathValidatorException.Reason!)
```

Creates a `CertPathValidatorException` with the specified detail message, cause, certification path, index, and reason.

| Parameters ||
|---|---|
| `msg` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the detail message (or `null` if none) |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!: the cause (or `null` if none) |
| `certPath` | [CertPath](https://developer.android.com/reference/kotlin/java/security/cert/CertPath)!: the certification path that was in the process of being validated when the error was encountered |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the certificate in the certification path that caused the error (or -1 if not applicable). Note that the list of certificates in a `CertPath` is zero based. |
| `reason` | [CertPathValidatorException.Reason](https://developer.android.com/reference/kotlin/java/security/cert/CertPathValidatorException.Reason)!: the reason the validation failed |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `certPath` is `null` and `index` is not -1 |
| `java.lang.IndexOutOfBoundsException` | if the index is out of range `(index < -1 || (certPath != null && index >= certPath.getCertificates().size()) ` |
| `java.lang.NullPointerException` | if `reason` is `null` |

### CertPathValidatorException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
CertPathValidatorException(cause: Throwable!)
```

Creates a `CertPathValidatorException` that wraps the specified throwable. This allows any exception to be converted into a `CertPathValidatorException`, while retaining information about the wrapped exception, which may be useful for debugging. The detail message is set to (`cause==null ? null : cause.toString()`) (which typically contains the class and detail message of cause).

| Parameters ||
|---|---|
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!: the cause (which is saved for later retrieval by the `https://developer.android.com/reference/kotlin/java/lang/Throwable.html#getCause()` method). (A `null` value is permitted, and indicates that the cause is nonexistent or unknown.) |

## Public methods

### getCertPath

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCertPath(): CertPath!
```

Returns the certification path that was being validated when the exception was thrown.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/security/cert/CertPath!` | the `CertPath` that was being validated when the exception was thrown (or `null` if not specified) |

### getIndex

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getIndex(): Int
```

Returns the index of the certificate in the certification path that caused the exception to be thrown. Note that the list of certificates in a `CertPath` is zero based. If no index has been set, -1 is returned.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the index that has been set, or -1 if none has been set |

### getReason

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getReason(): CertPathValidatorException.Reason!
```

Returns the reason that the validation failed. The reason is associated with the index of the certificate returned by `https://developer.android.com/reference/kotlin/java/security/cert/CertPathValidatorException#getIndex()`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/security/cert/CertPathValidatorException.Reason!` | the reason that the validation failed, or `BasicReason.UNSPECIFIED` if a reason has not been specified |
