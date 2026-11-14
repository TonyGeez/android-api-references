# WrapTogetherSpan

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WrapTogetherSpan

Kotlin| [Java](../android/text/style/WrapTogetherSpan.md) 
| --- | --- |

```
interface WrapTogetherSpan : ParagraphStyle
```

| [android.text.style.WrapTogetherSpan](../android/text/style/WrapTogetherSpan.md) |

| Known Direct Subclasses [LeadingMarginSpan.LeadingMarginSpan2](../android/text/style/LeadingMarginSpan.LeadingMarginSpan2.md), [LineHeightSpan](../android/text/style/LineHeightSpan.md) |------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [LeadingMarginSpan.LeadingMarginSpan2](../android/text/style/LeadingMarginSpan.LeadingMarginSpan2.md) | An extended version of [LeadingMarginSpan](../android/text/style/LeadingMarginSpan.md), which allows the implementor to specify the number of lines of the paragraph to which this object is attached that the "first line of paragraph" margin width will be applied to. | | [LineHeightSpan](../android/text/style/LineHeightSpan.md) | The classes that affect the line height of paragraph should implement this interface. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [DrawableMarginSpan](../android/text/style/DrawableMarginSpan.md), [IconMarginSpan](../android/text/style/IconMarginSpan.md), [LineHeightSpan.Standard](../android/text/style/LineHeightSpan.Standard.md), [LineHeightSpan.WithDensity](../android/text/style/LineHeightSpan.WithDensity.md) |----------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [DrawableMarginSpan](../android/text/style/DrawableMarginSpan.md) | A span which adds a drawable and a padding to the paragraph it's attached to. | | [IconMarginSpan](../android/text/style/IconMarginSpan.md) | Paragraph affecting span, that draws a bitmap at the beginning of a text. | | [LineHeightSpan.Standard](../android/text/style/LineHeightSpan.Standard.md) | Default implementation of the [LineHeightSpan](../android/text/style/LineHeightSpan.md), which changes the line height of the attached paragraph. | | [LineHeightSpan.WithDensity](../android/text/style/LineHeightSpan.WithDensity.md) | The classes that affect the line height of paragraph with respect to density, should implement this interface. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

## Summary
