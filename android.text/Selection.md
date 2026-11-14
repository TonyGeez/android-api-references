Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Selection

Kotlin | [Java](https://developer.android.com/reference/android/text/Selection "View this page in Java")

```
open class Selection
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.text.Selection](https://developer.android.com/reference/kotlin/android/text/Selection#) |

Utility class for manipulating cursors and selections in CharSequences. A cursor is a selection where the start and end are at the same offset.

## Summary

| Public methods ||
|---|---|
| open static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/text/Selection#extendDown(android.text.Spannable,%20android.text.Layout)(text: https://developer.android.com/reference/kotlin/android/text/Spannable!, layout: https://developer.android.com/reference/kotlin/android/text/Layout!)` Move the selection end to the buffer offset physically below the current selection end. |
| open static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/text/Selection#extendLeft(android.text.Spannable,%20android.text.Layout)(text: https://developer.android.com/reference/kotlin/android/text/Spannable!, layout: https://developer.android.com/reference/kotlin/android/text/Layout!)` Move the selection end to the buffer offset physically to the left of the current selection end. |
| open static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/text/Selection#extendRight(android.text.Spannable,%20android.text.Layout)(text: https://developer.android.com/reference/kotlin/android/text/Spannable!, layout: https://developer.android.com/reference/kotlin/android/text/Layout!)` Move the selection end to the buffer offset physically to the right of the current selection end. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/text/Selection#extendSelection(android.text.Spannable,%20kotlin.Int)(text: https://developer.android.com/reference/kotlin/android/text/Spannable!, index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Move the selection edge to offset `index`. |
| open static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/text/Selection#extendToLeftEdge(android.text.Spannable,%20android.text.Layout)(text: https://developer.android.com/reference/kotlin/android/text/Spannable!, layout: https://developer.android.com/reference/kotlin/android/text/Layout!)` <br /> |
| open static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/text/Selection#extendToParagraphEnd(android.text.Spannable)(text: https://developer.android.com/reference/kotlin/android/text/Spannable)` Extend the selection to the closest paragraph end offset. |
| open static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/text/Selection#extendToParagraphStart(android.text.Spannable)(text: https://developer.android.com/reference/kotlin/android/text/Spannable)` Extend the selection to the closest paragraph start offset. |
| open static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/text/Selection#extendToRightEdge(android.text.Spannable,%20android.text.Layout)(text: https://developer.android.com/reference/kotlin/android/text/Spannable!, layout: https://developer.android.com/reference/kotlin/android/text/Layout!)` <br /> |
| open static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/text/Selection#extendUp(android.text.Spannable,%20android.text.Layout)(text: https://developer.android.com/reference/kotlin/android/text/Spannable!, layout: https://developer.android.com/reference/kotlin/android/text/Layout!)` Move the selection end to the buffer offset physically above the current selection end. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/Selection#getSelectionEnd(kotlin.CharSequence)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!)` Return the offset of the selection edge or cursor, or -1 if there is no selection or cursor. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/Selection#getSelectionStart(kotlin.CharSequence)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!)` Return the offset of the selection anchor or cursor, or -1 if there is no selection or cursor. |
| open static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/text/Selection#moveDown(android.text.Spannable,%20android.text.Layout)(text: https://developer.android.com/reference/kotlin/android/text/Spannable!, layout: https://developer.android.com/reference/kotlin/android/text/Layout!)` Move the cursor to the buffer offset physically below the current offset, to the end of the buffer if it is on the bottom line but not at the end, or return false if the cursor is already at the end of the buffer. |
| open static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/text/Selection#moveLeft(android.text.Spannable,%20android.text.Layout)(text: https://developer.android.com/reference/kotlin/android/text/Spannable!, layout: https://developer.android.com/reference/kotlin/android/text/Layout!)` Move the cursor to the buffer offset physically to the left of the current offset, or return false if the cursor is already at the left edge of the line and there is not another line to move it to. |
| open static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/text/Selection#moveRight(android.text.Spannable,%20android.text.Layout)(text: https://developer.android.com/reference/kotlin/android/text/Spannable!, layout: https://developer.android.com/reference/kotlin/android/text/Layout!)` Move the cursor to the buffer offset physically to the right of the current offset, or return false if the cursor is already at at the right edge of the line and there is not another line to move it to. |
| open static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/text/Selection#moveToLeftEdge(android.text.Spannable,%20android.text.Layout)(text: https://developer.android.com/reference/kotlin/android/text/Spannable!, layout: https://developer.android.com/reference/kotlin/android/text/Layout!)` <br /> |
| open static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/text/Selection#moveToParagraphEnd(android.text.Spannable,%20android.text.Layout)(text: https://developer.android.com/reference/kotlin/android/text/Spannable, layout: https://developer.android.com/reference/kotlin/android/text/Layout)` Move the cursor to the closest paragraph end offset. |
| open static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/text/Selection#moveToParagraphStart(android.text.Spannable,%20android.text.Layout)(text: https://developer.android.com/reference/kotlin/android/text/Spannable, layout: https://developer.android.com/reference/kotlin/android/text/Layout)` Move the cursor to the closest paragraph start offset. |
| open static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/text/Selection#moveToRightEdge(android.text.Spannable,%20android.text.Layout)(text: https://developer.android.com/reference/kotlin/android/text/Spannable!, layout: https://developer.android.com/reference/kotlin/android/text/Layout!)` <br /> |
| open static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/text/Selection#moveUp(android.text.Spannable,%20android.text.Layout)(text: https://developer.android.com/reference/kotlin/android/text/Spannable!, layout: https://developer.android.com/reference/kotlin/android/text/Layout!)` Move the cursor to the buffer offset physically above the current offset, to the beginning if it is on the top line but not at the start, or return false if the cursor is already on the top line. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/text/Selection#removeSelection(android.text.Spannable)(text: https://developer.android.com/reference/kotlin/android/text/Spannable!)` Remove the selection or cursor, if any, from the text. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/text/Selection#selectAll(android.text.Spannable)(text: https://developer.android.com/reference/kotlin/android/text/Spannable!)` Select the entire text. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/text/Selection#setSelection(android.text.Spannable,%20kotlin.Int)(text: https://developer.android.com/reference/kotlin/android/text/Spannable!, index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Move the cursor to offset `index`. |
| open static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/text/Selection#setSelection(android.text.Spannable,%20kotlin.Int,%20kotlin.Int)(text: https://developer.android.com/reference/kotlin/android/text/Spannable!, start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, stop: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set the selection anchor to `start` and the selection edge to `stop`. |

| Properties ||
|---|---|
| static [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | `https://developer.android.com/reference/kotlin/android/text/Selection#SELECTION_END:kotlin.Any` <br /> |
| static [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | `https://developer.android.com/reference/kotlin/android/text/Selection#SELECTION_START:kotlin.Any` <br /> |

## Public methods

### extendDown

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun extendDown(
    text: Spannable!, 
    layout: Layout!
): Boolean
```

Move the selection end to the buffer offset physically below the current selection end.

### extendLeft

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun extendLeft(
    text: Spannable!, 
    layout: Layout!
): Boolean
```

Move the selection end to the buffer offset physically to the left of the current selection end.

### extendRight

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun extendRight(
    text: Spannable!, 
    layout: Layout!
): Boolean
```

Move the selection end to the buffer offset physically to the right of the current selection end.

### extendSelection

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun extendSelection(
    text: Spannable!, 
    index: Int
): Unit
```

Move the selection edge to offset `index`.

### extendToLeftEdge

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun extendToLeftEdge(
    text: Spannable!, 
    layout: Layout!
): Boolean
```

### extendToParagraphEnd

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun extendToParagraphEnd(text: Spannable): Boolean
```

Extend the selection to the closest paragraph end offset.

| Parameters ||
|---|---|
| `text` | [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable): the spannable text. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the selection is extended, otherwise false |

### extendToParagraphStart

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun extendToParagraphStart(text: Spannable): Boolean
```

Extend the selection to the closest paragraph start offset.

| Parameters ||
|---|---|
| `text` | [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable): the spannable text. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the selection is extended, otherwise false |

### extendToRightEdge

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun extendToRightEdge(
    text: Spannable!, 
    layout: Layout!
): Boolean
```

### extendUp

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun extendUp(
    text: Spannable!, 
    layout: Layout!
): Boolean
```

Move the selection end to the buffer offset physically above the current selection end.

### getSelectionEnd

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getSelectionEnd(text: CharSequence!): Int
```

Return the offset of the selection edge or cursor, or -1 if there is no selection or cursor.

### getSelectionStart

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getSelectionStart(text: CharSequence!): Int
```

Return the offset of the selection anchor or cursor, or -1 if there is no selection or cursor.

### moveDown

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun moveDown(
    text: Spannable!, 
    layout: Layout!
): Boolean
```

Move the cursor to the buffer offset physically below the current offset, to the end of the buffer if it is on the bottom line but not at the end, or return false if the cursor is already at the end of the buffer.

### moveLeft

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun moveLeft(
    text: Spannable!, 
    layout: Layout!
): Boolean
```

Move the cursor to the buffer offset physically to the left of the current offset, or return false if the cursor is already at the left edge of the line and there is not another line to move it to.

### moveRight

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun moveRight(
    text: Spannable!, 
    layout: Layout!
): Boolean
```

Move the cursor to the buffer offset physically to the right of the current offset, or return false if the cursor is already at at the right edge of the line and there is not another line to move it to.

### moveToLeftEdge

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun moveToLeftEdge(
    text: Spannable!, 
    layout: Layout!
): Boolean
```

### moveToParagraphEnd

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun moveToParagraphEnd(
    text: Spannable, 
    layout: Layout
): Boolean
```

Move the cursor to the closest paragraph end offset.

| Parameters ||
|---|---|
| `text` | [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable): the spannable text. This value cannot be `null`. |
| `layout` | [Layout](https://developer.android.com/reference/kotlin/android/text/Layout): layout to be used for drawing. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the cursor is moved, otherwise false. |

### moveToParagraphStart

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun moveToParagraphStart(
    text: Spannable, 
    layout: Layout
): Boolean
```

Move the cursor to the closest paragraph start offset.

| Parameters ||
|---|---|
| `text` | [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable): the spannable text. This value cannot be `null`. |
| `layout` | [Layout](https://developer.android.com/reference/kotlin/android/text/Layout): layout to be used for drawing. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the cursor is moved, otherwise false. |

### moveToRightEdge

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun moveToRightEdge(
    text: Spannable!, 
    layout: Layout!
): Boolean
```

### moveUp

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun moveUp(
    text: Spannable!, 
    layout: Layout!
): Boolean
```

Move the cursor to the buffer offset physically above the current offset, to the beginning if it is on the top line but not at the start, or return false if the cursor is already on the top line.

### removeSelection

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun removeSelection(text: Spannable!): Unit
```

Remove the selection or cursor, if any, from the text.

### selectAll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun selectAll(text: Spannable!): Unit
```

Select the entire text.

### setSelection

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun setSelection(
    text: Spannable!, 
    index: Int
): Unit
```

Move the cursor to offset `index`.

### setSelection

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun setSelection(
    text: Spannable!, 
    start: Int, 
    stop: Int
): Unit
```

Set the selection anchor to `start` and the selection edge to `stop`.

## Properties

### SELECTION_END

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SELECTION_END: Any!
```

### SELECTION_START

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SELECTION_START: Any!
```
