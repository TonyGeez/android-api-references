# EffectContext

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EffectContext

Kotlin| [Java](EffectContext.md) 
| --- | --- |

```
open class EffectContext
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.effect.EffectContext](EffectContext.md) |

An EffectContext keeps all necessary state information to run Effects within a Open GL ES 2.0 context.

Every EffectContext is bound to one GL context. The application is responsible for creating this EGL context, and making it current before applying any effect. If your EGL context is destroyed, the EffectContext becomes invalid and any effects bound to this context can no longer be used. If you switch to another EGL context, you must create a new EffectContext. Each Effect is bound to a single EffectContext, and can only be executed in that context.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [EffectContext](EffectContext.md)! | [createWithCurrentGlContext](EffectContext.md))`()` Creates a context within the current GL context. |
| open [EffectFactory](EffectFactory.md)! | [getFactory](EffectContext.md))`()` Returns the EffectFactory for this context. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [release](EffectContext.md))`()` Releases the context. |
| --- | --- |

## Public methods

### createWithCurrentGlContext

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun createWithCurrentGlContext(): EffectContext!
```

Creates a context within the current GL context.

Binds the EffectContext to the current OpenGL context. All subsequent calls to the EffectContext must be made in the GL context that was active during creation. When you have finished using a context, you must call [release()](EffectContext.md)). to dispose of all resources associated with this context. 

### getFactory

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFactory(): EffectFactory!
```

Returns the EffectFactory for this context.

The EffectFactory returned from this method allows instantiating new effects within this context.

| Return ||
|-----------------------------------------------------------------------------------------------------|----------------------------------------------|
| [EffectFactory](EffectFactory.md)! | The EffectFactory instance for this context. |

### release

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun release(): Unit
```

Releases the context.

Releases all the resources and effects associated with the EffectContext. This renders the context and all the effects bound to this context invalid. You must no longer use the context or any of its bound effects after calling release().

Note that this method must be called with the proper EGL context made current, as the EffectContext and its effects may release internal GL resources.
