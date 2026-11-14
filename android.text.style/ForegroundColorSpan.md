Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ForegroundColorSpan

Kotlin| [Java](https://developer.android.com/reference/android/text/style/ForegroundColorSpan "View this page in Java") 
| --- | --- |

```
open class ForegroundColorSpan : CharacterStyle, ParcelableSpan, UpdateAppearance
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.text.style.CharacterStyle](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle) ||
| | ↳ | [android.text.style.ForegroundColorSpan](https://developer.android.com/reference/kotlin/android/text/style/ForegroundColorSpan#) |

Changes the color of the text to which the span is attached.

For example, to set a green text color you would create a based on the text and set the span. 

```kotlin
<code>SpannableString string = new SpannableString("Text with a foreground color span");
 string.setSpan(new ForegroundColorSpan(color), 12, 28, Spanned.SPAN_EXCLUSIVE_EXCLUSIVE);</code>
```
Set a text color.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ForegroundColorSpan](https://developer.android.com/reference/kotlin/android/text/style/ForegroundColorSpan#ForegroundColorSpan(android.os.Parcel))`(`src:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`)` Creates a [ForegroundColorSpan](https://developer.android.com/reference/kotlin/android/text/style/ForegroundColorSpan#) from a parcel. |
| [ForegroundColorSpan](https://developer.android.com/reference/kotlin/android/text/style/ForegroundColorSpan#ForegroundColorSpan(kotlin.Int))`(`color:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a [ForegroundColorSpan](https://developer.android.com/reference/kotlin/android/text/style/ForegroundColorSpan#) from a color integer. |

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/text/style/ForegroundColorSpan#describeContents())`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getForegroundColor](https://developer.android.com/reference/kotlin/android/text/style/ForegroundColorSpan#getForegroundColor())`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSpanTypeId](https://developer.android.com/reference/kotlin/android/text/style/ForegroundColorSpan#getSpanTypeId())`()` <br /> |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/text/style/ForegroundColorSpan#toString())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateDrawState](https://developer.android.com/reference/kotlin/android/text/style/ForegroundColorSpan#updateDrawState(android.text.TextPaint))`(`textPaint:` ` [TextPaint](https://developer.android.com/reference/kotlin/android/text/TextPaint.html#)`)` Updates the color of the TextPaint to the foreground color. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/text/style/ForegroundColorSpan#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [CharacterStyle](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle) |-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [CharacterStyle](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle)! | [getUnderlying](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle#getUnderlying())`()` <br /> Returns "this" for most CharacterStyles, but for CharacterStyles that were generated by [wrap](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle#wrap(android.text.style.CharacterStyle)), returns the underlying CharacterStyle. <br /> | | [CharacterStyle](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle)! | [wrap](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle#wrap(android.text.style.CharacterStyle))`(`cs:` ` [CharacterStyle](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle)!`)` <br /> A given CharacterStyle can only applied to a single region of a given Spanned. If you need to attach the same CharacterStyle to multiple regions, you can use this method to wrap it with a new object that will have the same effect but be a distinct object so that it can also be attached without conflict. <br /> | ||

## Public constructors

### ForegroundColorSpan

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ForegroundColorSpan(src: Parcel)
```

Creates a [ForegroundColorSpan](https://developer.android.com/reference/kotlin/android/text/style/ForegroundColorSpan#) from a parcel.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------|
| `src` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):This value cannot be`null`. |

### ForegroundColorSpan

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ForegroundColorSpan(color: Int)
```

Creates a [ForegroundColorSpan](https://developer.android.com/reference/kotlin/android/text/style/ForegroundColorSpan#) from a color integer.

To get the color integer associated with a particular color resource ID, use android.content.res.Resources#getColor(int, Resources.Theme)

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------|
| `color` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):color integer that defines the text color |

## Public methods

### describeContents

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getForegroundColor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getForegroundColor(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the foreground color of this span. |

**See Also**

- [android.text.style.ForegroundColorSpan#ForegroundColorSpan(int)](https://developer.android.com/reference/kotlin/android/text/style/ForegroundColorSpan#ForegroundColorSpan(kotlin.Int)) 

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

Updates the color of the TextPaint to the foreground color.

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

Flatten this object in to a Parcel.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |
