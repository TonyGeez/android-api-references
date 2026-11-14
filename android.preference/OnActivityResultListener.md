# PreferenceManager.OnActivityResultListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnActivityResultListener

Kotlin| [Java](https://developer.android.com/reference/android/preference/PreferenceManager.OnActivityResultListener "View this page in Java") 
| --- | --- |

```
interface OnActivityResultListener
```

| [android.preference.PreferenceManager.OnActivityResultListener](https://developer.android.com/reference/kotlin/android/preference/PreferenceManager.OnActivityResultListener#) |

| Known Direct Subclasses [RingtonePreference](https://developer.android.com/reference/kotlin/android/preference/RingtonePreference) |------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------| | [RingtonePreference](https://developer.android.com/reference/kotlin/android/preference/RingtonePreference) | A [Preference](https://developer.android.com/reference/kotlin/android/preference/Preference) that allows the user to choose a ringtone from those on the device. | |
| --- | --- | --- | --- | --- | --- | --- |

| **This interface was deprecated in API level 29.**
|
| Use the [AndroidX](https://developer.android.com/jetpack/androidx.html) [Preference Library](https://developer.android.com/reference/androidx/preference/package-summary.html) for consistent behavior across all devices. For more information on using the AndroidX Preference Library see [Settings](https://developer.android.com/guide/topics/ui/settings.html).

Interface definition for a class that will be called when the container's activity receives an activity result.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onActivityResult](https://developer.android.com/reference/kotlin/android/preference/PreferenceManager.OnActivityResultListener#onActivityResult(kotlin.Int,%20kotlin.Int,%20android.content.Intent))`(`requestCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `resultCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `data:` ` [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!`)` See Activity's onActivityResult. |

## Public methods

### onActivityResult

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onActivityResult(
    requestCode: Int, 
    resultCode: Int, 
    data: Intent!
): Boolean
```

**Deprecated:** *Deprecated in Java.*

See Activity's onActivityResult.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Whether the request code was handled (in which case subsequent listeners will not be called. |
