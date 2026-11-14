# MenuItem

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MenuItem

Kotlin| [Java](../android/view/MenuItem.md) 
| --- | --- |

```
interface MenuItem
```

| [android.view.MenuItem](../android/view/MenuItem.md) |

Interface for direct access to a previously created menu item.

An Item is returned by calling one of the android.view.Menu#add methods.

For a feature set of specific menu types, see [Menu](../android/view/Menu.md).
|
| ### Developer Guides
|
| For information about creating menus, read the [Menus](https://developer.android.com/guide/topics/ui/menus.html) developer guide.

## Summary

| Nested classes ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [OnActionExpandListener](../android/view/MenuItem.OnActionExpandListener.md) Interface definition for a callback to be invoked when a menu item marked with [MenuItem.SHOW_AS_ACTION_COLLAPSE_ACTION_VIEW](../android/view/MenuItem.md) is expanded or collapsed. |
| abstract | [OnMenuItemClickListener](../android/view/MenuItem.OnMenuItemClickListener.md) Interface definition for a callback to be invoked when a menu item is clicked. |

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SHOW_AS_ACTION_ALWAYS](../android/view/MenuItem.md) Always show this item as a button in an Action Bar. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SHOW_AS_ACTION_COLLAPSE_ACTION_VIEW](../android/view/MenuItem.md) This item's action view collapses to a normal menu item. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SHOW_AS_ACTION_IF_ROOM](../android/view/MenuItem.md) Show this item as a button in an Action Bar if the system decides there is room for it. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SHOW_AS_ACTION_NEVER](../android/view/MenuItem.md) Never show this item as a button in an Action Bar. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SHOW_AS_ACTION_WITH_TEXT](../android/view/MenuItem.md) When this item is in the action bar, always show it with a text label even if it also has an icon specified. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [collapseActionView](../android/view/MenuItem.md))`()` Collapse the action view associated with this menu item. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [expandActionView](../android/view/MenuItem.md))`()` Expand the action view associated with this menu item. |
| abstract [ActionProvider](../android/view/ActionProvider.md)? | [getActionProvider](../android/view/MenuItem.md))`()` Gets the [ActionProvider](../android/view/ActionProvider.md). |
| --- | --- |
| abstract [View](../android/view/View.md)? | [getActionView](../android/view/MenuItem.md))`()` Returns the currently set action view for this menu item. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAlphabeticModifiers](../android/view/MenuItem.md))`()` Return the modifier for this menu item's alphabetic shortcut. |
| abstract [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [getAlphabeticShortcut](../android/view/MenuItem.md))`()` Return the char for this menu item's alphabetic shortcut. |
| --- | --- |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getContentDescription](../android/view/MenuItem.md))`()` Retrieve the content description associated with this menu item. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGroupId](../android/view/MenuItem.md))`()` Return the group identifier that this menu item is part of. |
| abstract [Drawable](../android/graphics/drawable/Drawable.md)? | [getIcon](../android/view/MenuItem.md))`()` Returns the icon for this item as a Drawable (getting it from resources if it hasn't been loaded before). |
| --- | --- |
| open [BlendMode](../android/graphics/BlendMode.md)? | [getIconTintBlendMode](../android/view/MenuItem.md))`()` Returns the blending mode used to apply the tint to this item's icon, if specified. |
| open [ColorStateList](../android/content/res/ColorStateList.md)? | [getIconTintList](../android/view/MenuItem.md))`()` <br /> |
| open [PorterDuff.Mode](../android/graphics/PorterDuff.Mode.md)? | [getIconTintMode](../android/view/MenuItem.md))`()` Returns the blending mode used to apply the tint to this item's icon, if specified. |
| --- | --- |
| abstract [Intent](../android/content/Intent.md)? | [getIntent](../android/view/MenuItem.md))`()` Return the Intent associated with this item. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getItemId](../android/view/MenuItem.md))`()` Return the identifier for this menu item. |
| abstract [ContextMenu.ContextMenuInfo](../android/view/ContextMenu.ContextMenuInfo.md)? | [getMenuInfo](../android/view/MenuItem.md))`()` Gets the extra information linked to this menu item. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getNumericModifiers](../android/view/MenuItem.md))`()` Return the modifiers for this menu item's numeric (12-key) shortcut. |
| abstract [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [getNumericShortcut](../android/view/MenuItem.md))`()` Return the char for this menu item's numeric (12-key) shortcut. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOrder](../android/view/MenuItem.md))`()` Return the category and order within the category of this item. |
| --- | --- |
| abstract [SubMenu](../android/view/SubMenu.md)? | [getSubMenu](../android/view/MenuItem.md))`()` Get the sub-menu to be invoked when this item is selected, if it has one. |
| abstract [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getTitle](../android/view/MenuItem.md))`()` Retrieve the current title of the item. |
| abstract [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getTitleCondensed](../android/view/MenuItem.md))`()` Retrieve the current condensed title of the item. |
| --- | --- |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getTooltipText](../android/view/MenuItem.md))`()` Retrieve the tooltip text associated with this menu item. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasSubMenu](../android/view/MenuItem.md))`()` Check whether this item has an associated sub-menu. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isActionViewExpanded](../android/view/MenuItem.md))`()` Returns true if this menu item's action view has been expanded. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCheckable](../android/view/MenuItem.md))`()` Return whether the item can currently display a check mark. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isChecked](../android/view/MenuItem.md))`()` Return whether the item is currently displaying a check mark. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEnabled](../android/view/MenuItem.md))`()` Return the enabled state of the menu item. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isVisible](../android/view/MenuItem.md))`()` Return the visibility of the menu item. |
| abstract [MenuItem](../android/view/MenuItem.md) | [setActionProvider](../android/view/MenuItem.md))`(`actionProvider:` ` [ActionProvider](../android/view/ActionProvider.md)?`)` Sets the [ActionProvider](../android/view/ActionProvider.md) responsible for creating an action view if the item is placed on the action bar. |
| abstract [MenuItem](../android/view/MenuItem.md) | [setActionView](../android/view/MenuItem.md))`(`view:` ` [View](../android/view/View.md)?`)` Set an action view for this menu item. |
| --- | --- |
| abstract [MenuItem](../android/view/MenuItem.md) | [setActionView](../android/view/MenuItem.md))`(`resId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set an action view for this menu item. |
| abstract [MenuItem](../android/view/MenuItem.md) | [setAlphabeticShortcut](../android/view/MenuItem.md))`(`alphaChar:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` Change the alphabetic shortcut associated with this item. |
| open [MenuItem](../android/view/MenuItem.md) | [setAlphabeticShortcut](../android/view/MenuItem.md))`(`alphaChar:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`, `alphaModifiers:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Change the alphabetic shortcut associated with this item. |
| --- | --- |
| abstract [MenuItem](../android/view/MenuItem.md) | [setCheckable](../android/view/MenuItem.md))`(`checkable:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Control whether this item can display a check mark. |
| abstract [MenuItem](../android/view/MenuItem.md) | [setChecked](../android/view/MenuItem.md))`(`checked:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Control whether this item is shown with a check mark. |
| open [MenuItem](../android/view/MenuItem.md) | [setContentDescription](../android/view/MenuItem.md))`(`contentDescription:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?`)` Change the content description associated with this menu item. |
| --- | --- |
| abstract [MenuItem](../android/view/MenuItem.md) | [setEnabled](../android/view/MenuItem.md))`(`enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether the menu item is enabled. |
| abstract [MenuItem](../android/view/MenuItem.md) | [setIcon](../android/view/MenuItem.md))`(`icon:` ` [Drawable](../android/graphics/drawable/Drawable.md)?`)` Change the icon associated with this item. |
| abstract [MenuItem](../android/view/MenuItem.md) | [setIcon](../android/view/MenuItem.md))`(`iconRes:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Change the icon associated with this item. |
| --- | --- |
| open [MenuItem](../android/view/MenuItem.md) | [setIconTintBlendMode](../android/view/MenuItem.md))`(`blendMode:` ` [BlendMode](../android/graphics/BlendMode.md)?`)` Specifies the blending mode used to apply the tint specified by [setIconTintList(android.content.res.ColorStateList)](../android/view/MenuItem.md))to this item's icon. |
| open [MenuItem](../android/view/MenuItem.md) | [setIconTintList](../android/view/MenuItem.md))`(`tint:` ` [ColorStateList](../android/content/res/ColorStateList.md)?`)` Applies a tint to this item's icon. |
| open [MenuItem](../android/view/MenuItem.md) | [setIconTintMode](../android/view/MenuItem.md))`(`tintMode:` ` [PorterDuff.Mode](../android/graphics/PorterDuff.Mode.md)?`)` Specifies the blending mode used to apply the tint specified by [setIconTintList(android.content.res.ColorStateList)](../android/view/MenuItem.md))to this item's icon. |
| --- | --- |
| abstract [MenuItem](../android/view/MenuItem.md) | [setIntent](../android/view/MenuItem.md))`(`intent:` ` [Intent](../android/content/Intent.md)?`)` Change the Intent associated with this item. |
| abstract [MenuItem](../android/view/MenuItem.md) | [setNumericShortcut](../android/view/MenuItem.md))`(`numericChar:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` Change the numeric shortcut associated with this item. |
| open [MenuItem](../android/view/MenuItem.md) | [setNumericShortcut](../android/view/MenuItem.md))`(`numericChar:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`, `numericModifiers:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Change the numeric shortcut and modifiers associated with this item. |
| --- | --- |
| abstract [MenuItem](../android/view/MenuItem.md) | [setOnActionExpandListener](../android/view/MenuItem.md))`(`listener:` ` [MenuItem.OnActionExpandListener](../android/view/MenuItem.OnActionExpandListener.md)?`)` Set an [OnActionExpandListener](../android/view/MenuItem.OnActionExpandListener.md) on this menu item to be notified when the associated action view is expanded or collapsed. |
| abstract [MenuItem](../android/view/MenuItem.md) | [setOnMenuItemClickListener](../android/view/MenuItem.md))`(`menuItemClickListener:` ` [MenuItem.OnMenuItemClickListener](../android/view/MenuItem.OnMenuItemClickListener.md)?`)` Set a custom listener for invocation of this menu item. |
| abstract [MenuItem](../android/view/MenuItem.md) | [setShortcut](../android/view/MenuItem.md))`(`numericChar:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`, `alphaChar:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` Change both the numeric and alphabetic shortcut associated with this item. |
| --- | --- |
| open [MenuItem](../android/view/MenuItem.md) | [setShortcut](../android/view/MenuItem.md))`(`numericChar:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`, `alphaChar:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`, `numericModifiers:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `alphaModifiers:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Change both the numeric and alphabetic shortcut associated with this item. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setShowAsAction](../android/view/MenuItem.md))`(`actionEnum:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets how this item should display in the presence of an Action Bar. |
| abstract [MenuItem](../android/view/MenuItem.md) | [setShowAsActionFlags](../android/view/MenuItem.md))`(`actionEnum:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets how this item should display in the presence of an Action Bar. |
| --- | --- |
| abstract [MenuItem](../android/view/MenuItem.md) | [setTitle](../android/view/MenuItem.md))`(`title:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Change the title associated with this item. |
| abstract [MenuItem](../android/view/MenuItem.md) | [setTitle](../android/view/MenuItem.md))`(`title:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?`)` Change the title associated with this item. |
| abstract [MenuItem](../android/view/MenuItem.md) | [setTitleCondensed](../android/view/MenuItem.md))`(`title:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?`)` Change the condensed title associated with this item. |
| --- | --- |
| open [MenuItem](../android/view/MenuItem.md) | [setTooltipText](../android/view/MenuItem.md))`(`tooltipText:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?`)` Change the tooltip text associated with this menu item. |
| abstract [MenuItem](../android/view/MenuItem.md) | [setVisible](../android/view/MenuItem.md))`(`visible:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets the visibility of the menu item. |

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

