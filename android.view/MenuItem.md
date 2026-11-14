# MenuItem

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MenuItem

Kotlin| [Java](MenuItem.md) 
| --- | --- |

```
interface MenuItem
```

| [android.view.MenuItem](MenuItem.md) |

Interface for direct access to a previously created menu item.

An Item is returned by calling one of the android.view.Menu#add methods.

For a feature set of specific menu types, see [Menu](Menu.md).
|
| ### Developer Guides
|
| For information about creating menus, read the [Menus](https://developer.android.com/guide/topics/ui/menus.html) developer guide.

## Summary

| Nested classes ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [OnActionExpandListener](../android/view/MenuItem.OnActionExpandListener.md) Interface definition for a callback to be invoked when a menu item marked with [MenuItem.SHOW_AS_ACTION_COLLAPSE_ACTION_VIEW](MenuItem.md) is expanded or collapsed. |
| abstract | [OnMenuItemClickListener](../android/view/MenuItem.OnMenuItemClickListener.md) Interface definition for a callback to be invoked when a menu item is clicked. |

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SHOW_AS_ACTION_ALWAYS](MenuItem.md) Always show this item as a button in an Action Bar. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SHOW_AS_ACTION_COLLAPSE_ACTION_VIEW](MenuItem.md) This item's action view collapses to a normal menu item. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SHOW_AS_ACTION_IF_ROOM](MenuItem.md) Show this item as a button in an Action Bar if the system decides there is room for it. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SHOW_AS_ACTION_NEVER](MenuItem.md) Never show this item as a button in an Action Bar. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SHOW_AS_ACTION_WITH_TEXT](MenuItem.md) When this item is in the action bar, always show it with a text label even if it also has an icon specified. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [collapseActionView](MenuItem.md))`()` Collapse the action view associated with this menu item. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [expandActionView](MenuItem.md))`()` Expand the action view associated with this menu item. |
| abstract [ActionProvider](ActionProvider.md)? | [getActionProvider](MenuItem.md))`()` Gets the [ActionProvider](ActionProvider.md). |
| --- | --- |
| abstract [View](View.md)? | [getActionView](MenuItem.md))`()` Returns the currently set action view for this menu item. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAlphabeticModifiers](MenuItem.md))`()` Return the modifier for this menu item's alphabetic shortcut. |
| abstract [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [getAlphabeticShortcut](MenuItem.md))`()` Return the char for this menu item's alphabetic shortcut. |
| --- | --- |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getContentDescription](MenuItem.md))`()` Retrieve the content description associated with this menu item. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGroupId](MenuItem.md))`()` Return the group identifier that this menu item is part of. |
| abstract [Drawable](../android.graphics.drawable/Drawable.md)? | [getIcon](MenuItem.md))`()` Returns the icon for this item as a Drawable (getting it from resources if it hasn't been loaded before). |
| --- | --- |
| open [BlendMode](../android.graphics/BlendMode.md)? | [getIconTintBlendMode](MenuItem.md))`()` Returns the blending mode used to apply the tint to this item's icon, if specified. |
| open [ColorStateList](../android.content.res/ColorStateList.md)? | [getIconTintList](MenuItem.md))`()` <br /> |
| open [PorterDuff.Mode](../android/graphics/PorterDuff.Mode.md)? | [getIconTintMode](MenuItem.md))`()` Returns the blending mode used to apply the tint to this item's icon, if specified. |
| --- | --- |
| abstract [Intent](../android.content/Intent.md)? | [getIntent](MenuItem.md))`()` Return the Intent associated with this item. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getItemId](MenuItem.md))`()` Return the identifier for this menu item. |
| abstract [ContextMenu.ContextMenuInfo](../android/view/ContextMenu.ContextMenuInfo.md)? | [getMenuInfo](MenuItem.md))`()` Gets the extra information linked to this menu item. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getNumericModifiers](MenuItem.md))`()` Return the modifiers for this menu item's numeric (12-key) shortcut. |
| abstract [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [getNumericShortcut](MenuItem.md))`()` Return the char for this menu item's numeric (12-key) shortcut. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOrder](MenuItem.md))`()` Return the category and order within the category of this item. |
| --- | --- |
| abstract [SubMenu](SubMenu.md)? | [getSubMenu](MenuItem.md))`()` Get the sub-menu to be invoked when this item is selected, if it has one. |
| abstract [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getTitle](MenuItem.md))`()` Retrieve the current title of the item. |
| abstract [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getTitleCondensed](MenuItem.md))`()` Retrieve the current condensed title of the item. |
| --- | --- |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getTooltipText](MenuItem.md))`()` Retrieve the tooltip text associated with this menu item. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasSubMenu](MenuItem.md))`()` Check whether this item has an associated sub-menu. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isActionViewExpanded](MenuItem.md))`()` Returns true if this menu item's action view has been expanded. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCheckable](MenuItem.md))`()` Return whether the item can currently display a check mark. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isChecked](MenuItem.md))`()` Return whether the item is currently displaying a check mark. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEnabled](MenuItem.md))`()` Return the enabled state of the menu item. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isVisible](MenuItem.md))`()` Return the visibility of the menu item. |
| abstract [MenuItem](MenuItem.md) | [setActionProvider](MenuItem.md))`(`actionProvider:` ` [ActionProvider](ActionProvider.md)?`)` Sets the [ActionProvider](ActionProvider.md) responsible for creating an action view if the item is placed on the action bar. |
| abstract [MenuItem](MenuItem.md) | [setActionView](MenuItem.md))`(`view:` ` [View](View.md)?`)` Set an action view for this menu item. |
| --- | --- |
| abstract [MenuItem](MenuItem.md) | [setActionView](MenuItem.md))`(`resId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set an action view for this menu item. |
| abstract [MenuItem](MenuItem.md) | [setAlphabeticShortcut](MenuItem.md))`(`alphaChar:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` Change the alphabetic shortcut associated with this item. |
| open [MenuItem](MenuItem.md) | [setAlphabeticShortcut](MenuItem.md))`(`alphaChar:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`, `alphaModifiers:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Change the alphabetic shortcut associated with this item. |
| --- | --- |
| abstract [MenuItem](MenuItem.md) | [setCheckable](MenuItem.md))`(`checkable:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Control whether this item can display a check mark. |
| abstract [MenuItem](MenuItem.md) | [setChecked](MenuItem.md))`(`checked:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Control whether this item is shown with a check mark. |
| open [MenuItem](MenuItem.md) | [setContentDescription](MenuItem.md))`(`contentDescription:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?`)` Change the content description associated with this menu item. |
| --- | --- |
| abstract [MenuItem](MenuItem.md) | [setEnabled](MenuItem.md))`(`enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether the menu item is enabled. |
| abstract [MenuItem](MenuItem.md) | [setIcon](MenuItem.md))`(`icon:` ` [Drawable](../android.graphics.drawable/Drawable.md)?`)` Change the icon associated with this item. |
| abstract [MenuItem](MenuItem.md) | [setIcon](MenuItem.md))`(`iconRes:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Change the icon associated with this item. |
| --- | --- |
| open [MenuItem](MenuItem.md) | [setIconTintBlendMode](MenuItem.md))`(`blendMode:` ` [BlendMode](../android.graphics/BlendMode.md)?`)` Specifies the blending mode used to apply the tint specified by [setIconTintList(android.content.res.ColorStateList)](MenuItem.md))to this item's icon. |
| open [MenuItem](MenuItem.md) | [setIconTintList](MenuItem.md))`(`tint:` ` [ColorStateList](../android.content.res/ColorStateList.md)?`)` Applies a tint to this item's icon. |
| open [MenuItem](MenuItem.md) | [setIconTintMode](MenuItem.md))`(`tintMode:` ` [PorterDuff.Mode](../android/graphics/PorterDuff.Mode.md)?`)` Specifies the blending mode used to apply the tint specified by [setIconTintList(android.content.res.ColorStateList)](MenuItem.md))to this item's icon. |
| --- | --- |
| abstract [MenuItem](MenuItem.md) | [setIntent](MenuItem.md))`(`intent:` ` [Intent](../android.content/Intent.md)?`)` Change the Intent associated with this item. |
| abstract [MenuItem](MenuItem.md) | [setNumericShortcut](MenuItem.md))`(`numericChar:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` Change the numeric shortcut associated with this item. |
| open [MenuItem](MenuItem.md) | [setNumericShortcut](MenuItem.md))`(`numericChar:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`, `numericModifiers:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Change the numeric shortcut and modifiers associated with this item. |
| --- | --- |
| abstract [MenuItem](MenuItem.md) | [setOnActionExpandListener](MenuItem.md))`(`listener:` ` [MenuItem.OnActionExpandListener](../android/view/MenuItem.OnActionExpandListener.md)?`)` Set an [OnActionExpandListener](../android/view/MenuItem.OnActionExpandListener.md) on this menu item to be notified when the associated action view is expanded or collapsed. |
| abstract [MenuItem](MenuItem.md) | [setOnMenuItemClickListener](MenuItem.md))`(`menuItemClickListener:` ` [MenuItem.OnMenuItemClickListener](../android/view/MenuItem.OnMenuItemClickListener.md)?`)` Set a custom listener for invocation of this menu item. |
| abstract [MenuItem](MenuItem.md) | [setShortcut](MenuItem.md))`(`numericChar:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`, `alphaChar:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` Change both the numeric and alphabetic shortcut associated with this item. |
| --- | --- |
| open [MenuItem](MenuItem.md) | [setShortcut](MenuItem.md))`(`numericChar:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`, `alphaChar:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`, `numericModifiers:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `alphaModifiers:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Change both the numeric and alphabetic shortcut associated with this item. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setShowAsAction](MenuItem.md))`(`actionEnum:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets how this item should display in the presence of an Action Bar. |
| abstract [MenuItem](MenuItem.md) | [setShowAsActionFlags](MenuItem.md))`(`actionEnum:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets how this item should display in the presence of an Action Bar. |
| --- | --- |
| abstract [MenuItem](MenuItem.md) | [setTitle](MenuItem.md))`(`title:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Change the title associated with this item. |
| abstract [MenuItem](MenuItem.md) | [setTitle](MenuItem.md))`(`title:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?`)` Change the title associated with this item. |
| abstract [MenuItem](MenuItem.md) | [setTitleCondensed](MenuItem.md))`(`title:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?`)` Change the condensed title associated with this item. |
| --- | --- |
| open [MenuItem](MenuItem.md) | [setTooltipText](MenuItem.md))`(`tooltipText:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?`)` Change the tooltip text associated with this menu item. |
| abstract [MenuItem](MenuItem.md) | [setVisible](MenuItem.md))`(`visible:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets the visibility of the menu item. |

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

Collapse the action view associated with this menu item. The menu item must have an action view set, as well as the showAsAction flag [SHOW_AS_ACTION_COLLAPSE_ACTION_VIEW](MenuItem.md). If a listener has been set using [setOnActionExpandListener(android.view.MenuItem.OnActionExpandListener)](MenuItem.md))it will have its [OnActionExpandListener.onMenuItemActionCollapse(MenuItem)](../android/view/MenuItem.OnActionExpandListener.md))method invoked. The listener may return false from this method to prevent collapsing the action view.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the action view was collapsed, false otherwise. |

### expandActionView

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun expandActionView(): Boolean
```

Expand the action view associated with this menu item. The menu item must have an action view set, as well as the showAsAction flag [SHOW_AS_ACTION_COLLAPSE_ACTION_VIEW](MenuItem.md). If a listener has been set using [setOnActionExpandListener(android.view.MenuItem.OnActionExpandListener)](MenuItem.md))it will have its [OnActionExpandListener.onMenuItemActionExpand(MenuItem)](../android/view/MenuItem.OnActionExpandListener.md))method invoked. The listener may return false from this method to prevent expanding the action view.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the action view was expanded, false otherwise. |

### getActionProvider

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getActionProvider(): ActionProvider?
```

Gets the [ActionProvider](ActionProvider.md).

