# Preference

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Preference

Kotlin| [Java](../android/preference/Preference.md) 
| --- | --- |

```
open class Preference : Comparable<Preference!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.preference.Preference](../android/preference/Preference.md) |

| Known Direct Subclasses [DialogPreference](../android/preference/DialogPreference.md), [PreferenceGroup](../android/preference/PreferenceGroup.md), [RingtonePreference](../android/preference/RingtonePreference.md), [TwoStatePreference](../android/preference/TwoStatePreference.md) |------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [DialogPreference](../android/preference/DialogPreference.md) | A base class for [Preference](../android/preference/Preference.md) objects that are dialog-based. | | [PreferenceGroup](../android/preference/PreferenceGroup.md) | A container for multiple [Preference](../android/preference/Preference.md) objects. | | [RingtonePreference](../android/preference/RingtonePreference.md) | A [Preference](../android/preference/Preference.md) that allows the user to choose a ringtone from those on the device. | | [TwoStatePreference](../android/preference/TwoStatePreference.md) | Common base class for preferences that have two selectable states, persist a boolean value in SharedPreferences, and may have dependent preferences that are enabled/disabled based on the current state. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [CheckBoxPreference](../android/preference/CheckBoxPreference.md), [EditTextPreference](../android/preference/EditTextPreference.md), [ListPreference](../android/preference/ListPreference.md), [MultiSelectListPreference](../android/preference/MultiSelectListPreference.md), [PreferenceCategory](../android/preference/PreferenceCategory.md), [PreferenceScreen](../android/preference/PreferenceScreen.md), [SwitchPreference](../android/preference/SwitchPreference.md) |--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------| | [CheckBoxPreference](../android/preference/CheckBoxPreference.md) | A [Preference](../android/preference/Preference.md) that provides checkbox widget functionality. | | [EditTextPreference](../android/preference/EditTextPreference.md) | A [Preference](../android/preference/Preference.md) that allows for string input. | | [ListPreference](../android/preference/ListPreference.md) | A [Preference](../android/preference/Preference.md) that displays a list of entries as a dialog. | | [MultiSelectListPreference](../android/preference/MultiSelectListPreference.md) | A [Preference](../android/preference/Preference.md) that displays a list of entries as a dialog. | | [PreferenceCategory](../android/preference/PreferenceCategory.md) | Used to group [Preference](../android/preference/Preference.md) objects and provide a disabled title above the group. | | [PreferenceScreen](../android/preference/PreferenceScreen.md) | Represents a top-level [Preference](../android/preference/Preference.md) that is the root of a Preference hierarchy. | | [SwitchPreference](../android/preference/SwitchPreference.md) | A [Preference](../android/preference/Preference.md) that provides a two-state toggleable option. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| **This class was deprecated in API level 29.**
|
| Use the [AndroidX](https://developer.android.com/jetpack/androidx.html) [Preference Library](../androidx/preference/_package.md) for consistent behavior across all devices. For more information on using the AndroidX Preference Library see [Settings](https://developer.android.com/guide/topics/ui/settings.html).

Represents the basic Preference UI building block displayed by a [PreferenceActivity](../android/preference/PreferenceActivity.md) in the form of a [ListView](../android/widget/ListView.md). This class provides the [View](../android/view/View.md) to be displayed in the activity and associates with a [SharedPreferences](../android/content/SharedPreferences.md) to store/retrieve the preference data.

When specifying a preference hierarchy in XML, each element can point to a subclass of [Preference](../android/preference/Preference.md), similar to the view hierarchy and layouts.

This class contains a`key`that will be used as the key into the [SharedPreferences](../android/content/SharedPreferences.md). It is up to the subclass to decide how to store the value.
|
| ### Developer Guides
|
| For information about building a settings UI with Preferences, read the [Settings](https://developer.android.com/guide/topics/ui/settings.html) guide.

## Summary

| Nested classes ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [BaseSavedState](../android/preference/Preference.BaseSavedState.md) A base class for managing the instance state of a [Preference](../android/preference/Preference.md). |
| abstract | [OnPreferenceChangeListener](../android/preference/Preference.OnPreferenceChangeListener.md) Interface definition for a callback to be invoked when the value of this [Preference](../android/preference/Preference.md) has been changed by the user and is about to be set and/or persisted. |
| abstract | [OnPreferenceClickListener](../android/preference/Preference.OnPreferenceClickListener.md) Interface definition for a callback to be invoked when a [Preference](../android/preference/Preference.md) is clicked. |
| --- | --- |

| XML attributes ||
|-----------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [`android:defaultValue`](../android/preference/Preference.md) | The default value for the preference, which will be set either if persistence is off or persistence is on and the preference is not found in the persistent storage. |
| [`android:dependency`](../android/preference/Preference.md) | The key of another Preference that this Preference will depend on. |
| [`android:enabled`](../android/preference/Preference.md) | Whether the Preference is enabled. |
| --- | --- |
| [`android:fragment`](../android/preference/Preference.md) | When used inside of a modern PreferenceActivity, this declares a new PreferenceFragment to be shown when the user selects this item. |
| [`android:icon`](../android/preference/Preference.md) | The optional icon for the preference. |
| [`android:iconSpaceReserved`](../android/preference/Preference.md) | Whether the space for the preference icon view will be reserved. |
| --- | --- |
| [`android:key`](../android/preference/Preference.md) | The key to store the Preference value. |
| [`android:layout`](../android/preference/Preference.md) | The layout for the Preference in a PreferenceActivity screen. |
| [`android:order`](../android/preference/Preference.md) | The order for the Preference (lower values are to be ordered first). |
| --- | --- |
| [`android:persistent`](../android/preference/Preference.md) | Whether the Preference stores its value to the storage. |
| [`android:recycleEnabled`](../android/preference/Preference.md) | Whether the preference has enabled to have its view recycled when used in the list view. |
| [`android:selectable`](../android/preference/Preference.md) | Whether the Preference is selectable. |
| --- | --- |
| [`android:shouldDisableView`](../android/preference/Preference.md) | Whether the view of this Preference should be disabled when this Preference is disabled. |
| [`android:singleLineTitle`](../android/preference/Preference.md) | Whether to use single line for the preference title text. |
| [`android:summary`](../android/preference/Preference.md) | The summary for the Preference. |
| --- | --- |
| [`android:title`](../android/preference/Preference.md) | The title for the Preference. |
| [`android:widgetLayout`](../android/preference/Preference.md) | The layout for the controllable widget portion of a Preference. |

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEFAULT_ORDER](../android/preference/Preference.md) Specify for [setOrder(int)](../android/preference/Preference.md))if a specific order is not required. |

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Preference](../android/preference/Preference.md))`(`context:` ` [Context](../android/content/Context.md)!`)` Constructor to create a Preference. |
| [Preference](../android/preference/Preference.md))`(`context:` ` [Context](../android/content/Context.md)!`, `attrs:` ` [AttributeSet](../android/util/AttributeSet.md)!`)` Constructor that is called when inflating a Preference from XML. |
| [Preference](../android/preference/Preference.md))`(`context:` ` [Context](../android/content/Context.md)!`, `attrs:` ` [AttributeSet](../android/util/AttributeSet.md)!`, `defStyleAttr:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Perform inflation from XML and apply a class-specific base style. |
| [Preference](../android/preference/Preference.md))`(`context:` ` [Context](../android/content/Context.md)!`, `attrs:` ` [AttributeSet](../android/util/AttributeSet.md)!`, `defStyleAttr:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `defStyleRes:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Perform inflation from XML and apply a class-specific base style. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compareTo](../android/preference/Preference.md))`(`other:` ` [Preference](../android/preference/Preference.md)!`)` Compares Preference objects based on order (if set), otherwise alphabetically on the titles. |
| open [Context](../android/content/Context.md)! | [getContext](../android/preference/Preference.md))`()` Returns the [android.content.Context](../android/content/Context.md) of this Preference. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDependency](../android/preference/Preference.md))`()` Returns the key of the dependency on this Preference. |
| --- | --- |
| open [SharedPreferences.Editor](../android/content/SharedPreferences.Editor.md)! | [getEditor](../android/preference/Preference.md))`()` Returns an [SharedPreferences.Editor](../android/content/SharedPreferences.Editor.md) where this Preference can save its value(s). |
| open [Bundle](../android/os/Bundle.md)! | [getExtras](../android/preference/Preference.md))`()` Return the extras Bundle object associated with this preference, creating a new Bundle if there currently isn't one. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getFragment](../android/preference/Preference.md))`()` Return the fragment class name associated with this Preference. |
| --- | --- |
| open [Drawable](../android/graphics/drawable/Drawable.md)! | [getIcon](../android/preference/Preference.md))`()` Returns the icon of this Preference. |
| open [Intent](../android/content/Intent.md)! | [getIntent](../android/preference/Preference.md))`()` Return the [Intent](../android/content/Intent.md) associated with this Preference. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getKey](../android/preference/Preference.md))`()` Gets the key for this Preference, which is also the key used for storing values into [SharedPreferences](../android/content/SharedPreferences.md) or [PreferenceDataStore](../android/preference/PreferenceDataStore.md). |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLayoutResource](../android/preference/Preference.md))`()` Gets the layout resource that will be shown as the [View](../android/view/View.md) for this Preference. |
| open [Preference.OnPreferenceChangeListener](../android/preference/Preference.OnPreferenceChangeListener.md)! | [getOnPreferenceChangeListener](../android/preference/Preference.md))`()` Returns the callback to be invoked when this Preference is changed by the user (but before the internal state has been updated). |
| open [Preference.OnPreferenceClickListener](../android/preference/Preference.OnPreferenceClickListener.md)! | [getOnPreferenceClickListener](../android/preference/Preference.md))`()` Returns the callback to be invoked when this Preference is clicked. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOrder](../android/preference/Preference.md))`()` Gets the order of this Preference with respect to other Preference objects on the same level. |
| open [PreferenceGroup](../android/preference/PreferenceGroup.md)? | [getParent](../android/preference/Preference.md))`()` Returns the [PreferenceGroup](../android/preference/PreferenceGroup.md) which is this Preference assigned to or`null`if this preference is not assigned to any group or is a root Preference. |
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getPersistedStringSet](../android/preference/Preference.md))`(`defaultReturnValue:` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Attempts to get a persisted set of Strings if this Preference is persistent. |
| --- | --- |
| open [PreferenceDataStore](../android/preference/PreferenceDataStore.md)? | [getPreferenceDataStore](../android/preference/Preference.md))`()` Returns [PreferenceDataStore](../android/preference/PreferenceDataStore.md) used by this Preference. |
| open [PreferenceManager](../android/preference/PreferenceManager.md)! | [getPreferenceManager](../android/preference/Preference.md))`()` Gets the [PreferenceManager](../android/preference/PreferenceManager.md) that manages this Preference object's tree. |
| open [SharedPreferences](../android/content/SharedPreferences.md)! | [getSharedPreferences](../android/preference/Preference.md))`()` Returns the [SharedPreferences](../android/content/SharedPreferences.md) where this Preference can read its value(s). |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getShouldDisableView](../android/preference/Preference.md))`()` Checks whether this Preference should disable its view when it's action is disabled. |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [getSummary](../android/preference/Preference.md))`()` Returns the summary of this Preference. |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [getTitle](../android/preference/Preference.md))`()` Returns the title of this Preference. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTitleRes](../android/preference/Preference.md))`()` Returns the title resource ID of this Preference. |
| open [View](../android/view/View.md)! | [getView](../android/preference/Preference.md))`(`convertView:` ` [View](../android/view/View.md)!`, `parent:` ` [ViewGroup](../android/view/ViewGroup.md)!`)` Gets the View that will be shown in the [PreferenceActivity](../android/preference/PreferenceActivity.md). |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getWidgetLayoutResource](../android/preference/Preference.md))`()` Gets the layout resource for the controllable widget portion of this Preference. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasKey](../android/preference/Preference.md))`()` Checks whether this Preference has a valid key. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEnabled](../android/preference/Preference.md))`()` Checks whether this Preference should be enabled in the list. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isIconSpaceReserved](../android/preference/Preference.md))`()` Gets whether the space this preference icon view is reserved. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPersistent](../android/preference/Preference.md))`()` Checks whether this Preference is persistent. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRecycleEnabled](../android/preference/Preference.md))`()` Checks whether this Preference has enabled to have its view recycled when used in the list view. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSelectable](../android/preference/Preference.md))`()` Checks whether this Preference should be selectable in the list. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSingleLineTitle](../android/preference/Preference.md))`()` Gets whether the title of this preference is constrained to a single line. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyDependencyChange](../android/preference/Preference.md))`(`disableDependents:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Notifies any listening dependents of a change that affects the dependency. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDependencyChanged](../android/preference/Preference.md))`(`dependency:` ` [Preference](../android/preference/Preference.md)!`, `disableDependent:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Called when the dependency changes. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onParentChanged](../android/preference/Preference.md))`(`parent:` ` [Preference](../android/preference/Preference.md)!`, `disableChild:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Called when the implicit parent dependency changes. |
| open [Bundle](../android/os/Bundle.md)! | [peekExtras](../android/preference/Preference.md))`()` Return the extras Bundle object associated with this preference, returning`null`if there is not currently one. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [persistStringSet](../android/preference/Preference.md))`(`values:` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Attempts to persist a set of Strings if this Preference is persistent. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [restoreHierarchyState](../android/preference/Preference.md))`(`container:` ` [Bundle](../android/os/Bundle.md)!`)` Restore this Preference hierarchy's previously saved state from the given container. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [saveHierarchyState](../android/preference/Preference.md))`(`container:` ` [Bundle](../android/os/Bundle.md)!`)` Store this Preference hierarchy's frozen state into the given container. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDefaultValue](../android/preference/Preference.md))`(`defaultValue:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Sets the default value for this Preference, which will be set either if persistence is off or persistence is on and the preference is not found in the persistent storage. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDependency](../android/preference/Preference.md))`(`dependencyKey:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the key of a Preference that this Preference will depend on. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEnabled](../android/preference/Preference.md))`(`enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether this Preference is enabled. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFragment](../android/preference/Preference.md))`(`fragment:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the class name of a fragment to be shown when this Preference is clicked. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setIcon](../android/preference/Preference.md))`(`icon:` ` [Drawable](../android/graphics/drawable/Drawable.md)!`)` Sets the icon for this Preference with a Drawable. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setIcon](../android/preference/Preference.md))`(`iconResId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the icon for this Preference with a resource ID. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setIconSpaceReserved](../android/preference/Preference.md))`(`iconSpaceReserved:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether to reserve the space of this Preference icon view when no icon is provided. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setIntent](../android/preference/Preference.md))`(`intent:` ` [Intent](../android/content/Intent.md)!`)` Sets an [Intent](../android/content/Intent.md) to be used for [Context.startActivity(Intent)](../android/content/Context.md))when this Preference is clicked. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setKey](../android/preference/Preference.md))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the key for this Preference, which is used as a key to the [SharedPreferences](../android/content/SharedPreferences.md) or [PreferenceDataStore](../android/preference/PreferenceDataStore.md). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLayoutResource](../android/preference/Preference.md))`(`layoutResId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the layout resource that is inflated as the [View](../android/view/View.md) to be shown for this Preference. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnPreferenceChangeListener](../android/preference/Preference.md))`(`onPreferenceChangeListener:` ` [Preference.OnPreferenceChangeListener](../android/preference/Preference.OnPreferenceChangeListener.md)!`)` Sets the callback to be invoked when this Preference is changed by the user (but before the internal state has been updated). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnPreferenceClickListener](../android/preference/Preference.md))`(`onPreferenceClickListener:` ` [Preference.OnPreferenceClickListener](../android/preference/Preference.OnPreferenceClickListener.md)!`)` Sets the callback to be invoked when this Preference is clicked. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOrder](../android/preference/Preference.md))`(`order:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the order of this Preference with respect to other Preference objects on the same level. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPersistent](../android/preference/Preference.md))`(`persistent:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether this Preference is persistent. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPreferenceDataStore](../android/preference/Preference.md))`(`dataStore:` ` [PreferenceDataStore](../android/preference/PreferenceDataStore.md)!`)` Sets a [PreferenceDataStore](../android/preference/PreferenceDataStore.md) to be used by this Preference instead of using [android.content.SharedPreferences](../android/content/SharedPreferences.md). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRecycleEnabled](../android/preference/Preference.md))`(`enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether this Preference has enabled to have its view recycled when used in the list view. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSelectable](../android/preference/Preference.md))`(`selectable:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether this Preference is selectable. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setShouldDisableView](../android/preference/Preference.md))`(`shouldDisableView:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether this Preference should disable its view when it gets disabled. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSingleLineTitle](../android/preference/Preference.md))`(`singleLineTitle:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether to constrain the title of this Preference to a single line instead of letting it wrap onto multiple lines. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSummary](../android/preference/Preference.md))`(`summaryResId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the summary for this Preference with a resource ID. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSummary](../android/preference/Preference.md))`(`summary:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Sets the summary for this Preference with a CharSequence. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTitle](../android/preference/Preference.md))`(`titleResId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the title for this Preference with a resource ID. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTitle](../android/preference/Preference.md))`(`title:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Sets the title for this Preference with a CharSequence. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setWidgetLayoutResource](../android/preference/Preference.md))`(`widgetLayoutResId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the layout for the controllable widget portion of this Preference. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [shouldCommit](../android/preference/Preference.md))`()` Returns whether the [Preference](../android/preference/Preference.md) should commit its saved value(s) in [getEditor()](../android/preference/Preference.md)). |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [shouldDisableDependents](../android/preference/Preference.md))`()` Checks whether this preference's dependents should currently be disabled. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/preference/Preference.md))`()` <br /> |

| Protected methods ||
|--------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [callChangeListener](../android/preference/Preference.md))`(`newValue:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Call this method after the user changes the preference, but before the internal state is set. |
| open [Preference](../android/preference/Preference.md)! | [findPreferenceInHierarchy](../android/preference/Preference.md))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Finds a Preference in this hierarchy (the whole thing, even above/below your [PreferenceScreen](../android/preference/PreferenceScreen.md) screen break) with the given key. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getPersistedBoolean](../android/preference/Preference.md))`(`defaultReturnValue:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Attempts to get a persisted boolean if this Preference is persistent. |
| --- | --- |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getPersistedFloat](../android/preference/Preference.md))`(`defaultReturnValue:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Attempts to get a persisted float if this Preference is persistent. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPersistedInt](../android/preference/Preference.md))`(`defaultReturnValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Attempts to get a persisted int if this Preference is persistent. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getPersistedLong](../android/preference/Preference.md))`(`defaultReturnValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Attempts to get a persisted long if this Preference is persistent. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getPersistedString](../android/preference/Preference.md))`(`defaultReturnValue:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Attempts to get a persisted String if this Preference is persistent. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyChanged](../android/preference/Preference.md))`()` Should be called when the data of this [Preference](../android/preference/Preference.md) has changed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyHierarchyChanged](../android/preference/Preference.md))`()` Should be called when a Preference has been added/removed from this group, or the ordering should be re-evaluated. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAttachedToActivity](../android/preference/Preference.md))`()` Called when the Preference hierarchy has been attached to the [PreferenceActivity](../android/preference/PreferenceActivity.md). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAttachedToHierarchy](../android/preference/Preference.md))`(`preferenceManager:` ` [PreferenceManager](../android/preference/PreferenceManager.md)!`)` Called when this Preference has been attached to a Preference hierarchy. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onBindView](../android/preference/Preference.md))`(`view:` ` [View](../android/view/View.md)!`)` Binds the created View to the data for this Preference. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onClick](../android/preference/Preference.md))`()` Processes a click on the preference. |
| open [View](../android/view/View.md)! | [onCreateView](../android/preference/Preference.md))`(`parent:` ` [ViewGroup](../android/view/ViewGroup.md)!`)` Creates the View to be shown for this Preference in the [PreferenceActivity](../android/preference/PreferenceActivity.md). |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [onGetDefaultValue](../android/preference/Preference.md))`(`a:` ` [TypedArray](../android/content/res/TypedArray.md)!`, `index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when a Preference is being inflated and the default value attribute needs to be read. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPrepareForRemoval](../android/preference/Preference.md))`()` Called when this Preference is being removed from the hierarchy. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onRestoreInstanceState](../android/preference/Preference.md))`(`state:` ` [Parcelable](../android/os/Parcelable.md)!`)` Hook allowing a Preference to re-apply a representation of its internal state that had previously been generated by [onSaveInstanceState](../android/preference/Preference.md)). |
| open [Parcelable](../android/os/Parcelable.md)! | [onSaveInstanceState](../android/preference/Preference.md))`()` Hook allowing a Preference to generate a representation of its internal state that can later be used to create a new instance with that same state. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSetInitialValue](../android/preference/Preference.md))`(`restorePersistedValue:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `defaultValue:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Implement this to set the initial value of the Preference. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [persistBoolean](../android/preference/Preference.md))`(`value:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Attempts to persist a boolean if this Preference is persistent. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [persistFloat](../android/preference/Preference.md))`(`value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Attempts to persist a long if this Preference is persistent. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [persistInt](../android/preference/Preference.md))`(`value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Attempts to persist an int if this Preference is persistent. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [persistLong](../android/preference/Preference.md))`(`value:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Attempts to persist a long if this Preference is persistent. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [persistString](../android/preference/Preference.md))`(`value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Attempts to persist a String if this Preference is persistent. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [shouldPersist](../android/preference/Preference.md))`()` Checks whether, at the given time this method is called, this Preference should store/restore its value(s) into the [SharedPreferences](../android/content/SharedPreferences.md) or into [PreferenceDataStore](../android/preference/PreferenceDataStore.md) if assigned. |

## XML attributes

### android:defaultValue

```
android:defaultValue
```
The default value for the preference, which will be set either if persistence is off or persistence is on and the preference is not found in the persistent storage.

May be a reference to another resource, in the form "`@[+][`*package* `:]`*type* `/`*name*" or a theme attribute in the form "`?[`*package* `:]`*type* `/`*name*".

May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character;

May be an integer value, such as "`100`".

May be a boolean value, such as "`true`" or "`false`".

May be a floating point value, such as "`1.2`". 

### android:dependency

```
android:dependency
```
The key of another Preference that this Preference will depend on. If the other Preference is not set or is off, this Preference will be disabled.

May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character; 

### android:enabled

```
android:enabled
```
Whether the Preference is enabled.

May be a boolean value, such as "`true`" or "`false`". 

### android:fragment

```
android:fragment
```
When used inside of a modern PreferenceActivity, this declares a new PreferenceFragment to be shown when the user selects this item.

May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character; 

### android:icon

```
android:icon
```
The optional icon for the preference.

May be a reference to another resource, in the form "`@[+][`*package* `:]`*type* `/`*name*" or a theme attribute in the form "`?[`*package* `:]`*type* `/`*name*". 

### android:iconSpaceReserved

```
android:iconSpaceReserved
```
Whether the space for the preference icon view will be reserved. By default, preference icon view visibility will be set to GONE when there is no icon provided, so the default value of this attribute is false.

May be a boolean value, such as "`true`" or "`false`". 

### android:key

```
android:key
```
The key to store the Preference value.

May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character; 

### android:layout

```
android:layout
```
The layout for the Preference in a PreferenceActivity screen. This should rarely need to be changed, look at widgetLayout instead.

May be a reference to another resource, in the form "`@[+][`*package* `:]`*type* `/`*name*" or a theme attribute in the form "`?[`*package* `:]`*type* `/`*name*". 

### android:order

```
android:order
```
The order for the Preference (lower values are to be ordered first). If this is not specified, the default ordering will be alphabetic.

May be an integer value, such as "`100`". 

### android:persistent

```
android:persistent
```
Whether the Preference stores its value to the storage.

May be a boolean value, such as "`true`" or "`false`". 

### android:recycleEnabled

```
android:recycleEnabled
```
Whether the preference has enabled to have its view recycled when used in the list view. This is true by default.

May be a boolean value, such as "`true`" or "`false`". 

### android:selectable

```
android:selectable
```
Whether the Preference is selectable.

May be a boolean value, such as "`true`" or "`false`". 

### android:shouldDisableView

```
android:shouldDisableView
```
Whether the view of this Preference should be disabled when this Preference is disabled.

May be a boolean value, such as "`true`" or "`false`". 

### android:singleLineTitle

```
android:singleLineTitle
```
Whether to use single line for the preference title text. By default, preference title will be constrained to one line, so the default value of this attribute is true.

May be a boolean value, such as "`true`" or "`false`". 

### android:summary

```
android:summary
```
The summary for the Preference. In API 25 and earlier, this value is read as a plain string with styling information stripped.

May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character; 

### android:title

```
android:title
```
The title for the Preference. In API 25 and earlier, this value is read as a plain string with styling information stripped.

May be a string value, using '\\\\;' to escape characters such as '\\\\n' or '\\\\uxxxx' for a unicode character; 

### android:widgetLayout

```
android:widgetLayout
```
The layout for the controllable widget portion of a Preference. This is inflated into the layout for a Preference and should be used more frequently than the layout attribute. For example, a checkbox preference would specify a custom layout (consisting of just the CheckBox) here.

May be a reference to another resource, in the form "`@[+][`*package* `:]`*type* `/`*name*" or a theme attribute in the form "`?[`*package* `:]`*type* `/`*name*".

## Constants

### DEFAULT_ORDER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEFAULT_ORDER: Int
```

**Deprecated:** *Deprecated in Java.*

Specify for [setOrder(int)](../android/preference/Preference.md))if a specific order is not required. 

 Value: 2147483647

## Public constructors

### Preference

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Preference(context: Context!)
```

Constructor to create a Preference.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md)!:The Context in which to store Preference values. |

### Preference

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Preference(
    context: Context!, 
    attrs: AttributeSet!)
```

Constructor that is called when inflating a Preference from XML. This is called when a Preference is being constructed from an XML file, supplying attributes that were specified in the XML file. This version uses a default style of 0, so the only attribute values applied are those in the Context's Theme and the given AttributeSet.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md)!:The Context this is associated with, through which it can access the current theme, resources, [SharedPreferences](../android/content/SharedPreferences.md), etc. |
| `attrs` | [AttributeSet](../android/util/AttributeSet.md)!:The attributes of the XML tag that is inflating the preference. |

**See Also**

- [#Preference(Context, AttributeSet, int)](../android/preference/Preference.md)) 

### Preference

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Preference(
    context: Context!, 
    attrs: AttributeSet!, 
    defStyleAttr: Int)
```

Perform inflation from XML and apply a class-specific base style. This constructor of Preference allows subclasses to use their own base style when they are inflating. For example, a [CheckBoxPreference](../android/preference/CheckBoxPreference.md) constructor calls this version of the super class constructor and supplies`android.R.attr.checkBoxPreferenceStyle`for defStyleAttr. This allows the theme's checkbox preference style to modify all of the base preference attributes as well as the [CheckBoxPreference](../android/preference/CheckBoxPreference.md) class's attributes.

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md)!:The Context this is associated with, through which it can access the current theme, resources, [SharedPreferences](../android/content/SharedPreferences.md), etc. |
| `attrs` | [AttributeSet](../android/util/AttributeSet.md)!:The attributes of the XML tag that is inflating the preference. |
| `defStyleAttr` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):An attribute in the current theme that contains a reference to a style resource that supplies default values for the view. Can be 0 to not look for defaults. |
| --- | --- |

**See Also**

- [#Preference(Context, AttributeSet)](../android/preference/Preference.md)) 

### Preference

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Preference(
    context: Context!, 
    attrs: AttributeSet!, 
    defStyleAttr: Int, 
    defStyleRes: Int)
```

Perform inflation from XML and apply a class-specific base style. This constructor of Preference allows subclasses to use their own base style when they are inflating. For example, a [CheckBoxPreference](../android/preference/CheckBoxPreference.md) constructor calls this version of the super class constructor and supplies`android.R.attr.checkBoxPreferenceStyle`for defStyleAttr. This allows the theme's checkbox preference style to modify all of the base preference attributes as well as the [CheckBoxPreference](../android/preference/CheckBoxPreference.md) class's attributes.

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md)!:The Context this is associated with, through which it can access the current theme, resources, [SharedPreferences](../android/content/SharedPreferences.md), etc. |
| `attrs` | [AttributeSet](../android/util/AttributeSet.md)!:The attributes of the XML tag that is inflating the preference. |
| `defStyleAttr` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):An attribute in the current theme that contains a reference to a style resource that supplies default values for the view. Can be 0 to not look for defaults. |
| --- | --- |
| `defStyleRes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A resource identifier of a style resource that supplies default values for the view, used only if defStyleAttr is 0 or can not be found in the theme. Can be 0 to not look for defaults. |

**See Also**

- [#Preference(Context, AttributeSet)](../android/preference/Preference.md))

## Public methods

### compareTo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun compareTo(other: Preference!): Int
```

**Deprecated:** *Deprecated in Java.*

Compares Preference objects based on order (if set), otherwise alphabetically on the titles.

| Parameters ||
|-----------|----------------------------------------|
| `o` | the object to be compared. |
| `another` | The Preference to compare to this one. |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | 0 if the same; less than 0 if this Preference sorts ahead of another; greater than 0 if this Preference sorts after another. |

| Exceptions ||
|----------------------------------|--------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the specified object is null |
| `java.lang.ClassCastException` | if the specified object's type prevents it from being compared to this object. |

### getContext

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getContext(): Context!
```

**Deprecated:** *Deprecated in Java.*

Returns the [android.content.Context](../android/content/Context.md) of this Preference. Each Preference in a Preference hierarchy can be from different Context (for example, if multiple activities provide preferences into a single [PreferenceActivity](../android/preference/PreferenceActivity.md)). This Context will be used to save the Preference values.

| Return ||
|------------------------------------------------------------------------------------------|---------------------------------|
| [Context](../android/content/Context.md)! | The Context of this Preference. |

### getDependency

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDependency(): String!
```

**Deprecated:** *Deprecated in Java.*

Returns the key of the dependency on this Preference.

| Return ||
|-----------------------------------------------------------------------------------|----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The key of the dependency. |

**See Also**

- [#setDependency(String)](../android/preference/Preference.md)) 

### getEditor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEditor(): SharedPreferences.Editor!
```

**Deprecated:** *Deprecated in Java.*

Returns an [SharedPreferences.Editor](../android/content/SharedPreferences.Editor.md) where this Preference can save its value(s). Usually it's easier to use one of the helper save methods: [persistBoolean(boolean)](../android/preference/Preference.md)), [persistFloat(float)](../android/preference/Preference.md)), [persistInt(int)](../android/preference/Preference.md)), [persistLong(long)](../android/preference/Preference.md)), [persistString(java.lang.String)](../android/preference/Preference.md)). To read values, see [getSharedPreferences()](../android/preference/Preference.md)). If [shouldCommit()](../android/preference/Preference.md))returns true, it is this Preference's responsibility to commit.

In some cases, writes to this will not be committed right away and hence not show up in the SharedPreferences, this is intended behavior to improve performance.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [SharedPreferences.Editor](../android/content/SharedPreferences.Editor.md)! | a [SharedPreferences.Editor](../android/content/SharedPreferences.Editor.md) where this preference saves its value(s). If this preference isn't attached to a Preference hierarchy or if a [PreferenceDataStore](../android/preference/PreferenceDataStore.md) has been set, this method returns`null`. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/preference/Preference#shouldCommit()>
- <https://developer.android.com/reference/kotlin/android/preference/Preference#getSharedPreferences()>
- [#setPreferenceDataStore(PreferenceDataStore)](../android/preference/Preference.md)) 

### getExtras

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getExtras(): Bundle!
```

**Deprecated:** *Deprecated in Java.*

Return the extras Bundle object associated with this preference, creating a new Bundle if there currently isn't one. You can use this to get and set individual extra key/value pairs. 

### getFragment

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFragment(): String!
```

**Deprecated:** *Deprecated in Java.*

Return the fragment class name associated with this Preference.

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The fragment class name last set via [setFragment](../android/preference/Preference.md))or XML. |

### getIcon

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getIcon(): Drawable!
```

**Deprecated:** *Deprecated in Java.*

Returns the icon of this Preference.

| Return ||
|------------------------------------------------------------------------------------------------------|----------|
| [Drawable](../android/graphics/drawable/Drawable.md)! | the icon |

**See Also**

- [#setIcon(Drawable)](../android/preference/Preference.md)) 

### getIntent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getIntent(): Intent!
```

**Deprecated:** *Deprecated in Java.*

Return the [Intent](../android/content/Intent.md) associated with this Preference.

| Return ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Intent](../android/content/Intent.md)! | The [Intent](../android/content/Intent.md) last set via [setIntent(android.content.Intent)](../android/preference/Preference.md))or XML. |

### getKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getKey(): String!
```

**Deprecated:** *Deprecated in Java.*

Gets the key for this Preference, which is also the key used for storing values into [SharedPreferences](../android/content/SharedPreferences.md) or [PreferenceDataStore](../android/preference/PreferenceDataStore.md).

| Return ||
|-----------------------------------------------------------------------------------|----------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The key. |

### getLayoutResource

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLayoutResource(): Int
```

**Deprecated:** *Deprecated in Java.*

Gets the layout resource that will be shown as the [View](../android/view/View.md) for this Preference.

| Return ||
|----------------------------------------------------------------------------|-------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The layout resource ID. |

### getOnPreferenceChangeListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getOnPreferenceChangeListener(): Preference.OnPreferenceChangeListener!
```

**Deprecated:** *Deprecated in Java.*

Returns the callback to be invoked when this Preference is changed by the user (but before the internal state has been updated).

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [Preference.OnPreferenceChangeListener](../android/preference/Preference.OnPreferenceChangeListener.md)! | The callback to be invoked. |

### getOnPreferenceClickListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getOnPreferenceClickListener(): Preference.OnPreferenceClickListener!
```

**Deprecated:** *Deprecated in Java.*

Returns the callback to be invoked when this Preference is clicked.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [Preference.OnPreferenceClickListener](../android/preference/Preference.OnPreferenceClickListener.md)! | The callback to be invoked. |

### getOrder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getOrder(): Int
```

**Deprecated:** *Deprecated in Java.*

Gets the order of this Preference with respect to other Preference objects on the same level.

| Return ||
|----------------------------------------------------------------------------|------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the order of this Preference |

**See Also**

- [#setOrder(int)](../android/preference/Preference.md)) 

### getParent

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getParent(): PreferenceGroup?
```

**Deprecated:** *Deprecated in Java.*

Returns the [PreferenceGroup](../android/preference/PreferenceGroup.md) which is this Preference assigned to or`null`if this preference is not assigned to any group or is a root Preference.

| Return ||
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [PreferenceGroup](../android/preference/PreferenceGroup.md)? | the parent PreferenceGroup or`null`if not attached to any |

### getPersistedStringSet

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPersistedStringSet(defaultReturnValue: MutableSet<String!>!): MutableSet<String!>!
```

**Deprecated:** *Deprecated in Java.*

Attempts to get a persisted set of Strings if this Preference is persistent.

| Parameters ||
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `defaultReturnValue` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:The default value to return if either this Preference is not persistent or this Preference is not present. |

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | The value from the data store or the default return value. |

**See Also**

- [#persistStringSet(Set)](../android/preference/Preference.md)) 

### getPreferenceDataStore

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPreferenceDataStore(): PreferenceDataStore?
```

**Deprecated:** *Deprecated in Java.*

Returns [PreferenceDataStore](../android/preference/PreferenceDataStore.md) used by this Preference. Returns`null`if [android.content.SharedPreferences](../android/content/SharedPreferences.md) is used instead.

By default preferences always use [android.content.SharedPreferences](../android/content/SharedPreferences.md). To make this preference to use the [PreferenceDataStore](../android/preference/PreferenceDataStore.md) you need to assign your implementation to the Preference itself via [setPreferenceDataStore(android.preference.PreferenceDataStore)](../android/preference/Preference.md))or to its [PreferenceManager](../android/preference/PreferenceManager.md) via [PreferenceManager.setPreferenceDataStore(PreferenceDataStore)](../android/preference/PreferenceManager.md)).

| Return ||
|---------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [PreferenceDataStore](../android/preference/PreferenceDataStore.md)? | The [PreferenceDataStore](../android/preference/PreferenceDataStore.md) used by this Preference or`null`if none. |

### getPreferenceManager

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPreferenceManager(): PreferenceManager!
```

**Deprecated:** *Deprecated in Java.*

Gets the [PreferenceManager](../android/preference/PreferenceManager.md) that manages this Preference object's tree.

| Return ||
|-----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [PreferenceManager](../android/preference/PreferenceManager.md)! | The [PreferenceManager](../android/preference/PreferenceManager.md). |

### getSharedPreferences

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSharedPreferences(): SharedPreferences!
```

**Deprecated:** *Deprecated in Java.*

Returns the [SharedPreferences](../android/content/SharedPreferences.md) where this Preference can read its value(s). Usually, it's easier to use one of the helper read methods: [getPersistedBoolean(boolean)](../android/preference/Preference.md)), [getPersistedFloat(float)](../android/preference/Preference.md)), [getPersistedInt(int)](../android/preference/Preference.md)), [getPersistedLong(long)](../android/preference/Preference.md)), [getPersistedString(java.lang.String)](../android/preference/Preference.md)). To save values, see [getEditor()](../android/preference/Preference.md)).

In some cases, writes to the [getEditor()](../android/preference/Preference.md))will not be committed right away and hence not show up in the returned [SharedPreferences](../android/content/SharedPreferences.md), this is intended behavior to improve performance.

| Return ||
|--------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [SharedPreferences](../android/content/SharedPreferences.md)! | the [SharedPreferences](../android/content/SharedPreferences.md) where this Preference reads its value(s). If this preference isn't attached to a Preference hierarchy or if a [PreferenceDataStore](../android/preference/PreferenceDataStore.md) has been set, this method returns`null`. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/preference/Preference#getEditor()>
- [#setPreferenceDataStore(PreferenceDataStore)](../android/preference/Preference.md)) 

### getShouldDisableView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getShouldDisableView(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Checks whether this Preference should disable its view when it's action is disabled.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if it should disable the view |

**See Also**

- [#setShouldDisableView(boolean)](../android/preference/Preference.md)) 

### getSummary

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSummary(): CharSequence!
```

**Deprecated:** *Deprecated in Java.*

Returns the summary of this Preference.

| Return ||
|------------------------------------------------------------------------------------------------|-------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | the summary |

**See Also**

- [#setSummary(CharSequence)](../android/preference/Preference.md)) 

### getTitle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTitle(): CharSequence!
```

**Deprecated:** *Deprecated in Java.*

Returns the title of this Preference.

| Return ||
|------------------------------------------------------------------------------------------------|-----------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | the title |

**See Also**

- [#setTitle(CharSequence)](../android/preference/Preference.md)) 

### getTitleRes

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTitleRes(): Int
```

**Deprecated:** *Deprecated in Java.*

Returns the title resource ID of this Preference. If the title did not come from a resource,`0`is returned.

| Return ||
|----------------------------------------------------------------------------|--------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the title resource |

**See Also**

- [#setTitle(int)](../android/preference/Preference.md)) 

### getView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getView(
    convertView: View!, 
    parent: ViewGroup!
): View!
```

**Deprecated:** *Deprecated in Java.*

Gets the View that will be shown in the [PreferenceActivity](../android/preference/PreferenceActivity.md).

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `convertView` | [View](../android/view/View.md)!:The old View to reuse, if possible. Note: You should check that this View is non-null and of an appropriate type before using. If it is not possible to convert this View to display the correct data, this method can create a new View. |
| `parent` | [ViewGroup](../android/view/ViewGroup.md)!:The parent that this View will eventually be attached to. |

| Return ||
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [View](../android/view/View.md)! | Returns the same Preference object, for chaining multiple calls into a single statement. |

**See Also**

- [#onCreateView(ViewGroup)](../android/preference/Preference.md))
- [#onBindView(View)](../android/preference/Preference.md)) 

### getWidgetLayoutResource

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getWidgetLayoutResource(): Int
```

**Deprecated:** *Deprecated in Java.*

Gets the layout resource for the controllable widget portion of this Preference.

| Return ||
|----------------------------------------------------------------------------|-------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The layout resource ID. |

### hasKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasKey(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Checks whether this Preference has a valid key.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the key exists and is not a blank string, false otherwise. |

### isEnabled

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isEnabled(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Checks whether this Preference should be enabled in the list.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this Preference is enabled, false otherwise |

### isIconSpaceReserved

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isIconSpaceReserved(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Gets whether the space this preference icon view is reserved.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the space of this preference icon view is reserved |

**See Also**

- [#setIconSpaceReserved(boolean)](../android/preference/Preference.md)) 

### isPersistent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isPersistent(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Checks whether this Preference is persistent. If it is, it stores its value(s) into the persistent [SharedPreferences](../android/content/SharedPreferences.md) storage by default or into [PreferenceDataStore](../android/preference/PreferenceDataStore.md) if assigned.

| Return ||
|------------------------------------------------------------------------------------|---------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if it is persistent. |

### isRecycleEnabled

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isRecycleEnabled(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Checks whether this Preference has enabled to have its view recycled when used in the list view.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this preference view should be recycled |

**See Also**

- [#setRecycleEnabled(boolean)](../android/preference/Preference.md)) 

### isSelectable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isSelectable(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Checks whether this Preference should be selectable in the list.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if it is selectable,`false`otherwise |

### isSingleLineTitle

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isSingleLineTitle(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Gets whether the title of this preference is constrained to a single line.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the title of this preference is constrained to a single line |

**See Also**

- [#setSingleLineTitle(boolean)](../android/preference/Preference.md)) 

### notifyDependencyChange

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun notifyDependencyChange(disableDependents: Boolean): Unit
```

**Deprecated:** *Deprecated in Java.*

Notifies any listening dependents of a change that affects the dependency.

| Parameters ||
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `disableDependents` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Whether this Preference should disable its dependents. |

### onDependencyChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onDependencyChanged(
    dependency: Preference!, 
    disableDependent: Boolean
): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when the dependency changes.

| Parameters ||
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `dependency` | [Preference](../android/preference/Preference.md)!:The Preference that this Preference depends on. |
| `disableDependent` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Set true to disable this Preference. |

### onParentChanged

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onParentChanged(
    parent: Preference!, 
    disableChild: Boolean
): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when the implicit parent dependency changes.

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `parent` | [Preference](../android/preference/Preference.md)!:The Preference that this Preference depends on. |
| `disableChild` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Set true to disable this Preference. |

### peekExtras

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun peekExtras(): Bundle!
```

**Deprecated:** *Deprecated in Java.*

Return the extras Bundle object associated with this preference, returning`null`if there is not currently one. 

### persistStringSet

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun persistStringSet(values: MutableSet<String!>!): Boolean
```

**Deprecated:** *Deprecated in Java.*

Attempts to persist a set of Strings if this Preference is persistent.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `values` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:The values to persist. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if this Preference is persistent. (This is not whether the value was persisted, since we may not necessarily commit if there will be a batch commit later.) |

**See Also**

- [#getPersistedStringSet(Set)](../android/preference/Preference.md)) 

### restoreHierarchyState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun restoreHierarchyState(container: Bundle!): Unit
```

**Deprecated:** *Deprecated in Java.*

Restore this Preference hierarchy's previously saved state from the given container.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------|
| `container` | [Bundle](../android/os/Bundle.md)!:The Bundle that holds the previously saved state. |

**See Also**

- [#saveHierarchyState](../android/preference/Preference.md))
- [#onRestoreInstanceState](../android/preference/Preference.md)) 

### saveHierarchyState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun saveHierarchyState(container: Bundle!): Unit
```

**Deprecated:** *Deprecated in Java.*

Store this Preference hierarchy's frozen state into the given container.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `container` | [Bundle](../android/os/Bundle.md)!:The Bundle in which to save the instance of this Preference. |

**See Also**

- [#restoreHierarchyState](../android/preference/Preference.md))
- [#onSaveInstanceState](../android/preference/Preference.md)) 

### setDefaultValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDefaultValue(defaultValue: Any!): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the default value for this Preference, which will be set either if persistence is off or persistence is on and the preference is not found in the persistent storage.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------|
| `defaultValue` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:The default value. |

### setDependency

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDependency(dependencyKey: String!): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the key of a Preference that this Preference will depend on. If that Preference is not set or is off, this Preference will be disabled.

| Parameters ||
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------|
| `dependencyKey` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The key of the Preference that this depends on. |

### setEnabled

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setEnabled(enabled: Boolean): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets whether this Preference is enabled. If disabled, it will not handle clicks.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------|
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):set`true`to enable it |

### setFragment

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setFragment(fragment: String!): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the class name of a fragment to be shown when this Preference is clicked.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `fragment` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The class name of the fragment associated with this Preference. |

### setIcon

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setIcon(icon: Drawable!): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the icon for this Preference with a Drawable. This icon will be placed into the ID [android.R.id#icon](../android/R.id.md) within the View created by [onCreateView(android.view.ViewGroup)](../android/preference/Preference.md)).

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `icon` | [Drawable](../android/graphics/drawable/Drawable.md)!:the optional icon for this Preference |

### setIcon

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setIcon(iconResId: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the icon for this Preference with a resource ID.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------|
| `iconResId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the icon as a resource ID |

**See Also**

- [#setIcon(Drawable)](../android/preference/Preference.md)) 

### setIconSpaceReserved

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setIconSpaceReserved(iconSpaceReserved: Boolean): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets whether to reserve the space of this Preference icon view when no icon is provided.

| Parameters ||
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `iconSpaceReserved` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):set`true`if the space for the icon view should be reserved |

### setIntent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setIntent(intent: Intent!): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets an [Intent](../android/content/Intent.md) to be used for [Context.startActivity(Intent)](../android/content/Context.md))when this Preference is clicked.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------|
| `intent` | [Intent](../android/content/Intent.md)!:The intent associated with this Preference. |

### setKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setKey(key: String!): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the key for this Preference, which is used as a key to the [SharedPreferences](../android/content/SharedPreferences.md) or [PreferenceDataStore](../android/preference/PreferenceDataStore.md). This should be unique for the package.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The key for the preference. |

### setLayoutResource

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setLayoutResource(layoutResId: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the layout resource that is inflated as the [View](../android/view/View.md) to be shown for this Preference. In most cases, the default layout is sufficient for custom Preference objects and only the widget layout needs to be changed.

This layout should contain a [ViewGroup](../android/view/ViewGroup.md) with ID [android.R.id#widget_frame](../android/R.id.md) to be the parent of the specific widget for this Preference. It should similarly contain [android.R.id#title](../android/R.id.md) and [android.R.id#summary](../android/R.id.md).

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `layoutResId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The layout resource ID to be inflated and returned as a [View](../android/view/View.md). |

**See Also**

- [#setWidgetLayoutResource(int)](../android/preference/Preference.md)) 

### setOnPreferenceChangeListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOnPreferenceChangeListener(onPreferenceChangeListener: Preference.OnPreferenceChangeListener!): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the callback to be invoked when this Preference is changed by the user (but before the internal state has been updated).

| Parameters ||
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `onPreferenceChangeListener` | [Preference.OnPreferenceChangeListener](../android/preference/Preference.OnPreferenceChangeListener.md)!:The callback to be invoked. |

### setOnPreferenceClickListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOnPreferenceClickListener(onPreferenceClickListener: Preference.OnPreferenceClickListener!): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the callback to be invoked when this Preference is clicked.

| Parameters ||
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `onPreferenceClickListener` | [Preference.OnPreferenceClickListener](../android/preference/Preference.OnPreferenceClickListener.md)!:The callback to be invoked. |

### setOrder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOrder(order: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the order of this Preference with respect to other Preference objects on the same level. If this is not specified, the default behavior is to sort alphabetically. The [PreferenceGroup.setOrderingAsAdded(boolean)](../android/preference/PreferenceGroup.md))can be used to order Preference objects based on the order they appear in the XML.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `order` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the order for this Preference. A lower value will be shown first. Use [DEFAULT_ORDER](../android/preference/Preference.md) to sort alphabetically or allow ordering from XML |

**See Also**

- [android.preference.PreferenceGroup#setOrderingAsAdded(boolean)](../android/preference/PreferenceGroup.md))
- [#DEFAULT_ORDER](../android/preference/Preference.md) 

### setPersistent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPersistent(persistent: Boolean): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets whether this Preference is persistent. When persistent, it stores its value(s) into the persistent [SharedPreferences](../android/content/SharedPreferences.md) storage by default or into [PreferenceDataStore](../android/preference/PreferenceDataStore.md) if assigned.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `persistent` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):set`true`if it should store its value(s) into the storage. |

### setPreferenceDataStore

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPreferenceDataStore(dataStore: PreferenceDataStore!): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets a [PreferenceDataStore](../android/preference/PreferenceDataStore.md) to be used by this Preference instead of using [android.content.SharedPreferences](../android/content/SharedPreferences.md).

The data store will remain assigned even if the Preference is moved around the preference hierarchy. It will also override a data store propagated from the [PreferenceManager](../android/preference/PreferenceManager.md) that owns this Preference.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dataStore` | [PreferenceDataStore](../android/preference/PreferenceDataStore.md)!:The [PreferenceDataStore](../android/preference/PreferenceDataStore.md) to be used by this Preference. |

**See Also**

- [android.preference.PreferenceManager#setPreferenceDataStore(PreferenceDataStore)](../android/preference/PreferenceManager.md)) 

### setRecycleEnabled

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setRecycleEnabled(enabled: Boolean): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets whether this Preference has enabled to have its view recycled when used in the list view. By default the recycling is enabled.

The value can be changed only before this preference is added to the preference hierarchy.

If view recycling is not allowed then each time the list view populates this preference the [getView(android.view.View,android.view.ViewGroup)](../android/preference/Preference.md))method receives a`null`convert view and needs to recreate the view. Otherwise view gets recycled and only [onBindView(android.view.View)](../android/preference/Preference.md))gets called. 
If you override this method you*must*call through to the superclass implementation.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------|
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):set`true`if this preference view should be recycled |

### setSelectable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSelectable(selectable: Boolean): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets whether this Preference is selectable.

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------|
| `selectable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):set`true`to make it selectable |

### setShouldDisableView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setShouldDisableView(shouldDisableView: Boolean): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets whether this Preference should disable its view when it gets disabled.

For example, set this and [setEnabled(boolean)](../android/preference/Preference.md))to false for preferences that are only displaying information and 1) should not be clickable 2) should not have the view set to the disabled state.

| Parameters ||
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `shouldDisableView` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):set`true`if this preference should disable its view when the preference is disabled |

### setSingleLineTitle

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSingleLineTitle(singleLineTitle: Boolean): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets whether to constrain the title of this Preference to a single line instead of letting it wrap onto multiple lines.

| Parameters ||
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `singleLineTitle` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):set`true`if the title should be constrained to one line |

### setSummary

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSummary(summaryResId: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the summary for this Preference with a resource ID.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------|
| `summaryResId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the summary as a resource |

**See Also**

- [#setSummary(CharSequence)](../android/preference/Preference.md)) 

### setSummary

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSummary(summary: CharSequence!): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the summary for this Preference with a CharSequence.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------|
| `summary` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the summary for the preference |

### setTitle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTitle(titleResId: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the title for this Preference with a resource ID.

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------|
| `titleResId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the title as a resource ID |

**See Also**

- [#setTitle(CharSequence)](../android/preference/Preference.md)) 

### setTitle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTitle(title: CharSequence!): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the title for this Preference with a CharSequence. This title will be placed into the ID [android.R.id#title](../android/R.id.md) within the View created by [onCreateView(android.view.ViewGroup)](../android/preference/Preference.md)).

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------|
| `title` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the title for this Preference |

### setWidgetLayoutResource

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setWidgetLayoutResource(widgetLayoutResId: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the layout for the controllable widget portion of this Preference. This is inflated into the main layout. For example, a [CheckBoxPreference](../android/preference/CheckBoxPreference.md) would specify a custom layout (consisting of just the CheckBox) here, instead of creating its own main layout.

| Parameters ||
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| `widgetLayoutResId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The layout resource ID to be inflated into the main layout. |

**See Also**

- [#setLayoutResource(int)](../android/preference/Preference.md)) 

### shouldCommit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun shouldCommit(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Returns whether the [Preference](../android/preference/Preference.md) should commit its saved value(s) in [getEditor()](../android/preference/Preference.md)). This may return false in situations where batch committing is being done (by the manager) to improve performance.

If this preference is using [PreferenceDataStore](../android/preference/PreferenceDataStore.md) this value is irrelevant.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Whether the Preference should commit its saved value(s). |

**See Also**

- <https://developer.android.com/reference/kotlin/android/preference/Preference#getEditor()> 

### shouldDisableDependents

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun shouldDisableDependents(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Checks whether this preference's dependents should currently be disabled.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the dependents should be disabled, otherwise false. |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

## Protected methods

### callChangeListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun callChangeListener(newValue: Any!): Boolean
```

**Deprecated:** *Deprecated in Java.*

Call this method after the user changes the preference, but before the internal state is set. This allows the client to ignore the user value.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------|
| `newValue` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:The new value of this Preference. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the user value should be set as the preference value (and persisted). |

### findPreferenceInHierarchy

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun findPreferenceInHierarchy(key: String!): Preference!
```

**Deprecated:** *Deprecated in Java.*

Finds a Preference in this hierarchy (the whole thing, even above/below your [PreferenceScreen](../android/preference/PreferenceScreen.md) screen break) with the given key.

This only functions after we have been attached to a hierarchy.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The key of the Preference to find. |

| Return ||
|----------------------------------------------------------------------------------------------|-----------------------------------------|
| [Preference](../android/preference/Preference.md)! | The Preference that uses the given key. |

### getPersistedBoolean

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun getPersistedBoolean(defaultReturnValue: Boolean): Boolean
```

**Deprecated:** *Deprecated in Java.*

Attempts to get a persisted boolean if this Preference is persistent.

| Parameters ||
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `defaultReturnValue` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):The default value to return if either this Preference is not persistent or this Preference is not present. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | The value from the data store or the default return value. |

**See Also**

- [#getPersistedString(String)](../android/preference/Preference.md))
- [#persistBoolean(boolean)](../android/preference/Preference.md)) 

### getPersistedFloat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun getPersistedFloat(defaultReturnValue: Float): Float
```

**Deprecated:** *Deprecated in Java.*

Attempts to get a persisted float if this Preference is persistent.

| Parameters ||
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `defaultReturnValue` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The default value to return if either this Preference is not persistent or this Preference is not present. |

| Return ||
|--------------------------------------------------------------------------------|------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | The value from the data store or the default return value. |

**See Also**

- [#getPersistedString(String)](../android/preference/Preference.md))
- [#persistFloat(float)](../android/preference/Preference.md)) 

### getPersistedInt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun getPersistedInt(defaultReturnValue: Int): Int
```

**Deprecated:** *Deprecated in Java.*

Attempts to get a persisted int if this Preference is persistent.

| Parameters ||
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `defaultReturnValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The default value to return if either this Preference is not persistent or this Preference is not present. |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The value from the data store or the default return value. |

**See Also**

- [#getPersistedString(String)](../android/preference/Preference.md))
- [#persistInt(int)](../android/preference/Preference.md)) 

### getPersistedLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun getPersistedLong(defaultReturnValue: Long): Long
```

**Deprecated:** *Deprecated in Java.*

Attempts to get a persisted long if this Preference is persistent.

| Parameters ||
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `defaultReturnValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The default value to return if either this Preference is not persistent or this Preference is not present. |

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The value from the data store or the default return value. |

**See Also**

- [#getPersistedString(String)](../android/preference/Preference.md))
- [#persistLong(long)](../android/preference/Preference.md)) 

### getPersistedString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun getPersistedString(defaultReturnValue: String!): String!
```

**Deprecated:** *Deprecated in Java.*

Attempts to get a persisted String if this Preference is persistent.

| Parameters ||
|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `defaultReturnValue` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The default value to return if either this Preference is not persistent or this Preference is not present. |

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The value from the data store or the default return value. |

**See Also**

- [#persistString(String)](../android/preference/Preference.md)) 

### notifyChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun notifyChanged(): Unit
```

**Deprecated:** *Deprecated in Java.*

Should be called when the data of this [Preference](../android/preference/Preference.md) has changed. 

### notifyHierarchyChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun notifyHierarchyChanged(): Unit
```

**Deprecated:** *Deprecated in Java.*

Should be called when a Preference has been added/removed from this group, or the ordering should be re-evaluated. 

### onAttachedToActivity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onAttachedToActivity(): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when the Preference hierarchy has been attached to the [PreferenceActivity](../android/preference/PreferenceActivity.md). This can also be called when this Preference has been attached to a group that was already attached to the [PreferenceActivity](../android/preference/PreferenceActivity.md). 

### onAttachedToHierarchy

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onAttachedToHierarchy(preferenceManager: PreferenceManager!): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when this Preference has been attached to a Preference hierarchy. Make sure to call the super implementation.

| Parameters ||
|---------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `preferenceManager` | [PreferenceManager](../android/preference/PreferenceManager.md)!:The PreferenceManager of the hierarchy. |

### onBindView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onBindView(view: View!): Unit
```

**Deprecated:** *Deprecated in Java.*

Binds the created View to the data for this Preference.

This is a good place to grab references to custom Views in the layout and set properties on them.

Make sure to call through to the superclass's implementation. 
If you override this method you*must*call through to the superclass implementation.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------|
| `view` | [View](../android/view/View.md)!:The View that shows this Preference. |

**See Also**

- [#onCreateView(ViewGroup)](../android/preference/Preference.md)) 

### onClick

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onClick(): Unit
```

**Deprecated:** *Deprecated in Java.*

Processes a click on the preference. This includes saving the value to the [SharedPreferences](../android/content/SharedPreferences.md). However, the overridden method should call [callChangeListener(java.lang.Object)](../android/preference/Preference.md))to make sure the client wants to update the preference's state with the new value. 

### onCreateView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onCreateView(parent: ViewGroup!): View!
```

**Deprecated:** *Deprecated in Java.*

Creates the View to be shown for this Preference in the [PreferenceActivity](../android/preference/PreferenceActivity.md). The default behavior is to inflate the main layout of this Preference (see [setLayoutResource(int)](../android/preference/Preference.md)). If changing this behavior, please specify a [ViewGroup](../android/view/ViewGroup.md) with ID [android.R.id#widget_frame](../android/R.id.md).

Make sure to call through to the superclass's implementation. 
If you override this method you*must*call through to the superclass implementation.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `parent` | [ViewGroup](../android/view/ViewGroup.md)!:The parent that this View will eventually be attached to. |

| Return ||
|---------------------------------------------------------------------------------|-----------------------------------------|
| [View](../android/view/View.md)! | The View that displays this Preference. |

**See Also**

- [#onBindView(View)](../android/preference/Preference.md)) 

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

For example, if the value type is String, the body of the method would proxy to [TypedArray.getString(int)](../android/content/res/TypedArray.md)).

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------|
| `a` | [TypedArray](../android/content/res/TypedArray.md)!:The set of attributes. |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index of the default value attribute. |

| Return ||
|-----------------------------------------------------------------------------|--------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | The default value of this preference type. |

### onPrepareForRemoval

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onPrepareForRemoval(): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when this Preference is being removed from the hierarchy. You should remove any references to this Preference that you know about. Make sure to call through to the superclass implementation. 
If you override this method you*must*call through to the superclass implementation. 

### onRestoreInstanceState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onRestoreInstanceState(state: Parcelable!): Unit
```

**Deprecated:** *Deprecated in Java.*

Hook allowing a Preference to re-apply a representation of its internal state that had previously been generated by [onSaveInstanceState](../android/preference/Preference.md)). This function will never be called with a`null`state.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `state` | [Parcelable](../android/os/Parcelable.md)!:The saved state that had previously been returned by [onSaveInstanceState](../android/preference/Preference.md)). |

**See Also**

- [#onSaveInstanceState](../android/preference/Preference.md))
- [#restoreHierarchyState](../android/preference/Preference.md)) 

### onSaveInstanceState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onSaveInstanceState(): Parcelable!
```

**Deprecated:** *Deprecated in Java.*

Hook allowing a Preference to generate a representation of its internal state that can later be used to create a new instance with that same state. This state should only contain information that is not persistent or can be reconstructed later.

| Return ||
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Parcelable](../android/os/Parcelable.md)! | A Parcelable object containing the current dynamic state of this Preference, or`null`if there is nothing interesting to save. The default implementation returns`null`. |

**See Also**

- [#onRestoreInstanceState](../android/preference/Preference.md))
- [#saveHierarchyState](../android/preference/Preference.md)) 

### onSetInitialValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onSetInitialValue(
    restorePersistedValue: Boolean, 
    defaultValue: Any!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Implement this to set the initial value of the Preference.

If restorePersistedValue is true, you should restore the Preference value from the [android.content.SharedPreferences](../android/content/SharedPreferences.md). If restorePersistedValue is false, you should set the Preference value to defaultValue that is given (and possibly store to SharedPreferences if [shouldPersist()](../android/preference/Preference.md))is true).

In case of using [PreferenceDataStore](../android/preference/PreferenceDataStore.md), the restorePersistedValue is always`true`. But the default value (if provided) is set.

This may not always be called. One example is if it should not persist but there is no default value given.

| Parameters ||
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `restorePersistedValue` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):True to restore the persisted value; false to use the given defaultValue. |
| `defaultValue` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:The default value for this Preference. Only use this if restorePersistedValue is false. |

### persistBoolean

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun persistBoolean(value: Boolean): Boolean
```

**Deprecated:** *Deprecated in Java.*

Attempts to persist a boolean if this Preference is persistent.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------|
| `value` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):The value to persist. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if this Preference is persistent. (This is not whether the value was persisted, since we may not necessarily commit if there will be a batch commit later.) |

**See Also**

- [#persistString(String)](../android/preference/Preference.md))
- [#getPersistedBoolean(boolean)](../android/preference/Preference.md)) 

### persistFloat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun persistFloat(value: Float): Boolean
```

**Deprecated:** *Deprecated in Java.*

Attempts to persist a long if this Preference is persistent.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------|
| `value` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The value to persist. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if this Preference is persistent. (This is not whether the value was persisted, since we may not necessarily commit if there will be a batch commit later.) |

**See Also**

- [#persistString(String)](../android/preference/Preference.md))
- [#getPersistedFloat(float)](../android/preference/Preference.md)) 

### persistInt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun persistInt(value: Int): Boolean
```

**Deprecated:** *Deprecated in Java.*

Attempts to persist an int if this Preference is persistent.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------|
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The value to persist. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if this Preference is persistent. (This is not whether the value was persisted, since we may not necessarily commit if there will be a batch commit later.) |

**See Also**

- [#persistString(String)](../android/preference/Preference.md))
- [#getPersistedInt(int)](../android/preference/Preference.md)) 

### persistLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun persistLong(value: Long): Boolean
```

**Deprecated:** *Deprecated in Java.*

Attempts to persist a long if this Preference is persistent.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------|
| `value` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The value to persist. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if this Preference is persistent. (This is not whether the value was persisted, since we may not necessarily commit if there will be a batch commit later.) |

**See Also**

- [#persistString(String)](../android/preference/Preference.md))
- [#getPersistedLong(long)](../android/preference/Preference.md)) 

### persistString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun persistString(value: String!): Boolean
```

**Deprecated:** *Deprecated in Java.*

Attempts to persist a String if this Preference is persistent.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------|
| `value` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The value to persist. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if this Preference is persistent. (This is not whether the value was persisted, since we may not necessarily commit if there will be a batch commit later.) |

**See Also**

- [#getPersistedString(String)](../android/preference/Preference.md)) 

### shouldPersist

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun shouldPersist(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Checks whether, at the given time this method is called, this Preference should store/restore its value(s) into the [SharedPreferences](../android/content/SharedPreferences.md) or into [PreferenceDataStore](../android/preference/PreferenceDataStore.md) if assigned. This, at minimum, checks whether this Preference is persistent and it currently has a key. Before you save/restore from the storage, check this first.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if it should persist the value. |
