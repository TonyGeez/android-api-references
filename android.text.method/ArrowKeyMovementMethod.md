Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ArrowKeyMovementMethod

Kotlin | [Java](ArrowKeyMovementMethod.md)
| --- | --- |

```
open class ArrowKeyMovementMethod : BaseMovementMethod, MovementMethod
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.text.method.BaseMovementMethod](BaseMovementMethod.md) ||
| | ↳ | [android.text.method.ArrowKeyMovementMethod](ArrowKeyMovementMethod.md) |

A movement method that provides cursor movement and selection. Supports displaying the context menu on DPad Center.

## Summary

| Public constructors ||
|---|---|
| ArrowKeyMovementMethod <br /> |

| Public methods ||
|---|---|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | canSelectArbitrarily Returns true if this movement method allows arbitrary selection of any text; false if it has no selection (like a movement method that only scrolls) or a constrained selection (for example limited to links. The "Select All" menu item is disabled if arbitrary selection is not allowed. |
| open static [MovementMethod](MovementMethod.md)! | getInstance <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | initialize <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | nextParagraph Performs a next paragraph movement action. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onTakeFocus <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | onTouchEvent <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | previousParagraph Performs a previous paragraph movement action. |

| Protected methods ||
|---|---|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | bottom Performs a bottom movement action. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | down Performs a down movement action. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | end Performs an end movement action. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | handleMovementKey Performs a movement key action. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | home Performs a home movement action. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | left Performs a left movement action. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | lineEnd Performs a line-end movement action. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | lineStart Performs a line-start movement action. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | pageDown Performs a page-down movement action. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | pageUp Performs a page-up movement action. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | right Performs a right movement action. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | top Performs a top movement action. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | up Performs an up movement action. |

| Inherited functions ||
|---|---|
| From class BaseMovementMethod |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getMovementMetaState Gets the meta state used for movement using the modifiers tracked by the text buffer as well as those present in the key event. The movement meta state excludes the state of locked modifiers or the SHIFT key since they are not used by movement actions (but they may be used for selection). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | onGenericMotionEvent <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | onKeyDown <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | onKeyOther If the key listener wants to other kinds of key events, return true, otherwise return false and the caller (i.e. the widget host) will handle the key. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | onKeyUp <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | onTrackballEvent <br /> | ||

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
| `widget` | [TextView](../android.widget/TextView.md): This value cannot be `null`. |
| `buffer` | [Spannable](../android.text/Spannable.md): This value cannot be `null`. |

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
| `widget` | [TextView](../android.widget/TextView.md): This value cannot be `null`. |
| `buffer` | [Spannable](../android.text/Spannable.md): This value cannot be `null`. |

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
| `widget` | [TextView](../android.widget/TextView.md)!: The text view. |
| `buffer` | [Spannable](../android.text/Spannable.md)!: The text buffer. |

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
| `widget` | [TextView](../android.widget/TextView.md)!: The text view. |
| `buffer` | [Spannable](../android.text/Spannable.md)!: The text buffer. |

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
| `widget` | [TextView](../android.widget/TextView.md)!: The text view. |
| `buffer` | [Spannable](../android.text/Spannable.md)!: The text buffer. |

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

Performs a movement key action. The default implementation decodes the key down and invokes movement actions such as down and up. onKeyDown calls this method once to handle an `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#ACTION_DOWN:kotlin.Int`. onKeyOther calls this method repeatedly to handle each repetition of an `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#ACTION_MULTIPLE:kotlin.Int`.

| Parameters ||
|---|---|
| `widget` | [TextView](../android.widget/TextView.md)!: The text view. |
| `buffer` | [Spannable](../android.text/Spannable.md)!: The text buffer. |
| `keyCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The key code. |
| --- | --- |
| `movementMetaState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The keyboard meta states used for movement. |
| `event` | [KeyEvent](../android.view/KeyEvent.md)!: The key event. |

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
| `widget` | [TextView](../android.widget/TextView.md)!: The text view. |
| `buffer` | [Spannable](../android.text/Spannable.md)!: The text buffer. |

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
| `widget` | [TextView](../android.widget/TextView.md)!: The text view. |
| `buffer` | [Spannable](../android.text/Spannable.md)!: The text buffer. |

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
| `widget` | [TextView](../android.widget/TextView.md)!: The text view. |
| `buffer` | [Spannable](../android.text/Spannable.md)!: The text buffer. |

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
| `widget` | [TextView](../android.widget/TextView.md)!: The text view. |
| `buffer` | [Spannable](../android.text/Spannable.md)!: The text buffer. |

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
| `widget` | [TextView](../android.widget/TextView.md)!: The text view. |
| `buffer` | [Spannable](../android.text/Spannable.md)!: The text buffer. |

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
| `widget` | [TextView](../android.widget/TextView.md)!: The text view. |
| `buffer` | [Spannable](../android.text/Spannable.md)!: The text buffer. |

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
| `widget` | [TextView](../android.widget/TextView.md)!: The text view. |
| `buffer` | [Spannable](../android.text/Spannable.md)!: The text buffer. |

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
| `widget` | [TextView](../android.widget/TextView.md)!: The text view. |
| `buffer` | [Spannable](../android.text/Spannable.md)!: The text buffer. |

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
| `widget` | [TextView](../android.widget/TextView.md)!: The text view. |
| `buffer` | [Spannable](../android.text/Spannable.md)!: The text buffer. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the event was handled. |
