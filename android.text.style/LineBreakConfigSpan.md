# LineBreakConfigSpan

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LineBreakConfigSpan

Kotlin| [Java](https://developer.android.com/reference/android/text/style/LineBreakConfigSpan "View this page in Java") 

```
class LineBreakConfigSpan : ParcelableSpan
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.text.style.LineBreakConfigSpan](https://developer.android.com/reference/kotlin/android/text/style/LineBreakConfigSpan#) |

LineBreakSpan for changing line break style of the specific region of the text.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [LineBreakConfigSpan](https://developer.android.com/reference/kotlin/android/text/style/LineBreakConfigSpan#LineBreakConfigSpan(android.graphics.text.LineBreakConfig))`(`lineBreakConfig:` ` [LineBreakConfig](https://developer.android.com/reference/kotlin/android/graphics/text/LineBreakConfig.html#)`)` Construct a new [LineBreakConfigSpan](https://developer.android.com/reference/kotlin/android/text/style/LineBreakConfigSpan#) |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [LineBreakConfigSpan](https://developer.android.com/reference/kotlin/android/text/style/LineBreakConfigSpan#) | [createNoBreakSpan](https://developer.android.com/reference/kotlin/android/text/style/LineBreakConfigSpan#createNoBreakSpan())`()` A specialized [LineBreakConfigSpan](https://developer.android.com/reference/kotlin/android/text/style/LineBreakConfigSpan#) that used for preventing line break. |
| static [LineBreakConfigSpan](https://developer.android.com/reference/kotlin/android/text/style/LineBreakConfigSpan#) | [createNoHyphenationSpan](https://developer.android.com/reference/kotlin/android/text/style/LineBreakConfigSpan#createNoHyphenationSpan())`()` A specialized [LineBreakConfigSpan](https://developer.android.com/reference/kotlin/android/text/style/LineBreakConfigSpan#) that used for preventing hyphenation. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/text/style/LineBreakConfigSpan#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/text/style/LineBreakConfigSpan#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [LineBreakConfig](https://developer.android.com/reference/kotlin/android/graphics/text/LineBreakConfig.html#) | [getLineBreakConfig](https://developer.android.com/reference/kotlin/android/text/style/LineBreakConfigSpan#getLineBreakConfig())`()` Gets an associated line break config. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSpanTypeId](https://developer.android.com/reference/kotlin/android/text/style/LineBreakConfigSpan#getSpanTypeId())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/text/style/LineBreakConfigSpan#hashCode())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/text/style/LineBreakConfigSpan#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/text/style/LineBreakConfigSpan#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [LineBreakConfigSpan](https://developer.android.com/reference/kotlin/android/text/style/LineBreakConfigSpan#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/text/style/LineBreakConfigSpan#CREATOR:android.os.Parcelable.Creator) <br /> |

## Public constructors

### LineBreakConfigSpan

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
LineBreakConfigSpan(lineBreakConfig: LineBreakConfig)
```

Construct a new [LineBreakConfigSpan](https://developer.android.com/reference/kotlin/android/text/style/LineBreakConfigSpan#)

| Parameters ||
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `lineBreakConfig` | [LineBreakConfig](https://developer.android.com/reference/kotlin/android/graphics/text/LineBreakConfig.html#):a line break config This value cannot be`null`. |

## Public methods

### createNoBreakSpan

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun createNoBreakSpan(): LineBreakConfigSpan
```

A specialized [LineBreakConfigSpan](https://developer.android.com/reference/kotlin/android/text/style/LineBreakConfigSpan#) that used for preventing line break. This is useful when you want to preserve some words in the same line. Note that even if this style is specified, the grapheme based line break is still performed for preventing clipping text.

| Return ||
|---------------------------------------------------------------------------------------------------------------|-----------------------------|
| [LineBreakConfigSpan](https://developer.android.com/reference/kotlin/android/text/style/LineBreakConfigSpan#) | This value cannot be`null`. |

**See Also**

- [android.text.style.LineBreakConfigSpan](https://developer.android.com/reference/kotlin/android/text/style/LineBreakConfigSpan#) 

### createNoHyphenationSpan

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun createNoHyphenationSpan(): LineBreakConfigSpan
```

A specialized [LineBreakConfigSpan](https://developer.android.com/reference/kotlin/android/text/style/LineBreakConfigSpan#) that used for preventing hyphenation.

| Return ||
|---------------------------------------------------------------------------------------------------------------|-----------------------------|
| [LineBreakConfigSpan](https://developer.android.com/reference/kotlin/android/text/style/LineBreakConfigSpan#) | This value cannot be`null`. |

### describeContents

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### equals

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getLineBreakConfig

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLineBreakConfig(): LineBreakConfig
```

Gets an associated line break config.

| Return ||
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [LineBreakConfig](https://developer.android.com/reference/kotlin/android/graphics/text/LineBreakConfig.html#) | associated line break config. This value cannot be`null`. |

### getSpanTypeId

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSpanTypeId(): Int
```  

### hashCode

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### toString

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<LineBreakConfigSpan!>
```