| Return ||
|-----------------------------------------------------------------------------------------------|-----------------------------------------------|
| [ActionProvider](ActionProvider.md)? | The action provider. This value may be`null`. |

**See Also**

- [android.view.ActionProvider](ActionProvider.md)
- [#setActionProvider(ActionProvider)](MenuItem.md)) 

### getActionView

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getActionView(): View?
```

Returns the currently set action view for this menu item.

| Return ||
|---------------------------------------------------------------------------|--------------------------------------------------|
| [View](View.md)? | This item's action view This value may be`null`. |

**See Also**

- [#setActionView(View)](MenuItem.md))
- [#setShowAsAction(int)](MenuItem.md)) 

### getAlphabeticModifiers

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAlphabeticModifiers(): Int
```

Return the modifier for this menu item's alphabetic shortcut. The modifier is a combination of [KeyEvent.META_META_ON](KeyEvent.md), [KeyEvent.META_CTRL_ON](KeyEvent.md), [KeyEvent.META_ALT_ON](KeyEvent.md), [KeyEvent.META_SHIFT_ON](KeyEvent.md), [KeyEvent.META_SYM_ON](KeyEvent.md), [KeyEvent.META_FUNCTION_ON](KeyEvent.md). For example, [KeyEvent.META_FUNCTION_ON](KeyEvent.md)| [KeyEvent.META_CTRL_ON](KeyEvent.md)
| --- | --- |

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

Returns the icon for this item as a Drawable (getting it from resources if it hasn't been loaded before). Note that if you call [setIconTintList(android.content.res.ColorStateList)](MenuItem.md))or [setIconTintMode(android.graphics.PorterDuff.Mode)](MenuItem.md))on this item, and you use a custom menu presenter in your application, you have to apply the tinting explicitly on the [Drawable](../android.graphics.drawable/Drawable.md) returned by this method.

| Return ||
|------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| [Drawable](../android.graphics.drawable/Drawable.md)? | The icon as a Drawable. This value may be`null`. |

### getIconTintBlendMode

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getIconTintBlendMode(): BlendMode?
```

Returns the blending mode used to apply the tint to this item's icon, if specified.

| Return ||
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [BlendMode](../android.graphics/BlendMode.md)? | the blending mode used to apply the tint to this item's icon This value may be`null`. |

**See Also**

- [#setIconTintBlendMode(BlendMode)](MenuItem.md)) 

### getIconTintList

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getIconTintList(): ColorStateList?
```

| Return ||
|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [ColorStateList](../android.content.res/ColorStateList.md)? | the tint applied to this item's icon This value may be`null`. |

**See Also**

- [#setIconTintList(ColorStateList)](MenuItem.md)) 

### getIconTintMode

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getIconTintMode(): PorterDuff.Mode?
```

Returns the blending mode used to apply the tint to this item's icon, if specified.

| Return ||
|-----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [PorterDuff.Mode](../android/graphics/PorterDuff.Mode.md)? | the blending mode used to apply the tint to this item's icon This value may be`null`. |

**See Also**

- [#setIconTintMode(PorterDuff.Mode)](MenuItem.md))
- [#setIconTintBlendMode(BlendMode)](MenuItem.md)) 

### getIntent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getIntent(): Intent?
```

Return the Intent associated with this item. This returns a reference to the Intent which you can change as desired to modify what the Item is holding.

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Intent](../android.content/Intent.md)? | Returns the last value supplied to [setIntent](MenuItem.md)), or null. |

**See Also**

- [#setIntent](MenuItem.md)) 

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
| [ContextMenu.ContextMenuInfo](../android/view/ContextMenu.ContextMenuInfo.md)? | The extra information linked to the View that added this menu item to the menu. This can be null. |

**See Also**

- [android.view.View.OnCreateContextMenuListener](../android/view/View.OnCreateContextMenuListener.md) 

### getNumericModifiers

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getNumericModifiers(): Int
```

Return the modifiers for this menu item's numeric (12-key) shortcut. The modifier is a combination of [KeyEvent.META_META_ON](KeyEvent.md), [KeyEvent.META_CTRL_ON](KeyEvent.md), [KeyEvent.META_ALT_ON](KeyEvent.md), [KeyEvent.META_SHIFT_ON](KeyEvent.md), [KeyEvent.META_SYM_ON](KeyEvent.md), [KeyEvent.META_FUNCTION_ON](KeyEvent.md). For example, [KeyEvent.META_FUNCTION_ON](KeyEvent.md)| [KeyEvent.META_CTRL_ON](KeyEvent.md)
| --- | --- |

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

An order integer contains the item's category (the upper bits of the integer; set by or/add the category with the order within the category) and the ordering of the item within that category (the lower bits). Example categories are [Menu.CATEGORY_SYSTEM](Menu.md), [Menu.CATEGORY_SECONDARY](Menu.md), [Menu.CATEGORY_ALTERNATIVE](Menu.md), [Menu.CATEGORY_CONTAINER](Menu.md). See [Menu](Menu.md) for a full list.

| Return ||
|----------------------------------------------------------------------------|-------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The order of this item. |

### getSubMenu

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getSubMenu(): SubMenu?
```

Get the sub-menu to be invoked when this item is selected, if it has one. See [hasSubMenu()](MenuItem.md)).

| Return ||
|---------------------------------------------------------------------------------|------------------------------------------------|
| [SubMenu](SubMenu.md)? | The associated menu if there is one, else null |

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
- [#SHOW_AS_ACTION_COLLAPSE_ACTION_VIEW](MenuItem.md)
- [android.view.MenuItem.OnActionExpandListener](../android/view/MenuItem.OnActionExpandListener.md) 

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

- [#setCheckable](MenuItem.md)) 

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

- [#setChecked](MenuItem.md)) 

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

Sets the [ActionProvider](ActionProvider.md) responsible for creating an action view if the item is placed on the action bar. The provider also provides a default action invoked if the item is placed in the overflow menu.

**Note:** Setting an action provider overrides the action view set via [setActionView(int)](MenuItem.md))or [setActionView(android.view.View)](MenuItem.md)).

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `actionProvider` | [ActionProvider](ActionProvider.md)?:The action provider. This value may be`null`. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MenuItem](MenuItem.md) | This Item so additional setters can be called. This value cannot be`null`. |

**See Also**

- [android.view.ActionProvider](ActionProvider.md) 

### setActionView

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setActionView(view: View?): MenuItem
```

Set an action view for this menu item. An action view will be displayed in place of an automatically generated menu item element in the UI when this item is shown as an action within a parent.

**Note:** Setting an action view overrides the action provider set via [setActionProvider(android.view.ActionProvider)](MenuItem.md)).

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [View](View.md)?:View to use for presenting this item to the user. This value may be`null`. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MenuItem](MenuItem.md) | This Item so additional setters can be called. This value cannot be`null`. |

**See Also**

- [#setShowAsAction(int)](MenuItem.md)) 

### setActionView

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setActionView(resId: Int): MenuItem
```

Set an action view for this menu item. An action view will be displayed in place of an automatically generated menu item element in the UI when this item is shown as an action within a parent.

**Note:** Setting an action view overrides the action provider set via [setActionProvider(android.view.ActionProvider)](MenuItem.md)).

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `resId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Layout resource to use for presenting this item to the user. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MenuItem](MenuItem.md) | This Item so additional setters can be called. This value cannot be`null`. |

**See Also**

- [#setShowAsAction(int)](MenuItem.md)) 

### setAlphabeticShortcut

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setAlphabeticShortcut(alphaChar: Char): MenuItem
```

