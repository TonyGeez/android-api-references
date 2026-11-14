Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DataSpace

```
class DataSpace
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.hardware.DataSpace](../android/hardware/DataSpace.md) |

DataSpace identifies three components of colors - standard (primaries), transfer and range.

A DataSpace describes how buffer data, such as from an `https://developer.android.com/reference/kotlin/android/media/Image.html#` or a `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer` should be interpreted by both applications and typical hardware.

As buffer information is not guaranteed to be representative of color information, while DataSpace is typically used to describe three aspects of interpreting colors, some DataSpaces may describe other typical interpretations of buffer data such as depth information.

Note that while `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.html#` and `DataSpace` are similar concepts, they are not equivalent. Not all ColorSpaces, such as `https://developer.android.com/reference/kotlin/android/graphics/ColorSpace.Named.html#`, are able to be understood by typical hardware blocks so they cannot be DataSpaces.

### Standard aspect

Defines the chromaticity coordinates of the source primaries in terms of the CIE 1931 definition of x and y specified in ISO 11664-1.

### Transfer aspect

Transfer characteristics are the opto-electronic transfer characteristic at the source as a function of linear optical intensity (luminance).

For digital signals, E corresponds to the recorded value. Normally, the transfer function is applied in RGB space to each of the R, G and B components independently. This may result in color shift that can be minized by applying the transfer function in Lab space only for the L component. Implementation may apply the transfer function in RGB space for all pixel formats if desired.

### Range aspect

