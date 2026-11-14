# TypedValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TypedValue

Kotlin| [Java](../android/util/TypedValue.md) 
| --- | --- |

```
open class TypedValue
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.util.TypedValue](../android/util/TypedValue.md) |

Container for a dynamically typed data value. Primarily used with [android.content.res.Resources](../android/content/res/Resources.md) for holding resource values.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [COMPLEX_MANTISSA_MASK](../android/util/TypedValue.md) Complex data: mask to extract mantissa information (after shifting by [COMPLEX_MANTISSA_SHIFT](../android/util/TypedValue.md)). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [COMPLEX_MANTISSA_SHIFT](../android/util/TypedValue.md) Complex data: bit location of mantissa information. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [COMPLEX_RADIX_0p23](../android/util/TypedValue.md) Complex data: the mantissa magnitude is 0 bits -- i. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [COMPLEX_RADIX_16p7](../android/util/TypedValue.md) Complex data: the mantissa magnitude is 16 bits -- i. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [COMPLEX_RADIX_23p0](../android/util/TypedValue.md) Complex data: the mantissa is an integral number -- i. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [COMPLEX_RADIX_8p15](../android/util/TypedValue.md) Complex data: the mantissa magnitude is 8 bits -- i. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [COMPLEX_RADIX_MASK](../android/util/TypedValue.md) Complex data: mask to extract radix information (after shifting by [COMPLEX_RADIX_SHIFT](../android/util/TypedValue.md)). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [COMPLEX_RADIX_SHIFT](../android/util/TypedValue.md) Complex data: where the radix information is, telling where the decimal place appears in the mantissa. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [COMPLEX_UNIT_DIP](../android/util/TypedValue.md) [TYPE_DIMENSION](../android/util/TypedValue.md) complex unit: Value is Device Independent Pixels. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [COMPLEX_UNIT_FRACTION](../android/util/TypedValue.md) [TYPE_FRACTION](../android/util/TypedValue.md) complex unit: A basic fraction of the overall size. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [COMPLEX_UNIT_FRACTION_PARENT](../android/util/TypedValue.md) [TYPE_FRACTION](../android/util/TypedValue.md) complex unit: A fraction of the parent size. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [COMPLEX_UNIT_IN](../android/util/TypedValue.md) [TYPE_DIMENSION](../android/util/TypedValue.md) complex unit: Value is in inches. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [COMPLEX_UNIT_MASK](../android/util/TypedValue.md) Complex data: mask to extract unit information (after shifting by [COMPLEX_UNIT_SHIFT](../android/util/TypedValue.md)). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [COMPLEX_UNIT_MM](../android/util/TypedValue.md) [TYPE_DIMENSION](../android/util/TypedValue.md) complex unit: Value is in millimeters. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [COMPLEX_UNIT_PT](../android/util/TypedValue.md) [TYPE_DIMENSION](../android/util/TypedValue.md) complex unit: Value is in points. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [COMPLEX_UNIT_PX](../android/util/TypedValue.md) [TYPE_DIMENSION](../android/util/TypedValue.md) complex unit: Value is raw pixels. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [COMPLEX_UNIT_SHIFT](../android/util/TypedValue.md) Complex data: bit location of unit information. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [COMPLEX_UNIT_SP](../android/util/TypedValue.md) [TYPE_DIMENSION](../android/util/TypedValue.md) complex unit: Value is a scaled pixel. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DATA_NULL_EMPTY](../android/util/TypedValue.md) [TYPE_NULL](../android/util/TypedValue.md) data indicating the value was explicitly set to null. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DATA_NULL_UNDEFINED](../android/util/TypedValue.md) [TYPE_NULL](../android/util/TypedValue.md) data indicating the value was not specified. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DENSITY_DEFAULT](../android/util/TypedValue.md) If [density](../android/util/TypedValue.md) is equal to this value, then the density should be treated as the system's default density value: [DisplayMetrics.DENSITY_DEFAULT](../android/util/DisplayMetrics.md). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DENSITY_NONE](../android/util/TypedValue.md) If [density](../android/util/TypedValue.md) is equal to this value, then there is no density associated with the resource and it should not be scaled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_ATTRIBUTE](../android/util/TypedValue.md) The data field holds an attribute resource identifier (referencing an attribute in the current theme style, not a resource entry). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_DIMENSION](../android/util/TypedValue.md) The data field holds a complex number encoding a dimension value. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_FIRST_COLOR_INT](../android/util/TypedValue.md) Identifies the start of integer values that were specified as color constants (starting with '#'). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_FIRST_INT](../android/util/TypedValue.md) Identifies the start of plain integer values. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_FLOAT](../android/util/TypedValue.md) The data field holds an IEEE 754 floating point number. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_FRACTION](../android/util/TypedValue.md) The data field holds a complex number encoding a fraction of a container. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_INT_BOOLEAN](../android/util/TypedValue.md) [data](../android/util/TypedValue.md) holds 0 to represent`false`, or a value different from 0 to represent`true`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_INT_COLOR_ARGB4](../android/util/TypedValue.md) The data field holds a color that was originally specified as #argb. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_INT_COLOR_ARGB8](../android/util/TypedValue.md) The data field holds a color that was originally specified as #aarrggbb. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_INT_COLOR_RGB4](../android/util/TypedValue.md) The data field holds a color that was originally specified as #rgb. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_INT_COLOR_RGB8](../android/util/TypedValue.md) The data field holds a color that was originally specified as #rrggbb. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_INT_DEC](../android/util/TypedValue.md) The data field holds a number that was originally specified in decimal. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_INT_HEX](../android/util/TypedValue.md) The data field holds a number that was originally specified in hexadecimal (0xn). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_LAST_COLOR_INT](../android/util/TypedValue.md) Identifies the end of integer values that were specified as color constants. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_LAST_INT](../android/util/TypedValue.md) Identifies the end of plain integer values. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_NULL](../android/util/TypedValue.md) The value contains no data. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_REFERENCE](../android/util/TypedValue.md) The data field holds a resource identifier. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_STRING](../android/util/TypedValue.md) The string field holds string data. |

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------|---|
| [TypedValue](../android/util/TypedValue.md))`()` <br /> |

| Public methods ||
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [applyDimension](../android/util/TypedValue.md))`(`unit:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `metrics:` ` [DisplayMetrics](../android/util/DisplayMetrics.md)!`)` Converts an unpacked complex data value holding a dimension to its final floating point pixel value. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [coerceToString](../android/util/TypedValue.md))`()` Regardless of the actual type of the value, try to convert it to a string value. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [coerceToString](../android/util/TypedValue.md))`(`type:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `data:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Perform type conversion as per [coerceToString()](../android/util/TypedValue.md))on an explicitly supplied type and data. |
| --- | --- |
| openstatic [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [complexToDimension](../android/util/TypedValue.md))`(`data:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `metrics:` ` [DisplayMetrics](../android/util/DisplayMetrics.md)!`)` Converts a complex data value holding a dimension to its final floating point value. |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [complexToDimensionPixelOffset](../android/util/TypedValue.md))`(`data:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `metrics:` ` [DisplayMetrics](../android/util/DisplayMetrics.md)!`)` Converts a complex data value holding a dimension to its final value as an integer pixel offset. |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [complexToDimensionPixelSize](../android/util/TypedValue.md))`(`data:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `metrics:` ` [DisplayMetrics](../android/util/DisplayMetrics.md)!`)` Converts a complex data value holding a dimension to its final value as an integer pixel size. |
| --- | --- |
| openstatic [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [complexToFloat](../android/util/TypedValue.md))`(`complex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieve the base value from a complex data integer. |
| openstatic [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [complexToFraction](../android/util/TypedValue.md))`(`data:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `base:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `pbase:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Converts a complex data value holding a fraction to its final floating point value. |
| openstatic [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [convertDimensionToPixels](../android/util/TypedValue.md))`(`unitToConvertFrom:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `metrics:` ` [DisplayMetrics](../android/util/DisplayMetrics.md)`)` Converts a dimension value to raw pixels, e. |
| --- | --- |
| openstatic [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [convertPixelsToDimension](../android/util/TypedValue.md))`(`unitToConvertTo:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `pixelValue:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `metrics:` ` [DisplayMetrics](../android/util/DisplayMetrics.md)`)` Converts a pixel value to the given dimension, e. |
| openstatic [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [deriveDimension](../android/util/TypedValue.md))`(`unitToConvertTo:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `pixelValue:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `metrics:` ` [DisplayMetrics](../android/util/DisplayMetrics.md)`)` Converts a pixel value to the given dimension, e. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getComplexUnit](../android/util/TypedValue.md))`()` Return the complex unit type for this value. |
| --- | --- |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getDimension](../android/util/TypedValue.md))`(`metrics:` ` [DisplayMetrics](../android/util/DisplayMetrics.md)!`)` Return the data for this value as a dimension. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getFloat](../android/util/TypedValue.md))`()` Return the data for this value as a float. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getFraction](../android/util/TypedValue.md))`(`base:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `pbase:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Return the data for this value as a fraction. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isColorType](../android/util/TypedValue.md))`()` Determine if a value is a color. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTo](../android/util/TypedValue.md))`(`other:` ` [TypedValue](../android/util/TypedValue.md)!`)` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/util/TypedValue.md))`()` <br /> |
| --- | --- |

