# MaskFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MaskFilter

Kotlin| [Java](MaskFilter.md) 
| --- | --- |

```
open class MaskFilter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.MaskFilter](MaskFilter.md) |

| Known Direct Subclasses [BlurMaskFilter](BlurMaskFilter.md), [EmbossMaskFilter](EmbossMaskFilter.md) |------------------------------------------------------------------------------------------------------|----------------------------------------------------------------| | [BlurMaskFilter](BlurMaskFilter.md) | This takes a mask, and blurs its edge by the specified radius. | | [EmbossMaskFilter](EmbossMaskFilter.md) | <br /> | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

MaskFilter is the base class for object that perform transformations on an alpha-channel mask before drawing it. A subclass of MaskFilter may be installed into a Paint. Blur and emboss are implemented as subclasses of MaskFilter.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------|---|
| [MaskFilter](MaskFilter.md))`()` <br /> |

| Protected methods ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](MaskFilter.md))`()` <br /> |

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