Defines the range of values corresponding to the unit range of `0-1`.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_ADOBE_RGB:kotlin.Int` Adobe RGB encoding. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_BT2020:kotlin.Int` ITU-R Recommendation 2020 (BT.2020) Ultra High-definition television. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_BT2020_HLG:kotlin.Int` Hybrid Log Gamma encoding. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_BT2020_PQ:kotlin.Int` Perceptual Quantizer encoding. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_BT601_525:kotlin.Int` ITU-R Recommendation 601 (BT.601) - 525-line Standard-definition television, 525 Lines (NTSC). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_BT601_625:kotlin.Int` ITU-R Recommendation 601 (BT.601) - 625-line Standard-definition television, 625 Lines (PAL). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_BT709:kotlin.Int` ITU-R Recommendation 709 (BT.709) High-definition television. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_DCI_P3:kotlin.Int` SMPTE EG 432-1 and SMPTE RP 431-2 Digital Cinema DCI-P3. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_DEPTH:kotlin.Int` Depth. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_DISPLAY_BT2020:kotlin.Int` Display BT. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_DISPLAY_P3:kotlin.Int` Display P3 encoding. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_DYNAMIC_DEPTH:kotlin.Int` ISO 16684-1:2011(E) Dynamic Depth. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_HEIF:kotlin.Int` High Efficiency Image File Format (HEIF). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_HEIF_ULTRAHDR:kotlin.Int` ISO/IEC 23008-12:2024 High Efficiency Image File Format (HEIF) with embedded HDR gain map |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_JFIF:kotlin.Int` JPEG File Interchange Format (JFIF). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_JPEG_R:kotlin.Int` Ultra HDR JPEG image with embedded HDR gain map following the Ultra HDR specification and starting with Android version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#VANILLA_ICE_CREAM:kotlin.Int` ISO/CD 21496‐1 |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_SCRGB:kotlin.Int` scRGB gamma encoding. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_SCRGB_LINEAR:kotlin.Int` scRGB linear encoding. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_SRGB:kotlin.Int` sRGB gamma encoding. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_SRGB_LINEAR:kotlin.Int` sRGB linear encoding. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_UNKNOWN:kotlin.Int` Default-assumption data space, when not explicitly specified. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#RANGE_EXTENDED:kotlin.Int` Extended range can be used in combination with FP16 to communicate scRGB or with `https://developer.android.com/reference/kotlin/android/view/SurfaceControl.Transaction.html#setExtendedRangeBrightness(android.view.SurfaceControl,%20kotlin.Float,%20kotlin.Float)` to indicate an HDR range. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#RANGE_FULL:kotlin.Int` Full range uses all values for Y, Cb and Cr from `0` to `2^b-1`, where b is the bit depth of the color format. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#RANGE_LIMITED:kotlin.Int` Limited range uses values `16/256*2^b` to `235/256*2^b` for Y, and `1/16*2^b` to `15/16*2^b` for Cb, Cr, R, G and B, where b is the bit depth of the color format. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#RANGE_UNSPECIFIED:kotlin.Int` Range characteristics are unknown or are determined by the application. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#STANDARD_ADOBE_RGB:kotlin.Int` Adobe RGB primaries. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#STANDARD_BT2020:kotlin.Int` Use the unadjusted `KR = 0.2627`, `KB = 0.0593` luminance interpretation for RGB conversion. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#STANDARD_BT2020_CONSTANT_LUMINANCE:kotlin.Int` Use the unadjusted `KR = 0.2627`, `KB = 0.0593` luminance interpretation for RGB conversion using the linear domain. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#STANDARD_BT470M:kotlin.Int` Use the unadjusted `KR = 0.30`, `KB = 0.11` luminance interpretation for RGB conversion. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#STANDARD_BT601_525:kotlin.Int` Use the adjusted `KR = 0.299`, `KB = 0.114` luminance interpretation for RGB conversion from the one purely determined by the primaries to minimize the color shift into RGB space that uses BT. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#STANDARD_BT601_525_UNADJUSTED:kotlin.Int` Use the unadjusted `KR = 0.212`, `KB = 0.087` luminance interpretation for RGB conversion (as in SMPTE 240M). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#STANDARD_BT601_625:kotlin.Int` Use the adjusted `KR = 0.299`, `KB = 0.114` luminance interpretation for RGB conversion from the one purely determined by the primaries to minimize the color shift into RGB space that uses BT. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#STANDARD_BT601_625_UNADJUSTED:kotlin.Int` Use the unadjusted `KR = 0.222`, `KB = 0.071` luminance interpretation for RGB conversion. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#STANDARD_BT709:kotlin.Int` Use the unadjusted `KR = 0.2126`, `KB = 0.0722` luminance interpretation for RGB conversion. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#STANDARD_DCI_P3:kotlin.Int` SMPTE EG 432-1 and SMPTE RP 431-2. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#STANDARD_FILM:kotlin.Int` Use the unadjusted `KR = 0.254`, `KB = 0.068` luminance interpretation for RGB conversion. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#STANDARD_UNSPECIFIED:kotlin.Int` Chromacity coordinates are unknown or are determined by the application. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#TRANSFER_GAMMA2_2:kotlin.Int` Display gamma 2. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#TRANSFER_GAMMA2_6:kotlin.Int` Display gamma 2. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#TRANSFER_GAMMA2_8:kotlin.Int` Display gamma 2. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#TRANSFER_HLG:kotlin.Int` ARIB STD-B67 Hybrid Log Gamma. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#TRANSFER_LINEAR:kotlin.Int` Linear transfer. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#TRANSFER_SMPTE_170M:kotlin.Int` SMPTE 170M transfer. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#TRANSFER_SRGB:kotlin.Int` sRGB transfer. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#TRANSFER_ST2084:kotlin.Int` SMPTE ST 2084 (Dolby Perceptual Quantizer). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#TRANSFER_UNSPECIFIED:kotlin.Int` Transfer characteristics are unknown or are determined by the application. |

| Public methods ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#getRange(kotlin.Int)(dataSpace: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Unpack the range field value from the packed dataSpace value |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#getStandard(kotlin.Int)(dataSpace: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Unpack the standard field value from the packed dataSpace value. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#getTransfer(kotlin.Int)(dataSpace: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Unpack the transfer field value from the packed dataSpace value |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#pack(kotlin.Int,%20kotlin.Int,%20kotlin.Int)(standard: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, transfer: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, range: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Pack the dataSpace value using standard, transfer and range field value. |

