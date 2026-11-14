# android.preference

# android.preference

Kotlin| [Java](https://developer.android.com/reference/android/preference/package-summary "View this page in Java")

## Interfaces

| [OnPreferenceChangeListener](https://developer.android.com/reference/kotlin/android/preference/Preference.OnPreferenceChangeListener) | Interface definition for a callback to be invoked when the value of this [Preference](https://developer.android.com/reference/kotlin/android/preference/Preference) has been changed by the user and is about to be set and/or persisted. |
| [OnPreferenceClickListener](https://developer.android.com/reference/kotlin/android/preference/Preference.OnPreferenceClickListener) | Interface definition for a callback to be invoked when a [Preference](https://developer.android.com/reference/kotlin/android/preference/Preference) is clicked. |
| [PreferenceDataStore](https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore) | A data store interface to be implemented and provided to the Preferences framework. |
| [OnPreferenceStartFragmentCallback](https://developer.android.com/reference/kotlin/android/preference/PreferenceFragment.OnPreferenceStartFragmentCallback) | Interface that PreferenceFragment's containing activity should implement to be able to process preference items that wish to switch to a new fragment. |
| [OnActivityDestroyListener](https://developer.android.com/reference/kotlin/android/preference/PreferenceManager.OnActivityDestroyListener) | Interface definition for a class that will be called when the container's activity is destroyed. |
| [OnActivityResultListener](https://developer.android.com/reference/kotlin/android/preference/PreferenceManager.OnActivityResultListener) | Interface definition for a class that will be called when the container's activity receives an activity result. |
| [OnActivityStopListener](https://developer.android.com/reference/kotlin/android/preference/PreferenceManager.OnActivityStopListener) | Interface definition for a class that will be called when the container's activity is stopped. |

## Classes

| [CheckBoxPreference](https://developer.android.com/reference/kotlin/android/preference/CheckBoxPreference) | A [Preference](https://developer.android.com/reference/kotlin/android/preference/Preference) that provides checkbox widget functionality. |
| [DialogPreference](https://developer.android.com/reference/kotlin/android/preference/DialogPreference) | A base class for [Preference](https://developer.android.com/reference/kotlin/android/preference/Preference) objects that are dialog-based. |
| [EditTextPreference](https://developer.android.com/reference/kotlin/android/preference/EditTextPreference) | A [Preference](https://developer.android.com/reference/kotlin/android/preference/Preference) that allows for string input. |
| [ListPreference](https://developer.android.com/reference/kotlin/android/preference/ListPreference) | A [Preference](https://developer.android.com/reference/kotlin/android/preference/Preference) that displays a list of entries as a dialog. |
| [MultiSelectListPreference](https://developer.android.com/reference/kotlin/android/preference/MultiSelectListPreference) | A [Preference](https://developer.android.com/reference/kotlin/android/preference/Preference) that displays a list of entries as a dialog. |
| [Preference](https://developer.android.com/reference/kotlin/android/preference/Preference) | Represents the basic Preference UI building block displayed by a [PreferenceActivity](https://developer.android.com/reference/kotlin/android/preference/PreferenceActivity) in the form of a [ListView](https://developer.android.com/reference/kotlin/android/widget/ListView.html#). |
| [PreferenceActivity](https://developer.android.com/reference/kotlin/android/preference/PreferenceActivity) | This is the base class for an activity to show a hierarchy of preferences to the user. |
| [PreferenceCategory](https://developer.android.com/reference/kotlin/android/preference/PreferenceCategory) | Used to group [Preference](https://developer.android.com/reference/kotlin/android/preference/Preference) objects and provide a disabled title above the group. |
| [PreferenceFragment](https://developer.android.com/reference/kotlin/android/preference/PreferenceFragment) | Shows a hierarchy of [Preference](https://developer.android.com/reference/kotlin/android/preference/Preference) objects as lists. |
| [PreferenceGroup](https://developer.android.com/reference/kotlin/android/preference/PreferenceGroup) | A container for multiple [Preference](https://developer.android.com/reference/kotlin/android/preference/Preference) objects. |
| [PreferenceManager](https://developer.android.com/reference/kotlin/android/preference/PreferenceManager) | Used to help create [Preference](https://developer.android.com/reference/kotlin/android/preference/Preference) hierarchies from activities or XML. |
| [PreferenceScreen](https://developer.android.com/reference/kotlin/android/preference/PreferenceScreen) | Represents a top-level [Preference](https://developer.android.com/reference/kotlin/android/preference/Preference) that is the root of a Preference hierarchy. |
| [RingtonePreference](https://developer.android.com/reference/kotlin/android/preference/RingtonePreference) | A [Preference](https://developer.android.com/reference/kotlin/android/preference/Preference) that allows the user to choose a ringtone from those on the device. |
| [SwitchPreference](https://developer.android.com/reference/kotlin/android/preference/SwitchPreference) | A [Preference](https://developer.android.com/reference/kotlin/android/preference/Preference) that provides a two-state toggleable option. |
| [TwoStatePreference](https://developer.android.com/reference/kotlin/android/preference/TwoStatePreference) | Common base class for preferences that have two selectable states, persist a boolean value in SharedPreferences, and may have dependent preferences that are enabled/disabled based on the current state. |
