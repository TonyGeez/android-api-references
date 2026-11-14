# SumPathEffect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SumPathEffect

Kotlin| [Java](SumPathEffect.md) 
| --- | --- |

```
open class SumPathEffect : PathEffect
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.graphics.PathEffect](PathEffect.md) ||
| | ↳ | [android.graphics.SumPathEffect](SumPathEffect.md) |

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SumPathEffect](SumPathEffect.md))`(`first:` ` [PathEffect](PathEffect.md)!`, `second:` ` [PathEffect](PathEffect.md)!`)` Construct a PathEffect whose effect is to apply two effects, in sequence. |

| Inherited functions ||
|---|---|
| From class [PathEffect](PathEffect.md) |------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](PathEffect.md))`()` <br /> | ||

## Public constructors

### SumPathEffect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SumPathEffect(
    first: PathEffect!, 
    second: PathEffect!)
```

Construct a PathEffect whose effect is to apply two effects, in sequence. (e.g. first(path) + second(path))
