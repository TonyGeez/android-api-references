# PreferenceFragment.OnPreferenceStartFragmentCallback

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnPreferenceStartFragmentCallback

Kotlin| [Java](../android/preference/PreferenceFragment.OnPreferenceStartFragmentCallback.md) 
| --- | --- |

```
interface OnPreferenceStartFragmentCallback
```

| [android.preference.PreferenceFragment.OnPreferenceStartFragmentCallback](../android/preference/PreferenceFragment.OnPreferenceStartFragmentCallback.md) |

| Known Direct Subclasses [PreferenceActivity](PreferenceActivity.md) |------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------| | [PreferenceActivity](PreferenceActivity.md) | This is the base class for an activity to show a hierarchy of preferences to the user. | |
| --- | --- | --- | --- | --- | --- | --- |

| **This interface was deprecated in API level 28.**
|
| Use

Interface that PreferenceFragment's containing activity should implement to be able to process preference items that wish to switch to a new fragment.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onPreferenceStartFragment](../android/preference/PreferenceFragment.OnPreferenceStartFragmentCallback.md))`(`caller:` ` [PreferenceFragment](PreferenceFragment.md)!`, `pref:` ` [Preference](Preference.md)!`)` Called when the user has clicked on a Preference that has a fragment class name associated with it. |

## Public methods

### onPreferenceStartFragment

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onPreferenceStartFragment(
    caller: PreferenceFragment!, 
    pref: Preference!
): Boolean
```

**Deprecated:** *Deprecated in Java.*

Called when the user has clicked on a Preference that has a fragment class name associated with it. The implementation to should instantiate and switch to an instance of the given fragment.
