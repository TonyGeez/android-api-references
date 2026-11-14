# SharedElementCallback.OnSharedElementsReadyListener

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnSharedElementsReadyListener

Kotlin| [Java](../android/app/SharedElementCallback.OnSharedElementsReadyListener.md) 
| --- | --- |

```
interface OnSharedElementsReadyListener
```

| [android.app.SharedElementCallback.OnSharedElementsReadyListener](../android/app/SharedElementCallback.OnSharedElementsReadyListener.md) |

Listener to be called after [android.app.SharedElementCallback#onSharedElementsArrived(java.util.List,java.util.List,android.app.SharedElementCallback.OnSharedElementsReadyListener)](../android/app/SharedElementCallback.md))when the shared elements are ready to be hidden in the source Activity and shown in the destination Activity.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSharedElementsReady](../android/app/SharedElementCallback.OnSharedElementsReadyListener.md))`()` Call this method during or after the OnSharedElementsReadyListener has been received in [SharedElementCallback.onSharedElementsArrived(List, List,](../android/app/SharedElementCallback.md))to indicate that the shared elements are ready to be hidden in the source and shown in the destination Activity. |

## Public methods

### onSharedElementsReady

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onSharedElementsReady(): Unit
```

Call this method during or after the OnSharedElementsReadyListener has been received in [SharedElementCallback.onSharedElementsArrived(List, List,](../android/app/SharedElementCallback.md))to indicate that the shared elements are ready to be hidden in the source and shown in the destination Activity.