Change the alphabetic shortcut associated with this item. The shortcut will be triggered when the key that generates the given character is pressed along with the corresponding modifier key. The default modifier is [KeyEvent.META_CTRL_ON](KeyEvent.md) in case nothing is specified. Case is not significant and shortcut characters will be displayed in lower case. Note that menu items with the characters '\\b' or '\\n' as shortcuts will get triggered by the Delete key or Carriage Return key, respectively.

See [Menu](Menu.md) for the menu types that support shortcuts.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `alphaChar` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):The alphabetic shortcut key. This is the shortcut when using a keyboard with alphabetic keys. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MenuItem](MenuItem.md) | This Item so additional setters can be called. This value cannot be`null`. |

### setAlphabeticShortcut

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setAlphabeticShortcut(
    alphaChar: Char, 
    alphaModifiers: Int
): MenuItem
```

Change the alphabetic shortcut associated with this item. The shortcut will be triggered when the key that generates the given character is pressed along with the modifier keys. Case is not significant and shortcut characters will be displayed in lower case. Note that menu items with the characters '\\b' or '\\n' as shortcuts will get triggered by the Delete key or Carriage Return key, respectively.

See [Menu](Menu.md) for the menu types that support shortcuts.

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `alphaChar` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):The alphabetic shortcut key. This is the shortcut when using a keyboard with alphabetic keys. |
| `alphaModifiers` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The modifier associated with the shortcut. It should be a combination of [KeyEvent.META_META_ON](KeyEvent.md), [KeyEvent.META_CTRL_ON](KeyEvent.md), [KeyEvent.META_ALT_ON](KeyEvent.md), [KeyEvent.META_SHIFT_ON](KeyEvent.md), [KeyEvent.META_SYM_ON](KeyEvent.md), [KeyEvent.META_FUNCTION_ON](KeyEvent.md). |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MenuItem](MenuItem.md) | This Item so additional setters can be called. This value cannot be`null`. |

### setCheckable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setCheckable(checkable: Boolean): MenuItem
```

