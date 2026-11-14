# ClearCredentialStateException

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ClearCredentialStateException

Kotlin| [Java](../android/credentials/ClearCredentialStateException.md) 
| --- | --- |

```
open class ClearCredentialStateException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) ||
| | | ↳ | [android.credentials.ClearCredentialStateException](../android/credentials/ClearCredentialStateException.md) |
| --- | --- | --- | --- |

Represents an error encountered during the [CredentialManager.clearCredentialState(ClearCredentialStateRequest,](../android/credentials/CredentialManager.md))operation.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TYPE_UNKNOWN](../android/credentials/ClearCredentialStateException.md) The error type value for when the given operation failed due to an unknown reason. |

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ClearCredentialStateException](../android/credentials/ClearCredentialStateException.md))`(`type:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Constructs a [ClearCredentialStateException](../android/credentials/ClearCredentialStateException.md). |
| [ClearCredentialStateException](../android/credentials/ClearCredentialStateException.md))`(`type:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Constructs a [ClearCredentialStateException](../android/credentials/ClearCredentialStateException.md). |
| [ClearCredentialStateException](../android/credentials/ClearCredentialStateException.md))`(`type:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?`)` Constructs a [ClearCredentialStateException](../android/credentials/ClearCredentialStateException.md). |
| [ClearCredentialStateException](../android/credentials/ClearCredentialStateException.md))`(`type:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?`)` Constructs a [ClearCredentialStateException](../android/credentials/ClearCredentialStateException.md). |

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getType](../android/credentials/ClearCredentialStateException.md))`()` Returns the specific exception type. |

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

Constructs a [ClearCredentialStateException](../android/credentials/ClearCredentialStateException.md).

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

Constructs a [ClearCredentialStateException](../android/credentials/ClearCredentialStateException.md).

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

Constructs a [ClearCredentialStateException](../android/credentials/ClearCredentialStateException.md).

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------|
| `type` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:This value may be`null`. |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?:This value may be`null`. |
| --- | --- |

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

Constructs a [ClearCredentialStateException](../android/credentials/ClearCredentialStateException.md).

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
