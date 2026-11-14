# Preference.OnPreferenceChangeListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnPreferenceChangeListener

Kotlin| [Java](https://developer.android.com/reference/android/preference/Preference.OnPreferenceChangeListener "View this page in Java") 
| --- | --- |

```
interface OnPreferenceChangeListener
```

| [android.preference.Preference.OnPreferenceChangeListener](https://developer.android.com/reference/kotlin/android/preference/Preference.OnPreferenceChangeListener#) |

| **This interface was deprecated in API level 29.**
|
| Use the [AndroidX](https://developer.android.com/jetpack/androidx.html) [Preference Library](https://developer.android.com/reference/androidx/preference/package-summary.html) for consistent behavior across all devices. For more information on using the AndroidX Preference Library see [Settings](https://developer.android.com/guide/topics/ui/settings.html).

Interface definition for a callback to be invoked when the value of this [Preference](https://developer.android.com/reference/kotlin/android/preference/Preference) has been changed by the user and is about to be set and/or persisted. This gives the client a chance to prevent setting and/or persisting the value.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onPreferenceChange](https://developer.android.com/reference/kotlin/android/preference/Preference.OnPreferenceChangeListener#onPreferenceChange(android.preference.Preference,%20kotlin.Any))`(`preference:` ` [Preference](https://developer.android.com/reference/kotlin/android/preference/Preference)!`, `newValue:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Called when a Preference has been changed by the user. |

## Public methods

### onPreferenceChange

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onPreferenceChange(
    preference: Preference!, 
    newValue: Any!
): Boolean
```

**Deprecated:** *Deprecated in Java.*

Called when a Preference has been changed by the user. This is called before the state of the Preference is about to be updated and before the state is persisted.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------|
| `preference` | [Preference](https://developer.android.com/reference/kotlin/android/preference/Preference)!:The changed Preference. |
| `newValue` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:The new value of the Preference. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True to update the state of the Preference with the new value. |
