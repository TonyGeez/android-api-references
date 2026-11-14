# PreferenceManager.OnActivityDestroyListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnActivityDestroyListener

Kotlin| [Java](https://developer.android.com/reference/android/preference/PreferenceManager.OnActivityDestroyListener "View this page in Java") 
| --- | --- |

```
interface OnActivityDestroyListener
```

| [android.preference.PreferenceManager.OnActivityDestroyListener](https://developer.android.com/reference/kotlin/android/preference/PreferenceManager.OnActivityDestroyListener#) |

| Known Direct Subclasses [DialogPreference](https://developer.android.com/reference/kotlin/android/preference/DialogPreference) |--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------| | [DialogPreference](https://developer.android.com/reference/kotlin/android/preference/DialogPreference) | A base class for [Preference](https://developer.android.com/reference/kotlin/android/preference/Preference) objects that are dialog-based. | |
| --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [EditTextPreference](https://developer.android.com/reference/kotlin/android/preference/EditTextPreference), [ListPreference](https://developer.android.com/reference/kotlin/android/preference/ListPreference), [MultiSelectListPreference](https://developer.android.com/reference/kotlin/android/preference/MultiSelectListPreference) |--------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------| | [EditTextPreference](https://developer.android.com/reference/kotlin/android/preference/EditTextPreference) | A [Preference](https://developer.android.com/reference/kotlin/android/preference/Preference) that allows for string input. | | [ListPreference](https://developer.android.com/reference/kotlin/android/preference/ListPreference) | A [Preference](https://developer.android.com/reference/kotlin/android/preference/Preference) that displays a list of entries as a dialog. | | [MultiSelectListPreference](https://developer.android.com/reference/kotlin/android/preference/MultiSelectListPreference) | A [Preference](https://developer.android.com/reference/kotlin/android/preference/Preference) that displays a list of entries as a dialog. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| **This interface was deprecated in API level 29.**
|
| Use the [AndroidX](https://developer.android.com/jetpack/androidx.html) [Preference Library](https://developer.android.com/reference/androidx/preference/package-summary.html) for consistent behavior across all devices. For more information on using the AndroidX Preference Library see [Settings](https://developer.android.com/guide/topics/ui/settings.html).

Interface definition for a class that will be called when the container's activity is destroyed.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onActivityDestroy](https://developer.android.com/reference/kotlin/android/preference/PreferenceManager.OnActivityDestroyListener#onActivityDestroy())`()` See Activity's onDestroy. |

## Public methods

### onActivityDestroy

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onActivityDestroy(): Unit
```

**Deprecated:** *Deprecated in Java.*

See Activity's onDestroy.
