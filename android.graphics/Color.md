# Color

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Color

Kotlin| [Java](https://developer.android.com/reference/android/graphics/Color "View this page in Java") 
| --- | --- |

```
open class Color
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.Color](https://developer.android.com/reference/kotlin/android/graphics/Color#) |

The`Color`class provides methods for creating, converting and manipulating colors. Colors have three different representations:

- Color ints, the most common representation
- Color longs
- `Color`instances

The section below describe each representation in detail.

### Color ints

Color ints are the most common representation of colors on Android and have been used since [API level 1](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#BASE:kotlin.Int).

A color int always defines a color in the [sRGB](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named) color space using 4 components packed in a single 32 bit integer value:

| Component | Name | Size | Range |
|-----------|-------|--------|------------------|
| A | Alpha | 8 bits | \\(\[0..255\]\\) |
| R | Red | 8 bits | \\(\[0..255\]\\) |
| G | Green | 8 bits | \\(\[0..255\]\\) |
| --- | --- | --- | --- |
| B | Blue | 8 bits | \\(\[0..255\]\\) |

The components in this table are listed in encoding order (see below), which is why color ints are called ARGB colors.

#### Usage in code

To avoid confusing color ints with arbitrary integer values, it is a good practice to annotate them with the`@ColorInt`annotation found in the Android Support Library.

#### Encoding

The four components of a color int are encoded in the following way: 

```kotlin
int color = (A & 0xff) << 24 | (R & 0xff) << 16 | (G & 0xff) << 8 | (B & 0xff);
  
```

Because of this encoding, color ints can easily be described as an integer constant in source. For instance, opaque blue is`0xff0000ff`and yellow is`0xffffff00`.

To easily encode color ints, it is recommended to use the static methods [argb(int,int,int,int)](https://developer.android.com/reference/kotlin/android/graphics/Color#argb(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))and [rgb(int,int,int)](https://developer.android.com/reference/kotlin/android/graphics/Color#rgb(kotlin.Int,%20kotlin.Int,%20kotlin.Int)). The second method omits the alpha component and assumes the color is opaque (alpha is 255). As a convenience this class also offers methods to encode color ints from components defined in the \\(\[0..1\]\\) range: [argb(float,float,float,float)](https://developer.android.com/reference/kotlin/android/graphics/Color#argb(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float))and [rgb(float,float,float)](https://developer.android.com/reference/kotlin/android/graphics/Color#rgb(kotlin.Float,%20kotlin.Float,%20kotlin.Float)).

Color longs (defined below) can be easily converted to color ints by invoking the [toArgb(long)](https://developer.android.com/reference/kotlin/android/graphics/Color#toArgb(kotlin.Long))method. This method performs a color space conversion if needed.

It is also possible to create a color int by invoking the method [toArgb()](https://developer.android.com/reference/kotlin/android/graphics/Color#toArgb())on a color instance.

#### Decoding

The four ARGB components can be individually extracted from a color int using the following expressions: 

```kotlin
int A = (color >> 24) & 0xff; // or color >>> 24
  int R = (color >> 16) & 0xff;
  int G = (color >>  8) & 0xff;
  int B = (color      ) & 0xff;
  
```

This class offers convenience methods to easily extract these components:

- [alpha(int)](https://developer.android.com/reference/kotlin/android/graphics/Color#alpha(kotlin.Int))to extract the alpha component
- [red(int)](https://developer.android.com/reference/kotlin/android/graphics/Color#red(kotlin.Int))to extract the red component
- [green(int)](https://developer.android.com/reference/kotlin/android/graphics/Color#green(kotlin.Int))to extract the green component
- [blue(int)](https://developer.android.com/reference/kotlin/android/graphics/Color#blue(kotlin.Int))to extract the blue component

### Color longs

Color longs are a representation introduced in [Android O](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int) to store colors in different [color spaces](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace), with more precision than color ints.

A color long always defines a color using 4 components packed in a single 64 bit long value. One of these components is always alpha while the other three components depend on the color space's [color model](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Model). The most common color model is the [RGB](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Model) model in which the components represent red, green and blue values.

**Component ranges:** the ranges defined in the tables below indicate the ranges that can be encoded in a color long. They do not represent the actual ranges as they may differ per color space. For instance, the RGB components of a color in the [Display P3](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named) color space use the \\(\[0..1\]\\) range. Please refer to the documentation of the various [color spaces](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named) to find their respective ranges.

**Alpha range:**while alpha is encoded in a color long using a 10 bit integer (thus using a range of \\(\[0..1023\]\\)), it is converted to and from \\(\[0..1\]\\) float values when decoding and encoding color longs.

**sRGB color space:** for compatibility reasons and ease of use, color longs encoding [sRGB](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named) colors do not use the same encoding as other color longs.

| Component | Name | Size | Range |
|-----------|-------------|---------|-----------------------------|
| [RGB](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Model) color model ||||
| R | Red | 16 bits | \\(\[-65504.0, 65504.0\]\\) |
| G | Green | 16 bits | \\(\[-65504.0, 65504.0\]\\) |
| --- | --- | --- | --- |
| B | Blue | 16 bits | \\(\[-65504.0, 65504.0\]\\) |
| A | Alpha | 10 bits | \\(\[0..1023\]\\) |
| | Color space | 6 bits | \\(\[0..63\]\\) |
| --- | --- | --- | --- |
| [sRGB](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named) color space ||||
| A | Alpha | 8 bits | \\(\[0..255\]\\) |
| R | Red | 8 bits | \\(\[0..255\]\\) |
| --- | --- | --- | --- |
| G | Green | 8 bits | \\(\[0..255\]\\) |
| B | Blue | 8 bits | \\(\[0..255\]\\) |
| X | Unused | 32 bits | \\(0\\) |
| --- | --- | --- | --- |
| [XYZ](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Model) color model ||||
| X | X | 16 bits | \\(\[-65504.0, 65504.0\]\\) |
| Y | Y | 16 bits | \\(\[-65504.0, 65504.0\]\\) |
| --- | --- | --- | --- |
| Z | Z | 16 bits | \\(\[-65504.0, 65504.0\]\\) |
| A | Alpha | 10 bits | \\(\[0..1023\]\\) |
| | Color space | 6 bits | \\(\[0..63\]\\) |
| --- | --- | --- | --- |
| [Lab](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Model) color model ||||
| L | L | 16 bits | \\(\[-65504.0, 65504.0\]\\) |
| a | a | 16 bits | \\(\[-65504.0, 65504.0\]\\) |
| --- | --- | --- | --- |
| b | b | 16 bits | \\(\[-65504.0, 65504.0\]\\) |
| A | Alpha | 10 bits | \\(\[0..1023\]\\) |
| | Color space | 6 bits | \\(\[0..63\]\\) |
| --- | --- | --- | --- |
| [CMYK](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Model) color model ||||
| Unsupported ||||

The components in this table are listed in encoding order (see below), which is why color longs in the RGB model are called RGBA colors (even if this doesn't quite hold for the special case of sRGB colors).

The color long encoding relies on half-precision float values (fp16). If you wish to know more about the limitations of half-precision float values, please refer to the documentation of the [Half](https://developer.android.com/reference/kotlin/android/util/Half.html#) class.

#### Usage in code

To avoid confusing color longs with arbitrary long values, it is a good practice to annotate them with the`@ColorLong`annotation found in the Android Support Library.

#### Encoding

Given the complex nature of color longs, it is strongly encouraged to use the various methods provided by this class to encode them.

The most flexible way to encode a color long is to use the method [pack(float,float,float,float,android.graphics.ColorSpace)](https://developer.android.com/reference/kotlin/android/graphics/Color#pack(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20android.graphics.ColorSpace)). This method allows you to specify three color components (typically RGB), an alpha component and a color space. To encode sRGB colors, use [pack(float,float,float)](https://developer.android.com/reference/kotlin/android/graphics/Color#pack(kotlin.Float,%20kotlin.Float,%20kotlin.Float))and [pack(float,float,float,float)](https://developer.android.com/reference/kotlin/android/graphics/Color#pack(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float))which are the equivalent of [rgb(int,int,int)](https://developer.android.com/reference/kotlin/android/graphics/Color#rgb(kotlin.Int,%20kotlin.Int,%20kotlin.Int))and [argb(int,int,int,int)](https://developer.android.com/reference/kotlin/android/graphics/Color#argb(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))for color ints. If you simply need to convert a color int into a color long, use [pack(int)](https://developer.android.com/reference/kotlin/android/graphics/Color#pack(kotlin.Int)).

It is also possible to create a color long value by invoking the method [pack()](https://developer.android.com/reference/kotlin/android/graphics/Color#pack())on a color instance.

#### Decoding

This class offers convenience methods to easily extract the components of a color long:

- [alpha(long)](https://developer.android.com/reference/kotlin/android/graphics/Color#alpha(kotlin.Long))to extract the alpha component
- [red(long)](https://developer.android.com/reference/kotlin/android/graphics/Color#red(kotlin.Long))to extract the red/X/L component
- [green(long)](https://developer.android.com/reference/kotlin/android/graphics/Color#green(kotlin.Long))to extract the green/Y/a component
- [blue(long)](https://developer.android.com/reference/kotlin/android/graphics/Color#blue(kotlin.Long))to extract the blue/Z/b component

The values returned by these methods depend on the color space encoded in the color long. The values are however typically in the \\(\[0..1\]\\) range for RGB colors. Please refer to the documentation of the various [color spaces](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named) for the exact ranges.

### Color instances

Color instances are a representation introduced in [Android O](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#O:kotlin.Int) to store colors in different [color spaces](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace), with more precision than both color ints and color longs. Color instances also offer the ability to store more than 4 components if necessary.

Colors instances are immutable and can be created using one of the various`valueOf`methods. For instance: 

```kotlin
// sRGB
  Color opaqueRed = Color.valueOf(0xffff0000); // from a color int
  Color translucentRed = Color.valueOf(1.0f, 0.0f, 0.0f, 0.5f);
 
  // Wide gamut color
  @ColorLong long p3 = pack(1.0f, 1.0f, 0.0f, 1.0f, colorSpaceP3);
  Color opaqueYellow = Color.valueOf(p3); // from a color long
 
  // CIE L*a*b* color space
  ColorSpace lab = ColorSpace.get(ColorSpace.Named.LAB);
  Color green = Color.valueOf(100.0f, -128.0f, 128.0f, 1.0f, lab);
  
```

Color instances can be converted to color ints ([toArgb()](https://developer.android.com/reference/kotlin/android/graphics/Color#toArgb())) or color longs ([pack()](https://developer.android.com/reference/kotlin/android/graphics/Color#pack())). They also offer easy access to their various components using the following methods:

- [alpha()](https://developer.android.com/reference/kotlin/android/graphics/Color#alpha()), returns the alpha component value
- [red()](https://developer.android.com/reference/kotlin/android/graphics/Color#red()), returns the red component value (or first component value in non-RGB models)
- [green()](https://developer.android.com/reference/kotlin/android/graphics/Color#green()), returns the green component value (or second component value in non-RGB models)
- [blue()](https://developer.android.com/reference/kotlin/android/graphics/Color#blue()), returns the blue component value (or third component value in non-RGB models)
- [getComponent(int)](https://developer.android.com/reference/kotlin/android/graphics/Color#getComponent(kotlin.Int)), returns a specific component value
- [getComponents()](https://developer.android.com/reference/kotlin/android/graphics/Color#getComponents()), returns all component values as an array

### Color space conversions

You can convert colors from one color space to another using [ColorSpace.connect(ColorSpace, ColorSpace)](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#connect(android.graphics.ColorSpace,%20android.graphics.ColorSpace))and its variants. However, the`Color`class provides a few convenience methods to simplify the process. Here is a brief description of some of them:

- [convert(android.graphics.ColorSpace)](https://developer.android.com/reference/kotlin/android/graphics/Color#convert(android.graphics.ColorSpace))to convert a color instance in a color space to a new color instance in a different color space
- [convert(float,float,float,float,android.graphics.ColorSpace,android.graphics.ColorSpace)](https://developer.android.com/reference/kotlin/android/graphics/Color#convert(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20android.graphics.ColorSpace,%20android.graphics.ColorSpace))to convert a color from a source color space to a destination color space
- [convert(long,android.graphics.ColorSpace)](https://developer.android.com/reference/kotlin/android/graphics/Color#convert(kotlin.Long,%20android.graphics.ColorSpace))to convert a color long from its built-in color space to a destination color space
- [convert(int,android.graphics.ColorSpace)](https://developer.android.com/reference/kotlin/android/graphics/Color#convert(kotlin.Int,%20android.graphics.ColorSpace))to convert a color int from sRGB to a destination color space

Please refere to the [ColorSpace](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace) documentation for more information.

### Alpha and transparency

The alpha component of a color defines the level of transparency of a color. When the alpha component is 0, the color is completely transparent. When the alpha is component is 1 (in the \\(\[0..1\]\\) range) or 255 (in the \\(\[0..255\]\\) range), the color is completely opaque.

The color representations described above do not use pre-multiplied color components (a pre-multiplied color component is a color component that has been multiplied by the value of the alpha component). For instance, the color int representation of opaque red is`0xffff0000`. For semi-transparent (50%) red, the representation becomes`0x80ff0000`. The equivalent color instance representations would be`(1.0, 0.0, 0.0, 1.0)`and`(1.0, 0.0, 0.0, 0.5)`.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BLACK](https://developer.android.com/reference/kotlin/android/graphics/Color#BLACK:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BLUE](https://developer.android.com/reference/kotlin/android/graphics/Color#BLUE:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CYAN](https://developer.android.com/reference/kotlin/android/graphics/Color#CYAN:kotlin.Int) <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DKGRAY](https://developer.android.com/reference/kotlin/android/graphics/Color#DKGRAY:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GRAY](https://developer.android.com/reference/kotlin/android/graphics/Color#GRAY:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GREEN](https://developer.android.com/reference/kotlin/android/graphics/Color#GREEN:kotlin.Int) <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LTGRAY](https://developer.android.com/reference/kotlin/android/graphics/Color#LTGRAY:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MAGENTA](https://developer.android.com/reference/kotlin/android/graphics/Color#MAGENTA:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RED](https://developer.android.com/reference/kotlin/android/graphics/Color#RED:kotlin.Int) <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRANSPARENT](https://developer.android.com/reference/kotlin/android/graphics/Color#TRANSPARENT:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [WHITE](https://developer.android.com/reference/kotlin/android/graphics/Color#WHITE:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [YELLOW](https://developer.android.com/reference/kotlin/android/graphics/Color#YELLOW:kotlin.Int) <br /> |
| --- | --- |

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Color](https://developer.android.com/reference/kotlin/android/graphics/Color#Color())`()` Creates a new color instance set to opaque black in the [sRGB](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named) color space. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HSVToColor](https://developer.android.com/reference/kotlin/android/graphics/Color#HSVToColor(kotlin.FloatArray))`(`hsv:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`)` Convert HSV components to an ARGB color. |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HSVToColor](https://developer.android.com/reference/kotlin/android/graphics/Color#HSVToColor(kotlin.Int,%20kotlin.FloatArray))`(`alpha:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `hsv:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`)` Convert HSV components to an ARGB color. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [RGBToHSV](https://developer.android.com/reference/kotlin/android/graphics/Color#RGBToHSV(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.FloatArray))`(`red:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `green:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `blue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `hsv:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`)` Convert RGB components to HSV. |
| --- | --- |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [alpha](https://developer.android.com/reference/kotlin/android/graphics/Color#alpha())`()` Returns the value of the alpha component in the range \\(\[0..1\]\\). |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [alpha](https://developer.android.com/reference/kotlin/android/graphics/Color#alpha(kotlin.Int))`(`color:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the alpha component of a color int. |
| openstatic [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [alpha](https://developer.android.com/reference/kotlin/android/graphics/Color#alpha(kotlin.Long))`(`color:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns the alpha component encoded in the specified color long. |
| --- | --- |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [argb](https://developer.android.com/reference/kotlin/android/graphics/Color#argb(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float))`(`alpha:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `red:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `green:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `blue:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Return a color-int from alpha, red, green, blue float components in the range \\(\[0..1\]\\). |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [argb](https://developer.android.com/reference/kotlin/android/graphics/Color#argb(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`alpha:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `red:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `green:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `blue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return a color-int from alpha, red, green, blue components. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [blue](https://developer.android.com/reference/kotlin/android/graphics/Color#blue())`()` Returns the value of the blue component in the range defined by this color's color space (see [ColorSpace.getMinValue(int)](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#getMinValue(kotlin.Int))and [ColorSpace.getMaxValue(int)](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#getMaxValue(kotlin.Int))). |
| --- | --- |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [blue](https://developer.android.com/reference/kotlin/android/graphics/Color#blue(kotlin.Int))`(`color:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the blue component of a color int. |
| openstatic [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [blue](https://developer.android.com/reference/kotlin/android/graphics/Color#blue(kotlin.Long))`(`color:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns the blue component encoded in the specified color long. |
| openstatic [ColorSpace](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace) | [colorSpace](https://developer.android.com/reference/kotlin/android/graphics/Color#colorSpace(kotlin.Long))`(`color:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns the color space encoded in the specified color long. |
| --- | --- |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [colorToHSV](https://developer.android.com/reference/kotlin/android/graphics/Color#colorToHSV(kotlin.Int,%20kotlin.FloatArray))`(`color:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `hsv:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!`)` Convert the ARGB color to its HSV components. |
| open [Color](https://developer.android.com/reference/kotlin/android/graphics/Color#) | [convert](https://developer.android.com/reference/kotlin/android/graphics/Color#convert(android.graphics.ColorSpace))`(`colorSpace:` ` [ColorSpace](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace)`)` Converts this color from its color space to the specified color space. |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [convert](https://developer.android.com/reference/kotlin/android/graphics/Color#convert(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20android.graphics.ColorSpace,%20android.graphics.ColorSpace))`(`r:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `g:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `b:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `a:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `source:` ` [ColorSpace](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace)`, `destination:` ` [ColorSpace](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace)`)` Converts the specified 3 component color from the source color space to the destination color space. |
| --- | --- |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [convert](https://developer.android.com/reference/kotlin/android/graphics/Color#convert(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20android.graphics.ColorSpace.Connector))`(`r:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `g:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `b:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `a:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `connector:` ` [ColorSpace.Connector](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Connector)`)` Converts the specified 3 component color from a color space to another using the specified color space [connector](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Connector). |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [convert](https://developer.android.com/reference/kotlin/android/graphics/Color#convert(kotlin.Int,%20android.graphics.ColorSpace))`(`color:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `colorSpace:` ` [ColorSpace](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace)`)` Converts the specified ARGB color int from the [sRGB](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named) color space into the specified destination color space. |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [convert](https://developer.android.com/reference/kotlin/android/graphics/Color#convert(kotlin.Long,%20android.graphics.ColorSpace))`(`color:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `colorSpace:` ` [ColorSpace](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace)`)` Converts the specified color long from its color space into the specified destination color space. |
| --- | --- |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [convert](https://developer.android.com/reference/kotlin/android/graphics/Color#convert(kotlin.Long,%20android.graphics.ColorSpace.Connector))`(`color:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `connector:` ` [ColorSpace.Connector](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Connector)`)` Converts the specified color long from a color space to another using the specified color space [connector](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Connector). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/graphics/Color#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| open [ColorSpace](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace) | [getColorSpace](https://developer.android.com/reference/kotlin/android/graphics/Color#getColorSpace())`()` Returns this color's color space. |
| --- | --- |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getComponent](https://developer.android.com/reference/kotlin/android/graphics/Color#getComponent(kotlin.Int))`(`component:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the value of the specified component in the range defined by this color's color space (see [ColorSpace.getMinValue(int)](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#getMinValue(kotlin.Int))and [ColorSpace.getMaxValue(int)](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#getMaxValue(kotlin.Int))). |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getComponentCount](https://developer.android.com/reference/kotlin/android/graphics/Color#getComponentCount())`()` Returns the number of components that form a color value according to this color space's color model, plus one extra component for alpha. |
| open [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html) | [getComponents](https://developer.android.com/reference/kotlin/android/graphics/Color#getComponents())`()` Returns this color's components as a new array. |
| --- | --- |
| open [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html) | [getComponents](https://developer.android.com/reference/kotlin/android/graphics/Color#getComponents(kotlin.FloatArray))`(`components:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)?`)` Copies this color's components in the supplied array. |
| open [ColorSpace.Model](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Model)! | [getModel](https://developer.android.com/reference/kotlin/android/graphics/Color#getModel())`()` Returns the color model of this color. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [green](https://developer.android.com/reference/kotlin/android/graphics/Color#green())`()` Returns the value of the green component in the range defined by this color's color space (see [ColorSpace.getMinValue(int)](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#getMinValue(kotlin.Int))and [ColorSpace.getMaxValue(int)](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#getMaxValue(kotlin.Int))). |
| --- | --- |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [green](https://developer.android.com/reference/kotlin/android/graphics/Color#green(kotlin.Int))`(`color:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the green component of a color int. |
| openstatic [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [green](https://developer.android.com/reference/kotlin/android/graphics/Color#green(kotlin.Long))`(`color:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns the green component encoded in the specified color long. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/graphics/Color#hashCode())`()` <br /> |
| --- | --- |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isInColorSpace](https://developer.android.com/reference/kotlin/android/graphics/Color#isInColorSpace(kotlin.Long,%20android.graphics.ColorSpace))`(`color:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `colorSpace:` ` [ColorSpace](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace)`)` Indicates whether the specified color is in the specified color space. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSrgb](https://developer.android.com/reference/kotlin/android/graphics/Color#isSrgb())`()` Indicates whether this color is in the [sRGB](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named) color space. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSrgb](https://developer.android.com/reference/kotlin/android/graphics/Color#isSrgb(kotlin.Long))`(`color:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Indicates whether the specified color is in the [sRGB](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named) color space. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isWideGamut](https://developer.android.com/reference/kotlin/android/graphics/Color#isWideGamut())`()` Indicates whether this color color is in a wide-gamut color space. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isWideGamut](https://developer.android.com/reference/kotlin/android/graphics/Color#isWideGamut(kotlin.Long))`(`color:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Indicates whether the specified color is in a wide-gamut color space. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [luminance](https://developer.android.com/reference/kotlin/android/graphics/Color#luminance())`()` Returns the relative luminance of this color. |
| --- | --- |
| openstatic [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [luminance](https://developer.android.com/reference/kotlin/android/graphics/Color#luminance(kotlin.Int))`(`color:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the relative luminance of a color. |
| openstatic [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [luminance](https://developer.android.com/reference/kotlin/android/graphics/Color#luminance(kotlin.Long))`(`color:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns the relative luminance of a color. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [pack](https://developer.android.com/reference/kotlin/android/graphics/Color#pack())`()` Packs this color into a color long. |
| --- | --- |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [pack](https://developer.android.com/reference/kotlin/android/graphics/Color#pack(kotlin.Float,%20kotlin.Float,%20kotlin.Float))`(`red:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `green:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `blue:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Packs the sRGB color defined by the specified red, green and blue component values into an RGBA color long in the sRGB color space. |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [pack](https://developer.android.com/reference/kotlin/android/graphics/Color#pack(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float))`(`red:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `green:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `blue:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `alpha:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Packs the sRGB color defined by the specified red, green, blue and alpha component values into an RGBA color long in the sRGB color space. |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [pack](https://developer.android.com/reference/kotlin/android/graphics/Color#pack(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20android.graphics.ColorSpace))`(`red:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `green:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `blue:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `alpha:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `colorSpace:` ` [ColorSpace](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace)`)` Packs the 3 component color defined by the specified red, green, blue and alpha component values into a color long in the specified color space. |
| --- | --- |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [pack](https://developer.android.com/reference/kotlin/android/graphics/Color#pack(kotlin.Int))`(`color:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Converts the specified ARGB color int to an RGBA color long in the sRGB color space. |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [parseColor](https://developer.android.com/reference/kotlin/android/graphics/Color#parseColor(kotlin.String))`(`colorString:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Parse the color string, and return the corresponding color-int. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [red](https://developer.android.com/reference/kotlin/android/graphics/Color#red())`()` Returns the value of the red component in the range defined by this color's color space (see [ColorSpace.getMinValue(int)](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#getMinValue(kotlin.Int))and [ColorSpace.getMaxValue(int)](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#getMaxValue(kotlin.Int))). |
| --- | --- |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [red](https://developer.android.com/reference/kotlin/android/graphics/Color#red(kotlin.Int))`(`color:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the red component of a color int. |
| openstatic [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [red](https://developer.android.com/reference/kotlin/android/graphics/Color#red(kotlin.Long))`(`color:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns the red component encoded in the specified color long. |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [rgb](https://developer.android.com/reference/kotlin/android/graphics/Color#rgb(kotlin.Float,%20kotlin.Float,%20kotlin.Float))`(`red:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `green:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `blue:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Return a color-int from red, green, blue float components in the range \\(\[0..1\]\\). |
| --- | --- |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [rgb](https://developer.android.com/reference/kotlin/android/graphics/Color#rgb(kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`red:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `green:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `blue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return a color-int from red, green, blue components. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [toArgb](https://developer.android.com/reference/kotlin/android/graphics/Color#toArgb())`()` Converts this color to an ARGB color int. |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [toArgb](https://developer.android.com/reference/kotlin/android/graphics/Color#toArgb(kotlin.Long))`(`color:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Converts the specified color long to an ARGB color int. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/graphics/Color#toString())`()` Returns a string representation of the object. |
| openstatic [Color](https://developer.android.com/reference/kotlin/android/graphics/Color#) | [valueOf](https://developer.android.com/reference/kotlin/android/graphics/Color#valueOf(kotlin.Float,%20kotlin.Float,%20kotlin.Float))`(`r:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `g:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `b:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Creates a new opaque`Color`in the [sRGB](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named) color space with the specified red, green and blue component values. |
| openstatic [Color](https://developer.android.com/reference/kotlin/android/graphics/Color#) | [valueOf](https://developer.android.com/reference/kotlin/android/graphics/Color#valueOf(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float))`(`r:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `g:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `b:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `a:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Creates a new`Color`in the [sRGB](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named) color space with the specified red, green, blue and alpha component values. |
| --- | --- |
| openstatic [Color](https://developer.android.com/reference/kotlin/android/graphics/Color#) | [valueOf](https://developer.android.com/reference/kotlin/android/graphics/Color#valueOf(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20android.graphics.ColorSpace))`(`r:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `g:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `b:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `a:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `colorSpace:` ` [ColorSpace](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace)`)` Creates a new`Color`in the specified color space with the specified red, green, blue and alpha component values. |
| openstatic [Color](https://developer.android.com/reference/kotlin/android/graphics/Color#) | [valueOf](https://developer.android.com/reference/kotlin/android/graphics/Color#valueOf(kotlin.FloatArray,%20android.graphics.ColorSpace))`(`components:` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)`, `colorSpace:` ` [ColorSpace](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace)`)` Creates a new`Color`in the specified color space with the specified component values. |
| openstatic [Color](https://developer.android.com/reference/kotlin/android/graphics/Color#) | [valueOf](https://developer.android.com/reference/kotlin/android/graphics/Color#valueOf(kotlin.Int))`(`color:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a new`Color`instance from an ARGB color int. |
| --- | --- |
| openstatic [Color](https://developer.android.com/reference/kotlin/android/graphics/Color#) | [valueOf](https://developer.android.com/reference/kotlin/android/graphics/Color#valueOf(kotlin.Long))`(`color:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Creates a new`Color`instance from a color long. |

## Constants

### BLACK

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BLACK: Int
```  

 Value: -16777216

### BLUE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BLUE: Int
```  

 Value: -16776961

### CYAN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CYAN: Int
```  

 Value: -16711681

### DKGRAY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DKGRAY: Int
```  

 Value: -12303292

### GRAY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GRAY: Int
```  

 Value: -7829368

### GREEN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GREEN: Int
```  

 Value: -16711936

### LTGRAY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LTGRAY: Int
```  

 Value: -3355444

### MAGENTA

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MAGENTA: Int
```  

 Value: -65281

### RED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RED: Int
```  

 Value: -65536

### TRANSPARENT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TRANSPARENT: Int
```  

 Value: 0

### WHITE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val WHITE: Int
```  

 Value: -1

### YELLOW

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val YELLOW: Int
```  

 Value: -256

## Public constructors

### Color

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Color()
```

Creates a new color instance set to opaque black in the [sRGB](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named) color space. 
**See Also**

- [#valueOf(float, float, float)](https://developer.android.com/reference/kotlin/android/graphics/Color#valueOf(kotlin.Float,%20kotlin.Float,%20kotlin.Float))
- [#valueOf(float, float, float, float)](https://developer.android.com/reference/kotlin/android/graphics/Color#valueOf(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float))
- [#valueOf(float, float, float, float, ColorSpace)](https://developer.android.com/reference/kotlin/android/graphics/Color#valueOf(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20android.graphics.ColorSpace))
- [#valueOf(float[], ColorSpace)](https://developer.android.com/reference/kotlin/android/graphics/Color#valueOf(kotlin.FloatArray,%20android.graphics.ColorSpace))
- [#valueOf(int)](https://developer.android.com/reference/kotlin/android/graphics/Color#valueOf(kotlin.Int))
- [#valueOf(long)](https://developer.android.com/reference/kotlin/android/graphics/Color#valueOf(kotlin.Long))

## Public methods

### HSVToColor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun HSVToColor(hsv: FloatArray!): Int
```

Convert HSV components to an ARGB color. Alpha set to 0xFF.

- `hsv[0]`is Hue \\(\[0..360\[\\)
- `hsv[1]`is Saturation \\(\[0...1\]\\)
- `hsv[2]`is Value \\(\[0...1\]\\)

If hsv values are out of range, they are pinned.

<br />

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `hsv` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:3 element array which holds the input HSV components. |

| Return ||
|----------------------------------------------------------------------------|--------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the resulting argb color |

### HSVToColor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun HSVToColor(
    alpha: Int, 
    hsv: FloatArray!
): Int
```

Convert HSV components to an ARGB color. The alpha component is passed through unchanged.

- `hsv[0]`is Hue \\(\[0..360\[\\)
- `hsv[1]`is Saturation \\(\[0...1\]\\)
- `hsv[2]`is Value \\(\[0...1\]\\)

If hsv values are out of range, they are pinned.

<br />

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `alpha` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the alpha component of the returned argb color. Value is between 0 and 255 inclusive |
| `hsv` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:3 element array which holds the input HSV components. |

| Return ||
|----------------------------------------------------------------------------|--------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the resulting argb color |

### RGBToHSV

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun RGBToHSV(
    red: Int, 
    green: Int, 
    blue: Int, 
    hsv: FloatArray!
): Unit
```

Convert RGB components to HSV.

- `hsv[0]`is Hue \\(\[0..360\[\\)
- `hsv[1]`is Saturation \\(\[0...1\]\\)
- `hsv[2]`is Value \\(\[0...1\]\\)

<br />

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `red` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):red component value \\(\[0..255\]\\) Value is between 0 and 255 inclusive |
| `green` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):green component value \\(\[0..255\]\\) Value is between 0 and 255 inclusive |
| `blue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):blue component value \\(\[0..255\]\\) Value is between 0 and 255 inclusive |
| --- | --- |
| `hsv` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:3 element array which holds the resulting HSV components. |

### alpha

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun alpha(): Float
```

Returns the value of the alpha component in the range \\(\[0..1\]\\). Calling this method is equivalent to`getComponent(getComponentCount() - 1)`. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/graphics/Color#red()>
- <https://developer.android.com/reference/kotlin/android/graphics/Color#green()>
- <https://developer.android.com/reference/kotlin/android/graphics/Color#blue()>
- <https://developer.android.com/reference/kotlin/android/graphics/Color#getComponents()>
- [#getComponent(int)](https://developer.android.com/reference/kotlin/android/graphics/Color#getComponent(kotlin.Int)) 

### alpha

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun alpha(color: Int): Int
```

Return the alpha component of a color int. This is the same as saying color \>\>\> 24

| Return ||
|----------------------------------------------------------------------------|--------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is between 0 and 255 inclusive |

### alpha

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun alpha(color: Long): Float
```

Returns the alpha component encoded in the specified color long. The returned value is always in the range \\(\[0..1\]\\).

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------|
| `color` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The color long whose alpha channel to extract |

| Return ||
|--------------------------------------------------------------------------------|-------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | A float value in the range \\(\[0..1\]\\) |

**See Also**

- [#colorSpace(long)](https://developer.android.com/reference/kotlin/android/graphics/Color#colorSpace(kotlin.Long))
- [#red(long)](https://developer.android.com/reference/kotlin/android/graphics/Color#red(kotlin.Long))
- [#green(long)](https://developer.android.com/reference/kotlin/android/graphics/Color#green(kotlin.Long))
- [#blue(long)](https://developer.android.com/reference/kotlin/android/graphics/Color#blue(kotlin.Long)) 

### argb

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun argb(
    alpha: Float, 
    red: Float, 
    green: Float, 
    blue: Float
): Int
```

Return a color-int from alpha, red, green, blue float components in the range \\(\[0..1\]\\). If the components are out of range, the returned color is undefined.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------|
| `alpha` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Alpha component \\(\[0..1\]\\) of the color |
| `red` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Red component \\(\[0..1\]\\) of the color |
| `green` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Green component \\(\[0..1\]\\) of the color |
| --- | --- |
| `blue` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Blue component \\(\[0..1\]\\) of the color |

### argb

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun argb(
    alpha: Int, 
    red: Int, 
    green: Int, 
    blue: Int
): Int
```

Return a color-int from alpha, red, green, blue components. These component values should be \\(\[0..255\]\\), but there is no range check performed, so if they are out of range, the returned color is undefined.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `alpha` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Alpha component \\(\[0..255\]\\) of the color Value is between 0 and 255 inclusive |
| `red` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Red component \\(\[0..255\]\\) of the color Value is between 0 and 255 inclusive |
| `green` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Green component \\(\[0..255\]\\) of the color Value is between 0 and 255 inclusive |
| --- | --- |
| `blue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Blue component \\(\[0..255\]\\) of the color Value is between 0 and 255 inclusive |

### blue

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun blue(): Float
```

Returns the value of the blue component in the range defined by this color's color space (see [ColorSpace.getMinValue(int)](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#getMinValue(kotlin.Int))and [ColorSpace.getMaxValue(int)](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#getMaxValue(kotlin.Int))).

If this color's color model is not [RGB](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Model), calling this method is equivalent to`getComponent(2)`. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/graphics/Color#alpha()>
- <https://developer.android.com/reference/kotlin/android/graphics/Color#red()>
- <https://developer.android.com/reference/kotlin/android/graphics/Color#getComponents()> 

### blue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun blue(color: Int): Int
```

Return the blue component of a color int. This is the same as saying color \& 0xFF

| Return ||
|----------------------------------------------------------------------------|--------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is between 0 and 255 inclusive |

### blue

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun blue(color: Long): Float
```

Returns the blue component encoded in the specified color long. The range of the returned value depends on the color space associated with the specified color. The color space can be queried by calling [colorSpace(long)](https://developer.android.com/reference/kotlin/android/graphics/Color#colorSpace(kotlin.Long)).

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------|
| `color` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The color long whose blue channel to extract |

| Return ||
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | A float value with a range defined by the specified color's color space |

**See Also**

- [#colorSpace(long)](https://developer.android.com/reference/kotlin/android/graphics/Color#colorSpace(kotlin.Long))
- [#red(long)](https://developer.android.com/reference/kotlin/android/graphics/Color#red(kotlin.Long))
- [#green(long)](https://developer.android.com/reference/kotlin/android/graphics/Color#green(kotlin.Long))
- [#alpha(long)](https://developer.android.com/reference/kotlin/android/graphics/Color#alpha(kotlin.Long)) 

### colorSpace

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun colorSpace(color: Long): ColorSpace
```

Returns the color space encoded in the specified color long.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------|
| `color` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The color long whose color space to extract |

| Return ||
|------------------------------------------------------------------------------------------|---------------------------------|
| [ColorSpace](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace) | A non-null color space instance |

| Exceptions ||
|--------------------------------------|--------------------------------------------------|
| `java.lang.IllegalArgumentException` | If the encoded color space is invalid or unknown |

**See Also**

- [#red(long)](https://developer.android.com/reference/kotlin/android/graphics/Color#red(kotlin.Long))
- [#green(long)](https://developer.android.com/reference/kotlin/android/graphics/Color#green(kotlin.Long))
- [#blue(long)](https://developer.android.com/reference/kotlin/android/graphics/Color#blue(kotlin.Long))
- [#alpha(long)](https://developer.android.com/reference/kotlin/android/graphics/Color#alpha(kotlin.Long)) 

### colorToHSV

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun colorToHSV(
    color: Int, 
    hsv: FloatArray!
): Unit
```

Convert the ARGB color to its HSV components.

- `hsv[0]`is Hue \\(\[0..360\[\\)
- `hsv[1]`is Saturation \\(\[0...1\]\\)
- `hsv[2]`is Value \\(\[0...1\]\\)

<br />

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `color` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the argb color to convert. The alpha component is ignored. |
| `hsv` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!:3 element array which holds the resulting HSV components. |

### convert

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun convert(colorSpace: ColorSpace): Color
```

Converts this color from its color space to the specified color space. The conversion is done using the default rendering intent as specified by [ColorSpace.connect(ColorSpace, ColorSpace)](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#connect(android.graphics.ColorSpace,%20android.graphics.ColorSpace)).

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------------|
| `colorSpace` | [ColorSpace](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace):The destination color space, cannot be null |

| Return ||
|---------------------------------------------------------------------------------|--------------------------------------------------------|
| [Color](https://developer.android.com/reference/kotlin/android/graphics/Color#) | A non-null color instance in the specified color space |

### convert

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun convert(
    r: Float, 
    g: Float, 
    b: Float, 
    a: Float, 
    source: ColorSpace, 
    destination: ColorSpace
): Long
```

Converts the specified 3 component color from the source color space to the destination color space. The resulting color is returned as a color long. See the documentation of this class for a description of the color long format.

When converting multiple colors in a row, it is recommended to use [convert(float,float,float,float,android.graphics.ColorSpace.Connector)](https://developer.android.com/reference/kotlin/android/graphics/Color#convert(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20android.graphics.ColorSpace.Connector))instead to avoid the creation of a [ColorSpace.Connector](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Connector) on every invocation.

The red, green and blue components must be in the range defined by the specified color space. See [ColorSpace.getMinValue(int)](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#getMinValue(kotlin.Int))and [ColorSpace.getMaxValue(int)](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#getMaxValue(kotlin.Int)).

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `r` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The red component of the color to convert |
| `g` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The green component of the color to convert |
| `b` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The blue component of the color to convert |
| --- | --- |
| `a` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The alpha component of the color to convert, in \\(\[0..1\]\\) |
| `source` | [ColorSpace](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace):The source color space, cannot be null |
| `destination` | [ColorSpace](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace):The destination color space, cannot be null |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------|---------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | A color long in the destination color space |

**See Also**

- [#convert(float, float, float, float, ColorSpace.Connector)](https://developer.android.com/reference/kotlin/android/graphics/Color#convert(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20android.graphics.ColorSpace.Connector)) 

### convert

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun convert(
    r: Float, 
    g: Float, 
    b: Float, 
    a: Float, 
    connector: ColorSpace.Connector
): Long
```

Converts the specified 3 component color from a color space to another using the specified color space [connector](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Connector). The resulting color is returned as a color long. See the documentation of this class for a description of the color long format.

When converting several colors in a row, this method is preferable to [convert(float,float,float,float,android.graphics.ColorSpace,android.graphics.ColorSpace)](https://developer.android.com/reference/kotlin/android/graphics/Color#convert(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20android.graphics.ColorSpace,%20android.graphics.ColorSpace))as it prevents a new connector from being created on every invocation.

The red, green and blue components must be in the range defined by the source color space of the connector. See [ColorSpace.getMinValue(int)](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#getMinValue(kotlin.Int))and [ColorSpace.getMaxValue(int)](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#getMaxValue(kotlin.Int)).

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `r` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The red component of the color to convert |
| `g` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The green component of the color to convert |
| `b` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The blue component of the color to convert |
| --- | --- |
| `a` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The alpha component of the color to convert, in \\(\[0..1\]\\) |
| `connector` | [ColorSpace.Connector](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Connector):A color space connector, cannot be null |

| Return ||
|------------------------------------------------------------------------------|--------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | A color long in the destination color space of the connector |

**See Also**

- [#convert(float, float, float, float, ColorSpace, ColorSpace)](https://developer.android.com/reference/kotlin/android/graphics/Color#convert(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20android.graphics.ColorSpace,%20android.graphics.ColorSpace)) 

### convert

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun convert(
    color: Int, 
    colorSpace: ColorSpace
): Long
```

Converts the specified ARGB color int from the [sRGB](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named) color space into the specified destination color space. The resulting color is returned as a color long. See the documentation of this class for a description of the color long format.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `color` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The sRGB color int to convert |
| `colorSpace` | [ColorSpace](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace):The destination color space This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------|---------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | A color long in the destination color space |

### convert

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun convert(
    color: Long, 
    colorSpace: ColorSpace
): Long
```

Converts the specified color long from its color space into the specified destination color space. The resulting color is returned as a color long. See the documentation of this class for a description of the color long format.

When converting several colors in a row, it is recommended to use [convert(long,android.graphics.ColorSpace.Connector)](https://developer.android.com/reference/kotlin/android/graphics/Color#convert(kotlin.Long,%20android.graphics.ColorSpace.Connector))instead to avoid the creation of a [ColorSpace.Connector](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Connector) on every invocation.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `color` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The color long to convert |
| `colorSpace` | [ColorSpace](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace):The destination color space This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------|---------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | A color long in the destination color space |

| Exceptions ||
|--------------------------------------|--------------------------------------------------|
| `java.lang.IllegalArgumentException` | If the encoded color space is invalid or unknown |

### convert

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun convert(
    color: Long, 
    connector: ColorSpace.Connector
): Long
```

Converts the specified color long from a color space to another using the specified color space [connector](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Connector). The resulting color is returned as a color long. See the documentation of this class for a description of the color long format.

When converting several colors in a row, this method is preferable to [convert(long,android.graphics.ColorSpace)](https://developer.android.com/reference/kotlin/android/graphics/Color#convert(kotlin.Long,%20android.graphics.ColorSpace))as it prevents a new connector from being created on every invocation.

The connector's source color space should match the color long's color space.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `color` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The color long to convert |
| `connector` | [ColorSpace.Connector](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Connector):A color space connector, cannot be null |

| Return ||
|------------------------------------------------------------------------------|--------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | A color long in the destination color space of the connector |

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getColorSpace

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getColorSpace(): ColorSpace
```

Returns this color's color space.

| Return ||
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [ColorSpace](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace) | A non-null instance of [ColorSpace](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace) |

### getComponent

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getComponent(component: Int): Float
```

Returns the value of the specified component in the range defined by this color's color space (see [ColorSpace.getMinValue(int)](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#getMinValue(kotlin.Int))and [ColorSpace.getMaxValue(int)](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#getMaxValue(kotlin.Int))).

If the requested component index is [getComponentCount()](https://developer.android.com/reference/kotlin/android/graphics/Color#getComponentCount()), this method returns the alpha component, always in the range \\(\[0..1\]\\).

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------|
| `component` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is between 0 and 4 inclusive |

| Exceptions ||
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ArrayIndexOutOfBoundsException` | If the specified component index is \< 0 or \>= [getComponentCount()](https://developer.android.com/reference/kotlin/android/graphics/Color#getComponentCount()) |

**See Also**

- <https://developer.android.com/reference/kotlin/android/graphics/Color#getComponents()> 

### getComponentCount

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getComponentCount(): Int
```

Returns the number of components that form a color value according to this color space's color model, plus one extra component for alpha.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The integer 4 or 5 Value is between 4 and 5 inclusive |

### getComponents

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getComponents(): FloatArray
```

Returns this color's components as a new array. The last element of the array is always the alpha component.

| Return ||
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html) | A new, non-null array whose size is equal to [getComponentCount()](https://developer.android.com/reference/kotlin/android/graphics/Color#getComponentCount()) |

**See Also**

- [#getComponent(int)](https://developer.android.com/reference/kotlin/android/graphics/Color#getComponent(kotlin.Int)) 

### getComponents

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getComponents(components: FloatArray?): FloatArray
```

Copies this color's components in the supplied array. The last element of the array is always the alpha component.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `components` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)?:An array of floats whose size must be at least [getComponentCount()](https://developer.android.com/reference/kotlin/android/graphics/Color#getComponentCount()), can be null |

| Return ||
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html) | The array passed as a parameter if not null, or a new array of length [getComponentCount()](https://developer.android.com/reference/kotlin/android/graphics/Color#getComponentCount()) |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If the specified array's length is less than [getComponentCount()](https://developer.android.com/reference/kotlin/android/graphics/Color#getComponentCount()) |

**See Also**

- [#getComponent(int)](https://developer.android.com/reference/kotlin/android/graphics/Color#getComponent(kotlin.Int)) 

### getModel

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getModel(): ColorSpace.Model!
```

Returns the color model of this color.

| Return ||
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [ColorSpace.Model](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Model)! | A non-null [ColorSpace.Model](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Model) |

### green

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun green(): Float
```

Returns the value of the green component in the range defined by this color's color space (see [ColorSpace.getMinValue(int)](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#getMinValue(kotlin.Int))and [ColorSpace.getMaxValue(int)](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#getMaxValue(kotlin.Int))).

If this color's color model is not [RGB](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Model), calling this method is equivalent to`getComponent(1)`. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/graphics/Color#alpha()>
- <https://developer.android.com/reference/kotlin/android/graphics/Color#red()>
- <https://developer.android.com/reference/kotlin/android/graphics/Color#getComponents()> 

### green

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun green(color: Int): Int
```

Return the green component of a color int. This is the same as saying (color \>\> 8) \& 0xFF

| Return ||
|----------------------------------------------------------------------------|--------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is between 0 and 255 inclusive |

### green

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun green(color: Long): Float
```

Returns the green component encoded in the specified color long. The range of the returned value depends on the color space associated with the specified color. The color space can be queried by calling [colorSpace(long)](https://developer.android.com/reference/kotlin/android/graphics/Color#colorSpace(kotlin.Long)).

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------|
| `color` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The color long whose green channel to extract |

| Return ||
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | A float value with a range defined by the specified color's color space |

**See Also**

- [#colorSpace(long)](https://developer.android.com/reference/kotlin/android/graphics/Color#colorSpace(kotlin.Long))
- [#red(long)](https://developer.android.com/reference/kotlin/android/graphics/Color#red(kotlin.Long))
- [#blue(long)](https://developer.android.com/reference/kotlin/android/graphics/Color#blue(kotlin.Long))
- [#alpha(long)](https://developer.android.com/reference/kotlin/android/graphics/Color#alpha(kotlin.Long)) 

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### isInColorSpace

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isInColorSpace(
    color: Long, 
    colorSpace: ColorSpace
): Boolean
```

Indicates whether the specified color is in the specified color space.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `color` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The color to test |
| `colorSpace` | [ColorSpace](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace):The color space to test against This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the color is in the specified color space, false otherwise |

**See Also**

- [#isSrgb(long)](https://developer.android.com/reference/kotlin/android/graphics/Color#isSrgb(kotlin.Long))
- [#isWideGamut(long)](https://developer.android.com/reference/kotlin/android/graphics/Color#isWideGamut(kotlin.Long)) 

### isSrgb

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isSrgb(): Boolean
```

Indicates whether this color is in the [sRGB](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named) color space.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if this color is in the sRGB color space, false otherwise |

**See Also**

- <https://developer.android.com/reference/kotlin/android/graphics/Color#isWideGamut()> 

### isSrgb

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isSrgb(color: Long): Boolean
```

Indicates whether the specified color is in the [sRGB](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named) color space.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------|
| `color` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The color to test |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the color is in the sRGB color space, false otherwise |

| Exceptions ||
|--------------------------------------|--------------------------------------------------|
| `java.lang.IllegalArgumentException` | If the encoded color space is invalid or unknown |

**See Also**

- [#isInColorSpace(long, ColorSpace)](https://developer.android.com/reference/kotlin/android/graphics/Color#isInColorSpace(kotlin.Long,%20android.graphics.ColorSpace))
- [#isWideGamut(long)](https://developer.android.com/reference/kotlin/android/graphics/Color#isWideGamut(kotlin.Long)) 

### isWideGamut

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isWideGamut(): Boolean
```

Indicates whether this color color is in a wide-gamut color space. See [ColorSpace.isWideGamut()](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#isWideGamut())for a definition of a wide-gamut color space.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if this color is in a wide-gamut color space, false otherwise |

**See Also**

- <https://developer.android.com/reference/kotlin/android/graphics/Color#isSrgb()>
- [android.graphics.ColorSpace#isWideGamut()](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#isWideGamut()) 

### isWideGamut

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isWideGamut(color: Long): Boolean
```

Indicates whether the specified color is in a wide-gamut color space. See [ColorSpace.isWideGamut()](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#isWideGamut())for a definition of a wide-gamut color space.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------|
| `color` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The color to test |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the color is in a wide-gamut color space, false otherwise |

| Exceptions ||
|--------------------------------------|--------------------------------------------------|
| `java.lang.IllegalArgumentException` | If the encoded color space is invalid or unknown |

**See Also**

- [#isInColorSpace(long, ColorSpace)](https://developer.android.com/reference/kotlin/android/graphics/Color#isInColorSpace(kotlin.Long,%20android.graphics.ColorSpace))
- [#isSrgb(long)](https://developer.android.com/reference/kotlin/android/graphics/Color#isSrgb(kotlin.Long))
- [android.graphics.ColorSpace#isWideGamut()](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#isWideGamut()) 

### luminance

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun luminance(): Float
```

Returns the relative luminance of this color.

Based on the formula for relative luminance defined in WCAG 2.0, W3C Recommendation 11 December 2008.

| Return ||
|--------------------------------------------------------------------------------|----------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | A value between 0 (darkest black) and 1 (lightest white) |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If the this color's color space does not use the [RGB](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Model) color model |

### luminance

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun luminance(color: Int): Float
```

Returns the relative luminance of a color.

Assumes sRGB encoding. Based on the formula for relative luminance defined in WCAG 2.0, W3C Recommendation 11 December 2008.

| Return ||
|--------------------------------------------------------------------------------|----------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | a value between 0 (darkest black) and 1 (lightest white) |

### luminance

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun luminance(color: Long): Float
```

Returns the relative luminance of a color.

Based on the formula for relative luminance defined in WCAG 2.0, W3C Recommendation 11 December 2008.

| Return ||
|--------------------------------------------------------------------------------|----------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | A value between 0 (darkest black) and 1 (lightest white) |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If the specified color's color space is unknown or does not use the [RGB](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Model) color model |

### pack

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun pack(): Long
```

Packs this color into a color long. See the documentation of this class for a description of the color long format.

| Return ||
|------------------------------------------------------------------------------|--------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | A color long |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If this color's color space has the id [ColorSpace.MIN_ID](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#MIN_ID:kotlin.Int) or if this color has more than 4 components |

### pack

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun pack(
    red: Float, 
    green: Float, 
    blue: Float
): Long
```

Packs the sRGB color defined by the specified red, green and blue component values into an RGBA color long in the sRGB color space. The alpha component is set to 1.0. See the documentation of this class for a description of the color long format.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `red` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The red component of the sRGB color to create, in \\(\[0..1\]\\) |
| `green` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The green component of the sRGB color to create, in \\(\[0..1\]\\) |
| `blue` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The blue component of the sRGB color to create, in \\(\[0..1\]\\) |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------|--------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | A color long |

### pack

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun pack(
    red: Float, 
    green: Float, 
    blue: Float, 
    alpha: Float
): Long
```

Packs the sRGB color defined by the specified red, green, blue and alpha component values into an RGBA color long in the sRGB color space. See the documentation of this class for a description of the color long format.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `red` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The red component of the sRGB color to create, in \\(\[0..1\]\\) |
| `green` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The green component of the sRGB color to create, in \\(\[0..1\]\\) |
| `blue` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The blue component of the sRGB color to create, in \\(\[0..1\]\\) |
| --- | --- |
| `alpha` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The alpha component of the sRGB color to create, in \\(\[0..1\]\\) |

| Return ||
|------------------------------------------------------------------------------|--------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | A color long |

### pack

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun pack(
    red: Float, 
    green: Float, 
    blue: Float, 
    alpha: Float, 
    colorSpace: ColorSpace
): Long
```

Packs the 3 component color defined by the specified red, green, blue and alpha component values into a color long in the specified color space. See the documentation of this class for a description of the color long format.

The red, green and blue components must be in the range defined by the specified color space. See [ColorSpace.getMinValue(int)](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#getMinValue(kotlin.Int))and [ColorSpace.getMaxValue(int)](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#getMaxValue(kotlin.Int)).

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `red` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The red component of the color to create |
| `green` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The green component of the color to create |
| `blue` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The blue component of the color to create |
| --- | --- |
| `alpha` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The alpha component of the color to create, in \\(\[0..1\]\\) |
| `colorSpace` | [ColorSpace](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace):This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------|--------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | A color long |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If the color space's id is [ColorSpace.MIN_ID](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#MIN_ID:kotlin.Int) or if the color space's color model has more than 3 components |

### pack

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun pack(color: Int): Long
```

Converts the specified ARGB color int to an RGBA color long in the sRGB color space. See the documentation of this class for a description of the color long format.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------|
| `color` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The ARGB color int to convert to an RGBA color long in sRGB |

| Return ||
|------------------------------------------------------------------------------|--------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | A color long |

### parseColor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun parseColor(colorString: String!): Int
```

Parse the color string, and return the corresponding color-int. If the string cannot be parsed, throws an IllegalArgumentException exception. Supported formats are:

<br />

- `RRGGBB`
- `AARRGGBB`

The following names are also accepted:`red`,`blue`,`green`,`black`,`white`,`gray`,`cyan`,`magenta`,`yellow`,`lightgray`,`darkgray`,`grey`,`lightgrey`,`darkgrey`,`aqua`,`fuchsia`,`lime`,`maroon`,`navy`,`olive`,`purple`,`silver`, and`teal`. 

### red

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun red(): Float
```

Returns the value of the red component in the range defined by this color's color space (see [ColorSpace.getMinValue(int)](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#getMinValue(kotlin.Int))and [ColorSpace.getMaxValue(int)](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#getMaxValue(kotlin.Int))).

If this color's color model is not [RGB](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Model), calling this method is equivalent to`getComponent(0)`. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/graphics/Color#alpha()>
- <https://developer.android.com/reference/kotlin/android/graphics/Color#red()>
- <https://developer.android.com/reference/kotlin/android/graphics/Color#getComponents()> 

### red

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun red(color: Int): Int
```

Return the red component of a color int. This is the same as saying (color \>\> 16) \& 0xFF

| Return ||
|----------------------------------------------------------------------------|--------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is between 0 and 255 inclusive |

### red

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun red(color: Long): Float
```

Returns the red component encoded in the specified color long. The range of the returned value depends on the color space associated with the specified color. The color space can be queried by calling [colorSpace(long)](https://developer.android.com/reference/kotlin/android/graphics/Color#colorSpace(kotlin.Long)).

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------|
| `color` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The color long whose red channel to extract |

| Return ||
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | A float value with a range defined by the specified color's color space |

**See Also**

- [#colorSpace(long)](https://developer.android.com/reference/kotlin/android/graphics/Color#colorSpace(kotlin.Long))
- [#green(long)](https://developer.android.com/reference/kotlin/android/graphics/Color#green(kotlin.Long))
- [#blue(long)](https://developer.android.com/reference/kotlin/android/graphics/Color#blue(kotlin.Long))
- [#alpha(long)](https://developer.android.com/reference/kotlin/android/graphics/Color#alpha(kotlin.Long)) 

### rgb

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun rgb(
    red: Float, 
    green: Float, 
    blue: Float
): Int
```

Return a color-int from red, green, blue float components in the range \\(\[0..1\]\\). The alpha component is implicitly 1.0 (fully opaque). If the components are out of range, the returned color is undefined.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------|
| `red` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Red component \\(\[0..1\]\\) of the color |
| `green` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Green component \\(\[0..1\]\\) of the color |
| `blue` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):Blue component \\(\[0..1\]\\) of the color |
| --- | --- |

### rgb

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun rgb(
    red: Int, 
    green: Int, 
    blue: Int
): Int
```

Return a color-int from red, green, blue components. The alpha component is implicitly 255 (fully opaque). These component values should be \\(\[0..255\]\\), but there is no range check performed, so if they are out of range, the returned color is undefined.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `red` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Red component \\(\[0..255\]\\) of the color Value is between 0 and 255 inclusive |
| `green` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Green component \\(\[0..255\]\\) of the color Value is between 0 and 255 inclusive |
| `blue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Blue component \\(\[0..255\]\\) of the color Value is between 0 and 255 inclusive |
| --- | --- |

### toArgb

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toArgb(): Int
```

Converts this color to an ARGB color int. A color int is always in the [sRGB](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named) color space. This implies a color space conversion is applied if needed.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | An ARGB color in the sRGB color space |

### toArgb

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun toArgb(color: Long): Int
```

Converts the specified color long to an ARGB color int. A color int is always in the [sRGB](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named) color space. This implies a color space conversion is applied if needed.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | An ARGB color in the sRGB color space |

| Exceptions ||
|--------------------------------------|--------------------------------------------------|
| `java.lang.IllegalArgumentException` | If the encoded color space is invalid or unknown |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Returns a string representation of the object. This method returns a string equal to the value of: 

```kotlin
"Color(" + r + ", " + g + ", " + b + ", " + a +
          ", " + getColorSpace().getName + ')'
  
```

For instance, the string representation of opaque black in the sRGB color space is equal to the following value: 

```kotlin
Color(0.0, 0.0, 0.0, 1.0, sRGB IEC61966-2.1)
  
```

| Return ||
|----------------------------------------------------------------------------------|------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | A non-null string representation of the object |

### valueOf

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun valueOf(
    r: Float, 
    g: Float, 
    b: Float
): Color
```

Creates a new opaque`Color`in the [sRGB](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named) color space with the specified red, green and blue component values. The component values must be in the range \\(\[0..1\]\\).

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `r` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The red component of the opaque sRGB color to create, in \\(\[0..1\]\\) |
| `g` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The green component of the opaque sRGB color to create, in \\(\[0..1\]\\) |
| `b` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The blue component of the opaque sRGB color to create, in \\(\[0..1\]\\) |
| --- | --- |

| Return ||
|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [Color](https://developer.android.com/reference/kotlin/android/graphics/Color#) | A non-null instance of [Color](https://developer.android.com/reference/kotlin/android/graphics/Color#) |

### valueOf

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun valueOf(
    r: Float, 
    g: Float, 
    b: Float, 
    a: Float
): Color
```

Creates a new`Color`in the [sRGB](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named) color space with the specified red, green, blue and alpha component values. The component values must be in the range \\(\[0..1\]\\).

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `r` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The red component of the sRGB color to create, in \\(\[0..1\]\\) |
| `g` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The green component of the sRGB color to create, in \\(\[0..1\]\\) |
| `b` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The blue component of the sRGB color to create, in \\(\[0..1\]\\) |
| --- | --- |
| `a` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The alpha component of the sRGB color to create, in \\(\[0..1\]\\) |

| Return ||
|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [Color](https://developer.android.com/reference/kotlin/android/graphics/Color#) | A non-null instance of [Color](https://developer.android.com/reference/kotlin/android/graphics/Color#) |

### valueOf

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun valueOf(
    r: Float, 
    g: Float, 
    b: Float, 
    a: Float, 
    colorSpace: ColorSpace
): Color
```

Creates a new`Color`in the specified color space with the specified red, green, blue and alpha component values. The range of the components is defined by [ColorSpace.getMinValue(int)](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#getMinValue(kotlin.Int))and [ColorSpace.getMaxValue(int)](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#getMaxValue(kotlin.Int)). The values passed to this method must be in the proper range.

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `r` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The red component of the color to create |
| `g` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The green component of the color to create |
| `b` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The blue component of the color to create |
| --- | --- |
| `a` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The alpha component of the color to create, in \\(\[0..1\]\\) |
| `colorSpace` | [ColorSpace](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace):The color space of the color to create This value cannot be`null`. |

| Return ||
|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [Color](https://developer.android.com/reference/kotlin/android/graphics/Color#) | A non-null instance of [Color](https://developer.android.com/reference/kotlin/android/graphics/Color#) |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If the specified color space uses a color model with more than 3 components |

### valueOf

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun valueOf(
    components: FloatArray, 
    colorSpace: ColorSpace
): Color
```

Creates a new`Color`in the specified color space with the specified component values. The range of the components is defined by [ColorSpace.getMinValue(int)](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#getMinValue(kotlin.Int))and [ColorSpace.getMaxValue(int)](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#getMaxValue(kotlin.Int)). The values passed to this method must be in the proper range. The alpha component is always in the range \\(\[0..1\]\\).

The length of the array of components must be at least [ColorSpace.getComponentCount()](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#getComponentCount())` + 1`. The component at index [ColorSpace.getComponentCount()](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace#getComponentCount())is always alpha.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `components` | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html):The components of the color to create, with alpha as the last component This value cannot be`null`. |
| `colorSpace` | [ColorSpace](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace):The color space of the color to create This value cannot be`null`. |

| Return ||
|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [Color](https://developer.android.com/reference/kotlin/android/graphics/Color#) | A non-null instance of [Color](https://developer.android.com/reference/kotlin/android/graphics/Color#) |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If the array of components is smaller than required by the color space |

### valueOf

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun valueOf(color: Int): Color
```

Creates a new`Color`instance from an ARGB color int. The resulting color is in the [sRGB](https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named) color space.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------|
| `color` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The ARGB color int to create a`Color`from |

| Return ||
|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [Color](https://developer.android.com/reference/kotlin/android/graphics/Color#) | A non-null instance of [Color](https://developer.android.com/reference/kotlin/android/graphics/Color#) |

### valueOf

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun valueOf(color: Long): Color
```

Creates a new`Color`instance from a color long. The resulting color is in the same color space as the specified color long.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------|
| `color` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The color long to create a`Color`from |

| Return ||
|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [Color](https://developer.android.com/reference/kotlin/android/graphics/Color#) | A non-null instance of [Color](https://developer.android.com/reference/kotlin/android/graphics/Color#) |

| Exceptions ||
|--------------------------------------|--------------------------------------------------|
| `java.lang.IllegalArgumentException` | If the encoded color space is invalid or unknown |
