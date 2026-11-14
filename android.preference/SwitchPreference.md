# SwitchPreference

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SwitchPreference

Kotlin | [Java](SwitchPreference.md) 
| --- | --- |

```
open class SwitchPreference : TwoStatePreference
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [android.preference.Preference](Preference.md) |||
| | ↳ | [android.preference.TwoStatePreference](TwoStatePreference.md) ||
| | | ↳ | [android.preference.SwitchPreference](SwitchPreference.md) |
| --- | --- | --- | --- |

| **This class was deprecated in API level 29.**
|
| Use the [AndroidX](https://developer.android.com/jetpack/androidx.html) [Preference Library](../androidx/preference/_package.md) for consistent behavior across all devices. For more information on using the AndroidX Preference Library see [Settings](https://developer.android.com/guide/topics/ui/settings.html).

A [Preference](Preference.md) that provides a two-state toggleable option.

This preference will store a boolean into the SharedPreferences.

## Summary

| XML attributes ||
|----------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [`android:disableDependentsState`](SwitchPreference.md) | The state (true for on, or false for off) that causes dependents to be disabled. |
| [`android:summaryOff`](SwitchPreference.md) | The summary for the Preference in a PreferenceActivity screen when the SwitchPreference is unchecked. |
| [`android:summaryOn`](SwitchPreference.md) | The summary for the Preference in a PreferenceActivity screen when the SwitchPreference is checked. |
| --- | --- |
| [`android:switchTextOff`](SwitchPreference.md) | The text used on the switch itself when in the "off" state. |
| [`android:switchTextOn`](SwitchPreference.md) | The text used on the switch itself when in the "on" state. |

| Inherited XML attributes ||
|---|---|
| From class [Preference](Preference.md) |---------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [android:defaultValue](Preference.md) | The default value for the preference, which will be set either if persistence is off or persistence is on and the preference is not found in the persistent storage. May be a reference to another resource, in the form "`@[+][`*package* `:]`*type* `/`*name*" or a theme attribute in the form "`?[`*package* `:]`*type* `/`*name*". May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character; May be an integer value, such as "`100`". May be a boolean value, such as "`true`" or "`false`". May be a floating point value, such as "`1.2`". <br /> | | [android:dependency](Preference.md) | The key of another Preference that this Preference will depend on. If the other Preference is not set or is off, this Preference will be disabled. May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character; <br /> | | [android:enabled](Preference.md) | Whether the Preference is enabled. May be a boolean value, such as "`true`" or "`false`". <br /> | | [android:fragment](Preference.md) | When used inside of a modern PreferenceActivity, this declares a new PreferenceFragment to be shown when the user selects this item. May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character; <br /> | | [android:icon](Preference.md) | The optional icon for the preference. May be a reference to another resource, in the form "`@[+][`*package* `:]`*type* `/`*name*" or a theme attribute in the form "`?[`*package* `:]`*type* `/`*name*". <br /> | | [android:iconSpaceReserved](Preference.md) | Whether the space for the preference icon view will be reserved. By default, preference icon view visibility will be set to GONE when there is no icon provided, so the default value of this attribute is false. May be a boolean value, such as "`true`" or "`false`". <br /> | | [android:key](Preference.md) | The key to store the Preference value. May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character; <br /> | | [android:layout](Preference.md) | The layout for the Preference in a PreferenceActivity screen. This should rarely need to be changed, look at widgetLayout instead. May be a reference to another resource, in the form "`@[+][`*package* `:]`*type* `/`*name*" or a theme attribute in the form "`?[`*package* `:]`*type* `/`*name*". <br /> | | [android:order](Preference.md) | The order for the Preference (lower values are to be ordered first). If this is not specified, the default ordering will be alphabetic. May be an integer value, such as "`100`". <br /> | | [android:persistent](Preference.md) | Whether the Preference stores its value to the storage. May be a boolean value, such as "`true`" or "`false`". <br /> | | [android:recycleEnabled](Preference.md) | Whether the preference has enabled to have its view recycled when used in the list view. This is true by default. May be a boolean value, such as "`true`" or "`false`". <br /> | | [android:selectable](Preference.md) | Whether the Preference is selectable. May be a boolean value, such as "`true`" or "`false`". <br /> | | [android:shouldDisableView](Preference.md) | Whether the view of this Preference should be disabled when this Preference is disabled. May be a boolean value, such as "`true`" or "`false`". <br /> | | [android:singleLineTitle](Preference.md) | Whether to use single line for the preference title text. By default, preference title will be constrained to one line, so the default value of this attribute is true. May be a boolean value, such as "`true`" or "`false`". <br /> | | [android:summary](Preference.md) | The summary for the Preference. In API 25 and earlier, this value is read as a plain string with styling information stripped. May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character; <br /> | | [android:title](Preference.md) | The title for the Preference. In API 25 and earlier, this value is read as a plain string with styling information stripped. May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character; <br /> | | [android:widgetLayout](Preference.md) | The layout for the controllable widget portion of a Preference. This is inflated into the layout for a Preference and should be used more frequently than the layout attribute. For example, a checkbox preference would specify a custom layout (consisting of just the CheckBox) here. May be a reference to another resource, in the form "`@[+][`*package* `:]`*type* `/`*name*" or a theme attribute in the form "`?[`*package* `:]`*type* `/`*name*". <br /> | ||

| Inherited constants ||
|---|---|
| From class [Preference](Preference.md) |----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEFAULT_ORDER](Preference.md) Specify for [setOrder(int)](Preference.md)) if a specific order is not required. <br /> | ||

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SwitchPreference](SwitchPreference.md))`(`context:` ` [Context](../android.content/Context.md)!`)` Construct a new SwitchPreference with default style options. |
| [SwitchPreference](SwitchPreference.md))`(`context:` ` [Context](../android.content/Context.md)!`, `attrs:` ` [AttributeSet](../android.util/AttributeSet.md)!`)` Construct a new SwitchPreference with the given style options. |
| [SwitchPreference](SwitchPreference.md))`(`context:` ` [Context](../android.content/Context.md)!`, `attrs:` ` [AttributeSet](../android.util/AttributeSet.md)!`, `defStyleAttr:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Construct a new SwitchPreference with the given style options. |
| [SwitchPreference](SwitchPreference.md))`(`context:` ` [Context](../android.content/Context.md)!`, `attrs:` ` [AttributeSet](../android.util/AttributeSet.md)!`, `defStyleAttr:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `defStyleRes:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Construct a new SwitchPreference with the given style options. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [getSwitchTextOff](SwitchPreference.md))`()` <br /> |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [getSwitchTextOn](SwitchPreference.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSwitchTextOff](SwitchPreference.md))`(`resId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the text displayed on the switch widget in the off state. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSwitchTextOff](SwitchPreference.md))`(`offText:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Set the text displayed on the switch widget in the off state. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSwitchTextOn](SwitchPreference.md))`(`resId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the text displayed on the switch widget in the on state. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSwitchTextOn](SwitchPreference.md))`(`onText:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Set the text displayed on the switch widget in the on state. |
| --- | --- |

