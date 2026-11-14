# SurfaceSyncGroup

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SurfaceSyncGroup

Kotlin| [Java](SurfaceSyncGroup.md) 
| --- | --- |

```
class SurfaceSyncGroup
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.window.SurfaceSyncGroup](SurfaceSyncGroup.md) |

A way for data to be gathered so multiple surfaces can be synced. This is intended to be used with AttachedSurfaceControl, SurfaceView, and SurfaceControlViewHost. This allows different parts of the system to synchronize different surfaces themselves without having to manage timing of different rendering threads. This will also allow synchronization of surfaces across multiple processes. The caller can add SurfaceControlViewHosts from another process to the SurfaceSyncGroup in a different process and this clas will ensure all the surfaces are ready before applying everything together. see the [SurfaceSyncGroup documentation](https://android.googlesource.com/platform/frameworks/base/+/master/core/java/android/window/SurfaceSyncGroup.md)

<br />

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SurfaceSyncGroup](SurfaceSyncGroup.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Starts a sync and will automatically apply the final, merged transaction. |

| Public methods ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [add](SurfaceSyncGroup.md))`(`attachedSurfaceControl:` ` [AttachedSurfaceControl](../android.view/AttachedSurfaceControl.md)?`, `runnable:` ` [Runnable](../java.lang/Runnable.md)?`)` Add an AttachedSurfaceControl to the SurfaceSyncGroup. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [add](SurfaceSyncGroup.md))`(`surfacePackage:` ` [SurfaceControlViewHost.SurfacePackage](../android/view/SurfaceControlViewHost.SurfacePackage.md)`, `runnable:` ` [Runnable](../java.lang/Runnable.md)?`)` Add a SurfaceControlViewHost. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addTransaction](SurfaceSyncGroup.md))`(`transaction:` ` [SurfaceControl.Transaction](../android/view/SurfaceControl.Transaction.md)`)` Add a Transaction to this SurfaceSyncGroup. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [markSyncReady](SurfaceSyncGroup.md))`()` Mark the SurfaceSyncGroup as ready to complete. |

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
This method must be called on the thread that originally created this UI element. This is typically the [main thread](../android.os/Looper.md))of your app.

| Parameters ||
|--------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `attachedSurfaceControl` | [AttachedSurfaceControl](../android.view/AttachedSurfaceControl.md)?:The AttachedSurfaceControl that will be add to this SurfaceSyncGroup. This value may be`null`. |
| `runnable` | [Runnable](../java.lang/Runnable.md)?:This is run on the same thread that the call was made on, but after the rendering is paused and before continuing to render the next frame. This method will not return until the execution of the runnable completes. This can be used to make changes to the AttachedSurfaceControl, ensuring that the changes are included in the sync. This value may be`null`. |

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
| `surfacePackage` | [SurfaceControlViewHost.SurfacePackage](../android/view/SurfaceControlViewHost.SurfacePackage.md):The SurfacePackage that will be added to this SurfaceSyncGroup. This value cannot be`null`. |
| `runnable` | [Runnable](../java.lang/Runnable.md)?:This is run on the same thread that the call was made on, but after the rendering is paused and before continuing to render the next frame. This method will not return until the execution of the runnable completes. This can be used to make changes to the SurfaceControlViewHost, ensuring that the changes are included in the sync. This value may be`null`. |

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
| `transaction` | [SurfaceControl.Transaction](../android/view/SurfaceControl.Transaction.md):The transaction to add to the SurfaceSyncGroup. This value cannot be`null`. |

### markSyncReady

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun markSyncReady(): Unit
```

Mark the SurfaceSyncGroup as ready to complete. No more data can be added to this SurfaceSyncGroup.

Once the SurfaceSyncGroup is marked as ready, it will be able to complete once all child SurfaceSyncGroup have completed their sync.