| Properties ||
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [assetCookie](../android/util/TypedValue.md) Additional information about where the value came from; only set for strings. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [changingConfigurations](../android/util/TypedValue.md) If the value came from a resource, these are the configurations for which its contents can change. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [data](../android/util/TypedValue.md) Basic data in the value, interpreted according to [type](../android/util/TypedValue.md) |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [density](../android/util/TypedValue.md) If the Value came from a resource, this holds the corresponding pixel density. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [resourceId](../android/util/TypedValue.md) If Value came from a resource, this holds the corresponding resource id. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [sourceResourceId](../android/util/TypedValue.md) If the Value came from a style resource or a layout resource (set in an XML layout), this holds the corresponding style or layout resource id against which the attribute was resolved. |
| --- | --- |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [string](../android/util/TypedValue.md) If the value holds a string, this is it. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [type](../android/util/TypedValue.md) The type held by this value, as defined by the constants here. |

## Constants

### COMPLEX_MANTISSA_MASK

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COMPLEX_MANTISSA_MASK: Int
```

Complex data: mask to extract mantissa information (after shifting by [COMPLEX_MANTISSA_SHIFT](../android/util/TypedValue.md)). This gives us 23 bits of precision; the top bit is the sign. 

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

Complex data: mask to extract radix information (after shifting by [COMPLEX_RADIX_SHIFT](../android/util/TypedValue.md)). This give us 4 possible fixed point representations as defined below. 

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

[TYPE_DIMENSION](../android/util/TypedValue.md) complex unit: Value is Device Independent Pixels. 

 Value: 1

### COMPLEX_UNIT_FRACTION

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COMPLEX_UNIT_FRACTION: Int
```

