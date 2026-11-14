# BlobStoreManager

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BlobStoreManager

Kotlin| [Java](https://developer.android.com/reference/android/app/blob/BlobStoreManager "View this page in Java") 
| --- | --- |

```
open class BlobStoreManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.blob.BlobStoreManager](https://developer.android.com/reference/kotlin/android/app/blob/BlobStoreManager#) |

This class provides access to the blob store managed by the system.

Apps can publish and access a data blob using a [BlobHandle](https://developer.android.com/reference/kotlin/android/app/blob/BlobHandle) object which can be created with[BlobHandle.createWithSha256(byte[], CharSequence, long, String)](https://developer.android.com/reference/kotlin/android/app/blob/BlobHandle#createWithSha256(kotlin.ByteArray,%20kotlin.CharSequence,%20kotlin.Long,%20kotlin.String)). This [BlobHandle](https://developer.android.com/reference/kotlin/android/app/blob/BlobHandle) object encapsulates the following pieces of information used for identifying the blobs:

- [BlobHandle.getSha256Digest()](https://developer.android.com/reference/kotlin/android/app/blob/BlobHandle#getSha256Digest())
- [BlobHandle.getLabel()](https://developer.android.com/reference/kotlin/android/app/blob/BlobHandle#getLabel())
- [BlobHandle.getExpiryTimeMillis()](https://developer.android.com/reference/kotlin/android/app/blob/BlobHandle#getExpiryTimeMillis())
- [BlobHandle.getTag()](https://developer.android.com/reference/kotlin/android/app/blob/BlobHandle#getTag())

For two [BlobHandle](https://developer.android.com/reference/kotlin/android/app/blob/BlobHandle) objects to be considered identical, all these pieces of information must be equal.

For contributing a new data blob, an app needs to create a session using [BlobStoreManager.createSession(BlobHandle)](https://developer.android.com/reference/kotlin/android/app/blob/BlobStoreManager#createSession(android.app.blob.BlobHandle))and then open this session for writing using [BlobStoreManager.openSession(long)](https://developer.android.com/reference/kotlin/android/app/blob/BlobStoreManager#openSession(kotlin.Long)).

The following code snippet shows how to create and open a session for writing: 

```kotlin
final long sessionId = blobStoreManager.createSession(blobHandle);
      try (BlobStoreManager.Session session = blobStoreManager.openSession(sessionId)) {
          try (OutputStream out = new ParcelFileDescriptor.AutoCloseOutputStream(
                  session.openWrite(offsetBytes, lengthBytes))) {
              writeData(out);
          }
      }
  
```

If all the data could not be written in a single attempt, apps can close this session and re-open it again using the session id obtained via [BlobStoreManager.createSession(BlobHandle)](https://developer.android.com/reference/kotlin/android/app/blob/BlobStoreManager#createSession(android.app.blob.BlobHandle)). Note that the session data is persisted and can be re-opened for completing the data contribution, even across device reboots.

After the data is written to the session, it can be committed using [Session.commit(Executor, Consumer)](https://developer.android.com/reference/kotlin/android/app/blob/BlobStoreManager.Session#commit(java.util.concurrent.Executor,%20java.util.function.Consumer)). Until the session is committed, data written to the session will not be shared with any app.

Once a session is committed using [Session.commit(Executor, Consumer)](https://developer.android.com/reference/kotlin/android/app/blob/BlobStoreManager.Session#commit(java.util.concurrent.Executor,%20java.util.function.Consumer)), any data written as part of this session is sealed and cannot be modified anymore.

Before committing the session, apps can indicate which apps are allowed to access the contributed data using one or more of the following access modes:

- [Session.allowPackageAccess(String, byte[])](https://developer.android.com/reference/kotlin/android/app/blob/BlobStoreManager.Session#allowPackageAccess(kotlin.String,%20kotlin.ByteArray))which will allow specific packages to access the blobs.
- [Session.allowSameSignatureAccess()](https://developer.android.com/reference/kotlin/android/app/blob/BlobStoreManager.Session#allowSameSignatureAccess())which will allow only apps which are signed with the same certificate as the app which contributed the blob to access it.
- [Session.allowPublicAccess()](https://developer.android.com/reference/kotlin/android/app/blob/BlobStoreManager.Session#allowPublicAccess())which will allow any app on the device to access the blob.

The following code snippet shows how to specify the access mode and commit the session: 

```kotlin
try (BlobStoreManager.Session session = blobStoreManager.openSession(sessionId)) {
          try (OutputStream out = new ParcelFileDescriptor.AutoCloseOutputStream(
                  session.openWrite(offsetBytes, lengthBytes))) {
              writeData(out);
          }
          session.allowSameSignatureAccess();
          session.allowPackageAccess(packageName, certificate);
          session.commit(executor, callback);
      }
  
```

Apps that satisfy at least one of the access mode constraints specified by the publisher of the data blob will be able to access it.

A data blob published without specifying any of these access modes will be considered private and only the app that contributed the data blob will be allowed to access it. This is still useful for overall device system health as the System can try to keep one copy of data blob on disk when multiple apps contribute the same data.

It is strongly recommended that apps use one of[Session.allowPackageAccess(String, byte[])](https://developer.android.com/reference/kotlin/android/app/blob/BlobStoreManager.Session#allowPackageAccess(kotlin.String,%20kotlin.ByteArray))or [Session.allowSameSignatureAccess()](https://developer.android.com/reference/kotlin/android/app/blob/BlobStoreManager.Session#allowSameSignatureAccess())when they know, ahead of time, the set of apps they would like to share the blobs with. [Session.allowPublicAccess()](https://developer.android.com/reference/kotlin/android/app/blob/BlobStoreManager.Session#allowPublicAccess())is meant for publicly available data committed from libraries and SDKs.

Once a data blob is committed with [Session.commit(Executor, Consumer)](https://developer.android.com/reference/kotlin/android/app/blob/BlobStoreManager.Session#commit(java.util.concurrent.Executor,%20java.util.function.Consumer)), it can be accessed using [BlobStoreManager.openBlob(BlobHandle)](https://developer.android.com/reference/kotlin/android/app/blob/BlobStoreManager#openBlob(android.app.blob.BlobHandle)), assuming the caller satisfies constraints of any of the access modes associated with that data blob. An app may acquire a lease on a blob with [BlobStoreManager.acquireLease(BlobHandle, int)](https://developer.android.com/reference/kotlin/android/app/blob/BlobStoreManager#acquireLease(android.app.blob.BlobHandle,%20kotlin.Int))and release the lease with [BlobStoreManager.releaseLease(BlobHandle)](https://developer.android.com/reference/kotlin/android/app/blob/BlobStoreManager#releaseLease(android.app.blob.BlobHandle)). A blob will not be deleted from the system while there is at least one app leasing it.

The following code snippet shows how to access the data blob: 

```kotlin
try (InputStream in = new ParcelFileDescriptor.AutoCloseInputStream(
              blobStoreManager.openBlob(blobHandle)) {
          useData(in);
      }
  
```

Restricted for SDK Runtime environment in API level 34.

## Summary

| Nested classes ||
|------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [Session](https://developer.android.com/reference/kotlin/android/app/blob/BlobStoreManager.Session) Represents an ongoing session of a blob's contribution to the blob store managed by the system. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [abandonSession](https://developer.android.com/reference/kotlin/android/app/blob/BlobStoreManager#abandonSession(kotlin.Long))`(`sessionId:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Abandons an existing session and deletes any data that was written to that session so far. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [acquireLease](https://developer.android.com/reference/kotlin/android/app/blob/BlobStoreManager#acquireLease(android.app.blob.BlobHandle,%20kotlin.Int))`(`blobHandle:` ` [BlobHandle](https://developer.android.com/reference/kotlin/android/app/blob/BlobHandle)`, `descriptionResId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Acquire a lease to the blob represented by`blobHandle`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [acquireLease](https://developer.android.com/reference/kotlin/android/app/blob/BlobStoreManager#acquireLease(android.app.blob.BlobHandle,%20kotlin.Int,%20kotlin.Long))`(`blobHandle:` ` [BlobHandle](https://developer.android.com/reference/kotlin/android/app/blob/BlobHandle)`, `descriptionResId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `leaseExpiryTimeMillis:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Acquire a lease to the blob represented by`blobHandle`. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [acquireLease](https://developer.android.com/reference/kotlin/android/app/blob/BlobStoreManager#acquireLease(android.app.blob.BlobHandle,%20kotlin.CharSequence))`(`blobHandle:` ` [BlobHandle](https://developer.android.com/reference/kotlin/android/app/blob/BlobHandle)`, `description:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)`)` Acquire a lease to the blob represented by`blobHandle`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [acquireLease](https://developer.android.com/reference/kotlin/android/app/blob/BlobStoreManager#acquireLease(android.app.blob.BlobHandle,%20kotlin.CharSequence,%20kotlin.Long))`(`blobHandle:` ` [BlobHandle](https://developer.android.com/reference/kotlin/android/app/blob/BlobHandle)`, `description:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)`, `leaseExpiryTimeMillis:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Acquire a lease to the blob represented by`blobHandle`. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [createSession](https://developer.android.com/reference/kotlin/android/app/blob/BlobStoreManager#createSession(android.app.blob.BlobHandle))`(`blobHandle:` ` [BlobHandle](https://developer.android.com/reference/kotlin/android/app/blob/BlobHandle)`)` Create a new session using the given [BlobHandle](https://developer.android.com/reference/kotlin/android/app/blob/BlobHandle), returning a unique id that represents the session. |
| --- | --- |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [BlobHandle](https://developer.android.com/reference/kotlin/android/app/blob/BlobHandle)!\> | [getLeasedBlobs](https://developer.android.com/reference/kotlin/android/app/blob/BlobStoreManager#getLeasedBlobs())`()` Return the [BlobHandles](https://developer.android.com/reference/kotlin/android/app/blob/BlobHandle) corresponding to the data blobs that the calling app currently has a lease on. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getRemainingLeaseQuotaBytes](https://developer.android.com/reference/kotlin/android/app/blob/BlobStoreManager#getRemainingLeaseQuotaBytes())`()` Return the remaining quota size for acquiring a lease (in bytes) which indicates the remaining amount of data that an app can acquire a lease on before the System starts rejecting lease requests. |
| open [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#) | [openBlob](https://developer.android.com/reference/kotlin/android/app/blob/BlobStoreManager#openBlob(android.app.blob.BlobHandle))`(`blobHandle:` ` [BlobHandle](https://developer.android.com/reference/kotlin/android/app/blob/BlobHandle)`)` Opens an existing blob for reading from the blob store managed by the system. |
| --- | --- |
| open [BlobStoreManager.Session](https://developer.android.com/reference/kotlin/android/app/blob/BlobStoreManager.Session) | [openSession](https://developer.android.com/reference/kotlin/android/app/blob/BlobStoreManager#openSession(kotlin.Long))`(`sessionId:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Open an existing session to actively perform work. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [releaseLease](https://developer.android.com/reference/kotlin/android/app/blob/BlobStoreManager#releaseLease(android.app.blob.BlobHandle))`(`blobHandle:` ` [BlobHandle](https://developer.android.com/reference/kotlin/android/app/blob/BlobHandle)`)` Release any active lease to the blob represented by`blobHandle`which is currently held by the caller. |

## Public methods

### abandonSession

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun abandonSession(sessionId: Long): Unit
```

Abandons an existing session and deletes any data that was written to that session so far.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sessionId` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):a unique id obtained via [createSession(android.app.blob.BlobHandle)](https://developer.android.com/reference/kotlin/android/app/blob/BlobStoreManager#createSession(android.app.blob.BlobHandle))that represents a particular session. Value is 1 or greater |

| Exceptions ||
|-------------------------------|----------------------------------------------------------------------------------------|
| `java.io.IOException` | when there is an I/O error while deleting the session. |
| `java.lang.SecurityException` | when the caller does not own the session, or the session does not exist or is invalid. |

### acquireLease

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun acquireLease(
    blobHandle: BlobHandle, 
    descriptionResId: Int
): Unit
```

Acquire a lease to the blob represented by`blobHandle`. This lease indicates to the system that the caller wants the blob to be kept around.

This is similar to [acquireLease(android.app.blob.BlobHandle,int,long)](https://developer.android.com/reference/kotlin/android/app/blob/BlobStoreManager#acquireLease(android.app.blob.BlobHandle,%20kotlin.Int,%20kotlin.Long))except clients don't have to specify the lease expiry time upfront using this API and need to explicitly release the lease using [releaseLease(android.app.blob.BlobHandle)](https://developer.android.com/reference/kotlin/android/app/blob/BlobStoreManager#releaseLease(android.app.blob.BlobHandle))when they no longer like to keep a blob around.

Any active leases will be automatically released when the blob's expiry time ([BlobHandle.getExpiryTimeMillis()](https://developer.android.com/reference/kotlin/android/app/blob/BlobHandle#getExpiryTimeMillis())) is elapsed.

This lease information is persisted and calling this more than once will result in latest lease overriding any previous lease.

When an app acquires a lease on a blob, the System will try to keep this blob around but note that it can still be deleted if it was requested by the user.

In case the resource name for the`descriptionResId`is modified as part of an app update, apps should re-acquire the lease with the new resource id.

| Parameters ||
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `blobHandle` | [BlobHandle](https://developer.android.com/reference/kotlin/android/app/blob/BlobHandle):the [BlobHandle](https://developer.android.com/reference/kotlin/android/app/blob/BlobHandle) representing the blob that the caller wants to acquire a lease for. This value cannot be`null`. |
| `descriptionResId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the resource id for a short description string that can be surfaced to the user explaining what the blob is used for. |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | when there is an I/O error while acquiring a lease to the blob. |
| `java.lang.SecurityException` | when the blob represented by the`blobHandle`does not exist or the caller does not have access to it. |
| `java.lang.IllegalArgumentException` | when`blobHandle`is invalid. |
| --- | --- |
| `android.os.LimitExceededException` | when a lease could not be acquired, such as when the caller is trying to acquire too many leases or acquire leases on too much data. Apps can avoid this by checking the remaining quota using [getRemainingLeaseQuotaBytes()](https://developer.android.com/reference/kotlin/android/app/blob/BlobStoreManager#getRemainingLeaseQuotaBytes())before trying to acquire a lease. |

**See Also**

- [#acquireLease(BlobHandle, int, long)](https://developer.android.com/reference/kotlin/android/app/blob/BlobStoreManager#acquireLease(android.app.blob.BlobHandle,%20kotlin.Int,%20kotlin.Long))
- [#acquireLease(BlobHandle, CharSequence, long)](https://developer.android.com/reference/kotlin/android/app/blob/BlobStoreManager#acquireLease(android.app.blob.BlobHandle,%20kotlin.CharSequence,%20kotlin.Long)) 

### acquireLease

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun acquireLease(
    blobHandle: BlobHandle, 
    descriptionResId: Int, 
    leaseExpiryTimeMillis: Long
): Unit
```

Acquire a lease to the blob represented by`blobHandle`. This lease indicates to the system that the caller wants the blob to be kept around.

Any active leases will be automatically released when the blob's expiry time ([BlobHandle.getExpiryTimeMillis()](https://developer.android.com/reference/kotlin/android/app/blob/BlobHandle#getExpiryTimeMillis())) is elapsed.

This lease information is persisted and calling this more than once will result in latest lease overriding any previous lease.

When an app acquires a lease on a blob, the System will try to keep this blob around but note that it can still be deleted if it was requested by the user.

In case the resource name for the`descriptionResId`is modified as part of an app update, apps should re-acquire the lease with the new resource id.

| Parameters ||
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `blobHandle` | [BlobHandle](https://developer.android.com/reference/kotlin/android/app/blob/BlobHandle):the [BlobHandle](https://developer.android.com/reference/kotlin/android/app/blob/BlobHandle) representing the blob that the caller wants to acquire a lease for. This value cannot be`null`. |
| `descriptionResId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the resource id for a short description string that can be surfaced to the user explaining what the blob is used for. |
| `leaseExpiryTimeMillis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the time in milliseconds after which the lease can be automatically released, in [System.currentTimeMillis()](https://developer.android.com/reference/kotlin/java/lang/System.html#currentTimeMillis())timebase. If its value is`0`, then the behavior of this API is identical to [acquireLease(android.app.blob.BlobHandle,int)](https://developer.android.com/reference/kotlin/android/app/blob/BlobStoreManager#acquireLease(android.app.blob.BlobHandle,%20kotlin.Int))where clients have to explicitly call [releaseLease(android.app.blob.BlobHandle)](https://developer.android.com/reference/kotlin/android/app/blob/BlobStoreManager#releaseLease(android.app.blob.BlobHandle))when they don't need the blob anymore. Value is a non-negative timestamp measured as the number of milliseconds since 1970-01-01T00:00:00Z. |
| --- | --- |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | when there is an I/O error while acquiring a lease to the blob. |
| `java.lang.SecurityException` | when the blob represented by the`blobHandle`does not exist or the caller does not have access to it. |
| `java.lang.IllegalArgumentException` | when`blobHandle`is invalid or if the`leaseExpiryTimeMillis`is greater than the [BlobHandle.getExpiryTimeMillis()](https://developer.android.com/reference/kotlin/android/app/blob/BlobHandle#getExpiryTimeMillis()). |
| --- | --- |
| `android.os.LimitExceededException` | when a lease could not be acquired, such as when the caller is trying to acquire too many leases or acquire leases on too much data. Apps can avoid this by checking the remaining quota using [getRemainingLeaseQuotaBytes()](https://developer.android.com/reference/kotlin/android/app/blob/BlobStoreManager#getRemainingLeaseQuotaBytes())before trying to acquire a lease. |

**See Also**

- [#acquireLease(BlobHandle, int)](https://developer.android.com/reference/kotlin/android/app/blob/BlobStoreManager#acquireLease(android.app.blob.BlobHandle,%20kotlin.Int))
- [#acquireLease(BlobHandle, CharSequence)](https://developer.android.com/reference/kotlin/android/app/blob/BlobStoreManager#acquireLease(android.app.blob.BlobHandle,%20kotlin.CharSequence)) 

### acquireLease

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun acquireLease(
    blobHandle: BlobHandle, 
    description: CharSequence
): Unit
```

Acquire a lease to the blob represented by`blobHandle`. This lease indicates to the system that the caller wants the blob to be kept around.

This is a variant of [acquireLease(android.app.blob.BlobHandle,int)](https://developer.android.com/reference/kotlin/android/app/blob/BlobStoreManager#acquireLease(android.app.blob.BlobHandle,%20kotlin.Int))taking a [CharSequence](https://developer.android.com/reference/kotlin/java/lang/CharSequence.html#) for`description`. It is highly recommended that callers only use this when a valid resource ID for`description`could not be provided. Otherwise, apps should prefer using [acquireLease(android.app.blob.BlobHandle,int)](https://developer.android.com/reference/kotlin/android/app/blob/BlobStoreManager#acquireLease(android.app.blob.BlobHandle,%20kotlin.Int))which will allow`description`to be localized.

This is similar to [acquireLease(android.app.blob.BlobHandle,java.lang.CharSequence,long)](https://developer.android.com/reference/kotlin/android/app/blob/BlobStoreManager#acquireLease(android.app.blob.BlobHandle,%20kotlin.CharSequence,%20kotlin.Long))except clients don't have to specify the lease expiry time upfront using this API and need to explicitly release the lease using [releaseLease(android.app.blob.BlobHandle)](https://developer.android.com/reference/kotlin/android/app/blob/BlobStoreManager#releaseLease(android.app.blob.BlobHandle))when they no longer like to keep a blob around.

Any active leases will be automatically released when the blob's expiry time ([BlobHandle.getExpiryTimeMillis()](https://developer.android.com/reference/kotlin/android/app/blob/BlobHandle#getExpiryTimeMillis())) is elapsed.

This lease information is persisted and calling this more than once will result in latest lease overriding any previous lease.

When an app acquires a lease on a blob, the System will try to keep this blob around but note that it can still be deleted if it was requested by the user.

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `blobHandle` | [BlobHandle](https://developer.android.com/reference/kotlin/android/app/blob/BlobHandle):the [BlobHandle](https://developer.android.com/reference/kotlin/android/app/blob/BlobHandle) representing the blob that the caller wants to acquire a lease for. This value cannot be`null`. |
| `description` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html):a short description string that can be surfaced to the user explaining what the blob is used for. It is recommended to keep this description brief. This may be truncated and ellipsized if it is too long to be displayed to the user. This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | when there is an I/O error while acquiring a lease to the blob. |
| `java.lang.SecurityException` | when the blob represented by the`blobHandle`does not exist or the caller does not have access to it. |
| `java.lang.IllegalArgumentException` | when`blobHandle`is invalid. |
| --- | --- |
| `android.os.LimitExceededException` | when a lease could not be acquired, such as when the caller is trying to acquire too many leases or acquire leases on too much data. Apps can avoid this by checking the remaining quota using [getRemainingLeaseQuotaBytes()](https://developer.android.com/reference/kotlin/android/app/blob/BlobStoreManager#getRemainingLeaseQuotaBytes())before trying to acquire a lease. |

**See Also**

- [#acquireLease(BlobHandle, int)](https://developer.android.com/reference/kotlin/android/app/blob/BlobStoreManager#acquireLease(android.app.blob.BlobHandle,%20kotlin.Int))
- [#acquireLease(BlobHandle, CharSequence, long)](https://developer.android.com/reference/kotlin/android/app/blob/BlobStoreManager#acquireLease(android.app.blob.BlobHandle,%20kotlin.CharSequence,%20kotlin.Long)) 

### acquireLease

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun acquireLease(
    blobHandle: BlobHandle, 
    description: CharSequence, 
    leaseExpiryTimeMillis: Long
): Unit
```

Acquire a lease to the blob represented by`blobHandle`. This lease indicates to the system that the caller wants the blob to be kept around.

This is a variant of [acquireLease(android.app.blob.BlobHandle,int,long)](https://developer.android.com/reference/kotlin/android/app/blob/BlobStoreManager#acquireLease(android.app.blob.BlobHandle,%20kotlin.Int,%20kotlin.Long))taking a [CharSequence](https://developer.android.com/reference/kotlin/java/lang/CharSequence.html#) for`description`. It is highly recommended that callers only use this when a valid resource ID for`description`could not be provided. Otherwise, apps should prefer using [acquireLease(android.app.blob.BlobHandle,int)](https://developer.android.com/reference/kotlin/android/app/blob/BlobStoreManager#acquireLease(android.app.blob.BlobHandle,%20kotlin.Int))which will allow`description`to be localized.

Any active leases will be automatically released when the blob's expiry time ([BlobHandle.getExpiryTimeMillis()](https://developer.android.com/reference/kotlin/android/app/blob/BlobHandle#getExpiryTimeMillis())) is elapsed.

This lease information is persisted and calling this more than once will result in latest lease overriding any previous lease.

When an app acquires a lease on a blob, the System will try to keep this blob around but note that it can still be deleted if it was requested by the user.

| Parameters ||
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `blobHandle` | [BlobHandle](https://developer.android.com/reference/kotlin/android/app/blob/BlobHandle):the [BlobHandle](https://developer.android.com/reference/kotlin/android/app/blob/BlobHandle) representing the blob that the caller wants to acquire a lease for. This value cannot be`null`. |
| `description` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html):a short description string that can be surfaced to the user explaining what the blob is used for. It is recommended to keep this description brief. This may be truncated and ellipsized if it is too long to be displayed to the user. This value cannot be`null`. |
| `leaseExpiryTimeMillis` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the time in milliseconds after which the lease can be automatically released, in [System.currentTimeMillis()](https://developer.android.com/reference/kotlin/java/lang/System.html#currentTimeMillis())timebase. If its value is`0`, then the behavior of this API is identical to [acquireLease(android.app.blob.BlobHandle,int)](https://developer.android.com/reference/kotlin/android/app/blob/BlobStoreManager#acquireLease(android.app.blob.BlobHandle,%20kotlin.Int))where clients have to explicitly call [releaseLease(android.app.blob.BlobHandle)](https://developer.android.com/reference/kotlin/android/app/blob/BlobStoreManager#releaseLease(android.app.blob.BlobHandle))when they don't need the blob anymore. Value is a non-negative timestamp measured as the number of milliseconds since 1970-01-01T00:00:00Z. |
| --- | --- |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | when there is an I/O error while acquiring a lease to the blob. |
| `java.lang.SecurityException` | when the blob represented by the`blobHandle`does not exist or the caller does not have access to it. |
| `java.lang.IllegalArgumentException` | when`blobHandle`is invalid or if the`leaseExpiryTimeMillis`is greater than the [BlobHandle.getExpiryTimeMillis()](https://developer.android.com/reference/kotlin/android/app/blob/BlobHandle#getExpiryTimeMillis()). |
| --- | --- |
| `android.os.LimitExceededException` | when a lease could not be acquired, such as when the caller is trying to acquire too many leases or acquire leases on too much data. Apps can avoid this by checking the remaining quota using [getRemainingLeaseQuotaBytes()](https://developer.android.com/reference/kotlin/android/app/blob/BlobStoreManager#getRemainingLeaseQuotaBytes())before trying to acquire a lease. |

**See Also**

- [#acquireLease(BlobHandle, int, long)](https://developer.android.com/reference/kotlin/android/app/blob/BlobStoreManager#acquireLease(android.app.blob.BlobHandle,%20kotlin.Int,%20kotlin.Long))
- [#acquireLease(BlobHandle, CharSequence)](https://developer.android.com/reference/kotlin/android/app/blob/BlobStoreManager#acquireLease(android.app.blob.BlobHandle,%20kotlin.CharSequence)) 

### createSession

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun createSession(blobHandle: BlobHandle): Long
```

Create a new session using the given [BlobHandle](https://developer.android.com/reference/kotlin/android/app/blob/BlobHandle), returning a unique id that represents the session. Once created, the session can be opened multiple times across multiple device boots.

The system may automatically destroy sessions that have not been finalized (either committed or abandoned) within a reasonable period of time, typically about a week.

If an app is planning to acquire a lease on this data (using [acquireLease(android.app.blob.BlobHandle,int)](https://developer.android.com/reference/kotlin/android/app/blob/BlobStoreManager#acquireLease(android.app.blob.BlobHandle,%20kotlin.Int))or one of it's other variants) after committing this data (using [Session.commit(Executor, Consumer)](https://developer.android.com/reference/kotlin/android/app/blob/BlobStoreManager.Session#commit(java.util.concurrent.Executor,%20java.util.function.Consumer))), it is recommended that the app checks the remaining quota for acquiring a lease first using [getRemainingLeaseQuotaBytes()](https://developer.android.com/reference/kotlin/android/app/blob/BlobStoreManager#getRemainingLeaseQuotaBytes())and can skip contributing this data if needed.

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `blobHandle` | [BlobHandle](https://developer.android.com/reference/kotlin/android/app/blob/BlobHandle):the [BlobHandle](https://developer.android.com/reference/kotlin/android/app/blob/BlobHandle) identifier for which a new session needs to be created. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | positive, non-zero unique id that represents the created session. This id remains consistent across device reboots until the session is finalized. IDs are not reused during a given boot. Value is 1 or greater |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | when there is an I/O error while creating the session. |
| `java.lang.SecurityException` | when the caller is not allowed to create a session, such as when called from an Instant app. |
| `java.lang.IllegalArgumentException` | when`blobHandle`is invalid. |
| --- | --- |
| `android.os.LimitExceededException` | when a new session could not be created, such as when the caller is trying to create too many sessions. |

### getLeasedBlobs

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLeasedBlobs(): MutableList<BlobHandle!>
```

Return the [BlobHandles](https://developer.android.com/reference/kotlin/android/app/blob/BlobHandle) corresponding to the data blobs that the calling app currently has a lease on.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [BlobHandle](https://developer.android.com/reference/kotlin/android/app/blob/BlobHandle)!> | a list of [BlobHandles](https://developer.android.com/reference/kotlin/android/app/blob/BlobHandle) that the caller has a lease on. This value cannot be`null`. |

### getRemainingLeaseQuotaBytes

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRemainingLeaseQuotaBytes(): Long
```

Return the remaining quota size for acquiring a lease (in bytes) which indicates the remaining amount of data that an app can acquire a lease on before the System starts rejecting lease requests. If an app wants to acquire a lease on a blob but the remaining quota size is not sufficient, then it can try releasing leases on any older blobs which are not needed anymore.

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the remaining quota size for acquiring a lease. Value is 0 or greater |

### openBlob

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun openBlob(blobHandle: BlobHandle): ParcelFileDescriptor
```

Opens an existing blob for reading from the blob store managed by the system.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `blobHandle` | [BlobHandle](https://developer.android.com/reference/kotlin/android/app/blob/BlobHandle):the [BlobHandle](https://developer.android.com/reference/kotlin/android/app/blob/BlobHandle) representing the blob that the caller wants to access. This value cannot be`null`. |

| Return ||
|--------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#) | a [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#) that can be used to read the blob content. This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | when there is an I/O while opening the blob for read. |
| `java.lang.IllegalArgumentException` | when`blobHandle`is invalid. |
| `java.lang.SecurityException` | when the blob represented by the`blobHandle`does not exist or the caller does not have access to it. |
| --- | --- |

### openSession

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun openSession(sessionId: Long): BlobStoreManager.Session
```

Open an existing session to actively perform work.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sessionId` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):a unique id obtained via [createSession(android.app.blob.BlobHandle)](https://developer.android.com/reference/kotlin/android/app/blob/BlobStoreManager#createSession(android.app.blob.BlobHandle))that represents a particular session. Value is 1 or greater |

| Return ||
|----------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [BlobStoreManager.Session](https://developer.android.com/reference/kotlin/android/app/blob/BlobStoreManager.Session) | the [Session](https://developer.android.com/reference/kotlin/android/app/blob/BlobStoreManager.Session) object corresponding to the`sessionId`. This value cannot be`null`. |

| Exceptions ||
|-------------------------------|----------------------------------------------------------------------------------------|
| `java.io.IOException` | when there is an I/O error while opening the session. |
| `java.lang.SecurityException` | when the caller does not own the session, or the session does not exist or is invalid. |

### releaseLease

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun releaseLease(blobHandle: BlobHandle): Unit
```

Release any active lease to the blob represented by`blobHandle`which is currently held by the caller.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `blobHandle` | [BlobHandle](https://developer.android.com/reference/kotlin/android/app/blob/BlobHandle):the [BlobHandle](https://developer.android.com/reference/kotlin/android/app/blob/BlobHandle) representing the blob that the caller wants to release the lease for. This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | when there is an I/O error while releasing the release to the blob. |
| `java.lang.SecurityException` | when the blob represented by the`blobHandle`does not exist or the caller does not have access to it. |
| `java.lang.IllegalArgumentException` | when`blobHandle`is invalid. |
| --- | --- |
