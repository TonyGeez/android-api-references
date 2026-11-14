# android.os.strictmode

# android.os.strictmode

Kotlin| [Java](_package.md)
| --- | --- |

## Exceptions

| [CleartextNetworkViolation](CleartextNetworkViolation.md) | <br /> |
| --- | --- |
| [ContentUriWithoutPermissionViolation](ContentUriWithoutPermissionViolation.md) | <br /> |
| [CredentialProtectedWhileLockedViolation](CredentialProtectedWhileLockedViolation.md) | Subclass of`Violation`that is used when a process accesses filesystem paths stored in credential protected storage areas while the user is locked. |
| [CustomViolation](CustomViolation.md) | <br /> |
| --- | --- |
| [DiskReadViolation](DiskReadViolation.md) | <br /> |
| [DiskWriteViolation](DiskWriteViolation.md) | <br /> |
| [ExplicitGcViolation](ExplicitGcViolation.md) | See # [android.os.StrictMode.ThreadPolicy.Builder#detectExplicitGc()](../android/os/StrictMode.ThreadPolicy.Builder.md)). |
| --- | --- |
| [FileUriExposedViolation](FileUriExposedViolation.md) | <br /> |
| [ImplicitDirectBootViolation](ImplicitDirectBootViolation.md) | Subclass of`Violation`that is used when a process implicitly relies on automatic Direct Boot filtering. |
| [IncorrectContextUseViolation](IncorrectContextUseViolation.md) | Incorrect usage of [Context](../android.content/Context.md), such as obtaining a UI service from non-UI [Context](../android.content/Context.md) instance. |
| --- | --- |
| [InstanceCountViolation](InstanceCountViolation.md) | <br /> |
| [IntentReceiverLeakedViolation](IntentReceiverLeakedViolation.md) | <br /> |
| [LeakedClosableViolation](LeakedClosableViolation.md) | <br /> |
| --- | --- |
| [NetworkViolation](NetworkViolation.md) | <br /> |
| [NonSdkApiUsedViolation](NonSdkApiUsedViolation.md) | Subclass of`Violation`that is used when a process accesses a non SDK API. |
| [ResourceMismatchViolation](ResourceMismatchViolation.md) | <br /> |
| --- | --- |
| [ServiceConnectionLeakedViolation](ServiceConnectionLeakedViolation.md) | <br /> |
| [SqliteObjectLeakedViolation](SqliteObjectLeakedViolation.md) | <br /> |
| [UnbufferedIoViolation](UnbufferedIoViolation.md) | See # [Builder.detectUnbufferedIo()](../android/os/StrictMode.ThreadPolicy.Builder.md)) |
| --- | --- |
| [UnsafeIntentLaunchViolation](UnsafeIntentLaunchViolation.md) | Violation raised when your app launches an [Intent](../android.content/Intent.md) which originated from outside your app. |
| [UntaggedSocketViolation](UntaggedSocketViolation.md) | <br /> |
| [Violation](Violation.md) | Root class for all StrictMode violations. |
| --- | --- |
| [WebViewMethodCalledOnWrongThreadViolation](WebViewMethodCalledOnWrongThreadViolation.md) | <br /> |
