Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ImageSpan

```
open class ImageSpan : DynamicDrawableSpan
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [android.text.style.CharacterStyle](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle) |||||
| | ↳ | [android.text.style.MetricAffectingSpan](https://developer.android.com/reference/kotlin/android/text/style/MetricAffectingSpan) ||||
| | | ↳ | [android.text.style.ReplacementSpan](https://developer.android.com/reference/kotlin/android/text/style/ReplacementSpan) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [android.text.style.DynamicDrawableSpan](https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan) ||
| | | | | ↳ | [android.text.style.ImageSpan](https://developer.android.com/reference/kotlin/android/text/style/ImageSpan#) |

Span that replaces the text it's attached to with a `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#` that can be aligned with the bottom or with the baseline of the surrounding text. The drawable can be constructed from varied sources:

- `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#` - see `https://developer.android.com/reference/kotlin/android/text/style/ImageSpan#ImageSpan(android.content.Context,%20android.graphics.Bitmap)` and `https://developer.android.com/reference/kotlin/android/text/style/ImageSpan#ImageSpan(android.content.Context,%20android.graphics.Bitmap,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#` - see `https://developer.android.com/reference/kotlin/android/text/style/ImageSpan#ImageSpan(android.graphics.drawable.Drawable,%20kotlin.Int)`
- resource id - see `https://developer.android.com/reference/kotlin/android/text/style/ImageSpan#ImageSpan(android.content.Context,%20kotlin.Int,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/net/Uri.html#` - see `https://developer.android.com/reference/kotlin/android/text/style/ImageSpan#ImageSpan(android.content.Context,%20android.net.Uri,%20kotlin.Int)`

The default value for the vertical alignment is `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_BOTTOM:kotlin.Int`

<br />

For example, an `ImagedSpan` can be used like this:

```kotlin
SpannableString string = new SpannableString("Bottom: span.\nBaseline: span.");
  // using the default alignment: ALIGN_BOTTOM
  string.setSpan(new ImageSpan(this, R.mipmap.ic_launcher), 7, 8, Spannable.SPAN_EXCLUSIVE_EXCLUSIVE);
  string.setSpan(new ImageSpan(this, R.mipmap.ic_launcher, DynamicDrawableSpan.ALIGN_BASELINE),
  22, 23, Spannable.SPAN_EXCLUSIVE_EXCLUSIVE);
  
```
Text with `ImageSpan`s aligned bottom and baseline.

## Summary

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_BASELINE:kotlin.Int` A constant indicating that the bottom of this span should be aligned with the baseline of the surrounding text. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_BOTTOM:kotlin.Int` A constant indicating that the bottom of this span should be aligned with the bottom of the surrounding text, i.e., at the same level as the lowest descender in the text. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_CENTER:kotlin.Int` A constant indicating that this span should be vertically centered between the top and the lowest descender. <br /> | ||

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/text/style/ImageSpan#ImageSpan(android.content.Context,%20android.graphics.Bitmap)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#, bitmap: https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)` Constructs an `https://developer.android.com/reference/kotlin/android/text/style/ImageSpan#` from a `https://developer.android.com/reference/kotlin/android/content/Context.html#` and a `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#` with the default alignment `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_BOTTOM:kotlin.Int` |
| `https://developer.android.com/reference/kotlin/android/text/style/ImageSpan#ImageSpan(android.content.Context,%20android.graphics.Bitmap,%20kotlin.Int)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#, bitmap: https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#, verticalAlignment: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Constructs an `https://developer.android.com/reference/kotlin/android/text/style/ImageSpan#` from a `https://developer.android.com/reference/kotlin/android/content/Context.html#`, a `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#` and a vertical alignment. |
| `https://developer.android.com/reference/kotlin/android/text/style/ImageSpan#ImageSpan(android.content.Context,%20android.net.Uri)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#, uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#)` Constructs an `https://developer.android.com/reference/kotlin/android/text/style/ImageSpan#` from a `https://developer.android.com/reference/kotlin/android/content/Context.html#` and a `https://developer.android.com/reference/kotlin/android/net/Uri.html#` with the default alignment `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_BOTTOM:kotlin.Int`. |
| `https://developer.android.com/reference/kotlin/android/text/style/ImageSpan#ImageSpan(android.content.Context,%20android.net.Uri,%20kotlin.Int)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#, uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#, verticalAlignment: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Constructs an `https://developer.android.com/reference/kotlin/android/text/style/ImageSpan#` from a `https://developer.android.com/reference/kotlin/android/content/Context.html#`, a `https://developer.android.com/reference/kotlin/android/net/Uri.html#` and a vertical alignment. |
| `https://developer.android.com/reference/kotlin/android/text/style/ImageSpan#ImageSpan(android.content.Context,%20kotlin.Int)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#, resourceId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Constructs an `https://developer.android.com/reference/kotlin/android/text/style/ImageSpan#` from a `https://developer.android.com/reference/kotlin/android/content/Context.html#` and a resource id with the default alignment `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_BOTTOM:kotlin.Int` |
| `https://developer.android.com/reference/kotlin/android/text/style/ImageSpan#ImageSpan(android.content.Context,%20kotlin.Int,%20kotlin.Int)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#, resourceId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, verticalAlignment: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Constructs an `https://developer.android.com/reference/kotlin/android/text/style/ImageSpan#` from a `https://developer.android.com/reference/kotlin/android/content/Context.html#`, a resource id and a vertical alignment. |
| `https://developer.android.com/reference/kotlin/android/text/style/ImageSpan#ImageSpan(android.graphics.Bitmap)(b: https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)` <br /> |
| `https://developer.android.com/reference/kotlin/android/text/style/ImageSpan#ImageSpan(android.graphics.Bitmap,%20kotlin.Int)(b: https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#, verticalAlignment: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| `https://developer.android.com/reference/kotlin/android/text/style/ImageSpan#ImageSpan(android.graphics.drawable.Drawable)(drawable: https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)` Constructs an `https://developer.android.com/reference/kotlin/android/text/style/ImageSpan#` from a drawable with the default alignment `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_BOTTOM:kotlin.Int`. |
| `https://developer.android.com/reference/kotlin/android/text/style/ImageSpan#ImageSpan(android.graphics.drawable.Drawable,%20kotlin.Int)(drawable: https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#, verticalAlignment: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Constructs an `https://developer.android.com/reference/kotlin/android/text/style/ImageSpan#` from a drawable and a vertical alignment. |
| `https://developer.android.com/reference/kotlin/android/text/style/ImageSpan#ImageSpan(android.graphics.drawable.Drawable,%20kotlin.String)(drawable: https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#, source: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Constructs an `https://developer.android.com/reference/kotlin/android/text/style/ImageSpan#` from a drawable and a source with the default alignment `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_BOTTOM:kotlin.Int` |
| `https://developer.android.com/reference/kotlin/android/text/style/ImageSpan#ImageSpan(android.graphics.drawable.Drawable,%20kotlin.String,%20kotlin.Int)(drawable: https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#, source: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, verticalAlignment: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Constructs an `https://developer.android.com/reference/kotlin/android/text/style/ImageSpan#` from a drawable, a source and a vertical alignment. |

| Public methods ||
|---|---|
| open [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)! | `https://developer.android.com/reference/kotlin/android/text/style/ImageSpan#getDrawable()()` Your subclass must implement this method to provide the bitmap to be drawn. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/text/style/ImageSpan#getSource()()` Returns the source string that was saved during construction. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/ImageSpan#toString()()` Returns a string representation of the object. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#draw(android.graphics.Canvas,%20kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int,%20kotlin.Float,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20android.graphics.Paint)(canvas: https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#, text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, end: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, top: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, bottom: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, paint: https://developer.android.com/reference/kotlin/android/graphics/Paint.html#)` Draws the span into the canvas. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#getSize(android.graphics.Paint,%20kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int,%20android.graphics.Paint.FontMetricsInt)(paint: https://developer.android.com/reference/kotlin/android/graphics/Paint.html#, text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, end: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, fm: https://developer.android.com/reference/kotlin/android/graphics/Paint.FontMetricsInt.html#?)` Returns the width of the span. Extending classes can set the height of the span by updating attributes of `https://developer.android.com/reference/kotlin/android/graphics/Paint.FontMetricsInt.html#`. If the span covers the whole text, and the height is not set, `https://developer.android.com/reference/kotlin/android/text/style/ReplacementSpan#draw(android.graphics.Canvas,%20kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int,%20kotlin.Float,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20android.graphics.Paint)` will not be called for the span. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#getVerticalAlignment()()` Returns the vertical alignment of this span, one of `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_BOTTOM:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_BASELINE:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_CENTER:kotlin.Int`. <br /> | ||
| From class `https://developer.android.com/reference/kotlin/android/text/style/ReplacementSpan` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?` | `https://developer.android.com/reference/kotlin/android/text/style/ReplacementSpan#getContentDescription()()` Gets a brief description of this ReplacementSpan for use in accessibility support. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/text/style/ReplacementSpan#setContentDescription(kotlin.CharSequence)(contentDescription: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?)` Sets the specific content description into ReplacementSpan. ReplacementSpans are shared with accessibility services, but only the content description is available from them. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/text/style/ReplacementSpan#updateDrawState(android.text.TextPaint)(ds: https://developer.android.com/reference/kotlin/android/text/TextPaint.html#!)` This method does nothing, since ReplacementSpans are drawn explicitly instead of affecting Paint properties. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/text/style/ReplacementSpan#updateMeasureState(android.text.TextPaint)(p: https://developer.android.com/reference/kotlin/android/text/TextPaint.html#)` This method does nothing, since ReplacementSpans are measured explicitly instead of affecting Paint properties. <br /> | ||
| From class `https://developer.android.com/reference/kotlin/android/text/style/MetricAffectingSpan` |---|---| | `https://developer.android.com/reference/kotlin/android/text/style/MetricAffectingSpan!` | `https://developer.android.com/reference/kotlin/android/text/style/MetricAffectingSpan#getUnderlying()()` Returns "this" for most MetricAffectingSpans, but for MetricAffectingSpans that were generated by `https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle#wrap(android.text.style.CharacterStyle)`, returns the underlying MetricAffectingSpan. <br /> | ||
| --- | --- | --- | --- | --- | --- | --- | --- |
| From class `https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle#updateDrawState(android.text.TextPaint)(tp: https://developer.android.com/reference/kotlin/android/text/TextPaint.html#!)` <br /> | | `https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle!` | `https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle#wrap(android.text.style.CharacterStyle)(cs: https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle!)` A given CharacterStyle can only applied to a single region of a given Spanned. If you need to attach the same CharacterStyle to multiple regions, you can use this method to wrap it with a new object that will have the same effect but be a distinct object so that it can also be attached without conflict. <br /> | ||

| Inherited properties ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#mVerticalAlignment:kotlin.Int` <br /> | ||

## Public constructors

### ImageSpan

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ImageSpan(
    context: Context, 
    bitmap: Bitmap)
```

Constructs an `https://developer.android.com/reference/kotlin/android/text/style/ImageSpan#` from a `https://developer.android.com/reference/kotlin/android/content/Context.html#` and a `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#` with the default alignment `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_BOTTOM:kotlin.Int`

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#): context used to create a drawable from `bitmap` based on the display metrics of the resources. This value cannot be `null`. |
| `bitmap` | [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#): bitmap to be rendered. This value cannot be `null`. |

### ImageSpan

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ImageSpan(
    context: Context, 
    bitmap: Bitmap, 
    verticalAlignment: Int)
```

Constructs an `https://developer.android.com/reference/kotlin/android/text/style/ImageSpan#` from a `https://developer.android.com/reference/kotlin/android/content/Context.html#`, a `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#` and a vertical alignment.

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#): context used to create a drawable from `bitmap` based on the display metrics of the resources. This value cannot be `null`. |
| `bitmap` | [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#): bitmap to be rendered. This value cannot be `null`. |
| `verticalAlignment` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): one of `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_BOTTOM:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_BASELINE:kotlin.Int` |
| --- | --- |

### ImageSpan

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ImageSpan(
    context: Context, 
    uri: Uri)
```

Constructs an `https://developer.android.com/reference/kotlin/android/text/style/ImageSpan#` from a `https://developer.android.com/reference/kotlin/android/content/Context.html#` and a `https://developer.android.com/reference/kotlin/android/net/Uri.html#` with the default alignment `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_BOTTOM:kotlin.Int`. The Uri source can be retrieved via `https://developer.android.com/reference/kotlin/android/text/style/ImageSpan#getSource()`

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#): context used to create a drawable from `bitmap` based on the display metrics of the resources. This value cannot be `null`. |
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#): `https://developer.android.com/reference/kotlin/android/net/Uri.html#` used to construct the drawable that will be rendered. This value cannot be `null`. |

### ImageSpan

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ImageSpan(
    context: Context, 
    uri: Uri, 
    verticalAlignment: Int)
```

Constructs an `https://developer.android.com/reference/kotlin/android/text/style/ImageSpan#` from a `https://developer.android.com/reference/kotlin/android/content/Context.html#`, a `https://developer.android.com/reference/kotlin/android/net/Uri.html#` and a vertical alignment. The Uri source can be retrieved via `https://developer.android.com/reference/kotlin/android/text/style/ImageSpan#getSource()`

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#): context used to create a drawable from `bitmap` based on the display metrics of the resources. This value cannot be `null`. |
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#): `https://developer.android.com/reference/kotlin/android/net/Uri.html#` used to construct the drawable that will be rendered. This value cannot be `null`. |
| `verticalAlignment` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): one of `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_BOTTOM:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_BASELINE:kotlin.Int` |
| --- | --- |

