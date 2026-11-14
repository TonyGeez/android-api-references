# EffectFactory

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EffectFactory

Kotlin| [Java](EffectFactory.md) 
| --- | --- |

```
open class EffectFactory
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.effect.EffectFactory](EffectFactory.md) |

The EffectFactory class defines the list of available Effects, and provides functionality to inspect and instantiate them. Some effects may not be available on all platforms, so before creating a certain effect, the application should confirm that the effect is supported on this platform by calling [isEffectSupported(java.lang.String)](EffectFactory.md)).

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EFFECT_AUTOFIX](EffectFactory.md) Attempts to auto-fix the image based on histogram equalization. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EFFECT_BACKDROPPER](EffectFactory.md) Replaces the background of the input frames with frames from a selected video. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EFFECT_BITMAPOVERLAY](EffectFactory.md) Overlays a bitmap (with premultiplied alpha channel) onto the input image. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EFFECT_BLACKWHITE](EffectFactory.md) Adjusts the range of minimal and maximal color pixel intensities. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EFFECT_BRIGHTNESS](EffectFactory.md) Adjusts the brightness of the image. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EFFECT_CONTRAST](EffectFactory.md) Adjusts the contrast of the image. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EFFECT_CROP](EffectFactory.md) Crops an upright rectangular area from the image. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EFFECT_CROSSPROCESS](EffectFactory.md) Applies a cross process effect on image, in which the red and green channels are enhanced while the blue channel is restricted. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EFFECT_DOCUMENTARY](EffectFactory.md) Applies black and white documentary style effect on image. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EFFECT_DUOTONE](EffectFactory.md) Representation of photo using only two color tones. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EFFECT_FILLLIGHT](EffectFactory.md) Applies back-light filling to the image. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EFFECT_FISHEYE](EffectFactory.md) Applies a fisheye lens distortion to the image. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EFFECT_FLIP](EffectFactory.md) Flips image vertically and/or horizontally. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EFFECT_GRAIN](EffectFactory.md) Applies film grain effect to image. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EFFECT_GRAYSCALE](EffectFactory.md) Converts image to grayscale. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EFFECT_LOMOISH](EffectFactory.md) Applies lomo-camera style effect to image. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EFFECT_NEGATIVE](EffectFactory.md) Inverts the image colors. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EFFECT_POSTERIZE](EffectFactory.md) Applies posterization effect to image. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EFFECT_REDEYE](EffectFactory.md) Removes red eyes on specified region. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EFFECT_ROTATE](EffectFactory.md) Rotates the image. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EFFECT_SATURATE](EffectFactory.md) Adjusts color saturation of image. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EFFECT_SEPIA](EffectFactory.md) Converts image to sepia tone. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EFFECT_SHARPEN](EffectFactory.md) Sharpens the image. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EFFECT_STRAIGHTEN](EffectFactory.md) Rotates the image according to the specified angle, and crops the image so that no non-image portions are visible. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EFFECT_TEMPERATURE](EffectFactory.md) Adjusts color temperature of the image. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EFFECT_TINT](EffectFactory.md) Tints the photo with specified color. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EFFECT_VIGNETTE](EffectFactory.md) Adds a vignette effect to image, i. |
| --- | --- |

| Public methods ||
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Effect](Effect.md)! | [createEffect](EffectFactory.md))`(`effectName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Instantiate a new effect with the given effect name. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEffectSupported](EffectFactory.md))`(`effectName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Check if an effect is supported on this platform. |

## Constants

### EFFECT_AUTOFIX

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EFFECT_AUTOFIX: String
```

Attempts to auto-fix the image based on histogram equalization.

Available parameters:

| Parameter name | Meaning | Valid values |
| --- | --- | --- |
| `scale` | The scale of the adjustment. | Float, between 0 and 1. Zero means no adjustment, while 1 indicates the maximum amount of adjustment. |

 Value: "android.media.effect.effects.AutoFixEffect"

### EFFECT_BACKDROPPER

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EFFECT_BACKDROPPER: String
```

Replaces the background of the input frames with frames from a selected video. Requires an initial learning period with only the background visible before the effect becomes active. The effect will wait until it does not see any motion in the scene before learning the background and starting the effect.

Available parameters:

| Parameter name | Meaning | Valid values |
| --- | --- | --- |
| `source` | A URI for the background video to use. This parameter must be supplied before calling apply() for the first time. | String, such as from [Uri.toString()](../android.net/Uri.md)) |

If the update listener is set for this effect using [Effect.setUpdateListener](Effect.md)), it will be called when the effect has finished learning the background, with a null value for the info parameter. 

 Value: "android.media.effect.effects.BackDropperEffect"

### EFFECT_BITMAPOVERLAY

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EFFECT_BITMAPOVERLAY: String
```

Overlays a bitmap (with premultiplied alpha channel) onto the input image. The bitmap is stretched to fit the input image.

Available parameters:

| Parameter name | Meaning | Valid values |
| --- | --- | --- |
| `bitmap` | The overlay bitmap. | A non-null Bitmap instance. |

 Value: "android.media.effect.effects.BitmapOverlayEffect"

### EFFECT_BLACKWHITE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EFFECT_BLACKWHITE: String
```

Adjusts the range of minimal and maximal color pixel intensities.

Available parameters:

| Parameter name | Meaning | Valid values |
| --- | --- | --- |
| `black` | The value of the minimal pixel. | Float, between 0 and 1. |
| `white` | The value of the maximal pixel. | Float, between 0 and 1. |

 Value: "android.media.effect.effects.BlackWhiteEffect"

### EFFECT_BRIGHTNESS

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EFFECT_BRIGHTNESS: String
```

Adjusts the brightness of the image.

Available parameters:

| Parameter name | Meaning | Valid values |
| --- | --- | --- |
| `brightness` | The brightness multiplier. | Positive float. 1.0 means no change; larger values will increase brightness. |

 Value: "android.media.effect.effects.BrightnessEffect"

### EFFECT_CONTRAST

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EFFECT_CONTRAST: String
```

Adjusts the contrast of the image.

Available parameters:

| Parameter name | Meaning | Valid values |
| --- | --- | --- |
| `contrast` | The contrast multiplier. | Float. 1.0 means no change; larger values will increase contrast. |

 Value: "android.media.effect.effects.ContrastEffect"

### EFFECT_CROP

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EFFECT_CROP: String
```

Crops an upright rectangular area from the image. If the crop region falls outside of the image bounds, the results are undefined.

Available parameters:

| Parameter name | Meaning | Valid values |
| --- | --- | --- |
| `xorigin` | The origin's x-value. | Integer, between 0 and width of the image. |
| `yorigin` | The origin's y-value. | Integer, between 0 and height of the image. |
| `width` | The width of the cropped image. | Integer, between 1 and the width of the image minus xorigin. |
| --- | --- | --- |
| `height` | The height of the cropped image. | Integer, between 1 and the height of the image minus yorigin. |

 Value: "android.media.effect.effects.CropEffect"

### EFFECT_CROSSPROCESS

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EFFECT_CROSSPROCESS: String
```

Applies a cross process effect on image, in which the red and green channels are enhanced while the blue channel is restricted.

Available parameters: None 

 Value: "android.media.effect.effects.CrossProcessEffect"

### EFFECT_DOCUMENTARY

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EFFECT_DOCUMENTARY: String
```

Applies black and white documentary style effect on image..

Available parameters: None 

 Value: "android.media.effect.effects.DocumentaryEffect"

### EFFECT_DUOTONE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EFFECT_DUOTONE: String
```

Representation of photo using only two color tones.

Available parameters:

| Parameter name | Meaning | Valid values |
| --- | --- | --- |
| `first_color` | The first color tone. | Integer, representing an ARGB color with 8 bits per channel. May be created using [Color](../android.graphics/Color.md) class. |
| `second_color` | The second color tone. | Integer, representing an ARGB color with 8 bits per channel. May be created using [Color](../android.graphics/Color.md) class. |

 Value: "android.media.effect.effects.DuotoneEffect"

### EFFECT_FILLLIGHT

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EFFECT_FILLLIGHT: String
```

Applies back-light filling to the image.

Available parameters:

| Parameter name | Meaning | Valid values |
| --- | --- | --- |
| `strength` | The strength of the backlight. | Float, between 0 and 1. Zero means no change. |

 Value: "android.media.effect.effects.FillLightEffect"

### EFFECT_FISHEYE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EFFECT_FISHEYE: String
```

Applies a fisheye lens distortion to the image.

Available parameters:

| Parameter name | Meaning | Valid values |
| --- | --- | --- |
| `scale` | The scale of the distortion. | Float, between 0 and 1. Zero means no distortion. |

 Value: "android.media.effect.effects.FisheyeEffect"

### EFFECT_FLIP

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EFFECT_FLIP: String
```

Flips image vertically and/or horizontally.

Available parameters:

| Parameter name | Meaning | Valid values |
| --- | --- | --- |
| `vertical` | Whether to flip image vertically. | Boolean |
| `horizontal` | Whether to flip image horizontally. | Boolean |

 Value: "android.media.effect.effects.FlipEffect"

### EFFECT_GRAIN

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EFFECT_GRAIN: String
```

Applies film grain effect to image.

Available parameters:

| Parameter name | Meaning | Valid values |
| --- | --- | --- |
| `strength` | The strength of the grain effect. | Float, between 0 and 1. Zero means no change. |

 Value: "android.media.effect.effects.GrainEffect"

### EFFECT_GRAYSCALE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EFFECT_GRAYSCALE: String
```

Converts image to grayscale.

Available parameters: None 

 Value: "android.media.effect.effects.GrayscaleEffect"

### EFFECT_LOMOISH

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EFFECT_LOMOISH: String
```

Applies lomo-camera style effect to image.

Available parameters: None 

 Value: "android.media.effect.effects.LomoishEffect"

### EFFECT_NEGATIVE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EFFECT_NEGATIVE: String
```

Inverts the image colors.

Available parameters: None 

 Value: "android.media.effect.effects.NegativeEffect"

### EFFECT_POSTERIZE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EFFECT_POSTERIZE: String
```

Applies posterization effect to image.

Available parameters: None 

 Value: "android.media.effect.effects.PosterizeEffect"

### EFFECT_REDEYE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EFFECT_REDEYE: String
```

Removes red eyes on specified region.

Available parameters:

| Parameter name | Meaning | Valid values |
| --- | --- | --- |
| `centers` | Multiple center points (x, y) of the red eye regions. | An array of floats, where (f\[2\*i\], f\[2\*i+1\]) specifies the center of the i'th eye. Coordinate values are expected to be normalized between 0 and 1. |

 Value: "android.media.effect.effects.RedEyeEffect"

### EFFECT_ROTATE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EFFECT_ROTATE: String
```

Rotates the image. The output frame size must be able to fit the rotated version of the input image. Note that the rotation snaps to a the closest multiple of 90 degrees.

Available parameters:

| Parameter name | Meaning | Valid values |
| --- | --- | --- |
| `angle` | The angle of rotation in degrees. | Integer value. This will be rounded to the nearest multiple of 90. |

 Value: "android.media.effect.effects.RotateEffect"

### EFFECT_SATURATE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EFFECT_SATURATE: String
```

Adjusts color saturation of image.

Available parameters:

| Parameter name | Meaning | Valid values |
| --- | --- | --- |
| `scale` | The scale of color saturation. | Float, between -1 and 1. 0 means no change, while -1 indicates full desaturation, i.e. grayscale. |

 Value: "android.media.effect.effects.SaturateEffect"

### EFFECT_SEPIA

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EFFECT_SEPIA: String
```

Converts image to sepia tone.

Available parameters: None 

 Value: "android.media.effect.effects.SepiaEffect"

### EFFECT_SHARPEN

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EFFECT_SHARPEN: String
```

Sharpens the image.

Available parameters:

| Parameter name | Meaning | Valid values |
| --- | --- | --- |
| `scale` | The degree of sharpening. | Float, between 0 and 1. 0 means no change. |

 Value: "android.media.effect.effects.SharpenEffect"

### EFFECT_STRAIGHTEN

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EFFECT_STRAIGHTEN: String
```

Rotates the image according to the specified angle, and crops the image so that no non-image portions are visible.

Available parameters:

| Parameter name | Meaning | Valid values |
| --- | --- | --- |
| `angle` | The angle of rotation. | Float, between -45 and +45. |

 Value: "android.media.effect.effects.StraightenEffect"

### EFFECT_TEMPERATURE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EFFECT_TEMPERATURE: String
```

Adjusts color temperature of the image.

Available parameters:

| Parameter name | Meaning | Valid values |
| --- | --- | --- |
| `scale` | The value of color temperature. | Float, between 0 and 1, with 0 indicating cool, and 1 indicating warm. A value of of 0.5 indicates no change. |

 Value: "android.media.effect.effects.ColorTemperatureEffect"

### EFFECT_TINT

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EFFECT_TINT: String
```

Tints the photo with specified color.

Available parameters:

| Parameter name | Meaning | Valid values |
| --- | --- | --- |
| `tint` | The color of the tint. | Integer, representing an ARGB color with 8 bits per channel. May be created using [Color](../android.graphics/Color.md) class. |

 Value: "android.media.effect.effects.TintEffect"

### EFFECT_VIGNETTE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EFFECT_VIGNETTE: String
```

Adds a vignette effect to image, i.e. fades away the outer image edges.

Available parameters:

| Parameter name | Meaning | Valid values |
| --- | --- | --- |
| `scale` | The scale of vignetting. | Float, between 0 and 1. 0 means no change. |

 Value: "android.media.effect.effects.VignetteEffect"

## Public methods

### createEffect

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun createEffect(effectName: String!): Effect!
```

Instantiate a new effect with the given effect name.

The effect's parameters will be set to their default values.

Note that the EGL context associated with the current EffectContext need not be made current when creating an effect. This allows the host application to instantiate effects before any EGL context has become current.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------|
| `effectName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the effect to create. |

| Return ||
|---------------------------------------------------------------------------------------|------------------------|
| [Effect](Effect.md)! | A new Effect instance. |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the effect with the specified name is not supported or not known. |

### isEffectSupported

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isEffectSupported(effectName: String!): Boolean
```

Check if an effect is supported on this platform.

Some effects may only be available on certain platforms. Use this method before instantiating an effect to make sure it is supported.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------|
| `effectName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the effect. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true, if the effect is supported on this platform. |

| Exceptions ||
|--------------------------------------|----------------------------------|
| `java.lang.IllegalArgumentException` | if the effect name is not known. |
