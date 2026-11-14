# MovementMethod

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MovementMethod

Kotlin| [Java](https://developer.android.com/reference/android/text/method/MovementMethod "View this page in Java") 
| --- | --- |

```
interface MovementMethod
```

| [android.text.method.MovementMethod](https://developer.android.com/reference/kotlin/android/text/method/MovementMethod#) |

| Known Direct Subclasses [ArrowKeyMovementMethod](https://developer.android.com/reference/kotlin/android/text/method/ArrowKeyMovementMethod), [BaseMovementMethod](https://developer.android.com/reference/kotlin/android/text/method/BaseMovementMethod), [ScrollingMovementMethod](https://developer.android.com/reference/kotlin/android/text/method/ScrollingMovementMethod) |-----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------| | [ArrowKeyMovementMethod](https://developer.android.com/reference/kotlin/android/text/method/ArrowKeyMovementMethod) | A movement method that provides cursor movement and selection. | | [BaseMovementMethod](https://developer.android.com/reference/kotlin/android/text/method/BaseMovementMethod) | Base classes for movement methods. | | [ScrollingMovementMethod](https://developer.android.com/reference/kotlin/android/text/method/ScrollingMovementMethod) | A movement method that interprets movement keys by scrolling the text buffer. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [ArrowKeyMovementMethod](https://developer.android.com/reference/kotlin/android/text/method/ArrowKeyMovementMethod), [LinkMovementMethod](https://developer.android.com/reference/kotlin/android/text/method/LinkMovementMethod), [LinkMovementMethod](https://developer.android.com/reference/kotlin/android/text/method/LinkMovementMethod), [ScrollingMovementMethod](https://developer.android.com/reference/kotlin/android/text/method/ScrollingMovementMethod) |-----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------| | [ArrowKeyMovementMethod](https://developer.android.com/reference/kotlin/android/text/method/ArrowKeyMovementMethod) | A movement method that provides cursor movement and selection. | | [LinkMovementMethod](https://developer.android.com/reference/kotlin/android/text/method/LinkMovementMethod) | A movement method that traverses links in the text buffer and scrolls if necessary. | | [LinkMovementMethod](https://developer.android.com/reference/kotlin/android/text/method/LinkMovementMethod) | A movement method that traverses links in the text buffer and scrolls if necessary. | | [ScrollingMovementMethod](https://developer.android.com/reference/kotlin/android/text/method/ScrollingMovementMethod) | A movement method that interprets movement keys by scrolling the text buffer. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Provides cursor positioning, scrolling and text selection functionality in a [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#).

The [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#) delegates handling of key events, trackball motions and touches to the movement method for purposes of content navigation. The framework automatically selects an appropriate movement method based on the content of the [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#).

This interface is intended for use by the framework; it should not be implemented directly by applications.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [canSelectArbitrarily](https://developer.android.com/reference/kotlin/android/text/method/MovementMethod#canSelectArbitrarily())`()` Returns true if this movement method allows arbitrary selection of any text; false if it has no selection (like a movement method that only scrolls) or a constrained selection (for example limited to links. The "Select All" menu item is disabled if arbitrary selection is not allowed. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [initialize](https://developer.android.com/reference/kotlin/android/text/method/MovementMethod#initialize(android.widget.TextView,%20android.text.Spannable))`(`widget:` ` [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!`, `text:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!`)` <br /> |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onGenericMotionEvent](https://developer.android.com/reference/kotlin/android/text/method/MovementMethod#onGenericMotionEvent(android.widget.TextView,%20android.text.Spannable,%20android.view.MotionEvent))`(`widget:` ` [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!`, `text:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!`, `event:` ` [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#)!`)` <br /> |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onKeyDown](https://developer.android.com/reference/kotlin/android/text/method/MovementMethod#onKeyDown(android.widget.TextView,%20android.text.Spannable,%20kotlin.Int,%20android.view.KeyEvent))`(`widget:` ` [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!`, `text:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!`, `keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)!`)` <br /> |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onKeyOther](https://developer.android.com/reference/kotlin/android/text/method/MovementMethod#onKeyOther(android.widget.TextView,%20android.text.Spannable,%20android.view.KeyEvent))`(`view:` ` [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!`, `text:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!`, `event:` ` [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)!`)` If the key listener wants to other kinds of key events, return true, otherwise return false and the caller (i.e. the widget host) will handle the key. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onKeyUp](https://developer.android.com/reference/kotlin/android/text/method/MovementMethod#onKeyUp(android.widget.TextView,%20android.text.Spannable,%20kotlin.Int,%20android.view.KeyEvent))`(`widget:` ` [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!`, `text:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!`, `keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)!`)` <br /> |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onTakeFocus](https://developer.android.com/reference/kotlin/android/text/method/MovementMethod#onTakeFocus(android.widget.TextView,%20android.text.Spannable,%20kotlin.Int))`(`widget:` ` [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!`, `text:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!`, `direction:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onTouchEvent](https://developer.android.com/reference/kotlin/android/text/method/MovementMethod#onTouchEvent(android.widget.TextView,%20android.text.Spannable,%20android.view.MotionEvent))`(`widget:` ` [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!`, `text:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!`, `event:` ` [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#)!`)` <br /> |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onTrackballEvent](https://developer.android.com/reference/kotlin/android/text/method/MovementMethod#onTrackballEvent(android.widget.TextView,%20android.text.Spannable,%20android.view.MotionEvent))`(`widget:` ` [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!`, `text:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!`, `event:` ` [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#)!`)` <br /> |
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
