# TypefaceSpan

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TypefaceSpan

Kotlin| [Java](../android/text/style/TypefaceSpan.md) 
| --- | --- |

```
open class TypefaceSpan : MetricAffectingSpan, ParcelableSpan
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [android.text.style.CharacterStyle](../android/text/style/CharacterStyle.md) |||
| | ↳ | [android.text.style.MetricAffectingSpan](../android/text/style/MetricAffectingSpan.md) ||
| | | ↳ | [android.text.style.TypefaceSpan](../android/text/style/TypefaceSpan.md) |
| --- | --- | --- | --- |

Span that updates the typeface of the text it's attached to. The`TypefaceSpan`can be constructed either based on a font family or based on a`Typeface`. When [TypefaceSpan(java.lang.String)](../android/text/style/TypefaceSpan.md))is used, the previous style of the`TextView`is kept. When [TypefaceSpan(android.graphics.Typeface)](../android/text/style/TypefaceSpan.md))is used, the`Typeface`style replaces the`TextView`'s style.

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
| [TypefaceSpan](../android/text/style/TypefaceSpan.md))`(`typeface:` ` [Typeface](../android/graphics/Typeface.md)`)` Constructs a [TypefaceSpan](../android/text/style/TypefaceSpan.md) from a [Typeface](../android/graphics/Typeface.md). |
| [TypefaceSpan](../android/text/style/TypefaceSpan.md))`(`src:` ` [Parcel](../android/os/Parcel.md)`)` Constructs a [TypefaceSpan](../android/text/style/TypefaceSpan.md) from a parcel. |
| [TypefaceSpan](../android/text/style/TypefaceSpan.md))`(`family:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Constructs a [TypefaceSpan](../android/text/style/TypefaceSpan.md) based on the font family. |

| Public methods ||
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/text/style/TypefaceSpan.md))`()` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getFamily](../android/text/style/TypefaceSpan.md))`()` Returns the font family name set in the span. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSpanTypeId](../android/text/style/TypefaceSpan.md))`()` <br /> |
| --- | --- |
| open [Typeface](../android/graphics/Typeface.md)? | [getTypeface](../android/text/style/TypefaceSpan.md))`()` Returns the typeface set in the span. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/text/style/TypefaceSpan.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateDrawState](../android/text/style/TypefaceSpan.md))`(`ds:` ` [TextPaint](../android/text/TextPaint.md)`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateMeasureState](../android/text/style/TypefaceSpan.md))`(`paint:` ` [TextPaint](../android/text/TextPaint.md)`)` Classes that extend MetricAffectingSpan implement this method to update the text formatting in a way that can change the width or height of characters. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/text/style/TypefaceSpan.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Inherited functions ||
|---|---|
| From class [MetricAffectingSpan](../android/text/style/MetricAffectingSpan.md) |---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [MetricAffectingSpan](../android/text/style/MetricAffectingSpan.md)! | [getUnderlying](../android/text/style/MetricAffectingSpan.md))`()` <br /> Returns "this" for most MetricAffectingSpans, but for MetricAffectingSpans that were generated by [wrap](../android/text/style/CharacterStyle.md)), returns the underlying MetricAffectingSpan. <br /> | ||
| From class [CharacterStyle](../android/text/style/CharacterStyle.md) |-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateDrawState](../android/text/style/CharacterStyle.md))`(`tp:` ` [TextPaint](../android/text/TextPaint.md)!`)` <br /> | | [CharacterStyle](../android/text/style/CharacterStyle.md)! | [wrap](../android/text/style/CharacterStyle.md))`(`cs:` ` [CharacterStyle](../android/text/style/CharacterStyle.md)!`)` <br /> A given CharacterStyle can only applied to a single region of a given Spanned. If you need to attach the same CharacterStyle to multiple regions, you can use this method to wrap it with a new object that will have the same effect but be a distinct object so that it can also be attached without conflict. <br /> | ||

## Public constructors

### TypefaceSpan

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TypefaceSpan(typeface: Typeface)
```

Constructs a [TypefaceSpan](../android/text/style/TypefaceSpan.md) from a [Typeface](../android/graphics/Typeface.md). The previous style of the TextPaint is overridden and the style of the typeface is used.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------|
| `typeface` | [Typeface](../android/graphics/Typeface.md):the typeface This value cannot be`null`. |

### TypefaceSpan

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TypefaceSpan(src: Parcel)
```

Constructs a [TypefaceSpan](../android/text/style/TypefaceSpan.md) from a parcel.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------|
| `src` | [Parcel](../android/os/Parcel.md):This value cannot be`null`. |

### TypefaceSpan

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TypefaceSpan(family: String?)
```

Constructs a [TypefaceSpan](../android/text/style/TypefaceSpan.md) based on the font family. The previous style of the TextPaint is kept. If the font family is null, the text paint is not modified.

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

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

- [#TypefaceSpan(String)](../android/text/style/TypefaceSpan.md)) 

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
| [Typeface](../android/graphics/Typeface.md)? | the typeface set This value may be`null`. |

**See Also**

- [#TypefaceSpan(Typeface)](../android/text/style/TypefaceSpan.md)) 

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
| `ds` | [TextPaint](../android/text/TextPaint.md):This value cannot be`null`. |

### updateMeasureState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun updateMeasureState(paint: TextPaint): Unit
```

Classes that extend MetricAffectingSpan implement this method to update the text formatting in a way that can change the width or height of characters.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------|
| `textPaint` | the paint used for drawing the text This value cannot be`null`. |
| `paint` | [TextPaint](../android/text/TextPaint.md):This value cannot be`null`. |

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
| `dest` | [Parcel](../android/os/Parcel.md):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |
