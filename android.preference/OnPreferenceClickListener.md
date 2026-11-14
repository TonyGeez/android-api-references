# Preference.OnPreferenceClickListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnPreferenceClickListener

Kotlin| [Java](https://developer.android.com/reference/android/preference/Preference.OnPreferenceClickListener "View this page in Java") 
| --- | --- |

```
interface OnPreferenceClickListener
```

| [android.preference.Preference.OnPreferenceClickListener](https://developer.android.com/reference/kotlin/android/preference/Preference.OnPreferenceClickListener#) |

| **This interface was deprecated in API level 29.**
|
| Use the [AndroidX](https://developer.android.com/jetpack/androidx.html) [Preference Library](https://developer.android.com/reference/androidx/preference/package-summary.html) for consistent behavior across all devices. For more information on using the AndroidX Preference Library see [Settings](https://developer.android.com/guide/topics/ui/settings.html).

Interface definition for a callback to be invoked when a [Preference](https://developer.android.com/reference/kotlin/android/preference/Preference) is clicked.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onPreferenceClick](https://developer.android.com/reference/kotlin/android/preference/Preference.OnPreferenceClickListener#onPreferenceClick(android.preference.Preference))`(`preference:` ` [Preference](https://developer.android.com/reference/kotlin/android/preference/Preference)!`)` Called when a Preference has been clicked. |

## Public methods

### onPreferenceClick

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onPreferenceClick(preference: Preference!): Boolean
```

**Deprecated:** *Deprecated in Java.*

Called when a Preference has been clicked.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------|
| `preference` | [Preference](https://developer.android.com/reference/kotlin/android/preference/Preference)!:The Preference that was clicked. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the click was handled. |
