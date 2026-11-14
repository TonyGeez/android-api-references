Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AnimatorSet

Kotlin | [Java](AnimatorSet.md)
| --- | --- |

```
class AnimatorSet : Animator
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.animation.Animator](Animator.md) ||
| | ↳ | [android.animation.AnimatorSet](AnimatorSet.md) |

This class plays a set of `https://developer.android.com/reference/kotlin/android/animation/Animator` objects in the specified order. Animations can be set up to play together, in sequence, or after a specified delay.

There are two different approaches to adding animations to a `AnimatorSet`: either the `https://developer.android.com/reference/kotlin/android/animation/AnimatorSet#playTogether(android.animation.Animator)` or `https://developer.android.com/reference/kotlin/android/animation/AnimatorSet#playSequentially(android.animation.Animator)` methods can be called to add a set of animations all at once, or the `https://developer.android.com/reference/kotlin/android/animation/AnimatorSet#play(android.animation.Animator)` can be used in conjunction with methods in the `https://developer.android.com/reference/kotlin/android/animation/AnimatorSet.Builder` class to add animations one by one.

It is possible to set up a `AnimatorSet` with circular dependencies between its animations. For example, an animation a1 could be set up to start before animation a2, a2 before a3, and a3 before a1. The results of this configuration are undefined, but will typically result in none of the affected animations being played. Because of this (and because circular dependencies do not make logical sense anyway), circular dependencies should be avoided, and the dependency flow of animations should only be in one direction.
|
| ### Developer Guides
|
| For more information about animating with `AnimatorSet`, read the [Property Animation](https://developer.android.com/guide/topics/graphics/prop-animation.html#choreography) developer guide.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/animation/AnimatorSet.Builder` The `Builder` object is a utility class to facilitate adding animations to a `AnimatorSet` along with the relationships between the various animations. |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/animation/Animator` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | `https://developer.android.com/reference/kotlin/android/animation/Animator#DURATION_INFINITE:kotlin.Long` The value used to indicate infinite duration (e.g. when Animators repeat infinitely). <br /> | ||

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/animation/AnimatorSet#AnimatorSet()()` <br /> |

| Public methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/animation/AnimatorSet#cancel()()` Cancels the animation. |
| [AnimatorSet](AnimatorSet.md) | `https://developer.android.com/reference/kotlin/android/animation/AnimatorSet#clone()()` Creates and returns a copy of this object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/animation/AnimatorSet#end()()` Ends the animation. |
| --- | --- |
| [ArrayList](../java.util/ArrayList.md)\< [Animator](Animator.md)!\>! | `https://developer.android.com/reference/kotlin/android/animation/AnimatorSet#getChildAnimations()()` Returns the current list of child Animator objects controlled by this AnimatorSet. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/animation/AnimatorSet#getCurrentPlayTime()()` Returns the milliseconds elapsed since the start of the animation. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/animation/AnimatorSet#getDuration()()` Gets the length of each of the child animations of this AnimatorSet. |
| --- | --- |
| [TimeInterpolator](TimeInterpolator.md)! | `https://developer.android.com/reference/kotlin/android/animation/AnimatorSet#getInterpolator()()` Returns the timing interpolator that this animation uses. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/animation/AnimatorSet#getStartDelay()()` The amount of time, in milliseconds, to delay starting the animation after `https://developer.android.com/reference/kotlin/android/animation/AnimatorSet#start()` is called. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/animation/AnimatorSet#getTotalDuration()()` Gets the total duration of the animation, accounting for animation sequences, start delay, and repeating. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/animation/AnimatorSet#isRunning()()` Returns true if any of the child animations of this AnimatorSet have been started and have not yet ended. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/animation/AnimatorSet#isStarted()()` Returns whether this Animator has been started and not yet ended. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/animation/AnimatorSet#pause()()` Pauses a running animation. |
| --- | --- |
| [AnimatorSet.Builder](../android/animation/AnimatorSet.Builder.md)! | `https://developer.android.com/reference/kotlin/android/animation/AnimatorSet#play(android.animation.Animator)(anim: https://developer.android.com/reference/kotlin/android/animation/Animator!)` This method creates a `Builder` object, which is used to set up playing constraints. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/animation/AnimatorSet#playSequentially(android.animation.Animator)(vararg items: https://developer.android.com/reference/kotlin/android/animation/Animator!)` Sets up this AnimatorSet to play each of the supplied animations when the previous animation ends. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/animation/AnimatorSet#playSequentially(kotlin.collections.MutableList)(items: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/animation/Animator!>!)` Sets up this AnimatorSet to play each of the supplied animations when the previous animation ends. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/animation/AnimatorSet#playTogether(android.animation.Animator)(vararg items: https://developer.android.com/reference/kotlin/android/animation/Animator!)` Sets up this AnimatorSet to play all of the supplied animations at the same time. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/animation/AnimatorSet#playTogether(kotlin.collections.MutableCollection)(items: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<https://developer.android.com/reference/kotlin/android/animation/Animator!>!)` Sets up this AnimatorSet to play all of the supplied animations at the same time. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/animation/AnimatorSet#resume()()` Resumes a paused animation, causing the animator to pick up where it left off when it was paused. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/animation/AnimatorSet#reverse()()` Plays the AnimatorSet in reverse. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/animation/AnimatorSet#setCurrentPlayTime(kotlin.Long)(playTime: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Sets the position of the animation to the specified point in time. |
| [AnimatorSet](AnimatorSet.md)! | `https://developer.android.com/reference/kotlin/android/animation/AnimatorSet#setDuration(kotlin.Long)(duration: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Sets the length of each of the current child animations of this AnimatorSet. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/animation/AnimatorSet#setInterpolator(android.animation.TimeInterpolator)(interpolator: https://developer.android.com/reference/kotlin/android/animation/TimeInterpolator!)` Sets the TimeInterpolator for all current `https://developer.android.com/reference/kotlin/android/animation/AnimatorSet#getChildAnimations()` of this AnimatorSet. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/animation/AnimatorSet#setStartDelay(kotlin.Long)(startDelay: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` The amount of time, in milliseconds, to delay starting the animation after `https://developer.android.com/reference/kotlin/android/animation/AnimatorSet#start()` is called. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/animation/AnimatorSet#setTarget(kotlin.Any)(target: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Sets the target object for all current `https://developer.android.com/reference/kotlin/android/animation/AnimatorSet#getChildAnimations()` of this AnimatorSet that take targets (`https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator` and AnimatorSet). |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/animation/AnimatorSet#setupEndValues()()` This method tells the object to use appropriate information to extract ending values for the animation. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/animation/AnimatorSet#setupStartValues()()` This method tells the object to use appropriate information to extract starting values for the animation. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/animation/AnimatorSet#start()()` Starts this animation. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/animation/AnimatorSet#toString()()` Returns a string representation of the object. |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/animation/Animator` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/animation/Animator#addListener(android.animation.Animator.AnimatorListener)(listener: https://developer.android.com/reference/kotlin/android/animation/Animator.AnimatorListener!)` Adds a listener to the set of listeners that are sent events through the life of an animation, such as start, repeat, and end. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/animation/Animator#addPauseListener(android.animation.Animator.AnimatorPauseListener)(listener: https://developer.android.com/reference/kotlin/android/animation/Animator.AnimatorPauseListener!)` Adds a pause listener to this animator. <br /> | | `https://developer.android.com/reference/kotlin/java/util/ArrayList.html#<https://developer.android.com/reference/kotlin/android/animation/Animator.AnimatorListener!>!` | `https://developer.android.com/reference/kotlin/android/animation/Animator#getListeners()()` Gets the set of `https://developer.android.com/reference/kotlin/android/animation/Animator.AnimatorListener` objects that are currently listening for events on this `Animator` object. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/animation/Animator#isPaused()()` Returns whether this animator is currently in a paused state. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/animation/Animator#removeAllListeners()()` Removes all `https://developer.android.com/reference/kotlin/android/animation/Animator#addListener(android.animation.Animator.AnimatorListener)` and `https://developer.android.com/reference/kotlin/android/animation/Animator#addPauseListener(android.animation.Animator.AnimatorPauseListener)` from this object. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/animation/Animator#removeListener(android.animation.Animator.AnimatorListener)(listener: https://developer.android.com/reference/kotlin/android/animation/Animator.AnimatorListener!)` Removes a listener from the set listening to this animation. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/animation/Animator#removePauseListener(android.animation.Animator.AnimatorPauseListener)(listener: https://developer.android.com/reference/kotlin/android/animation/Animator.AnimatorPauseListener!)` Removes a pause listener from the set listening to this animation. <br /> | ||

## Public constructors

### AnimatorSet

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
AnimatorSet()
```

## Public methods

### cancel

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun cancel(): Unit
```

Cancels the animation. Unlike `https://developer.android.com/reference/kotlin/android/animation/Animator#end()`, `cancel()` causes the animation to stop in its tracks, sending an `https://developer.android.com/reference/kotlin/android/animation/Animator.AnimatorListener#onAnimationCancel(android.animation.Animator)` to its listeners, followed by an `https://developer.android.com/reference/kotlin/android/animation/Animator.AnimatorListener#onAnimationEnd(android.animation.Animator)` message.

This method must be called on the thread that is running the animation.

Note that canceling a `AnimatorSet` also cancels all of the animations that it is responsible for.

### clone

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun clone(): AnimatorSet
```

Creates and returns a copy of this object. The precise meaning of "copy" may depend on the class of the object. The general intent is that, for any object `x`, the expression:

```kotlin
x.clone() != x
```
will be true, and that the expression:

```kotlin
x.clone().getClass() == x.getClass()
```
will be `true`, but these are not absolute requirements. While it is typically the case that:

```kotlin
x.clone().equals(x)
```
will be `true`, this is not an absolute requirement.

<br />

By convention, the returned object should be obtained by calling `super.clone`. If a class and all of its superclasses (except `Object`) obey this convention, it will be the case that `x.clone().getClass() == x.getClass()`.

By convention, the object returned by this method should be independent of this object (which is being cloned). To achieve this independence, it may be necessary to modify one or more fields of the object returned by `super.clone` before returning it. Typically, this means copying any mutable objects that comprise the internal "deep structure" of the object being cloned and replacing the references to these objects with references to the copies. If a class contains only primitive fields or references to immutable objects, then it is usually the case that no fields in the object returned by `super.clone` need to be modified.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/animation/AnimatorSet#` | a clone of this instance. |

| Exceptions ||
|---|---|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the `Cloneable` interface. Subclasses that override the `clone` method can also throw this exception to indicate that an instance cannot be cloned. |

### end

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun end(): Unit
```

Ends the animation. This causes the animation to assign the end value of the property being animated, then calling the `https://developer.android.com/reference/kotlin/android/animation/Animator.AnimatorListener#onAnimationEnd(android.animation.Animator)` method on its listeners.

This method must be called on the thread that is running the animation.

Note that ending a `AnimatorSet` also ends all of the animations that it is responsible for.

### getChildAnimations

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getChildAnimations(): ArrayList<Animator!>!
```

Returns the current list of child Animator objects controlled by this AnimatorSet. This is a copy of the internal list; modifications to the returned list will not affect the AnimatorSet, although changes to the underlying Animator objects will affect those objects being managed by the AnimatorSet.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/ArrayList.html#<https://developer.android.com/reference/kotlin/android/animation/Animator!>!` | ArrayList The list of child animations of this AnimatorSet. |

### getCurrentPlayTime

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCurrentPlayTime(): Long
```

Returns the milliseconds elapsed since the start of the animation.

For ongoing animations, this method returns the current progress of the animation in terms of play time. For an animation that has not yet been started: if the animation has been seeked to a certain time via `https://developer.android.com/reference/kotlin/android/animation/AnimatorSet#setCurrentPlayTime(kotlin.Long)`, the seeked play time will be returned; otherwise, this method will return 0.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the current position in time of the animation in milliseconds |

### getDuration

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDuration(): Long
```

Gets the length of each of the child animations of this AnimatorSet. This value may be less than 0, which indicates that no duration has been set on this AnimatorSet and each of the child animations will use their own duration.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | The length of the animation, in milliseconds, of each of the child animations of this AnimatorSet. |

### getInterpolator

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getInterpolator(): TimeInterpolator!
```

Returns the timing interpolator that this animation uses.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/animation/TimeInterpolator!` | The timing interpolator for this animation. |

### getStartDelay

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getStartDelay(): Long
```

The amount of time, in milliseconds, to delay starting the animation after `https://developer.android.com/reference/kotlin/android/animation/AnimatorSet#start()` is called.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the number of milliseconds to delay running the animation |

### getTotalDuration

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTotalDuration(): Long
```

Gets the total duration of the animation, accounting for animation sequences, start delay, and repeating. Return `https://developer.android.com/reference/kotlin/android/animation/Animator#DURATION_INFINITE:kotlin.Long` if the duration is infinite.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | Total time an animation takes to finish, starting from the time `https://developer.android.com/reference/kotlin/android/animation/Animator#start()` is called. `https://developer.android.com/reference/kotlin/android/animation/Animator#DURATION_INFINITE:kotlin.Long` will be returned if the animation or any child animation repeats infinite times. |

### isRunning

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isRunning(): Boolean
```

Returns true if any of the child animations of this AnimatorSet have been started and have not yet ended. Child animations will not be started until the AnimatorSet has gone past its initial delay set through `https://developer.android.com/reference/kotlin/android/animation/AnimatorSet#setStartDelay(kotlin.Long)`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Whether this AnimatorSet has gone past the initial delay, and at least one child animation has been started and not yet ended. |

### isStarted

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isStarted(): Boolean
```

Returns whether this Animator has been started and not yet ended. For reusable Animators (which most Animators are, apart from the one-shot animator produced by `https://developer.android.com/reference/kotlin/android/view/ViewAnimationUtils.html#createCircularReveal(android.view.View,%20kotlin.Int,%20kotlin.Int,%20kotlin.Float,%20kotlin.Float)`), this state is a superset of `https://developer.android.com/reference/kotlin/android/animation/Animator#isRunning()`, because an Animator with a nonzero `https://developer.android.com/reference/kotlin/android/animation/Animator#getStartDelay()` will return true for `https://developer.android.com/reference/kotlin/android/animation/Animator#isStarted()` during the delay phase, whereas `https://developer.android.com/reference/kotlin/android/animation/Animator#isRunning()` will return true only after the delay phase is complete. Non-reusable animators will always return true after they have been started, because they cannot return to a non-started state.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Whether the Animator has been started and not yet ended. |

### pause

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun pause(): Unit
```

Pauses a running animation. This method should only be called on the same thread on which the animation was started. If the animation has not yet been `https://developer.android.com/reference/kotlin/android/animation/Animator#isStarted()` or has since ended, then the call is ignored. Paused animations can be resumed by calling `https://developer.android.com/reference/kotlin/android/animation/Animator#resume()`.

### play

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun play(anim: Animator!): AnimatorSet.Builder!
```

This method creates a `Builder` object, which is used to set up playing constraints. This initial `play()` method tells the `Builder` the animation that is the dependency for the succeeding commands to the `Builder`. For example, calling `play(a1).with(a2)` sets up the AnimatorSet to play `a1` and `a2` at the same time, `play(a1).before(a2)` sets up the AnimatorSet to play `a1` first, followed by `a2`, and `play(a1).after(a2)` sets up the AnimatorSet to play `a2` first, followed by `a1`.

Note that `play()` is the only way to tell the `Builder` the animation upon which the dependency is created, so successive calls to the various functions in `Builder` will all refer to the initial parameter supplied in `play()` as the dependency of the other animations. For example, calling `play(a1).before(a2).before(a3)` will play both `a2` and `a3` when a1 ends; it does not set up a dependency between `a2` and `a3`.

| Parameters ||
|---|---|
| `anim` | [Animator](Animator.md)!: The animation that is the dependency used in later calls to the methods in the returned `Builder` object. A null parameter will result in a null `Builder` return value. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/animation/AnimatorSet.Builder!` | Builder The object that constructs the AnimatorSet based on the dependencies outlined in the calls to `play` and the other methods in the `Builder` |

### playSequentially

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun playSequentially(vararg items: Animator!): Unit
```

Sets up this AnimatorSet to play each of the supplied animations when the previous animation ends.

| Parameters ||
|---|---|
| `items` | [Animator](Animator.md)!: The animations that will be started one after another. |

### playSequentially

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun playSequentially(items: MutableList<Animator!>!): Unit
```

Sets up this AnimatorSet to play each of the supplied animations when the previous animation ends.

| Parameters ||
|---|---|
| `items` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Animator](Animator.md)!\>!: The animations that will be started one after another. |

### playTogether

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun playTogether(vararg items: Animator!): Unit
```

Sets up this AnimatorSet to play all of the supplied animations at the same time. This is equivalent to calling `https://developer.android.com/reference/kotlin/android/animation/AnimatorSet#play(android.animation.Animator)` with the first animator in the set and then `https://developer.android.com/reference/kotlin/android/animation/AnimatorSet.Builder#with(android.animation.Animator)` with each of the other animators. Note that an Animator with a `https://developer.android.com/reference/kotlin/android/animation/Animator#setStartDelay(kotlin.Long)` will not actually start until that delay elapses, which means that if the first animator in the list supplied to this constructor has a startDelay, none of the other animators will start until that first animator's startDelay has elapsed.

| Parameters ||
|---|---|
| `items` | [Animator](Animator.md)!: The animations that will be started simultaneously. |

### playTogether

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun playTogether(items: MutableCollection<Animator!>!): Unit
```

Sets up this AnimatorSet to play all of the supplied animations at the same time.

| Parameters ||
|---|---|
| `items` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [Animator](Animator.md)!\>!: The animations that will be started simultaneously. |

### resume

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun resume(): Unit
```

Resumes a paused animation, causing the animator to pick up where it left off when it was paused. This method should only be called on the same thread on which the animation was started. Calls to resume() on an animator that is not currently paused will be ignored.

### reverse

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun reverse(): Unit
```

Plays the AnimatorSet in reverse. If the animation has been seeked to a specific play time using `https://developer.android.com/reference/kotlin/android/animation/AnimatorSet#setCurrentPlayTime(kotlin.Long)`, it will play backwards from the point seeked when reverse was called. Otherwise, then it will start from the end and play backwards. This behavior is only set for the current animation; future playing of the animation will use the default behavior of playing forward.

Note: reverse is not supported for infinite AnimatorSet.

### setCurrentPlayTime

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setCurrentPlayTime(playTime: Long): Unit
```

Sets the position of the animation to the specified point in time. This time should be between 0 and the total duration of the animation, including any repetition. If the animation has not yet been started, then it will not advance forward after it is set to this time; it will simply set the time to this value and perform any appropriate actions based on that time. If the animation is already running, then setCurrentPlayTime() will set the current playing time to this value and continue playing from that point. On `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int` and above, an AnimatorSet that hasn't been `https://developer.android.com/reference/kotlin/android/animation/AnimatorSet#start()`ed, will issue `https://developer.android.com/reference/kotlin/android/animation/Animator.AnimatorListener#onAnimationStart(android.animation.Animator,%20kotlin.Boolean)` and `https://developer.android.com/reference/kotlin/android/animation/Animator.AnimatorListener#onAnimationEnd(android.animation.Animator,%20kotlin.Boolean)` events.

| Parameters ||
|---|---|
| `playTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The time, in milliseconds, to which the animation is advanced or rewound. Unless the animation is reversing, the playtime is considered the time since the end of the start delay of the AnimatorSet in a forward playing direction. |

### setDuration

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setDuration(duration: Long): AnimatorSet!
```

Sets the length of each of the current child animations of this AnimatorSet. By default, each child animation will use its own duration. If the duration is set on the AnimatorSet, then each child animation inherits this duration.

| Parameters ||
|---|---|
| `duration` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The length of the animation, in milliseconds, of each of the child animations of this AnimatorSet. |

### setInterpolator

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setInterpolator(interpolator: TimeInterpolator!): Unit
```

Sets the TimeInterpolator for all current `https://developer.android.com/reference/kotlin/android/animation/AnimatorSet#getChildAnimations()` of this AnimatorSet. The default value is null, which means that no interpolator is set on this AnimatorSet. Setting the interpolator to any non-null value will cause that interpolator to be set on the child animations when the set is started.

| Parameters ||
|---|---|
| `value` | the interpolator to be used by this animation |
| `interpolator` | [TimeInterpolator](TimeInterpolator.md)!: the interpolator to be used by each child animation of this AnimatorSet |

### setStartDelay

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setStartDelay(startDelay: Long): Unit
```

The amount of time, in milliseconds, to delay starting the animation after `https://developer.android.com/reference/kotlin/android/animation/AnimatorSet#start()` is called. Note that the start delay should always be non-negative. Any negative start delay will be clamped to 0 on N and above.

