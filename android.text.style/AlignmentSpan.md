# AlignmentSpan

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AlignmentSpan

Kotlin| [Java](https://developer.android.com/reference/android/text/style/AlignmentSpan "View this page in Java") 
| --- | --- |

```
interface AlignmentSpan : ParagraphStyle
```

| [android.text.style.AlignmentSpan](https://developer.android.com/reference/kotlin/android/text/style/AlignmentSpan#) |

| Known Direct Subclasses [AlignmentSpan.Standard](https://developer.android.com/reference/kotlin/android/text/style/AlignmentSpan.Standard) |--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------| | [AlignmentSpan.Standard](https://developer.android.com/reference/kotlin/android/text/style/AlignmentSpan.Standard) | Default implementation of the [AlignmentSpan](https://developer.android.com/reference/kotlin/android/text/style/AlignmentSpan#). | |
| --- | --- | --- | --- | --- | --- | --- |

Span that allows defining the alignment of text at the paragraph level.

## Summary

| Nested classes ||
|------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [Standard](https://developer.android.com/reference/kotlin/android/text/style/AlignmentSpan.Standard) Default implementation of the [AlignmentSpan](https://developer.android.com/reference/kotlin/android/text/style/AlignmentSpan#). |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Layout.Alignment](https://developer.android.com/reference/kotlin/android/text/Layout.Alignment.html#)! | [getAlignment](https://developer.android.com/reference/kotlin/android/text/style/AlignmentSpan#getAlignment())`()` Returns the alignment of the text. |

## Public methods

### getAlignment

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getAlignment(): Layout.Alignment!
```

Returns the alignment of the text.

| Return ||
|---------------------------------------------------------------------------------------------------------|--------------------|
| [Layout.Alignment](https://developer.android.com/reference/kotlin/android/text/Layout.Alignment.html#)! | the text alignment |
