# Keyframe

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Keyframe

Kotlin| [Java](https://developer.android.com/reference/android/animation/Keyframe "View this page in Java") 

```
abstract class Keyframe : Cloneable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.animation.Keyframe](https://developer.android.com/reference/kotlin/android/animation/Keyframe#) |

This class holds a time/value pair for an animation. The Keyframe class is used by [ValueAnimator](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator) to define the values that the animation target will have over the course of the animation. As the time proceeds from one keyframe to the other, the value of the target object will animate between the value at the previous keyframe and the value at the next keyframe. Each keyframe also holds an optional [TimeInterpolator](https://developer.android.com/reference/kotlin/android/animation/TimeInterpolator) object, which defines the time interpolation over the intervalue preceding the keyframe.

The Keyframe class itself is abstract. The type-specific factory methods will return a subclass of Keyframe specific to the type of value being stored. This is done to improve performance when dealing with the most common cases (e.g.,`float`and`int`values). Other types will fall into a more general Keyframe class that treats its values as Objects. Unless your animation requires dealing with a custom type or a data structure that needs to be animated directly (and evaluated using an implementation of [TypeEvaluator](https://developer.android.com/reference/kotlin/android/animation/TypeEvaluator)), you should stick to using float and int as animations using those types have lower runtime overhead than other types.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------|---|
| [Keyframe](https://developer.android.com/reference/kotlin/android/animation/Keyframe#Keyframe())`()` <br /> |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Keyframe](https://developer.android.com/reference/kotlin/android/animation/Keyframe#) | [clone](https://developer.android.com/reference/kotlin/android/animation/Keyframe#clone())`()` <br /> |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getFraction](https://developer.android.com/reference/kotlin/android/animation/Keyframe#getFraction())`()` Gets the time for this keyframe, as a fraction of the overall animation duration. |
| open [TimeInterpolator](https://developer.android.com/reference/kotlin/android/animation/TimeInterpolator)! | [getInterpolator](https://developer.android.com/reference/kotlin/android/animation/Keyframe#getInterpolator())`()` Gets the optional interpolator for this Keyframe. |
| open [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>! | [getType](https://developer.android.com/reference/kotlin/android/animation/Keyframe#getType())`()` Gets the type of keyframe. |
| abstract [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getValue](https://developer.android.com/reference/kotlin/android/animation/Keyframe#getValue())`()` Gets the value for this Keyframe. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasValue](https://developer.android.com/reference/kotlin/android/animation/Keyframe#hasValue())`()` Indicates whether this keyframe has a valid value. |
| openstatic [Keyframe](https://developer.android.com/reference/kotlin/android/animation/Keyframe#)! | [ofFloat](https://developer.android.com/reference/kotlin/android/animation/Keyframe#ofFloat(kotlin.Float))`(`fraction:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Constructs a Keyframe object with the given time. |
| openstatic [Keyframe](https://developer.android.com/reference/kotlin/android/animation/Keyframe#)! | [ofFloat](https://developer.android.com/reference/kotlin/android/animation/Keyframe#ofFloat(kotlin.Float,%20kotlin.Float))`(`fraction:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `value:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Constructs a Keyframe object with the given time and value. |
| openstatic [Keyframe](https://developer.android.com/reference/kotlin/android/animation/Keyframe#)! | [ofInt](https://developer.android.com/reference/kotlin/android/animation/Keyframe#ofInt(kotlin.Float))`(`fraction:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Constructs a Keyframe object with the given time. |
| openstatic [Keyframe](https://developer.android.com/reference/kotlin/android/animation/Keyframe#)! | [ofInt](https://developer.android.com/reference/kotlin/android/animation/Keyframe#ofInt(kotlin.Float,%20kotlin.Int))`(`fraction:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs a Keyframe object with the given time and value. |
| openstatic [Keyframe](https://developer.android.com/reference/kotlin/android/animation/Keyframe#)! | [ofObject](https://developer.android.com/reference/kotlin/android/animation/Keyframe#ofObject(kotlin.Float))`(`fraction:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Constructs a Keyframe object with the given time. |
| openstatic [Keyframe](https://developer.android.com/reference/kotlin/android/animation/Keyframe#)! | [ofObject](https://developer.android.com/reference/kotlin/android/animation/Keyframe#ofObject(kotlin.Float,%20kotlin.Any))`(`fraction:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `value:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Constructs a Keyframe object with the given time and value. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFraction](https://developer.android.com/reference/kotlin/android/animation/Keyframe#setFraction(kotlin.Float))`(`fraction:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets the time for this keyframe, as a fraction of the overall animation duration. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInterpolator](https://developer.android.com/reference/kotlin/android/animation/Keyframe#setInterpolator(android.animation.TimeInterpolator))`(`interpolator:` ` [TimeInterpolator](https://developer.android.com/reference/kotlin/android/animation/TimeInterpolator)!`)` Sets the optional interpolator for this Keyframe. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setValue](https://developer.android.com/reference/kotlin/android/animation/Keyframe#setValue(kotlin.Any))`(`value:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Sets the value for this Keyframe. |

## Public constructors

### Keyframe

```
Keyframe()
```

## Public methods

### clone

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun clone(): Keyframe
```

| Return ||
|----------------------------------------------------------------------------------------|---------------------------|
| [Keyframe](https://developer.android.com/reference/kotlin/android/animation/Keyframe#) | a clone of this instance. |

| Exceptions ||
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the`Cloneable`interface. Subclasses that override the`clone`method can also throw this exception to indicate that an instance cannot be cloned. |

### getFraction

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFraction(): Float
```

Gets the time for this keyframe, as a fraction of the overall animation duration.

| Return ||
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | The time associated with this keyframe, as a fraction of the overall animation duration. This should be a value between 0 and 1. |

### getInterpolator

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getInterpolator(): TimeInterpolator!
```

Gets the optional interpolator for this Keyframe. A value of`null`indicates that there is no interpolation, which is the same as linear interpolation.

| Return ||
|--------------------------------------------------------------------------------------------------------|----------------------------------------------|
| [TimeInterpolator](https://developer.android.com/reference/kotlin/android/animation/TimeInterpolator)! | The optional interpolator for this Keyframe. |

### getType

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getType(): Class<Any!>!
```

Gets the type of keyframe. This information is used by ValueAnimator to determine the type of [TypeEvaluator](https://developer.android.com/reference/kotlin/android/animation/TypeEvaluator) to use when calculating values between keyframes. The type is based on the type of Keyframe created.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>! | The type of the value stored in the Keyframe. |

### getValue

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getValue(): Any!
```

Gets the value for this Keyframe.

| Return ||
|-----------------------------------------------------------------------------|------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | The value for this Keyframe. |

### hasValue

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasValue(): Boolean
```

Indicates whether this keyframe has a valid value. This method is called internally when an [ObjectAnimator](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator) first starts; keyframes without values are assigned values at that time by deriving the value for the property from the target object.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | boolean Whether this object has a value assigned. |

### ofFloat

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun ofFloat(fraction: Float): Keyframe!
```

Constructs a Keyframe object with the given time. The value at this time will be derived from the target object when the animation first starts (note that this implies that keyframes with no initial value must be used as part of an [ObjectAnimator](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator)). The time defines the time, as a proportion of an overall animation's duration, at which the value will hold true for the animation. The value for the animation between keyframes will be calculated as an interpolation between the values at those keyframes.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fraction` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The time, expressed as a value between 0 and 1, representing the fraction of time elapsed of the overall animation duration. |

### ofFloat

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun ofFloat(
    fraction: Float, 
    value: Float
): Keyframe!
```

Constructs a Keyframe object with the given time and value. The time defines the time, as a proportion of an overall animation's duration, at which the value will hold true for the animation. The value for the animation between keyframes will be calculated as an interpolation between the values at those keyframes.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fraction` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The time, expressed as a value between 0 and 1, representing the fraction of time elapsed of the overall animation duration. |
| `value` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The value that the object will animate to as the animation time approaches the time in this keyframe, and the value animated from as the time passes the time in this keyframe. |

### ofInt

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun ofInt(fraction: Float): Keyframe!
```

Constructs a Keyframe object with the given time. The value at this time will be derived from the target object when the animation first starts (note that this implies that keyframes with no initial value must be used as part of an [ObjectAnimator](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator)). The time defines the time, as a proportion of an overall animation's duration, at which the value will hold true for the animation. The value for the animation between keyframes will be calculated as an interpolation between the values at those keyframes.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fraction` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The time, expressed as a value between 0 and 1, representing the fraction of time elapsed of the overall animation duration. |

### ofInt

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun ofInt(
    fraction: Float, 
    value: Int
): Keyframe!
```

Constructs a Keyframe object with the given time and value. The time defines the time, as a proportion of an overall animation's duration, at which the value will hold true for the animation. The value for the animation between keyframes will be calculated as an interpolation between the values at those keyframes.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fraction` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The time, expressed as a value between 0 and 1, representing the fraction of time elapsed of the overall animation duration. |
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The value that the object will animate to as the animation time approaches the time in this keyframe, and the value animated from as the time passes the time in this keyframe. |

### ofObject

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun ofObject(fraction: Float): Keyframe!
```

Constructs a Keyframe object with the given time. The value at this time will be derived from the target object when the animation first starts (note that this implies that keyframes with no initial value must be used as part of an [ObjectAnimator](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator)). The time defines the time, as a proportion of an overall animation's duration, at which the value will hold true for the animation. The value for the animation between keyframes will be calculated as an interpolation between the values at those keyframes.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fraction` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The time, expressed as a value between 0 and 1, representing the fraction of time elapsed of the overall animation duration. |

### ofObject

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun ofObject(
    fraction: Float, 
    value: Any!
): Keyframe!
```

Constructs a Keyframe object with the given time and value. The time defines the time, as a proportion of an overall animation's duration, at which the value will hold true for the animation. The value for the animation between keyframes will be calculated as an interpolation between the values at those keyframes.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fraction` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The time, expressed as a value between 0 and 1, representing the fraction of time elapsed of the overall animation duration. |
| `value` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:The value that the object will animate to as the animation time approaches the time in this keyframe, and the value animated from as the time passes the time in this keyframe. |

### setFraction

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setFraction(fraction: Float): Unit
```

Sets the time for this keyframe, as a fraction of the overall animation duration.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fraction` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):time associated with this keyframe, as a fraction of the overall animation duration. This should be a value between 0 and 1. |

### setInterpolator

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setInterpolator(interpolator: TimeInterpolator!): Unit
```

Sets the optional interpolator for this Keyframe. A value of`null`indicates that there is no interpolation, which is the same as linear interpolation.

| Return ||
|------------------------------------------------------------------------------|----------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | The optional interpolator for this Keyframe. |

### setValue

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setValue(value: Any!): Unit
```

Sets the value for this Keyframe.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------|
| `value` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:value for this Keyframe. |
