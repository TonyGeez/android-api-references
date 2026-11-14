# android.preference

# android.preference

Kotlin| [Java](../android/preference/_package.md)
| --- | --- |

## Interfaces

| [OnPreferenceChangeListener](../android/preference/Preference.OnPreferenceChangeListener.md) | Interface definition for a callback to be invoked when the value of this [Preference](../android/preference/Preference.md) has been changed by the user and is about to be set and/or persisted. |
| --- | --- |
| [OnPreferenceClickListener](../android/preference/Preference.OnPreferenceClickListener.md) | Interface definition for a callback to be invoked when a [Preference](../android/preference/Preference.md) is clicked. |
| [PreferenceDataStore](../android/preference/PreferenceDataStore.md) | A data store interface to be implemented and provided to the Preferences framework. |
| [OnPreferenceStartFragmentCallback](../android/preference/PreferenceFragment.OnPreferenceStartFragmentCallback.md) | Interface that PreferenceFragment's containing activity should implement to be able to process preference items that wish to switch to a new fragment. |
| --- | --- |
| [OnActivityDestroyListener](../android/preference/PreferenceManager.OnActivityDestroyListener.md) | Interface definition for a class that will be called when the container's activity is destroyed. |
| [OnActivityResultListener](../android/preference/PreferenceManager.OnActivityResultListener.md) | Interface definition for a class that will be called when the container's activity receives an activity result. |
| [OnActivityStopListener](../android/preference/PreferenceManager.OnActivityStopListener.md) | Interface definition for a class that will be called when the container's activity is stopped. |
| --- | --- |

## Classes

| [CheckBoxPreference](../android/preference/CheckBoxPreference.md) | A [Preference](../android/preference/Preference.md) that provides checkbox widget functionality. |
| --- | --- |
| [DialogPreference](../android/preference/DialogPreference.md) | A base class for [Preference](../android/preference/Preference.md) objects that are dialog-based. |
| [EditTextPreference](../android/preference/EditTextPreference.md) | A [Preference](../android/preference/Preference.md) that allows for string input. |
| [ListPreference](../android/preference/ListPreference.md) | A [Preference](../android/preference/Preference.md) that displays a list of entries as a dialog. |
| --- | --- |
| [MultiSelectListPreference](../android/preference/MultiSelectListPreference.md) | A [Preference](../android/preference/Preference.md) that displays a list of entries as a dialog. |
| [Preference](../android/preference/Preference.md) | Represents the basic Preference UI building block displayed by a [PreferenceActivity](../android/preference/PreferenceActivity.md) in the form of a [ListView](../android/widget/ListView.md). |
| [PreferenceActivity](../android/preference/PreferenceActivity.md) | This is the base class for an activity to show a hierarchy of preferences to the user. |
| --- | --- |
| [PreferenceCategory](../android/preference/PreferenceCategory.md) | Used to group [Preference](../android/preference/Preference.md) objects and provide a disabled title above the group. |
| [PreferenceFragment](../android/preference/PreferenceFragment.md) | Shows a hierarchy of [Preference](../android/preference/Preference.md) objects as lists. |
| [PreferenceGroup](../android/preference/PreferenceGroup.md) | A container for multiple [Preference](../android/preference/Preference.md) objects. |
| --- | --- |
| [PreferenceManager](../android/preference/PreferenceManager.md) | Used to help create [Preference](../android/preference/Preference.md) hierarchies from activities or XML. |
| [PreferenceScreen](../android/preference/PreferenceScreen.md) | Represents a top-level [Preference](../android/preference/Preference.md) that is the root of a Preference hierarchy. |
| [RingtonePreference](../android/preference/RingtonePreference.md) | A [Preference](../android/preference/Preference.md) that allows the user to choose a ringtone from those on the device. |
| --- | --- |
| [SwitchPreference](../android/preference/SwitchPreference.md) | A [Preference](../android/preference/Preference.md) that provides a two-state toggleable option. |
| [TwoStatePreference](../android/preference/TwoStatePreference.md) | Common base class for preferences that have two selectable states, persist a boolean value in SharedPreferences, and may have dependent preferences that are enabled/disabled based on the current state. |
