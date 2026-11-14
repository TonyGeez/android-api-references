# Activity.ScreenCaptureCallback

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ScreenCaptureCallback

Kotlin| [Java](../android/app/Activity.ScreenCaptureCallback.md) 
| --- | --- |

```
interface ScreenCaptureCallback
```

| [android.app.Activity.ScreenCaptureCallback](../android/app/Activity.ScreenCaptureCallback.md) |

Interface for observing screen captures of an [Activity](Activity.md).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onScreenCaptured](../android/app/Activity.ScreenCaptureCallback.md))`()` Called when one of the monitored activities is captured. |

## Public methods

### onScreenCaptured

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onScreenCaptured(): Unit
```

Called when one of the monitored activities is captured. This is not invoked if the activity window has [WindowManager.LayoutParams.FLAG_SECURE](../android/view/WindowManager.LayoutParams.md) set.
