# LayoutInflater.Factory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Factory

Kotlin | [Java](../android/view/LayoutInflater.Factory.md) 
| --- | --- |

```
interface Factory
```

| [android.view.LayoutInflater.Factory](../android/view/LayoutInflater.Factory.md) |

| Known Direct Subclasses [LayoutInflater.Factory2](../android/view/LayoutInflater.Factory2.md) |----------------------------------------------------------------------------------------------------------------|--------| | [LayoutInflater.Factory2](../android/view/LayoutInflater.Factory2.md) | <br /> | |
| --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [AccountAuthenticatorActivity](../android/accounts/AccountAuthenticatorActivity.md), [Activity](../android/app/Activity.md), [ActivityGroup](../android/app/ActivityGroup.md), [AliasActivity](../android/app/AliasActivity.md), [ExpandableListActivity](../android/app/ExpandableListActivity.md), [LauncherActivity](../android/app/LauncherActivity.md), [ListActivity](../android/app/ListActivity.md), [NativeActivity](../android/app/NativeActivity.md), [PreferenceActivity](../android/preference/PreferenceActivity.md), [TabActivity](../android/app/TabActivity.md) |------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AccountAuthenticatorActivity](../android/accounts/AccountAuthenticatorActivity.md) | Base class for implementing an Activity that is used to help implement an AbstractAccountAuthenticator. | | [Activity](../android/app/Activity.md) | An activity is a single, focused thing that the user can do. | | [ActivityGroup](../android/app/ActivityGroup.md) | A screen that contains and runs multiple embedded activities. | | [AliasActivity](../android/app/AliasActivity.md) | Stub activity that launches another activity (and then finishes itself) based on information in its component's manifest meta-data. | | [ExpandableListActivity](../android/app/ExpandableListActivity.md) | An activity that displays an expandable list of items by binding to a data source implementing the ExpandableListAdapter, and exposes event handlers when the user selects an item. | | [LauncherActivity](../android/app/LauncherActivity.md) | Displays a list of all activities which can be performed for a given intent. | | [ListActivity](../android/app/ListActivity.md) | An activity that displays a list of items by binding to a data source such as an array or Cursor, and exposes event handlers when the user selects an item. | | [NativeActivity](../android/app/NativeActivity.md) | Convenience for implementing an activity that will be implemented purely in native code. | | [PreferenceActivity](../android/preference/PreferenceActivity.md) | This is the base class for an activity to show a hierarchy of preferences to the user. | | [TabActivity](../android/app/TabActivity.md) | For apps developing against [android.os.Build.VERSION_CODES#HONEYCOMB](../android/os/Build.VERSION_CODES.md) or later, tabs are typically presented in the UI using the new [ActionBar.newTab()](../android/app/ActionBar.md)) and related APIs for placing tabs within their action bar area. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

## Summary

| Public methods ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [View](../android/view/View.md)? | [onCreateView](../android/view/LayoutInflater.Factory.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `context:` ` [Context](../android/content/Context.md)`, `attrs:` ` [AttributeSet](../android/util/AttributeSet.md)`)` Hook you can supply that is called when inflating from a LayoutInflater. |

## Public methods

### onCreateView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onCreateView(
    name: String, 
    context: Context, 
    attrs: AttributeSet
): View?
```

Hook you can supply that is called when inflating from a LayoutInflater. You can use this to customize the tag names available in your XML layout files.

Note that it is good practice to prefix these custom names with your package (i.e., com.coolcompany.apps) to avoid conflicts with system names.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): Tag name to be inflated. This value cannot be `null`. |
| `context` | [Context](../android/content/Context.md): The context the view is being created in. This value cannot be `null`. |
| `attrs` | [AttributeSet](../android/util/AttributeSet.md): Inflation attributes as specified in XML file. This value cannot be `null`. |
| --- | --- |

| Return ||
|---------------------------------------------------------------------------|----------------------------------------------------------------|
| [View](../android/view/View.md)? | View Newly created view. Return null for the default behavior. |
