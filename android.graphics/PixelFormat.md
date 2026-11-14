# PixelFormat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PixelFormat

Kotlin| [Java](PixelFormat.md) 
| --- | --- |

```
open class PixelFormat
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.PixelFormat](PixelFormat.md) |

## Summary

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [A_8](PixelFormat.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [JPEG](PixelFormat.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LA_88](PixelFormat.md) <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [L_8](PixelFormat.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [OPAQUE](PixelFormat.md) System chooses an opaque format (no alpha bits required) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RGBA_1010102](PixelFormat.md) <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RGBA_4444](PixelFormat.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RGBA_5551](PixelFormat.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RGBA_8888](PixelFormat.md) <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RGBA_F16](PixelFormat.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RGBX_8888](PixelFormat.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RGB_332](PixelFormat.md) <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RGB_565](PixelFormat.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RGB_888](PixelFormat.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRANSLUCENT](PixelFormat.md) System chooses a format that supports translucency (many alpha bits) |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRANSPARENT](PixelFormat.md) System chooses a format that supports transparency (at least 1 alpha bit) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UNKNOWN](PixelFormat.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [YCbCr_420_SP](PixelFormat.md) <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [YCbCr_422_I](PixelFormat.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [YCbCr_422_SP](PixelFormat.md) <br /> |

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------|---|
| [PixelFormat](PixelFormat.md))`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [formatHasAlpha](PixelFormat.md))`(`format:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getPixelFormatInfo](PixelFormat.md))`(`format:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `info:` ` [PixelFormat](PixelFormat.md)!`)` <br /> |

| Properties ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [bitsPerPixel](PixelFormat.md) <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [bytesPerPixel](PixelFormat.md) <br /> |

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

**Deprecated:** *use [ImageFormat.JPEG](ImageFormat.md) instead.* 

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

**Deprecated:** *use [ImageFormat.NV21](ImageFormat.md) instead.* 

 Value: 17

### YCbCr_422_I

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val YCbCr_422_I: Int
```

**Deprecated:** *use [ImageFormat.YUY2](ImageFormat.md) instead.* 

 Value: 20

### YCbCr_422_SP

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val YCbCr_422_SP: Int
```

**Deprecated:** *use [ImageFormat.NV16](ImageFormat.md) instead.* 

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
| `format` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.graphics.PixelFormat#RGBA_8888](PixelFormat.md), [android.graphics.PixelFormat#RGBX_8888](PixelFormat.md), [android.graphics.PixelFormat#RGBA_F16](PixelFormat.md), [android.graphics.PixelFormat#RGBA_1010102](PixelFormat.md), [android.graphics.PixelFormat#RGB_888](PixelFormat.md), [android.graphics.PixelFormat#RGB_565](PixelFormat.md), or android.graphics.PixelFormat.R_8 |

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
| `format` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.graphics.PixelFormat#RGBA_8888](PixelFormat.md), [android.graphics.PixelFormat#RGBX_8888](PixelFormat.md), [android.graphics.PixelFormat#RGBA_F16](PixelFormat.md), [android.graphics.PixelFormat#RGBA_1010102](PixelFormat.md), [android.graphics.PixelFormat#RGB_888](PixelFormat.md), [android.graphics.PixelFormat#RGB_565](PixelFormat.md), or android.graphics.PixelFormat.R_8 |

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
