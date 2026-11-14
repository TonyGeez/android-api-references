# PixelFormat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PixelFormat

Kotlin| [Java](https://developer.android.com/reference/android/graphics/PixelFormat "View this page in Java") 

```
open class PixelFormat
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.graphics.PixelFormat](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat#) |

## Summary

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [A_8](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat#A_8:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [JPEG](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat#JPEG:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LA_88](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat#LA_88:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [L_8](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat#L_8:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [OPAQUE](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat#OPAQUE:kotlin.Int) System chooses an opaque format (no alpha bits required) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RGBA_1010102](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat#RGBA_1010102:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RGBA_4444](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat#RGBA_4444:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RGBA_5551](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat#RGBA_5551:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RGBA_8888](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat#RGBA_8888:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RGBA_F16](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat#RGBA_F16:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RGBX_8888](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat#RGBX_8888:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RGB_332](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat#RGB_332:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RGB_565](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat#RGB_565:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RGB_888](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat#RGB_888:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRANSLUCENT](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat#TRANSLUCENT:kotlin.Int) System chooses a format that supports translucency (many alpha bits) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRANSPARENT](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat#TRANSPARENT:kotlin.Int) System chooses a format that supports transparency (at least 1 alpha bit) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UNKNOWN](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat#UNKNOWN:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [YCbCr_420_SP](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat#YCbCr_420_SP:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [YCbCr_422_I](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat#YCbCr_422_I:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [YCbCr_422_SP](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat#YCbCr_422_SP:kotlin.Int) <br /> |

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------|---|
| [PixelFormat](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat#PixelFormat())`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [formatHasAlpha](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat#formatHasAlpha(kotlin.Int))`(`format:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getPixelFormatInfo](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat#getPixelFormatInfo(kotlin.Int,%20android.graphics.PixelFormat))`(`format:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `info:` ` [PixelFormat](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat#)!`)` <br /> |

| Properties ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [bitsPerPixel](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat#bitsPerPixel:kotlin.Int) <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [bytesPerPixel](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat#bytesPerPixel:kotlin.Int) <br /> |

## Constants

### A_8

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val A_8: Int
```

**Deprecated:** *Deprecated in Java.* 

 Value: 8

### JPEG

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val JPEG: Int
```

**Deprecated:** *use [ImageFormat.JPEG](https://developer.android.com/reference/kotlin/android/graphics/ImageFormat#JPEG:kotlin.Int) instead.* 

 Value: 256

### LA_88

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LA_88: Int
```

**Deprecated:** *Deprecated in Java.* 

 Value: 10

### L_8

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val L_8: Int
```

**Deprecated:** *Deprecated in Java.* 

 Value: 9

### OPAQUE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OPAQUE: Int
```

System chooses an opaque format (no alpha bits required) 

 Value: -1

### RGBA_1010102

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RGBA_1010102: Int
```  

 Value: 43

### RGBA_4444

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RGBA_4444: Int
```

**Deprecated:** *Deprecated in Java.* 

 Value: 7

### RGBA_5551

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RGBA_5551: Int
```

**Deprecated:** *Deprecated in Java.* 

 Value: 6

### RGBA_8888

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RGBA_8888: Int
```  

 Value: 1

### RGBA_F16

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RGBA_F16: Int
```  

 Value: 22

### RGBX_8888

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RGBX_8888: Int
```  

 Value: 2

### RGB_332

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RGB_332: Int
```

**Deprecated:** *Deprecated in Java.* 

 Value: 11

### RGB_565

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RGB_565: Int
```  

 Value: 4

### RGB_888

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RGB_888: Int
```  

 Value: 3

### TRANSLUCENT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TRANSLUCENT: Int
```

System chooses a format that supports translucency (many alpha bits) 

 Value: -3

### TRANSPARENT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TRANSPARENT: Int
```

System chooses a format that supports transparency (at least 1 alpha bit) 

 Value: -2

### UNKNOWN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UNKNOWN: Int
```  

 Value: 0

### YCbCr_420_SP

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val YCbCr_420_SP: Int
```

**Deprecated:** *use [ImageFormat.NV21](https://developer.android.com/reference/kotlin/android/graphics/ImageFormat#NV21:kotlin.Int) instead.* 

 Value: 17

### YCbCr_422_I

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val YCbCr_422_I: Int
```

**Deprecated:** *use [ImageFormat.YUY2](https://developer.android.com/reference/kotlin/android/graphics/ImageFormat#YUY2:kotlin.Int) instead.* 

 Value: 20

### YCbCr_422_SP

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val YCbCr_422_SP: Int
```

**Deprecated:** *use [ImageFormat.NV16](https://developer.android.com/reference/kotlin/android/graphics/ImageFormat#NV16:kotlin.Int) instead.* 

 Value: 16

## Public constructors

### PixelFormat

```
PixelFormat()
```

## Public methods

### formatHasAlpha

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun formatHasAlpha(format: Int): Boolean
```

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `format` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.graphics.PixelFormat#RGBA_8888](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat#RGBA_8888:kotlin.Int), [android.graphics.PixelFormat#RGBX_8888](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat#RGBX_8888:kotlin.Int), [android.graphics.PixelFormat#RGBA_F16](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat#RGBA_F16:kotlin.Int), [android.graphics.PixelFormat#RGBA_1010102](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat#RGBA_1010102:kotlin.Int), [android.graphics.PixelFormat#RGB_888](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat#RGB_888:kotlin.Int), [android.graphics.PixelFormat#RGB_565](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat#RGB_565:kotlin.Int), or android.graphics.PixelFormat.R_8 |

### getPixelFormatInfo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getPixelFormatInfo(
    format: Int, 
    info: PixelFormat!
): Unit
```

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `format` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.graphics.PixelFormat#RGBA_8888](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat#RGBA_8888:kotlin.Int), [android.graphics.PixelFormat#RGBX_8888](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat#RGBX_8888:kotlin.Int), [android.graphics.PixelFormat#RGBA_F16](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat#RGBA_F16:kotlin.Int), [android.graphics.PixelFormat#RGBA_1010102](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat#RGBA_1010102:kotlin.Int), [android.graphics.PixelFormat#RGB_888](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat#RGB_888:kotlin.Int), [android.graphics.PixelFormat#RGB_565](https://developer.android.com/reference/kotlin/android/graphics/PixelFormat#RGB_565:kotlin.Int), or android.graphics.PixelFormat.R_8 |

## Properties

### bitsPerPixel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var bitsPerPixel: Int
```  

### bytesPerPixel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var bytesPerPixel: Int
```
