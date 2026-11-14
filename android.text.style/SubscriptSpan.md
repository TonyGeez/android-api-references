# SubscriptSpan

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SubscriptSpan

Kotlin| [Java](https://developer.android.com/reference/android/text/style/SubscriptSpan "View this page in Java") 
| --- | --- |

```
open class SubscriptSpan : MetricAffectingSpan, ParcelableSpan
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [android.text.style.CharacterStyle](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle) |||
| | ↳ | [android.text.style.MetricAffectingSpan](https://developer.android.com/reference/kotlin/android/text/style/MetricAffectingSpan) ||
| | | ↳ | [android.text.style.SubscriptSpan](https://developer.android.com/reference/kotlin/android/text/style/SubscriptSpan#) |
| --- | --- | --- | --- |

The span that moves the position of the text baseline lower.

The span can be used like this: 

```kotlin
<code>SpannableString string = new SpannableString("☕- C8H10N4O2\n");
 string.setSpan(new SubscriptSpan(), 4, 5, Spanned.SPAN_EXCLUSIVE_EXCLUSIVE);
 string.setSpan(new SubscriptSpan(), 6, 8, Spanned.SPAN_EXCLUSIVE_EXCLUSIVE);
 string.setSpan(new SubscriptSpan(), 9, 10, Spanned.SPAN_EXCLUSIVE_EXCLUSIVE);
 string.setSpan(new SubscriptSpan(), 11, 12, Spanned.SPAN_EXCLUSIVE_EXCLUSIVE);</code>
```
Text with`SubscriptSpan`. Note: Since the span affects the position of the text, if the text is on the last line of a TextView, it may appear cut.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SubscriptSpan](https://developer.android.com/reference/kotlin/android/text/style/SubscriptSpan#SubscriptSpan())`()` Creates a [SubscriptSpan](https://developer.android.com/reference/kotlin/android/text/style/SubscriptSpan#). |
| [SubscriptSpan](https://developer.android.com/reference/kotlin/android/text/style/SubscriptSpan#SubscriptSpan(android.os.Parcel))`(`src:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`)` Creates a [SubscriptSpan](https://developer.android.com/reference/kotlin/android/text/style/SubscriptSpan#) from a parcel. |

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/text/style/SubscriptSpan#describeContents())`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSpanTypeId](https://developer.android.com/reference/kotlin/android/text/style/SubscriptSpan#getSpanTypeId())`()` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/text/style/SubscriptSpan#toString())`()` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateDrawState](https://developer.android.com/reference/kotlin/android/text/style/SubscriptSpan#updateDrawState(android.text.TextPaint))`(`textPaint:` ` [TextPaint](https://developer.android.com/reference/kotlin/android/text/TextPaint.html#)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateMeasureState](https://developer.android.com/reference/kotlin/android/text/style/SubscriptSpan#updateMeasureState(android.text.TextPaint))`(`textPaint:` ` [TextPaint](https://developer.android.com/reference/kotlin/android/text/TextPaint.html#)`)` Classes that extend MetricAffectingSpan implement this method to update the text formatting in a way that can change the width or height of characters. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/text/style/SubscriptSpan#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [MetricAffectingSpan](https://developer.android.com/reference/kotlin/android/text/style/MetricAffectingSpan) |---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [MetricAffectingSpan](https://developer.android.com/reference/kotlin/android/text/style/MetricAffectingSpan)! | [getUnderlying](https://developer.android.com/reference/kotlin/android/text/style/MetricAffectingSpan#getUnderlying())`()` <br /> Returns "this" for most MetricAffectingSpans, but for MetricAffectingSpans that were generated by [wrap](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle#wrap(android.text.style.CharacterStyle)), returns the underlying MetricAffectingSpan. <br /> | ||
| From class [CharacterStyle](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle) |-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateDrawState](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle#updateDrawState(android.text.TextPaint))`(`tp:` ` [TextPaint](https://developer.android.com/reference/kotlin/android/text/TextPaint.html#)!`)` <br /> | | [CharacterStyle](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle)! | [wrap](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle#wrap(android.text.style.CharacterStyle))`(`cs:` ` [CharacterStyle](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle)!`)` <br /> A given CharacterStyle can only applied to a single region of a given Spanned. If you need to attach the same CharacterStyle to multiple regions, you can use this method to wrap it with a new object that will have the same effect but be a distinct object so that it can also be attached without conflict. <br /> | ||

## Public constructors

### SubscriptSpan

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SubscriptSpan()
```

Creates a [SubscriptSpan](https://developer.android.com/reference/kotlin/android/text/style/SubscriptSpan#). 

### SubscriptSpan

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SubscriptSpan(src: Parcel)
```

Creates a [SubscriptSpan](https://developer.android.com/reference/kotlin/android/text/style/SubscriptSpan#) from a parcel.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------|
| `src` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):This value cannot be`null`. |

## Public methods

### describeContents

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

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
open fun updateDrawState(textPaint: TextPaint): Unit
```

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------|
| `textPaint` | [TextPaint](https://developer.android.com/reference/kotlin/android/text/TextPaint.html#):This value cannot be`null`. |

### updateMeasureState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun updateMeasureState(textPaint: TextPaint): Unit
```

Classes that extend MetricAffectingSpan implement this method to update the text formatting in a way that can change the width or height of characters.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------|
| `textPaint` | [TextPaint](https://developer.android.com/reference/kotlin/android/text/TextPaint.html#):This value cannot be`null`. |

### writeToParcel

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |
