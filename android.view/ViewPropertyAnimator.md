# ViewPropertyAnimator

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ViewPropertyAnimator

Kotlin| [Java](https://developer.android.com/reference/android/view/ViewPropertyAnimator "View this page in Java") 
| --- | --- |

```
open class ViewPropertyAnimator
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.ViewPropertyAnimator](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#) |

This class enables automatic and optimized animation of select properties on View objects. If only one or two properties on a View object are being animated, then using an [android.animation.ObjectAnimator](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator.html#) is fine; the property setters called by ObjectAnimator are well equipped to do the right thing to set the property and invalidate the view appropriately. But if several properties are animated simultaneously, or if you just want a more convenient syntax to animate a specific property, then ViewPropertyAnimator might be more well-suited to the task.

This class may provide better performance for several simultaneous animations, because it will optimize invalidate calls to take place only once for several properties instead of each animated property independently causing its own invalidation. Also, the syntax of using this class could be easier to use because the caller need only tell the View object which property to animate, and the value to animate either to or by, and this class handles the details of configuring the underlying Animator class and starting it.

This class is not constructed by the caller, but rather by the View whose properties it will animate. Calls to [android.view.View#animate()](https://developer.android.com/reference/kotlin/android/view/View#animate())will return a reference to the appropriate ViewPropertyAnimator object for that View.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [ViewPropertyAnimator](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#) | [alpha](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#alpha(kotlin.Float))`(`value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` This method will cause the View's`alpha`property to be animated to the specified value. |
| open [ViewPropertyAnimator](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#) | [alphaBy](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#alphaBy(kotlin.Float))`(`value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` This method will cause the View's`alpha`property to be animated by the specified value. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [cancel](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#cancel())`()` Cancels all property animations that are currently running or pending. |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getDuration](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#getDuration())`()` Returns the current duration of property animations. |
| open [TimeInterpolator](https://developer.android.com/reference/kotlin/android/animation/TimeInterpolator.html#)? | [getInterpolator](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#getInterpolator())`()` Returns the timing interpolator that this animation uses. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getStartDelay](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#getStartDelay())`()` Returns the current startDelay of property animations. |
| --- | --- |
| open [ViewPropertyAnimator](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#) | [rotation](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#rotation(kotlin.Float))`(`value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` This method will cause the View's`rotation`property to be animated to the specified value. |
| open [ViewPropertyAnimator](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#) | [rotationBy](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#rotationBy(kotlin.Float))`(`value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` This method will cause the View's`rotation`property to be animated by the specified value. |
| open [ViewPropertyAnimator](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#) | [rotationX](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#rotationX(kotlin.Float))`(`value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` This method will cause the View's`rotationX`property to be animated to the specified value. |
| --- | --- |
| open [ViewPropertyAnimator](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#) | [rotationXBy](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#rotationXBy(kotlin.Float))`(`value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` This method will cause the View's`rotationX`property to be animated by the specified value. |
| open [ViewPropertyAnimator](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#) | [rotationY](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#rotationY(kotlin.Float))`(`value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` This method will cause the View's`rotationY`property to be animated to the specified value. |
| open [ViewPropertyAnimator](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#) | [rotationYBy](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#rotationYBy(kotlin.Float))`(`value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` This method will cause the View's`rotationY`property to be animated by the specified value. |
| --- | --- |
| open [ViewPropertyAnimator](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#) | [scaleX](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#scaleX(kotlin.Float))`(`value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` This method will cause the View's`scaleX`property to be animated to the specified value. |
| open [ViewPropertyAnimator](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#) | [scaleXBy](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#scaleXBy(kotlin.Float))`(`value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` This method will cause the View's`scaleX`property to be animated by the specified value. |
| open [ViewPropertyAnimator](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#) | [scaleY](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#scaleY(kotlin.Float))`(`value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` This method will cause the View's`scaleY`property to be animated to the specified value. |
| --- | --- |
| open [ViewPropertyAnimator](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#) | [scaleYBy](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#scaleYBy(kotlin.Float))`(`value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` This method will cause the View's`scaleY`property to be animated by the specified value. |
| open [ViewPropertyAnimator](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#) | [setDuration](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#setDuration(kotlin.Long))`(`duration:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the duration for the underlying animator that animates the requested properties. |
| open [ViewPropertyAnimator](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#) | [setInterpolator](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#setInterpolator(android.animation.TimeInterpolator))`(`interpolator:` ` [TimeInterpolator](https://developer.android.com/reference/kotlin/android/animation/TimeInterpolator.html#)!`)` Sets the interpolator for the underlying animator that animates the requested properties. |
| --- | --- |
| open [ViewPropertyAnimator](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#) | [setListener](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#setListener(android.animation.Animator.AnimatorListener))`(`listener:` ` [Animator.AnimatorListener](https://developer.android.com/reference/kotlin/android/animation/Animator.AnimatorListener.html#)?`)` Sets a listener for events in the underlying Animators that run the property animations. |
| open [ViewPropertyAnimator](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#) | [setStartDelay](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#setStartDelay(kotlin.Long))`(`startDelay:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the startDelay for the underlying animator that animates the requested properties. |
| open [ViewPropertyAnimator](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#) | [setUpdateListener](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#setUpdateListener(android.animation.ValueAnimator.AnimatorUpdateListener))`(`listener:` ` [ValueAnimator.AnimatorUpdateListener](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator.AnimatorUpdateListener.html#)?`)` Sets a listener for update events in the underlying ValueAnimator that runs the property animations. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [start](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#start())`()` Starts the currently pending property animations immediately. |
| open [ViewPropertyAnimator](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#) | [translationX](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#translationX(kotlin.Float))`(`value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` This method will cause the View's`translationX`property to be animated to the specified value. |
| open [ViewPropertyAnimator](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#) | [translationXBy](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#translationXBy(kotlin.Float))`(`value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` This method will cause the View's`translationX`property to be animated by the specified value. |
| --- | --- |
| open [ViewPropertyAnimator](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#) | [translationY](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#translationY(kotlin.Float))`(`value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` This method will cause the View's`translationY`property to be animated to the specified value. |
| open [ViewPropertyAnimator](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#) | [translationYBy](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#translationYBy(kotlin.Float))`(`value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` This method will cause the View's`translationY`property to be animated by the specified value. |
| open [ViewPropertyAnimator](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#) | [translationZ](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#translationZ(kotlin.Float))`(`value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` This method will cause the View's`translationZ`property to be animated to the specified value. |
| --- | --- |
| open [ViewPropertyAnimator](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#) | [translationZBy](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#translationZBy(kotlin.Float))`(`value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` This method will cause the View's`translationZ`property to be animated by the specified value. |
| open [ViewPropertyAnimator](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#) | [withEndAction](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#withEndAction(java.lang.Runnable))`(`runnable:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!`)` Specifies an action to take place when the next animation ends. |
| open [ViewPropertyAnimator](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#) | [withLayer](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#withLayer())`()` The View associated with this ViewPropertyAnimator will have its [layer type](https://developer.android.com/reference/kotlin/android/view/View#setLayerType(kotlin.Int,%20android.graphics.Paint))set to [View.LAYER_TYPE_HARDWARE](https://developer.android.com/reference/kotlin/android/view/View#LAYER_TYPE_HARDWARE:kotlin.Int) for the duration of the next animation. |
| --- | --- |
| open [ViewPropertyAnimator](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#) | [withStartAction](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#withStartAction(java.lang.Runnable))`(`runnable:` ` [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!`)` Specifies an action to take place when the next animation runs. |
| open [ViewPropertyAnimator](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#) | [x](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#x(kotlin.Float))`(`value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` This method will cause the View's`x`property to be animated to the specified value. |
| open [ViewPropertyAnimator](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#) | [xBy](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#xBy(kotlin.Float))`(`value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` This method will cause the View's`x`property to be animated by the specified value. |
| --- | --- |
| open [ViewPropertyAnimator](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#) | [y](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#y(kotlin.Float))`(`value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` This method will cause the View's`y`property to be animated to the specified value. |
| open [ViewPropertyAnimator](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#) | [yBy](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#yBy(kotlin.Float))`(`value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` This method will cause the View's`y`property to be animated by the specified value. |
| open [ViewPropertyAnimator](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#) | [z](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#z(kotlin.Float))`(`value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` This method will cause the View's`z`property to be animated to the specified value. |
| --- | --- |
| open [ViewPropertyAnimator](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#) | [zBy](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#zBy(kotlin.Float))`(`value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` This method will cause the View's`z`property to be animated by the specified value. |

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
| [ViewPropertyAnimator](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#) | This object, allowing calls to methods in this class to be chained. This value cannot be`null`. |

**See Also**

- [android.view.View#setAlpha(float)](https://developer.android.com/reference/kotlin/android/view/View#setAlpha(kotlin.Float)) 

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
| [ViewPropertyAnimator](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#) | This object, allowing calls to methods in this class to be chained. This value cannot be`null`. |

**See Also**

- [android.view.View#setAlpha(float)](https://developer.android.com/reference/kotlin/android/view/View#setAlpha(kotlin.Float)) 

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

- [#setDuration(long)](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#setDuration(kotlin.Long)) 

### getInterpolator

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getInterpolator(): TimeInterpolator?
```

Returns the timing interpolator that this animation uses.

| Return ||
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [TimeInterpolator](https://developer.android.com/reference/kotlin/android/animation/TimeInterpolator.html#)? | The timing interpolator for this animation. This value may be`null`. |

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

- [#setStartDelay(long)](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#setStartDelay(kotlin.Long)) 

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
| [ViewPropertyAnimator](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#) | This object, allowing calls to methods in this class to be chained. This value cannot be`null`. |

**See Also**

- [android.view.View#setRotation(float)](https://developer.android.com/reference/kotlin/android/view/View#setRotation(kotlin.Float)) 

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
| [ViewPropertyAnimator](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#) | This object, allowing calls to methods in this class to be chained. This value cannot be`null`. |

**See Also**

- [android.view.View#setRotation(float)](https://developer.android.com/reference/kotlin/android/view/View#setRotation(kotlin.Float)) 

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
| [ViewPropertyAnimator](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#) | This object, allowing calls to methods in this class to be chained. This value cannot be`null`. |

**See Also**

- [android.view.View#setRotationX(float)](https://developer.android.com/reference/kotlin/android/view/View#setRotationX(kotlin.Float)) 

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
| [ViewPropertyAnimator](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#) | This object, allowing calls to methods in this class to be chained. This value cannot be`null`. |

**See Also**

- [android.view.View#setRotationX(float)](https://developer.android.com/reference/kotlin/android/view/View#setRotationX(kotlin.Float)) 

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
| [ViewPropertyAnimator](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#) | This object, allowing calls to methods in this class to be chained. This value cannot be`null`. |

**See Also**

- [android.view.View#setRotationY(float)](https://developer.android.com/reference/kotlin/android/view/View#setRotationY(kotlin.Float)) 

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
| [ViewPropertyAnimator](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#) | This object, allowing calls to methods in this class to be chained. This value cannot be`null`. |

**See Also**

- [android.view.View#setRotationY(float)](https://developer.android.com/reference/kotlin/android/view/View#setRotationY(kotlin.Float)) 

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
| [ViewPropertyAnimator](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#) | This object, allowing calls to methods in this class to be chained. This value cannot be`null`. |

**See Also**

- [android.view.View#setScaleX(float)](https://developer.android.com/reference/kotlin/android/view/View#setScaleX(kotlin.Float)) 

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
| [ViewPropertyAnimator](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#) | This object, allowing calls to methods in this class to be chained. This value cannot be`null`. |

**See Also**

- [android.view.View#setScaleX(float)](https://developer.android.com/reference/kotlin/android/view/View#setScaleX(kotlin.Float)) 

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
| [ViewPropertyAnimator](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#) | This object, allowing calls to methods in this class to be chained. This value cannot be`null`. |

**See Also**

- [android.view.View#setScaleY(float)](https://developer.android.com/reference/kotlin/android/view/View#setScaleY(kotlin.Float)) 

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
| [ViewPropertyAnimator](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#) | This object, allowing calls to methods in this class to be chained. This value cannot be`null`. |

**See Also**

- [android.view.View#setScaleY(float)](https://developer.android.com/reference/kotlin/android/view/View#setScaleY(kotlin.Float)) 

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
| [ViewPropertyAnimator](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#) | This object, allowing calls to methods in this class to be chained. This value cannot be`null`. |

### setInterpolator

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setInterpolator(interpolator: TimeInterpolator!): ViewPropertyAnimator
```

Sets the interpolator for the underlying animator that animates the requested properties. By default, the animator uses the default interpolator for ValueAnimator. Calling this method will cause the declared object to be used instead.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `interpolator` | [TimeInterpolator](https://developer.android.com/reference/kotlin/android/animation/TimeInterpolator.html#)!:The TimeInterpolator to be used for ensuing property animations. A value of`null`will result in linear interpolation. |

| Return ||
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [ViewPropertyAnimator](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#) | This object, allowing calls to methods in this class to be chained. This value cannot be`null`. |

### setListener

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setListener(listener: Animator.AnimatorListener?): ViewPropertyAnimator
```

Sets a listener for events in the underlying Animators that run the property animations.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [Animator.AnimatorListener](https://developer.android.com/reference/kotlin/android/animation/Animator.AnimatorListener.html#)?:The listener to be called with AnimatorListener events. A value of`null`removes any existing listener. |

| Return ||
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [ViewPropertyAnimator](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#) | This object, allowing calls to methods in this class to be chained. This value cannot be`null`. |

**See Also**

- [android.animation.Animator.AnimatorListener](https://developer.android.com/reference/kotlin/android/animation/Animator.AnimatorListener.html#) 

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
| [ViewPropertyAnimator](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#) | This object, allowing calls to methods in this class to be chained. This value cannot be`null`. |

### setUpdateListener

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setUpdateListener(listener: ValueAnimator.AnimatorUpdateListener?): ViewPropertyAnimator
```

Sets a listener for update events in the underlying ValueAnimator that runs the property animations. Note that the underlying animator is animating between 0 and 1 (these values are then turned into the actual property values internally by ViewPropertyAnimator). So the animator cannot give information on the current values of the properties being animated by this ViewPropertyAnimator, although the view object itself can be queried to get the current values.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [ValueAnimator.AnimatorUpdateListener](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator.AnimatorUpdateListener.html#)?:The listener to be called with update events. A value of`null`removes any existing listener. |

| Return ||
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [ViewPropertyAnimator](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#) | This object, allowing calls to methods in this class to be chained. This value cannot be`null`. |

**See Also**

- [android.animation.ValueAnimator.AnimatorUpdateListener](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator.AnimatorUpdateListener.html#) 

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
| [ViewPropertyAnimator](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#) | This object, allowing calls to methods in this class to be chained. This value cannot be`null`. |

**See Also**

- [android.view.View#setTranslationX(float)](https://developer.android.com/reference/kotlin/android/view/View#setTranslationX(kotlin.Float)) 

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
| [ViewPropertyAnimator](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#) | This object, allowing calls to methods in this class to be chained. This value cannot be`null`. |

**See Also**

- [android.view.View#setTranslationX(float)](https://developer.android.com/reference/kotlin/android/view/View#setTranslationX(kotlin.Float)) 

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
| [ViewPropertyAnimator](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#) | This object, allowing calls to methods in this class to be chained. This value cannot be`null`. |

**See Also**

- [android.view.View#setTranslationY(float)](https://developer.android.com/reference/kotlin/android/view/View#setTranslationY(kotlin.Float)) 

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
| [ViewPropertyAnimator](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#) | This object, allowing calls to methods in this class to be chained. This value cannot be`null`. |

**See Also**

- [android.view.View#setTranslationY(float)](https://developer.android.com/reference/kotlin/android/view/View#setTranslationY(kotlin.Float)) 

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
| [ViewPropertyAnimator](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#) | This object, allowing calls to methods in this class to be chained. This value cannot be`null`. |

**See Also**

- [android.view.View#setTranslationZ(float)](https://developer.android.com/reference/kotlin/android/view/View#setTranslationZ(kotlin.Float)) 

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
| [ViewPropertyAnimator](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#) | This object, allowing calls to methods in this class to be chained. This value cannot be`null`. |

**See Also**

- [android.view.View#setTranslationZ(float)](https://developer.android.com/reference/kotlin/android/view/View#setTranslationZ(kotlin.Float)) 

### withEndAction

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun withEndAction(runnable: Runnable!): ViewPropertyAnimator
```

Specifies an action to take place when the next animation ends. The action is only run if the animation ends normally; if the ViewPropertyAnimator is canceled during that animation, the runnable will not run. This method, along with [withStartAction(java.lang.Runnable)](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#withStartAction(java.lang.Runnable)), is intended to help facilitate choreographing ViewPropertyAnimator animations with other animations or actions in the application.

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
| `runnable` | [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!:The action to run when the next animation ends. |

| Return ||
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [ViewPropertyAnimator](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#) | This object, allowing calls to methods in this class to be chained. This value cannot be`null`. |

### withLayer

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun withLayer(): ViewPropertyAnimator
```

The View associated with this ViewPropertyAnimator will have its [layer type](https://developer.android.com/reference/kotlin/android/view/View#setLayerType(kotlin.Int,%20android.graphics.Paint))set to [View.LAYER_TYPE_HARDWARE](https://developer.android.com/reference/kotlin/android/view/View#LAYER_TYPE_HARDWARE:kotlin.Int) for the duration of the next animation. As stated in the documentation for [View.LAYER_TYPE_HARDWARE](https://developer.android.com/reference/kotlin/android/view/View#LAYER_TYPE_HARDWARE:kotlin.Int), the actual type of layer used internally depends on the runtime situation of the view. If the activity and this view are hardware-accelerated, then the layer will be accelerated as well. If the activity or the view is not accelerated, then the layer will effectively be the same as [View.LAYER_TYPE_SOFTWARE](https://developer.android.com/reference/kotlin/android/view/View#LAYER_TYPE_SOFTWARE:kotlin.Int).

This state is not persistent, either on the View or on this ViewPropertyAnimator: the layer type of the View will be restored when the animation ends to what it was when this method was called, and this setting on ViewPropertyAnimator is only valid for the next animation. Note that calling this method and then independently setting the layer type of the View (by a direct call to [View.setLayerType(int, android.graphics.Paint)](https://developer.android.com/reference/kotlin/android/view/View#setLayerType(kotlin.Int,%20android.graphics.Paint))) will result in some inconsistency, including having the layer type restored to its pre-withLayer() value when the animation ends.

| Return ||
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [ViewPropertyAnimator](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#) | This object, allowing calls to methods in this class to be chained. This value cannot be`null`. |

**See Also**

- [android.view.View#setLayerType(int, android.graphics.Paint)](https://developer.android.com/reference/kotlin/android/view/View#setLayerType(kotlin.Int,%20android.graphics.Paint)) 

### withStartAction

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun withStartAction(runnable: Runnable!): ViewPropertyAnimator
```

Specifies an action to take place when the next animation runs. If there is a [startDelay](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#setStartDelay(kotlin.Long))set on this ViewPropertyAnimator, then the action will run after that startDelay expires, when the actual animation begins. This method, along with [withEndAction(java.lang.Runnable)](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#withEndAction(java.lang.Runnable)), is intended to help facilitate choreographing ViewPropertyAnimator animations with other animations or actions in the application.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------|
| `runnable` | [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#)!:The action to run when the next animation starts. |

| Return ||
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [ViewPropertyAnimator](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#) | This object, allowing calls to methods in this class to be chained. This value cannot be`null`. |

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
| [ViewPropertyAnimator](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#) | This object, allowing calls to methods in this class to be chained. This value cannot be`null`. |

**See Also**

- [android.view.View#setX(float)](https://developer.android.com/reference/kotlin/android/view/View#setX(kotlin.Float)) 

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
| [ViewPropertyAnimator](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#) | This object, allowing calls to methods in this class to be chained. This value cannot be`null`. |

**See Also**

- [android.view.View#setX(float)](https://developer.android.com/reference/kotlin/android/view/View#setX(kotlin.Float)) 

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
| [ViewPropertyAnimator](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#) | This object, allowing calls to methods in this class to be chained. This value cannot be`null`. |

**See Also**

- [android.view.View#setY(float)](https://developer.android.com/reference/kotlin/android/view/View#setY(kotlin.Float)) 

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
| [ViewPropertyAnimator](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#) | This object, allowing calls to methods in this class to be chained. This value cannot be`null`. |

**See Also**

- [android.view.View#setY(float)](https://developer.android.com/reference/kotlin/android/view/View#setY(kotlin.Float)) 

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
| [ViewPropertyAnimator](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#) | This object, allowing calls to methods in this class to be chained. This value cannot be`null`. |

**See Also**

- [android.view.View#setZ(float)](https://developer.android.com/reference/kotlin/android/view/View#setZ(kotlin.Float)) 

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
| [ViewPropertyAnimator](https://developer.android.com/reference/kotlin/android/view/ViewPropertyAnimator#) | This object, allowing calls to methods in this class to be chained. This value cannot be`null`. |

**See Also**

- [android.view.View#setZ(float)](https://developer.android.com/reference/kotlin/android/view/View#setZ(kotlin.Float))
