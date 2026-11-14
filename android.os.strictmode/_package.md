# android.os.strictmode

# android.os.strictmode

Kotlin| [Java](https://developer.android.com/reference/android/os/strictmode/package-summary "View this page in Java")

## Exceptions

| [CleartextNetworkViolation](https://developer.android.com/reference/kotlin/android/os/strictmode/CleartextNetworkViolation) | <br /> |
| [ContentUriWithoutPermissionViolation](https://developer.android.com/reference/kotlin/android/os/strictmode/ContentUriWithoutPermissionViolation) | <br /> |
| [CredentialProtectedWhileLockedViolation](https://developer.android.com/reference/kotlin/android/os/strictmode/CredentialProtectedWhileLockedViolation) | Subclass of`Violation`that is used when a process accesses filesystem paths stored in credential protected storage areas while the user is locked. |
| [CustomViolation](https://developer.android.com/reference/kotlin/android/os/strictmode/CustomViolation) | <br /> |
| [DiskReadViolation](https://developer.android.com/reference/kotlin/android/os/strictmode/DiskReadViolation) | <br /> |
| [DiskWriteViolation](https://developer.android.com/reference/kotlin/android/os/strictmode/DiskWriteViolation) | <br /> |
| [ExplicitGcViolation](https://developer.android.com/reference/kotlin/android/os/strictmode/ExplicitGcViolation) | See # [android.os.StrictMode.ThreadPolicy.Builder#detectExplicitGc()](https://developer.android.com/reference/kotlin/android/os/StrictMode.ThreadPolicy.Builder.html#detectExplicitGc()). |
| [FileUriExposedViolation](https://developer.android.com/reference/kotlin/android/os/strictmode/FileUriExposedViolation) | <br /> |
| [ImplicitDirectBootViolation](https://developer.android.com/reference/kotlin/android/os/strictmode/ImplicitDirectBootViolation) | Subclass of`Violation`that is used when a process implicitly relies on automatic Direct Boot filtering. |
| [IncorrectContextUseViolation](https://developer.android.com/reference/kotlin/android/os/strictmode/IncorrectContextUseViolation) | Incorrect usage of [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#), such as obtaining a UI service from non-UI [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#) instance. |
| [InstanceCountViolation](https://developer.android.com/reference/kotlin/android/os/strictmode/InstanceCountViolation) | <br /> |
| [IntentReceiverLeakedViolation](https://developer.android.com/reference/kotlin/android/os/strictmode/IntentReceiverLeakedViolation) | <br /> |
| [LeakedClosableViolation](https://developer.android.com/reference/kotlin/android/os/strictmode/LeakedClosableViolation) | <br /> |
| [NetworkViolation](https://developer.android.com/reference/kotlin/android/os/strictmode/NetworkViolation) | <br /> |
| [NonSdkApiUsedViolation](https://developer.android.com/reference/kotlin/android/os/strictmode/NonSdkApiUsedViolation) | Subclass of`Violation`that is used when a process accesses a non SDK API. |
| [ResourceMismatchViolation](https://developer.android.com/reference/kotlin/android/os/strictmode/ResourceMismatchViolation) | <br /> |
| [ServiceConnectionLeakedViolation](https://developer.android.com/reference/kotlin/android/os/strictmode/ServiceConnectionLeakedViolation) | <br /> |
| [SqliteObjectLeakedViolation](https://developer.android.com/reference/kotlin/android/os/strictmode/SqliteObjectLeakedViolation) | <br /> |
| [UnbufferedIoViolation](https://developer.android.com/reference/kotlin/android/os/strictmode/UnbufferedIoViolation) | See # [Builder.detectUnbufferedIo()](https://developer.android.com/reference/kotlin/android/os/StrictMode.ThreadPolicy.Builder.html#detectUnbufferedIo()) |
| [UnsafeIntentLaunchViolation](https://developer.android.com/reference/kotlin/android/os/strictmode/UnsafeIntentLaunchViolation) | Violation raised when your app launches an [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#) which originated from outside your app. |
| [UntaggedSocketViolation](https://developer.android.com/reference/kotlin/android/os/strictmode/UntaggedSocketViolation) | <br /> |
| [Violation](https://developer.android.com/reference/kotlin/android/os/strictmode/Violation) | Root class for all StrictMode violations. |
| [WebViewMethodCalledOnWrongThreadViolation](https://developer.android.com/reference/kotlin/android/os/strictmode/WebViewMethodCalledOnWrongThreadViolation) | <br /> |
