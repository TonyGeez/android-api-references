# ViewPropertyAnimator

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ViewPropertyAnimator

Kotlin| [Java](ViewPropertyAnimator.md) 
| --- | --- |

```
open class ViewPropertyAnimator
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.ViewPropertyAnimator](ViewPropertyAnimator.md) |

This class enables automatic and optimized animation of select properties on View objects. If only one or two properties on a View object are being animated, then using an [android.animation.ObjectAnimator](../android.animation/ObjectAnimator.md) is fine; the property setters called by ObjectAnimator are well equipped to do the right thing to set the property and invalidate the view appropriately. But if several properties are animated simultaneously, or if you just want a more convenient syntax to animate a specific property, then ViewPropertyAnimator might be more well-suited to the task.

This class may provide better performance for several simultaneous animations, because it will optimize invalidate calls to take place only once for several properties instead of each animated property independently causing its own invalidation. Also, the syntax of using this class could be easier to use because the caller need only tell the View object which property to animate, and the value to animate either to or by, and this class handles the details of configuring the underlying Animator class and starting it.

This class is not constructed by the caller, but rather by the View whose properties it will animate. Calls to [android.view.View#animate()](View.md))will return a reference to the appropriate ViewPropertyAnimator object for that View.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [ViewPropertyAnimator](ViewPropertyAnimator.md) | [alpha](ViewPropertyAnimator.md))`(`value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` This method will cause the View's`alpha`property to be animated to the specified value. |
| open [ViewPropertyAnimator](ViewPropertyAnimator.md) | [alphaBy](ViewPropertyAnimator.md))`(`value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` This method will cause the View's`alpha`property to be animated by the specified value. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [cancel](ViewPropertyAnimator.md))`()` Cancels all property animations that are currently running or pending. |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getDuration](ViewPropertyAnimator.md))`()` Returns the current duration of property animations. |
| open [TimeInterpolator](../android.animation/TimeInterpolator.md)? | [getInterpolator](ViewPropertyAnimator.md))`()` Returns the timing interpolator that this animation uses. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getStartDelay](ViewPropertyAnimator.md))`()` Returns the current startDelay of property animations. |
| --- | --- |
| open [ViewPropertyAnimator](ViewPropertyAnimator.md) | [rotation](ViewPropertyAnimator.md))`(`value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` This method will cause the View's`rotation`property to be animated to the specified value. |
| open [ViewPropertyAnimator](ViewPropertyAnimator.md) | [rotationBy](ViewPropertyAnimator.md))`(`value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` This method will cause the View's`rotation`property to be animated by the specified value. |
| open [ViewPropertyAnimator](ViewPropertyAnimator.md) | [rotationX](ViewPropertyAnimator.md))`(`value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` This method will cause the View's`rotationX`property to be animated to the specified value. |
| --- | --- |
| open [ViewPropertyAnimator](ViewPropertyAnimator.md) | [rotationXBy](ViewPropertyAnimator.md))`(`value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` This method will cause the View's`rotationX`property to be animated by the specified value. |
| open [ViewPropertyAnimator](ViewPropertyAnimator.md) | [rotationY](ViewPropertyAnimator.md))`(`value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` This method will cause the View's`rotationY`property to be animated to the specified value. |
| open [ViewPropertyAnimator](ViewPropertyAnimator.md) | [rotationYBy](ViewPropertyAnimator.md))`(`value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` This method will cause the View's`rotationY`property to be animated by the specified value. |
| --- | --- |
| open [ViewPropertyAnimator](ViewPropertyAnimator.md) | [scaleX](ViewPropertyAnimator.md))`(`value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` This method will cause the View's`scaleX`property to be animated to the specified value. |
| open [ViewPropertyAnimator](ViewPropertyAnimator.md) | [scaleXBy](ViewPropertyAnimator.md))`(`value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` This method will cause the View's`scaleX`property to be animated by the specified value. |
| open [ViewPropertyAnimator](ViewPropertyAnimator.md) | [scaleY](ViewPropertyAnimator.md))`(`value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` This method will cause the View's`scaleY`property to be animated to the specified value. |
| --- | --- |
| open [ViewPropertyAnimator](ViewPropertyAnimator.md) | [scaleYBy](ViewPropertyAnimator.md))`(`value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` This method will cause the View's`scaleY`property to be animated by the specified value. |
| open [ViewPropertyAnimator](ViewPropertyAnimator.md) | [setDuration](ViewPropertyAnimator.md))`(`duration:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the duration for the underlying animator that animates the requested properties. |
| open [ViewPropertyAnimator](ViewPropertyAnimator.md) | [setInterpolator](ViewPropertyAnimator.md))`(`interpolator:` ` [TimeInterpolator](../android.animation/TimeInterpolator.md)!`)` Sets the interpolator for the underlying animator that animates the requested properties. |
| --- | --- |
| open [ViewPropertyAnimator](ViewPropertyAnimator.md) | [setListener](ViewPropertyAnimator.md))`(`listener:` ` [Animator.AnimatorListener](../android/animation/Animator.AnimatorListener.md)?`)` Sets a listener for events in the underlying Animators that run the property animations. |
| open [ViewPropertyAnimator](ViewPropertyAnimator.md) | [setStartDelay](ViewPropertyAnimator.md))`(`startDelay:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the startDelay for the underlying animator that animates the requested properties. |
| open [ViewPropertyAnimator](ViewPropertyAnimator.md) | [setUpdateListener](ViewPropertyAnimator.md))`(`listener:` ` [ValueAnimator.AnimatorUpdateListener](../android/animation/ValueAnimator.AnimatorUpdateListener.md)?`)` Sets a listener for update events in the underlying ValueAnimator that runs the property animations. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [start](ViewPropertyAnimator.md))`()` Starts the currently pending property animations immediately. |
| open [ViewPropertyAnimator](ViewPropertyAnimator.md) | [translationX](ViewPropertyAnimator.md))`(`value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` This method will cause the View's`translationX`property to be animated to the specified value. |
| open [ViewPropertyAnimator](ViewPropertyAnimator.md) | [translationXBy](ViewPropertyAnimator.md))`(`value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` This method will cause the View's`translationX`property to be animated by the specified value. |
| --- | --- |
| open [ViewPropertyAnimator](ViewPropertyAnimator.md) | [translationY](ViewPropertyAnimator.md))`(`value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` This method will cause the View's`translationY`property to be animated to the specified value. |
| open [ViewPropertyAnimator](ViewPropertyAnimator.md) | [translationYBy](ViewPropertyAnimator.md))`(`value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` This method will cause the View's`translationY`property to be animated by the specified value. |
| open [ViewPropertyAnimator](ViewPropertyAnimator.md) | [translationZ](ViewPropertyAnimator.md))`(`value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` This method will cause the View's`translationZ`property to be animated to the specified value. |
| --- | --- |
| open [ViewPropertyAnimator](ViewPropertyAnimator.md) | [translationZBy](ViewPropertyAnimator.md))`(`value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` This method will cause the View's`translationZ`property to be animated by the specified value. |
| open [ViewPropertyAnimator](ViewPropertyAnimator.md) | [withEndAction](ViewPropertyAnimator.md))`(`runnable:` ` [Runnable](../java.lang/Runnable.md)!`)` Specifies an action to take place when the next animation ends. |
| open [ViewPropertyAnimator](ViewPropertyAnimator.md) | [withLayer](ViewPropertyAnimator.md))`()` The View associated with this ViewPropertyAnimator will have its [layer type](View.md))set to [View.LAYER_TYPE_HARDWARE](View.md) for the duration of the next animation. |
| --- | --- |
| open [ViewPropertyAnimator](ViewPropertyAnimator.md) | [withStartAction](ViewPropertyAnimator.md))`(`runnable:` ` [Runnable](../java.lang/Runnable.md)!`)` Specifies an action to take place when the next animation runs. |
| open [ViewPropertyAnimator](ViewPropertyAnimator.md) | [x](ViewPropertyAnimator.md))`(`value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` This method will cause the View's`x`property to be animated to the specified value. |
| open [ViewPropertyAnimator](ViewPropertyAnimator.md) | [xBy](ViewPropertyAnimator.md))`(`value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` This method will cause the View's`x`property to be animated by the specified value. |
| --- | --- |
| open [ViewPropertyAnimator](ViewPropertyAnimator.md) | [y](ViewPropertyAnimator.md))`(`value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` This method will cause the View's`y`property to be animated to the specified value. |
| open [ViewPropertyAnimator](ViewPropertyAnimator.md) | [yBy](ViewPropertyAnimator.md))`(`value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` This method will cause the View's`y`property to be animated by the specified value. |
| open [ViewPropertyAnimator](ViewPropertyAnimator.md) | [z](ViewPropertyAnimator.md))`(`value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` This method will cause the View's`z`property to be animated to the specified value. |
| --- | --- |
| open [ViewPropertyAnimator](ViewPropertyAnimator.md) | [zBy](ViewPropertyAnimator.md))`(`value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` This method will cause the View's`z`property to be animated by the specified value. |

## Public methods

### alpha

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun alpha(value: Float): ViewPropertyAnimator
```

This method will cause the View's`alpha`property to be animated to the specified value. Animations already running on the property will be canceled.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `value` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The value to be animated to. Value is between 0.0f and 1.0f inclusive |

| Return ||
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [ViewPropertyAnimator](ViewPropertyAnimator.md) | This object, allowing calls to methods in this class to be chained. This value cannot be`null`. |

**See Also**

- [android.view.View#setAlpha(float)](View.md)) 

### alphaBy

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun alphaBy(value: Float): ViewPropertyAnimator
```

This method will cause the View's`alpha`property to be animated by the specified value. Animations already running on the property will be canceled.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `value` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The amount to be animated by, as an offset from the current value. |

| Return ||
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [ViewPropertyAnimator](ViewPropertyAnimator.md) | This object, allowing calls to methods in this class to be chained. This value cannot be`null`. |

**See Also**

- [android.view.View#setAlpha(float)](View.md)) 

### cancel

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun cancel(): Unit
```

Cancels all property animations that are currently running or pending. 

### getDuration

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDuration(): Long
```

Returns the current duration of property animations. If the duration was set on this object, that value is returned. Otherwise, the default value of the underlying Animator is returned.

| Return ||
|------------------------------------------------------------------------------|----------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The duration of animations, in milliseconds. |

**See Also**

- [#setDuration(long)](ViewPropertyAnimator.md)) 

### getInterpolator

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getInterpolator(): TimeInterpolator?
```

Returns the timing interpolator that this animation uses.

| Return ||
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [TimeInterpolator](../android.animation/TimeInterpolator.md)? | The timing interpolator for this animation. This value may be`null`. |

### getStartDelay

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getStartDelay(): Long
```

Returns the current startDelay of property animations. If the startDelay was set on this object, that value is returned. Otherwise, the default value of the underlying Animator is returned.

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The startDelay of animations, in milliseconds. |

**See Also**

- [#setStartDelay(long)](ViewPropertyAnimator.md)) 

### rotation

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun rotation(value: Float): ViewPropertyAnimator
```

This method will cause the View's`rotation`property to be animated to the specified value. Animations already running on the property will be canceled.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------|
| `value` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The value to be animated to. |

| Return ||
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [ViewPropertyAnimator](ViewPropertyAnimator.md) | This object, allowing calls to methods in this class to be chained. This value cannot be`null`. |

**See Also**

- [android.view.View#setRotation(float)](View.md)) 

### rotationBy

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun rotationBy(value: Float): ViewPropertyAnimator
```

This method will cause the View's`rotation`property to be animated by the specified value. Animations already running on the property will be canceled.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `value` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The amount to be animated by, as an offset from the current value. |

| Return ||
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [ViewPropertyAnimator](ViewPropertyAnimator.md) | This object, allowing calls to methods in this class to be chained. This value cannot be`null`. |

**See Also**

- [android.view.View#setRotation(float)](View.md)) 

### rotationX

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun rotationX(value: Float): ViewPropertyAnimator
```

This method will cause the View's`rotationX`property to be animated to the specified value. Animations already running on the property will be canceled.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------|
| `value` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The value to be animated to. |

| Return ||
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [ViewPropertyAnimator](ViewPropertyAnimator.md) | This object, allowing calls to methods in this class to be chained. This value cannot be`null`. |

**See Also**

- [android.view.View#setRotationX(float)](View.md)) 

### rotationXBy

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun rotationXBy(value: Float): ViewPropertyAnimator
```

This method will cause the View's`rotationX`property to be animated by the specified value. Animations already running on the property will be canceled.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `value` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The amount to be animated by, as an offset from the current value. |

| Return ||
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [ViewPropertyAnimator](ViewPropertyAnimator.md) | This object, allowing calls to methods in this class to be chained. This value cannot be`null`. |

**See Also**

- [android.view.View#setRotationX(float)](View.md)) 

### rotationY

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun rotationY(value: Float): ViewPropertyAnimator
```

This method will cause the View's`rotationY`property to be animated to the specified value. Animations already running on the property will be canceled.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------|
| `value` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The value to be animated to. |

| Return ||
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [ViewPropertyAnimator](ViewPropertyAnimator.md) | This object, allowing calls to methods in this class to be chained. This value cannot be`null`. |

**See Also**

- [android.view.View#setRotationY(float)](View.md)) 

### rotationYBy

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun rotationYBy(value: Float): ViewPropertyAnimator
```

This method will cause the View's`rotationY`property to be animated by the specified value. Animations already running on the property will be canceled.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `value` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The amount to be animated by, as an offset from the current value. |

| Return ||
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [ViewPropertyAnimator](ViewPropertyAnimator.md) | This object, allowing calls to methods in this class to be chained. This value cannot be`null`. |

**See Also**

- [android.view.View#setRotationY(float)](View.md)) 

### scaleX

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun scaleX(value: Float): ViewPropertyAnimator
```

This method will cause the View's`scaleX`property to be animated to the specified value. Animations already running on the property will be canceled.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------|
| `value` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The value to be animated to. |

| Return ||
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [ViewPropertyAnimator](ViewPropertyAnimator.md) | This object, allowing calls to methods in this class to be chained. This value cannot be`null`. |

**See Also**

- [android.view.View#setScaleX(float)](View.md)) 

### scaleXBy

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun scaleXBy(value: Float): ViewPropertyAnimator
```

This method will cause the View's`scaleX`property to be animated by the specified value. Animations already running on the property will be canceled.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `value` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The amount to be animated by, as an offset from the current value. |

| Return ||
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [ViewPropertyAnimator](ViewPropertyAnimator.md) | This object, allowing calls to methods in this class to be chained. This value cannot be`null`. |

**See Also**

- [android.view.View#setScaleX(float)](View.md)) 

### scaleY

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun scaleY(value: Float): ViewPropertyAnimator
```

This method will cause the View's`scaleY`property to be animated to the specified value. Animations already running on the property will be canceled.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------|
| `value` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The value to be animated to. |

| Return ||
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [ViewPropertyAnimator](ViewPropertyAnimator.md) | This object, allowing calls to methods in this class to be chained. This value cannot be`null`. |

**See Also**

- [android.view.View#setScaleY(float)](View.md)) 

### scaleYBy

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun scaleYBy(value: Float): ViewPropertyAnimator
```

This method will cause the View's`scaleY`property to be animated by the specified value. Animations already running on the property will be canceled.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `value` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The amount to be animated by, as an offset from the current value. |

| Return ||
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [ViewPropertyAnimator](ViewPropertyAnimator.md) | This object, allowing calls to methods in this class to be chained. This value cannot be`null`. |

**See Also**

- [android.view.View#setScaleY(float)](View.md)) 

### setDuration

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setDuration(duration: Long): ViewPropertyAnimator
```

Sets the duration for the underlying animator that animates the requested properties. By default, the animator uses the default value for ValueAnimator. Calling this method will cause the declared value to be used instead.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `duration` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The length of ensuing property animations, in milliseconds. The value cannot be negative. |

| Return ||
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [ViewPropertyAnimator](ViewPropertyAnimator.md) | This object, allowing calls to methods in this class to be chained. This value cannot be`null`. |

### setInterpolator

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setInterpolator(interpolator: TimeInterpolator!): ViewPropertyAnimator
```

Sets the interpolator for the underlying animator that animates the requested properties. By default, the animator uses the default interpolator for ValueAnimator. Calling this method will cause the declared object to be used instead.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `interpolator` | [TimeInterpolator](../android.animation/TimeInterpolator.md)!:The TimeInterpolator to be used for ensuing property animations. A value of`null`will result in linear interpolation. |

| Return ||
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [ViewPropertyAnimator](ViewPropertyAnimator.md) | This object, allowing calls to methods in this class to be chained. This value cannot be`null`. |

### setListener

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setListener(listener: Animator.AnimatorListener?): ViewPropertyAnimator
```

Sets a listener for events in the underlying Animators that run the property animations.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [Animator.AnimatorListener](../android/animation/Animator.AnimatorListener.md)?:The listener to be called with AnimatorListener events. A value of`null`removes any existing listener. |

| Return ||
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [ViewPropertyAnimator](ViewPropertyAnimator.md) | This object, allowing calls to methods in this class to be chained. This value cannot be`null`. |

**See Also**

- [android.animation.Animator.AnimatorListener](../android/animation/Animator.AnimatorListener.md) 

### setStartDelay

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setStartDelay(startDelay: Long): ViewPropertyAnimator
```

Sets the startDelay for the underlying animator that animates the requested properties. By default, the animator uses the default value for ValueAnimator. Calling this method will cause the declared value to be used instead.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `startDelay` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The delay of ensuing property animations, in milliseconds. The value cannot be negative. |

| Return ||
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [ViewPropertyAnimator](ViewPropertyAnimator.md) | This object, allowing calls to methods in this class to be chained. This value cannot be`null`. |

### setUpdateListener

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setUpdateListener(listener: ValueAnimator.AnimatorUpdateListener?): ViewPropertyAnimator
```

Sets a listener for update events in the underlying ValueAnimator that runs the property animations. Note that the underlying animator is animating between 0 and 1 (these values are then turned into the actual property values internally by ViewPropertyAnimator). So the animator cannot give information on the current values of the properties being animated by this ViewPropertyAnimator, although the view object itself can be queried to get the current values.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [ValueAnimator.AnimatorUpdateListener](../android/animation/ValueAnimator.AnimatorUpdateListener.md)?:The listener to be called with update events. A value of`null`removes any existing listener. |

| Return ||
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [ViewPropertyAnimator](ViewPropertyAnimator.md) | This object, allowing calls to methods in this class to be chained. This value cannot be`null`. |

**See Also**

- [android.animation.ValueAnimator.AnimatorUpdateListener](../android/animation/ValueAnimator.AnimatorUpdateListener.md) 

### start

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun start(): Unit
```

Starts the currently pending property animations immediately. Calling`start()`is optional because all animations start automatically at the next opportunity. However, if the animations are needed to start immediately and synchronously (not at the time when the next event is processed by the hierarchy, which is when the animations would begin otherwise), then this method can be used. 

### translationX

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun translationX(value: Float): ViewPropertyAnimator
```

This method will cause the View's`translationX`property to be animated to the specified value. Animations already running on the property will be canceled.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------|
| `value` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The value to be animated to. |

| Return ||
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [ViewPropertyAnimator](ViewPropertyAnimator.md) | This object, allowing calls to methods in this class to be chained. This value cannot be`null`. |

**See Also**

- [android.view.View#setTranslationX(float)](View.md)) 

### translationXBy

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun translationXBy(value: Float): ViewPropertyAnimator
```

This method will cause the View's`translationX`property to be animated by the specified value. Animations already running on the property will be canceled.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `value` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The amount to be animated by, as an offset from the current value. |

| Return ||
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [ViewPropertyAnimator](ViewPropertyAnimator.md) | This object, allowing calls to methods in this class to be chained. This value cannot be`null`. |

**See Also**

- [android.view.View#setTranslationX(float)](View.md)) 

### translationY

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun translationY(value: Float): ViewPropertyAnimator
```

This method will cause the View's`translationY`property to be animated to the specified value. Animations already running on the property will be canceled.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------|
| `value` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The value to be animated to. |

| Return ||
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [ViewPropertyAnimator](ViewPropertyAnimator.md) | This object, allowing calls to methods in this class to be chained. This value cannot be`null`. |

**See Also**

- [android.view.View#setTranslationY(float)](View.md)) 

### translationYBy

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun translationYBy(value: Float): ViewPropertyAnimator
```

This method will cause the View's`translationY`property to be animated by the specified value. Animations already running on the property will be canceled.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `value` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The amount to be animated by, as an offset from the current value. |

| Return ||
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [ViewPropertyAnimator](ViewPropertyAnimator.md) | This object, allowing calls to methods in this class to be chained. This value cannot be`null`. |

**See Also**

- [android.view.View#setTranslationY(float)](View.md)) 

### translationZ

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun translationZ(value: Float): ViewPropertyAnimator
```

This method will cause the View's`translationZ`property to be animated to the specified value. Animations already running on the property will be canceled.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------|
| `value` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The value to be animated to. |

| Return ||
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [ViewPropertyAnimator](ViewPropertyAnimator.md) | This object, allowing calls to methods in this class to be chained. This value cannot be`null`. |

**See Also**

- [android.view.View#setTranslationZ(float)](View.md)) 

### translationZBy

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun translationZBy(value: Float): ViewPropertyAnimator
```

This method will cause the View's`translationZ`property to be animated by the specified value. Animations already running on the property will be canceled.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `value` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The amount to be animated by, as an offset from the current value. |

| Return ||
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [ViewPropertyAnimator](ViewPropertyAnimator.md) | This object, allowing calls to methods in this class to be chained. This value cannot be`null`. |

**See Also**

- [android.view.View#setTranslationZ(float)](View.md)) 

### withEndAction

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun withEndAction(runnable: Runnable!): ViewPropertyAnimator
```

Specifies an action to take place when the next animation ends. The action is only run if the animation ends normally; if the ViewPropertyAnimator is canceled during that animation, the runnable will not run. This method, along with [withStartAction(java.lang.Runnable)](ViewPropertyAnimator.md)), is intended to help facilitate choreographing ViewPropertyAnimator animations with other animations or actions in the application.

For example, the following code animates a view to x=200 and then back to 0: 

```kotlin
Runnable endAction = new Runnable() {
          public void run() {
              view.animate().x(0);
          }
      };
      view.animate().x(200).withEndAction(endAction);
  
```

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------|
| `runnable` | [Runnable](../java.lang/Runnable.md)!:The action to run when the next animation ends. |

| Return ||
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [ViewPropertyAnimator](ViewPropertyAnimator.md) | This object, allowing calls to methods in this class to be chained. This value cannot be`null`. |

### withLayer

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun withLayer(): ViewPropertyAnimator
```

The View associated with this ViewPropertyAnimator will have its [layer type](View.md))set to [View.LAYER_TYPE_HARDWARE](View.md) for the duration of the next animation. As stated in the documentation for [View.LAYER_TYPE_HARDWARE](View.md), the actual type of layer used internally depends on the runtime situation of the view. If the activity and this view are hardware-accelerated, then the layer will be accelerated as well. If the activity or the view is not accelerated, then the layer will effectively be the same as [View.LAYER_TYPE_SOFTWARE](View.md).

This state is not persistent, either on the View or on this ViewPropertyAnimator: the layer type of the View will be restored when the animation ends to what it was when this method was called, and this setting on ViewPropertyAnimator is only valid for the next animation. Note that calling this method and then independently setting the layer type of the View (by a direct call to [View.setLayerType(int, android.graphics.Paint)](View.md))) will result in some inconsistency, including having the layer type restored to its pre-withLayer() value when the animation ends.

| Return ||
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [ViewPropertyAnimator](ViewPropertyAnimator.md) | This object, allowing calls to methods in this class to be chained. This value cannot be`null`. |

**See Also**

- [android.view.View#setLayerType(int, android.graphics.Paint)](View.md)) 

### withStartAction

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun withStartAction(runnable: Runnable!): ViewPropertyAnimator
```

Specifies an action to take place when the next animation runs. If there is a [startDelay](ViewPropertyAnimator.md))set on this ViewPropertyAnimator, then the action will run after that startDelay expires, when the actual animation begins. This method, along with [withEndAction(java.lang.Runnable)](ViewPropertyAnimator.md)), is intended to help facilitate choreographing ViewPropertyAnimator animations with other animations or actions in the application.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------|
| `runnable` | [Runnable](../java.lang/Runnable.md)!:The action to run when the next animation starts. |

| Return ||
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [ViewPropertyAnimator](ViewPropertyAnimator.md) | This object, allowing calls to methods in this class to be chained. This value cannot be`null`. |

### x

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun x(value: Float): ViewPropertyAnimator
```

This method will cause the View's`x`property to be animated to the specified value. Animations already running on the property will be canceled.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------|
| `value` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The value to be animated to. |

| Return ||
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [ViewPropertyAnimator](ViewPropertyAnimator.md) | This object, allowing calls to methods in this class to be chained. This value cannot be`null`. |

**See Also**

- [android.view.View#setX(float)](View.md)) 

### xBy

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun xBy(value: Float): ViewPropertyAnimator
```

This method will cause the View's`x`property to be animated by the specified value. Animations already running on the property will be canceled.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `value` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The amount to be animated by, as an offset from the current value. |

| Return ||
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [ViewPropertyAnimator](ViewPropertyAnimator.md) | This object, allowing calls to methods in this class to be chained. This value cannot be`null`. |

**See Also**

- [android.view.View#setX(float)](View.md)) 

### y

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun y(value: Float): ViewPropertyAnimator
```

This method will cause the View's`y`property to be animated to the specified value. Animations already running on the property will be canceled.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------|
| `value` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The value to be animated to. |

| Return ||
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [ViewPropertyAnimator](ViewPropertyAnimator.md) | This object, allowing calls to methods in this class to be chained. This value cannot be`null`. |

**See Also**

- [android.view.View#setY(float)](View.md)) 

### yBy

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun yBy(value: Float): ViewPropertyAnimator
```

This method will cause the View's`y`property to be animated by the specified value. Animations already running on the property will be canceled.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `value` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The amount to be animated by, as an offset from the current value. |

| Return ||
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [ViewPropertyAnimator](ViewPropertyAnimator.md) | This object, allowing calls to methods in this class to be chained. This value cannot be`null`. |

**See Also**

- [android.view.View#setY(float)](View.md)) 

### z

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun z(value: Float): ViewPropertyAnimator
```

This method will cause the View's`z`property to be animated to the specified value. Animations already running on the property will be canceled.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------|
| `value` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The value to be animated to. |

| Return ||
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [ViewPropertyAnimator](ViewPropertyAnimator.md) | This object, allowing calls to methods in this class to be chained. This value cannot be`null`. |

**See Also**

- [android.view.View#setZ(float)](View.md)) 

### zBy

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun zBy(value: Float): ViewPropertyAnimator
```

This method will cause the View's`z`property to be animated by the specified value. Animations already running on the property will be canceled.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `value` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The amount to be animated by, as an offset from the current value. |

| Return ||
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [ViewPropertyAnimator](ViewPropertyAnimator.md) | This object, allowing calls to methods in this class to be chained. This value cannot be`null`. |

**See Also**

- [android.view.View#setZ(float)](View.md))