Control whether this item can display a check mark. Setting this does not actually display a check mark (see [setChecked](MenuItem.md))for that); rather, it ensures there is room in the item in which to display a check mark.

See [Menu](Menu.md) for the menu types that support check marks.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `checkable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Set to true to allow a check mark, false to disallow. The default is false. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MenuItem](MenuItem.md) | This Item so additional setters can be called. This value cannot be`null`. |

**See Also**

- [#setChecked](MenuItem.md))
- [#isCheckable](MenuItem.md))
- [android.view.Menu#setGroupCheckable](Menu.md)) 

### setChecked

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setChecked(checked: Boolean): MenuItem
```

Control whether this item is shown with a check mark. Note that you must first have enabled checking with [setCheckable](MenuItem.md))or else the check mark will not appear. If this item is a member of a group that contains mutually-exclusive items (set via [Menu.setGroupCheckable(int, boolean, boolean)](Menu.md)), the other items in the group will be unchecked.

See [Menu](Menu.md) for the menu types that support check marks.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `checked` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Set to true to display a check mark, false to hide it. The default value is false. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MenuItem](MenuItem.md) | This Item so additional setters can be called. This value cannot be`null`. |

**See Also**

- [#setCheckable](MenuItem.md))
- [#isChecked](MenuItem.md))
- [android.view.Menu#setGroupCheckable](Menu.md)) 

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
| [MenuItem](MenuItem.md) | This value cannot be`null`. |

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
| [MenuItem](MenuItem.md) | This Item so additional setters can be called. This value cannot be`null`. |

### setIcon

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setIcon(icon: Drawable?): MenuItem
```

Change the icon associated with this item. This icon will not always be shown, so the title should be sufficient in describing this item. See [Menu](Menu.md) for the menu types that support icons.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `icon` | [Drawable](../android.graphics.drawable/Drawable.md)?:The new icon (as a Drawable) to be displayed. This value may be`null`. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MenuItem](MenuItem.md) | This Item so additional setters can be called. This value cannot be`null`. |

### setIcon

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setIcon(iconRes: Int): MenuItem
```

Change the icon associated with this item. This icon will not always be shown, so the title should be sufficient in describing this item. See [Menu](Menu.md) for the menu types that support icons.

This method will set the resource ID of the icon which will be used to lazily get the Drawable when this item is being shown.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------|
| `iconRes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The new icon (as a resource ID) to be displayed. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MenuItem](MenuItem.md) | This Item so additional setters can be called. This value cannot be`null`. |

### setIconTintBlendMode

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setIconTintBlendMode(blendMode: BlendMode?): MenuItem
```

Specifies the blending mode used to apply the tint specified by [setIconTintList(android.content.res.ColorStateList)](MenuItem.md))to this item's icon. The default mode is [BlendMode.SRC_IN](../android.graphics/BlendMode.md).

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `blendMode` | [BlendMode](../android.graphics/BlendMode.md)?:the blending mode used to apply the tint, may be`null`to clear tint |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------|
| [MenuItem](MenuItem.md) | This value cannot be`null`. |

**See Also**

- [#setIconTintList(ColorStateList)](MenuItem.md)) 

### setIconTintList

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setIconTintList(tint: ColorStateList?): MenuItem
```

Applies a tint to this item's icon. Does not modify the current tint mode, which is [PorterDuff.Mode.SRC_IN](../android/graphics/PorterDuff.Mode.md) by default.

Subsequent calls to [setIcon(android.graphics.drawable.Drawable)](MenuItem.md))or [setIcon(int)](MenuItem.md))will automatically mutate the icon and apply the specified tint and tint mode using [Drawable.setTintList(ColorStateList)](../android.graphics.drawable/Drawable.md)).

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tint` | [ColorStateList](../android.content.res/ColorStateList.md)?:the tint to apply, may be`null`to clear tint |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------|
| [MenuItem](MenuItem.md) | This value cannot be`null`. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/view/MenuItem#getIconTintList()>
- [android.graphics.drawable.Drawable#setTintList(ColorStateList)](../android.graphics.drawable/Drawable.md)) 

### setIconTintMode

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setIconTintMode(tintMode: PorterDuff.Mode?): MenuItem
```

Specifies the blending mode used to apply the tint specified by [setIconTintList(android.content.res.ColorStateList)](MenuItem.md))to this item's icon. The default mode is [PorterDuff.Mode.SRC_IN](../android/graphics/PorterDuff.Mode.md).

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tintMode` | [PorterDuff.Mode](../android/graphics/PorterDuff.Mode.md)?:the blending mode used to apply the tint, may be`null`to clear tint |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------|
| [MenuItem](MenuItem.md) | This value cannot be`null`. |

**See Also**

- [#setIconTintList(ColorStateList)](MenuItem.md))
- [android.graphics.drawable.Drawable#setTintMode(PorterDuff.Mode)](../android.graphics.drawable/Drawable.md))
- [android.graphics.drawable.Drawable#setTintBlendMode(BlendMode)](../android.graphics.drawable/Drawable.md)) 

### setIntent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setIntent(intent: Intent?): MenuItem
```

Change the Intent associated with this item. By default there is no Intent associated with a menu item. If you set one, and nothing else handles the item, then the default behavior will be to call android.content.Context#startActivity with the given Intent.

Note that setIntent() can not be used with the versions of android.view.Menu#add that take a Runnable, because [Runnable.run](../java.lang/Runnable.md))does not return a value so there is no way to tell if it handled the item. In this case it is assumed that the Runnable always handles the item, and the intent will never be started.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `intent` | [Intent](../android.content/Intent.md)?:The Intent to associated with the item. This Intent object is*not* copied, so be careful not to modify it later. This value may be`null`. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MenuItem](MenuItem.md) | This Item so additional setters can be called. This value cannot be`null`. |

**See Also**

- [#getIntent](MenuItem.md)) 

### setNumericShortcut

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setNumericShortcut(numericChar: Char): MenuItem
```

Change the numeric shortcut associated with this item.

See [Menu](Menu.md) for the menu types that support shortcuts.

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `numericChar` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):The numeric shortcut key. This is the shortcut when using a 12-key (numeric) keyboard. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MenuItem](MenuItem.md) | This Item so additional setters can be called. This value cannot be`null`. |

### setNumericShortcut

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setNumericShortcut(
    numericChar: Char, 
    numericModifiers: Int
): MenuItem
```

Change the numeric shortcut and modifiers associated with this item.

See [Menu](Menu.md) for the menu types that support shortcuts.

| Parameters ||
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `numericChar` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):The numeric shortcut key. This is the shortcut when using a 12-key (numeric) keyboard. |
| `numericModifiers` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The modifier associated with the shortcut. It should be a combination of [KeyEvent.META_META_ON](KeyEvent.md), [KeyEvent.META_CTRL_ON](KeyEvent.md), [KeyEvent.META_ALT_ON](KeyEvent.md), [KeyEvent.META_SHIFT_ON](KeyEvent.md), [KeyEvent.META_SYM_ON](KeyEvent.md), [KeyEvent.META_FUNCTION_ON](KeyEvent.md). |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MenuItem](MenuItem.md) | This Item so additional setters can be called. This value cannot be`null`. |

### setOnActionExpandListener

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setOnActionExpandListener(listener: MenuItem.OnActionExpandListener?): MenuItem
```

Set an [OnActionExpandListener](../android/view/MenuItem.OnActionExpandListener.md) on this menu item to be notified when the associated action view is expanded or collapsed. The menu item must be configured to expand or collapse its action view using the flag [SHOW_AS_ACTION_COLLAPSE_ACTION_VIEW](MenuItem.md).

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [MenuItem.OnActionExpandListener](../android/view/MenuItem.OnActionExpandListener.md)?:Listener that will respond to expand/collapse events This value may be`null`. |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [MenuItem](MenuItem.md) | This menu item instance for call chaining This value cannot be`null`. |

### setOnMenuItemClickListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setOnMenuItemClickListener(menuItemClickListener: MenuItem.OnMenuItemClickListener?): MenuItem
```

Set a custom listener for invocation of this menu item. In most situations, it is more efficient and easier to use [Activity.onOptionsItemSelected(MenuItem)](../android.app/Activity.md))or [Activity.onContextItemSelected(MenuItem)](../android.app/Activity.md)).

| Parameters ||
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `menuItemClickListener` | [MenuItem.OnMenuItemClickListener](../android/view/MenuItem.OnMenuItemClickListener.md)?:The object to receive invokations. This value may be`null`. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MenuItem](MenuItem.md) | This Item so additional setters can be called. This value cannot be`null`. |

**See Also**

- [android.app.Activity#onOptionsItemSelected(MenuItem)](../android.app/Activity.md))
- [android.app.Activity#onContextItemSelected(MenuItem)](../android.app/Activity.md)) 

### setShortcut

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setShortcut(
    numericChar: Char, 
    alphaChar: Char
): MenuItem
```

Change both the numeric and alphabetic shortcut associated with this item. Note that the shortcut will be triggered when the key that generates the given character is pressed along with the corresponding modifier key. The default modifier is [KeyEvent.META_CTRL_ON](KeyEvent.md) in case nothing is specified. Also note that case is not significant and that alphabetic shortcut characters will be handled in lower case.

See [Menu](Menu.md) for the menu types that support shortcuts.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `numericChar` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):The numeric shortcut key. This is the shortcut when using a numeric (e.g., 12-key) keyboard. |
| `alphaChar` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):The alphabetic shortcut key. This is the shortcut when using a keyboard with alphabetic keys. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MenuItem](MenuItem.md) | This Item so additional setters can be called. This value cannot be`null`. |

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

See [Menu](Menu.md) for the menu types that support shortcuts.

| Parameters ||
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `numericChar` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):The numeric shortcut key. This is the shortcut when using a numeric (e.g., 12-key) keyboard. |
| `numericModifiers` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The numeric modifier associated with the shortcut. It should be a combination of [KeyEvent.META_META_ON](KeyEvent.md), [KeyEvent.META_CTRL_ON](KeyEvent.md), [KeyEvent.META_ALT_ON](KeyEvent.md), [KeyEvent.META_SHIFT_ON](KeyEvent.md), [KeyEvent.META_SYM_ON](KeyEvent.md), [KeyEvent.META_FUNCTION_ON](KeyEvent.md). |
| `alphaChar` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):The alphabetic shortcut key. This is the shortcut when using a keyboard with alphabetic keys. |
| --- | --- |
| `alphaModifiers` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The alphabetic modifier associated with the shortcut. It should be a combination of [KeyEvent.META_META_ON](KeyEvent.md), [KeyEvent.META_CTRL_ON](KeyEvent.md), [KeyEvent.META_ALT_ON](KeyEvent.md), [KeyEvent.META_SHIFT_ON](KeyEvent.md), [KeyEvent.META_SYM_ON](KeyEvent.md), [KeyEvent.META_FUNCTION_ON](KeyEvent.md). |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MenuItem](MenuItem.md) | This Item so additional setters can be called. This value cannot be`null`. |

### setShowAsAction

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setShowAsAction(actionEnum: Int): Unit
```

Sets how this item should display in the presence of an Action Bar. The parameter actionEnum is a flag set. One of [SHOW_AS_ACTION_ALWAYS](MenuItem.md), [SHOW_AS_ACTION_IF_ROOM](MenuItem.md), or [SHOW_AS_ACTION_NEVER](MenuItem.md) should be used, and you may optionally OR the value with [SHOW_AS_ACTION_WITH_TEXT](MenuItem.md). SHOW_AS_ACTION_WITH_TEXT requests that when the item is shown as an action, it should be shown with a text label.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `actionEnum` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):How the item should display. One of [SHOW_AS_ACTION_ALWAYS](MenuItem.md), [SHOW_AS_ACTION_IF_ROOM](MenuItem.md), or [SHOW_AS_ACTION_NEVER](MenuItem.md). SHOW_AS_ACTION_NEVER is the default. |

**See Also**

- [android.app.ActionBar](../android.app/ActionBar.md)
- [#setActionView(View)](MenuItem.md)) 

### setShowAsActionFlags

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setShowAsActionFlags(actionEnum: Int): MenuItem
```

Sets how this item should display in the presence of an Action Bar. The parameter actionEnum is a flag set. One of [SHOW_AS_ACTION_ALWAYS](MenuItem.md), [SHOW_AS_ACTION_IF_ROOM](MenuItem.md), or [SHOW_AS_ACTION_NEVER](MenuItem.md) should be used, and you may optionally OR the value with [SHOW_AS_ACTION_WITH_TEXT](MenuItem.md). SHOW_AS_ACTION_WITH_TEXT requests that when the item is shown as an action, it should be shown with a text label.