## Constants

### DATASPACE_ADOBE_RGB

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATASPACE_ADOBE_RGB: Int
```

Adobe RGB encoding.

Composed of the following -

```kotlin
Primaries: STANDARD_ADOBE_RGB
    Transfer: TRANSFER_GAMMA2_2
    Range: RANGE_FULL
```
Note: Application is responsible for gamma encoding the data.

 Value: 151715840

### DATASPACE_BT2020

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATASPACE_BT2020: Int
```

ITU-R Recommendation 2020 (BT.2020) Ultra High-definition television.

Composed of the following -

```kotlin
Primaries: STANDARD_BT2020
    Transfer: TRANSFER_SMPTE_170M
    Range: RANGE_FULL
```

 Value: 147193856

### DATASPACE_BT2020_HLG

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATASPACE_BT2020_HLG: Int
```

Hybrid Log Gamma encoding.

Composed of the following -

```kotlin
Primaries: STANDARD_BT2020
    Transfer: TRANSFER_HLG
    Range: RANGE_FULL
```

 Value: 168165376

### DATASPACE_BT2020_PQ

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATASPACE_BT2020_PQ: Int
```

Perceptual Quantizer encoding.

Composed of the following -

```kotlin
Primaries: STANDARD_BT2020
    Transfer: TRANSFER_ST2084
    Range: RANGE_FULL
```

 Value: 163971072

### DATASPACE_BT601_525

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATASPACE_BT601_525: Int
```

ITU-R Recommendation 601 (BT.601) - 525-line Standard-definition television, 525 Lines (NTSC).

Composed of the following -

```kotlin
Primaries: STANDARD_BT601_525
    Transfer: TRANSFER_SMPTE_170M
    Range: RANGE_LIMITED
```

 Value: 281280512

### DATASPACE_BT601_625

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATASPACE_BT601_625: Int
```

ITU-R Recommendation 601 (BT.601) - 625-line Standard-definition television, 625 Lines (PAL).

Composed of the following -

```kotlin
Primaries: STANDARD_BT601_625
    Transfer: TRANSFER_SMPTE_170M
    Range: RANGE_LIMITED
```

 Value: 281149440

### DATASPACE_BT709

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATASPACE_BT709: Int
```

ITU-R Recommendation 709 (BT.709) High-definition television.

Composed of the following -

```kotlin
Primaries: STANDARD_BT709
    Transfer: TRANSFER_SMPTE_170M
    Range: RANGE_LIMITED
```

 Value: 281083904

### DATASPACE_DCI_P3

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATASPACE_DCI_P3: Int
```

SMPTE EG 432-1 and SMPTE RP 431-2 Digital Cinema DCI-P3.

Composed of the following -

```kotlin
Primaries: STANDARD_DCI_P3
    Transfer: TRANSFER_GAMMA2_6
    Range: RANGE_FULL
```
Note: Application is responsible for gamma encoding the data as a 2.6 gamma encoding is not supported in HW.

 Value: 155844608

### DATASPACE_DEPTH

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATASPACE_DEPTH: Int
```

Depth. This value is valid with formats HAL_PIXEL_FORMAT_Y16 and HAL_PIXEL_FORMAT_BLOB.

 Value: 4096

### DATASPACE_DISPLAY_BT2020

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATASPACE_DISPLAY_BT2020: Int
```

Display BT. 2020 encoding.

Composed of the following -

```kotlin
Primaries: STANDARD_BT2020
    Transfer: TRANSFER_SRGB
    Range: RANGE_FULL
```

 Value: 142999552

### DATASPACE_DISPLAY_P3

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATASPACE_DISPLAY_P3: Int
```

Display P3 encoding.

Composed of the following -

```kotlin
Primaries: STANDARD_DCI_P3
    Transfer: TRANSFER_SRGB
    Range: RANGE_FULL
```

 Value: 143261696

### DATASPACE_DYNAMIC_DEPTH

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATASPACE_DYNAMIC_DEPTH: Int
```

