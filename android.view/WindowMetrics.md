# WindowMetrics

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WindowMetrics

Kotlin| [Java](https://developer.android.com/reference/android/view/WindowMetrics "View this page in Java") 

```
class WindowMetrics
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.view.WindowMetrics](https://developer.android.com/reference/kotlin/android/view/WindowMetrics#) |

Metrics about a Window, consisting of the bounds and [WindowInsets](https://developer.android.com/reference/kotlin/android/view/WindowInsets).

This is usually obtained from [WindowManager.getCurrentWindowMetrics()](https://developer.android.com/reference/kotlin/android/view/WindowManager#getCurrentWindowMetrics())and [WindowManager.getMaximumWindowMetrics()](https://developer.android.com/reference/kotlin/android/view/WindowManager#getMaximumWindowMetrics()).
After [android.os.Build.VERSION_CODES#UPSIDE_DOWN_CAKE](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int), it also provides density.

### Obtains Window Dimensions in Density-independent Pixel(DP)

While [getDensity()](https://developer.android.com/reference/kotlin/android/view/WindowMetrics#getDensity())is provided, the dimension in density-independent pixel could also be calculated with`WindowMetrics`properties, which is similar to [android.content.res.Configuration#screenWidthDp](https://developer.android.com/reference/kotlin/android/content/res/Configuration.html#screenWidthDp:kotlin.Int) 

```kotlin
float widthInDp = windowMetrics.getBounds().width() / windowMetrics.getDensity();
  float heightInDp = windowMetrics.getBounds().height() / windowMetrics.getDensity();
  
```
Also, the density in DPI can be obtained by: 

```kotlin
float densityDp = DisplayMetrics.DENSITY_DEFAULT * windowMetrics.getDensity();
  
```

<br />

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [WindowMetrics](https://developer.android.com/reference/kotlin/android/view/WindowMetrics#WindowMetrics(android.graphics.Rect,%20android.view.WindowInsets))`(`bounds:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)`, `windowInsets:` ` [WindowInsets](https://developer.android.com/reference/kotlin/android/view/WindowInsets)`)` <br /> |
| [WindowMetrics](https://developer.android.com/reference/kotlin/android/view/WindowMetrics#WindowMetrics(android.graphics.Rect,%20android.view.WindowInsets,%20kotlin.Float))`(`bounds:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)`, `windowInsets:` ` [WindowInsets](https://developer.android.com/reference/kotlin/android/view/WindowInsets)`, `density:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` The constructor to create a [WindowMetrics](https://developer.android.com/reference/kotlin/android/view/WindowMetrics#) instance. |

| Public methods ||
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#) | [getBounds](https://developer.android.com/reference/kotlin/android/view/WindowMetrics#getBounds())`()` Returns the bounds of the area associated with this window or`UiContext`. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getDensity](https://developer.android.com/reference/kotlin/android/view/WindowMetrics#getDensity())`()` Returns the density of the area associated with this window or`UiContext`, which uses the same units as [android.util.DisplayMetrics#density](https://developer.android.com/reference/kotlin/android/util/DisplayMetrics.html#density:kotlin.Float). |
| [WindowInsets](https://developer.android.com/reference/kotlin/android/view/WindowInsets) | [getWindowInsets](https://developer.android.com/reference/kotlin/android/view/WindowMetrics#getWindowInsets())`()` Returns the [WindowInsets](https://developer.android.com/reference/kotlin/android/view/WindowInsets) of the area associated with this window or`UiContext`. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/view/WindowMetrics#toString())`()` <br /> |

## Public constructors

### WindowMetrics

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
WindowMetrics(
    bounds: Rect, 
    windowInsets: WindowInsets)
```

**Deprecated:** *use [WindowMetrics(android.graphics.Rect,android.view.WindowInsets,float)](https://developer.android.com/reference/kotlin/android/view/WindowMetrics#WindowMetrics(android.graphics.Rect,%20android.view.WindowInsets,%20kotlin.Float))instead.*

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------|
| `bounds` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#):This value cannot be`null`. |
| `windowInsets` | [WindowInsets](https://developer.android.com/reference/kotlin/android/view/WindowInsets):This value cannot be`null`. |

### WindowMetrics

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
WindowMetrics(
    bounds: Rect, 
    windowInsets: WindowInsets, 
    density: Float)
```

The constructor to create a [WindowMetrics](https://developer.android.com/reference/kotlin/android/view/WindowMetrics#) instance.

Note that in most cases [WindowMetrics](https://developer.android.com/reference/kotlin/android/view/WindowMetrics#) is obtained from [WindowManager.getCurrentWindowMetrics()](https://developer.android.com/reference/kotlin/android/view/WindowManager#getCurrentWindowMetrics())or [WindowManager.getMaximumWindowMetrics()](https://developer.android.com/reference/kotlin/android/view/WindowManager#getMaximumWindowMetrics()).

| Parameters ||
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `bounds` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#):The window bounds This value cannot be`null`. |
| `windowInsets` | [WindowInsets](https://developer.android.com/reference/kotlin/android/view/WindowInsets):The [WindowInsets](https://developer.android.com/reference/kotlin/android/view/WindowInsets) of the window This value cannot be`null`. |
| `density` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The window density |

## Public methods

### getBounds

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getBounds(): Rect
```

Returns the bounds of the area associated with this window or`UiContext`.

**Note that the size of the reported bounds can have different size than [Display.getSize(Point)](https://developer.android.com/reference/kotlin/android/view/Display#getSize(android.graphics.Point))based on your target API level and calling context.** This method reports the window size including all system bar areas, while [Display.getSize(Point)](https://developer.android.com/reference/kotlin/android/view/Display#getSize(android.graphics.Point))can report the area excluding navigation bars and display cutout areas depending on the calling context and target SDK level. Please refer to [Display.getSize(Point)](https://developer.android.com/reference/kotlin/android/view/Display#getSize(android.graphics.Point))for details.

The following code snippet shows how to get the bounds excluding navigation bars and display cutout: 

```kotlin
final WindowMetrics metrics = windowManager.getCurrentWindowMetrics();
  // Gets all excluding insets
  final WindowInsets windowInsets = metrics.getWindowInsets();
  Insets insets = windowInsets.getInsetsIgnoringVisibility(WindowInsets.Type.navigationBars()
          | WindowInsets.Type.displayCutout());
 
  int insetsWidth = insets.right + insets.left;
  int insetsHeight = insets.top + insets.bottom;
 
  // Legacy size that Display#getSize reports
  final Rect bounds = metrics.getBounds();
  final Size legacySize = new Size(bounds.width() - insetsWidth,
          bounds.height() - insetsHeight);
  
```

<br />

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------|
| [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#) | window bounds in pixels. This value cannot be`null`. |

### getDensity

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDensity(): Float
```

Returns the density of the area associated with this window or`UiContext`, which uses the same units as [android.util.DisplayMetrics#density](https://developer.android.com/reference/kotlin/android/util/DisplayMetrics.html#density:kotlin.Float). 
**See Also**

- [android.util.DisplayMetrics#DENSITY_DEFAULT](https://developer.android.com/reference/kotlin/android/util/DisplayMetrics.html#DENSITY_DEFAULT:kotlin.Int)
- [android.util.DisplayMetrics#density](https://developer.android.com/reference/kotlin/android/util/DisplayMetrics.html#density:kotlin.Float) 

### getWindowInsets

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getWindowInsets(): WindowInsets
```

Returns the [WindowInsets](https://developer.android.com/reference/kotlin/android/view/WindowInsets) of the area associated with this window or`UiContext`.

| Return ||
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [WindowInsets](https://developer.android.com/reference/kotlin/android/view/WindowInsets) | the [WindowInsets](https://developer.android.com/reference/kotlin/android/view/WindowInsets) of the visual area. This value cannot be`null`. |

### toString

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |
