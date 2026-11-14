# Violation

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Violation

Kotlin| [Java](Violation.md) 
| --- | --- |

```
abstract class Violation : Throwable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||
| | ↳ | [android.os.strictmode.Violation](Violation.md) |

| Known Direct Subclasses [CleartextNetworkViolation](CleartextNetworkViolation.md), [ContentUriWithoutPermissionViolation](ContentUriWithoutPermissionViolation.md), [CredentialProtectedWhileLockedViolation](CredentialProtectedWhileLockedViolation.md), [CustomViolation](CustomViolation.md), [DiskReadViolation](DiskReadViolation.md), [DiskWriteViolation](DiskWriteViolation.md), [ExplicitGcViolation](ExplicitGcViolation.md), [FileUriExposedViolation](FileUriExposedViolation.md), [ImplicitDirectBootViolation](ImplicitDirectBootViolation.md), [IncorrectContextUseViolation](IncorrectContextUseViolation.md), [InstanceCountViolation](InstanceCountViolation.md), [IntentReceiverLeakedViolation](IntentReceiverLeakedViolation.md), and 10 others. |-------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [CleartextNetworkViolation](CleartextNetworkViolation.md) | <br /> | | [ContentUriWithoutPermissionViolation](ContentUriWithoutPermissionViolation.md) | <br /> | | [CredentialProtectedWhileLockedViolation](CredentialProtectedWhileLockedViolation.md) | Subclass of`Violation`that is used when a process accesses filesystem paths stored in credential protected storage areas while the user is locked. | | [CustomViolation](CustomViolation.md) | <br /> | | [DiskReadViolation](DiskReadViolation.md) | <br /> | | [DiskWriteViolation](DiskWriteViolation.md) | <br /> | | [ExplicitGcViolation](ExplicitGcViolation.md) | See # [android.os.StrictMode.ThreadPolicy.Builder#detectExplicitGc()](../android/os/StrictMode.ThreadPolicy.Builder.md)). | | [FileUriExposedViolation](FileUriExposedViolation.md) | <br /> | | [ImplicitDirectBootViolation](ImplicitDirectBootViolation.md) | Subclass of`Violation`that is used when a process implicitly relies on automatic Direct Boot filtering. | | [IncorrectContextUseViolation](IncorrectContextUseViolation.md) | Incorrect usage of [Context](../android.content/Context.md), such as obtaining a UI service from non-UI [Context](../android.content/Context.md) instance. | | [InstanceCountViolation](InstanceCountViolation.md) | <br /> | | [IntentReceiverLeakedViolation](IntentReceiverLeakedViolation.md) | <br /> | | [LeakedClosableViolation](LeakedClosableViolation.md) | <br /> | | [NetworkViolation](NetworkViolation.md) | <br /> | | [NonSdkApiUsedViolation](NonSdkApiUsedViolation.md) | Subclass of`Violation`that is used when a process accesses a non SDK API. | | [ResourceMismatchViolation](ResourceMismatchViolation.md) | <br /> | | [ServiceConnectionLeakedViolation](ServiceConnectionLeakedViolation.md) | <br /> | | [SqliteObjectLeakedViolation](SqliteObjectLeakedViolation.md) | <br /> | | [UnbufferedIoViolation](UnbufferedIoViolation.md) | See # [Builder.detectUnbufferedIo()](../android/os/StrictMode.ThreadPolicy.Builder.md)) | | [UnsafeIntentLaunchViolation](UnsafeIntentLaunchViolation.md) | Violation raised when your app launches an [Intent](../android.content/Intent.md) which originated from outside your app. | | [UntaggedSocketViolation](UntaggedSocketViolation.md) | <br /> | | [WebViewMethodCalledOnWrongThreadViolation](WebViewMethodCalledOnWrongThreadViolation.md) | <br /> | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Root class for all StrictMode violations.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) | [fillInStackTrace](Violation.md))`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](Violation.md))`()` <br /> |
| open [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) | [initCause](Violation.md))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStackTrace](Violation.md))`(`stackTrace:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [StackTraceElement](../java.lang/StackTraceElement.md)!>`)` <br /> |

## Public methods

### fillInStackTrace

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun fillInStackTrace(): Throwable
```

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------------------|
| [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) | a reference to this`Throwable`instance. |

### hashCode

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### initCause

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun initCause(cause: Throwable?): Throwable
```

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?:the cause (which is saved for later retrieval by the [getCause()](../java.lang/Throwable.md))method). (A`null`value is permitted, and indicates that the cause is nonexistent or unknown.) |

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------------------|
| [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) | a reference to this`Throwable`instance. |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if`cause`is this throwable. (A throwable cannot be its own cause.) |
| `java.lang.IllegalStateException` | if this throwable was created with [Throwable(java.lang.Throwable)](../java.lang/Throwable.md))or [Throwable(java.lang.String,java.lang.Throwable)](../java.lang/Throwable.md)), or this method has already been called on this throwable. |

### setStackTrace

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setStackTrace(stackTrace: Array<StackTraceElement!>): Unit
```

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `stackTrace` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [StackTraceElement](../java.lang/StackTraceElement.md)!\>:the stack trace elements to be associated with this`Throwable`. The specified array is copied by this call; changes in the specified array after the method invocation returns will have no affect on this`Throwable`'s stack trace. |

| Exceptions ||
|----------------------------------|-------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if`stackTrace`is`null`or if any of the elements of`stackTrace`are`null` |
