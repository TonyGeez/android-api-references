# PopupMenu

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PopupMenu

Kotlin| [Java](PopupMenu.md) 
| --- | --- |

```
open class PopupMenu
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.widget.PopupMenu](PopupMenu.md) |

A PopupMenu displays a [Menu](../android.view/Menu.md) in a modal popup window anchored to a [View](../android.view/View.md). The popup will appear below the anchor view if there is room, or above it if there is not. If the IME is visible the popup will not overlap it until it is touched. Touching outside of the popup will dismiss it.

## Summary

| Nested classes ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [OnDismissListener](../android/widget/PopupMenu.OnDismissListener.md) Callback interface used to notify the application that the menu has closed. |
| abstract | [OnMenuItemClickListener](../android/widget/PopupMenu.OnMenuItemClickListener.md) Interface responsible for receiving menu item click events if the items themselves do not have individual item click listeners. |

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PopupMenu](PopupMenu.md))`(`context:` ` [Context](../android.content/Context.md)!`, `anchor:` ` [View](../android.view/View.md)!`)` Constructor to create a new popup menu with an anchor view. |
| [PopupMenu](PopupMenu.md))`(`context:` ` [Context](../android.content/Context.md)!`, `anchor:` ` [View](../android.view/View.md)!`, `gravity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructor to create a new popup menu with an anchor view and alignment gravity. |
| [PopupMenu](PopupMenu.md))`(`context:` ` [Context](../android.content/Context.md)!`, `anchor:` ` [View](../android.view/View.md)!`, `gravity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `popupStyleAttr:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `popupStyleRes:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructor a create a new popup menu with a specific style. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dismiss](PopupMenu.md))`()` Dismiss the menu popup. |
| open [View.OnTouchListener](../android/view/View.OnTouchListener.md)! | [getDragToOpenListener](PopupMenu.md))`()` Returns an [OnTouchListener](../android/view/View.OnTouchListener.md) that can be added to the anchor view to implement drag-to-open behavior. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGravity](PopupMenu.md))`()` <br /> |
| --- | --- |
| open [Menu](../android.view/Menu.md)! | [getMenu](PopupMenu.md))`()` Returns the [Menu](../android.view/Menu.md) associated with this popup. |
| open [MenuInflater](../android.view/MenuInflater.md)! | [getMenuInflater](PopupMenu.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [inflate](PopupMenu.md))`(`menuRes:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Inflate a menu resource into this PopupMenu. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setForceShowIcon](PopupMenu.md))`(`forceShowIcon:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether the popup menu's adapter is forced to show icons in the menu item views. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setGravity](PopupMenu.md))`(`gravity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the gravity used to align the popup window to its anchor view. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnDismissListener](PopupMenu.md))`(`listener:` ` [PopupMenu.OnDismissListener](../android/widget/PopupMenu.OnDismissListener.md)!`)` Sets a listener that will be notified when this menu is dismissed. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnMenuItemClickListener](PopupMenu.md))`(`listener:` ` [PopupMenu.OnMenuItemClickListener](../android/widget/PopupMenu.OnMenuItemClickListener.md)!`)` Sets a listener that will be notified when the user selects an item from the menu. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [show](PopupMenu.md))`()` Show the menu popup anchored to the view specified during construction. |

## Public constructors

### PopupMenu

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PopupMenu(
    context: Context!, 
    anchor: View!)
```

Constructor to create a new popup menu with an anchor view.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android.content/Context.md)!:Context the popup menu is running in, through which it can access the current theme, resources, etc. |
| `anchor` | [View](../android.view/View.md)!:Anchor view for this popup. The popup will appear below the anchor if there is room, or above it if there is not. |

### PopupMenu

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PopupMenu(
    context: Context!, 
    anchor: View!, 
    gravity: Int)
```

Constructor to create a new popup menu with an anchor view and alignment gravity.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android.content/Context.md)!:Context the popup menu is running in, through which it can access the current theme, resources, etc. |
| `anchor` | [View](../android.view/View.md)!:Anchor view for this popup. The popup will appear below the anchor if there is room, or above it if there is not. |
| `gravity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The [Gravity](../android.view/Gravity.md) value for aligning the popup with its anchor. |
| --- | --- |

### PopupMenu

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PopupMenu(
    context: Context!, 
    anchor: View!, 
    gravity: Int, 
    popupStyleAttr: Int, 
    popupStyleRes: Int)
```

Constructor a create a new popup menu with a specific style.

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android.content/Context.md)!:Context the popup menu is running in, through which it can access the current theme, resources, etc. |
| `anchor` | [View](../android.view/View.md)!:Anchor view for this popup. The popup will appear below the anchor if there is room, or above it if there is not. |
| `gravity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The [Gravity](../android.view/Gravity.md) value for aligning the popup with its anchor. |
| --- | --- |
| `popupStyleAttr` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):An attribute in the current theme that contains a reference to a style resource that supplies default values for the popup window. Can be 0 to not look for defaults. |
| `popupStyleRes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A resource identifier of a style resource that supplies default values for the popup window, used only if popupStyleAttr is 0 or can not be found in the theme. Can be 0 to not look for defaults. |

## Public methods

### dismiss

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dismiss(): Unit
```

Dismiss the menu popup. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/widget/PopupMenu#show()> 

### getDragToOpenListener

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDragToOpenListener(): View.OnTouchListener!
```

Returns an [OnTouchListener](../android/view/View.OnTouchListener.md) that can be added to the anchor view to implement drag-to-open behavior.

When the listener is set on a view, touching that view and dragging outside of its bounds will open the popup window. Lifting will select the currently touched list item.

Example usage: 

```kotlin
PopupMenu myPopup = new PopupMenu(context, myAnchor);
  myAnchor.setOnTouchListener(myPopup.getDragToOpenListener());
  
```

| Return ||
|-----------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| [View.OnTouchListener](../android/view/View.OnTouchListener.md)! | a touch listener that controls drag-to-open behavior |

### getGravity

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getGravity(): Int
```

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the gravity used to align the popup window to its anchor view |

**See Also**

- [#setGravity(int)](PopupMenu.md)) 

### getMenu

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMenu(): Menu!
```

Returns the [Menu](../android.view/Menu.md) associated with this popup. Populate the returned Menu with items before calling [show()](PopupMenu.md)).

| Return ||
|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [Menu](../android.view/Menu.md)! | the [Menu](../android.view/Menu.md) associated with this popup |

**See Also**

- <https://developer.android.com/reference/kotlin/android/widget/PopupMenu#show()>
- <https://developer.android.com/reference/kotlin/android/widget/PopupMenu#getMenuInflater()> 

### getMenuInflater

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMenuInflater(): MenuInflater!
```

| Return ||
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MenuInflater](../android.view/MenuInflater.md)! | a [MenuInflater](../android.view/MenuInflater.md) that can be used to inflate menu items from XML into the menu returned by [getMenu()](PopupMenu.md)) |

**See Also**

- <https://developer.android.com/reference/kotlin/android/widget/PopupMenu#getMenu()> 

### inflate

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun inflate(menuRes: Int): Unit
```

Inflate a menu resource into this PopupMenu. This is equivalent to calling`popupMenu.getMenuInflater().inflate(menuRes, popupMenu.getMenu())`.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------|
| `menuRes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Menu resource to inflate |

### setForceShowIcon

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setForceShowIcon(forceShowIcon: Boolean): Unit
```

Sets whether the popup menu's adapter is forced to show icons in the menu item views.

Changes take effect on the next call to show().

| Parameters ||
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `forceShowIcon` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`to force icons to be shown, or`false`for icons to be optionally shown |

### setGravity

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setGravity(gravity: Int): Unit
```

Sets the gravity used to align the popup window to its anchor view.

If the popup is showing, calling this method will take effect only the next time the popup is shown.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------|
| `gravity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the gravity used to align the popup window |

**See Also**

- <https://developer.android.com/reference/kotlin/android/widget/PopupMenu#getGravity()> 

### setOnDismissListener

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOnDismissListener(listener: PopupMenu.OnDismissListener!): Unit
```

Sets a listener that will be notified when this menu is dismissed.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [PopupMenu.OnDismissListener](../android/widget/PopupMenu.OnDismissListener.md)!:the listener to notify |

### setOnMenuItemClickListener

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOnMenuItemClickListener(listener: PopupMenu.OnMenuItemClickListener!): Unit
```

Sets a listener that will be notified when the user selects an item from the menu.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [PopupMenu.OnMenuItemClickListener](../android/widget/PopupMenu.OnMenuItemClickListener.md)!:the listener to notify |

### show

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun show(): Unit
```

Show the menu popup anchored to the view specified during construction. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/widget/PopupMenu#dismiss()>
