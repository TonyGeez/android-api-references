Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RingtonePreference

Kotlin | [Java](RingtonePreference.md)
| --- | --- |

```
open class RingtonePreference : Preference, PreferenceManager.OnActivityResultListener
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.preference.Preference](Preference.md) ||
| | ↳ | [android.preference.RingtonePreference](RingtonePreference.md) |

> [!CAUTION]
> **This class was deprecated in API level 29.**
>
> Use the [AndroidX](https://developer.android.com/jetpack/androidx.html) [Preference Library](../androidx/preference/_package.md) for consistent behavior across all devices. For more information on using the AndroidX Preference Library see [Settings](https://developer.android.com/guide/topics/ui/settings.html).

A Preference that allows the user to choose a ringtone from those on the device. The chosen ringtone's URI will be persisted as a string.

If the user chooses the "Default" item, the saved string will be one of `https://developer.android.com/reference/kotlin/android/provider/Settings.System.html#DEFAULT_RINGTONE_URI:android.net.Uri`, `https://developer.android.com/reference/kotlin/android/provider/Settings.System.html#DEFAULT_NOTIFICATION_URI:android.net.Uri`, or `https://developer.android.com/reference/kotlin/android/provider/Settings.System.html#DEFAULT_ALARM_ALERT_URI:android.net.Uri`. If the user chooses the "Silent" item, the saved string will be an empty string.

## Summary

| XML attributes ||
|---|---|
| [`android:ringtoneType`](RingtonePreference.md) | Which ringtone type(s) to show in the picker. |
| [`android:showDefault`](RingtonePreference.md) | Whether to show an item for a default sound. |
| [`android:showSilent`](RingtonePreference.md) | Whether to show an item for 'Silent'. |
| --- | --- |

| Inherited XML attributes ||
|---|---|
| From class Preference |---|---| | attr_Preference | The default value for the preference, which will be set either if persistence is off or persistence is on and the preference is not found in the persistent storage. May be a reference to another resource, in the form "`@[+][package:]type/name`" or a theme attribute in the form "`?[package:]type/name`". May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character; May be an integer value, such as "`100`". May be a boolean value, such as "`true`" or "`false`". May be a floating point value, such as "`1.2`". <br /> | | attr_Preference | The key of another Preference that this Preference will depend on. If the other Preference is not set or is off, this Preference will be disabled. May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character; <br /> | | attr_Preference | Whether the Preference is enabled. May be a boolean value, such as "`true`" or "`false`". <br /> | | attr_Preference | When used inside of a modern PreferenceActivity, this declares a new PreferenceFragment to be shown when the user selects this item. May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character; <br /> | | attr_Preference | The optional icon for the preference. May be a reference to another resource, in the form "`@[+][package:]type/name`" or a theme attribute in the form "`?[package:]type/name`". <br /> | | attr_Preference | Whether the space for the preference icon view will be reserved. By default, preference icon view visibility will be set to GONE when there is no icon provided, so the default value of this attribute is false. May be a boolean value, such as "`true`" or "`false`". <br /> | | attr_Preference | The key to store the Preference value. May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character; <br /> | | attr_Preference | The layout for the Preference in a PreferenceActivity screen. This should rarely need to be changed, look at widgetLayout instead. May be a reference to another resource, in the form "`@[+][package:]type/name`" or a theme attribute in the form "`?[package:]type/name`". <br /> | | attr_Preference | The order for the Preference (lower values are to be ordered first). If this is not specified, the default ordering will be alphabetic. May be an integer value, such as "`100`". <br /> | | attr_Preference | Whether the Preference stores its value to the storage. May be a boolean value, such as "`true`" or "`false`". <br /> | | attr_Preference | Whether the preference has enabled to have its view recycled when used in the list view. This is true by default. May be a boolean value, such as "`true`" or "`false`". <br /> | | attr_Preference | Whether the Preference is selectable. May be a boolean value, such as "`true`" or "`false`". <br /> | | attr_Preference | Whether the view of this Preference should be disabled when this Preference is disabled. May be a boolean value, such as "`true`" or "`false`". <br /> | | attr_Preference | Whether to use single line for the preference title text. By default, preference title will be constrained to one line, so the default value of this attribute is true. May be a boolean value, such as "`true`" or "`false`". <br /> | | attr_Preference | The summary for the Preference. In API 25 and earlier, this value is read as a plain string with styling information stripped. May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character; <br /> | | attr_Preference | The title for the Preference. In API 25 and earlier, this value is read as a plain string with styling information stripped. May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character; <br /> | | attr_Preference | The layout for the controllable widget portion of a Preference. This is inflated into the layout for a Preference and should be used more frequently than the layout attribute. For example, a checkbox preference would specify a custom layout (consisting of just the CheckBox) here. May be a reference to another resource, in the form "`@[+][package:]type/name`" or a theme attribute in the form "`?[package:]type/name`". <br /> | ||

| Inherited constants ||
|---|---|
| From class Preference |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/preference/Preference#DEFAULT_ORDER:kotlin.Int` Specify for setOrder if a specific order is not required. <br /> | ||

| Public constructors ||
|---|---|
| RingtonePreference <br /> |
| RingtonePreference <br /> |
| RingtonePreference <br /> |
| RingtonePreference <br /> |

| Public methods ||
|---|---|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getRingtoneType Returns the sound type(s) that are shown in the picker. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | getShowDefault Returns whether to a show an item for the default sound/ringtone. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | getShowSilent Returns whether to a show an item for 'Silent'. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | onActivityResult See Activity's onActivityResult. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setRingtoneType Sets the sound type(s) that are shown in the picker. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setShowDefault Sets whether to show an item for the default sound/ringtone. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setShowSilent Sets whether to show an item for 'Silent'. |

| Protected methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onAttachedToHierarchy Called when this Preference has been attached to a Preference hierarchy. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onClick Processes a click on the preference. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | onGetDefaultValue Called when a Preference is being inflated and the default value attribute needs to be read. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onPrepareRingtonePickerIntent Prepares the intent to launch the ringtone picker. |
| open [Uri](../android.net/Uri.md)! | onRestoreRingtone Called when the chooser is about to be shown and the current ringtone should be marked. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onSaveRingtone Called when a ringtone is chosen. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onSetInitialValue Implement this to set the initial value of the Preference. |

