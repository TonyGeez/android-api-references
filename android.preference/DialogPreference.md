# DialogPreference

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DialogPreference

Kotlin| [Java](DialogPreference.md) 
| --- | --- |

```
abstract class DialogPreference : Preference, DialogInterface.OnClickListener, DialogInterface.OnDismissListener, PreferenceManager.OnActivityDestroyListener
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.preference.Preference](Preference.md) ||
| | ↳ | [android.preference.DialogPreference](DialogPreference.md) |

| Known Direct Subclasses [EditTextPreference](EditTextPreference.md), [ListPreference](ListPreference.md), [MultiSelectListPreference](MultiSelectListPreference.md) |--------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------| | [EditTextPreference](EditTextPreference.md) | A [Preference](Preference.md) that allows for string input. | | [ListPreference](ListPreference.md) | A [Preference](Preference.md) that displays a list of entries as a dialog. | | [MultiSelectListPreference](MultiSelectListPreference.md) | A [Preference](Preference.md) that displays a list of entries as a dialog. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| **This class was deprecated in API level 29.**
|
| Use the [AndroidX](https://developer.android.com/jetpack/androidx.html) [Preference Library](../androidx/preference/_package.md) for consistent behavior across all devices. For more information on using the AndroidX Preference Library see [Settings](https://developer.android.com/guide/topics/ui/settings.html).

A base class for [Preference](Preference.md) objects that are dialog-based. These preferences will, when clicked, open a dialog showing the actual preference controls.

## Summary

| XML attributes ||
|------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| [`android:dialogIcon`](DialogPreference.md) | The icon for the dialog. |
| [`android:dialogLayout`](DialogPreference.md) | A layout to be used as the content View for the dialog. |
| [`android:dialogMessage`](DialogPreference.md) | The message in the dialog. |
| --- | --- |
| [`android:dialogTitle`](DialogPreference.md) | The title in the dialog. |
| [`android:negativeButtonText`](DialogPreference.md) | The negative button text for the dialog. |
| [`android:positiveButtonText`](DialogPreference.md) | The positive button text for the dialog. |
| --- | --- |

| Inherited XML attributes ||
|---|---|
| From class [Preference](Preference.md) |---------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [android:defaultValue](Preference.md) | The default value for the preference, which will be set either if persistence is off or persistence is on and the preference is not found in the persistent storage. May be a reference to another resource, in the form "`@[+][`*package* `:]`*type* `/`*name*" or a theme attribute in the form "`?[`*package* `:]`*type* `/`*name*". May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character; May be an integer value, such as "`100`". May be a boolean value, such as "`true`" or "`false`". May be a floating point value, such as "`1.2`". <br /> | | [android:dependency](Preference.md) | The key of another Preference that this Preference will depend on. If the other Preference is not set or is off, this Preference will be disabled. May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character; <br /> | | [android:enabled](Preference.md) | Whether the Preference is enabled. May be a boolean value, such as "`true`" or "`false`". <br /> | | [android:fragment](Preference.md) | When used inside of a modern PreferenceActivity, this declares a new PreferenceFragment to be shown when the user selects this item. May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character; <br /> | | [android:icon](Preference.md) | The optional icon for the preference. May be a reference to another resource, in the form "`@[+][`*package* `:]`*type* `/`*name*" or a theme attribute in the form "`?[`*package* `:]`*type* `/`*name*". <br /> | | [android:iconSpaceReserved](Preference.md) | Whether the space for the preference icon view will be reserved. By default, preference icon view visibility will be set to GONE when there is no icon provided, so the default value of this attribute is false. May be a boolean value, such as "`true`" or "`false`". <br /> | | [android:key](Preference.md) | The key to store the Preference value. May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character; <br /> | | [android:layout](Preference.md) | The layout for the Preference in a PreferenceActivity screen. This should rarely need to be changed, look at widgetLayout instead. May be a reference to another resource, in the form "`@[+][`*package* `:]`*type* `/`*name*" or a theme attribute in the form "`?[`*package* `:]`*type* `/`*name*". <br /> | | [android:order](Preference.md) | The order for the Preference (lower values are to be ordered first). If this is not specified, the default ordering will be alphabetic. May be an integer value, such as "`100`". <br /> | | [android:persistent](Preference.md) | Whether the Preference stores its value to the storage. May be a boolean value, such as "`true`" or "`false`". <br /> | | [android:recycleEnabled](Preference.md) | Whether the preference has enabled to have its view recycled when used in the list view. This is true by default. May be a boolean value, such as "`true`" or "`false`". <br /> | | [android:selectable](Preference.md) | Whether the Preference is selectable. May be a boolean value, such as "`true`" or "`false`". <br /> | | [android:shouldDisableView](Preference.md) | Whether the view of this Preference should be disabled when this Preference is disabled. May be a boolean value, such as "`true`" or "`false`". <br /> | | [android:singleLineTitle](Preference.md) | Whether to use single line for the preference title text. By default, preference title will be constrained to one line, so the default value of this attribute is true. May be a boolean value, such as "`true`" or "`false`". <br /> | | [android:summary](Preference.md) | The summary for the Preference. In API 25 and earlier, this value is read as a plain string with styling information stripped. May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character; <br /> | | [android:title](Preference.md) | The title for the Preference. In API 25 and earlier, this value is read as a plain string with styling information stripped. May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character; <br /> | | [android:widgetLayout](Preference.md) | The layout for the controllable widget portion of a Preference. This is inflated into the layout for a Preference and should be used more frequently than the layout attribute. For example, a checkbox preference would specify a custom layout (consisting of just the CheckBox) here. May be a reference to another resource, in the form "`@[+][`*package* `:]`*type* `/`*name*" or a theme attribute in the form "`?[`*package* `:]`*type* `/`*name*". <br /> | ||

| Inherited constants ||
|---|---|
| From class [Preference](Preference.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEFAULT_ORDER](Preference.md) <br /> Specify for [setOrder(int)](Preference.md))if a specific order is not required. <br /> | ||

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DialogPreference](DialogPreference.md))`(`context:` ` [Context](../android.content/Context.md)!`)` <br /> |
| [DialogPreference](DialogPreference.md))`(`context:` ` [Context](../android.content/Context.md)!`, `attrs:` ` [AttributeSet](../android.util/AttributeSet.md)!`)` <br /> |
| [DialogPreference](DialogPreference.md))`(`context:` ` [Context](../android.content/Context.md)!`, `attrs:` ` [AttributeSet](../android.util/AttributeSet.md)!`, `defStyleAttr:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| [DialogPreference](DialogPreference.md))`(`context:` ` [Context](../android.content/Context.md)!`, `attrs:` ` [AttributeSet](../android.util/AttributeSet.md)!`, `defStyleAttr:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `defStyleRes:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Dialog](../android.app/Dialog.md)! | [getDialog](DialogPreference.md))`()` Gets the dialog that is shown by this preference. |
| open [Drawable](../android.graphics.drawable/Drawable.md)! | [getDialogIcon](DialogPreference.md))`()` Returns the icon to be shown on subsequent dialogs. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDialogLayoutResource](DialogPreference.md))`()` Returns the layout resource that is used as the content View for subsequent dialogs. |
| --- | --- |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [getDialogMessage](DialogPreference.md))`()` Returns the message to be shown on subsequent dialogs. |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [getDialogTitle](DialogPreference.md))`()` Returns the title to be shown on subsequent dialogs. |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [getNegativeButtonText](DialogPreference.md))`()` Returns the text of the negative button to be shown on subsequent dialogs. |
| --- | --- |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [getPositiveButtonText](DialogPreference.md))`()` Returns the text of the positive button to be shown on subsequent dialogs. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onActivityDestroy](DialogPreference.md))`()` See Activity's onDestroy. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onClick](DialogPreference.md))`(`dialog:` ` [DialogInterface](../android.content/DialogInterface.md)!`, `which:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDismiss](DialogPreference.md))`(`dialog:` ` [DialogInterface](../android.content/DialogInterface.md)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDialogIcon](DialogPreference.md))`(`dialogIcon:` ` [Drawable](../android.graphics.drawable/Drawable.md)!`)` Sets the icon of the dialog. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDialogIcon](DialogPreference.md))`(`dialogIconRes:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the icon (resource ID) of the dialog. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDialogLayoutResource](DialogPreference.md))`(`dialogLayoutResId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the layout resource that is inflated as the [View](../android.view/View.md) to be shown as the content View of subsequent dialogs. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDialogMessage](DialogPreference.md))`(`dialogMessageResId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDialogMessage](DialogPreference.md))`(`dialogMessage:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Sets the message of the dialog. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDialogTitle](DialogPreference.md))`(`dialogTitleResId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDialogTitle](DialogPreference.md))`(`dialogTitle:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Sets the title of the dialog. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNegativeButtonText](DialogPreference.md))`(`negativeButtonTextResId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNegativeButtonText](DialogPreference.md))`(`negativeButtonText:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Sets the text of the negative button of the dialog. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPositiveButtonText](DialogPreference.md))`(`positiveButtonTextResId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPositiveButtonText](DialogPreference.md))`(`positiveButtonText:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Sets the text of the positive button of the dialog. |
| --- | --- |

| Protected methods ||
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onBindDialogView](DialogPreference.md))`(`view:` ` [View](../android.view/View.md)!`)` Binds views in the content View of the dialog to data. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onClick](DialogPreference.md))`()` <br /> |
| open [View](../android.view/View.md)! | [onCreateDialogView](DialogPreference.md))`()` Creates the content view for the dialog (if a custom content view is required). |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDialogClosed](DialogPreference.md))`(`positiveResult:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Called when the dialog is dismissed and should be used to save data to the [SharedPreferences](../android.content/SharedPreferences.md). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPrepareDialogBuilder](DialogPreference.md))`(`builder:` ` [AlertDialog.Builder](../android/app/AlertDialog.Builder.md)!`)` Prepares the dialog builder to be shown when the preference is clicked. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onRestoreInstanceState](DialogPreference.md))`(`state:` ` [Parcelable](../android.os/Parcelable.md)!`)` <br /> |
| --- | --- |
| open [Parcelable](../android.os/Parcelable.md)! | [onSaveInstanceState](DialogPreference.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [showDialog](DialogPreference.md))`(`state:` ` [Bundle](../android.os/Bundle.md)!`)` Shows the dialog associated with this Preference. |

| Inherited functions ||
|---|---|
| From class [Preference](Preference.md) |-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [callChangeListener](Preference.md))`(`newValue:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> Call this method after the user changes the preference, but before the internal state is set. This allows the client to ignore the user value. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compareTo](Preference.md))`(`other:` ` [Preference](Preference.md)!`)` <br /> Compares Preference objects based on order (if set), otherwise alphabetically on the titles. <br /> | | [Preference](Preference.md)! | [findPreferenceInHierarchy](Preference.md))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Finds a Preference in this hierarchy (the whole thing, even above/below your [PreferenceScreen](PreferenceScreen.md) screen break) with the given key. This only functions after we have been attached to a hierarchy. <br /> | | [Context](../android.content/Context.md)! | [getContext](Preference.md))`()` <br /> Returns the [android.content.Context](../android.content/Context.md) of this Preference. Each Preference in a Preference hierarchy can be from different Context (for example, if multiple activities provide preferences into a single [PreferenceActivity](PreferenceActivity.md)). This Context will be used to save the Preference values. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDependency](Preference.md))`()` <br /> Returns the key of the dependency on this Preference. <br /> | | [SharedPreferences.Editor](../android/content/SharedPreferences.Editor.md)! | [getEditor](Preference.md))`()` <br /> Returns an [SharedPreferences.Editor](../android/content/SharedPreferences.Editor.md) where this Preference can save its value(s). Usually it's easier to use one of the helper save methods: [persistBoolean(boolean)](Preference.md)), [persistFloat(float)](Preference.md)), [persistInt(int)](Preference.md)), [persistLong(long)](Preference.md)), [persistString(java.lang.String)](Preference.md)). To read values, see [getSharedPreferences()](Preference.md)). If [shouldCommit()](Preference.md))returns true, it is this Preference's responsibility to commit. In some cases, writes to this will not be committed right away and hence not show up in the SharedPreferences, this is intended behavior to improve performance. <br /> | | [Bundle](../android.os/Bundle.md)! | [getExtras](Preference.md))`()` <br /> Return the extras Bundle object associated with this preference, creating a new Bundle if there currently isn't one. You can use this to get and set individual extra key/value pairs. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getFragment](Preference.md))`()` <br /> Return the fragment class name associated with this Preference. <br /> | | [Drawable](../android.graphics.drawable/Drawable.md)! | [getIcon](Preference.md))`()` <br /> Returns the icon of this Preference. <br /> | | [Intent](../android.content/Intent.md)! | [getIntent](Preference.md))`()` <br /> Return the [Intent](../android.content/Intent.md) associated with this Preference. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getKey](Preference.md))`()` <br /> Gets the key for this Preference, which is also the key used for storing values into [SharedPreferences](../android.content/SharedPreferences.md) or [PreferenceDataStore](PreferenceDataStore.md). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLayoutResource](Preference.md))`()` <br /> Gets the layout resource that will be shown as the [View](../android.view/View.md) for this Preference. <br /> | | [Preference.OnPreferenceChangeListener](../android/preference/Preference.OnPreferenceChangeListener.md)! | [getOnPreferenceChangeListener](Preference.md))`()` <br /> Returns the callback to be invoked when this Preference is changed by the user (but before the internal state has been updated). <br /> | | [Preference.OnPreferenceClickListener](../android/preference/Preference.OnPreferenceClickListener.md)! | [getOnPreferenceClickListener](Preference.md))`()` <br /> Returns the callback to be invoked when this Preference is clicked. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOrder](Preference.md))`()` <br /> Gets the order of this Preference with respect to other Preference objects on the same level. <br /> | | [PreferenceGroup](PreferenceGroup.md)? | [getParent](Preference.md))`()` <br /> Returns the [PreferenceGroup](PreferenceGroup.md) which is this Preference assigned to or`null`if this preference is not assigned to any group or is a root Preference. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getPersistedBoolean](Preference.md))`(`defaultReturnValue:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Attempts to get a persisted boolean if this Preference is persistent. <br /> | | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getPersistedFloat](Preference.md))`(`defaultReturnValue:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` <br /> Attempts to get a persisted float if this Preference is persistent. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPersistedInt](Preference.md))`(`defaultReturnValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Attempts to get a persisted int if this Preference is persistent. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getPersistedLong](Preference.md))`(`defaultReturnValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Attempts to get a persisted long if this Preference is persistent. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getPersistedString](Preference.md))`(`defaultReturnValue:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Attempts to get a persisted String if this Preference is persistent. <br /> | | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | [getPersistedStringSet](Preference.md))`(`defaultReturnValue:` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` <br /> Attempts to get a persisted set of Strings if this Preference is persistent. <br /> | | [PreferenceDataStore](PreferenceDataStore.md)? | [getPreferenceDataStore](Preference.md))`()` <br /> Returns [PreferenceDataStore](PreferenceDataStore.md) used by this Preference. Returns`null`if [android.content.SharedPreferences](../android.content/SharedPreferences.md) is used instead. By default preferences always use [android.content.SharedPreferences](../android.content/SharedPreferences.md). To make this preference to use the [PreferenceDataStore](PreferenceDataStore.md) you need to assign your implementation to the Preference itself via [setPreferenceDataStore(android.preference.PreferenceDataStore)](Preference.md))or to its [PreferenceManager](PreferenceManager.md) via [PreferenceManager.setPreferenceDataStore(PreferenceDataStore)](PreferenceManager.md)). <br /> | | [PreferenceManager](PreferenceManager.md)! | [getPreferenceManager](Preference.md))`()` <br /> Gets the [PreferenceManager](PreferenceManager.md) that manages this Preference object's tree. <br /> | | [SharedPreferences](../android.content/SharedPreferences.md)! | [getSharedPreferences](Preference.md))`()` <br /> Returns the [SharedPreferences](../android.content/SharedPreferences.md) where this Preference can read its value(s). Usually, it's easier to use one of the helper read methods: [getPersistedBoolean(boolean)](Preference.md)), [getPersistedFloat(float)](Preference.md)), [getPersistedInt(int)](Preference.md)), [getPersistedLong(long)](Preference.md)), [getPersistedString(java.lang.String)](Preference.md)). To save values, see [getEditor()](Preference.md)). In some cases, writes to the [getEditor()](Preference.md))will not be committed right away and hence not show up in the returned [SharedPreferences](../android.content/SharedPreferences.md), this is intended behavior to improve performance. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getShouldDisableView](Preference.md))`()` <br /> Checks whether this Preference should disable its view when it's action is disabled. <br /> | | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [getSummary](Preference.md))`()` <br /> Returns the summary of this Preference. <br /> | | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [getTitle](Preference.md))`()` <br /> Returns the title of this Preference. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTitleRes](Preference.md))`()` <br /> Returns the title resource ID of this Preference. If the title did not come from a resource,`0`is returned. <br /> | | [View](../android.view/View.md)! | [getView](Preference.md))`(`convertView:` ` [View](../android.view/View.md)!`, `parent:` ` [ViewGroup](../android.view/ViewGroup.md)!`)` <br /> Gets the View that will be shown in the [PreferenceActivity](PreferenceActivity.md). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getWidgetLayoutResource](Preference.md))`()` <br /> Gets the layout resource for the controllable widget portion of this Preference. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasKey](Preference.md))`()` <br /> Checks whether this Preference has a valid key. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEnabled](Preference.md))`()` <br /> Checks whether this Preference should be enabled in the list. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isIconSpaceReserved](Preference.md))`()` <br /> Gets whether the space this preference icon view is reserved. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPersistent](Preference.md))`()` <br /> Checks whether this Preference is persistent. If it is, it stores its value(s) into the persistent [SharedPreferences](../android.content/SharedPreferences.md) storage by default or into [PreferenceDataStore](PreferenceDataStore.md) if assigned. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRecycleEnabled](Preference.md))`()` <br /> Checks whether this Preference has enabled to have its view recycled when used in the list view. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSelectable](Preference.md))`()` <br /> Checks whether this Preference should be selectable in the list. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSingleLineTitle](Preference.md))`()` <br /> Gets whether the title of this preference is constrained to a single line. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyChanged](Preference.md))`()` <br /> Should be called when the data of this [Preference](Preference.md) has changed. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyDependencyChange](Preference.md))`(`disableDependents:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Notifies any listening dependents of a change that affects the dependency. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyHierarchyChanged](Preference.md))`()` <br /> Should be called when a Preference has been added/removed from this group, or the ordering should be re-evaluated. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAttachedToActivity](Preference.md))`()` <br /> Called when the Preference hierarchy has been attached to the [PreferenceActivity](PreferenceActivity.md). This can also be called when this Preference has been attached to a group that was already attached to the [PreferenceActivity](PreferenceActivity.md). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAttachedToHierarchy](Preference.md))`(`preferenceManager:` ` [PreferenceManager](PreferenceManager.md)!`)` <br /> Called when this Preference has been attached to a Preference hierarchy. Make sure to call the super implementation. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onBindView](Preference.md))`(`view:` ` [View](../android.view/View.md)!`)` <br /> Binds the created View to the data for this Preference. This is a good place to grab references to custom Views in the layout and set properties on them. Make sure to call through to the superclass's implementation. If you override this method you*must*call through to the superclass implementation. <br /> | | [View](../android.view/View.md)! | [onCreateView](Preference.md))`(`parent:` ` [ViewGroup](../android.view/ViewGroup.md)!`)` <br /> Creates the View to be shown for this Preference in the [PreferenceActivity](PreferenceActivity.md). The default behavior is to inflate the main layout of this Preference (see [setLayoutResource(int)](Preference.md)). If changing this behavior, please specify a [ViewGroup](../android.view/ViewGroup.md) with ID [android.R.id#widget_frame](../android/R.id.md). Make sure to call through to the superclass's implementation. If you override this method you*must*call through to the superclass implementation. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDependencyChanged](Preference.md))`(`dependency:` ` [Preference](Preference.md)!`, `disableDependent:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Called when the dependency changes. <br /> | | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [onGetDefaultValue](Preference.md))`(`a:` ` [TypedArray](../android.content.res/TypedArray.md)!`, `index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Called when a Preference is being inflated and the default value attribute needs to be read. Since different Preference types have different value types, the subclass should get and return the default value which will be its value type. For example, if the value type is String, the body of the method would proxy to [TypedArray.getString(int)](../android.content.res/TypedArray.md)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onParentChanged](Preference.md))`(`parent:` ` [Preference](Preference.md)!`, `disableChild:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Called when the implicit parent dependency changes. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPrepareForRemoval](Preference.md))`()` <br /> Called when this Preference is being removed from the hierarchy. You should remove any references to this Preference that you know about. Make sure to call through to the superclass implementation. If you override this method you*must*call through to the superclass implementation. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSetInitialValue](Preference.md))`(`restorePersistedValue:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `defaultValue:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> Implement this to set the initial value of the Preference. If restorePersistedValue is true, you should restore the Preference value from the [android.content.SharedPreferences](../android.content/SharedPreferences.md). If restorePersistedValue is false, you should set the Preference value to defaultValue that is given (and possibly store to SharedPreferences if [shouldPersist()](Preference.md))is true). In case of using [PreferenceDataStore](PreferenceDataStore.md), the restorePersistedValue is always`true`. But the default value (if provided) is set. This may not always be called. One example is if it should not persist but there is no default value given. <br /> | | [Bundle](../android.os/Bundle.md)! | [peekExtras](Preference.md))`()` <br /> Return the extras Bundle object associated with this preference, returning`null`if there is not currently one. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [persistBoolean](Preference.md))`(`value:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Attempts to persist a boolean if this Preference is persistent. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [persistFloat](Preference.md))`(`value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` <br /> Attempts to persist a long if this Preference is persistent. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [persistInt](Preference.md))`(`value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Attempts to persist an int if this Preference is persistent. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [persistLong](Preference.md))`(`value:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Attempts to persist a long if this Preference is persistent. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [persistString](Preference.md))`(`value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Attempts to persist a String if this Preference is persistent. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [persistStringSet](Preference.md))`(`values:` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` <br /> Attempts to persist a set of Strings if this Preference is persistent. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [restoreHierarchyState](Preference.md))`(`container:` ` [Bundle](../android.os/Bundle.md)!`)` <br /> Restore this Preference hierarchy's previously saved state from the given container. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [saveHierarchyState](Preference.md))`(`container:` ` [Bundle](../android.os/Bundle.md)!`)` <br /> Store this Preference hierarchy's frozen state into the given container. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDefaultValue](Preference.md))`(`defaultValue:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> Sets the default value for this Preference, which will be set either if persistence is off or persistence is on and the preference is not found in the persistent storage. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDependency](Preference.md))`(`dependencyKey:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Sets the key of a Preference that this Preference will depend on. If that Preference is not set or is off, this Preference will be disabled. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEnabled](Preference.md))`(`enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Sets whether this Preference is enabled. If disabled, it will not handle clicks. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFragment](Preference.md))`(`fragment:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Sets the class name of a fragment to be shown when this Preference is clicked. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setIcon](Preference.md))`(`icon:` ` [Drawable](../android.graphics.drawable/Drawable.md)!`)` <br /> Sets the icon for this Preference with a Drawable. This icon will be placed into the ID [android.R.id#icon](../android/R.id.md) within the View created by [onCreateView(android.view.ViewGroup)](Preference.md)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setIcon](Preference.md))`(`iconResId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the icon for this Preference with a resource ID. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setIconSpaceReserved](Preference.md))`(`iconSpaceReserved:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Sets whether to reserve the space of this Preference icon view when no icon is provided. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setIntent](Preference.md))`(`intent:` ` [Intent](../android.content/Intent.md)!`)` <br /> Sets an [Intent](../android.content/Intent.md) to be used for [Context.startActivity(Intent)](../android.content/Context.md))when this Preference is clicked. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setKey](Preference.md))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Sets the key for this Preference, which is used as a key to the [SharedPreferences](../android.content/SharedPreferences.md) or [PreferenceDataStore](PreferenceDataStore.md). This should be unique for the package. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLayoutResource](Preference.md))`(`layoutResId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the layout resource that is inflated as the [View](../android.view/View.md) to be shown for this Preference. In most cases, the default layout is sufficient for custom Preference objects and only the widget layout needs to be changed. This layout should contain a [ViewGroup](../android.view/ViewGroup.md) with ID [android.R.id#widget_frame](../android/R.id.md) to be the parent of the specific widget for this Preference. It should similarly contain [android.R.id#title](../android/R.id.md) and [android.R.id#summary](../android/R.id.md). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnPreferenceChangeListener](Preference.md))`(`onPreferenceChangeListener:` ` [Preference.OnPreferenceChangeListener](../android/preference/Preference.OnPreferenceChangeListener.md)!`)` <br /> Sets the callback to be invoked when this Preference is changed by the user (but before the internal state has been updated). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnPreferenceClickListener](Preference.md))`(`onPreferenceClickListener:` ` [Preference.OnPreferenceClickListener](../android/preference/Preference.OnPreferenceClickListener.md)!`)` <br /> Sets the callback to be invoked when this Preference is clicked. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOrder](Preference.md))`(`order:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the order of this Preference with respect to other Preference objects on the same level. If this is not specified, the default behavior is to sort alphabetically. The [PreferenceGroup.setOrderingAsAdded(boolean)](PreferenceGroup.md))can be used to order Preference objects based on the order they appear in the XML. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPersistent](Preference.md))`(`persistent:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Sets whether this Preference is persistent. When persistent, it stores its value(s) into the persistent [SharedPreferences](../android.content/SharedPreferences.md) storage by default or into [PreferenceDataStore](PreferenceDataStore.md) if assigned. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPreferenceDataStore](Preference.md))`(`dataStore:` ` [PreferenceDataStore](PreferenceDataStore.md)!`)` <br /> Sets a [PreferenceDataStore](PreferenceDataStore.md) to be used by this Preference instead of using [android.content.SharedPreferences](../android.content/SharedPreferences.md). The data store will remain assigned even if the Preference is moved around the preference hierarchy. It will also override a data store propagated from the [PreferenceManager](PreferenceManager.md) that owns this Preference. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRecycleEnabled](Preference.md))`(`enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Sets whether this Preference has enabled to have its view recycled when used in the list view. By default the recycling is enabled. The value can be changed only before this preference is added to the preference hierarchy. If view recycling is not allowed then each time the list view populates this preference the [getView(android.view.View,android.view.ViewGroup)](Preference.md))method receives a`null`convert view and needs to recreate the view. Otherwise view gets recycled and only [onBindView(android.view.View)](Preference.md))gets called. If you override this method you*must*call through to the superclass implementation. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSelectable](Preference.md))`(`selectable:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Sets whether this Preference is selectable. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setShouldDisableView](Preference.md))`(`shouldDisableView:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Sets whether this Preference should disable its view when it gets disabled. For example, set this and [setEnabled(boolean)](Preference.md))to false for preferences that are only displaying information and 1) should not be clickable 2) should not have the view set to the disabled state. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSingleLineTitle](Preference.md))`(`singleLineTitle:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Sets whether to constrain the title of this Preference to a single line instead of letting it wrap onto multiple lines. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSummary](Preference.md))`(`summaryResId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the summary for this Preference with a resource ID. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSummary](Preference.md))`(`summary:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` <br /> Sets the summary for this Preference with a CharSequence. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTitle](Preference.md))`(`titleResId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the title for this Preference with a resource ID. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTitle](Preference.md))`(`title:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` <br /> Sets the title for this Preference with a CharSequence. This title will be placed into the ID [android.R.id#title](../android/R.id.md) within the View created by [onCreateView(android.view.ViewGroup)](Preference.md)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setWidgetLayoutResource](Preference.md))`(`widgetLayoutResId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the layout for the controllable widget portion of this Preference. This is inflated into the main layout. For example, a [CheckBoxPreference](CheckBoxPreference.md) would specify a custom layout (consisting of just the CheckBox) here, instead of creating its own main layout. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [shouldCommit](Preference.md))`()` <br /> Returns whether the [Preference](Preference.md) should commit its saved value(s) in [getEditor()](Preference.md)). This may return false in situations where batch committing is being done (by the manager) to improve performance. If this preference is using [PreferenceDataStore](PreferenceDataStore.md) this value is irrelevant. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [shouldDisableDependents](Preference.md))`()` <br /> Checks whether this preference's dependents should currently be disabled. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [shouldPersist](Preference.md))`()` <br /> Checks whether, at the given time this method is called, this Preference should store/restore its value(s) into the [SharedPreferences](../android.content/SharedPreferences.md) or into [PreferenceDataStore](PreferenceDataStore.md) if assigned. This, at minimum, checks whether this Preference is persistent and it currently has a key. Before you save/restore from the storage, check this first. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](Preference.md))`()` <br /> | ||

## XML attributes

### android:dialogIcon

```
android:dialogIcon
```
The icon for the dialog.

May be a reference to another resource, in the form "`@[+][`*package* `:]`*type* `/`*name*" or a theme attribute in the form "`?[`*package* `:]`*type* `/`*name*". 

### android:dialogLayout

```
android:dialogLayout
```
A layout to be used as the content View for the dialog. By default, this shouldn't be needed. If a custom DialogPreference is required, this should be set. For example, the EditTextPreference uses a layout with an EditText as this attribute.

May be a reference to another resource, in the form "`@[+][`*package* `:]`*type* `/`*name*" or a theme attribute in the form "`?[`*package* `:]`*type* `/`*name*". 

### android:dialogMessage

```
android:dialogMessage
```
The message in the dialog. If a dialogLayout is provided and contains a TextView with ID android:id/message, this message will be placed in there.

May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character; 

### android:dialogTitle

```
android:dialogTitle
```
The title in the dialog.

May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character; 

### android:negativeButtonText

```
android:negativeButtonText
```
The negative button text for the dialog. Set to @null to hide the negative button.

May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character; 

### android:positiveButtonText

```
android:positiveButtonText
```
The positive button text for the dialog. Set to @null to hide the positive button.

May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character;

## Public constructors

### DialogPreference

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DialogPreference(context: Context!)
```  

### DialogPreference

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DialogPreference(
    context: Context!, 
    attrs: AttributeSet!)
```  

### DialogPreference

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DialogPreference(
    context: Context!, 
    attrs: AttributeSet!, 
    defStyleAttr: Int)
```  

### DialogPreference

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DialogPreference(
    context: Context!, 
    attrs: AttributeSet!, 
    defStyleAttr: Int, 
    defStyleRes: Int)
```

## Public methods

### getDialog

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDialog(): Dialog!
```

**Deprecated:** *Deprecated in Java.*

Gets the dialog that is shown by this preference.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------|
| [Dialog](../android.app/Dialog.md)! | The dialog, or null if a dialog is not being shown. |

### getDialogIcon

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDialogIcon(): Drawable!
```

**Deprecated:** *Deprecated in Java.*

Returns the icon to be shown on subsequent dialogs.

| Return ||
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [Drawable](../android.graphics.drawable/Drawable.md)! | The icon, as a [Drawable](../android.graphics.drawable/Drawable.md). |

### getDialogLayoutResource

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDialogLayoutResource(): Int
```

**Deprecated:** *Deprecated in Java.*

Returns the layout resource that is used as the content View for subsequent dialogs.

| Return ||
|----------------------------------------------------------------------------|----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The layout resource. |

### getDialogMessage

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDialogMessage(): CharSequence!
```

**Deprecated:** *Deprecated in Java.*

Returns the message to be shown on subsequent dialogs.

| Return ||
|------------------------------------------------------------------------------------------------|--------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | The message. |

### getDialogTitle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDialogTitle(): CharSequence!
```

**Deprecated:** *Deprecated in Java.*

Returns the title to be shown on subsequent dialogs.

| Return ||
|------------------------------------------------------------------------------------------------|------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | The title. |

### getNegativeButtonText

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getNegativeButtonText(): CharSequence!
```

**Deprecated:** *Deprecated in Java.*

Returns the text of the negative button to be shown on subsequent dialogs.

| Return ||
|------------------------------------------------------------------------------------------------|----------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | The text of the negative button. |

### getPositiveButtonText

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPositiveButtonText(): CharSequence!
```

**Deprecated:** *Deprecated in Java.*

Returns the text of the positive button to be shown on subsequent dialogs.

| Return ||
|------------------------------------------------------------------------------------------------|----------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | The text of the positive button. |

### onActivityDestroy

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onActivityDestroy(): Unit
```

**Deprecated:** *Deprecated in Java.*

See Activity's onDestroy. 

### onClick

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onClick(
    dialog: DialogInterface!, 
    which: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dialog` | [DialogInterface](../android.content/DialogInterface.md)!:the dialog that received the click |
| `which` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the button that was clicked (ex. [DialogInterface.BUTTON_POSITIVE](../android.content/DialogInterface.md)) or the position of the item clicked |

### onDismiss

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onDismiss(dialog: DialogInterface!): Unit
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dialog` | [DialogInterface](../android.content/DialogInterface.md)!:the dialog that was dismissed will be passed into the method |

### setDialogIcon

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDialogIcon(dialogIcon: Drawable!): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the icon of the dialog. This will be shown on subsequent dialogs.

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dialogIcon` | [Drawable](../android.graphics.drawable/Drawable.md)!:The icon, as a [Drawable](../android.graphics.drawable/Drawable.md). |

### setDialogIcon

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDialogIcon(dialogIconRes: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the icon (resource ID) of the dialog. This will be shown on subsequent dialogs.

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------|
| `dialogIconRes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The icon, as a resource ID. |

### setDialogLayoutResource

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDialogLayoutResource(dialogLayoutResId: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the layout resource that is inflated as the [View](../android.view/View.md) to be shown as the content View of subsequent dialogs.

| Parameters ||
|---------------------|-------------------------------------------------------------------------------------------------------------------|
| `dialogLayoutResId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The layout resource ID to be inflated. |

**See Also**

- [#setDialogMessage(CharSequence)](DialogPreference.md)) 

### setDialogMessage

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDialogMessage(dialogMessageResId: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|----------------------|--------------------------------------------------------------------------------------------------------------|
| `dialogMessageResId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The dialog message as a resource. |

**See Also**

- [#setDialogMessage(CharSequence)](DialogPreference.md)) 

### setDialogMessage

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDialogMessage(dialogMessage: CharSequence!): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the message of the dialog. This will be shown on subsequent dialogs.

This message forms the content View of the dialog and conflicts with list-based dialogs, for example. If setting a custom View on a dialog via [setDialogLayoutResource(int)](DialogPreference.md)), include a text View with ID [android.R.id#message](../android/R.id.md) and it will be populated with this message.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------|
| `dialogMessage` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:The message. |

### setDialogTitle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDialogTitle(dialogTitleResId: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|--------------------|------------------------------------------------------------------------------------------------------------|
| `dialogTitleResId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The dialog title as a resource. |

**See Also**

- [#setDialogTitle(CharSequence)](DialogPreference.md)) 

### setDialogTitle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDialogTitle(dialogTitle: CharSequence!): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the title of the dialog. This will be shown on subsequent dialogs.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------|
| `dialogTitle` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:The title. |

### setNegativeButtonText

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setNegativeButtonText(negativeButtonTextResId: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|---------------------------|--------------------------------------------------------------------------------------------------------------------|
| `negativeButtonTextResId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The negative button text as a resource. |

**See Also**

- [#setNegativeButtonText(CharSequence)](DialogPreference.md)) 

### setNegativeButtonText

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setNegativeButtonText(negativeButtonText: CharSequence!): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the text of the negative button of the dialog. This will be shown on subsequent dialogs.

| Parameters ||
|----------------------|---------------------------------------------------------------------------------------------------------------------------------|
| `negativeButtonText` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:The text of the negative button. |

### setPositiveButtonText

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPositiveButtonText(positiveButtonTextResId: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|---------------------------|--------------------------------------------------------------------------------------------------------------------|
| `positiveButtonTextResId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The positive button text as a resource. |

**See Also**

- [#setPositiveButtonText(CharSequence)](DialogPreference.md)) 

### setPositiveButtonText

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPositiveButtonText(positiveButtonText: CharSequence!): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the text of the positive button of the dialog. This will be shown on subsequent dialogs.

| Parameters ||
|----------------------|---------------------------------------------------------------------------------------------------------------------------------|
| `positiveButtonText` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:The text of the positive button. |

## Protected methods

### onBindDialogView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onBindDialogView(view: View!): Unit
```

**Deprecated:** *Deprecated in Java.*

Binds views in the content View of the dialog to data.

Make sure to call through to the superclass implementation. 
If you override this method you*must*call through to the superclass implementation.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------|
| `view` | [View](../android.view/View.md)!:The content View of the dialog, if it is custom. |

### onClick

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onClick(): Unit
```

**Deprecated:** *Deprecated in Java.* 

### onCreateDialogView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onCreateDialogView(): View!
```

**Deprecated:** *Deprecated in Java.*

Creates the content view for the dialog (if a custom content view is required). By default, it inflates the dialog layout resource if it is set.

| Return ||
|---------------------------------------------------------------------------------|----------------------------------|
| [View](../android.view/View.md)! | The content View for the dialog. |

**See Also**

- [#setLayoutResource(int)](Preference.md)) 

### onDialogClosed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onDialogClosed(positiveResult: Boolean): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when the dialog is dismissed and should be used to save data to the [SharedPreferences](../android.content/SharedPreferences.md).

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `positiveResult` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Whether the positive button was clicked (true), or the negative button was clicked or the dialog was canceled (false). |

### onPrepareDialogBuilder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onPrepareDialogBuilder(builder: AlertDialog.Builder!): Unit
```

**Deprecated:** *Deprecated in Java.*

Prepares the dialog builder to be shown when the preference is clicked. Use this to set custom properties on the dialog.

Do not [AlertDialog.Builder.create()](../android/app/AlertDialog.Builder.md))or [AlertDialog.Builder.show()](../android/app/AlertDialog.Builder.md)). 

### onRestoreInstanceState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onRestoreInstanceState(state: Parcelable!): Unit
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `state` | [Parcelable](../android.os/Parcelable.md)!:The saved state that had previously been returned by [onSaveInstanceState](Preference.md)). |

### onSaveInstanceState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onSaveInstanceState(): Parcelable!
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Parcelable](../android.os/Parcelable.md)! | A Parcelable object containing the current dynamic state of this Preference, or`null`if there is nothing interesting to save. The default implementation returns`null`. |

### showDialog

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun showDialog(state: Bundle!): Unit
```

**Deprecated:** *Deprecated in Java.*

Shows the dialog associated with this Preference. This is normally initiated automatically on clicking on the preference. Call this method if you need to show the dialog on some other event.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------|
| `state` | [Bundle](../android.os/Bundle.md)!:Optional instance state to restore on the dialog |
