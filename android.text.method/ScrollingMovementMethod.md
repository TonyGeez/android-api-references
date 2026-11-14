# ScrollingMovementMethod

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ScrollingMovementMethod

Kotlin| [Java](../android/text/method/ScrollingMovementMethod.md) 
| --- | --- |

```
open class ScrollingMovementMethod : BaseMovementMethod, MovementMethod
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.text.method.BaseMovementMethod](../android/text/method/BaseMovementMethod.md) ||
| | ↳ | [android.text.method.ScrollingMovementMethod](../android/text/method/ScrollingMovementMethod.md) |

| Known Direct Subclasses [LinkMovementMethod](../android/text/method/LinkMovementMethod.md) |-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------| | [LinkMovementMethod](../android/text/method/LinkMovementMethod.md) | A movement method that traverses links in the text buffer and scrolls if necessary. | |
| --- | --- | --- | --- | --- | --- | --- |

A movement method that interprets movement keys by scrolling the text buffer.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ScrollingMovementMethod](../android/text/method/ScrollingMovementMethod.md))`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [MovementMethod](../android/text/method/MovementMethod.md)! | [getInstance](../android/text/method/ScrollingMovementMethod.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onTakeFocus](../android/text/method/ScrollingMovementMethod.md))`(`widget:` ` [TextView](../android/widget/TextView.md)!`, `text:` ` [Spannable](../android/text/Spannable.md)!`, `dir:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onTouchEvent](../android/text/method/ScrollingMovementMethod.md))`(`widget:` ` [TextView](../android/widget/TextView.md)!`, `buffer:` ` [Spannable](../android/text/Spannable.md)!`, `event:` ` [MotionEvent](../android/view/MotionEvent.md)!`)` <br /> |
| --- | --- |

| Protected methods ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [bottom](../android/text/method/ScrollingMovementMethod.md))`(`widget:` ` [TextView](../android/widget/TextView.md)!`, `buffer:` ` [Spannable](../android/text/Spannable.md)!`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [down](../android/text/method/ScrollingMovementMethod.md))`(`widget:` ` [TextView](../android/widget/TextView.md)!`, `buffer:` ` [Spannable](../android/text/Spannable.md)!`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [end](../android/text/method/ScrollingMovementMethod.md))`(`widget:` ` [TextView](../android/widget/TextView.md)!`, `buffer:` ` [Spannable](../android/text/Spannable.md)!`)` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [home](../android/text/method/ScrollingMovementMethod.md))`(`widget:` ` [TextView](../android/widget/TextView.md)!`, `buffer:` ` [Spannable](../android/text/Spannable.md)!`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [left](../android/text/method/ScrollingMovementMethod.md))`(`widget:` ` [TextView](../android/widget/TextView.md)!`, `buffer:` ` [Spannable](../android/text/Spannable.md)!`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [lineEnd](../android/text/method/ScrollingMovementMethod.md))`(`widget:` ` [TextView](../android/widget/TextView.md)!`, `buffer:` ` [Spannable](../android/text/Spannable.md)!`)` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [lineStart](../android/text/method/ScrollingMovementMethod.md))`(`widget:` ` [TextView](../android/widget/TextView.md)!`, `buffer:` ` [Spannable](../android/text/Spannable.md)!`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [pageDown](../android/text/method/ScrollingMovementMethod.md))`(`widget:` ` [TextView](../android/widget/TextView.md)!`, `buffer:` ` [Spannable](../android/text/Spannable.md)!`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [pageUp](../android/text/method/ScrollingMovementMethod.md))`(`widget:` ` [TextView](../android/widget/TextView.md)!`, `buffer:` ` [Spannable](../android/text/Spannable.md)!`)` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [right](../android/text/method/ScrollingMovementMethod.md))`(`widget:` ` [TextView](../android/widget/TextView.md)!`, `buffer:` ` [Spannable](../android/text/Spannable.md)!`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [top](../android/text/method/ScrollingMovementMethod.md))`(`widget:` ` [TextView](../android/widget/TextView.md)!`, `buffer:` ` [Spannable](../android/text/Spannable.md)!`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [up](../android/text/method/ScrollingMovementMethod.md))`(`widget:` ` [TextView](../android/widget/TextView.md)!`, `buffer:` ` [Spannable](../android/text/Spannable.md)!`)` <br /> |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [BaseMovementMethod](../android/text/method/BaseMovementMethod.md) |------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [canSelectArbitrarily](../android/text/method/BaseMovementMethod.md))`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMovementMetaState](../android/text/method/BaseMovementMethod.md))`(`buffer:` ` [Spannable](../android/text/Spannable.md)!`, `event:` ` [KeyEvent](../android/view/KeyEvent.md)!`)` <br /> Gets the meta state used for movement using the modifiers tracked by the text buffer as well as those present in the key event. The movement meta state excludes the state of locked modifiers or the SHIFT key since they are not used by movement actions (but they may be used for selection). <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [handleMovementKey](../android/text/method/BaseMovementMethod.md))`(`widget:` ` [TextView](../android/widget/TextView.md)!`, `buffer:` ` [Spannable](../android/text/Spannable.md)!`, `keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `movementMetaState:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](../android/view/KeyEvent.md)!`)` <br /> Performs a movement key action. The default implementation decodes the key down and invokes movement actions such as [down](../android/text/method/BaseMovementMethod.md))and [up](../android/text/method/BaseMovementMethod.md)). [onKeyDown(android.widget.TextView,android.text.Spannable,int,android.view.KeyEvent)](../android/text/method/BaseMovementMethod.md))calls this method once to handle an [KeyEvent.ACTION_DOWN](../android/view/KeyEvent.md). [onKeyOther(android.widget.TextView,android.text.Spannable,android.view.KeyEvent)](../android/text/method/BaseMovementMethod.md))calls this method repeatedly to handle each repetition of an [KeyEvent.ACTION_MULTIPLE](../android/view/KeyEvent.md). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [initialize](../android/text/method/BaseMovementMethod.md))`(`widget:` ` [TextView](../android/widget/TextView.md)!`, `text:` ` [Spannable](../android/text/Spannable.md)!`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [nextParagraph](../android/text/method/BaseMovementMethod.md))`(`widget:` ` [TextView](../android/widget/TextView.md)`, `buffer:` ` [Spannable](../android/text/Spannable.md)`)` <br /> Performs a next paragraph movement action. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onGenericMotionEvent](../android/text/method/BaseMovementMethod.md))`(`widget:` ` [TextView](../android/widget/TextView.md)!`, `text:` ` [Spannable](../android/text/Spannable.md)!`, `event:` ` [MotionEvent](../android/view/MotionEvent.md)!`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onKeyDown](../android/text/method/BaseMovementMethod.md))`(`widget:` ` [TextView](../android/widget/TextView.md)!`, `text:` ` [Spannable](../android/text/Spannable.md)!`, `keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](../android/view/KeyEvent.md)!`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onKeyOther](../android/text/method/BaseMovementMethod.md))`(`widget:` ` [TextView](../android/widget/TextView.md)!`, `text:` ` [Spannable](../android/text/Spannable.md)!`, `event:` ` [KeyEvent](../android/view/KeyEvent.md)!`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onKeyUp](../android/text/method/BaseMovementMethod.md))`(`widget:` ` [TextView](../android/widget/TextView.md)!`, `text:` ` [Spannable](../android/text/Spannable.md)!`, `keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](../android/view/KeyEvent.md)!`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onTrackballEvent](../android/text/method/BaseMovementMethod.md))`(`widget:` ` [TextView](../android/widget/TextView.md)!`, `text:` ` [Spannable](../android/text/Spannable.md)!`, `event:` ` [MotionEvent](../android/view/MotionEvent.md)!`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [previousParagraph](../android/text/method/BaseMovementMethod.md))`(`widget:` ` [TextView](../android/widget/TextView.md)`, `buffer:` ` [Spannable](../android/text/Spannable.md)`)` <br /> Performs a previous paragraph movement action. <br /> | ||

## Public constructors

### ScrollingMovementMethod

```
ScrollingMovementMethod()
```

## Public methods

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(): MovementMethod!
```  

### onTakeFocus

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onTakeFocus(
    widget: TextView!, 
    text: Spannable!, 
    dir: Int
): Unit
```  

### onTouchEvent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onTouchEvent(
    widget: TextView!, 
    buffer: Spannable!, 
    event: MotionEvent!
): Boolean
```

## Protected methods

### bottom

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun bottom(
    widget: TextView!, 
    buffer: Spannable!
): Boolean
```

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------|
| `widget` | [TextView](../android/widget/TextView.md)!:The text view. |
| `buffer` | [Spannable](../android/text/Spannable.md)!:The text buffer. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the event was handled. |

### down

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun down(
    widget: TextView!, 
    buffer: Spannable!
): Boolean
```

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------|
| `widget` | [TextView](../android/widget/TextView.md)!:The text view. |
| `buffer` | [Spannable](../android/text/Spannable.md)!:The text buffer. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the event was handled. |

### end

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun end(
    widget: TextView!, 
    buffer: Spannable!
): Boolean
```

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------|
| `widget` | [TextView](../android/widget/TextView.md)!:The text view. |
| `buffer` | [Spannable](../android/text/Spannable.md)!:The text buffer. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the event was handled. |

### home

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun home(
    widget: TextView!, 
    buffer: Spannable!
): Boolean
```

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------|
| `widget` | [TextView](../android/widget/TextView.md)!:The text view. |
| `buffer` | [Spannable](../android/text/Spannable.md)!:The text buffer. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the event was handled. |

### left

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun left(
    widget: TextView!, 
    buffer: Spannable!
): Boolean
```

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------|
| `widget` | [TextView](../android/widget/TextView.md)!:The text view. |
| `buffer` | [Spannable](../android/text/Spannable.md)!:The text buffer. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the event was handled. |

### lineEnd

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun lineEnd(
    widget: TextView!, 
    buffer: Spannable!
): Boolean
```

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------|
| `widget` | [TextView](../android/widget/TextView.md)!:The text view. |
| `buffer` | [Spannable](../android/text/Spannable.md)!:The text buffer. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the event was handled. |

### lineStart

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun lineStart(
    widget: TextView!, 
    buffer: Spannable!
): Boolean
```

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------|
| `widget` | [TextView](../android/widget/TextView.md)!:The text view. |
| `buffer` | [Spannable](../android/text/Spannable.md)!:The text buffer. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the event was handled. |

### pageDown

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun pageDown(
    widget: TextView!, 
    buffer: Spannable!
): Boolean
```

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------|
| `widget` | [TextView](../android/widget/TextView.md)!:The text view. |
| `buffer` | [Spannable](../android/text/Spannable.md)!:The text buffer. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the event was handled. |

### pageUp

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun pageUp(
    widget: TextView!, 
    buffer: Spannable!
): Boolean
```

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------|
| `widget` | [TextView](../android/widget/TextView.md)!:The text view. |
| `buffer` | [Spannable](../android/text/Spannable.md)!:The text buffer. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the event was handled. |

### right

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun right(
    widget: TextView!, 
    buffer: Spannable!
): Boolean
```

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------|
| `widget` | [TextView](../android/widget/TextView.md)!:The text view. |
| `buffer` | [Spannable](../android/text/Spannable.md)!:The text buffer. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the event was handled. |

### top

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun top(
    widget: TextView!, 
    buffer: Spannable!
): Boolean
```

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------|
| `widget` | [TextView](../android/widget/TextView.md)!:The text view. |
| `buffer` | [Spannable](../android/text/Spannable.md)!:The text buffer. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the event was handled. |

### up

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun up(
    widget: TextView!, 
    buffer: Spannable!
): Boolean
```

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------|
| `widget` | [TextView](../android/widget/TextView.md)!:The text view. |
| `buffer` | [Spannable](../android/text/Spannable.md)!:The text buffer. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the event was handled. |
