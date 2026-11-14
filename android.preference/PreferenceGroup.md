# PreferenceGroup

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PreferenceGroup

Kotlin| [Java](../android/preference/PreferenceGroup.md) 
| --- | --- |

```
abstract class PreferenceGroup : Preference
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.preference.Preference](../android/preference/Preference.md) ||
| | ↳ | [android.preference.PreferenceGroup](../android/preference/PreferenceGroup.md) |

| Known Direct Subclasses [PreferenceCategory](../android/preference/PreferenceCategory.md), [PreferenceScreen](../android/preference/PreferenceScreen.md) |------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------| | [PreferenceCategory](../android/preference/PreferenceCategory.md) | Used to group [Preference](../android/preference/Preference.md) objects and provide a disabled title above the group. | | [PreferenceScreen](../android/preference/PreferenceScreen.md) | Represents a top-level [Preference](../android/preference/Preference.md) that is the root of a Preference hierarchy. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| **This class was deprecated in API level 29.**
|
| Use the [AndroidX](https://developer.android.com/jetpack/androidx.html) [Preference Library](../androidx/preference/_package.md) for consistent behavior across all devices. For more information on using the AndroidX Preference Library see [Settings](https://developer.android.com/guide/topics/ui/settings.html).

A container for multiple [Preference](../android/preference/Preference.md) objects. It is a base class for Preference objects that are parents, such as [PreferenceCategory](../android/preference/PreferenceCategory.md) and [PreferenceScreen](../android/preference/PreferenceScreen.md).
|
| ### Developer Guides
|
| For information about building a settings UI with Preferences, read the [Settings](https://developer.android.com/guide/topics/ui/settings.html) guide.

<br />

## Summary

| XML attributes ||
|-------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [`android:orderingFromXml`](../android/preference/PreferenceGroup.md) | Whether to order the Preference under this group as they appear in the XML file. |

| Inherited XML attributes ||
|---|---|
| From class [Preference](../android/preference/Preference.md) |---------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [android:defaultValue](../android/preference/Preference.md) | The default value for the preference, which will be set either if persistence is off or persistence is on and the preference is not found in the persistent storage. May be a reference to another resource, in the form "`@[+][`*package* `:]`*type* `/`*name*" or a theme attribute in the form "`?[`*package* `:]`*type* `/`*name*". May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character; May be an integer value, such as "`100`". May be a boolean value, such as "`true`" or "`false`". May be a floating point value, such as "`1.2`". <br /> | | [android:dependency](../android/preference/Preference.md) | The key of another Preference that this Preference will depend on. If the other Preference is not set or is off, this Preference will be disabled. May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character; <br /> | | [android:enabled](../android/preference/Preference.md) | Whether the Preference is enabled. May be a boolean value, such as "`true`" or "`false`". <br /> | | [android:fragment](../android/preference/Preference.md) | When used inside of a modern PreferenceActivity, this declares a new PreferenceFragment to be shown when the user selects this item. May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character; <br /> | | [android:icon](../android/preference/Preference.md) | The optional icon for the preference. May be a reference to another resource, in the form "`@[+][`*package* `:]`*type* `/`*name*" or a theme attribute in the form "`?[`*package* `:]`*type* `/`*name*". <br /> | | [android:iconSpaceReserved](../android/preference/Preference.md) | Whether the space for the preference icon view will be reserved. By default, preference icon view visibility will be set to GONE when there is no icon provided, so the default value of this attribute is false. May be a boolean value, such as "`true`" or "`false`". <br /> | | [android:key](../android/preference/Preference.md) | The key to store the Preference value. May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character; <br /> | | [android:layout](../android/preference/Preference.md) | The layout for the Preference in a PreferenceActivity screen. This should rarely need to be changed, look at widgetLayout instead. May be a reference to another resource, in the form "`@[+][`*package* `:]`*type* `/`*name*" or a theme attribute in the form "`?[`*package* `:]`*type* `/`*name*". <br /> | | [android:order](../android/preference/Preference.md) | The order for the Preference (lower values are to be ordered first). If this is not specified, the default ordering will be alphabetic. May be an integer value, such as "`100`". <br /> | | [android:persistent](../android/preference/Preference.md) | Whether the Preference stores its value to the storage. May be a boolean value, such as "`true`" or "`false`". <br /> | | [android:recycleEnabled](../android/preference/Preference.md) | Whether the preference has enabled to have its view recycled when used in the list view. This is true by default. May be a boolean value, such as "`true`" or "`false`". <br /> | | [android:selectable](../android/preference/Preference.md) | Whether the Preference is selectable. May be a boolean value, such as "`true`" or "`false`". <br /> | | [android:shouldDisableView](../android/preference/Preference.md) | Whether the view of this Preference should be disabled when this Preference is disabled. May be a boolean value, such as "`true`" or "`false`". <br /> | | [android:singleLineTitle](../android/preference/Preference.md) | Whether to use single line for the preference title text. By default, preference title will be constrained to one line, so the default value of this attribute is true. May be a boolean value, such as "`true`" or "`false`". <br /> | | [android:summary](../android/preference/Preference.md) | The summary for the Preference. In API 25 and earlier, this value is read as a plain string with styling information stripped. May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character; <br /> | | [android:title](../android/preference/Preference.md) | The title for the Preference. In API 25 and earlier, this value is read as a plain string with styling information stripped. May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character; <br /> | | [android:widgetLayout](../android/preference/Preference.md) | The layout for the controllable widget portion of a Preference. This is inflated into the layout for a Preference and should be used more frequently than the layout attribute. For example, a checkbox preference would specify a custom layout (consisting of just the CheckBox) here. May be a reference to another resource, in the form "`@[+][`*package* `:]`*type* `/`*name*" or a theme attribute in the form "`?[`*package* `:]`*type* `/`*name*". <br /> | ||

| Inherited constants ||
|---|---|
| From class [Preference](../android/preference/Preference.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEFAULT_ORDER](../android/preference/Preference.md) <br /> Specify for [setOrder(int)](../android/preference/Preference.md))if a specific order is not required. <br /> | ||

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PreferenceGroup](../android/preference/PreferenceGroup.md))`(`context:` ` [Context](../android/content/Context.md)!`, `attrs:` ` [AttributeSet](../android/util/AttributeSet.md)!`)` <br /> |
| [PreferenceGroup](../android/preference/PreferenceGroup.md))`(`context:` ` [Context](../android/content/Context.md)!`, `attrs:` ` [AttributeSet](../android/util/AttributeSet.md)!`, `defStyleAttr:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| [PreferenceGroup](../android/preference/PreferenceGroup.md))`(`context:` ` [Context](../android/content/Context.md)!`, `attrs:` ` [AttributeSet](../android/util/AttributeSet.md)!`, `defStyleAttr:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `defStyleRes:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Public methods ||
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addItemFromInflater](../android/preference/PreferenceGroup.md))`(`preference:` ` [Preference](../android/preference/Preference.md)!`)` Called by the inflater to add an item to this group. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addPreference](../android/preference/PreferenceGroup.md))`(`preference:` ` [Preference](../android/preference/Preference.md)!`)` Adds a [Preference](../android/preference/Preference.md) at the correct position based on the preference's order. |
| open [Preference](../android/preference/Preference.md)! | [findPreference](../android/preference/PreferenceGroup.md))`(`key:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Finds a [Preference](../android/preference/Preference.md) based on its key. |
| --- | --- |
| open [Preference](../android/preference/Preference.md)! | [getPreference](../android/preference/PreferenceGroup.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the [Preference](../android/preference/Preference.md) at a particular index. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPreferenceCount](../android/preference/PreferenceGroup.md))`()` Returns the number of children [Preference](../android/preference/Preference.md) s. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOrderingAsAdded](../android/preference/PreferenceGroup.md))`()` Whether this group is ordering preferences in the order they are added. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyDependencyChange](../android/preference/PreferenceGroup.md))`(`disableDependents:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeAll](../android/preference/PreferenceGroup.md))`()` Removes all [Preferences](../android/preference/Preference.md) from this group. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removePreference](../android/preference/PreferenceGroup.md))`(`preference:` ` [Preference](../android/preference/Preference.md)!`)` Removes a [Preference](../android/preference/Preference.md) from this group. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOrderingAsAdded](../android/preference/PreferenceGroup.md))`(`orderingAsAdded:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Whether to order the [Preference](../android/preference/Preference.md) children of this group as they are added. |

| Protected methods ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dispatchRestoreInstanceState](../android/preference/PreferenceGroup.md))`(`container:` ` [Bundle](../android/os/Bundle.md)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dispatchSaveInstanceState](../android/preference/PreferenceGroup.md))`(`container:` ` [Bundle](../android/os/Bundle.md)!`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOnSameScreenAsChildren](../android/preference/PreferenceGroup.md))`()` Whether this preference group should be shown on the same screen as its contained preferences. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAttachedToActivity](../android/preference/PreferenceGroup.md))`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onPrepareAddPreference](../android/preference/PreferenceGroup.md))`(`preference:` ` [Preference](../android/preference/Preference.md)!`)` Prepares a [Preference](../android/preference/Preference.md) to be added to the group. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPrepareForRemoval](../android/preference/PreferenceGroup.md))`()` <br /> |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [Preference](../android/preference/Preference.md) |-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [callChangeListener](../android/preference/Preference.md))`(`newValue:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> Call this method after the user changes the preference, but before the internal state is set. This allows the client to ignore the user value. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compareTo](../android/preference/Preference.md))`(`other:` ` [Preference](../android/preference/Preference.md)!`)` <br /> Compares Preference objects based on order (if set), otherwise alphabetically on the titles. <br /> | | [Preference](../android/preference/Preference.md)! | [findPreferenceInHierarchy](../android/preference/Preference.md))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Finds a Preference in this hierarchy (the whole thing, even above/below your [PreferenceScreen](../android/preference/PreferenceScreen.md) screen break) with the given key. This only functions after we have been attached to a hierarchy. <br /> | | [Context](../android/content/Context.md)! | [getContext](../android/preference/Preference.md))`()` <br /> Returns the [android.content.Context](../android/content/Context.md) of this Preference. Each Preference in a Preference hierarchy can be from different Context (for example, if multiple activities provide preferences into a single [PreferenceActivity](../android/preference/PreferenceActivity.md)). This Context will be used to save the Preference values. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDependency](../android/preference/Preference.md))`()` <br /> Returns the key of the dependency on this Preference. <br /> | | [SharedPreferences.Editor](../android/content/SharedPreferences.Editor.md)! | [getEditor](../android/preference/Preference.md))`()` <br /> Returns an [SharedPreferences.Editor](../android/content/SharedPreferences.Editor.md) where this Preference can save its value(s). Usually it's easier to use one of the helper save methods: [persistBoolean(boolean)](../android/preference/Preference.md)), [persistFloat(float)](../android/preference/Preference.md)), [persistInt(int)](../android/preference/Preference.md)), [persistLong(long)](../android/preference/Preference.md)), [persistString(java.lang.String)](../android/preference/Preference.md)). To read values, see [getSharedPreferences()](../android/preference/Preference.md)). If [shouldCommit()](../android/preference/Preference.md))returns true, it is this Preference's responsibility to commit. In some cases, writes to this will not be committed right away and hence not show up in the SharedPreferences, this is intended behavior to improve performance. <br /> | | [Bundle](../android/os/Bundle.md)! | [getExtras](../android/preference/Preference.md))`()` <br /> Return the extras Bundle object associated with this preference, creating a new Bundle if there currently isn't one. You can use this to get and set individual extra key/value pairs. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getFragment](../android/preference/Preference.md))`()` <br /> Return the fragment class name associated with this Preference. <br /> | | [Drawable](../android/graphics/drawable/Drawable.md)! | [getIcon](../android/preference/Preference.md))`()` <br /> Returns the icon of this Preference. <br /> | | [Intent](../android/content/Intent.md)! | [getIntent](../android/preference/Preference.md))`()` <br /> Return the [Intent](../android/content/Intent.md) associated with this Preference. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getKey](../android/preference/Preference.md))`()` <br /> Gets the key for this Preference, which is also the key used for storing values into [SharedPreferences](../android/content/SharedPreferences.md) or [PreferenceDataStore](../android/preference/PreferenceDataStore.md). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLayoutResource](../android/preference/Preference.md))`()` <br /> Gets the layout resource that will be shown as the [View](../android/view/View.md) for this Preference. <br /> | | [Preference.OnPreferenceChangeListener](../android/preference/Preference.OnPreferenceChangeListener.md)! | [getOnPreferenceChangeListener](../android/preference/Preference.md))`()` <br /> Returns the callback to be invoked when this Preference is changed by the user (but before the internal state has been updated). <br /> | | [Preference.OnPreferenceClickListener](../android/preference/Preference.OnPreferenceClickListener.md)! | [getOnPreferenceClickListener](../android/preference/Preference.md))`()` <br /> Returns the callback to be invoked when this Preference is clicked. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOrder](../android/preference/Preference.md))`()` <br /> Gets the order of this Preference with respect to other Preference objects on the same level. <br /> | | [PreferenceGroup](../android/preference/PreferenceGroup.md)? | [getParent](../android/preference/Preference.md))`()` <br /> Returns the [PreferenceGroup](../android/preference/PreferenceGroup.md) which is this Preference assigned to or`null`if this preference is not assigned to any group or is a root Preference. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getPersistedBoolean](../android/preference/Preference.md))`(`defaultReturnValue:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Attempts to get a persisted boolean if this Preference is persistent. <br /> | | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getPersistedFloat](../android/preference/Preference.md))`(`defaultReturnValue:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` <br /> Attempts to get a persisted float if this Preference is persistent. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPersistedInt](../android/preference/Preference.md))`(`defaultReturnValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Attempts to get a persisted int if this Preference is persistent. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getPersistedLong](../android/preference/Preference.md))`(`defaultReturnValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Attempts to get a persisted long if this Preference is persistent. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getPersistedString](../android/preference/Preference.md))`(`defaultReturnValue:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Attempts to get a persisted String if this Preference is persistent. <br /> | | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | [getPersistedStringSet](../android/preference/Preference.md))`(`defaultReturnValue:` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` <br /> Attempts to get a persisted set of Strings if this Preference is persistent. <br /> | | [PreferenceDataStore](../android/preference/PreferenceDataStore.md)? | [getPreferenceDataStore](../android/preference/Preference.md))`()` <br /> Returns [PreferenceDataStore](../android/preference/PreferenceDataStore.md) used by this Preference. Returns`null`if [android.content.SharedPreferences](../android/content/SharedPreferences.md) is used instead. By default preferences always use [android.content.SharedPreferences](../android/content/SharedPreferences.md). To make this preference to use the [PreferenceDataStore](../android/preference/PreferenceDataStore.md) you need to assign your implementation to the Preference itself via [setPreferenceDataStore(android.preference.PreferenceDataStore)](../android/preference/Preference.md))or to its [PreferenceManager](../android/preference/PreferenceManager.md) via [PreferenceManager.setPreferenceDataStore(PreferenceDataStore)](../android/preference/PreferenceManager.md)). <br /> | | [PreferenceManager](../android/preference/PreferenceManager.md)! | [getPreferenceManager](../android/preference/Preference.md))`()` <br /> Gets the [PreferenceManager](../android/preference/PreferenceManager.md) that manages this Preference object's tree. <br /> | | [SharedPreferences](../android/content/SharedPreferences.md)! | [getSharedPreferences](../android/preference/Preference.md))`()` <br /> Returns the [SharedPreferences](../android/content/SharedPreferences.md) where this Preference can read its value(s). Usually, it's easier to use one of the helper read methods: [getPersistedBoolean(boolean)](../android/preference/Preference.md)), [getPersistedFloat(float)](../android/preference/Preference.md)), [getPersistedInt(int)](../android/preference/Preference.md)), [getPersistedLong(long)](../android/preference/Preference.md)), [getPersistedString(java.lang.String)](../android/preference/Preference.md)). To save values, see [getEditor()](../android/preference/Preference.md)). In some cases, writes to the [getEditor()](../android/preference/Preference.md))will not be committed right away and hence not show up in the returned [SharedPreferences](../android/content/SharedPreferences.md), this is intended behavior to improve performance. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getShouldDisableView](../android/preference/Preference.md))`()` <br /> Checks whether this Preference should disable its view when it's action is disabled. <br /> | | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [getSummary](../android/preference/Preference.md))`()` <br /> Returns the summary of this Preference. <br /> | | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [getTitle](../android/preference/Preference.md))`()` <br /> Returns the title of this Preference. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTitleRes](../android/preference/Preference.md))`()` <br /> Returns the title resource ID of this Preference. If the title did not come from a resource,`0`is returned. <br /> | | [View](../android/view/View.md)! | [getView](../android/preference/Preference.md))`(`convertView:` ` [View](../android/view/View.md)!`, `parent:` ` [ViewGroup](../android/view/ViewGroup.md)!`)` <br /> Gets the View that will be shown in the [PreferenceActivity](../android/preference/PreferenceActivity.md). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getWidgetLayoutResource](../android/preference/Preference.md))`()` <br /> Gets the layout resource for the controllable widget portion of this Preference. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasKey](../android/preference/Preference.md))`()` <br /> Checks whether this Preference has a valid key. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEnabled](../android/preference/Preference.md))`()` <br /> Checks whether this Preference should be enabled in the list. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isIconSpaceReserved](../android/preference/Preference.md))`()` <br /> Gets whether the space this preference icon view is reserved. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPersistent](../android/preference/Preference.md))`()` <br /> Checks whether this Preference is persistent. If it is, it stores its value(s) into the persistent [SharedPreferences](../android/content/SharedPreferences.md) storage by default or into [PreferenceDataStore](../android/preference/PreferenceDataStore.md) if assigned. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRecycleEnabled](../android/preference/Preference.md))`()` <br /> Checks whether this Preference has enabled to have its view recycled when used in the list view. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSelectable](../android/preference/Preference.md))`()` <br /> Checks whether this Preference should be selectable in the list. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSingleLineTitle](../android/preference/Preference.md))`()` <br /> Gets whether the title of this preference is constrained to a single line. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyChanged](../android/preference/Preference.md))`()` <br /> Should be called when the data of this [Preference](../android/preference/Preference.md) has changed. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyHierarchyChanged](../android/preference/Preference.md))`()` <br /> Should be called when a Preference has been added/removed from this group, or the ordering should be re-evaluated. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAttachedToHierarchy](../android/preference/Preference.md))`(`preferenceManager:` ` [PreferenceManager](../android/preference/PreferenceManager.md)!`)` <br /> Called when this Preference has been attached to a Preference hierarchy. Make sure to call the super implementation. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onBindView](../android/preference/Preference.md))`(`view:` ` [View](../android/view/View.md)!`)` <br /> Binds the created View to the data for this Preference. This is a good place to grab references to custom Views in the layout and set properties on them. Make sure to call through to the superclass's implementation. If you override this method you*must*call through to the superclass implementation. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onClick](../android/preference/Preference.md))`()` <br /> Processes a click on the preference. This includes saving the value to the [SharedPreferences](../android/content/SharedPreferences.md). However, the overridden method should call [callChangeListener(java.lang.Object)](../android/preference/Preference.md))to make sure the client wants to update the preference's state with the new value. <br /> | | [View](../android/view/View.md)! | [onCreateView](../android/preference/Preference.md))`(`parent:` ` [ViewGroup](../android/view/ViewGroup.md)!`)` <br /> Creates the View to be shown for this Preference in the [PreferenceActivity](../android/preference/PreferenceActivity.md). The default behavior is to inflate the main layout of this Preference (see [setLayoutResource(int)](../android/preference/Preference.md)). If changing this behavior, please specify a [ViewGroup](../android/view/ViewGroup.md) with ID [android.R.id#widget_frame](../android/R.id.md). Make sure to call through to the superclass's implementation. If you override this method you*must*call through to the superclass implementation. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDependencyChanged](../android/preference/Preference.md))`(`dependency:` ` [Preference](../android/preference/Preference.md)!`, `disableDependent:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Called when the dependency changes. <br /> | | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [onGetDefaultValue](../android/preference/Preference.md))`(`a:` ` [TypedArray](../android/content/res/TypedArray.md)!`, `index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Called when a Preference is being inflated and the default value attribute needs to be read. Since different Preference types have different value types, the subclass should get and return the default value which will be its value type. For example, if the value type is String, the body of the method would proxy to [TypedArray.getString(int)](../android/content/res/TypedArray.md)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onParentChanged](../android/preference/Preference.md))`(`parent:` ` [Preference](../android/preference/Preference.md)!`, `disableChild:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Called when the implicit parent dependency changes. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onRestoreInstanceState](../android/preference/Preference.md))`(`state:` ` [Parcelable](../android/os/Parcelable.md)!`)` <br /> Hook allowing a Preference to re-apply a representation of its internal state that had previously been generated by [onSaveInstanceState](../android/preference/Preference.md)). This function will never be called with a`null`state. <br /> | | [Parcelable](../android/os/Parcelable.md)! | [onSaveInstanceState](../android/preference/Preference.md))`()` <br /> Hook allowing a Preference to generate a representation of its internal state that can later be used to create a new instance with that same state. This state should only contain information that is not persistent or can be reconstructed later. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSetInitialValue](../android/preference/Preference.md))`(`restorePersistedValue:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `defaultValue:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> Implement this to set the initial value of the Preference. If restorePersistedValue is true, you should restore the Preference value from the [android.content.SharedPreferences](../android/content/SharedPreferences.md). If restorePersistedValue is false, you should set the Preference value to defaultValue that is given (and possibly store to SharedPreferences if [shouldPersist()](../android/preference/Preference.md))is true). In case of using [PreferenceDataStore](../android/preference/PreferenceDataStore.md), the restorePersistedValue is always`true`. But the default value (if provided) is set. This may not always be called. One example is if it should not persist but there is no default value given. <br /> | | [Bundle](../android/os/Bundle.md)! | [peekExtras](../android/preference/Preference.md))`()` <br /> Return the extras Bundle object associated with this preference, returning`null`if there is not currently one. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [persistBoolean](../android/preference/Preference.md))`(`value:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Attempts to persist a boolean if this Preference is persistent. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [persistFloat](../android/preference/Preference.md))`(`value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` <br /> Attempts to persist a long if this Preference is persistent. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [persistInt](../android/preference/Preference.md))`(`value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Attempts to persist an int if this Preference is persistent. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [persistLong](../android/preference/Preference.md))`(`value:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Attempts to persist a long if this Preference is persistent. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [persistString](../android/preference/Preference.md))`(`value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Attempts to persist a String if this Preference is persistent. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [persistStringSet](../android/preference/Preference.md))`(`values:` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` <br /> Attempts to persist a set of Strings if this Preference is persistent. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [restoreHierarchyState](../android/preference/Preference.md))`(`container:` ` [Bundle](../android/os/Bundle.md)!`)` <br /> Restore this Preference hierarchy's previously saved state from the given container. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [saveHierarchyState](../android/preference/Preference.md))`(`container:` ` [Bundle](../android/os/Bundle.md)!`)` <br /> Store this Preference hierarchy's frozen state into the given container. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDefaultValue](../android/preference/Preference.md))`(`defaultValue:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> Sets the default value for this Preference, which will be set either if persistence is off or persistence is on and the preference is not found in the persistent storage. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDependency](../android/preference/Preference.md))`(`dependencyKey:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Sets the key of a Preference that this Preference will depend on. If that Preference is not set or is off, this Preference will be disabled. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEnabled](../android/preference/Preference.md))`(`enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Sets whether this Preference is enabled. If disabled, it will not handle clicks. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFragment](../android/preference/Preference.md))`(`fragment:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Sets the class name of a fragment to be shown when this Preference is clicked. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setIcon](../android/preference/Preference.md))`(`icon:` ` [Drawable](../android/graphics/drawable/Drawable.md)!`)` <br /> Sets the icon for this Preference with a Drawable. This icon will be placed into the ID [android.R.id#icon](../android/R.id.md) within the View created by [onCreateView(android.view.ViewGroup)](../android/preference/Preference.md)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setIcon](../android/preference/Preference.md))`(`iconResId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the icon for this Preference with a resource ID. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setIconSpaceReserved](../android/preference/Preference.md))`(`iconSpaceReserved:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Sets whether to reserve the space of this Preference icon view when no icon is provided. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setIntent](../android/preference/Preference.md))`(`intent:` ` [Intent](../android/content/Intent.md)!`)` <br /> Sets an [Intent](../android/content/Intent.md) to be used for [Context.startActivity(Intent)](../android/content/Context.md))when this Preference is clicked. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setKey](../android/preference/Preference.md))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Sets the key for this Preference, which is used as a key to the [SharedPreferences](../android/content/SharedPreferences.md) or [PreferenceDataStore](../android/preference/PreferenceDataStore.md). This should be unique for the package. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLayoutResource](../android/preference/Preference.md))`(`layoutResId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the layout resource that is inflated as the [View](../android/view/View.md) to be shown for this Preference. In most cases, the default layout is sufficient for custom Preference objects and only the widget layout needs to be changed. This layout should contain a [ViewGroup](../android/view/ViewGroup.md) with ID [android.R.id#widget_frame](../android/R.id.md) to be the parent of the specific widget for this Preference. It should similarly contain [android.R.id#title](../android/R.id.md) and [android.R.id#summary](../android/R.id.md). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnPreferenceChangeListener](../android/preference/Preference.md))`(`onPreferenceChangeListener:` ` [Preference.OnPreferenceChangeListener](../android/preference/Preference.OnPreferenceChangeListener.md)!`)` <br /> Sets the callback to be invoked when this Preference is changed by the user (but before the internal state has been updated). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnPreferenceClickListener](../android/preference/Preference.md))`(`onPreferenceClickListener:` ` [Preference.OnPreferenceClickListener](../android/preference/Preference.OnPreferenceClickListener.md)!`)` <br /> Sets the callback to be invoked when this Preference is clicked. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOrder](../android/preference/Preference.md))`(`order:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the order of this Preference with respect to other Preference objects on the same level. If this is not specified, the default behavior is to sort alphabetically. The [PreferenceGroup.setOrderingAsAdded(boolean)](../android/preference/PreferenceGroup.md))can be used to order Preference objects based on the order they appear in the XML. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPersistent](../android/preference/Preference.md))`(`persistent:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Sets whether this Preference is persistent. When persistent, it stores its value(s) into the persistent [SharedPreferences](../android/content/SharedPreferences.md) storage by default or into [PreferenceDataStore](../android/preference/PreferenceDataStore.md) if assigned. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPreferenceDataStore](../android/preference/Preference.md))`(`dataStore:` ` [PreferenceDataStore](../android/preference/PreferenceDataStore.md)!`)` <br /> Sets a [PreferenceDataStore](../android/preference/PreferenceDataStore.md) to be used by this Preference instead of using [android.content.SharedPreferences](../android/content/SharedPreferences.md). The data store will remain assigned even if the Preference is moved around the preference hierarchy. It will also override a data store propagated from the [PreferenceManager](../android/preference/PreferenceManager.md) that owns this Preference. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRecycleEnabled](../android/preference/Preference.md))`(`enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Sets whether this Preference has enabled to have its view recycled when used in the list view. By default the recycling is enabled. The value can be changed only before this preference is added to the preference hierarchy. If view recycling is not allowed then each time the list view populates this preference the [getView(android.view.View,android.view.ViewGroup)](../android/preference/Preference.md))method receives a`null`convert view and needs to recreate the view. Otherwise view gets recycled and only [onBindView(android.view.View)](../android/preference/Preference.md))gets called. If you override this method you*must*call through to the superclass implementation. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSelectable](../android/preference/Preference.md))`(`selectable:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Sets whether this Preference is selectable. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setShouldDisableView](../android/preference/Preference.md))`(`shouldDisableView:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Sets whether this Preference should disable its view when it gets disabled. For example, set this and [setEnabled(boolean)](../android/preference/Preference.md))to false for preferences that are only displaying information and 1) should not be clickable 2) should not have the view set to the disabled state. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSingleLineTitle](../android/preference/Preference.md))`(`singleLineTitle:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Sets whether to constrain the title of this Preference to a single line instead of letting it wrap onto multiple lines. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSummary](../android/preference/Preference.md))`(`summaryResId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the summary for this Preference with a resource ID. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSummary](../android/preference/Preference.md))`(`summary:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` <br /> Sets the summary for this Preference with a CharSequence. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTitle](../android/preference/Preference.md))`(`titleResId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the title for this Preference with a resource ID. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTitle](../android/preference/Preference.md))`(`title:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` <br /> Sets the title for this Preference with a CharSequence. This title will be placed into the ID [android.R.id#title](../android/R.id.md) within the View created by [onCreateView(android.view.ViewGroup)](../android/preference/Preference.md)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setWidgetLayoutResource](../android/preference/Preference.md))`(`widgetLayoutResId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the layout for the controllable widget portion of this Preference. This is inflated into the main layout. For example, a [CheckBoxPreference](../android/preference/CheckBoxPreference.md) would specify a custom layout (consisting of just the CheckBox) here, instead of creating its own main layout. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [shouldCommit](../android/preference/Preference.md))`()` <br /> Returns whether the [Preference](../android/preference/Preference.md) should commit its saved value(s) in [getEditor()](../android/preference/Preference.md)). This may return false in situations where batch committing is being done (by the manager) to improve performance. If this preference is using [PreferenceDataStore](../android/preference/PreferenceDataStore.md) this value is irrelevant. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [shouldDisableDependents](../android/preference/Preference.md))`()` <br /> Checks whether this preference's dependents should currently be disabled. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [shouldPersist](../android/preference/Preference.md))`()` <br /> Checks whether, at the given time this method is called, this Preference should store/restore its value(s) into the [SharedPreferences](../android/content/SharedPreferences.md) or into [PreferenceDataStore](../android/preference/PreferenceDataStore.md) if assigned. This, at minimum, checks whether this Preference is persistent and it currently has a key. Before you save/restore from the storage, check this first. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/preference/Preference.md))`()` <br /> | ||

## XML attributes

### android:orderingFromXml

```
android:orderingFromXml
```
Whether to order the Preference under this group as they appear in the XML file. If this is false, the ordering will follow the Preference order attribute and default to alphabetic for those without the order attribute.

May be a boolean value, such as "`true`" or "`false`".

## Public constructors

### PreferenceGroup

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PreferenceGroup(
    context: Context!, 
    attrs: AttributeSet!)
```  

### PreferenceGroup

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PreferenceGroup(
    context: Context!, 
    attrs: AttributeSet!, 
    defStyleAttr: Int)
```  

### PreferenceGroup

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PreferenceGroup(
    context: Context!, 
    attrs: AttributeSet!, 
    defStyleAttr: Int, 
    defStyleRes: Int)
```

## Public methods

### addItemFromInflater

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addItemFromInflater(preference: Preference!): Unit
```

**Deprecated:** *Deprecated in Java.*

Called by the inflater to add an item to this group. 

### addPreference

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addPreference(preference: Preference!): Boolean
```

**Deprecated:** *Deprecated in Java.*

Adds a [Preference](../android/preference/Preference.md) at the correct position based on the preference's order.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------|
| `preference` | [Preference](../android/preference/Preference.md)!:The preference to add. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Whether the preference is now in this group. |

### findPreference

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun findPreference(key: CharSequence!): Preference!
```

**Deprecated:** *Deprecated in Java.*

Finds a [Preference](../android/preference/Preference.md) based on its key. If two [Preference](../android/preference/Preference.md) share the same key (not recommended), the first to appear will be returned (to retrieve the other preference with the same key, call this method on the first preference). If this preference has the key, it will not be returned.

This will recursively search for the preference into children that are also [PreferenceGroups](../android/preference/PreferenceGroup.md).

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:The key of the preference to retrieve. |

| Return ||
|---------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [Preference](../android/preference/Preference.md)! | The [Preference](../android/preference/Preference.md) with the key, or null. |

### getPreference

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPreference(index: Int): Preference!
```

**Deprecated:** *Deprecated in Java.*

Returns the [Preference](../android/preference/Preference.md) at a particular index.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index of the [Preference](../android/preference/Preference.md) to retrieve. |

| Return ||
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [Preference](../android/preference/Preference.md)! | The [Preference](../android/preference/Preference.md). |

### getPreferenceCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPreferenceCount(): Int
```

**Deprecated:** *Deprecated in Java.*

Returns the number of children [Preference](../android/preference/Preference.md) s.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The number of preference children in this group. |

### isOrderingAsAdded

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isOrderingAsAdded(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Whether this group is ordering preferences in the order they are added.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Whether this group orders based on the order the children are added. |

**See Also**

- [#setOrderingAsAdded(boolean)](../android/preference/PreferenceGroup.md)) 

### notifyDependencyChange

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun notifyDependencyChange(disableDependents: Boolean): Unit
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `disableDependents` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Whether this Preference should disable its dependents. |

### removeAll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeAll(): Unit
```

**Deprecated:** *Deprecated in Java.*

Removes all [Preferences](../android/preference/Preference.md) from this group. 

### removePreference

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removePreference(preference: Preference!): Boolean
```

**Deprecated:** *Deprecated in Java.*

Removes a [Preference](../android/preference/Preference.md) from this group.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------|
| `preference` | [Preference](../android/preference/Preference.md)!:The preference to remove. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Whether the preference was found and removed. |

### setOrderingAsAdded

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOrderingAsAdded(orderingAsAdded: Boolean): Unit
```

**Deprecated:** *Deprecated in Java.*

Whether to order the [Preference](../android/preference/Preference.md) children of this group as they are added. If this is false, the ordering will follow each Preference order and default to alphabetic for those without an order.

If this is called after preferences are added, they will not be re-ordered in the order they were added, hence call this method early on.

| Parameters ||
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| `orderingAsAdded` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Whether to order according to the order added. |

**See Also**

- [android.preference.Preference#setOrder(int)](../android/preference/Preference.md))

## Protected methods

### dispatchRestoreInstanceState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun dispatchRestoreInstanceState(container: Bundle!): Unit
```

**Deprecated:** *Deprecated in Java.* 

### dispatchSaveInstanceState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun dispatchSaveInstanceState(container: Bundle!): Unit
```

**Deprecated:** *Deprecated in Java.* 

### isOnSameScreenAsChildren

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun isOnSameScreenAsChildren(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Whether this preference group should be shown on the same screen as its contained preferences.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the contained preferences should be shown on the same screen as this preference. |

### onAttachedToActivity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onAttachedToActivity(): Unit
```

**Deprecated:** *Deprecated in Java.* 

### onPrepareAddPreference

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onPrepareAddPreference(preference: Preference!): Boolean
```

**Deprecated:** *Deprecated in Java.*

Prepares a [Preference](../android/preference/Preference.md) to be added to the group.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------|
| `preference` | [Preference](../android/preference/Preference.md)!:The preference to add. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Whether to allow adding the preference (true), or not (false). |

### onPrepareForRemoval

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onPrepareForRemoval(): Unit
```

**Deprecated:** *Deprecated in Java.*
