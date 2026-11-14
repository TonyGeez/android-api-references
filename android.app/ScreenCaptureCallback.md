# Activity.ScreenCaptureCallback

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ScreenCaptureCallback

Kotlin| [Java](https://developer.android.com/reference/android/app/Activity.ScreenCaptureCallback "View this page in Java") 

```
interface ScreenCaptureCallback
```

| [android.app.Activity.ScreenCaptureCallback](https://developer.android.com/reference/kotlin/android/app/Activity.ScreenCaptureCallback#) |

Interface for observing screen captures of an [Activity](https://developer.android.com/reference/kotlin/android/app/Activity).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onScreenCaptured](https://developer.android.com/reference/kotlin/android/app/Activity.ScreenCaptureCallback#onScreenCaptured())`()` Called when one of the monitored activities is captured. |

## Public methods

### onScreenCaptured

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onScreenCaptured(): Unit
```

Called when one of the monitored activities is captured. This is not invoked if the activity window has [WindowManager.LayoutParams.FLAG_SECURE](https://developer.android.com/reference/kotlin/android/view/WindowManager.LayoutParams.html#FLAG_SECURE:kotlin.Int) set.
