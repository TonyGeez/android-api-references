# PathEffect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PathEffect

Kotlin| [Java](../android/graphics/PathEffect.md) 
| --- | --- |

```
open class PathEffect
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.PathEffect](../android/graphics/PathEffect.md) |

| Known Direct Subclasses [ComposePathEffect](../android/graphics/ComposePathEffect.md), [CornerPathEffect](../android/graphics/CornerPathEffect.md), [DashPathEffect](../android/graphics/DashPathEffect.md), [DiscretePathEffect](../android/graphics/DiscretePathEffect.md), [PathDashPathEffect](../android/graphics/PathDashPathEffect.md), [SumPathEffect](../android/graphics/SumPathEffect.md) |----------------------------------------------------------------------------------------------------------|--------| | [ComposePathEffect](../android/graphics/ComposePathEffect.md) | <br /> | | [CornerPathEffect](../android/graphics/CornerPathEffect.md) | <br /> | | [DashPathEffect](../android/graphics/DashPathEffect.md) | <br /> | | [DiscretePathEffect](../android/graphics/DiscretePathEffect.md) | <br /> | | [PathDashPathEffect](../android/graphics/PathDashPathEffect.md) | <br /> | | [SumPathEffect](../android/graphics/SumPathEffect.md) | <br /> | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

PathEffect is the base class for objects in the Paint that affect the geometry of a drawing primitive before it is transformed by the canvas' matrix and drawn.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------|---|
| [PathEffect](../android/graphics/PathEffect.md))`()` <br /> |

| Protected methods ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](../android/graphics/PathEffect.md))`()` <br /> |

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
