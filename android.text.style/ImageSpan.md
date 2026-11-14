Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ImageSpan

```
open class ImageSpan : DynamicDrawableSpan
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [android.text.style.CharacterStyle](CharacterStyle.md) |||||
| | ↳ | [android.text.style.MetricAffectingSpan](MetricAffectingSpan.md) ||||
| | | ↳ | [android.text.style.ReplacementSpan](ReplacementSpan.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [android.text.style.DynamicDrawableSpan](DynamicDrawableSpan.md) ||
| | | | | ↳ | [android.text.style.ImageSpan](ImageSpan.md) |

Span that replaces the text it's attached to with a `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#` that can be aligned with the bottom or with the baseline of the surrounding text. The drawable can be constructed from varied sources:

- `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#` - see ImageSpan and ImageSpan
- `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#` - see ImageSpan
- resource id - see ImageSpan
- `https://developer.android.com/reference/kotlin/android/net/Uri.html#` - see ImageSpan

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
| From class DynamicDrawableSpan |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_BASELINE:kotlin.Int` A constant indicating that the bottom of this span should be aligned with the baseline of the surrounding text. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_BOTTOM:kotlin.Int` A constant indicating that the bottom of this span should be aligned with the bottom of the surrounding text, i.e., at the same level as the lowest descender in the text. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_CENTER:kotlin.Int` A constant indicating that this span should be vertically centered between the top and the lowest descender. <br /> | ||

| Public constructors ||
|---|---|
| ImageSpan Constructs an ImageSpan from a `https://developer.android.com/reference/kotlin/android/content/Context.html#` and a `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#` with the default alignment `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_BOTTOM:kotlin.Int` |
| ImageSpan Constructs an ImageSpan from a `https://developer.android.com/reference/kotlin/android/content/Context.html#`, a `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#` and a vertical alignment. |
| ImageSpan Constructs an ImageSpan from a `https://developer.android.com/reference/kotlin/android/content/Context.html#` and a `https://developer.android.com/reference/kotlin/android/net/Uri.html#` with the default alignment `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_BOTTOM:kotlin.Int`. |
| ImageSpan Constructs an ImageSpan from a `https://developer.android.com/reference/kotlin/android/content/Context.html#`, a `https://developer.android.com/reference/kotlin/android/net/Uri.html#` and a vertical alignment. |
| ImageSpan Constructs an ImageSpan from a `https://developer.android.com/reference/kotlin/android/content/Context.html#` and a resource id with the default alignment `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_BOTTOM:kotlin.Int` |
| ImageSpan Constructs an ImageSpan from a `https://developer.android.com/reference/kotlin/android/content/Context.html#`, a resource id and a vertical alignment. |
| ImageSpan <br /> |
| ImageSpan <br /> |
| ImageSpan Constructs an ImageSpan from a drawable with the default alignment `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_BOTTOM:kotlin.Int`. |
| ImageSpan Constructs an ImageSpan from a drawable and a vertical alignment. |
| ImageSpan Constructs an ImageSpan from a drawable and a source with the default alignment `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_BOTTOM:kotlin.Int` |
| ImageSpan Constructs an ImageSpan from a drawable, a source and a vertical alignment. |

| Public methods ||
|---|---|
| open [Drawable](../android.graphics.drawable/Drawable.md)! | getDrawable Your subclass must implement this method to provide the bitmap to be drawn. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | getSource Returns the source string that was saved during construction. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | toString Returns a string representation of the object. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class DynamicDrawableSpan |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | draw Draws the span into the canvas. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getSize Returns the width of the span. Extending classes can set the height of the span by updating attributes of `https://developer.android.com/reference/kotlin/android/graphics/Paint.FontMetricsInt.html#`. If the span covers the whole text, and the height is not set, draw will not be called for the span. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getVerticalAlignment Returns the vertical alignment of this span, one of `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_BOTTOM:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_BASELINE:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_CENTER:kotlin.Int`. <br /> | ||
| From class ReplacementSpan |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?` | getContentDescription Gets a brief description of this ReplacementSpan for use in accessibility support. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setContentDescription Sets the specific content description into ReplacementSpan. ReplacementSpans are shared with accessibility services, but only the content description is available from them. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | updateDrawState This method does nothing, since ReplacementSpans are drawn explicitly instead of affecting Paint properties. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | updateMeasureState This method does nothing, since ReplacementSpans are measured explicitly instead of affecting Paint properties. <br /> | ||
| From class MetricAffectingSpan |---|---| | `https://developer.android.com/reference/kotlin/android/text/style/MetricAffectingSpan!` | getUnderlying Returns "this" for most MetricAffectingSpans, but for MetricAffectingSpans that were generated by wrap, returns the underlying MetricAffectingSpan. <br /> | ||
| --- | --- | --- | --- | --- | --- | --- | --- |
| From class CharacterStyle |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | updateDrawState <br /> | | `https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle!` | wrap A given CharacterStyle can only applied to a single region of a given Spanned. If you need to attach the same CharacterStyle to multiple regions, you can use this method to wrap it with a new object that will have the same effect but be a distinct object so that it can also be attached without conflict. <br /> | ||

| Inherited properties ||
|---|---|
| From class DynamicDrawableSpan |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#mVerticalAlignment:kotlin.Int` <br /> | ||

## Public constructors

### ImageSpan

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ImageSpan(
    context: Context, 
    bitmap: Bitmap)
