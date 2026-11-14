Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ArrowKeyMovementMethod

Kotlin | [Java](../android/text/method/ArrowKeyMovementMethod.md)
| --- | --- |

```
open class ArrowKeyMovementMethod : BaseMovementMethod, MovementMethod
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.text.method.BaseMovementMethod](../android/text/method/BaseMovementMethod.md) ||
| | ↳ | [android.text.method.ArrowKeyMovementMethod](../android/text/method/ArrowKeyMovementMethod.md) |

A movement method that provides cursor movement and selection. Supports displaying the context menu on DPad Center.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/text/method/ArrowKeyMovementMethod#ArrowKeyMovementMethod()()` <br /> |

| Public methods ||
|---|---|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/text/method/ArrowKeyMovementMethod#canSelectArbitrarily()()` Returns true if this movement method allows arbitrary selection of any text; false if it has no selection (like a movement method that only scrolls) or a constrained selection (for example limited to links. The "Select All" menu item is disabled if arbitrary selection is not allowed. |
| open static [MovementMethod](../android/text/method/MovementMethod.md)! | `https://developer.android.com/reference/kotlin/android/text/method/ArrowKeyMovementMethod#getInstance()()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/text/method/ArrowKeyMovementMethod#initialize(android.widget.TextView,%20android.text.Spannable)(widget: https://developer.android.com/reference/kotlin/android/widget/TextView.html#!, text: https://developer.android.com/reference/kotlin/android/text/Spannable.html#!)` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/text/method/ArrowKeyMovementMethod#nextParagraph(android.widget.TextView,%20android.text.Spannable)(widget: https://developer.android.com/reference/kotlin/android/widget/TextView.html#, buffer: https://developer.android.com/reference/kotlin/android/text/Spannable.html#)` Performs a next paragraph movement action. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/text/method/ArrowKeyMovementMethod#onTakeFocus(android.widget.TextView,%20android.text.Spannable,%20kotlin.Int)(view: https://developer.android.com/reference/kotlin/android/widget/TextView.html#!, text: https://developer.android.com/reference/kotlin/android/text/Spannable.html#!, dir: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/text/method/ArrowKeyMovementMethod#onTouchEvent(android.widget.TextView,%20android.text.Spannable,%20android.view.MotionEvent)(widget: https://developer.android.com/reference/kotlin/android/widget/TextView.html#!, buffer: https://developer.android.com/reference/kotlin/android/text/Spannable.html#!, event: https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#!)` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/text/method/ArrowKeyMovementMethod#previousParagraph(android.widget.TextView,%20android.text.Spannable)(widget: https://developer.android.com/reference/kotlin/android/widget/TextView.html#, buffer: https://developer.android.com/reference/kotlin/android/text/Spannable.html#)` Performs a previous paragraph movement action. |

| Protected methods ||
|---|---|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/text/method/ArrowKeyMovementMethod#bottom(android.widget.TextView,%20android.text.Spannable)(widget: https://developer.android.com/reference/kotlin/android/widget/TextView.html#!, buffer: https://developer.android.com/reference/kotlin/android/text/Spannable.html#!)` Performs a bottom movement action. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/text/method/ArrowKeyMovementMethod#down(android.widget.TextView,%20android.text.Spannable)(widget: https://developer.android.com/reference/kotlin/android/widget/TextView.html#!, buffer: https://developer.android.com/reference/kotlin/android/text/Spannable.html#!)` Performs a down movement action. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/text/method/ArrowKeyMovementMethod#end(android.widget.TextView,%20android.text.Spannable)(widget: https://developer.android.com/reference/kotlin/android/widget/TextView.html#!, buffer: https://developer.android.com/reference/kotlin/android/text/Spannable.html#!)` Performs an end movement action. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/text/method/ArrowKeyMovementMethod#handleMovementKey(android.widget.TextView,%20android.text.Spannable,%20kotlin.Int,%20kotlin.Int,%20android.view.KeyEvent)(widget: https://developer.android.com/reference/kotlin/android/widget/TextView.html#!, buffer: https://developer.android.com/reference/kotlin/android/text/Spannable.html#!, keyCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, movementMetaState: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, event: https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#!)` Performs a movement key action. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/text/method/ArrowKeyMovementMethod#home(android.widget.TextView,%20android.text.Spannable)(widget: https://developer.android.com/reference/kotlin/android/widget/TextView.html#!, buffer: https://developer.android.com/reference/kotlin/android/text/Spannable.html#!)` Performs a home movement action. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/text/method/ArrowKeyMovementMethod#left(android.widget.TextView,%20android.text.Spannable)(widget: https://developer.android.com/reference/kotlin/android/widget/TextView.html#!, buffer: https://developer.android.com/reference/kotlin/android/text/Spannable.html#!)` Performs a left movement action. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/text/method/ArrowKeyMovementMethod#lineEnd(android.widget.TextView,%20android.text.Spannable)(widget: https://developer.android.com/reference/kotlin/android/widget/TextView.html#!, buffer: https://developer.android.com/reference/kotlin/android/text/Spannable.html#!)` Performs a line-end movement action. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/text/method/ArrowKeyMovementMethod#lineStart(android.widget.TextView,%20android.text.Spannable)(widget: https://developer.android.com/reference/kotlin/android/widget/TextView.html#!, buffer: https://developer.android.com/reference/kotlin/android/text/Spannable.html#!)` Performs a line-start movement action. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/text/method/ArrowKeyMovementMethod#pageDown(android.widget.TextView,%20android.text.Spannable)(widget: https://developer.android.com/reference/kotlin/android/widget/TextView.html#!, buffer: https://developer.android.com/reference/kotlin/android/text/Spannable.html#!)` Performs a page-down movement action. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/text/method/ArrowKeyMovementMethod#pageUp(android.widget.TextView,%20android.text.Spannable)(widget: https://developer.android.com/reference/kotlin/android/widget/TextView.html#!, buffer: https://developer.android.com/reference/kotlin/android/text/Spannable.html#!)` Performs a page-up movement action. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/text/method/ArrowKeyMovementMethod#right(android.widget.TextView,%20android.text.Spannable)(widget: https://developer.android.com/reference/kotlin/android/widget/TextView.html#!, buffer: https://developer.android.com/reference/kotlin/android/text/Spannable.html#!)` Performs a right movement action. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/text/method/ArrowKeyMovementMethod#top(android.widget.TextView,%20android.text.Spannable)(widget: https://developer.android.com/reference/kotlin/android/widget/TextView.html#!, buffer: https://developer.android.com/reference/kotlin/android/text/Spannable.html#!)` Performs a top movement action. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/text/method/ArrowKeyMovementMethod#up(android.widget.TextView,%20android.text.Spannable)(widget: https://developer.android.com/reference/kotlin/android/widget/TextView.html#!, buffer: https://developer.android.com/reference/kotlin/android/text/Spannable.html#!)` Performs an up movement action. |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/text/method/BaseMovementMethod` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/method/BaseMovementMethod#getMovementMetaState(android.text.Spannable,%20android.view.KeyEvent)(buffer: https://developer.android.com/reference/kotlin/android/text/Spannable.html#!, event: https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#!)` Gets the meta state used for movement using the modifiers tracked by the text buffer as well as those present in the key event. The movement meta state excludes the state of locked modifiers or the SHIFT key since they are not used by movement actions (but they may be used for selection). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/text/method/BaseMovementMethod#onGenericMotionEvent(android.widget.TextView,%20android.text.Spannable,%20android.view.MotionEvent)(widget: https://developer.android.com/reference/kotlin/android/widget/TextView.html#!, text: https://developer.android.com/reference/kotlin/android/text/Spannable.html#!, event: https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#!)` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/text/method/BaseMovementMethod#onKeyDown(android.widget.TextView,%20android.text.Spannable,%20kotlin.Int,%20android.view.KeyEvent)(widget: https://developer.android.com/reference/kotlin/android/widget/TextView.html#!, text: https://developer.android.com/reference/kotlin/android/text/Spannable.html#!, keyCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, event: https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#!)` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/text/method/BaseMovementMethod#onKeyOther(android.widget.TextView,%20android.text.Spannable,%20android.view.KeyEvent)(widget: https://developer.android.com/reference/kotlin/android/widget/TextView.html#!, text: https://developer.android.com/reference/kotlin/android/text/Spannable.html#!, event: https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#!)` If the key listener wants to other kinds of key events, return true, otherwise return false and the caller (i.e. the widget host) will handle the key. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/text/method/BaseMovementMethod#onKeyUp(android.widget.TextView,%20android.text.Spannable,%20kotlin.Int,%20android.view.KeyEvent)(widget: https://developer.android.com/reference/kotlin/android/widget/TextView.html#!, text: https://developer.android.com/reference/kotlin/android/text/Spannable.html#!, keyCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, event: https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#!)` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/text/method/BaseMovementMethod#onTrackballEvent(android.widget.TextView,%20android.text.Spannable,%20android.view.MotionEvent)(widget: https://developer.android.com/reference/kotlin/android/widget/TextView.html#!, text: https://developer.android.com/reference/kotlin/android/text/Spannable.html#!, event: https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#!)` <br /> | ||

## Public constructors

### ArrowKeyMovementMethod

```
ArrowKeyMovementMethod()
```

## Public methods

### canSelectArbitrarily

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun canSelectArbitrarily(): Boolean
```

Returns true if this movement method allows arbitrary selection of any text; false if it has no selection (like a movement method that only scrolls) or a constrained selection (for example limited to links. The "Select All" menu item is disabled if arbitrary selection is not allowed.

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getInstance(): MovementMethod!
```

### initialize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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
|---|---|
| `widget` | [TextView](../android/widget/TextView.md): This value cannot be `null`. |
| `buffer` | [Spannable](../android/text/Spannable.md): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the event was handled, otherwise false. |

### onTakeFocus

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onTakeFocus(
    view: TextView!, 
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
|---|---|
| `widget` | [TextView](../android/widget/TextView.md): This value cannot be `null`. |
| `buffer` | [Spannable](../android/text/Spannable.md): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the event was handled, otherwise false. |

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
|---|---|
| `widget` | [TextView](../android/widget/TextView.md)!: The text view. |
| `buffer` | [Spannable](../android/text/Spannable.md)!: The text buffer. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the event was handled. |

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
|---|---|
| `widget` | [TextView](../android/widget/TextView.md)!: The text view. |
| `buffer` | [Spannable](../android/text/Spannable.md)!: The text buffer. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the event was handled. |

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
|---|---|
| `widget` | [TextView](../android/widget/TextView.md)!: The text view. |
| `buffer` | [Spannable](../android/text/Spannable.md)!: The text buffer. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the event was handled. |

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

Performs a movement key action. The default implementation decodes the key down and invokes movement actions such as `https://developer.android.com/reference/kotlin/android/text/method/BaseMovementMethod#down(android.widget.TextView,%20android.text.Spannable)` and `https://developer.android.com/reference/kotlin/android/text/method/BaseMovementMethod#up(android.widget.TextView,%20android.text.Spannable)`. `https://developer.android.com/reference/kotlin/android/text/method/BaseMovementMethod#onKeyDown(android.widget.TextView,%20android.text.Spannable,%20kotlin.Int,%20android.view.KeyEvent)` calls this method once to handle an `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#ACTION_DOWN:kotlin.Int`. `https://developer.android.com/reference/kotlin/android/text/method/BaseMovementMethod#onKeyOther(android.widget.TextView,%20android.text.Spannable,%20android.view.KeyEvent)` calls this method repeatedly to handle each repetition of an `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#ACTION_MULTIPLE:kotlin.Int`.

| Parameters ||
|---|---|
| `widget` | [TextView](../android/widget/TextView.md)!: The text view. |
| `buffer` | [Spannable](../android/text/Spannable.md)!: The text buffer. |
| `keyCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The key code. |
| --- | --- |
| `movementMetaState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The keyboard meta states used for movement. |
| `event` | [KeyEvent](../android/view/KeyEvent.md)!: The key event. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the event was handled. |

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
|---|---|
| `widget` | [TextView](../android/widget/TextView.md)!: The text view. |
| `buffer` | [Spannable](../android/text/Spannable.md)!: The text buffer. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the event was handled. |

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
|---|---|
| `widget` | [TextView](../android/widget/TextView.md)!: The text view. |
| `buffer` | [Spannable](../android/text/Spannable.md)!: The text buffer. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the event was handled. |

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
|---|---|
| `widget` | [TextView](../android/widget/TextView.md)!: The text view. |
| `buffer` | [Spannable](../android/text/Spannable.md)!: The text buffer. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the event was handled. |

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
|---|---|
| `widget` | [TextView](../android/widget/TextView.md)!: The text view. |
| `buffer` | [Spannable](../android/text/Spannable.md)!: The text buffer. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the event was handled. |

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
|---|---|
| `widget` | [TextView](../android/widget/TextView.md)!: The text view. |
| `buffer` | [Spannable](../android/text/Spannable.md)!: The text buffer. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the event was handled. |

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
|---|---|
| `widget` | [TextView](../android/widget/TextView.md)!: The text view. |
| `buffer` | [Spannable](../android/text/Spannable.md)!: The text buffer. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the event was handled. |

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
|---|---|
| `widget` | [TextView](../android/widget/TextView.md)!: The text view. |
| `buffer` | [Spannable](../android/text/Spannable.md)!: The text buffer. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the event was handled. |

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
|---|---|
| `widget` | [TextView](../android/widget/TextView.md)!: The text view. |
| `buffer` | [Spannable](../android/text/Spannable.md)!: The text buffer. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the event was handled. |

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
|---|---|
| `widget` | [TextView](../android/widget/TextView.md)!: The text view. |
| `buffer` | [Spannable](../android/text/Spannable.md)!: The text buffer. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the event was handled. |
