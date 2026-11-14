# MenuItem

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MenuItem

Kotlin| [Java](https://developer.android.com/reference/android/view/MenuItem "View this page in Java") 

```
interface MenuItem
```

| [android.view.MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem#) |

Interface for direct access to a previously created menu item.

An Item is returned by calling one of the android.view.Menu#add methods.

For a feature set of specific menu types, see [Menu](https://developer.android.com/reference/kotlin/android/view/Menu).
|
| ### Developer Guides
|
| For information about creating menus, read the [Menus](https://developer.android.com/guide/topics/ui/menus.html) developer guide.

## Summary

| Nested classes ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [OnActionExpandListener](https://developer.android.com/reference/kotlin/android/view/MenuItem.OnActionExpandListener) Interface definition for a callback to be invoked when a menu item marked with [MenuItem.SHOW_AS_ACTION_COLLAPSE_ACTION_VIEW](https://developer.android.com/reference/kotlin/android/view/MenuItem#SHOW_AS_ACTION_COLLAPSE_ACTION_VIEW:kotlin.Int) is expanded or collapsed. |
| abstract | [OnMenuItemClickListener](https://developer.android.com/reference/kotlin/android/view/MenuItem.OnMenuItemClickListener) Interface definition for a callback to be invoked when a menu item is clicked. |

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SHOW_AS_ACTION_ALWAYS](https://developer.android.com/reference/kotlin/android/view/MenuItem#SHOW_AS_ACTION_ALWAYS:kotlin.Int) Always show this item as a button in an Action Bar. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SHOW_AS_ACTION_COLLAPSE_ACTION_VIEW](https://developer.android.com/reference/kotlin/android/view/MenuItem#SHOW_AS_ACTION_COLLAPSE_ACTION_VIEW:kotlin.Int) This item's action view collapses to a normal menu item. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SHOW_AS_ACTION_IF_ROOM](https://developer.android.com/reference/kotlin/android/view/MenuItem#SHOW_AS_ACTION_IF_ROOM:kotlin.Int) Show this item as a button in an Action Bar if the system decides there is room for it. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SHOW_AS_ACTION_NEVER](https://developer.android.com/reference/kotlin/android/view/MenuItem#SHOW_AS_ACTION_NEVER:kotlin.Int) Never show this item as a button in an Action Bar. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SHOW_AS_ACTION_WITH_TEXT](https://developer.android.com/reference/kotlin/android/view/MenuItem#SHOW_AS_ACTION_WITH_TEXT:kotlin.Int) When this item is in the action bar, always show it with a text label even if it also has an icon specified. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [collapseActionView](https://developer.android.com/reference/kotlin/android/view/MenuItem#collapseActionView())`()` Collapse the action view associated with this menu item. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [expandActionView](https://developer.android.com/reference/kotlin/android/view/MenuItem#expandActionView())`()` Expand the action view associated with this menu item. |
| abstract [ActionProvider](https://developer.android.com/reference/kotlin/android/view/ActionProvider)? | [getActionProvider](https://developer.android.com/reference/kotlin/android/view/MenuItem#getActionProvider())`()` Gets the [ActionProvider](https://developer.android.com/reference/kotlin/android/view/ActionProvider). |
| abstract [View](https://developer.android.com/reference/kotlin/android/view/View)? | [getActionView](https://developer.android.com/reference/kotlin/android/view/MenuItem#getActionView())`()` Returns the currently set action view for this menu item. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAlphabeticModifiers](https://developer.android.com/reference/kotlin/android/view/MenuItem#getAlphabeticModifiers())`()` Return the modifier for this menu item's alphabetic shortcut. |
| abstract [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [getAlphabeticShortcut](https://developer.android.com/reference/kotlin/android/view/MenuItem#getAlphabeticShortcut())`()` Return the char for this menu item's alphabetic shortcut. |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getContentDescription](https://developer.android.com/reference/kotlin/android/view/MenuItem#getContentDescription())`()` Retrieve the content description associated with this menu item. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGroupId](https://developer.android.com/reference/kotlin/android/view/MenuItem#getGroupId())`()` Return the group identifier that this menu item is part of. |
| abstract [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)? | [getIcon](https://developer.android.com/reference/kotlin/android/view/MenuItem#getIcon())`()` Returns the icon for this item as a Drawable (getting it from resources if it hasn't been loaded before). |
| open [BlendMode](https://developer.android.com/reference/kotlin/android/graphics/BlendMode.html#)? | [getIconTintBlendMode](https://developer.android.com/reference/kotlin/android/view/MenuItem#getIconTintBlendMode())`()` Returns the blending mode used to apply the tint to this item's icon, if specified. |
| open [ColorStateList](https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#)? | [getIconTintList](https://developer.android.com/reference/kotlin/android/view/MenuItem#getIconTintList())`()` <br /> |
| open [PorterDuff.Mode](https://developer.android.com/reference/kotlin/android/graphics/PorterDuff.Mode.html#)? | [getIconTintMode](https://developer.android.com/reference/kotlin/android/view/MenuItem#getIconTintMode())`()` Returns the blending mode used to apply the tint to this item's icon, if specified. |
| abstract [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)? | [getIntent](https://developer.android.com/reference/kotlin/android/view/MenuItem#getIntent())`()` Return the Intent associated with this item. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getItemId](https://developer.android.com/reference/kotlin/android/view/MenuItem#getItemId())`()` Return the identifier for this menu item. |
| abstract [ContextMenu.ContextMenuInfo](https://developer.android.com/reference/kotlin/android/view/ContextMenu.ContextMenuInfo)? | [getMenuInfo](https://developer.android.com/reference/kotlin/android/view/MenuItem#getMenuInfo())`()` Gets the extra information linked to this menu item. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getNumericModifiers](https://developer.android.com/reference/kotlin/android/view/MenuItem#getNumericModifiers())`()` Return the modifiers for this menu item's numeric (12-key) shortcut. |
| abstract [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [getNumericShortcut](https://developer.android.com/reference/kotlin/android/view/MenuItem#getNumericShortcut())`()` Return the char for this menu item's numeric (12-key) shortcut. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOrder](https://developer.android.com/reference/kotlin/android/view/MenuItem#getOrder())`()` Return the category and order within the category of this item. |
| abstract [SubMenu](https://developer.android.com/reference/kotlin/android/view/SubMenu)? | [getSubMenu](https://developer.android.com/reference/kotlin/android/view/MenuItem#getSubMenu())`()` Get the sub-menu to be invoked when this item is selected, if it has one. |
| abstract [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getTitle](https://developer.android.com/reference/kotlin/android/view/MenuItem#getTitle())`()` Retrieve the current title of the item. |
| abstract [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getTitleCondensed](https://developer.android.com/reference/kotlin/android/view/MenuItem#getTitleCondensed())`()` Retrieve the current condensed title of the item. |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getTooltipText](https://developer.android.com/reference/kotlin/android/view/MenuItem#getTooltipText())`()` Retrieve the tooltip text associated with this menu item. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasSubMenu](https://developer.android.com/reference/kotlin/android/view/MenuItem#hasSubMenu())`()` Check whether this item has an associated sub-menu. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isActionViewExpanded](https://developer.android.com/reference/kotlin/android/view/MenuItem#isActionViewExpanded())`()` Returns true if this menu item's action view has been expanded. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCheckable](https://developer.android.com/reference/kotlin/android/view/MenuItem#isCheckable())`()` Return whether the item can currently display a check mark. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isChecked](https://developer.android.com/reference/kotlin/android/view/MenuItem#isChecked())`()` Return whether the item is currently displaying a check mark. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEnabled](https://developer.android.com/reference/kotlin/android/view/MenuItem#isEnabled())`()` Return the enabled state of the menu item. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isVisible](https://developer.android.com/reference/kotlin/android/view/MenuItem#isVisible())`()` Return the visibility of the menu item. |
| abstract [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem#) | [setActionProvider](https://developer.android.com/reference/kotlin/android/view/MenuItem#setActionProvider(android.view.ActionProvider))`(`actionProvider:` ` [ActionProvider](https://developer.android.com/reference/kotlin/android/view/ActionProvider)?`)` Sets the [ActionProvider](https://developer.android.com/reference/kotlin/android/view/ActionProvider) responsible for creating an action view if the item is placed on the action bar. |
| abstract [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem#) | [setActionView](https://developer.android.com/reference/kotlin/android/view/MenuItem#setActionView(android.view.View))`(`view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View)?`)` Set an action view for this menu item. |
| abstract [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem#) | [setActionView](https://developer.android.com/reference/kotlin/android/view/MenuItem#setActionView(kotlin.Int))`(`resId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set an action view for this menu item. |
| abstract [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem#) | [setAlphabeticShortcut](https://developer.android.com/reference/kotlin/android/view/MenuItem#setAlphabeticShortcut(kotlin.Char))`(`alphaChar:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` Change the alphabetic shortcut associated with this item. |
| open [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem#) | [setAlphabeticShortcut](https://developer.android.com/reference/kotlin/android/view/MenuItem#setAlphabeticShortcut(kotlin.Char,%20kotlin.Int))`(`alphaChar:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`, `alphaModifiers:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Change the alphabetic shortcut associated with this item. |
| abstract [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem#) | [setCheckable](https://developer.android.com/reference/kotlin/android/view/MenuItem#setCheckable(kotlin.Boolean))`(`checkable:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Control whether this item can display a check mark. |
| abstract [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem#) | [setChecked](https://developer.android.com/reference/kotlin/android/view/MenuItem#setChecked(kotlin.Boolean))`(`checked:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Control whether this item is shown with a check mark. |
| open [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem#) | [setContentDescription](https://developer.android.com/reference/kotlin/android/view/MenuItem#setContentDescription(kotlin.CharSequence))`(`contentDescription:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?`)` Change the content description associated with this menu item. |
| abstract [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem#) | [setEnabled](https://developer.android.com/reference/kotlin/android/view/MenuItem#setEnabled(kotlin.Boolean))`(`enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether the menu item is enabled. |
| abstract [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem#) | [setIcon](https://developer.android.com/reference/kotlin/android/view/MenuItem#setIcon(android.graphics.drawable.Drawable))`(`icon:` ` [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)?`)` Change the icon associated with this item. |
| abstract [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem#) | [setIcon](https://developer.android.com/reference/kotlin/android/view/MenuItem#setIcon(kotlin.Int))`(`iconRes:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Change the icon associated with this item. |
| open [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem#) | [setIconTintBlendMode](https://developer.android.com/reference/kotlin/android/view/MenuItem#setIconTintBlendMode(android.graphics.BlendMode))`(`blendMode:` ` [BlendMode](https://developer.android.com/reference/kotlin/android/graphics/BlendMode.html#)?`)` Specifies the blending mode used to apply the tint specified by [setIconTintList(android.content.res.ColorStateList)](https://developer.android.com/reference/kotlin/android/view/MenuItem#setIconTintList(android.content.res.ColorStateList))to this item's icon. |
| open [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem#) | [setIconTintList](https://developer.android.com/reference/kotlin/android/view/MenuItem#setIconTintList(android.content.res.ColorStateList))`(`tint:` ` [ColorStateList](https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#)?`)` Applies a tint to this item's icon. |
| open [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem#) | [setIconTintMode](https://developer.android.com/reference/kotlin/android/view/MenuItem#setIconTintMode(android.graphics.PorterDuff.Mode))`(`tintMode:` ` [PorterDuff.Mode](https://developer.android.com/reference/kotlin/android/graphics/PorterDuff.Mode.html#)?`)` Specifies the blending mode used to apply the tint specified by [setIconTintList(android.content.res.ColorStateList)](https://developer.android.com/reference/kotlin/android/view/MenuItem#setIconTintList(android.content.res.ColorStateList))to this item's icon. |
| abstract [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem#) | [setIntent](https://developer.android.com/reference/kotlin/android/view/MenuItem#setIntent(android.content.Intent))`(`intent:` ` [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)?`)` Change the Intent associated with this item. |
| abstract [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem#) | [setNumericShortcut](https://developer.android.com/reference/kotlin/android/view/MenuItem#setNumericShortcut(kotlin.Char))`(`numericChar:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` Change the numeric shortcut associated with this item. |
| open [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem#) | [setNumericShortcut](https://developer.android.com/reference/kotlin/android/view/MenuItem#setNumericShortcut(kotlin.Char,%20kotlin.Int))`(`numericChar:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`, `numericModifiers:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Change the numeric shortcut and modifiers associated with this item. |
| abstract [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem#) | [setOnActionExpandListener](https://developer.android.com/reference/kotlin/android/view/MenuItem#setOnActionExpandListener(android.view.MenuItem.OnActionExpandListener))`(`listener:` ` [MenuItem.OnActionExpandListener](https://developer.android.com/reference/kotlin/android/view/MenuItem.OnActionExpandListener)?`)` Set an [OnActionExpandListener](https://developer.android.com/reference/kotlin/android/view/MenuItem.OnActionExpandListener) on this menu item to be notified when the associated action view is expanded or collapsed. |
| abstract [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem#) | [setOnMenuItemClickListener](https://developer.android.com/reference/kotlin/android/view/MenuItem#setOnMenuItemClickListener(android.view.MenuItem.OnMenuItemClickListener))`(`menuItemClickListener:` ` [MenuItem.OnMenuItemClickListener](https://developer.android.com/reference/kotlin/android/view/MenuItem.OnMenuItemClickListener)?`)` Set a custom listener for invocation of this menu item. |
| abstract [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem#) | [setShortcut](https://developer.android.com/reference/kotlin/android/view/MenuItem#setShortcut(kotlin.Char,%20kotlin.Char))`(`numericChar:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`, `alphaChar:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` Change both the numeric and alphabetic shortcut associated with this item. |
| open [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem#) | [setShortcut](https://developer.android.com/reference/kotlin/android/view/MenuItem#setShortcut(kotlin.Char,%20kotlin.Char,%20kotlin.Int,%20kotlin.Int))`(`numericChar:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`, `alphaChar:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`, `numericModifiers:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `alphaModifiers:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Change both the numeric and alphabetic shortcut associated with this item. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setShowAsAction](https://developer.android.com/reference/kotlin/android/view/MenuItem#setShowAsAction(kotlin.Int))`(`actionEnum:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets how this item should display in the presence of an Action Bar. |
| abstract [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem#) | [setShowAsActionFlags](https://developer.android.com/reference/kotlin/android/view/MenuItem#setShowAsActionFlags(kotlin.Int))`(`actionEnum:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets how this item should display in the presence of an Action Bar. |
| abstract [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem#) | [setTitle](https://developer.android.com/reference/kotlin/android/view/MenuItem#setTitle(kotlin.Int))`(`title:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Change the title associated with this item. |
| abstract [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem#) | [setTitle](https://developer.android.com/reference/kotlin/android/view/MenuItem#setTitle(kotlin.CharSequence))`(`title:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?`)` Change the title associated with this item. |
| abstract [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem#) | [setTitleCondensed](https://developer.android.com/reference/kotlin/android/view/MenuItem#setTitleCondensed(kotlin.CharSequence))`(`title:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?`)` Change the condensed title associated with this item. |
| open [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem#) | [setTooltipText](https://developer.android.com/reference/kotlin/android/view/MenuItem#setTooltipText(kotlin.CharSequence))`(`tooltipText:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?`)` Change the tooltip text associated with this menu item. |
| abstract [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem#) | [setVisible](https://developer.android.com/reference/kotlin/android/view/MenuItem#setVisible(kotlin.Boolean))`(`visible:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets the visibility of the menu item. |

## Constants

### SHOW_AS_ACTION_ALWAYS

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SHOW_AS_ACTION_ALWAYS: Int
```

Always show this item as a button in an Action Bar. Use sparingly! If too many items are set to always show in the Action Bar it can crowd the Action Bar and degrade the user experience on devices with smaller screens. A good rule of thumb is to have no more than 2 items set to always show at a time. 

 Value: 2

### SHOW_AS_ACTION_COLLAPSE_ACTION_VIEW

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SHOW_AS_ACTION_COLLAPSE_ACTION_VIEW: Int
```

This item's action view collapses to a normal menu item. When expanded, the action view temporarily takes over a larger segment of its container. 

 Value: 8

### SHOW_AS_ACTION_IF_ROOM

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SHOW_AS_ACTION_IF_ROOM: Int
```

Show this item as a button in an Action Bar if the system decides there is room for it. 

 Value: 1

### SHOW_AS_ACTION_NEVER

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SHOW_AS_ACTION_NEVER: Int
```

Never show this item as a button in an Action Bar. 

 Value: 0

### SHOW_AS_ACTION_WITH_TEXT

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SHOW_AS_ACTION_WITH_TEXT: Int
```

When this item is in the action bar, always show it with a text label even if it also has an icon specified. 

 Value: 4

## Public methods

### collapseActionView

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun collapseActionView(): Boolean
```

Collapse the action view associated with this menu item. The menu item must have an action view set, as well as the showAsAction flag [SHOW_AS_ACTION_COLLAPSE_ACTION_VIEW](https://developer.android.com/reference/kotlin/android/view/MenuItem#SHOW_AS_ACTION_COLLAPSE_ACTION_VIEW:kotlin.Int). If a listener has been set using [setOnActionExpandListener(android.view.MenuItem.OnActionExpandListener)](https://developer.android.com/reference/kotlin/android/view/MenuItem#setOnActionExpandListener(android.view.MenuItem.OnActionExpandListener))it will have its [OnActionExpandListener.onMenuItemActionCollapse(MenuItem)](https://developer.android.com/reference/kotlin/android/view/MenuItem.OnActionExpandListener#onMenuItemActionCollapse(android.view.MenuItem))method invoked. The listener may return false from this method to prevent collapsing the action view.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the action view was collapsed, false otherwise. |

### expandActionView

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun expandActionView(): Boolean
```

Expand the action view associated with this menu item. The menu item must have an action view set, as well as the showAsAction flag [SHOW_AS_ACTION_COLLAPSE_ACTION_VIEW](https://developer.android.com/reference/kotlin/android/view/MenuItem#SHOW_AS_ACTION_COLLAPSE_ACTION_VIEW:kotlin.Int). If a listener has been set using [setOnActionExpandListener(android.view.MenuItem.OnActionExpandListener)](https://developer.android.com/reference/kotlin/android/view/MenuItem#setOnActionExpandListener(android.view.MenuItem.OnActionExpandListener))it will have its [OnActionExpandListener.onMenuItemActionExpand(MenuItem)](https://developer.android.com/reference/kotlin/android/view/MenuItem.OnActionExpandListener#onMenuItemActionExpand(android.view.MenuItem))method invoked. The listener may return false from this method to prevent expanding the action view.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the action view was expanded, false otherwise. |

### getActionProvider

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getActionProvider(): ActionProvider?
```

Gets the [ActionProvider](https://developer.android.com/reference/kotlin/android/view/ActionProvider).

| Return ||
|-----------------------------------------------------------------------------------------------|-----------------------------------------------|
| [ActionProvider](https://developer.android.com/reference/kotlin/android/view/ActionProvider)? | The action provider. This value may be`null`. |

**See Also**

- [android.view.ActionProvider](https://developer.android.com/reference/kotlin/android/view/ActionProvider)
- [#setActionProvider(ActionProvider)](https://developer.android.com/reference/kotlin/android/view/MenuItem#setActionProvider(android.view.ActionProvider)) 

### getActionView

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getActionView(): View?
```

Returns the currently set action view for this menu item.

| Return ||
|---------------------------------------------------------------------------|--------------------------------------------------|
| [View](https://developer.android.com/reference/kotlin/android/view/View)? | This item's action view This value may be`null`. |

**See Also**

- [#setActionView(View)](https://developer.android.com/reference/kotlin/android/view/MenuItem#setActionView(android.view.View))
- [#setShowAsAction(int)](https://developer.android.com/reference/kotlin/android/view/MenuItem#setShowAsAction(kotlin.Int)) 

### getAlphabeticModifiers

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAlphabeticModifiers(): Int
```

Return the modifier for this menu item's alphabetic shortcut. The modifier is a combination of [KeyEvent.META_META_ON](https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_META_ON:kotlin.Int), [KeyEvent.META_CTRL_ON](https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_CTRL_ON:kotlin.Int), [KeyEvent.META_ALT_ON](https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_ALT_ON:kotlin.Int), [KeyEvent.META_SHIFT_ON](https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_SHIFT_ON:kotlin.Int), [KeyEvent.META_SYM_ON](https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_SYM_ON:kotlin.Int), [KeyEvent.META_FUNCTION_ON](https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_FUNCTION_ON:kotlin.Int). For example, [KeyEvent.META_FUNCTION_ON](https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_FUNCTION_ON:kotlin.Int)| [KeyEvent.META_CTRL_ON](https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_CTRL_ON:kotlin.Int)

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Modifier associated with the keyboard shortcut. |

### getAlphabeticShortcut

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getAlphabeticShortcut(): Char
```

Return the char for this menu item's alphabetic shortcut.

| Return ||
|------------------------------------------------------------------------------|--------------------------------------------|
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | Alphabetic character to use as a shortcut. |

### getContentDescription

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getContentDescription(): CharSequence?
```

Retrieve the content description associated with this menu item.

| Return ||
|------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | The content description. This value may be`null`. |

### getGroupId

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getGroupId(): Int
```

Return the group identifier that this menu item is part of. The group identifier can not be changed after the menu is created.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The menu item's group identifier. |

### getIcon

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getIcon(): Drawable?
```

Returns the icon for this item as a Drawable (getting it from resources if it hasn't been loaded before). Note that if you call [setIconTintList(android.content.res.ColorStateList)](https://developer.android.com/reference/kotlin/android/view/MenuItem#setIconTintList(android.content.res.ColorStateList))or [setIconTintMode(android.graphics.PorterDuff.Mode)](https://developer.android.com/reference/kotlin/android/view/MenuItem#setIconTintMode(android.graphics.PorterDuff.Mode))on this item, and you use a custom menu presenter in your application, you have to apply the tinting explicitly on the [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#) returned by this method.

| Return ||
|------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)? | The icon as a Drawable. This value may be`null`. |

### getIconTintBlendMode

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getIconTintBlendMode(): BlendMode?
```

Returns the blending mode used to apply the tint to this item's icon, if specified.

| Return ||
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [BlendMode](https://developer.android.com/reference/kotlin/android/graphics/BlendMode.html#)? | the blending mode used to apply the tint to this item's icon This value may be`null`. |

**See Also**

- [#setIconTintBlendMode(BlendMode)](https://developer.android.com/reference/kotlin/android/view/MenuItem#setIconTintBlendMode(android.graphics.BlendMode)) 

### getIconTintList

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getIconTintList(): ColorStateList?
```

| Return ||
|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [ColorStateList](https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#)? | the tint applied to this item's icon This value may be`null`. |

**See Also**

- [#setIconTintList(ColorStateList)](https://developer.android.com/reference/kotlin/android/view/MenuItem#setIconTintList(android.content.res.ColorStateList)) 

### getIconTintMode

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getIconTintMode(): PorterDuff.Mode?
```

Returns the blending mode used to apply the tint to this item's icon, if specified.

| Return ||
|-----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [PorterDuff.Mode](https://developer.android.com/reference/kotlin/android/graphics/PorterDuff.Mode.html#)? | the blending mode used to apply the tint to this item's icon This value may be`null`. |

**See Also**

- [#setIconTintMode(PorterDuff.Mode)](https://developer.android.com/reference/kotlin/android/view/MenuItem#setIconTintMode(android.graphics.PorterDuff.Mode))
- [#setIconTintBlendMode(BlendMode)](https://developer.android.com/reference/kotlin/android/view/MenuItem#setIconTintBlendMode(android.graphics.BlendMode)) 

### getIntent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getIntent(): Intent?
```

Return the Intent associated with this item. This returns a reference to the Intent which you can change as desired to modify what the Item is holding.

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)? | Returns the last value supplied to [setIntent](https://developer.android.com/reference/kotlin/android/view/MenuItem#setIntent(android.content.Intent)), or null. |

**See Also**

- [#setIntent](https://developer.android.com/reference/kotlin/android/view/MenuItem#setIntent(android.content.Intent)) 

### getItemId

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getItemId(): Int
```

Return the identifier for this menu item. The identifier can not be changed after the menu is created.

| Return ||
|----------------------------------------------------------------------------|-----------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The menu item's identifier. |

### getMenuInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getMenuInfo(): ContextMenu.ContextMenuInfo?
```

Gets the extra information linked to this menu item. This extra information is set by the View that added this menu item to the menu.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [ContextMenu.ContextMenuInfo](https://developer.android.com/reference/kotlin/android/view/ContextMenu.ContextMenuInfo)? | The extra information linked to the View that added this menu item to the menu. This can be null. |

**See Also**

- [android.view.View.OnCreateContextMenuListener](https://developer.android.com/reference/kotlin/android/view/View.OnCreateContextMenuListener) 

### getNumericModifiers

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getNumericModifiers(): Int
```

Return the modifiers for this menu item's numeric (12-key) shortcut. The modifier is a combination of [KeyEvent.META_META_ON](https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_META_ON:kotlin.Int), [KeyEvent.META_CTRL_ON](https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_CTRL_ON:kotlin.Int), [KeyEvent.META_ALT_ON](https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_ALT_ON:kotlin.Int), [KeyEvent.META_SHIFT_ON](https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_SHIFT_ON:kotlin.Int), [KeyEvent.META_SYM_ON](https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_SYM_ON:kotlin.Int), [KeyEvent.META_FUNCTION_ON](https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_FUNCTION_ON:kotlin.Int). For example, [KeyEvent.META_FUNCTION_ON](https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_FUNCTION_ON:kotlin.Int)| [KeyEvent.META_CTRL_ON](https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_CTRL_ON:kotlin.Int)

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Modifier associated with the numeric shortcut. |

### getNumericShortcut

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getNumericShortcut(): Char
```

Return the char for this menu item's numeric (12-key) shortcut.

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------|
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | Numeric character to use as a shortcut. |

### getOrder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getOrder(): Int
```

Return the category and order within the category of this item. This item will be shown before all items (within its category) that have order greater than this value.

An order integer contains the item's category (the upper bits of the integer; set by or/add the category with the order within the category) and the ordering of the item within that category (the lower bits). Example categories are [Menu.CATEGORY_SYSTEM](https://developer.android.com/reference/kotlin/android/view/Menu#CATEGORY_SYSTEM:kotlin.Int), [Menu.CATEGORY_SECONDARY](https://developer.android.com/reference/kotlin/android/view/Menu#CATEGORY_SECONDARY:kotlin.Int), [Menu.CATEGORY_ALTERNATIVE](https://developer.android.com/reference/kotlin/android/view/Menu#CATEGORY_ALTERNATIVE:kotlin.Int), [Menu.CATEGORY_CONTAINER](https://developer.android.com/reference/kotlin/android/view/Menu#CATEGORY_CONTAINER:kotlin.Int). See [Menu](https://developer.android.com/reference/kotlin/android/view/Menu) for a full list.

| Return ||
|----------------------------------------------------------------------------|-------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The order of this item. |

### getSubMenu

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getSubMenu(): SubMenu?
```

Get the sub-menu to be invoked when this item is selected, if it has one. See [hasSubMenu()](https://developer.android.com/reference/kotlin/android/view/MenuItem#hasSubMenu()).

| Return ||
|---------------------------------------------------------------------------------|------------------------------------------------|
| [SubMenu](https://developer.android.com/reference/kotlin/android/view/SubMenu)? | The associated menu if there is one, else null |

### getTitle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getTitle(): CharSequence?
```

Retrieve the current title of the item.

| Return ||
|------------------------------------------------------------------------------------------------|-------------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | The title. This value may be`null`. |

### getTitleCondensed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getTitleCondensed(): CharSequence?
```

Retrieve the current condensed title of the item. If a condensed title was never set, it will return the normal title.

| Return ||
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | The condensed title, if it exists. Otherwise the normal title. This value may be`null`. |

### getTooltipText

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTooltipText(): CharSequence?
```

Retrieve the tooltip text associated with this menu item.

| Return ||
|------------------------------------------------------------------------------------------------|--------------------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | The tooltip text. This value may be`null`. |

### hasSubMenu

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun hasSubMenu(): Boolean
```

Check whether this item has an associated sub-menu. I.e. it is a sub-menu of another menu.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | If true this item has a menu; else it is a normal item. |

### isActionViewExpanded

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isActionViewExpanded(): Boolean
```

Returns true if this menu item's action view has been expanded.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the item's action view is expanded, false otherwise. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/view/MenuItem#expandActionView()>
- <https://developer.android.com/reference/kotlin/android/view/MenuItem#collapseActionView()>
- [#SHOW_AS_ACTION_COLLAPSE_ACTION_VIEW](https://developer.android.com/reference/kotlin/android/view/MenuItem#SHOW_AS_ACTION_COLLAPSE_ACTION_VIEW:kotlin.Int)
- [android.view.MenuItem.OnActionExpandListener](https://developer.android.com/reference/kotlin/android/view/MenuItem.OnActionExpandListener) 

### isCheckable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isCheckable(): Boolean
```

Return whether the item can currently display a check mark.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | If a check mark can be displayed, returns true. |

**See Also**

- [#setCheckable](https://developer.android.com/reference/kotlin/android/view/MenuItem#setCheckable(kotlin.Boolean)) 

### isChecked

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isChecked(): Boolean
```

Return whether the item is currently displaying a check mark.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | If a check mark is displayed, returns true. |

**See Also**

- [#setChecked](https://developer.android.com/reference/kotlin/android/view/MenuItem#setChecked(kotlin.Boolean)) 

### isEnabled

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isEnabled(): Boolean
```

Return the enabled state of the menu item.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | If true the item is enabled and hence invokable; else it is not. |

### isVisible

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isVisible(): Boolean
```

Return the visibility of the menu item.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | If true the item is visible; else it is hidden. |

### setActionProvider

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setActionProvider(actionProvider: ActionProvider?): MenuItem
```

Sets the [ActionProvider](https://developer.android.com/reference/kotlin/android/view/ActionProvider) responsible for creating an action view if the item is placed on the action bar. The provider also provides a default action invoked if the item is placed in the overflow menu.

**Note:** Setting an action provider overrides the action view set via [setActionView(int)](https://developer.android.com/reference/kotlin/android/view/MenuItem#setActionView(kotlin.Int))or [setActionView(android.view.View)](https://developer.android.com/reference/kotlin/android/view/MenuItem#setActionView(android.view.View)).

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `actionProvider` | [ActionProvider](https://developer.android.com/reference/kotlin/android/view/ActionProvider)?:The action provider. This value may be`null`. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem#) | This Item so additional setters can be called. This value cannot be`null`. |

**See Also**

- [android.view.ActionProvider](https://developer.android.com/reference/kotlin/android/view/ActionProvider) 

### setActionView

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setActionView(view: View?): MenuItem
```

Set an action view for this menu item. An action view will be displayed in place of an automatically generated menu item element in the UI when this item is shown as an action within a parent.

**Note:** Setting an action view overrides the action provider set via [setActionProvider(android.view.ActionProvider)](https://developer.android.com/reference/kotlin/android/view/MenuItem#setActionProvider(android.view.ActionProvider)).

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [View](https://developer.android.com/reference/kotlin/android/view/View)?:View to use for presenting this item to the user. This value may be`null`. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem#) | This Item so additional setters can be called. This value cannot be`null`. |

**See Also**

- [#setShowAsAction(int)](https://developer.android.com/reference/kotlin/android/view/MenuItem#setShowAsAction(kotlin.Int)) 

### setActionView

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setActionView(resId: Int): MenuItem
```

Set an action view for this menu item. An action view will be displayed in place of an automatically generated menu item element in the UI when this item is shown as an action within a parent.

**Note:** Setting an action view overrides the action provider set via [setActionProvider(android.view.ActionProvider)](https://developer.android.com/reference/kotlin/android/view/MenuItem#setActionProvider(android.view.ActionProvider)).

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `resId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Layout resource to use for presenting this item to the user. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem#) | This Item so additional setters can be called. This value cannot be`null`. |

**See Also**

- [#setShowAsAction(int)](https://developer.android.com/reference/kotlin/android/view/MenuItem#setShowAsAction(kotlin.Int)) 

### setAlphabeticShortcut

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setAlphabeticShortcut(alphaChar: Char): MenuItem
```

Change the alphabetic shortcut associated with this item. The shortcut will be triggered when the key that generates the given character is pressed along with the corresponding modifier key. The default modifier is [KeyEvent.META_CTRL_ON](https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_CTRL_ON:kotlin.Int) in case nothing is specified. Case is not significant and shortcut characters will be displayed in lower case. Note that menu items with the characters '\\b' or '\\n' as shortcuts will get triggered by the Delete key or Carriage Return key, respectively.

See [Menu](https://developer.android.com/reference/kotlin/android/view/Menu) for the menu types that support shortcuts.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `alphaChar` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):The alphabetic shortcut key. This is the shortcut when using a keyboard with alphabetic keys. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem#) | This Item so additional setters can be called. This value cannot be`null`. |

### setAlphabeticShortcut

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setAlphabeticShortcut(
    alphaChar: Char, 
    alphaModifiers: Int
): MenuItem
```

Change the alphabetic shortcut associated with this item. The shortcut will be triggered when the key that generates the given character is pressed along with the modifier keys. Case is not significant and shortcut characters will be displayed in lower case. Note that menu items with the characters '\\b' or '\\n' as shortcuts will get triggered by the Delete key or Carriage Return key, respectively.

See [Menu](https://developer.android.com/reference/kotlin/android/view/Menu) for the menu types that support shortcuts.

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `alphaChar` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):The alphabetic shortcut key. This is the shortcut when using a keyboard with alphabetic keys. |
| `alphaModifiers` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The modifier associated with the shortcut. It should be a combination of [KeyEvent.META_META_ON](https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_META_ON:kotlin.Int), [KeyEvent.META_CTRL_ON](https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_CTRL_ON:kotlin.Int), [KeyEvent.META_ALT_ON](https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_ALT_ON:kotlin.Int), [KeyEvent.META_SHIFT_ON](https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_SHIFT_ON:kotlin.Int), [KeyEvent.META_SYM_ON](https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_SYM_ON:kotlin.Int), [KeyEvent.META_FUNCTION_ON](https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_FUNCTION_ON:kotlin.Int). |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem#) | This Item so additional setters can be called. This value cannot be`null`. |

### setCheckable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setCheckable(checkable: Boolean): MenuItem
```

Control whether this item can display a check mark. Setting this does not actually display a check mark (see [setChecked](https://developer.android.com/reference/kotlin/android/view/MenuItem#setChecked(kotlin.Boolean))for that); rather, it ensures there is room in the item in which to display a check mark.

See [Menu](https://developer.android.com/reference/kotlin/android/view/Menu) for the menu types that support check marks.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `checkable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Set to true to allow a check mark, false to disallow. The default is false. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem#) | This Item so additional setters can be called. This value cannot be`null`. |

**See Also**

- [#setChecked](https://developer.android.com/reference/kotlin/android/view/MenuItem#setChecked(kotlin.Boolean))
- [#isCheckable](https://developer.android.com/reference/kotlin/android/view/MenuItem#isCheckable())
- [android.view.Menu#setGroupCheckable](https://developer.android.com/reference/kotlin/android/view/Menu#setGroupCheckable(kotlin.Int,%20kotlin.Boolean,%20kotlin.Boolean)) 

### setChecked

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setChecked(checked: Boolean): MenuItem
```

Control whether this item is shown with a check mark. Note that you must first have enabled checking with [setCheckable](https://developer.android.com/reference/kotlin/android/view/MenuItem#setCheckable(kotlin.Boolean))or else the check mark will not appear. If this item is a member of a group that contains mutually-exclusive items (set via [Menu.setGroupCheckable(int, boolean, boolean)](https://developer.android.com/reference/kotlin/android/view/Menu#setGroupCheckable(kotlin.Int,%20kotlin.Boolean,%20kotlin.Boolean)), the other items in the group will be unchecked.

See [Menu](https://developer.android.com/reference/kotlin/android/view/Menu) for the menu types that support check marks.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `checked` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Set to true to display a check mark, false to hide it. The default value is false. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem#) | This Item so additional setters can be called. This value cannot be`null`. |

**See Also**

- [#setCheckable](https://developer.android.com/reference/kotlin/android/view/MenuItem#setCheckable(kotlin.Boolean))
- [#isChecked](https://developer.android.com/reference/kotlin/android/view/MenuItem#isChecked())
- [android.view.Menu#setGroupCheckable](https://developer.android.com/reference/kotlin/android/view/Menu#setGroupCheckable(kotlin.Int,%20kotlin.Boolean,%20kotlin.Boolean)) 

### setContentDescription

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setContentDescription(contentDescription: CharSequence?): MenuItem
```

Change the content description associated with this menu item.

| Parameters ||
|----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `contentDescription` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?:The new content description. This value may be`null`. |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------|
| [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem#) | This value cannot be`null`. |

### setEnabled

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setEnabled(enabled: Boolean): MenuItem
```

Sets whether the menu item is enabled. Disabling a menu item will not allow it to be invoked via its shortcut. The menu item will still be visible.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):If true then the item will be invokable; if false it is won't be invokable. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem#) | This Item so additional setters can be called. This value cannot be`null`. |

### setIcon

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setIcon(icon: Drawable?): MenuItem
```

Change the icon associated with this item. This icon will not always be shown, so the title should be sufficient in describing this item. See [Menu](https://developer.android.com/reference/kotlin/android/view/Menu) for the menu types that support icons.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `icon` | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)?:The new icon (as a Drawable) to be displayed. This value may be`null`. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem#) | This Item so additional setters can be called. This value cannot be`null`. |

### setIcon

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setIcon(iconRes: Int): MenuItem
```

Change the icon associated with this item. This icon will not always be shown, so the title should be sufficient in describing this item. See [Menu](https://developer.android.com/reference/kotlin/android/view/Menu) for the menu types that support icons.

This method will set the resource ID of the icon which will be used to lazily get the Drawable when this item is being shown.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------|
| `iconRes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The new icon (as a resource ID) to be displayed. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem#) | This Item so additional setters can be called. This value cannot be`null`. |

### setIconTintBlendMode

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setIconTintBlendMode(blendMode: BlendMode?): MenuItem
```

Specifies the blending mode used to apply the tint specified by [setIconTintList(android.content.res.ColorStateList)](https://developer.android.com/reference/kotlin/android/view/MenuItem#setIconTintList(android.content.res.ColorStateList))to this item's icon. The default mode is [BlendMode.SRC_IN](https://developer.android.com/reference/kotlin/android/graphics/BlendMode.html#).

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `blendMode` | [BlendMode](https://developer.android.com/reference/kotlin/android/graphics/BlendMode.html#)?:the blending mode used to apply the tint, may be`null`to clear tint |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------|
| [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem#) | This value cannot be`null`. |

**See Also**

- [#setIconTintList(ColorStateList)](https://developer.android.com/reference/kotlin/android/view/MenuItem#setIconTintList(android.content.res.ColorStateList)) 

### setIconTintList

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setIconTintList(tint: ColorStateList?): MenuItem
```

Applies a tint to this item's icon. Does not modify the current tint mode, which is [PorterDuff.Mode.SRC_IN](https://developer.android.com/reference/kotlin/android/graphics/PorterDuff.Mode.html#) by default.

Subsequent calls to [setIcon(android.graphics.drawable.Drawable)](https://developer.android.com/reference/kotlin/android/view/MenuItem#setIcon(android.graphics.drawable.Drawable))or [setIcon(int)](https://developer.android.com/reference/kotlin/android/view/MenuItem#setIcon(kotlin.Int))will automatically mutate the icon and apply the specified tint and tint mode using [Drawable.setTintList(ColorStateList)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#setTintList(android.content.res.ColorStateList)).

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tint` | [ColorStateList](https://developer.android.com/reference/kotlin/android/content/res/ColorStateList.html#)?:the tint to apply, may be`null`to clear tint |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------|
| [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem#) | This value cannot be`null`. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/view/MenuItem#getIconTintList()>
- [android.graphics.drawable.Drawable#setTintList(ColorStateList)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#setTintList(android.content.res.ColorStateList)) 

### setIconTintMode

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setIconTintMode(tintMode: PorterDuff.Mode?): MenuItem
```

Specifies the blending mode used to apply the tint specified by [setIconTintList(android.content.res.ColorStateList)](https://developer.android.com/reference/kotlin/android/view/MenuItem#setIconTintList(android.content.res.ColorStateList))to this item's icon. The default mode is [PorterDuff.Mode.SRC_IN](https://developer.android.com/reference/kotlin/android/graphics/PorterDuff.Mode.html#).

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tintMode` | [PorterDuff.Mode](https://developer.android.com/reference/kotlin/android/graphics/PorterDuff.Mode.html#)?:the blending mode used to apply the tint, may be`null`to clear tint |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------|
| [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem#) | This value cannot be`null`. |

**See Also**

- [#setIconTintList(ColorStateList)](https://developer.android.com/reference/kotlin/android/view/MenuItem#setIconTintList(android.content.res.ColorStateList))
- [android.graphics.drawable.Drawable#setTintMode(PorterDuff.Mode)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#setTintMode(android.graphics.PorterDuff.Mode))
- [android.graphics.drawable.Drawable#setTintBlendMode(BlendMode)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#setTintBlendMode(android.graphics.BlendMode)) 

### setIntent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setIntent(intent: Intent?): MenuItem
```

Change the Intent associated with this item. By default there is no Intent associated with a menu item. If you set one, and nothing else handles the item, then the default behavior will be to call android.content.Context#startActivity with the given Intent.

Note that setIntent() can not be used with the versions of android.view.Menu#add that take a Runnable, because [Runnable.run](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#run())does not return a value so there is no way to tell if it handled the item. In this case it is assumed that the Runnable always handles the item, and the intent will never be started.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `intent` | [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)?:The Intent to associated with the item. This Intent object is*not* copied, so be careful not to modify it later. This value may be`null`. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem#) | This Item so additional setters can be called. This value cannot be`null`. |

**See Also**

- [#getIntent](https://developer.android.com/reference/kotlin/android/view/MenuItem#getIntent()) 

### setNumericShortcut

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setNumericShortcut(numericChar: Char): MenuItem
```

Change the numeric shortcut associated with this item.

See [Menu](https://developer.android.com/reference/kotlin/android/view/Menu) for the menu types that support shortcuts.

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `numericChar` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):The numeric shortcut key. This is the shortcut when using a 12-key (numeric) keyboard. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem#) | This Item so additional setters can be called. This value cannot be`null`. |

### setNumericShortcut

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setNumericShortcut(
    numericChar: Char, 
    numericModifiers: Int
): MenuItem
```

Change the numeric shortcut and modifiers associated with this item.

See [Menu](https://developer.android.com/reference/kotlin/android/view/Menu) for the menu types that support shortcuts.

| Parameters ||
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `numericChar` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):The numeric shortcut key. This is the shortcut when using a 12-key (numeric) keyboard. |
| `numericModifiers` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The modifier associated with the shortcut. It should be a combination of [KeyEvent.META_META_ON](https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_META_ON:kotlin.Int), [KeyEvent.META_CTRL_ON](https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_CTRL_ON:kotlin.Int), [KeyEvent.META_ALT_ON](https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_ALT_ON:kotlin.Int), [KeyEvent.META_SHIFT_ON](https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_SHIFT_ON:kotlin.Int), [KeyEvent.META_SYM_ON](https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_SYM_ON:kotlin.Int), [KeyEvent.META_FUNCTION_ON](https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_FUNCTION_ON:kotlin.Int). |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem#) | This Item so additional setters can be called. This value cannot be`null`. |

### setOnActionExpandListener

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setOnActionExpandListener(listener: MenuItem.OnActionExpandListener?): MenuItem
```

Set an [OnActionExpandListener](https://developer.android.com/reference/kotlin/android/view/MenuItem.OnActionExpandListener) on this menu item to be notified when the associated action view is expanded or collapsed. The menu item must be configured to expand or collapse its action view using the flag [SHOW_AS_ACTION_COLLAPSE_ACTION_VIEW](https://developer.android.com/reference/kotlin/android/view/MenuItem#SHOW_AS_ACTION_COLLAPSE_ACTION_VIEW:kotlin.Int).

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [MenuItem.OnActionExpandListener](https://developer.android.com/reference/kotlin/android/view/MenuItem.OnActionExpandListener)?:Listener that will respond to expand/collapse events This value may be`null`. |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem#) | This menu item instance for call chaining This value cannot be`null`. |

### setOnMenuItemClickListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setOnMenuItemClickListener(menuItemClickListener: MenuItem.OnMenuItemClickListener?): MenuItem
```

Set a custom listener for invocation of this menu item. In most situations, it is more efficient and easier to use [Activity.onOptionsItemSelected(MenuItem)](https://developer.android.com/reference/kotlin/android/app/Activity.html#onOptionsItemSelected(android.view.MenuItem))or [Activity.onContextItemSelected(MenuItem)](https://developer.android.com/reference/kotlin/android/app/Activity.html#onContextItemSelected(android.view.MenuItem)).

| Parameters ||
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `menuItemClickListener` | [MenuItem.OnMenuItemClickListener](https://developer.android.com/reference/kotlin/android/view/MenuItem.OnMenuItemClickListener)?:The object to receive invokations. This value may be`null`. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem#) | This Item so additional setters can be called. This value cannot be`null`. |

**See Also**

- [android.app.Activity#onOptionsItemSelected(MenuItem)](https://developer.android.com/reference/kotlin/android/app/Activity.html#onOptionsItemSelected(android.view.MenuItem))
- [android.app.Activity#onContextItemSelected(MenuItem)](https://developer.android.com/reference/kotlin/android/app/Activity.html#onContextItemSelected(android.view.MenuItem)) 

### setShortcut

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setShortcut(
    numericChar: Char, 
    alphaChar: Char
): MenuItem
```

Change both the numeric and alphabetic shortcut associated with this item. Note that the shortcut will be triggered when the key that generates the given character is pressed along with the corresponding modifier key. The default modifier is [KeyEvent.META_CTRL_ON](https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_CTRL_ON:kotlin.Int) in case nothing is specified. Also note that case is not significant and that alphabetic shortcut characters will be handled in lower case.

See [Menu](https://developer.android.com/reference/kotlin/android/view/Menu) for the menu types that support shortcuts.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `numericChar` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):The numeric shortcut key. This is the shortcut when using a numeric (e.g., 12-key) keyboard. |
| `alphaChar` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):The alphabetic shortcut key. This is the shortcut when using a keyboard with alphabetic keys. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem#) | This Item so additional setters can be called. This value cannot be`null`. |

### setShortcut

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setShortcut(
    numericChar: Char, 
    alphaChar: Char, 
    numericModifiers: Int, 
    alphaModifiers: Int
): MenuItem
```

Change both the numeric and alphabetic shortcut associated with this item. Note that the shortcut will be triggered when the key that generates the given character is pressed along with the corresponding modifier key. Also note that case is not significant and that alphabetic shortcut characters will be handled in lower case.

See [Menu](https://developer.android.com/reference/kotlin/android/view/Menu) for the menu types that support shortcuts.

| Parameters ||
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `numericChar` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):The numeric shortcut key. This is the shortcut when using a numeric (e.g., 12-key) keyboard. |
| `numericModifiers` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The numeric modifier associated with the shortcut. It should be a combination of [KeyEvent.META_META_ON](https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_META_ON:kotlin.Int), [KeyEvent.META_CTRL_ON](https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_CTRL_ON:kotlin.Int), [KeyEvent.META_ALT_ON](https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_ALT_ON:kotlin.Int), [KeyEvent.META_SHIFT_ON](https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_SHIFT_ON:kotlin.Int), [KeyEvent.META_SYM_ON](https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_SYM_ON:kotlin.Int), [KeyEvent.META_FUNCTION_ON](https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_FUNCTION_ON:kotlin.Int). |
| `alphaChar` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):The alphabetic shortcut key. This is the shortcut when using a keyboard with alphabetic keys. |
| `alphaModifiers` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The alphabetic modifier associated with the shortcut. It should be a combination of [KeyEvent.META_META_ON](https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_META_ON:kotlin.Int), [KeyEvent.META_CTRL_ON](https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_CTRL_ON:kotlin.Int), [KeyEvent.META_ALT_ON](https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_ALT_ON:kotlin.Int), [KeyEvent.META_SHIFT_ON](https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_SHIFT_ON:kotlin.Int), [KeyEvent.META_SYM_ON](https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_SYM_ON:kotlin.Int), [KeyEvent.META_FUNCTION_ON](https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_FUNCTION_ON:kotlin.Int). |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem#) | This Item so additional setters can be called. This value cannot be`null`. |

### setShowAsAction

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setShowAsAction(actionEnum: Int): Unit
```

Sets how this item should display in the presence of an Action Bar. The parameter actionEnum is a flag set. One of [SHOW_AS_ACTION_ALWAYS](https://developer.android.com/reference/kotlin/android/view/MenuItem#SHOW_AS_ACTION_ALWAYS:kotlin.Int), [SHOW_AS_ACTION_IF_ROOM](https://developer.android.com/reference/kotlin/android/view/MenuItem#SHOW_AS_ACTION_IF_ROOM:kotlin.Int), or [SHOW_AS_ACTION_NEVER](https://developer.android.com/reference/kotlin/android/view/MenuItem#SHOW_AS_ACTION_NEVER:kotlin.Int) should be used, and you may optionally OR the value with [SHOW_AS_ACTION_WITH_TEXT](https://developer.android.com/reference/kotlin/android/view/MenuItem#SHOW_AS_ACTION_WITH_TEXT:kotlin.Int). SHOW_AS_ACTION_WITH_TEXT requests that when the item is shown as an action, it should be shown with a text label.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `actionEnum` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):How the item should display. One of [SHOW_AS_ACTION_ALWAYS](https://developer.android.com/reference/kotlin/android/view/MenuItem#SHOW_AS_ACTION_ALWAYS:kotlin.Int), [SHOW_AS_ACTION_IF_ROOM](https://developer.android.com/reference/kotlin/android/view/MenuItem#SHOW_AS_ACTION_IF_ROOM:kotlin.Int), or [SHOW_AS_ACTION_NEVER](https://developer.android.com/reference/kotlin/android/view/MenuItem#SHOW_AS_ACTION_NEVER:kotlin.Int). SHOW_AS_ACTION_NEVER is the default. |

**See Also**

- [android.app.ActionBar](https://developer.android.com/reference/kotlin/android/app/ActionBar.html#)
- [#setActionView(View)](https://developer.android.com/reference/kotlin/android/view/MenuItem#setActionView(android.view.View)) 

### setShowAsActionFlags

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setShowAsActionFlags(actionEnum: Int): MenuItem
```

Sets how this item should display in the presence of an Action Bar. The parameter actionEnum is a flag set. One of [SHOW_AS_ACTION_ALWAYS](https://developer.android.com/reference/kotlin/android/view/MenuItem#SHOW_AS_ACTION_ALWAYS:kotlin.Int), [SHOW_AS_ACTION_IF_ROOM](https://developer.android.com/reference/kotlin/android/view/MenuItem#SHOW_AS_ACTION_IF_ROOM:kotlin.Int), or [SHOW_AS_ACTION_NEVER](https://developer.android.com/reference/kotlin/android/view/MenuItem#SHOW_AS_ACTION_NEVER:kotlin.Int) should be used, and you may optionally OR the value with [SHOW_AS_ACTION_WITH_TEXT](https://developer.android.com/reference/kotlin/android/view/MenuItem#SHOW_AS_ACTION_WITH_TEXT:kotlin.Int). SHOW_AS_ACTION_WITH_TEXT requests that when the item is shown as an action, it should be shown with a text label.

Note: This method differs from [setShowAsAction(int)](https://developer.android.com/reference/kotlin/android/view/MenuItem#setShowAsAction(kotlin.Int))only in that it returns the current MenuItem instance for call chaining.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `actionEnum` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):How the item should display. One of [SHOW_AS_ACTION_ALWAYS](https://developer.android.com/reference/kotlin/android/view/MenuItem#SHOW_AS_ACTION_ALWAYS:kotlin.Int), [SHOW_AS_ACTION_IF_ROOM](https://developer.android.com/reference/kotlin/android/view/MenuItem#SHOW_AS_ACTION_IF_ROOM:kotlin.Int), or [SHOW_AS_ACTION_NEVER](https://developer.android.com/reference/kotlin/android/view/MenuItem#SHOW_AS_ACTION_NEVER:kotlin.Int). SHOW_AS_ACTION_NEVER is the default. |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem#) | This MenuItem instance for call chaining. This value cannot be`null`. |

**See Also**

- [android.app.ActionBar](https://developer.android.com/reference/kotlin/android/app/ActionBar.html#)
- [#setActionView(View)](https://developer.android.com/reference/kotlin/android/view/MenuItem#setActionView(android.view.View)) 

### setTitle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setTitle(title: Int): MenuItem
```

Change the title associated with this item.

Some menu types do not sufficient space to show the full title, and instead a condensed title is preferred. See [Menu](https://developer.android.com/reference/kotlin/android/view/Menu) for more information.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------|
| `title` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The resource id of the new text to be displayed. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem#) | This Item so additional setters can be called. This value cannot be`null`. |

**See Also**

- [#setTitleCondensed(CharSequence)](https://developer.android.com/reference/kotlin/android/view/MenuItem#setTitleCondensed(kotlin.CharSequence)) 

### setTitle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setTitle(title: CharSequence?): MenuItem
```

Change the title associated with this item.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| `title` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?:The new text to be displayed. This value may be`null`. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem#) | This Item so additional setters can be called. This value cannot be`null`. |

### setTitleCondensed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setTitleCondensed(title: CharSequence?): MenuItem
```

Change the condensed title associated with this item. The condensed title is used in situations where the normal title may be too long to be displayed.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `title` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?:The new text to be displayed as the condensed title. This value may be`null`. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem#) | This Item so additional setters can be called. This value cannot be`null`. |

### setTooltipText

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTooltipText(tooltipText: CharSequence?): MenuItem
```

Change the tooltip text associated with this menu item.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `tooltipText` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?:The new tooltip text. This value may be`null`. |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------|
| [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem#) | This value cannot be`null`. |

### setVisible

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setVisible(visible: Boolean): MenuItem
```

Sets the visibility of the menu item. Even if a menu item is not visible, it may still be invoked via its shortcut (to completely disable an item, set it to invisible and [disabled](https://developer.android.com/reference/kotlin/android/view/MenuItem#setEnabled(kotlin.Boolean))).

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `visible` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):If true then the item will be visible; if false it is hidden. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem#) | This Item so additional setters can be called. This value cannot be`null`. |
