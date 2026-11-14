# EffectUpdateListener

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EffectUpdateListener

Kotlin| [Java](../android/media/effect/EffectUpdateListener.md) 
| --- | --- |

```
interface EffectUpdateListener
```

| [android.media.effect.EffectUpdateListener](../android/media/effect/EffectUpdateListener.md) |

Some effects may issue callbacks to inform the host of changes to the effect state. This is the listener interface for receiving those callbacks.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onEffectUpdated](../android/media/effect/EffectUpdateListener.md))`(`effect:` ` [Effect](../android/media/effect/Effect.md)!`, `info:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Called when the effect state is updated. |

## Public methods

### onEffectUpdated

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onEffectUpdated(
    effect: Effect!, 
    info: Any!
): Unit
```

Called when the effect state is updated.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `effect` | [Effect](../android/media/effect/Effect.md)!:The effect that has been updated. |
| `info` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:A value that gives more information about the update. See the effect's documentation for more details on what this object is. |