| Inherited functions ||
|---|---|
| From class Preference |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | callChangeListener Call this method after the user changes the preference, but before the internal state is set. This allows the client to ignore the user value. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | compareTo Compares Preference objects based on order (if set), otherwise alphabetically on the titles. <br /> | | `https://developer.android.com/reference/kotlin/android/preference/Preference!` | findPreferenceInHierarchy Finds a Preference in this hierarchy (the whole thing, even above/below your PreferenceScreen screen break) with the given key. This only functions after we have been attached to a hierarchy. <br /> | | `https://developer.android.com/reference/kotlin/android/content/Context.html#!` | getContext Returns the `https://developer.android.com/reference/kotlin/android/content/Context.html#` of this Preference. Each Preference in a Preference hierarchy can be from different Context (for example, if multiple activities provide preferences into a single PreferenceActivity). This Context will be used to save the Preference values. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | getDependency Returns the key of the dependency on this Preference. <br /> | | `https://developer.android.com/reference/kotlin/android/content/SharedPreferences.Editor.html#!` | getEditor Returns an `https://developer.android.com/reference/kotlin/android/content/SharedPreferences.Editor.html#` where this Preference can save its value(s). Usually it's easier to use one of the helper save methods: persistBoolean, persistFloat, persistInt, persistLong, persistString. To read values, see getSharedPreferences. If shouldCommit returns true, it is this Preference's responsibility to commit. In some cases, writes to this will not be committed right away and hence not show up in the SharedPreferences, this is intended behavior to improve performance. <br /> | | `https://developer.android.com/reference/kotlin/android/os/Bundle.html#!` | getExtras Return the extras Bundle object associated with this preference, creating a new Bundle if there currently isn't one. You can use this to get and set individual extra key/value pairs. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | getFragment Return the fragment class name associated with this Preference. <br /> | | `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#!` | getIcon Returns the icon of this Preference. <br /> | | `https://developer.android.com/reference/kotlin/android/content/Intent.html#!` | getIntent Return the `https://developer.android.com/reference/kotlin/android/content/Intent.html#` associated with this Preference. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | getKey Gets the key for this Preference, which is also the key used for storing values into `https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#` or PreferenceDataStore. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getLayoutResource Gets the layout resource that will be shown as the `https://developer.android.com/reference/kotlin/android/view/View.html#` for this Preference. <br /> | | `https://developer.android.com/reference/kotlin/android/preference/Preference.OnPreferenceChangeListener!` | getOnPreferenceChangeListener Returns the callback to be invoked when this Preference is changed by the user (but before the internal state has been updated). <br /> | | `https://developer.android.com/reference/kotlin/android/preference/Preference.OnPreferenceClickListener!` | getOnPreferenceClickListener Returns the callback to be invoked when this Preference is clicked. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getOrder Gets the order of this Preference with respect to other Preference objects on the same level. <br /> | | PreferenceGroup | getParent Returns the PreferenceGroup which is this Preference assigned to or `null` if this preference is not assigned to any group or is a root Preference. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | getPersistedBoolean Attempts to get a persisted boolean if this Preference is persistent. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | getPersistedFloat Attempts to get a persisted float if this Preference is persistent. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getPersistedInt Attempts to get a persisted int if this Preference is persistent. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | getPersistedLong Attempts to get a persisted long if this Preference is persistent. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | getPersistedString Attempts to get a persisted String if this Preference is persistent. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!` | getPersistedStringSet Attempts to get a persisted set of Strings if this Preference is persistent. <br /> | | PreferenceDataStore | getPreferenceDataStore Returns PreferenceDataStore used by this Preference. Returns `null` if `https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#` is used instead. By default preferences always use `https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#`. To make this preference to use the PreferenceDataStore you need to assign your implementation to the Preference itself via setPreferenceDataStore or to its PreferenceManager via setPreferenceDataStore. <br /> | | `https://developer.android.com/reference/kotlin/android/preference/PreferenceManager!` | getPreferenceManager Gets the PreferenceManager that manages this Preference object's tree. <br /> | | `https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#!` | getSharedPreferences Returns the `https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#` where this Preference can read its value(s). Usually, it's easier to use one of the helper read methods: getPersistedBoolean, getPersistedFloat, getPersistedInt, getPersistedLong, getPersistedString. To save values, see getEditor. In some cases, writes to the getEditor will not be committed right away and hence not show up in the returned `https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#`, this is intended behavior to improve performance. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | getShouldDisableView Checks whether this Preference should disable its view when it's action is disabled. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!` | getSummary Returns the summary of this Preference. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!` | getTitle Returns the title of this Preference. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getTitleRes Returns the title resource ID of this Preference. If the title did not come from a resource, `0` is returned. <br /> | | `https://developer.android.com/reference/kotlin/android/view/View.html#!` | getView Gets the View that will be shown in the PreferenceActivity. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getWidgetLayoutResource Gets the layout resource for the controllable widget portion of this Preference. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | hasKey Checks whether this Preference has a valid key. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | isEnabled Checks whether this Preference should be enabled in the list. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | isIconSpaceReserved Gets whether the space this preference icon view is reserved. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | isPersistent Checks whether this Preference is persistent. If it is, it stores its value(s) into the persistent `https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#` storage by default or into PreferenceDataStore if assigned. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | isRecycleEnabled Checks whether this Preference has enabled to have its view recycled when used in the list view. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | isSelectable Checks whether this Preference should be selectable in the list. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | isSingleLineTitle Gets whether the title of this preference is constrained to a single line. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | notifyChanged Should be called when the data of this Preference has changed. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | notifyDependencyChange Notifies any listening dependents of a change that affects the dependency. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | notifyHierarchyChanged Should be called when a Preference has been added/removed from this group, or the ordering should be re-evaluated. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onAttachedToActivity Called when the Preference hierarchy has been attached to the PreferenceActivity. This can also be called when this Preference has been attached to a group that was already attached to the PreferenceActivity. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onBindView Binds the created View to the data for this Preference. This is a good place to grab references to custom Views in the layout and set properties on them. Make sure to call through to the superclass's implementation. If you override this method you *must* call through to the superclass implementation. <br /> | | `https://developer.android.com/reference/kotlin/android/view/View.html#!` | onCreateView Creates the View to be shown for this Preference in the PreferenceActivity. The default behavior is to inflate the main layout of this Preference (see setLayoutResource. If changing this behavior, please specify a `https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#` with ID `https://developer.android.com/reference/kotlin/android/R.id.html#widget_frame:kotlin.Int`. Make sure to call through to the superclass's implementation. If you override this method you *must* call through to the superclass implementation. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onDependencyChanged Called when the dependency changes. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onParentChanged Called when the implicit parent dependency changes. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onPrepareForRemoval Called when this Preference is being removed from the hierarchy. You should remove any references to this Preference that you know about. Make sure to call through to the superclass implementation. If you override this method you *must* call through to the superclass implementation. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onRestoreInstanceState Hook allowing a Preference to re-apply a representation of its internal state that had previously been generated by onSaveInstanceState. This function will never be called with a `null` state. <br /> | | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#!` | onSaveInstanceState Hook allowing a Preference to generate a representation of its internal state that can later be used to create a new instance with that same state. This state should only contain information that is not persistent or can be reconstructed later. <br /> | | `https://developer.android.com/reference/kotlin/android/os/Bundle.html#!` | peekExtras Return the extras Bundle object associated with this preference, returning `null` if there is not currently one. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | persistBoolean Attempts to persist a boolean if this Preference is persistent. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | persistFloat Attempts to persist a long if this Preference is persistent. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | persistInt Attempts to persist an int if this Preference is persistent. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | persistLong Attempts to persist a long if this Preference is persistent. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | persistString Attempts to persist a String if this Preference is persistent. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | persistStringSet Attempts to persist a set of Strings if this Preference is persistent. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | restoreHierarchyState Restore this Preference hierarchy's previously saved state from the given container. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | saveHierarchyState Store this Preference hierarchy's frozen state into the given container. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setDefaultValue Sets the default value for this Preference, which will be set either if persistence is off or persistence is on and the preference is not found in the persistent storage. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setDependency Sets the key of a Preference that this Preference will depend on. If that Preference is not set or is off, this Preference will be disabled. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setEnabled Sets whether this Preference is enabled. If disabled, it will not handle clicks. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setFragment Sets the class name of a fragment to be shown when this Preference is clicked. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setIcon Sets the icon for this Preference with a Drawable. This icon will be placed into the ID `https://developer.android.com/reference/kotlin/android/R.id.html#icon:kotlin.Int` within the View created by onCreateView. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setIcon Sets the icon for this Preference with a resource ID. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setIconSpaceReserved Sets whether to reserve the space of this Preference icon view when no icon is provided. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setIntent Sets an `https://developer.android.com/reference/kotlin/android/content/Intent.html#` to be used for startActivity when this Preference is clicked. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setKey Sets the key for this Preference, which is used as a key to the `https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#` or PreferenceDataStore. This should be unique for the package. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setLayoutResource Sets the layout resource that is inflated as the `https://developer.android.com/reference/kotlin/android/view/View.html#` to be shown for this Preference. In most cases, the default layout is sufficient for custom Preference objects and only the widget layout needs to be changed. This layout should contain a `https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#` with ID `https://developer.android.com/reference/kotlin/android/R.id.html#widget_frame:kotlin.Int` to be the parent of the specific widget for this Preference. It should similarly contain `https://developer.android.com/reference/kotlin/android/R.id.html#title:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/R.id.html#summary:kotlin.Int`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setOnPreferenceChangeListener Sets the callback to be invoked when this Preference is changed by the user (but before the internal state has been updated). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setOnPreferenceClickListener Sets the callback to be invoked when this Preference is clicked. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setOrder Sets the order of this Preference with respect to other Preference objects on the same level. If this is not specified, the default behavior is to sort alphabetically. The setOrderingAsAdded can be used to order Preference objects based on the order they appear in the XML. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setPersistent Sets whether this Preference is persistent. When persistent, it stores its value(s) into the persistent `https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#` storage by default or into PreferenceDataStore if assigned. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setPreferenceDataStore Sets a PreferenceDataStore to be used by this Preference instead of using `https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#`. The data store will remain assigned even if the Preference is moved around the preference hierarchy. It will also override a data store propagated from the PreferenceManager that owns this Preference. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setRecycleEnabled Sets whether this Preference has enabled to have its view recycled when used in the list view. By default the recycling is enabled. The value can be changed only before this preference is added to the preference hierarchy. If view recycling is not allowed then each time the list view populates this preference the getView method receives a `null` convert view and needs to recreate the view. Otherwise view gets recycled and only onBindView gets called. If you override this method you *must* call through to the superclass implementation. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setSelectable Sets whether this Preference is selectable. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setShouldDisableView Sets whether this Preference should disable its view when it gets disabled. For example, set this and setEnabled to false for preferences that are only displaying information and 1) should not be clickable 2) should not have the view set to the disabled state. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setSingleLineTitle Sets whether to constrain the title of this Preference to a single line instead of letting it wrap onto multiple lines. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setSummary Sets the summary for this Preference with a resource ID. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setSummary Sets the summary for this Preference with a CharSequence. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setTitle Sets the title for this Preference with a resource ID. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setTitle Sets the title for this Preference with a CharSequence. This title will be placed into the ID `https://developer.android.com/reference/kotlin/android/R.id.html#title:kotlin.Int` within the View created by onCreateView. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setWidgetLayoutResource Sets the layout for the controllable widget portion of this Preference. This is inflated into the main layout. For example, a CheckBoxPreference would specify a custom layout (consisting of just the CheckBox) here, instead of creating its own main layout. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | shouldCommit Returns whether the Preference should commit its saved value(s) in getEditor. This may return false in situations where batch committing is being done (by the manager) to improve performance. If this preference is using PreferenceDataStore this value is irrelevant. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | shouldDisableDependents Checks whether this preference's dependents should currently be disabled. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | shouldPersist Checks whether, at the given time this method is called, this Preference should store/restore its value(s) into the `https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#` or into PreferenceDataStore if assigned. This, at minimum, checks whether this Preference is persistent and it currently has a key. Before you save/restore from the storage, check this first. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | toString Returns a string representation of the object. <br /> | ||

## XML attributes

### android:ringtoneType

```
android:ringtoneType
```
Which ringtone type(s) to show in the picker.

Must be one or more (separated by '|') of the following constant values.
| --- | --- |

| Constant | Value | Description |
|---|---|---|
| alarm | 4 | Alarm sounds. |
| all | 7 | All available ringtone sounds. |
| notification | 2 | Notification sounds. |
| --- | --- | --- |
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

- setRingtoneType

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
| `preferenceManager` | [PreferenceManager](PreferenceManager.md)!: The PreferenceManager of the hierarchy. |

### onClick

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun onClick(): Unit
```

**Deprecated:** *Deprecated in Java.*

Processes a click on the preference. This includes saving the value to the `https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#`. However, the overridden method should call callChangeListener to make sure the client wants to update the preference's state with the new value.

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

For example, if the value type is String, the body of the method would proxy to getString.

| Parameters ||
|---|---|
| `a` | [TypedArray](../android.content.res/TypedArray.md)!: The set of attributes. |
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
| `ringtonePickerIntent` | [Intent](../android.content/Intent.md)!: The ringtone picker intent that can be modified by putting extras. |

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
| `ringtoneUri` | [Uri](../android.net/Uri.md)!: The chosen ringtone's `https://developer.android.com/reference/kotlin/android/net/Uri.html#`. Can be null. |

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

If restorePersistedValue is true, you should restore the Preference value from the `https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#`. If restorePersistedValue is false, you should set the Preference value to defaultValue that is given (and possibly store to SharedPreferences if shouldPersist is true).

In case of using PreferenceDataStore, the restorePersistedValue is always `true`. But the default value (if provided) is set.

This may not always be called. One example is if it should not persist but there is no default value given.

| Parameters ||
|---|---|
| `restorePersistedValue` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): True to restore the persisted value; false to use the given defaultValue. |
| `defaultValue` | The default value for this Preference. Only use this if restorePersistedValue is false. |
