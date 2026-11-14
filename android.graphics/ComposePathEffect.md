# ComposePathEffect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ComposePathEffect

Kotlin | [Java](https://developer.android.com/reference/android/graphics/ComposePathEffect "View this page in Java") 
| --- | --- |

```
open class ComposePathEffect : PathEffect
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.graphics.PathEffect](https://developer.android.com/reference/kotlin/android/graphics/PathEffect) ||
| | ↳ | [android.graphics.ComposePathEffect](https://developer.android.com/reference/kotlin/android/graphics/ComposePathEffect#) |

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ComposePathEffect](https://developer.android.com/reference/kotlin/android/graphics/ComposePathEffect#ComposePathEffect(android.graphics.PathEffect,%20android.graphics.PathEffect))`(`outerpe:` ` [PathEffect](https://developer.android.com/reference/kotlin/android/graphics/PathEffect)!`, `innerpe:` ` [PathEffect](https://developer.android.com/reference/kotlin/android/graphics/PathEffect)!`)` Construct a PathEffect whose effect is to apply first the inner effect and the outer pathEffect (e.g. outer(inner(path))). |

| Inherited functions ||
|---|---|
| From class [PathEffect](https://developer.android.com/reference/kotlin/android/graphics/PathEffect) |------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](https://developer.android.com/reference/kotlin/android/graphics/PathEffect#finalize())`()` <br /> | ||

## Public constructors

### ComposePathEffect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ComposePathEffect(
    outerpe: PathEffect!, 
    innerpe: PathEffect!)
```

Construct a PathEffect whose effect is to apply first the inner effect and the outer pathEffect (e.g. outer(inner(path))).
