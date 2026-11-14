Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AnimationUtils

```
open class AnimationUtils
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.view.animation.AnimationUtils](https://developer.android.com/reference/kotlin/android/view/animation/AnimationUtils#) |

Defines common utilities for working with animations.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/animation/AnimationUtils#AnimationUtils()()` <br /> |

| Public methods ||
|---|---|
| open static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/view/animation/AnimationUtils#currentAnimationTimeMillis()()` Returns the current animation time in milliseconds. |
| open static [Animation](https://developer.android.com/reference/kotlin/android/view/animation/Animation)! | `https://developer.android.com/reference/kotlin/android/view/animation/AnimationUtils#loadAnimation(android.content.Context,%20kotlin.Int)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!, id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Loads an `https://developer.android.com/reference/kotlin/android/view/animation/Animation` object from a resource |
| open static [Interpolator](https://developer.android.com/reference/kotlin/android/view/animation/Interpolator)! | `https://developer.android.com/reference/kotlin/android/view/animation/AnimationUtils#loadInterpolator(android.content.Context,%20kotlin.Int)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!, id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Loads an `https://developer.android.com/reference/kotlin/android/view/animation/Interpolator` object from a resource |
| open static [LayoutAnimationController](https://developer.android.com/reference/kotlin/android/view/animation/LayoutAnimationController)! | `https://developer.android.com/reference/kotlin/android/view/animation/AnimationUtils#loadLayoutAnimation(android.content.Context,%20kotlin.Int)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!, id: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Loads a `https://developer.android.com/reference/kotlin/android/view/animation/LayoutAnimationController` object from a resource |
| open static [Animation](https://developer.android.com/reference/kotlin/android/view/animation/Animation)! | `https://developer.android.com/reference/kotlin/android/view/animation/AnimationUtils#makeInAnimation(android.content.Context,%20kotlin.Boolean)(c: https://developer.android.com/reference/kotlin/android/content/Context.html#!, fromLeft: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Make an animation for objects becoming visible. |
| open static [Animation](https://developer.android.com/reference/kotlin/android/view/animation/Animation)! | `https://developer.android.com/reference/kotlin/android/view/animation/AnimationUtils#makeInChildBottomAnimation(android.content.Context)(c: https://developer.android.com/reference/kotlin/android/content/Context.html#!)` Make an animation for objects becoming visible. |
| open static [Animation](https://developer.android.com/reference/kotlin/android/view/animation/Animation)! | `https://developer.android.com/reference/kotlin/android/view/animation/AnimationUtils#makeOutAnimation(android.content.Context,%20kotlin.Boolean)(c: https://developer.android.com/reference/kotlin/android/content/Context.html#!, toRight: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Make an animation for objects becoming invisible. |

## Public constructors

### AnimationUtils

```
AnimationUtils()
```

## Public methods

### currentAnimationTimeMillis

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun currentAnimationTimeMillis(): Long
```

Returns the current animation time in milliseconds. This time should be used when invoking `https://developer.android.com/reference/kotlin/android/view/animation/Animation#setStartTime(kotlin.Long)`. Refer to `https://developer.android.com/reference/kotlin/android/os/SystemClock.html#` for more information about the different available clocks. The clock used by this method is *not* the "wall" clock (it is not `https://developer.android.com/reference/kotlin/java/lang/System.html#currentTimeMillis()`).

Do not use this method for animation progress or with `https://developer.android.com/reference/kotlin/android/animation/Animator.html#`. Using this timestamp for animations will introduce undersirable animation skips after missed frames. Use #getAnimationTimeNanos() instead.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the current animation time in milliseconds |

**See Also**

- `https://developer.android.com/reference/kotlin/android/os/SystemClock.html#`

### loadAnimation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun loadAnimation(
    context: Context!, 
    id: Int
): Animation!
```

Loads an `https://developer.android.com/reference/kotlin/android/view/animation/Animation` object from a resource

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!: Application context used to access resources |
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The resource id of the animation to load |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/animation/Animation!` | The animation object referenced by the specified id |

| Exceptions ||
|---|---|
| `android.content.res.Resources.NotFoundException` | when the animation cannot be loaded |

### loadInterpolator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun loadInterpolator(
    context: Context!, 
    id: Int
): Interpolator!
```

Loads an `https://developer.android.com/reference/kotlin/android/view/animation/Interpolator` object from a resource

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!: Application context used to access resources |
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The resource id of the animation to load |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/animation/Interpolator!` | The interpolator object referenced by the specified id |

| Exceptions ||
|---|---|
| `android.content.res.Resources.NotFoundException` | |

### loadLayoutAnimation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun loadLayoutAnimation(
    context: Context!, 
    id: Int
): LayoutAnimationController!
```

Loads a `https://developer.android.com/reference/kotlin/android/view/animation/LayoutAnimationController` object from a resource

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!: Application context used to access resources |
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The resource id of the animation to load |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/animation/LayoutAnimationController!` | The animation controller object referenced by the specified id |

| Exceptions ||
|---|---|
| `android.content.res.Resources.NotFoundException` | when the layout animation controller cannot be loaded |

### makeInAnimation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun makeInAnimation(
    c: Context!, 
    fromLeft: Boolean
): Animation!
```

Make an animation for objects becoming visible. Uses a slide and fade effect.

| Parameters ||
|---|---|
| `c` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!: Context for loading resources |
| `fromLeft` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): is the object to be animated coming from the left |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/animation/Animation!` | The new animation |

### makeInChildBottomAnimation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun makeInChildBottomAnimation(c: Context!): Animation!
```

Make an animation for objects becoming visible. Uses a slide up and fade effect.

| Parameters ||
|---|---|
| `c` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!: Context for loading resources |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/animation/Animation!` | The new animation |

### makeOutAnimation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun makeOutAnimation(
    c: Context!, 
    toRight: Boolean
): Animation!
```

Make an animation for objects becoming invisible. Uses a slide and fade effect.

| Parameters ||
|---|---|
| `c` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!: Context for loading resources |
| `toRight` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): is the object to be animated exiting to the right |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/animation/Animation!` | The new animation |
