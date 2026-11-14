# TypefaceSpan

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TypefaceSpan

Kotlin| [Java](https://developer.android.com/reference/android/text/style/TypefaceSpan "View this page in Java") 
| --- | --- |

```
open class TypefaceSpan : MetricAffectingSpan, ParcelableSpan
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [android.text.style.CharacterStyle](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle) |||
| | ↳ | [android.text.style.MetricAffectingSpan](https://developer.android.com/reference/kotlin/android/text/style/MetricAffectingSpan) ||
| | | ↳ | [android.text.style.TypefaceSpan](https://developer.android.com/reference/kotlin/android/text/style/TypefaceSpan#) |
| --- | --- | --- | --- |

Span that updates the typeface of the text it's attached to. The`TypefaceSpan`can be constructed either based on a font family or based on a`Typeface`. When [TypefaceSpan(java.lang.String)](https://developer.android.com/reference/kotlin/android/text/style/TypefaceSpan#TypefaceSpan(kotlin.String))is used, the previous style of the`TextView`is kept. When [TypefaceSpan(android.graphics.Typeface)](https://developer.android.com/reference/kotlin/android/text/style/TypefaceSpan#TypefaceSpan(android.graphics.Typeface))is used, the`Typeface`style replaces the`TextView`'s style.

For example, let's consider a`TextView`with`android:textStyle="italic"`and a typeface created based on a font from resources, with a bold style. When applying a`TypefaceSpan`based the typeface, the text will only keep the bold style, overriding the`TextView`'s textStyle. When applying a`TypefaceSpan`based on a font family: "monospace", the resulted text will keep the italic style. 

```kotlin
Typeface myTypeface = Typeface.create(ResourcesCompat.getFont(context, R.font.acme),
  Typeface.BOLD);
  SpannableString string = new SpannableString("Text with typeface span.");
  string.setSpan(new TypefaceSpan(myTypeface), 10, 18, Spannable.SPAN_EXCLUSIVE_EXCLUSIVE);
  string.setSpan(new TypefaceSpan("monospace"), 19, 22, Spannable.SPAN_EXCLUSIVE_EXCLUSIVE);
  
```
Text with`TypefaceSpan`s constructed based on a font from resource and from a font family.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [TypefaceSpan](https://developer.android.com/reference/kotlin/android/text/style/TypefaceSpan#TypefaceSpan(android.graphics.Typeface))`(`typeface:` ` [Typeface](https://developer.android.com/reference/kotlin/android/graphics/Typeface.html#)`)` Constructs a [TypefaceSpan](https://developer.android.com/reference/kotlin/android/text/style/TypefaceSpan#) from a [Typeface](https://developer.android.com/reference/kotlin/android/graphics/Typeface.html#). |
| [TypefaceSpan](https://developer.android.com/reference/kotlin/android/text/style/TypefaceSpan#TypefaceSpan(android.os.Parcel))`(`src:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`)` Constructs a [TypefaceSpan](https://developer.android.com/reference/kotlin/android/text/style/TypefaceSpan#) from a parcel. |
| [TypefaceSpan](https://developer.android.com/reference/kotlin/android/text/style/TypefaceSpan#TypefaceSpan(kotlin.String))`(`family:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Constructs a [TypefaceSpan](https://developer.android.com/reference/kotlin/android/text/style/TypefaceSpan#) based on the font family. |

| Public methods ||
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/text/style/TypefaceSpan#describeContents())`()` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getFamily](https://developer.android.com/reference/kotlin/android/text/style/TypefaceSpan#getFamily())`()` Returns the font family name set in the span. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSpanTypeId](https://developer.android.com/reference/kotlin/android/text/style/TypefaceSpan#getSpanTypeId())`()` <br /> |
| --- | --- |
| open [Typeface](https://developer.android.com/reference/kotlin/android/graphics/Typeface.html#)? | [getTypeface](https://developer.android.com/reference/kotlin/android/text/style/TypefaceSpan#getTypeface())`()` Returns the typeface set in the span. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/text/style/TypefaceSpan#toString())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateDrawState](https://developer.android.com/reference/kotlin/android/text/style/TypefaceSpan#updateDrawState(android.text.TextPaint))`(`ds:` ` [TextPaint](https://developer.android.com/reference/kotlin/android/text/TextPaint.html#)`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateMeasureState](https://developer.android.com/reference/kotlin/android/text/style/TypefaceSpan#updateMeasureState(android.text.TextPaint))`(`paint:` ` [TextPaint](https://developer.android.com/reference/kotlin/android/text/TextPaint.html#)`)` Classes that extend MetricAffectingSpan implement this method to update the text formatting in a way that can change the width or height of characters. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/text/style/TypefaceSpan#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Inherited functions ||
|---|---|
| From class [MetricAffectingSpan](https://developer.android.com/reference/kotlin/android/text/style/MetricAffectingSpan) |---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [MetricAffectingSpan](https://developer.android.com/reference/kotlin/android/text/style/MetricAffectingSpan)! | [getUnderlying](https://developer.android.com/reference/kotlin/android/text/style/MetricAffectingSpan#getUnderlying())`()` <br /> Returns "this" for most MetricAffectingSpans, but for MetricAffectingSpans that were generated by [wrap](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle#wrap(android.text.style.CharacterStyle)), returns the underlying MetricAffectingSpan. <br /> | ||
| From class [CharacterStyle](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle) |-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateDrawState](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle#updateDrawState(android.text.TextPaint))`(`tp:` ` [TextPaint](https://developer.android.com/reference/kotlin/android/text/TextPaint.html#)!`)` <br /> | | [CharacterStyle](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle)! | [wrap](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle#wrap(android.text.style.CharacterStyle))`(`cs:` ` [CharacterStyle](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle)!`)` <br /> A given CharacterStyle can only applied to a single region of a given Spanned. If you need to attach the same CharacterStyle to multiple regions, you can use this method to wrap it with a new object that will have the same effect but be a distinct object so that it can also be attached without conflict. <br /> | ||

## Public constructors

### TypefaceSpan

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TypefaceSpan(typeface: Typeface)
```

Constructs a [TypefaceSpan](https://developer.android.com/reference/kotlin/android/text/style/TypefaceSpan#) from a [Typeface](https://developer.android.com/reference/kotlin/android/graphics/Typeface.html#). The previous style of the TextPaint is overridden and the style of the typeface is used.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------|
| `typeface` | [Typeface](https://developer.android.com/reference/kotlin/android/graphics/Typeface.html#):the typeface This value cannot be`null`. |

### TypefaceSpan

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TypefaceSpan(src: Parcel)
```

Constructs a [TypefaceSpan](https://developer.android.com/reference/kotlin/android/text/style/TypefaceSpan#) from a parcel.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------|
| `src` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):This value cannot be`null`. |

### TypefaceSpan

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TypefaceSpan(family: String?)
```

Constructs a [TypefaceSpan](https://developer.android.com/reference/kotlin/android/text/style/TypefaceSpan#) based on the font family. The previous style of the TextPaint is kept. If the font family is null, the text paint is not modified.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `family` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The font family for this typeface. Examples include "monospace", "serif", and "sans-serif" This value may be`null`. |

## Public methods

### describeContents

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getFamily

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFamily(): String?
```

Returns the font family name set in the span.

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | the font family name This value may be`null`. |

**See Also**

- [#TypefaceSpan(String)](https://developer.android.com/reference/kotlin/android/text/style/TypefaceSpan#TypefaceSpan(kotlin.String)) 

### getSpanTypeId

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSpanTypeId(): Int
```  

### getTypeface

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTypeface(): Typeface?
```

Returns the typeface set in the span.

| Return ||
|---------------------------------------------------------------------------------------------|-------------------------------------------|
| [Typeface](https://developer.android.com/reference/kotlin/android/graphics/Typeface.html#)? | the typeface set This value may be`null`. |

**See Also**

- [#TypefaceSpan(Typeface)](https://developer.android.com/reference/kotlin/android/text/style/TypefaceSpan#TypefaceSpan(android.graphics.Typeface)) 

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

| Parameters ||
|------|----------------------------------------------------------------------------------------------------------------------|
| `ds` | [TextPaint](https://developer.android.com/reference/kotlin/android/text/TextPaint.html#):This value cannot be`null`. |

### updateMeasureState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun updateMeasureState(paint: TextPaint): Unit
```

Classes that extend MetricAffectingSpan implement this method to update the text formatting in a way that can change the width or height of characters.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------|
| `textPaint` | the paint used for drawing the text This value cannot be`null`. |
| `paint` | [TextPaint](https://developer.android.com/reference/kotlin/android/text/TextPaint.html#):This value cannot be`null`. |

### writeToParcel

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |
