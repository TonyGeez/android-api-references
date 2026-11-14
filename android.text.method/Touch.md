# Touch

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Touch

Kotlin| [Java](https://developer.android.com/reference/android/text/method/Touch "View this page in Java") 
| --- | --- |

```
open class Touch
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.text.method.Touch](https://developer.android.com/reference/kotlin/android/text/method/Touch#) |

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getInitialScrollX](https://developer.android.com/reference/kotlin/android/text/method/Touch#getInitialScrollX(android.widget.TextView,%20android.text.Spannable))`(`widget:` ` [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!`, `buffer:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!`)` <br /> |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getInitialScrollY](https://developer.android.com/reference/kotlin/android/text/method/Touch#getInitialScrollY(android.widget.TextView,%20android.text.Spannable))`(`widget:` ` [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!`, `buffer:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!`)` <br /> |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onTouchEvent](https://developer.android.com/reference/kotlin/android/text/method/Touch#onTouchEvent(android.widget.TextView,%20android.text.Spannable,%20android.view.MotionEvent))`(`widget:` ` [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!`, `buffer:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!`, `event:` ` [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#)!`)` Handles touch events for dragging. |
| --- | --- |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [scrollTo](https://developer.android.com/reference/kotlin/android/text/method/Touch#scrollTo(android.widget.TextView,%20android.text.Layout,%20kotlin.Int,%20kotlin.Int))`(`widget:` ` [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!`, `layout:` ` [Layout](https://developer.android.com/reference/kotlin/android/text/Layout.html#)!`, `x:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `y:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Scrolls the specified widget to the specified coordinates, except constrains the X scrolling position to the horizontal regions of the text that will be visible after scrolling to the specified Y position. |

## Public methods

### getInitialScrollX

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInitialScrollX(
    widget: TextView!, 
    buffer: Spannable!
): Int
```

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------|
| `widget` | [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!:The text view. |
| `buffer` | [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!:The text buffer. |

### getInitialScrollY

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInitialScrollY(
    widget: TextView!, 
    buffer: Spannable!
): Int
```

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------|
| `widget` | [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!:The text view. |
| `buffer` | [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!:The text buffer. |

### onTouchEvent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun onTouchEvent(
    widget: TextView!, 
    buffer: Spannable!, 
    event: MotionEvent!
): Boolean
```

Handles touch events for dragging. You may want to do other actions like moving the cursor on touch as well. 

### scrollTo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun scrollTo(
    widget: TextView!, 
    layout: Layout!, 
    x: Int, 
    y: Int
): Unit
```

Scrolls the specified widget to the specified coordinates, except constrains the X scrolling position to the horizontal regions of the text that will be visible after scrolling to the specified Y position.
