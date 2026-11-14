# Touch

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Touch

Kotlin| [Java](../android/text/method/Touch.md) 
| --- | --- |

```
open class Touch
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.text.method.Touch](../android/text/method/Touch.md) |

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getInitialScrollX](../android/text/method/Touch.md))`(`widget:` ` [TextView](../android/widget/TextView.md)!`, `buffer:` ` [Spannable](../android/text/Spannable.md)!`)` <br /> |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getInitialScrollY](../android/text/method/Touch.md))`(`widget:` ` [TextView](../android/widget/TextView.md)!`, `buffer:` ` [Spannable](../android/text/Spannable.md)!`)` <br /> |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onTouchEvent](../android/text/method/Touch.md))`(`widget:` ` [TextView](../android/widget/TextView.md)!`, `buffer:` ` [Spannable](../android/text/Spannable.md)!`, `event:` ` [MotionEvent](../android/view/MotionEvent.md)!`)` Handles touch events for dragging. |
| --- | --- |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [scrollTo](../android/text/method/Touch.md))`(`widget:` ` [TextView](../android/widget/TextView.md)!`, `layout:` ` [Layout](../android/text/Layout.md)!`, `x:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `y:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Scrolls the specified widget to the specified coordinates, except constrains the X scrolling position to the horizontal regions of the text that will be visible after scrolling to the specified Y position. |

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
| `widget` | [TextView](../android/widget/TextView.md)!:The text view. |
| `buffer` | [Spannable](../android/text/Spannable.md)!:The text buffer. |

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
| `widget` | [TextView](../android/widget/TextView.md)!:The text view. |
| `buffer` | [Spannable](../android/text/Spannable.md)!:The text buffer. |

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
