# Preference

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Preference

Kotlin| [Java](https://developer.android.com/reference/android/preference/Preference "View this page in Java") 

```
open class Preference : Comparable<Preference!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.preference.Preference](https://developer.android.com/reference/kotlin/android/preference/Preference#) |

| Known Direct Subclasses [DialogPreference](https://developer.android.com/reference/kotlin/android/preference/DialogPreference), [PreferenceGroup](https://developer.android.com/reference/kotlin/android/preference/PreferenceGroup), [RingtonePreference](https://developer.android.com/reference/kotlin/android/preference/RingtonePreference), [TwoStatePreference](https://developer.android.com/reference/kotlin/android/preference/TwoStatePreference) |------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [DialogPreference](https://developer.android.com/reference/kotlin/android/preference/DialogPreference) | A base class for [Preference](https://developer.android.com/reference/kotlin/android/preference/Preference#) objects that are dialog-based. | | [PreferenceGroup](https://developer.android.com/reference/kotlin/android/preference/PreferenceGroup) | A container for multiple [Preference](https://developer.android.com/reference/kotlin/android/preference/Preference#) objects. | | [RingtonePreference](https://developer.android.com/reference/kotlin/android/preference/RingtonePreference) | A [Preference](https://developer.android.com/reference/kotlin/android/preference/Preference#) that allows the user to choose a ringtone from those on the device. | | [TwoStatePreference](https://developer.android.com/reference/kotlin/android/preference/TwoStatePreference) | Common base class for preferences that have two selectable states, persist a boolean value in SharedPreferences, and may have dependent preferences that are enabled/disabled based on the current state. | |

| Known Indirect Subclasses [CheckBoxPreference](https://developer.android.com/reference/kotlin/android/preference/CheckBoxPreference), [EditTextPreference](https://developer.android.com/reference/kotlin/android/preference/EditTextPreference), [ListPreference](https://developer.android.com/reference/kotlin/android/preference/ListPreference), [MultiSelectListPreference](https://developer.android.com/reference/kotlin/android/preference/MultiSelectListPreference), [PreferenceCategory](https://developer.android.com/reference/kotlin/android/preference/PreferenceCategory), [PreferenceScreen](https://developer.android.com/reference/kotlin/android/preference/PreferenceScreen), [SwitchPreference](https://developer.android.com/reference/kotlin/android/preference/SwitchPreference) |--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------| | [CheckBoxPreference](https://developer.android.com/reference/kotlin/android/preference/CheckBoxPreference) | A [Preference](https://developer.android.com/reference/kotlin/android/preference/Preference#) that provides checkbox widget functionality. | | [EditTextPreference](https://developer.android.com/reference/kotlin/android/preference/EditTextPreference) | A [Preference](https://developer.android.com/reference/kotlin/android/preference/Preference#) that allows for string input. | | [ListPreference](https://developer.android.com/reference/kotlin/android/preference/ListPreference) | A [Preference](https://developer.android.com/reference/kotlin/android/preference/Preference#) that displays a list of entries as a dialog. | | [MultiSelectListPreference](https://developer.android.com/reference/kotlin/android/preference/MultiSelectListPreference) | A [Preference](https://developer.android.com/reference/kotlin/android/preference/Preference#) that displays a list of entries as a dialog. | | [PreferenceCategory](https://developer.android.com/reference/kotlin/android/preference/PreferenceCategory) | Used to group [Preference](https://developer.android.com/reference/kotlin/android/preference/Preference#) objects and provide a disabled title above the group. | | [PreferenceScreen](https://developer.android.com/reference/kotlin/android/preference/PreferenceScreen) | Represents a top-level [Preference](https://developer.android.com/reference/kotlin/android/preference/Preference#) that is the root of a Preference hierarchy. | | [SwitchPreference](https://developer.android.com/reference/kotlin/android/preference/SwitchPreference) | A [Preference](https://developer.android.com/reference/kotlin/android/preference/Preference#) that provides a two-state toggleable option. | |

| **This class was deprecated in API level 29.**
|
| Use the [AndroidX](https://developer.android.com/jetpack/androidx.html) [Preference Library](https://developer.android.com/reference/androidx/preference/package-summary.html) for consistent behavior across all devices. For more information on using the AndroidX Preference Library see [Settings](https://developer.android.com/guide/topics/ui/settings.html).

Represents the basic Preference UI building block displayed by a [PreferenceActivity](https://developer.android.com/reference/kotlin/android/preference/PreferenceActivity) in the form of a [ListView](https://developer.android.com/reference/kotlin/android/widget/ListView.html#). This class provides the [View](https://developer.android.com/reference/kotlin/android/view/View.html#) to be displayed in the activity and associates with a [SharedPreferences](https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#) to store/retrieve the preference data.

When specifying a preference hierarchy in XML, each element can point to a subclass of [Preference](https://developer.android.com/reference/kotlin/android/preference/Preference#), similar to the view hierarchy and layouts.

This class contains a`key`that will be used as the key into the [SharedPreferences](https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#). It is up to the subclass to decide how to store the value.
|
| ### Developer Guides
|
| For information about building a settings UI with Preferences, read the [Settings](https://developer.android.com/guide/topics/ui/settings.html) guide.

## Summary

| Nested classes ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [BaseSavedState](https://developer.android.com/reference/kotlin/android/preference/Preference.BaseSavedState) A base class for managing the instance state of a [Preference](https://developer.android.com/reference/kotlin/android/preference/Preference#). |
| abstract | [OnPreferenceChangeListener](https://developer.android.com/reference/kotlin/android/preference/Preference.OnPreferenceChangeListener) Interface definition for a callback to be invoked when the value of this [Preference](https://developer.android.com/reference/kotlin/android/preference/Preference#) has been changed by the user and is about to be set and/or persisted. |
| abstract | [OnPreferenceClickListener](https://developer.android.com/reference/kotlin/android/preference/Preference.OnPreferenceClickListener) Interface definition for a callback to be invoked when a [Preference](https://developer.android.com/reference/kotlin/android/preference/Preference#) is clicked. |

| XML attributes ||
|-----------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [`android:defaultValue`](https://developer.android.com/reference/kotlin/android/preference/Preference#attr_Preference) | The default value for the preference, which will be set either if persistence is off or persistence is on and the preference is not found in the persistent storage. |
| [`android:dependency`](https://developer.android.com/reference/kotlin/android/preference/Preference#attr_Preference) | The key of another Preference that this Preference will depend on. |
| [`android:enabled`](https://developer.android.com/reference/kotlin/android/preference/Preference#attr_Preference) | Whether the Preference is enabled. |
| [`android:fragment`](https://developer.android.com/reference/kotlin/android/preference/Preference#attr_Preference) | When used inside of a modern PreferenceActivity, this declares a new PreferenceFragment to be shown when the user selects this item. |
| [`android:icon`](https://developer.android.com/reference/kotlin/android/preference/Preference#attr_Preference) | The optional icon for the preference. |
| [`android:iconSpaceReserved`](https://developer.android.com/reference/kotlin/android/preference/Preference#attr_Preference) | Whether the space for the preference icon view will be reserved. |
| [`android:key`](https://developer.android.com/reference/kotlin/android/preference/Preference#attr_Preference) | The key to store the Preference value. |
| [`android:layout`](https://developer.android.com/reference/kotlin/android/preference/Preference#attr_Preference) | The layout for the Preference in a PreferenceActivity screen. |
| [`android:order`](https://developer.android.com/reference/kotlin/android/preference/Preference#attr_Preference) | The order for the Preference (lower values are to be ordered first). |
| [`android:persistent`](https://developer.android.com/reference/kotlin/android/preference/Preference#attr_Preference) | Whether the Preference stores its value to the storage. |
| [`android:recycleEnabled`](https://developer.android.com/reference/kotlin/android/preference/Preference#attr_Preference) | Whether the preference has enabled to have its view recycled when used in the list view. |
| [`android:selectable`](https://developer.android.com/reference/kotlin/android/preference/Preference#attr_Preference) | Whether the Preference is selectable. |
| [`android:shouldDisableView`](https://developer.android.com/reference/kotlin/android/preference/Preference#attr_Preference) | Whether the view of this Preference should be disabled when this Preference is disabled. |
| [`android:singleLineTitle`](https://developer.android.com/reference/kotlin/android/preference/Preference#attr_Preference) | Whether to use single line for the preference title text. |
| [`android:summary`](https://developer.android.com/reference/kotlin/android/preference/Preference#attr_Preference) | The summary for the Preference. |
| [`android:title`](https://developer.android.com/reference/kotlin/android/preference/Preference#attr_Preference) | The title for the Preference. |
| [`android:widgetLayout`](https://developer.android.com/reference/kotlin/android/preference/Preference#attr_Preference) | The layout for the controllable widget portion of a Preference. |

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DEFAULT_ORDER](https://developer.android.com/reference/kotlin/android/preference/Preference#DEFAULT_ORDER:kotlin.Int) Specify for [setOrder(int)](https://developer.android.com/reference/kotlin/android/preference/Preference#setOrder(kotlin.Int))if a specific order is not required. |

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Preference](https://developer.android.com/reference/kotlin/android/preference/Preference#Preference(android.content.Context))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`)` Constructor to create a Preference. |
| [Preference](https://developer.android.com/reference/kotlin/android/preference/Preference#Preference(android.content.Context,%20android.util.AttributeSet))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `attrs:` ` [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)!`)` Constructor that is called when inflating a Preference from XML. |
| [Preference](https://developer.android.com/reference/kotlin/android/preference/Preference#Preference(android.content.Context,%20android.util.AttributeSet,%20kotlin.Int))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `attrs:` ` [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)!`, `defStyleAttr:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Perform inflation from XML and apply a class-specific base style. |
| [Preference](https://developer.android.com/reference/kotlin/android/preference/Preference#Preference(android.content.Context,%20android.util.AttributeSet,%20kotlin.Int,%20kotlin.Int))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `attrs:` ` [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)!`, `defStyleAttr:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `defStyleRes:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Perform inflation from XML and apply a class-specific base style. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compareTo](https://developer.android.com/reference/kotlin/android/preference/Preference#compareTo(android.preference.Preference))`(`other:` ` [Preference](https://developer.android.com/reference/kotlin/android/preference/Preference#)!`)` Compares Preference objects based on order (if set), otherwise alphabetically on the titles. |
| open [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)! | [getContext](https://developer.android.com/reference/kotlin/android/preference/Preference#getContext())`()` Returns the [android.content.Context](https://developer.android.com/reference/kotlin/android/content/Context.html#) of this Preference. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getDependency](https://developer.android.com/reference/kotlin/android/preference/Preference#getDependency())`()` Returns the key of the dependency on this Preference. |
| open [SharedPreferences.Editor](https://developer.android.com/reference/kotlin/android/content/SharedPreferences.Editor.html#)! | [getEditor](https://developer.android.com/reference/kotlin/android/preference/Preference#getEditor())`()` Returns an [SharedPreferences.Editor](https://developer.android.com/reference/kotlin/android/content/SharedPreferences.Editor.html#) where this Preference can save its value(s). |
| open [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)! | [getExtras](https://developer.android.com/reference/kotlin/android/preference/Preference#getExtras())`()` Return the extras Bundle object associated with this preference, creating a new Bundle if there currently isn't one. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getFragment](https://developer.android.com/reference/kotlin/android/preference/Preference#getFragment())`()` Return the fragment class name associated with this Preference. |
| open [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)! | [getIcon](https://developer.android.com/reference/kotlin/android/preference/Preference#getIcon())`()` Returns the icon of this Preference. |
| open [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)! | [getIntent](https://developer.android.com/reference/kotlin/android/preference/Preference#getIntent())`()` Return the [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#) associated with this Preference. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getKey](https://developer.android.com/reference/kotlin/android/preference/Preference#getKey())`()` Gets the key for this Preference, which is also the key used for storing values into [SharedPreferences](https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#) or [PreferenceDataStore](https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore). |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLayoutResource](https://developer.android.com/reference/kotlin/android/preference/Preference#getLayoutResource())`()` Gets the layout resource that will be shown as the [View](https://developer.android.com/reference/kotlin/android/view/View.html#) for this Preference. |
| open [Preference.OnPreferenceChangeListener](https://developer.android.com/reference/kotlin/android/preference/Preference.OnPreferenceChangeListener)! | [getOnPreferenceChangeListener](https://developer.android.com/reference/kotlin/android/preference/Preference#getOnPreferenceChangeListener())`()` Returns the callback to be invoked when this Preference is changed by the user (but before the internal state has been updated). |
| open [Preference.OnPreferenceClickListener](https://developer.android.com/reference/kotlin/android/preference/Preference.OnPreferenceClickListener)! | [getOnPreferenceClickListener](https://developer.android.com/reference/kotlin/android/preference/Preference#getOnPreferenceClickListener())`()` Returns the callback to be invoked when this Preference is clicked. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOrder](https://developer.android.com/reference/kotlin/android/preference/Preference#getOrder())`()` Gets the order of this Preference with respect to other Preference objects on the same level. |
| open [PreferenceGroup](https://developer.android.com/reference/kotlin/android/preference/PreferenceGroup)? | [getParent](https://developer.android.com/reference/kotlin/android/preference/Preference#getParent())`()` Returns the [PreferenceGroup](https://developer.android.com/reference/kotlin/android/preference/PreferenceGroup) which is this Preference assigned to or`null`if this preference is not assigned to any group or is a root Preference. |
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getPersistedStringSet](https://developer.android.com/reference/kotlin/android/preference/Preference#getPersistedStringSet(kotlin.collections.MutableSet))`(`defaultReturnValue:` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Attempts to get a persisted set of Strings if this Preference is persistent. |
| open [PreferenceDataStore](https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore)? | [getPreferenceDataStore](https://developer.android.com/reference/kotlin/android/preference/Preference#getPreferenceDataStore())`()` Returns [PreferenceDataStore](https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore) used by this Preference. |
| open [PreferenceManager](https://developer.android.com/reference/kotlin/android/preference/PreferenceManager)! | [getPreferenceManager](https://developer.android.com/reference/kotlin/android/preference/Preference#getPreferenceManager())`()` Gets the [PreferenceManager](https://developer.android.com/reference/kotlin/android/preference/PreferenceManager) that manages this Preference object's tree. |
| open [SharedPreferences](https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#)! | [getSharedPreferences](https://developer.android.com/reference/kotlin/android/preference/Preference#getSharedPreferences())`()` Returns the [SharedPreferences](https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#) where this Preference can read its value(s). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getShouldDisableView](https://developer.android.com/reference/kotlin/android/preference/Preference#getShouldDisableView())`()` Checks whether this Preference should disable its view when it's action is disabled. |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [getSummary](https://developer.android.com/reference/kotlin/android/preference/Preference#getSummary())`()` Returns the summary of this Preference. |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [getTitle](https://developer.android.com/reference/kotlin/android/preference/Preference#getTitle())`()` Returns the title of this Preference. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTitleRes](https://developer.android.com/reference/kotlin/android/preference/Preference#getTitleRes())`()` Returns the title resource ID of this Preference. |
| open [View](https://developer.android.com/reference/kotlin/android/view/View.html#)! | [getView](https://developer.android.com/reference/kotlin/android/preference/Preference#getView(android.view.View,%20android.view.ViewGroup))`(`convertView:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `parent:` ` [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!`)` Gets the View that will be shown in the [PreferenceActivity](https://developer.android.com/reference/kotlin/android/preference/PreferenceActivity). |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getWidgetLayoutResource](https://developer.android.com/reference/kotlin/android/preference/Preference#getWidgetLayoutResource())`()` Gets the layout resource for the controllable widget portion of this Preference. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasKey](https://developer.android.com/reference/kotlin/android/preference/Preference#hasKey())`()` Checks whether this Preference has a valid key. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEnabled](https://developer.android.com/reference/kotlin/android/preference/Preference#isEnabled())`()` Checks whether this Preference should be enabled in the list. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isIconSpaceReserved](https://developer.android.com/reference/kotlin/android/preference/Preference#isIconSpaceReserved())`()` Gets whether the space this preference icon view is reserved. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPersistent](https://developer.android.com/reference/kotlin/android/preference/Preference#isPersistent())`()` Checks whether this Preference is persistent. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRecycleEnabled](https://developer.android.com/reference/kotlin/android/preference/Preference#isRecycleEnabled())`()` Checks whether this Preference has enabled to have its view recycled when used in the list view. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSelectable](https://developer.android.com/reference/kotlin/android/preference/Preference#isSelectable())`()` Checks whether this Preference should be selectable in the list. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSingleLineTitle](https://developer.android.com/reference/kotlin/android/preference/Preference#isSingleLineTitle())`()` Gets whether the title of this preference is constrained to a single line. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyDependencyChange](https://developer.android.com/reference/kotlin/android/preference/Preference#notifyDependencyChange(kotlin.Boolean))`(`disableDependents:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Notifies any listening dependents of a change that affects the dependency. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDependencyChanged](https://developer.android.com/reference/kotlin/android/preference/Preference#onDependencyChanged(android.preference.Preference,%20kotlin.Boolean))`(`dependency:` ` [Preference](https://developer.android.com/reference/kotlin/android/preference/Preference#)!`, `disableDependent:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Called when the dependency changes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onParentChanged](https://developer.android.com/reference/kotlin/android/preference/Preference#onParentChanged(android.preference.Preference,%20kotlin.Boolean))`(`parent:` ` [Preference](https://developer.android.com/reference/kotlin/android/preference/Preference#)!`, `disableChild:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Called when the implicit parent dependency changes. |
| open [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)! | [peekExtras](https://developer.android.com/reference/kotlin/android/preference/Preference#peekExtras())`()` Return the extras Bundle object associated with this preference, returning`null`if there is not currently one. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [persistStringSet](https://developer.android.com/reference/kotlin/android/preference/Preference#persistStringSet(kotlin.collections.MutableSet))`(`values:` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Attempts to persist a set of Strings if this Preference is persistent. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [restoreHierarchyState](https://developer.android.com/reference/kotlin/android/preference/Preference#restoreHierarchyState(android.os.Bundle))`(`container:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`)` Restore this Preference hierarchy's previously saved state from the given container. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [saveHierarchyState](https://developer.android.com/reference/kotlin/android/preference/Preference#saveHierarchyState(android.os.Bundle))`(`container:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`)` Store this Preference hierarchy's frozen state into the given container. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDefaultValue](https://developer.android.com/reference/kotlin/android/preference/Preference#setDefaultValue(kotlin.Any))`(`defaultValue:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Sets the default value for this Preference, which will be set either if persistence is off or persistence is on and the preference is not found in the persistent storage. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDependency](https://developer.android.com/reference/kotlin/android/preference/Preference#setDependency(kotlin.String))`(`dependencyKey:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the key of a Preference that this Preference will depend on. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEnabled](https://developer.android.com/reference/kotlin/android/preference/Preference#setEnabled(kotlin.Boolean))`(`enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether this Preference is enabled. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFragment](https://developer.android.com/reference/kotlin/android/preference/Preference#setFragment(kotlin.String))`(`fragment:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the class name of a fragment to be shown when this Preference is clicked. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setIcon](https://developer.android.com/reference/kotlin/android/preference/Preference#setIcon(android.graphics.drawable.Drawable))`(`icon:` ` [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)!`)` Sets the icon for this Preference with a Drawable. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setIcon](https://developer.android.com/reference/kotlin/android/preference/Preference#setIcon(kotlin.Int))`(`iconResId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the icon for this Preference with a resource ID. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setIconSpaceReserved](https://developer.android.com/reference/kotlin/android/preference/Preference#setIconSpaceReserved(kotlin.Boolean))`(`iconSpaceReserved:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether to reserve the space of this Preference icon view when no icon is provided. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setIntent](https://developer.android.com/reference/kotlin/android/preference/Preference#setIntent(android.content.Intent))`(`intent:` ` [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!`)` Sets an [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#) to be used for [Context.startActivity(Intent)](https://developer.android.com/reference/kotlin/android/content/Context.html#startActivity(android.content.Intent))when this Preference is clicked. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setKey](https://developer.android.com/reference/kotlin/android/preference/Preference#setKey(kotlin.String))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the key for this Preference, which is used as a key to the [SharedPreferences](https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#) or [PreferenceDataStore](https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLayoutResource](https://developer.android.com/reference/kotlin/android/preference/Preference#setLayoutResource(kotlin.Int))`(`layoutResId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the layout resource that is inflated as the [View](https://developer.android.com/reference/kotlin/android/view/View.html#) to be shown for this Preference. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnPreferenceChangeListener](https://developer.android.com/reference/kotlin/android/preference/Preference#setOnPreferenceChangeListener(android.preference.Preference.OnPreferenceChangeListener))`(`onPreferenceChangeListener:` ` [Preference.OnPreferenceChangeListener](https://developer.android.com/reference/kotlin/android/preference/Preference.OnPreferenceChangeListener)!`)` Sets the callback to be invoked when this Preference is changed by the user (but before the internal state has been updated). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnPreferenceClickListener](https://developer.android.com/reference/kotlin/android/preference/Preference#setOnPreferenceClickListener(android.preference.Preference.OnPreferenceClickListener))`(`onPreferenceClickListener:` ` [Preference.OnPreferenceClickListener](https://developer.android.com/reference/kotlin/android/preference/Preference.OnPreferenceClickListener)!`)` Sets the callback to be invoked when this Preference is clicked. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOrder](https://developer.android.com/reference/kotlin/android/preference/Preference#setOrder(kotlin.Int))`(`order:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the order of this Preference with respect to other Preference objects on the same level. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPersistent](https://developer.android.com/reference/kotlin/android/preference/Preference#setPersistent(kotlin.Boolean))`(`persistent:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether this Preference is persistent. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPreferenceDataStore](https://developer.android.com/reference/kotlin/android/preference/Preference#setPreferenceDataStore(android.preference.PreferenceDataStore))`(`dataStore:` ` [PreferenceDataStore](https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore)!`)` Sets a [PreferenceDataStore](https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore) to be used by this Preference instead of using [android.content.SharedPreferences](https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRecycleEnabled](https://developer.android.com/reference/kotlin/android/preference/Preference#setRecycleEnabled(kotlin.Boolean))`(`enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether this Preference has enabled to have its view recycled when used in the list view. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSelectable](https://developer.android.com/reference/kotlin/android/preference/Preference#setSelectable(kotlin.Boolean))`(`selectable:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether this Preference is selectable. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setShouldDisableView](https://developer.android.com/reference/kotlin/android/preference/Preference#setShouldDisableView(kotlin.Boolean))`(`shouldDisableView:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether this Preference should disable its view when it gets disabled. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSingleLineTitle](https://developer.android.com/reference/kotlin/android/preference/Preference#setSingleLineTitle(kotlin.Boolean))`(`singleLineTitle:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether to constrain the title of this Preference to a single line instead of letting it wrap onto multiple lines. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSummary](https://developer.android.com/reference/kotlin/android/preference/Preference#setSummary(kotlin.Int))`(`summaryResId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the summary for this Preference with a resource ID. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSummary](https://developer.android.com/reference/kotlin/android/preference/Preference#setSummary(kotlin.CharSequence))`(`summary:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Sets the summary for this Preference with a CharSequence. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTitle](https://developer.android.com/reference/kotlin/android/preference/Preference#setTitle(kotlin.Int))`(`titleResId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the title for this Preference with a resource ID. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTitle](https://developer.android.com/reference/kotlin/android/preference/Preference#setTitle(kotlin.CharSequence))`(`title:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Sets the title for this Preference with a CharSequence. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setWidgetLayoutResource](https://developer.android.com/reference/kotlin/android/preference/Preference#setWidgetLayoutResource(kotlin.Int))`(`widgetLayoutResId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the layout for the controllable widget portion of this Preference. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [shouldCommit](https://developer.android.com/reference/kotlin/android/preference/Preference#shouldCommit())`()` Returns whether the [Preference](https://developer.android.com/reference/kotlin/android/preference/Preference#) should commit its saved value(s) in [getEditor()](https://developer.android.com/reference/kotlin/android/preference/Preference#getEditor()). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [shouldDisableDependents](https://developer.android.com/reference/kotlin/android/preference/Preference#shouldDisableDependents())`()` Checks whether this preference's dependents should currently be disabled. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/preference/Preference#toString())`()` <br /> |

| Protected methods ||
|--------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [callChangeListener](https://developer.android.com/reference/kotlin/android/preference/Preference#callChangeListener(kotlin.Any))`(`newValue:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Call this method after the user changes the preference, but before the internal state is set. |
| open [Preference](https://developer.android.com/reference/kotlin/android/preference/Preference#)! | [findPreferenceInHierarchy](https://developer.android.com/reference/kotlin/android/preference/Preference#findPreferenceInHierarchy(kotlin.String))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Finds a Preference in this hierarchy (the whole thing, even above/below your [PreferenceScreen](https://developer.android.com/reference/kotlin/android/preference/PreferenceScreen) screen break) with the given key. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getPersistedBoolean](https://developer.android.com/reference/kotlin/android/preference/Preference#getPersistedBoolean(kotlin.Boolean))`(`defaultReturnValue:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Attempts to get a persisted boolean if this Preference is persistent. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getPersistedFloat](https://developer.android.com/reference/kotlin/android/preference/Preference#getPersistedFloat(kotlin.Float))`(`defaultReturnValue:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Attempts to get a persisted float if this Preference is persistent. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPersistedInt](https://developer.android.com/reference/kotlin/android/preference/Preference#getPersistedInt(kotlin.Int))`(`defaultReturnValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Attempts to get a persisted int if this Preference is persistent. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getPersistedLong](https://developer.android.com/reference/kotlin/android/preference/Preference#getPersistedLong(kotlin.Long))`(`defaultReturnValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Attempts to get a persisted long if this Preference is persistent. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getPersistedString](https://developer.android.com/reference/kotlin/android/preference/Preference#getPersistedString(kotlin.String))`(`defaultReturnValue:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Attempts to get a persisted String if this Preference is persistent. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyChanged](https://developer.android.com/reference/kotlin/android/preference/Preference#notifyChanged())`()` Should be called when the data of this [Preference](https://developer.android.com/reference/kotlin/android/preference/Preference#) has changed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [notifyHierarchyChanged](https://developer.android.com/reference/kotlin/android/preference/Preference#notifyHierarchyChanged())`()` Should be called when a Preference has been added/removed from this group, or the ordering should be re-evaluated. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAttachedToActivity](https://developer.android.com/reference/kotlin/android/preference/Preference#onAttachedToActivity())`()` Called when the Preference hierarchy has been attached to the [PreferenceActivity](https://developer.android.com/reference/kotlin/android/preference/PreferenceActivity). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAttachedToHierarchy](https://developer.android.com/reference/kotlin/android/preference/Preference#onAttachedToHierarchy(android.preference.PreferenceManager))`(`preferenceManager:` ` [PreferenceManager](https://developer.android.com/reference/kotlin/android/preference/PreferenceManager)!`)` Called when this Preference has been attached to a Preference hierarchy. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onBindView](https://developer.android.com/reference/kotlin/android/preference/Preference#onBindView(android.view.View))`(`view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`)` Binds the created View to the data for this Preference. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onClick](https://developer.android.com/reference/kotlin/android/preference/Preference#onClick())`()` Processes a click on the preference. |
| open [View](https://developer.android.com/reference/kotlin/android/view/View.html#)! | [onCreateView](https://developer.android.com/reference/kotlin/android/preference/Preference#onCreateView(android.view.ViewGroup))`(`parent:` ` [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!`)` Creates the View to be shown for this Preference in the [PreferenceActivity](https://developer.android.com/reference/kotlin/android/preference/PreferenceActivity). |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [onGetDefaultValue](https://developer.android.com/reference/kotlin/android/preference/Preference#onGetDefaultValue(android.content.res.TypedArray,%20kotlin.Int))`(`a:` ` [TypedArray](https://developer.android.com/reference/kotlin/android/content/res/TypedArray.html#)!`, `index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when a Preference is being inflated and the default value attribute needs to be read. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPrepareForRemoval](https://developer.android.com/reference/kotlin/android/preference/Preference#onPrepareForRemoval())`()` Called when this Preference is being removed from the hierarchy. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onRestoreInstanceState](https://developer.android.com/reference/kotlin/android/preference/Preference#onRestoreInstanceState(android.os.Parcelable))`(`state:` ` [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#)!`)` Hook allowing a Preference to re-apply a representation of its internal state that had previously been generated by [onSaveInstanceState](https://developer.android.com/reference/kotlin/android/preference/Preference#onSaveInstanceState()). |
| open [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#)! | [onSaveInstanceState](https://developer.android.com/reference/kotlin/android/preference/Preference#onSaveInstanceState())`()` Hook allowing a Preference to generate a representation of its internal state that can later be used to create a new instance with that same state. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSetInitialValue](https://developer.android.com/reference/kotlin/android/preference/Preference#onSetInitialValue(kotlin.Boolean,%20kotlin.Any))`(`restorePersistedValue:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `defaultValue:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Implement this to set the initial value of the Preference. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [persistBoolean](https://developer.android.com/reference/kotlin/android/preference/Preference#persistBoolean(kotlin.Boolean))`(`value:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Attempts to persist a boolean if this Preference is persistent. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [persistFloat](https://developer.android.com/reference/kotlin/android/preference/Preference#persistFloat(kotlin.Float))`(`value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Attempts to persist a long if this Preference is persistent. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [persistInt](https://developer.android.com/reference/kotlin/android/preference/Preference#persistInt(kotlin.Int))`(`value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Attempts to persist an int if this Preference is persistent. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [persistLong](https://developer.android.com/reference/kotlin/android/preference/Preference#persistLong(kotlin.Long))`(`value:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Attempts to persist a long if this Preference is persistent. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [persistString](https://developer.android.com/reference/kotlin/android/preference/Preference#persistString(kotlin.String))`(`value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Attempts to persist a String if this Preference is persistent. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [shouldPersist](https://developer.android.com/reference/kotlin/android/preference/Preference#shouldPersist())`()` Checks whether, at the given time this method is called, this Preference should store/restore its value(s) into the [SharedPreferences](https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#) or into [PreferenceDataStore](https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore) if assigned. |

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

Specify for [setOrder(int)](https://developer.android.com/reference/kotlin/android/preference/Preference#setOrder(kotlin.Int))if a specific order is not required. 

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
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:The Context in which to store Preference values. |

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
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:The Context this is associated with, through which it can access the current theme, resources, [SharedPreferences](https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#), etc. |
| `attrs` | [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)!:The attributes of the XML tag that is inflating the preference. |

**See Also**

- [#Preference(Context, AttributeSet, int)](https://developer.android.com/reference/kotlin/android/preference/Preference#Preference(android.content.Context,%20android.util.AttributeSet,%20kotlin.Int)) 

### Preference

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Preference(
    context: Context!, 
    attrs: AttributeSet!, 
    defStyleAttr: Int)
```

Perform inflation from XML and apply a class-specific base style. This constructor of Preference allows subclasses to use their own base style when they are inflating. For example, a [CheckBoxPreference](https://developer.android.com/reference/kotlin/android/preference/CheckBoxPreference) constructor calls this version of the super class constructor and supplies`android.R.attr.checkBoxPreferenceStyle`for defStyleAttr. This allows the theme's checkbox preference style to modify all of the base preference attributes as well as the [CheckBoxPreference](https://developer.android.com/reference/kotlin/android/preference/CheckBoxPreference) class's attributes.

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:The Context this is associated with, through which it can access the current theme, resources, [SharedPreferences](https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#), etc. |
| `attrs` | [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)!:The attributes of the XML tag that is inflating the preference. |
| `defStyleAttr` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):An attribute in the current theme that contains a reference to a style resource that supplies default values for the view. Can be 0 to not look for defaults. |

**See Also**

- [#Preference(Context, AttributeSet)](https://developer.android.com/reference/kotlin/android/preference/Preference#Preference(android.content.Context,%20android.util.AttributeSet)) 

### Preference

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Preference(
    context: Context!, 
    attrs: AttributeSet!, 
    defStyleAttr: Int, 
    defStyleRes: Int)
```

Perform inflation from XML and apply a class-specific base style. This constructor of Preference allows subclasses to use their own base style when they are inflating. For example, a [CheckBoxPreference](https://developer.android.com/reference/kotlin/android/preference/CheckBoxPreference) constructor calls this version of the super class constructor and supplies`android.R.attr.checkBoxPreferenceStyle`for defStyleAttr. This allows the theme's checkbox preference style to modify all of the base preference attributes as well as the [CheckBoxPreference](https://developer.android.com/reference/kotlin/android/preference/CheckBoxPreference) class's attributes.

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:The Context this is associated with, through which it can access the current theme, resources, [SharedPreferences](https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#), etc. |
| `attrs` | [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)!:The attributes of the XML tag that is inflating the preference. |
| `defStyleAttr` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):An attribute in the current theme that contains a reference to a style resource that supplies default values for the view. Can be 0 to not look for defaults. |
| `defStyleRes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A resource identifier of a style resource that supplies default values for the view, used only if defStyleAttr is 0 or can not be found in the theme. Can be 0 to not look for defaults. |

**See Also**

- [#Preference(Context, AttributeSet)](https://developer.android.com/reference/kotlin/android/preference/Preference#Preference(android.content.Context,%20android.util.AttributeSet))

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

Returns the [android.content.Context](https://developer.android.com/reference/kotlin/android/content/Context.html#) of this Preference. Each Preference in a Preference hierarchy can be from different Context (for example, if multiple activities provide preferences into a single [PreferenceActivity](https://developer.android.com/reference/kotlin/android/preference/PreferenceActivity)). This Context will be used to save the Preference values.

| Return ||
|------------------------------------------------------------------------------------------|---------------------------------|
| [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)! | The Context of this Preference. |

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

- [#setDependency(String)](https://developer.android.com/reference/kotlin/android/preference/Preference#setDependency(kotlin.String)) 

### getEditor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEditor(): SharedPreferences.Editor!
```

**Deprecated:** *Deprecated in Java.*

Returns an [SharedPreferences.Editor](https://developer.android.com/reference/kotlin/android/content/SharedPreferences.Editor.html#) where this Preference can save its value(s). Usually it's easier to use one of the helper save methods: [persistBoolean(boolean)](https://developer.android.com/reference/kotlin/android/preference/Preference#persistBoolean(kotlin.Boolean)), [persistFloat(float)](https://developer.android.com/reference/kotlin/android/preference/Preference#persistFloat(kotlin.Float)), [persistInt(int)](https://developer.android.com/reference/kotlin/android/preference/Preference#persistInt(kotlin.Int)), [persistLong(long)](https://developer.android.com/reference/kotlin/android/preference/Preference#persistLong(kotlin.Long)), [persistString(java.lang.String)](https://developer.android.com/reference/kotlin/android/preference/Preference#persistString(kotlin.String)). To read values, see [getSharedPreferences()](https://developer.android.com/reference/kotlin/android/preference/Preference#getSharedPreferences()). If [shouldCommit()](https://developer.android.com/reference/kotlin/android/preference/Preference#shouldCommit())returns true, it is this Preference's responsibility to commit.

In some cases, writes to this will not be committed right away and hence not show up in the SharedPreferences, this is intended behavior to improve performance.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [SharedPreferences.Editor](https://developer.android.com/reference/kotlin/android/content/SharedPreferences.Editor.html#)! | a [SharedPreferences.Editor](https://developer.android.com/reference/kotlin/android/content/SharedPreferences.Editor.html#) where this preference saves its value(s). If this preference isn't attached to a Preference hierarchy or if a [PreferenceDataStore](https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore) has been set, this method returns`null`. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/preference/Preference#shouldCommit()>
- <https://developer.android.com/reference/kotlin/android/preference/Preference#getSharedPreferences()>
- [#setPreferenceDataStore(PreferenceDataStore)](https://developer.android.com/reference/kotlin/android/preference/Preference#setPreferenceDataStore(android.preference.PreferenceDataStore)) 

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
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The fragment class name last set via [setFragment](https://developer.android.com/reference/kotlin/android/preference/Preference#setFragment(kotlin.String))or XML. |

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
| [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)! | the icon |

**See Also**

- [#setIcon(Drawable)](https://developer.android.com/reference/kotlin/android/preference/Preference#setIcon(android.graphics.drawable.Drawable)) 

### getIntent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getIntent(): Intent!
```

**Deprecated:** *Deprecated in Java.*

Return the [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#) associated with this Preference.

| Return ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)! | The [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#) last set via [setIntent(android.content.Intent)](https://developer.android.com/reference/kotlin/android/preference/Preference#setIntent(android.content.Intent))or XML. |

### getKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getKey(): String!
```

**Deprecated:** *Deprecated in Java.*

Gets the key for this Preference, which is also the key used for storing values into [SharedPreferences](https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#) or [PreferenceDataStore](https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore).

| Return ||
|-----------------------------------------------------------------------------------|----------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The key. |

### getLayoutResource

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLayoutResource(): Int
```

**Deprecated:** *Deprecated in Java.*

Gets the layout resource that will be shown as the [View](https://developer.android.com/reference/kotlin/android/view/View.html#) for this Preference.

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
| [Preference.OnPreferenceChangeListener](https://developer.android.com/reference/kotlin/android/preference/Preference.OnPreferenceChangeListener)! | The callback to be invoked. |

### getOnPreferenceClickListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getOnPreferenceClickListener(): Preference.OnPreferenceClickListener!
```

**Deprecated:** *Deprecated in Java.*

Returns the callback to be invoked when this Preference is clicked.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [Preference.OnPreferenceClickListener](https://developer.android.com/reference/kotlin/android/preference/Preference.OnPreferenceClickListener)! | The callback to be invoked. |

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

- [#setOrder(int)](https://developer.android.com/reference/kotlin/android/preference/Preference#setOrder(kotlin.Int)) 

### getParent

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getParent(): PreferenceGroup?
```

**Deprecated:** *Deprecated in Java.*

Returns the [PreferenceGroup](https://developer.android.com/reference/kotlin/android/preference/PreferenceGroup) which is this Preference assigned to or`null`if this preference is not assigned to any group or is a root Preference.

| Return ||
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [PreferenceGroup](https://developer.android.com/reference/kotlin/android/preference/PreferenceGroup)? | the parent PreferenceGroup or`null`if not attached to any |

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

- [#persistStringSet(Set)](https://developer.android.com/reference/kotlin/android/preference/Preference#persistStringSet(kotlin.collections.MutableSet)) 

### getPreferenceDataStore

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPreferenceDataStore(): PreferenceDataStore?
```

**Deprecated:** *Deprecated in Java.*

Returns [PreferenceDataStore](https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore) used by this Preference. Returns`null`if [android.content.SharedPreferences](https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#) is used instead.

By default preferences always use [android.content.SharedPreferences](https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#). To make this preference to use the [PreferenceDataStore](https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore) you need to assign your implementation to the Preference itself via [setPreferenceDataStore(android.preference.PreferenceDataStore)](https://developer.android.com/reference/kotlin/android/preference/Preference#setPreferenceDataStore(android.preference.PreferenceDataStore))or to its [PreferenceManager](https://developer.android.com/reference/kotlin/android/preference/PreferenceManager) via [PreferenceManager.setPreferenceDataStore(PreferenceDataStore)](https://developer.android.com/reference/kotlin/android/preference/PreferenceManager#setPreferenceDataStore(android.preference.PreferenceDataStore)).

| Return ||
|---------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [PreferenceDataStore](https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore)? | The [PreferenceDataStore](https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore) used by this Preference or`null`if none. |

### getPreferenceManager

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPreferenceManager(): PreferenceManager!
```

**Deprecated:** *Deprecated in Java.*

Gets the [PreferenceManager](https://developer.android.com/reference/kotlin/android/preference/PreferenceManager) that manages this Preference object's tree.

| Return ||
|-----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [PreferenceManager](https://developer.android.com/reference/kotlin/android/preference/PreferenceManager)! | The [PreferenceManager](https://developer.android.com/reference/kotlin/android/preference/PreferenceManager). |

### getSharedPreferences

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSharedPreferences(): SharedPreferences!
```

**Deprecated:** *Deprecated in Java.*

Returns the [SharedPreferences](https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#) where this Preference can read its value(s). Usually, it's easier to use one of the helper read methods: [getPersistedBoolean(boolean)](https://developer.android.com/reference/kotlin/android/preference/Preference#getPersistedBoolean(kotlin.Boolean)), [getPersistedFloat(float)](https://developer.android.com/reference/kotlin/android/preference/Preference#getPersistedFloat(kotlin.Float)), [getPersistedInt(int)](https://developer.android.com/reference/kotlin/android/preference/Preference#getPersistedInt(kotlin.Int)), [getPersistedLong(long)](https://developer.android.com/reference/kotlin/android/preference/Preference#getPersistedLong(kotlin.Long)), [getPersistedString(java.lang.String)](https://developer.android.com/reference/kotlin/android/preference/Preference#getPersistedString(kotlin.String)). To save values, see [getEditor()](https://developer.android.com/reference/kotlin/android/preference/Preference#getEditor()).

In some cases, writes to the [getEditor()](https://developer.android.com/reference/kotlin/android/preference/Preference#getEditor())will not be committed right away and hence not show up in the returned [SharedPreferences](https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#), this is intended behavior to improve performance.

| Return ||
|--------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [SharedPreferences](https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#)! | the [SharedPreferences](https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#) where this Preference reads its value(s). If this preference isn't attached to a Preference hierarchy or if a [PreferenceDataStore](https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore) has been set, this method returns`null`. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/preference/Preference#getEditor()>
- [#setPreferenceDataStore(PreferenceDataStore)](https://developer.android.com/reference/kotlin/android/preference/Preference#setPreferenceDataStore(android.preference.PreferenceDataStore)) 

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

- [#setShouldDisableView(boolean)](https://developer.android.com/reference/kotlin/android/preference/Preference#setShouldDisableView(kotlin.Boolean)) 

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

- [#setSummary(CharSequence)](https://developer.android.com/reference/kotlin/android/preference/Preference#setSummary(kotlin.CharSequence)) 

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

- [#setTitle(CharSequence)](https://developer.android.com/reference/kotlin/android/preference/Preference#setTitle(kotlin.CharSequence)) 

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

- [#setTitle(int)](https://developer.android.com/reference/kotlin/android/preference/Preference#setTitle(kotlin.Int)) 

### getView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getView(
    convertView: View!, 
    parent: ViewGroup!
): View!
```

**Deprecated:** *Deprecated in Java.*

Gets the View that will be shown in the [PreferenceActivity](https://developer.android.com/reference/kotlin/android/preference/PreferenceActivity).

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `convertView` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:The old View to reuse, if possible. Note: You should check that this View is non-null and of an appropriate type before using. If it is not possible to convert this View to display the correct data, this method can create a new View. |
| `parent` | [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!:The parent that this View will eventually be attached to. |

| Return ||
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [View](https://developer.android.com/reference/kotlin/android/view/View.html#)! | Returns the same Preference object, for chaining multiple calls into a single statement. |

**See Also**

- [#onCreateView(ViewGroup)](https://developer.android.com/reference/kotlin/android/preference/Preference#onCreateView(android.view.ViewGroup))
- [#onBindView(View)](https://developer.android.com/reference/kotlin/android/preference/Preference#onBindView(android.view.View)) 

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

- [#setIconSpaceReserved(boolean)](https://developer.android.com/reference/kotlin/android/preference/Preference#setIconSpaceReserved(kotlin.Boolean)) 

### isPersistent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isPersistent(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Checks whether this Preference is persistent. If it is, it stores its value(s) into the persistent [SharedPreferences](https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#) storage by default or into [PreferenceDataStore](https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore) if assigned.

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

- [#setRecycleEnabled(boolean)](https://developer.android.com/reference/kotlin/android/preference/Preference#setRecycleEnabled(kotlin.Boolean)) 

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

- [#setSingleLineTitle(boolean)](https://developer.android.com/reference/kotlin/android/preference/Preference#setSingleLineTitle(kotlin.Boolean)) 

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
| `dependency` | [Preference](https://developer.android.com/reference/kotlin/android/preference/Preference#)!:The Preference that this Preference depends on. |
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
| `parent` | [Preference](https://developer.android.com/reference/kotlin/android/preference/Preference#)!:The Preference that this Preference depends on. |
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

- [#getPersistedStringSet(Set)](https://developer.android.com/reference/kotlin/android/preference/Preference#getPersistedStringSet(kotlin.collections.MutableSet)) 

### restoreHierarchyState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun restoreHierarchyState(container: Bundle!): Unit
```

**Deprecated:** *Deprecated in Java.*

Restore this Preference hierarchy's previously saved state from the given container.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------|
| `container` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!:The Bundle that holds the previously saved state. |

**See Also**

- [#saveHierarchyState](https://developer.android.com/reference/kotlin/android/preference/Preference#saveHierarchyState(android.os.Bundle))
- [#onRestoreInstanceState](https://developer.android.com/reference/kotlin/android/preference/Preference#onRestoreInstanceState(android.os.Parcelable)) 

### saveHierarchyState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun saveHierarchyState(container: Bundle!): Unit
```

**Deprecated:** *Deprecated in Java.*

Store this Preference hierarchy's frozen state into the given container.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `container` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!:The Bundle in which to save the instance of this Preference. |

**See Also**

- [#restoreHierarchyState](https://developer.android.com/reference/kotlin/android/preference/Preference#restoreHierarchyState(android.os.Bundle))
- [#onSaveInstanceState](https://developer.android.com/reference/kotlin/android/preference/Preference#onSaveInstanceState()) 

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

Sets the icon for this Preference with a Drawable. This icon will be placed into the ID [android.R.id#icon](https://developer.android.com/reference/kotlin/android/R.id.html#icon:kotlin.Int) within the View created by [onCreateView(android.view.ViewGroup)](https://developer.android.com/reference/kotlin/android/preference/Preference#onCreateView(android.view.ViewGroup)).

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `icon` | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)!:the optional icon for this Preference |

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

- [#setIcon(Drawable)](https://developer.android.com/reference/kotlin/android/preference/Preference#setIcon(android.graphics.drawable.Drawable)) 

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

Sets an [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#) to be used for [Context.startActivity(Intent)](https://developer.android.com/reference/kotlin/android/content/Context.html#startActivity(android.content.Intent))when this Preference is clicked.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------|
| `intent` | [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!:The intent associated with this Preference. |

### setKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setKey(key: String!): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the key for this Preference, which is used as a key to the [SharedPreferences](https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#) or [PreferenceDataStore](https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore). This should be unique for the package.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The key for the preference. |

### setLayoutResource

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setLayoutResource(layoutResId: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the layout resource that is inflated as the [View](https://developer.android.com/reference/kotlin/android/view/View.html#) to be shown for this Preference. In most cases, the default layout is sufficient for custom Preference objects and only the widget layout needs to be changed.

This layout should contain a [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#) with ID [android.R.id#widget_frame](https://developer.android.com/reference/kotlin/android/R.id.html#widget_frame:kotlin.Int) to be the parent of the specific widget for this Preference. It should similarly contain [android.R.id#title](https://developer.android.com/reference/kotlin/android/R.id.html#title:kotlin.Int) and [android.R.id#summary](https://developer.android.com/reference/kotlin/android/R.id.html#summary:kotlin.Int).

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `layoutResId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The layout resource ID to be inflated and returned as a [View](https://developer.android.com/reference/kotlin/android/view/View.html#). |

**See Also**

- [#setWidgetLayoutResource(int)](https://developer.android.com/reference/kotlin/android/preference/Preference#setWidgetLayoutResource(kotlin.Int)) 

### setOnPreferenceChangeListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOnPreferenceChangeListener(onPreferenceChangeListener: Preference.OnPreferenceChangeListener!): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the callback to be invoked when this Preference is changed by the user (but before the internal state has been updated).

| Parameters ||
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `onPreferenceChangeListener` | [Preference.OnPreferenceChangeListener](https://developer.android.com/reference/kotlin/android/preference/Preference.OnPreferenceChangeListener)!:The callback to be invoked. |

### setOnPreferenceClickListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOnPreferenceClickListener(onPreferenceClickListener: Preference.OnPreferenceClickListener!): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the callback to be invoked when this Preference is clicked.

| Parameters ||
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `onPreferenceClickListener` | [Preference.OnPreferenceClickListener](https://developer.android.com/reference/kotlin/android/preference/Preference.OnPreferenceClickListener)!:The callback to be invoked. |

### setOrder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOrder(order: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the order of this Preference with respect to other Preference objects on the same level. If this is not specified, the default behavior is to sort alphabetically. The [PreferenceGroup.setOrderingAsAdded(boolean)](https://developer.android.com/reference/kotlin/android/preference/PreferenceGroup#setOrderingAsAdded(kotlin.Boolean))can be used to order Preference objects based on the order they appear in the XML.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `order` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the order for this Preference. A lower value will be shown first. Use [DEFAULT_ORDER](https://developer.android.com/reference/kotlin/android/preference/Preference#DEFAULT_ORDER:kotlin.Int) to sort alphabetically or allow ordering from XML |

**See Also**

- [android.preference.PreferenceGroup#setOrderingAsAdded(boolean)](https://developer.android.com/reference/kotlin/android/preference/PreferenceGroup#setOrderingAsAdded(kotlin.Boolean))
- [#DEFAULT_ORDER](https://developer.android.com/reference/kotlin/android/preference/Preference#DEFAULT_ORDER:kotlin.Int) 

### setPersistent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPersistent(persistent: Boolean): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets whether this Preference is persistent. When persistent, it stores its value(s) into the persistent [SharedPreferences](https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#) storage by default or into [PreferenceDataStore](https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore) if assigned.

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

Sets a [PreferenceDataStore](https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore) to be used by this Preference instead of using [android.content.SharedPreferences](https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#).

The data store will remain assigned even if the Preference is moved around the preference hierarchy. It will also override a data store propagated from the [PreferenceManager](https://developer.android.com/reference/kotlin/android/preference/PreferenceManager) that owns this Preference.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dataStore` | [PreferenceDataStore](https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore)!:The [PreferenceDataStore](https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore) to be used by this Preference. |

**See Also**

- [android.preference.PreferenceManager#setPreferenceDataStore(PreferenceDataStore)](https://developer.android.com/reference/kotlin/android/preference/PreferenceManager#setPreferenceDataStore(android.preference.PreferenceDataStore)) 

### setRecycleEnabled

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setRecycleEnabled(enabled: Boolean): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets whether this Preference has enabled to have its view recycled when used in the list view. By default the recycling is enabled.

The value can be changed only before this preference is added to the preference hierarchy.

If view recycling is not allowed then each time the list view populates this preference the [getView(android.view.View,android.view.ViewGroup)](https://developer.android.com/reference/kotlin/android/preference/Preference#getView(android.view.View,%20android.view.ViewGroup))method receives a`null`convert view and needs to recreate the view. Otherwise view gets recycled and only [onBindView(android.view.View)](https://developer.android.com/reference/kotlin/android/preference/Preference#onBindView(android.view.View))gets called. 
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

For example, set this and [setEnabled(boolean)](https://developer.android.com/reference/kotlin/android/preference/Preference#setEnabled(kotlin.Boolean))to false for preferences that are only displaying information and 1) should not be clickable 2) should not have the view set to the disabled state.

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

- [#setSummary(CharSequence)](https://developer.android.com/reference/kotlin/android/preference/Preference#setSummary(kotlin.CharSequence)) 

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

- [#setTitle(CharSequence)](https://developer.android.com/reference/kotlin/android/preference/Preference#setTitle(kotlin.CharSequence)) 

### setTitle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTitle(title: CharSequence!): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the title for this Preference with a CharSequence. This title will be placed into the ID [android.R.id#title](https://developer.android.com/reference/kotlin/android/R.id.html#title:kotlin.Int) within the View created by [onCreateView(android.view.ViewGroup)](https://developer.android.com/reference/kotlin/android/preference/Preference#onCreateView(android.view.ViewGroup)).

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------|
| `title` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the title for this Preference |

### setWidgetLayoutResource

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setWidgetLayoutResource(widgetLayoutResId: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the layout for the controllable widget portion of this Preference. This is inflated into the main layout. For example, a [CheckBoxPreference](https://developer.android.com/reference/kotlin/android/preference/CheckBoxPreference) would specify a custom layout (consisting of just the CheckBox) here, instead of creating its own main layout.

| Parameters ||
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| `widgetLayoutResId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The layout resource ID to be inflated into the main layout. |

**See Also**

- [#setLayoutResource(int)](https://developer.android.com/reference/kotlin/android/preference/Preference#setLayoutResource(kotlin.Int)) 

### shouldCommit

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun shouldCommit(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Returns whether the [Preference](https://developer.android.com/reference/kotlin/android/preference/Preference#) should commit its saved value(s) in [getEditor()](https://developer.android.com/reference/kotlin/android/preference/Preference#getEditor()). This may return false in situations where batch committing is being done (by the manager) to improve performance.

If this preference is using [PreferenceDataStore](https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore) this value is irrelevant.

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

Finds a Preference in this hierarchy (the whole thing, even above/below your [PreferenceScreen](https://developer.android.com/reference/kotlin/android/preference/PreferenceScreen) screen break) with the given key.

This only functions after we have been attached to a hierarchy.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------|
| `key` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The key of the Preference to find. |

| Return ||
|----------------------------------------------------------------------------------------------|-----------------------------------------|
| [Preference](https://developer.android.com/reference/kotlin/android/preference/Preference#)! | The Preference that uses the given key. |

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

- [#getPersistedString(String)](https://developer.android.com/reference/kotlin/android/preference/Preference#getPersistedString(kotlin.String))
- [#persistBoolean(boolean)](https://developer.android.com/reference/kotlin/android/preference/Preference#persistBoolean(kotlin.Boolean)) 

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

- [#getPersistedString(String)](https://developer.android.com/reference/kotlin/android/preference/Preference#getPersistedString(kotlin.String))
- [#persistFloat(float)](https://developer.android.com/reference/kotlin/android/preference/Preference#persistFloat(kotlin.Float)) 

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

- [#getPersistedString(String)](https://developer.android.com/reference/kotlin/android/preference/Preference#getPersistedString(kotlin.String))
- [#persistInt(int)](https://developer.android.com/reference/kotlin/android/preference/Preference#persistInt(kotlin.Int)) 

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

- [#getPersistedString(String)](https://developer.android.com/reference/kotlin/android/preference/Preference#getPersistedString(kotlin.String))
- [#persistLong(long)](https://developer.android.com/reference/kotlin/android/preference/Preference#persistLong(kotlin.Long)) 

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

- [#persistString(String)](https://developer.android.com/reference/kotlin/android/preference/Preference#persistString(kotlin.String)) 

### notifyChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun notifyChanged(): Unit
```

**Deprecated:** *Deprecated in Java.*

Should be called when the data of this [Preference](https://developer.android.com/reference/kotlin/android/preference/Preference#) has changed. 

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

Called when the Preference hierarchy has been attached to the [PreferenceActivity](https://developer.android.com/reference/kotlin/android/preference/PreferenceActivity). This can also be called when this Preference has been attached to a group that was already attached to the [PreferenceActivity](https://developer.android.com/reference/kotlin/android/preference/PreferenceActivity). 

### onAttachedToHierarchy

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onAttachedToHierarchy(preferenceManager: PreferenceManager!): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when this Preference has been attached to a Preference hierarchy. Make sure to call the super implementation.

| Parameters ||
|---------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `preferenceManager` | [PreferenceManager](https://developer.android.com/reference/kotlin/android/preference/PreferenceManager)!:The PreferenceManager of the hierarchy. |

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
| `view` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:The View that shows this Preference. |

**See Also**

- [#onCreateView(ViewGroup)](https://developer.android.com/reference/kotlin/android/preference/Preference#onCreateView(android.view.ViewGroup)) 

### onClick

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onClick(): Unit
```

**Deprecated:** *Deprecated in Java.*

Processes a click on the preference. This includes saving the value to the [SharedPreferences](https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#). However, the overridden method should call [callChangeListener(java.lang.Object)](https://developer.android.com/reference/kotlin/android/preference/Preference#callChangeListener(kotlin.Any))to make sure the client wants to update the preference's state with the new value. 

### onCreateView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onCreateView(parent: ViewGroup!): View!
```

**Deprecated:** *Deprecated in Java.*

Creates the View to be shown for this Preference in the [PreferenceActivity](https://developer.android.com/reference/kotlin/android/preference/PreferenceActivity). The default behavior is to inflate the main layout of this Preference (see [setLayoutResource(int)](https://developer.android.com/reference/kotlin/android/preference/Preference#setLayoutResource(kotlin.Int)). If changing this behavior, please specify a [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#) with ID [android.R.id#widget_frame](https://developer.android.com/reference/kotlin/android/R.id.html#widget_frame:kotlin.Int).

Make sure to call through to the superclass's implementation. 
If you override this method you*must*call through to the superclass implementation.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `parent` | [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)!:The parent that this View will eventually be attached to. |

| Return ||
|---------------------------------------------------------------------------------|-----------------------------------------|
| [View](https://developer.android.com/reference/kotlin/android/view/View.html#)! | The View that displays this Preference. |

**See Also**

- [#onBindView(View)](https://developer.android.com/reference/kotlin/android/preference/Preference#onBindView(android.view.View)) 

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

For example, if the value type is String, the body of the method would proxy to [TypedArray.getString(int)](https://developer.android.com/reference/kotlin/android/content/res/TypedArray.html#getString(kotlin.Int)).

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------|
| `a` | [TypedArray](https://developer.android.com/reference/kotlin/android/content/res/TypedArray.html#)!:The set of attributes. |
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

Hook allowing a Preference to re-apply a representation of its internal state that had previously been generated by [onSaveInstanceState](https://developer.android.com/reference/kotlin/android/preference/Preference#onSaveInstanceState()). This function will never be called with a`null`state.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `state` | [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#)!:The saved state that had previously been returned by [onSaveInstanceState](https://developer.android.com/reference/kotlin/android/preference/Preference#onSaveInstanceState()). |

**See Also**

- [#onSaveInstanceState](https://developer.android.com/reference/kotlin/android/preference/Preference#onSaveInstanceState())
- [#restoreHierarchyState](https://developer.android.com/reference/kotlin/android/preference/Preference#restoreHierarchyState(android.os.Bundle)) 

### onSaveInstanceState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onSaveInstanceState(): Parcelable!
```

**Deprecated:** *Deprecated in Java.*

Hook allowing a Preference to generate a representation of its internal state that can later be used to create a new instance with that same state. This state should only contain information that is not persistent or can be reconstructed later.

| Return ||
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#)! | A Parcelable object containing the current dynamic state of this Preference, or`null`if there is nothing interesting to save. The default implementation returns`null`. |

**See Also**

- [#onRestoreInstanceState](https://developer.android.com/reference/kotlin/android/preference/Preference#onRestoreInstanceState(android.os.Parcelable))
- [#saveHierarchyState](https://developer.android.com/reference/kotlin/android/preference/Preference#saveHierarchyState(android.os.Bundle)) 

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

If restorePersistedValue is true, you should restore the Preference value from the [android.content.SharedPreferences](https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#). If restorePersistedValue is false, you should set the Preference value to defaultValue that is given (and possibly store to SharedPreferences if [shouldPersist()](https://developer.android.com/reference/kotlin/android/preference/Preference#shouldPersist())is true).

In case of using [PreferenceDataStore](https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore), the restorePersistedValue is always`true`. But the default value (if provided) is set.

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

- [#persistString(String)](https://developer.android.com/reference/kotlin/android/preference/Preference#persistString(kotlin.String))
- [#getPersistedBoolean(boolean)](https://developer.android.com/reference/kotlin/android/preference/Preference#getPersistedBoolean(kotlin.Boolean)) 

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

- [#persistString(String)](https://developer.android.com/reference/kotlin/android/preference/Preference#persistString(kotlin.String))
- [#getPersistedFloat(float)](https://developer.android.com/reference/kotlin/android/preference/Preference#getPersistedFloat(kotlin.Float)) 

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

- [#persistString(String)](https://developer.android.com/reference/kotlin/android/preference/Preference#persistString(kotlin.String))
- [#getPersistedInt(int)](https://developer.android.com/reference/kotlin/android/preference/Preference#getPersistedInt(kotlin.Int)) 

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

- [#persistString(String)](https://developer.android.com/reference/kotlin/android/preference/Preference#persistString(kotlin.String))
- [#getPersistedLong(long)](https://developer.android.com/reference/kotlin/android/preference/Preference#getPersistedLong(kotlin.Long)) 

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

- [#getPersistedString(String)](https://developer.android.com/reference/kotlin/android/preference/Preference#getPersistedString(kotlin.String)) 

### shouldPersist

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun shouldPersist(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Checks whether, at the given time this method is called, this Preference should store/restore its value(s) into the [SharedPreferences](https://developer.android.com/reference/kotlin/android/content/SharedPreferences.html#) or into [PreferenceDataStore](https://developer.android.com/reference/kotlin/android/preference/PreferenceDataStore) if assigned. This, at minimum, checks whether this Preference is persistent and it currently has a key. Before you save/restore from the storage, check this first.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if it should persist the value. |
