# Xfermode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Xfermode

Kotlin| [Java](https://developer.android.com/reference/android/graphics/Xfermode "View this page in Java") 

```
open class Xfermode
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.graphics.Xfermode](https://developer.android.com/reference/kotlin/android/graphics/Xfermode#) |

| Known Direct Subclasses [PorterDuffXfermode](https://developer.android.com/reference/kotlin/android/graphics/PorterDuffXfermode), [RuntimeXfermode](https://developer.android.com/reference/kotlin/android/graphics/RuntimeXfermode) |----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [PorterDuffXfermode](https://developer.android.com/reference/kotlin/android/graphics/PorterDuffXfermode) | Specialized implementation of [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint)'s [transfer mode](https://developer.android.com/reference/kotlin/android/graphics/Paint#setXfermode(android.graphics.Xfermode)). | | [RuntimeXfermode](https://developer.android.com/reference/kotlin/android/graphics/RuntimeXfermode) | A [RuntimeXfermode](https://developer.android.com/reference/kotlin/android/graphics/RuntimeXfermode) calculates a per-pixel color based on the output of a user \* defined Android Graphics Shading Language (AGSL) function. | |

Xfermode is the base class for objects that are called to implement custom "transfer-modes" in the drawing pipeline. The static function Create(Modes) can be called to return an instance of any of the predefined subclasses as specified in the Modes enum. When an Xfermode is assigned to a Paint, then objects drawn with that paint have the xfermode applied.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------|---|
| [Xfermode](https://developer.android.com/reference/kotlin/android/graphics/Xfermode#Xfermode())`()` <br /> |

## Public constructors

### Xfermode

```
Xfermode()
```
