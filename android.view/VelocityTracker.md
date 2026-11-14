# VelocityTracker

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# VelocityTracker

Kotlin | [Java](VelocityTracker.md) 
| --- | --- |

```
class VelocityTracker
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.VelocityTracker](VelocityTracker.md) |

Helper for tracking the velocity of motion events, for implementing flinging and other such gestures. Use [obtain](VelocityTracker.md)) to retrieve a new instance of the class when you are going to begin tracking. Put the motion events you receive into it with [addMovement(android.view.MotionEvent)](VelocityTracker.md)). When you want to determine the velocity, call [computeCurrentVelocity(int)](VelocityTracker.md)) and then call the velocity-getter methods like [getXVelocity(int)](VelocityTracker.md)), [getYVelocity(int)](VelocityTracker.md)), or [getAxisVelocity(int,int)](VelocityTracker.md)) to retrieve velocity for different axes and/or pointer IDs.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addMovement](VelocityTracker.md))`(`event:` ` [MotionEvent](MotionEvent.md)!`)` Add a user's movement to the tracker. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](VelocityTracker.md))`()` Reset the velocity tracker back to its initial state. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [computeCurrentVelocity](VelocityTracker.md))`(`units:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Equivalent to invoking [computeCurrentVelocity(int,float)](VelocityTracker.md)) with a maximum velocity of Float. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [computeCurrentVelocity](VelocityTracker.md))`(`units:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `maxVelocity:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Compute the current velocity based on the points that have been collected. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getAxisVelocity](VelocityTracker.md))`(`axis:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Equivalent to calling [getAxisVelocity(int,int)](VelocityTracker.md)) for `axis` and the active pointer. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getAxisVelocity](VelocityTracker.md))`(`axis:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieve the last computed velocity for a given motion axis. |
| --- | --- |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getXVelocity](VelocityTracker.md))`()` Retrieve the last computed X velocity. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getXVelocity](VelocityTracker.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieve the last computed X velocity. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getYVelocity](VelocityTracker.md))`()` Retrieve the last computed Y velocity. |
| --- | --- |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getYVelocity](VelocityTracker.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Retrieve the last computed Y velocity. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAxisSupported](VelocityTracker.md))`(`axis:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Checks whether a given velocity-trackable [MotionEvent](MotionEvent.md) axis is supported for velocity tracking by this [VelocityTracker](VelocityTracker.md) instance (refer to [getAxisVelocity(int,int)](VelocityTracker.md)) for a list of potentially velocity-trackable axes). |
| static [VelocityTracker](VelocityTracker.md)! | [obtain](VelocityTracker.md))`()` Retrieve a new VelocityTracker object to watch the velocity of a motion. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [recycle](VelocityTracker.md))`()` Return a VelocityTracker object back to be re-used by others. |

| Protected methods ||
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](VelocityTracker.md))`()` <br /> |

## Public methods

### addMovement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun addMovement(event: MotionEvent!): Unit
```

Add a user's movement to the tracker. You should call this for the initial [MotionEvent.ACTION_DOWN](MotionEvent.md), the following [MotionEvent.ACTION_MOVE](MotionEvent.md) events that you receive, and the final [MotionEvent.ACTION_UP](MotionEvent.md). You can, however, call this for whichever events you desire.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `event` | [MotionEvent](MotionEvent.md)!: The MotionEvent you received and would like to track. |

### clear

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun clear(): Unit
```

Reset the velocity tracker back to its initial state. 

### computeCurrentVelocity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun computeCurrentVelocity(units: Int): Unit
```

Equivalent to invoking [computeCurrentVelocity(int,float)](VelocityTracker.md)) with a maximum velocity of Float.MAX_VALUE. 
**See Also**

- [#computeCurrentVelocity(int, float)](VelocityTracker.md)) 

### computeCurrentVelocity

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun computeCurrentVelocity(
    units: Int, 
    maxVelocity: Float
): Unit
```

Compute the current velocity based on the points that have been collected. Only call this when you actually want to retrieve velocity information, as it is relatively expensive. You can then retrieve the velocity with [getXVelocity()](VelocityTracker.md)) and [getYVelocity()](VelocityTracker.md)).

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `units` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The units you would like the velocity in. A value of 1 provides units per millisecond, 1000 provides units per second, etc. Note that the units referred to here are the same units with which motion is reported. For axes X and Y, the units are pixels. |
| `maxVelocity` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html): The maximum velocity that can be computed by this method. This value must be declared in the same unit as the units parameter. This value must be positive. |

### getAxisVelocity

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAxisVelocity(axis: Int): Float
```

Equivalent to calling [getAxisVelocity(int,int)](VelocityTracker.md)) for `axis` and the active pointer.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `axis` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Which axis' velocity to return. Value is [android.view.MotionEvent#AXIS_X](MotionEvent.md), [android.view.MotionEvent#AXIS_Y](MotionEvent.md), or [android.view.MotionEvent#AXIS_SCROLL](MotionEvent.md) |

| Return ||
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | The previously computed velocity for `axis` for the active pointer if `axis` is supported for velocity tracking, or 0 if velocity tracking is not supported for the axis. |

**See Also**

- [#isAxisSupported(int)](VelocityTracker.md))
- [#getAxisVelocity(int, int)](VelocityTracker.md)) 

### getAxisVelocity

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAxisVelocity(
    axis: Int, 
    id: Int
): Float
```

