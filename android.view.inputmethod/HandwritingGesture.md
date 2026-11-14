# HandwritingGesture

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# HandwritingGesture

Kotlin| [Java](https://developer.android.com/reference/android/view/inputmethod/HandwritingGesture "View this page in Java") 

```
abstract class HandwritingGesture
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.view.inputmethod.HandwritingGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/HandwritingGesture#) |

| Known Direct Subclasses [InsertGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/InsertGesture), [InsertModeGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/InsertModeGesture), [JoinOrSplitGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/JoinOrSplitGesture), [PreviewableHandwritingGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/PreviewableHandwritingGesture), [RemoveSpaceGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/RemoveSpaceGesture) |----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [InsertGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/InsertGesture) | A sub-class of [HandwritingGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/HandwritingGesture#) for inserting text at the defined insertion point. | | [InsertModeGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/InsertModeGesture) | A sub-class of [HandwritingGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/HandwritingGesture#) for starting an insert mode which inserts a space in the editor to let users hand write freely at the designated insertion point. | | [JoinOrSplitGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/JoinOrSplitGesture) | A subclass of [HandwritingGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/HandwritingGesture#) for deleting or inserting whitespace in text. | | [PreviewableHandwritingGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/PreviewableHandwritingGesture) | A [HandwritingGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/HandwritingGesture#) that can be [previewed](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#previewHandwritingGesture(android.view.inputmethod.PreviewableHandwritingGesture,%20android.os.CancellationSignal)). | | [RemoveSpaceGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/RemoveSpaceGesture) | A subclass of [HandwritingGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/HandwritingGesture#) for removing whitespace from text. | |

| Known Indirect Subclasses [DeleteGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/DeleteGesture), [DeleteRangeGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/DeleteRangeGesture), [SelectGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/SelectGesture), [SelectRangeGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/SelectRangeGesture) |------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [DeleteGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/DeleteGesture) | A sub-class of [HandwritingGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/HandwritingGesture#) for deleting an area of text using single rectangle. | | [DeleteRangeGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/DeleteRangeGesture) | A subclass of [HandwritingGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/HandwritingGesture#) for deleting a range of text by defining start and end rectangles. | | [SelectGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/SelectGesture) | A sub-class of [HandwritingGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/HandwritingGesture#) for selecting an area of text using single rectangle. | | [SelectRangeGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/SelectRangeGesture) | A subclass of [HandwritingGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/HandwritingGesture#) for selecting a range of text by defining start and end rectangles. | |

Base class for stylus handwriting gestures.

During a stylus handwriting session, user can perform a stylus gesture operation like [SelectGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/SelectGesture), [DeleteGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/DeleteGesture), [InsertGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/InsertGesture) on an area of text. IME is responsible for listening to stylus [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#) s using [InputMethodService.onStylusHandwritingMotionEvent](https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService.html#onStylusHandwritingMotionEvent(android.view.MotionEvent))and interpret if it can translate to a gesture operation.

While creating gesture operations [SelectGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/SelectGesture) and [DeleteGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/DeleteGesture),`Granularity`helps pick the correct granular level of text like word level [GRANULARITY_WORD](https://developer.android.com/reference/kotlin/android/view/inputmethod/HandwritingGesture#GRANULARITY_WORD:kotlin.Int), or character level [GRANULARITY_CHARACTER](https://developer.android.com/reference/kotlin/android/view/inputmethod/HandwritingGesture#GRANULARITY_CHARACTER:kotlin.Int).

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GRANULARITY_CHARACTER](https://developer.android.com/reference/kotlin/android/view/inputmethod/HandwritingGesture#GRANULARITY_CHARACTER:kotlin.Int) Operate on text per character basis. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GRANULARITY_WORD](https://developer.android.com/reference/kotlin/android/view/inputmethod/HandwritingGesture#GRANULARITY_WORD:kotlin.Int) Operate text per word basis. |

| Public methods ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getFallbackText](https://developer.android.com/reference/kotlin/android/view/inputmethod/HandwritingGesture#getFallbackText())`()` The fallback text that will be committed at current cursor position if there is no applicable text beneath the area of gesture. |

## Constants

### GRANULARITY_CHARACTER

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GRANULARITY_CHARACTER: Int
```

Operate on text per character basis. i.e. each character is selected based on its intersection with selection rectangle.

Strategy of operating at a granular level is maintained in the UI toolkit. A character/word/line is included if its center is within the gesture rectangle. e.g. if a selection [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF.html#) with [GRANULARITY_CHARACTER](https://developer.android.com/reference/kotlin/android/view/inputmethod/HandwritingGesture#GRANULARITY_CHARACTER:kotlin.Int) includes width-wise center of the character, it should be selected. Similarly, text in a line should be included in the operation if rectangle includes line height center. 

 Value: 2

### GRANULARITY_WORD

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GRANULARITY_WORD: Int
```

Operate text per word basis. e.g. if selection includes width-wise center of the word, whole word is selected.

Strategy of operating at a granular level is maintained in the UI toolkit. A character/word/line is included if its center is within the gesture rectangle. e.g. if a selection [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF.html#) with [GRANULARITY_WORD](https://developer.android.com/reference/kotlin/android/view/inputmethod/HandwritingGesture#GRANULARITY_WORD:kotlin.Int) includes width-wise center of the word, it should be selected. Similarly, text in a line should be included in the operation if rectangle includes line height center.
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