ISO 16684-1:2011(E) Dynamic Depth. Embedded depth metadata following the dynamic depth specification.

 Value: 4098

### DATASPACE_HEIF

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATASPACE_HEIF: Int
```

High Efficiency Image File Format (HEIF).

This value is valid with `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer#BLOB:kotlin.Int` format. The combination is an HEIC image encoded by HEIC or HEVC encoder according to ISO/IEC 23008-12.

 Value: 4100

### DATASPACE_HEIF_ULTRAHDR

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATASPACE_HEIF_ULTRAHDR: Int
```

ISO/IEC 23008-12:2024 High Efficiency Image File Format (HEIF) with embedded HDR gain map

This value is valid with formats:

- HAL_PIXEL_FORMAT_BLOB: A HEIC image encoded by HEVC encoder according to ISO/IEC 23008-12:2024 that includes an HDR gain map and metadata according to ISO/CD 21496‐1.

 Value: 4102

### DATASPACE_JFIF

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATASPACE_JFIF: Int
```

JPEG File Interchange Format (JFIF).

Composed of the following -

```kotlin
Primaries: STANDARD_BT601_625
    Transfer: TRANSFER_SMPTE_170M
    Range: RANGE_FULL
```
Same model as BT.601-625, but all values (Y, Cb, Cr) range from `0` to `255`

 Value: 146931712

### DATASPACE_JPEG_R

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATASPACE_JPEG_R: Int
```

Ultra HDR JPEG image with embedded HDR gain map following the Ultra HDR specification and starting with Android version `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#VANILLA_ICE_CREAM:kotlin.Int` ISO/CD 21496‐1

This value is valid with formats:

- HAL_PIXEL_FORMAT_BLOB: JPEG image encoded by Jpeg/R encoder according to ISO/CD 21496‐1

The image contains a standard SDR JPEG and a gain map. Ultra HDR decoders can use the gain map to boost the brightness of the rendered image.

 Value: 4101

### DATASPACE_SCRGB

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATASPACE_SCRGB: Int
```

scRGB gamma encoding.

Composed of the following -

```kotlin
Primaries: STANDARD_BT709
    Transfer: TRANSFER_SRGB
    Range: RANGE_EXTENDED
```
The values are floating point. A pixel value of 1.0, 1.0, 1.0 corresponds to sRGB white (D65) at 80 nits. Values beyond the range \[0.0 - 1.0\] would correspond to other colors spaces and/or HDR content.

 Value: 411107328

### DATASPACE_SCRGB_LINEAR

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATASPACE_SCRGB_LINEAR: Int
```

scRGB linear encoding.

Composed of the following -

```kotlin
Primaries: STANDARD_BT709
    Transfer: TRANSFER_LINEAR
    Range: RANGE_EXTENDED
```
The values are floating point. A pixel value of 1.0, 1.0, 1.0 corresponds to sRGB white (D65) at 80 nits. Values beyond the range \[0.0 - 1.0\] would correspond to other colors spaces and/or HDR content.

 Value: 406913024

### DATASPACE_SRGB

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATASPACE_SRGB: Int
```

sRGB gamma encoding.

Composed of the following -

```kotlin
Primaries: STANDARD_BT709
    Transfer: TRANSFER_SRGB
    Range: RANGE_FULL
```
When written, the inverse transformation is performed. The alpha component, if present, is always stored in linear space and is left unmodified when read or written.

 Value: 142671872

### DATASPACE_SRGB_LINEAR

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATASPACE_SRGB_LINEAR: Int
```

sRGB linear encoding.

Composed of the following -

```kotlin
Primaries: STANDARD_BT709
    Transfer: TRANSFER_LINEAR
    Range: RANGE_FULL
```
The values are encoded using the full range (\[0,255\] for 8-bit) for all components.

 Value: 138477568

