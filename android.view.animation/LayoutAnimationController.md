# LayoutAnimationController

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LayoutAnimationController

Kotlin| [Java](LayoutAnimationController.md) 
| --- | --- |

```
open class LayoutAnimationController
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.animation.LayoutAnimationController](LayoutAnimationController.md) |

| Known Direct Subclasses [GridLayoutAnimationController](GridLayoutAnimationController.md) |--------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------| | [GridLayoutAnimationController](GridLayoutAnimationController.md) | A layout animation controller is used to animated a grid layout's children. | |
| --- | --- | --- | --- | --- | --- | --- |

A layout animation controller is used to animate the children of a layout or a view group. Each child uses the same animation but for every one of them, the animation starts at a different time. A layout animation controller is used by [android.view.ViewGroup](../android.view/ViewGroup.md) to compute the delay by which each child's animation start must be offset. The delay is computed by using characteristics of each child, like its index in the view group. This standard implementation computes the delay by multiplying a fixed amount of miliseconds by the index of the child in its parent view group. Subclasses are supposed to override [getDelayForView(android.view.View)](LayoutAnimationController.md))to implement a different way of computing the delay. For instance, a [android.view.animation.GridLayoutAnimationController](GridLayoutAnimationController.md) will compute the delay based on the column and row indices of the child in its parent view group. Information used to compute the animation delay of each child are stored in an instance of [android.view.animation.LayoutAnimationController.AnimationParameters](../android/view/animation/LayoutAnimationController.AnimationParameters.md), itself stored in the [android.view.ViewGroup.LayoutParams](../android/view/ViewGroup.LayoutParams.md) of the view.

## Summary

| Nested classes ||
|------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [AnimationParameters](../android/view/animation/LayoutAnimationController.AnimationParameters.md) The set of parameters that has to be attached to each view contained in the view group animated by the layout animation controller. |

| XML attributes ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [`android:animation`](LayoutAnimationController.md) | Animation to use on each child. |
| [`android:animationOrder`](LayoutAnimationController.md) | The order in which the animations will be started. |
| [`android:delay`](LayoutAnimationController.md) | Fraction of the animation duration used to delay the beginning of the animation of each child. |
| --- | --- |
| [`android:interpolator`](LayoutAnimationController.md) | Interpolator used to interpolate the delay between the start of each animation. |

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ORDER_NORMAL](LayoutAnimationController.md) Distributes the animation delays in the order in which view were added to their view group. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ORDER_RANDOM](LayoutAnimationController.md) Randomly distributes the animation delays. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ORDER_REVERSE](LayoutAnimationController.md) Distributes the animation delays in the reverse order in which view were added to their view group. |
| --- | --- |

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [LayoutAnimationController](LayoutAnimationController.md))`(`context:` ` [Context](../android.content/Context.md)!`, `attrs:` ` [AttributeSet](../android.util/AttributeSet.md)!`)` Creates a new layout animation controller from external resources. |
| [LayoutAnimationController](LayoutAnimationController.md))`(`animation:` ` [Animation](Animation.md)!`)` Creates a new layout animation controller with a delay of 50% and the specified animation. |
| [LayoutAnimationController](LayoutAnimationController.md))`(`animation:` ` [Animation](Animation.md)!`, `delay:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Creates a new layout animation controller with the specified delay and the specified animation. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Animation](Animation.md)! | [getAnimation](LayoutAnimationController.md))`()` Returns the animation applied to each child of the view group on which this controller is set. |
| [Animation](Animation.md)! | [getAnimationForView](LayoutAnimationController.md))`(`view:` ` [View](../android.view/View.md)!`)` Returns the animation to be applied to the specified view. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getDelay](LayoutAnimationController.md))`()` Returns the delay by which the children's animation are offset. |
| --- | --- |
| open [Interpolator](Interpolator.md)! | [getInterpolator](LayoutAnimationController.md))`()` Returns the interpolator used to interpolate the delays between the children. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOrder](LayoutAnimationController.md))`()` Returns the order used to compute the delay of each child's animation. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDone](LayoutAnimationController.md))`()` Indicates whether the layout animation is over or not. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAnimation](LayoutAnimationController.md))`(`context:` ` [Context](../android.content/Context.md)!`, `resourceID:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the animation to be run on each child of the view group on which this layout animation controller is . |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAnimation](LayoutAnimationController.md))`(`animation:` ` [Animation](Animation.md)!`)` Sets the animation to be run on each child of the view group on which this layout animation controller is . |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDelay](LayoutAnimationController.md))`(`delay:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets the delay, as a fraction of the animation duration, by which the children's animations are offset. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInterpolator](LayoutAnimationController.md))`(`context:` ` [Context](../android.content/Context.md)!`, `resourceID:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the interpolator used to interpolate the delays between the children. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInterpolator](LayoutAnimationController.md))`(`interpolator:` ` [Interpolator](Interpolator.md)!`)` Sets the interpolator used to interpolate the delays between the children. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOrder](LayoutAnimationController.md))`(`order:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the order used to compute the delay of each child's animation. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [start](LayoutAnimationController.md))`()` Starts the animation. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [willOverlap](LayoutAnimationController.md))`()` Indicates whether two children's animations will overlap. |

| Protected methods ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getDelayForView](LayoutAnimationController.md))`(`view:` ` [View](../android.view/View.md)!`)` Returns the amount of milliseconds by which the specified view's animation must be delayed or offset. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTransformedIndex](LayoutAnimationController.md))`(`params:` ` [LayoutAnimationController.AnimationParameters](../android/view/animation/LayoutAnimationController.AnimationParameters.md)!`)` Transforms the index stored in [android.view.animation.LayoutAnimationController.AnimationParameters](../android/view/animation/LayoutAnimationController.AnimationParameters.md) by the order returned by [getOrder()](LayoutAnimationController.md)). |

| Properties ||
|-----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Animation](Animation.md)! | [mAnimation](LayoutAnimationController.md) The animation applied on each child of the view group on which this layout animation controller is set. |
| [Interpolator](Interpolator.md)! | [mInterpolator](LayoutAnimationController.md) The interpolator used to interpolate the delays. |
| [Random](../java.util/Random.md)! | [mRandomizer](LayoutAnimationController.md) The randomizer used when the order is set to random. |
| --- | --- |

## XML attributes

### android:animation

```
android:animation
```
Animation to use on each child.

May be a reference to another resource, in the form "`@[+][`*package* `:]`*type* `/`*name*" or a theme attribute in the form "`?[`*package* `:]`*type* `/`*name*". 

### android:animationOrder

```
android:animationOrder
```
The order in which the animations will be started.

Must be one of the following constant values.

| Constant | Value | Description |
|----------|-------|----------------------------------------------|
| normal | 0 | Animations are started in the natural order. |
| random | 2 | Animations are started randomly. |
| reverse | 1 | Animations are started in the reverse order. |
| --- | --- | --- |

### android:delay

```
android:delay
```
Fraction of the animation duration used to delay the beginning of the animation of each child.

May be a floating point value, such as "`1.2`".

May be a fractional value, which is a floating point number appended with either % or %p, such as "`14.5%`". The % suffix always means a percentage of the base size; the optional %p suffix provides a size relative to some parent container. 

### android:interpolator

```
android:interpolator
```
Interpolator used to interpolate the delay between the start of each animation.

May be a reference to another resource, in the form "`@[+][`*package* `:]`*type* `/`*name*" or a theme attribute in the form "`?[`*package* `:]`*type* `/`*name*".

## Constants

### ORDER_NORMAL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ORDER_NORMAL: Int
```

Distributes the animation delays in the order in which view were added to their view group. 

 Value: 0

### ORDER_RANDOM

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ORDER_RANDOM: Int
```

Randomly distributes the animation delays. 

 Value: 2

### ORDER_REVERSE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ORDER_REVERSE: Int
```

Distributes the animation delays in the reverse order in which view were added to their view group. 

 Value: 1

## Public constructors

### LayoutAnimationController

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
LayoutAnimationController(
    context: Context!, 
    attrs: AttributeSet!)
```

Creates a new layout animation controller from external resources.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android.content/Context.md)!:the Context the view group is running in, through which it can access the resources |
| `attrs` | [AttributeSet](../android.util/AttributeSet.md)!:the attributes of the XML tag that is inflating the layout animation controller |

### LayoutAnimationController

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
LayoutAnimationController(animation: Animation!)
```

Creates a new layout animation controller with a delay of 50% and the specified animation.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `animation` | [Animation](Animation.md)!:the animation to use on each child of the view group |

### LayoutAnimationController

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
LayoutAnimationController(
    animation: Animation!, 
    delay: Float)
```

Creates a new layout animation controller with the specified delay and the specified animation.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `animation` | [Animation](Animation.md)!:the animation to use on each child of the view group |
| `delay` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):the delay by which each child's animation must be offset |

## Public methods

### getAnimation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAnimation(): Animation!
```

Returns the animation applied to each child of the view group on which this controller is set.

| Return ||
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [Animation](Animation.md)! | an [android.view.animation.Animation](Animation.md) instance |

**See Also**

- [#setAnimation(android.content.Context, int)](LayoutAnimationController.md))
- [#setAnimation(Animation)](LayoutAnimationController.md)) 

### getAnimationForView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAnimationForView(view: View!): Animation!
```

Returns the animation to be applied to the specified view. The returned animation is delayed by an offset computed according to the information provided by [android.view.animation.LayoutAnimationController.AnimationParameters](../android/view/animation/LayoutAnimationController.AnimationParameters.md). This method is called by view groups to obtain the animation to set on a specific child.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------|
| `view` | [View](../android.view/View.md)!:the view to animate |

| Return ||
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Animation](Animation.md)! | an animation delayed by the number of milliseconds returned by [getDelayForView(android.view.View)](LayoutAnimationController.md)) |

**See Also**

- <https://developer.android.com/reference/kotlin/android/view/animation/LayoutAnimationController#getDelay()>
- [#setDelay(float)](LayoutAnimationController.md))
- <https://developer.android.com/reference/kotlin/android/view/animation/LayoutAnimationController#getDelayForView(android.view.View)> 

### getDelay

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDelay(): Float
```

Returns the delay by which the children's animation are offset. The delay is expressed as a fraction of the animation duration.

| Return ||
|--------------------------------------------------------------------------------|--------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | a fraction of the animation duration |

**See Also**

- [#setDelay(float)](LayoutAnimationController.md)) 

### getInterpolator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getInterpolator(): Interpolator!
```

Returns the interpolator used to interpolate the delays between the children.

| Return ||
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [Interpolator](Interpolator.md)! | an [android.view.animation.Interpolator](Interpolator.md) |

### getOrder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getOrder(): Int
```

Returns the order used to compute the delay of each child's animation.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | one of [ORDER_NORMAL](LayoutAnimationController.md), [ORDER_REVERSE](LayoutAnimationController.md) or [ORDER_RANDOM](LayoutAnimationController.md) |

### isDone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isDone(): Boolean
```

Indicates whether the layout animation is over or not. A layout animation is considered done when the animation with the longest delay is done.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if all of the children's animations are over, false otherwise |

### setAnimation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setAnimation(
    context: Context!, 
    resourceID: Int
): Unit
```

Sets the animation to be run on each child of the view group on which this layout animation controller is .

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android.content/Context.md)!:the context from which the animation must be inflated |
| `resourceID` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the resource identifier of the animation |

**See Also**

- [#setAnimation(Animation)](LayoutAnimationController.md))
- <https://developer.android.com/reference/kotlin/android/view/animation/LayoutAnimationController#getAnimation()> 

### setAnimation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setAnimation(animation: Animation!): Unit
```

Sets the animation to be run on each child of the view group on which this layout animation controller is .

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `animation` | [Animation](Animation.md)!:the animation to run on each child of the view group |

**See Also**

- [#setAnimation(android.content.Context, int)](LayoutAnimationController.md))
- <https://developer.android.com/reference/kotlin/android/view/animation/LayoutAnimationController#getAnimation()> 

### setDelay

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDelay(delay: Float): Unit
```

Sets the delay, as a fraction of the animation duration, by which the children's animations are offset. The general formula is: 

```kotlin
child animation delay = child index * delay * animation duration
  
```

<br />

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------|
| `delay` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):a fraction of the animation duration |

**See Also**

- <https://developer.android.com/reference/kotlin/android/view/animation/LayoutAnimationController#getDelay()> 

### setInterpolator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setInterpolator(
    context: Context!, 
    resourceID: Int
): Unit
```

Sets the interpolator used to interpolate the delays between the children.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android.content/Context.md)!:the context from which the interpolator must be inflated |
| `resourceID` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the resource identifier of the interpolator |

**See Also**

- <https://developer.android.com/reference/kotlin/android/view/animation/LayoutAnimationController#getInterpolator()>
- [#setInterpolator(Interpolator)](LayoutAnimationController.md)) 

### setInterpolator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setInterpolator(interpolator: Interpolator!): Unit
```

Sets the interpolator used to interpolate the delays between the children.

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------|
| `interpolator` | [Interpolator](Interpolator.md)!:the interpolator |

**See Also**

- <https://developer.android.com/reference/kotlin/android/view/animation/LayoutAnimationController#getInterpolator()>
- [#setInterpolator(Interpolator)](LayoutAnimationController.md)) 

### setOrder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOrder(order: Int): Unit
```

Sets the order used to compute the delay of each child's animation.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `order` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):one of [ORDER_NORMAL](LayoutAnimationController.md), [ORDER_REVERSE](LayoutAnimationController.md) or [ORDER_RANDOM](LayoutAnimationController.md) |

### start

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun start(): Unit
```

Starts the animation. 

### willOverlap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun willOverlap(): Boolean
```

Indicates whether two children's animations will overlap. Animations overlap when the delay is lower than 100% (or 1.0).

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if animations will overlap, false otherwise |

## Protected methods

### getDelayForView

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun getDelayForView(view: View!): Long
```

Returns the amount of milliseconds by which the specified view's animation must be delayed or offset. Subclasses should override this method to return a suitable value. This implementation returns`child animation delay`milliseconds where: 

```kotlin
child animation delay = child index * delay
  
```
The index is retrieved from the [android.view.animation.LayoutAnimationController.AnimationParameters](../android/view/animation/LayoutAnimationController.AnimationParameters.md) found in the view's [android.view.ViewGroup.LayoutParams](../android/view/ViewGroup.LayoutParams.md).

<br />

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [View](../android.view/View.md)!:the view for which to obtain the animation's delay |

| Return ||
|------------------------------------------------------------------------------|-------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | a delay in milliseconds |

**See Also**

- <https://developer.android.com/reference/kotlin/android/view/animation/LayoutAnimationController#getAnimationForView(android.view.View)>
- <https://developer.android.com/reference/kotlin/android/view/animation/LayoutAnimationController#getDelay()>
- <https://developer.android.com/reference/kotlin/android/view/animation/LayoutAnimationController#getTransformedIndex(android.view.animation.LayoutAnimationController.AnimationParameters)>
- [android.view.ViewGroup.LayoutParams](../android/view/ViewGroup.LayoutParams.md) 

### getTransformedIndex

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun getTransformedIndex(params: LayoutAnimationController.AnimationParameters!): Int
```

Transforms the index stored in [android.view.animation.LayoutAnimationController.AnimationParameters](../android/view/animation/LayoutAnimationController.AnimationParameters.md) by the order returned by [getOrder()](LayoutAnimationController.md)). Subclasses should override this method to provide additional support for other types of ordering. This method should be invoked by [getDelayForView(android.view.View)](LayoutAnimationController.md))prior to any computation.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `params` | [LayoutAnimationController.AnimationParameters](../android/view/animation/LayoutAnimationController.AnimationParameters.md)!:the animation parameters containing the index |

| Return ||
|----------------------------------------------------------------------------|---------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a transformed index |

## Properties

### mAnimation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var mAnimation: Animation!
```

The animation applied on each child of the view group on which this layout animation controller is set. 

### mInterpolator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var mInterpolator: Interpolator!
```

The interpolator used to interpolate the delays. 

### mRandomizer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected var mRandomizer: Random!
```

The randomizer used when the order is set to random. Subclasses should use this object to avoid creating their own.
