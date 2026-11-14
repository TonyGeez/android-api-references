Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DynamicDrawableSpan

```
abstract class DynamicDrawableSpan : ReplacementSpan
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [android.text.style.CharacterStyle](CharacterStyle.md) ||||
| | ↳ | [android.text.style.MetricAffectingSpan](MetricAffectingSpan.md) |||
| | | ↳ | [android.text.style.ReplacementSpan](ReplacementSpan.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [android.text.style.DynamicDrawableSpan](DynamicDrawableSpan.md) |

| Known Direct Subclasses [ImageSpan](ImageSpan.md) |---|---| | [ImageSpan](ImageSpan.md) | Span that replaces the text it's attached to with a `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#` that can be aligned with the bottom or with the baseline of the surrounding text. | |
| --- | --- | --- | --- | --- | --- | --- |

Span that replaces the text it's attached to with a `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#` that can be aligned with the bottom or with the baseline of the surrounding text.

For an implementation that constructs the drawable from various sources (`Bitmap`, `Drawable`, resource id or `Uri`) use `https://developer.android.com/reference/kotlin/android/text/style/ImageSpan`.

A simple implementation of `DynamicDrawableSpan` that uses drawables from resources looks like this:

```kotlin
class MyDynamicDrawableSpan extends DynamicDrawableSpan {
 
  private final Context mContext;
  private final int mResourceId;
 
  public MyDynamicDrawableSpan(Context context, @DrawableRes int resourceId) {
      mContext = context;
      mResourceId = resourceId;
  }
 
  @Override
  public Drawable getDrawable() {
       Drawable drawable = mContext.getDrawable(mResourceId);
       drawable.setBounds(0, 0, drawable.getIntrinsicWidth(), drawable.getIntrinsicHeight());
       return drawable;
  }
  }
```
The class can be used like this:

```kotlin
SpannableString string = new SpannableString("Text with a drawable span");
  string.setSpan(new MyDynamicDrawableSpan(context, R.mipmap.ic_launcher), 12, 20, Spanned
  .SPAN_EXCLUSIVE_EXCLUSIVE);
```
Replacing text with a drawable.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_BASELINE:kotlin.Int` A constant indicating that the bottom of this span should be aligned with the baseline of the surrounding text. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_BOTTOM:kotlin.Int` A constant indicating that the bottom of this span should be aligned with the bottom of the surrounding text, i. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_CENTER:kotlin.Int` A constant indicating that this span should be vertically centered between the top and the lowest descender. |
| --- | --- |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#DynamicDrawableSpan()()` Creates a `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#`. |

| Protected constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#DynamicDrawableSpan(kotlin.Int)(verticalAlignment: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Creates a `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#` based on a vertical alignment. |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#draw(android.graphics.Canvas,%20kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int,%20kotlin.Float,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20android.graphics.Paint)(canvas: https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#, text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, end: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, top: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, bottom: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, paint: https://developer.android.com/reference/kotlin/android/graphics/Paint.html#)` Draws the span into the canvas. |
| abstract [Drawable](../android.graphics.drawable/Drawable.md)! | `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#getDrawable()()` Your subclass must implement this method to provide the bitmap to be drawn. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#getSize(android.graphics.Paint,%20kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int,%20android.graphics.Paint.FontMetricsInt)(paint: https://developer.android.com/reference/kotlin/android/graphics/Paint.html#, text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, end: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, fm: https://developer.android.com/reference/kotlin/android/graphics/Paint.FontMetricsInt.html#?)` Returns the width of the span. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#getVerticalAlignment()()` Returns the vertical alignment of this span, one of `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_BOTTOM:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_BASELINE:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_CENTER:kotlin.Int`. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#toString()()` Returns a string representation of the object. |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/text/style/ReplacementSpan` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?` | `https://developer.android.com/reference/kotlin/android/text/style/ReplacementSpan#getContentDescription()()` Gets a brief description of this ReplacementSpan for use in accessibility support. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/text/style/ReplacementSpan#setContentDescription(kotlin.CharSequence)(contentDescription: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?)` Sets the specific content description into ReplacementSpan. ReplacementSpans are shared with accessibility services, but only the content description is available from them. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/text/style/ReplacementSpan#updateDrawState(android.text.TextPaint)(ds: https://developer.android.com/reference/kotlin/android/text/TextPaint.html#!)` This method does nothing, since ReplacementSpans are drawn explicitly instead of affecting Paint properties. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/text/style/ReplacementSpan#updateMeasureState(android.text.TextPaint)(p: https://developer.android.com/reference/kotlin/android/text/TextPaint.html#)` This method does nothing, since ReplacementSpans are measured explicitly instead of affecting Paint properties. <br /> | ||
| From class `https://developer.android.com/reference/kotlin/android/text/style/MetricAffectingSpan` |---|---| | `https://developer.android.com/reference/kotlin/android/text/style/MetricAffectingSpan!` | `https://developer.android.com/reference/kotlin/android/text/style/MetricAffectingSpan#getUnderlying()()` Returns "this" for most MetricAffectingSpans, but for MetricAffectingSpans that were generated by `https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle#wrap(android.text.style.CharacterStyle)`, returns the underlying MetricAffectingSpan. <br /> | ||
| From class `https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle#updateDrawState(android.text.TextPaint)(tp: https://developer.android.com/reference/kotlin/android/text/TextPaint.html#!)` <br /> | | `https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle!` | `https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle#wrap(android.text.style.CharacterStyle)(cs: https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle!)` A given CharacterStyle can only applied to a single region of a given Spanned. If you need to attach the same CharacterStyle to multiple regions, you can use this method to wrap it with a new object that will have the same effect but be a distinct object so that it can also be attached without conflict. <br /> | ||
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Properties ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#mVerticalAlignment:kotlin.Int` <br /> |

