# DisplayMetrics

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DisplayMetrics

Kotlin| [Java](../android/util/DisplayMetrics.md) 
| --- | --- |

```
open class DisplayMetrics
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.util.DisplayMetrics](../android/util/DisplayMetrics.md) |

A structure describing general information about a display, such as its size, density, and font scaling.

To access the DisplayMetrics members, retrieve display metrics like this: 

```kotlin
context.getResources().getDisplayMetrics();
```

For UI layout, obtain [android.view.WindowMetrics](../android/view/WindowMetrics.md) from [WindowManager.getCurrentWindowMetrics()](../android/view/WindowManager.md)).`DisplayMetrics`should only be used for obtaining display related properties, such as [xdpi](../android/util/DisplayMetrics.md) and [ydpi](../android/util/DisplayMetrics.md)

See [density](../android/util/DisplayMetrics.md) for more information about the differences between [xdpi](../android/util/DisplayMetrics.md), [ydpi](../android/util/DisplayMetrics.md) and [density](../android/util/DisplayMetrics.md).

## Summary

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DENSITY_140](../android/util/DisplayMetrics.md) Intermediate density for screens that sit between [DENSITY_LOW](../android/util/DisplayMetrics.md)(120dpi) and [DENSITY_MEDIUM](../android/util/DisplayMetrics.md)(160dpi). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DENSITY_180](../android/util/DisplayMetrics.md) Intermediate density for screens that sit between [DENSITY_MEDIUM](../android/util/DisplayMetrics.md)(160dpi) and [DENSITY_HIGH](../android/util/DisplayMetrics.md)(240dpi). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DENSITY_200](../android/util/DisplayMetrics.md) Intermediate density for screens that sit between [DENSITY_MEDIUM](../android/util/DisplayMetrics.md)(160dpi) and [DENSITY_HIGH](../android/util/DisplayMetrics.md)(240dpi). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DENSITY_220](../android/util/DisplayMetrics.md) Intermediate density for screens that sit between [DENSITY_MEDIUM](../android/util/DisplayMetrics.md)(160dpi) and [DENSITY_HIGH](../android/util/DisplayMetrics.md)(240dpi). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DENSITY_260](../android/util/DisplayMetrics.md) Intermediate density for screens that sit between [DENSITY_HIGH](../android/util/DisplayMetrics.md)(240dpi) and [DENSITY_XHIGH](../android/util/DisplayMetrics.md)(320dpi). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DENSITY_280](../android/util/DisplayMetrics.md) Intermediate density for screens that sit between [DENSITY_HIGH](../android/util/DisplayMetrics.md)(240dpi) and [DENSITY_XHIGH](../android/util/DisplayMetrics.md)(320dpi). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DENSITY_300](../android/util/DisplayMetrics.md) Intermediate density for screens that sit between [DENSITY_HIGH](../android/util/DisplayMetrics.md)(240dpi) and [DENSITY_XHIGH](../android/util/DisplayMetrics.md)(320dpi). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DENSITY_340](../android/util/DisplayMetrics.md) Intermediate density for screens that sit somewhere between [DENSITY_XHIGH](../android/util/DisplayMetrics.md)(320 dpi) and [DENSITY_XXHIGH](../android/util/DisplayMetrics.md)(480 dpi). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DENSITY_360](../android/util/DisplayMetrics.md) Intermediate density for screens that sit somewhere between [DENSITY_XHIGH](../android/util/DisplayMetrics.md)(320 dpi) and [DENSITY_XXHIGH](../android/util/DisplayMetrics.md)(480 dpi). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DENSITY_390](../android/util/DisplayMetrics.md) Intermediate density for screens that sit somewhere between [DENSITY_XHIGH](../android/util/DisplayMetrics.md)(320 dpi) and [DENSITY_XXHIGH](../android/util/DisplayMetrics.md)(480 dpi). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DENSITY_400](../android/util/DisplayMetrics.md) Intermediate density for screens that sit somewhere between [DENSITY_XHIGH](../android/util/DisplayMetrics.md)(320 dpi) and [DENSITY_XXHIGH](../android/util/DisplayMetrics.md)(480 dpi). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DENSITY_420](../android/util/DisplayMetrics.md) Intermediate density for screens that sit somewhere between [DENSITY_XHIGH](../android/util/DisplayMetrics.md)(320 dpi) and [DENSITY_XXHIGH](../android/util/DisplayMetrics.md)(480 dpi). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DENSITY_440](../android/util/DisplayMetrics.md) Intermediate density for screens that sit somewhere between [DENSITY_XHIGH](../android/util/DisplayMetrics.md)(320 dpi) and [DENSITY_XXHIGH](../android/util/DisplayMetrics.md)(480 dpi). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DENSITY_450](../android/util/DisplayMetrics.md) Intermediate density for screens that sit somewhere between [DENSITY_XHIGH](../android/util/DisplayMetrics.md)(320 dpi) and [DENSITY_XXHIGH](../android/util/DisplayMetrics.md)(480 dpi). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DENSITY_520](../android/util/DisplayMetrics.md) Intermediate density for screens that sit somewhere between [DENSITY_XXHIGH](../android/util/DisplayMetrics.md)(480 dpi) and [DENSITY_XXXHIGH](../android/util/DisplayMetrics.md)(640 dpi). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DENSITY_560](../android/util/DisplayMetrics.md) Intermediate density for screens that sit somewhere between [DENSITY_XXHIGH](../android/util/DisplayMetrics.md)(480 dpi) and [DENSITY_XXXHIGH](../android/util/DisplayMetrics.md)(640 dpi). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DENSITY_600](../android/util/DisplayMetrics.md) Intermediate density for screens that sit somewhere between [DENSITY_XXHIGH](../android/util/DisplayMetrics.md)(480 dpi) and [DENSITY_XXXHIGH](../android/util/DisplayMetrics.md)(640 dpi). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DENSITY_DEFAULT](../android/util/DisplayMetrics.md) The reference density used throughout the system. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DENSITY_HIGH](../android/util/DisplayMetrics.md) Standard quantized DPI for high-density screens. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DENSITY_LOW](../android/util/DisplayMetrics.md) Standard quantized DPI for low-density screens. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DENSITY_MEDIUM](../android/util/DisplayMetrics.md) Standard quantized DPI for medium-density screens. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DENSITY_TV](../android/util/DisplayMetrics.md) This is a secondary density, added for some common screen configurations. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DENSITY_XHIGH](../android/util/DisplayMetrics.md) Standard quantized DPI for extra-high-density screens. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DENSITY_XXHIGH](../android/util/DisplayMetrics.md) Standard quantized DPI for extra-extra-high-density screens. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DENSITY_XXXHIGH](../android/util/DisplayMetrics.md) Standard quantized DPI for extra-extra-extra-high-density screens. |

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------|---|
| [DisplayMetrics](../android/util/DisplayMetrics.md))`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/util/DisplayMetrics.md))`(`other:` ` [DisplayMetrics](../android/util/DisplayMetrics.md)!`)` Returns true if these display metrics equal the other display metrics. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/util/DisplayMetrics.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/util/DisplayMetrics.md))`()` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTo](../android/util/DisplayMetrics.md))`(`o:` ` [DisplayMetrics](../android/util/DisplayMetrics.md)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setToDefaults](../android/util/DisplayMetrics.md))`()` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/util/DisplayMetrics.md))`()` <br /> |
| --- | --- |

