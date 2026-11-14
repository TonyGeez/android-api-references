# SubMenu

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SubMenu

Kotlin| [Java](../android/view/SubMenu.md) 
| --- | --- |

```
interface SubMenu : Menu
```

| [android.view.SubMenu](../android/view/SubMenu.md) |

Subclass of [Menu](../android/view/Menu.md) for sub menus.

Sub menus do not support item icons, or nested sub menus.
|
| ### Developer Guides
|
| For information about creating menus, read the [Menus](https://developer.android.com/guide/topics/ui/menus.html) developer guide.

## Summary

| Inherited constants ||
|---|---|
| From class [Menu](../android/view/Menu.md) |----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CATEGORY_ALTERNATIVE](../android/view/Menu.md) <br /> Category code for the order integer for items/groups that are alternative actions on the data that is currently displayed -- or/add this with your base value. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CATEGORY_CONTAINER](../android/view/Menu.md) <br /> Category code for the order integer for items/groups that are part of a container -- or/add this with your base value. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CATEGORY_SECONDARY](../android/view/Menu.md) <br /> Category code for the order integer for items/groups that are user-supplied secondary (infrequently used) options -- or/add this with your base value. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CATEGORY_SYSTEM](../android/view/Menu.md) <br /> Category code for the order integer for items/groups that are provided by the system -- or/add this with your base value. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FIRST](../android/view/Menu.md) <br /> First value for group and item identifier integers. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_ALWAYS_PERFORM_CLOSE](../android/view/Menu.md) <br /> Flag for [performShortcut(int,android.view.KeyEvent,int)](../android/view/Menu.md)): if set, always close the menu after executing the shortcut. Closing the menu also resets the prepared state. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_APPEND_TO_GROUP](../android/view/Menu.md) <br /> Flag for [addIntentOptions](../android/view/Menu.md)): if set, do not automatically remove any existing menu items in the same group. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_PERFORM_NO_CLOSE](../android/view/Menu.md) <br /> Flag for [performShortcut](../android/view/Menu.md)): if set, do not close the menu after executing the shortcut. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NONE](../android/view/Menu.md) <br /> Value to use for group and item identifier integers when you don't care about them. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SUPPORTED_MODIFIERS_MASK](../android/view/Menu.md) <br /> A mask of all supported modifiers for MenuItem's keyboard shortcuts <br /> | ||

| Public methods ||
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearHeader](../android/view/SubMenu.md))`()` Clears the header of the submenu. |
| abstract [MenuItem](../android/view/MenuItem.md)! | [getItem](../android/view/SubMenu.md))`()` Gets the [MenuItem](../android/view/MenuItem.md) that represents this submenu in the parent menu. |
| abstract [SubMenu](../android/view/SubMenu.md)! | [setHeaderIcon](../android/view/SubMenu.md))`(`icon:` ` [Drawable](../android/graphics/drawable/Drawable.md)!`)` Sets the submenu header's icon to the icon given in icon [Drawable](../android/graphics/drawable/Drawable.md). |
| --- | --- |
| abstract [SubMenu](../android/view/SubMenu.md)! | [setHeaderIcon](../android/view/SubMenu.md))`(`iconRes:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the submenu header's icon to the icon given in iconRes resource id. |
| abstract [SubMenu](../android/view/SubMenu.md)! | [setHeaderTitle](../android/view/SubMenu.md))`(`titleRes:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the submenu header's title to the title given in titleRes resource identifier. |
| abstract [SubMenu](../android/view/SubMenu.md)! | [setHeaderTitle](../android/view/SubMenu.md))`(`title:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Sets the submenu header's title to the title given in title. |
| --- | --- |
| abstract [SubMenu](../android/view/SubMenu.md)! | [setHeaderView](../android/view/SubMenu.md))`(`view:` ` [View](../android/view/View.md)!`)` Sets the header of the submenu to the [View](../android/view/View.md) given in view. |
| abstract [SubMenu](../android/view/SubMenu.md)! | [setIcon](../android/view/SubMenu.md))`(`icon:` ` [Drawable](../android/graphics/drawable/Drawable.md)!`)` Change the icon associated with this submenu's item in its parent menu. |
| abstract [SubMenu](../android/view/SubMenu.md)! | [setIcon](../android/view/SubMenu.md))`(`iconRes:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Change the icon associated with this submenu's item in its parent menu. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [Menu](../android/view/Menu.md) |------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [MenuItem](../android/view/MenuItem.md)! | [add](../android/view/Menu.md))`(`titleRes:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Add a new item to the menu. This item displays the given title for its label. <br /> | | [MenuItem](../android/view/MenuItem.md)! | [add](../android/view/Menu.md))`(`groupId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `itemId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `order:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `titleRes:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Variation on [add(int,int,int,java.lang.CharSequence)](../android/view/Menu.md))that takes a string resource identifier instead of the string itself. <br /> | | [MenuItem](../android/view/MenuItem.md)! | [add](../android/view/Menu.md))`(`groupId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `itemId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `order:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `title:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` <br /> Add a new item to the menu. This item displays the given title for its label. <br /> | | [MenuItem](../android/view/MenuItem.md)! | [add](../android/view/Menu.md))`(`title:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` <br /> Add a new item to the menu. This item displays the given title for its label. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [addIntentOptions](../android/view/Menu.md))`(`groupId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `itemId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `order:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `caller:` ` [ComponentName](../android/content/ComponentName.md)!`, `specifics:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Intent](../android/content/Intent.md)!>!`, `intent:` ` [Intent](../android/content/Intent.md)!`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `outSpecificItems:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [MenuItem](../android/view/MenuItem.md)!>!`)` <br /> Add a group of menu items corresponding to actions that can be performed for a particular Intent. The Intent is most often configured with a null action, the data that the current activity is working with, and includes either the [Intent.CATEGORY_ALTERNATIVE](../android/content/Intent.md) or [Intent.CATEGORY_SELECTED_ALTERNATIVE](../android/content/Intent.md) to find activities that have said they would like to be included as optional action. You can, however, use any Intent you want. See android.content.pm.PackageManager#queryIntentActivityOptions for more \* details on the caller, specifics, and intent arguments. The list returned by that function is used to populate the resulting menu items. All of the menu items of possible options for the intent will be added with the given group and id. You can use the group to control ordering of the items in relation to other items in the menu. Normally this function will automatically remove any existing items in the menu in the same group and place a divider above and below the added items; this behavior can be modified with the flags parameter. For each of the generated items [MenuItem.setIntent](../android/view/MenuItem.md))is called to associate the appropriate Intent with the item; this means the activity will automatically be started for you without having to do anything else. <br /> | | [SubMenu](../android/view/SubMenu.md)! | [addSubMenu](../android/view/Menu.md))`(`titleRes:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Add a new sub-menu to the menu. This item displays the given title for its label. To modify other attributes on the submenu's menu item, use [SubMenu.getItem()](../android/view/SubMenu.md)). <br /> | | [SubMenu](../android/view/SubMenu.md)! | [addSubMenu](../android/view/Menu.md))`(`groupId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `itemId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `order:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `titleRes:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Variation on [addSubMenu(int,int,int,java.lang.CharSequence)](../android/view/Menu.md))that takes a string resource identifier for the title instead of the string itself. <br /> | | [SubMenu](../android/view/SubMenu.md)! | [addSubMenu](../android/view/Menu.md))`(`groupId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `itemId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `order:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `title:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` <br /> Add a new sub-menu to the menu. This item displays the given title for its label. To modify other attributes on the submenu's menu item, use [SubMenu.getItem()](../android/view/SubMenu.md)). Note that you can only have one level of sub-menus, i.e. you cannnot add a subMenu to a subMenu: An [UnsupportedOperationException](../java/lang/UnsupportedOperationException.md) will be thrown if you try. <br /> | | [SubMenu](../android/view/SubMenu.md)! | [addSubMenu](../android/view/Menu.md))`(`title:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` <br /> Add a new sub-menu to the menu. This item displays the given title for its label. To modify other attributes on the submenu's menu item, use [SubMenu.getItem()](../android/view/SubMenu.md)). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](../android/view/Menu.md))`()` <br /> Remove all existing items from the menu, leaving it empty as if it had just been created. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](../android/view/Menu.md))`()` <br /> Closes the menu, if open. <br /> | | [MenuItem](../android/view/MenuItem.md)! | [findItem](../android/view/Menu.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Return the menu item with a particular identifier. <br /> | | [MenuItem](../android/view/MenuItem.md)! | [getItem](../android/view/Menu.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Gets the menu item at the given index. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasVisibleItems](../android/view/Menu.md))`()` <br /> Return whether the menu currently has item items that are visible. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isShortcutKey](../android/view/Menu.md))`(`keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](../android/view/KeyEvent.md)!`)` <br /> Is a keypress one of the defined shortcut keys for this window. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [performIdentifierAction](../android/view/Menu.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Execute the menu item action associated with the given menu identifier. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [performShortcut](../android/view/Menu.md))`(`keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](../android/view/KeyEvent.md)!`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Execute the menu item action associated with the given shortcut character. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeGroup](../android/view/Menu.md))`(`groupId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Remove all items in the given group. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeItem](../android/view/Menu.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Remove the item with the given identifier. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setGroupCheckable](../android/view/Menu.md))`(`group:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `checkable:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `exclusive:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Control whether a particular group of items can show a check mark. This is similar to calling [MenuItem.setCheckable](../android/view/MenuItem.md))on all of the menu items with the given group identifier, but in addition you can control whether this group contains a mutually-exclusive set items. This should be called after the items of the group have been added to the menu. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setGroupDividerEnabled](../android/view/Menu.md))`(`groupDividerEnabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Enable or disable the group dividers. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setGroupEnabled](../android/view/Menu.md))`(`group:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Enable or disable all menu items that are in the given group. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setGroupVisible](../android/view/Menu.md))`(`group:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `visible:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Show or hide all menu items that are in the given group. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setQwertyMode](../android/view/Menu.md))`(`isQwerty:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Control whether the menu should be running in qwerty mode (alphabetic shortcuts) or 12-key mode (numeric shortcuts). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [size](../android/view/Menu.md))`()` <br /> Get the number of items in the menu. Note that this will change any times items are added or removed from the menu. <br /> | ||

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

Gets the [MenuItem](../android/view/MenuItem.md) that represents this submenu in the parent menu. Use this for setting additional item attributes.

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [MenuItem](../android/view/MenuItem.md)! | The [MenuItem](../android/view/MenuItem.md) that launches the submenu when invoked. |

### setHeaderIcon

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setHeaderIcon(icon: Drawable!): SubMenu!
```

Sets the submenu header's icon to the icon given in icon [Drawable](../android/graphics/drawable/Drawable.md).

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `icon` | [Drawable](../android/graphics/drawable/Drawable.md)!:The [Drawable](../android/graphics/drawable/Drawable.md) used for the icon. |

| Return ||
|----------------------------------------------------------------------------------|---------------------------------------------------|
| [SubMenu](../android/view/SubMenu.md)! | This SubMenu so additional setters can be called. |

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
| [SubMenu](../android/view/SubMenu.md)! | This SubMenu so additional setters can be called. |

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
| [SubMenu](../android/view/SubMenu.md)! | This SubMenu so additional setters can be called. |

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
| [SubMenu](../android/view/SubMenu.md)! | This SubMenu so additional setters can be called. |

### setHeaderView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setHeaderView(view: View!): SubMenu!
```

Sets the header of the submenu to the [View](../android/view/View.md) given in view. This replaces the header title and icon (and those replace this).

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [View](../android/view/View.md)!:The [View](../android/view/View.md) used for the header. |

| Return ||
|----------------------------------------------------------------------------------|---------------------------------------------------|
| [SubMenu](../android/view/SubMenu.md)! | This SubMenu so additional setters can be called. |

### setIcon

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setIcon(icon: Drawable!): SubMenu!
```

Change the icon associated with this submenu's item in its parent menu.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `icon` | [Drawable](../android/graphics/drawable/Drawable.md)!:The new icon (as a Drawable) to be displayed. |

| Return ||
|----------------------------------------------------------------------------------|---------------------------------------------------|
| [SubMenu](../android/view/SubMenu.md)! | This SubMenu so additional setters can be called. |

**See Also**

- [android.view.MenuItem#setIcon(Drawable)](../android/view/MenuItem.md)) 

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
| [SubMenu](../android/view/SubMenu.md)! | This SubMenu so additional setters can be called. |

**See Also**

- [android.view.MenuItem#setIcon(int)](../android/view/MenuItem.md))
