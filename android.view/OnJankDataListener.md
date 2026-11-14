# SurfaceControl.OnJankDataListener

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnJankDataListener

Kotlin| [Java](https://developer.android.com/reference/android/view/SurfaceControl.OnJankDataListener "View this page in Java") 
| --- | --- |

```
interface OnJankDataListener
```

| [android.view.SurfaceControl.OnJankDataListener](https://developer.android.com/reference/kotlin/android/view/SurfaceControl.OnJankDataListener#) |

Listener interface to be informed about SurfaceFlinger's jank classification for a specific surface.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onJankDataAvailable](https://developer.android.com/reference/kotlin/android/view/SurfaceControl.OnJankDataListener#onJankDataAvailable(kotlin.collections.MutableList))`(`jankData:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [SurfaceControl.JankData](https://developer.android.com/reference/kotlin/android/view/SurfaceControl.JankData)!>`)` Called when new jank classifications are available. |

## Public methods

### onJankDataAvailable

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onJankDataAvailable(jankData: MutableList<SurfaceControl.JankData!>): Unit
```

Called when new jank classifications are available. The listener is invoked out of band of the rendered frames with jank classification data for a batch of frames.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `jankData` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [SurfaceControl.JankData](https://developer.android.com/reference/kotlin/android/view/SurfaceControl.JankData)!\>:This value cannot be`null`. |
