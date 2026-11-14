Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AbstractThreadedSyncAdapter

Kotlin | [Java](AbstractThreadedSyncAdapter.md)
| --- | --- |

```
abstract class AbstractThreadedSyncAdapter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.content.AbstractThreadedSyncAdapter](AbstractThreadedSyncAdapter.md) |

An abstract implementation of a SyncAdapter that spawns a thread to invoke a sync operation. If a sync operation is already in progress when a sync request is received, an error will be returned to the new request and the existing request will be allowed to continue. However if there is no sync in progress then a thread will be spawned and `https://developer.android.com/reference/kotlin/android/content/AbstractThreadedSyncAdapter#onPerformSync(android.accounts.Account,%20android.os.Bundle,%20kotlin.String,%20android.content.ContentProviderClient,%20android.content.SyncResult)` will be invoked on that thread.

Syncs can be cancelled at any time by the framework. For example a sync that was not user-initiated and lasts longer than 10 minutes will be considered timed-out and cancelled. Similarly the framework will attempt to determine whether or not an adapter is making progress by monitoring its network activity over the course of a minute. If the network traffic over this window is close enough to zero the sync will be cancelled. You can also request the sync be cancelled via `https://developer.android.com/reference/kotlin/android/content/ContentResolver#cancelSync(android.accounts.Account,%20kotlin.String)` or `https://developer.android.com/reference/kotlin/android/content/ContentResolver#cancelSync(android.content.SyncRequest)`.

A sync is cancelled by issuing a `https://developer.android.com/reference/kotlin/java/lang/Thread.html#interrupt()` on the syncing thread. **Either your code in `https://developer.android.com/reference/kotlin/android/content/AbstractThreadedSyncAdapter#onPerformSync(android.accounts.Account,%20android.os.Bundle,%20kotlin.String,%20android.content.ContentProviderClient,%20android.content.SyncResult)` must check `https://developer.android.com/reference/kotlin/java/lang/Thread.html#interrupted()`, or you you must override one of `https://developer.android.com/reference/kotlin/android/content/AbstractThreadedSyncAdapter#onSyncCanceled(java.lang.Thread)`/`https://developer.android.com/reference/kotlin/android/content/AbstractThreadedSyncAdapter#onSyncCanceled()`** (depending on whether or not your adapter supports syncing of multiple accounts in parallel). If your adapter does not respect the cancel issued by the framework you run the risk of your app's entire process being killed.

In order to be a sync adapter one must extend this class, provide implementations for the abstract methods and write a service that returns the result of `https://developer.android.com/reference/kotlin/android/content/AbstractThreadedSyncAdapter#getSyncAdapterBinder()` in the service's `https://developer.android.com/reference/kotlin/android/app/Service.html#onBind(android.content.Intent)` when invoked with an intent with action `android.content.SyncAdapter`. This service must specify the following intent filter and metadata tags in its AndroidManifest.xml file

```kotlin
<intent-filter>
      <action android:name="android.content.SyncAdapter" />
    </intent-filter>
    <meta-data android:name="android.content.SyncAdapter"
              android:resource="@xml/syncadapter" />
  
```
The `android:resource` attribute must point to a resource that looks like:

```kotlin
<sync-adapter xmlns:android="http://schemas.android.com/apk/res/android"
     android:contentAuthority="authority"
     android:accountType="accountType"
     android:userVisible="true|false"
     android:supportsUploading="true|false"
     android:allowParallelSyncs="true|false"
     android:isAlwaysSyncable="true|false"
     android:syncAdapterSettingsAction="ACTION_OF_SETTINGS_ACTIVITY"
  />
  
```

- The `android:contentAuthority` and `android:accountType` attributes indicate which content authority and for which account types this sync adapter serves.
- `android:userVisible` defaults to true and controls whether or not this sync adapter shows up in the Sync Settings screen.
- `android:supportsUploading` defaults to true and if true an upload-only sync will be requested for all syncadapters associated with an authority whenever that authority's content provider does a `https://developer.android.com/reference/kotlin/android/content/ContentResolver#notifyChange(android.net.Uri,%20android.database.ContentObserver,%20kotlin.Boolean)` with syncToNetwork set to true.
- `android:allowParallelSyncs` defaults to false and if true indicates that the sync adapter can handle syncs for multiple accounts at the same time. Otherwise the SyncManager will wait until the sync adapter is not in use before requesting that it sync an account's data.
- `android:isAlwaysSyncable` defaults to false and if true tells the SyncManager to initialize the isSyncable state to 1 for that sync adapter for each account that is added.
- `android:syncAdapterSettingsAction` defaults to null and if supplied it specifies an Intent action of an activity that can be used to adjust the sync adapter's sync settings. The activity must live in the same package as the sync adapter.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/content/AbstractThreadedSyncAdapter#LOG_SYNC_DETAILS:kotlin.Int` Kernel event log tag. |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/content/AbstractThreadedSyncAdapter#AbstractThreadedSyncAdapter(android.content.Context,%20kotlin.Boolean)(context: https://developer.android.com/reference/kotlin/android/content/Context!, autoInitialize: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Creates an `https://developer.android.com/reference/kotlin/android/content/AbstractThreadedSyncAdapter#`. |
| `https://developer.android.com/reference/kotlin/android/content/AbstractThreadedSyncAdapter#AbstractThreadedSyncAdapter(android.content.Context,%20kotlin.Boolean,%20kotlin.Boolean)(context: https://developer.android.com/reference/kotlin/android/content/Context!, autoInitialize: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, allowParallelSyncs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Creates an `https://developer.android.com/reference/kotlin/android/content/AbstractThreadedSyncAdapter#`. |

| Public methods ||
|---|---|
| open [Context](Context.md)! | `https://developer.android.com/reference/kotlin/android/content/AbstractThreadedSyncAdapter#getContext()()` <br /> |
| [IBinder](../android.os/IBinder.md)! | `https://developer.android.com/reference/kotlin/android/content/AbstractThreadedSyncAdapter#getSyncAdapterBinder()()` <br /> |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/AbstractThreadedSyncAdapter#onPerformSync(android.accounts.Account,%20android.os.Bundle,%20kotlin.String,%20android.content.ContentProviderClient,%20android.content.SyncResult)(account: https://developer.android.com/reference/kotlin/android/accounts/Account.html#!, extras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!, authority: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, provider: https://developer.android.com/reference/kotlin/android/content/ContentProviderClient!, syncResult: https://developer.android.com/reference/kotlin/android/content/SyncResult!)` Perform a sync for this account. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/AbstractThreadedSyncAdapter#onSecurityException(android.accounts.Account,%20android.os.Bundle,%20kotlin.String,%20android.content.SyncResult)(account: https://developer.android.com/reference/kotlin/android/accounts/Account.html#!, extras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!, authority: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, syncResult: https://developer.android.com/reference/kotlin/android/content/SyncResult!)` Report that there was a security exception when opening the content provider prior to calling `https://developer.android.com/reference/kotlin/android/content/AbstractThreadedSyncAdapter#onPerformSync(android.accounts.Account,%20android.os.Bundle,%20kotlin.String,%20android.content.ContentProviderClient,%20android.content.SyncResult)`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/AbstractThreadedSyncAdapter#onSyncCanceled()()` Indicates that a sync operation has been canceled. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/content/AbstractThreadedSyncAdapter#onSyncCanceled(java.lang.Thread)(thread: https://developer.android.com/reference/kotlin/java/lang/Thread.html#!)` Indicates that a sync operation has been canceled. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/content/AbstractThreadedSyncAdapter#onUnsyncableAccount()()` Allows to defer syncing until all accounts are properly set up. |

## Constants

### LOG_SYNC_DETAILS

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LOG_SYNC_DETAILS: Int
```

**Deprecated:** *Private constant. May go away in the next release.*

Kernel event log tag. Also listed in data/etc/event-log-tags.

 Value: 2743

## Public constructors

### AbstractThreadedSyncAdapter

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
AbstractThreadedSyncAdapter(
    context: Context!, 
    autoInitialize: Boolean)
```

Creates an `https://developer.android.com/reference/kotlin/android/content/AbstractThreadedSyncAdapter#`.

| Parameters ||
|---|---|
| `context` | [Context](Context.md)!: the `https://developer.android.com/reference/kotlin/android/content/Context` that this is running within. |
| `autoInitialize` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): if true then sync requests that have `https://developer.android.com/reference/kotlin/android/content/ContentResolver#SYNC_EXTRAS_INITIALIZE:kotlin.String` set will be internally handled by `https://developer.android.com/reference/kotlin/android/content/AbstractThreadedSyncAdapter#` by calling `https://developer.android.com/reference/kotlin/android/content/ContentResolver#setIsSyncable(android.accounts.Account,%20kotlin.String,%20kotlin.Int)` with 1 if it is currently set to \<0. |

### AbstractThreadedSyncAdapter

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
AbstractThreadedSyncAdapter(
    context: Context!, 
    autoInitialize: Boolean, 
    allowParallelSyncs: Boolean)
```

Creates an `https://developer.android.com/reference/kotlin/android/content/AbstractThreadedSyncAdapter#`.

| Parameters ||
|---|---|
| `context` | [Context](Context.md)!: the `https://developer.android.com/reference/kotlin/android/content/Context` that this is running within. |
| `autoInitialize` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): if true then sync requests that have `https://developer.android.com/reference/kotlin/android/content/ContentResolver#SYNC_EXTRAS_INITIALIZE:kotlin.String` set will be internally handled by `https://developer.android.com/reference/kotlin/android/content/AbstractThreadedSyncAdapter#` by calling `https://developer.android.com/reference/kotlin/android/content/ContentResolver#setIsSyncable(android.accounts.Account,%20kotlin.String,%20kotlin.Int)` with 1 if it is currently set to \<0. |
| `allowParallelSyncs` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): if true then allow syncs for different accounts to run at the same time, each in their own thread. This must be consistent with the setting in the SyncAdapter's configuration file. |
| --- | --- |

## Public methods

### getContext

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getContext(): Context!
```

### getSyncAdapterBinder

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSyncAdapterBinder(): IBinder!
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/IBinder.html#!` | a reference to the IBinder of the SyncAdapter service. |

### onPerformSync

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun onPerformSync(
    account: Account!, 
    extras: Bundle!, 
    authority: String!, 
    provider: ContentProviderClient!, 
    syncResult: SyncResult!
): Unit
```

Perform a sync for this account. SyncAdapter-specific parameters may be specified in extras, which is guaranteed to not be null. Invocations of this method are guaranteed to be serialized.

| Parameters ||
|---|---|
| `account` | [Account](../android.accounts/Account.md)!: the account that should be synced |
| `extras` | [Bundle](../android.os/Bundle.md)!: SyncAdapter-specific parameters |
| `authority` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the authority of this sync request |
| --- | --- |
| `provider` | [ContentProviderClient](ContentProviderClient.md)!: a ContentProviderClient that points to the ContentProvider for this authority |
| `syncResult` | [SyncResult](SyncResult.md)!: SyncAdapter-specific parameters |

### onSecurityException

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onSecurityException(
    account: Account!, 
    extras: Bundle!, 
    authority: String!, 
    syncResult: SyncResult!
): Unit
```

Report that there was a security exception when opening the content provider prior to calling `https://developer.android.com/reference/kotlin/android/content/AbstractThreadedSyncAdapter#onPerformSync(android.accounts.Account,%20android.os.Bundle,%20kotlin.String,%20android.content.ContentProviderClient,%20android.content.SyncResult)`. This will be treated as a sync database failure.

| Parameters ||
|---|---|
| `account` | [Account](../android.accounts/Account.md)!: the account that attempted to sync |
| `extras` | [Bundle](../android.os/Bundle.md)!: SyncAdapter-specific parameters |
| `authority` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the authority of the failed sync request |
| --- | --- |
| `syncResult` | [SyncResult](SyncResult.md)!: SyncAdapter-specific parameters |

### onSyncCanceled

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onSyncCanceled(): Unit
```

Indicates that a sync operation has been canceled. This will be invoked on a separate thread than the sync thread and so you must consider the multi-threaded implications of the work that you do in this method.

This will only be invoked when the SyncAdapter indicates that it doesn't support parallel syncs.

### onSyncCanceled

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onSyncCanceled(thread: Thread!): Unit
```

Indicates that a sync operation has been canceled. This will be invoked on a separate thread than the sync thread and so you must consider the multi-threaded implications of the work that you do in this method.

This will only be invoked when the SyncAdapter indicates that it does support parallel syncs.

| Parameters ||
|---|---|
| `thread` | [Thread](../java.lang/Thread.md)!: the Thread of the sync that is to be canceled. |

### onUnsyncableAccount

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onUnsyncableAccount(): Boolean
```

Allows to defer syncing until all accounts are properly set up.

Called when a account / authority pair

- that can be handled by this adapter
- `https://developer.android.com/reference/kotlin/android/content/ContentResolver#requestSync(android.content.SyncRequest)`
- and the account/provider `https://developer.android.com/reference/kotlin/android/content/ContentResolver#getIsSyncable(android.accounts.Account,%20kotlin.String)`.

This might be called on a different service connection as `https://developer.android.com/reference/kotlin/android/content/AbstractThreadedSyncAdapter#onPerformSync(android.accounts.Account,%20android.os.Bundle,%20kotlin.String,%20android.content.ContentProviderClient,%20android.content.SyncResult)`.

The system expects this method to immediately return. If the call stalls the system behaves as if this method returned `true`. If it is required to perform a longer task (such as interacting with the user), return `false` and proceed in a difference context, such as an `https://developer.android.com/reference/kotlin/android/app/Activity.html#`, or foreground service. The sync can then be rescheduled once the account becomes syncable. 
This method must be called from the main thread of your app.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | If `false` syncing is deferred. Returns `true` by default, i.e. by default syncing starts immediately. |
