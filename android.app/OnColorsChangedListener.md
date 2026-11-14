# WallpaperManager.OnColorsChangedListener

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnColorsChangedListener

Kotlin| [Java](https://developer.android.com/reference/android/app/WallpaperManager.OnColorsChangedListener "View this page in Java") 

```
interface OnColorsChangedListener
```

| [android.app.WallpaperManager.OnColorsChangedListener](https://developer.android.com/reference/kotlin/android/app/WallpaperManager.OnColorsChangedListener#) |

Interface definition for a callback to be invoked when colors change on a wallpaper.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onColorsChanged](https://developer.android.com/reference/kotlin/android/app/WallpaperManager.OnColorsChangedListener#onColorsChanged(android.app.WallpaperColors,%20kotlin.Int))`(`colors:` ` [WallpaperColors](https://developer.android.com/reference/kotlin/android/app/WallpaperColors)?`, `which:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when colors change. |

## Public methods

### onColorsChanged

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onColorsChanged(
    colors: WallpaperColors?, 
    which: Int
): Unit
```

Called when colors change. A [android.app.WallpaperColors](https://developer.android.com/reference/kotlin/android/app/WallpaperColors) object containing a simplified color histogram will be given.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `colors` | [WallpaperColors](https://developer.android.com/reference/kotlin/android/app/WallpaperColors)?:Wallpaper color info,`null`when not available. |
| `which` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A combination of [FLAG_LOCK](https://developer.android.com/reference/kotlin/android/app/WallpaperManager#FLAG_LOCK:kotlin.Int) and [FLAG_SYSTEM](https://developer.android.com/reference/kotlin/android/app/WallpaperManager#FLAG_SYSTEM:kotlin.Int) |

**See Also**

- [android.service.wallpaper.WallpaperService.Engine#onComputeColors()](https://developer.android.com/reference/kotlin/android/service/wallpaper/WallpaperService.Engine.html#onComputeColors())
