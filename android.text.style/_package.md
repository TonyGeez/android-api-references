# android.text.style

# android.text.style

Kotlin| [Java](../android/text/style/_package.md)
| --- | --- |

## Interfaces

| [AlignmentSpan](../android/text/style/AlignmentSpan.md) | Span that allows defining the alignment of text at the paragraph level. |
| --- | --- |
| [LeadingMarginSpan](../android/text/style/LeadingMarginSpan.md) | A paragraph style affecting the leading margin. |
| [LineBackgroundSpan](../android/text/style/LineBackgroundSpan.md) | Used to change the background of lines where the span is attached to. |
| [LineHeightSpan](../android/text/style/LineHeightSpan.md) | The classes that affect the line height of paragraph should implement this interface. |
| --- | --- |
| [ParagraphStyle](../android/text/style/ParagraphStyle.md) | The classes that affect paragraph-level text formatting implement this interface. |
| [TabStopSpan](../android/text/style/TabStopSpan.md) | Paragraph affecting span that changes the position of the tab with respect to the leading margin of the line. |
| [UpdateAppearance](../android/text/style/UpdateAppearance.md) | The classes that affect character-level text in a way that modifies their appearance when one is added or removed must implement this interface. |
| --- | --- |
| [UpdateLayout](../android/text/style/UpdateLayout.md) | The classes that affect character-level text formatting in a way that triggers a text layout update when one is added or removed must implement this interface. |
| [WrapTogetherSpan](../android/text/style/WrapTogetherSpan.md) | <br /> |

## Classes

| [AbsoluteSizeSpan](../android/text/style/AbsoluteSizeSpan.md) | A span that changes the size of the text it's attached to. |
| --- | --- |
| [BackgroundColorSpan](../android/text/style/BackgroundColorSpan.md) | Changes the background color of the text to which the span is attached. |
| [BulletSpan](../android/text/style/BulletSpan.md) | A span which styles paragraphs as bullet points (respecting layout direction). |
| [CharacterStyle](../android/text/style/CharacterStyle.md) | The classes that affect character-level text formatting extend this class. |
| --- | --- |
| [ClickableSpan](../android/text/style/ClickableSpan.md) | If an object of this type is attached to the text of a TextView with a movement method of LinkMovementMethod, the affected spans of text can be selected. |
| [DrawableMarginSpan](../android/text/style/DrawableMarginSpan.md) | A span which adds a drawable and a padding to the paragraph it's attached to. |
| [DynamicDrawableSpan](../android/text/style/DynamicDrawableSpan.md) | Span that replaces the text it's attached to with a [Drawable](../android/graphics/drawable/Drawable.md) that can be aligned with the bottom or with the baseline of the surrounding text. |
| --- | --- |
| [EasyEditSpan](../android/text/style/EasyEditSpan.md) | Provides an easy way to edit a portion of text. |
| [ForegroundColorSpan](../android/text/style/ForegroundColorSpan.md) | Changes the color of the text to which the span is attached. |
| [IconMarginSpan](../android/text/style/IconMarginSpan.md) | Paragraph affecting span, that draws a bitmap at the beginning of a text. |
| --- | --- |
| [ImageSpan](../android/text/style/ImageSpan.md) | Span that replaces the text it's attached to with a [Drawable](../android/graphics/drawable/Drawable.md) that can be aligned with the bottom or with the baseline of the surrounding text. |
| [LineBreakConfigSpan](../android/text/style/LineBreakConfigSpan.md) | LineBreakSpan for changing line break style of the specific region of the text. |
| [LocaleSpan](../android/text/style/LocaleSpan.md) | Changes the [Locale](../java/util/Locale.md) of the text to which the span is attached. |
| --- | --- |
| [MaskFilterSpan](../android/text/style/MaskFilterSpan.md) | Span that allows setting a [MaskFilter](../android/graphics/MaskFilter.md) to the text it's attached to. |
| [MetricAffectingSpan](../android/text/style/MetricAffectingSpan.md) | The classes that affect character-level text formatting in a way that changes the width or height of characters extend this class. |
| [NoWritingToolsSpan](../android/text/style/NoWritingToolsSpan.md) | A span that signals to IMEs that writing tools should not modify the text. |
| --- | --- |
| [QuoteSpan](../android/text/style/QuoteSpan.md) | A span which styles paragraphs by adding a vertical stripe at the beginning of the text (respecting layout direction). |
| [RelativeSizeSpan](../android/text/style/RelativeSizeSpan.md) | Uniformly scales the size of the text to which it's attached by a certain proportion. |
| [ReplacementSpan](../android/text/style/ReplacementSpan.md) | <br /> |
| --- | --- |
| [ScaleXSpan](../android/text/style/ScaleXSpan.md) | Scales horizontally the size of the text to which it's attached by a certain factor. |
| [StrikethroughSpan](../android/text/style/StrikethroughSpan.md) | A span that strikes through the text it's attached to. |
| [StyleSpan](../android/text/style/StyleSpan.md) | Span that allows setting the style of the text it's attached to. |
| --- | --- |
| [SubscriptSpan](../android/text/style/SubscriptSpan.md) | The span that moves the position of the text baseline lower. |
| [SuggestionRangeSpan](../android/text/style/SuggestionRangeSpan.md) | A SuggestionRangeSpan is used to show which part of an EditText is affected by a suggestion popup window. |
| [SuggestionSpan](../android/text/style/SuggestionSpan.md) | Holds suggestion candidates for the text enclosed in this span. |
| --- | --- |
| [SuperscriptSpan](../android/text/style/SuperscriptSpan.md) | The span that moves the position of the text baseline higher. |
| [TextAppearanceSpan](../android/text/style/TextAppearanceSpan.md) | Sets the text appearance using the given [TextAppearance](../android/R.styleable.md) attributes. |
| [TtsSpan](../android/text/style/TtsSpan.md) | A span that supplies additional meta-data for the associated text intended for text-to-speech engines. |
| --- | --- |
| [TypefaceSpan](../android/text/style/TypefaceSpan.md) | Span that updates the typeface of the text it's attached to. |
| [UnderlineSpan](../android/text/style/UnderlineSpan.md) | A span that underlines the text it's attached to. |
| [URLSpan](../android/text/style/URLSpan.md) | Implementation of the [ClickableSpan](../android/text/style/ClickableSpan.md) that allows setting a url string. |
| --- | --- |