| Properties ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DENSITY_DEVICE_STABLE](../android/util/DisplayMetrics.md) The device's stable density. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [density](../android/util/DisplayMetrics.md) The logical density of the display. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [densityDpi](../android/util/DisplayMetrics.md) The screen density expressed as dots-per-inch. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [heightPixels](../android/util/DisplayMetrics.md) The absolute height of the available display size in pixels. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [scaledDensity](../android/util/DisplayMetrics.md) A scaling factor for fonts displayed on the display. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [widthPixels](../android/util/DisplayMetrics.md) The absolute width of the available display size in pixels. |
| --- | --- |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [xdpi](../android/util/DisplayMetrics.md) The exact physical pixels per inch of the screen in the X dimension. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [ydpi](../android/util/DisplayMetrics.md) The exact physical pixels per inch of the screen in the Y dimension. |

## Constants

### DENSITY_140

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DENSITY_140: Int
```

Intermediate density for screens that sit between [DENSITY_LOW](../android/util/DisplayMetrics.md)(120dpi) and [DENSITY_MEDIUM](../android/util/DisplayMetrics.md)(160dpi). This is not a density that applications should target, instead relying on the system to scale their [DENSITY_MEDIUM](../android/util/DisplayMetrics.md) assets for them. 

 Value: 140

### DENSITY_180

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DENSITY_180: Int
```