### ImageSpan

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ImageSpan(
    context: Context, 
    resourceId: Int)
```

Constructs an `https://developer.android.com/reference/kotlin/android/text/style/ImageSpan#` from a `https://developer.android.com/reference/kotlin/android/content/Context.html#` and a resource id with the default alignment `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_BOTTOM:kotlin.Int`

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#): context used to retrieve the drawable from resources. This value cannot be `null`. |
| `resourceId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): drawable resource id based on which the drawable is retrieved |

### ImageSpan

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ImageSpan(
    context: Context, 
    resourceId: Int, 
    verticalAlignment: Int)
```

Constructs an `https://developer.android.com/reference/kotlin/android/text/style/ImageSpan#` from a `https://developer.android.com/reference/kotlin/android/content/Context.html#`, a resource id and a vertical alignment.

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#): context used to retrieve the drawable from resources. This value cannot be `null`. |
| `resourceId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): drawable resource id based on which the drawable is retrieved. |
| `verticalAlignment` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): one of `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_BOTTOM:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_BASELINE:kotlin.Int` |
| --- | --- |

### ImageSpan

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ImageSpan(b: Bitmap)
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/text/style/ImageSpan#ImageSpan(android.content.Context,%20android.graphics.Bitmap)` instead.*

| Parameters ||
|---|---|
| `b` | [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#): This value cannot be `null`. |

### ImageSpan

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ImageSpan(
    b: Bitmap, 
    verticalAlignment: Int)
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/text/style/ImageSpan#ImageSpan(android.content.Context,%20android.graphics.Bitmap,%20kotlin.Int)` instead.*

| Parameters ||
|---|---|
| `b` | [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#): This value cannot be `null`. |

### ImageSpan

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ImageSpan(drawable: Drawable)
```

Constructs an `https://developer.android.com/reference/kotlin/android/text/style/ImageSpan#` from a drawable with the default alignment `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_BOTTOM:kotlin.Int`.

| Parameters ||
|---|---|
| `drawable` | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#): drawable to be rendered. This value cannot be `null`. |

### ImageSpan

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ImageSpan(
    drawable: Drawable, 
    verticalAlignment: Int)
```

Constructs an `https://developer.android.com/reference/kotlin/android/text/style/ImageSpan#` from a drawable and a vertical alignment.

| Parameters ||
|---|---|
| `drawable` | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#): drawable to be rendered. This value cannot be `null`. |
| `verticalAlignment` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): one of `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_BOTTOM:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_BASELINE:kotlin.Int` |

### ImageSpan

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ImageSpan(
    drawable: Drawable, 
    source: String)
```

Constructs an `https://developer.android.com/reference/kotlin/android/text/style/ImageSpan#` from a drawable and a source with the default alignment `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_BOTTOM:kotlin.Int`

| Parameters ||
|---|---|
| `drawable` | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#): drawable to be rendered. This value cannot be `null`. |
| `source` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): drawable's Uri source. This value cannot be `null`. |

### ImageSpan

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ImageSpan(
    drawable: Drawable, 
    source: String, 
    verticalAlignment: Int)
```

Constructs an `https://developer.android.com/reference/kotlin/android/text/style/ImageSpan#` from a drawable, a source and a vertical alignment.

| Parameters ||
|---|---|
| `drawable` | [Drawable](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#): drawable to be rendered. This value cannot be `null`. |
| `source` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): drawable's uri source. This value cannot be `null`. |
| `verticalAlignment` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): one of `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_BOTTOM:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_BASELINE:kotlin.Int` |
| --- | --- |

## Public methods

### getDrawable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDrawable(): Drawable!
```

Your subclass must implement this method to provide the bitmap to be drawn. The dimensions of the bitmap must be the same from each call to the next.

### getSource

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSource(): String?
```

Returns the source string that was saved during construction.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | the source string that was saved during construction. This value may be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/text/style/ImageSpan#ImageSpan(android.graphics.drawable.Drawable,%20kotlin.String)`
- `https://developer.android.com/reference/kotlin/android/text/style/ImageSpan#ImageSpan(android.content.Context,%20android.net.Uri)`

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |
