# SharedElementCallback.OnSharedElementsReadyListener

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnSharedElementsReadyListener

Kotlin| [Java](https://developer.android.com/reference/android/app/SharedElementCallback.OnSharedElementsReadyListener "View this page in Java") 

```
interface OnSharedElementsReadyListener
```

| [android.app.SharedElementCallback.OnSharedElementsReadyListener](https://developer.android.com/reference/kotlin/android/app/SharedElementCallback.OnSharedElementsReadyListener#) |

Listener to be called after [android.app.SharedElementCallback#onSharedElementsArrived(java.util.List,java.util.List,android.app.SharedElementCallback.OnSharedElementsReadyListener)](https://developer.android.com/reference/kotlin/android/app/SharedElementCallback#onSharedElementsArrived(kotlin.collections.MutableList,%20kotlin.collections.MutableList,%20android.app.SharedElementCallback.OnSharedElementsReadyListener))when the shared elements are ready to be hidden in the source Activity and shown in the destination Activity.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSharedElementsReady](https://developer.android.com/reference/kotlin/android/app/SharedElementCallback.OnSharedElementsReadyListener#onSharedElementsReady())`()` Call this method during or after the OnSharedElementsReadyListener has been received in [SharedElementCallback.onSharedElementsArrived(List, List,](https://developer.android.com/reference/kotlin/android/app/SharedElementCallback#onSharedElementsArrived(kotlin.collections.MutableList,%20kotlin.collections.MutableList,%20android.app.SharedElementCallback.OnSharedElementsReadyListener))to indicate that the shared elements are ready to be hidden in the source and shown in the destination Activity. |

## Public methods

### onSharedElementsReady

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onSharedElementsReady(): Unit
```

Call this method during or after the OnSharedElementsReadyListener has been received in [SharedElementCallback.onSharedElementsArrived(List, List,](https://developer.android.com/reference/kotlin/android/app/SharedElementCallback#onSharedElementsArrived(kotlin.collections.MutableList,%20kotlin.collections.MutableList,%20android.app.SharedElementCallback.OnSharedElementsReadyListener))to indicate that the shared elements are ready to be hidden in the source and shown in the destination Activity.