Collapse the action view associated with this menu item. The menu item must have an action view set, as well as the showAsAction flag [SHOW_AS_ACTION_COLLAPSE_ACTION_VIEW](../android/view/MenuItem.md). If a listener has been set using [setOnActionExpandListener(android.view.MenuItem.OnActionExpandListener)](../android/view/MenuItem.md))it will have its [OnActionExpandListener.onMenuItemActionCollapse(MenuItem)](../android/view/MenuItem.OnActionExpandListener.md))method invoked. The listener may return false from this method to prevent collapsing the action view.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the action view was collapsed, false otherwise. |

### expandActionView

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun expandActionView(): Boolean
```

Expand the action view associated with this menu item. The menu item must have an action view set, as well as the showAsAction flag [SHOW_AS_ACTION_COLLAPSE_ACTION_VIEW](../android/view/MenuItem.md). If a listener has been set using [setOnActionExpandListener(android.view.MenuItem.OnActionExpandListener)](../android/view/MenuItem.md))it will have its [OnActionExpandListener.onMenuItemActionExpand(MenuItem)](../android/view/MenuItem.OnActionExpandListener.md))method invoked. The listener may return false from this method to prevent expanding the action view.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the action view was expanded, false otherwise. |

### getActionProvider

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getActionProvider(): ActionProvider?
```

Gets the [ActionProvider](../android/view/ActionProvider.md).

| Return ||
|-----------------------------------------------------------------------------------------------|-----------------------------------------------|
| [ActionProvider](../android/view/ActionProvider.md)? | The action provider. This value may be`null`. |

**See Also**

- [android.view.ActionProvider](../android/view/ActionProvider.md)
- [#setActionProvider(ActionProvider)](../android/view/MenuItem.md)) 

### getActionView

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getActionView(): View?
```

Returns the currently set action view for this menu item.

| Return ||
|---------------------------------------------------------------------------|--------------------------------------------------|
| [View](../android/view/View.md)? | This item's action view This value may be`null`. |

**See Also**

- [#setActionView(View)](../android/view/MenuItem.md))
- [#setShowAsAction(int)](../android/view/MenuItem.md)) 

### getAlphabeticModifiers

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAlphabeticModifiers(): Int
```

Return the modifier for this menu item's alphabetic shortcut. The modifier is a combination of [KeyEvent.META_META_ON](../android/view/KeyEvent.md), [KeyEvent.META_CTRL_ON](../android/view/KeyEvent.md), [KeyEvent.META_ALT_ON](../android/view/KeyEvent.md), [KeyEvent.META_SHIFT_ON](../android/view/KeyEvent.md), [KeyEvent.META_SYM_ON](../android/view/KeyEvent.md), [KeyEvent.META_FUNCTION_ON](../android/view/KeyEvent.md). For example, [KeyEvent.META_FUNCTION_ON](../android/view/KeyEvent.md)| [KeyEvent.META_CTRL_ON](../android/view/KeyEvent.md)
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

Returns the icon for this item as a Drawable (getting it from resources if it hasn't been loaded before). Note that if you call [setIconTintList(android.content.res.ColorStateList)](../android/view/MenuItem.md))or [setIconTintMode(android.graphics.PorterDuff.Mode)](../android/view/MenuItem.md))on this item, and you use a custom menu presenter in your application, you have to apply the tinting explicitly on the [Drawable](../android/graphics/drawable/Drawable.md) returned by this method.

| Return ||
|------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| [Drawable](../android/graphics/drawable/Drawable.md)? | The icon as a Drawable. This value may be`null`. |

### getIconTintBlendMode

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getIconTintBlendMode(): BlendMode?
```

Returns the blending mode used to apply the tint to this item's icon, if specified.

| Return ||
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [BlendMode](../android/graphics/BlendMode.md)? | the blending mode used to apply the tint to this item's icon This value may be`null`. |

**See Also**

- [#setIconTintBlendMode(BlendMode)](../android/view/MenuItem.md)) 

### getIconTintList

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getIconTintList(): ColorStateList?
```

| Return ||
|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [ColorStateList](../android/content/res/ColorStateList.md)? | the tint applied to this item's icon This value may be`null`. |

**See Also**

- [#setIconTintList(ColorStateList)](../android/view/MenuItem.md)) 

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

- [#setIconTintMode(PorterDuff.Mode)](../android/view/MenuItem.md))
- [#setIconTintBlendMode(BlendMode)](../android/view/MenuItem.md)) 

### getIntent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getIntent(): Intent?
```

Return the Intent associated with this item. This returns a reference to the Intent which you can change as desired to modify what the Item is holding.

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Intent](../android/content/Intent.md)? | Returns the last value supplied to [setIntent](../android/view/MenuItem.md)), or null. |

**See Also**

- [#setIntent](../android/view/MenuItem.md)) 

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

Return the modifiers for this menu item's numeric (12-key) shortcut. The modifier is a combination of [KeyEvent.META_META_ON](../android/view/KeyEvent.md), [KeyEvent.META_CTRL_ON](../android/view/KeyEvent.md), [KeyEvent.META_ALT_ON](../android/view/KeyEvent.md), [KeyEvent.META_SHIFT_ON](../android/view/KeyEvent.md), [KeyEvent.META_SYM_ON](../android/view/KeyEvent.md), [KeyEvent.META_FUNCTION_ON](../android/view/KeyEvent.md). For example, [KeyEvent.META_FUNCTION_ON](../android/view/KeyEvent.md)| [KeyEvent.META_CTRL_ON](../android/view/KeyEvent.md)
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

An order integer contains the item's category (the upper bits of the integer; set by or/add the category with the order within the category) and the ordering of the item within that category (the lower bits). Example categories are [Menu.CATEGORY_SYSTEM](../android/view/Menu.md), [Menu.CATEGORY_SECONDARY](../android/view/Menu.md), [Menu.CATEGORY_ALTERNATIVE](../android/view/Menu.md), [Menu.CATEGORY_CONTAINER](../android/view/Menu.md). See [Menu](../android/view/Menu.md) for a full list.

| Return ||
|----------------------------------------------------------------------------|-------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The order of this item. |

### getSubMenu

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getSubMenu(): SubMenu?
```

Get the sub-menu to be invoked when this item is selected, if it has one. See [hasSubMenu()](../android/view/MenuItem.md)).

| Return ||
|---------------------------------------------------------------------------------|------------------------------------------------|
| [SubMenu](../android/view/SubMenu.md)? | The associated menu if there is one, else null |

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
- [#SHOW_AS_ACTION_COLLAPSE_ACTION_VIEW](../android/view/MenuItem.md)
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

- [#setCheckable](../android/view/MenuItem.md)) 

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

- [#setChecked](../android/view/MenuItem.md)) 

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

Sets the [ActionProvider](../android/view/ActionProvider.md) responsible for creating an action view if the item is placed on the action bar. The provider also provides a default action invoked if the item is placed in the overflow menu.

**Note:** Setting an action provider overrides the action view set via [setActionView(int)](../android/view/MenuItem.md))or [setActionView(android.view.View)](../android/view/MenuItem.md)).

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `actionProvider` | [ActionProvider](../android/view/ActionProvider.md)?:The action provider. This value may be`null`. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MenuItem](../android/view/MenuItem.md) | This Item so additional setters can be called. This value cannot be`null`. |

**See Also**

- [android.view.ActionProvider](../android/view/ActionProvider.md) 

### setActionView

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setActionView(view: View?): MenuItem
```

Set an action view for this menu item. An action view will be displayed in place of an automatically generated menu item element in the UI when this item is shown as an action within a parent.

**Note:** Setting an action view overrides the action provider set via [setActionProvider(android.view.ActionProvider)](../android/view/MenuItem.md)).

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [View](../android/view/View.md)?:View to use for presenting this item to the user. This value may be`null`. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MenuItem](../android/view/MenuItem.md) | This Item so additional setters can be called. This value cannot be`null`. |

**See Also**

- [#setShowAsAction(int)](../android/view/MenuItem.md)) 

### setActionView

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setActionView(resId: Int): MenuItem
```

Set an action view for this menu item. An action view will be displayed in place of an automatically generated menu item element in the UI when this item is shown as an action within a parent.

**Note:** Setting an action view overrides the action provider set via [setActionProvider(android.view.ActionProvider)](../android/view/MenuItem.md)).

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `resId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Layout resource to use for presenting this item to the user. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MenuItem](../android/view/MenuItem.md) | This Item so additional setters can be called. This value cannot be`null`. |

**See Also**

- [#setShowAsAction(int)](../android/view/MenuItem.md)) 

### setAlphabeticShortcut

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setAlphabeticShortcut(alphaChar: Char): MenuItem
```

Change the alphabetic shortcut associated with this item. The shortcut will be triggered when the key that generates the given character is pressed along with the corresponding modifier key. The default modifier is [KeyEvent.META_CTRL_ON](../android/view/KeyEvent.md) in case nothing is specified. Case is not significant and shortcut characters will be displayed in lower case. Note that menu items with the characters '\\b' or '\\n' as shortcuts will get triggered by the Delete key or Carriage Return key, respectively.

See [Menu](../android/view/Menu.md) for the menu types that support shortcuts.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `alphaChar` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):The alphabetic shortcut key. This is the shortcut when using a keyboard with alphabetic keys. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MenuItem](../android/view/MenuItem.md) | This Item so additional setters can be called. This value cannot be`null`. |

### setAlphabeticShortcut

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setAlphabeticShortcut(
    alphaChar: Char, 
    alphaModifiers: Int
): MenuItem
```

Change the alphabetic shortcut associated with this item. The shortcut will be triggered when the key that generates the given character is pressed along with the modifier keys. Case is not significant and shortcut characters will be displayed in lower case. Note that menu items with the characters '\\b' or '\\n' as shortcuts will get triggered by the Delete key or Carriage Return key, respectively.

See [Menu](../android/view/Menu.md) for the menu types that support shortcuts.

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `alphaChar` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):The alphabetic shortcut key. This is the shortcut when using a keyboard with alphabetic keys. |
| `alphaModifiers` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The modifier associated with the shortcut. It should be a combination of [KeyEvent.META_META_ON](../android/view/KeyEvent.md), [KeyEvent.META_CTRL_ON](../android/view/KeyEvent.md), [KeyEvent.META_ALT_ON](../android/view/KeyEvent.md), [KeyEvent.META_SHIFT_ON](../android/view/KeyEvent.md), [KeyEvent.META_SYM_ON](../android/view/KeyEvent.md), [KeyEvent.META_FUNCTION_ON](../android/view/KeyEvent.md). |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MenuItem](../android/view/MenuItem.md) | This Item so additional setters can be called. This value cannot be`null`. |

### setCheckable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setCheckable(checkable: Boolean): MenuItem
```

Control whether this item can display a check mark. Setting this does not actually display a check mark (see [setChecked](../android/view/MenuItem.md))for that); rather, it ensures there is room in the item in which to display a check mark.

