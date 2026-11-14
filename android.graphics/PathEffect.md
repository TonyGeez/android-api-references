# PathEffect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PathEffect

Kotlin| [Java](https://developer.android.com/reference/android/graphics/PathEffect "View this page in Java") 
| --- | --- |

```
open class PathEffect
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.PathEffect](https://developer.android.com/reference/kotlin/android/graphics/PathEffect#) |

| Known Direct Subclasses [ComposePathEffect](https://developer.android.com/reference/kotlin/android/graphics/ComposePathEffect), [CornerPathEffect](https://developer.android.com/reference/kotlin/android/graphics/CornerPathEffect), [DashPathEffect](https://developer.android.com/reference/kotlin/android/graphics/DashPathEffect), [DiscretePathEffect](https://developer.android.com/reference/kotlin/android/graphics/DiscretePathEffect), [PathDashPathEffect](https://developer.android.com/reference/kotlin/android/graphics/PathDashPathEffect), [SumPathEffect](https://developer.android.com/reference/kotlin/android/graphics/SumPathEffect) |----------------------------------------------------------------------------------------------------------|--------| | [ComposePathEffect](https://developer.android.com/reference/kotlin/android/graphics/ComposePathEffect) | <br /> | | [CornerPathEffect](https://developer.android.com/reference/kotlin/android/graphics/CornerPathEffect) | <br /> | | [DashPathEffect](https://developer.android.com/reference/kotlin/android/graphics/DashPathEffect) | <br /> | | [DiscretePathEffect](https://developer.android.com/reference/kotlin/android/graphics/DiscretePathEffect) | <br /> | | [PathDashPathEffect](https://developer.android.com/reference/kotlin/android/graphics/PathDashPathEffect) | <br /> | | [SumPathEffect](https://developer.android.com/reference/kotlin/android/graphics/SumPathEffect) | <br /> | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

PathEffect is the base class for objects in the Paint that affect the geometry of a drawing primitive before it is transformed by the canvas' matrix and drawn.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------|---|
| [PathEffect](https://developer.android.com/reference/kotlin/android/graphics/PathEffect#PathEffect())`()` <br /> |

| Protected methods ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](https://developer.android.com/reference/kotlin/android/graphics/PathEffect#finalize())`()` <br /> |

## Public constructors

### PathEffect

```
PathEffect()
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
