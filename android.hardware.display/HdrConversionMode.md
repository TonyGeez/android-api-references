# HdrConversionMode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# HdrConversionMode

Kotlin| [Java](https://developer.android.com/reference/android/hardware/display/HdrConversionMode "View this page in Java") 
| --- | --- |

```
class HdrConversionMode : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.hardware.display.HdrConversionMode](https://developer.android.com/reference/kotlin/android/hardware/display/HdrConversionMode#) |

Describes the HDR conversion mode for a device. HDR conversion mode has a conversionMode and preferredHdrOutputType.

<br />

The conversionMode can be one of: [HdrConversionMode.HDR_CONVERSION_UNSUPPORTED](https://developer.android.com/reference/kotlin/android/hardware/display/HdrConversionMode#HDR_CONVERSION_UNSUPPORTED:kotlin.Int): HDR conversion is unsupported. In this mode, preferredHdrOutputType should not be set. [HdrConversionMode.HDR_CONVERSION_PASSTHROUGH](https://developer.android.com/reference/kotlin/android/hardware/display/HdrConversionMode#HDR_CONVERSION_PASSTHROUGH:kotlin.Int): HDR conversion is disabled. The output HDR type will change dynamically to match the content. In this mode, preferredHdrOutputType should not be set. [HdrConversionMode.HDR_CONVERSION_SYSTEM](https://developer.android.com/reference/kotlin/android/hardware/display/HdrConversionMode#HDR_CONVERSION_SYSTEM:kotlin.Int): The output HDR type is selected by the implementation. In this mode, preferredHdrOutputType will be the mode preferred by the system when querying. However, it should be set to HDR_TYPE_INVALID when setting the mode. [HdrConversionMode.HDR_CONVERSION_FORCE](https://developer.android.com/reference/kotlin/android/hardware/display/HdrConversionMode#HDR_CONVERSION_FORCE:kotlin.Int): The implementation converts all content to this HDR type, when possible. In this mode, preferredHdrOutputType should be set.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HDR_CONVERSION_FORCE](https://developer.android.com/reference/kotlin/android/hardware/display/HdrConversionMode#HDR_CONVERSION_FORCE:kotlin.Int) HDR output conversion is set by the user. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HDR_CONVERSION_PASSTHROUGH](https://developer.android.com/reference/kotlin/android/hardware/display/HdrConversionMode#HDR_CONVERSION_PASSTHROUGH:kotlin.Int) HDR output conversion is disabled |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HDR_CONVERSION_SYSTEM](https://developer.android.com/reference/kotlin/android/hardware/display/HdrConversionMode#HDR_CONVERSION_SYSTEM:kotlin.Int) HDR output conversion is managed by the device manufacturer's implementation. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HDR_CONVERSION_UNSUPPORTED](https://developer.android.com/reference/kotlin/android/hardware/display/HdrConversionMode#HDR_CONVERSION_UNSUPPORTED:kotlin.Int) HDR output conversion is unsupported |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [HdrConversionMode](https://developer.android.com/reference/kotlin/android/hardware/display/HdrConversionMode#HdrConversionMode(kotlin.Int))`(`conversionMode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| [HdrConversionMode](https://developer.android.com/reference/kotlin/android/hardware/display/HdrConversionMode#HdrConversionMode(kotlin.Int,%20kotlin.Int))`(`conversionMode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `preferredHdrOutputType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Public methods ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/hardware/display/HdrConversionMode#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/hardware/display/HdrConversionMode#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getConversionMode](https://developer.android.com/reference/kotlin/android/hardware/display/HdrConversionMode#getConversionMode())`()` <br /> |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPreferredHdrOutputType](https://developer.android.com/reference/kotlin/android/hardware/display/HdrConversionMode#getPreferredHdrOutputType())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/hardware/display/HdrConversionMode#hashCode())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/hardware/display/HdrConversionMode#toString())`()` <br /> |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/hardware/display/HdrConversionMode#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [HdrConversionMode](https://developer.android.com/reference/kotlin/android/hardware/display/HdrConversionMode#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/hardware/display/HdrConversionMode#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### HDR_CONVERSION_FORCE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HDR_CONVERSION_FORCE: Int
```

HDR output conversion is set by the user. The preferred output type must be set in this case. 

 Value: 3

### HDR_CONVERSION_PASSTHROUGH

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HDR_CONVERSION_PASSTHROUGH: Int
```

HDR output conversion is disabled 

 Value: 1

### HDR_CONVERSION_SYSTEM

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HDR_CONVERSION_SYSTEM: Int
```

HDR output conversion is managed by the device manufacturer's implementation. 

 Value: 2

### HDR_CONVERSION_UNSUPPORTED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HDR_CONVERSION_UNSUPPORTED: Int
```

HDR output conversion is unsupported 

 Value: 0

## Public constructors

### HdrConversionMode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
HdrConversionMode(conversionMode: Int)
```

| Parameters ||
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `conversionMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.hardware.display.HdrConversionMode#HDR_CONVERSION_PASSTHROUGH](https://developer.android.com/reference/kotlin/android/hardware/display/HdrConversionMode#HDR_CONVERSION_PASSTHROUGH:kotlin.Int), [android.hardware.display.HdrConversionMode#HDR_CONVERSION_SYSTEM](https://developer.android.com/reference/kotlin/android/hardware/display/HdrConversionMode#HDR_CONVERSION_SYSTEM:kotlin.Int), or [android.hardware.display.HdrConversionMode#HDR_CONVERSION_FORCE](https://developer.android.com/reference/kotlin/android/hardware/display/HdrConversionMode#HDR_CONVERSION_FORCE:kotlin.Int) |

### HdrConversionMode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
HdrConversionMode(
    conversionMode: Int, 
    preferredHdrOutputType: Int)
```

| Parameters ||
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `conversionMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.hardware.display.HdrConversionMode#HDR_CONVERSION_PASSTHROUGH](https://developer.android.com/reference/kotlin/android/hardware/display/HdrConversionMode#HDR_CONVERSION_PASSTHROUGH:kotlin.Int), [android.hardware.display.HdrConversionMode#HDR_CONVERSION_SYSTEM](https://developer.android.com/reference/kotlin/android/hardware/display/HdrConversionMode#HDR_CONVERSION_SYSTEM:kotlin.Int), or [android.hardware.display.HdrConversionMode#HDR_CONVERSION_FORCE](https://developer.android.com/reference/kotlin/android/hardware/display/HdrConversionMode#HDR_CONVERSION_FORCE:kotlin.Int) |
| `preferredHdrOutputType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.view.Display.HdrCapabilities#HDR_TYPE_INVALID](https://developer.android.com/reference/kotlin/android/view/Display.HdrCapabilities.html#HDR_TYPE_INVALID:kotlin.Int), [android.view.Display.HdrCapabilities#HDR_TYPE_DOLBY_VISION](https://developer.android.com/reference/kotlin/android/view/Display.HdrCapabilities.html#HDR_TYPE_DOLBY_VISION:kotlin.Int), [android.view.Display.HdrCapabilities#HDR_TYPE_HDR10](https://developer.android.com/reference/kotlin/android/view/Display.HdrCapabilities.html#HDR_TYPE_HDR10:kotlin.Int), [android.view.Display.HdrCapabilities#HDR_TYPE_HLG](https://developer.android.com/reference/kotlin/android/view/Display.HdrCapabilities.html#HDR_TYPE_HLG:kotlin.Int), or [android.view.Display.HdrCapabilities#HDR_TYPE_HDR10_PLUS](https://developer.android.com/reference/kotlin/android/view/Display.HdrCapabilities.html#HDR_TYPE_HDR10_PLUS:kotlin.Int) |

## Public methods

### describeContents

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### equals

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The`equals`method implements an equivalence relation on non-null object references:

- It is*reflexive* : for any non-null reference value`x`,`x.equals(x)`should return`true`.
- It is*symmetric* : for any non-null reference values`x`and`y`,`x.equals(y)`should return`true`if and only if`y.equals(x)`returns`true`.
- It is*transitive* : for any non-null reference values`x`,`y`, and`z`, if`x.equals(y)`returns`true`and`y.equals(z)`returns`true`, then`x.equals(z)`should return`true`.
- It is*consistent* : for any non-null reference values`x`and`y`, multiple invocations of`x.equals(y)`consistently return`true`or consistently return`false`, provided no information used in`equals`comparisons on the objects is modified.
- For any non-null reference value`x`,`x.equals(null)`should return`false`.

An equivalence relation partitions the elements it operates on into*equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |
| `o` | This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getConversionMode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getConversionMode(): Int
```

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.hardware.display.HdrConversionMode#HDR_CONVERSION_PASSTHROUGH](https://developer.android.com/reference/kotlin/android/hardware/display/HdrConversionMode#HDR_CONVERSION_PASSTHROUGH:kotlin.Int), [android.hardware.display.HdrConversionMode#HDR_CONVERSION_SYSTEM](https://developer.android.com/reference/kotlin/android/hardware/display/HdrConversionMode#HDR_CONVERSION_SYSTEM:kotlin.Int), or [android.hardware.display.HdrConversionMode#HDR_CONVERSION_FORCE](https://developer.android.com/reference/kotlin/android/hardware/display/HdrConversionMode#HDR_CONVERSION_FORCE:kotlin.Int) |

### getPreferredHdrOutputType

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPreferredHdrOutputType(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.view.Display.HdrCapabilities#HDR_TYPE_INVALID](https://developer.android.com/reference/kotlin/android/view/Display.HdrCapabilities.html#HDR_TYPE_INVALID:kotlin.Int), [android.view.Display.HdrCapabilities#HDR_TYPE_DOLBY_VISION](https://developer.android.com/reference/kotlin/android/view/Display.HdrCapabilities.html#HDR_TYPE_DOLBY_VISION:kotlin.Int), [android.view.Display.HdrCapabilities#HDR_TYPE_HDR10](https://developer.android.com/reference/kotlin/android/view/Display.HdrCapabilities.html#HDR_TYPE_HDR10:kotlin.Int), [android.view.Display.HdrCapabilities#HDR_TYPE_HLG](https://developer.android.com/reference/kotlin/android/view/Display.HdrCapabilities.html#HDR_TYPE_HLG:kotlin.Int), or [android.view.Display.HdrCapabilities#HDR_TYPE_HDR10_PLUS](https://developer.android.com/reference/kotlin/android/view/Display.HdrCapabilities.html#HDR_TYPE_HDR10_PLUS:kotlin.Int) |

### hashCode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### toString

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<HdrConversionMode!>
```
