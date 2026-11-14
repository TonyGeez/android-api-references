# Application.OnProvideAssistDataListener

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnProvideAssistDataListener

Kotlin| [Java](https://developer.android.com/reference/android/app/Application.OnProvideAssistDataListener "View this page in Java") 
| --- | --- |

```
interface OnProvideAssistDataListener
```

| [android.app.Application.OnProvideAssistDataListener](https://developer.android.com/reference/kotlin/android/app/Application.OnProvideAssistDataListener#) |

Callback interface for use with [Application.registerOnProvideAssistDataListener](https://developer.android.com/reference/kotlin/android/app/Application#registerOnProvideAssistDataListener(android.app.Application.OnProvideAssistDataListener))and [Application.unregisterOnProvideAssistDataListener](https://developer.android.com/reference/kotlin/android/app/Application#unregisterOnProvideAssistDataListener(android.app.Application.OnProvideAssistDataListener)).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onProvideAssistData](https://developer.android.com/reference/kotlin/android/app/Application.OnProvideAssistDataListener#onProvideAssistData(android.app.Activity,%20android.os.Bundle))`(`activity:` ` [Activity](https://developer.android.com/reference/kotlin/android/app/Activity)!`, `data:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`)` This is called when the user is requesting an assist, to build a full [Intent.ACTION_ASSIST](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_ASSIST:kotlin.String) Intent with all of the context of the current application. |

## Public methods

### onProvideAssistData

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onProvideAssistData(
    activity: Activity!, 
    data: Bundle!
): Unit
```

This is called when the user is requesting an assist, to build a full [Intent.ACTION_ASSIST](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_ASSIST:kotlin.String) Intent with all of the context of the current application. You can override this method to place into the bundle anything you would like to appear in the [Intent.EXTRA_ASSIST_CONTEXT](https://developer.android.com/reference/kotlin/android/content/Intent.html#EXTRA_ASSIST_CONTEXT:kotlin.String) part of the assist Intent.
