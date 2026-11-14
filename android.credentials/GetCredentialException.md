# GetCredentialException

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GetCredentialException

Kotlin | [Java](https://developer.android.com/reference/android/credentials/GetCredentialException "View this page in Java") 

```
open class GetCredentialException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||
| | | ↳ | [android.credentials.GetCredentialException](https://developer.android.com/reference/kotlin/android/credentials/GetCredentialException#) |

Represents an error encountered during the [CredentialManager.getCredential(Context, GetCredentialRequest,](https://developer.android.com/reference/kotlin/android/credentials/CredentialManager#getCredential(android.content.Context,%20android.credentials.GetCredentialRequest,%20android.os.CancellationSignal,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)) operation.

## Summary

| Constants ||
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TYPE_INTERRUPTED](https://developer.android.com/reference/kotlin/android/credentials/GetCredentialException#TYPE_INTERRUPTED:kotlin.String) The error type value for when the given operation failed due to internal interruption. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TYPE_NO_CREDENTIAL](https://developer.android.com/reference/kotlin/android/credentials/GetCredentialException#TYPE_NO_CREDENTIAL:kotlin.String) The error type value for when no credential is found available for the given [android.credentials.CredentialManager#getCredential(android.content.Context,android.credentials.GetCredentialRequest,android.os.CancellationSignal,java.util.concurrent.Executor,android.os.OutcomeReceiver)](https://developer.android.com/reference/kotlin/android/credentials/CredentialManager#getCredential(android.content.Context,%20android.credentials.GetCredentialRequest,%20android.os.CancellationSignal,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)) request. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TYPE_UNKNOWN](https://developer.android.com/reference/kotlin/android/credentials/GetCredentialException#TYPE_UNKNOWN:kotlin.String) The error type value for when the given operation failed due to an unknown reason. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TYPE_USER_CANCELED](https://developer.android.com/reference/kotlin/android/credentials/GetCredentialException#TYPE_USER_CANCELED:kotlin.String) The error type value for when the user intentionally cancelled the request. |

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [GetCredentialException](https://developer.android.com/reference/kotlin/android/credentials/GetCredentialException#GetCredentialException(kotlin.String))`(`type:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Constructs a [GetCredentialException](https://developer.android.com/reference/kotlin/android/credentials/GetCredentialException#). |
| [GetCredentialException](https://developer.android.com/reference/kotlin/android/credentials/GetCredentialException#GetCredentialException(kotlin.String,%20kotlin.String))`(`type:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Constructs a [GetCredentialException](https://developer.android.com/reference/kotlin/android/credentials/GetCredentialException#). |
| [GetCredentialException](https://developer.android.com/reference/kotlin/android/credentials/GetCredentialException#GetCredentialException(kotlin.String,%20kotlin.String,%20kotlin.Throwable))`(`type:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?`)` Constructs a [GetCredentialException](https://developer.android.com/reference/kotlin/android/credentials/GetCredentialException#). |
| [GetCredentialException](https://developer.android.com/reference/kotlin/android/credentials/GetCredentialException#GetCredentialException(kotlin.String,%20kotlin.Throwable))`(`type:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?`)` Constructs a [GetCredentialException](https://developer.android.com/reference/kotlin/android/credentials/GetCredentialException#). |

| Public methods ||
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getType](https://developer.android.com/reference/kotlin/android/credentials/GetCredentialException#getType())`()` Returns the specific exception type. |

## Constants

### TYPE_INTERRUPTED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_INTERRUPTED: String
```

The error type value for when the given operation failed due to internal interruption. Retrying the same operation should fix the error. 

 Value: "android.credentials.GetCredentialException.TYPE_INTERRUPTED"

### TYPE_NO_CREDENTIAL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_NO_CREDENTIAL: String
```

The error type value for when no credential is found available for the given [android.credentials.CredentialManager#getCredential(android.content.Context,android.credentials.GetCredentialRequest,android.os.CancellationSignal,java.util.concurrent.Executor,android.os.OutcomeReceiver)](https://developer.android.com/reference/kotlin/android/credentials/CredentialManager#getCredential(android.content.Context,%20android.credentials.GetCredentialRequest,%20android.os.CancellationSignal,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)) request. 

 Value: "android.credentials.GetCredentialException.TYPE_NO_CREDENTIAL"

### TYPE_UNKNOWN

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_UNKNOWN: String
```

The error type value for when the given operation failed due to an unknown reason. 

 Value: "android.credentials.GetCredentialException.TYPE_UNKNOWN"

### TYPE_USER_CANCELED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_USER_CANCELED: String
```

The error type value for when the user intentionally cancelled the request.

This is a strong indicator that your app should refrain from making the same api call for a certain amount of time to provide a better user experience. 

 Value: "android.credentials.GetCredentialException.TYPE_USER_CANCELED"

## Public constructors

### GetCredentialException

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
GetCredentialException(type: String)
```

Constructs a [GetCredentialException](https://developer.android.com/reference/kotlin/android/credentials/GetCredentialException#).

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------|
| `type` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

| Exceptions ||
|--------------------------------------|-------------------|
| `java.lang.IllegalArgumentException` | If type is empty. |

### GetCredentialException

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
GetCredentialException(
    type: String, 
    message: String?)
```

Constructs a [GetCredentialException](https://developer.android.com/reference/kotlin/android/credentials/GetCredentialException#).

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------|
| `type` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |

| Exceptions ||
|--------------------------------------|-------------------|
| `java.lang.IllegalArgumentException` | If type is empty. |

### GetCredentialException

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
GetCredentialException(
    type: String, 
    message: String?, 
    cause: Throwable?)
```

Constructs a [GetCredentialException](https://developer.android.com/reference/kotlin/android/credentials/GetCredentialException#).

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------|
| `type` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?: This value may be `null`. |

| Exceptions ||
|--------------------------------------|-------------------|
| `java.lang.IllegalArgumentException` | If type is empty. |

### GetCredentialException

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
GetCredentialException(
    type: String, 
    cause: Throwable?)
```

Constructs a [GetCredentialException](https://developer.android.com/reference/kotlin/android/credentials/GetCredentialException#).

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------|
| `type` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?: This value may be `null`. |

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
|----------------------------------------------------------------------------------|------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be `null`. |
