# RequestSurfacePackageException

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RequestSurfacePackageException

Kotlin| [Java](RequestSurfacePackageException.md) 
| --- | --- |

```
class RequestSurfacePackageException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) ||
| | | ↳ | [android.app.sdksandbox.RequestSurfacePackageException](RequestSurfacePackageException.md) |
| --- | --- | --- | --- |

| **This exception was deprecated in API level 35.**
|
| Exception is used at [SdkSandboxManager.requestSurfacePackage](SdkSandboxManager.md))which is getting deprecated.

Exception thrown by [SdkSandboxManager.requestSurfacePackage](SdkSandboxManager.md))

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [RequestSurfacePackageException](RequestSurfacePackageException.md))`(`requestSurfacePackageErrorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Initializes a [RequestSurfacePackageException](RequestSurfacePackageException.md) with a result code and a message |
| [RequestSurfacePackageException](RequestSurfacePackageException.md))`(`requestSurfacePackageErrorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?`)` Initializes a [RequestSurfacePackageException](RequestSurfacePackageException.md) with a result code, a message and a cause. |
| [RequestSurfacePackageException](RequestSurfacePackageException.md))`(`requestSurfacePackageErrorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?`, `extraInfo:` ` [Bundle](../android.os/Bundle.md)`)` Initializes a [RequestSurfacePackageException](RequestSurfacePackageException.md) with a result code, a message, a cause and extra information. |

| Public methods ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Bundle](../android.os/Bundle.md) | [getExtraErrorInformation](RequestSurfacePackageException.md))`()` Returns the extra error information this exception was constructed with. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRequestSurfacePackageErrorCode](RequestSurfacePackageException.md))`()` Returns the result code this exception was constructed with. |

## Public constructors

### RequestSurfacePackageException

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 

```
RequestSurfacePackageException(
    requestSurfacePackageErrorCode: Int, 
    message: String?)
```

Initializes a [RequestSurfacePackageException](RequestSurfacePackageException.md) with a result code and a message

| Parameters ||
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `requestSurfacePackageErrorCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The result code. Value is [android.app.sdksandbox.SdkSandboxManager#REQUEST_SURFACE_PACKAGE_INTERNAL_ERROR](SdkSandboxManager.md), or [android.app.sdksandbox.SdkSandboxManager#REQUEST_SURFACE_PACKAGE_SDK_NOT_LOADED](SdkSandboxManager.md) |
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The detailed message which is saved for later retrieval by the [getMessage()](../java.lang/Throwable.md))method. This value may be`null`. |

### RequestSurfacePackageException

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 

```
RequestSurfacePackageException(
    requestSurfacePackageErrorCode: Int, 
    message: String?, 
    cause: Throwable?)
```

Initializes a [RequestSurfacePackageException](RequestSurfacePackageException.md) with a result code, a message and a cause.

| Parameters ||
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `requestSurfacePackageErrorCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The result code. Value is [android.app.sdksandbox.SdkSandboxManager#REQUEST_SURFACE_PACKAGE_INTERNAL_ERROR](SdkSandboxManager.md), or [android.app.sdksandbox.SdkSandboxManager#REQUEST_SURFACE_PACKAGE_SDK_NOT_LOADED](SdkSandboxManager.md) |
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The detailed message which is saved for later retrieval by the [getMessage()](../java.lang/Throwable.md))method. This value may be`null`. |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?:The cause of the exception, which is saved for later retrieval by the [getCause()](../java.lang/Throwable.md))method. A null value is permitted, and indicates that the cause is nonexistent or unknown. |
| --- | --- |

### RequestSurfacePackageException

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 

```
RequestSurfacePackageException(
    requestSurfacePackageErrorCode: Int, 
    message: String?, 
    cause: Throwable?, 
    extraInfo: Bundle)
```

Initializes a [RequestSurfacePackageException](RequestSurfacePackageException.md) with a result code, a message, a cause and extra information.

| Parameters ||
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `requestSurfacePackageErrorCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The result code. Value is [android.app.sdksandbox.SdkSandboxManager#REQUEST_SURFACE_PACKAGE_INTERNAL_ERROR](SdkSandboxManager.md), or [android.app.sdksandbox.SdkSandboxManager#REQUEST_SURFACE_PACKAGE_SDK_NOT_LOADED](SdkSandboxManager.md) |
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The detailed message which is saved for later retrieval by the [getMessage()](../java.lang/Throwable.md))method. This value may be`null`. |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?:The cause of the exception, which is saved for later retrieval by the [getCause()](../java.lang/Throwable.md))method. A null value is permitted, and indicates that the cause is nonexistent or unknown. |
| --- | --- |
| `extraInfo` | [Bundle](../android.os/Bundle.md):Extra error information. This is empty if there is no such information. This value cannot be`null`. |

## Public methods

### getExtraErrorInformation

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getExtraErrorInformation(): Bundle
```

**Deprecated:** *Deprecated in Java.*

Returns the extra error information this exception was constructed with.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [Bundle](../android.os/Bundle.md) | The extra error information Bundle. This value cannot be`null`. |

### getRequestSurfacePackageErrorCode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRequestSurfacePackageErrorCode(): Int
```

**Deprecated:** *Deprecated in Java.*

Returns the result code this exception was constructed with.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The result code from [SdkSandboxManager.requestSurfacePackage](SdkSandboxManager.md))Value is [android.app.sdksandbox.SdkSandboxManager#REQUEST_SURFACE_PACKAGE_INTERNAL_ERROR](SdkSandboxManager.md), or [android.app.sdksandbox.SdkSandboxManager#REQUEST_SURFACE_PACKAGE_SDK_NOT_LOADED](SdkSandboxManager.md) |