Retrieve the last computed velocity for a given motion axis. You must first call [computeCurrentVelocity(int)](VelocityTracker.md)) or [computeCurrentVelocity(int,float)](VelocityTracker.md)) before calling this function.

In addition to [MotionEvent.AXIS_X](MotionEvent.md) and [MotionEvent.AXIS_Y](MotionEvent.md) which have been supported since the introduction of this class, the following axes can be candidates for this method:

- [MotionEvent.AXIS_SCROLL](MotionEvent.md): supported starting [android.os.Build.VERSION_CODES#UPSIDE_DOWN_CAKE](../android/os/Build.VERSION_CODES.md)

Before accessing velocities of an axis using this method, check that your [VelocityTracker](VelocityTracker.md) instance supports the axis by using [isAxisSupported(int)](VelocityTracker.md)).

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `axis` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Which axis' velocity to return. Value is [android.view.MotionEvent#AXIS_X](MotionEvent.md), [android.view.MotionEvent#AXIS_Y](MotionEvent.md), or [android.view.MotionEvent#AXIS_SCROLL](MotionEvent.md) |
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Which pointer's velocity to return. |

| Return ||
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | The previously computed velocity for `axis` for pointer ID of `id` if `axis` is supported for velocity tracking, or 0 if velocity tracking is not supported for the axis. |

**See Also**

- [#isAxisSupported(int)](VelocityTracker.md)) 

### getXVelocity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getXVelocity(): Float
```

Retrieve the last computed X velocity. You must first call [computeCurrentVelocity(int)](VelocityTracker.md)) before calling this function.

| Return ||
|--------------------------------------------------------------------------------|-------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | The previously computed X velocity. |

### getXVelocity

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getXVelocity(id: Int): Float
```

Retrieve the last computed X velocity. You must first call [computeCurrentVelocity(int)](VelocityTracker.md)) before calling this function.

| Parameters ||
|------|-----------------------------------------------------------------------------------------------------------------|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Which pointer's velocity to return. |

| Return ||
|--------------------------------------------------------------------------------|-------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | The previously computed X velocity. |

### getYVelocity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getYVelocity(): Float
```

Retrieve the last computed Y velocity. You must first call [computeCurrentVelocity(int)](VelocityTracker.md)) before calling this function.

| Return ||
|--------------------------------------------------------------------------------|-------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | The previously computed Y velocity. |

### getYVelocity

Added in [API level 8](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getYVelocity(id: Int): Float
```

Retrieve the last computed Y velocity. You must first call [computeCurrentVelocity(int)](VelocityTracker.md)) before calling this function.

| Parameters ||
|------|-----------------------------------------------------------------------------------------------------------------|
| `id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Which pointer's velocity to return. |

| Return ||
|--------------------------------------------------------------------------------|-------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | The previously computed Y velocity. |

### isAxisSupported

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isAxisSupported(axis: Int): Boolean
```

Checks whether a given velocity-trackable [MotionEvent](MotionEvent.md) axis is supported for velocity tracking by this [VelocityTracker](VelocityTracker.md) instance (refer to [getAxisVelocity(int,int)](VelocityTracker.md)) for a list of potentially velocity-trackable axes).

Note that the value returned from this method will stay the same for a given instance, so a single check for axis support is enough per a [VelocityTracker](VelocityTracker.md) instance.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `axis` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The axis to check for velocity support. Value is [android.view.MotionEvent#AXIS_X](MotionEvent.md), [android.view.MotionEvent#AXIS_Y](MotionEvent.md), or [android.view.MotionEvent#AXIS_SCROLL](MotionEvent.md) |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true` if `axis` is supported for velocity tracking, or `false` otherwise. |

**See Also**

- [#getAxisVelocity(int, int)](VelocityTracker.md))
- [#getAxisVelocity(int)](VelocityTracker.md)) 

### obtain

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun obtain(): VelocityTracker!
```

Retrieve a new VelocityTracker object to watch the velocity of a motion. Be sure to call [recycle](VelocityTracker.md)) when done. You should generally only maintain an active object while tracking a movement, so that the VelocityTracker can be re-used elsewhere.

| Return ||
|--------------------------------------------------------------------------------------------------|--------------------------------|
| [VelocityTracker](VelocityTracker.md)! | Returns a new VelocityTracker. |

### recycle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun recycle(): Unit
```

Return a VelocityTracker object back to be re-used by others. You must not touch the object after calling this function.

## Protected methods

### finalize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected fun finalize(): Unit
```

| Exceptions ||
|-----------------------|---------------------------------------|
| `java.lang.Throwable` | the `Exception` raised by this method |
