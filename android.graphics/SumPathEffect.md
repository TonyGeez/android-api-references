# SumPathEffect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SumPathEffect

Kotlin| [Java](../android/graphics/SumPathEffect.md) 
| --- | --- |

```
open class SumPathEffect : PathEffect
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.graphics.PathEffect](../android/graphics/PathEffect.md) ||
| | ↳ | [android.graphics.SumPathEffect](../android/graphics/SumPathEffect.md) |

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SumPathEffect](../android/graphics/SumPathEffect.md))`(`first:` ` [PathEffect](../android/graphics/PathEffect.md)!`, `second:` ` [PathEffect](../android/graphics/PathEffect.md)!`)` Construct a PathEffect whose effect is to apply two effects, in sequence. |

| Inherited functions ||
|---|---|
| From class [PathEffect](../android/graphics/PathEffect.md) |------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](../android/graphics/PathEffect.md))`()` <br /> | ||

## Public constructors

### SumPathEffect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SumPathEffect(
    first: PathEffect!, 
    second: PathEffect!)
```

Construct a PathEffect whose effect is to apply two effects, in sequence. (e.g. first(path) + second(path))
