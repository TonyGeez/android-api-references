# SubMenu

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SubMenu

Kotlin| [Java](https://developer.android.com/reference/android/view/SubMenu "View this page in Java") 
| --- | --- |

```
interface SubMenu : Menu
```

| [android.view.SubMenu](https://developer.android.com/reference/kotlin/android/view/SubMenu#) |

Subclass of [Menu](https://developer.android.com/reference/kotlin/android/view/Menu) for sub menus.

Sub menus do not support item icons, or nested sub menus.
|
| ### Developer Guides
|
| For information about creating menus, read the [Menus](https://developer.android.com/guide/topics/ui/menus.html) developer guide.

## Summary

| Inherited constants ||
|---|---|
| From class [Menu](https://developer.android.com/reference/kotlin/android/view/Menu) |----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CATEGORY_ALTERNATIVE](https://developer.android.com/reference/kotlin/android/view/Menu#CATEGORY_ALTERNATIVE:kotlin.Int) <br /> Category code for the order integer for items/groups that are alternative actions on the data that is currently displayed -- or/add this with your base value. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CATEGORY_CONTAINER](https://developer.android.com/reference/kotlin/android/view/Menu#CATEGORY_CONTAINER:kotlin.Int) <br /> Category code for the order integer for items/groups that are part of a container -- or/add this with your base value. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CATEGORY_SECONDARY](https://developer.android.com/reference/kotlin/android/view/Menu#CATEGORY_SECONDARY:kotlin.Int) <br /> Category code for the order integer for items/groups that are user-supplied secondary (infrequently used) options -- or/add this with your base value. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CATEGORY_SYSTEM](https://developer.android.com/reference/kotlin/android/view/Menu#CATEGORY_SYSTEM:kotlin.Int) <br /> Category code for the order integer for items/groups that are provided by the system -- or/add this with your base value. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FIRST](https://developer.android.com/reference/kotlin/android/view/Menu#FIRST:kotlin.Int) <br /> First value for group and item identifier integers. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_ALWAYS_PERFORM_CLOSE](https://developer.android.com/reference/kotlin/android/view/Menu#FLAG_ALWAYS_PERFORM_CLOSE:kotlin.Int) <br /> Flag for [performShortcut(int,android.view.KeyEvent,int)](https://developer.android.com/reference/kotlin/android/view/Menu#performShortcut(kotlin.Int,%20android.view.KeyEvent,%20kotlin.Int)): if set, always close the menu after executing the shortcut. Closing the menu also resets the prepared state. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_APPEND_TO_GROUP](https://developer.android.com/reference/kotlin/android/view/Menu#FLAG_APPEND_TO_GROUP:kotlin.Int) <br /> Flag for [addIntentOptions](https://developer.android.com/reference/kotlin/android/view/Menu#addIntentOptions(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20android.content.ComponentName,%20kotlin.Array,%20android.content.Intent,%20kotlin.Int,%20kotlin.Array)): if set, do not automatically remove any existing menu items in the same group. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_PERFORM_NO_CLOSE](https://developer.android.com/reference/kotlin/android/view/Menu#FLAG_PERFORM_NO_CLOSE:kotlin.Int) <br /> Flag for [performShortcut](https://developer.android.com/reference/kotlin/android/view/Menu#performShortcut(kotlin.Int,%20android.view.KeyEvent,%20kotlin.Int)): if set, do not close the menu after executing the shortcut. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NONE](https://developer.android.com/reference/kotlin/android/view/Menu#NONE:kotlin.Int) <br /> Value to use for group and item identifier integers when you don't care about them. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SUPPORTED_MODIFIERS_MASK](https://developer.android.com/reference/kotlin/android/view/Menu#SUPPORTED_MODIFIERS_MASK:kotlin.Int) <br /> A mask of all supported modifiers for MenuItem's keyboard shortcuts <br /> | ||

| Public methods ||
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearHeader](https://developer.android.com/reference/kotlin/android/view/SubMenu#clearHeader())`()` Clears the header of the submenu. |
| abstract [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem)! | [getItem](https://developer.android.com/reference/kotlin/android/view/SubMenu#getItem())`()` Gets the [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem) that represents this submenu in the parent menu. |
| abstract [SubMenu](https://developer.android.com/reference/kotlin/android/view/SubMenu#)! | [setHeaderIcon](https://developer.android.com/reference/kotlin/android/view/SubMenu#setHeaderIcon(android.graphics.drawable.Drawable))`(`icon:` ` [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)!`)` Sets the submenu header's icon to the icon given in icon [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#). |
| --- | --- |
| abstract [SubMenu](https://developer.android.com/reference/kotlin/android/view/SubMenu#)! | [setHeaderIcon](https://developer.android.com/reference/kotlin/android/view/SubMenu#setHeaderIcon(kotlin.Int))`(`iconRes:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the submenu header's icon to the icon given in iconRes resource id. |
| abstract [SubMenu](https://developer.android.com/reference/kotlin/android/view/SubMenu#)! | [setHeaderTitle](https://developer.android.com/reference/kotlin/android/view/SubMenu#setHeaderTitle(kotlin.Int))`(`titleRes:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the submenu header's title to the title given in titleRes resource identifier. |
| abstract [SubMenu](https://developer.android.com/reference/kotlin/android/view/SubMenu#)! | [setHeaderTitle](https://developer.android.com/reference/kotlin/android/view/SubMenu#setHeaderTitle(kotlin.CharSequence))`(`title:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Sets the submenu header's title to the title given in title. |
| --- | --- |
| abstract [SubMenu](https://developer.android.com/reference/kotlin/android/view/SubMenu#)! | [setHeaderView](https://developer.android.com/reference/kotlin/android/view/SubMenu#setHeaderView(android.view.View))`(`view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View)!`)` Sets the header of the submenu to the [View](https://developer.android.com/reference/kotlin/android/view/View) given in view. |
| abstract [SubMenu](https://developer.android.com/reference/kotlin/android/view/SubMenu#)! | [setIcon](https://developer.android.com/reference/kotlin/android/view/SubMenu#setIcon(android.graphics.drawable.Drawable))`(`icon:` ` [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)!`)` Change the icon associated with this submenu's item in its parent menu. |
| abstract [SubMenu](https://developer.android.com/reference/kotlin/android/view/SubMenu#)! | [setIcon](https://developer.android.com/reference/kotlin/android/view/SubMenu#setIcon(kotlin.Int))`(`iconRes:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Change the icon associated with this submenu's item in its parent menu. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [Menu](https://developer.android.com/reference/kotlin/android/view/Menu) |------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem)! | [add](https://developer.android.com/reference/kotlin/android/view/Menu#add(kotlin.Int))`(`titleRes:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Add a new item to the menu. This item displays the given title for its label. <br /> | | [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem)! | [add](https://developer.android.com/reference/kotlin/android/view/Menu#add(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`groupId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `itemId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `order:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `titleRes:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Variation on [add(int,int,int,java.lang.CharSequence)](https://developer.android.com/reference/kotlin/android/view/Menu#add(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.CharSequence))that takes a string resource identifier instead of the string itself. <br /> | | [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem)! | [add](https://developer.android.com/reference/kotlin/android/view/Menu#add(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.CharSequence))`(`groupId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `itemId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `order:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `title:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` <br /> Add a new item to the menu. This item displays the given title for its label. <br /> | | [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem)! | [add](https://developer.android.com/reference/kotlin/android/view/Menu#add(kotlin.CharSequence))`(`title:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` <br /> Add a new item to the menu. This item displays the given title for its label. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [addIntentOptions](https://developer.android.com/reference/kotlin/android/view/Menu#addIntentOptions(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20android.content.ComponentName,%20kotlin.Array,%20android.content.Intent,%20kotlin.Int,%20kotlin.Array))`(`groupId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `itemId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `order:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `caller:` ` [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#)!`, `specifics:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!>!`, `intent:` ` [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `outSpecificItems:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem)!>!`)` <br /> Add a group of menu items corresponding to actions that can be performed for a particular Intent. The Intent is most often configured with a null action, the data that the current activity is working with, and includes either the [Intent.CATEGORY_ALTERNATIVE](https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_ALTERNATIVE:kotlin.String) or [Intent.CATEGORY_SELECTED_ALTERNATIVE](https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_SELECTED_ALTERNATIVE:kotlin.String) to find activities that have said they would like to be included as optional action. You can, however, use any Intent you want. See android.content.pm.PackageManager#queryIntentActivityOptions for more \* details on the caller, specifics, and intent arguments. The list returned by that function is used to populate the resulting menu items. All of the menu items of possible options for the intent will be added with the given group and id. You can use the group to control ordering of the items in relation to other items in the menu. Normally this function will automatically remove any existing items in the menu in the same group and place a divider above and below the added items; this behavior can be modified with the flags parameter. For each of the generated items [MenuItem.setIntent](https://developer.android.com/reference/kotlin/android/view/MenuItem#setIntent(android.content.Intent))is called to associate the appropriate Intent with the item; this means the activity will automatically be started for you without having to do anything else. <br /> | | [SubMenu](https://developer.android.com/reference/kotlin/android/view/SubMenu#)! | [addSubMenu](https://developer.android.com/reference/kotlin/android/view/Menu#addSubMenu(kotlin.Int))`(`titleRes:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Add a new sub-menu to the menu. This item displays the given title for its label. To modify other attributes on the submenu's menu item, use [SubMenu.getItem()](https://developer.android.com/reference/kotlin/android/view/SubMenu#getItem()). <br /> | | [SubMenu](https://developer.android.com/reference/kotlin/android/view/SubMenu#)! | [addSubMenu](https://developer.android.com/reference/kotlin/android/view/Menu#addSubMenu(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`groupId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `itemId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `order:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `titleRes:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Variation on [addSubMenu(int,int,int,java.lang.CharSequence)](https://developer.android.com/reference/kotlin/android/view/Menu#addSubMenu(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.CharSequence))that takes a string resource identifier for the title instead of the string itself. <br /> | | [SubMenu](https://developer.android.com/reference/kotlin/android/view/SubMenu#)! | [addSubMenu](https://developer.android.com/reference/kotlin/android/view/Menu#addSubMenu(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.CharSequence))`(`groupId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `itemId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `order:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `title:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` <br /> Add a new sub-menu to the menu. This item displays the given title for its label. To modify other attributes on the submenu's menu item, use [SubMenu.getItem()](https://developer.android.com/reference/kotlin/android/view/SubMenu#getItem()). Note that you can only have one level of sub-menus, i.e. you cannnot add a subMenu to a subMenu: An [UnsupportedOperationException](https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#) will be thrown if you try. <br /> | | [SubMenu](https://developer.android.com/reference/kotlin/android/view/SubMenu#)! | [addSubMenu](https://developer.android.com/reference/kotlin/android/view/Menu#addSubMenu(kotlin.CharSequence))`(`title:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` <br /> Add a new sub-menu to the menu. This item displays the given title for its label. To modify other attributes on the submenu's menu item, use [SubMenu.getItem()](https://developer.android.com/reference/kotlin/android/view/SubMenu#getItem()). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](https://developer.android.com/reference/kotlin/android/view/Menu#clear())`()` <br /> Remove all existing items from the menu, leaving it empty as if it had just been created. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/android/view/Menu#close())`()` <br /> Closes the menu, if open. <br /> | | [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem)! | [findItem](https://developer.android.com/reference/kotlin/android/view/Menu#findItem(kotlin.Int))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Return the menu item with a particular identifier. <br /> | | [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem)! | [getItem](https://developer.android.com/reference/kotlin/android/view/Menu#getItem(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Gets the menu item at the given index. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasVisibleItems](https://developer.android.com/reference/kotlin/android/view/Menu#hasVisibleItems())`()` <br /> Return whether the menu currently has item items that are visible. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isShortcutKey](https://developer.android.com/reference/kotlin/android/view/Menu#isShortcutKey(kotlin.Int,%20android.view.KeyEvent))`(`keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent)!`)` <br /> Is a keypress one of the defined shortcut keys for this window. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [performIdentifierAction](https://developer.android.com/reference/kotlin/android/view/Menu#performIdentifierAction(kotlin.Int,%20kotlin.Int))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Execute the menu item action associated with the given menu identifier. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [performShortcut](https://developer.android.com/reference/kotlin/android/view/Menu#performShortcut(kotlin.Int,%20android.view.KeyEvent,%20kotlin.Int))`(`keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent)!`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Execute the menu item action associated with the given shortcut character. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeGroup](https://developer.android.com/reference/kotlin/android/view/Menu#removeGroup(kotlin.Int))`(`groupId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Remove all items in the given group. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeItem](https://developer.android.com/reference/kotlin/android/view/Menu#removeItem(kotlin.Int))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Remove the item with the given identifier. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setGroupCheckable](https://developer.android.com/reference/kotlin/android/view/Menu#setGroupCheckable(kotlin.Int,%20kotlin.Boolean,%20kotlin.Boolean))`(`group:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `checkable:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `exclusive:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Control whether a particular group of items can show a check mark. This is similar to calling [MenuItem.setCheckable](https://developer.android.com/reference/kotlin/android/view/MenuItem#setCheckable(kotlin.Boolean))on all of the menu items with the given group identifier, but in addition you can control whether this group contains a mutually-exclusive set items. This should be called after the items of the group have been added to the menu. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setGroupDividerEnabled](https://developer.android.com/reference/kotlin/android/view/Menu#setGroupDividerEnabled(kotlin.Boolean))`(`groupDividerEnabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Enable or disable the group dividers. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setGroupEnabled](https://developer.android.com/reference/kotlin/android/view/Menu#setGroupEnabled(kotlin.Int,%20kotlin.Boolean))`(`group:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Enable or disable all menu items that are in the given group. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setGroupVisible](https://developer.android.com/reference/kotlin/android/view/Menu#setGroupVisible(kotlin.Int,%20kotlin.Boolean))`(`group:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `visible:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Show or hide all menu items that are in the given group. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setQwertyMode](https://developer.android.com/reference/kotlin/android/view/Menu#setQwertyMode(kotlin.Boolean))`(`isQwerty:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Control whether the menu should be running in qwerty mode (alphabetic shortcuts) or 12-key mode (numeric shortcuts). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [size](https://developer.android.com/reference/kotlin/android/view/Menu#size())`()` <br /> Get the number of items in the menu. Note that this will change any times items are added or removed from the menu. <br /> | ||

## Public methods

### clearHeader

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun clearHeader(): Unit
```

Clears the header of the submenu. 

### getItem

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getItem(): MenuItem!
```

Gets the [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem) that represents this submenu in the parent menu. Use this for setting additional item attributes.

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem)! | The [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem) that launches the submenu when invoked. |

### setHeaderIcon

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setHeaderIcon(icon: Drawable!): SubMenu!
```

Sets the submenu header's icon to the icon given in icon [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#).

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `icon` | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)!:The [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#) used for the icon. |

| Return ||
|----------------------------------------------------------------------------------|---------------------------------------------------|
| [SubMenu](https://developer.android.com/reference/kotlin/android/view/SubMenu#)! | This SubMenu so additional setters can be called. |

### setHeaderIcon

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setHeaderIcon(iconRes: Int): SubMenu!
```

Sets the submenu header's icon to the icon given in iconRes resource id.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------|
| `iconRes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The resource identifier used for the icon. |

| Return ||
|----------------------------------------------------------------------------------|---------------------------------------------------|
| [SubMenu](https://developer.android.com/reference/kotlin/android/view/SubMenu#)! | This SubMenu so additional setters can be called. |

### setHeaderTitle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setHeaderTitle(titleRes: Int): SubMenu!
```

Sets the submenu header's title to the title given in titleRes resource identifier.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------|
| `titleRes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The string resource identifier used for the title. |

| Return ||
|----------------------------------------------------------------------------------|---------------------------------------------------|
| [SubMenu](https://developer.android.com/reference/kotlin/android/view/SubMenu#)! | This SubMenu so additional setters can be called. |

### setHeaderTitle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setHeaderTitle(title: CharSequence!): SubMenu!
```

Sets the submenu header's title to the title given in title.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `title` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:The character sequence used for the title. |

| Return ||
|----------------------------------------------------------------------------------|---------------------------------------------------|
| [SubMenu](https://developer.android.com/reference/kotlin/android/view/SubMenu#)! | This SubMenu so additional setters can be called. |

### setHeaderView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setHeaderView(view: View!): SubMenu!
```

Sets the header of the submenu to the [View](https://developer.android.com/reference/kotlin/android/view/View) given in view. This replaces the header title and icon (and those replace this).

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [View](https://developer.android.com/reference/kotlin/android/view/View)!:The [View](https://developer.android.com/reference/kotlin/android/view/View) used for the header. |

| Return ||
|----------------------------------------------------------------------------------|---------------------------------------------------|
| [SubMenu](https://developer.android.com/reference/kotlin/android/view/SubMenu#)! | This SubMenu so additional setters can be called. |

### setIcon

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setIcon(icon: Drawable!): SubMenu!
```

Change the icon associated with this submenu's item in its parent menu.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `icon` | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)!:The new icon (as a Drawable) to be displayed. |

| Return ||
|----------------------------------------------------------------------------------|---------------------------------------------------|
| [SubMenu](https://developer.android.com/reference/kotlin/android/view/SubMenu#)! | This SubMenu so additional setters can be called. |

**See Also**

- [android.view.MenuItem#setIcon(Drawable)](https://developer.android.com/reference/kotlin/android/view/MenuItem#setIcon(android.graphics.drawable.Drawable)) 

### setIcon

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setIcon(iconRes: Int): SubMenu!
```

Change the icon associated with this submenu's item in its parent menu.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------|
| `iconRes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The new icon (as a resource ID) to be displayed. |

| Return ||
|----------------------------------------------------------------------------------|---------------------------------------------------|
| [SubMenu](https://developer.android.com/reference/kotlin/android/view/SubMenu#)! | This SubMenu so additional setters can be called. |

**See Also**

- [android.view.MenuItem#setIcon(int)](https://developer.android.com/reference/kotlin/android/view/MenuItem#setIcon(kotlin.Int))
