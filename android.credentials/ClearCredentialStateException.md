# ClearCredentialStateException

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ClearCredentialStateException

Kotlin| [Java](https://developer.android.com/reference/android/credentials/ClearCredentialStateException "View this page in Java") 

```
open class ClearCredentialStateException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||
| | | ↳ | [android.credentials.ClearCredentialStateException](https://developer.android.com/reference/kotlin/android/credentials/ClearCredentialStateException#) |

Represents an error encountered during the [CredentialManager.clearCredentialState(ClearCredentialStateRequest,](https://developer.android.com/reference/kotlin/android/credentials/CredentialManager#clearCredentialState(android.credentials.ClearCredentialStateRequest,%20android.os.CancellationSignal,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver))operation.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TYPE_UNKNOWN](https://developer.android.com/reference/kotlin/android/credentials/ClearCredentialStateException#TYPE_UNKNOWN:kotlin.String) The error type value for when the given operation failed due to an unknown reason. |

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ClearCredentialStateException](https://developer.android.com/reference/kotlin/android/credentials/ClearCredentialStateException#ClearCredentialStateException(kotlin.String))`(`type:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Constructs a [ClearCredentialStateException](https://developer.android.com/reference/kotlin/android/credentials/ClearCredentialStateException#). |
| [ClearCredentialStateException](https://developer.android.com/reference/kotlin/android/credentials/ClearCredentialStateException#ClearCredentialStateException(kotlin.String,%20kotlin.String))`(`type:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Constructs a [ClearCredentialStateException](https://developer.android.com/reference/kotlin/android/credentials/ClearCredentialStateException#). |
| [ClearCredentialStateException](https://developer.android.com/reference/kotlin/android/credentials/ClearCredentialStateException#ClearCredentialStateException(kotlin.String,%20kotlin.String,%20kotlin.Throwable))`(`type:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?`)` Constructs a [ClearCredentialStateException](https://developer.android.com/reference/kotlin/android/credentials/ClearCredentialStateException#). |
| [ClearCredentialStateException](https://developer.android.com/reference/kotlin/android/credentials/ClearCredentialStateException#ClearCredentialStateException(kotlin.String,%20kotlin.Throwable))`(`type:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?`)` Constructs a [ClearCredentialStateException](https://developer.android.com/reference/kotlin/android/credentials/ClearCredentialStateException#). |

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getType](https://developer.android.com/reference/kotlin/android/credentials/ClearCredentialStateException#getType())`()` Returns the specific exception type. |

## Constants

### TYPE_UNKNOWN

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_UNKNOWN: String
```

The error type value for when the given operation failed due to an unknown reason. 

 Value: "android.credentials.ClearCredentialStateException.TYPE_UNKNOWN"

## Public constructors

### ClearCredentialStateException

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ClearCredentialStateException(type: String)
```

Constructs a [ClearCredentialStateException](https://developer.android.com/reference/kotlin/android/credentials/ClearCredentialStateException#).

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------|
| `type` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|-------------------|
| `java.lang.IllegalArgumentException` | If type is empty. |

### ClearCredentialStateException

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ClearCredentialStateException(
    type: String, 
    message: String?)
```

Constructs a [ClearCredentialStateException](https://developer.android.com/reference/kotlin/android/credentials/ClearCredentialStateException#).

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------|
| `type` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:This value may be`null`. |

| Exceptions ||
|--------------------------------------|-------------------|
| `java.lang.IllegalArgumentException` | If type is empty. |

### ClearCredentialStateException

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ClearCredentialStateException(
    type: String, 
    message: String?, 
    cause: Throwable?)
```

Constructs a [ClearCredentialStateException](https://developer.android.com/reference/kotlin/android/credentials/ClearCredentialStateException#).

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------|
| `type` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:This value may be`null`. |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?:This value may be`null`. |

| Exceptions ||
|--------------------------------------|-------------------|
| `java.lang.IllegalArgumentException` | If type is empty. |

### ClearCredentialStateException

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ClearCredentialStateException(
    type: String, 
    cause: Throwable?)
```

Constructs a [ClearCredentialStateException](https://developer.android.com/reference/kotlin/android/credentials/ClearCredentialStateException#).

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------|
| `type` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?:This value may be`null`. |

| Exceptions ||
|--------------------------------------|-------------------|
| `java.lang.IllegalArgumentException` | If type is empty. |

## Public methods

### getType

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getType(): String
```

Returns the specific exception type.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |
