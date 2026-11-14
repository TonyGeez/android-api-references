# BaseMovementMethod

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BaseMovementMethod

Kotlin| [Java](../android/text/method/BaseMovementMethod.md) 
| --- | --- |

```
open class BaseMovementMethod : MovementMethod
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.text.method.BaseMovementMethod](../android/text/method/BaseMovementMethod.md) |

| Known Direct Subclasses [ArrowKeyMovementMethod](../android/text/method/ArrowKeyMovementMethod.md), [ScrollingMovementMethod](../android/text/method/ScrollingMovementMethod.md) |-----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------| | [ArrowKeyMovementMethod](../android/text/method/ArrowKeyMovementMethod.md) | A movement method that provides cursor movement and selection. | | [ScrollingMovementMethod](../android/text/method/ScrollingMovementMethod.md) | A movement method that interprets movement keys by scrolling the text buffer. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [LinkMovementMethod](../android/text/method/LinkMovementMethod.md) |-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------| | [LinkMovementMethod](../android/text/method/LinkMovementMethod.md) | A movement method that traverses links in the text buffer and scrolls if necessary. | |
| --- | --- | --- | --- | --- | --- | --- |

Base classes for movement methods.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------|---|
| [BaseMovementMethod](../android/text/method/BaseMovementMethod.md))`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [canSelectArbitrarily](../android/text/method/BaseMovementMethod.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [initialize](../android/text/method/BaseMovementMethod.md))`(`widget:` ` [TextView](../android/widget/TextView.md)!`, `text:` ` [Spannable](../android/text/Spannable.md)!`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [nextParagraph](../android/text/method/BaseMovementMethod.md))`(`widget:` ` [TextView](../android/widget/TextView.md)`, `buffer:` ` [Spannable](../android/text/Spannable.md)`)` Performs a next paragraph movement action. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onGenericMotionEvent](../android/text/method/BaseMovementMethod.md))`(`widget:` ` [TextView](../android/widget/TextView.md)!`, `text:` ` [Spannable](../android/text/Spannable.md)!`, `event:` ` [MotionEvent](../android/view/MotionEvent.md)!`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onKeyDown](../android/text/method/BaseMovementMethod.md))`(`widget:` ` [TextView](../android/widget/TextView.md)!`, `text:` ` [Spannable](../android/text/Spannable.md)!`, `keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](../android/view/KeyEvent.md)!`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onKeyOther](../android/text/method/BaseMovementMethod.md))`(`widget:` ` [TextView](../android/widget/TextView.md)!`, `text:` ` [Spannable](../android/text/Spannable.md)!`, `event:` ` [KeyEvent](../android/view/KeyEvent.md)!`)` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onKeyUp](../android/text/method/BaseMovementMethod.md))`(`widget:` ` [TextView](../android/widget/TextView.md)!`, `text:` ` [Spannable](../android/text/Spannable.md)!`, `keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](../android/view/KeyEvent.md)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onTakeFocus](../android/text/method/BaseMovementMethod.md))`(`widget:` ` [TextView](../android/widget/TextView.md)!`, `text:` ` [Spannable](../android/text/Spannable.md)!`, `direction:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onTouchEvent](../android/text/method/BaseMovementMethod.md))`(`widget:` ` [TextView](../android/widget/TextView.md)!`, `text:` ` [Spannable](../android/text/Spannable.md)!`, `event:` ` [MotionEvent](../android/view/MotionEvent.md)!`)` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onTrackballEvent](../android/text/method/BaseMovementMethod.md))`(`widget:` ` [TextView](../android/widget/TextView.md)!`, `text:` ` [Spannable](../android/text/Spannable.md)!`, `event:` ` [MotionEvent](../android/view/MotionEvent.md)!`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [previousParagraph](../android/text/method/BaseMovementMethod.md))`(`widget:` ` [TextView](../android/widget/TextView.md)`, `buffer:` ` [Spannable](../android/text/Spannable.md)`)` Performs a previous paragraph movement action. |

| Protected methods ||
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [bottom](../android/text/method/BaseMovementMethod.md))`(`widget:` ` [TextView](../android/widget/TextView.md)!`, `buffer:` ` [Spannable](../android/text/Spannable.md)!`)` Performs a bottom movement action. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [down](../android/text/method/BaseMovementMethod.md))`(`widget:` ` [TextView](../android/widget/TextView.md)!`, `buffer:` ` [Spannable](../android/text/Spannable.md)!`)` Performs a down movement action. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [end](../android/text/method/BaseMovementMethod.md))`(`widget:` ` [TextView](../android/widget/TextView.md)!`, `buffer:` ` [Spannable](../android/text/Spannable.md)!`)` Performs an end movement action. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMovementMetaState](../android/text/method/BaseMovementMethod.md))`(`buffer:` ` [Spannable](../android/text/Spannable.md)!`, `event:` ` [KeyEvent](../android/view/KeyEvent.md)!`)` Gets the meta state used for movement using the modifiers tracked by the text buffer as well as those present in the key event. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [handleMovementKey](../android/text/method/BaseMovementMethod.md))`(`widget:` ` [TextView](../android/widget/TextView.md)!`, `buffer:` ` [Spannable](../android/text/Spannable.md)!`, `keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `movementMetaState:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](../android/view/KeyEvent.md)!`)` Performs a movement key action. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [home](../android/text/method/BaseMovementMethod.md))`(`widget:` ` [TextView](../android/widget/TextView.md)!`, `buffer:` ` [Spannable](../android/text/Spannable.md)!`)` Performs a home movement action. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [left](../android/text/method/BaseMovementMethod.md))`(`widget:` ` [TextView](../android/widget/TextView.md)!`, `buffer:` ` [Spannable](../android/text/Spannable.md)!`)` Performs a left movement action. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [lineEnd](../android/text/method/BaseMovementMethod.md))`(`widget:` ` [TextView](../android/widget/TextView.md)!`, `buffer:` ` [Spannable](../android/text/Spannable.md)!`)` Performs a line-end movement action. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [lineStart](../android/text/method/BaseMovementMethod.md))`(`widget:` ` [TextView](../android/widget/TextView.md)!`, `buffer:` ` [Spannable](../android/text/Spannable.md)!`)` Performs a line-start movement action. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [pageDown](../android/text/method/BaseMovementMethod.md))`(`widget:` ` [TextView](../android/widget/TextView.md)!`, `buffer:` ` [Spannable](../android/text/Spannable.md)!`)` Performs a page-down movement action. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [pageUp](../android/text/method/BaseMovementMethod.md))`(`widget:` ` [TextView](../android/widget/TextView.md)!`, `buffer:` ` [Spannable](../android/text/Spannable.md)!`)` Performs a page-up movement action. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [right](../android/text/method/BaseMovementMethod.md))`(`widget:` ` [TextView](../android/widget/TextView.md)!`, `buffer:` ` [Spannable](../android/text/Spannable.md)!`)` Performs a right movement action. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [top](../android/text/method/BaseMovementMethod.md))`(`widget:` ` [TextView](../android/widget/TextView.md)!`, `buffer:` ` [Spannable](../android/text/Spannable.md)!`)` Performs a top movement action. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [up](../android/text/method/BaseMovementMethod.md))`(`widget:` ` [TextView](../android/widget/TextView.md)!`, `buffer:` ` [Spannable](../android/text/Spannable.md)!`)` Performs an up movement action. |

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
| `widget` | [TextView](../android/widget/TextView.md):the text view This value cannot be`null`. |
| `buffer` | [Spannable](../android/text/Spannable.md):the text buffer This value cannot be`null`. |

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
| `widget` | [TextView](../android/widget/TextView.md):the text view This value cannot be`null`. |
| `buffer` | [Spannable](../android/text/Spannable.md):the text buffer This value cannot be`null`. |

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
| `widget` | [TextView](../android/widget/TextView.md)!:The text view. |
| `buffer` | [Spannable](../android/text/Spannable.md)!:The text buffer. |

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

Performs an end movement action. Moves the cursor or scrolls to the start of the line or to the top of the document depending on whether the insertion point is being moved or the document is being scrolled.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------|
| `widget` | [TextView](../android/widget/TextView.md)!:The text view. |
| `buffer` | [Spannable](../android/text/Spannable.md)!:The text buffer. |

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
| `buffer` | [Spannable](../android/text/Spannable.md)!:The text buffer. |
| `event` | [KeyEvent](../android/view/KeyEvent.md)!:The key event. |

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

Performs a movement key action. The default implementation decodes the key down and invokes movement actions such as [down](../android/text/method/BaseMovementMethod.md))and [up](../android/text/method/BaseMovementMethod.md)). [onKeyDown(android.widget.TextView,android.text.Spannable,int,android.view.KeyEvent)](../android/text/method/BaseMovementMethod.md))calls this method once to handle an [KeyEvent.ACTION_DOWN](../android/view/KeyEvent.md). [onKeyOther(android.widget.TextView,android.text.Spannable,android.view.KeyEvent)](../android/text/method/BaseMovementMethod.md))calls this method repeatedly to handle each repetition of an [KeyEvent.ACTION_MULTIPLE](../android/view/KeyEvent.md).

| Parameters ||
|---------------------|------------------------------------------------------------------------------------------------------------------------|
| `widget` | [TextView](../android/widget/TextView.md)!:The text view. |
| `buffer` | [Spannable](../android/text/Spannable.md)!:The text buffer. |
| `event` | [KeyEvent](../android/view/KeyEvent.md)!:The key event. |
| --- | --- |
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
| `widget` | [TextView](../android/widget/TextView.md)!:The text view. |
| `buffer` | [Spannable](../android/text/Spannable.md)!:The text buffer. |

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

Performs a line-end movement action. Moves the cursor or scrolls to the end of the line.

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

Performs a line-start movement action. Moves the cursor or scrolls to the start of the line.

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

Performs a page-down movement action. Moves the cursor or scrolls down by one page.

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

Performs a page-up movement action. Moves the cursor or scrolls up by one page.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------|
| `widget` | [TextView](../android/widget/TextView.md)!:The text view. |
| `buffer` | [Spannable](../android/text/Spannable.md)!:The text buffer. |

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

Performs a top movement action. Moves the cursor or scrolls to the top of the buffer.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------|
| `widget` | [TextView](../android/widget/TextView.md)!:The text view. |
| `buffer` | [Spannable](../android/text/Spannable.md)!:The text buffer. |

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
| `widget` | [TextView](../android/widget/TextView.md)!:The text view. |
| `buffer` | [Spannable](../android/text/Spannable.md)!:The text buffer. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the event was handled. |
