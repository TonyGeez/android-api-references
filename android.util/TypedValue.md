# TypedValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TypedValue

Kotlin| [Java](https://developer.android.com/reference/android/util/TypedValue "View this page in Java") 

```
open class TypedValue
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.util.TypedValue](https://developer.android.com/reference/kotlin/android/util/TypedValue#) |

Container for a dynamically typed data value. Primarily used with [android.content.res.Resources](https://developer.android.com/reference/kotlin/android/content/res/Resources.html#) for holding resource values.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [COMPLEX_MANTISSA_MASK](https://developer.android.com/reference/kotlin/android/util/TypedValue#COMPLEX_MANTISSA_MASK:kotlin.Int) Complex data: mask to extract mantissa information (after shifting by [COMPLEX_MANTISSA_SHIFT](https://developer.android.com/reference/kotlin/android/util/TypedValue#COMPLEX_MANTISSA_SHIFT:kotlin.Int)). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [COMPLEX_MANTISSA_SHIFT](https://developer.android.com/reference/kotlin/android/util/TypedValue#COMPLEX_MANTISSA_SHIFT:kotlin.Int) Complex data: bit location of mantissa information. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [COMPLEX_RADIX_0p23](https://developer.android.com/reference/kotlin/android/util/TypedValue#COMPLEX_RADIX_0p23:kotlin.Int) Complex data: the mantissa magnitude is 0 bits -- i. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [COMPLEX_RADIX_16p7](https://developer.android.com/reference/kotlin/android/util/TypedValue#COMPLEX_RADIX_16p7:kotlin.Int) Complex data: the mantissa magnitude is 16 bits -- i. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [COMPLEX_RADIX_23p0](https://developer.android.com/reference/kotlin/android/util/TypedValue#COMPLEX_RADIX_23p0:kotlin.Int) Complex data: the mantissa is an integral number -- i. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [COMPLEX_RADIX_8p15](https://developer.android.com/reference/kotlin/android/util/TypedValue#COMPLEX_RADIX_8p15:kotlin.Int) Complex data: the mantissa magnitude is 8 bits -- i. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [COMPLEX_RADIX_MASK](https://developer.android.com/reference/kotlin/android/util/TypedValue#COMPLEX_RADIX_MASK:kotlin.Int) Complex data: mask to extract radix information (after shifting by [COMPLEX_RADIX_SHIFT](https://developer.android.com/reference/kotlin/android/util/TypedValue#COMPLEX_RADIX_SHIFT:kotlin.Int)). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [COMPLEX_RADIX_SHIFT](https://developer.android.com/reference/kotlin/android/util/TypedValue#COMPLEX_RADIX_SHIFT:kotlin.Int) Complex data: where the radix information is, telling where the decimal place appears in the mantissa. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [COMPLEX_UNIT_DIP](https://developer.android.com/reference/kotlin/android/util/TypedValue#COMPLEX_UNIT_DIP:kotlin.Int) [TYPE_DIMENSION](https://developer.android.com/reference/kotlin/android/util/TypedValue#TYPE_DIMENSION:kotlin.Int) complex unit: Value is Device Independent Pixels. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [COMPLEX_UNIT_FRACTION](https://developer.android.com/reference/kotlin/android/util/TypedValue#COMPLEX_UNIT_FRACTION:kotlin.Int) [TYPE_FRACTION](https://developer.android.com/reference/kotlin/android/util/TypedValue#TYPE_FRACTION:kotlin.Int) complex unit: A basic fraction of the overall size. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [COMPLEX_UNIT_FRACTION_PARENT](https://developer.android.com/reference/kotlin/android/util/TypedValue#COMPLEX_UNIT_FRACTION_PARENT:kotlin.Int) [TYPE_FRACTION](https://developer.android.com/reference/kotlin/android/util/TypedValue#TYPE_FRACTION:kotlin.Int) complex unit: A fraction of the parent size. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [COMPLEX_UNIT_IN](https://developer.android.com/reference/kotlin/android/util/TypedValue#COMPLEX_UNIT_IN:kotlin.Int) [TYPE_DIMENSION](https://developer.android.com/reference/kotlin/android/util/TypedValue#TYPE_DIMENSION:kotlin.Int) complex unit: Value is in inches. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [COMPLEX_UNIT_MASK](https://developer.android.com/reference/kotlin/android/util/TypedValue#COMPLEX_UNIT_MASK:kotlin.Int) Complex data: mask to extract unit information (after shifting by [COMPLEX_UNIT_SHIFT](https://developer.android.com/reference/kotlin/android/util/TypedValue#COMPLEX_UNIT_SHIFT:kotlin.Int)). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [COMPLEX_UNIT_MM](https://developer.android.com/reference/kotlin/android/util/TypedValue#COMPLEX_UNIT_MM:kotlin.Int) [TYPE_DIMENSION](https://developer.android.com/reference/kotlin/android/util/TypedValue#TYPE_DIMENSION:kotlin.Int) complex unit: Value is in millimeters. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [COMPLEX_UNIT_PT](https://developer.android.com/reference/kotlin/android/util/TypedValue#COMPLEX_UNIT_PT:kotlin.Int) [TYPE_DIMENSION](https://developer.android.com/reference/kotlin/android/util/TypedValue#TYPE_DIMENSION:kotlin.Int) complex unit: Value is in points. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [COMPLEX_UNIT_PX](https://developer.android.com/reference/kotlin/android/util/TypedValue#COMPLEX_UNIT_PX:kotlin.Int) [TYPE_DIMENSION](https://developer.android.com/reference/kotlin/android/util/TypedValue#TYPE_DIMENSION:kotlin.Int) complex unit: Value is raw pixels. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [COMPLEX_UNIT_SHIFT](https://developer.android.com/reference/kotlin/android/util/TypedValue#COMPLEX_UNIT_SHIFT:kotlin.Int) Complex data: bit location of unit information. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [COMPLEX_UNIT_SP](https://developer.android.com/reference/kotlin/android/util/TypedValue#COMPLEX_UNIT_SP:kotlin.Int) [TYPE_DIMENSION](https://developer.android.com/reference/kotlin/android/util/TypedValue#TYPE_DIMENSION:kotlin.Int) complex unit: Value is a scaled pixel. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DATA_NULL_EMPTY](https://developer.android.com/reference/kotlin/android/util/TypedValue#DATA_NULL_EMPTY:kotlin.Int) [TYPE_NULL](https://developer.android.com/reference/kotlin/android/util/TypedValue#TYPE_NULL:kotlin.Int) data indicating the value was explicitly set to null. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DATA_NULL_UNDEFINED](https://developer.android.com/reference/kotlin/android/util/TypedValue#DATA_NULL_UNDEFINED:kotlin.Int) [TYPE_NULL](https://developer.android.com/reference/kotlin/android/util/TypedValue#TYPE_NULL:kotlin.Int) data indicating the value was not specified. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DENSITY_DEFAULT](https://developer.android.com/reference/kotlin/android/util/TypedValue#DENSITY_DEFAULT:kotlin.Int) If [density](https://developer.android.com/reference/kotlin/android/util/TypedValue#density:kotlin.Int) is equal to this value, then the density should be treated as the system's default density value: [DisplayMetrics.DENSITY_DEFAULT](https://developer.android.com/reference/kotlin/android/util/DisplayMetrics#DENSITY_DEFAULT:kotlin.Int). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DENSITY_NONE](https://developer.android.com/reference/kotlin/android/util/TypedValue#DENSITY_NONE:kotlin.Int) If [density](https://developer.android.com/reference/kotlin/android/util/TypedValue#density:kotlin.Int) is equal to this value, then there is no density associated with the resource and it should not be scaled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_ATTRIBUTE](https://developer.android.com/reference/kotlin/android/util/TypedValue#TYPE_ATTRIBUTE:kotlin.Int) The data field holds an attribute resource identifier (referencing an attribute in the current theme style, not a resource entry). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_DIMENSION](https://developer.android.com/reference/kotlin/android/util/TypedValue#TYPE_DIMENSION:kotlin.Int) The data field holds a complex number encoding a dimension value. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_FIRST_COLOR_INT](https://developer.android.com/reference/kotlin/android/util/TypedValue#TYPE_FIRST_COLOR_INT:kotlin.Int) Identifies the start of integer values that were specified as color constants (starting with '#'). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_FIRST_INT](https://developer.android.com/reference/kotlin/android/util/TypedValue#TYPE_FIRST_INT:kotlin.Int) Identifies the start of plain integer values. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_FLOAT](https://developer.android.com/reference/kotlin/android/util/TypedValue#TYPE_FLOAT:kotlin.Int) The data field holds an IEEE 754 floating point number. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_FRACTION](https://developer.android.com/reference/kotlin/android/util/TypedValue#TYPE_FRACTION:kotlin.Int) The data field holds a complex number encoding a fraction of a container. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_INT_BOOLEAN](https://developer.android.com/reference/kotlin/android/util/TypedValue#TYPE_INT_BOOLEAN:kotlin.Int) [data](https://developer.android.com/reference/kotlin/android/util/TypedValue#data:kotlin.Int) holds 0 to represent`false`, or a value different from 0 to represent`true`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_INT_COLOR_ARGB4](https://developer.android.com/reference/kotlin/android/util/TypedValue#TYPE_INT_COLOR_ARGB4:kotlin.Int) The data field holds a color that was originally specified as #argb. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_INT_COLOR_ARGB8](https://developer.android.com/reference/kotlin/android/util/TypedValue#TYPE_INT_COLOR_ARGB8:kotlin.Int) The data field holds a color that was originally specified as #aarrggbb. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_INT_COLOR_RGB4](https://developer.android.com/reference/kotlin/android/util/TypedValue#TYPE_INT_COLOR_RGB4:kotlin.Int) The data field holds a color that was originally specified as #rgb. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_INT_COLOR_RGB8](https://developer.android.com/reference/kotlin/android/util/TypedValue#TYPE_INT_COLOR_RGB8:kotlin.Int) The data field holds a color that was originally specified as #rrggbb. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_INT_DEC](https://developer.android.com/reference/kotlin/android/util/TypedValue#TYPE_INT_DEC:kotlin.Int) The data field holds a number that was originally specified in decimal. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_INT_HEX](https://developer.android.com/reference/kotlin/android/util/TypedValue#TYPE_INT_HEX:kotlin.Int) The data field holds a number that was originally specified in hexadecimal (0xn). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_LAST_COLOR_INT](https://developer.android.com/reference/kotlin/android/util/TypedValue#TYPE_LAST_COLOR_INT:kotlin.Int) Identifies the end of integer values that were specified as color constants. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_LAST_INT](https://developer.android.com/reference/kotlin/android/util/TypedValue#TYPE_LAST_INT:kotlin.Int) Identifies the end of plain integer values. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_NULL](https://developer.android.com/reference/kotlin/android/util/TypedValue#TYPE_NULL:kotlin.Int) The value contains no data. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_REFERENCE](https://developer.android.com/reference/kotlin/android/util/TypedValue#TYPE_REFERENCE:kotlin.Int) The data field holds a resource identifier. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_STRING](https://developer.android.com/reference/kotlin/android/util/TypedValue#TYPE_STRING:kotlin.Int) The string field holds string data. |

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------|---|
| [TypedValue](https://developer.android.com/reference/kotlin/android/util/TypedValue#TypedValue())`()` <br /> |

| Public methods ||
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [applyDimension](https://developer.android.com/reference/kotlin/android/util/TypedValue#applyDimension(kotlin.Int,%20kotlin.Float,%20android.util.DisplayMetrics))`(`unit:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `metrics:` ` [DisplayMetrics](https://developer.android.com/reference/kotlin/android/util/DisplayMetrics)!`)` Converts an unpacked complex data value holding a dimension to its final floating point pixel value. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [coerceToString](https://developer.android.com/reference/kotlin/android/util/TypedValue#coerceToString())`()` Regardless of the actual type of the value, try to convert it to a string value. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [coerceToString](https://developer.android.com/reference/kotlin/android/util/TypedValue#coerceToString(kotlin.Int,%20kotlin.Int))`(`type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `data:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Perform type conversion as per [coerceToString()](https://developer.android.com/reference/kotlin/android/util/TypedValue#coerceToString())on an explicitly supplied type and data. |
| openstatic [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [complexToDimension](https://developer.android.com/reference/kotlin/android/util/TypedValue#complexToDimension(kotlin.Int,%20android.util.DisplayMetrics))`(`data:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `metrics:` ` [DisplayMetrics](https://developer.android.com/reference/kotlin/android/util/DisplayMetrics)!`)` Converts a complex data value holding a dimension to its final floating point value. |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [complexToDimensionPixelOffset](https://developer.android.com/reference/kotlin/android/util/TypedValue#complexToDimensionPixelOffset(kotlin.Int,%20android.util.DisplayMetrics))`(`data:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `metrics:` ` [DisplayMetrics](https://developer.android.com/reference/kotlin/android/util/DisplayMetrics)!`)` Converts a complex data value holding a dimension to its final value as an integer pixel offset. |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [complexToDimensionPixelSize](https://developer.android.com/reference/kotlin/android/util/TypedValue#complexToDimensionPixelSize(kotlin.Int,%20android.util.DisplayMetrics))`(`data:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `metrics:` ` [DisplayMetrics](https://developer.android.com/reference/kotlin/android/util/DisplayMetrics)!`)` Converts a complex data value holding a dimension to its final value as an integer pixel size. |
| openstatic [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [complexToFloat](https://developer.android.com/reference/kotlin/android/util/TypedValue#complexToFloat(kotlin.Int))`(`complex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieve the base value from a complex data integer. |
| openstatic [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [complexToFraction](https://developer.android.com/reference/kotlin/android/util/TypedValue#complexToFraction(kotlin.Int,%20kotlin.Float,%20kotlin.Float))`(`data:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `base:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `pbase:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Converts a complex data value holding a fraction to its final floating point value. |
| openstatic [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [convertDimensionToPixels](https://developer.android.com/reference/kotlin/android/util/TypedValue#convertDimensionToPixels(kotlin.Int,%20kotlin.Float,%20android.util.DisplayMetrics))`(`unitToConvertFrom:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `metrics:` ` [DisplayMetrics](https://developer.android.com/reference/kotlin/android/util/DisplayMetrics)`)` Converts a dimension value to raw pixels, e. |
| openstatic [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [convertPixelsToDimension](https://developer.android.com/reference/kotlin/android/util/TypedValue#convertPixelsToDimension(kotlin.Int,%20kotlin.Float,%20android.util.DisplayMetrics))`(`unitToConvertTo:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `pixelValue:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `metrics:` ` [DisplayMetrics](https://developer.android.com/reference/kotlin/android/util/DisplayMetrics)`)` Converts a pixel value to the given dimension, e. |
| openstatic [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [deriveDimension](https://developer.android.com/reference/kotlin/android/util/TypedValue#deriveDimension(kotlin.Int,%20kotlin.Float,%20android.util.DisplayMetrics))`(`unitToConvertTo:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `pixelValue:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `metrics:` ` [DisplayMetrics](https://developer.android.com/reference/kotlin/android/util/DisplayMetrics)`)` Converts a pixel value to the given dimension, e. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getComplexUnit](https://developer.android.com/reference/kotlin/android/util/TypedValue#getComplexUnit())`()` Return the complex unit type for this value. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getDimension](https://developer.android.com/reference/kotlin/android/util/TypedValue#getDimension(android.util.DisplayMetrics))`(`metrics:` ` [DisplayMetrics](https://developer.android.com/reference/kotlin/android/util/DisplayMetrics)!`)` Return the data for this value as a dimension. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getFloat](https://developer.android.com/reference/kotlin/android/util/TypedValue#getFloat())`()` Return the data for this value as a float. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getFraction](https://developer.android.com/reference/kotlin/android/util/TypedValue#getFraction(kotlin.Float,%20kotlin.Float))`(`base:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `pbase:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Return the data for this value as a fraction. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isColorType](https://developer.android.com/reference/kotlin/android/util/TypedValue#isColorType())`()` Determine if a value is a color. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTo](https://developer.android.com/reference/kotlin/android/util/TypedValue#setTo(android.util.TypedValue))`(`other:` ` [TypedValue](https://developer.android.com/reference/kotlin/android/util/TypedValue#)!`)` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/util/TypedValue#toString())`()` <br /> |

| Properties ||
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [assetCookie](https://developer.android.com/reference/kotlin/android/util/TypedValue#assetCookie:kotlin.Int) Additional information about where the value came from; only set for strings. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [changingConfigurations](https://developer.android.com/reference/kotlin/android/util/TypedValue#changingConfigurations:kotlin.Int) If the value came from a resource, these are the configurations for which its contents can change. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [data](https://developer.android.com/reference/kotlin/android/util/TypedValue#data:kotlin.Int) Basic data in the value, interpreted according to [type](https://developer.android.com/reference/kotlin/android/util/TypedValue#type:kotlin.Int) |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [density](https://developer.android.com/reference/kotlin/android/util/TypedValue#density:kotlin.Int) If the Value came from a resource, this holds the corresponding pixel density. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [resourceId](https://developer.android.com/reference/kotlin/android/util/TypedValue#resourceId:kotlin.Int) If Value came from a resource, this holds the corresponding resource id. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [sourceResourceId](https://developer.android.com/reference/kotlin/android/util/TypedValue#sourceResourceId:kotlin.Int) If the Value came from a style resource or a layout resource (set in an XML layout), this holds the corresponding style or layout resource id against which the attribute was resolved. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [string](https://developer.android.com/reference/kotlin/android/util/TypedValue#string:kotlin.CharSequence) If the value holds a string, this is it. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [type](https://developer.android.com/reference/kotlin/android/util/TypedValue#type:kotlin.Int) The type held by this value, as defined by the constants here. |

## Constants

### COMPLEX_MANTISSA_MASK

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COMPLEX_MANTISSA_MASK: Int
```

Complex data: mask to extract mantissa information (after shifting by [COMPLEX_MANTISSA_SHIFT](https://developer.android.com/reference/kotlin/android/util/TypedValue#COMPLEX_MANTISSA_SHIFT:kotlin.Int)). This gives us 23 bits of precision; the top bit is the sign. 

 Value: 16777215

### COMPLEX_MANTISSA_SHIFT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COMPLEX_MANTISSA_SHIFT: Int
```

Complex data: bit location of mantissa information. 

 Value: 8

### COMPLEX_RADIX_0p23

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COMPLEX_RADIX_0p23: Int
```

Complex data: the mantissa magnitude is 0 bits -- i.e, 0x0.nnnnnn 

 Value: 3

### COMPLEX_RADIX_16p7

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COMPLEX_RADIX_16p7: Int
```

Complex data: the mantissa magnitude is 16 bits -- i.e, 0xnnnn.nn 

 Value: 1

### COMPLEX_RADIX_23p0

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COMPLEX_RADIX_23p0: Int
```

Complex data: the mantissa is an integral number -- i.e., 0xnnnnnn.0 

 Value: 0

### COMPLEX_RADIX_8p15

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COMPLEX_RADIX_8p15: Int
```

Complex data: the mantissa magnitude is 8 bits -- i.e, 0xnn.nnnn 

 Value: 2

### COMPLEX_RADIX_MASK

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COMPLEX_RADIX_MASK: Int
```

Complex data: mask to extract radix information (after shifting by [COMPLEX_RADIX_SHIFT](https://developer.android.com/reference/kotlin/android/util/TypedValue#COMPLEX_RADIX_SHIFT:kotlin.Int)). This give us 4 possible fixed point representations as defined below. 

 Value: 3

### COMPLEX_RADIX_SHIFT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COMPLEX_RADIX_SHIFT: Int
```

Complex data: where the radix information is, telling where the decimal place appears in the mantissa. 

 Value: 4

### COMPLEX_UNIT_DIP

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COMPLEX_UNIT_DIP: Int
```

[TYPE_DIMENSION](https://developer.android.com/reference/kotlin/android/util/TypedValue#TYPE_DIMENSION:kotlin.Int) complex unit: Value is Device Independent Pixels. 

 Value: 1

### COMPLEX_UNIT_FRACTION

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COMPLEX_UNIT_FRACTION: Int
```

[TYPE_FRACTION](https://developer.android.com/reference/kotlin/android/util/TypedValue#TYPE_FRACTION:kotlin.Int) complex unit: A basic fraction of the overall size. 

 Value: 0

### COMPLEX_UNIT_FRACTION_PARENT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COMPLEX_UNIT_FRACTION_PARENT: Int
```

[TYPE_FRACTION](https://developer.android.com/reference/kotlin/android/util/TypedValue#TYPE_FRACTION:kotlin.Int) complex unit: A fraction of the parent size. 

 Value: 1

### COMPLEX_UNIT_IN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COMPLEX_UNIT_IN: Int
```

[TYPE_DIMENSION](https://developer.android.com/reference/kotlin/android/util/TypedValue#TYPE_DIMENSION:kotlin.Int) complex unit: Value is in inches. 

 Value: 4

### COMPLEX_UNIT_MASK

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COMPLEX_UNIT_MASK: Int
```

Complex data: mask to extract unit information (after shifting by [COMPLEX_UNIT_SHIFT](https://developer.android.com/reference/kotlin/android/util/TypedValue#COMPLEX_UNIT_SHIFT:kotlin.Int)). This gives us 16 possible types, as defined below. 

 Value: 15

### COMPLEX_UNIT_MM

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COMPLEX_UNIT_MM: Int
```

[TYPE_DIMENSION](https://developer.android.com/reference/kotlin/android/util/TypedValue#TYPE_DIMENSION:kotlin.Int) complex unit: Value is in millimeters. 

 Value: 5

### COMPLEX_UNIT_PT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COMPLEX_UNIT_PT: Int
```

[TYPE_DIMENSION](https://developer.android.com/reference/kotlin/android/util/TypedValue#TYPE_DIMENSION:kotlin.Int) complex unit: Value is in points. 

 Value: 3

### COMPLEX_UNIT_PX

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COMPLEX_UNIT_PX: Int
```

[TYPE_DIMENSION](https://developer.android.com/reference/kotlin/android/util/TypedValue#TYPE_DIMENSION:kotlin.Int) complex unit: Value is raw pixels. 

 Value: 0

### COMPLEX_UNIT_SHIFT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COMPLEX_UNIT_SHIFT: Int
```

Complex data: bit location of unit information. 

 Value: 0

### COMPLEX_UNIT_SP

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COMPLEX_UNIT_SP: Int
```

[TYPE_DIMENSION](https://developer.android.com/reference/kotlin/android/util/TypedValue#TYPE_DIMENSION:kotlin.Int) complex unit: Value is a scaled pixel. 

 Value: 2

### DATA_NULL_EMPTY

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATA_NULL_EMPTY: Int
```

[TYPE_NULL](https://developer.android.com/reference/kotlin/android/util/TypedValue#TYPE_NULL:kotlin.Int) data indicating the value was explicitly set to null. 

 Value: 1

### DATA_NULL_UNDEFINED

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATA_NULL_UNDEFINED: Int
```

[TYPE_NULL](https://developer.android.com/reference/kotlin/android/util/TypedValue#TYPE_NULL:kotlin.Int) data indicating the value was not specified. 

 Value: 0

### DENSITY_DEFAULT

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DENSITY_DEFAULT: Int
```

If [density](https://developer.android.com/reference/kotlin/android/util/TypedValue#density:kotlin.Int) is equal to this value, then the density should be treated as the system's default density value: [DisplayMetrics.DENSITY_DEFAULT](https://developer.android.com/reference/kotlin/android/util/DisplayMetrics#DENSITY_DEFAULT:kotlin.Int). 

 Value: 0

### DENSITY_NONE

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DENSITY_NONE: Int
```

If [density](https://developer.android.com/reference/kotlin/android/util/TypedValue#density:kotlin.Int) is equal to this value, then there is no density associated with the resource and it should not be scaled. 

 Value: 65535

### TYPE_ATTRIBUTE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_ATTRIBUTE: Int
```

The data field holds an attribute resource identifier (referencing an attribute in the current theme style, not a resource entry). 

 Value: 2

### TYPE_DIMENSION

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_DIMENSION: Int
```

The data field holds a complex number encoding a dimension value. 

 Value: 5

### TYPE_FIRST_COLOR_INT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_FIRST_COLOR_INT: Int
```

Identifies the start of integer values that were specified as color constants (starting with '#'). 

 Value: 28

### TYPE_FIRST_INT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_FIRST_INT: Int
```

Identifies the start of plain integer values. Any type value from this to [TYPE_LAST_INT](https://developer.android.com/reference/kotlin/android/util/TypedValue#TYPE_LAST_INT:kotlin.Int) means the data field holds a generic integer value. 

 Value: 16

### TYPE_FLOAT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_FLOAT: Int
```

The data field holds an IEEE 754 floating point number. 

 Value: 4

### TYPE_FRACTION

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_FRACTION: Int
```

The data field holds a complex number encoding a fraction of a container. 

 Value: 6

### TYPE_INT_BOOLEAN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_INT_BOOLEAN: Int
```

[data](https://developer.android.com/reference/kotlin/android/util/TypedValue#data:kotlin.Int) holds 0 to represent`false`, or a value different from 0 to represent`true`. 

 Value: 18

### TYPE_INT_COLOR_ARGB4

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_INT_COLOR_ARGB4: Int
```

The data field holds a color that was originally specified as #argb. 

 Value: 30

### TYPE_INT_COLOR_ARGB8

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_INT_COLOR_ARGB8: Int
```

The data field holds a color that was originally specified as #aarrggbb. 

 Value: 28

### TYPE_INT_COLOR_RGB4

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_INT_COLOR_RGB4: Int
```

The data field holds a color that was originally specified as #rgb. 

 Value: 31

### TYPE_INT_COLOR_RGB8

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_INT_COLOR_RGB8: Int
```

The data field holds a color that was originally specified as #rrggbb. 

 Value: 29

### TYPE_INT_DEC

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_INT_DEC: Int
```

The data field holds a number that was originally specified in decimal. 

 Value: 16

### TYPE_INT_HEX

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_INT_HEX: Int
```

The data field holds a number that was originally specified in hexadecimal (0xn). 

 Value: 17

### TYPE_LAST_COLOR_INT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_LAST_COLOR_INT: Int
```

Identifies the end of integer values that were specified as color constants. 

 Value: 31

### TYPE_LAST_INT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_LAST_INT: Int
```

Identifies the end of plain integer values. 

 Value: 31

### TYPE_NULL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_NULL: Int
```

The value contains no data. 

 Value: 0

### TYPE_REFERENCE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_REFERENCE: Int
```

The data field holds a resource identifier. 

 Value: 1

### TYPE_STRING

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_STRING: Int
```

The string field holds string data. In addition, if data is non-zero then it is the string block index of the string and assetCookie is the set of assets the string came from. 

 Value: 3

## Public constructors

### TypedValue

```
TypedValue()
```

## Public methods

### applyDimension

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun applyDimension(
    unit: Int, 
    value: Float, 
    metrics: DisplayMetrics!
): Float
```

Converts an unpacked complex data value holding a dimension to its final floating point pixel value. The two parameters unit and value are as in [TYPE_DIMENSION](https://developer.android.com/reference/kotlin/android/util/TypedValue#TYPE_DIMENSION:kotlin.Int).

To convert the other way, e.g. from pixels to DP, use [deriveDimension(int,float,android.util.DisplayMetrics)](https://developer.android.com/reference/kotlin/android/util/TypedValue#deriveDimension(kotlin.Int,%20kotlin.Float,%20android.util.DisplayMetrics)).

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `unit` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The unit to convert from. Value is [android.util.TypedValue#COMPLEX_UNIT_PX](https://developer.android.com/reference/kotlin/android/util/TypedValue#COMPLEX_UNIT_PX:kotlin.Int), [android.util.TypedValue#COMPLEX_UNIT_DIP](https://developer.android.com/reference/kotlin/android/util/TypedValue#COMPLEX_UNIT_DIP:kotlin.Int), [android.util.TypedValue#COMPLEX_UNIT_SP](https://developer.android.com/reference/kotlin/android/util/TypedValue#COMPLEX_UNIT_SP:kotlin.Int), [android.util.TypedValue#COMPLEX_UNIT_PT](https://developer.android.com/reference/kotlin/android/util/TypedValue#COMPLEX_UNIT_PT:kotlin.Int), [android.util.TypedValue#COMPLEX_UNIT_IN](https://developer.android.com/reference/kotlin/android/util/TypedValue#COMPLEX_UNIT_IN:kotlin.Int), or [android.util.TypedValue#COMPLEX_UNIT_MM](https://developer.android.com/reference/kotlin/android/util/TypedValue#COMPLEX_UNIT_MM:kotlin.Int) |
| `value` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The value to apply the unit to. |
| `metrics` | [DisplayMetrics](https://developer.android.com/reference/kotlin/android/util/DisplayMetrics)!:Current display metrics to use in the conversion -- supplies display density and scaling information. |

| Return ||
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | The equivalent pixel value---i.e. the complex floating point value multiplied by the appropriate metrics depending on its unit---or zero if unit is not valid. |

### coerceToString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun coerceToString(): CharSequence!
```

Regardless of the actual type of the value, try to convert it to a string value. For example, a color type will be converted to a string of the form #aarrggbb.

| Return ||
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | CharSequence The coerced string value. If the value is null or the type is not known, null is returned. |

### coerceToString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun coerceToString(
    type: Int, 
    data: Int
): String!
```

Perform type conversion as per [coerceToString()](https://developer.android.com/reference/kotlin/android/util/TypedValue#coerceToString())on an explicitly supplied type and data.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------|
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The data type identifier. |
| `data` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The data value. |

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | String The coerced string value. If the value is null or the type is not known, null is returned. |

### complexToDimension

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun complexToDimension(
    data: Int, 
    metrics: DisplayMetrics!
): Float
```

Converts a complex data value holding a dimension to its final floating point value. The given data must be structured as a [TYPE_DIMENSION](https://developer.android.com/reference/kotlin/android/util/TypedValue#TYPE_DIMENSION:kotlin.Int).

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `data` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A complex data value holding a unit, magnitude, and mantissa. |
| `metrics` | [DisplayMetrics](https://developer.android.com/reference/kotlin/android/util/DisplayMetrics)!:Current display metrics to use in the conversion -- supplies display density and scaling information. |

| Return ||
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | The complex floating point value multiplied by the appropriate metrics depending on its unit. |

### complexToDimensionPixelOffset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun complexToDimensionPixelOffset(
    data: Int, 
    metrics: DisplayMetrics!
): Int
```

Converts a complex data value holding a dimension to its final value as an integer pixel offset. This is the same as [complexToDimension](https://developer.android.com/reference/kotlin/android/util/TypedValue#complexToDimension(kotlin.Int,%20android.util.DisplayMetrics)), except the raw floating point value is truncated to an integer (pixel) value. The given data must be structured as a [TYPE_DIMENSION](https://developer.android.com/reference/kotlin/android/util/TypedValue#TYPE_DIMENSION:kotlin.Int).

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `data` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A complex data value holding a unit, magnitude, and mantissa. |
| `metrics` | [DisplayMetrics](https://developer.android.com/reference/kotlin/android/util/DisplayMetrics)!:Current display metrics to use in the conversion -- supplies display density and scaling information. |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The number of pixels specified by the data and its desired multiplier and units. |

### complexToDimensionPixelSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun complexToDimensionPixelSize(
    data: Int, 
    metrics: DisplayMetrics!
): Int
```

Converts a complex data value holding a dimension to its final value as an integer pixel size. This is the same as [complexToDimension](https://developer.android.com/reference/kotlin/android/util/TypedValue#complexToDimension(kotlin.Int,%20android.util.DisplayMetrics)), except the raw floating point value is converted to an integer (pixel) value for use as a size. A size conversion involves rounding the base value, and ensuring that a non-zero base value is at least one pixel in size. The given data must be structured as a [TYPE_DIMENSION](https://developer.android.com/reference/kotlin/android/util/TypedValue#TYPE_DIMENSION:kotlin.Int).

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `data` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A complex data value holding a unit, magnitude, and mantissa. |
| `metrics` | [DisplayMetrics](https://developer.android.com/reference/kotlin/android/util/DisplayMetrics)!:Current display metrics to use in the conversion -- supplies display density and scaling information. |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The number of pixels specified by the data and its desired multiplier and units. |

### complexToFloat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun complexToFloat(complex: Int): Float
```

Retrieve the base value from a complex data integer. This uses the [COMPLEX_MANTISSA_MASK](https://developer.android.com/reference/kotlin/android/util/TypedValue#COMPLEX_MANTISSA_MASK:kotlin.Int) and [COMPLEX_RADIX_MASK](https://developer.android.com/reference/kotlin/android/util/TypedValue#COMPLEX_RADIX_MASK:kotlin.Int) fields of the data to compute a floating point representation of the number they describe. The units are ignored.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------|
| `complex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A complex data value. |

| Return ||
|--------------------------------------------------------------------------------|-----------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | A floating point value corresponding to the complex data. |

### complexToFraction

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun complexToFraction(
    data: Int, 
    base: Float, 
    pbase: Float
): Float
```

Converts a complex data value holding a fraction to its final floating point value. The given data must be structured as a [TYPE_FRACTION](https://developer.android.com/reference/kotlin/android/util/TypedValue#TYPE_FRACTION:kotlin.Int).

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `data` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A complex data value holding a unit, magnitude, and mantissa. |
| `base` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The base value of this fraction. In other words, a standard fraction is multiplied by this value. |
| `pbase` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The parent base value of this fraction. In other words, a parent fraction (nn%p) is multiplied by this value. |

| Return ||
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | The complex floating point value multiplied by the appropriate base value depending on its unit. |

### convertDimensionToPixels

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun convertDimensionToPixels(
    unitToConvertFrom: Int, 
    value: Float, 
    metrics: DisplayMetrics
): Float
```

Converts a dimension value to raw pixels, e.g. DP to PX.

This is just an alias of [applyDimension(int,float,android.util.DisplayMetrics)](https://developer.android.com/reference/kotlin/android/util/TypedValue#applyDimension(kotlin.Int,%20kotlin.Float,%20android.util.DisplayMetrics))with an easier-to-find name.

| Parameters ||
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `unitToConvertFrom` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The unit to convert from. Value is [android.util.TypedValue#COMPLEX_UNIT_PX](https://developer.android.com/reference/kotlin/android/util/TypedValue#COMPLEX_UNIT_PX:kotlin.Int), [android.util.TypedValue#COMPLEX_UNIT_DIP](https://developer.android.com/reference/kotlin/android/util/TypedValue#COMPLEX_UNIT_DIP:kotlin.Int), [android.util.TypedValue#COMPLEX_UNIT_SP](https://developer.android.com/reference/kotlin/android/util/TypedValue#COMPLEX_UNIT_SP:kotlin.Int), [android.util.TypedValue#COMPLEX_UNIT_PT](https://developer.android.com/reference/kotlin/android/util/TypedValue#COMPLEX_UNIT_PT:kotlin.Int), [android.util.TypedValue#COMPLEX_UNIT_IN](https://developer.android.com/reference/kotlin/android/util/TypedValue#COMPLEX_UNIT_IN:kotlin.Int), or [android.util.TypedValue#COMPLEX_UNIT_MM](https://developer.android.com/reference/kotlin/android/util/TypedValue#COMPLEX_UNIT_MM:kotlin.Int) |
| `value` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The dimension value to apply the unit to. |
| `metrics` | [DisplayMetrics](https://developer.android.com/reference/kotlin/android/util/DisplayMetrics):Current display metrics to use in the conversion -- supplies display density and scaling information. This value cannot be`null`. |

| Return ||
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | The equivalent pixel value---i.e. the complex floating point value multiplied by the appropriate metrics depending on its unit---or zero if unit is not valid. |

### convertPixelsToDimension

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun convertPixelsToDimension(
    unitToConvertTo: Int, 
    pixelValue: Float, 
    metrics: DisplayMetrics
): Float
```

Converts a pixel value to the given dimension, e.g. PX to DP.

This is just an alias of [deriveDimension(int,float,android.util.DisplayMetrics)](https://developer.android.com/reference/kotlin/android/util/TypedValue#deriveDimension(kotlin.Int,%20kotlin.Float,%20android.util.DisplayMetrics))with an easier-to-find name.

| Parameters ||
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `unitToConvertTo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The unit to convert to. Value is [android.util.TypedValue#COMPLEX_UNIT_PX](https://developer.android.com/reference/kotlin/android/util/TypedValue#COMPLEX_UNIT_PX:kotlin.Int), [android.util.TypedValue#COMPLEX_UNIT_DIP](https://developer.android.com/reference/kotlin/android/util/TypedValue#COMPLEX_UNIT_DIP:kotlin.Int), [android.util.TypedValue#COMPLEX_UNIT_SP](https://developer.android.com/reference/kotlin/android/util/TypedValue#COMPLEX_UNIT_SP:kotlin.Int), [android.util.TypedValue#COMPLEX_UNIT_PT](https://developer.android.com/reference/kotlin/android/util/TypedValue#COMPLEX_UNIT_PT:kotlin.Int), [android.util.TypedValue#COMPLEX_UNIT_IN](https://developer.android.com/reference/kotlin/android/util/TypedValue#COMPLEX_UNIT_IN:kotlin.Int), or [android.util.TypedValue#COMPLEX_UNIT_MM](https://developer.android.com/reference/kotlin/android/util/TypedValue#COMPLEX_UNIT_MM:kotlin.Int) |
| `pixelValue` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The raw pixels value to convert from. |
| `metrics` | [DisplayMetrics](https://developer.android.com/reference/kotlin/android/util/DisplayMetrics):Current display metrics to use in the conversion -- supplies display density and scaling information. This value cannot be`null`. |

| Return ||
|--------------------------------------------------------------------------------|------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | A dimension value equivalent to the given number of pixels |

| Exceptions ||
|--------------------------------------|----------------------------------|
| `java.lang.IllegalArgumentException` | if unitToConvertTo is not valid. |

### deriveDimension

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun deriveDimension(
    unitToConvertTo: Int, 
    pixelValue: Float, 
    metrics: DisplayMetrics
): Float
```

Converts a pixel value to the given dimension, e.g. PX to DP.

This is the inverse of [applyDimension(int,float,android.util.DisplayMetrics)](https://developer.android.com/reference/kotlin/android/util/TypedValue#applyDimension(kotlin.Int,%20kotlin.Float,%20android.util.DisplayMetrics))

| Parameters ||
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `unitToConvertTo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The unit to convert to. Value is [android.util.TypedValue#COMPLEX_UNIT_PX](https://developer.android.com/reference/kotlin/android/util/TypedValue#COMPLEX_UNIT_PX:kotlin.Int), [android.util.TypedValue#COMPLEX_UNIT_DIP](https://developer.android.com/reference/kotlin/android/util/TypedValue#COMPLEX_UNIT_DIP:kotlin.Int), [android.util.TypedValue#COMPLEX_UNIT_SP](https://developer.android.com/reference/kotlin/android/util/TypedValue#COMPLEX_UNIT_SP:kotlin.Int), [android.util.TypedValue#COMPLEX_UNIT_PT](https://developer.android.com/reference/kotlin/android/util/TypedValue#COMPLEX_UNIT_PT:kotlin.Int), [android.util.TypedValue#COMPLEX_UNIT_IN](https://developer.android.com/reference/kotlin/android/util/TypedValue#COMPLEX_UNIT_IN:kotlin.Int), or [android.util.TypedValue#COMPLEX_UNIT_MM](https://developer.android.com/reference/kotlin/android/util/TypedValue#COMPLEX_UNIT_MM:kotlin.Int) |
| `pixelValue` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The raw pixels value to convert from. |
| `metrics` | [DisplayMetrics](https://developer.android.com/reference/kotlin/android/util/DisplayMetrics):Current display metrics to use in the conversion -- supplies display density and scaling information. This value cannot be`null`. |

| Return ||
|--------------------------------------------------------------------------------|------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | A dimension value equivalent to the given number of pixels |

| Exceptions ||
|--------------------------------------|----------------------------------|
| `java.lang.IllegalArgumentException` | if unitToConvertTo is not valid. |

### getComplexUnit

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getComplexUnit(): Int
```

Return the complex unit type for this value. For example, a dimen type with value 12sp will return [COMPLEX_UNIT_SP](https://developer.android.com/reference/kotlin/android/util/TypedValue#COMPLEX_UNIT_SP:kotlin.Int). Only use for values whose type is [TYPE_DIMENSION](https://developer.android.com/reference/kotlin/android/util/TypedValue#TYPE_DIMENSION:kotlin.Int).

| Return ||
|----------------------------------------------------------------------------|------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The complex unit type. |

### getDimension

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDimension(metrics: DisplayMetrics!): Float
```

Return the data for this value as a dimension. Only use for values whose type is [TYPE_DIMENSION](https://developer.android.com/reference/kotlin/android/util/TypedValue#TYPE_DIMENSION:kotlin.Int).

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `metrics` | [DisplayMetrics](https://developer.android.com/reference/kotlin/android/util/DisplayMetrics)!:Current display metrics to use in the conversion -- supplies display density and scaling information. |

| Return ||
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | The complex floating point value multiplied by the appropriate metrics depending on its unit. |

### getFloat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFloat(): Float
```

Return the data for this value as a float. Only use for values whose type is [TYPE_FLOAT](https://developer.android.com/reference/kotlin/android/util/TypedValue#TYPE_FLOAT:kotlin.Int). 

### getFraction

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFraction(
    base: Float, 
    pbase: Float
): Float
```

Return the data for this value as a fraction. Only use for values whose type is [TYPE_FRACTION](https://developer.android.com/reference/kotlin/android/util/TypedValue#TYPE_FRACTION:kotlin.Int).

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `base` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The base value of this fraction. In other words, a standard fraction is multiplied by this value. |
| `pbase` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The parent base value of this fraction. In other words, a parent fraction (nn%p) is multiplied by this value. |

| Return ||
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | The complex floating point value multiplied by the appropriate base value depending on its unit. |

### isColorType

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isColorType(): Boolean
```

Determine if a value is a color. This works by comparing [type](https://developer.android.com/reference/kotlin/android/util/TypedValue#type:kotlin.Int) to [TYPE_FIRST_COLOR_INT](https://developer.android.com/reference/kotlin/android/util/TypedValue#TYPE_FIRST_COLOR_INT:kotlin.Int) and [TYPE_LAST_COLOR_INT](https://developer.android.com/reference/kotlin/android/util/TypedValue#TYPE_LAST_COLOR_INT:kotlin.Int).

| Return ||
|------------------------------------------------------------------------------------|-------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this value is a color |

### setTo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTo(other: TypedValue!): Unit
```  

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

## Properties

### assetCookie

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var assetCookie: Int
```

Additional information about where the value came from; only set for strings. 

### changingConfigurations

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var changingConfigurations: Int
```

If the value came from a resource, these are the configurations for which its contents can change.

For example, if a resource has a value defined for the -land resource qualifier, this field will have the [android.content.pm.ActivityInfo#CONFIG_ORIENTATION](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_ORIENTATION:kotlin.Int) bit set.

Value is either`0`or a combination of [android.content.pm.ActivityInfo#CONFIG_MCC](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_MCC:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_MNC](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_MNC:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_LOCALE](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_LOCALE:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_TOUCHSCREEN](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_TOUCHSCREEN:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_KEYBOARD](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_KEYBOARD:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_KEYBOARD_HIDDEN](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_KEYBOARD_HIDDEN:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_NAVIGATION](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_NAVIGATION:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_ORIENTATION](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_ORIENTATION:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_SCREEN_LAYOUT](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_SCREEN_LAYOUT:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_UI_MODE](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_UI_MODE:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_SCREEN_SIZE](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_SCREEN_SIZE:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_SMALLEST_SCREEN_SIZE](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_SMALLEST_SCREEN_SIZE:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_DENSITY](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_DENSITY:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_LAYOUT_DIRECTION](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_LAYOUT_DIRECTION:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_COLOR_MODE](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_COLOR_MODE:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_FONT_SCALE](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_FONT_SCALE:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_GRAMMATICAL_GENDER](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_GRAMMATICAL_GENDER:kotlin.Int), [android.content.pm.ActivityInfo#CONFIG_FONT_WEIGHT_ADJUSTMENT](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_FONT_WEIGHT_ADJUSTMENT:kotlin.Int), android.content.pm.ActivityInfo.CONFIG_WINDOW_CONFIGURATION, [android.content.pm.ActivityInfo#CONFIG_ASSETS_PATHS](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_ASSETS_PATHS:kotlin.Int), and [android.content.pm.ActivityInfo#CONFIG_RESOURCES_UNUSED](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_RESOURCES_UNUSED:kotlin.Int) 
**See Also**

- [android.content.pm.ActivityInfo#CONFIG_MCC](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_MCC:kotlin.Int)
- [android.content.pm.ActivityInfo#CONFIG_MNC](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_MNC:kotlin.Int)
- [android.content.pm.ActivityInfo#CONFIG_LOCALE](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_LOCALE:kotlin.Int)
- [android.content.pm.ActivityInfo#CONFIG_TOUCHSCREEN](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_TOUCHSCREEN:kotlin.Int)
- [android.content.pm.ActivityInfo#CONFIG_KEYBOARD](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_KEYBOARD:kotlin.Int)
- [android.content.pm.ActivityInfo#CONFIG_KEYBOARD_HIDDEN](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_KEYBOARD_HIDDEN:kotlin.Int)
- [android.content.pm.ActivityInfo#CONFIG_NAVIGATION](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_NAVIGATION:kotlin.Int)
- [android.content.pm.ActivityInfo#CONFIG_ORIENTATION](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_ORIENTATION:kotlin.Int)
- [android.content.pm.ActivityInfo#CONFIG_SCREEN_LAYOUT](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_SCREEN_LAYOUT:kotlin.Int)
- [android.content.pm.ActivityInfo#CONFIG_UI_MODE](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_UI_MODE:kotlin.Int)
- [android.content.pm.ActivityInfo#CONFIG_SCREEN_SIZE](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_SCREEN_SIZE:kotlin.Int)
- [android.content.pm.ActivityInfo#CONFIG_SMALLEST_SCREEN_SIZE](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_SMALLEST_SCREEN_SIZE:kotlin.Int)
- [android.content.pm.ActivityInfo#CONFIG_DENSITY](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_DENSITY:kotlin.Int)
- [android.content.pm.ActivityInfo#CONFIG_LAYOUT_DIRECTION](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_LAYOUT_DIRECTION:kotlin.Int)
- [android.content.pm.ActivityInfo#CONFIG_COLOR_MODE](https://developer.android.com/reference/kotlin/android/content/pm/ActivityInfo.html#CONFIG_COLOR_MODE:kotlin.Int) 

### data

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var data: Int
```

Basic data in the value, interpreted according to [type](https://developer.android.com/reference/kotlin/android/util/TypedValue#type:kotlin.Int) 

### density

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var density: Int
```

If the Value came from a resource, this holds the corresponding pixel density. 

### resourceId

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var resourceId: Int
```

If Value came from a resource, this holds the corresponding resource id. 

### sourceResourceId

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var sourceResourceId: Int
```

If the Value came from a style resource or a layout resource (set in an XML layout), this holds the corresponding style or layout resource id against which the attribute was resolved. 

### string

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var string: CharSequence!
```

If the value holds a string, this is it. 

### type

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var type: Int
```

The type held by this value, as defined by the constants here. This tells you how to interpret the other fields in the object.
