# MovementMethod

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MovementMethod

Kotlin| [Java](MovementMethod.md) 
| --- | --- |

```
interface MovementMethod
```

| [android.text.method.MovementMethod](MovementMethod.md) |

| Known Direct Subclasses [ArrowKeyMovementMethod](ArrowKeyMovementMethod.md), [BaseMovementMethod](BaseMovementMethod.md), [ScrollingMovementMethod](ScrollingMovementMethod.md) |-----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------| | [ArrowKeyMovementMethod](ArrowKeyMovementMethod.md) | A movement method that provides cursor movement and selection. | | [BaseMovementMethod](BaseMovementMethod.md) | Base classes for movement methods. | | [ScrollingMovementMethod](ScrollingMovementMethod.md) | A movement method that interprets movement keys by scrolling the text buffer. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [ArrowKeyMovementMethod](ArrowKeyMovementMethod.md), [LinkMovementMethod](LinkMovementMethod.md), [LinkMovementMethod](LinkMovementMethod.md), [ScrollingMovementMethod](ScrollingMovementMethod.md) |-----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------| | [ArrowKeyMovementMethod](ArrowKeyMovementMethod.md) | A movement method that provides cursor movement and selection. | | [LinkMovementMethod](LinkMovementMethod.md) | A movement method that traverses links in the text buffer and scrolls if necessary. | | [LinkMovementMethod](LinkMovementMethod.md) | A movement method that traverses links in the text buffer and scrolls if necessary. | | [ScrollingMovementMethod](ScrollingMovementMethod.md) | A movement method that interprets movement keys by scrolling the text buffer. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Provides cursor positioning, scrolling and text selection functionality in a [TextView](../android.widget/TextView.md).

The [TextView](../android.widget/TextView.md) delegates handling of key events, trackball motions and touches to the movement method for purposes of content navigation. The framework automatically selects an appropriate movement method based on the content of the [TextView](../android.widget/TextView.md).

This interface is intended for use by the framework; it should not be implemented directly by applications.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [canSelectArbitrarily](MovementMethod.md))`()` Returns true if this movement method allows arbitrary selection of any text; false if it has no selection (like a movement method that only scrolls) or a constrained selection (for example limited to links. The "Select All" menu item is disabled if arbitrary selection is not allowed. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [initialize](MovementMethod.md))`(`widget:` ` [TextView](../android.widget/TextView.md)!`, `text:` ` [Spannable](../android.text/Spannable.md)!`)` <br /> |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onGenericMotionEvent](MovementMethod.md))`(`widget:` ` [TextView](../android.widget/TextView.md)!`, `text:` ` [Spannable](../android.text/Spannable.md)!`, `event:` ` [MotionEvent](../android.view/MotionEvent.md)!`)` <br /> |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onKeyDown](MovementMethod.md))`(`widget:` ` [TextView](../android.widget/TextView.md)!`, `text:` ` [Spannable](../android.text/Spannable.md)!`, `keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](../android.view/KeyEvent.md)!`)` <br /> |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onKeyOther](MovementMethod.md))`(`view:` ` [TextView](../android.widget/TextView.md)!`, `text:` ` [Spannable](../android.text/Spannable.md)!`, `event:` ` [KeyEvent](../android.view/KeyEvent.md)!`)` If the key listener wants to other kinds of key events, return true, otherwise return false and the caller (i.e. the widget host) will handle the key. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onKeyUp](MovementMethod.md))`(`widget:` ` [TextView](../android.widget/TextView.md)!`, `text:` ` [Spannable](../android.text/Spannable.md)!`, `keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](../android.view/KeyEvent.md)!`)` <br /> |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onTakeFocus](MovementMethod.md))`(`widget:` ` [TextView](../android.widget/TextView.md)!`, `text:` ` [Spannable](../android.text/Spannable.md)!`, `direction:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onTouchEvent](MovementMethod.md))`(`widget:` ` [TextView](../android.widget/TextView.md)!`, `text:` ` [Spannable](../android.text/Spannable.md)!`, `event:` ` [MotionEvent](../android.view/MotionEvent.md)!`)` <br /> |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onTrackballEvent](MovementMethod.md))`(`widget:` ` [TextView](../android.widget/TextView.md)!`, `text:` ` [Spannable](../android.text/Spannable.md)!`, `event:` ` [MotionEvent](../android.view/MotionEvent.md)!`)` <br /> |
| --- | --- |

## Public methods

### canSelectArbitrarily

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun canSelectArbitrarily(): Boolean
```

Returns true if this movement method allows arbitrary selection of any text; false if it has no selection (like a movement method that only scrolls) or a constrained selection (for example limited to links. The "Select All" menu item is disabled if arbitrary selection is not allowed. 

### initialize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun initialize(
    widget: TextView!, 
    text: Spannable!
): Unit
```  

### onGenericMotionEvent

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onGenericMotionEvent(
    widget: TextView!, 
    text: Spannable!, 
    event: MotionEvent!
): Boolean
```  

### onKeyDown

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onKeyDown(
    widget: TextView!, 
    text: Spannable!, 
    keyCode: Int, 
    event: KeyEvent!
): Boolean
```  

### onKeyOther

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onKeyOther(
    view: TextView!, 
    text: Spannable!, 
    event: KeyEvent!
): Boolean
```

If the key listener wants to other kinds of key events, return true, otherwise return false and the caller (i.e. the widget host) will handle the key. 

### onKeyUp

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onKeyUp(
    widget: TextView!, 
    text: Spannable!, 
    keyCode: Int, 
    event: KeyEvent!
): Boolean
```  

### onTakeFocus

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onTakeFocus(
    widget: TextView!, 
    text: Spannable!, 
    direction: Int
): Unit
```  

### onTouchEvent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onTouchEvent(
    widget: TextView!, 
    text: Spannable!, 
    event: MotionEvent!
): Boolean
```  

### onTrackballEvent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onTrackballEvent(
    widget: TextView!, 
    text: Spannable!, 
    event: MotionEvent!
): Boolean
```