Note: This method differs from [setShowAsAction(int)](MenuItem.md))only in that it returns the current MenuItem instance for call chaining.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `actionEnum` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):How the item should display. One of [SHOW_AS_ACTION_ALWAYS](MenuItem.md), [SHOW_AS_ACTION_IF_ROOM](MenuItem.md), or [SHOW_AS_ACTION_NEVER](MenuItem.md). SHOW_AS_ACTION_NEVER is the default. |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [MenuItem](MenuItem.md) | This MenuItem instance for call chaining. This value cannot be`null`. |

**See Also**

- [android.app.ActionBar](../android.app/ActionBar.md)
- [#setActionView(View)](MenuItem.md)) 

### setTitle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setTitle(title: Int): MenuItem
```

Change the title associated with this item.

Some menu types do not sufficient space to show the full title, and instead a condensed title is preferred. See [Menu](Menu.md) for more information.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------|
| `title` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The resource id of the new text to be displayed. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MenuItem](MenuItem.md) | This Item so additional setters can be called. This value cannot be`null`. |

**See Also**

- [#setTitleCondensed(CharSequence)](MenuItem.md)) 

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
| [MenuItem](MenuItem.md) | This Item so additional setters can be called. This value cannot be`null`. |

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
| [MenuItem](MenuItem.md) | This Item so additional setters can be called. This value cannot be`null`. |

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
| [MenuItem](MenuItem.md) | This value cannot be`null`. |

### setVisible

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setVisible(visible: Boolean): MenuItem
```

Sets the visibility of the menu item. Even if a menu item is not visible, it may still be invoked via its shortcut (to completely disable an item, set it to invisible and [disabled](MenuItem.md))).

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `visible` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):If true then the item will be visible; if false it is hidden. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MenuItem](MenuItem.md) | This Item so additional setters can be called. This value cannot be`null`. |
