# WallpaperManager.OnColorsChangedListener

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnColorsChangedListener

Kotlin| [Java](../android/app/WallpaperManager.OnColorsChangedListener.md) 
| --- | --- |

```
interface OnColorsChangedListener
```

| [android.app.WallpaperManager.OnColorsChangedListener](../android/app/WallpaperManager.OnColorsChangedListener.md) |

Interface definition for a callback to be invoked when colors change on a wallpaper.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onColorsChanged](../android/app/WallpaperManager.OnColorsChangedListener.md))`(`colors:` ` [WallpaperColors](../android/app/WallpaperColors.md)?`, `which:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when colors change. |

## Public methods

### onColorsChanged

Added in [API level 27](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onColorsChanged(
    colors: WallpaperColors?, 
    which: Int
): Unit
```

Called when colors change. A [android.app.WallpaperColors](../android/app/WallpaperColors.md) object containing a simplified color histogram will be given.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `colors` | [WallpaperColors](../android/app/WallpaperColors.md)?:Wallpaper color info,`null`when not available. |
| `which` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A combination of [FLAG_LOCK](../android/app/WallpaperManager.md) and [FLAG_SYSTEM](../android/app/WallpaperManager.md) |

**See Also**

- [android.service.wallpaper.WallpaperService.Engine#onComputeColors()](../android/service/wallpaper/WallpaperService.Engine.md))
