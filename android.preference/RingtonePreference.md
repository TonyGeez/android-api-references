Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RingtonePreference

Kotlin | [Java](https://developer.android.com/reference/android/preference/RingtonePreference "View this page in Java")

```
open class RingtonePreference : Preference, PreferenceManager.OnActivityResultListener
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [android.preference.Preference](https://developer.android.com/reference/kotlin/android/preference/Preference) ||
| | ↳ | [android.preference.RingtonePreference](https://developer.android.com/reference/kotlin/android/preference/RingtonePreference#) |

> [!CAUTION]
> **This class was deprecated in API level 29.**
>
> Use the [AndroidX](https://developer.android.com/jetpack/androidx.html) [Preference Library](https://developer.android.com/reference/androidx/preference/package-summary.html) for consistent behavior across all devices. For more information on using the AndroidX Preference Library see [Settings](https://developer.android.com/guide/topics/ui/settings.html).

A `https://developer.android.com/reference/kotlin/android/preference/Preference` that allows the user to choose a ringtone from those on the device. The chosen ringtone's URI will be persisted as a string.

If the user chooses the "Default" item, the saved string will be one of `https://developer.android.com/reference/kotlin/android/provider/Settings.System.html#DEFAULT_RINGTONE_URI:android.net.Uri`, `https://developer.android.com/reference/kotlin/android/provider/Settings.System.html#DEFAULT_NOTIFICATION_URI:android.net.Uri`, or `https://developer.android.com/reference/kotlin/android/provider/Settings.System.html#DEFAULT_ALARM_ALERT_URI:android.net.Uri`. If the user chooses the "Silent" item, the saved string will be an empty string.

## Summary

| XML attributes ||
|---|---|
| [`android:ringtoneType`](https://developer.android.com/reference/kotlin/android/preference/RingtonePreference#attr_RingtonePreference) | Which ringtone type(s) to show in the picker. |
| [`android:showDefault`](https://developer.android.com/reference/kotlin/android/preference/RingtonePreference#attr_RingtonePreference) | Whether to show an item for a default sound. |
| [`android:showSilent`](https://developer.android.com/reference/kotlin/android/preference/RingtonePreference#attr_RingtonePreference) | Whether to show an item for 'Silent'. |

| Inherited XML attributes ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/preference/Preference` |---|---| | `https://developer.android.com/reference/kotlin/android/preference/Preference#attr_Preference` | The default value for the preference, which will be set either if persistence is off or persistence is on and the preference is not found in the persistent storage. May be a reference to another resource, in the form "`@[+][package:]type/name`" or a theme attribute in the form "`?[package:]type/name`". May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character; May be an integer value, such as "`100`". May be a boolean value, such as "`true`" or "`false`". May be a floating point value, such as "`1.2`". <br /> | | `https://developer.android.com/reference/kotlin/android/preference/Preference#attr_Preference` | The key of another Preference that this Preference will depend on. If the other Preference is not set or is off, this Preference will be disabled. May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character; <br /> | | `https://developer.android.com/reference/kotlin/android/preference/Preference#attr_Preference` | Whether the Preference is enabled. May be a boolean value, such as "`true`" or "`false`". <br /> | | `https://developer.android.com/reference/kotlin/android/preference/Preference#attr_Preference` | When used inside of a modern PreferenceActivity, this declares a new PreferenceFragment to be shown when the user selects this item. May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character; <br /> | | `https://developer.android.com/reference/kotlin/android/preference/Preference#attr_Preference` | The optional icon for the preference. May be a reference to another resource, in the form "`@[+][package:]type/name`" or a theme attribute in the form "`?[package:]type/name`". <br /> | | `https://developer.android.com/reference/kotlin/android/preference/Preference#attr_Preference` | Whether the space for the preference icon view will be reserved. By default, preference icon view visibility will be set to GONE when there is no icon provided, so the default value of this attribute is false. May be a boolean value, such as "`true`" or "`false`". <br /> | | `https://developer.android.com/reference/kotlin/android/preference/Preference#attr_Preference` | The key to store the Preference value. May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character; <br /> | | `https://developer.android.com/reference/kotlin/android/preference/Preference#attr_Preference` | The layout for the Preference in a PreferenceActivity screen. This should rarely need to be changed, look at widgetLayout instead. May be a reference to another resource, in the form "`@[+][package:]type/name`" or a theme attribute in the form "`?[package:]type/name`". <br /> | | `https://developer.android.com/reference/kotlin/android/preference/Preference#attr_Preference` | The order for the Preference (lower values are to be ordered first). If this is not specified, the default ordering will be alphabetic. May be an integer value, such as "`100`". <br /> | | `https://developer.android.com/reference/kotlin/android/preference/Preference#attr_Preference` | Whether the Preference stores its value to the storage. May be a boolean value, such as "`true`" or "`false`". <br /> | | `https://developer.android.com/reference/kotlin/android/preference/Preference#attr_Preference` | Whether the preference has enabled to have its view recycled when used in the list view. This is true by default. May be a boolean value, such as "`true`" or "`false`". <br /> | | `https://developer.android.com/reference/kotlin/android/preference/Preference#attr_Preference` | Whether the Preference is selectable. May be a boolean value, such as "`true`" or "`false`". <br /> | | `https://developer.android.com/reference/kotlin/android/preference/Preference#attr_Preference` | Whether the view of this Preference should be disabled when this Preference is disabled. May be a boolean value, such as "`true`" or "`false`". <br /> | | `https://developer.android.com/reference/kotlin/android/preference/Preference#attr_Preference` | Whether to use single line for the preference title text. By default, preference title will be constrained to one line, so the default value of this attribute is true. May be a boolean value, such as "`true`" or "`false`". <br /> | | `https://developer.android.com/reference/kotlin/android/preference/Preference#attr_Preference` | The summary for the Preference. In API 25 and earlier, this value is read as a plain string with styling information stripped. May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character; <br /> | | `https://developer.android.com/reference/kotlin/android/preference/Preference#attr_Preference` | The title for the Preference. In API 25 and earlier, this value is read as a plain string with styling information stripped. May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character; <br /> | | `https://developer.android.com/reference/kotlin/android/preference/Preference#attr_Preference` | The layout for the controllable widget portion of a Preference. This is inflated into the layout for a Preference and should be used more frequently than the layout attribute. For example, a checkbox preference would specify a custom layout (consisting of just the CheckBox) here. May be a reference to another resource, in the form "`@[+][package:]type/name`" or a theme attribute in the form "`?[package:]type/name`". <br /> | ||

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/preference/Preference` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/preference/Preference#DEFAULT_ORDER:kotlin.Int` Specify for `https://developer.android.com/reference/kotlin/android/preference/Preference#setOrder(kotlin.Int)` if a specific order is not required. <br /> | ||

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/preference/RingtonePreference#RingtonePreference(android.content.Context)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!)` <br /> |
| `https://developer.android.com/reference/kotlin/android/preference/RingtonePreference#RingtonePreference(android.content.Context,%20android.util.AttributeSet)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!, attrs: https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#!)` <br /> |
| `https://developer.android.com/reference/kotlin/android/preference/RingtonePreference#RingtonePreference(android.content.Context,%20android.util.AttributeSet,%20kotlin.Int)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!, attrs: https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#!, defStyleAttr: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| `https://developer.android.com/reference/kotlin/android/preference/RingtonePreference#RingtonePreference(android.content.Context,%20android.util.AttributeSet,%20kotlin.Int,%20kotlin.Int)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!, attrs: https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#!, defStyleAttr: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, defStyleRes: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |

| Public methods ||
|---|---|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/preference/RingtonePreference#getRingtoneType()()` Returns the sound type(s) that are shown in the picker. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/preference/RingtonePreference#getShowDefault()()` Returns whether to a show an item for the default sound/ringtone. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/preference/RingtonePreference#getShowSilent()()` Returns whether to a show an item for 'Silent'. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/preference/RingtonePreference#onActivityResult(kotlin.Int,%20kotlin.Int,%20android.content.Intent)(requestCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, resultCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, data: https://developer.android.com/reference/kotlin/android/content/Intent.html#!)` See Activity's onActivityResult. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/preference/RingtonePreference#setRingtoneType(kotlin.Int)(type: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the sound type(s) that are shown in the picker. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/preference/RingtonePreference#setShowDefault(kotlin.Boolean)(showDefault: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets whether to show an item for the default sound/ringtone. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/preference/RingtonePreference#setShowSilent(kotlin.Boolean)(showSilent: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets whether to show an item for 'Silent'. |

| Protected methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/preference/RingtonePreference#onAttachedToHierarchy(android.preference.PreferenceManager)(preferenceManager: https://developer.android.com/reference/kotlin/android/preference/PreferenceManager!)` Called when this Preference has been attached to a Preference hierarchy. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/preference/RingtonePreference#onClick()()` Processes a click on the preference. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | `https://developer.android.com/reference/kotlin/android/preference/RingtonePreference#onGetDefaultValue(android.content.res.TypedArray,%20kotlin.Int)(a: https://developer.android.com/reference/kotlin/android/content/res/TypedArray.html#!, index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Called when a Preference is being inflated and the default value attribute needs to be read. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/preference/RingtonePreference#onPrepareRingtonePickerIntent(android.content.Intent)(ringtonePickerIntent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!)` Prepares the intent to launch the ringtone picker. |
| open [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)! | `https://developer.android.com/reference/kotlin/android/preference/RingtonePreference#onRestoreRingtone()()` Called when the chooser is about to be shown and the current ringtone should be marked. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/preference/RingtonePreference#onSaveRingtone(android.net.Uri)(ringtoneUri: https://developer.android.com/reference/kotlin/android/net/Uri.html#!)` Called when a ringtone is chosen. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/preference/RingtonePreference#onSetInitialValue(kotlin.Boolean,%20kotlin.Any)(restorePersistedValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, defaultValueObj: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!)` Implement this to set the initial value of the Preference. |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/preference/Preference` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/preference/Preference#callChangeListener(kotlin.Any)(newValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!)` Call this method after the user changes the preference, but before the internal state is set. This allows the client to ignore the user value. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/preference/Preference#compareTo(android.preference.Preference)(other: https://developer.android.com/reference/kotlin/android/preference/Preference!)` Compares Preference objects based on order (if set), otherwise alphabetically on the titles. <br /> | | `https://developer.android.com/reference/kotlin/android/preference/Preference!` | `https://developer.android.com/reference/kotlin/android/preference/Preference#findPreferenceInHierarchy(kotlin.String)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Finds a Preference in this hierarchy (the whole thing, even above/below your `https://developer.android.com/reference/kotlin/android/preference/PreferenceScreen` screen break) with the given key. This only functions after we have been attached to a hierarchy. <br /> | | `https://developer.android.com/reference/kotlin/android/content/Context.html#!` | `https://developer.android.com/reference/kotlin/android/preference/Preference#getContext()()` Returns the `https://developer.android.com/reference/kotlin/android/content/Context.html#` of this Preference. Each Preference in a Preference hierarchy can be from different Context (for example, if multiple activities provide preferences into a single `https://developer.android.com/reference/kotlin/android/preference/PreferenceActivity`). This Context will be used to save the Preference values. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | `https://developer.android.com/reference/kotlin/android/preference/Preference#getDependency()()` Returns the key of the dependency on this Preference. <br /> | | `https://developer.android.com/reference/kotlin/android/content/SharedPreferences.Editor.html#!` | `https://developer.android.com/reference/kotlin/android/preference/Preference#getEditor()()` Returns an `https://developer.android.com/reference/kotlin/android/content/SharedPreferences.Editor.html#` where this Preference can save its value(s). Usually it's easier to use one of the helper save methods: `https://developer.android.com/reference/kotlin/android/preference/Preference#persistBoolean(kotlin.Boolean)`, `https://developer.android.com/reference/kotlin/android/preference/Preference#persistFloat(kotlin.Float)`, `https://developer.android.com/reference/kotlin/android/preference/Preference#persistInt(kotlin.Int)`, `https://developer.android.com/reference/kotlin/android/preference/Preference#persistLong(kotlin.Long)`, `https://developer.android.com/reference/kotlin/android/preference/Preference#persistString(kotlin.String)`. To read values, see `https://developer.android.com/reference/kotlin/android/preference/Preference#getSharedPreferences()`. If `https://developer.android.com/reference/kotlin/android/preference/Preference#shouldCommit()` returns true, it is this Preference's responsibility to commit. In some cases, writes to this will not be committed right away and hence not show up in the SharedPreferences, this is intended behavior to improve performance. <br /> | | `https://developer.android.com/reference/kotlin/android/os/Bundle.html#!` | `https://developer.android.com/reference/kotlin/android/preference/Preference#getExtras()()` Return the extras Bundle object associated with this preference, creating a new Bundle if there currently isn't one. You can use this to get and set individual extra key/value pairs. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | `https://developer.android.com/reference/kotlin/android/preference/Preference#getFragment()()` Return the fragment class name associated with this Preference. <br /> | | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!` | `https://developer.android.com/reference/kotlin/android/preference/Preference#getIcon()()` Returns the icon of this Preference. <br /> | | `https://developer.android.com/reference/kotlin/android/content/Intent.html#!` | `https://developer.android.com/reference/kotlin/android/preference/Preference#getIntent()()` Return the `https://developer.android.com/reference/kotlin/android/content/Intent.html#` associated with this Preference. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | `https://developer.android.com/reference/kotlin/android/preference/Preference#getKey()()` Gets the key for this Preference, which is also the key used for storing values into `https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#` or `https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/preference/Preference#getLayoutResource()()` Gets the layout resource that will be shown as the `https://developer.android.com/reference/kotlin/android/view/View.html#` for this Preference. <br /> | | `https://developer.android.com/reference/kotlin/android/preference/Preference.OnPreferenceChangeListener!` | `https://developer.android.com/reference/kotlin/android/preference/Preference#getOnPreferenceChangeListener()()` Returns the callback to be invoked when this Preference is changed by the user (but before the internal state has been updated). <br /> | | `https://developer.android.com/reference/kotlin/android/preference/Preference.OnPreferenceClickListener!` | `https://developer.android.com/reference/kotlin/android/preference/Preference#getOnPreferenceClickListener()()` Returns the callback to be invoked when this Preference is clicked. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/preference/Preference#getOrder()()` Gets the order of this Preference with respect to other Preference objects on the same level. <br /> | | `https://developer.android.com/reference/kotlin/android/preference/PreferenceGroup?` | `https://developer.android.com/reference/kotlin/android/preference/Preference#getParent()()` Returns the `https://developer.android.com/reference/kotlin/android/preference/PreferenceGroup` which is this Preference assigned to or `null` if this preference is not assigned to any group or is a root Preference. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/preference/Preference#getPersistedBoolean(kotlin.Boolean)(defaultReturnValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Attempts to get a persisted boolean if this Preference is persistent. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | `https://developer.android.com/reference/kotlin/android/preference/Preference#getPersistedFloat(kotlin.Float)(defaultReturnValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Attempts to get a persisted float if this Preference is persistent. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/preference/Preference#getPersistedInt(kotlin.Int)(defaultReturnValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Attempts to get a persisted int if this Preference is persistent. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | `https://developer.android.com/reference/kotlin/android/preference/Preference#getPersistedLong(kotlin.Long)(defaultReturnValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Attempts to get a persisted long if this Preference is persistent. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | `https://developer.android.com/reference/kotlin/android/preference/Preference#getPersistedString(kotlin.String)(defaultReturnValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Attempts to get a persisted String if this Preference is persistent. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | `https://developer.android.com/reference/kotlin/android/preference/Preference#getPersistedStringSet(kotlin.collections.MutableSet)(defaultReturnValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!)` Attempts to get a persisted set of Strings if this Preference is persistent. <br /> | | `https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore?` | `https://developer.android.com/reference/kotlin/android/preference/Preference#getPreferenceDataStore()()` Returns `https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore` used by this Preference. Returns `null` if `https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#` is used instead. By default preferences always use `https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#`. To make this preference to use the `https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore` you need to assign your implementation to the Preference itself via `https://developer.android.com/reference/kotlin/android/preference/Preference#setPreferenceDataStore(android.preference.PreferenceDataStore)` or to its `https://developer.android.com/reference/kotlin/android/preference/PreferenceManager` via `https://developer.android.com/reference/kotlin/android/preference/PreferenceManager#setPreferenceDataStore(android.preference.PreferenceDataStore)`. <br /> | | `https://developer.android.com/reference/kotlin/android/preference/PreferenceManager!` | `https://developer.android.com/reference/kotlin/android/preference/Preference#getPreferenceManager()()` Gets the `https://developer.android.com/reference/kotlin/android/preference/PreferenceManager` that manages this Preference object's tree. <br /> | | `https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#!` | `https://developer.android.com/reference/kotlin/android/preference/Preference#getSharedPreferences()()` Returns the `https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#` where this Preference can read its value(s). Usually, it's easier to use one of the helper read methods: `https://developer.android.com/reference/kotlin/android/preference/Preference#getPersistedBoolean(kotlin.Boolean)`, `https://developer.android.com/reference/kotlin/android/preference/Preference#getPersistedFloat(kotlin.Float)`, `https://developer.android.com/reference/kotlin/android/preference/Preference#getPersistedInt(kotlin.Int)`, `https://developer.android.com/reference/kotlin/android/preference/Preference#getPersistedLong(kotlin.Long)`, `https://developer.android.com/reference/kotlin/android/preference/Preference#getPersistedString(kotlin.String)`. To save values, see `https://developer.android.com/reference/kotlin/android/preference/Preference#getEditor()`. In some cases, writes to the `https://developer.android.com/reference/kotlin/android/preference/Preference#getEditor()` will not be committed right away and hence not show up in the returned `https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#`, this is intended behavior to improve performance. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/preference/Preference#getShouldDisableView()()` Checks whether this Preference should disable its view when it's action is disabled. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!` | `https://developer.android.com/reference/kotlin/android/preference/Preference#getSummary()()` Returns the summary of this Preference. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!` | `https://developer.android.com/reference/kotlin/android/preference/Preference#getTitle()()` Returns the title of this Preference. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/preference/Preference#getTitleRes()()` Returns the title resource ID of this Preference. If the title did not come from a resource, `0` is returned. <br /> | | `https://developer.android.com/reference/kotlin/android/view/View.html#!` | `https://developer.android.com/reference/kotlin/android/preference/Preference#getView(android.view.View,%20android.view.ViewGroup)(convertView: https://developer.android.com/reference/kotlin/android/view/View.html#!, parent: https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#!)` Gets the View that will be shown in the `https://developer.android.com/reference/kotlin/android/preference/PreferenceActivity`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/preference/Preference#getWidgetLayoutResource()()` Gets the layout resource for the controllable widget portion of this Preference. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/preference/Preference#hasKey()()` Checks whether this Preference has a valid key. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/preference/Preference#isEnabled()()` Checks whether this Preference should be enabled in the list. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/preference/Preference#isIconSpaceReserved()()` Gets whether the space this preference icon view is reserved. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/preference/Preference#isPersistent()()` Checks whether this Preference is persistent. If it is, it stores its value(s) into the persistent `https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#` storage by default or into `https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore` if assigned. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/preference/Preference#isRecycleEnabled()()` Checks whether this Preference has enabled to have its view recycled when used in the list view. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/preference/Preference#isSelectable()()` Checks whether this Preference should be selectable in the list. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/preference/Preference#isSingleLineTitle()()` Gets whether the title of this preference is constrained to a single line. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/preference/Preference#notifyChanged()()` Should be called when the data of this `https://developer.android.com/reference/kotlin/android/preference/Preference` has changed. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/preference/Preference#notifyDependencyChange(kotlin.Boolean)(disableDependents: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Notifies any listening dependents of a change that affects the dependency. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/preference/Preference#notifyHierarchyChanged()()` Should be called when a Preference has been added/removed from this group, or the ordering should be re-evaluated. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/preference/Preference#onAttachedToActivity()()` Called when the Preference hierarchy has been attached to the `https://developer.android.com/reference/kotlin/android/preference/PreferenceActivity`. This can also be called when this Preference has been attached to a group that was already attached to the `https://developer.android.com/reference/kotlin/android/preference/PreferenceActivity`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/preference/Preference#onBindView(android.view.View)(view: https://developer.android.com/reference/kotlin/android/view/View.html#!)` Binds the created View to the data for this Preference. This is a good place to grab references to custom Views in the layout and set properties on them. Make sure to call through to the superclass's implementation. If you override this method you *must* call through to the superclass implementation. <br /> | | `https://developer.android.com/reference/kotlin/android/view/View.html#!` | `https://developer.android.com/reference/kotlin/android/preference/Preference#onCreateView(android.view.ViewGroup)(parent: https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#!)` Creates the View to be shown for this Preference in the `https://developer.android.com/reference/kotlin/android/preference/PreferenceActivity`. The default behavior is to inflate the main layout of this Preference (see `https://developer.android.com/reference/kotlin/android/preference/Preference#setLayoutResource(kotlin.Int)`. If changing this behavior, please specify a `https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#` with ID `https://developer.android.com/reference/kotlin/android/R.id.html#widget_frame:kotlin.Int`. Make sure to call through to the superclass's implementation. If you override this method you *must* call through to the superclass implementation. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/preference/Preference#onDependencyChanged(android.preference.Preference,%20kotlin.Boolean)(dependency: https://developer.android.com/reference/kotlin/android/preference/Preference!, disableDependent: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Called when the dependency changes. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/preference/Preference#onParentChanged(android.preference.Preference,%20kotlin.Boolean)(parent: https://developer.android.com/reference/kotlin/android/preference/Preference!, disableChild: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Called when the implicit parent dependency changes. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/preference/Preference#onPrepareForRemoval()()` Called when this Preference is being removed from the hierarchy. You should remove any references to this Preference that you know about. Make sure to call through to the superclass implementation. If you override this method you *must* call through to the superclass implementation. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/preference/Preference#onRestoreInstanceState(android.os.Parcelable)(state: https://developer.android.com/reference/kotlin/android/os/Parcelable.html#!)` Hook allowing a Preference to re-apply a representation of its internal state that had previously been generated by `https://developer.android.com/reference/kotlin/android/preference/Preference#onSaveInstanceState()`. This function will never be called with a `null` state. <br /> | | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#!` | `https://developer.android.com/reference/kotlin/android/preference/Preference#onSaveInstanceState()()` Hook allowing a Preference to generate a representation of its internal state that can later be used to create a new instance with that same state. This state should only contain information that is not persistent or can be reconstructed later. <br /> | | `https://developer.android.com/reference/kotlin/android/os/Bundle.html#!` | `https://developer.android.com/reference/kotlin/android/preference/Preference#peekExtras()()` Return the extras Bundle object associated with this preference, returning `null` if there is not currently one. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/preference/Preference#persistBoolean(kotlin.Boolean)(value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Attempts to persist a boolean if this Preference is persistent. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/preference/Preference#persistFloat(kotlin.Float)(value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Attempts to persist a long if this Preference is persistent. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/preference/Preference#persistInt(kotlin.Int)(value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Attempts to persist an int if this Preference is persistent. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/preference/Preference#persistLong(kotlin.Long)(value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Attempts to persist a long if this Preference is persistent. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/preference/Preference#persistString(kotlin.String)(value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Attempts to persist a String if this Preference is persistent. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/preference/Preference#persistStringSet(kotlin.collections.MutableSet)(values: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!)` Attempts to persist a set of Strings if this Preference is persistent. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/preference/Preference#restoreHierarchyState(android.os.Bundle)(container: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!)` Restore this Preference hierarchy's previously saved state from the given container. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/preference/Preference#saveHierarchyState(android.os.Bundle)(container: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!)` Store this Preference hierarchy's frozen state into the given container. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/preference/Preference#setDefaultValue(kotlin.Any)(defaultValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!)` Sets the default value for this Preference, which will be set either if persistence is off or persistence is on and the preference is not found in the persistent storage. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/preference/Preference#setDependency(kotlin.String)(dependencyKey: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Sets the key of a Preference that this Preference will depend on. If that Preference is not set or is off, this Preference will be disabled. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/preference/Preference#setEnabled(kotlin.Boolean)(enabled: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets whether this Preference is enabled. If disabled, it will not handle clicks. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/preference/Preference#setFragment(kotlin.String)(fragment: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Sets the class name of a fragment to be shown when this Preference is clicked. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/preference/Preference#setIcon(android.graphics.drawable.Drawable)(icon: https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!)` Sets the icon for this Preference with a Drawable. This icon will be placed into the ID `https://developer.android.com/reference/kotlin/android/R.id.html#icon:kotlin.Int` within the View created by `https://developer.android.com/reference/kotlin/android/preference/Preference#onCreateView(android.view.ViewGroup)`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/preference/Preference#setIcon(kotlin.Int)(iconResId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the icon for this Preference with a resource ID. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/preference/Preference#setIconSpaceReserved(kotlin.Boolean)(iconSpaceReserved: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets whether to reserve the space of this Preference icon view when no icon is provided. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/preference/Preference#setIntent(android.content.Intent)(intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#!)` Sets an `https://developer.android.com/reference/kotlin/android/content/Intent.html#` to be used for `https://developer.android.com/reference/kotlin/android/content/Context.html#startActivity(android.content.Intent)` when this Preference is clicked. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/preference/Preference#setKey(kotlin.String)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Sets the key for this Preference, which is used as a key to the `https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#` or `https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore`. This should be unique for the package. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/preference/Preference#setLayoutResource(kotlin.Int)(layoutResId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the layout resource that is inflated as the `https://developer.android.com/reference/kotlin/android/view/View.html#` to be shown for this Preference. In most cases, the default layout is sufficient for custom Preference objects and only the widget layout needs to be changed. This layout should contain a `https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#` with ID `https://developer.android.com/reference/kotlin/android/R.id.html#widget_frame:kotlin.Int` to be the parent of the specific widget for this Preference. It should similarly contain `https://developer.android.com/reference/kotlin/android/R.id.html#title:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/R.id.html#summary:kotlin.Int`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/preference/Preference#setOnPreferenceChangeListener(android.preference.Preference.OnPreferenceChangeListener)(onPreferenceChangeListener: https://developer.android.com/reference/kotlin/android/preference/Preference.OnPreferenceChangeListener!)` Sets the callback to be invoked when this Preference is changed by the user (but before the internal state has been updated). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/preference/Preference#setOnPreferenceClickListener(android.preference.Preference.OnPreferenceClickListener)(onPreferenceClickListener: https://developer.android.com/reference/kotlin/android/preference/Preference.OnPreferenceClickListener!)` Sets the callback to be invoked when this Preference is clicked. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/preference/Preference#setOrder(kotlin.Int)(order: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the order of this Preference with respect to other Preference objects on the same level. If this is not specified, the default behavior is to sort alphabetically. The `https://developer.android.com/reference/kotlin/android/preference/PreferenceGroup#setOrderingAsAdded(kotlin.Boolean)` can be used to order Preference objects based on the order they appear in the XML. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/preference/Preference#setPersistent(kotlin.Boolean)(persistent: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets whether this Preference is persistent. When persistent, it stores its value(s) into the persistent `https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#` storage by default or into `https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore` if assigned. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/preference/Preference#setPreferenceDataStore(android.preference.PreferenceDataStore)(dataStore: https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore!)` Sets a `https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore` to be used by this Preference instead of using `https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#`. The data store will remain assigned even if the Preference is moved around the preference hierarchy. It will also override a data store propagated from the `https://developer.android.com/reference/kotlin/android/preference/PreferenceManager` that owns this Preference. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/preference/Preference#setRecycleEnabled(kotlin.Boolean)(enabled: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets whether this Preference has enabled to have its view recycled when used in the list view. By default the recycling is enabled. The value can be changed only before this preference is added to the preference hierarchy. If view recycling is not allowed then each time the list view populates this preference the `https://developer.android.com/reference/kotlin/android/preference/Preference#getView(android.view.View,%20android.view.ViewGroup)` method receives a `null` convert view and needs to recreate the view. Otherwise view gets recycled and only `https://developer.android.com/reference/kotlin/android/preference/Preference#onBindView(android.view.View)` gets called. If you override this method you *must* call through to the superclass implementation. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/preference/Preference#setSelectable(kotlin.Boolean)(selectable: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets whether this Preference is selectable. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/preference/Preference#setShouldDisableView(kotlin.Boolean)(shouldDisableView: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets whether this Preference should disable its view when it gets disabled. For example, set this and `https://developer.android.com/reference/kotlin/android/preference/Preference#setEnabled(kotlin.Boolean)` to false for preferences that are only displaying information and 1) should not be clickable 2) should not have the view set to the disabled state. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/preference/Preference#setSingleLineTitle(kotlin.Boolean)(singleLineTitle: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets whether to constrain the title of this Preference to a single line instead of letting it wrap onto multiple lines. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/preference/Preference#setSummary(kotlin.Int)(summaryResId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the summary for this Preference with a resource ID. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/preference/Preference#setSummary(kotlin.CharSequence)(summary: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!)` Sets the summary for this Preference with a CharSequence. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/preference/Preference#setTitle(kotlin.Int)(titleResId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the title for this Preference with a resource ID. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/preference/Preference#setTitle(kotlin.CharSequence)(title: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!)` Sets the title for this Preference with a CharSequence. This title will be placed into the ID `https://developer.android.com/reference/kotlin/android/R.id.html#title:kotlin.Int` within the View created by `https://developer.android.com/reference/kotlin/android/preference/Preference#onCreateView(android.view.ViewGroup)`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/preference/Preference#setWidgetLayoutResource(kotlin.Int)(widgetLayoutResId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the layout for the controllable widget portion of this Preference. This is inflated into the main layout. For example, a `https://developer.android.com/reference/kotlin/android/preference/CheckBoxPreference` would specify a custom layout (consisting of just the CheckBox) here, instead of creating its own main layout. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/preference/Preference#shouldCommit()()` Returns whether the `https://developer.android.com/reference/kotlin/android/preference/Preference` should commit its saved value(s) in `https://developer.android.com/reference/kotlin/android/preference/Preference#getEditor()`. This may return false in situations where batch committing is being done (by the manager) to improve performance. If this preference is using `https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore` this value is irrelevant. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/preference/Preference#shouldDisableDependents()()` Checks whether this preference's dependents should currently be disabled. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/preference/Preference#shouldPersist()()` Checks whether, at the given time this method is called, this Preference should store/restore its value(s) into the `https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#` or into `https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore` if assigned. This, at minimum, checks whether this Preference is persistent and it currently has a key. Before you save/restore from the storage, check this first. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | `https://developer.android.com/reference/kotlin/android/preference/Preference#toString()()` Returns a string representation of the object. <br /> | ||

## XML attributes

### android:ringtoneType

```
android:ringtoneType
```
Which ringtone type(s) to show in the picker.

Must be one or more (separated by '|') of the following constant values.

| Constant | Value | Description |
|---|---|---|
| alarm | 4 | Alarm sounds. |
| all | 7 | All available ringtone sounds. |
| notification | 2 | Notification sounds. |
| ringtone | 1 | Ringtones. |

### android:showDefault

```
android:showDefault
```
Whether to show an item for a default sound.

May be a boolean value, such as "`true`" or "`false`".

### android:showSilent

```
android:showSilent
```
Whether to show an item for 'Silent'.

May be a boolean value, such as "`true`" or "`false`".

## Public constructors

### RingtonePreference

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
RingtonePreference(context: Context!)
```

### RingtonePreference

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
RingtonePreference(
    context: Context!, 
    attrs: AttributeSet!)
```

### RingtonePreference

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
RingtonePreference(
    context: Context!, 
    attrs: AttributeSet!, 
    defStyleAttr: Int)
```

### RingtonePreference

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
RingtonePreference(
    context: Context!, 
    attrs: AttributeSet!, 
    defStyleAttr: Int, 
    defStyleRes: Int)
```

## Public methods

### getRingtoneType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getRingtoneType(): Int
```

**Deprecated:** *Deprecated in Java.*

Returns the sound type(s) that are shown in the picker.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The sound type(s) that are shown in the picker. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/preference/RingtonePreference#setRingtoneType(kotlin.Int)`

### getShowDefault

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getShowDefault(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Returns whether to a show an item for the default sound/ringtone.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Whether to show an item for the default sound/ringtone. |

### getShowSilent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getShowSilent(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Returns whether to a show an item for 'Silent'.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Whether to show an item for 'Silent'. |

### onActivityResult

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onActivityResult(
    requestCode: Int, 
    resultCode: Int, 
    data: Intent!
): Boolean
```

**Deprecated:** *Deprecated in Java.*

See Activity's onActivityResult.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Whether the request code was handled (in which case subsequent listeners will not be called. |

### setRingtoneType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setRingtoneType(type: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the sound type(s) that are shown in the picker.

| Parameters ||
|---|---|
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The sound type(s) that are shown in the picker. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/RingtoneManager.html#EXTRA_RINGTONE_TYPE:kotlin.String`

### setShowDefault

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setShowDefault(showDefault: Boolean): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets whether to show an item for the default sound/ringtone. The default to use will be deduced from the sound type(s) being shown.

| Parameters ||
|---|---|
| `showDefault` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Whether to show the default or not. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/RingtoneManager.html#EXTRA_RINGTONE_SHOW_DEFAULT:kotlin.String`

### setShowSilent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setShowSilent(showSilent: Boolean): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets whether to show an item for 'Silent'.

| Parameters ||
|---|---|
| `showSilent` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Whether to show 'Silent'. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/RingtoneManager.html#EXTRA_RINGTONE_SHOW_SILENT:kotlin.String`

## Protected methods

### onAttachedToHierarchy

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun onAttachedToHierarchy(preferenceManager: PreferenceManager!): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when this Preference has been attached to a Preference hierarchy. Make sure to call the super implementation.

| Parameters ||
|---|---|
| `preferenceManager` | [PreferenceManager](https://developer.android.com/reference/kotlin/android/preference/PreferenceManager)!: The PreferenceManager of the hierarchy. |

### onClick

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun onClick(): Unit
```

**Deprecated:** *Deprecated in Java.*

Processes a click on the preference. This includes saving the value to the `https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#`. However, the overridden method should call `https://developer.android.com/reference/kotlin/android/preference/Preference#callChangeListener(kotlin.Any)` to make sure the client wants to update the preference's state with the new value.

### onGetDefaultValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun onGetDefaultValue(
    a: TypedArray!, 
    index: Int
): Any!
```

**Deprecated:** *Deprecated in Java.*

Called when a Preference is being inflated and the default value attribute needs to be read. Since different Preference types have different value types, the subclass should get and return the default value which will be its value type.

For example, if the value type is String, the body of the method would proxy to `https://developer.android.com/reference/kotlin/android/content/res/TypedArray.html#getString(kotlin.Int)`.

| Parameters ||
|---|---|
| `a` | [TypedArray](https://developer.android.com/reference/kotlin/android/content/res/TypedArray.html#)!: The set of attributes. |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index of the default value attribute. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!` | The default value of this preference type. |

### onPrepareRingtonePickerIntent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun onPrepareRingtonePickerIntent(ringtonePickerIntent: Intent!): Unit
```

**Deprecated:** *Deprecated in Java.*

Prepares the intent to launch the ringtone picker. This can be modified to adjust the parameters of the ringtone picker.

| Parameters ||
|---|---|
| `ringtonePickerIntent` | [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!: The ringtone picker intent that can be modified by putting extras. |

### onRestoreRingtone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun onRestoreRingtone(): Uri!
```

**Deprecated:** *Deprecated in Java.*

Called when the chooser is about to be shown and the current ringtone should be marked. Can return null to not mark any ringtone.

By default, this restores the previous ringtone URI from the persistent storage.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/Uri.html#!` | The ringtone to be marked as the current ringtone. |

### onSaveRingtone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun onSaveRingtone(ringtoneUri: Uri!): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when a ringtone is chosen.

By default, this saves the ringtone URI to the persistent storage as a string.

| Parameters ||
|---|---|
| `ringtoneUri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!: The chosen ringtone's `https://developer.android.com/reference/kotlin/android/net/Uri.html#`. Can be null. |

### onSetInitialValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun onSetInitialValue(
    restorePersistedValue: Boolean, 
    defaultValueObj: Any!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Implement this to set the initial value of the Preference.

If restorePersistedValue is true, you should restore the Preference value from the `https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#`. If restorePersistedValue is false, you should set the Preference value to defaultValue that is given (and possibly store to SharedPreferences if `https://developer.android.com/reference/kotlin/android/preference/Preference#shouldPersist()` is true).

In case of using `https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore`, the restorePersistedValue is always `true`. But the default value (if provided) is set.

This may not always be called. One example is if it should not persist but there is no default value given.

| Parameters ||
|---|---|
| `restorePersistedValue` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): True to restore the persisted value; false to use the given defaultValue. |
| `defaultValue` | The default value for this Preference. Only use this if restorePersistedValue is false. |
