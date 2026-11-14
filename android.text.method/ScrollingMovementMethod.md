# ScrollingMovementMethod

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ScrollingMovementMethod

Kotlin| [Java](https://developer.android.com/reference/android/text/method/ScrollingMovementMethod "View this page in Java") 

```
open class ScrollingMovementMethod : BaseMovementMethod, MovementMethod
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [android.text.method.BaseMovementMethod](https://developer.android.com/reference/kotlin/android/text/method/BaseMovementMethod) ||
| | ↳ | [android.text.method.ScrollingMovementMethod](https://developer.android.com/reference/kotlin/android/text/method/ScrollingMovementMethod#) |

| Known Direct Subclasses [LinkMovementMethod](https://developer.android.com/reference/kotlin/android/text/method/LinkMovementMethod) |-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------| | [LinkMovementMethod](https://developer.android.com/reference/kotlin/android/text/method/LinkMovementMethod) | A movement method that traverses links in the text buffer and scrolls if necessary. | |

A movement method that interprets movement keys by scrolling the text buffer.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ScrollingMovementMethod](https://developer.android.com/reference/kotlin/android/text/method/ScrollingMovementMethod#ScrollingMovementMethod())`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [MovementMethod](https://developer.android.com/reference/kotlin/android/text/method/MovementMethod)! | [getInstance](https://developer.android.com/reference/kotlin/android/text/method/ScrollingMovementMethod#getInstance())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onTakeFocus](https://developer.android.com/reference/kotlin/android/text/method/ScrollingMovementMethod#onTakeFocus(android.widget.TextView,%20android.text.Spannable,%20kotlin.Int))`(`widget:` ` [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!`, `text:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!`, `dir:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onTouchEvent](https://developer.android.com/reference/kotlin/android/text/method/ScrollingMovementMethod#onTouchEvent(android.widget.TextView,%20android.text.Spannable,%20android.view.MotionEvent))`(`widget:` ` [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!`, `buffer:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!`, `event:` ` [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#)!`)` <br /> |

| Protected methods ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [bottom](https://developer.android.com/reference/kotlin/android/text/method/ScrollingMovementMethod#bottom(android.widget.TextView,%20android.text.Spannable))`(`widget:` ` [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!`, `buffer:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [down](https://developer.android.com/reference/kotlin/android/text/method/ScrollingMovementMethod#down(android.widget.TextView,%20android.text.Spannable))`(`widget:` ` [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!`, `buffer:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [end](https://developer.android.com/reference/kotlin/android/text/method/ScrollingMovementMethod#end(android.widget.TextView,%20android.text.Spannable))`(`widget:` ` [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!`, `buffer:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [home](https://developer.android.com/reference/kotlin/android/text/method/ScrollingMovementMethod#home(android.widget.TextView,%20android.text.Spannable))`(`widget:` ` [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!`, `buffer:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [left](https://developer.android.com/reference/kotlin/android/text/method/ScrollingMovementMethod#left(android.widget.TextView,%20android.text.Spannable))`(`widget:` ` [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!`, `buffer:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [lineEnd](https://developer.android.com/reference/kotlin/android/text/method/ScrollingMovementMethod#lineEnd(android.widget.TextView,%20android.text.Spannable))`(`widget:` ` [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!`, `buffer:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [lineStart](https://developer.android.com/reference/kotlin/android/text/method/ScrollingMovementMethod#lineStart(android.widget.TextView,%20android.text.Spannable))`(`widget:` ` [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!`, `buffer:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [pageDown](https://developer.android.com/reference/kotlin/android/text/method/ScrollingMovementMethod#pageDown(android.widget.TextView,%20android.text.Spannable))`(`widget:` ` [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!`, `buffer:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [pageUp](https://developer.android.com/reference/kotlin/android/text/method/ScrollingMovementMethod#pageUp(android.widget.TextView,%20android.text.Spannable))`(`widget:` ` [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!`, `buffer:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [right](https://developer.android.com/reference/kotlin/android/text/method/ScrollingMovementMethod#right(android.widget.TextView,%20android.text.Spannable))`(`widget:` ` [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!`, `buffer:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [top](https://developer.android.com/reference/kotlin/android/text/method/ScrollingMovementMethod#top(android.widget.TextView,%20android.text.Spannable))`(`widget:` ` [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!`, `buffer:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [up](https://developer.android.com/reference/kotlin/android/text/method/ScrollingMovementMethod#up(android.widget.TextView,%20android.text.Spannable))`(`widget:` ` [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!`, `buffer:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!`)` <br /> |

| Inherited functions ||
|---|---|
| From class [BaseMovementMethod](https://developer.android.com/reference/kotlin/android/text/method/BaseMovementMethod) |------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [canSelectArbitrarily](https://developer.android.com/reference/kotlin/android/text/method/BaseMovementMethod#canSelectArbitrarily())`()` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMovementMetaState](https://developer.android.com/reference/kotlin/android/text/method/BaseMovementMethod#getMovementMetaState(android.text.Spannable,%20android.view.KeyEvent))`(`buffer:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!`, `event:` ` [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)!`)` <br /> Gets the meta state used for movement using the modifiers tracked by the text buffer as well as those present in the key event. The movement meta state excludes the state of locked modifiers or the SHIFT key since they are not used by movement actions (but they may be used for selection). <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [handleMovementKey](https://developer.android.com/reference/kotlin/android/text/method/BaseMovementMethod#handleMovementKey(android.widget.TextView,%20android.text.Spannable,%20kotlin.Int,%20kotlin.Int,%20android.view.KeyEvent))`(`widget:` ` [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!`, `buffer:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!`, `keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `movementMetaState:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)!`)` <br /> Performs a movement key action. The default implementation decodes the key down and invokes movement actions such as [down](https://developer.android.com/reference/kotlin/android/text/method/BaseMovementMethod#down(android.widget.TextView,%20android.text.Spannable))and [up](https://developer.android.com/reference/kotlin/android/text/method/BaseMovementMethod#up(android.widget.TextView,%20android.text.Spannable)). [onKeyDown(android.widget.TextView,android.text.Spannable,int,android.view.KeyEvent)](https://developer.android.com/reference/kotlin/android/text/method/BaseMovementMethod#onKeyDown(android.widget.TextView,%20android.text.Spannable,%20kotlin.Int,%20android.view.KeyEvent))calls this method once to handle an [KeyEvent.ACTION_DOWN](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#ACTION_DOWN:kotlin.Int). [onKeyOther(android.widget.TextView,android.text.Spannable,android.view.KeyEvent)](https://developer.android.com/reference/kotlin/android/text/method/BaseMovementMethod#onKeyOther(android.widget.TextView,%20android.text.Spannable,%20android.view.KeyEvent))calls this method repeatedly to handle each repetition of an [KeyEvent.ACTION_MULTIPLE](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#ACTION_MULTIPLE:kotlin.Int). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [initialize](https://developer.android.com/reference/kotlin/android/text/method/BaseMovementMethod#initialize(android.widget.TextView,%20android.text.Spannable))`(`widget:` ` [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!`, `text:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [nextParagraph](https://developer.android.com/reference/kotlin/android/text/method/BaseMovementMethod#nextParagraph(android.widget.TextView,%20android.text.Spannable))`(`widget:` ` [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)`, `buffer:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)`)` <br /> Performs a next paragraph movement action. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onGenericMotionEvent](https://developer.android.com/reference/kotlin/android/text/method/BaseMovementMethod#onGenericMotionEvent(android.widget.TextView,%20android.text.Spannable,%20android.view.MotionEvent))`(`widget:` ` [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!`, `text:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!`, `event:` ` [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#)!`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onKeyDown](https://developer.android.com/reference/kotlin/android/text/method/BaseMovementMethod#onKeyDown(android.widget.TextView,%20android.text.Spannable,%20kotlin.Int,%20android.view.KeyEvent))`(`widget:` ` [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!`, `text:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!`, `keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)!`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onKeyOther](https://developer.android.com/reference/kotlin/android/text/method/BaseMovementMethod#onKeyOther(android.widget.TextView,%20android.text.Spannable,%20android.view.KeyEvent))`(`widget:` ` [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!`, `text:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!`, `event:` ` [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)!`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onKeyUp](https://developer.android.com/reference/kotlin/android/text/method/BaseMovementMethod#onKeyUp(android.widget.TextView,%20android.text.Spannable,%20kotlin.Int,%20android.view.KeyEvent))`(`widget:` ` [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!`, `text:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!`, `keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)!`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onTrackballEvent](https://developer.android.com/reference/kotlin/android/text/method/BaseMovementMethod#onTrackballEvent(android.widget.TextView,%20android.text.Spannable,%20android.view.MotionEvent))`(`widget:` ` [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!`, `text:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!`, `event:` ` [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#)!`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [previousParagraph](https://developer.android.com/reference/kotlin/android/text/method/BaseMovementMethod#previousParagraph(android.widget.TextView,%20android.text.Spannable))`(`widget:` ` [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)`, `buffer:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)`)` <br /> Performs a previous paragraph movement action. <br /> | ||

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
| `widget` | [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!:The text view. |
| `buffer` | [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!:The text buffer. |

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
| `widget` | [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!:The text view. |
| `buffer` | [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!:The text buffer. |

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
| `widget` | [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!:The text view. |
| `buffer` | [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!:The text buffer. |

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
| `widget` | [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!:The text view. |
| `buffer` | [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!:The text buffer. |

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
| `widget` | [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!:The text view. |
| `buffer` | [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!:The text buffer. |

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
| `widget` | [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!:The text view. |
| `buffer` | [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!:The text buffer. |

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
| `widget` | [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!:The text view. |
| `buffer` | [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!:The text buffer. |

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
| `widget` | [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!:The text view. |
| `buffer` | [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!:The text buffer. |

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
| `widget` | [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!:The text view. |
| `buffer` | [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!:The text buffer. |

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
| `widget` | [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!:The text view. |
| `buffer` | [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!:The text buffer. |

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
| `widget` | [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!:The text view. |
| `buffer` | [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!:The text buffer. |

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
| `widget` | [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!:The text view. |
| `buffer` | [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!:The text buffer. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the event was handled. |