### DATASPACE_UNKNOWN

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATASPACE_UNKNOWN: Int
```

Default-assumption data space, when not explicitly specified.

It is safest to assume a buffer is an image with sRGB primaries and encoding ranges, but the consumer and/or the producer of the data may simply be using defaults. No automatic gamma transform should be expected, except for a possible display gamma transform when drawn to a screen.

 Value: 0

### RANGE_EXTENDED

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RANGE_EXTENDED: Int
```

Extended range can be used in combination with FP16 to communicate scRGB or with `https://developer.android.com/reference/kotlin/android/view/SurfaceControl.Transaction.html#setExtendedRangeBrightness(android.view.SurfaceControl,%20kotlin.Float,%20kotlin.Float)` to indicate an HDR range.

When used with floating point pixel formats and #STANDARD_BT709 then \[0.0 - 1.0\] is the standard sRGB space and values outside the range \[0.0 - 1.0\] can encode color outside the sRGB gamut. \[-0.5, 7.5\] is the standard scRGB range. Used to blend/merge multiple dataspaces on a single display.

As of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int` this may be combined with `https://developer.android.com/reference/kotlin/android/view/SurfaceControl.Transaction.html#setExtendedRangeBrightness(android.view.SurfaceControl,%20kotlin.Float,%20kotlin.Float)` and other formats such as `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer#RGBA_8888:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/hardware/HardwareBuffer#RGBA_1010102:kotlin.Int` to communicate a variable HDR brightness range

 Value: 402653184

### RANGE_FULL

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RANGE_FULL: Int
```

Full range uses all values for Y, Cb and Cr from `0` to `2^b-1`, where b is the bit depth of the color format.

 Value: 134217728

### RANGE_LIMITED

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RANGE_LIMITED: Int
```

Limited range uses values `16/256*2^b` to `235/256*2^b` for Y, and `1/16*2^b` to `15/16*2^b` for Cb, Cr, R, G and B, where b is the bit depth of the color format.

E.g. For 8-bit-depth formats: Luma (Y) samples should range from 16 to 235, inclusive Chroma (Cb, Cr) samples should range from 16 to 240, inclusive For 10-bit-depth formats: Luma (Y) samples should range from 64 to 940, inclusive Chroma (Cb, Cr) samples should range from 64 to 960, inclusive.

 Value: 268435456

### RANGE_UNSPECIFIED

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RANGE_UNSPECIFIED: Int
```

Range characteristics are unknown or are determined by the application.

 Value: 0

### STANDARD_ADOBE_RGB

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STANDARD_ADOBE_RGB: Int
```

Adobe RGB primaries.

```kotlin
Primaries:       x       y
   green           0.210   0.710
   blue            0.150   0.060
   red             0.640   0.330
   white (D65)     0.3127  0.3290 
```

<br />

 Value: 720896

### STANDARD_BT2020

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STANDARD_BT2020: Int
```

Use the unadjusted `KR = 0.2627`, `KB = 0.0593` luminance interpretation for RGB conversion.

```kotlin
Primaries:       x       y
   green           0.170   0.797
   blue            0.131   0.046
   red             0.708   0.292
   white (D65)     0.3127  0.3290 
```

<br />

 Value: 393216

### STANDARD_BT2020_CONSTANT_LUMINANCE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STANDARD_BT2020_CONSTANT_LUMINANCE: Int
```

Use the unadjusted `KR = 0.2627`, `KB = 0.0593` luminance interpretation for RGB conversion using the linear domain.

```kotlin
Primaries:       x       y
   green           0.170   0.797
   blue            0.131   0.046
   red             0.708   0.292
   white (D65)     0.3127  0.3290 
```

<br />

 Value: 458752

### STANDARD_BT470M

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STANDARD_BT470M: Int
```

Use the unadjusted `KR = 0.30`, `KB = 0.11` luminance interpretation for RGB conversion.

```kotlin
Primaries:       x      y
   green           0.21   0.71
   blue            0.14   0.08
   red             0.67   0.33
   white (C)       0.310  0.316 
```

<br />

 Value: 524288

### STANDARD_BT601_525

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STANDARD_BT601_525: Int
```

