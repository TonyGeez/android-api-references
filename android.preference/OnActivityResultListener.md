# PreferenceManager.OnActivityResultListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnActivityResultListener

Kotlin| [Java](../android/preference/PreferenceManager.OnActivityResultListener.md) 
| --- | --- |

```
interface OnActivityResultListener
```

| [android.preference.PreferenceManager.OnActivityResultListener](../android/preference/PreferenceManager.OnActivityResultListener.md) |

| Known Direct Subclasses [RingtonePreference](RingtonePreference.md) |------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------| | [RingtonePreference](RingtonePreference.md) | A [Preference](Preference.md) that allows the user to choose a ringtone from those on the device. | |
| --- | --- | --- | --- | --- | --- | --- |

| **This interface was deprecated in API level 29.**
|
| Use the [AndroidX](https://developer.android.com/jetpack/androidx.html) [Preference Library](../androidx/preference/_package.md) for consistent behavior across all devices. For more information on using the AndroidX Preference Library see [Settings](https://developer.android.com/guide/topics/ui/settings.html).

Interface definition for a class that will be called when the container's activity receives an activity result.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onActivityResult](../android/preference/PreferenceManager.OnActivityResultListener.md))`(`requestCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `resultCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `data:` ` [Intent](../android.content/Intent.md)!`)` See Activity's onActivityResult. |

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
