# PreferenceManager.OnActivityDestroyListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnActivityDestroyListener

Kotlin| [Java](../android/preference/PreferenceManager.OnActivityDestroyListener.md) 
| --- | --- |

```
interface OnActivityDestroyListener
```

| [android.preference.PreferenceManager.OnActivityDestroyListener](../android/preference/PreferenceManager.OnActivityDestroyListener.md) |

| Known Direct Subclasses [DialogPreference](DialogPreference.md) |--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------| | [DialogPreference](DialogPreference.md) | A base class for [Preference](Preference.md) objects that are dialog-based. | |
| --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [EditTextPreference](EditTextPreference.md), [ListPreference](ListPreference.md), [MultiSelectListPreference](MultiSelectListPreference.md) |--------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------| | [EditTextPreference](EditTextPreference.md) | A [Preference](Preference.md) that allows for string input. | | [ListPreference](ListPreference.md) | A [Preference](Preference.md) that displays a list of entries as a dialog. | | [MultiSelectListPreference](MultiSelectListPreference.md) | A [Preference](Preference.md) that displays a list of entries as a dialog. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| **This interface was deprecated in API level 29.**
|
| Use the [AndroidX](https://developer.android.com/jetpack/androidx.html) [Preference Library](../androidx/preference/_package.md) for consistent behavior across all devices. For more information on using the AndroidX Preference Library see [Settings](https://developer.android.com/guide/topics/ui/settings.html).

Interface definition for a class that will be called when the container's activity is destroyed.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onActivityDestroy](../android/preference/PreferenceManager.OnActivityDestroyListener.md))`()` See Activity's onDestroy. |

## Public methods

### onActivityDestroy

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onActivityDestroy(): Unit
```

**Deprecated:** *Deprecated in Java.*

See Activity's onDestroy.
