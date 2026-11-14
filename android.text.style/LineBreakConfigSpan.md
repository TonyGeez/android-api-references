# LineBreakConfigSpan

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LineBreakConfigSpan

Kotlin| [Java](LineBreakConfigSpan.md) 
| --- | --- |

```
class LineBreakConfigSpan : ParcelableSpan
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.text.style.LineBreakConfigSpan](LineBreakConfigSpan.md) |

LineBreakSpan for changing line break style of the specific region of the text.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [LineBreakConfigSpan](LineBreakConfigSpan.md))`(`lineBreakConfig:` ` [LineBreakConfig](../android.graphics.text/LineBreakConfig.md)`)` Construct a new [LineBreakConfigSpan](LineBreakConfigSpan.md) |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [LineBreakConfigSpan](LineBreakConfigSpan.md) | [createNoBreakSpan](LineBreakConfigSpan.md))`()` A specialized [LineBreakConfigSpan](LineBreakConfigSpan.md) that used for preventing line break. |
| static [LineBreakConfigSpan](LineBreakConfigSpan.md) | [createNoHyphenationSpan](LineBreakConfigSpan.md))`()` A specialized [LineBreakConfigSpan](LineBreakConfigSpan.md) that used for preventing hyphenation. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](LineBreakConfigSpan.md))`()` <br /> |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](LineBreakConfigSpan.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [LineBreakConfig](../android.graphics.text/LineBreakConfig.md) | [getLineBreakConfig](LineBreakConfigSpan.md))`()` Gets an associated line break config. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSpanTypeId](LineBreakConfigSpan.md))`()` <br /> |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](LineBreakConfigSpan.md))`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](LineBreakConfigSpan.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](LineBreakConfigSpan.md))`(`dest:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [LineBreakConfigSpan](LineBreakConfigSpan.md)!\> | [CREATOR](LineBreakConfigSpan.md) <br /> |

## Public constructors

### LineBreakConfigSpan

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
LineBreakConfigSpan(lineBreakConfig: LineBreakConfig)
```

Construct a new [LineBreakConfigSpan](LineBreakConfigSpan.md)

| Parameters ||
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `lineBreakConfig` | [LineBreakConfig](../android.graphics.text/LineBreakConfig.md):a line break config This value cannot be`null`. |

## Public methods

### createNoBreakSpan

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun createNoBreakSpan(): LineBreakConfigSpan
```

A specialized [LineBreakConfigSpan](LineBreakConfigSpan.md) that used for preventing line break. This is useful when you want to preserve some words in the same line. Note that even if this style is specified, the grapheme based line break is still performed for preventing clipping text.

| Return ||
|---------------------------------------------------------------------------------------------------------------|-----------------------------|
| [LineBreakConfigSpan](LineBreakConfigSpan.md) | This value cannot be`null`. |

**See Also**

- [android.text.style.LineBreakConfigSpan](LineBreakConfigSpan.md) 

### createNoHyphenationSpan

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun createNoHyphenationSpan(): LineBreakConfigSpan
```

A specialized [LineBreakConfigSpan](LineBreakConfigSpan.md) that used for preventing hyphenation.

| Return ||
|---------------------------------------------------------------------------------------------------------------|-----------------------------|
| [LineBreakConfigSpan](LineBreakConfigSpan.md) | This value cannot be`null`. |

### describeContents

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) |

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
| [LineBreakConfig](../android.graphics.text/LineBreakConfig.md) | associated line break config. This value cannot be`null`. |

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
| `dest` | [Parcel](../android.os/Parcel.md):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<LineBreakConfigSpan!>
```
