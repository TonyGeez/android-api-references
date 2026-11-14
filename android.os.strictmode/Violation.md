# Violation

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Violation

Kotlin| [Java](https://developer.android.com/reference/android/os/strictmode/Violation "View this page in Java") 

```
abstract class Violation : Throwable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||
| | ↳ | [android.os.strictmode.Violation](https://developer.android.com/reference/kotlin/android/os/strictmode/Violation#) |

| Known Direct Subclasses [CleartextNetworkViolation](https://developer.android.com/reference/kotlin/android/os/strictmode/CleartextNetworkViolation), [ContentUriWithoutPermissionViolation](https://developer.android.com/reference/kotlin/android/os/strictmode/ContentUriWithoutPermissionViolation), [CredentialProtectedWhileLockedViolation](https://developer.android.com/reference/kotlin/android/os/strictmode/CredentialProtectedWhileLockedViolation), [CustomViolation](https://developer.android.com/reference/kotlin/android/os/strictmode/CustomViolation), [DiskReadViolation](https://developer.android.com/reference/kotlin/android/os/strictmode/DiskReadViolation), [DiskWriteViolation](https://developer.android.com/reference/kotlin/android/os/strictmode/DiskWriteViolation), [ExplicitGcViolation](https://developer.android.com/reference/kotlin/android/os/strictmode/ExplicitGcViolation), [FileUriExposedViolation](https://developer.android.com/reference/kotlin/android/os/strictmode/FileUriExposedViolation), [ImplicitDirectBootViolation](https://developer.android.com/reference/kotlin/android/os/strictmode/ImplicitDirectBootViolation), [IncorrectContextUseViolation](https://developer.android.com/reference/kotlin/android/os/strictmode/IncorrectContextUseViolation), [InstanceCountViolation](https://developer.android.com/reference/kotlin/android/os/strictmode/InstanceCountViolation), [IntentReceiverLeakedViolation](https://developer.android.com/reference/kotlin/android/os/strictmode/IntentReceiverLeakedViolation), and 10 others. |-------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [CleartextNetworkViolation](https://developer.android.com/reference/kotlin/android/os/strictmode/CleartextNetworkViolation) | <br /> | | [ContentUriWithoutPermissionViolation](https://developer.android.com/reference/kotlin/android/os/strictmode/ContentUriWithoutPermissionViolation) | <br /> | | [CredentialProtectedWhileLockedViolation](https://developer.android.com/reference/kotlin/android/os/strictmode/CredentialProtectedWhileLockedViolation) | Subclass of`Violation`that is used when a process accesses filesystem paths stored in credential protected storage areas while the user is locked. | | [CustomViolation](https://developer.android.com/reference/kotlin/android/os/strictmode/CustomViolation) | <br /> | | [DiskReadViolation](https://developer.android.com/reference/kotlin/android/os/strictmode/DiskReadViolation) | <br /> | | [DiskWriteViolation](https://developer.android.com/reference/kotlin/android/os/strictmode/DiskWriteViolation) | <br /> | | [ExplicitGcViolation](https://developer.android.com/reference/kotlin/android/os/strictmode/ExplicitGcViolation) | See # [android.os.StrictMode.ThreadPolicy.Builder#detectExplicitGc()](https://developer.android.com/reference/kotlin/android/os/StrictMode.ThreadPolicy.Builder.html#detectExplicitGc()). | | [FileUriExposedViolation](https://developer.android.com/reference/kotlin/android/os/strictmode/FileUriExposedViolation) | <br /> | | [ImplicitDirectBootViolation](https://developer.android.com/reference/kotlin/android/os/strictmode/ImplicitDirectBootViolation) | Subclass of`Violation`that is used when a process implicitly relies on automatic Direct Boot filtering. | | [IncorrectContextUseViolation](https://developer.android.com/reference/kotlin/android/os/strictmode/IncorrectContextUseViolation) | Incorrect usage of [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#), such as obtaining a UI service from non-UI [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#) instance. | | [InstanceCountViolation](https://developer.android.com/reference/kotlin/android/os/strictmode/InstanceCountViolation) | <br /> | | [IntentReceiverLeakedViolation](https://developer.android.com/reference/kotlin/android/os/strictmode/IntentReceiverLeakedViolation) | <br /> | | [LeakedClosableViolation](https://developer.android.com/reference/kotlin/android/os/strictmode/LeakedClosableViolation) | <br /> | | [NetworkViolation](https://developer.android.com/reference/kotlin/android/os/strictmode/NetworkViolation) | <br /> | | [NonSdkApiUsedViolation](https://developer.android.com/reference/kotlin/android/os/strictmode/NonSdkApiUsedViolation) | Subclass of`Violation`that is used when a process accesses a non SDK API. | | [ResourceMismatchViolation](https://developer.android.com/reference/kotlin/android/os/strictmode/ResourceMismatchViolation) | <br /> | | [ServiceConnectionLeakedViolation](https://developer.android.com/reference/kotlin/android/os/strictmode/ServiceConnectionLeakedViolation) | <br /> | | [SqliteObjectLeakedViolation](https://developer.android.com/reference/kotlin/android/os/strictmode/SqliteObjectLeakedViolation) | <br /> | | [UnbufferedIoViolation](https://developer.android.com/reference/kotlin/android/os/strictmode/UnbufferedIoViolation) | See # [Builder.detectUnbufferedIo()](https://developer.android.com/reference/kotlin/android/os/StrictMode.ThreadPolicy.Builder.html#detectUnbufferedIo()) | | [UnsafeIntentLaunchViolation](https://developer.android.com/reference/kotlin/android/os/strictmode/UnsafeIntentLaunchViolation) | Violation raised when your app launches an [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#) which originated from outside your app. | | [UntaggedSocketViolation](https://developer.android.com/reference/kotlin/android/os/strictmode/UntaggedSocketViolation) | <br /> | | [WebViewMethodCalledOnWrongThreadViolation](https://developer.android.com/reference/kotlin/android/os/strictmode/WebViewMethodCalledOnWrongThreadViolation) | <br /> | |

Root class for all StrictMode violations.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) | [fillInStackTrace](https://developer.android.com/reference/kotlin/android/os/strictmode/Violation#fillInStackTrace())`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/os/strictmode/Violation#hashCode())`()` <br /> |
| open [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) | [initCause](https://developer.android.com/reference/kotlin/android/os/strictmode/Violation#initCause(kotlin.Throwable))`(`cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStackTrace](https://developer.android.com/reference/kotlin/android/os/strictmode/Violation#setStackTrace(kotlin.Array))`(`stackTrace:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [StackTraceElement](https://developer.android.com/reference/kotlin/java/lang/StackTraceElement.html#)!>`)` <br /> |

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
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?:the cause (which is saved for later retrieval by the [getCause()](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#getCause())method). (A`null`value is permitted, and indicates that the cause is nonexistent or unknown.) |

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------------------|
| [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) | a reference to this`Throwable`instance. |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if`cause`is this throwable. (A throwable cannot be its own cause.) |
| `java.lang.IllegalStateException` | if this throwable was created with [Throwable(java.lang.Throwable)](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#Throwable(kotlin.Throwable))or [Throwable(java.lang.String,java.lang.Throwable)](https://developer.android.com/reference/kotlin/java/lang/Throwable.html#Throwable(kotlin.String,%20kotlin.Throwable)), or this method has already been called on this throwable. |

### setStackTrace

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setStackTrace(stackTrace: Array<StackTraceElement!>): Unit
```

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `stackTrace` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [StackTraceElement](https://developer.android.com/reference/kotlin/java/lang/StackTraceElement.html#)!\>:the stack trace elements to be associated with this`Throwable`. The specified array is copied by this call; changes in the specified array after the method invocation returns will have no affect on this`Throwable`'s stack trace. |

| Exceptions ||
|----------------------------------|-------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if`stackTrace`is`null`or if any of the elements of`stackTrace`are`null` |
