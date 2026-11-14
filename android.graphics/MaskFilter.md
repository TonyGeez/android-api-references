# MaskFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MaskFilter

Kotlin| [Java](https://developer.android.com/reference/android/graphics/MaskFilter "View this page in Java") 

```
open class MaskFilter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.graphics.MaskFilter](https://developer.android.com/reference/kotlin/android/graphics/MaskFilter#) |

| Known Direct Subclasses [BlurMaskFilter](https://developer.android.com/reference/kotlin/android/graphics/BlurMaskFilter), [EmbossMaskFilter](https://developer.android.com/reference/kotlin/android/graphics/EmbossMaskFilter) |------------------------------------------------------------------------------------------------------|----------------------------------------------------------------| | [BlurMaskFilter](https://developer.android.com/reference/kotlin/android/graphics/BlurMaskFilter) | This takes a mask, and blurs its edge by the specified radius. | | [EmbossMaskFilter](https://developer.android.com/reference/kotlin/android/graphics/EmbossMaskFilter) | <br /> | |

MaskFilter is the base class for object that perform transformations on an alpha-channel mask before drawing it. A subclass of MaskFilter may be installed into a Paint. Blur and emboss are implemented as subclasses of MaskFilter.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------|---|
| [MaskFilter](https://developer.android.com/reference/kotlin/android/graphics/MaskFilter#MaskFilter())`()` <br /> |

| Protected methods ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](https://developer.android.com/reference/kotlin/android/graphics/MaskFilter#finalize())`()` <br /> |

## Public constructors

### MaskFilter

```
MaskFilter()
```

## Protected methods

### finalize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun finalize(): Unit
```

| Exceptions ||
|-----------------------|-------------------------------------|
| `java.lang.Throwable` | the`Exception`raised by this method |