| Protected methods ||
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onBindView](SwitchPreference.md))`(`view:` ` [View](../android.view/View.md)!`)` <br /> |

| Inherited functions ||
|---|---|
| From class [Preference](Preference.md) |-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [callChangeListener](Preference.md))`(`newValue:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Call this method after the user changes the preference, but before the internal state is set. This allows the client to ignore the user value. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compareTo](Preference.md))`(`other:` ` [Preference](Preference.md)!`)` Compares Preference objects based on order (if set), otherwise alphabetically on the titles. <br /> | | [Preference](Preference.md)! | [findPreferenceInHierarchy](Preference.md))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Finds a Preference in this hierarchy (the whole thing, even above/below your [PreferenceScreen](PreferenceScreen.md) screen break) with the given key. This only functions after we have been attached to a hierarchy. <br /> | | [Context](../android.content/Context.md)! | [getContext](Preference.md))`()` Returns the [android.content.Context](../android.content/Context.md) of this Preference. Each Preference in a Preference hierarchy can be from different Context (for example, if multiple activities provide preferences into a single [PreferenceActivity](PreferenceActivity.md)). This Context will be used to save the Preference values. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDependency](Preference.md))`()` Returns the key of the dependency on this Preference. <br /> | | [SharedPreferences.Editor](../android/content/SharedPreferences.Editor.md)! | [getEditor](Preference.md))`()` Returns an [SharedPreferences.Editor](../android/content/SharedPreferences.Editor.md) where this Preference can save its value(s). Usually it's easier to use one of the helper save methods: [persistBoolean(boolean)](Preference.md)), [persistFloat(float)](Preference.md)), [persistInt(int)](Preference.md)), [persistLong(long)](Preference.md)), [persistString(java.lang.String)](Preference.md)). To read values, see [getSharedPreferences()](Preference.md)). If [shouldCommit()](Preference.md)) returns true, it is this Preference's responsibility to commit. In some cases, writes to this will not be committed right away and hence not show up in the SharedPreferences, this is intended behavior to improve performance. <br /> | | [Bundle](../android.os/Bundle.md)! | [getExtras](Preference.md))`()` Return the extras Bundle object associated with this preference, creating a new Bundle if there currently isn't one. You can use this to get and set individual extra key/value pairs. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getFragment](Preference.md))`()` Return the fragment class name associated with this Preference. <br /> | | [Drawable](../android.graphics.drawable/Drawable.md)! | [getIcon](Preference.md))`()` Returns the icon of this Preference. <br /> | | [Intent](../android.content/Intent.md)! | [getIntent](Preference.md))`()` Return the [Intent](../android.content/Intent.md) associated with this Preference. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getKey](Preference.md))`()` Gets the key for this Preference, which is also the key used for storing values into [SharedPreferences](../android.content/SharedPreferences.md) or [PreferenceDataStore](PreferenceDataStore.md). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLayoutResource](Preference.md))`()` Gets the layout resource that will be shown as the [View](../android.view/View.md) for this Preference. <br /> | | [Preference.OnPreferenceChangeListener](../android/preference/Preference.OnPreferenceChangeListener.md)! | [getOnPreferenceChangeListener](Preference.md))`()` Returns the callback to be invoked when this Preference is changed by the user (but before the internal state has been updated). <br /> | | [Preference.OnPreferenceClickListener](../android/preference/Preference.OnPreferenceClickListener.md)! | [getOnPreferenceClickListener](Preference.md))`()` Returns the callback to be invoked when this Preference is clicked. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOrder](Preference.md))`()` Gets the order of this Preference with respect to other Preference objects on the same level. <br /> | | [PreferenceGroup](PreferenceGroup.md)? | [getParent](Preference.md))`()` Returns the [PreferenceGroup](PreferenceGroup.md) which is this Preference assigned to or `null` if this preference is not assigned to any group or is a root Preference. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getPersistedBoolean](Preference.md))`(`defaultReturnValue:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Attempts to get a persisted boolean if this Preference is persistent. <br /> | | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getPersistedFloat](Preference.md))`(`defaultReturnValue:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Attempts to get a persisted float if this Preference is persistent. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPersistedInt](Preference.md))`(`defaultReturnValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Attempts to get a persisted int if this Preference is persistent. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getPersistedLong](Preference.md))`(`defaultReturnValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Attempts to get a persisted long if this Preference is persistent. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getPersistedString](Preference.md))`(`defaultReturnValue:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Attempts to get a persisted String if this Preference is persistent. <br /> | | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | [getPersistedStringSet](Preference.md))`(`defaultReturnValue:` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Attempts to get a persisted set of Strings if this Preference is persistent. <br /> | | [PreferenceDataStore](PreferenceDataStore.md)? | [getPreferenceDataStore](Preference.md))`()` Returns [PreferenceDataStore](PreferenceDataStore.md) used by this Preference. Returns `null` if [android.content.SharedPreferences](../android.content/SharedPreferences.md) is used instead. By default preferences always use [android.content.SharedPreferences](../android.content/SharedPreferences.md). To make this preference to use the [PreferenceDataStore](PreferenceDataStore.md) you need to assign your implementation to the Preference itself via [setPreferenceDataStore(android.preference.PreferenceDataStore)](Preference.md)) or to its [PreferenceManager](PreferenceManager.md) via [PreferenceManager.setPreferenceDataStore(PreferenceDataStore)](PreferenceManager.md)). <br /> | | [PreferenceManager](PreferenceManager.md)! | [getPreferenceManager](Preference.md))`()` Gets the [PreferenceManager](PreferenceManager.md) that manages this Preference object's tree. <br /> | | [SharedPreferences](../android.content/SharedPreferences.md)! | [getSharedPreferences](Preference.md))`()` Returns the [SharedPreferences](../android.content/SharedPreferences.md) where this Preference can read its value(s). Usually, it's easier to use one of the helper read methods: [getPersistedBoolean(boolean)](Preference.md)), [getPersistedFloat(float)](Preference.md)), [getPersistedInt(int)](Preference.md)), [getPersistedLong(long)](Preference.md)), [getPersistedString(java.lang.String)](Preference.md)). To save values, see [getEditor()](Preference.md)). In some cases, writes to the [getEditor()](Preference.md)) will not be committed right away and hence not show up in the returned [SharedPreferences](../android.content/SharedPreferences.md), this is intended behavior to improve performance. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getShouldDisableView](Preference.md))`()` Checks whether this Preference should disable its view when it's action is disabled. <br /> | | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [getSummary](Preference.md))`()` Returns the summary of this Preference. <br /> | | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [getTitle](Preference.md))`()` Returns the title of this Preference. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTitleRes](Preference.md))`()` Returns the title resource ID of this Preference. If the title did not come from a resource, `0` is returned. <br /> | | [View](../android.view/View.md)! | [getView](Preference.md))`(`convertView:` ` [View](../android.view/View.md)!`, `parent:` ` [ViewGroup](../android.view/ViewGroup.md)!`)` Gets the View that will be shown in the [PreferenceActivity](PreferenceActivity.md). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getWidgetLayoutResource](Preference.md))`()` Gets the layout resource for the controllable widget portion of this Preference. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasKey](Preference.md))`()` Checks whether this Preference has a valid key. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEnabled](Preference.md))`()` Checks whether this Preference should be enabled in the list. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isIconSpaceReserved](Preference.md))`()` Gets whether the space this preference icon view is reserved. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPersistent](Preference.md))`()` Checks whether this Preference is persistent. If it is, it stores its value(s) into the persistent [SharedPreferences](../android.content/SharedPreferences.md) storage by default or into [PreferenceDataStore](PreferenceDataStore.md) if assigned. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRecycleEnabled](Preference.md))`()` Checks whether this Preference has enabled to have its view recycled when used in the list view. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSelectable](Preference.md))`()` Checks whether this Preference should be selectable in the list. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSingleLineTitle](Preference.md))`()` Gets whether the title of this preference is constrained to a single line. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyChanged](Preference.md))`()` Should be called when the data of this [Preference](Preference.md) has changed. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyDependencyChange](Preference.md))`(`disableDependents:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Notifies any listening dependents of a change that affects the dependency. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyHierarchyChanged](Preference.md))`()` Should be called when a Preference has been added/removed from this group, or the ordering should be re-evaluated. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAttachedToActivity](Preference.md))`()` Called when the Preference hierarchy has been attached to the [PreferenceActivity](PreferenceActivity.md). This can also be called when this Preference has been attached to a group that was already attached to the [PreferenceActivity](PreferenceActivity.md). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAttachedToHierarchy](Preference.md))`(`preferenceManager:` ` [PreferenceManager](PreferenceManager.md)!`)` Called when this Preference has been attached to a Preference hierarchy. Make sure to call the super implementation. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onBindView](Preference.md))`(`view:` ` [View](../android.view/View.md)!`)` Binds the created View to the data for this Preference. This is a good place to grab references to custom Views in the layout and set properties on them. Make sure to call through to the superclass's implementation. If you override this method you *must* call through to the superclass implementation. <br /> | | [View](../android.view/View.md)! | [onCreateView](Preference.md))`(`parent:` ` [ViewGroup](../android.view/ViewGroup.md)!`)` Creates the View to be shown for this Preference in the [PreferenceActivity](PreferenceActivity.md). The default behavior is to inflate the main layout of this Preference (see [setLayoutResource(int)](Preference.md)). If changing this behavior, please specify a [ViewGroup](../android.view/ViewGroup.md) with ID [android.R.id#widget_frame](../android/R.id.md). Make sure to call through to the superclass's implementation. If you override this method you *must* call through to the superclass implementation. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDependencyChanged](Preference.md))`(`dependency:` ` [Preference](Preference.md)!`, `disableDependent:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Called when the dependency changes. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onParentChanged](Preference.md))`(`parent:` ` [Preference](Preference.md)!`, `disableChild:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Called when the implicit parent dependency changes. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPrepareForRemoval](Preference.md))`()` Called when this Preference is being removed from the hierarchy. You should remove any references to this Preference that you know about. Make sure to call through to the superclass implementation. If you override this method you *must* call through to the superclass implementation. <br /> | | [Bundle](../android.os/Bundle.md)! | [peekExtras](Preference.md))`()` Return the extras Bundle object associated with this preference, returning `null` if there is not currently one. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [persistBoolean](Preference.md))`(`value:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Attempts to persist a boolean if this Preference is persistent. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [persistFloat](Preference.md))`(`value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Attempts to persist a long if this Preference is persistent. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [persistInt](Preference.md))`(`value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Attempts to persist an int if this Preference is persistent. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [persistLong](Preference.md))`(`value:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Attempts to persist a long if this Preference is persistent. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [persistString](Preference.md))`(`value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Attempts to persist a String if this Preference is persistent. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [persistStringSet](Preference.md))`(`values:` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Attempts to persist a set of Strings if this Preference is persistent. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [restoreHierarchyState](Preference.md))`(`container:` ` [Bundle](../android.os/Bundle.md)!`)` Restore this Preference hierarchy's previously saved state from the given container. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [saveHierarchyState](Preference.md))`(`container:` ` [Bundle](../android.os/Bundle.md)!`)` Store this Preference hierarchy's frozen state into the given container. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDefaultValue](Preference.md))`(`defaultValue:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Sets the default value for this Preference, which will be set either if persistence is off or persistence is on and the preference is not found in the persistent storage. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDependency](Preference.md))`(`dependencyKey:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the key of a Preference that this Preference will depend on. If that Preference is not set or is off, this Preference will be disabled. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEnabled](Preference.md))`(`enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether this Preference is enabled. If disabled, it will not handle clicks. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFragment](Preference.md))`(`fragment:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the class name of a fragment to be shown when this Preference is clicked. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setIcon](Preference.md))`(`icon:` ` [Drawable](../android.graphics.drawable/Drawable.md)!`)` Sets the icon for this Preference with a Drawable. This icon will be placed into the ID [android.R.id#icon](../android/R.id.md) within the View created by [onCreateView(android.view.ViewGroup)](Preference.md)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setIcon](Preference.md))`(`iconResId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the icon for this Preference with a resource ID. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setIconSpaceReserved](Preference.md))`(`iconSpaceReserved:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether to reserve the space of this Preference icon view when no icon is provided. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setIntent](Preference.md))`(`intent:` ` [Intent](../android.content/Intent.md)!`)` Sets an [Intent](../android.content/Intent.md) to be used for [Context.startActivity(Intent)](../android.content/Context.md)) when this Preference is clicked. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setKey](Preference.md))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the key for this Preference, which is used as a key to the [SharedPreferences](../android.content/SharedPreferences.md) or [PreferenceDataStore](PreferenceDataStore.md). This should be unique for the package. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLayoutResource](Preference.md))`(`layoutResId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the layout resource that is inflated as the [View](../android.view/View.md) to be shown for this Preference. In most cases, the default layout is sufficient for custom Preference objects and only the widget layout needs to be changed. This layout should contain a [ViewGroup](../android.view/ViewGroup.md) with ID [android.R.id#widget_frame](../android/R.id.md) to be the parent of the specific widget for this Preference. It should similarly contain [android.R.id#title](../android/R.id.md) and [android.R.id#summary](../android/R.id.md). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnPreferenceChangeListener](Preference.md))`(`onPreferenceChangeListener:` ` [Preference.OnPreferenceChangeListener](../android/preference/Preference.OnPreferenceChangeListener.md)!`)` Sets the callback to be invoked when this Preference is changed by the user (but before the internal state has been updated). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnPreferenceClickListener](Preference.md))`(`onPreferenceClickListener:` ` [Preference.OnPreferenceClickListener](../android/preference/Preference.OnPreferenceClickListener.md)!`)` Sets the callback to be invoked when this Preference is clicked. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOrder](Preference.md))`(`order:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the order of this Preference with respect to other Preference objects on the same level. If this is not specified, the default behavior is to sort alphabetically. The [PreferenceGroup.setOrderingAsAdded(boolean)](PreferenceGroup.md)) can be used to order Preference objects based on the order they appear in the XML. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPersistent](Preference.md))`(`persistent:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether this Preference is persistent. When persistent, it stores its value(s) into the persistent [SharedPreferences](../android.content/SharedPreferences.md) storage by default or into [PreferenceDataStore](PreferenceDataStore.md) if assigned. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPreferenceDataStore](Preference.md))`(`dataStore:` ` [PreferenceDataStore](PreferenceDataStore.md)!`)` Sets a [PreferenceDataStore](PreferenceDataStore.md) to be used by this Preference instead of using [android.content.SharedPreferences](../android.content/SharedPreferences.md). The data store will remain assigned even if the Preference is moved around the preference hierarchy. It will also override a data store propagated from the [PreferenceManager](PreferenceManager.md) that owns this Preference. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRecycleEnabled](Preference.md))`(`enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether this Preference has enabled to have its view recycled when used in the list view. By default the recycling is enabled. The value can be changed only before this preference is added to the preference hierarchy. If view recycling is not allowed then each time the list view populates this preference the [getView(android.view.View,android.view.ViewGroup)](Preference.md)) method receives a `null` convert view and needs to recreate the view. Otherwise view gets recycled and only [onBindView(android.view.View)](Preference.md)) gets called. If you override this method you *must* call through to the superclass implementation. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSelectable](Preference.md))`(`selectable:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether this Preference is selectable. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setShouldDisableView](Preference.md))`(`shouldDisableView:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether this Preference should disable its view when it gets disabled. For example, set this and [setEnabled(boolean)](Preference.md)) to false for preferences that are only displaying information and 1) should not be clickable 2) should not have the view set to the disabled state. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSingleLineTitle](Preference.md))`(`singleLineTitle:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether to constrain the title of this Preference to a single line instead of letting it wrap onto multiple lines. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSummary](Preference.md))`(`summaryResId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the summary for this Preference with a resource ID. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSummary](Preference.md))`(`summary:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Sets the summary for this Preference with a CharSequence. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTitle](Preference.md))`(`titleResId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the title for this Preference with a resource ID. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTitle](Preference.md))`(`title:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Sets the title for this Preference with a CharSequence. This title will be placed into the ID [android.R.id#title](../android/R.id.md) within the View created by [onCreateView(android.view.ViewGroup)](Preference.md)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setWidgetLayoutResource](Preference.md))`(`widgetLayoutResId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the layout for the controllable widget portion of this Preference. This is inflated into the main layout. For example, a [CheckBoxPreference](CheckBoxPreference.md) would specify a custom layout (consisting of just the CheckBox) here, instead of creating its own main layout. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [shouldCommit](Preference.md))`()` Returns whether the [Preference](Preference.md) should commit its saved value(s) in [getEditor()](Preference.md)). This may return false in situations where batch committing is being done (by the manager) to improve performance. If this preference is using [PreferenceDataStore](PreferenceDataStore.md) this value is irrelevant. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [shouldPersist](Preference.md))`()` Checks whether, at the given time this method is called, this Preference should store/restore its value(s) into the [SharedPreferences](../android.content/SharedPreferences.md) or into [PreferenceDataStore](PreferenceDataStore.md) if assigned. This, at minimum, checks whether this Preference is persistent and it currently has a key. Before you save/restore from the storage, check this first. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](Preference.md))`()` <br /> | ||
| From class [TwoStatePreference](TwoStatePreference.md) |------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getDisableDependentsState](TwoStatePreference.md))`()` Returns whether dependents are disabled when this preference is on (`true`) or when this preference is off (`false`). <br /> | | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [getSummaryOff](TwoStatePreference.md))`()` Returns the summary to be shown when unchecked. <br /> | | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [getSummaryOn](TwoStatePreference.md))`()` Returns the summary to be shown when checked. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isChecked](TwoStatePreference.md))`()` Returns the checked state. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onClick](TwoStatePreference.md))`()` <br /> | | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [onGetDefaultValue](TwoStatePreference.md))`(`a:` ` [TypedArray](../android.content.res/TypedArray.md)!`, `index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onRestoreInstanceState](TwoStatePreference.md))`(`state:` ` [Parcelable](../android.os/Parcelable.md)!`)` <br /> | | [Parcelable](../android.os/Parcelable.md)! | [onSaveInstanceState](TwoStatePreference.md))`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSetInitialValue](TwoStatePreference.md))`(`restoreValue:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `defaultValue:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setChecked](TwoStatePreference.md))`(`checked:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets the checked state and saves it to the [SharedPreferences](../android.content/SharedPreferences.md). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDisableDependentsState](TwoStatePreference.md))`(`disableDependentsState:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether dependents are disabled when this preference is on (`true`) or when this preference is off (`false`). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSummaryOff](TwoStatePreference.md))`(`summaryResId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSummaryOff](TwoStatePreference.md))`(`summary:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Sets the summary to be shown when unchecked. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSummaryOn](TwoStatePreference.md))`(`summaryResId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSummaryOn](TwoStatePreference.md))`(`summary:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Sets the summary to be shown when checked. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [shouldDisableDependents](TwoStatePreference.md))`()` <br /> | ||

## XML attributes

### android:disableDependentsState

```
android:disableDependentsState
```
The state (true for on, or false for off) that causes dependents to be disabled. By default, dependents will be disabled when this is unchecked, so the value of this preference is false.

May be a boolean value, such as "`true`" or "`false`". 

### android:summaryOff

```
android:summaryOff
```
The summary for the Preference in a PreferenceActivity screen when the SwitchPreference is unchecked. If separate on/off summaries are not needed, the summary attribute can be used instead.

May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character; 

### android:summaryOn

```
android:summaryOn
```
The summary for the Preference in a PreferenceActivity screen when the SwitchPreference is checked. If separate on/off summaries are not needed, the summary attribute can be used instead.

May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character; 

### android:switchTextOff

```
android:switchTextOff
```
The text used on the switch itself when in the "off" state. This should be a very SHORT string, as it appears in a small space.

May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character; 

### android:switchTextOn

```
android:switchTextOn
```
The text used on the switch itself when in the "on" state. This should be a very SHORT string, as it appears in a small space.

May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character;

## Public constructors

### SwitchPreference

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SwitchPreference(context: Context!)
```

Construct a new SwitchPreference with default style options.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android.content/Context.md)!: The Context that will style this preference |

### SwitchPreference

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SwitchPreference(
    context: Context!, 
    attrs: AttributeSet!)
```

Construct a new SwitchPreference with the given style options.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android.content/Context.md)!: The Context that will style this preference |
| `attrs` | [AttributeSet](../android.util/AttributeSet.md)!: Style attributes that differ from the default |

### SwitchPreference

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SwitchPreference(
    context: Context!, 
    attrs: AttributeSet!, 
    defStyleAttr: Int)
```

Construct a new SwitchPreference with the given style options.

| Parameters ||
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android.content/Context.md)!: The Context that will style this preference |
| `attrs` | [AttributeSet](../android.util/AttributeSet.md)!: Style attributes that differ from the default |
| `defStyleAttr` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): An attribute in the current theme that contains a reference to a style resource that supplies default values for the view. Can be 0 to not look for defaults. |
| --- | --- |

### SwitchPreference

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SwitchPreference(
    context: Context!, 
    attrs: AttributeSet!, 
    defStyleAttr: Int, 
    defStyleRes: Int)
```

Construct a new SwitchPreference with the given style options.

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android.content/Context.md)!: The Context that will style this preference |
| `attrs` | [AttributeSet](../android.util/AttributeSet.md)!: Style attributes that differ from the default |
| `defStyleAttr` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): An attribute in the current theme that contains a reference to a style resource that supplies default values for the view. Can be 0 to not look for defaults. |
| --- | --- |
| `defStyleRes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): A resource identifier of a style resource that supplies default values for the view, used only if defStyleAttr is 0 or can not be found in the theme. Can be 0 to not look for defaults. |

## Public methods

### getSwitchTextOff

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSwitchTextOff(): CharSequence!
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | The text that will be displayed on the switch widget in the off state |

### getSwitchTextOn

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSwitchTextOn(): CharSequence!
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | The text that will be displayed on the switch widget in the on state |

### setSwitchTextOff

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSwitchTextOff(resId: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Set the text displayed on the switch widget in the off state. This should be a very short string; one word if possible.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------|
| `resId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The text as a string resource ID |

### setSwitchTextOff

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSwitchTextOff(offText: CharSequence!): Unit
```

**Deprecated:** *Deprecated in Java.*

Set the text displayed on the switch widget in the off state. This should be a very short string; one word if possible.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------|
| `offText` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: Text to display in the off state |

### setSwitchTextOn

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSwitchTextOn(resId: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Set the text displayed on the switch widget in the on state. This should be a very short string; one word if possible.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------|
| `resId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The text as a string resource ID |

### setSwitchTextOn

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSwitchTextOn(onText: CharSequence!): Unit
```

**Deprecated:** *Deprecated in Java.*

Set the text displayed on the switch widget in the on state. This should be a very short string; one word if possible.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------|
| `onText` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: Text to display in the on state |

## Protected methods

### onBindView

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onBindView(view: View!): Unit
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------|
| `view` | [View](../android.view/View.md)!: The View that shows this Preference. |
