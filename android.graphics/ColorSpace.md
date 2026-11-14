Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ColorSpace

Kotlin | [Java](../android/graphics/ColorSpace.md)
| --- | --- |

```
abstract class ColorSpace
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.ColorSpace](../android/graphics/ColorSpace.md) |

| Known Direct Subclasses [ColorSpace.Rgb](../android/graphics/ColorSpace.Rgb.md) |---|---| | [ColorSpace.Rgb](../android/graphics/ColorSpace.Rgb.md) | An RGB color space is an additive color space using the `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Model` color model (a color is therefore represented by a tuple of 3 numbers). | |
| --- | --- | --- | --- | --- | --- | --- |

A `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#` is used to identify a specific organization of colors. Each color space is characterized by a `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Model` that defines how a color value is represented (for instance the `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Model` color model defines a color value as a triplet of numbers).

Each component of a color must fall within a valid range, specific to each color space, defined by `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#getMinValue(kotlin.Int)` and `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#getMaxValue(kotlin.Int)` This range is commonly \\(\[0..1\]\\). While it is recommended to use values in the valid range, a color space always clamps input and output values when performing operations such as converting to a different color space.

### Using color spaces

This implementation provides a pre-defined set of common color spaces described in the `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named` enum. To obtain an instance of one of the pre-defined color spaces, simply invoke `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#get(android.graphics.ColorSpace.Named)`:

```kotlin
ColorSpace sRgb = ColorSpace.get(ColorSpace.Named.SRGB);
  
```

The `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#get(android.graphics.ColorSpace.Named)` method always returns the same instance for a given name. Color spaces with an `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Model` color model can be safely cast to `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Rgb`. Doing so gives you access to more APIs to query various properties of RGB color models: color gamut primaries, transfer functions, conversions to and from linear space, etc. Please refer to `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Rgb` for more information.

The documentation of `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named` provides a detailed description of the various characteristics of each available color space.

### Color space conversions

To allow conversion between color spaces, this implementation uses the CIE XYZ profile connection space (PCS). Color values can be converted to and from this PCS using `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#toXyz(kotlin.FloatArray)` and `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#fromXyz(kotlin.FloatArray)`.

For color space with a non-RGB color model, the white point of the PCS *must be* the CIE standard illuminant D50. RGB color spaces use their native white point (D65 for `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named` for instance and must undergo `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Adaptation` as necessary.

Since the white point of the PCS is not defined for RGB color space, it is highly recommended to use the variants of the `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#connect(android.graphics.ColorSpace,%20android.graphics.ColorSpace)` method to perform conversions between color spaces. A color space can be manually adapted to a specific white point using `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#adapt(android.graphics.ColorSpace,%20kotlin.FloatArray)`. Please refer to the documentation of `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Rgb` for more information. Several common CIE standard illuminants are provided in this class as reference (see `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#ILLUMINANT_D65:kotlin.FloatArray` or `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#ILLUMINANT_D50:kotlin.FloatArray` for instance).

Here is an example of how to convert from a color space to another:

```kotlin
// Convert from DCI-P3 to Rec.2020
  ColorSpace.Connector connector = ColorSpace.connect(
          ColorSpace.get(ColorSpace.Named.DCI_P3),
          ColorSpace.get(ColorSpace.Named.BT2020));
 
  float[] bt2020 = connector.transform(p3r, p3g, p3b);
  
```

You can easily convert to `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named` by omitting the second parameter:

```kotlin
// Convert from DCI-P3 to sRGB
  ColorSpace.Connector connector = ColorSpace.connect(ColorSpace.get(ColorSpace.Named.DCI_P3));
 
  float[] sRGB = connector.transform(p3r, p3g, p3b);
  
```

Conversions also work between color spaces with different color models:

```kotlin
// Convert from CIE L*a*b* (color model Lab) to Rec.709 (color model RGB)
  ColorSpace.Connector connector = ColorSpace.connect(
          ColorSpace.get(ColorSpace.Named.CIE_LAB),
          ColorSpace.get(ColorSpace.Named.BT709));
  
```

### Color spaces and multi-threading

Color spaces and other related classes (`https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Connector` for instance) are immutable and stateless. They can be safely used from multiple concurrent threads.

Public static methods provided by this class, such as `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#get(android.graphics.ColorSpace.Named)` and `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#connect(android.graphics.ColorSpace,%20android.graphics.ColorSpace)`, are also guaranteed to be thread-safe.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Adaptation` List of adaptation matrices that can be used for chromatic adaptation using the von Kries transform. |
| open | `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Connector` A connector transforms colors from a source color space to a destination color space. |
| | `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Model` A color model is required by a `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#` to describe the way colors can be represented as tuples of numbers. |
| --- | --- |
| | `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named` List of common, named color spaces. |
| | `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.RenderIntent` A render intent determines how a `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Connector` maps colors from one color space to another. |
| open | `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Rgb` An RGB color space is an additive color space using the `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Model` color model (a color is therefore represented by a tuple of 3 numbers). |
| --- | --- |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#MAX_ID:kotlin.Int` The maximum ID value a color space can have. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#MIN_ID:kotlin.Int` The minimum ID value a color space can have. |

| Public methods ||
|---|---|
| open static [ColorSpace](../android/graphics/ColorSpace.md) | `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#adapt(android.graphics.ColorSpace,%20kotlin.FloatArray)(colorSpace: https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#, whitePoint: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)` Performs the chromatic adaptation of a color space from its native white point to the specified white point. |
| open static [ColorSpace](../android/graphics/ColorSpace.md) | `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#adapt(android.graphics.ColorSpace,%20kotlin.FloatArray,%20android.graphics.ColorSpace.Adaptation)(colorSpace: https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#, whitePoint: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html, adaptation: https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Adaptation)` Performs the chromatic adaptation of a color space from its native white point to the specified white point. |
| open static [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#cctToXyz(kotlin.Int)(cct: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Computes the chromaticity coordinates of a specified correlated color temperature (CCT) on the Planckian locus. |
| --- | --- |
| open static [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#chromaticAdaptation(android.graphics.ColorSpace.Adaptation,%20kotlin.FloatArray,%20kotlin.FloatArray)(adaptation: https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Adaptation, srcWhitePoint: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html, dstWhitePoint: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)` Computes the chromatic adaptation transform from the specified source white point to the specified destination white point. |
| open static [ColorSpace.Connector](../android/graphics/ColorSpace.Connector.md) | `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#connect(android.graphics.ColorSpace)(source: https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#)` Connects the specified color spaces to sRGB. |
| open static [ColorSpace.Connector](../android/graphics/ColorSpace.Connector.md) | `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#connect(android.graphics.ColorSpace,%20android.graphics.ColorSpace)(source: https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#, destination: https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#)` Connects two color spaces to allow conversion from the source color space to the destination color space. |
| --- | --- |
| open static [ColorSpace.Connector](../android/graphics/ColorSpace.Connector.md) | `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#connect(android.graphics.ColorSpace,%20android.graphics.ColorSpace,%20android.graphics.ColorSpace.RenderIntent)(source: https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#, destination: https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#, intent: https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.RenderIntent)` Connects two color spaces to allow conversion from the source color space to the destination color space. |
| open static [ColorSpace.Connector](../android/graphics/ColorSpace.Connector.md) | `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#connect(android.graphics.ColorSpace,%20android.graphics.ColorSpace.RenderIntent)(source: https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#, intent: https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.RenderIntent)` Connects the specified color spaces to sRGB. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| --- | --- |
| open [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#fromXyz(kotlin.Float,%20kotlin.Float,%20kotlin.Float)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, y: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, z: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Converts tristimulus values from the CIE XYZ space to this color space's color model. |
| abstract [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#fromXyz(kotlin.FloatArray)(v: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)` Converts tristimulus values from the CIE XYZ space to this color space's color model. |
| open static [ColorSpace](../android/graphics/ColorSpace.md) | `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#get(android.graphics.ColorSpace.Named)(name: https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named)` Returns an instance of `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#` identified by the specified name. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#getComponentCount()()` Returns the number of components that form a color value according to this color space's color model. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#getDataSpace()()` Retrieve the `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#` value from a `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#` object. |
| open static [ColorSpace](../android/graphics/ColorSpace.md)? | `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#getFromDataSpace(kotlin.Int)(dataSpace: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Create a `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#` object using a `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#` value. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#getId()()` Returns the ID of this color space. |
| abstract [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#getMaxValue(kotlin.Int)(component: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the maximum valid value for the specified component of this color space's color model. |
| abstract [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#getMinValue(kotlin.Int)(component: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the minimum valid value for the specified component of this color space's color model. |
| --- | --- |
| open [ColorSpace.Model](../android/graphics/ColorSpace.Model.md) | `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#getModel()()` Return the color model of this color space. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#getName()()` Returns the name of this color space. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#hashCode()()` Returns a hash code value for the object. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#isSrgb()()` Indicates whether this color space is the sRGB color space or equivalent to the sRGB color space. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#isWideGamut()()` Returns whether this color space is a wide-gamut color space. |
| open static [ColorSpace](../android/graphics/ColorSpace.md)? | `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#match(kotlin.FloatArray,%20android.graphics.ColorSpace.Rgb.TransferParameters)(toXYZD50: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html, function: https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Rgb.TransferParameters)` Returns a `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named` instance of `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#` that matches the specified RGB to CIE XYZ transform and transfer functions. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#toString()()` Returns a string representation of the object. |
| open [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#toXyz(kotlin.Float,%20kotlin.Float,%20kotlin.Float)(r: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, g: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Converts a color value from this color space's model to tristimulus CIE XYZ values. |
| abstract [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#toXyz(kotlin.FloatArray)(v: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)` Converts a color value from this color space's model to tristimulus CIE XYZ values. |
| --- | --- |

| Properties ||
|---|---|
| static [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)! | `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#ILLUMINANT_A:kotlin.FloatArray` Standard CIE 1931 2° illuminant A, encoded in xyY. |
| static [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)! | `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#ILLUMINANT_B:kotlin.FloatArray` Standard CIE 1931 2° illuminant B, encoded in xyY. |
| static [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)! | `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#ILLUMINANT_C:kotlin.FloatArray` Standard CIE 1931 2° illuminant C, encoded in xyY. |
| --- | --- |
| static [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)! | `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#ILLUMINANT_D50:kotlin.FloatArray` Standard CIE 1931 2° illuminant D50, encoded in xyY. |
| static [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)! | `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#ILLUMINANT_D55:kotlin.FloatArray` Standard CIE 1931 2° illuminant D55, encoded in xyY. |
| static [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)! | `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#ILLUMINANT_D60:kotlin.FloatArray` Standard CIE 1931 2° illuminant D60, encoded in xyY. |
| --- | --- |
| static [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)! | `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#ILLUMINANT_D65:kotlin.FloatArray` Standard CIE 1931 2° illuminant D65, encoded in xyY. |
| static [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)! | `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#ILLUMINANT_D75:kotlin.FloatArray` Standard CIE 1931 2° illuminant D75, encoded in xyY. |
| static [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)! | `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#ILLUMINANT_E:kotlin.FloatArray` Standard CIE 1931 2° illuminant E, encoded in xyY. |
| --- | --- |

## Constants

### MAX_ID

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MAX_ID: Int
```

The maximum ID value a color space can have.

 Value: 63

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#getId()`

### MIN_ID

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MIN_ID: Int
```

The minimum ID value a color space can have.

 Value: -1

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#getId()`

## Public methods

### adapt

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun adapt(
    colorSpace: ColorSpace, 
    whitePoint: FloatArray
): ColorSpace
```

Performs the chromatic adaptation of a color space from its native white point to the specified white point.

The chromatic adaptation is performed using the `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Adaptation` matrix.

The color space returned by this method always has an ID of `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#MIN_ID:kotlin.Int`.

| Parameters ||
|---|---|
| `colorSpace` | [ColorSpace](../android/graphics/ColorSpace.md): The color space to chromatically adapt. This value cannot be `null`. |
| `whitePoint` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html): The new white point. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#` | A `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#` instance with the same name, primaries, transfer functions and range as the specified color space. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Adaptation`
- `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#adapt(android.graphics.ColorSpace,%20kotlin.FloatArray,%20android.graphics.ColorSpace.Adaptation)`

### adapt

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun adapt(
    colorSpace: ColorSpace, 
    whitePoint: FloatArray, 
    adaptation: ColorSpace.Adaptation
): ColorSpace
```

Performs the chromatic adaptation of a color space from its native white point to the specified white point. If the specified color space does not have an `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Model` color model, or if the color space already has the target white point, the color space is returned unmodified.

The chromatic adaptation is performed using the von Kries method described in the documentation of `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Adaptation`.

The color space returned by this method always has an ID of `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#MIN_ID:kotlin.Int`.

| Parameters ||
|---|---|
| `colorSpace` | [ColorSpace](../android/graphics/ColorSpace.md): The color space to chromatically adapt. This value cannot be `null`. |
| `whitePoint` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html): The new white point. This value cannot be `null`. |
| `adaptation` | [ColorSpace.Adaptation](../android/graphics/ColorSpace.Adaptation.md): The adaptation matrix. This value cannot be `null`. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#` | A new color space if the specified color space has an RGB model and a white point different from the specified white point; the specified color space otherwise. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Adaptation`
- `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#adapt(android.graphics.ColorSpace,%20kotlin.FloatArray)`

### cctToXyz

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun cctToXyz(cct: Int): FloatArray
```

Computes the chromaticity coordinates of a specified correlated color temperature (CCT) on the Planckian locus. The specified CCT must be greater than 0. A meaningful CCT range is \[1667, 25000\].

The transform is computed using the methods in Kang et al., *Design of Advanced Color - Temperature Control System for HDTV Applications*, Journal of Korean Physical Society 41, 865-871 (2002).

| Parameters ||
|---|---|
| `cct` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The correlated color temperature, in Kelvin. Value is 1 or greater |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html` | Corresponding XYZ values. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If cct is invalid |

### chromaticAdaptation

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun chromaticAdaptation(
    adaptation: ColorSpace.Adaptation, 
    srcWhitePoint: FloatArray, 
    dstWhitePoint: FloatArray
): FloatArray
```

Computes the chromatic adaptation transform from the specified source white point to the specified destination white point.

The transform is computed using the von Kries method, described in more details in the documentation of `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Adaptation`. The `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Adaptation` enum provides different matrices that can be used to perform the adaptation.

| Parameters ||
|---|---|
| `adaptation` | [ColorSpace.Adaptation](../android/graphics/ColorSpace.Adaptation.md): The adaptation method. This value cannot be `null`. |
| `srcWhitePoint` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html): The white point to adapt from. This value cannot be `null`. |
| `dstWhitePoint` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html): The white point to adapt to. This value cannot be `null`. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html` | A 3x3 matrix as a non-null array of 9 floats |

### connect

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun connect(source: ColorSpace): ColorSpace.Connector
```

Connects the specified color spaces to sRGB. If the source color space does not use CIE XYZ D65 as its profile connection space, the two spaces are chromatically adapted to use the CIE standard illuminant `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#ILLUMINANT_D50:kotlin.FloatArray` as needed.

If the source is the sRGB color space, an optimized connector is returned to avoid unnecessary computations and loss of precision.

Colors are mapped from the source color space to the destination color space using the `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.RenderIntent` render intent.

| Parameters ||
|---|---|
| `source` | [ColorSpace](../android/graphics/ColorSpace.md): The color space to convert colors from. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Connector` | A non-null connector between the specified color space and sRGB |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#connect(android.graphics.ColorSpace,%20android.graphics.ColorSpace.RenderIntent)`
- `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#connect(android.graphics.ColorSpace,%20android.graphics.ColorSpace)`
- `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#connect(android.graphics.ColorSpace,%20android.graphics.ColorSpace,%20android.graphics.ColorSpace.RenderIntent)`

### connect

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun connect(
    source: ColorSpace, 
    destination: ColorSpace
): ColorSpace.Connector
```

Connects two color spaces to allow conversion from the source color space to the destination color space. If the source and destination color spaces do not have the same profile connection space (CIE XYZ with the same white point), they are chromatically adapted to use the CIE standard illuminant `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#ILLUMINANT_D50:kotlin.FloatArray` as needed.

If the source and destination are the same, an optimized connector is returned to avoid unnecessary computations and loss of precision.

Colors are mapped from the source color space to the destination color space using the `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.RenderIntent` render intent.

| Parameters ||
|---|---|
| `source` | [ColorSpace](../android/graphics/ColorSpace.md): The color space to convert colors from. This value cannot be `null`. |
| `destination` | [ColorSpace](../android/graphics/ColorSpace.md): The color space to convert colors to. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Connector` | A non-null connector between the two specified color spaces |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#connect(android.graphics.ColorSpace)`
- `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#connect(android.graphics.ColorSpace,%20android.graphics.ColorSpace.RenderIntent)`
- `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#connect(android.graphics.ColorSpace,%20android.graphics.ColorSpace,%20android.graphics.ColorSpace.RenderIntent)`

### connect

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun connect(
    source: ColorSpace, 
    destination: ColorSpace, 
    intent: ColorSpace.RenderIntent
): ColorSpace.Connector
```

Connects two color spaces to allow conversion from the source color space to the destination color space. If the source and destination color spaces do not have the same profile connection space (CIE XYZ with the same white point), they are chromatically adapted to use the CIE standard illuminant `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#ILLUMINANT_D50:kotlin.FloatArray` as needed.

If the source and destination are the same, an optimized connector is returned to avoid unnecessary computations and loss of precision.

| Parameters ||
|---|---|
| `source` | [ColorSpace](../android/graphics/ColorSpace.md): The color space to convert colors from. This value cannot be `null`. |
| `destination` | [ColorSpace](../android/graphics/ColorSpace.md): The color space to convert colors to. This value cannot be `null`. |
| `intent` | [ColorSpace.RenderIntent](../android/graphics/ColorSpace.RenderIntent.md): The render intent to map colors from the source to the destination. This value cannot be `null`. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Connector` | A non-null connector between the two specified color spaces |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#connect(android.graphics.ColorSpace)`
- `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#connect(android.graphics.ColorSpace,%20android.graphics.ColorSpace.RenderIntent)`
- `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#connect(android.graphics.ColorSpace,%20android.graphics.ColorSpace)`

### connect

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun connect(
    source: ColorSpace, 
    intent: ColorSpace.RenderIntent
): ColorSpace.Connector
```

Connects the specified color spaces to sRGB. If the source color space does not use CIE XYZ D65 as its profile connection space, the two spaces are chromatically adapted to use the CIE standard illuminant `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#ILLUMINANT_D50:kotlin.FloatArray` as needed.

If the source is the sRGB color space, an optimized connector is returned to avoid unnecessary computations and loss of precision.

| Parameters ||
|---|---|
| `source` | [ColorSpace](../android/graphics/ColorSpace.md): The color space to convert colors from. This value cannot be `null`. |
| `intent` | [ColorSpace.RenderIntent](../android/graphics/ColorSpace.RenderIntent.md): The render intent to map colors from the source to the destination. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Connector` | A non-null connector between the specified color space and sRGB |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#connect(android.graphics.ColorSpace)`
- `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#connect(android.graphics.ColorSpace,%20android.graphics.ColorSpace)`
- `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#connect(android.graphics.ColorSpace,%20android.graphics.ColorSpace,%20android.graphics.ColorSpace.RenderIntent)`

### equals

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The `equals` method implements an equivalence relation on non-null object references:

- It is *reflexive* : for any non-null reference value `x`, `x.equals(x)` should return `true`.
- It is *symmetric* : for any non-null reference values `x` and `y`, `x.equals(y)` should return `true` if and only if `y.equals(x)` returns `true`.
- It is *transitive* : for any non-null reference values `x`, `y`, and `z`, if `x.equals(y)` returns `true` and `y.equals(z)` returns `true`, then `x.equals(z)` should return `true`.
- It is *consistent* : for any non-null reference values `x` and `y`, multiple invocations of `x.equals(y)` consistently return `true` or consistently return `false`, provided no information used in `equals` comparisons on the objects is modified.
- For any non-null reference value `x`, `x.equals(null)` should return `false`.

An equivalence relation partitions the elements it operates on into *equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

### fromXyz

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun fromXyz(
    x: Float, 
    y: Float, 
    z: Float
): FloatArray
```

Converts tristimulus values from the CIE XYZ space to this color space's color model.

| Parameters ||
|---|---|
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The X component of the color value |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The Y component of the color value |
| `z` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The Z component of the color value |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html` | A new array whose size is equal to the number of color components as returned by `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Model#getComponentCount()` This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#fromXyz(kotlin.FloatArray)`
- `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#toXyz(kotlin.Float,%20kotlin.Float,%20kotlin.Float)`

### fromXyz

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun fromXyz(v: FloatArray): FloatArray
```

Converts tristimulus values from the CIE XYZ space to this color space's color model. The resulting value is passed back in the specified array.

The specified array's length must be at least equal to to the number of color components as returned by `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Model#getComponentCount()`, and its first 3 values must be the XYZ components to convert from.

| Parameters ||
|---|---|
| `v` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html): An array of color components containing the XYZ values to convert from, and large enough to hold the number of components of this color space's model. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html` | The array passed in parameter. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#fromXyz(kotlin.Float,%20kotlin.Float,%20kotlin.Float)`
- `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#toXyz(kotlin.FloatArray)`

### get

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun get(name: ColorSpace.Named): ColorSpace
```

Returns an instance of `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#` identified by the specified name. The list of names provided in the `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named` enum gives access to a variety of common RGB color spaces.

This method always returns the same instance for a given name.

This method is thread-safe.
Note that in the Android W release and later, this can return the SRGB ColorSpace if the `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named` parameter is not enabled in the corresponding release.

| Parameters ||
|---|---|
| `name` | [ColorSpace.Named](../android/graphics/ColorSpace.Named.md): The name of the color space to get an instance of. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#` | A non-null `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#` instance. If the ColorSpace is not supported then the SRGB ColorSpace is returned. |

### getComponentCount

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getComponentCount(): Int
```

Returns the number of components that form a color value according to this color space's color model.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | An integer between 1 and 4. Value is between 1 and 4 inclusive |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Model`
- `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#getModel()`

### getDataSpace

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDataSpace(): Int
```

Retrieve the `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#` value from a `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#` object.

If this `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#` object has no matching `dataSpace` value, `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_UNKNOWN:kotlin.Int` will return.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the dataspace value. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_SCRGB_LINEAR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_SRGB:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_SCRGB:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_DISPLAY_P3:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_BT2020_HLG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_BT2020_PQ:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_ADOBE_RGB:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_JFIF:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_BT601_625:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_BT601_525:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_BT2020:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_BT709:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_DCI_P3:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_SRGB_LINEAR:kotlin.Int` |

### getFromDataSpace

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getFromDataSpace(dataSpace: Int): ColorSpace?
```

Create a `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#` object using a `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#` value.

This function maps from a dataspace to a `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named` ColorSpace. If no `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named` ColorSpace object matching the `dataSpace` value can be created, `null` will return.

| Parameters ||
|---|---|
| `dataSpace` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The dataspace value. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_SCRGB_LINEAR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_SRGB:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_SCRGB:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_DISPLAY_P3:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_BT2020_HLG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_BT2020_PQ:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_ADOBE_RGB:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_JFIF:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_BT601_625:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_BT601_525:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_BT2020:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_BT709:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_DCI_P3:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace.html#DATASPACE_SRGB_LINEAR:kotlin.Int` |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#?` | the ColorSpace object or `null` if no matching colorspace can be found. |

### getId

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getId(): Int
```

Returns the ID of this color space. Positive IDs match the color spaces enumerated in `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named`. A negative ID indicates a color space created by calling one of the public constructors.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | An integer between `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#MIN_ID:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#MAX_ID:kotlin.Int` Value is between `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#MIN_ID:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#MAX_ID:kotlin.Int` inclusive |

### getMaxValue

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getMaxValue(component: Int): Float
```

Returns the maximum valid value for the specified component of this color space's color model.

| Parameters ||
|---|---|
| `component` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index of the component. Value is between 0 and 3 inclusive |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | A floating point value greater than `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#getMinValue(kotlin.Int)` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#getMinValue(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Model#getComponentCount()`

### getMinValue

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getMinValue(component: Int): Float
```

Returns the minimum valid value for the specified component of this color space's color model.

| Parameters ||
|---|---|
| `component` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The index of the component. Value is between 0 and 3 inclusive |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | A floating point value less than `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#getMaxValue(kotlin.Int)` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#getMaxValue(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Model#getComponentCount()`

### getModel

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getModel(): ColorSpace.Model
```

Return the color model of this color space.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Model` | A non-null `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Model` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Model`
- `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#getComponentCount()`

### getName

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getName(): String
```

Returns the name of this color space. The name is never null and contains always at least 1 character.

Color space names are recommended to be unique but are not guaranteed to be. There is no defined format but the name usually falls in one of the following categories:

- Generic names used to identify color spaces in non-RGB color models. For instance: `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named`.
- Names tied to a particular specification. For instance: `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named` or `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named`.
- Ad-hoc names, often generated procedurally or by the user during a calibration workflow. These names often contain the make and model of the display.

Because the format of color space names is not defined, it is not recommended to programmatically identify a color space by its name alone. Names can be used as a first approximation.

It is however perfectly acceptable to display color space names to users in a UI, or in debuggers and logs. When displaying a color space name to the user, it is recommended to add extra information to avoid ambiguities: color model, a representation of the color space's gamut, white point, etc.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | A non-null String of length \>= 1 |

### hashCode

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by `https://developer.android.com/reference/kotlin/java/util/HashMap.html#`.

The general contract of `hashCode` is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the `hashCode` method must consistently return the same integer, provided no information used in `equals` comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce the same integer result.
- It is *not* required that if two objects are unequal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

### isSrgb

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isSrgb(): Boolean
```

Indicates whether this color space is the sRGB color space or equivalent to the sRGB color space.

A color space is considered sRGB if it meets all the following conditions:

- Its color model is `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Model`.
- Its primaries are within 1e-3 of the true `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named` primaries.
- Its white point is within 1e-3 of the CIE standard illuminant `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#ILLUMINANT_D65:kotlin.FloatArray`.
- Its opto-electronic transfer function is not linear.
- Its electro-optical transfer function is not linear.
- Its transfer functions yield values within 1e-3 of `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named`.
- Its range is \\(\[0..1\]\\).

This method always returns true for `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if this color space is the sRGB color space (or a close approximation), false otherwise |

### isWideGamut

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun isWideGamut(): Boolean
```

Returns whether this color space is a wide-gamut color space. An RGB color space is wide-gamut if its gamut entirely contains the `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named` gamut and if the area of its gamut is 90% of greater than the area of the `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named` gamut.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if this color space is a wide-gamut color space, false otherwise |

### match

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun match(
    toXYZD50: FloatArray, 
    function: ColorSpace.Rgb.TransferParameters
): ColorSpace?
```

Returns a `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named` instance of `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#` that matches the specified RGB to CIE XYZ transform and transfer functions. If no instance can be found, this method returns null.

The color transform matrix is assumed to target the CIE XYZ space a `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#ILLUMINANT_D50:kotlin.FloatArray` standard illuminant.

| Parameters ||
|---|---|
| `toXYZD50` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html): 3x3 column-major transform matrix from RGB to the profile connection space CIE XYZ as an array of 9 floats, cannot be null |
| `function` | [ColorSpace.Rgb.TransferParameters](../android/graphics/ColorSpace.Rgb.TransferParameters.md): Parameters for the transfer functions. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#?` | A non-null `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#` if a match is found, null otherwise |

### toString

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Returns a string representation of the object. This method returns a string equal to the value of:

```kotlin
getName() + "(id=" + getId() + ", model=" + getModel() + ")"
  
```

For instance, the string representation of the `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named` color space is equal to the following value:

```kotlin
sRGB IEC61966-2.1 (id=0, model=RGB)
  
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | A string representation of the object. This value cannot be `null`. |

### toXyz

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toXyz(
    r: Float, 
    g: Float, 
    b: Float
): FloatArray
```

Converts a color value from this color space's model to tristimulus CIE XYZ values. If the color model of this color space is not `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Model`, it is assumed that the target CIE XYZ space uses a `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#ILLUMINANT_D50:kotlin.FloatArray` standard illuminant.

This method is a convenience for color spaces with a model of 3 components (`https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Model` or `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Model` for instance). With color spaces using fewer or more components, use `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#toXyz(kotlin.FloatArray)` instead
.

| Parameters ||
|---|---|
| `r` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The first component of the value to convert from (typically R in RGB) |
| `g` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The second component of the value to convert from (typically G in RGB) |
| `b` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The third component of the value to convert from (typically B in RGB) |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html` | A new array of 3 floats, containing tristimulus XYZ values. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#toXyz(kotlin.FloatArray)`
- `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#fromXyz(kotlin.Float,%20kotlin.Float,%20kotlin.Float)`

### toXyz

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun toXyz(v: FloatArray): FloatArray
```

Converts a color value from this color space's model to tristimulus CIE XYZ values. If the color model of this color space is not `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Model`, it is assumed that the target CIE XYZ space uses a `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#ILLUMINANT_D50:kotlin.FloatArray` standard illuminant.

The specified array's length must be at least equal to to the number of color components as returned by `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Model#getComponentCount()`.

| Parameters ||
|---|---|
| `v` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html): An array of color components containing the color space's color value to convert to XYZ, and large enough to hold the resulting tristimulus XYZ values. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html` | The array passed in parameter. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#toXyz(kotlin.Float,%20kotlin.Float,%20kotlin.Float)`
- `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#fromXyz(kotlin.FloatArray)`

## Properties

### ILLUMINANT_A

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ILLUMINANT_A: FloatArray!
```

Standard CIE 1931 2° illuminant A, encoded in xyY. This illuminant has a color temperature of 2856K.

### ILLUMINANT_B

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ILLUMINANT_B: FloatArray!
```

Standard CIE 1931 2° illuminant B, encoded in xyY. This illuminant has a color temperature of 4874K.

### ILLUMINANT_C

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ILLUMINANT_C: FloatArray!
```

Standard CIE 1931 2° illuminant C, encoded in xyY. This illuminant has a color temperature of 6774K.

### ILLUMINANT_D50

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ILLUMINANT_D50: FloatArray!
```

Standard CIE 1931 2° illuminant D50, encoded in xyY. This illuminant has a color temperature of 5003K. This illuminant is used by the profile connection space in ICC profiles.

### ILLUMINANT_D55

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ILLUMINANT_D55: FloatArray!
```

Standard CIE 1931 2° illuminant D55, encoded in xyY. This illuminant has a color temperature of 5503K.

### ILLUMINANT_D60

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ILLUMINANT_D60: FloatArray!
```

Standard CIE 1931 2° illuminant D60, encoded in xyY. This illuminant has a color temperature of 6004K.

### ILLUMINANT_D65

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ILLUMINANT_D65: FloatArray!
```

Standard CIE 1931 2° illuminant D65, encoded in xyY. This illuminant has a color temperature of 6504K. This illuminant is commonly used in RGB color spaces such as sRGB, BT.709, etc.

### ILLUMINANT_D75

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ILLUMINANT_D75: FloatArray!
```

Standard CIE 1931 2° illuminant D75, encoded in xyY. This illuminant has a color temperature of 7504K.

### ILLUMINANT_E

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ILLUMINANT_E: FloatArray!
```

Standard CIE 1931 2° illuminant E, encoded in xyY. This illuminant has a color temperature of 5454K.
