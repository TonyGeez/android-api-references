# ListPopupWindow

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ListPopupWindow

Kotlin| [Java](../android/widget/ListPopupWindow.md) 
| --- | --- |

```
open class ListPopupWindow
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.widget.ListPopupWindow](../android/widget/ListPopupWindow.md) |

A ListPopupWindow anchors itself to a host view and displays a list of choices.

ListPopupWindow contains a number of tricky behaviors surrounding positioning, scrolling parents to fit the dropdown, interacting sanely with the IME if present, and others.

## Summary

| XML attributes ||
|------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [`android:dropDownHorizontalOffset`](../android/widget/ListPopupWindow.md) | Amount of pixels by which the drop down should be offset horizontally. |
| [`android:dropDownVerticalOffset`](../android/widget/ListPopupWindow.md) | Amount of pixels by which the drop down should be offset vertically. |

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INPUT_METHOD_FROM_FOCUSABLE](../android/widget/ListPopupWindow.md) Mode for [setInputMethodMode(int)](../android/widget/ListPopupWindow.md)): the requirements for the input method should be based on the focusability of the popup. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INPUT_METHOD_NEEDED](../android/widget/ListPopupWindow.md) Mode for [setInputMethodMode(int)](../android/widget/ListPopupWindow.md)): this popup always needs to work with an input method, regardless of whether it is focusable. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INPUT_METHOD_NOT_NEEDED](../android/widget/ListPopupWindow.md) Mode for [setInputMethodMode(int)](../android/widget/ListPopupWindow.md)): this popup never needs to work with an input method, regardless of whether it is focusable. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MATCH_PARENT](../android/widget/ListPopupWindow.md) Alias for [ViewGroup.LayoutParams.MATCH_PARENT](../android/view/ViewGroup.LayoutParams.md). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [POSITION_PROMPT_ABOVE](../android/widget/ListPopupWindow.md) The provided prompt view should appear above list content. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [POSITION_PROMPT_BELOW](../android/widget/ListPopupWindow.md) The provided prompt view should appear below list content. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WRAP_CONTENT](../android/widget/ListPopupWindow.md) Alias for [ViewGroup.LayoutParams.WRAP_CONTENT](../android/view/ViewGroup.LayoutParams.md). |

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ListPopupWindow](../android/widget/ListPopupWindow.md))`(`context:` ` [Context](../android/content/Context.md)`)` Create a new, empty popup window capable of displaying items from a ListAdapter. |
| [ListPopupWindow](../android/widget/ListPopupWindow.md))`(`context:` ` [Context](../android/content/Context.md)`, `attrs:` ` [AttributeSet](../android/util/AttributeSet.md)?`)` Create a new, empty popup window capable of displaying items from a ListAdapter. |
| [ListPopupWindow](../android/widget/ListPopupWindow.md))`(`context:` ` [Context](../android/content/Context.md)`, `attrs:` ` [AttributeSet](../android/util/AttributeSet.md)?`, `defStyleAttr:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create a new, empty popup window capable of displaying items from a ListAdapter. |
| [ListPopupWindow](../android/widget/ListPopupWindow.md))`(`context:` ` [Context](../android/content/Context.md)`, `attrs:` ` [AttributeSet](../android/util/AttributeSet.md)?`, `defStyleAttr:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `defStyleRes:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create a new, empty popup window capable of displaying items from a ListAdapter. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearListSelection](../android/widget/ListPopupWindow.md))`()` Clear any current list selection. |
| open [View.OnTouchListener](../android/view/View.OnTouchListener.md)! | [createDragToOpenListener](../android/widget/ListPopupWindow.md))`(`src:` ` [View](../android/view/View.md)!`)` Returns an [OnTouchListener](../android/view/View.OnTouchListener.md) that can be added to the source view to implement drag-to-open behavior. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dismiss](../android/widget/ListPopupWindow.md))`()` Dismiss the popup window. |
| --- | --- |
| open [View](../android/view/View.md)? | [getAnchorView](../android/widget/ListPopupWindow.md))`()` Returns the view that will be used to anchor this popup. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAnimationStyle](../android/widget/ListPopupWindow.md))`()` Returns the animation style that will be used when the popup window is shown or dismissed. |
| open [Drawable](../android/graphics/drawable/Drawable.md)? | [getBackground](../android/widget/ListPopupWindow.md))`()` <br /> |
| --- | --- |
| open [Rect](../android/graphics/Rect.md)? | [getEpicenterBounds](../android/widget/ListPopupWindow.md))`()` Returns bounds which are used as a popup's epicenter of the enter and exit transitions. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getHeight](../android/widget/ListPopupWindow.md))`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getHorizontalOffset](../android/widget/ListPopupWindow.md))`()` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getInputMethodMode](../android/widget/ListPopupWindow.md))`()` Return the current value in [setInputMethodMode(int)](../android/widget/ListPopupWindow.md)). |
| open [ListView](../android/widget/ListView.md)? | [getListView](../android/widget/ListPopupWindow.md))`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPromptPosition](../android/widget/ListPopupWindow.md))`()` <br /> |
| --- | --- |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)? | [getSelectedItem](../android/widget/ListPopupWindow.md))`()` <br /> |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getSelectedItemId](../android/widget/ListPopupWindow.md))`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSelectedItemPosition](../android/widget/ListPopupWindow.md))`()` <br /> |
| --- | --- |
| open [View](../android/view/View.md)? | [getSelectedView](../android/widget/ListPopupWindow.md))`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSoftInputMode](../android/widget/ListPopupWindow.md))`()` Returns the current value in [setSoftInputMode(int)](../android/widget/ListPopupWindow.md)). |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVerticalOffset](../android/widget/ListPopupWindow.md))`()` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getWidth](../android/widget/ListPopupWindow.md))`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isInputMethodNotNeeded](../android/widget/ListPopupWindow.md))`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isModal](../android/widget/ListPopupWindow.md))`()` Returns whether the popup window will be modal when shown. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isShowing](../android/widget/ListPopupWindow.md))`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onKeyDown](../android/widget/ListPopupWindow.md))`(`keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](../android/view/KeyEvent.md)`)` Filter key down events. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onKeyPreIme](../android/widget/ListPopupWindow.md))`(`keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](../android/view/KeyEvent.md)`)` Filter pre-IME key events. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onKeyUp](../android/widget/ListPopupWindow.md))`(`keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](../android/view/KeyEvent.md)`)` Filter key up events. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [performItemClick](../android/widget/ListPopupWindow.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Perform an item click operation on the specified list adapter position. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [postShow](../android/widget/ListPopupWindow.md))`()` Post a [show()](../android/widget/ListPopupWindow.md))call to the UI thread. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAdapter](../android/widget/ListPopupWindow.md))`(`adapter:` ` [ListAdapter](../android/widget/ListAdapter.md)?`)` Sets the adapter that provides the data and the views to represent the data in this popup window. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAnchorView](../android/widget/ListPopupWindow.md))`(`anchor:` ` [View](../android/view/View.md)?`)` Sets the popup's anchor view. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAnimationStyle](../android/widget/ListPopupWindow.md))`(`animationStyle:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set an animation style to use when the popup window is shown or dismissed. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBackgroundDrawable](../android/widget/ListPopupWindow.md))`(`d:` ` [Drawable](../android/graphics/drawable/Drawable.md)?`)` Sets a drawable to be the background for the popup window. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setContentWidth](../android/widget/ListPopupWindow.md))`(`width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the width of the popup window by the size of its content. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDropDownGravity](../android/widget/ListPopupWindow.md))`(`gravity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the gravity of the dropdown list. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEpicenterBounds](../android/widget/ListPopupWindow.md))`(`bounds:` ` [Rect](../android/graphics/Rect.md)?`)` Specifies the anchor-relative bounds of the popup's transition epicenter. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setHeight](../android/widget/ListPopupWindow.md))`(`height:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the height of the popup window in pixels. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setHorizontalOffset](../android/widget/ListPopupWindow.md))`(`offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the horizontal offset of this popup from its anchor view in pixels. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInputMethodMode](../android/widget/ListPopupWindow.md))`(`mode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Control how the popup operates with an input method: one of [INPUT_METHOD_FROM_FOCUSABLE](../android/widget/ListPopupWindow.md), [INPUT_METHOD_NEEDED](../android/widget/ListPopupWindow.md), or [INPUT_METHOD_NOT_NEEDED](../android/widget/ListPopupWindow.md). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setListSelector](../android/widget/ListPopupWindow.md))`(`selector:` ` [Drawable](../android/graphics/drawable/Drawable.md)!`)` Sets a drawable to use as the list item selector. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setModal](../android/widget/ListPopupWindow.md))`(`modal:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Set whether this window should be modal when shown. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnDismissListener](../android/widget/ListPopupWindow.md))`(`listener:` ` [PopupWindow.OnDismissListener](../android/widget/PopupWindow.OnDismissListener.md)?`)` Set a listener to receive a callback when the popup is dismissed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnItemClickListener](../android/widget/ListPopupWindow.md))`(`clickListener:` ` [AdapterView.OnItemClickListener](../android/widget/AdapterView.OnItemClickListener.md)?`)` Sets a listener to receive events when a list item is clicked. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnItemSelectedListener](../android/widget/ListPopupWindow.md))`(`selectedListener:` ` [AdapterView.OnItemSelectedListener](../android/widget/AdapterView.OnItemSelectedListener.md)?`)` Sets a listener to receive events when a list item is selected. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPromptPosition](../android/widget/ListPopupWindow.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set where the optional prompt view should appear. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPromptView](../android/widget/ListPopupWindow.md))`(`prompt:` ` [View](../android/view/View.md)?`)` Set a view to act as a user prompt for this popup window. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSelection](../android/widget/ListPopupWindow.md))`(`position:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the selected position of the list. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSoftInputMode](../android/widget/ListPopupWindow.md))`(`mode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the operating mode for the soft input area. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setVerticalOffset](../android/widget/ListPopupWindow.md))`(`offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the vertical offset of this popup from its anchor view in pixels. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setWidth](../android/widget/ListPopupWindow.md))`(`width:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the width of the popup window in pixels. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setWindowLayoutType](../android/widget/ListPopupWindow.md))`(`layoutType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the layout type for this popup window. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [show](../android/widget/ListPopupWindow.md))`()` Show the popup list. |

## XML attributes

### android:dropDownHorizontalOffset

```
android:dropDownHorizontalOffset
```
Amount of pixels by which the drop down should be offset horizontally.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters). 

### android:dropDownVerticalOffset

```
android:dropDownVerticalOffset
```
Amount of pixels by which the drop down should be offset vertically.

May be a dimension value, which is a floating point number appended with a unit such as "`14.5sp`". Available units are: px (pixels), dp (density-independent pixels), sp (scaled pixels based on preferred font size), in (inches), and mm (millimeters).

## Constants

### INPUT_METHOD_FROM_FOCUSABLE

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INPUT_METHOD_FROM_FOCUSABLE: Int
```

Mode for [setInputMethodMode(int)](../android/widget/ListPopupWindow.md)): the requirements for the input method should be based on the focusability of the popup. That is if it is focusable than it needs to work with the input method, else it doesn't. 

 Value: 0

### INPUT_METHOD_NEEDED

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INPUT_METHOD_NEEDED: Int
```

Mode for [setInputMethodMode(int)](../android/widget/ListPopupWindow.md)): this popup always needs to work with an input method, regardless of whether it is focusable. This means that it will always be displayed so that the user can also operate the input method while it is shown. 

 Value: 1

### INPUT_METHOD_NOT_NEEDED

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INPUT_METHOD_NOT_NEEDED: Int
```

Mode for [setInputMethodMode(int)](../android/widget/ListPopupWindow.md)): this popup never needs to work with an input method, regardless of whether it is focusable. This means that it will always be displayed to use as much space on the screen as needed, regardless of whether this covers the input method. 

 Value: 2

### MATCH_PARENT

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MATCH_PARENT: Int
```

