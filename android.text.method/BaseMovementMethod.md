# BaseMovementMethod

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BaseMovementMethod

Kotlin| [Java](https://developer.android.com/reference/android/text/method/BaseMovementMethod "View this page in Java") 

```
open class BaseMovementMethod : MovementMethod
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.text.method.BaseMovementMethod](https://developer.android.com/reference/kotlin/android/text/method/BaseMovementMethod#) |

| Known Direct Subclasses [ArrowKeyMovementMethod](https://developer.android.com/reference/kotlin/android/text/method/ArrowKeyMovementMethod), [ScrollingMovementMethod](https://developer.android.com/reference/kotlin/android/text/method/ScrollingMovementMethod) |-----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------| | [ArrowKeyMovementMethod](https://developer.android.com/reference/kotlin/android/text/method/ArrowKeyMovementMethod) | A movement method that provides cursor movement and selection. | | [ScrollingMovementMethod](https://developer.android.com/reference/kotlin/android/text/method/ScrollingMovementMethod) | A movement method that interprets movement keys by scrolling the text buffer. | |

| Known Indirect Subclasses [LinkMovementMethod](https://developer.android.com/reference/kotlin/android/text/method/LinkMovementMethod) |-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------| | [LinkMovementMethod](https://developer.android.com/reference/kotlin/android/text/method/LinkMovementMethod) | A movement method that traverses links in the text buffer and scrolls if necessary. | |

Base classes for movement methods.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------|---|
| [BaseMovementMethod](https://developer.android.com/reference/kotlin/android/text/method/BaseMovementMethod#BaseMovementMethod())`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [canSelectArbitrarily](https://developer.android.com/reference/kotlin/android/text/method/BaseMovementMethod#canSelectArbitrarily())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [initialize](https://developer.android.com/reference/kotlin/android/text/method/BaseMovementMethod#initialize(android.widget.TextView,%20android.text.Spannable))`(`widget:` ` [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!`, `text:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [nextParagraph](https://developer.android.com/reference/kotlin/android/text/method/BaseMovementMethod#nextParagraph(android.widget.TextView,%20android.text.Spannable))`(`widget:` ` [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)`, `buffer:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)`)` Performs a next paragraph movement action. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onGenericMotionEvent](https://developer.android.com/reference/kotlin/android/text/method/BaseMovementMethod#onGenericMotionEvent(android.widget.TextView,%20android.text.Spannable,%20android.view.MotionEvent))`(`widget:` ` [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!`, `text:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!`, `event:` ` [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#)!`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onKeyDown](https://developer.android.com/reference/kotlin/android/text/method/BaseMovementMethod#onKeyDown(android.widget.TextView,%20android.text.Spannable,%20kotlin.Int,%20android.view.KeyEvent))`(`widget:` ` [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!`, `text:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!`, `keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)!`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onKeyOther](https://developer.android.com/reference/kotlin/android/text/method/BaseMovementMethod#onKeyOther(android.widget.TextView,%20android.text.Spannable,%20android.view.KeyEvent))`(`widget:` ` [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!`, `text:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!`, `event:` ` [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)!`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onKeyUp](https://developer.android.com/reference/kotlin/android/text/method/BaseMovementMethod#onKeyUp(android.widget.TextView,%20android.text.Spannable,%20kotlin.Int,%20android.view.KeyEvent))`(`widget:` ` [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!`, `text:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!`, `keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onTakeFocus](https://developer.android.com/reference/kotlin/android/text/method/BaseMovementMethod#onTakeFocus(android.widget.TextView,%20android.text.Spannable,%20kotlin.Int))`(`widget:` ` [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!`, `text:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!`, `direction:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onTouchEvent](https://developer.android.com/reference/kotlin/android/text/method/BaseMovementMethod#onTouchEvent(android.widget.TextView,%20android.text.Spannable,%20android.view.MotionEvent))`(`widget:` ` [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!`, `text:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!`, `event:` ` [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#)!`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onTrackballEvent](https://developer.android.com/reference/kotlin/android/text/method/BaseMovementMethod#onTrackballEvent(android.widget.TextView,%20android.text.Spannable,%20android.view.MotionEvent))`(`widget:` ` [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!`, `text:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!`, `event:` ` [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#)!`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [previousParagraph](https://developer.android.com/reference/kotlin/android/text/method/BaseMovementMethod#previousParagraph(android.widget.TextView,%20android.text.Spannable))`(`widget:` ` [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)`, `buffer:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)`)` Performs a previous paragraph movement action. |

| Protected methods ||
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [bottom](https://developer.android.com/reference/kotlin/android/text/method/BaseMovementMethod#bottom(android.widget.TextView,%20android.text.Spannable))`(`widget:` ` [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!`, `buffer:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!`)` Performs a bottom movement action. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [down](https://developer.android.com/reference/kotlin/android/text/method/BaseMovementMethod#down(android.widget.TextView,%20android.text.Spannable))`(`widget:` ` [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!`, `buffer:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!`)` Performs a down movement action. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [end](https://developer.android.com/reference/kotlin/android/text/method/BaseMovementMethod#end(android.widget.TextView,%20android.text.Spannable))`(`widget:` ` [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!`, `buffer:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!`)` Performs an end movement action. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMovementMetaState](https://developer.android.com/reference/kotlin/android/text/method/BaseMovementMethod#getMovementMetaState(android.text.Spannable,%20android.view.KeyEvent))`(`buffer:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!`, `event:` ` [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)!`)` Gets the meta state used for movement using the modifiers tracked by the text buffer as well as those present in the key event. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [handleMovementKey](https://developer.android.com/reference/kotlin/android/text/method/BaseMovementMethod#handleMovementKey(android.widget.TextView,%20android.text.Spannable,%20kotlin.Int,%20kotlin.Int,%20android.view.KeyEvent))`(`widget:` ` [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!`, `buffer:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!`, `keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `movementMetaState:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)!`)` Performs a movement key action. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [home](https://developer.android.com/reference/kotlin/android/text/method/BaseMovementMethod#home(android.widget.TextView,%20android.text.Spannable))`(`widget:` ` [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!`, `buffer:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!`)` Performs a home movement action. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [left](https://developer.android.com/reference/kotlin/android/text/method/BaseMovementMethod#left(android.widget.TextView,%20android.text.Spannable))`(`widget:` ` [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!`, `buffer:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!`)` Performs a left movement action. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [lineEnd](https://developer.android.com/reference/kotlin/android/text/method/BaseMovementMethod#lineEnd(android.widget.TextView,%20android.text.Spannable))`(`widget:` ` [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!`, `buffer:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!`)` Performs a line-end movement action. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [lineStart](https://developer.android.com/reference/kotlin/android/text/method/BaseMovementMethod#lineStart(android.widget.TextView,%20android.text.Spannable))`(`widget:` ` [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!`, `buffer:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!`)` Performs a line-start movement action. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [pageDown](https://developer.android.com/reference/kotlin/android/text/method/BaseMovementMethod#pageDown(android.widget.TextView,%20android.text.Spannable))`(`widget:` ` [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!`, `buffer:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!`)` Performs a page-down movement action. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [pageUp](https://developer.android.com/reference/kotlin/android/text/method/BaseMovementMethod#pageUp(android.widget.TextView,%20android.text.Spannable))`(`widget:` ` [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!`, `buffer:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!`)` Performs a page-up movement action. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [right](https://developer.android.com/reference/kotlin/android/text/method/BaseMovementMethod#right(android.widget.TextView,%20android.text.Spannable))`(`widget:` ` [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!`, `buffer:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!`)` Performs a right movement action. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [top](https://developer.android.com/reference/kotlin/android/text/method/BaseMovementMethod#top(android.widget.TextView,%20android.text.Spannable))`(`widget:` ` [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!`, `buffer:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!`)` Performs a top movement action. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [up](https://developer.android.com/reference/kotlin/android/text/method/BaseMovementMethod#up(android.widget.TextView,%20android.text.Spannable))`(`widget:` ` [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!`, `buffer:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!`)` Performs an up movement action. |

## Public constructors

### BaseMovementMethod

```
BaseMovementMethod()
```

## Public methods

### canSelectArbitrarily

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun canSelectArbitrarily(): Boolean
```  

### initialize

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun initialize(
    widget: TextView!, 
    text: Spannable!
): Unit
```  

### nextParagraph

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun nextParagraph(
    widget: TextView, 
    buffer: Spannable
): Boolean
```

Performs a next paragraph movement action.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------|
| `widget` | [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#):the text view This value cannot be`null`. |
| `buffer` | [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#):the text buffer This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the event was handled, otherwise false. |

### onGenericMotionEvent

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onGenericMotionEvent(
    widget: TextView!, 
    text: Spannable!, 
    event: MotionEvent!
): Boolean
```  

### onKeyDown

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onKeyDown(
    widget: TextView!, 
    text: Spannable!, 
    keyCode: Int, 
    event: KeyEvent!
): Boolean
```  

### onKeyOther

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onKeyOther(
    widget: TextView!, 
    text: Spannable!, 
    event: KeyEvent!
): Boolean
```  

### onKeyUp

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onKeyUp(
    widget: TextView!, 
    text: Spannable!, 
    keyCode: Int, 
    event: KeyEvent!
): Boolean
```  

### onTakeFocus

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onTakeFocus(
    widget: TextView!, 
    text: Spannable!, 
    direction: Int
): Unit
```  

### onTouchEvent

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onTouchEvent(
    widget: TextView!, 
    text: Spannable!, 
    event: MotionEvent!
): Boolean
```  

### onTrackballEvent

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onTrackballEvent(
    widget: TextView!, 
    text: Spannable!, 
    event: MotionEvent!
): Boolean
```  

### previousParagraph

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun previousParagraph(
    widget: TextView, 
    buffer: Spannable
): Boolean
```

Performs a previous paragraph movement action.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------|
| `widget` | [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#):the text view This value cannot be`null`. |
| `buffer` | [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#):the text buffer This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the event was handled, otherwise false. |

## Protected methods

### bottom

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun bottom(
    widget: TextView!, 
    buffer: Spannable!
): Boolean
```

Performs a bottom movement action. Moves the cursor or scrolls to the bottom of the buffer.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------|
| `widget` | [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!:The text view. |
| `buffer` | [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!:The text buffer. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the event was handled. |

### down

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun down(
    widget: TextView!, 
    buffer: Spannable!
): Boolean
```

Performs a down movement action. Moves the cursor or scrolls down by one line.

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

Performs an end movement action. Moves the cursor or scrolls to the start of the line or to the top of the document depending on whether the insertion point is being moved or the document is being scrolled.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------|
| `widget` | [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!:The text view. |
| `buffer` | [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!:The text buffer. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the event was handled. |

### getMovementMetaState

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun getMovementMetaState(
    buffer: Spannable!, 
    event: KeyEvent!
): Int
```

Gets the meta state used for movement using the modifiers tracked by the text buffer as well as those present in the key event. The movement meta state excludes the state of locked modifiers or the SHIFT key since they are not used by movement actions (but they may be used for selection).

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------|
| `buffer` | [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!:The text buffer. |
| `event` | [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)!:The key event. |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The keyboard meta states used for movement. |

### handleMovementKey

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun handleMovementKey(
    widget: TextView!, 
    buffer: Spannable!, 
    keyCode: Int, 
    movementMetaState: Int, 
    event: KeyEvent!
): Boolean
```

Performs a movement key action. The default implementation decodes the key down and invokes movement actions such as [down](https://developer.android.com/reference/kotlin/android/text/method/BaseMovementMethod#down(android.widget.TextView,%20android.text.Spannable))and [up](https://developer.android.com/reference/kotlin/android/text/method/BaseMovementMethod#up(android.widget.TextView,%20android.text.Spannable)). [onKeyDown(android.widget.TextView,android.text.Spannable,int,android.view.KeyEvent)](https://developer.android.com/reference/kotlin/android/text/method/BaseMovementMethod#onKeyDown(android.widget.TextView,%20android.text.Spannable,%20kotlin.Int,%20android.view.KeyEvent))calls this method once to handle an [KeyEvent.ACTION_DOWN](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#ACTION_DOWN:kotlin.Int). [onKeyOther(android.widget.TextView,android.text.Spannable,android.view.KeyEvent)](https://developer.android.com/reference/kotlin/android/text/method/BaseMovementMethod#onKeyOther(android.widget.TextView,%20android.text.Spannable,%20android.view.KeyEvent))calls this method repeatedly to handle each repetition of an [KeyEvent.ACTION_MULTIPLE](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#ACTION_MULTIPLE:kotlin.Int).

| Parameters ||
|---------------------|------------------------------------------------------------------------------------------------------------------------|
| `widget` | [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!:The text view. |
| `buffer` | [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!:The text buffer. |
| `event` | [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)!:The key event. |
| `keyCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The key code. |
| `movementMetaState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The keyboard meta states used for movement. |

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

Performs a home movement action. Moves the cursor or scrolls to the start of the line or to the top of the document depending on whether the insertion point is being moved or the document is being scrolled.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------|
| `widget` | [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!:The text view. |
| `buffer` | [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!:The text buffer. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the event was handled. |

### left

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun left(
    widget: TextView!, 
    buffer: Spannable!
): Boolean
```

Performs a left movement action. Moves the cursor or scrolls left by one character.

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

Performs a line-end movement action. Moves the cursor or scrolls to the end of the line.

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

Performs a line-start movement action. Moves the cursor or scrolls to the start of the line.

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

Performs a page-down movement action. Moves the cursor or scrolls down by one page.

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

Performs a page-up movement action. Moves the cursor or scrolls up by one page.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------|
| `widget` | [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!:The text view. |
| `buffer` | [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!:The text buffer. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the event was handled. |

### right

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun right(
    widget: TextView!, 
    buffer: Spannable!
): Boolean
```

Performs a right movement action. Moves the cursor or scrolls right by one character.

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

Performs a top movement action. Moves the cursor or scrolls to the top of the buffer.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------|
| `widget` | [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!:The text view. |
| `buffer` | [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!:The text buffer. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the event was handled. |

### up

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun up(
    widget: TextView!, 
    buffer: Spannable!
): Boolean
```

Performs an up movement action. Moves the cursor or scrolls up by one line.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------|
| `widget` | [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#)!:The text view. |
| `buffer` | [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!:The text buffer. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the event was handled. |
