# IconMarginSpan

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IconMarginSpan

Kotlin| [Java](https://developer.android.com/reference/android/text/style/IconMarginSpan "View this page in Java") 

```
open class IconMarginSpan : LeadingMarginSpan, LineHeightSpan
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.text.style.IconMarginSpan](https://developer.android.com/reference/kotlin/android/text/style/IconMarginSpan#) |

Paragraph affecting span, that draws a bitmap at the beginning of a text. The span also allows setting a padding between the bitmap and the text. The default value of the padding is 0px. The span should be attached from the first character of the text.

For example, an`IconMarginSpan`with a bitmap and a padding of 30px can be set like this: 

```kotlin
SpannableString string = new SpannableString("Text with icon and padding");
  string.setSpan(new IconMarginSpan(bitmap, 30), 0, string.length(),
  Spanned.SPAN_EXCLUSIVE_EXCLUSIVE);
  
```
Text with`IconMarginSpan`

<br />

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [IconMarginSpan](https://developer.android.com/reference/kotlin/android/text/style/IconMarginSpan#IconMarginSpan(android.graphics.Bitmap))`(`bitmap:` ` [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)`)` Creates an [IconMarginSpan](https://developer.android.com/reference/kotlin/android/text/style/IconMarginSpan#) from a [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#). |
| [IconMarginSpan](https://developer.android.com/reference/kotlin/android/text/style/IconMarginSpan#IconMarginSpan(android.graphics.Bitmap,%20kotlin.Int))`(`bitmap:` ` [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)`, `pad:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates an [IconMarginSpan](https://developer.android.com/reference/kotlin/android/text/style/IconMarginSpan#) from a [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#). |

| Public methods ||
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [chooseHeight](https://developer.android.com/reference/kotlin/android/text/style/IconMarginSpan#chooseHeight(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20android.graphics.Paint.FontMetricsInt))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `istartv:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `v:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `fm:` ` [Paint.FontMetricsInt](https://developer.android.com/reference/kotlin/android/graphics/Paint.FontMetricsInt.html#)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [drawLeadingMargin](https://developer.android.com/reference/kotlin/android/text/style/IconMarginSpan#drawLeadingMargin(android.graphics.Canvas,%20android.graphics.Paint,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20android.text.Layout))`(`c:` ` [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#)!`, `p:` ` [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint.html#)!`, `x:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dir:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `top:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `baseline:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bottom:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `first:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `layout:` ` [Layout](https://developer.android.com/reference/kotlin/android/text/Layout.html#)!`)` <br /> |
| open [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#) | [getBitmap](https://developer.android.com/reference/kotlin/android/text/style/IconMarginSpan#getBitmap())`()` Returns the bitmap to be used at the beginning of the text |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLeadingMargin](https://developer.android.com/reference/kotlin/android/text/style/IconMarginSpan#getLeadingMargin(kotlin.Boolean))`(`first:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPadding](https://developer.android.com/reference/kotlin/android/text/style/IconMarginSpan#getPadding())`()` Returns the padding width between the bitmap and the text. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/text/style/IconMarginSpan#toString())`()` <br /> |

## Public constructors

### IconMarginSpan

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
IconMarginSpan(bitmap: Bitmap)
```

Creates an [IconMarginSpan](https://developer.android.com/reference/kotlin/android/text/style/IconMarginSpan#) from a [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#).

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `bitmap` | [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#):bitmap to be rendered at the beginning of the text This value cannot be`null`. |

### IconMarginSpan

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
IconMarginSpan(
    bitmap: Bitmap, 
    pad: Int)
```

Creates an [IconMarginSpan](https://developer.android.com/reference/kotlin/android/text/style/IconMarginSpan#) from a [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#).

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `bitmap` | [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#):bitmap to be rendered at the beginning of the text This value cannot be`null`. |
| `pad` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):padding width, in pixels, between the bitmap and the text Value is 0 or greater |

## Public methods

### chooseHeight

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun chooseHeight(
    text: CharSequence!, 
    start: Int, 
    end: Int, 
    istartv: Int, 
    v: Int, 
    fm: Paint.FontMetricsInt!
): Unit
```

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the text |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the start of the line |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the end of the line |
| `spanstartv` | the start of the span |
| `lineHeight` | the line height |
| `fm` | [Paint.FontMetricsInt](https://developer.android.com/reference/kotlin/android/graphics/Paint.FontMetricsInt.html#)!:font metrics of the paint, in integers |

### drawLeadingMargin

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun drawLeadingMargin(
    c: Canvas!, 
    p: Paint!, 
    x: Int, 
    dir: Int, 
    top: Int, 
    baseline: Int, 
    bottom: Int, 
    text: CharSequence!, 
    start: Int, 
    end: Int, 
    first: Boolean, 
    layout: Layout!
): Unit
```

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `c` | [Canvas](https://developer.android.com/reference/kotlin/android/graphics/Canvas.html#)!:the canvas |
| `p` | [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint.html#)!:the paint. The this should be left unchanged on exit. |
| `x` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the current position of the margin |
| `dir` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the base direction of the paragraph; if negative, the margin is to the right of the text, otherwise it is to the left. |
| `top` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the top of the line |
| `baseline` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the baseline of the line |
| `bottom` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the bottom of the line |
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the text |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the start of the line |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the end of the line |
| `first` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if this is the first line of its paragraph |
| `layout` | [Layout](https://developer.android.com/reference/kotlin/android/text/Layout.html#)!:the layout containing this line |

### getBitmap

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getBitmap(): Bitmap
```

Returns the bitmap to be used at the beginning of the text

| Return ||
|----------------------------------------------------------------------------------------|--------------------------------------|
| [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#) | a bitmap This value cannot be`null`. |

### getLeadingMargin

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLeadingMargin(first: Boolean): Int
```

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `first` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if the request is for the first line of a paragraph, false for subsequent lines |

| Return ||
|----------------------------------------------------------------------------|----------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the offset for the margin. |

### getPadding

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPadding(): Int
```

Returns the padding width between the bitmap and the text. 
The units of this value are pixels.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a padding width in pixels The units of this value are pixels. |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |
