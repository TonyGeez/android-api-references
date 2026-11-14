Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AbsoluteSizeSpan

```
open class AbsoluteSizeSpan : MetricAffectingSpan, ParcelableSpan
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [android.text.style.CharacterStyle](../android/text/style/CharacterStyle.md) |||
| | ↳ | [android.text.style.MetricAffectingSpan](../android/text/style/MetricAffectingSpan.md) ||
| | | ↳ | [android.text.style.AbsoluteSizeSpan](../android/text/style/AbsoluteSizeSpan.md) |
| --- | --- | --- | --- |

A span that changes the size of the text it's attached to.

For example, the size of the text can be changed to 55dp like this:

```kotlin
<code>SpannableString string = new SpannableString("Text with absolute size span");
 string.setSpan(new AbsoluteSizeSpan(55, true), 10, 23, Spanned.SPAN_EXCLUSIVE_EXCLUSIVE);</code>
```
Text with text size updated.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/text/style/AbsoluteSizeSpan#AbsoluteSizeSpan(android.os.Parcel)(src: https://developer.android.com/reference/kotlin/android/os/Parcel.html#)` Creates an `https://developer.android.com/reference/kotlin/android/text/style/AbsoluteSizeSpan#` from a parcel. |
| `https://developer.android.com/reference/kotlin/android/text/style/AbsoluteSizeSpan#AbsoluteSizeSpan(kotlin.Int)(size: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set the text size to `size` physical pixels. |
| `https://developer.android.com/reference/kotlin/android/text/style/AbsoluteSizeSpan#AbsoluteSizeSpan(kotlin.Int,%20kotlin.Boolean)(size: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, dip: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Set the text size to `size` physical pixels, or to `size` device-independent pixels if `dip` is true. |

| Public methods ||
|---|---|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/AbsoluteSizeSpan#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/AbsoluteSizeSpan#getDip()()` Returns whether the size is in device-independent pixels or not, depending on the `dip` flag passed in `https://developer.android.com/reference/kotlin/android/text/style/AbsoluteSizeSpan#AbsoluteSizeSpan(kotlin.Int,%20kotlin.Boolean)` |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/AbsoluteSizeSpan#getSize()()` Get the text size. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/AbsoluteSizeSpan#getSpanTypeId()()` Return a special type identifier for this span class. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/AbsoluteSizeSpan#toString()()` Returns a string representation of the object. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/AbsoluteSizeSpan#updateDrawState(android.text.TextPaint)(ds: https://developer.android.com/reference/kotlin/android/text/TextPaint.html#)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/AbsoluteSizeSpan#updateMeasureState(android.text.TextPaint)(ds: https://developer.android.com/reference/kotlin/android/text/TextPaint.html#)` Classes that extend MetricAffectingSpan implement this method to update the text formatting in a way that can change the width or height of characters. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/text/style/AbsoluteSizeSpan#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

Inherited functions From class `https://developer.android.com/reference/kotlin/android/text/style/MetricAffectingSpan` `https://developer.android.com/reference/kotlin/android/text/style/MetricAffectingSpan!` `https://developer.android.com/reference/kotlin/android/text/style/MetricAffectingSpan#getUnderlying()()`

Returns "this" for most MetricAffectingSpans, but for MetricAffectingSpans that were generated by `https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle#wrap(android.text.style.CharacterStyle)`, returns the underlying MetricAffectingSpan.

<br />

From class `https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle#updateDrawState(android.text.TextPaint)(tp: https://developer.android.com/reference/kotlin/android/text/TextPaint.html#!)`

<br />

`https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle!` `https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle#wrap(android.text.style.CharacterStyle)(cs: https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle!)`

A given CharacterStyle can only applied to a single region of a given Spanned. If you need to attach the same CharacterStyle to multiple regions, you can use this method to wrap it with a new object that will have the same effect but be a distinct object so that it can also be attached without conflict.

<br />

## Public constructors

### AbsoluteSizeSpan

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
AbsoluteSizeSpan(src: Parcel)
```

Creates an `https://developer.android.com/reference/kotlin/android/text/style/AbsoluteSizeSpan#` from a parcel.

| Parameters ||
|---|---|
| `src` | [Parcel](../android/os/Parcel.md): This value cannot be `null`. |

### AbsoluteSizeSpan

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
AbsoluteSizeSpan(size: Int)
```

Set the text size to `size` physical pixels.

### AbsoluteSizeSpan

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
AbsoluteSizeSpan(
    size: Int, 
    dip: Boolean)
```

Set the text size to `size` physical pixels, or to `size` device-independent pixels if `dip` is true.

## Public methods

### describeContents

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getDip

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDip(): Boolean
```

Returns whether the size is in device-independent pixels or not, depending on the `dip` flag passed in `https://developer.android.com/reference/kotlin/android/text/style/AbsoluteSizeSpan#AbsoluteSizeSpan(kotlin.Int,%20kotlin.Boolean)`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the size is in device-independent pixels, `false` otherwise |

**See Also**

- `https://developer.android.com/reference/kotlin/android/text/style/AbsoluteSizeSpan#AbsoluteSizeSpan(kotlin.Int,%20kotlin.Boolean)`

### getSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSize(): Int
```

Get the text size. This is in physical pixels if `https://developer.android.com/reference/kotlin/android/text/style/AbsoluteSizeSpan#getDip()` returns false or in device-independent pixels if `https://developer.android.com/reference/kotlin/android/text/style/AbsoluteSizeSpan#getDip()` returns true.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the text size, either in physical pixels or device-independent pixels. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/text/style/AbsoluteSizeSpan#AbsoluteSizeSpan(kotlin.Int,%20kotlin.Boolean)`

### getSpanTypeId

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSpanTypeId(): Int
```

Return a special type identifier for this span class.

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### updateDrawState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun updateDrawState(ds: TextPaint): Unit
```

| Parameters ||
|---|---|
| `ds` | [TextPaint](../android/text/TextPaint.md): This value cannot be `null`. |

### updateMeasureState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun updateMeasureState(ds: TextPaint): Unit
```

Classes that extend MetricAffectingSpan implement this method to update the text formatting in a way that can change the width or height of characters.

| Parameters ||
|---|---|
| `textPaint` | the paint used for drawing the text. This value cannot be `null`. |
| `ds` | [TextPaint](../android/text/TextPaint.md): This value cannot be `null`. |

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
|---|---|
| `dest` | [Parcel](../android/os/Parcel.md): This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |
