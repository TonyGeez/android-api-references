Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PccSandboxManager

```
class PccSandboxManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.privatecompute.PccSandboxManager](../android/app/privatecompute/PccSandboxManager.md) |

Manager for interacting with the Private Compute Core (PCC) sandbox.

## Summary

| Public methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/privatecompute/PccSandboxManager#egressData(android.app.privatecompute.EgressRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)(request: https://developer.android.com/reference/kotlin/android/app/privatecompute/EgressRequest<T>, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<T, https://developer.android.com/reference/kotlin/android/app/privatecompute/PccEgressException!>)` Initiates an egress request from a PCC process. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/privatecompute/PccSandboxManager#isPccTrustedSystemComponent(kotlin.Int,%20kotlin.String)(uid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Returns whether the given package is considered a "Trusted System Component" by the framework. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/privatecompute/PccSandboxManager#isPrivateComputeServicesUid(kotlin.Int)(uid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns whether the given UID belongs to a Private Compute Services (PCS) package. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/privatecompute/PccSandboxManager#startNonPccProcessForDataMigration(java.util.concurrent.Executor,%20android.os.OutcomeReceiver)(executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://developer.android.com/reference/kotlin/android/app/privatecompute/MigrationRequestResult!, https://developer.android.com/reference/kotlin/android/app/privatecompute/MigrationException!>)` Requests the framework to start the non-PCC migration service of the calling application. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/privatecompute/PccSandboxManager#writeToAuditLog(android.os.PersistableBundle)(data: https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#)` Writes data to the audit log, if audit mode is enabled. |

## Public methods

### egressData

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun <T : EgressResponse!> egressData(
    request: EgressRequest<T>, 
    executor: Executor, 
    callback: OutcomeReceiver<T, PccEgressException!>
): Unit
```

Initiates an egress request from a PCC process.

These requests may be subject to rate limits or user consent defined by the OS. For exact details refer to the exact sub-class of the EgressRequest.

| Parameters ||
|---|---|
| `request` | [EgressRequest](../android/app/privatecompute/EgressRequest.md)\<T\>: The base EgressRequest containing the payload and use-case. This value cannot be `null`. |
| `executor` | [Executor](../java/util/concurrent/Executor.md): The Executor on which the callback should be invoked. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [OutcomeReceiver](../android/os/OutcomeReceiver.md)\<T, [PccEgressException](../android/app/privatecompute/PccEgressException.md)!\>: The callback to receive the EgressResponse containing the status. This value cannot be `null`. |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If the `request` is invalid. |
| `java.lang.IllegalStateException` | If the request cannot be processed due to the current state of the system (e.g. rate limit exceeded). |
| `java.lang.NullPointerException` | If `request`, `executor`, or `callback` is `null`. |
| --- | --- |
| `java.lang.SecurityException` | If the calling UID is not running in a valid Private Compute Core sandbox or the underlying feature (such as Proactive Assistance) is disabled. |

### isPccTrustedSystemComponent

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isPccTrustedSystemComponent(
    uid: Int, 
    packageName: String?
): Boolean
```

Returns whether the given package is considered a "Trusted System Component" by the framework. This also includes Private Compute Services apps, which are an extension to the framework's trust boundary. Trusted System components are allowed two-way communication with the PCC components.

| Parameters ||
|---|---|
| `uid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The UID of the application. |
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: The package name of the application. This can be null when a single packagename isn't available, e.g. for SYSTEM_UID. If non-null, this API checks whether `uid` corresponds to `packageName`, and returns `false` if it doesn't. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the app is a trusted system component, `false` otherwise. |

### isPrivateComputeServicesUid

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isPrivateComputeServicesUid(uid: Int): Boolean
```

Returns whether the given UID belongs to a Private Compute Services (PCS) package. These are packages that hold the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#PROVIDE_PRIVATE_COMPUTE_SERVICES:kotlin.String`.

| Parameters ||
|---|---|
| `uid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The UID to check. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the UID belongs to a PCS package, `false` otherwise. |

### startNonPccProcessForDataMigration

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun startNonPccProcessForDataMigration(
    executor: Executor, 
    callback: OutcomeReceiver<MigrationRequestResult!, MigrationException!>
): Unit
```

Requests the framework to start the non-PCC migration service of the calling application.

This is intended for PCC components to trigger a process outside the PCC sandbox to perform tasks like data migration. The system will look for a service extending `https://developer.android.com/reference/kotlin/android/app/privatecompute/DataMigrationToPccService` in the application's manifest that is **not** marked as a PCC component. If found, the non-PCC process is started and the service is invoked.

If the non-PCC process is already running, this ensures the migration service is triggered. System unbinds from the service either when the service indicates it has accepted/rejected the request, or failing that, after a timeout of `https://developer.android.com/reference/kotlin/android/app/privatecompute/DataMigrationToPccService#MIGRATION_TIMEOUT_MS:kotlin.Long`.

| Parameters ||
|---|---|
| `executor` | [Executor](../java/util/concurrent/Executor.md): The executor on which the callback will be invoked. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [OutcomeReceiver](../android/os/OutcomeReceiver.md)\< [MigrationRequestResult](../android/app/privatecompute/MigrationRequestResult.md)!, [MigrationException](../android/app/privatecompute/MigrationException.md)!\>: The callback to receive the result of the migration request. This value cannot be `null`. |

### writeToAuditLog

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToAuditLog(data: PersistableBundle): Unit
```

Writes data to the audit log, if audit mode is enabled. Otherwise, does nothing.

Nested Bundles are supported up to a depth of 100.

| Parameters ||
|---|---|
| `data` | [PersistableBundle](../android/os/PersistableBundle.md): The data to write to the audit log. This value cannot be `null`. |
