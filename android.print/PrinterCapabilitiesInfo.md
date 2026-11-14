# PrinterCapabilitiesInfo

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PrinterCapabilitiesInfo

Kotlin| [Java](PrinterCapabilitiesInfo.md) 
| --- | --- |

```
class PrinterCapabilitiesInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.print.PrinterCapabilitiesInfo](PrinterCapabilitiesInfo.md) |

This class represents the capabilities of a printer. Instances of this class are created by a print service to report the capabilities of a printer it manages. The capabilities of a printer specify how it can print content. For example, what are the media sizes supported by the printer, what are the minimal margins of the printer based on its technical design, etc.

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/print/PrinterCapabilitiesInfo.Builder.md) Builder for creating of a [PrinterCapabilitiesInfo](PrinterCapabilitiesInfo.md). |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](PrinterCapabilitiesInfo.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](PrinterCapabilitiesInfo.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getColorModes](PrinterCapabilitiesInfo.md))`()` Gets the bit mask of supported color modes. |
| --- | --- |
| [PrintAttributes](PrintAttributes.md) | [getDefaults](PrinterCapabilitiesInfo.md))`()` Gets the default print attributes. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDuplexModes](PrinterCapabilitiesInfo.md))`()` Gets the bit mask of supported duplex modes. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [PrintAttributes.MediaSize](../android/print/PrintAttributes.MediaSize.md)!\> | [getMediaSizes](PrinterCapabilitiesInfo.md))`()` Gets the supported media sizes. |
| --- | --- |
| [PrintAttributes.Margins](../android/print/PrintAttributes.Margins.md) | [getMinMargins](PrinterCapabilitiesInfo.md))`()` Gets the minimal margins. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [PrintAttributes.Resolution](../android/print/PrintAttributes.Resolution.md)!\> | [getResolutions](PrinterCapabilitiesInfo.md))`()` Gets the supported resolutions. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](PrinterCapabilitiesInfo.md))`()` <br /> |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](PrinterCapabilitiesInfo.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](PrinterCapabilitiesInfo.md))`(`parcel:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [PrinterCapabilitiesInfo](PrinterCapabilitiesInfo.md)!\> | [CREATOR](PrinterCapabilitiesInfo.md) <br /> |

## Public methods

### describeContents

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) |

### equals

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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
|-------|--------------------------|
| `obj` | This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getColorModes

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getColorModes(): Int
```

Gets the bit mask of supported color modes.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The bit mask of supported color modes. Value is either`0`or a combination of [android.print.PrintAttributes#COLOR_MODE_MONOCHROME](PrintAttributes.md), and [android.print.PrintAttributes#COLOR_MODE_COLOR](PrintAttributes.md) |

**See Also**

- [android.print.PrintAttributes#COLOR_MODE_COLOR](PrintAttributes.md)
- [android.print.PrintAttributes#COLOR_MODE_MONOCHROME](PrintAttributes.md) 

### getDefaults

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDefaults(): PrintAttributes
```

Gets the default print attributes.

| Return ||
|-------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| [PrintAttributes](PrintAttributes.md) | The default attributes. This value cannot be`null`. |

### getDuplexModes

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDuplexModes(): Int
```

Gets the bit mask of supported duplex modes.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The bit mask of supported duplex modes. Value is either`0`or a combination of [android.print.PrintAttributes#DUPLEX_MODE_NONE](PrintAttributes.md), [android.print.PrintAttributes#DUPLEX_MODE_LONG_EDGE](PrintAttributes.md), and [android.print.PrintAttributes#DUPLEX_MODE_SHORT_EDGE](PrintAttributes.md) |

**See Also**

- [android.print.PrintAttributes#DUPLEX_MODE_NONE](PrintAttributes.md)
- [android.print.PrintAttributes#DUPLEX_MODE_LONG_EDGE](PrintAttributes.md)
- [android.print.PrintAttributes#DUPLEX_MODE_SHORT_EDGE](PrintAttributes.md) 

### getMediaSizes

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMediaSizes(): MutableList<PrintAttributes.MediaSize!>
```

Gets the supported media sizes.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [PrintAttributes.MediaSize](../android/print/PrintAttributes.MediaSize.md)!> | The media sizes. This value cannot be`null`. |

### getMinMargins

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMinMargins(): PrintAttributes.Margins
```

Gets the minimal margins. These are the minimal margins the printer physically supports.

| Return ||
|-----------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| [PrintAttributes.Margins](../android/print/PrintAttributes.Margins.md) | The minimal margins. This value cannot be`null`. |

### getResolutions

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getResolutions(): MutableList<PrintAttributes.Resolution!>
```

Gets the supported resolutions.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [PrintAttributes.Resolution](../android/print/PrintAttributes.Resolution.md)!> | The resolutions. This value cannot be`null`. |

### hashCode

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### toString

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    parcel: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<PrinterCapabilitiesInfo!>
```
