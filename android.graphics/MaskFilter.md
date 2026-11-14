# MaskFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MaskFilter

Kotlin| [Java](../android/graphics/MaskFilter.md) 
| --- | --- |

```
open class MaskFilter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.MaskFilter](../android/graphics/MaskFilter.md) |

| Known Direct Subclasses [BlurMaskFilter](../android/graphics/BlurMaskFilter.md), [EmbossMaskFilter](../android/graphics/EmbossMaskFilter.md) |------------------------------------------------------------------------------------------------------|----------------------------------------------------------------| | [BlurMaskFilter](../android/graphics/BlurMaskFilter.md) | This takes a mask, and blurs its edge by the specified radius. | | [EmbossMaskFilter](../android/graphics/EmbossMaskFilter.md) | <br /> | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

MaskFilter is the base class for object that perform transformations on an alpha-channel mask before drawing it. A subclass of MaskFilter may be installed into a Paint. Blur and emboss are implemented as subclasses of MaskFilter.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------|---|
| [MaskFilter](../android/graphics/MaskFilter.md))`()` <br /> |

| Protected methods ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](../android/graphics/MaskFilter.md))`()` <br /> |

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
