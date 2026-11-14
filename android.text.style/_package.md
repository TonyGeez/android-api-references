# android.text.style

# android.text.style

Kotlin| [Java](_package.md)
| --- | --- |

## Interfaces

| [AlignmentSpan](AlignmentSpan.md) | Span that allows defining the alignment of text at the paragraph level. |
| --- | --- |
| [LeadingMarginSpan](LeadingMarginSpan.md) | A paragraph style affecting the leading margin. |
| [LineBackgroundSpan](LineBackgroundSpan.md) | Used to change the background of lines where the span is attached to. |
| [LineHeightSpan](LineHeightSpan.md) | The classes that affect the line height of paragraph should implement this interface. |
| --- | --- |
| [ParagraphStyle](ParagraphStyle.md) | The classes that affect paragraph-level text formatting implement this interface. |
| [TabStopSpan](TabStopSpan.md) | Paragraph affecting span that changes the position of the tab with respect to the leading margin of the line. |
| [UpdateAppearance](UpdateAppearance.md) | The classes that affect character-level text in a way that modifies their appearance when one is added or removed must implement this interface. |
| --- | --- |
| [UpdateLayout](UpdateLayout.md) | The classes that affect character-level text formatting in a way that triggers a text layout update when one is added or removed must implement this interface. |
| [WrapTogetherSpan](WrapTogetherSpan.md) | <br /> |

## Classes

| [AbsoluteSizeSpan](AbsoluteSizeSpan.md) | A span that changes the size of the text it's attached to. |
| --- | --- |
| [BackgroundColorSpan](BackgroundColorSpan.md) | Changes the background color of the text to which the span is attached. |
| [BulletSpan](BulletSpan.md) | A span which styles paragraphs as bullet points (respecting layout direction). |
| [CharacterStyle](CharacterStyle.md) | The classes that affect character-level text formatting extend this class. |
| --- | --- |
| [ClickableSpan](ClickableSpan.md) | If an object of this type is attached to the text of a TextView with a movement method of LinkMovementMethod, the affected spans of text can be selected. |
| [DrawableMarginSpan](DrawableMarginSpan.md) | A span which adds a drawable and a padding to the paragraph it's attached to. |
| [DynamicDrawableSpan](DynamicDrawableSpan.md) | Span that replaces the text it's attached to with a [Drawable](../android.graphics.drawable/Drawable.md) that can be aligned with the bottom or with the baseline of the surrounding text. |
| --- | --- |
| [EasyEditSpan](EasyEditSpan.md) | Provides an easy way to edit a portion of text. |
| [ForegroundColorSpan](ForegroundColorSpan.md) | Changes the color of the text to which the span is attached. |
| [IconMarginSpan](IconMarginSpan.md) | Paragraph affecting span, that draws a bitmap at the beginning of a text. |
| --- | --- |
| [ImageSpan](ImageSpan.md) | Span that replaces the text it's attached to with a [Drawable](../android.graphics.drawable/Drawable.md) that can be aligned with the bottom or with the baseline of the surrounding text. |
| [LineBreakConfigSpan](LineBreakConfigSpan.md) | LineBreakSpan for changing line break style of the specific region of the text. |
| [LocaleSpan](LocaleSpan.md) | Changes the [Locale](../java.util/Locale.md) of the text to which the span is attached. |
| --- | --- |
| [MaskFilterSpan](MaskFilterSpan.md) | Span that allows setting a [MaskFilter](../android.graphics/MaskFilter.md) to the text it's attached to. |
| [MetricAffectingSpan](MetricAffectingSpan.md) | The classes that affect character-level text formatting in a way that changes the width or height of characters extend this class. |
| [NoWritingToolsSpan](NoWritingToolsSpan.md) | A span that signals to IMEs that writing tools should not modify the text. |
| --- | --- |
| [QuoteSpan](QuoteSpan.md) | A span which styles paragraphs by adding a vertical stripe at the beginning of the text (respecting layout direction). |
| [RelativeSizeSpan](RelativeSizeSpan.md) | Uniformly scales the size of the text to which it's attached by a certain proportion. |
| [ReplacementSpan](ReplacementSpan.md) | <br /> |
| --- | --- |
| [ScaleXSpan](ScaleXSpan.md) | Scales horizontally the size of the text to which it's attached by a certain factor. |
| [StrikethroughSpan](StrikethroughSpan.md) | A span that strikes through the text it's attached to. |
| [StyleSpan](StyleSpan.md) | Span that allows setting the style of the text it's attached to. |
| --- | --- |
| [SubscriptSpan](SubscriptSpan.md) | The span that moves the position of the text baseline lower. |
| [SuggestionRangeSpan](SuggestionRangeSpan.md) | A SuggestionRangeSpan is used to show which part of an EditText is affected by a suggestion popup window. |
| [SuggestionSpan](SuggestionSpan.md) | Holds suggestion candidates for the text enclosed in this span. |
| --- | --- |
| [SuperscriptSpan](SuperscriptSpan.md) | The span that moves the position of the text baseline higher. |
| [TextAppearanceSpan](TextAppearanceSpan.md) | Sets the text appearance using the given [TextAppearance](../android/R.styleable.md) attributes. |
| [TtsSpan](TtsSpan.md) | A span that supplies additional meta-data for the associated text intended for text-to-speech engines. |
| --- | --- |
| [TypefaceSpan](TypefaceSpan.md) | Span that updates the typeface of the text it's attached to. |
| [UnderlineSpan](UnderlineSpan.md) | A span that underlines the text it's attached to. |
| [URLSpan](URLSpan.md) | Implementation of the [ClickableSpan](ClickableSpan.md) that allows setting a url string. |
| --- | --- |
