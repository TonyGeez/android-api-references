# BackendBusyException

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BackendBusyException

Kotlin| [Java](https://developer.android.com/reference/android/security/keystore/BackendBusyException "View this page in Java") 

```
open class BackendBusyException : ProviderException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||||
| | | ↳ | [java.lang.RuntimeException](https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#) |||
| | | | ↳ | [java.security.ProviderException](https://developer.android.com/reference/kotlin/java/security/ProviderException.html#) ||
| | | | | ↳ | [android.security.keystore.BackendBusyException](https://developer.android.com/reference/kotlin/android/security/keystore/BackendBusyException#) |

Indicates a transient error that prevented a key operation from being created. Callers should try again with a back-off period of [getBackOffHintMillis()](https://developer.android.com/reference/kotlin/android/security/keystore/BackendBusyException#getBackOffHintMillis())milliseconds.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [BackendBusyException](https://developer.android.com/reference/kotlin/android/security/keystore/BackendBusyException#BackendBusyException(kotlin.Long))`(`backOffHintMillis:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Constructs a new`BackendBusyException`without detail message and cause. |
| [BackendBusyException](https://developer.android.com/reference/kotlin/android/security/keystore/BackendBusyException#BackendBusyException(kotlin.Long,%20kotlin.String))`(`backOffHintMillis:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Constructs a new`BackendBusyException`with the provided detail message and no cause. |
| [BackendBusyException](https://developer.android.com/reference/kotlin/android/security/keystore/BackendBusyException#BackendBusyException(kotlin.Long,%20kotlin.String,%20kotlin.Throwable))`(`backOffHintMillis:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)`)` Constructs a new`BackendBusyException`with the provided detail message and cause. |

| Public methods ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getBackOffHintMillis](https://developer.android.com/reference/kotlin/android/security/keystore/BackendBusyException#getBackOffHintMillis())`()` When retrying to start a Keystore operation after receiving this exception, this can be used to determine how long to wait before retrying. |

## Public constructors

### BackendBusyException

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BackendBusyException(backOffHintMillis: Long)
```

Constructs a new`BackendBusyException`without detail message and cause.

| Parameters ||
|---------------------|--------------------------------------------------------------------------------------------------------------------------------|
| `backOffHintMillis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):Value is a non-negative duration in milliseconds. |

### BackendBusyException

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BackendBusyException(
    backOffHintMillis: Long, 
    message: String)
```

Constructs a new`BackendBusyException`with the provided detail message and no cause.

| Parameters ||
|---------------------|--------------------------------------------------------------------------------------------------------------------------------|
| `backOffHintMillis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):Value is a non-negative duration in milliseconds. |
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |

### BackendBusyException

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BackendBusyException(
    backOffHintMillis: Long, 
    message: String, 
    cause: Throwable)
```

Constructs a new`BackendBusyException`with the provided detail message and cause.

| Parameters ||
|---------------------|--------------------------------------------------------------------------------------------------------------------------------|
| `backOffHintMillis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):Value is a non-negative duration in milliseconds. |
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html):This value cannot be`null`. |

## Public methods

### getBackOffHintMillis

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getBackOffHintMillis(): Long
```

When retrying to start a Keystore operation after receiving this exception, this can be used to determine how long to wait before retrying. It is not guaranteed that the operation will succeeds after this time. Multiple retries may be necessary if the system is congested. 
Value is a non-negative duration in milliseconds.

| Return ||
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | Number of milliseconds to back off before retrying. Value is a non-negative duration in milliseconds. |
