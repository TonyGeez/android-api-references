# MultiSelectListPreference

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MultiSelectListPreference

Kotlin| [Java](../android/preference/MultiSelectListPreference.md) 
| --- | --- |

```
open class MultiSelectListPreference : DialogPreference
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [android.preference.Preference](../android/preference/Preference.md) |||
| | ↳ | [android.preference.DialogPreference](../android/preference/DialogPreference.md) ||
| | | ↳ | [android.preference.MultiSelectListPreference](../android/preference/MultiSelectListPreference.md) |
| --- | --- | --- | --- |

| **This class was deprecated in API level 29.**
|
| Use the [AndroidX](https://developer.android.com/jetpack/androidx.html) [Preference Library](../androidx/preference/_package.md) for consistent behavior across all devices. For more information on using the AndroidX Preference Library see [Settings](https://developer.android.com/guide/topics/ui/settings.html).

A [Preference](../android/preference/Preference.md) that displays a list of entries as a dialog.

This preference will store a set of strings into the SharedPreferences. This set will contain one or more values from the[setEntryValues(java.lang.CharSequence[])](https://developer.android.com/reference/kotlin/android/preference/MultiSelectListPreference#setEntryValues(kotlin.Array))array.

## Summary

| XML attributes ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [`android:entries`](../android/preference/MultiSelectListPreference.md) | The human-readable array to present as a list. |
| [`android:entryValues`](../android/preference/MultiSelectListPreference.md) | The array to find the value to save for a preference when an entry from entries is selected. |

| Inherited XML attributes ||
|---|---|
| From class [DialogPreference](../android/preference/DialogPreference.md) |----------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [android:dialogIcon](../android/preference/DialogPreference.md) | The icon for the dialog. May be a reference to another resource, in the form "`@[+][`*package* `:]`*type* `/`*name*" or a theme attribute in the form "`?[`*package* `:]`*type* `/`*name*". <br /> | | [android:dialogLayout](../android/preference/DialogPreference.md) | A layout to be used as the content View for the dialog. By default, this shouldn't be needed. If a custom DialogPreference is required, this should be set. For example, the EditTextPreference uses a layout with an EditText as this attribute. May be a reference to another resource, in the form "`@[+][`*package* `:]`*type* `/`*name*" or a theme attribute in the form "`?[`*package* `:]`*type* `/`*name*". <br /> | | [android:dialogMessage](../android/preference/DialogPreference.md) | The message in the dialog. If a dialogLayout is provided and contains a TextView with ID android:id/message, this message will be placed in there. May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character; <br /> | | [android:dialogTitle](../android/preference/DialogPreference.md) | The title in the dialog. May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character; <br /> | | [android:negativeButtonText](../android/preference/DialogPreference.md) | The negative button text for the dialog. Set to @null to hide the negative button. May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character; <br /> | | [android:positiveButtonText](../android/preference/DialogPreference.md) | The positive button text for the dialog. Set to @null to hide the positive button. May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character; <br /> | ||
| From class [Preference](../android/preference/Preference.md) |---------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [android:defaultValue](../android/preference/Preference.md) | The default value for the preference, which will be set either if persistence is off or persistence is on and the preference is not found in the persistent storage. May be a reference to another resource, in the form "`@[+][`*package* `:]`*type* `/`*name*" or a theme attribute in the form "`?[`*package* `:]`*type* `/`*name*". May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character; May be an integer value, such as "`100`". May be a boolean value, such as "`true`" or "`false`". May be a floating point value, such as "`1.2`". <br /> | | [android:dependency](../android/preference/Preference.md) | The key of another Preference that this Preference will depend on. If the other Preference is not set or is off, this Preference will be disabled. May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character; <br /> | | [android:enabled](../android/preference/Preference.md) | Whether the Preference is enabled. May be a boolean value, such as "`true`" or "`false`". <br /> | | [android:fragment](../android/preference/Preference.md) | When used inside of a modern PreferenceActivity, this declares a new PreferenceFragment to be shown when the user selects this item. May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character; <br /> | | [android:icon](../android/preference/Preference.md) | The optional icon for the preference. May be a reference to another resource, in the form "`@[+][`*package* `:]`*type* `/`*name*" or a theme attribute in the form "`?[`*package* `:]`*type* `/`*name*". <br /> | | [android:iconSpaceReserved](../android/preference/Preference.md) | Whether the space for the preference icon view will be reserved. By default, preference icon view visibility will be set to GONE when there is no icon provided, so the default value of this attribute is false. May be a boolean value, such as "`true`" or "`false`". <br /> | | [android:key](../android/preference/Preference.md) | The key to store the Preference value. May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character; <br /> | | [android:layout](../android/preference/Preference.md) | The layout for the Preference in a PreferenceActivity screen. This should rarely need to be changed, look at widgetLayout instead. May be a reference to another resource, in the form "`@[+][`*package* `:]`*type* `/`*name*" or a theme attribute in the form "`?[`*package* `:]`*type* `/`*name*". <br /> | | [android:order](../android/preference/Preference.md) | The order for the Preference (lower values are to be ordered first). If this is not specified, the default ordering will be alphabetic. May be an integer value, such as "`100`". <br /> | | [android:persistent](../android/preference/Preference.md) | Whether the Preference stores its value to the storage. May be a boolean value, such as "`true`" or "`false`". <br /> | | [android:recycleEnabled](../android/preference/Preference.md) | Whether the preference has enabled to have its view recycled when used in the list view. This is true by default. May be a boolean value, such as "`true`" or "`false`". <br /> | | [android:selectable](../android/preference/Preference.md) | Whether the Preference is selectable. May be a boolean value, such as "`true`" or "`false`". <br /> | | [android:shouldDisableView](../android/preference/Preference.md) | Whether the view of this Preference should be disabled when this Preference is disabled. May be a boolean value, such as "`true`" or "`false`". <br /> | | [android:singleLineTitle](../android/preference/Preference.md) | Whether to use single line for the preference title text. By default, preference title will be constrained to one line, so the default value of this attribute is true. May be a boolean value, such as "`true`" or "`false`". <br /> | | [android:summary](../android/preference/Preference.md) | The summary for the Preference. In API 25 and earlier, this value is read as a plain string with styling information stripped. May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character; <br /> | | [android:title](../android/preference/Preference.md) | The title for the Preference. In API 25 and earlier, this value is read as a plain string with styling information stripped. May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character; <br /> | | [android:widgetLayout](../android/preference/Preference.md) | The layout for the controllable widget portion of a Preference. This is inflated into the layout for a Preference and should be used more frequently than the layout attribute. For example, a checkbox preference would specify a custom layout (consisting of just the CheckBox) here. May be a reference to another resource, in the form "`@[+][`*package* `:]`*type* `/`*name*" or a theme attribute in the form "`?[`*package* `:]`*type* `/`*name*". <br /> | ||

| Inherited constants ||
|---|---|
| From class [Preference](../android/preference/Preference.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEFAULT_ORDER](../android/preference/Preference.md) <br /> Specify for [setOrder(int)](../android/preference/Preference.md))if a specific order is not required. <br /> | ||

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [MultiSelectListPreference](../android/preference/MultiSelectListPreference.md))`(`context:` ` [Context](../android/content/Context.md)!`)` <br /> |
| [MultiSelectListPreference](../android/preference/MultiSelectListPreference.md))`(`context:` ` [Context](../android/content/Context.md)!`, `attrs:` ` [AttributeSet](../android/util/AttributeSet.md)!`)` <br /> |
| [MultiSelectListPreference](../android/preference/MultiSelectListPreference.md))`(`context:` ` [Context](../android/content/Context.md)!`, `attrs:` ` [AttributeSet](../android/util/AttributeSet.md)!`, `defStyleAttr:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| [MultiSelectListPreference](../android/preference/MultiSelectListPreference.md))`(`context:` ` [Context](../android/content/Context.md)!`, `attrs:` ` [AttributeSet](../android/util/AttributeSet.md)!`, `defStyleAttr:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `defStyleRes:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [findIndexOfValue](../android/preference/MultiSelectListPreference.md))`(`value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the index of the given value (in the entry values array). |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!\>! | [getEntries](../android/preference/MultiSelectListPreference.md))`()` The list of entries to be shown in the list in subsequent dialogs. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!\>! | [getEntryValues](../android/preference/MultiSelectListPreference.md))`()` Returns the array of values to be saved for the preference. |
| --- | --- |
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getValues](../android/preference/MultiSelectListPreference.md))`()` Retrieves the current value of the key. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEntries](../android/preference/MultiSelectListPreference.md))`(`entriesResId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEntries](../android/preference/MultiSelectListPreference.md))`(`entries:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!>!`)` Sets the human-readable entries to be shown in the list. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEntryValues](../android/preference/MultiSelectListPreference.md))`(`entryValuesResId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEntryValues](../android/preference/MultiSelectListPreference.md))`(`entryValues:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!>!`)` The array to find the value to save for a preference when an entry from entries is selected. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setValues](../android/preference/MultiSelectListPreference.md))`(`values:` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Sets the value of the key. |
| --- | --- |

| Protected methods ||
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDialogClosed](../android/preference/MultiSelectListPreference.md))`(`positiveResult:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [onGetDefaultValue](../android/preference/MultiSelectListPreference.md))`(`a:` ` [TypedArray](../android/content/res/TypedArray.md)!`, `index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPrepareDialogBuilder](../android/preference/MultiSelectListPreference.md))`(`builder:` ` [AlertDialog.Builder](../android/app/AlertDialog.Builder.md)!`)` <br /> |
| --- | --- |
| open [Parcelable](../android/os/Parcelable.md)! | [onSaveInstanceState](../android/preference/MultiSelectListPreference.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSetInitialValue](../android/preference/MultiSelectListPreference.md))`(`restoreValue:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `defaultValue:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> |

| Inherited functions ||
|---|---|
| From class [Preference](../android/preference/Preference.md) |-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [callChangeListener](../android/preference/Preference.md))`(`newValue:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> Call this method after the user changes the preference, but before the internal state is set. This allows the client to ignore the user value. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compareTo](../android/preference/Preference.md))`(`other:` ` [Preference](../android/preference/Preference.md)!`)` <br /> Compares Preference objects based on order (if set), otherwise alphabetically on the titles. <br /> | | [Preference](../android/preference/Preference.md)! | [findPreferenceInHierarchy](../android/preference/Preference.md))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Finds a Preference in this hierarchy (the whole thing, even above/below your [PreferenceScreen](../android/preference/PreferenceScreen.md) screen break) with the given key. This only functions after we have been attached to a hierarchy. <br /> | | [Context](../android/content/Context.md)! | [getContext](../android/preference/Preference.md))`()` <br /> Returns the [android.content.Context](../android/content/Context.md) of this Preference. Each Preference in a Preference hierarchy can be from different Context (for example, if multiple activities provide preferences into a single [PreferenceActivity](../android/preference/PreferenceActivity.md)). This Context will be used to save the Preference values. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDependency](../android/preference/Preference.md))`()` <br /> Returns the key of the dependency on this Preference. <br /> | | [SharedPreferences.Editor](../android/content/SharedPreferences.Editor.md)! | [getEditor](../android/preference/Preference.md))`()` <br /> Returns an [SharedPreferences.Editor](../android/content/SharedPreferences.Editor.md) where this Preference can save its value(s). Usually it's easier to use one of the helper save methods: [persistBoolean(boolean)](../android/preference/Preference.md)), [persistFloat(float)](../android/preference/Preference.md)), [persistInt(int)](../android/preference/Preference.md)), [persistLong(long)](../android/preference/Preference.md)), [persistString(java.lang.String)](../android/preference/Preference.md)). To read values, see [getSharedPreferences()](../android/preference/Preference.md)). If [shouldCommit()](../android/preference/Preference.md))returns true, it is this Preference's responsibility to commit. In some cases, writes to this will not be committed right away and hence not show up in the SharedPreferences, this is intended behavior to improve performance. <br /> | | [Bundle](../android/os/Bundle.md)! | [getExtras](../android/preference/Preference.md))`()` <br /> Return the extras Bundle object associated with this preference, creating a new Bundle if there currently isn't one. You can use this to get and set individual extra key/value pairs. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getFragment](../android/preference/Preference.md))`()` <br /> Return the fragment class name associated with this Preference. <br /> | | [Drawable](../android/graphics/drawable/Drawable.md)! | [getIcon](../android/preference/Preference.md))`()` <br /> Returns the icon of this Preference. <br /> | | [Intent](../android/content/Intent.md)! | [getIntent](../android/preference/Preference.md))`()` <br /> Return the [Intent](../android/content/Intent.md) associated with this Preference. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getKey](../android/preference/Preference.md))`()` <br /> Gets the key for this Preference, which is also the key used for storing values into [SharedPreferences](../android/content/SharedPreferences.md) or [PreferenceDataStore](../android/preference/PreferenceDataStore.md). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLayoutResource](../android/preference/Preference.md))`()` <br /> Gets the layout resource that will be shown as the [View](../android/view/View.md) for this Preference. <br /> | | [Preference.OnPreferenceChangeListener](../android/preference/Preference.OnPreferenceChangeListener.md)! | [getOnPreferenceChangeListener](../android/preference/Preference.md))`()` <br /> Returns the callback to be invoked when this Preference is changed by the user (but before the internal state has been updated). <br /> | | [Preference.OnPreferenceClickListener](../android/preference/Preference.OnPreferenceClickListener.md)! | [getOnPreferenceClickListener](../android/preference/Preference.md))`()` <br /> Returns the callback to be invoked when this Preference is clicked. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOrder](../android/preference/Preference.md))`()` <br /> Gets the order of this Preference with respect to other Preference objects on the same level. <br /> | | [PreferenceGroup](../android/preference/PreferenceGroup.md)? | [getParent](../android/preference/Preference.md))`()` <br /> Returns the [PreferenceGroup](../android/preference/PreferenceGroup.md) which is this Preference assigned to or`null`if this preference is not assigned to any group or is a root Preference. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getPersistedBoolean](../android/preference/Preference.md))`(`defaultReturnValue:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Attempts to get a persisted boolean if this Preference is persistent. <br /> | | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getPersistedFloat](../android/preference/Preference.md))`(`defaultReturnValue:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` <br /> Attempts to get a persisted float if this Preference is persistent. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPersistedInt](../android/preference/Preference.md))`(`defaultReturnValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Attempts to get a persisted int if this Preference is persistent. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getPersistedLong](../android/preference/Preference.md))`(`defaultReturnValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Attempts to get a persisted long if this Preference is persistent. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getPersistedString](../android/preference/Preference.md))`(`defaultReturnValue:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Attempts to get a persisted String if this Preference is persistent. <br /> | | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | [getPersistedStringSet](../android/preference/Preference.md))`(`defaultReturnValue:` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` <br /> Attempts to get a persisted set of Strings if this Preference is persistent. <br /> | | [PreferenceDataStore](../android/preference/PreferenceDataStore.md)? | [getPreferenceDataStore](../android/preference/Preference.md))`()` <br /> Returns [PreferenceDataStore](../android/preference/PreferenceDataStore.md) used by this Preference. Returns`null`if [android.content.SharedPreferences](../android/content/SharedPreferences.md) is used instead. By default preferences always use [android.content.SharedPreferences](../android/content/SharedPreferences.md). To make this preference to use the [PreferenceDataStore](../android/preference/PreferenceDataStore.md) you need to assign your implementation to the Preference itself via [setPreferenceDataStore(android.preference.PreferenceDataStore)](../android/preference/Preference.md))or to its [PreferenceManager](../android/preference/PreferenceManager.md) via [PreferenceManager.setPreferenceDataStore(PreferenceDataStore)](../android/preference/PreferenceManager.md)). <br /> | | [PreferenceManager](../android/preference/PreferenceManager.md)! | [getPreferenceManager](../android/preference/Preference.md))`()` <br /> Gets the [PreferenceManager](../android/preference/PreferenceManager.md) that manages this Preference object's tree. <br /> | | [SharedPreferences](../android/content/SharedPreferences.md)! | [getSharedPreferences](../android/preference/Preference.md))`()` <br /> Returns the [SharedPreferences](../android/content/SharedPreferences.md) where this Preference can read its value(s). Usually, it's easier to use one of the helper read methods: [getPersistedBoolean(boolean)](../android/preference/Preference.md)), [getPersistedFloat(float)](../android/preference/Preference.md)), [getPersistedInt(int)](../android/preference/Preference.md)), [getPersistedLong(long)](../android/preference/Preference.md)), [getPersistedString(java.lang.String)](../android/preference/Preference.md)). To save values, see [getEditor()](../android/preference/Preference.md)). In some cases, writes to the [getEditor()](../android/preference/Preference.md))will not be committed right away and hence not show up in the returned [SharedPreferences](../android/content/SharedPreferences.md), this is intended behavior to improve performance. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getShouldDisableView](../android/preference/Preference.md))`()` <br /> Checks whether this Preference should disable its view when it's action is disabled. <br /> | | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [getSummary](../android/preference/Preference.md))`()` <br /> Returns the summary of this Preference. <br /> | | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [getTitle](../android/preference/Preference.md))`()` <br /> Returns the title of this Preference. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTitleRes](../android/preference/Preference.md))`()` <br /> Returns the title resource ID of this Preference. If the title did not come from a resource,`0`is returned. <br /> | | [View](../android/view/View.md)! | [getView](../android/preference/Preference.md))`(`convertView:` ` [View](../android/view/View.md)!`, `parent:` ` [ViewGroup](../android/view/ViewGroup.md)!`)` <br /> Gets the View that will be shown in the [PreferenceActivity](../android/preference/PreferenceActivity.md). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getWidgetLayoutResource](../android/preference/Preference.md))`()` <br /> Gets the layout resource for the controllable widget portion of this Preference. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasKey](../android/preference/Preference.md))`()` <br /> Checks whether this Preference has a valid key. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEnabled](../android/preference/Preference.md))`()` <br /> Checks whether this Preference should be enabled in the list. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isIconSpaceReserved](../android/preference/Preference.md))`()` <br /> Gets whether the space this preference icon view is reserved. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPersistent](../android/preference/Preference.md))`()` <br /> Checks whether this Preference is persistent. If it is, it stores its value(s) into the persistent [SharedPreferences](../android/content/SharedPreferences.md) storage by default or into [PreferenceDataStore](../android/preference/PreferenceDataStore.md) if assigned. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRecycleEnabled](../android/preference/Preference.md))`()` <br /> Checks whether this Preference has enabled to have its view recycled when used in the list view. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSelectable](../android/preference/Preference.md))`()` <br /> Checks whether this Preference should be selectable in the list. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSingleLineTitle](../android/preference/Preference.md))`()` <br /> Gets whether the title of this preference is constrained to a single line. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyChanged](../android/preference/Preference.md))`()` <br /> Should be called when the data of this [Preference](../android/preference/Preference.md) has changed. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyDependencyChange](../android/preference/Preference.md))`(`disableDependents:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Notifies any listening dependents of a change that affects the dependency. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyHierarchyChanged](../android/preference/Preference.md))`()` <br /> Should be called when a Preference has been added/removed from this group, or the ordering should be re-evaluated. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAttachedToActivity](../android/preference/Preference.md))`()` <br /> Called when the Preference hierarchy has been attached to the [PreferenceActivity](../android/preference/PreferenceActivity.md). This can also be called when this Preference has been attached to a group that was already attached to the [PreferenceActivity](../android/preference/PreferenceActivity.md). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAttachedToHierarchy](../android/preference/Preference.md))`(`preferenceManager:` ` [PreferenceManager](../android/preference/PreferenceManager.md)!`)` <br /> Called when this Preference has been attached to a Preference hierarchy. Make sure to call the super implementation. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onBindView](../android/preference/Preference.md))`(`view:` ` [View](../android/view/View.md)!`)` <br /> Binds the created View to the data for this Preference. This is a good place to grab references to custom Views in the layout and set properties on them. Make sure to call through to the superclass's implementation. If you override this method you*must*call through to the superclass implementation. <br /> | | [View](../android/view/View.md)! | [onCreateView](../android/preference/Preference.md))`(`parent:` ` [ViewGroup](../android/view/ViewGroup.md)!`)` <br /> Creates the View to be shown for this Preference in the [PreferenceActivity](../android/preference/PreferenceActivity.md). The default behavior is to inflate the main layout of this Preference (see [setLayoutResource(int)](../android/preference/Preference.md)). If changing this behavior, please specify a [ViewGroup](../android/view/ViewGroup.md) with ID [android.R.id#widget_frame](../android/R.id.md). Make sure to call through to the superclass's implementation. If you override this method you*must*call through to the superclass implementation. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDependencyChanged](../android/preference/Preference.md))`(`dependency:` ` [Preference](../android/preference/Preference.md)!`, `disableDependent:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Called when the dependency changes. <br /> | | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [onGetDefaultValue](../android/preference/Preference.md))`(`a:` ` [TypedArray](../android/content/res/TypedArray.md)!`, `index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Called when a Preference is being inflated and the default value attribute needs to be read. Since different Preference types have different value types, the subclass should get and return the default value which will be its value type. For example, if the value type is String, the body of the method would proxy to [TypedArray.getString(int)](../android/content/res/TypedArray.md)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onParentChanged](../android/preference/Preference.md))`(`parent:` ` [Preference](../android/preference/Preference.md)!`, `disableChild:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Called when the implicit parent dependency changes. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPrepareForRemoval](../android/preference/Preference.md))`()` <br /> Called when this Preference is being removed from the hierarchy. You should remove any references to this Preference that you know about. Make sure to call through to the superclass implementation. If you override this method you*must*call through to the superclass implementation. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSetInitialValue](../android/preference/Preference.md))`(`restorePersistedValue:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `defaultValue:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> Implement this to set the initial value of the Preference. If restorePersistedValue is true, you should restore the Preference value from the [android.content.SharedPreferences](../android/content/SharedPreferences.md). If restorePersistedValue is false, you should set the Preference value to defaultValue that is given (and possibly store to SharedPreferences if [shouldPersist()](../android/preference/Preference.md))is true). In case of using [PreferenceDataStore](../android/preference/PreferenceDataStore.md), the restorePersistedValue is always`true`. But the default value (if provided) is set. This may not always be called. One example is if it should not persist but there is no default value given. <br /> | | [Bundle](../android/os/Bundle.md)! | [peekExtras](../android/preference/Preference.md))`()` <br /> Return the extras Bundle object associated with this preference, returning`null`if there is not currently one. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [persistBoolean](../android/preference/Preference.md))`(`value:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Attempts to persist a boolean if this Preference is persistent. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [persistFloat](../android/preference/Preference.md))`(`value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` <br /> Attempts to persist a long if this Preference is persistent. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [persistInt](../android/preference/Preference.md))`(`value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Attempts to persist an int if this Preference is persistent. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [persistLong](../android/preference/Preference.md))`(`value:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Attempts to persist a long if this Preference is persistent. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [persistString](../android/preference/Preference.md))`(`value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Attempts to persist a String if this Preference is persistent. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [persistStringSet](../android/preference/Preference.md))`(`values:` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` <br /> Attempts to persist a set of Strings if this Preference is persistent. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [restoreHierarchyState](../android/preference/Preference.md))`(`container:` ` [Bundle](../android/os/Bundle.md)!`)` <br /> Restore this Preference hierarchy's previously saved state from the given container. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [saveHierarchyState](../android/preference/Preference.md))`(`container:` ` [Bundle](../android/os/Bundle.md)!`)` <br /> Store this Preference hierarchy's frozen state into the given container. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDefaultValue](../android/preference/Preference.md))`(`defaultValue:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> Sets the default value for this Preference, which will be set either if persistence is off or persistence is on and the preference is not found in the persistent storage. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDependency](../android/preference/Preference.md))`(`dependencyKey:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Sets the key of a Preference that this Preference will depend on. If that Preference is not set or is off, this Preference will be disabled. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEnabled](../android/preference/Preference.md))`(`enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Sets whether this Preference is enabled. If disabled, it will not handle clicks. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFragment](../android/preference/Preference.md))`(`fragment:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Sets the class name of a fragment to be shown when this Preference is clicked. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setIcon](../android/preference/Preference.md))`(`icon:` ` [Drawable](../android/graphics/drawable/Drawable.md)!`)` <br /> Sets the icon for this Preference with a Drawable. This icon will be placed into the ID [android.R.id#icon](../android/R.id.md) within the View created by [onCreateView(android.view.ViewGroup)](../android/preference/Preference.md)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setIcon](../android/preference/Preference.md))`(`iconResId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the icon for this Preference with a resource ID. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setIconSpaceReserved](../android/preference/Preference.md))`(`iconSpaceReserved:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Sets whether to reserve the space of this Preference icon view when no icon is provided. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setIntent](../android/preference/Preference.md))`(`intent:` ` [Intent](../android/content/Intent.md)!`)` <br /> Sets an [Intent](../android/content/Intent.md) to be used for [Context.startActivity(Intent)](../android/content/Context.md))when this Preference is clicked. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setKey](../android/preference/Preference.md))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Sets the key for this Preference, which is used as a key to the [SharedPreferences](../android/content/SharedPreferences.md) or [PreferenceDataStore](../android/preference/PreferenceDataStore.md). This should be unique for the package. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLayoutResource](../android/preference/Preference.md))`(`layoutResId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the layout resource that is inflated as the [View](../android/view/View.md) to be shown for this Preference. In most cases, the default layout is sufficient for custom Preference objects and only the widget layout needs to be changed. This layout should contain a [ViewGroup](../android/view/ViewGroup.md) with ID [android.R.id#widget_frame](../android/R.id.md) to be the parent of the specific widget for this Preference. It should similarly contain [android.R.id#title](../android/R.id.md) and [android.R.id#summary](../android/R.id.md). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnPreferenceChangeListener](../android/preference/Preference.md))`(`onPreferenceChangeListener:` ` [Preference.OnPreferenceChangeListener](../android/preference/Preference.OnPreferenceChangeListener.md)!`)` <br /> Sets the callback to be invoked when this Preference is changed by the user (but before the internal state has been updated). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnPreferenceClickListener](../android/preference/Preference.md))`(`onPreferenceClickListener:` ` [Preference.OnPreferenceClickListener](../android/preference/Preference.OnPreferenceClickListener.md)!`)` <br /> Sets the callback to be invoked when this Preference is clicked. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOrder](../android/preference/Preference.md))`(`order:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the order of this Preference with respect to other Preference objects on the same level. If this is not specified, the default behavior is to sort alphabetically. The [PreferenceGroup.setOrderingAsAdded(boolean)](../android/preference/PreferenceGroup.md))can be used to order Preference objects based on the order they appear in the XML. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPersistent](../android/preference/Preference.md))`(`persistent:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Sets whether this Preference is persistent. When persistent, it stores its value(s) into the persistent [SharedPreferences](../android/content/SharedPreferences.md) storage by default or into [PreferenceDataStore](../android/preference/PreferenceDataStore.md) if assigned. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPreferenceDataStore](../android/preference/Preference.md))`(`dataStore:` ` [PreferenceDataStore](../android/preference/PreferenceDataStore.md)!`)` <br /> Sets a [PreferenceDataStore](../android/preference/PreferenceDataStore.md) to be used by this Preference instead of using [android.content.SharedPreferences](../android/content/SharedPreferences.md). The data store will remain assigned even if the Preference is moved around the preference hierarchy. It will also override a data store propagated from the [PreferenceManager](../android/preference/PreferenceManager.md) that owns this Preference. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRecycleEnabled](../android/preference/Preference.md))`(`enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Sets whether this Preference has enabled to have its view recycled when used in the list view. By default the recycling is enabled. The value can be changed only before this preference is added to the preference hierarchy. If view recycling is not allowed then each time the list view populates this preference the [getView(android.view.View,android.view.ViewGroup)](../android/preference/Preference.md))method receives a`null`convert view and needs to recreate the view. Otherwise view gets recycled and only [onBindView(android.view.View)](../android/preference/Preference.md))gets called. If you override this method you*must*call through to the superclass implementation. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSelectable](../android/preference/Preference.md))`(`selectable:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Sets whether this Preference is selectable. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setShouldDisableView](../android/preference/Preference.md))`(`shouldDisableView:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Sets whether this Preference should disable its view when it gets disabled. For example, set this and [setEnabled(boolean)](../android/preference/Preference.md))to false for preferences that are only displaying information and 1) should not be clickable 2) should not have the view set to the disabled state. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSingleLineTitle](../android/preference/Preference.md))`(`singleLineTitle:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Sets whether to constrain the title of this Preference to a single line instead of letting it wrap onto multiple lines. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSummary](../android/preference/Preference.md))`(`summaryResId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the summary for this Preference with a resource ID. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSummary](../android/preference/Preference.md))`(`summary:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` <br /> Sets the summary for this Preference with a CharSequence. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTitle](../android/preference/Preference.md))`(`titleResId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the title for this Preference with a resource ID. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTitle](../android/preference/Preference.md))`(`title:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` <br /> Sets the title for this Preference with a CharSequence. This title will be placed into the ID [android.R.id#title](../android/R.id.md) within the View created by [onCreateView(android.view.ViewGroup)](../android/preference/Preference.md)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setWidgetLayoutResource](../android/preference/Preference.md))`(`widgetLayoutResId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the layout for the controllable widget portion of this Preference. This is inflated into the main layout. For example, a [CheckBoxPreference](../android/preference/CheckBoxPreference.md) would specify a custom layout (consisting of just the CheckBox) here, instead of creating its own main layout. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [shouldCommit](../android/preference/Preference.md))`()` <br /> Returns whether the [Preference](../android/preference/Preference.md) should commit its saved value(s) in [getEditor()](../android/preference/Preference.md)). This may return false in situations where batch committing is being done (by the manager) to improve performance. If this preference is using [PreferenceDataStore](../android/preference/PreferenceDataStore.md) this value is irrelevant. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [shouldDisableDependents](../android/preference/Preference.md))`()` <br /> Checks whether this preference's dependents should currently be disabled. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [shouldPersist](../android/preference/Preference.md))`()` <br /> Checks whether, at the given time this method is called, this Preference should store/restore its value(s) into the [SharedPreferences](../android/content/SharedPreferences.md) or into [PreferenceDataStore](../android/preference/PreferenceDataStore.md) if assigned. This, at minimum, checks whether this Preference is persistent and it currently has a key. Before you save/restore from the storage, check this first. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/preference/Preference.md))`()` <br /> | ||
| From class [DialogPreference](../android/preference/DialogPreference.md) |------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Dialog](../android/app/Dialog.md)! | [getDialog](../android/preference/DialogPreference.md))`()` <br /> Gets the dialog that is shown by this preference. <br /> | | [Drawable](../android/graphics/drawable/Drawable.md)! | [getDialogIcon](../android/preference/DialogPreference.md))`()` <br /> Returns the icon to be shown on subsequent dialogs. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDialogLayoutResource](../android/preference/DialogPreference.md))`()` <br /> Returns the layout resource that is used as the content View for subsequent dialogs. <br /> | | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [getDialogMessage](../android/preference/DialogPreference.md))`()` <br /> Returns the message to be shown on subsequent dialogs. <br /> | | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [getDialogTitle](../android/preference/DialogPreference.md))`()` <br /> Returns the title to be shown on subsequent dialogs. <br /> | | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [getNegativeButtonText](../android/preference/DialogPreference.md))`()` <br /> Returns the text of the negative button to be shown on subsequent dialogs. <br /> | | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [getPositiveButtonText](../android/preference/DialogPreference.md))`()` <br /> Returns the text of the positive button to be shown on subsequent dialogs. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onActivityDestroy](../android/preference/DialogPreference.md))`()` <br /> See Activity's onDestroy. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onBindDialogView](../android/preference/DialogPreference.md))`(`view:` ` [View](../android/view/View.md)!`)` <br /> Binds views in the content View of the dialog to data. Make sure to call through to the superclass implementation. If you override this method you*must*call through to the superclass implementation. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onClick](../android/preference/DialogPreference.md))`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onClick](../android/preference/DialogPreference.md))`(`dialog:` ` [DialogInterface](../android/content/DialogInterface.md)!`, `which:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [View](../android/view/View.md)! | [onCreateDialogView](../android/preference/DialogPreference.md))`()` <br /> Creates the content view for the dialog (if a custom content view is required). By default, it inflates the dialog layout resource if it is set. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDismiss](../android/preference/DialogPreference.md))`(`dialog:` ` [DialogInterface](../android/content/DialogInterface.md)!`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onRestoreInstanceState](../android/preference/DialogPreference.md))`(`state:` ` [Parcelable](../android/os/Parcelable.md)!`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDialogIcon](../android/preference/DialogPreference.md))`(`dialogIcon:` ` [Drawable](../android/graphics/drawable/Drawable.md)!`)` <br /> Sets the icon of the dialog. This will be shown on subsequent dialogs. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDialogIcon](../android/preference/DialogPreference.md))`(`dialogIconRes:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the icon (resource ID) of the dialog. This will be shown on subsequent dialogs. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDialogLayoutResource](../android/preference/DialogPreference.md))`(`dialogLayoutResId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the layout resource that is inflated as the [View](../android/view/View.md) to be shown as the content View of subsequent dialogs. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDialogMessage](../android/preference/DialogPreference.md))`(`dialogMessageResId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDialogMessage](../android/preference/DialogPreference.md))`(`dialogMessage:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` <br /> Sets the message of the dialog. This will be shown on subsequent dialogs. This message forms the content View of the dialog and conflicts with list-based dialogs, for example. If setting a custom View on a dialog via [setDialogLayoutResource(int)](../android/preference/DialogPreference.md)), include a text View with ID [android.R.id#message](../android/R.id.md) and it will be populated with this message. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDialogTitle](../android/preference/DialogPreference.md))`(`dialogTitleResId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDialogTitle](../android/preference/DialogPreference.md))`(`dialogTitle:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` <br /> Sets the title of the dialog. This will be shown on subsequent dialogs. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNegativeButtonText](../android/preference/DialogPreference.md))`(`negativeButtonTextResId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNegativeButtonText](../android/preference/DialogPreference.md))`(`negativeButtonText:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` <br /> Sets the text of the negative button of the dialog. This will be shown on subsequent dialogs. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPositiveButtonText](../android/preference/DialogPreference.md))`(`positiveButtonTextResId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPositiveButtonText](../android/preference/DialogPreference.md))`(`positiveButtonText:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` <br /> Sets the text of the positive button of the dialog. This will be shown on subsequent dialogs. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [showDialog](../android/preference/DialogPreference.md))`(`state:` ` [Bundle](../android/os/Bundle.md)!`)` <br /> Shows the dialog associated with this Preference. This is normally initiated automatically on clicking on the preference. Call this method if you need to show the dialog on some other event. <br /> | ||