| Parameters ||
|---|---|
| `startDelay` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The amount of the delay, in milliseconds |

### setTarget

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setTarget(target: Any?): Unit
```

Sets the target object for all current `https://developer.android.com/reference/kotlin/android/animation/AnimatorSet#getChildAnimations()` of this AnimatorSet that take targets (`https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator` and AnimatorSet).

| Parameters ||
|---|---|
| `target` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?: The object being animated |

### setupEndValues

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setupEndValues(): Unit
```

This method tells the object to use appropriate information to extract ending values for the animation. For example, a AnimatorSet object will pass this call to its child objects to tell them to set up the values. A ObjectAnimator object will use the information it has about its target object and PropertyValuesHolder objects to get the start values for its properties. A ValueAnimator object will ignore the request since it does not have enough information (such as a target object) to gather these values.

### setupStartValues

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setupStartValues(): Unit
```

This method tells the object to use appropriate information to extract starting values for the animation. For example, a AnimatorSet object will pass this call to its child objects to tell them to set up the values. A ObjectAnimator object will use the information it has about its target object and PropertyValuesHolder objects to get the start values for its properties. A ValueAnimator object will ignore the request since it does not have enough information (such as a target object) to gather these values.

### start

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun start(): Unit
```

Starts this animation. If the animation has a nonzero startDelay, the animation will start running after that delay elapses. A non-delayed animation will have its initial value(s) set immediately, followed by calls to `https://developer.android.com/reference/kotlin/android/animation/Animator.AnimatorListener#onAnimationStart(android.animation.Animator)` for any listeners of this animator.

The animation started by calling this method will be run on the thread that called this method. This thread should have a Looper on it (a runtime exception will be thrown if this is not the case). Also, if the animation will animate properties of objects in the view hierarchy, then the calling thread should be the UI thread for that view hierarchy.

Starting this `AnimatorSet` will, in turn, start the animations for which it is responsible. The details of when exactly those animations are started depends on the dependency relationships that have been set up between the animations. **Note:** Manipulating AnimatorSet's lifecycle in the child animators' listener callbacks will lead to undefined behaviors. Also, AnimatorSet will ignore any seeking in the child animators once `https://developer.android.com/reference/kotlin/android/animation/AnimatorSet#start()` is called.

### toString

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |
