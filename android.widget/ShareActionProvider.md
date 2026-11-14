# ShareActionProvider

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ShareActionProvider

Kotlin| [Java](../android/widget/ShareActionProvider.md) 
| --- | --- |

```
open class ShareActionProvider : ActionProvider
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.view.ActionProvider](../android/view/ActionProvider.md) ||
| | ↳ | [android.widget.ShareActionProvider](../android/widget/ShareActionProvider.md) |

This is a provider for a share action. It is responsible for creating views that enable data sharing and also to show a sub menu with sharing activities if the hosting item is placed on the overflow menu.

Here is how to use the action provider with custom backing file in a [MenuItem](../android/view/MenuItem.md): 

```kotlin
// In Activity#onCreateOptionsMenu
  public boolean onCreateOptionsMenu(Menu menu) {
      // Get the menu item.
      MenuItem menuItem = menu.findItem(R.id.my_menu_item);
      // Get the provider and hold onto it to set/change the share intent.
      mShareActionProvider = (ShareActionProvider) menuItem.getActionProvider();
      // Set history different from the default before getting the action
      // view since a call to <code><a docref="android.view.MenuItem$getActionView()">MenuItem.getActionView()</a></code>calls
      // <code><a docref="android.view.ActionProvider$onCreateActionView()">ActionProvider.onCreateActionView()</a></code>which uses the backing file name. Omit this
      // line if using the default share history file is desired.
      mShareActionProvider.setShareHistoryFileName("custom_share_history.xml");
      . . .
  }
 
  // Somewhere in the application.
  public void doShare(Intent shareIntent) {
      // When you want to share set the share intent.
      mShareActionProvider.setShareIntent(shareIntent);
  }
```

**Note:**While the sample snippet demonstrates how to use this provider in the context of a menu item, the use of the provider is not limited to menu items.

## Summary

| Nested classes ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [OnShareTargetSelectedListener](../android/widget/ShareActionProvider.OnShareTargetSelectedListener.md) Listener for the event of selecting a share target. |

| Constants ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [DEFAULT_SHARE_HISTORY_FILE_NAME](../android/widget/ShareActionProvider.md) The default name for storing share history. |

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ShareActionProvider](../android/widget/ShareActionProvider.md))`(`context:` ` [Context](../android/content/Context.md)!`)` Creates a new instance. |

| Public methods ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasSubMenu](../android/widget/ShareActionProvider.md))`()` Determines if this ActionProvider has a submenu associated with it. |
| open [View](../android/view/View.md) | [onCreateActionView](../android/widget/ShareActionProvider.md))`()` Factory method called by the Android framework to create new action views. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPrepareSubMenu](../android/widget/ShareActionProvider.md))`(`subMenu:` ` [SubMenu](../android/view/SubMenu.md)`)` Called to prepare an associated submenu for the menu item backed by this ActionProvider. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnShareTargetSelectedListener](../android/widget/ShareActionProvider.md))`(`listener:` ` [ShareActionProvider.OnShareTargetSelectedListener](../android/widget/ShareActionProvider.OnShareTargetSelectedListener.md)!`)` Sets a listener to be notified when a share target has been selected. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setShareHistoryFileName](../android/widget/ShareActionProvider.md))`(`shareHistoryFile:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the file name of a file for persisting the share history which history will be used for ordering share targets. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setShareIntent](../android/widget/ShareActionProvider.md))`(`shareIntent:` ` [Intent](../android/content/Intent.md)!`)` Sets an intent with information about the share action. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [ActionProvider](../android/view/ActionProvider.md) |------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isVisible](../android/view/ActionProvider.md))`()` <br /> If [overridesItemVisibility()](../android/view/ActionProvider.md))returns true, the return value of this method will help determine the visibility of the [MenuItem](../android/view/MenuItem.md) this ActionProvider is bound to. If the MenuItem's visibility is explicitly set to false by the application, the MenuItem will not be shown, even if this method returns true. <br /> | | [View](../android/view/View.md) | [onCreateActionView](../android/view/ActionProvider.md))`(`forItem:` ` [MenuItem](../android/view/MenuItem.md)`)` <br /> Factory method called by the Android framework to create new action views. This method returns a new action view for the given MenuItem. If your ActionProvider implementation overrides the deprecated no-argument overload [onCreateActionView()](../android/view/ActionProvider.md)), overriding this method for devices running API 16 or later is recommended but optional. The default implementation calls [onCreateActionView()](../android/view/ActionProvider.md))for compatibility with applications written for older platform versions. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onPerformDefaultAction](../android/view/ActionProvider.md))`()` <br /> Performs an optional default action. For the case of an action provider placed in a menu item not shown as an action this method is invoked if previous callbacks for processing menu selection has handled the event. A menu item selection is processed in the following order: - Receiving a call to [MenuItem.OnMenuItemClickListener.onMenuItemClick](../android/view/MenuItem.OnMenuItemClickListener.md)). - Receiving a call to [Activity.onOptionsItemSelected(MenuItem)](../android/app/Activity.md)) - Receiving a call to [Fragment.onOptionsItemSelected(MenuItem)](../android/app/Fragment.md)) - Launching the [android.content.Intent](../android/content/Intent.md) set via [MenuItem.setIntent(android.content.Intent)](../android/view/MenuItem.md)) - Invoking this method. <br /> The default implementation does not perform any action and returns false. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [overridesItemVisibility](../android/view/ActionProvider.md))`()` <br /> The result of this method determines whether or not [isVisible()](../android/view/ActionProvider.md))will be used by the [MenuItem](../android/view/MenuItem.md) this ActionProvider is bound to help determine its visibility. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [refreshVisibility](../android/view/ActionProvider.md))`()` <br /> If this ActionProvider is associated with an item in a menu, refresh the visibility of the item based on [overridesItemVisibility()](../android/view/ActionProvider.md))and [isVisible()](../android/view/ActionProvider.md)). If [overridesItemVisibility()](../android/view/ActionProvider.md))returns false, this call will have no effect. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setVisibilityListener](../android/view/ActionProvider.md))`(`listener:` ` [ActionProvider.VisibilityListener](../android/view/ActionProvider.VisibilityListener.md)?`)` <br /> Set a listener to be notified when this ActionProvider's overridden visibility changes. This should only be used by MenuItem implementations. <br /> | ||

## Constants

### DEFAULT_SHARE_HISTORY_FILE_NAME

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DEFAULT_SHARE_HISTORY_FILE_NAME: String
```

The default name for storing share history. 

 Value: "share_history.xml"

## Public constructors

### ShareActionProvider

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ShareActionProvider(context: Context!)
```

Creates a new instance.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md)!:Context for accessing resources. |

## Public methods

### hasSubMenu

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasSubMenu(): Boolean
```

Determines if this ActionProvider has a submenu associated with it.

Associated submenus will be shown when an action view is not. This provider instance will receive a call to [onPrepareSubMenu(android.view.SubMenu)](../android/view/ActionProvider.md))after the call to [onPerformDefaultAction()](../android/view/ActionProvider.md))and before a submenu is displayed to the user.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the item backed by this provider should have an associated submenu |

