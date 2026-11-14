# WindowMetrics

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WindowMetrics

Kotlin| [Java](WindowMetrics.md) 
| --- | --- |

```
class WindowMetrics
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.WindowMetrics](WindowMetrics.md) |

Metrics about a Window, consisting of the bounds and [WindowInsets](WindowInsets.md).

This is usually obtained from [WindowManager.getCurrentWindowMetrics()](WindowManager.md))and [WindowManager.getMaximumWindowMetrics()](WindowManager.md)).
After [android.os.Build.VERSION_CODES#UPSIDE_DOWN_CAKE](../android/os/Build.VERSION_CODES.md), it also provides density.

### Obtains Window Dimensions in Density-independent Pixel(DP)

While [getDensity()](WindowMetrics.md))is provided, the dimension in density-independent pixel could also be calculated with`WindowMetrics`properties, which is similar to [android.content.res.Configuration#screenWidthDp](../android.content.res/Configuration.md) 

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
| [WindowMetrics](WindowMetrics.md))`(`bounds:` ` [Rect](../android.graphics/Rect.md)`, `windowInsets:` ` [WindowInsets](WindowInsets.md)`)` <br /> |
| [WindowMetrics](WindowMetrics.md))`(`bounds:` ` [Rect](../android.graphics/Rect.md)`, `windowInsets:` ` [WindowInsets](WindowInsets.md)`, `density:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` The constructor to create a [WindowMetrics](WindowMetrics.md) instance. |

| Public methods ||
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Rect](../android.graphics/Rect.md) | [getBounds](WindowMetrics.md))`()` Returns the bounds of the area associated with this window or`UiContext`. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getDensity](WindowMetrics.md))`()` Returns the density of the area associated with this window or`UiContext`, which uses the same units as [android.util.DisplayMetrics#density](../android.util/DisplayMetrics.md). |
| [WindowInsets](WindowInsets.md) | [getWindowInsets](WindowMetrics.md))`()` Returns the [WindowInsets](WindowInsets.md) of the area associated with this window or`UiContext`. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](WindowMetrics.md))`()` <br /> |

## Public constructors

### WindowMetrics

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
WindowMetrics(
    bounds: Rect, 
    windowInsets: WindowInsets)
```

**Deprecated:** *use [WindowMetrics(android.graphics.Rect,android.view.WindowInsets,float)](WindowMetrics.md))instead.*

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------|
| `bounds` | [Rect](../android.graphics/Rect.md):This value cannot be`null`. |
| `windowInsets` | [WindowInsets](WindowInsets.md):This value cannot be`null`. |

### WindowMetrics

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
WindowMetrics(
    bounds: Rect, 
    windowInsets: WindowInsets, 
    density: Float)
```

The constructor to create a [WindowMetrics](WindowMetrics.md) instance.

Note that in most cases [WindowMetrics](WindowMetrics.md) is obtained from [WindowManager.getCurrentWindowMetrics()](WindowManager.md))or [WindowManager.getMaximumWindowMetrics()](WindowManager.md)).

| Parameters ||
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `bounds` | [Rect](../android.graphics/Rect.md):The window bounds This value cannot be`null`. |
| `windowInsets` | [WindowInsets](WindowInsets.md):The [WindowInsets](WindowInsets.md) of the window This value cannot be`null`. |
| `density` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The window density |
| --- | --- |

## Public methods

### getBounds

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getBounds(): Rect
```

Returns the bounds of the area associated with this window or`UiContext`.

**Note that the size of the reported bounds can have different size than [Display.getSize(Point)](Display.md))based on your target API level and calling context.** This method reports the window size including all system bar areas, while [Display.getSize(Point)](Display.md))can report the area excluding navigation bars and display cutout areas depending on the calling context and target SDK level. Please refer to [Display.getSize(Point)](Display.md))for details.

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
| [Rect](../android.graphics/Rect.md) | window bounds in pixels. This value cannot be`null`. |

### getDensity

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDensity(): Float
```

Returns the density of the area associated with this window or`UiContext`, which uses the same units as [android.util.DisplayMetrics#density](../android.util/DisplayMetrics.md). 
**See Also**

- [android.util.DisplayMetrics#DENSITY_DEFAULT](../android.util/DisplayMetrics.md)
- [android.util.DisplayMetrics#density](../android.util/DisplayMetrics.md) 

### getWindowInsets

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getWindowInsets(): WindowInsets
```

Returns the [WindowInsets](WindowInsets.md) of the area associated with this window or`UiContext`.

| Return ||
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [WindowInsets](WindowInsets.md) | the [WindowInsets](WindowInsets.md) of the visual area. This value cannot be`null`. |

### toString

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |
