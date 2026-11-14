# ComposePathEffect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ComposePathEffect

Kotlin | [Java](ComposePathEffect.md) 
| --- | --- |

```
open class ComposePathEffect : PathEffect
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.graphics.PathEffect](PathEffect.md) ||
| | ↳ | [android.graphics.ComposePathEffect](ComposePathEffect.md) |

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ComposePathEffect](ComposePathEffect.md))`(`outerpe:` ` [PathEffect](PathEffect.md)!`, `innerpe:` ` [PathEffect](PathEffect.md)!`)` Construct a PathEffect whose effect is to apply first the inner effect and the outer pathEffect (e.g. outer(inner(path))). |

| Inherited functions ||
|---|---|
| From class [PathEffect](PathEffect.md) |------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](PathEffect.md))`()` <br /> | ||

## Public constructors

### ComposePathEffect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ComposePathEffect(
    outerpe: PathEffect!, 
    innerpe: PathEffect!)
```

Construct a PathEffect whose effect is to apply first the inner effect and the outer pathEffect (e.g. outer(inner(path))).
