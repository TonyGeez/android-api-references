# RequestSurfacePackageException

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RequestSurfacePackageException

Kotlin| [Java](https://developer.android.com/reference/android/app/sdksandbox/RequestSurfacePackageException "View this page in Java") 
| --- | --- |

```
class RequestSurfacePackageException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||
| | | ↳ | [android.app.sdksandbox.RequestSurfacePackageException](https://developer.android.com/reference/kotlin/android/app/sdksandbox/RequestSurfacePackageException#) |
| --- | --- | --- | --- |

| **This exception was deprecated in API level 35.**
|
| Exception is used at [SdkSandboxManager.requestSurfacePackage](https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#requestSurfacePackage(kotlin.String,%20android.os.Bundle,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver))which is getting deprecated.

Exception thrown by [SdkSandboxManager.requestSurfacePackage](https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#requestSurfacePackage(kotlin.String,%20android.os.Bundle,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver))

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [RequestSurfacePackageException](https://developer.android.com/reference/kotlin/android/app/sdksandbox/RequestSurfacePackageException#RequestSurfacePackageException(kotlin.Int,%20kotlin.String))`(`requestSurfacePackageErrorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Initializes a [RequestSurfacePackageException](https://developer.android.com/reference/kotlin/android/app/sdksandbox/RequestSurfacePackageException#) with a result code and a message |
| [RequestSurfacePackageException](https://developer.android.com/reference/kotlin/android/app/sdksandbox/RequestSurfacePackageException#RequestSurfacePackageException(kotlin.Int,%20kotlin.String,%20kotlin.Throwable))`(`requestSurfacePackageErrorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?`)` Initializes a [RequestSurfacePackageException](https://developer.android.com/reference/kotlin/android/app/sdksandbox/RequestSurfacePackageException#) with a result code, a message and a cause. |
| [RequestSurfacePackageException](https://developer.android.com/reference/kotlin/android/app/sdksandbox/RequestSurfacePackageException#RequestSurfacePackageException(kotlin.Int,%20kotlin.String,%20kotlin.Throwable,%20android.os.Bundle))`(`requestSurfacePackageErrorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?`, `extraInfo:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)`)` Initializes a [RequestSurfacePackageException](https://developer.android.com/reference/kotlin/android/app/sdksandbox/RequestSurfacePackageException#) with a result code, a message, a cause and extra information. |

| Public methods ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) | [getExtraErrorInformation](https://developer.android.com/reference/kotlin/android/app/sdksandbox/RequestSurfacePackageException#getExtraErrorInformation())`()` Returns the extra error information this exception was constructed with. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRequestSurfacePackageErrorCode](https://developer.android.com/reference/kotlin/android/app/sdksandbox/RequestSurfacePackageException#getRequestSurfacePackageErrorCode())`()` Returns the result code this exception was constructed with. |

## Public constructors

### RequestSurfacePackageException

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 

```
RequestSurfacePackageException(
    requestSurfacePackageErrorCode: Int, 
    message: String?)
```

Initializes a [RequestSurfacePackageException](https://developer.android.com/reference/kotlin/android/app/sdksandbox/RequestSurfacePackageException#) with a result code and a message

| Parameters ||
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `requestSurfacePackageErrorCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The result code. Value is [android.app.sdksandbox.SdkSandboxManager#REQUEST_SURFACE_PACKAGE_INTERNAL_ERROR](https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#REQUEST_SURFACE_PACKAGE_INTERNAL_ERROR:kotlin.Int), or [android.app.sdksandbox.SdkSandboxManager#REQUEST_SURFACE_PACKAGE_SDK_NOT_LOADED](https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#REQUEST_SURFACE_PACKAGE_SDK_NOT_LOADED:kotlin.Int) |
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The detailed message which is saved for later retrieval by the [getMessage()](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#getMessage())method. This value may be`null`. |

### RequestSurfacePackageException

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 4](https://developer.android.com/sdkExtensions) 

```
RequestSurfacePackageException(
    requestSurfacePackageErrorCode: Int, 
    message: String?, 
    cause: Throwable?)
```

Initializes a [RequestSurfacePackageException](https://developer.android.com/reference/kotlin/android/app/sdksandbox/RequestSurfacePackageException#) with a result code, a message and a cause.

| Parameters ||
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `requestSurfacePackageErrorCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The result code. Value is [android.app.sdksandbox.SdkSandboxManager#REQUEST_SURFACE_PACKAGE_INTERNAL_ERROR](https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#REQUEST_SURFACE_PACKAGE_INTERNAL_ERROR:kotlin.Int), or [android.app.sdksandbox.SdkSandboxManager#REQUEST_SURFACE_PACKAGE_SDK_NOT_LOADED](https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#REQUEST_SURFACE_PACKAGE_SDK_NOT_LOADED:kotlin.Int) |
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The detailed message which is saved for later retrieval by the [getMessage()](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#getMessage())method. This value may be`null`. |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?:The cause of the exception, which is saved for later retrieval by the [getCause()](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#getCause())method. A null value is permitted, and indicates that the cause is nonexistent or unknown. |
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

Initializes a [RequestSurfacePackageException](https://developer.android.com/reference/kotlin/android/app/sdksandbox/RequestSurfacePackageException#) with a result code, a message, a cause and extra information.

| Parameters ||
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `requestSurfacePackageErrorCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The result code. Value is [android.app.sdksandbox.SdkSandboxManager#REQUEST_SURFACE_PACKAGE_INTERNAL_ERROR](https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#REQUEST_SURFACE_PACKAGE_INTERNAL_ERROR:kotlin.Int), or [android.app.sdksandbox.SdkSandboxManager#REQUEST_SURFACE_PACKAGE_SDK_NOT_LOADED](https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#REQUEST_SURFACE_PACKAGE_SDK_NOT_LOADED:kotlin.Int) |
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The detailed message which is saved for later retrieval by the [getMessage()](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#getMessage())method. This value may be`null`. |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?:The cause of the exception, which is saved for later retrieval by the [getCause()](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#getCause())method. A null value is permitted, and indicates that the cause is nonexistent or unknown. |
| --- | --- |
| `extraInfo` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#):Extra error information. This is empty if there is no such information. This value cannot be`null`. |

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
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) | The extra error information Bundle. This value cannot be`null`. |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The result code from [SdkSandboxManager.requestSurfacePackage](https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#requestSurfacePackage(kotlin.String,%20android.os.Bundle,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver))Value is [android.app.sdksandbox.SdkSandboxManager#REQUEST_SURFACE_PACKAGE_INTERNAL_ERROR](https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#REQUEST_SURFACE_PACKAGE_INTERNAL_ERROR:kotlin.Int), or [android.app.sdksandbox.SdkSandboxManager#REQUEST_SURFACE_PACKAGE_SDK_NOT_LOADED](https://developer.android.com/reference/kotlin/android/app/sdksandbox/SdkSandboxManager#REQUEST_SURFACE_PACKAGE_SDK_NOT_LOADED:kotlin.Int) |
