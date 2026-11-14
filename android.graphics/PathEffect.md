# PathEffect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PathEffect

Kotlin| [Java](PathEffect.md) 
| --- | --- |

```
open class PathEffect
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.PathEffect](PathEffect.md) |

| Known Direct Subclasses [ComposePathEffect](ComposePathEffect.md), [CornerPathEffect](CornerPathEffect.md), [DashPathEffect](DashPathEffect.md), [DiscretePathEffect](DiscretePathEffect.md), [PathDashPathEffect](PathDashPathEffect.md), [SumPathEffect](SumPathEffect.md) |----------------------------------------------------------------------------------------------------------|--------| | [ComposePathEffect](ComposePathEffect.md) | <br /> | | [CornerPathEffect](CornerPathEffect.md) | <br /> | | [DashPathEffect](DashPathEffect.md) | <br /> | | [DiscretePathEffect](DiscretePathEffect.md) | <br /> | | [PathDashPathEffect](PathDashPathEffect.md) | <br /> | | [SumPathEffect](SumPathEffect.md) | <br /> | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

PathEffect is the base class for objects in the Paint that affect the geometry of a drawing primitive before it is transformed by the canvas' matrix and drawn.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------|---|
| [PathEffect](PathEffect.md))`()` <br /> |

| Protected methods ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](PathEffect.md))`()` <br /> |

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