## Constants

### ALIGN_BASELINE

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ALIGN_BASELINE: Int
```

A constant indicating that the bottom of this span should be aligned with the baseline of the surrounding text.

 Value: 1

### ALIGN_BOTTOM

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ALIGN_BOTTOM: Int
```

A constant indicating that the bottom of this span should be aligned with the bottom of the surrounding text, i.e., at the same level as the lowest descender in the text.

 Value: 0

### ALIGN_CENTER

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ALIGN_CENTER: Int
```

A constant indicating that this span should be vertically centered between the top and the lowest descender.

 Value: 2

## Public constructors

### DynamicDrawableSpan

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
DynamicDrawableSpan()
```

Creates a `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#`. The default vertical alignment is `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_BOTTOM:kotlin.Int`

## Protected constructors

### DynamicDrawableSpan

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected DynamicDrawableSpan(verticalAlignment: Int)
```

Creates a `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#` based on a vertical alignment.\\

| Parameters ||
|---|---|
| `verticalAlignment` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): one of `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_BOTTOM:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_BASELINE:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_CENTER:kotlin.Int` Value is one of the following: - `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_BOTTOM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_BASELINE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_CENTER:kotlin.Int` |

## Public methods

### draw

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun draw(
    canvas: Canvas, 
    text: CharSequence!, 
    start: Int, 
    end: Int, 
    x: Float, 
    top: Int, 
    y: Int, 
    bottom: Int, 
    paint: Paint
): Unit
```

Draws the span into the canvas.

| Parameters ||
|---|---|
| `canvas` | [Canvas](../android.graphics/Canvas.md): This value cannot be `null`. |
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: Current text. |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is 0 or greater |
| --- | --- |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is 0 or greater |
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): Edge of the replacement closest to the leading margin. |
| `top` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Top of the line. |
| --- | --- |
| `y` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Baseline. |
| `bottom` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Bottom of the line. |
| `paint` | [Paint](../android.graphics/Paint.md): This value cannot be `null`. |
| --- | --- |

### getDrawable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getDrawable(): Drawable!
```

Your subclass must implement this method to provide the bitmap to be drawn. The dimensions of the bitmap must be the same from each call to the next.

### getSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSize(
    paint: Paint, 
    text: CharSequence!, 
    start: Int, 
    end: Int, 
    fm: Paint.FontMetricsInt?
): Int
```

Returns the width of the span. Extending classes can set the height of the span by updating attributes of `https://developer.android.com/reference/kotlin/android/graphics/Paint.FontMetricsInt.html#`. If the span covers the whole text, and the height is not set, `https://developer.android.com/reference/kotlin/android/text/style/ReplacementSpan#draw(android.graphics.Canvas,%20kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int,%20kotlin.Float,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20android.graphics.Paint)` will not be called for the span.

| Parameters ||
|---|---|
| `paint` | [Paint](../android.graphics/Paint.md): This value cannot be `null`. |
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: Current text. |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is 0 or greater |
| --- | --- |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is 0 or greater |
| `fm` | [Paint.FontMetricsInt](../android/graphics/Paint.FontMetricsInt.md)?: This value may be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Width of the span. |

### getVerticalAlignment

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getVerticalAlignment(): Int
```

Returns the vertical alignment of this span, one of `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_BOTTOM:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_BASELINE:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_CENTER:kotlin.Int`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_BOTTOM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_BASELINE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_CENTER:kotlin.Int` |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

## Properties

### mVerticalAlignment

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected val mVerticalAlignment: Int
```
