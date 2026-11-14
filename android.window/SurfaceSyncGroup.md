# SurfaceSyncGroup

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SurfaceSyncGroup

Kotlin| [Java](https://developer.android.com/reference/android/window/SurfaceSyncGroup "View this page in Java") 
| --- | --- |

```
class SurfaceSyncGroup
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.window.SurfaceSyncGroup](https://developer.android.com/reference/kotlin/android/window/SurfaceSyncGroup#) |

A way for data to be gathered so multiple surfaces can be synced. This is intended to be used with AttachedSurfaceControl, SurfaceView, and SurfaceControlViewHost. This allows different parts of the system to synchronize different surfaces themselves without having to manage timing of different rendering threads. This will also allow synchronization of surfaces across multiple processes. The caller can add SurfaceControlViewHosts from another process to the SurfaceSyncGroup in a different process and this clas will ensure all the surfaces are ready before applying everything together. see the [SurfaceSyncGroup documentation](https://android.googlesource.com/platform/frameworks/base/+/master/core/java/android/window/SurfaceSyncGroup.md)

<br />

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SurfaceSyncGroup](https://developer.android.com/reference/kotlin/android/window/SurfaceSyncGroup#SurfaceSyncGroup(kotlin.String))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Starts a sync and will automatically apply the final, merged transaction. |

| Public methods ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [add](https://developer.android.com/reference/kotlin/android/window/SurfaceSyncGroup#add(android.view.AttachedSurfaceControl,%20java.lang.Runnable))`(`attachedSurfaceControl:` ` [AttachedSurfaceControl](https://developer.android.com/reference/kotlin/android/view/AttachedSurfaceControl.html#)?`, `runnable:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)?`)` Add an AttachedSurfaceControl to the SurfaceSyncGroup. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [add](https://developer.android.com/reference/kotlin/android/window/SurfaceSyncGroup#add(android.view.SurfaceControlViewHost.SurfacePackage,%20java.lang.Runnable))`(`surfacePackage:` ` [SurfaceControlViewHost.SurfacePackage](https://developer.android.com/reference/kotlin/android/view/SurfaceControlViewHost.SurfacePackage.html#)`, `runnable:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)?`)` Add a SurfaceControlViewHost. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addTransaction](https://developer.android.com/reference/kotlin/android/window/SurfaceSyncGroup#addTransaction(android.view.SurfaceControl.Transaction))`(`transaction:` ` [SurfaceControl.Transaction](https://developer.android.com/reference/kotlin/android/view/SurfaceControl.Transaction.html#)`)` Add a Transaction to this SurfaceSyncGroup. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [markSyncReady](https://developer.android.com/reference/kotlin/android/window/SurfaceSyncGroup#markSyncReady())`()` Mark the SurfaceSyncGroup as ready to complete. |

## Public constructors

### SurfaceSyncGroup

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SurfaceSyncGroup(name: String)
```

Starts a sync and will automatically apply the final, merged transaction.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):Used for identifying and debugging. This value cannot be`null`. |

## Public methods

### add

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun add(
    attachedSurfaceControl: AttachedSurfaceControl?, 
    runnable: Runnable?
): Boolean
```

Add an AttachedSurfaceControl to the SurfaceSyncGroup. The AttachedSurfaceControl will pause rendering to ensure the runnable can be invoked and that the sync picks up the frame that contains the changes. 
This method must be called on the thread that originally created this UI element. This is typically the [main thread](https://developer.android.com/reference/kotlin/android/os/Looper.html#getMainLooper())of your app.

| Parameters ||
|--------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `attachedSurfaceControl` | [AttachedSurfaceControl](https://developer.android.com/reference/kotlin/android/view/AttachedSurfaceControl.html#)?:The AttachedSurfaceControl that will be add to this SurfaceSyncGroup. This value may be`null`. |
| `runnable` | [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)?:This is run on the same thread that the call was made on, but after the rendering is paused and before continuing to render the next frame. This method will not return until the execution of the runnable completes. This can be used to make changes to the AttachedSurfaceControl, ensuring that the changes are included in the sync. This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the AttachedSurfaceControl was successfully added to the SurfaceSyncGroup, false otherwise. |

### add

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun add(
    surfacePackage: SurfaceControlViewHost.SurfacePackage, 
    runnable: Runnable?
): Boolean
```

Add a SurfaceControlViewHost.SurfacePackage to the SurfaceSyncGroup. This will get the SurfaceSyncGroup from the SurfacePackage, which will pause rendering for the SurfaceControlViewHost. The runnable will be invoked to allow the host to update the SCVH in a synchronized way. Finally, it will add the SCVH to the SurfaceSyncGroup and unpause rendering in the SCVH, allowing the changes to get picked up and included in the sync.

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `surfacePackage` | [SurfaceControlViewHost.SurfacePackage](https://developer.android.com/reference/kotlin/android/view/SurfaceControlViewHost.SurfacePackage.html#):The SurfacePackage that will be added to this SurfaceSyncGroup. This value cannot be`null`. |
| `runnable` | [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)?:This is run on the same thread that the call was made on, but after the rendering is paused and before continuing to render the next frame. This method will not return until the execution of the runnable completes. This can be used to make changes to the SurfaceControlViewHost, ensuring that the changes are included in the sync. This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the SurfaceControlViewHost was successfully added to the current SurfaceSyncGroup, false otherwise. |

### addTransaction

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun addTransaction(transaction: SurfaceControl.Transaction): Unit
```

Add a Transaction to this SurfaceSyncGroup. This allows the caller to provide other info that should be synced with the other transactions in this SurfaceSyncGroup.

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `transaction` | [SurfaceControl.Transaction](https://developer.android.com/reference/kotlin/android/view/SurfaceControl.Transaction.html#):The transaction to add to the SurfaceSyncGroup. This value cannot be`null`. |

### markSyncReady

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun markSyncReady(): Unit
```

Mark the SurfaceSyncGroup as ready to complete. No more data can be added to this SurfaceSyncGroup.

Once the SurfaceSyncGroup is marked as ready, it will be able to complete once all child SurfaceSyncGroup have completed their sync.
