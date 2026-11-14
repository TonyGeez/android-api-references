# HdrConversionMode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# HdrConversionMode

Kotlin| [Java](HdrConversionMode.md) 
| --- | --- |

```
class HdrConversionMode : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.hardware.display.HdrConversionMode](HdrConversionMode.md) |

Describes the HDR conversion mode for a device. HDR conversion mode has a conversionMode and preferredHdrOutputType.

<br />

The conversionMode can be one of: [HdrConversionMode.HDR_CONVERSION_UNSUPPORTED](HdrConversionMode.md): HDR conversion is unsupported. In this mode, preferredHdrOutputType should not be set. [HdrConversionMode.HDR_CONVERSION_PASSTHROUGH](HdrConversionMode.md): HDR conversion is disabled. The output HDR type will change dynamically to match the content. In this mode, preferredHdrOutputType should not be set. [HdrConversionMode.HDR_CONVERSION_SYSTEM](HdrConversionMode.md): The output HDR type is selected by the implementation. In this mode, preferredHdrOutputType will be the mode preferred by the system when querying. However, it should be set to HDR_TYPE_INVALID when setting the mode. [HdrConversionMode.HDR_CONVERSION_FORCE](HdrConversionMode.md): The implementation converts all content to this HDR type, when possible. In this mode, preferredHdrOutputType should be set.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HDR_CONVERSION_FORCE](HdrConversionMode.md) HDR output conversion is set by the user. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HDR_CONVERSION_PASSTHROUGH](HdrConversionMode.md) HDR output conversion is disabled |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HDR_CONVERSION_SYSTEM](HdrConversionMode.md) HDR output conversion is managed by the device manufacturer's implementation. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HDR_CONVERSION_UNSUPPORTED](HdrConversionMode.md) HDR output conversion is unsupported |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [HdrConversionMode](HdrConversionMode.md))`(`conversionMode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| [HdrConversionMode](HdrConversionMode.md))`(`conversionMode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `preferredHdrOutputType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Public methods ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](HdrConversionMode.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](HdrConversionMode.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getConversionMode](HdrConversionMode.md))`()` <br /> |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPreferredHdrOutputType](HdrConversionMode.md))`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](HdrConversionMode.md))`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](HdrConversionMode.md))`()` <br /> |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](HdrConversionMode.md))`(`dest:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [HdrConversionMode](HdrConversionMode.md)!\> | [CREATOR](HdrConversionMode.md) <br /> |

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
| `conversionMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.hardware.display.HdrConversionMode#HDR_CONVERSION_PASSTHROUGH](HdrConversionMode.md), [android.hardware.display.HdrConversionMode#HDR_CONVERSION_SYSTEM](HdrConversionMode.md), or [android.hardware.display.HdrConversionMode#HDR_CONVERSION_FORCE](HdrConversionMode.md) |

### HdrConversionMode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
HdrConversionMode(
    conversionMode: Int, 
    preferredHdrOutputType: Int)
```

| Parameters ||
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `conversionMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.hardware.display.HdrConversionMode#HDR_CONVERSION_PASSTHROUGH](HdrConversionMode.md), [android.hardware.display.HdrConversionMode#HDR_CONVERSION_SYSTEM](HdrConversionMode.md), or [android.hardware.display.HdrConversionMode#HDR_CONVERSION_FORCE](HdrConversionMode.md) |
| `preferredHdrOutputType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.view.Display.HdrCapabilities#HDR_TYPE_INVALID](../android/view/Display.HdrCapabilities.md), [android.view.Display.HdrCapabilities#HDR_TYPE_DOLBY_VISION](../android/view/Display.HdrCapabilities.md), [android.view.Display.HdrCapabilities#HDR_TYPE_HDR10](../android/view/Display.HdrCapabilities.md), [android.view.Display.HdrCapabilities#HDR_TYPE_HLG](../android/view/Display.HdrCapabilities.md), or [android.view.Display.HdrCapabilities#HDR_TYPE_HDR10_PLUS](../android/view/Display.HdrCapabilities.md) |

## Public methods

### describeContents

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.hardware.display.HdrConversionMode#HDR_CONVERSION_PASSTHROUGH](HdrConversionMode.md), [android.hardware.display.HdrConversionMode#HDR_CONVERSION_SYSTEM](HdrConversionMode.md), or [android.hardware.display.HdrConversionMode#HDR_CONVERSION_FORCE](HdrConversionMode.md) |

### getPreferredHdrOutputType

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPreferredHdrOutputType(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.view.Display.HdrCapabilities#HDR_TYPE_INVALID](../android/view/Display.HdrCapabilities.md), [android.view.Display.HdrCapabilities#HDR_TYPE_DOLBY_VISION](../android/view/Display.HdrCapabilities.md), [android.view.Display.HdrCapabilities#HDR_TYPE_HDR10](../android/view/Display.HdrCapabilities.md), [android.view.Display.HdrCapabilities#HDR_TYPE_HLG](../android/view/Display.HdrCapabilities.md), or [android.view.Display.HdrCapabilities#HDR_TYPE_HDR10_PLUS](../android/view/Display.HdrCapabilities.md) |

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
| `dest` | [Parcel](../android.os/Parcel.md):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<HdrConversionMode!>
```
