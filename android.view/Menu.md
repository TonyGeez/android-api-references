# Menu

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Menu

Kotlin| [Java](https://developer.android.com/reference/android/view/Menu "View this page in Java") 

```
interface Menu
```

| [android.view.Menu](https://developer.android.com/reference/kotlin/android/view/Menu#) |

| Known Direct Subclasses [ContextMenu](https://developer.android.com/reference/kotlin/android/view/ContextMenu), [SubMenu](https://developer.android.com/reference/kotlin/android/view/SubMenu) |----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ContextMenu](https://developer.android.com/reference/kotlin/android/view/ContextMenu) | Extension of [Menu](https://developer.android.com/reference/kotlin/android/view/Menu#) for context menus providing functionality to modify the header of the context menu. | | [SubMenu](https://developer.android.com/reference/kotlin/android/view/SubMenu) | Subclass of [Menu](https://developer.android.com/reference/kotlin/android/view/Menu#) for sub menus. | |

Interface for managing the items in a menu.

By default, every Activity supports an options menu of actions or options. You can add items to this menu and handle clicks on your additions. The easiest way of adding menu items is inflating an XML file into the [Menu](https://developer.android.com/reference/kotlin/android/view/Menu#) via [MenuInflater](https://developer.android.com/reference/kotlin/android/view/MenuInflater). The easiest way of attaching code to clicks is via [Activity.onOptionsItemSelected(MenuItem)](https://developer.android.com/reference/kotlin/android/app/Activity.html#onOptionsItemSelected(android.view.MenuItem))and [Activity.onContextItemSelected(MenuItem)](https://developer.android.com/reference/kotlin/android/app/Activity.html#onContextItemSelected(android.view.MenuItem)).

Different menu types support different features:

1. **Context menus**: Do not support item shortcuts and item icons.
2. **Options menus** : The**icon menus** do not support item check marks and only show the item's [condensed title](https://developer.android.com/reference/kotlin/android/view/MenuItem#setTitleCondensed(kotlin.CharSequence)). The**expanded menus**(only available if six or more menu items are visible, reached via the 'More' item in the icon menu) do not show item icons, and item check marks are discouraged.
3. **Sub menus**: Do not support item icons, or nested sub menus.

| ### Developer Guides
|
| For more information about creating menus, read the [Menus](https://developer.android.com/guide/topics/ui/menus.html) developer guide.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CATEGORY_ALTERNATIVE](https://developer.android.com/reference/kotlin/android/view/Menu#CATEGORY_ALTERNATIVE:kotlin.Int) Category code for the order integer for items/groups that are alternative actions on the data that is currently displayed -- or/add this with your base value. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CATEGORY_CONTAINER](https://developer.android.com/reference/kotlin/android/view/Menu#CATEGORY_CONTAINER:kotlin.Int) Category code for the order integer for items/groups that are part of a container -- or/add this with your base value. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CATEGORY_SECONDARY](https://developer.android.com/reference/kotlin/android/view/Menu#CATEGORY_SECONDARY:kotlin.Int) Category code for the order integer for items/groups that are user-supplied secondary (infrequently used) options -- or/add this with your base value. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CATEGORY_SYSTEM](https://developer.android.com/reference/kotlin/android/view/Menu#CATEGORY_SYSTEM:kotlin.Int) Category code for the order integer for items/groups that are provided by the system -- or/add this with your base value. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FIRST](https://developer.android.com/reference/kotlin/android/view/Menu#FIRST:kotlin.Int) First value for group and item identifier integers. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_ALWAYS_PERFORM_CLOSE](https://developer.android.com/reference/kotlin/android/view/Menu#FLAG_ALWAYS_PERFORM_CLOSE:kotlin.Int) Flag for [performShortcut(int,android.view.KeyEvent,int)](https://developer.android.com/reference/kotlin/android/view/Menu#performShortcut(kotlin.Int,%20android.view.KeyEvent,%20kotlin.Int)): if set, always close the menu after executing the shortcut. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_APPEND_TO_GROUP](https://developer.android.com/reference/kotlin/android/view/Menu#FLAG_APPEND_TO_GROUP:kotlin.Int) Flag for [addIntentOptions](https://developer.android.com/reference/kotlin/android/view/Menu#addIntentOptions(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20android.content.ComponentName,%20kotlin.Array,%20android.content.Intent,%20kotlin.Int,%20kotlin.Array)): if set, do not automatically remove any existing menu items in the same group. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_PERFORM_NO_CLOSE](https://developer.android.com/reference/kotlin/android/view/Menu#FLAG_PERFORM_NO_CLOSE:kotlin.Int) Flag for [performShortcut](https://developer.android.com/reference/kotlin/android/view/Menu#performShortcut(kotlin.Int,%20android.view.KeyEvent,%20kotlin.Int)): if set, do not close the menu after executing the shortcut. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NONE](https://developer.android.com/reference/kotlin/android/view/Menu#NONE:kotlin.Int) Value to use for group and item identifier integers when you don't care about them. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SUPPORTED_MODIFIERS_MASK](https://developer.android.com/reference/kotlin/android/view/Menu#SUPPORTED_MODIFIERS_MASK:kotlin.Int) A mask of all supported modifiers for MenuItem's keyboard shortcuts |

| Public methods ||
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem)! | [add](https://developer.android.com/reference/kotlin/android/view/Menu#add(kotlin.Int))`(`titleRes:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Add a new item to the menu. |
| abstract [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem)! | [add](https://developer.android.com/reference/kotlin/android/view/Menu#add(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`groupId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `itemId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `order:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `titleRes:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Variation on [add(int,int,int,java.lang.CharSequence)](https://developer.android.com/reference/kotlin/android/view/Menu#add(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.CharSequence))that takes a string resource identifier instead of the string itself. |
| abstract [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem)! | [add](https://developer.android.com/reference/kotlin/android/view/Menu#add(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.CharSequence))`(`groupId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `itemId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `order:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `title:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Add a new item to the menu. |
| abstract [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem)! | [add](https://developer.android.com/reference/kotlin/android/view/Menu#add(kotlin.CharSequence))`(`title:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Add a new item to the menu. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [addIntentOptions](https://developer.android.com/reference/kotlin/android/view/Menu#addIntentOptions(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20android.content.ComponentName,%20kotlin.Array,%20android.content.Intent,%20kotlin.Int,%20kotlin.Array))`(`groupId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `itemId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `order:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `caller:` ` [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#)!`, `specifics:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!>!`, `intent:` ` [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `outSpecificItems:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem)!>!`)` Add a group of menu items corresponding to actions that can be performed for a particular Intent. |
| abstract [SubMenu](https://developer.android.com/reference/kotlin/android/view/SubMenu)! | [addSubMenu](https://developer.android.com/reference/kotlin/android/view/Menu#addSubMenu(kotlin.Int))`(`titleRes:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Add a new sub-menu to the menu. |
| abstract [SubMenu](https://developer.android.com/reference/kotlin/android/view/SubMenu)! | [addSubMenu](https://developer.android.com/reference/kotlin/android/view/Menu#addSubMenu(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`groupId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `itemId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `order:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `titleRes:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Variation on [addSubMenu(int,int,int,java.lang.CharSequence)](https://developer.android.com/reference/kotlin/android/view/Menu#addSubMenu(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.CharSequence))that takes a string resource identifier for the title instead of the string itself. |
| abstract [SubMenu](https://developer.android.com/reference/kotlin/android/view/SubMenu)! | [addSubMenu](https://developer.android.com/reference/kotlin/android/view/Menu#addSubMenu(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.CharSequence))`(`groupId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `itemId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `order:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `title:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Add a new sub-menu to the menu. |
| abstract [SubMenu](https://developer.android.com/reference/kotlin/android/view/SubMenu)! | [addSubMenu](https://developer.android.com/reference/kotlin/android/view/Menu#addSubMenu(kotlin.CharSequence))`(`title:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Add a new sub-menu to the menu. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](https://developer.android.com/reference/kotlin/android/view/Menu#clear())`()` Remove all existing items from the menu, leaving it empty as if it had just been created. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/android/view/Menu#close())`()` Closes the menu, if open. |
| abstract [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem)! | [findItem](https://developer.android.com/reference/kotlin/android/view/Menu#findItem(kotlin.Int))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the menu item with a particular identifier. |
| abstract [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem)! | [getItem](https://developer.android.com/reference/kotlin/android/view/Menu#getItem(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Gets the menu item at the given index. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasVisibleItems](https://developer.android.com/reference/kotlin/android/view/Menu#hasVisibleItems())`()` Return whether the menu currently has item items that are visible. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isShortcutKey](https://developer.android.com/reference/kotlin/android/view/Menu#isShortcutKey(kotlin.Int,%20android.view.KeyEvent))`(`keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent)!`)` Is a keypress one of the defined shortcut keys for this window. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [performIdentifierAction](https://developer.android.com/reference/kotlin/android/view/Menu#performIdentifierAction(kotlin.Int,%20kotlin.Int))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Execute the menu item action associated with the given menu identifier. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [performShortcut](https://developer.android.com/reference/kotlin/android/view/Menu#performShortcut(kotlin.Int,%20android.view.KeyEvent,%20kotlin.Int))`(`keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent)!`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Execute the menu item action associated with the given shortcut character. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeGroup](https://developer.android.com/reference/kotlin/android/view/Menu#removeGroup(kotlin.Int))`(`groupId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Remove all items in the given group. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeItem](https://developer.android.com/reference/kotlin/android/view/Menu#removeItem(kotlin.Int))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Remove the item with the given identifier. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setGroupCheckable](https://developer.android.com/reference/kotlin/android/view/Menu#setGroupCheckable(kotlin.Int,%20kotlin.Boolean,%20kotlin.Boolean))`(`group:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `checkable:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `exclusive:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Control whether a particular group of items can show a check mark. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setGroupDividerEnabled](https://developer.android.com/reference/kotlin/android/view/Menu#setGroupDividerEnabled(kotlin.Boolean))`(`groupDividerEnabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Enable or disable the group dividers. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setGroupEnabled](https://developer.android.com/reference/kotlin/android/view/Menu#setGroupEnabled(kotlin.Int,%20kotlin.Boolean))`(`group:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Enable or disable all menu items that are in the given group. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setGroupVisible](https://developer.android.com/reference/kotlin/android/view/Menu#setGroupVisible(kotlin.Int,%20kotlin.Boolean))`(`group:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `visible:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Show or hide all menu items that are in the given group. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setQwertyMode](https://developer.android.com/reference/kotlin/android/view/Menu#setQwertyMode(kotlin.Boolean))`(`isQwerty:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Control whether the menu should be running in qwerty mode (alphabetic shortcuts) or 12-key mode (numeric shortcuts). |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [size](https://developer.android.com/reference/kotlin/android/view/Menu#size())`()` Get the number of items in the menu. |

## Constants

### CATEGORY_ALTERNATIVE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CATEGORY_ALTERNATIVE: Int
```

Category code for the order integer for items/groups that are alternative actions on the data that is currently displayed -- or/add this with your base value. 

 Value: 262144

### CATEGORY_CONTAINER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CATEGORY_CONTAINER: Int
```

Category code for the order integer for items/groups that are part of a container -- or/add this with your base value. 

 Value: 65536

### CATEGORY_SECONDARY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CATEGORY_SECONDARY: Int
```

Category code for the order integer for items/groups that are user-supplied secondary (infrequently used) options -- or/add this with your base value. 

 Value: 196608

### CATEGORY_SYSTEM

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CATEGORY_SYSTEM: Int
```

Category code for the order integer for items/groups that are provided by the system -- or/add this with your base value. 

 Value: 131072

### FIRST

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FIRST: Int
```

First value for group and item identifier integers. 

 Value: 1

### FLAG_ALWAYS_PERFORM_CLOSE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_ALWAYS_PERFORM_CLOSE: Int
```

Flag for [performShortcut(int,android.view.KeyEvent,int)](https://developer.android.com/reference/kotlin/android/view/Menu#performShortcut(kotlin.Int,%20android.view.KeyEvent,%20kotlin.Int)): if set, always close the menu after executing the shortcut. Closing the menu also resets the prepared state. 

 Value: 2

### FLAG_APPEND_TO_GROUP

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_APPEND_TO_GROUP: Int
```

Flag for [addIntentOptions](https://developer.android.com/reference/kotlin/android/view/Menu#addIntentOptions(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20android.content.ComponentName,%20kotlin.Array,%20android.content.Intent,%20kotlin.Int,%20kotlin.Array)): if set, do not automatically remove any existing menu items in the same group. 

 Value: 1

### FLAG_PERFORM_NO_CLOSE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_PERFORM_NO_CLOSE: Int
```

Flag for [performShortcut](https://developer.android.com/reference/kotlin/android/view/Menu#performShortcut(kotlin.Int,%20android.view.KeyEvent,%20kotlin.Int)): if set, do not close the menu after executing the shortcut. 

 Value: 1

### NONE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NONE: Int
```

Value to use for group and item identifier integers when you don't care about them. 

 Value: 0

### SUPPORTED_MODIFIERS_MASK

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUPPORTED_MODIFIERS_MASK: Int
```

A mask of all supported modifiers for MenuItem's keyboard shortcuts 

 Value: 69647

## Public methods

### add

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun add(titleRes: Int): MenuItem!
```

Add a new item to the menu. This item displays the given title for its label.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------|
| `titleRes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Resource identifier of title string. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------|
| [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem)! | The newly added menu item. |

### add

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun add(
    groupId: Int, 
    itemId: Int, 
    order: Int, 
    titleRes: Int
): MenuItem!
```

Variation on [add(int,int,int,java.lang.CharSequence)](https://developer.android.com/reference/kotlin/android/view/Menu#add(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.CharSequence))that takes a string resource identifier instead of the string itself.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `groupId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The group identifier that this item should be part of. This can also be used to define groups of items for batch state changes. Normally use [NONE](https://developer.android.com/reference/kotlin/android/view/Menu#NONE:kotlin.Int) if an item should not be in a group. |
| `itemId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Unique item ID. Use [NONE](https://developer.android.com/reference/kotlin/android/view/Menu#NONE:kotlin.Int) if you do not need a unique ID. |
| `order` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The order for the item. Use [NONE](https://developer.android.com/reference/kotlin/android/view/Menu#NONE:kotlin.Int) if you do not care about the order. See [MenuItem.getOrder()](https://developer.android.com/reference/kotlin/android/view/MenuItem#getOrder()). |
| `titleRes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Resource identifier of title string. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------|
| [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem)! | The newly added menu item. |

### add

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun add(
    groupId: Int, 
    itemId: Int, 
    order: Int, 
    title: CharSequence!
): MenuItem!
```

Add a new item to the menu. This item displays the given title for its label.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `groupId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The group identifier that this item should be part of. This can be used to define groups of items for batch state changes. Normally use [NONE](https://developer.android.com/reference/kotlin/android/view/Menu#NONE:kotlin.Int) if an item should not be in a group. |
| `itemId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Unique item ID. Use [NONE](https://developer.android.com/reference/kotlin/android/view/Menu#NONE:kotlin.Int) if you do not need a unique ID. |
| `order` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The order for the item. Use [NONE](https://developer.android.com/reference/kotlin/android/view/Menu#NONE:kotlin.Int) if you do not care about the order. See [MenuItem.getOrder()](https://developer.android.com/reference/kotlin/android/view/MenuItem#getOrder()). |
| `title` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:The text to display for the item. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------|
| [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem)! | The newly added menu item. |

### add

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun add(title: CharSequence!): MenuItem!
```

Add a new item to the menu. This item displays the given title for its label.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------|
| `title` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:The text to display for the item. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------|
| [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem)! | The newly added menu item. |

### addIntentOptions

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun addIntentOptions(
    groupId: Int, 
    itemId: Int, 
    order: Int, 
    caller: ComponentName!, 
    specifics: Array<Intent!>!, 
    intent: Intent!, 
    flags: Int, 
    outSpecificItems: Array<MenuItem!>!
): Int
```

Add a group of menu items corresponding to actions that can be performed for a particular Intent. The Intent is most often configured with a null action, the data that the current activity is working with, and includes either the [Intent.CATEGORY_ALTERNATIVE](https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_ALTERNATIVE:kotlin.String) or [Intent.CATEGORY_SELECTED_ALTERNATIVE](https://developer.android.com/reference/kotlin/android/content/Intent.html#CATEGORY_SELECTED_ALTERNATIVE:kotlin.String) to find activities that have said they would like to be included as optional action. You can, however, use any Intent you want.

See android.content.pm.PackageManager#queryIntentActivityOptions for more \* details on the caller, specifics, and intent arguments. The list returned by that function is used to populate the resulting menu items.

All of the menu items of possible options for the intent will be added with the given group and id. You can use the group to control ordering of the items in relation to other items in the menu. Normally this function will automatically remove any existing items in the menu in the same group and place a divider above and below the added items; this behavior can be modified with the flags parameter. For each of the generated items [MenuItem.setIntent](https://developer.android.com/reference/kotlin/android/view/MenuItem#setIntent(android.content.Intent))is called to associate the appropriate Intent with the item; this means the activity will automatically be started for you without having to do anything else.

| Parameters ||
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `groupId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The group identifier that the items should be part of. This can also be used to define groups of items for batch state changes. Normally use [NONE](https://developer.android.com/reference/kotlin/android/view/Menu#NONE:kotlin.Int) if the items should not be in a group. |
| `itemId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Unique item ID. Use [NONE](https://developer.android.com/reference/kotlin/android/view/Menu#NONE:kotlin.Int) if you do not need a unique ID. |
| `order` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The order for the items. Use [NONE](https://developer.android.com/reference/kotlin/android/view/Menu#NONE:kotlin.Int) if you do not care about the order. See [MenuItem.getOrder()](https://developer.android.com/reference/kotlin/android/view/MenuItem#getOrder()). |
| `caller` | [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#)!:The current activity component name as defined by queryIntentActivityOptions(). |
| `specifics` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!\>!:Specific items to place first as defined by queryIntentActivityOptions(). |
| `intent` | [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!:Intent describing the kinds of items to populate in the list as defined by queryIntentActivityOptions(). |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional options controlling how the items are added. |
| `outSpecificItems` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem)!\>!:Optional array in which to place the menu items that were generated for each of the specifics that were requested. Entries may be null if no activity was found for that specific action. |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The number of menu items that were added. |

**See Also**

- [#FLAG_APPEND_TO_GROUP](https://developer.android.com/reference/kotlin/android/view/Menu#FLAG_APPEND_TO_GROUP:kotlin.Int)
- [android.view.MenuItem#setIntent](https://developer.android.com/reference/kotlin/android/view/MenuItem#setIntent(android.content.Intent)) 

### addSubMenu

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun addSubMenu(titleRes: Int): SubMenu!
```

Add a new sub-menu to the menu. This item displays the given title for its label. To modify other attributes on the submenu's menu item, use [SubMenu.getItem()](https://developer.android.com/reference/kotlin/android/view/SubMenu#getItem()).

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------|
| `titleRes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Resource identifier of title string. |

| Return ||
|---------------------------------------------------------------------------------|--------------------------|
| [SubMenu](https://developer.android.com/reference/kotlin/android/view/SubMenu)! | The newly added sub-menu |

### addSubMenu

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun addSubMenu(
    groupId: Int, 
    itemId: Int, 
    order: Int, 
    titleRes: Int
): SubMenu!
```

Variation on [addSubMenu(int,int,int,java.lang.CharSequence)](https://developer.android.com/reference/kotlin/android/view/Menu#addSubMenu(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.CharSequence))that takes a string resource identifier for the title instead of the string itself.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `groupId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The group identifier that this item should be part of. This can also be used to define groups of items for batch state changes. Normally use [NONE](https://developer.android.com/reference/kotlin/android/view/Menu#NONE:kotlin.Int) if an item should not be in a group. |
| `itemId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Unique item ID. Use [NONE](https://developer.android.com/reference/kotlin/android/view/Menu#NONE:kotlin.Int) if you do not need a unique ID. |
| `order` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The order for the item. Use [NONE](https://developer.android.com/reference/kotlin/android/view/Menu#NONE:kotlin.Int) if you do not care about the order. See [MenuItem.getOrder()](https://developer.android.com/reference/kotlin/android/view/MenuItem#getOrder()). |
| `titleRes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Resource identifier of title string. |

| Return ||
|---------------------------------------------------------------------------------|--------------------------|
| [SubMenu](https://developer.android.com/reference/kotlin/android/view/SubMenu)! | The newly added sub-menu |

### addSubMenu

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun addSubMenu(
    groupId: Int, 
    itemId: Int, 
    order: Int, 
    title: CharSequence!
): SubMenu!
```

Add a new sub-menu to the menu. This item displays the given title for its label. To modify other attributes on the submenu's menu item, use [SubMenu.getItem()](https://developer.android.com/reference/kotlin/android/view/SubMenu#getItem()).

Note that you can only have one level of sub-menus, i.e. you cannnot add a subMenu to a subMenu: An [UnsupportedOperationException](https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#) will be thrown if you try.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `groupId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The group identifier that this item should be part of. This can also be used to define groups of items for batch state changes. Normally use [NONE](https://developer.android.com/reference/kotlin/android/view/Menu#NONE:kotlin.Int) if an item should not be in a group. |
| `itemId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Unique item ID. Use [NONE](https://developer.android.com/reference/kotlin/android/view/Menu#NONE:kotlin.Int) if you do not need a unique ID. |
| `order` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The order for the item. Use [NONE](https://developer.android.com/reference/kotlin/android/view/Menu#NONE:kotlin.Int) if you do not care about the order. See [MenuItem.getOrder()](https://developer.android.com/reference/kotlin/android/view/MenuItem#getOrder()). |
| `title` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:The text to display for the item. |

| Return ||
|---------------------------------------------------------------------------------|--------------------------|
| [SubMenu](https://developer.android.com/reference/kotlin/android/view/SubMenu)! | The newly added sub-menu |

### addSubMenu

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun addSubMenu(title: CharSequence!): SubMenu!
```

Add a new sub-menu to the menu. This item displays the given title for its label. To modify other attributes on the submenu's menu item, use [SubMenu.getItem()](https://developer.android.com/reference/kotlin/android/view/SubMenu#getItem()).

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------|
| `title` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:The text to display for the item. |

| Return ||
|---------------------------------------------------------------------------------|--------------------------|
| [SubMenu](https://developer.android.com/reference/kotlin/android/view/SubMenu)! | The newly added sub-menu |

### clear

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun clear(): Unit
```

Remove all existing items from the menu, leaving it empty as if it had just been created. 

### close

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun close(): Unit
```

Closes the menu, if open. 

### findItem

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun findItem(id: Int): MenuItem!
```

Return the menu item with a particular identifier.

| Parameters ||
|------|----------------------------------------------------------------------------------------------------|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The identifier to find. |

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem)! | The menu item object, or null if there is no item with this identifier. |

### getItem

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getItem(index: Int): MenuItem!
```

Gets the menu item at the given index.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index of the menu item to return. |

| Return ||
|-----------------------------------------------------------------------------------|----------------|
| [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem)! | The menu item. |

| Exceptions ||
|---------------------------------------|------------------------------|
| `java.lang.IndexOutOfBoundsException` | when`index < 0 || >= size()` |

### hasVisibleItems

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun hasVisibleItems(): Boolean
```

Return whether the menu currently has item items that are visible.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if there is one or more item visible, else false. |

### isShortcutKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isShortcutKey(
    keyCode: Int, 
    event: KeyEvent!
): Boolean
```

Is a keypress one of the defined shortcut keys for this window.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `keyCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the key code from [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent) to check. |
| `event` | [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent)!:the [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent) to use to help check. |

### performIdentifierAction

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun performIdentifierAction(
    id: Int, 
    flags: Int
): Boolean
```

Execute the menu item action associated with the given menu identifier.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Identifier associated with the menu item. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional option flags or 0. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | If the given identifier exists and is shown, returns true; else returns false. |

**See Also**

- [#FLAG_PERFORM_NO_CLOSE](https://developer.android.com/reference/kotlin/android/view/Menu#FLAG_PERFORM_NO_CLOSE:kotlin.Int) 

### performShortcut

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun performShortcut(
    keyCode: Int, 
    event: KeyEvent!, 
    flags: Int
): Boolean
```

Execute the menu item action associated with the given shortcut character.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------|
| `keyCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The keycode of the shortcut key. |
| `event` | [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent)!:Key event message. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional option flags or 0. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | If the given shortcut exists and is shown, returns true; else returns false. |

**See Also**

- [#FLAG_PERFORM_NO_CLOSE](https://developer.android.com/reference/kotlin/android/view/Menu#FLAG_PERFORM_NO_CLOSE:kotlin.Int) 

### removeGroup

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun removeGroup(groupId: Int): Unit
```

Remove all items in the given group.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `groupId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The group to be removed. If there are no items in this group, nothing happens. |

### removeItem

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun removeItem(id: Int): Unit
```

Remove the item with the given identifier.

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The item to be removed. If there is no item with this identifier, nothing happens. |

### setGroupCheckable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setGroupCheckable(
    group: Int, 
    checkable: Boolean, 
    exclusive: Boolean
): Unit
```

Control whether a particular group of items can show a check mark. This is similar to calling [MenuItem.setCheckable](https://developer.android.com/reference/kotlin/android/view/MenuItem#setCheckable(kotlin.Boolean))on all of the menu items with the given group identifier, but in addition you can control whether this group contains a mutually-exclusive set items. This should be called after the items of the group have been added to the menu.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `group` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The group of items to operate on. |
| `checkable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Set to true to allow a check mark, false to disallow. The default is false. |
| `exclusive` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):If set to true, only one item in this group can be checked at a time; checking an item will automatically uncheck all others in the group. If set to false, each item can be checked independently of the others. |

**See Also**

- [android.view.MenuItem#setCheckable](https://developer.android.com/reference/kotlin/android/view/MenuItem#setCheckable(kotlin.Boolean))
- [android.view.MenuItem#setChecked](https://developer.android.com/reference/kotlin/android/view/MenuItem#setChecked(kotlin.Boolean)) 

### setGroupDividerEnabled

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setGroupDividerEnabled(groupDividerEnabled: Boolean): Unit
```

Enable or disable the group dividers. 

### setGroupEnabled

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setGroupEnabled(
    group: Int, 
    enabled: Boolean
): Unit
```

Enable or disable all menu items that are in the given group.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `group` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The group of items to operate on. |
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):If true the items will be enabled, else they will be disabled. |

**See Also**

- [android.view.MenuItem#setEnabled](https://developer.android.com/reference/kotlin/android/view/MenuItem#setEnabled(kotlin.Boolean)) 

### setGroupVisible

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setGroupVisible(
    group: Int, 
    visible: Boolean
): Unit
```

Show or hide all menu items that are in the given group.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `group` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The group of items to operate on. |
| `visible` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):If true the items are visible, else they are hidden. |

**See Also**

- [android.view.MenuItem#setVisible](https://developer.android.com/reference/kotlin/android/view/MenuItem#setVisible(kotlin.Boolean)) 

### setQwertyMode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setQwertyMode(isQwerty: Boolean): Unit
```

Control whether the menu should be running in qwerty mode (alphabetic shortcuts) or 12-key mode (numeric shortcuts).

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `isQwerty` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):If true the menu will use alphabetic shortcuts; else it will use numeric shortcuts. |

### size

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun size(): Int
```

Get the number of items in the menu. Note that this will change any times items are added or removed from the menu.

| Return ||
|----------------------------------------------------------------------------|-----------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The item count. |