Intermediate density for screens that sit between [DENSITY_MEDIUM](../android/util/DisplayMetrics.md)(160dpi) and [DENSITY_HIGH](../android/util/DisplayMetrics.md)(240dpi). This is not a density that applications should target, instead relying on the system to scale their [DENSITY_HIGH](../android/util/DisplayMetrics.md) assets for them. 

 Value: 180

### DENSITY_200

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DENSITY_200: Int
```

Intermediate density for screens that sit between [DENSITY_MEDIUM](../android/util/DisplayMetrics.md)(160dpi) and [DENSITY_HIGH](../android/util/DisplayMetrics.md)(240dpi). This is not a density that applications should target, instead relying on the system to scale their [DENSITY_HIGH](../android/util/DisplayMetrics.md) assets for them. 

 Value: 200

### DENSITY_220

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DENSITY_220: Int
```

Intermediate density for screens that sit between [DENSITY_MEDIUM](../android/util/DisplayMetrics.md)(160dpi) and [DENSITY_HIGH](../android/util/DisplayMetrics.md)(240dpi). This is not a density that applications should target, instead relying on the system to scale their [DENSITY_HIGH](../android/util/DisplayMetrics.md) assets for them. 

 Value: 220

### DENSITY_260

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DENSITY_260: Int
```

Intermediate density for screens that sit between [DENSITY_HIGH](../android/util/DisplayMetrics.md)(240dpi) and [DENSITY_XHIGH](../android/util/DisplayMetrics.md)(320dpi). This is not a density that applications should target, instead relying on the system to scale their [DENSITY_XHIGH](../android/util/DisplayMetrics.md) assets for them. 

 Value: 260

### DENSITY_280

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DENSITY_280: Int
```

Intermediate density for screens that sit between [DENSITY_HIGH](../android/util/DisplayMetrics.md)(240dpi) and [DENSITY_XHIGH](../android/util/DisplayMetrics.md)(320dpi). This is not a density that applications should target, instead relying on the system to scale their [DENSITY_XHIGH](../android/util/DisplayMetrics.md) assets for them. 

 Value: 280

### DENSITY_300

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DENSITY_300: Int
```

Intermediate density for screens that sit between [DENSITY_HIGH](../android/util/DisplayMetrics.md)(240dpi) and [DENSITY_XHIGH](../android/util/DisplayMetrics.md)(320dpi). This is not a density that applications should target, instead relying on the system to scale their [DENSITY_XHIGH](../android/util/DisplayMetrics.md) assets for them. 

 Value: 300

### DENSITY_340

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DENSITY_340: Int
```

Intermediate density for screens that sit somewhere between [DENSITY_XHIGH](../android/util/DisplayMetrics.md)(320 dpi) and [DENSITY_XXHIGH](../android/util/DisplayMetrics.md)(480 dpi). This is not a density that applications should target, instead relying on the system to scale their [DENSITY_XXHIGH](../android/util/DisplayMetrics.md) assets for them. 

 Value: 340

### DENSITY_360

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DENSITY_360: Int
```

Intermediate density for screens that sit somewhere between [DENSITY_XHIGH](../android/util/DisplayMetrics.md)(320 dpi) and [DENSITY_XXHIGH](../android/util/DisplayMetrics.md)(480 dpi). This is not a density that applications should target, instead relying on the system to scale their [DENSITY_XXHIGH](../android/util/DisplayMetrics.md) assets for them. 

 Value: 360

### DENSITY_390

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DENSITY_390: Int
```

Intermediate density for screens that sit somewhere between [DENSITY_XHIGH](../android/util/DisplayMetrics.md)(320 dpi) and [DENSITY_XXHIGH](../android/util/DisplayMetrics.md)(480 dpi). This is not a density that applications should target, instead relying on the system to scale their [DENSITY_XXHIGH](../android/util/DisplayMetrics.md) assets for them. 

 Value: 390

### DENSITY_400

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DENSITY_400: Int
```

Intermediate density for screens that sit somewhere between [DENSITY_XHIGH](../android/util/DisplayMetrics.md)(320 dpi) and [DENSITY_XXHIGH](../android/util/DisplayMetrics.md)(480 dpi). This is not a density that applications should target, instead relying on the system to scale their [DENSITY_XXHIGH](../android/util/DisplayMetrics.md) assets for them. 

 Value: 400

### DENSITY_420

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DENSITY_420: Int
```

Intermediate density for screens that sit somewhere between [DENSITY_XHIGH](../android/util/DisplayMetrics.md)(320 dpi) and [DENSITY_XXHIGH](../android/util/DisplayMetrics.md)(480 dpi). This is not a density that applications should target, instead relying on the system to scale their [DENSITY_XXHIGH](../android/util/DisplayMetrics.md) assets for them. 

 Value: 420

### DENSITY_440

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DENSITY_440: Int
```

Intermediate density for screens that sit somewhere between [DENSITY_XHIGH](../android/util/DisplayMetrics.md)(320 dpi) and [DENSITY_XXHIGH](../android/util/DisplayMetrics.md)(480 dpi). This is not a density that applications should target, instead relying on the system to scale their [DENSITY_XXHIGH](../android/util/DisplayMetrics.md) assets for them. 

 Value: 440

### DENSITY_450

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DENSITY_450: Int
```

Intermediate density for screens that sit somewhere between [DENSITY_XHIGH](../android/util/DisplayMetrics.md)(320 dpi) and [DENSITY_XXHIGH](../android/util/DisplayMetrics.md)(480 dpi). This is not a density that applications should target, instead relying on the system to scale their [DENSITY_XXHIGH](../android/util/DisplayMetrics.md) assets for them. 

 Value: 450

### DENSITY_520

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DENSITY_520: Int
```

Intermediate density for screens that sit somewhere between [DENSITY_XXHIGH](../android/util/DisplayMetrics.md)(480 dpi) and [DENSITY_XXXHIGH](../android/util/DisplayMetrics.md)(640 dpi). This is not a density that applications should target, instead relying on the system to scale their [DENSITY_XXXHIGH](../android/util/DisplayMetrics.md) assets for them. 

 Value: 520

### DENSITY_560

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DENSITY_560: Int
```

Intermediate density for screens that sit somewhere between [DENSITY_XXHIGH](../android/util/DisplayMetrics.md)(480 dpi) and [DENSITY_XXXHIGH](../android/util/DisplayMetrics.md)(640 dpi). This is not a density that applications should target, instead relying on the system to scale their [DENSITY_XXXHIGH](../android/util/DisplayMetrics.md) assets for them. 

 Value: 560

### DENSITY_600

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DENSITY_600: Int
```

Intermediate density for screens that sit somewhere between [DENSITY_XXHIGH](../android/util/DisplayMetrics.md)(480 dpi) and [DENSITY_XXXHIGH](../android/util/DisplayMetrics.md)(640 dpi). This is not a density that applications should target, instead relying on the system to scale their [DENSITY_XXXHIGH](../android/util/DisplayMetrics.md) assets for them. 

 Value: 600

### DENSITY_DEFAULT

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DENSITY_DEFAULT: Int
```

The reference density used throughout the system. 

 Value: 160

### DENSITY_HIGH

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DENSITY_HIGH: Int
```

Standard quantized DPI for high-density screens. 

 Value: 240

### DENSITY_LOW

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DENSITY_LOW: Int
```

Standard quantized DPI for low-density screens. 

 Value: 120

### DENSITY_MEDIUM

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DENSITY_MEDIUM: Int
```

Standard quantized DPI for medium-density screens. 

 Value: 160

### DENSITY_TV

Added in [API level 13](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DENSITY_TV: Int
```

This is a secondary density, added for some common screen configurations. It is recommended that applications not generally target this as a first class density -- that is, don't supply specific graphics for this density, instead allow the platform to scale from other densities (typically [DENSITY_HIGH](../android/util/DisplayMetrics.md)) as appropriate. In most cases (such as using bitmaps in [android.graphics.drawable.Drawable](../android/graphics/drawable/Drawable.md)) the platform can perform this scaling at load time, so the only cost is some slight startup runtime overhead.

This density was original introduced to correspond with a 720p TV screen: the density for 1080p televisions is [DENSITY_XHIGH](../android/util/DisplayMetrics.md), and the value here provides the same UI size for a TV running at 720p. It has also found use in 7" tablets, when these devices have 1280x720 displays. 

 Value: 213

### DENSITY_XHIGH

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DENSITY_XHIGH: Int
```

Standard quantized DPI for extra-high-density screens. 

 Value: 320

### DENSITY_XXHIGH

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DENSITY_XXHIGH: Int
```

Standard quantized DPI for extra-extra-high-density screens. 

 Value: 480

### DENSITY_XXXHIGH

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DENSITY_XXXHIGH: Int
```

Standard quantized DPI for extra-extra-extra-high-density screens. Applications should not generally worry about this density; relying on XHIGH graphics being scaled up to it should be sufficient for almost all cases. A typical use of this density would be 4K television screens -- 3840x2160, which is 2x a traditional HD 1920x1080 screen which runs at DENSITY_XHIGH. 

 Value: 640

## Public constructors

### DisplayMetrics

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DisplayMetrics()
```

## Public methods

### equals

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: DisplayMetrics!): Boolean
```

Returns true if these display metrics equal the other display metrics.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `other` | [DisplayMetrics](../android/util/DisplayMetrics.md)!:The display metrics with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the display metrics are equal. |

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
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

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### setTo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTo(o: DisplayMetrics!): Unit
```  

### setToDefaults

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setToDefaults(): Unit
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

### DENSITY_DEVICE_STABLE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DENSITY_DEVICE_STABLE: Int
```

The device's stable density.

This value is constant at run time and may not reflect the current display density. To obtain the current density for a specific display, use [densityDpi](../android/util/DisplayMetrics.md). 

### density

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var density: Float
```

The logical density of the display. This is a scaling factor for the Density Independent Pixel unit, where one DIP is one pixel on an approximately 160 dpi screen (for example a 240x320, 1.5"x2" screen), providing the baseline of the system's display. Thus on a 160dpi screen this density value will be 1; on a 120 dpi screen it would be .75; etc.

This value does not exactly follow the real screen size (as given by [xdpi](../android/util/DisplayMetrics.md) and [ydpi](../android/util/DisplayMetrics.md)), but rather is used to scale the size of the overall UI in steps based on gross changes in the display dpi. For example, a 240x320 screen will have a density of 1 even if its width is 1.8", 1.3", etc. However, if the screen resolution is increased to 320x480 but the screen size remained 1.5"x2" then the density would be increased (probably to 1.5). 
**See Also**

- [#DENSITY_DEFAULT](../android/util/DisplayMetrics.md) 

### densityDpi

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var densityDpi: Int
```

The screen density expressed as dots-per-inch. May be any one of the`DENSITY_`constants defined above. New constants are frequently added, and constants added on new Android versions may be backported to previous Android versions, so applications should not strongly rely on density matching one of the enum constants. 
Value is [android.util.DisplayMetrics#DENSITY_LOW](../android/util/DisplayMetrics.md), [android.util.DisplayMetrics#DENSITY_140](../android/util/DisplayMetrics.md), [android.util.DisplayMetrics#DENSITY_MEDIUM](../android/util/DisplayMetrics.md), [android.util.DisplayMetrics#DENSITY_180](../android/util/DisplayMetrics.md), [android.util.DisplayMetrics#DENSITY_200](../android/util/DisplayMetrics.md), [android.util.DisplayMetrics#DENSITY_TV](../android/util/DisplayMetrics.md), [android.util.DisplayMetrics#DENSITY_220](../android/util/DisplayMetrics.md), [android.util.DisplayMetrics#DENSITY_HIGH](../android/util/DisplayMetrics.md), [android.util.DisplayMetrics#DENSITY_260](../android/util/DisplayMetrics.md), [android.util.DisplayMetrics#DENSITY_280](../android/util/DisplayMetrics.md), [android.util.DisplayMetrics#DENSITY_300](../android/util/DisplayMetrics.md), [android.util.DisplayMetrics#DENSITY_XHIGH](../android/util/DisplayMetrics.md), [android.util.DisplayMetrics#DENSITY_340](../android/util/DisplayMetrics.md), [android.util.DisplayMetrics#DENSITY_360](../android/util/DisplayMetrics.md), [android.util.DisplayMetrics#DENSITY_390](../android/util/DisplayMetrics.md), [android.util.DisplayMetrics#DENSITY_400](../android/util/DisplayMetrics.md), [android.util.DisplayMetrics#DENSITY_420](../android/util/DisplayMetrics.md), [android.util.DisplayMetrics#DENSITY_440](../android/util/DisplayMetrics.md), [android.util.DisplayMetrics#DENSITY_450](../android/util/DisplayMetrics.md), [android.util.DisplayMetrics#DENSITY_XXHIGH](../android/util/DisplayMetrics.md), [android.util.DisplayMetrics#DENSITY_520](../android/util/DisplayMetrics.md), [android.util.DisplayMetrics#DENSITY_560](../android/util/DisplayMetrics.md), [android.util.DisplayMetrics#DENSITY_600](../android/util/DisplayMetrics.md), or [android.util.DisplayMetrics#DENSITY_XXXHIGH](../android/util/DisplayMetrics.md) 

### heightPixels

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var heightPixels: Int
```

The absolute height of the available display size in pixels. 

### scaledDensity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var scaledDensity: Float
```

**Deprecated:** *this scalar factor is no longer accurate due to adaptive non-linear font scaling. Please use [TypedValue.applyDimension(int, float, DisplayMetrics)](../android/util/TypedValue.md))or [TypedValue.deriveDimension(int, float, DisplayMetrics)](../android/util/TypedValue.md))to convert between SP font sizes and pixels.*

A scaling factor for fonts displayed on the display. This is the same as [density](../android/util/DisplayMetrics.md), except that it may be adjusted in smaller increments at runtime based on a user preference for the font size. 

### widthPixels

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var widthPixels: Int
```

The absolute width of the available display size in pixels. 

### xdpi

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var xdpi: Float
```

The exact physical pixels per inch of the screen in the X dimension. 

### ydpi

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
var ydpi: Float
```

The exact physical pixels per inch of the screen in the Y dimension.
