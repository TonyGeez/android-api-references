# PopupMenu

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PopupMenu

Kotlin| [Java](https://developer.android.com/reference/android/widget/PopupMenu "View this page in Java") 
| --- | --- |

```
open class PopupMenu
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.widget.PopupMenu](https://developer.android.com/reference/kotlin/android/widget/PopupMenu#) |

A PopupMenu displays a [Menu](https://developer.android.com/reference/kotlin/android/view/Menu.html#) in a modal popup window anchored to a [View](https://developer.android.com/reference/kotlin/android/view/View.html#). The popup will appear below the anchor view if there is room, or above it if there is not. If the IME is visible the popup will not overlap it until it is touched. Touching outside of the popup will dismiss it.

## Summary

| Nested classes ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [OnDismissListener](https://developer.android.com/reference/kotlin/android/widget/PopupMenu.OnDismissListener) Callback interface used to notify the application that the menu has closed. |
| abstract | [OnMenuItemClickListener](https://developer.android.com/reference/kotlin/android/widget/PopupMenu.OnMenuItemClickListener) Interface responsible for receiving menu item click events if the items themselves do not have individual item click listeners. |

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PopupMenu](https://developer.android.com/reference/kotlin/android/widget/PopupMenu#PopupMenu(android.content.Context,%20android.view.View))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `anchor:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`)` Constructor to create a new popup menu with an anchor view. |
| [PopupMenu](https://developer.android.com/reference/kotlin/android/widget/PopupMenu#PopupMenu(android.content.Context,%20android.view.View,%20kotlin.Int))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `anchor:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `gravity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructor to create a new popup menu with an anchor view and alignment gravity. |
| [PopupMenu](https://developer.android.com/reference/kotlin/android/widget/PopupMenu#PopupMenu(android.content.Context,%20android.view.View,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `anchor:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `gravity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `popupStyleAttr:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `popupStyleRes:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructor a create a new popup menu with a specific style. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dismiss](https://developer.android.com/reference/kotlin/android/widget/PopupMenu#dismiss())`()` Dismiss the menu popup. |
| open [View.OnTouchListener](https://developer.android.com/reference/kotlin/android/view/View.OnTouchListener.html#)! | [getDragToOpenListener](https://developer.android.com/reference/kotlin/android/widget/PopupMenu#getDragToOpenListener())`()` Returns an [OnTouchListener](https://developer.android.com/reference/kotlin/android/view/View.OnTouchListener.html#) that can be added to the anchor view to implement drag-to-open behavior. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGravity](https://developer.android.com/reference/kotlin/android/widget/PopupMenu#getGravity())`()` <br /> |
| --- | --- |
| open [Menu](https://developer.android.com/reference/kotlin/android/view/Menu.html#)! | [getMenu](https://developer.android.com/reference/kotlin/android/widget/PopupMenu#getMenu())`()` Returns the [Menu](https://developer.android.com/reference/kotlin/android/view/Menu.html#) associated with this popup. |
| open [MenuInflater](https://developer.android.com/reference/kotlin/android/view/MenuInflater.html#)! | [getMenuInflater](https://developer.android.com/reference/kotlin/android/widget/PopupMenu#getMenuInflater())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [inflate](https://developer.android.com/reference/kotlin/android/widget/PopupMenu#inflate(kotlin.Int))`(`menuRes:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Inflate a menu resource into this PopupMenu. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setForceShowIcon](https://developer.android.com/reference/kotlin/android/widget/PopupMenu#setForceShowIcon(kotlin.Boolean))`(`forceShowIcon:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether the popup menu's adapter is forced to show icons in the menu item views. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setGravity](https://developer.android.com/reference/kotlin/android/widget/PopupMenu#setGravity(kotlin.Int))`(`gravity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the gravity used to align the popup window to its anchor view. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnDismissListener](https://developer.android.com/reference/kotlin/android/widget/PopupMenu#setOnDismissListener(android.widget.PopupMenu.OnDismissListener))`(`listener:` ` [PopupMenu.OnDismissListener](https://developer.android.com/reference/kotlin/android/widget/PopupMenu.OnDismissListener)!`)` Sets a listener that will be notified when this menu is dismissed. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnMenuItemClickListener](https://developer.android.com/reference/kotlin/android/widget/PopupMenu#setOnMenuItemClickListener(android.widget.PopupMenu.OnMenuItemClickListener))`(`listener:` ` [PopupMenu.OnMenuItemClickListener](https://developer.android.com/reference/kotlin/android/widget/PopupMenu.OnMenuItemClickListener)!`)` Sets a listener that will be notified when the user selects an item from the menu. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [show](https://developer.android.com/reference/kotlin/android/widget/PopupMenu#show())`()` Show the menu popup anchored to the view specified during construction. |

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
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:Context the popup menu is running in, through which it can access the current theme, resources, etc. |
| `anchor` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:Anchor view for this popup. The popup will appear below the anchor if there is room, or above it if there is not. |

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
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:Context the popup menu is running in, through which it can access the current theme, resources, etc. |
| `anchor` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:Anchor view for this popup. The popup will appear below the anchor if there is room, or above it if there is not. |
| `gravity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The [Gravity](https://developer.android.com/reference/kotlin/android/view/Gravity.html#) value for aligning the popup with its anchor. |
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
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:Context the popup menu is running in, through which it can access the current theme, resources, etc. |
| `anchor` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!:Anchor view for this popup. The popup will appear below the anchor if there is room, or above it if there is not. |
| `gravity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The [Gravity](https://developer.android.com/reference/kotlin/android/view/Gravity.html#) value for aligning the popup with its anchor. |
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

Returns an [OnTouchListener](https://developer.android.com/reference/kotlin/android/view/View.OnTouchListener.html#) that can be added to the anchor view to implement drag-to-open behavior.

When the listener is set on a view, touching that view and dragging outside of its bounds will open the popup window. Lifting will select the currently touched list item.

Example usage: 

```kotlin
PopupMenu myPopup = new PopupMenu(context, myAnchor);
  myAnchor.setOnTouchListener(myPopup.getDragToOpenListener());
  
```

| Return ||
|-----------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| [View.OnTouchListener](https://developer.android.com/reference/kotlin/android/view/View.OnTouchListener.html#)! | a touch listener that controls drag-to-open behavior |

### getGravity

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getGravity(): Int
```

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the gravity used to align the popup window to its anchor view |

**See Also**

- [#setGravity(int)](https://developer.android.com/reference/kotlin/android/widget/PopupMenu#setGravity(kotlin.Int)) 

### getMenu

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMenu(): Menu!
```

Returns the [Menu](https://developer.android.com/reference/kotlin/android/view/Menu.html#) associated with this popup. Populate the returned Menu with items before calling [show()](https://developer.android.com/reference/kotlin/android/widget/PopupMenu#show()).

| Return ||
|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [Menu](https://developer.android.com/reference/kotlin/android/view/Menu.html#)! | the [Menu](https://developer.android.com/reference/kotlin/android/view/Menu.html#) associated with this popup |

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
| [MenuInflater](https://developer.android.com/reference/kotlin/android/view/MenuInflater.html#)! | a [MenuInflater](https://developer.android.com/reference/kotlin/android/view/MenuInflater.html#) that can be used to inflate menu items from XML into the menu returned by [getMenu()](https://developer.android.com/reference/kotlin/android/widget/PopupMenu#getMenu()) |

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
| `listener` | [PopupMenu.OnDismissListener](https://developer.android.com/reference/kotlin/android/widget/PopupMenu.OnDismissListener)!:the listener to notify |

### setOnMenuItemClickListener

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOnMenuItemClickListener(listener: PopupMenu.OnMenuItemClickListener!): Unit
```

Sets a listener that will be notified when the user selects an item from the menu.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [PopupMenu.OnMenuItemClickListener](https://developer.android.com/reference/kotlin/android/widget/PopupMenu.OnMenuItemClickListener)!:the listener to notify |

### show

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun show(): Unit
```

Show the menu popup anchored to the view specified during construction. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/widget/PopupMenu#dismiss()>
