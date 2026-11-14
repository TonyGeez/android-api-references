# CreateCredentialException

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CreateCredentialException

Kotlin| [Java](CreateCredentialException.md) 
| --- | --- |

```
open class CreateCredentialException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) ||
| | | ↳ | [android.credentials.CreateCredentialException](CreateCredentialException.md) |
| --- | --- | --- | --- |

Represents an error encountered during the [CredentialManager.createCredential(Context, CreateCredentialRequest,](CredentialManager.md))operation.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TYPE_INTERRUPTED](CreateCredentialException.md) The error type value for when the given operation failed due to internal interruption. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TYPE_NO_CREATE_OPTIONS](CreateCredentialException.md) The error type value for when no create options are available from any provider(s), for the given [CredentialManager.createCredential(Context, CreateCredentialRequest,](CredentialManager.md))request. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TYPE_UNKNOWN](CreateCredentialException.md) The error type value for when the given operation failed due to an unknown reason. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TYPE_USER_CANCELED](CreateCredentialException.md) The error type value for when the user intentionally cancelled the request. |

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CreateCredentialException](CreateCredentialException.md))`(`type:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Constructs a [CreateCredentialException](CreateCredentialException.md). |
| [CreateCredentialException](CreateCredentialException.md))`(`type:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Constructs a [CreateCredentialException](CreateCredentialException.md). |
| [CreateCredentialException](CreateCredentialException.md))`(`type:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?`)` Constructs a [CreateCredentialException](CreateCredentialException.md). |
| [CreateCredentialException](CreateCredentialException.md))`(`type:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?`)` Constructs a [CreateCredentialException](CreateCredentialException.md). |

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getType](CreateCredentialException.md))`()` Returns the specific exception type. |

## Constants

### TYPE_INTERRUPTED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_INTERRUPTED: String
```

The error type value for when the given operation failed due to internal interruption. Retrying the same operation should fix the error. 

 Value: "android.credentials.CreateCredentialException.TYPE_INTERRUPTED"

### TYPE_NO_CREATE_OPTIONS

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_NO_CREATE_OPTIONS: String
```

The error type value for when no create options are available from any provider(s), for the given [CredentialManager.createCredential(Context, CreateCredentialRequest,](CredentialManager.md))request. 

 Value: "android.credentials.CreateCredentialException.TYPE_NO_CREATE_OPTIONS"

### TYPE_UNKNOWN

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_UNKNOWN: String
```

The error type value for when the given operation failed due to an unknown reason. 

 Value: "android.credentials.CreateCredentialException.TYPE_UNKNOWN"

### TYPE_USER_CANCELED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_USER_CANCELED: String
```

The error type value for when the user intentionally cancelled the request.

This is a strong indicator that your app should refrain from making the same api call for a certain amount of time to provide a better user experience. 

 Value: "android.credentials.CreateCredentialException.TYPE_USER_CANCELED"

## Public constructors

### CreateCredentialException

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CreateCredentialException(type: String)
```

Constructs a [CreateCredentialException](CreateCredentialException.md).

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------|
| `type` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|-------------------|
| `java.lang.IllegalArgumentException` | If type is empty. |

### CreateCredentialException

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CreateCredentialException(
    type: String, 
    message: String?)
```

Constructs a [CreateCredentialException](CreateCredentialException.md).

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------|
| `type` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:This value may be`null`. |

| Exceptions ||
|--------------------------------------|-------------------|
| `java.lang.IllegalArgumentException` | If type is empty. |

### CreateCredentialException

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CreateCredentialException(
    type: String, 
    message: String?, 
    cause: Throwable?)
```

Constructs a [CreateCredentialException](CreateCredentialException.md).

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------|
| `type` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:This value may be`null`. |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?:This value may be`null`. |
| --- | --- |

| Exceptions ||
|--------------------------------------|-------------------|
| `java.lang.IllegalArgumentException` | If type is empty. |

### CreateCredentialException

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CreateCredentialException(
    type: String, 
    cause: Throwable?)
```

Constructs a [CreateCredentialException](CreateCredentialException.md).

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