### onCreateActionView

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onCreateActionView(): View
```

Factory method called by the Android framework to create new action views.

This method has been deprecated in favor of [onCreateActionView(android.view.MenuItem)](../android/view/ActionProvider.md)). Newer apps that wish to support platform versions prior to API 16 should also implement this method to return a valid action view.

| Return ||
|--------------------------------------------------------------------------------|------------------------------------------------|
| [View](../android/view/View.md) | A new action view. This value cannot be`null`. |

### onPrepareSubMenu

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onPrepareSubMenu(subMenu: SubMenu): Unit
```

Called to prepare an associated submenu for the menu item backed by this ActionProvider.

if [hasSubMenu()](../android/view/ActionProvider.md))returns true, this method will be called when the menu item is selected to prepare the submenu for presentation to the user. Apps may use this to create or alter submenu content right before display.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `subMenu` | [SubMenu](../android/view/SubMenu.md):Submenu that will be displayed This value cannot be`null`. |

### setOnShareTargetSelectedListener

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOnShareTargetSelectedListener(listener: ShareActionProvider.OnShareTargetSelectedListener!): Unit
```

Sets a listener to be notified when a share target has been selected. The listener can optionally decide to handle the selection and not rely on the default behavior which is to launch the activity.

**Note:**If you choose the backing share history file you will still be notified in this callback.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [ShareActionProvider.OnShareTargetSelectedListener](../android/widget/ShareActionProvider.OnShareTargetSelectedListener.md)!:The listener. |

### setShareHistoryFileName

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setShareHistoryFileName(shareHistoryFile: String!): Unit
```

Sets the file name of a file for persisting the share history which history will be used for ordering share targets. This file will be used for all view created by [onCreateActionView()](../android/widget/ShareActionProvider.md)). Defaults to [DEFAULT_SHARE_HISTORY_FILE_NAME](../android/widget/ShareActionProvider.md). Set to`null`if share history should not be persisted between sessions.

**Note:** The history file name can be set any time, however only the action views created by [onCreateActionView()](../android/widget/ShareActionProvider.md))after setting the file name will be backed by the provided file. Therefore, if you want to use different history files for sharing specific types of content, every time you change the history file [setShareHistoryFileName(java.lang.String)](../android/widget/ShareActionProvider.md))you must call [android.app.Activity#invalidateOptionsMenu()](../android/app/Activity.md))to recreate the action view. You should**not** call [android.app.Activity#invalidateOptionsMenu()](../android/app/Activity.md))from [android.app.Activity#onCreateOptionsMenu(Menu)](../android/app/Activity.md)). 

```kotlin
private void doShare(Intent intent) {
      if (IMAGE.equals(intent.getMimeType())) {
          mShareActionProvider.setHistoryFileName(SHARE_IMAGE_HISTORY_FILE_NAME);
      } else if (TEXT.equals(intent.getMimeType())) {
          mShareActionProvider.setHistoryFileName(SHARE_TEXT_HISTORY_FILE_NAME);
      }
      mShareActionProvider.setIntent(intent);
      invalidateOptionsMenu();
  }
```

| Parameters ||
|--------------------|----------------------------------------------------------------------------------------------------------------|
| `shareHistoryFile` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The share history file name. |

### setShareIntent

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setShareIntent(shareIntent: Intent!): Unit
```

Sets an intent with information about the share action. Here is a sample for constructing a share intent: 

```kotlin
Intent shareIntent = new Intent(Intent.ACTION_SEND);
  shareIntent.setType("image/*");
  Uri uri = Uri.fromFile(new File(getFilesDir(), "foo.jpg"));
  shareIntent.putExtra(Intent.EXTRA_STREAM, uri);
```

<br />

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------|
| `shareIntent` | [Intent](../android/content/Intent.md)!:The share intent. |

**See Also**

- [android.content.Intent#ACTION_SEND](../android/content/Intent.md)
- [android.content.Intent#ACTION_SEND_MULTIPLE](../android/content/Intent.md)