See [Menu](../android/view/Menu.md) for the menu types that support check marks.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `checkable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Set to true to allow a check mark, false to disallow. The default is false. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MenuItem](../android/view/MenuItem.md) | This Item so additional setters can be called. This value cannot be`null`. |

**See Also**

- [#setChecked](../android/view/MenuItem.md))
- [#isCheckable](../android/view/MenuItem.md))
- [android.view.Menu#setGroupCheckable](../android/view/Menu.md)) 

### setChecked

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setChecked(checked: Boolean): MenuItem
```

Control whether this item is shown with a check mark. Note that you must first have enabled checking with [setCheckable](../android/view/MenuItem.md))or else the check mark will not appear. If this item is a member of a group that contains mutually-exclusive items (set via [Menu.setGroupCheckable(int, boolean, boolean)](../android/view/Menu.md)), the other items in the group will be unchecked.

See [Menu](../android/view/Menu.md) for the menu types that support check marks.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `checked` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Set to true to display a check mark, false to hide it. The default value is false. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MenuItem](../android/view/MenuItem.md) | This Item so additional setters can be called. This value cannot be`null`. |

**See Also**

- [#setCheckable](../android/view/MenuItem.md))
- [#isChecked](../android/view/MenuItem.md))
- [android.view.Menu#setGroupCheckable](../android/view/Menu.md)) 

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
| [MenuItem](../android/view/MenuItem.md) | This value cannot be`null`. |

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
| [MenuItem](../android/view/MenuItem.md) | This Item so additional setters can be called. This value cannot be`null`. |

### setIcon

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setIcon(icon: Drawable?): MenuItem
```

Change the icon associated with this item. This icon will not always be shown, so the title should be sufficient in describing this item. See [Menu](../android/view/Menu.md) for the menu types that support icons.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `icon` | [Drawable](../android/graphics/drawable/Drawable.md)?:The new icon (as a Drawable) to be displayed. This value may be`null`. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MenuItem](../android/view/MenuItem.md) | This Item so additional setters can be called. This value cannot be`null`. |

### setIcon

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setIcon(iconRes: Int): MenuItem
```

Change the icon associated with this item. This icon will not always be shown, so the title should be sufficient in describing this item. See [Menu](../android/view/Menu.md) for the menu types that support icons.

This method will set the resource ID of the icon which will be used to lazily get the Drawable when this item is being shown.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------|
| `iconRes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The new icon (as a resource ID) to be displayed. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MenuItem](../android/view/MenuItem.md) | This Item so additional setters can be called. This value cannot be`null`. |

### setIconTintBlendMode

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setIconTintBlendMode(blendMode: BlendMode?): MenuItem
```

Specifies the blending mode used to apply the tint specified by [setIconTintList(android.content.res.ColorStateList)](../android/view/MenuItem.md))to this item's icon. The default mode is [BlendMode.SRC_IN](../android/graphics/BlendMode.md).

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `blendMode` | [BlendMode](../android/graphics/BlendMode.md)?:the blending mode used to apply the tint, may be`null`to clear tint |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------|
| [MenuItem](../android/view/MenuItem.md) | This value cannot be`null`. |

**See Also**

- [#setIconTintList(ColorStateList)](../android/view/MenuItem.md)) 

### setIconTintList

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setIconTintList(tint: ColorStateList?): MenuItem
```

Applies a tint to this item's icon. Does not modify the current tint mode, which is [PorterDuff.Mode.SRC_IN](../android/graphics/PorterDuff.Mode.md) by default.

Subsequent calls to [setIcon(android.graphics.drawable.Drawable)](../android/view/MenuItem.md))or [setIcon(int)](../android/view/MenuItem.md))will automatically mutate the icon and apply the specified tint and tint mode using [Drawable.setTintList(ColorStateList)](../android/graphics/drawable/Drawable.md)).

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tint` | [ColorStateList](../android/content/res/ColorStateList.md)?:the tint to apply, may be`null`to clear tint |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------|
| [MenuItem](../android/view/MenuItem.md) | This value cannot be`null`. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/view/MenuItem#getIconTintList()>
- [android.graphics.drawable.Drawable#setTintList(ColorStateList)](../android/graphics/drawable/Drawable.md)) 

### setIconTintMode

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setIconTintMode(tintMode: PorterDuff.Mode?): MenuItem
```

Specifies the blending mode used to apply the tint specified by [setIconTintList(android.content.res.ColorStateList)](../android/view/MenuItem.md))to this item's icon. The default mode is [PorterDuff.Mode.SRC_IN](../android/graphics/PorterDuff.Mode.md).

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tintMode` | [PorterDuff.Mode](../android/graphics/PorterDuff.Mode.md)?:the blending mode used to apply the tint, may be`null`to clear tint |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------|
| [MenuItem](../android/view/MenuItem.md) | This value cannot be`null`. |

**See Also**

- [#setIconTintList(ColorStateList)](../android/view/MenuItem.md))
- [android.graphics.drawable.Drawable#setTintMode(PorterDuff.Mode)](../android/graphics/drawable/Drawable.md))
- [android.graphics.drawable.Drawable#setTintBlendMode(BlendMode)](../android/graphics/drawable/Drawable.md)) 

### setIntent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setIntent(intent: Intent?): MenuItem
```

Change the Intent associated with this item. By default there is no Intent associated with a menu item. If you set one, and nothing else handles the item, then the default behavior will be to call android.content.Context#startActivity with the given Intent.

Note that setIntent() can not be used with the versions of android.view.Menu#add that take a Runnable, because [Runnable.run](../java/lang/Runnable.md))does not return a value so there is no way to tell if it handled the item. In this case it is assumed that the Runnable always handles the item, and the intent will never be started.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `intent` | [Intent](../android/content/Intent.md)?:The Intent to associated with the item. This Intent object is*not* copied, so be careful not to modify it later. This value may be`null`. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MenuItem](../android/view/MenuItem.md) | This Item so additional setters can be called. This value cannot be`null`. |

**See Also**

- [#getIntent](../android/view/MenuItem.md)) 

### setNumericShortcut

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setNumericShortcut(numericChar: Char): MenuItem
```

Change the numeric shortcut associated with this item.

See [Menu](../android/view/Menu.md) for the menu types that support shortcuts.

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `numericChar` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):The numeric shortcut key. This is the shortcut when using a 12-key (numeric) keyboard. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MenuItem](../android/view/MenuItem.md) | This Item so additional setters can be called. This value cannot be`null`. |

### setNumericShortcut

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setNumericShortcut(
    numericChar: Char, 
    numericModifiers: Int
): MenuItem
```

Change the numeric shortcut and modifiers associated with this item.

See [Menu](../android/view/Menu.md) for the menu types that support shortcuts.

| Parameters ||
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `numericChar` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):The numeric shortcut key. This is the shortcut when using a 12-key (numeric) keyboard. |
| `numericModifiers` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The modifier associated with the shortcut. It should be a combination of [KeyEvent.META_META_ON](../android/view/KeyEvent.md), [KeyEvent.META_CTRL_ON](../android/view/KeyEvent.md), [KeyEvent.META_ALT_ON](../android/view/KeyEvent.md), [KeyEvent.META_SHIFT_ON](../android/view/KeyEvent.md), [KeyEvent.META_SYM_ON](../android/view/KeyEvent.md), [KeyEvent.META_FUNCTION_ON](../android/view/KeyEvent.md). |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MenuItem](../android/view/MenuItem.md) | This Item so additional setters can be called. This value cannot be`null`. |

### setOnActionExpandListener

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setOnActionExpandListener(listener: MenuItem.OnActionExpandListener?): MenuItem
```

Set an [OnActionExpandListener](../android/view/MenuItem.OnActionExpandListener.md) on this menu item to be notified when the associated action view is expanded or collapsed. The menu item must be configured to expand or collapse its action view using the flag [SHOW_AS_ACTION_COLLAPSE_ACTION_VIEW](../android/view/MenuItem.md).

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [MenuItem.OnActionExpandListener](../android/view/MenuItem.OnActionExpandListener.md)?:Listener that will respond to expand/collapse events This value may be`null`. |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [MenuItem](../android/view/MenuItem.md) | This menu item instance for call chaining This value cannot be`null`. |

### setOnMenuItemClickListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setOnMenuItemClickListener(menuItemClickListener: MenuItem.OnMenuItemClickListener?): MenuItem
```

Set a custom listener for invocation of this menu item. In most situations, it is more efficient and easier to use [Activity.onOptionsItemSelected(MenuItem)](../android/app/Activity.md))or [Activity.onContextItemSelected(MenuItem)](../android/app/Activity.md)).

| Parameters ||
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `menuItemClickListener` | [MenuItem.OnMenuItemClickListener](../android/view/MenuItem.OnMenuItemClickListener.md)?:The object to receive invokations. This value may be`null`. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MenuItem](../android/view/MenuItem.md) | This Item so additional setters can be called. This value cannot be`null`. |

**See Also**

- [android.app.Activity#onOptionsItemSelected(MenuItem)](../android/app/Activity.md))
- [android.app.Activity#onContextItemSelected(MenuItem)](../android/app/Activity.md)) 

### setShortcut

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setShortcut(
    numericChar: Char, 
    alphaChar: Char
): MenuItem
```

Change both the numeric and alphabetic shortcut associated with this item. Note that the shortcut will be triggered when the key that generates the given character is pressed along with the corresponding modifier key. The default modifier is [KeyEvent.META_CTRL_ON](../android/view/KeyEvent.md) in case nothing is specified. Also note that case is not significant and that alphabetic shortcut characters will be handled in lower case.

See [Menu](../android/view/Menu.md) for the menu types that support shortcuts.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `numericChar` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):The numeric shortcut key. This is the shortcut when using a numeric (e.g., 12-key) keyboard. |
| `alphaChar` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):The alphabetic shortcut key. This is the shortcut when using a keyboard with alphabetic keys. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MenuItem](../android/view/MenuItem.md) | This Item so additional setters can be called. This value cannot be`null`. |

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

See [Menu](../android/view/Menu.md) for the menu types that support shortcuts.

| Parameters ||
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `numericChar` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):The numeric shortcut key. This is the shortcut when using a numeric (e.g., 12-key) keyboard. |
| `numericModifiers` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The numeric modifier associated with the shortcut. It should be a combination of [KeyEvent.META_META_ON](../android/view/KeyEvent.md), [KeyEvent.META_CTRL_ON](../android/view/KeyEvent.md), [KeyEvent.META_ALT_ON](../android/view/KeyEvent.md), [KeyEvent.META_SHIFT_ON](../android/view/KeyEvent.md), [KeyEvent.META_SYM_ON](../android/view/KeyEvent.md), [KeyEvent.META_FUNCTION_ON](../android/view/KeyEvent.md). |
| `alphaChar` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):The alphabetic shortcut key. This is the shortcut when using a keyboard with alphabetic keys. |
| --- | --- |
| `alphaModifiers` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The alphabetic modifier associated with the shortcut. It should be a combination of [KeyEvent.META_META_ON](../android/view/KeyEvent.md), [KeyEvent.META_CTRL_ON](../android/view/KeyEvent.md), [KeyEvent.META_ALT_ON](../android/view/KeyEvent.md), [KeyEvent.META_SHIFT_ON](../android/view/KeyEvent.md), [KeyEvent.META_SYM_ON](../android/view/KeyEvent.md), [KeyEvent.META_FUNCTION_ON](../android/view/KeyEvent.md). |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MenuItem](../android/view/MenuItem.md) | This Item so additional setters can be called. This value cannot be`null`. |

### setShowAsAction

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setShowAsAction(actionEnum: Int): Unit
```

Sets how this item should display in the presence of an Action Bar. The parameter actionEnum is a flag set. One of [SHOW_AS_ACTION_ALWAYS](../android/view/MenuItem.md), [SHOW_AS_ACTION_IF_ROOM](../android/view/MenuItem.md), or [SHOW_AS_ACTION_NEVER](../android/view/MenuItem.md) should be used, and you may optionally OR the value with [SHOW_AS_ACTION_WITH_TEXT](../android/view/MenuItem.md). SHOW_AS_ACTION_WITH_TEXT requests that when the item is shown as an action, it should be shown with a text label.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `actionEnum` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):How the item should display. One of [SHOW_AS_ACTION_ALWAYS](../android/view/MenuItem.md), [SHOW_AS_ACTION_IF_ROOM](../android/view/MenuItem.md), or [SHOW_AS_ACTION_NEVER](../android/view/MenuItem.md). SHOW_AS_ACTION_NEVER is the default. |

**See Also**

- [android.app.ActionBar](../android/app/ActionBar.md)
- [#setActionView(View)](../android/view/MenuItem.md)) 

### setShowAsActionFlags

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setShowAsActionFlags(actionEnum: Int): MenuItem
```

Sets how this item should display in the presence of an Action Bar. The parameter actionEnum is a flag set. One of [SHOW_AS_ACTION_ALWAYS](../android/view/MenuItem.md), [SHOW_AS_ACTION_IF_ROOM](../android/view/MenuItem.md), or [SHOW_AS_ACTION_NEVER](../android/view/MenuItem.md) should be used, and you may optionally OR the value with [SHOW_AS_ACTION_WITH_TEXT](../android/view/MenuItem.md). SHOW_AS_ACTION_WITH_TEXT requests that when the item is shown as an action, it should be shown with a text label.

Note: This method differs from [setShowAsAction(int)](../android/view/MenuItem.md))only in that it returns the current MenuItem instance for call chaining.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `actionEnum` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):How the item should display. One of [SHOW_AS_ACTION_ALWAYS](../android/view/MenuItem.md), [SHOW_AS_ACTION_IF_ROOM](../android/view/MenuItem.md), or [SHOW_AS_ACTION_NEVER](../android/view/MenuItem.md). SHOW_AS_ACTION_NEVER is the default. |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [MenuItem](../android/view/MenuItem.md) | This MenuItem instance for call chaining. This value cannot be`null`. |

**See Also**

- [android.app.ActionBar](../android/app/ActionBar.md)
- [#setActionView(View)](../android/view/MenuItem.md)) 

### setTitle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setTitle(title: Int): MenuItem
```

Change the title associated with this item.

Some menu types do not sufficient space to show the full title, and instead a condensed title is preferred. See [Menu](../android/view/Menu.md) for more information.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------|
| `title` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The resource id of the new text to be displayed. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MenuItem](../android/view/MenuItem.md) | This Item so additional setters can be called. This value cannot be`null`. |

**See Also**

- [#setTitleCondensed(CharSequence)](../android/view/MenuItem.md)) 

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
| [MenuItem](../android/view/MenuItem.md) | This Item so additional setters can be called. This value cannot be`null`. |

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
| [MenuItem](../android/view/MenuItem.md) | This Item so additional setters can be called. This value cannot be`null`. |

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
| [MenuItem](../android/view/MenuItem.md) | This value cannot be`null`. |

### setVisible

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setVisible(visible: Boolean): MenuItem
```

Sets the visibility of the menu item. Even if a menu item is not visible, it may still be invoked via its shortcut (to completely disable an item, set it to invisible and [disabled](../android/view/MenuItem.md))).

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `visible` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):If true then the item will be visible; if false it is hidden. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MenuItem](../android/view/MenuItem.md) | This Item so additional setters can be called. This value cannot be`null`. |