## XML attributes

### android:entries

```
android:entries
```
The human-readable array to present as a list. Each entry must have a corresponding index in entryValues.

May be a reference to another resource, in the form "`@[+][`*package* `:]`*type* `/`*name*" or a theme attribute in the form "`?[`*package* `:]`*type* `/`*name*". 

### android:entryValues

```
android:entryValues
```
The array to find the value to save for a preference when an entry from entries is selected. If a user clicks the second item in entries, the second item in this array will be saved to the preference.

May be a reference to another resource, in the form "`@[+][`*package* `:]`*type* `/`*name*" or a theme attribute in the form "`?[`*package* `:]`*type* `/`*name*".

## Public constructors

### MultiSelectListPreference

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
MultiSelectListPreference(context: Context!)
```  

### MultiSelectListPreference

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
MultiSelectListPreference(
    context: Context!, 
    attrs: AttributeSet!)
```  

### MultiSelectListPreference

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
MultiSelectListPreference(
    context: Context!, 
    attrs: AttributeSet!, 
    defStyleAttr: Int)
```  

### MultiSelectListPreference

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
MultiSelectListPreference(
    context: Context!, 
    attrs: AttributeSet!, 
    defStyleAttr: Int, 
    defStyleRes: Int)
```

## Public methods

### findIndexOfValue

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun findIndexOfValue(value: String!): Int
```

**Deprecated:** *Deprecated in Java.*

Returns the index of the given value (in the entry values array).

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------|
| `value` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The value whose index should be returned. |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The index of the value, or -1 if not found. |

### getEntries

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEntries(): Array<CharSequence!>!
```

**Deprecated:** *Deprecated in Java.*

The list of entries to be shown in the list in subsequent dialogs.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!>! | The list as an array. |

### getEntryValues

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEntryValues(): Array<CharSequence!>!
```

**Deprecated:** *Deprecated in Java.*

Returns the array of values to be saved for the preference.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!>! | The array of values. |

### getValues

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getValues(): MutableSet<String!>!
```

**Deprecated:** *Deprecated in Java.*

Retrieves the current value of the key. 

### setEntries

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setEntries(entriesResId: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|----------------|-------------------------------------------------------------------------------------------------------------|
| `entriesResId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The entries array as a resource. |

**See Also**

- [#setEntries(CharSequence[])](https://developer.android.com/reference/kotlin/android/preference/MultiSelectListPreference#setEntries(kotlin.Array)) 

### setEntries

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setEntries(entries: Array<CharSequence!>!): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the human-readable entries to be shown in the list. This will be shown in subsequent dialogs.

Each entry must have a corresponding index in[setEntryValues(java.lang.CharSequence[])](https://developer.android.com/reference/kotlin/android/preference/MultiSelectListPreference#setEntryValues(kotlin.Array)).

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `entries` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!\>!:The entries. |

**See Also**

- [#setEntryValues(CharSequence[])](https://developer.android.com/reference/kotlin/android/preference/MultiSelectListPreference#setEntryValues(kotlin.Array)) 

### setEntryValues

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setEntryValues(entryValuesResId: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|--------------------|------------------------------------------------------------------------------------------------------------------|
| `entryValuesResId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The entry values array as a resource. |

**See Also**

- [#setEntryValues(CharSequence[])](https://developer.android.com/reference/kotlin/android/preference/MultiSelectListPreference#setEntryValues(kotlin.Array)) 

### setEntryValues

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setEntryValues(entryValues: Array<CharSequence!>!): Unit
```

**Deprecated:** *Deprecated in Java.*

The array to find the value to save for a preference when an entry from entries is selected. If a user clicks on the second item in entries, the second item in this array will be saved to the preference.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `entryValues` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!\>!:The array to be used as values to save for the preference. |

### setValues

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setValues(values: MutableSet<String!>!): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the value of the key. This should contain entries in [getEntryValues()](../android/preference/MultiSelectListPreference.md)).

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `values` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:The values to set for the key. |

## Protected methods

### onDialogClosed

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onDialogClosed(positiveResult: Boolean): Unit
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `positiveResult` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Whether the positive button was clicked (true), or the negative button was clicked or the dialog was canceled (false). |

### onGetDefaultValue

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onGetDefaultValue(
    a: TypedArray!, 
    index: Int
): Any!
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------|
| `a` | [TypedArray](../android/content/res/TypedArray.md)!:The set of attributes. |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index of the default value attribute. |

| Return ||
|-----------------------------------------------------------------------------|--------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | The default value of this preference type. |

### onPrepareDialogBuilder

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onPrepareDialogBuilder(builder: AlertDialog.Builder!): Unit
```

**Deprecated:** *Deprecated in Java.* 

### onSaveInstanceState

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onSaveInstanceState(): Parcelable!
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Parcelable](../android/os/Parcelable.md)! | A Parcelable object containing the current dynamic state of this Preference, or`null`if there is nothing interesting to save. The default implementation returns`null`. |

### onSetInitialValue

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onSetInitialValue(
    restoreValue: Boolean, 
    defaultValue: Any!
): Unit
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `restorePersistedValue` | True to restore the persisted value; false to use the given defaultValue. |
| `defaultValue` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:The default value for this Preference. Only use this if restorePersistedValue is false. |