[TYPE_FRACTION](../android/util/TypedValue.md) complex unit: A basic fraction of the overall size. 

 Value: 0

### COMPLEX_UNIT_FRACTION_PARENT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COMPLEX_UNIT_FRACTION_PARENT: Int
```

[TYPE_FRACTION](../android/util/TypedValue.md) complex unit: A fraction of the parent size. 

 Value: 1

### COMPLEX_UNIT_IN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COMPLEX_UNIT_IN: Int
```

[TYPE_DIMENSION](../android/util/TypedValue.md) complex unit: Value is in inches. 

 Value: 4

### COMPLEX_UNIT_MASK

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COMPLEX_UNIT_MASK: Int
```

Complex data: mask to extract unit information (after shifting by [COMPLEX_UNIT_SHIFT](../android/util/TypedValue.md)). This gives us 16 possible types, as defined below. 

 Value: 15

### COMPLEX_UNIT_MM

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COMPLEX_UNIT_MM: Int
```

[TYPE_DIMENSION](../android/util/TypedValue.md) complex unit: Value is in millimeters. 

 Value: 5

### COMPLEX_UNIT_PT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COMPLEX_UNIT_PT: Int
```

[TYPE_DIMENSION](../android/util/TypedValue.md) complex unit: Value is in points. 

 Value: 3

### COMPLEX_UNIT_PX

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COMPLEX_UNIT_PX: Int
```

[TYPE_DIMENSION](../android/util/TypedValue.md) complex unit: Value is raw pixels. 

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

[TYPE_DIMENSION](../android/util/TypedValue.md) complex unit: Value is a scaled pixel. 

 Value: 2

