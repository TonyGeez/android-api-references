# GetCredentialException

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GetCredentialException

Kotlin | [Java](GetCredentialException.md) 
| --- | --- |

```
open class GetCredentialException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) ||
| | | ↳ | [android.credentials.GetCredentialException](GetCredentialException.md) |
| --- | --- | --- | --- |

Represents an error encountered during the [CredentialManager.getCredential(Context, GetCredentialRequest,](CredentialManager.md)) operation.

## Summary

| Constants ||
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TYPE_INTERRUPTED](GetCredentialException.md) The error type value for when the given operation failed due to internal interruption. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TYPE_NO_CREDENTIAL](GetCredentialException.md) The error type value for when no credential is found available for the given [android.credentials.CredentialManager#getCredential(android.content.Context,android.credentials.GetCredentialRequest,android.os.CancellationSignal,java.util.concurrent.Executor,android.os.OutcomeReceiver)](CredentialManager.md)) request. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TYPE_UNKNOWN](GetCredentialException.md) The error type value for when the given operation failed due to an unknown reason. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TYPE_USER_CANCELED](GetCredentialException.md) The error type value for when the user intentionally cancelled the request. |

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [GetCredentialException](GetCredentialException.md))`(`type:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Constructs a [GetCredentialException](GetCredentialException.md). |
| [GetCredentialException](GetCredentialException.md))`(`type:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Constructs a [GetCredentialException](GetCredentialException.md). |
| [GetCredentialException](GetCredentialException.md))`(`type:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?`)` Constructs a [GetCredentialException](GetCredentialException.md). |
| [GetCredentialException](GetCredentialException.md))`(`type:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?`)` Constructs a [GetCredentialException](GetCredentialException.md). |

| Public methods ||
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getType](GetCredentialException.md))`()` Returns the specific exception type. |

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

The error type value for when no credential is found available for the given [android.credentials.CredentialManager#getCredential(android.content.Context,android.credentials.GetCredentialRequest,android.os.CancellationSignal,java.util.concurrent.Executor,android.os.OutcomeReceiver)](CredentialManager.md)) request. 

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

Constructs a [GetCredentialException](GetCredentialException.md).

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

Constructs a [GetCredentialException](GetCredentialException.md).

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

Constructs a [GetCredentialException](GetCredentialException.md).

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------|
| `type` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?: This value may be `null`. |
| --- | --- |

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

Constructs a [GetCredentialException](GetCredentialException.md).

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
