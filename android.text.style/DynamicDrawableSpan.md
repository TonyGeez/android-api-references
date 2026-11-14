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

For an implementation that constructs the drawable from various sources (`Bitmap`, `Drawable`, resource id or `Uri`) use ImageSpan.

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
| DynamicDrawableSpan Creates a DynamicDrawableSpan. |

| Protected constructors ||
|---|---|
| DynamicDrawableSpan Creates a DynamicDrawableSpan based on a vertical alignment. |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | draw Draws the span into the canvas. |
| abstract [Drawable](../android.graphics.drawable/Drawable.md)! | getDrawable Your subclass must implement this method to provide the bitmap to be drawn. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getSize Returns the width of the span. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getVerticalAlignment Returns the vertical alignment of this span, one of `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_BOTTOM:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_BASELINE:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_CENTER:kotlin.Int`. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | toString Returns a string representation of the object. |

| Inherited functions ||
|---|---|
| From class ReplacementSpan |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?` | getContentDescription Gets a brief description of this ReplacementSpan for use in accessibility support. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setContentDescription Sets the specific content description into ReplacementSpan. ReplacementSpans are shared with accessibility services, but only the content description is available from them. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | updateDrawState This method does nothing, since ReplacementSpans are drawn explicitly instead of affecting Paint properties. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | updateMeasureState This method does nothing, since ReplacementSpans are measured explicitly instead of affecting Paint properties. <br /> | ||
| From class MetricAffectingSpan |---|---| | `https://developer.android.com/reference/kotlin/android/text/style/MetricAffectingSpan!` | getUnderlying Returns "this" for most MetricAffectingSpans, but for MetricAffectingSpans that were generated by wrap, returns the underlying MetricAffectingSpan. <br /> | ||
| From class CharacterStyle |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | updateDrawState <br /> | | `https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle!` | wrap A given CharacterStyle can only applied to a single region of a given Spanned. If you need to attach the same CharacterStyle to multiple regions, you can use this method to wrap it with a new object that will have the same effect but be a distinct object so that it can also be attached without conflict. <br /> | ||
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

Creates a DynamicDrawableSpan. The default vertical alignment is `https://developer.android.com/reference/kotlin/android/text/style/DynamicDrawableSpan#ALIGN_BOTTOM:kotlin.Int`

## Protected constructors

### DynamicDrawableSpan

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected DynamicDrawableSpan(verticalAlignment: Int)
```

Creates a DynamicDrawableSpan based on a vertical alignment.\\

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

Returns the width of the span. Extending classes can set the height of the span by updating attributes of `https://developer.android.com/reference/kotlin/android/graphics/Paint.FontMetricsInt.html#`. If the span covers the whole text, and the height is not set, draw will not be called for the span.

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
