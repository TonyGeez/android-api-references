# DrawFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DrawFilter

Kotlin| [Java](../android/graphics/DrawFilter.md) 
| --- | --- |

```
open class DrawFilter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.DrawFilter](../android/graphics/DrawFilter.md) |

| Known Direct Subclasses [PaintFlagsDrawFilter](../android/graphics/PaintFlagsDrawFilter.md) |--------------------------------------------------------------------------------------------------------------|--------| | [PaintFlagsDrawFilter](../android/graphics/PaintFlagsDrawFilter.md) | <br /> | |
| --- | --- | --- | --- | --- | --- | --- |

A DrawFilter subclass can be installed in a Canvas. When it is present, it can modify the paint that is used to draw (temporarily). With this, a filter can disable/enable antialiasing, or change the color for everything this is drawn.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------|---|
| [DrawFilter](../android/graphics/DrawFilter.md))`()` <br /> |

| Protected methods ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](../android/graphics/DrawFilter.md))`()` <br /> |

## Public constructors

### DrawFilter

```
DrawFilter()
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
