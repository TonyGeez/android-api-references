# android.text.style

# android.text.style

Kotlin| [Java](https://developer.android.com/reference/android/text/style/package-summary "View this page in Java")

## Interfaces

| [AlignmentSpan](https://developer.android.com/reference/kotlin/android/text/style/AlignmentSpan) | Span that allows defining the alignment of text at the paragraph level. |
| [LeadingMarginSpan](https://developer.android.com/reference/kotlin/android/text/style/LeadingMarginSpan) | A paragraph style affecting the leading margin. |
| [LineBackgroundSpan](https://developer.android.com/reference/kotlin/android/text/style/LineBackgroundSpan) | Used to change the background of lines where the span is attached to. |
| [LineHeightSpan](https://developer.android.com/reference/kotlin/android/text/style/LineHeightSpan) | The classes that affect the line height of paragraph should implement this interface. |
| [ParagraphStyle](https://developer.android.com/reference/kotlin/android/text/style/ParagraphStyle) | The classes that affect paragraph-level text formatting implement this interface. |
| [TabStopSpan](https://developer.android.com/reference/kotlin/android/text/style/TabStopSpan) | Paragraph affecting span that changes the position of the tab with respect to the leading margin of the line. |
| [UpdateAppearance](https://developer.android.com/reference/kotlin/android/text/style/UpdateAppearance) | The classes that affect character-level text in a way that modifies their appearance when one is added or removed must implement this interface. |
| [UpdateLayout](https://developer.android.com/reference/kotlin/android/text/style/UpdateLayout) | The classes that affect character-level text formatting in a way that triggers a text layout update when one is added or removed must implement this interface. |
| [WrapTogetherSpan](https://developer.android.com/reference/kotlin/android/text/style/WrapTogetherSpan) | <br /> |

## Classes

| [AbsoluteSizeSpan](https://developer.android.com/reference/kotlin/android/text/style/AbsoluteSizeSpan) | A span that changes the size of the text it's attached to. |
| [BackgroundColorSpan](https://developer.android.com/reference/kotlin/android/text/style/BackgroundColorSpan) | Changes the background color of the text to which the span is attached. |
| [BulletSpan](https://developer.android.com/reference/kotlin/android/text/style/BulletSpan) | A span which styles paragraphs as bullet points (respecting layout direction). |
| [CharacterStyle](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle) | The classes that affect character-level text formatting extend this class. |
| [ClickableSpan](https://developer.android.com/reference/kotlin/android/text/style/ClickableSpan) | If an object of this type is attached to the text of a TextView with a movement method of LinkMovementMethod, the affected spans of text can be selected. |
| [DrawableMarginSpan](https://developer.android.com/reference/kotlin/android/text/style/DrawableMarginSpan) | A span which adds a drawable and a padding to the paragraph it's attached to. |
| [DynamicDrawableSpan](https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan) | Span that replaces the text it's attached to with a [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#) that can be aligned with the bottom or with the baseline of the surrounding text. |
| [EasyEditSpan](https://developer.android.com/reference/kotlin/android/text/style/EasyEditSpan) | Provides an easy way to edit a portion of text. |
| [ForegroundColorSpan](https://developer.android.com/reference/kotlin/android/text/style/ForegroundColorSpan) | Changes the color of the text to which the span is attached. |
| [IconMarginSpan](https://developer.android.com/reference/kotlin/android/text/style/IconMarginSpan) | Paragraph affecting span, that draws a bitmap at the beginning of a text. |
| [ImageSpan](https://developer.android.com/reference/kotlin/android/text/style/ImageSpan) | Span that replaces the text it's attached to with a [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#) that can be aligned with the bottom or with the baseline of the surrounding text. |
| [LineBreakConfigSpan](https://developer.android.com/reference/kotlin/android/text/style/LineBreakConfigSpan) | LineBreakSpan for changing line break style of the specific region of the text. |
| [LocaleSpan](https://developer.android.com/reference/kotlin/android/text/style/LocaleSpan) | Changes the [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#) of the text to which the span is attached. |
| [MaskFilterSpan](https://developer.android.com/reference/kotlin/android/text/style/MaskFilterSpan) | Span that allows setting a [MaskFilter](https://developer.android.com/reference/kotlin/android/graphics/MaskFilter.html#) to the text it's attached to. |
| [MetricAffectingSpan](https://developer.android.com/reference/kotlin/android/text/style/MetricAffectingSpan) | The classes that affect character-level text formatting in a way that changes the width or height of characters extend this class. |
| [NoWritingToolsSpan](https://developer.android.com/reference/kotlin/android/text/style/NoWritingToolsSpan) | A span that signals to IMEs that writing tools should not modify the text. |
| [QuoteSpan](https://developer.android.com/reference/kotlin/android/text/style/QuoteSpan) | A span which styles paragraphs by adding a vertical stripe at the beginning of the text (respecting layout direction). |
| [RelativeSizeSpan](https://developer.android.com/reference/kotlin/android/text/style/RelativeSizeSpan) | Uniformly scales the size of the text to which it's attached by a certain proportion. |
| [ReplacementSpan](https://developer.android.com/reference/kotlin/android/text/style/ReplacementSpan) | <br /> |
| [ScaleXSpan](https://developer.android.com/reference/kotlin/android/text/style/ScaleXSpan) | Scales horizontally the size of the text to which it's attached by a certain factor. |
| [StrikethroughSpan](https://developer.android.com/reference/kotlin/android/text/style/StrikethroughSpan) | A span that strikes through the text it's attached to. |
| [StyleSpan](https://developer.android.com/reference/kotlin/android/text/style/StyleSpan) | Span that allows setting the style of the text it's attached to. |
| [SubscriptSpan](https://developer.android.com/reference/kotlin/android/text/style/SubscriptSpan) | The span that moves the position of the text baseline lower. |
| [SuggestionRangeSpan](https://developer.android.com/reference/kotlin/android/text/style/SuggestionRangeSpan) | A SuggestionRangeSpan is used to show which part of an EditText is affected by a suggestion popup window. |
| [SuggestionSpan](https://developer.android.com/reference/kotlin/android/text/style/SuggestionSpan) | Holds suggestion candidates for the text enclosed in this span. |
| [SuperscriptSpan](https://developer.android.com/reference/kotlin/android/text/style/SuperscriptSpan) | The span that moves the position of the text baseline higher. |
| [TextAppearanceSpan](https://developer.android.com/reference/kotlin/android/text/style/TextAppearanceSpan) | Sets the text appearance using the given [TextAppearance](https://developer.android.com/reference/kotlin/android/R.styleable.html#TextAppearance:kotlin.IntArray) attributes. |
| [TtsSpan](https://developer.android.com/reference/kotlin/android/text/style/TtsSpan) | A span that supplies additional meta-data for the associated text intended for text-to-speech engines. |
| [TypefaceSpan](https://developer.android.com/reference/kotlin/android/text/style/TypefaceSpan) | Span that updates the typeface of the text it's attached to. |
| [UnderlineSpan](https://developer.android.com/reference/kotlin/android/text/style/UnderlineSpan) | A span that underlines the text it's attached to. |
| [URLSpan](https://developer.android.com/reference/kotlin/android/text/style/URLSpan) | Implementation of the [ClickableSpan](https://developer.android.com/reference/kotlin/android/text/style/ClickableSpan) that allows setting a url string. |