### DATA_NULL_EMPTY

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATA_NULL_EMPTY: Int
```

[TYPE_NULL](../android/util/TypedValue.md) data indicating the value was explicitly set to null. 

 Value: 1

### DATA_NULL_UNDEFINED

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATA_NULL_UNDEFINED: Int
```

[TYPE_NULL](../android/util/TypedValue.md) data indicating the value was not specified. 

 Value: 0

### DENSITY_DEFAULT

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DENSITY_DEFAULT: Int
```

If [density](../android/util/TypedValue.md) is equal to this value, then the density should be treated as the system's default density value: [DisplayMetrics.DENSITY_DEFAULT](../android/util/DisplayMetrics.md). 

 Value: 0

### DENSITY_NONE

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DENSITY_NONE: Int
```

If [density](../android/util/TypedValue.md) is equal to this value, then there is no density associated with the resource and it should not be scaled. 

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

Identifies the start of plain integer values. Any type value from this to [TYPE_LAST_INT](../android/util/TypedValue.md) means the data field holds a generic integer value. 

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

[data](../android/util/TypedValue.md) holds 0 to represent`false`, or a value different from 0 to represent`true`. 

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

Converts an unpacked complex data value holding a dimension to its final floating point pixel value. The two parameters unit and value are as in [TYPE_DIMENSION](../android/util/TypedValue.md).

To convert the other way, e.g. from pixels to DP, use [deriveDimension(int,float,android.util.DisplayMetrics)](../android/util/TypedValue.md)).

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `unit` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The unit to convert from. Value is [android.util.TypedValue#COMPLEX_UNIT_PX](../android/util/TypedValue.md), [android.util.TypedValue#COMPLEX_UNIT_DIP](../android/util/TypedValue.md), [android.util.TypedValue#COMPLEX_UNIT_SP](../android/util/TypedValue.md), [android.util.TypedValue#COMPLEX_UNIT_PT](../android/util/TypedValue.md), [android.util.TypedValue#COMPLEX_UNIT_IN](../android/util/TypedValue.md), or [android.util.TypedValue#COMPLEX_UNIT_MM](../android/util/TypedValue.md) |
| `value` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The value to apply the unit to. |
| `metrics` | [DisplayMetrics](../android/util/DisplayMetrics.md)!:Current display metrics to use in the conversion -- supplies display density and scaling information. |
| --- | --- |

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

Perform type conversion as per [coerceToString()](../android/util/TypedValue.md))on an explicitly supplied type and data.

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

Converts a complex data value holding a dimension to its final floating point value. The given data must be structured as a [TYPE_DIMENSION](../android/util/TypedValue.md).

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `data` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A complex data value holding a unit, magnitude, and mantissa. |
| `metrics` | [DisplayMetrics](../android/util/DisplayMetrics.md)!:Current display metrics to use in the conversion -- supplies display density and scaling information. |

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

Converts a complex data value holding a dimension to its final value as an integer pixel offset. This is the same as [complexToDimension](../android/util/TypedValue.md)), except the raw floating point value is truncated to an integer (pixel) value. The given data must be structured as a [TYPE_DIMENSION](../android/util/TypedValue.md).

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `data` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A complex data value holding a unit, magnitude, and mantissa. |
| `metrics` | [DisplayMetrics](../android/util/DisplayMetrics.md)!:Current display metrics to use in the conversion -- supplies display density and scaling information. |

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

Converts a complex data value holding a dimension to its final value as an integer pixel size. This is the same as [complexToDimension](../android/util/TypedValue.md)), except the raw floating point value is converted to an integer (pixel) value for use as a size. A size conversion involves rounding the base value, and ensuring that a non-zero base value is at least one pixel in size. The given data must be structured as a [TYPE_DIMENSION](../android/util/TypedValue.md).

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `data` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A complex data value holding a unit, magnitude, and mantissa. |
| `metrics` | [DisplayMetrics](../android/util/DisplayMetrics.md)!:Current display metrics to use in the conversion -- supplies display density and scaling information. |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The number of pixels specified by the data and its desired multiplier and units. |

