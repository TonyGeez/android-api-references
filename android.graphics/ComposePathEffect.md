# ComposePathEffect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ComposePathEffect

Kotlin | [Java](../android/graphics/ComposePathEffect.md) 
| --- | --- |

```
open class ComposePathEffect : PathEffect
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.graphics.PathEffect](../android/graphics/PathEffect.md) ||
| | ↳ | [android.graphics.ComposePathEffect](../android/graphics/ComposePathEffect.md) |

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ComposePathEffect](../android/graphics/ComposePathEffect.md))`(`outerpe:` ` [PathEffect](../android/graphics/PathEffect.md)!`, `innerpe:` ` [PathEffect](../android/graphics/PathEffect.md)!`)` Construct a PathEffect whose effect is to apply first the inner effect and the outer pathEffect (e.g. outer(inner(path))). |

| Inherited functions ||
|---|---|
| From class [PathEffect](../android/graphics/PathEffect.md) |------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](../android/graphics/PathEffect.md))`()` <br /> | ||

## Public constructors

### ComposePathEffect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ComposePathEffect(
    outerpe: PathEffect!, 
    innerpe: PathEffect!)
```

Construct a PathEffect whose effect is to apply first the inner effect and the outer pathEffect (e.g. outer(inner(path))).
