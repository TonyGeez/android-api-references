# Application.OnProvideAssistDataListener

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnProvideAssistDataListener

Kotlin| [Java](../android/app/Application.OnProvideAssistDataListener.md) 
| --- | --- |

```
interface OnProvideAssistDataListener
```

| [android.app.Application.OnProvideAssistDataListener](../android/app/Application.OnProvideAssistDataListener.md) |

Callback interface for use with [Application.registerOnProvideAssistDataListener](Application.md))and [Application.unregisterOnProvideAssistDataListener](Application.md)).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onProvideAssistData](../android/app/Application.OnProvideAssistDataListener.md))`(`activity:` ` [Activity](Activity.md)!`, `data:` ` [Bundle](../android.os/Bundle.md)!`)` This is called when the user is requesting an assist, to build a full [Intent.ACTION_ASSIST](../android.content/Intent.md) Intent with all of the context of the current application. |

## Public methods

### onProvideAssistData

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onProvideAssistData(
    activity: Activity!, 
    data: Bundle!
): Unit
```

This is called when the user is requesting an assist, to build a full [Intent.ACTION_ASSIST](../android.content/Intent.md) Intent with all of the context of the current application. You can override this method to place into the bundle anything you would like to appear in the [Intent.EXTRA_ASSIST_CONTEXT](../android.content/Intent.md) part of the assist Intent.
