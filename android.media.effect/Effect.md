Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Effect

Kotlin | [Java](Effect.md)
| --- | --- |

```
abstract class Effect
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.effect.Effect](Effect.md) |

Effects are high-performance transformations that can be applied to image frames. These are passed in the form of OpenGL ES 2.0 texture names. Typical frames could be images loaded from disk, or frames from the camera or other video streams.

To create an Effect you must first create an EffectContext. You can obtain an instance of the context's EffectFactory by calling getFactory. The EffectFactory allows you to instantiate specific Effects.

The application is responsible for creating an EGL context, and making it current before applying an effect. An effect is bound to a single EffectContext, which in turn is bound to a single EGL context. If your EGL context is destroyed, the EffectContext becomes invalid and any effects bound to this context can no longer be used.

## Summary

| Public constructors ||
|---|---|
| Effect <br /> |

| Public methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | apply Apply an effect to GL textures. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getName Get the effect name. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | release Release an effect. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setParameter Set a filter parameter. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setUpdateListener Set an effect listener. |

## Public constructors

### Effect

```
Effect()
```

## Public methods

### apply

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun apply(
    inputTexId: Int, 
    width: Int, 
    height: Int, 
    outputTexId: Int
): Unit
```

Apply an effect to GL textures.

Apply the Effect on the specified input GL texture, and write the result into the output GL texture. The texture names passed must be valid in the current GL context.

The input texture must be a valid texture name with the given width and height and must be bound to a GL_TEXTURE_2D texture image (usually done by calling the glTexImage2D() function). Multiple mipmap levels may be provided.

If the output texture has not been bound to a texture image, it will be automatically bound by the effect as a GL_TEXTURE_2D. It will contain one mipmap level (0), which will have the same size as the input. No other mipmap levels are defined. If the output texture was bound already, and its size does not match the input texture size, the result may be clipped or only partially fill the texture.

Note, that regardless of whether a texture image was originally provided or not, both the input and output textures are owned by the caller. That is, the caller is responsible for calling glDeleteTextures() to deallocate the input and output textures.

| Parameters ||
|---|---|
| `inputTexId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The GL texture name of a valid and bound input texture. |
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The width of the input texture in pixels. |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The height of the input texture in pixels. |
| --- | --- |
| `outputTexId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The GL texture name of the output texture. |

### getName

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getName(): String!
```

Get the effect name. Returns the unique name of the effect, which matches the name used for instantiating this effect by the EffectFactory.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | The name of the effect. |

### release

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun release(): Unit
```

Release an effect.

Releases the effect and any resources associated with it. You may call this if you need to make sure acquired resources are no longer held by the effect. Releasing an effect makes it invalid for reuse.

Note that this method must be called with the EffectContext and EGL context current, as the effect may release internal GL resources.

### setParameter

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setParameter(
    parameterKey: String!, 
    value: Any!
): Unit
```

Set a filter parameter. Consult the effect documentation for a list of supported parameter keys for each effect.

| Parameters ||
|---|---|
| `parameterKey` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The name of the parameter to adjust. |
| `value` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: The new value to set the parameter to. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if parameterName is not a recognized name, or the value is not a valid value for this parameter. |

### setUpdateListener

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setUpdateListener(listener: EffectUpdateListener!): Unit
```

Set an effect listener. Some effects may report state changes back to the host, if a listener is set. Consult the individual effect documentation for more details.

| Parameters ||
|---|---|
| `listener` | [EffectUpdateListener](EffectUpdateListener.md)!: The listener to receive update callbacks on. |
