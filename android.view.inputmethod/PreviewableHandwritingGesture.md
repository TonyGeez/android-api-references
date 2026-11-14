# PreviewableHandwritingGesture

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PreviewableHandwritingGesture

Kotlin| [Java](PreviewableHandwritingGesture.md) 
| --- | --- |

```
abstract class PreviewableHandwritingGesture : HandwritingGesture
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.view.inputmethod.HandwritingGesture](HandwritingGesture.md) ||
| | ↳ | [android.view.inputmethod.PreviewableHandwritingGesture](PreviewableHandwritingGesture.md) |

| Known Direct Subclasses [DeleteGesture](DeleteGesture.md), [DeleteRangeGesture](DeleteRangeGesture.md), [SelectGesture](SelectGesture.md), [SelectRangeGesture](SelectRangeGesture.md) |------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [DeleteGesture](DeleteGesture.md) | A sub-class of [HandwritingGesture](HandwritingGesture.md) for deleting an area of text using single rectangle. | | [DeleteRangeGesture](DeleteRangeGesture.md) | A subclass of [HandwritingGesture](HandwritingGesture.md) for deleting a range of text by defining start and end rectangles. | | [SelectGesture](SelectGesture.md) | A sub-class of [HandwritingGesture](HandwritingGesture.md) for selecting an area of text using single rectangle. | | [SelectRangeGesture](SelectRangeGesture.md) | A subclass of [HandwritingGesture](HandwritingGesture.md) for selecting a range of text by defining start and end rectangles. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A [HandwritingGesture](HandwritingGesture.md) that can be [previewed](InputConnection.md)). Note: An editor might only implement a subset of gesture previews and declares the supported ones via [EditorInfo.getSupportedHandwritingGesturePreviews](EditorInfo.md)).

## Summary

| Inherited constants ||
|---|---|
| From class [HandwritingGesture](HandwritingGesture.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GRANULARITY_CHARACTER](HandwritingGesture.md) <br /> Operate on text per character basis. i.e. each character is selected based on its intersection with selection rectangle. Strategy of operating at a granular level is maintained in the UI toolkit. A character/word/line is included if its center is within the gesture rectangle. e.g. if a selection [RectF](../android.graphics/RectF.md) with [GRANULARITY_CHARACTER](HandwritingGesture.md) includes width-wise center of the character, it should be selected. Similarly, text in a line should be included in the operation if rectangle includes line height center. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GRANULARITY_WORD](HandwritingGesture.md) <br /> Operate text per word basis. e.g. if selection includes width-wise center of the word, whole word is selected. Strategy of operating at a granular level is maintained in the UI toolkit. A character/word/line is included if its center is within the gesture rectangle. e.g. if a selection [RectF](../android.graphics/RectF.md) with [GRANULARITY_WORD](HandwritingGesture.md) includes width-wise center of the word, it should be selected. Similarly, text in a line should be included in the operation if rectangle includes line height center. Refer to https://www.unicode.org/reports/tr29/#Word_Boundaries for more detail on how word breaks are decided. <br /> | ||

| Inherited functions ||
|---|---|
| From class [HandwritingGesture](HandwritingGesture.md) |-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getFallbackText](HandwritingGesture.md))`()` <br /> The fallback text that will be committed at current cursor position if there is no applicable text beneath the area of gesture. For example, select can fail if gesture is drawn over area that has no text beneath. example 2: join can fail if the gesture is drawn over text but there is no whitespace. <br /> | ||
