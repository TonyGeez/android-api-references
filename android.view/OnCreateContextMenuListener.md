# View.OnCreateContextMenuListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnCreateContextMenuListener

Kotlin| [Java](../android/view/View.OnCreateContextMenuListener.md) 
| --- | --- |

```
interface OnCreateContextMenuListener
```

| [android.view.View.OnCreateContextMenuListener](../android/view/View.OnCreateContextMenuListener.md) |

| Known Direct Subclasses [Activity](../android.app/Activity.md), [Dialog](../android.app/Dialog.md), [ExpandableListActivity](../android.app/ExpandableListActivity.md), [Fragment](../android.app/Fragment.md) |-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Activity](../android.app/Activity.md) | An activity is a single, focused thing that the user can do. | | [Dialog](../android.app/Dialog.md) | Base class for Dialogs. | | [ExpandableListActivity](../android.app/ExpandableListActivity.md) | An activity that displays an expandable list of items by binding to a data source implementing the ExpandableListAdapter, and exposes event handlers when the user selects an item. | | [Fragment](../android.app/Fragment.md) | A Fragment is a piece of an application's user interface or behavior that can be placed in an [Activity](../android.app/Activity.md). | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [AccountAuthenticatorActivity](../android.accounts/AccountAuthenticatorActivity.md), [ActivityGroup](../android.app/ActivityGroup.md), [AlertDialog](../android.app/AlertDialog.md), [AliasActivity](../android.app/AliasActivity.md), [CharacterPickerDialog](../android.text.method/CharacterPickerDialog.md), [DatePickerDialog](../android.app/DatePickerDialog.md), [DialogFragment](../android.app/DialogFragment.md), [ExpandableListActivity](../android.app/ExpandableListActivity.md), [LauncherActivity](../android.app/LauncherActivity.md), [ListActivity](../android.app/ListActivity.md), [ListFragment](../android.app/ListFragment.md), [NativeActivity](../android.app/NativeActivity.md), and 7 others. |------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AccountAuthenticatorActivity](../android.accounts/AccountAuthenticatorActivity.md) | Base class for implementing an Activity that is used to help implement an AbstractAccountAuthenticator. | | [ActivityGroup](../android.app/ActivityGroup.md) | A screen that contains and runs multiple embedded activities. | | [AlertDialog](../android.app/AlertDialog.md) | A subclass of Dialog that can display one, two or three buttons. | | [AliasActivity](../android.app/AliasActivity.md) | Stub activity that launches another activity (and then finishes itself) based on information in its component's manifest meta-data. | | [CharacterPickerDialog](../android.text.method/CharacterPickerDialog.md) | Dialog for choosing accented characters related to a base character. | | [DatePickerDialog](../android.app/DatePickerDialog.md) | A simple dialog containing an [android.widget.DatePicker](../android.widget/DatePicker.md). | | [DialogFragment](../android.app/DialogFragment.md) | A fragment that displays a dialog window, floating on top of its activity's window. | | [ExpandableListActivity](../android.app/ExpandableListActivity.md) | An activity that displays an expandable list of items by binding to a data source implementing the ExpandableListAdapter, and exposes event handlers when the user selects an item. | | [LauncherActivity](../android.app/LauncherActivity.md) | Displays a list of all activities which can be performed for a given intent. | | [ListActivity](../android.app/ListActivity.md) | An activity that displays a list of items by binding to a data source such as an array or Cursor, and exposes event handlers when the user selects an item. | | [ListFragment](../android.app/ListFragment.md) | A fragment that displays a list of items by binding to a data source such as an array or Cursor, and exposes event handlers when the user selects an item. | | [NativeActivity](../android.app/NativeActivity.md) | Convenience for implementing an activity that will be implemented purely in native code. | | [PreferenceActivity](../android.preference/PreferenceActivity.md) | This is the base class for an activity to show a hierarchy of preferences to the user. | | [PreferenceFragment](../android.preference/PreferenceFragment.md) | Shows a hierarchy of [Preference](../android.preference/Preference.md) objects as lists. | | [Presentation](../android.app/Presentation.md) | Base class for presentations. | | [ProgressDialog](../android.app/ProgressDialog.md) | A dialog showing a progress indicator and an optional text message or view. | | [TabActivity](../android.app/TabActivity.md) | For apps developing against [android.os.Build.VERSION_CODES#HONEYCOMB](../android/os/Build.VERSION_CODES.md) or later, tabs are typically presented in the UI using the new [ActionBar.newTab()](../android.app/ActionBar.md))and related APIs for placing tabs within their action bar area. | | [TimePickerDialog](../android.app/TimePickerDialog.md) | A dialog that prompts the user for the time of day using a [TimePicker](../android.widget/TimePicker.md). | | [WebViewFragment](../android.webkit/WebViewFragment.md) | A fragment that displays a WebView. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Interface definition for a callback to be invoked when the context menu for this view is being built.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCreateContextMenu](../android/view/View.OnCreateContextMenuListener.md))`(`menu:` ` [ContextMenu](ContextMenu.md)!`, `v:` ` [View](View.md)!`, `menuInfo:` ` [ContextMenu.ContextMenuInfo](../android/view/ContextMenu.ContextMenuInfo.md)!`)` Called when the context menu for this view is being built. |

## Public methods

### onCreateContextMenu

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onCreateContextMenu(
    menu: ContextMenu!, 
    v: View!, 
    menuInfo: ContextMenu.ContextMenuInfo!
): Unit
```

Called when the context menu for this view is being built. It is not safe to hold onto the menu after this method returns.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `menu` | [ContextMenu](ContextMenu.md)!:The context menu that is being built |
| `v` | [View](View.md)!:The view for which the context menu is being built |
| `menuInfo` | [ContextMenu.ContextMenuInfo](../android/view/ContextMenu.ContextMenuInfo.md)!:Extra information about the item for which the context menu should be shown. This information will vary depending on the class of v. |
| --- | --- |
