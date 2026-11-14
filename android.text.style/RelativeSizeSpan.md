# RelativeSizeSpan

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RelativeSizeSpan

Kotlin| [Java](https://developer.android.com/reference/android/text/style/RelativeSizeSpan "View this page in Java") 
| --- | --- |

```
open class RelativeSizeSpan : MetricAffectingSpan, ParcelableSpan
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [android.text.style.CharacterStyle](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle) |||
| | ↳ | [android.text.style.MetricAffectingSpan](https://developer.android.com/reference/kotlin/android/text/style/MetricAffectingSpan) ||
| | | ↳ | [android.text.style.RelativeSizeSpan](https://developer.android.com/reference/kotlin/android/text/style/RelativeSizeSpan#) |
| --- | --- | --- | --- |

Uniformly scales the size of the text to which it's attached by a certain proportion.

For example, a`RelativeSizeSpan`that increases the text size by 50% can be constructed like this: 

```kotlin
<code>SpannableString string = new SpannableString("Text with relative size span");
 string.setSpan(new RelativeSizeSpan(1.5f), 10, 24, Spanned.SPAN_EXCLUSIVE_EXCLUSIVE);</code>
```
Text increased by 50% with`RelativeSizeSpan`.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [RelativeSizeSpan](https://developer.android.com/reference/kotlin/android/text/style/RelativeSizeSpan#RelativeSizeSpan(android.os.Parcel))`(`src:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`)` Creates a [RelativeSizeSpan](https://developer.android.com/reference/kotlin/android/text/style/RelativeSizeSpan#) from a parcel. |
| [RelativeSizeSpan](https://developer.android.com/reference/kotlin/android/text/style/RelativeSizeSpan#RelativeSizeSpan(kotlin.Float))`(`proportion:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Creates a [RelativeSizeSpan](https://developer.android.com/reference/kotlin/android/text/style/RelativeSizeSpan#) based on a proportion. |

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/text/style/RelativeSizeSpan#describeContents())`()` <br /> |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getSizeChange](https://developer.android.com/reference/kotlin/android/text/style/RelativeSizeSpan#getSizeChange())`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSpanTypeId](https://developer.android.com/reference/kotlin/android/text/style/RelativeSizeSpan#getSpanTypeId())`()` <br /> |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/text/style/RelativeSizeSpan#toString())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateDrawState](https://developer.android.com/reference/kotlin/android/text/style/RelativeSizeSpan#updateDrawState(android.text.TextPaint))`(`ds:` ` [TextPaint](https://developer.android.com/reference/kotlin/android/text/TextPaint.html#)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateMeasureState](https://developer.android.com/reference/kotlin/android/text/style/RelativeSizeSpan#updateMeasureState(android.text.TextPaint))`(`ds:` ` [TextPaint](https://developer.android.com/reference/kotlin/android/text/TextPaint.html#)`)` Classes that extend MetricAffectingSpan implement this method to update the text formatting in a way that can change the width or height of characters. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/text/style/RelativeSizeSpan#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Inherited functions ||
|---|---|
| From class [MetricAffectingSpan](https://developer.android.com/reference/kotlin/android/text/style/MetricAffectingSpan) |---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [MetricAffectingSpan](https://developer.android.com/reference/kotlin/android/text/style/MetricAffectingSpan)! | [getUnderlying](https://developer.android.com/reference/kotlin/android/text/style/MetricAffectingSpan#getUnderlying())`()` <br /> Returns "this" for most MetricAffectingSpans, but for MetricAffectingSpans that were generated by [wrap](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle#wrap(android.text.style.CharacterStyle)), returns the underlying MetricAffectingSpan. <br /> | ||
| From class [CharacterStyle](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle) |-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateDrawState](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle#updateDrawState(android.text.TextPaint))`(`tp:` ` [TextPaint](https://developer.android.com/reference/kotlin/android/text/TextPaint.html#)!`)` <br /> | | [CharacterStyle](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle)! | [wrap](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle#wrap(android.text.style.CharacterStyle))`(`cs:` ` [CharacterStyle](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle)!`)` <br /> A given CharacterStyle can only applied to a single region of a given Spanned. If you need to attach the same CharacterStyle to multiple regions, you can use this method to wrap it with a new object that will have the same effect but be a distinct object so that it can also be attached without conflict. <br /> | ||

## Public constructors

### RelativeSizeSpan

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
RelativeSizeSpan(src: Parcel)
```

Creates a [RelativeSizeSpan](https://developer.android.com/reference/kotlin/android/text/style/RelativeSizeSpan#) from a parcel.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------|
| `src` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):This value cannot be`null`. |

### RelativeSizeSpan

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
RelativeSizeSpan(proportion: Float)
```

Creates a [RelativeSizeSpan](https://developer.android.com/reference/kotlin/android/text/style/RelativeSizeSpan#) based on a proportion.

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| `proportion` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):the proportion with which the text is scaled. Value is 0.0f or greater |

## Public methods

### describeContents

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getSizeChange

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSizeChange(): Float
```

| Return ||
|--------------------------------------------------------------------------------|-----------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | the proportion with which the text size is changed. |

### getSpanTypeId

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSpanTypeId(): Int
```  

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
open fun updateMeasureState(ds: TextPaint): Unit
```

Classes that extend MetricAffectingSpan implement this method to update the text formatting in a way that can change the width or height of characters.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------|
| `textPaint` | the paint used for drawing the text This value cannot be`null`. |
| `ds` | [TextPaint](https://developer.android.com/reference/kotlin/android/text/TextPaint.html#):This value cannot be`null`. |

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
