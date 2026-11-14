# HandwritingGesture

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# HandwritingGesture

Kotlin| [Java](../android/view/inputmethod/HandwritingGesture.md) 
| --- | --- |

```
abstract class HandwritingGesture
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.inputmethod.HandwritingGesture](../android/view/inputmethod/HandwritingGesture.md) |

| Known Direct Subclasses [InsertGesture](../android/view/inputmethod/InsertGesture.md), [InsertModeGesture](../android/view/inputmethod/InsertModeGesture.md), [JoinOrSplitGesture](../android/view/inputmethod/JoinOrSplitGesture.md), [PreviewableHandwritingGesture](../android/view/inputmethod/PreviewableHandwritingGesture.md), [RemoveSpaceGesture](../android/view/inputmethod/RemoveSpaceGesture.md) |----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [InsertGesture](../android/view/inputmethod/InsertGesture.md) | A sub-class of [HandwritingGesture](../android/view/inputmethod/HandwritingGesture.md) for inserting text at the defined insertion point. | | [InsertModeGesture](../android/view/inputmethod/InsertModeGesture.md) | A sub-class of [HandwritingGesture](../android/view/inputmethod/HandwritingGesture.md) for starting an insert mode which inserts a space in the editor to let users hand write freely at the designated insertion point. | | [JoinOrSplitGesture](../android/view/inputmethod/JoinOrSplitGesture.md) | A subclass of [HandwritingGesture](../android/view/inputmethod/HandwritingGesture.md) for deleting or inserting whitespace in text. | | [PreviewableHandwritingGesture](../android/view/inputmethod/PreviewableHandwritingGesture.md) | A [HandwritingGesture](../android/view/inputmethod/HandwritingGesture.md) that can be [previewed](../android/view/inputmethod/InputConnection.md)). | | [RemoveSpaceGesture](../android/view/inputmethod/RemoveSpaceGesture.md) | A subclass of [HandwritingGesture](../android/view/inputmethod/HandwritingGesture.md) for removing whitespace from text. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [DeleteGesture](../android/view/inputmethod/DeleteGesture.md), [DeleteRangeGesture](../android/view/inputmethod/DeleteRangeGesture.md), [SelectGesture](../android/view/inputmethod/SelectGesture.md), [SelectRangeGesture](../android/view/inputmethod/SelectRangeGesture.md) |------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [DeleteGesture](../android/view/inputmethod/DeleteGesture.md) | A sub-class of [HandwritingGesture](../android/view/inputmethod/HandwritingGesture.md) for deleting an area of text using single rectangle. | | [DeleteRangeGesture](../android/view/inputmethod/DeleteRangeGesture.md) | A subclass of [HandwritingGesture](../android/view/inputmethod/HandwritingGesture.md) for deleting a range of text by defining start and end rectangles. | | [SelectGesture](../android/view/inputmethod/SelectGesture.md) | A sub-class of [HandwritingGesture](../android/view/inputmethod/HandwritingGesture.md) for selecting an area of text using single rectangle. | | [SelectRangeGesture](../android/view/inputmethod/SelectRangeGesture.md) | A subclass of [HandwritingGesture](../android/view/inputmethod/HandwritingGesture.md) for selecting a range of text by defining start and end rectangles. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Base class for stylus handwriting gestures.

During a stylus handwriting session, user can perform a stylus gesture operation like [SelectGesture](../android/view/inputmethod/SelectGesture.md), [DeleteGesture](../android/view/inputmethod/DeleteGesture.md), [InsertGesture](../android/view/inputmethod/InsertGesture.md) on an area of text. IME is responsible for listening to stylus [MotionEvent](../android/view/MotionEvent.md) s using [InputMethodService.onStylusHandwritingMotionEvent](../android/inputmethodservice/InputMethodService.md))and interpret if it can translate to a gesture operation.

While creating gesture operations [SelectGesture](../android/view/inputmethod/SelectGesture.md) and [DeleteGesture](../android/view/inputmethod/DeleteGesture.md),`Granularity`helps pick the correct granular level of text like word level [GRANULARITY_WORD](../android/view/inputmethod/HandwritingGesture.md), or character level [GRANULARITY_CHARACTER](../android/view/inputmethod/HandwritingGesture.md).

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GRANULARITY_CHARACTER](../android/view/inputmethod/HandwritingGesture.md) Operate on text per character basis. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GRANULARITY_WORD](../android/view/inputmethod/HandwritingGesture.md) Operate text per word basis. |

| Public methods ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getFallbackText](../android/view/inputmethod/HandwritingGesture.md))`()` The fallback text that will be committed at current cursor position if there is no applicable text beneath the area of gesture. |

## Constants

### GRANULARITY_CHARACTER

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GRANULARITY_CHARACTER: Int
```

Operate on text per character basis. i.e. each character is selected based on its intersection with selection rectangle.

Strategy of operating at a granular level is maintained in the UI toolkit. A character/word/line is included if its center is within the gesture rectangle. e.g. if a selection [RectF](../android/graphics/RectF.md) with [GRANULARITY_CHARACTER](../android/view/inputmethod/HandwritingGesture.md) includes width-wise center of the character, it should be selected. Similarly, text in a line should be included in the operation if rectangle includes line height center. 

 Value: 2

### GRANULARITY_WORD

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GRANULARITY_WORD: Int
```

Operate text per word basis. e.g. if selection includes width-wise center of the word, whole word is selected.

Strategy of operating at a granular level is maintained in the UI toolkit. A character/word/line is included if its center is within the gesture rectangle. e.g. if a selection [RectF](../android/graphics/RectF.md) with [GRANULARITY_WORD](../android/view/inputmethod/HandwritingGesture.md) includes width-wise center of the word, it should be selected. Similarly, text in a line should be included in the operation if rectangle includes line height center.
Refer to https://www.unicode.org/reports/tr29/#Word_Boundaries for more detail on how word breaks are decided. 

 Value: 1

## Public methods

### getFallbackText

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFallbackText(): String?
```

The fallback text that will be committed at current cursor position if there is no applicable text beneath the area of gesture. For example, select can fail if gesture is drawn over area that has no text beneath. example 2: join can fail if the gesture is drawn over text but there is no whitespace.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | This value may be`null`. |