Use the adjusted `KR = 0.299`, `KB = 0.114` luminance interpretation for RGB conversion from the one purely determined by the primaries to minimize the color shift into RGB space that uses BT.709 primaries.

```kotlin
Primaries:       x       y
   green           0.310   0.595
   blue            0.155   0.070
   red             0.630   0.340
   white (D65)     0.3127  0.3290 
```

<br />

 Value: 262144

### STANDARD_BT601_525_UNADJUSTED

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STANDARD_BT601_525_UNADJUSTED: Int
```

Use the unadjusted `KR = 0.212`, `KB = 0.087` luminance interpretation for RGB conversion (as in SMPTE 240M).

```kotlin
Primaries:       x       y
   green           0.310   0.595
   blue            0.155   0.070
   red             0.630   0.340
   white (D65)     0.3127  0.3290 
```

<br />

 Value: 327680

### STANDARD_BT601_625

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STANDARD_BT601_625: Int
```

Use the adjusted `KR = 0.299`, `KB = 0.114` luminance interpretation for RGB conversion from the one purely determined by the primaries to minimize the color shift into RGB space that uses BT.709 primaries.

```kotlin
Primaries:       x       y
   green           0.290   0.600
   blue            0.150   0.060
   red             0.640   0.330
   white (D65)     0.3127  0.3290 
```

<br />

 Value: 131072

### STANDARD_BT601_625_UNADJUSTED

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STANDARD_BT601_625_UNADJUSTED: Int
```

Use the unadjusted `KR = 0.222`, `KB = 0.071` luminance interpretation for RGB conversion.

```kotlin
Primaries:       x       y
   green           0.290   0.600
   blue            0.150   0.060
   red             0.640   0.330
   white (D65)     0.3127  0.3290 
```

<br />

 Value: 196608

### STANDARD_BT709

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STANDARD_BT709: Int
```

Use the unadjusted `KR = 0.2126`, `KB = 0.0722` luminance interpretation for RGB conversion.

```kotlin
Primaries:       x       y
   green           0.300   0.600
   blue            0.150   0.060
   red             0.640   0.330
   white (D65)     0.3127  0.3290 
```

<br />

 Value: 65536

### STANDARD_DCI_P3

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STANDARD_DCI_P3: Int
```

SMPTE EG 432-1 and SMPTE RP 431-2.

```kotlin
Primaries:       x       y
   green           0.265   0.690
   blue            0.150   0.060
   red             0.680   0.320
   white (D65)     0.3127  0.3290 
```

<br />

 Value: 655360

### STANDARD_FILM

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STANDARD_FILM: Int
```

Use the unadjusted `KR = 0.254`, `KB = 0.068` luminance interpretation for RGB conversion.

```kotlin
Primaries:       x       y
   green           0.243   0.692
   blue            0.145   0.049
   red             0.681   0.319
   white (C)       0.310   0.316 
```

<br />

 Value: 589824

### STANDARD_UNSPECIFIED

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STANDARD_UNSPECIFIED: Int
```

Chromacity coordinates are unknown or are determined by the application.

 Value: 0

### TRANSFER_GAMMA2_2

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TRANSFER_GAMMA2_2: Int
```

Display gamma 2.2.

```kotlin
<code>Transfer characteristic curve:
  E = L ^ (1/2.2)
      L - luminance of image 0 &lt;= L &lt;= 1 for conventional colorimetry
      E - corresponding electrical signal</code>
```

<br />

 Value: 16777216

### TRANSFER_GAMMA2_6

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TRANSFER_GAMMA2_6: Int
```

Display gamma 2.6.

```kotlin
<code>Transfer characteristic curve:
  E = L ^ (1/2.6)
      L - luminance of image 0 &lt;= L &lt;= 1 for conventional colorimetry
      E - corresponding electrical signal</code>
```

<br />

 Value: 20971520

### TRANSFER_GAMMA2_8

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TRANSFER_GAMMA2_8: Int
```

Display gamma 2.8.

```kotlin
<code>Transfer characteristic curve:
  E = L ^ (1/2.8)
      L - luminance of image 0 &lt;= L &lt;= 1 for conventional colorimetry
      E - corresponding electrical signal</code>
```

<br />

 Value: 25165824

### TRANSFER_HLG

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TRANSFER_HLG: Int
```

ARIB STD-B67 Hybrid Log Gamma.

```kotlin
<code>Transfer characteristic curve:
  E = r * L^0.5                 for 0 &lt;= L &lt;= 1
    = a * ln(L - b) + c         for 1 &lt; L
  a = 0.17883277
  b = 0.28466892
  c = 0.55991073
  r = 0.5
      L - luminance of image 0 &lt;= L for HDR colorimetry. L = 1 corresponds
          to reference white level of 100 cd/m2
      E - corresponding electrical signal</code>
```

<br />

 Value: 33554432

### TRANSFER_LINEAR

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TRANSFER_LINEAR: Int
```

Linear transfer.

```kotlin
<code>Transfer characteristic curve:
   E = L
       L - luminance of image 0 &lt;= L &lt;= 1 for conventional colorimetry
       E - corresponding electrical signal</code>
```

<br />

 Value: 4194304

### TRANSFER_SMPTE_170M

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TRANSFER_SMPTE_170M: Int
```

SMPTE 170M transfer.

```kotlin
<code>Transfer characteristic curve:
  E = 1.099 * L ^ 0.45 - 0.099  for 0.018 &lt;= L &lt;= 1
    = 4.500 * L                 for 0 &lt;= L &lt; 0.018
      L - luminance of image 0 &lt;= L &lt;= 1 for conventional colorimetry
      E - corresponding electrical signal</code>
```
Use for YCbCr formats.

<br />

 Value: 12582912

### TRANSFER_SRGB

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TRANSFER_SRGB: Int
```

sRGB transfer.

```kotlin
<code>Transfer characteristic curve:
  E = 1.055 * L^(1/2.4) - 0.055  for 0.0031308 &lt;= L &lt;= 1
    = 12.92 * L                  for 0 &lt;= L &lt; 0.0031308
      L - luminance of image 0 &lt;= L &lt;= 1 for conventional colorimetry
      E - corresponding electrical signal</code>
```
Use for RGB formats.

<br />

 Value: 8388608

### TRANSFER_ST2084

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TRANSFER_ST2084: Int
```

SMPTE ST 2084 (Dolby Perceptual Quantizer).

```kotlin
<code>Transfer characteristic curve:
  E = ((c1 + c2 * L^n) / (1 + c3 * L^n)) ^ m
  c1 = c3 - c2 + 1 = 3424 / 4096 = 0.8359375
  c2 = 32 * 2413 / 4096 = 18.8515625
  c3 = 32 * 2392 / 4096 = 18.6875
  m = 128 * 2523 / 4096 = 78.84375
  n = 0.25 * 2610 / 4096 = 0.1593017578125
      L - luminance of image 0 &lt;= L &lt;= 1 for HDR colorimetry.
          L = 1 corresponds to 10000 cd/m2
      E - corresponding electrical signal</code>
```

<br />

 Value: 29360128

### TRANSFER_UNSPECIFIED

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TRANSFER_UNSPECIFIED: Int
```

Transfer characteristics are unknown or are determined by the application.

 Value: 0

## Public methods

### getRange

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getRange(dataSpace: Int): Int
```

Unpack the range field value from the packed dataSpace value

| Parameters ||
|---|---|
| `dataSpace` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The packed dataspace value. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_SCRGB_LINEAR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_SRGB:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_SCRGB:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_DISPLAY_P3:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_BT2020_HLG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_BT2020_PQ:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_ADOBE_RGB:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_JFIF:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_BT601_625:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_BT601_525:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_BT2020:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_BT709:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_DCI_P3:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_SRGB_LINEAR:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The range aspect. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#RANGE_UNSPECIFIED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#RANGE_FULL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#RANGE_LIMITED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#RANGE_EXTENDED:kotlin.Int` |

### getStandard

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getStandard(dataSpace: Int): Int
```

Unpack the standard field value from the packed dataSpace value.

| Parameters ||
|---|---|
| `dataSpace` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The packed dataspace value. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_SCRGB_LINEAR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_SRGB:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_SCRGB:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_DISPLAY_P3:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_BT2020_HLG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_BT2020_PQ:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_ADOBE_RGB:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_JFIF:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_BT601_625:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_BT601_525:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_BT2020:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_BT709:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_DCI_P3:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_SRGB_LINEAR:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The standard aspect. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#STANDARD_UNSPECIFIED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#STANDARD_BT709:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#STANDARD_BT601_625:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#STANDARD_BT601_625_UNADJUSTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#STANDARD_BT601_525:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#STANDARD_BT601_525_UNADJUSTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#STANDARD_BT2020:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#STANDARD_BT2020_CONSTANT_LUMINANCE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#STANDARD_BT470M:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#STANDARD_FILM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#STANDARD_DCI_P3:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#STANDARD_ADOBE_RGB:kotlin.Int` |

### getTransfer

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getTransfer(dataSpace: Int): Int
```

Unpack the transfer field value from the packed dataSpace value

| Parameters ||
|---|---|
| `dataSpace` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The packed dataspace value. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_SCRGB_LINEAR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_SRGB:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_SCRGB:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_DISPLAY_P3:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_BT2020_HLG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_BT2020_PQ:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_ADOBE_RGB:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_JFIF:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_BT601_625:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_BT601_525:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_BT2020:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_BT709:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_DCI_P3:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_SRGB_LINEAR:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The transfer aspect. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#TRANSFER_UNSPECIFIED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#TRANSFER_LINEAR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#TRANSFER_SRGB:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#TRANSFER_SMPTE_170M:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#TRANSFER_GAMMA2_2:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#TRANSFER_GAMMA2_6:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#TRANSFER_GAMMA2_8:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#TRANSFER_ST2084:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#TRANSFER_HLG:kotlin.Int` |

### pack

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun pack(
    standard: Int, 
    transfer: Int, 
    range: Int
): Int
```

Pack the dataSpace value using standard, transfer and range field value. Field values should be in the correct bits place.

| Parameters ||
|---|---|
| `standard` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Chromaticity coordinates of source primaries. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#STANDARD_UNSPECIFIED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#STANDARD_BT709:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#STANDARD_BT601_625:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#STANDARD_BT601_625_UNADJUSTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#STANDARD_BT601_525:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#STANDARD_BT601_525_UNADJUSTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#STANDARD_BT2020:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#STANDARD_BT2020_CONSTANT_LUMINANCE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#STANDARD_BT470M:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#STANDARD_FILM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#STANDARD_DCI_P3:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#STANDARD_ADOBE_RGB:kotlin.Int` |
| `transfer` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Opto-electronic transfer characteristic at the source. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#TRANSFER_UNSPECIFIED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#TRANSFER_LINEAR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#TRANSFER_SRGB:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#TRANSFER_SMPTE_170M:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#TRANSFER_GAMMA2_2:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#TRANSFER_GAMMA2_6:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#TRANSFER_GAMMA2_8:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#TRANSFER_ST2084:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#TRANSFER_HLG:kotlin.Int` |
| `range` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The range of values. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#RANGE_UNSPECIFIED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#RANGE_FULL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#RANGE_LIMITED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#RANGE_EXTENDED:kotlin.Int` |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The int dataspace packed by standard, transfer and range value. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_SCRGB_LINEAR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_SRGB:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_SCRGB:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_DISPLAY_P3:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_BT2020_HLG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_BT2020_PQ:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_ADOBE_RGB:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_JFIF:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_BT601_625:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_BT601_525:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_BT2020:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_BT709:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_DCI_P3:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/hardware/DataSpace#DATASPACE_SRGB_LINEAR:kotlin.Int` |
