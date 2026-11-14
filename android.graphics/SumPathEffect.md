# SumPathEffect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SumPathEffect

Kotlin| [Java](https://developer.android.com/reference/android/graphics/SumPathEffect "View this page in Java") 

```
open class SumPathEffect : PathEffect
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [android.graphics.PathEffect](https://developer.android.com/reference/kotlin/android/graphics/PathEffect) ||
| | ↳ | [android.graphics.SumPathEffect](https://developer.android.com/reference/kotlin/android/graphics/SumPathEffect#) |

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SumPathEffect](https://developer.android.com/reference/kotlin/android/graphics/SumPathEffect#SumPathEffect(android.graphics.PathEffect,%20android.graphics.PathEffect))`(`first:` ` [PathEffect](https://developer.android.com/reference/kotlin/android/graphics/PathEffect)!`, `second:` ` [PathEffect](https://developer.android.com/reference/kotlin/android/graphics/PathEffect)!`)` Construct a PathEffect whose effect is to apply two effects, in sequence. |

| Inherited functions ||
|---|---|
| From class [PathEffect](https://developer.android.com/reference/kotlin/android/graphics/PathEffect) |------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](https://developer.android.com/reference/kotlin/android/graphics/PathEffect#finalize())`()` <br /> | ||

## Public constructors

### SumPathEffect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SumPathEffect(
    first: PathEffect!, 
    second: PathEffect!)
```

Construct a PathEffect whose effect is to apply two effects, in sequence. (e.g. first(path) + second(path))
