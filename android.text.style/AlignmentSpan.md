# AlignmentSpan

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AlignmentSpan

Kotlin| [Java](../android/text/style/AlignmentSpan.md) 
| --- | --- |

```
interface AlignmentSpan : ParagraphStyle
```

| [android.text.style.AlignmentSpan](../android/text/style/AlignmentSpan.md) |

| Known Direct Subclasses [AlignmentSpan.Standard](../android/text/style/AlignmentSpan.Standard.md) |--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------| | [AlignmentSpan.Standard](../android/text/style/AlignmentSpan.Standard.md) | Default implementation of the [AlignmentSpan](../android/text/style/AlignmentSpan.md). | |
| --- | --- | --- | --- | --- | --- | --- |

Span that allows defining the alignment of text at the paragraph level.

## Summary

| Nested classes ||
|------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [Standard](../android/text/style/AlignmentSpan.Standard.md) Default implementation of the [AlignmentSpan](../android/text/style/AlignmentSpan.md). |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Layout.Alignment](../android/text/Layout.Alignment.md)! | [getAlignment](../android/text/style/AlignmentSpan.md))`()` Returns the alignment of the text. |

## Public methods

### getAlignment

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getAlignment(): Layout.Alignment!
```

Returns the alignment of the text.

| Return ||
|---------------------------------------------------------------------------------------------------------|--------------------|
| [Layout.Alignment](../android/text/Layout.Alignment.md)! | the text alignment |
