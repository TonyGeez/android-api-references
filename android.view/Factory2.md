# LayoutInflater.Factory2

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Factory2

Kotlin| [Java](https://developer.android.com/reference/android/view/LayoutInflater.Factory2 "View this page in Java") 
| --- | --- |

```
interface Factory2 : LayoutInflater.Factory
```

| [android.view.LayoutInflater.Factory2](https://developer.android.com/reference/kotlin/android/view/LayoutInflater.Factory2#) |

| Known Direct Subclasses [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#) |---------------------------------------------------------------------------------------|--------------------------------------------------------------| | [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#) | An activity is a single, focused thing that the user can do. | |
| --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [AccountAuthenticatorActivity](https://developer.android.com/reference/kotlin/android/accounts/AccountAuthenticatorActivity.html#), [ActivityGroup](https://developer.android.com/reference/kotlin/android/app/ActivityGroup.html#), [AliasActivity](https://developer.android.com/reference/kotlin/android/app/AliasActivity.html#), [ExpandableListActivity](https://developer.android.com/reference/kotlin/android/app/ExpandableListActivity.html#), [LauncherActivity](https://developer.android.com/reference/kotlin/android/app/LauncherActivity.html#), [ListActivity](https://developer.android.com/reference/kotlin/android/app/ListActivity.html#), [NativeActivity](https://developer.android.com/reference/kotlin/android/app/NativeActivity.html#), [PreferenceActivity](https://developer.android.com/reference/kotlin/android/preference/PreferenceActivity.html#), [TabActivity](https://developer.android.com/reference/kotlin/android/app/TabActivity.html#) |------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AccountAuthenticatorActivity](https://developer.android.com/reference/kotlin/android/accounts/AccountAuthenticatorActivity.html#) | Base class for implementing an Activity that is used to help implement an AbstractAccountAuthenticator. | | [ActivityGroup](https://developer.android.com/reference/kotlin/android/app/ActivityGroup.html#) | A screen that contains and runs multiple embedded activities. | | [AliasActivity](https://developer.android.com/reference/kotlin/android/app/AliasActivity.html#) | Stub activity that launches another activity (and then finishes itself) based on information in its component's manifest meta-data. | | [ExpandableListActivity](https://developer.android.com/reference/kotlin/android/app/ExpandableListActivity.html#) | An activity that displays an expandable list of items by binding to a data source implementing the ExpandableListAdapter, and exposes event handlers when the user selects an item. | | [LauncherActivity](https://developer.android.com/reference/kotlin/android/app/LauncherActivity.html#) | Displays a list of all activities which can be performed for a given intent. | | [ListActivity](https://developer.android.com/reference/kotlin/android/app/ListActivity.html#) | An activity that displays a list of items by binding to a data source such as an array or Cursor, and exposes event handlers when the user selects an item. | | [NativeActivity](https://developer.android.com/reference/kotlin/android/app/NativeActivity.html#) | Convenience for implementing an activity that will be implemented purely in native code. | | [PreferenceActivity](https://developer.android.com/reference/kotlin/android/preference/PreferenceActivity.html#) | This is the base class for an activity to show a hierarchy of preferences to the user. | | [TabActivity](https://developer.android.com/reference/kotlin/android/app/TabActivity.html#) | For apps developing against [android.os.Build.VERSION_CODES#HONEYCOMB](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#HONEYCOMB:kotlin.Int) or later, tabs are typically presented in the UI using the new [ActionBar.newTab()](https://developer.android.com/reference/kotlin/android/app/ActionBar.html#newTab())and related APIs for placing tabs within their action bar area. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

## Summary

| Public methods ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [View](https://developer.android.com/reference/kotlin/android/view/View)? | [onCreateView](https://developer.android.com/reference/kotlin/android/view/LayoutInflater.Factory2#onCreateView(android.view.View,%20kotlin.String,%20android.content.Context,%20android.util.AttributeSet))`(`parent:` ` [View](https://developer.android.com/reference/kotlin/android/view/View)?`, `name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)`, `attrs:` ` [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)`)` Version of [onCreateView(java.lang.String,android.content.Context,android.util.AttributeSet)](https://developer.android.com/reference/kotlin/android/view/LayoutInflater.Factory#onCreateView(kotlin.String,%20android.content.Context,%20android.util.AttributeSet))that also supplies the parent that the view created view will be placed in. |

| Inherited functions ||
|---|---|
| From class [Factory](https://developer.android.com/reference/kotlin/android/view/LayoutInflater.Factory) |---------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [View](https://developer.android.com/reference/kotlin/android/view/View)? | [onCreateView](https://developer.android.com/reference/kotlin/android/view/LayoutInflater.Factory#onCreateView(kotlin.String,%20android.content.Context,%20android.util.AttributeSet))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)`, `attrs:` ` [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#)`)` <br /> Hook you can supply that is called when inflating from a LayoutInflater. You can use this to customize the tag names available in your XML layout files. Note that it is good practice to prefix these custom names with your package (i.e., com.coolcompany.apps) to avoid conflicts with system names. <br /> | ||

## Public methods

### onCreateView

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onCreateView(
    parent: View?, 
    name: String, 
    context: Context, 
    attrs: AttributeSet
): View?
```

Version of [onCreateView(java.lang.String,android.content.Context,android.util.AttributeSet)](https://developer.android.com/reference/kotlin/android/view/LayoutInflater.Factory#onCreateView(kotlin.String,%20android.content.Context,%20android.util.AttributeSet))that also supplies the parent that the view created view will be placed in.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parent` | [View](https://developer.android.com/reference/kotlin/android/view/View)?:The parent that the created view will be placed in;*note that this may be null*. |
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):Tag name to be inflated. This value cannot be`null`. |
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#):The context the view is being created in. This value cannot be`null`. |
| --- | --- |
| `attrs` | [AttributeSet](https://developer.android.com/reference/kotlin/android/util/AttributeSet.html#):Inflation attributes as specified in XML file. This value cannot be`null`. |

| Return ||
|---------------------------------------------------------------------------|----------------------------------------------------------------|
| [View](https://developer.android.com/reference/kotlin/android/view/View)? | View Newly created view. Return null for the default behavior. |
