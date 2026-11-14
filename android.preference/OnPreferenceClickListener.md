# Preference.OnPreferenceClickListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnPreferenceClickListener

Kotlin| [Java](../android/preference/Preference.OnPreferenceClickListener.md) 
| --- | --- |

```
interface OnPreferenceClickListener
```

| [android.preference.Preference.OnPreferenceClickListener](../android/preference/Preference.OnPreferenceClickListener.md) |

| **This interface was deprecated in API level 29.**
|
| Use the [AndroidX](https://developer.android.com/jetpack/androidx.html) [Preference Library](../androidx/preference/_package.md) for consistent behavior across all devices. For more information on using the AndroidX Preference Library see [Settings](https://developer.android.com/guide/topics/ui/settings.html).

Interface definition for a callback to be invoked when a [Preference](../android/preference/Preference.md) is clicked.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onPreferenceClick](../android/preference/Preference.OnPreferenceClickListener.md))`(`preference:` ` [Preference](../android/preference/Preference.md)!`)` Called when a Preference has been clicked. |

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
| `preference` | [Preference](../android/preference/Preference.md)!:The Preference that was clicked. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the click was handled. |
