# Xfermode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Xfermode

Kotlin| [Java](../android/graphics/Xfermode.md) 
| --- | --- |

```
open class Xfermode
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.Xfermode](../android/graphics/Xfermode.md) |

| Known Direct Subclasses [PorterDuffXfermode](../android/graphics/PorterDuffXfermode.md), [RuntimeXfermode](../android/graphics/RuntimeXfermode.md) |----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [PorterDuffXfermode](../android/graphics/PorterDuffXfermode.md) | Specialized implementation of [Paint](../android/graphics/Paint.md)'s [transfer mode](../android/graphics/Paint.md)). | | [RuntimeXfermode](../android/graphics/RuntimeXfermode.md) | A [RuntimeXfermode](../android/graphics/RuntimeXfermode.md) calculates a per-pixel color based on the output of a user \* defined Android Graphics Shading Language (AGSL) function. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Xfermode is the base class for objects that are called to implement custom "transfer-modes" in the drawing pipeline. The static function Create(Modes) can be called to return an instance of any of the predefined subclasses as specified in the Modes enum. When an Xfermode is assigned to a Paint, then objects drawn with that paint have the xfermode applied.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------|---|
| [Xfermode](../android/graphics/Xfermode.md))`()` <br /> |

## Public constructors

### Xfermode

```
Xfermode()
```