### complexToFloat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun complexToFloat(complex: Int): Float
```

Retrieve the base value from a complex data integer. This uses the [COMPLEX_MANTISSA_MASK](../android/util/TypedValue.md) and [COMPLEX_RADIX_MASK](../android/util/TypedValue.md) fields of the data to compute a floating point representation of the number they describe. The units are ignored.

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

Converts a complex data value holding a fraction to its final floating point value. The given data must be structured as a [TYPE_FRACTION](../android/util/TypedValue.md).

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `data` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A complex data value holding a unit, magnitude, and mantissa. |
| `base` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The base value of this fraction. In other words, a standard fraction is multiplied by this value. |
| `pbase` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The parent base value of this fraction. In other words, a parent fraction (nn%p) is multiplied by this value. |
| --- | --- |

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

This is just an alias of [applyDimension(int,float,android.util.DisplayMetrics)](../android/util/TypedValue.md))with an easier-to-find name.

| Parameters ||
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `unitToConvertFrom` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The unit to convert from. Value is [android.util.TypedValue#COMPLEX_UNIT_PX](../android/util/TypedValue.md), [android.util.TypedValue#COMPLEX_UNIT_DIP](../android/util/TypedValue.md), [android.util.TypedValue#COMPLEX_UNIT_SP](../android/util/TypedValue.md), [android.util.TypedValue#COMPLEX_UNIT_PT](../android/util/TypedValue.md), [android.util.TypedValue#COMPLEX_UNIT_IN](../android/util/TypedValue.md), or [android.util.TypedValue#COMPLEX_UNIT_MM](../android/util/TypedValue.md) |
| `value` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The dimension value to apply the unit to. |
| `metrics` | [DisplayMetrics](../android/util/DisplayMetrics.md):Current display metrics to use in the conversion -- supplies display density and scaling information. This value cannot be`null`. |
| --- | --- |

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

This is just an alias of [deriveDimension(int,float,android.util.DisplayMetrics)](../android/util/TypedValue.md))with an easier-to-find name.

| Parameters ||
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `unitToConvertTo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The unit to convert to. Value is [android.util.TypedValue#COMPLEX_UNIT_PX](../android/util/TypedValue.md), [android.util.TypedValue#COMPLEX_UNIT_DIP](../android/util/TypedValue.md), [android.util.TypedValue#COMPLEX_UNIT_SP](../android/util/TypedValue.md), [android.util.TypedValue#COMPLEX_UNIT_PT](../android/util/TypedValue.md), [android.util.TypedValue#COMPLEX_UNIT_IN](../android/util/TypedValue.md), or [android.util.TypedValue#COMPLEX_UNIT_MM](../android/util/TypedValue.md) |
| `pixelValue` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The raw pixels value to convert from. |
| `metrics` | [DisplayMetrics](../android/util/DisplayMetrics.md):Current display metrics to use in the conversion -- supplies display density and scaling information. This value cannot be`null`. |
| --- | --- |

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

This is the inverse of [applyDimension(int,float,android.util.DisplayMetrics)](../android/util/TypedValue.md))

| Parameters ||
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `unitToConvertTo` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The unit to convert to. Value is [android.util.TypedValue#COMPLEX_UNIT_PX](../android/util/TypedValue.md), [android.util.TypedValue#COMPLEX_UNIT_DIP](../android/util/TypedValue.md), [android.util.TypedValue#COMPLEX_UNIT_SP](../android/util/TypedValue.md), [android.util.TypedValue#COMPLEX_UNIT_PT](../android/util/TypedValue.md), [android.util.TypedValue#COMPLEX_UNIT_IN](../android/util/TypedValue.md), or [android.util.TypedValue#COMPLEX_UNIT_MM](../android/util/TypedValue.md) |
| `pixelValue` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The raw pixels value to convert from. |
| `metrics` | [DisplayMetrics](../android/util/DisplayMetrics.md):Current display metrics to use in the conversion -- supplies display density and scaling information. This value cannot be`null`. |
| --- | --- |

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

Return the complex unit type for this value. For example, a dimen type with value 12sp will return [COMPLEX_UNIT_SP](../android/util/TypedValue.md). Only use for values whose type is [TYPE_DIMENSION](../android/util/TypedValue.md).

| Return ||
|----------------------------------------------------------------------------|------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The complex unit type. |

### getDimension

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDimension(metrics: DisplayMetrics!): Float
```

Return the data for this value as a dimension. Only use for values whose type is [TYPE_DIMENSION](../android/util/TypedValue.md).

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `metrics` | [DisplayMetrics](../android/util/DisplayMetrics.md)!:Current display metrics to use in the conversion -- supplies display density and scaling information. |

| Return ||
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | The complex floating point value multiplied by the appropriate metrics depending on its unit. |

### getFloat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFloat(): Float
```

Return the data for this value as a float. Only use for values whose type is [TYPE_FLOAT](../android/util/TypedValue.md). 

### getFraction

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFraction(
    base: Float, 
    pbase: Float
): Float
```

Return the data for this value as a fraction. Only use for values whose type is [TYPE_FRACTION](../android/util/TypedValue.md).

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

Determine if a value is a color. This works by comparing [type](../android/util/TypedValue.md) to [TYPE_FIRST_COLOR_INT](../android/util/TypedValue.md) and [TYPE_LAST_COLOR_INT](../android/util/TypedValue.md).

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

For example, if a resource has a value defined for the -land resource qualifier, this field will have the [android.content.pm.ActivityInfo#CONFIG_ORIENTATION](../android/content/pm/ActivityInfo.md) bit set.

Value is either`0`or a combination of [android.content.pm.ActivityInfo#CONFIG_MCC](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_MNC](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_LOCALE](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_TOUCHSCREEN](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_KEYBOARD](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_KEYBOARD_HIDDEN](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_NAVIGATION](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_ORIENTATION](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_SCREEN_LAYOUT](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_UI_MODE](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_SCREEN_SIZE](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_SMALLEST_SCREEN_SIZE](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_DENSITY](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_LAYOUT_DIRECTION](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_COLOR_MODE](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_FONT_SCALE](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_GRAMMATICAL_GENDER](../android/content/pm/ActivityInfo.md), [android.content.pm.ActivityInfo#CONFIG_FONT_WEIGHT_ADJUSTMENT](../android/content/pm/ActivityInfo.md), android.content.pm.ActivityInfo.CONFIG_WINDOW_CONFIGURATION, [android.content.pm.ActivityInfo#CONFIG_ASSETS_PATHS](../android/content/pm/ActivityInfo.md), and [android.content.pm.ActivityInfo#CONFIG_RESOURCES_UNUSED](../android/content/pm/ActivityInfo.md) 
**See Also**

- [android.content.pm.ActivityInfo#CONFIG_MCC](../android/content/pm/ActivityInfo.md)
- [android.content.pm.ActivityInfo#CONFIG_MNC](../android/content/pm/ActivityInfo.md)
- [android.content.pm.ActivityInfo#CONFIG_LOCALE](../android/content/pm/ActivityInfo.md)
- [android.content.pm.ActivityInfo#CONFIG_TOUCHSCREEN](../android/content/pm/ActivityInfo.md)
- [android.content.pm.ActivityInfo#CONFIG_KEYBOARD](../android/content/pm/ActivityInfo.md)
- [android.content.pm.ActivityInfo#CONFIG_KEYBOARD_HIDDEN](../android/content/pm/ActivityInfo.md)
- [android.content.pm.ActivityInfo#CONFIG_NAVIGATION](../android/content/pm/ActivityInfo.md)
- [android.content.pm.ActivityInfo#CONFIG_ORIENTATION](../android/content/pm/ActivityInfo.md)
- [android.content.pm.ActivityInfo#CONFIG_SCREEN_LAYOUT](../android/content/pm/ActivityInfo.md)
- [android.content.pm.ActivityInfo#CONFIG_UI_MODE](../android/content/pm/ActivityInfo.md)
- [android.content.pm.ActivityInfo#CONFIG_SCREEN_SIZE](../android/content/pm/ActivityInfo.md)
- [android.content.pm.ActivityInfo#CONFIG_SMALLEST_SCREEN_SIZE](../android/content/pm/ActivityInfo.md)
- [android.content.pm.ActivityInfo#CONFIG_DENSITY](../android/content/pm/ActivityInfo.md)
- [android.content.pm.ActivityInfo#CONFIG_LAYOUT_DIRECTION](../android/content/pm/ActivityInfo.md)
- [android.content.pm.ActivityInfo#CONFIG_COLOR_MODE](../android/content/pm/ActivityInfo.md) 

### data

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var data: Int
```

Basic data in the value, interpreted according to [type](../android/util/TypedValue.md) 

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
