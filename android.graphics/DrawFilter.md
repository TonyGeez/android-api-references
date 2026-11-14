# DrawFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DrawFilter

Kotlin| [Java](https://developer.android.com/reference/android/graphics/DrawFilter "View this page in Java") 
| --- | --- |

```
open class DrawFilter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.DrawFilter](https://developer.android.com/reference/kotlin/android/graphics/DrawFilter#) |

| Known Direct Subclasses [PaintFlagsDrawFilter](https://developer.android.com/reference/kotlin/android/graphics/PaintFlagsDrawFilter) |--------------------------------------------------------------------------------------------------------------|--------| | [PaintFlagsDrawFilter](https://developer.android.com/reference/kotlin/android/graphics/PaintFlagsDrawFilter) | <br /> | |
| --- | --- | --- | --- | --- | --- | --- |

A DrawFilter subclass can be installed in a Canvas. When it is present, it can modify the paint that is used to draw (temporarily). With this, a filter can disable/enable antialiasing, or change the color for everything this is drawn.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------|---|
| [DrawFilter](https://developer.android.com/reference/kotlin/android/graphics/DrawFilter#DrawFilter())`()` <br /> |

| Protected methods ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](https://developer.android.com/reference/kotlin/android/graphics/DrawFilter#finalize())`()` <br /> |

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