```

Constructs an ImageSpan from a `https://developer.android.com/reference/kotlin/android/content/Context.html#` and a `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#` with the default alignment `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_BOTTOM:kotlin.Int`

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md): context used to create a drawable from `bitmap` based on the display metrics of the resources. This value cannot be `null`. |
| `bitmap` | [Bitmap](../android.graphics/Bitmap.md): bitmap to be rendered. This value cannot be `null`. |

### ImageSpan

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ImageSpan(
    context: Context, 
    bitmap: Bitmap, 
    verticalAlignment: Int)
```

Constructs an ImageSpan from a `https://developer.android.com/reference/kotlin/android/content/Context.html#`, a `https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#` and a vertical alignment.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md): context used to create a drawable from `bitmap` based on the display metrics of the resources. This value cannot be `null`. |
| `bitmap` | [Bitmap](../android.graphics/Bitmap.md): bitmap to be rendered. This value cannot be `null`. |
| `verticalAlignment` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): one of `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_BOTTOM:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_BASELINE:kotlin.Int` |
| --- | --- |

### ImageSpan

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ImageSpan(
    context: Context, 
    uri: Uri)
```

Constructs an ImageSpan from a `https://developer.android.com/reference/kotlin/android/content/Context.html#` and a `https://developer.android.com/reference/kotlin/android/net/Uri.html#` with the default alignment `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_BOTTOM:kotlin.Int`. The Uri source can be retrieved via getSource

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md): context used to create a drawable from `bitmap` based on the display metrics of the resources. This value cannot be `null`. |
| `uri` | [Uri](../android.net/Uri.md): `https://developer.android.com/reference/kotlin/android/net/Uri.html#` used to construct the drawable that will be rendered. This value cannot be `null`. |

### ImageSpan

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ImageSpan(
    context: Context, 
    uri: Uri, 
    verticalAlignment: Int)
```

Constructs an ImageSpan from a `https://developer.android.com/reference/kotlin/android/content/Context.html#`, a `https://developer.android.com/reference/kotlin/android/net/Uri.html#` and a vertical alignment. The Uri source can be retrieved via getSource

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md): context used to create a drawable from `bitmap` based on the display metrics of the resources. This value cannot be `null`. |
| `uri` | [Uri](../android.net/Uri.md): `https://developer.android.com/reference/kotlin/android/net/Uri.html#` used to construct the drawable that will be rendered. This value cannot be `null`. |
| `verticalAlignment` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): one of `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_BOTTOM:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_BASELINE:kotlin.Int` |
| --- | --- |

### ImageSpan

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ImageSpan(
    context: Context, 
    resourceId: Int)
```

Constructs an ImageSpan from a `https://developer.android.com/reference/kotlin/android/content/Context.html#` and a resource id with the default alignment `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_BOTTOM:kotlin.Int`

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md): context used to retrieve the drawable from resources. This value cannot be `null`. |
| `resourceId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): drawable resource id based on which the drawable is retrieved |

### ImageSpan

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ImageSpan(
    context: Context, 
    resourceId: Int, 
    verticalAlignment: Int)
```

Constructs an ImageSpan from a `https://developer.android.com/reference/kotlin/android/content/Context.html#`, a resource id and a vertical alignment.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md): context used to retrieve the drawable from resources. This value cannot be `null`. |
| `resourceId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): drawable resource id based on which the drawable is retrieved. |
| `verticalAlignment` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): one of `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_BOTTOM:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_BASELINE:kotlin.Int` |
| --- | --- |

### ImageSpan

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ImageSpan(b: Bitmap)
```

**Deprecated:** *Use ImageSpan instead.*

| Parameters ||
|---|---|
| `b` | [Bitmap](../android.graphics/Bitmap.md): This value cannot be `null`. |

### ImageSpan

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ImageSpan(
    b: Bitmap, 
    verticalAlignment: Int)
```

**Deprecated:** *Use ImageSpan instead.*

| Parameters ||
|---|---|
| `b` | [Bitmap](../android.graphics/Bitmap.md): This value cannot be `null`. |

### ImageSpan

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ImageSpan(drawable: Drawable)
```

Constructs an ImageSpan from a drawable with the default alignment `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_BOTTOM:kotlin.Int`.

| Parameters ||
|---|---|
| `drawable` | [Drawable](../android.graphics.drawable/Drawable.md): drawable to be rendered. This value cannot be `null`. |

### ImageSpan

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ImageSpan(
    drawable: Drawable, 
    verticalAlignment: Int)
```

Constructs an ImageSpan from a drawable and a vertical alignment.

| Parameters ||
|---|---|
| `drawable` | [Drawable](../android.graphics.drawable/Drawable.md): drawable to be rendered. This value cannot be `null`. |
| `verticalAlignment` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): one of `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_BOTTOM:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_BASELINE:kotlin.Int` |

### ImageSpan

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ImageSpan(
    drawable: Drawable, 
    source: String)
```

Constructs an ImageSpan from a drawable and a source with the default alignment `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_BOTTOM:kotlin.Int`

| Parameters ||
|---|---|
| `drawable` | [Drawable](../android.graphics.drawable/Drawable.md): drawable to be rendered. This value cannot be `null`. |
| `source` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): drawable's Uri source. This value cannot be `null`. |

### ImageSpan

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ImageSpan(
    drawable: Drawable, 
    source: String, 
    verticalAlignment: Int)
```

Constructs an ImageSpan from a drawable, a source and a vertical alignment.

| Parameters ||
|---|---|
| `drawable` | [Drawable](../android.graphics.drawable/Drawable.md): drawable to be rendered. This value cannot be `null`. |
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

- ImageSpan
- ImageSpan

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |
