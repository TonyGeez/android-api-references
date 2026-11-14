# ClickableSpan

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ClickableSpan

Kotlin| [Java](https://developer.android.com/reference/android/text/style/ClickableSpan "View this page in Java") 
| --- | --- |

```
abstract class ClickableSpan : CharacterStyle, UpdateAppearance
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.text.style.CharacterStyle](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle) ||
| | ↳ | [android.text.style.ClickableSpan](https://developer.android.com/reference/kotlin/android/text/style/ClickableSpan#) |

| Known Direct Subclasses [TextLinks.TextLinkSpan](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextLinks.TextLinkSpan.html#), [URLSpan](https://developer.android.com/reference/kotlin/android/text/style/URLSpan) |-----------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------| | [TextLinks.TextLinkSpan](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextLinks.TextLinkSpan.html#) | A ClickableSpan for a TextLink. | | [URLSpan](https://developer.android.com/reference/kotlin/android/text/style/URLSpan) | Implementation of the [ClickableSpan](https://developer.android.com/reference/kotlin/android/text/style/ClickableSpan#) that allows setting a url string. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

If an object of this type is attached to the text of a TextView with a movement method of LinkMovementMethod, the affected spans of text can be selected. If selected and clicked, the [onClick](https://developer.android.com/reference/kotlin/android/text/style/ClickableSpan#onClick(android.view.View))method will be called.

The text with a`ClickableSpan`attached will be underlined and the link color will be used as a text color. The default link color is the theme's accent color or`android:textColorLink`if this attribute is defined in the theme. For example, considering that we have a`CustomClickableSpan`that extends`ClickableSpan`, it can be used like this: 

```kotlin
<code>SpannableString string = new SpannableString("Text with clickable text");
 string.setSpan(new CustomClickableSpan(), 10, 19, Spanned.SPAN_EXCLUSIVE_EXCLUSIVE);</code>
```
Text with`ClickableSpan`.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------|---|
| [ClickableSpan](https://developer.android.com/reference/kotlin/android/text/style/ClickableSpan#ClickableSpan())`()` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onClick](https://developer.android.com/reference/kotlin/android/text/style/ClickableSpan#onClick(android.view.View))`(`widget:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)`)` Performs the click action associated with this span. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/text/style/ClickableSpan#toString())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateDrawState](https://developer.android.com/reference/kotlin/android/text/style/ClickableSpan#updateDrawState(android.text.TextPaint))`(`ds:` ` [TextPaint](https://developer.android.com/reference/kotlin/android/text/TextPaint.html#)`)` Makes the text underlined and in the link color. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [CharacterStyle](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle) |-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [CharacterStyle](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle)! | [getUnderlying](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle#getUnderlying())`()` <br /> Returns "this" for most CharacterStyles, but for CharacterStyles that were generated by [wrap](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle#wrap(android.text.style.CharacterStyle)), returns the underlying CharacterStyle. <br /> | | [CharacterStyle](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle)! | [wrap](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle#wrap(android.text.style.CharacterStyle))`(`cs:` ` [CharacterStyle](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle)!`)` <br /> A given CharacterStyle can only applied to a single region of a given Spanned. If you need to attach the same CharacterStyle to multiple regions, you can use this method to wrap it with a new object that will have the same effect but be a distinct object so that it can also be attached without conflict. <br /> | ||

## Public constructors

### ClickableSpan

```
ClickableSpan()
```

## Public methods

### onClick

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onClick(widget: View): Unit
```

Performs the click action associated with this span.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------|
| `widget` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#):This value cannot be`null`. |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### updateDrawState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun updateDrawState(ds: TextPaint): Unit
```

Makes the text underlined and in the link color.

| Parameters ||
|------|----------------------------------------------------------------------------------------------------------------------|
| `ds` | [TextPaint](https://developer.android.com/reference/kotlin/android/text/TextPaint.html#):This value cannot be`null`. |