Alias for [ViewGroup.LayoutParams.MATCH_PARENT](../android/view/ViewGroup.LayoutParams.md). If used to specify a popup width, the popup will match the width of the anchor view. If used to specify a popup height, the popup will fill available space. 

 Value: -1

### POSITION_PROMPT_ABOVE

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val POSITION_PROMPT_ABOVE: Int
```

The provided prompt view should appear above list content. 

 Value: 0

**See Also**

- [#setPromptPosition(int)](../android/widget/ListPopupWindow.md))
- <https://developer.android.com/reference/kotlin/android/widget/ListPopupWindow#getPromptPosition()>
- [#setPromptView(View)](../android/widget/ListPopupWindow.md)) 

### POSITION_PROMPT_BELOW

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val POSITION_PROMPT_BELOW: Int
```

The provided prompt view should appear below list content. 

 Value: 1

**See Also**

- [#setPromptPosition(int)](../android/widget/ListPopupWindow.md))
- <https://developer.android.com/reference/kotlin/android/widget/ListPopupWindow#getPromptPosition()>
- [#setPromptView(View)](../android/widget/ListPopupWindow.md)) 

### WRAP_CONTENT

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WRAP_CONTENT: Int
```

Alias for [ViewGroup.LayoutParams.WRAP_CONTENT](../android/view/ViewGroup.LayoutParams.md). If used to specify a popup width, the popup will use the width of its content. 

 Value: -2

## Public constructors

### ListPopupWindow

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ListPopupWindow(context: Context)
```

Create a new, empty popup window capable of displaying items from a ListAdapter. Backgrounds should be set using [setBackgroundDrawable(android.graphics.drawable.Drawable)](../android/widget/ListPopupWindow.md)).

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md):Context used for contained views. This value cannot be`null`. |

### ListPopupWindow

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ListPopupWindow(
    context: Context, 
    attrs: AttributeSet?)
```

Create a new, empty popup window capable of displaying items from a ListAdapter. Backgrounds should be set using [setBackgroundDrawable(android.graphics.drawable.Drawable)](../android/widget/ListPopupWindow.md)).

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md):Context used for contained views. This value cannot be`null`. |
| `attrs` | [AttributeSet](../android/util/AttributeSet.md)?:Attributes from inflating parent views used to style the popup. This value may be`null`. |

### ListPopupWindow

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ListPopupWindow(
    context: Context, 
    attrs: AttributeSet?, 
    defStyleAttr: Int)
```

Create a new, empty popup window capable of displaying items from a ListAdapter. Backgrounds should be set using [setBackgroundDrawable(android.graphics.drawable.Drawable)](../android/widget/ListPopupWindow.md)).

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md):Context used for contained views. This value cannot be`null`. |
| `attrs` | [AttributeSet](../android/util/AttributeSet.md)?:Attributes from inflating parent views used to style the popup. This value may be`null`. |
| `defStyleAttr` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Default style attribute to use for popup content. |
| --- | --- |

### ListPopupWindow

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ListPopupWindow(
    context: Context, 
    attrs: AttributeSet?, 
    defStyleAttr: Int, 
    defStyleRes: Int)
```

Create a new, empty popup window capable of displaying items from a ListAdapter. Backgrounds should be set using [setBackgroundDrawable(android.graphics.drawable.Drawable)](../android/widget/ListPopupWindow.md)).

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md):Context used for contained views. This value cannot be`null`. |
| `attrs` | [AttributeSet](../android/util/AttributeSet.md)?:Attributes from inflating parent views used to style the popup. This value may be`null`. |
| `defStyleAttr` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Style attribute to read for default styling of popup content. |
| --- | --- |
| `defStyleRes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Style resource ID to use for default styling of popup content. |

## Public methods

### clearListSelection

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clearListSelection(): Unit
```

Clear any current list selection. Only valid when [isShowing()](../android/widget/ListPopupWindow.md))==`true`. 

### createDragToOpenListener

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun createDragToOpenListener(src: View!): View.OnTouchListener!
```

Returns an [OnTouchListener](../android/view/View.OnTouchListener.md) that can be added to the source view to implement drag-to-open behavior. Generally, the source view should be the same view that was passed to [setAnchorView](../android/widget/ListPopupWindow.md)).

When the listener is set on a view, touching that view and dragging outside of its bounds will open the popup window. Lifting will select the currently touched list item.

Example usage: 

```kotlin
ListPopupWindow myPopup = new ListPopupWindow(context);
  myPopup.setAnchor(myAnchor);
  OnTouchListener dragListener = myPopup.createDragToOpenListener(myAnchor);
  myAnchor.setOnTouchListener(dragListener);
  
```

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------------------|
| `src` | [View](../android/view/View.md)!:the view on which the resulting listener will be set |

| Return ||
|-----------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| [View.OnTouchListener](../android/view/View.OnTouchListener.md)! | a touch listener that controls drag-to-open behavior |

### dismiss

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dismiss(): Unit
```

Dismiss the popup window. 

### getAnchorView

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAnchorView(): View?
```

Returns the view that will be used to anchor this popup.

| Return ||
|---------------------------------------------------------------------------------|--------------------------------------------------|
| [View](../android/view/View.md)? | The popup's anchor view This value may be`null`. |

### getAnimationStyle

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAnimationStyle(): Int
```

Returns the animation style that will be used when the popup window is shown or dismissed.

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Animation style that will be used. |

### getBackground

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getBackground(): Drawable?
```

| Return ||
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Drawable](../android/graphics/drawable/Drawable.md)? | The background drawable for the popup window. This value may be`null`. |

### getEpicenterBounds

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEpicenterBounds(): Rect?
```

Returns bounds which are used as a popup's epicenter of the enter and exit transitions.

| Return ||
|-------------------------------------------------------------------------------------|----------------------------------------------------|
| [Rect](../android/graphics/Rect.md)? | bounds relative to anchor view, or`null`if not set |

**See Also**

- [#setEpicenterBounds(Rect)](../android/widget/ListPopupWindow.md)) 

### getHeight

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getHeight(): Int
```

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The height of the popup window in pixels. |

### getHorizontalOffset

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getHorizontalOffset(): Int
```

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The horizontal offset of the popup from its anchor in pixels. |

### getInputMethodMode

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getInputMethodMode(): Int
```

Return the current value in [setInputMethodMode(int)](../android/widget/ListPopupWindow.md)). 
**See Also**

- [#setInputMethodMode(int)](../android/widget/ListPopupWindow.md)) 

### getListView

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getListView(): ListView?
```

| Return ||
|-------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ListView](../android/widget/ListView.md)? | The [ListView](../android/widget/ListView.md) displayed within the popup window. Only valid when [isShowing()](../android/widget/ListPopupWindow.md))==`true`. This value may be`null`. |

### getPromptPosition

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPromptPosition(): Int
```

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Where the optional prompt view should appear. |

**See Also**

- [#POSITION_PROMPT_ABOVE](../android/widget/ListPopupWindow.md)
- [#POSITION_PROMPT_BELOW](../android/widget/ListPopupWindow.md) 

### getSelectedItem

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSelectedItem(): Any?
```

| Return ||
|-----------------------------------------------------------------------------|------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)? | The currently selected item or null if the popup is not showing. |

### getSelectedItemId

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSelectedItemId(): Long
```

| Return ||
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The ID of the currently selected item or [ListView.INVALID_ROW_ID](../android/widget/AdapterView.md) if [isShowing()](../android/widget/ListPopupWindow.md))==`false`. |

**See Also**

- [android.widget.ListView#getSelectedItemId()](../android/widget/AdapterView.md)) 

### getSelectedItemPosition

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSelectedItemPosition(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The position of the currently selected item or [ListView.INVALID_POSITION](../android/widget/AdapterView.md) if [isShowing()](../android/widget/ListPopupWindow.md))==`false`. |

**See Also**

- [android.widget.ListView#getSelectedItemPosition()](../android/widget/AdapterView.md)) 

### getSelectedView

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSelectedView(): View?
```

| Return ||
|---------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [View](../android/view/View.md)? | The View for the currently selected item or null if [isShowing()](../android/widget/ListPopupWindow.md))==`false`. |

**See Also**

- [android.widget.ListView#getSelectedView()](../android/widget/AbsListView.md)) 

### getSoftInputMode

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSoftInputMode(): Int
```

Returns the current value in [setSoftInputMode(int)](../android/widget/ListPopupWindow.md)). 
**See Also**

- [#setSoftInputMode(int)](../android/widget/ListPopupWindow.md))
- [android.view.WindowManager.LayoutParams#softInputMode](../android/view/WindowManager.LayoutParams.md) 

### getVerticalOffset

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getVerticalOffset(): Int
```

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The vertical offset of the popup from its anchor in pixels. |

### getWidth

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getWidth(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The width of the popup window in pixels. |

### isInputMethodNotNeeded

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isInputMethodNotNeeded(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this popup is configured to assume the user does not need to interact with the IME while it is showing,`false`otherwise. |

### isModal

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isModal(): Boolean
```

Returns whether the popup window will be modal when shown.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the popup window will be modal,`false`otherwise. |

### isShowing

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isShowing(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the popup is currently showing,`false`otherwise. |

### onKeyDown

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onKeyDown(
    keyCode: Int, 
    event: KeyEvent
): Boolean
```

Filter key down events. By forwarding key down events to this function, views using non-modal ListPopupWindow can have it handle key selection of items.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `keyCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):keyCode param passed to the host view's onKeyDown |
| `event` | [KeyEvent](../android/view/KeyEvent.md):event param passed to the host view's onKeyDown This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the event was handled, false if it was ignored. |

**See Also**

- [#setModal(boolean)](../android/widget/ListPopupWindow.md))
- [#onKeyUp(int, KeyEvent)](../android/widget/ListPopupWindow.md)) 

### onKeyPreIme

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onKeyPreIme(
    keyCode: Int, 
    event: KeyEvent
): Boolean
```

Filter pre-IME key events. By forwarding [View.onKeyPreIme(int, KeyEvent)](../android/view/View.md))events to this function, views using ListPopupWindow can have it dismiss the popup when the back key is pressed.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `keyCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):keyCode param passed to the host view's onKeyPreIme |
| `event` | [KeyEvent](../android/view/KeyEvent.md):event param passed to the host view's onKeyPreIme This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the event was handled, false if it was ignored. |

**See Also**

- [#setModal(boolean)](../android/widget/ListPopupWindow.md)) 

### onKeyUp

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onKeyUp(
    keyCode: Int, 
    event: KeyEvent
): Boolean
```

Filter key up events. By forwarding key up events to this function, views using non-modal ListPopupWindow can have it handle key selection of items.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `keyCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):keyCode param passed to the host view's onKeyUp |
| `event` | [KeyEvent](../android/view/KeyEvent.md):event param passed to the host view's onKeyUp This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the event was handled, false if it was ignored. |

**See Also**

- [#setModal(boolean)](../android/widget/ListPopupWindow.md))
- [#onKeyDown(int, KeyEvent)](../android/widget/ListPopupWindow.md)) 

### performItemClick

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun performItemClick(position: Int): Boolean
```

Perform an item click operation on the specified list adapter position.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------|
| `position` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Adapter position for performing the click |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the click action could be performed, false if not. (e.g. if the popup was not showing, this method would return false.) |

### postShow

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun postShow(): Unit
```

Post a [show()](../android/widget/ListPopupWindow.md))call to the UI thread. 

### setAdapter

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setAdapter(adapter: ListAdapter?): Unit
```

Sets the adapter that provides the data and the views to represent the data in this popup window.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `adapter` | [ListAdapter](../android/widget/ListAdapter.md)?:The adapter to use to create this window's content. This value may be`null`. |

### setAnchorView

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setAnchorView(anchor: View?): Unit
```

Sets the popup's anchor view. This popup will always be positioned relative to the anchor view when shown.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------|
| `anchor` | [View](../android/view/View.md)?:The view to use as an anchor. This value may be`null`. |

### setAnimationStyle

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setAnimationStyle(animationStyle: Int): Unit
```

Set an animation style to use when the popup window is shown or dismissed.

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------|
| `animationStyle` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Animation style to use. |

### setBackgroundDrawable

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setBackgroundDrawable(d: Drawable?): Unit
```

Sets a drawable to be the background for the popup window.

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `d` | [Drawable](../android/graphics/drawable/Drawable.md)?:A drawable to set as the background. This value may be`null`. |

### setContentWidth

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setContentWidth(width: Int): Unit
```

Sets the width of the popup window by the size of its content. The final width may be larger to accommodate styled window dressing.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------|
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Desired width of content in pixels. |

### setDropDownGravity

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDropDownGravity(gravity: Int): Unit
```

Set the gravity of the dropdown list. This is commonly used to set gravity to START or END for alignment with the anchor.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------|
| `gravity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Gravity value to use |

### setEpicenterBounds

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setEpicenterBounds(bounds: Rect?): Unit
```

Specifies the anchor-relative bounds of the popup's transition epicenter.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `bounds` | [Rect](../android/graphics/Rect.md)?:anchor-relative bounds, or`null`to use default epicenter |

**See Also**

- <https://developer.android.com/reference/kotlin/android/widget/ListPopupWindow#getEpicenterBounds()> 

### setHeight

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setHeight(height: Int): Unit
```

Sets the height of the popup window in pixels. Can also be [MATCH_PARENT](../android/widget/ListPopupWindow.md).

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Height of the popup window must be a positive value, [MATCH_PARENT](../android/widget/ListPopupWindow.md), or [WRAP_CONTENT](../android/widget/ListPopupWindow.md). |

| Exceptions ||
|--------------------------------------|------------------------------------|
| `java.lang.IllegalArgumentException` | if height is set to negative value |

### setHorizontalOffset

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setHorizontalOffset(offset: Int): Unit
```

Set the horizontal offset of this popup from its anchor view in pixels.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------|
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The horizontal offset of the popup from its anchor. |

### setInputMethodMode

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setInputMethodMode(mode: Int): Unit
```

Control how the popup operates with an input method: one of [INPUT_METHOD_FROM_FOCUSABLE](../android/widget/ListPopupWindow.md), [INPUT_METHOD_NEEDED](../android/widget/ListPopupWindow.md), or [INPUT_METHOD_NOT_NEEDED](../android/widget/ListPopupWindow.md).

If the popup is showing, calling this method will take effect only the next time the popup is shown or through a manual call to the [show()](../android/widget/ListPopupWindow.md))method. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/widget/ListPopupWindow#getInputMethodMode()>
- <https://developer.android.com/reference/kotlin/android/widget/ListPopupWindow#show()> 

### setListSelector

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setListSelector(selector: Drawable!): Unit
```

Sets a drawable to use as the list item selector.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `selector` | [Drawable](../android/graphics/drawable/Drawable.md)!:List selector drawable to use in the popup. |

### setModal

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setModal(modal: Boolean): Unit
```

Set whether this window should be modal when shown.

If a popup window is modal, it will receive all touch and key input. If the user touches outside the popup window's content area the popup window will be dismissed.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `modal` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`if the popup window should be modal,`false`otherwise. |

### setOnDismissListener

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOnDismissListener(listener: PopupWindow.OnDismissListener?): Unit
```

Set a listener to receive a callback when the popup is dismissed.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [PopupWindow.OnDismissListener](../android/widget/PopupWindow.OnDismissListener.md)?:Listener that will be notified when the popup is dismissed. This value may be`null`. |

### setOnItemClickListener

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOnItemClickListener(clickListener: AdapterView.OnItemClickListener?): Unit
```

Sets a listener to receive events when a list item is clicked.

| Parameters ||
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `clickListener` | [AdapterView.OnItemClickListener](../android/widget/AdapterView.OnItemClickListener.md)?:Listener to register This value may be`null`. |

**See Also**

- [android.widget.ListView#setOnItemClickListener(android.widget.AdapterView.OnItemClickListener)](../android/widget/AdapterView.md)) 

### setOnItemSelectedListener

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOnItemSelectedListener(selectedListener: AdapterView.OnItemSelectedListener?): Unit
```

Sets a listener to receive events when a list item is selected.

| Parameters ||
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `selectedListener` | [AdapterView.OnItemSelectedListener](../android/widget/AdapterView.OnItemSelectedListener.md)?:Listener to register. This value may be`null`. |

**See Also**

- [android.widget.ListView#setOnItemSelectedListener(OnItemSelectedListener)](../android/widget/AdapterView.md)) 

### setPromptPosition

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPromptPosition(position: Int): Unit
```

Set where the optional prompt view should appear. The default is [POSITION_PROMPT_ABOVE](../android/widget/ListPopupWindow.md).

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `position` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A position constant declaring where the prompt should be displayed. |

**See Also**

- [#POSITION_PROMPT_ABOVE](../android/widget/ListPopupWindow.md)
- [#POSITION_PROMPT_BELOW](../android/widget/ListPopupWindow.md) 

### setPromptView

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPromptView(prompt: View?): Unit
```

Set a view to act as a user prompt for this popup window. Where the prompt view will appear is controlled by [setPromptPosition(int)](../android/widget/ListPopupWindow.md)).

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `prompt` | [View](../android/view/View.md)?:View to use as an informational prompt. This value may be`null`. |

### setSelection

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSelection(position: Int): Unit
```

Set the selected position of the list. Only valid when [isShowing()](../android/widget/ListPopupWindow.md))==`true`.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------|
| `position` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):List position to set as selected. |

### setSoftInputMode

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setSoftInputMode(mode: Int): Unit
```

Sets the operating mode for the soft input area.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The desired mode, see [android.view.WindowManager.LayoutParams#softInputMode](../android/view/WindowManager.LayoutParams.md) for the full list |

**See Also**

- [android.view.WindowManager.LayoutParams#softInputMode](../android/view/WindowManager.LayoutParams.md)
- <https://developer.android.com/reference/kotlin/android/widget/ListPopupWindow#getSoftInputMode()> 

### setVerticalOffset

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setVerticalOffset(offset: Int): Unit
```

Set the vertical offset of this popup from its anchor view in pixels.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------|
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The vertical offset of the popup from its anchor. |

### setWidth

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setWidth(width: Int): Unit
```

Sets the width of the popup window in pixels. Can also be [MATCH_PARENT](../android/widget/ListPopupWindow.md) or [WRAP_CONTENT](../android/widget/ListPopupWindow.md).

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------|
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Width of the popup window. |

### setWindowLayoutType

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setWindowLayoutType(layoutType: Int): Unit
```

Set the layout type for this popup window.

See [WindowManager.LayoutParams.type](../android/view/WindowManager.LayoutParams.md) for possible values.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------|
| `layoutType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Layout type for this window. |

**See Also**

- [android.view.WindowManager.LayoutParams#type](../android/view/WindowManager.LayoutParams.md) 

### show

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun show(): Unit
```

Show the popup list. If the list is already showing, this method will recalculate the popup's size and position.
