# PreferenceManager.OnActivityStopListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnActivityStopListener

Kotlin| [Java](https://developer.android.com/reference/android/preference/PreferenceManager.OnActivityStopListener "View this page in Java") 

```
interface OnActivityStopListener
```

| [android.preference.PreferenceManager.OnActivityStopListener](https://developer.android.com/reference/kotlin/android/preference/PreferenceManager.OnActivityStopListener#) |

| **This interface was deprecated in API level 29.**
|
| Use the [AndroidX](https://developer.android.com/jetpack/androidx.html) [Preference Library](https://developer.android.com/reference/androidx/preference/package-summary.html) for consistent behavior across all devices. For more information on using the AndroidX Preference Library see [Settings](https://developer.android.com/guide/topics/ui/settings.html).

Interface definition for a class that will be called when the container's activity is stopped.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onActivityStop](https://developer.android.com/reference/kotlin/android/preference/PreferenceManager.OnActivityStopListener#onActivityStop())`()` See Activity's onStop. |

## Public methods

### onActivityStop

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onActivityStop(): Unit
```

**Deprecated:** *Deprecated in Java.*

See Activity's onStop.
