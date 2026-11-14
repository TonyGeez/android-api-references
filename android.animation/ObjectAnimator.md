# ObjectAnimator

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ObjectAnimator

Kotlin| [Java](https://developer.android.com/reference/android/animation/ObjectAnimator "View this page in Java") 
| --- | --- |

```
class ObjectAnimator : ValueAnimator
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [android.animation.Animator](https://developer.android.com/reference/kotlin/android/animation/Animator) |||
| | ↳ | [android.animation.ValueAnimator](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator) ||
| | | ↳ | [android.animation.ObjectAnimator](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#) |
| --- | --- | --- | --- |

This subclass of [ValueAnimator](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator) provides support for animating properties on target objects. The constructors of this class take parameters to define the target object that will be animated as well as the name of the property that will be animated. Appropriate set/get functions are then determined internally and the animation will call these functions as necessary to animate the property.

Animators can be created from either code or resource files, as shown here:

Starting from API 23, it is possible to use [PropertyValuesHolder](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder) and [Keyframe](https://developer.android.com/reference/kotlin/android/animation/Keyframe) in resource files to create more complex animations. Using PropertyValuesHolders allows animators to animate several properties in parallel, as shown in this sample:

Using Keyframes allows animations to follow more complex paths from the start to the end values. Note that you can specify explicit fractional values (from 0 to 1) for each keyframe to determine when, in the overall duration, the animation should arrive at that value. Alternatively, you can leave the fractions off and the keyframes will be equally distributed within the total duration. Also, a keyframe with no value will derive its value from the target object when the animator starts, just like animators with only one value specified. In addition, an optional interpolator can be specified. The interpolator will be applied on the interval between the keyframe that the interpolator is set on and the previous keyframe. When no interpolator is supplied, the default [AccelerateDecelerateInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/AccelerateDecelerateInterpolator.html#) will be used.
|
| ### Developer Guides
|
| For more information about animating with`ObjectAnimator`, read the [Property Animation](https://developer.android.com/guide/topics/graphics/prop-animation.html#object-animator) developer guide.

## Summary

| Inherited constants ||
|---|---|
| From class [Animator](https://developer.android.com/reference/kotlin/android/animation/Animator) |------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [DURATION_INFINITE](https://developer.android.com/reference/kotlin/android/animation/Animator#DURATION_INFINITE:kotlin.Long) <br /> The value used to indicate infinite duration (e.g. when Animators repeat infinitely). <br /> | ||
| From class [ValueAnimator](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator) |----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INFINITE](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator#INFINITE:kotlin.Int) <br /> This value used used with the [setRepeatCount(int)](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator#setRepeatCount(kotlin.Int))property to repeat the animation indefinitely. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESTART](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator#RESTART:kotlin.Int) <br /> When the animation reaches the end and`repeatCount`is INFINITE or a positive value, the animation restarts from the beginning. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REVERSE](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator#REVERSE:kotlin.Int) <br /> When the animation reaches the end and`repeatCount`is INFINITE or a positive value, the animation reverses direction on every iteration. <br /> | ||

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ObjectAnimator](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#ObjectAnimator())`()` Creates a new ObjectAnimator object. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ObjectAnimator](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#) | [clone](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#clone())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getPropertyName](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#getPropertyName())`()` Gets the name of the property that will be animated. |
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)? | [getTarget](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#getTarget())`()` The target object whose property will be animated by this animation |
| --- | --- |
| static [ObjectAnimator](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#)! | [ofArgb](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#ofArgb(kotlin.Any,%20kotlin.String,%20kotlin.Int))`(`target:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `propertyName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `vararg` `values:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs and returns an ObjectAnimator that animates between color values. |
| static [ObjectAnimator](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#)! | [ofArgb](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#ofArgb(android.animation.ObjectAnimator.ofArgb.T,%20android.util.Property,%20kotlin.Int))`(`target:` `T`, `property:` ` [Property](https://developer.android.com/reference/kotlin/android/util/Property.html#)<T,` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!>!`, `vararg` `values:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs and returns an ObjectAnimator that animates between color values. |
| static [ObjectAnimator](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#)! | [ofFloat](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#ofFloat(kotlin.Any,%20kotlin.String,%20kotlin.Float))`(`target:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `propertyName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `vararg` `values:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Constructs and returns an ObjectAnimator that animates between float values. |
| --- | --- |
| static [ObjectAnimator](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#)! | [ofFloat](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#ofFloat(kotlin.Any,%20kotlin.String,%20kotlin.String,%20android.graphics.Path))`(`target:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `xPropertyName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `yPropertyName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `path:` ` [Path](https://developer.android.com/reference/kotlin/android/graphics/Path.html#)!`)` Constructs and returns an ObjectAnimator that animates coordinates along a`Path`using two properties. |
| static [ObjectAnimator](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#)! | [ofFloat](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#ofFloat(android.animation.ObjectAnimator.ofFloat.T,%20android.util.Property,%20android.util.Property,%20android.graphics.Path))`(`target:` `T`, `xProperty:` ` [Property](https://developer.android.com/reference/kotlin/android/util/Property.html#)<T,` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)!>!`, `yProperty:` ` [Property](https://developer.android.com/reference/kotlin/android/util/Property.html#)<T,` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)!>!`, `path:` ` [Path](https://developer.android.com/reference/kotlin/android/graphics/Path.html#)!`)` Constructs and returns an ObjectAnimator that animates coordinates along a`Path`using two properties. |
| static [ObjectAnimator](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#)! | [ofFloat](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#ofFloat(android.animation.ObjectAnimator.ofFloat.T,%20android.util.Property,%20kotlin.Float))`(`target:` `T`, `property:` ` [Property](https://developer.android.com/reference/kotlin/android/util/Property.html#)<T,` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)!>!`, `vararg` `values:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Constructs and returns an ObjectAnimator that animates between float values. |
| --- | --- |
| static [ObjectAnimator](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#)! | [ofInt](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#ofInt(kotlin.Any,%20kotlin.String,%20kotlin.Int))`(`target:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `propertyName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `vararg` `values:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs and returns an ObjectAnimator that animates between int values. |
| static [ObjectAnimator](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#)! | [ofInt](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#ofInt(kotlin.Any,%20kotlin.String,%20kotlin.String,%20android.graphics.Path))`(`target:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `xPropertyName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `yPropertyName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `path:` ` [Path](https://developer.android.com/reference/kotlin/android/graphics/Path.html#)!`)` Constructs and returns an ObjectAnimator that animates coordinates along a`Path`using two properties. |
| static [ObjectAnimator](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#)! | [ofInt](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#ofInt(android.animation.ObjectAnimator.ofInt.T,%20android.util.Property,%20android.util.Property,%20android.graphics.Path))`(`target:` `T`, `xProperty:` ` [Property](https://developer.android.com/reference/kotlin/android/util/Property.html#)<T,` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!>!`, `yProperty:` ` [Property](https://developer.android.com/reference/kotlin/android/util/Property.html#)<T,` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!>!`, `path:` ` [Path](https://developer.android.com/reference/kotlin/android/graphics/Path.html#)!`)` Constructs and returns an ObjectAnimator that animates coordinates along a`Path`using two properties. |
| --- | --- |
| static [ObjectAnimator](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#)! | [ofInt](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#ofInt(android.animation.ObjectAnimator.ofInt.T,%20android.util.Property,%20kotlin.Int))`(`target:` `T`, `property:` ` [Property](https://developer.android.com/reference/kotlin/android/util/Property.html#)<T,` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!>!`, `vararg` `values:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs and returns an ObjectAnimator that animates between int values. |
| static [ObjectAnimator](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#)! | [ofMultiFloat](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#ofMultiFloat(kotlin.Any,%20kotlin.String,%20android.animation.TypeConverter,%20android.animation.TypeEvaluator,%20android.animation.ObjectAnimator.ofMultiFloat.T))`(`target:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `propertyName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `converter:` ` [TypeConverter](https://developer.android.com/reference/kotlin/android/animation/TypeConverter)<T,` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!>!`, `evaluator:` ` [TypeEvaluator](https://developer.android.com/reference/kotlin/android/animation/TypeEvaluator)<T>!`, `vararg` `values:` `T`)` Constructs and returns an ObjectAnimator that animates over values for a multiple float parameters setter. |
| static [ObjectAnimator](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#)! | [ofMultiFloat](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#ofMultiFloat(kotlin.Any,%20kotlin.String,%20android.graphics.Path))`(`target:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `propertyName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `path:` ` [Path](https://developer.android.com/reference/kotlin/android/graphics/Path.html#)!`)` Constructs and returns an ObjectAnimator that animates the target using a multi-float setter along the given`Path`. |
| --- | --- |
| static [ObjectAnimator](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#)! | [ofMultiFloat](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#ofMultiFloat(kotlin.Any,%20kotlin.String,%20kotlin.Array))`(`target:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `propertyName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `values:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!>!`)` Constructs and returns an ObjectAnimator that animates over float values for a multiple parameters setter. |
| static [ObjectAnimator](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#)! | [ofMultiInt](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#ofMultiInt(kotlin.Any,%20kotlin.String,%20android.animation.TypeConverter,%20android.animation.TypeEvaluator,%20android.animation.ObjectAnimator.ofMultiInt.T))`(`target:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `propertyName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `converter:` ` [TypeConverter](https://developer.android.com/reference/kotlin/android/animation/TypeConverter)<T,` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!>!`, `evaluator:` ` [TypeEvaluator](https://developer.android.com/reference/kotlin/android/animation/TypeEvaluator)<T>!`, `vararg` `values:` `T`)` Constructs and returns an ObjectAnimator that animates over values for a multiple int parameters setter. |
| static [ObjectAnimator](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#)! | [ofMultiInt](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#ofMultiInt(kotlin.Any,%20kotlin.String,%20android.graphics.Path))`(`target:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `propertyName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `path:` ` [Path](https://developer.android.com/reference/kotlin/android/graphics/Path.html#)!`)` Constructs and returns an ObjectAnimator that animates the target using a multi-int setter along the given`Path`. |
| --- | --- |
| static [ObjectAnimator](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#)! | [ofMultiInt](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#ofMultiInt(kotlin.Any,%20kotlin.String,%20kotlin.Array))`(`target:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `propertyName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `values:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!>!`)` Constructs and returns an ObjectAnimator that animates over int values for a multiple parameters setter. |
| static [ObjectAnimator](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#) | [ofObject](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#ofObject(kotlin.Any,%20kotlin.String,%20android.animation.TypeConverter,%20android.graphics.Path))`(`target:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `propertyName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `converter:` ` [TypeConverter](https://developer.android.com/reference/kotlin/android/animation/TypeConverter)< [PointF](https://developer.android.com/reference/kotlin/android/graphics/PointF.html#)!,` `*>?`, `path:` ` [Path](https://developer.android.com/reference/kotlin/android/graphics/Path.html#)!`)` Constructs and returns an ObjectAnimator that animates a property along a`Path`. |
| static [ObjectAnimator](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#)! | [ofObject](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#ofObject(kotlin.Any,%20kotlin.String,%20android.animation.TypeEvaluator,%20kotlin.Any))`(`target:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `propertyName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `evaluator:` ` [TypeEvaluator](https://developer.android.com/reference/kotlin/android/animation/TypeEvaluator)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>!`, `vararg` `values:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Constructs and returns an ObjectAnimator that animates between Object values. |
| --- | --- |
| static [ObjectAnimator](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#) | [ofObject](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#ofObject(android.animation.ObjectAnimator.ofObject.T,%20android.util.Property,%20android.animation.TypeConverter,%20android.animation.TypeEvaluator,%20android.animation.ObjectAnimator.ofObject.V))`(`target:` `T`, `property:` ` [Property](https://developer.android.com/reference/kotlin/android/util/Property.html#)<T,` `P>!`, `converter:` ` [TypeConverter](https://developer.android.com/reference/kotlin/android/animation/TypeConverter)<V,` `P>!`, `evaluator:` ` [TypeEvaluator](https://developer.android.com/reference/kotlin/android/animation/TypeEvaluator)<V>!`, `vararg` `values:` `V`)` Constructs and returns an ObjectAnimator that animates between Object values. |
| static [ObjectAnimator](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#) | [ofObject](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#ofObject(android.animation.ObjectAnimator.ofObject.T,%20android.util.Property,%20android.animation.TypeConverter,%20android.graphics.Path))`(`target:` `T`, `property:` ` [Property](https://developer.android.com/reference/kotlin/android/util/Property.html#)<T,` `V>`, `converter:` ` [TypeConverter](https://developer.android.com/reference/kotlin/android/animation/TypeConverter)< [PointF](https://developer.android.com/reference/kotlin/android/graphics/PointF.html#)!,` `V>?`, `path:` ` [Path](https://developer.android.com/reference/kotlin/android/graphics/Path.html#)!`)` Constructs and returns an ObjectAnimator that animates a property along a`Path`. |
| static [ObjectAnimator](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#) | [ofObject](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#ofObject(android.animation.ObjectAnimator.ofObject.T,%20android.util.Property,%20android.animation.TypeEvaluator,%20android.animation.ObjectAnimator.ofObject.V))`(`target:` `T`, `property:` ` [Property](https://developer.android.com/reference/kotlin/android/util/Property.html#)<T,` `V>!`, `evaluator:` ` [TypeEvaluator](https://developer.android.com/reference/kotlin/android/animation/TypeEvaluator)<V>!`, `vararg` `values:` `V`)` Constructs and returns an ObjectAnimator that animates between Object values. |
| --- | --- |
| static [ObjectAnimator](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#) | [ofPropertyValuesHolder](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#ofPropertyValuesHolder(kotlin.Any,%20android.animation.PropertyValuesHolder))`(`target:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `vararg` `values:` ` [PropertyValuesHolder](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder)!`)` Constructs and returns an ObjectAnimator that animates between the sets of values specified in`PropertyValueHolder`objects. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAutoCancel](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#setAutoCancel(kotlin.Boolean))`(`cancel:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` autoCancel controls whether an ObjectAnimator will be canceled automatically when any other ObjectAnimator with the same target and properties is started. |
| [ObjectAnimator](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#) | [setDuration](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#setDuration(kotlin.Long))`(`duration:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the length of the animation. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFloatValues](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#setFloatValues(kotlin.Float))`(`vararg` `values:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setIntValues](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#setIntValues(kotlin.Int))`(`vararg` `values:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setObjectValues](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#setObjectValues(kotlin.Any))`(`vararg` `values:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setProperty](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#setProperty(android.util.Property))`(`property:` ` [Property](https://developer.android.com/reference/kotlin/android/util/Property.html#)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!,` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>`)` Sets the property that will be animated. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPropertyName](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#setPropertyName(kotlin.String))`(`propertyName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Sets the name of the property that will be animated. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTarget](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#setTarget(kotlin.Any))`(`target:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Sets the target object whose property will be animated by this animation. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setupEndValues](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#setupEndValues())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setupStartValues](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#setupStartValues())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [start](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#start())`()` <br /> |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#toString())`()` Returns a string representation of the object. |

| Inherited functions ||
|---|---|
| From class [Animator](https://developer.android.com/reference/kotlin/android/animation/Animator) |------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addListener](https://developer.android.com/reference/kotlin/android/animation/Animator#addListener(android.animation.Animator.AnimatorListener))`(`listener:` ` [Animator.AnimatorListener](https://developer.android.com/reference/kotlin/android/animation/Animator.AnimatorListener)!`)` <br /> Adds a listener to the set of listeners that are sent events through the life of an animation, such as start, repeat, and end. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addPauseListener](https://developer.android.com/reference/kotlin/android/animation/Animator#addPauseListener(android.animation.Animator.AnimatorPauseListener))`(`listener:` ` [Animator.AnimatorPauseListener](https://developer.android.com/reference/kotlin/android/animation/Animator.AnimatorPauseListener)!`)` <br /> Adds a pause listener to this animator. <br /> | | [ArrayList](https://developer.android.com/reference/kotlin/java/util/ArrayList.html#)< [Animator.AnimatorListener](https://developer.android.com/reference/kotlin/android/animation/Animator.AnimatorListener)!>! | [getListeners](https://developer.android.com/reference/kotlin/android/animation/Animator#getListeners())`()` <br /> Gets the set of [android.animation.Animator.AnimatorListener](https://developer.android.com/reference/kotlin/android/animation/Animator.AnimatorListener) objects that are currently listening for events on this`Animator`object. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPaused](https://developer.android.com/reference/kotlin/android/animation/Animator#isPaused())`()` <br /> Returns whether this animator is currently in a paused state. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeAllListeners](https://developer.android.com/reference/kotlin/android/animation/Animator#removeAllListeners())`()` <br /> Removes all [listeners](https://developer.android.com/reference/kotlin/android/animation/Animator#addListener(android.animation.Animator.AnimatorListener))and [pauseListeners](https://developer.android.com/reference/kotlin/android/animation/Animator#addPauseListener(android.animation.Animator.AnimatorPauseListener))from this object. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeListener](https://developer.android.com/reference/kotlin/android/animation/Animator#removeListener(android.animation.Animator.AnimatorListener))`(`listener:` ` [Animator.AnimatorListener](https://developer.android.com/reference/kotlin/android/animation/Animator.AnimatorListener)!`)` <br /> Removes a listener from the set listening to this animation. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removePauseListener](https://developer.android.com/reference/kotlin/android/animation/Animator#removePauseListener(android.animation.Animator.AnimatorPauseListener))`(`listener:` ` [Animator.AnimatorPauseListener](https://developer.android.com/reference/kotlin/android/animation/Animator.AnimatorPauseListener)!`)` <br /> Removes a pause listener from the set listening to this animation. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTarget](https://developer.android.com/reference/kotlin/android/animation/Animator#setTarget(kotlin.Any))`(`target:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> Sets the target object whose property will be animated by this animation. Not all subclasses operate on target objects (for example, [ValueAnimator](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator), but this method is on the superclass for the convenience of dealing generically with those subclasses that do handle targets. **Note:**The target is stored as a weak reference internally to avoid leaking resources by having animators directly reference old targets. Therefore, you should ensure that animator targets always have a hard reference elsewhere. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setupEndValues](https://developer.android.com/reference/kotlin/android/animation/Animator#setupEndValues())`()` <br /> This method tells the object to use appropriate information to extract ending values for the animation. For example, a AnimatorSet object will pass this call to its child objects to tell them to set up the values. A ObjectAnimator object will use the information it has about its target object and PropertyValuesHolder objects to get the start values for its properties. A ValueAnimator object will ignore the request since it does not have enough information (such as a target object) to gather these values. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setupStartValues](https://developer.android.com/reference/kotlin/android/animation/Animator#setupStartValues())`()` <br /> This method tells the object to use appropriate information to extract starting values for the animation. For example, a AnimatorSet object will pass this call to its child objects to tell them to set up the values. A ObjectAnimator object will use the information it has about its target object and PropertyValuesHolder objects to get the start values for its properties. A ValueAnimator object will ignore the request since it does not have enough information (such as a target object) to gather these values. <br /> | ||
| From class [ValueAnimator](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator) |-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addUpdateListener](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator#addUpdateListener(android.animation.ValueAnimator.AnimatorUpdateListener))`(`listener:` ` [ValueAnimator.AnimatorUpdateListener](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator.AnimatorUpdateListener)!`)` <br /> Adds a listener to the set of listeners that are sent update events through the life of an animation. This method is called on all listeners for every frame of the animation, after the values for the animation have been calculated. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [areAnimatorsEnabled](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator#areAnimatorsEnabled())`()` <br /> Returns whether animators are currently enabled, system-wide. By default, all animators are enabled. This can change if either the user sets a Developer Option to set the animator duration scale to 0 or by Battery Savery mode being enabled (which disables all animations). Developers should not typically need to call this method, but should an app wish to show a different experience when animators are disabled, this return value can be used as a decider of which experience to offer. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [cancel](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator#cancel())`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [end](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator#end())`()` <br /> | | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getAnimatedFraction](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator#getAnimatedFraction())`()` <br /> Returns the current animation fraction, which is the elapsed/interpolated fraction used in the most recent frame update on the animation. <br /> | | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getAnimatedValue](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator#getAnimatedValue())`()` <br /> The most recent value calculated by this`ValueAnimator`when there is just one property being animated. This value is only sensible while the animation is running. The main purpose for this read-only property is to retrieve the value from the`ValueAnimator`during a call to [AnimatorUpdateListener.onAnimationUpdate(ValueAnimator)](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator.AnimatorUpdateListener#onAnimationUpdate(android.animation.ValueAnimator)), which is called during each animation frame, immediately after the value is calculated. <br /> | | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getAnimatedValue](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator#getAnimatedValue(kotlin.String))`(`propertyName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> The most recent value calculated by this`ValueAnimator`for`propertyName`. The main purpose for this read-only property is to retrieve the value from the`ValueAnimator`during a call to [AnimatorUpdateListener.onAnimationUpdate(ValueAnimator)](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator.AnimatorUpdateListener#onAnimationUpdate(android.animation.ValueAnimator)), which is called during each animation frame, immediately after the value is calculated. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getCurrentPlayTime](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator#getCurrentPlayTime())`()` <br /> Gets the current position of the animation in time, which is equal to the current time minus the time that the animation started. An animation that is not yet started will return a value of zero, unless the animation has has its play time set via [setCurrentPlayTime(long)](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator#setCurrentPlayTime(kotlin.Long))or [setCurrentFraction(float)](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator#setCurrentFraction(kotlin.Float)), in which case it will return the time that was set. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getDuration](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator#getDuration())`()` <br /> Gets the length of the animation. The default duration is 300 milliseconds. <br /> | | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getDurationScale](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator#getDurationScale())`()` <br /> Returns the system-wide scaling factor for Animator-based animations. This affects both the start delay and duration of all such animations. Setting to 0 will cause animations to end immediately. The default value is 1.0f. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getFrameDelay](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator#getFrameDelay())`()` <br /> The amount of time, in milliseconds, between each frame of the animation. This is a requested time that the animation will attempt to honor, but the actual delay between frames may be different, depending on system load and capabilities. This is a static function because the same delay will be applied to all animations, since they are all run off of a single timing loop. The frame delay may be ignored when the animation system uses an external timing source, such as the display refresh rate (vsync), to govern animations. Note that this method should be called from the same thread that [start()](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator#start())is called in order to check the frame delay for that animation. A runtime exception will be thrown if the calling thread does not have a Looper. <br /> | | [TimeInterpolator](https://developer.android.com/reference/kotlin/android/animation/TimeInterpolator)! | [getInterpolator](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator#getInterpolator())`()` <br /> Returns the timing interpolator that this ValueAnimator uses. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRepeatCount](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator#getRepeatCount())`()` <br /> Defines how many times the animation should repeat. The default value is 0. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRepeatMode](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator#getRepeatMode())`()` <br /> Defines what this animation should do when it reaches the end. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getStartDelay](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator#getStartDelay())`()` <br /> The amount of time, in milliseconds, to delay starting the animation after [start()](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator#start())is called. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getTotalDuration](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator#getTotalDuration())`()` <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [PropertyValuesHolder](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder)!>! | [getValues](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator#getValues())`()` <br /> Returns the values that this ValueAnimator animates between. These values are stored in PropertyValuesHolder objects, even if the ValueAnimator was created with a simple list of value objects instead. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRunning](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator#isRunning())`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isStarted](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator#isStarted())`()` <br /> | | [ValueAnimator](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator)! | [ofArgb](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator#ofArgb(kotlin.Int))`(`vararg` `values:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Constructs and returns a ValueAnimator that animates between color values. A single value implies that that value is the one being animated to. However, this is not typically useful in a ValueAnimator object because there is no way for the object to determine the starting value for the animation (unlike ObjectAnimator, which can derive that value from the target object and property being animated). Therefore, there should typically be two or more values. <br /> | | [ValueAnimator](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator)! | [ofFloat](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator#ofFloat(kotlin.Float))`(`vararg` `values:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` <br /> Constructs and returns a ValueAnimator that animates between float values. A single value implies that that value is the one being animated to. However, this is not typically useful in a ValueAnimator object because there is no way for the object to determine the starting value for the animation (unlike ObjectAnimator, which can derive that value from the target object and property being animated). Therefore, there should typically be two or more values. <br /> | | [ValueAnimator](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator)! | [ofInt](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator#ofInt(kotlin.Int))`(`vararg` `values:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Constructs and returns a ValueAnimator that animates between int values. A single value implies that that value is the one being animated to. However, this is not typically useful in a ValueAnimator object because there is no way for the object to determine the starting value for the animation (unlike ObjectAnimator, which can derive that value from the target object and property being animated). Therefore, there should typically be two or more values. <br /> | | [ValueAnimator](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator)! | [ofObject](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator#ofObject(android.animation.TypeEvaluator,%20kotlin.Any))`(`evaluator:` ` [TypeEvaluator](https://developer.android.com/reference/kotlin/android/animation/TypeEvaluator)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>!`, `vararg` `values:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> Constructs and returns a ValueAnimator that animates between Object values. A single value implies that that value is the one being animated to. However, this is not typically useful in a ValueAnimator object because there is no way for the object to determine the starting value for the animation (unlike ObjectAnimator, which can derive that value from the target object and property being animated). Therefore, there should typically be two or more values. **Note:**The Object values are stored as references to the original objects, which means that changes to those objects after this method is called will affect the values on the animator. If the objects will be mutated externally after this method is called, callers should pass a copy of those objects instead. Since ValueAnimator does not know how to animate between arbitrary Objects, this factory method also takes a TypeEvaluator object that the ValueAnimator will use to perform that interpolation. <br /> | | [ValueAnimator](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator)! | [ofPropertyValuesHolder](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator#ofPropertyValuesHolder(android.animation.PropertyValuesHolder))`(`vararg` `values:` ` [PropertyValuesHolder](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder)!`)` <br /> Constructs and returns a ValueAnimator that animates between the values specified in the PropertyValuesHolder objects. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [pause](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator#pause())`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [registerDurationScaleChangeListener](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator#registerDurationScaleChangeListener(android.animation.ValueAnimator.DurationScaleChangeListener))`(`listener:` ` [ValueAnimator.DurationScaleChangeListener](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator.DurationScaleChangeListener)`)` <br /> Registers a [DurationScaleChangeListener](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator.DurationScaleChangeListener) This listens for changes to the system-wide scaling factor for Animator-based animations. Listeners will be called on the main thread. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeAllUpdateListeners](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator#removeAllUpdateListeners())`()` <br /> Removes all listeners from the set listening to frame updates for this animation. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeUpdateListener](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator#removeUpdateListener(android.animation.ValueAnimator.AnimatorUpdateListener))`(`listener:` ` [ValueAnimator.AnimatorUpdateListener](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator.AnimatorUpdateListener)!`)` <br /> Removes a listener from the set listening to frame updates for this animation. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [resume](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator#resume())`()` <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reverse](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator#reverse())`()` <br /> Plays the ValueAnimator in reverse. If the animation is already running, it will stop itself and play backwards from the point reached when reverse was called. If the animation is not currently running, then it will start from the end and play backwards. This behavior is only set for the current animation; future playing of the animation will use the default behavior of playing forward. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCurrentFraction](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator#setCurrentFraction(kotlin.Float))`(`fraction:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` <br /> Sets the position of the animation to the specified fraction. This fraction should be between 0 and the total fraction of the animation, including any repetition. That is, a fraction of 0 will position the animation at the beginning, a value of 1 at the end, and a value of 2 at the end of a reversing animator that repeats once. If the animation has not yet been started, then it will not advance forward after it is set to this fraction; it will simply set the fraction to this value and perform any appropriate actions based on that fraction. If the animation is already running, then setCurrentFraction() will set the current fraction to this value and continue playing from that point. [Animator.AnimatorListener](https://developer.android.com/reference/kotlin/android/animation/Animator.AnimatorListener) events are not called due to changing the fraction; those events are only processed while the animation is running. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCurrentPlayTime](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator#setCurrentPlayTime(kotlin.Long))`(`playTime:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Sets the position of the animation to the specified point in time. This time should be between 0 and the total duration of the animation, including any repetition. If the animation has not yet been started, then it will not advance forward after it is set to this time; it will simply set the time to this value and perform any appropriate actions based on that time. If the animation is already running, then setCurrentPlayTime() will set the current playing time to this value and continue playing from that point. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEvaluator](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator#setEvaluator(android.animation.TypeEvaluator))`(`value:` ` [TypeEvaluator](https://developer.android.com/reference/kotlin/android/animation/TypeEvaluator)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>!`)` <br /> The type evaluator to be used when calculating the animated values of this animation. The system will automatically assign a float or int evaluator based on the type of`startValue`and`endValue`in the constructor. But if these values are not one of these primitive types, or if different evaluation is desired (such as is necessary with int values that represent colors), a custom evaluator needs to be assigned. For example, when running an animation on color values, the [ArgbEvaluator](https://developer.android.com/reference/kotlin/android/animation/ArgbEvaluator) should be used to get correct RGB color interpolation. If this ValueAnimator has only one set of values being animated between, this evaluator will be used for that set. If there are several sets of values being animated, which is the case if PropertyValuesHolder objects were set on the ValueAnimator, then the evaluator is assigned just to the first PropertyValuesHolder object. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFrameDelay](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator#setFrameDelay(kotlin.Long))`(`frameDelay:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> The amount of time, in milliseconds, between each frame of the animation. This is a requested time that the animation will attempt to honor, but the actual delay between frames may be different, depending on system load and capabilities. This is a static function because the same delay will be applied to all animations, since they are all run off of a single timing loop. The frame delay may be ignored when the animation system uses an external timing source, such as the display refresh rate (vsync), to govern animations. Note that this method should be called from the same thread that [start()](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator#start())is called in order to have the new frame delay take effect on that animation. A runtime exception will be thrown if the calling thread does not have a Looper. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInterpolator](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator#setInterpolator(android.animation.TimeInterpolator))`(`value:` ` [TimeInterpolator](https://developer.android.com/reference/kotlin/android/animation/TimeInterpolator)!`)` <br /> The time interpolator used in calculating the elapsed fraction of this animation. The interpolator determines whether the animation runs with linear or non-linear motion, such as acceleration and deceleration. The default value is [android.view.animation.AccelerateDecelerateInterpolator](https://developer.android.com/reference/kotlin/android/view/animation/AccelerateDecelerateInterpolator.html#) <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRepeatCount](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator#setRepeatCount(kotlin.Int))`(`value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets how many times the animation should be repeated. If the repeat count is 0, the animation is never repeated. If the repeat count is greater than 0 or [INFINITE](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator#INFINITE:kotlin.Int), the repeat mode will be taken into account. The repeat count is 0 by default. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRepeatMode](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator#setRepeatMode(kotlin.Int))`(`value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Defines what this animation should do when it reaches the end. This setting is applied only when the repeat count is either greater than 0 or [INFINITE](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator#INFINITE:kotlin.Int). Defaults to [RESTART](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator#RESTART:kotlin.Int). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStartDelay](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator#setStartDelay(kotlin.Long))`(`startDelay:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> The amount of time, in milliseconds, to delay starting the animation after [start()](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator#start())is called. Note that the start delay should always be non-negative. Any negative start delay will be clamped to 0 on N and above. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setValues](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator#setValues(android.animation.PropertyValuesHolder))`(`vararg` `values:` ` [PropertyValuesHolder](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder)!`)` <br /> Sets the values, per property, being animated between. This function is called internally by the constructors of ValueAnimator that take a list of values. But a ValueAnimator can be constructed without values and this method can be called to set the values manually instead. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [unregisterDurationScaleChangeListener](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator#unregisterDurationScaleChangeListener(android.animation.ValueAnimator.DurationScaleChangeListener))`(`listener:` ` [ValueAnimator.DurationScaleChangeListener](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator.DurationScaleChangeListener)`)` <br /> Unregisters a DurationScaleChangeListener. <br /> | ||

## Public constructors

### ObjectAnimator

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ObjectAnimator()
```

Creates a new ObjectAnimator object. This default constructor is primarily for use internally; the other constructors which take parameters are more generally useful.

## Public methods

### clone

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun clone(): ObjectAnimator
```

| Return ||
|----------------------------------------------------------------------------------------------------|---------------------------|
| [ObjectAnimator](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#) | a clone of this instance. |

| Exceptions ||
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the`Cloneable`interface. Subclasses that override the`clone`method can also throw this exception to indicate that an instance cannot be cloned. |

### getPropertyName

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPropertyName(): String?
```

Gets the name of the property that will be animated. This name will be used to derive a setter function that will be called to set animated values. For example, a property name of`foo`will result in a call to the function`setFoo()`on the target object. If either`valueFrom`or`valueTo`is null, then a getter function will also be derived and called.

If this animator was created with a [Property](https://developer.android.com/reference/kotlin/android/util/Property.html#) object instead of the string name of a property, then this method will return the [name](https://developer.android.com/reference/kotlin/android/util/Property.html#getName())of that Property object instead. If this animator was created with one or more [PropertyValuesHolder](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder) objects, then this method will return the [name](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder#getPropertyName())of that object (if there was just one) or a comma-separated list of all of the names (if there are more than one). 

### getTarget

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTarget(): Any?
```

The target object whose property will be animated by this animation

| Return ||
|-----------------------------------------------------------------------------|----------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)? | The object being animated This value may be`null`. |

### ofArgb

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun ofArgb(
    target: Any!, 
    propertyName: String!, 
    vararg values: Int
): ObjectAnimator!
```

Constructs and returns an ObjectAnimator that animates between color values. A single value implies that that value is the one being animated to, in which case the start value will be derived from the property being animated and the target object when #start() is called for the first time. Two values imply starting and ending values. More than two values imply a starting value, values to animate through along the way, and an ending value (these values will be distributed evenly across the duration of the animation).

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `target` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:The object whose property is to be animated. This object should have a public method on it called`setName()`, where`name`is the value of the`propertyName`parameter. |
| `propertyName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the property being animated. |
| `values` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A set of values that the animation will animate between over time. |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [ObjectAnimator](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#)! | An ObjectAnimator object that is set up to animate between the given values. |

### ofArgb

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun <T : Any!> ofArgb(
    target: T, 
    property: Property<T, Int!>!, 
    vararg values: Int
): ObjectAnimator!
```

Constructs and returns an ObjectAnimator that animates between color values. A single value implies that that value is the one being animated to, in which case the start value will be derived from the property being animated and the target object when #start() is called for the first time. Two values imply starting and ending values. More than two values imply a starting value, values to animate through along the way, and an ending value (these values will be distributed evenly across the duration of the animation).

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `target` | T:The object whose property is to be animated. |
| `property` | [Property](https://developer.android.com/reference/kotlin/android/util/Property.html#)\<T, [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\>!:The property being animated. |
| `values` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A set of values that the animation will animate between over time. |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [ObjectAnimator](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#)! | An ObjectAnimator object that is set up to animate between the given values. |

### ofFloat

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun ofFloat(
    target: Any!, 
    propertyName: String!, 
    vararg values: Float
): ObjectAnimator!
```

Constructs and returns an ObjectAnimator that animates between float values. A single value implies that that value is the one being animated to, in which case the start value will be derived from the property being animated and the target object when #start() is called for the first time. Two values imply starting and ending values. More than two values imply a starting value, values to animate through along the way, and an ending value (these values will be distributed evenly across the duration of the animation).

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `target` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:The object whose property is to be animated. This object should have a public method on it called`setName()`, where`name`is the value of the`propertyName`parameter. |
| `propertyName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the property being animated. |
| `values` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):A set of values that the animation will animate between over time. |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [ObjectAnimator](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#)! | An ObjectAnimator object that is set up to animate between the given values. |

### ofFloat

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun ofFloat(
    target: Any!, 
    xPropertyName: String!, 
    yPropertyName: String!, 
    path: Path!
): ObjectAnimator!
```

Constructs and returns an ObjectAnimator that animates coordinates along a`Path`using two properties. A`Path`animation moves in two dimensions, animating coordinates`(x, y)`together to follow the line. In this variation, the coordinates are floats that are set to separate properties designated by`xPropertyName`and`yPropertyName`.

| Parameters ||
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `target` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:The object whose properties are to be animated. This object should have public methods on it called`setNameX()`and`setNameY`, where`nameX`and`nameY`are the value of the`xPropertyName`and`yPropertyName`parameters, respectively. |
| `xPropertyName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the property for the x coordinate being animated. |
| `yPropertyName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the property for the y coordinate being animated. |
| --- | --- |
| `path` | [Path](https://developer.android.com/reference/kotlin/android/graphics/Path.html#)!:The`Path`to animate values along. |

| Return ||
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [ObjectAnimator](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#)! | An ObjectAnimator object that is set up to animate along`path`. |

### ofFloat

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun <T : Any!> ofFloat(
    target: T, 
    xProperty: Property<T, Float!>!, 
    yProperty: Property<T, Float!>!, 
    path: Path!
): ObjectAnimator!
```

Constructs and returns an ObjectAnimator that animates coordinates along a`Path`using two properties. A`Path`animation moves in two dimensions, animating coordinates`(x, y)`together to follow the line. In this variation, the coordinates are floats that are set to separate properties,`xProperty`and`yProperty`.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `target` | T:The object whose properties are to be animated. |
| `xProperty` | [Property](https://developer.android.com/reference/kotlin/android/util/Property.html#)\<T, [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)!\>!:The property for the x coordinate being animated. |
| `yProperty` | [Property](https://developer.android.com/reference/kotlin/android/util/Property.html#)\<T, [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)!\>!:The property for the y coordinate being animated. |
| --- | --- |
| `path` | [Path](https://developer.android.com/reference/kotlin/android/graphics/Path.html#)!:The`Path`to animate values along. |

| Return ||
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [ObjectAnimator](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#)! | An ObjectAnimator object that is set up to animate along`path`. |

### ofFloat

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun <T : Any!> ofFloat(
    target: T, 
    property: Property<T, Float!>!, 
    vararg values: Float
): ObjectAnimator!
```

Constructs and returns an ObjectAnimator that animates between float values. A single value implies that that value is the one being animated to, in which case the start value will be derived from the property being animated and the target object when #start() is called for the first time. Two values imply starting and ending values. More than two values imply a starting value, values to animate through along the way, and an ending value (these values will be distributed evenly across the duration of the animation).

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `target` | T:The object whose property is to be animated. |
| `property` | [Property](https://developer.android.com/reference/kotlin/android/util/Property.html#)\<T, [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)!\>!:The property being animated. |
| `values` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):A set of values that the animation will animate between over time. |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [ObjectAnimator](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#)! | An ObjectAnimator object that is set up to animate between the given values. |

### ofInt

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun ofInt(
    target: Any!, 
    propertyName: String!, 
    vararg values: Int
): ObjectAnimator!
```

Constructs and returns an ObjectAnimator that animates between int values. A single value implies that that value is the one being animated to, in which case the start value will be derived from the property being animated and the target object when #start() is called for the first time. Two values imply starting and ending values. More than two values imply a starting value, values to animate through along the way, and an ending value (these values will be distributed evenly across the duration of the animation).

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `target` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:The object whose property is to be animated. This object should have a public method on it called`setName()`, where`name`is the value of the`propertyName`parameter. |
| `propertyName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the property being animated. |
| `values` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A set of values that the animation will animate between over time. |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [ObjectAnimator](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#)! | An ObjectAnimator object that is set up to animate between the given values. |

### ofInt

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun ofInt(
    target: Any!, 
    xPropertyName: String!, 
    yPropertyName: String!, 
    path: Path!
): ObjectAnimator!
```

Constructs and returns an ObjectAnimator that animates coordinates along a`Path`using two properties. A`Path`animation moves in two dimensions, animating coordinates`(x, y)`together to follow the line. In this variation, the coordinates are integers that are set to separate properties designated by`xPropertyName`and`yPropertyName`.

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `target` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:The object whose properties are to be animated. This object should have public methods on it called`setNameX()`and`setNameY`, where`nameX`and`nameY`are the value of`xPropertyName`and`yPropertyName`parameters, respectively. |
| `xPropertyName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the property for the x coordinate being animated. |
| `yPropertyName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the property for the y coordinate being animated. |
| --- | --- |
| `path` | [Path](https://developer.android.com/reference/kotlin/android/graphics/Path.html#)!:The`Path`to animate values along. |

| Return ||
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [ObjectAnimator](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#)! | An ObjectAnimator object that is set up to animate along`path`. |

### ofInt

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun <T : Any!> ofInt(
    target: T, 
    xProperty: Property<T, Int!>!, 
    yProperty: Property<T, Int!>!, 
    path: Path!
): ObjectAnimator!
```

Constructs and returns an ObjectAnimator that animates coordinates along a`Path`using two properties. A`Path`animation moves in two dimensions, animating coordinates`(x, y)`together to follow the line. In this variation, the coordinates are integers that are set to separate properties,`xProperty`and`yProperty`.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `target` | T:The object whose properties are to be animated. |
| `xProperty` | [Property](https://developer.android.com/reference/kotlin/android/util/Property.html#)\<T, [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\>!:The property for the x coordinate being animated. |
| `yProperty` | [Property](https://developer.android.com/reference/kotlin/android/util/Property.html#)\<T, [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\>!:The property for the y coordinate being animated. |
| --- | --- |
| `path` | [Path](https://developer.android.com/reference/kotlin/android/graphics/Path.html#)!:The`Path`to animate values along. |

| Return ||
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [ObjectAnimator](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#)! | An ObjectAnimator object that is set up to animate along`path`. |

### ofInt

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun <T : Any!> ofInt(
    target: T, 
    property: Property<T, Int!>!, 
    vararg values: Int
): ObjectAnimator!
```

Constructs and returns an ObjectAnimator that animates between int values. A single value implies that that value is the one being animated to, in which case the start value will be derived from the property being animated and the target object when #start() is called for the first time. Two values imply starting and ending values. More than two values imply a starting value, values to animate through along the way, and an ending value (these values will be distributed evenly across the duration of the animation).

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `target` | T:The object whose property is to be animated. |
| `property` | [Property](https://developer.android.com/reference/kotlin/android/util/Property.html#)\<T, [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\>!:The property being animated. |
| `values` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A set of values that the animation will animate between over time. |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [ObjectAnimator](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#)! | An ObjectAnimator object that is set up to animate between the given values. |

### ofMultiFloat

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
@SafeVarargs static fun <T : Any!> ofMultiFloat(
    target: Any!, 
    propertyName: String!, 
    converter: TypeConverter<T, FloatArray!>!, 
    evaluator: TypeEvaluator<T>!, 
    vararg values: T
): ObjectAnimator!
```

Constructs and returns an ObjectAnimator that animates over values for a multiple float parameters setter. Only public methods that take only float parameters are supported.

At least two values must be provided, a start and end. More than two values imply a starting value, values to animate through along the way, and an ending value (these values will be distributed evenly across the duration of the animation).

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `target` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:The object whose property is to be animated. This object may have a public method on it called`setName()`, where`name`is the value of the`propertyName`parameter.`propertyName`may also be the case-sensitive complete name of the public setter method. |
| `propertyName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the property being animated or the name of the setter method. |
| `converter` | [TypeConverter](https://developer.android.com/reference/kotlin/android/animation/TypeConverter)\<T, [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!\>!:Converts T objects into float parameters for the multi-value setter. |
| --- | --- |
| `evaluator` | [TypeEvaluator](https://developer.android.com/reference/kotlin/android/animation/TypeEvaluator)\<T\>!:A TypeEvaluator that will be called on each animation frame to provide the necessary interpolation between the Object values to derive the animated value. |
| `values` | T:A set of values that the animation will animate between over time. |

| Return ||
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [ObjectAnimator](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#)! | An ObjectAnimator object that is set up to animate between the given values. |

### ofMultiFloat

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun ofMultiFloat(
    target: Any!, 
    propertyName: String!, 
    path: Path!
): ObjectAnimator!
```

Constructs and returns an ObjectAnimator that animates the target using a multi-float setter along the given`Path`. A`Path`animation moves in two dimensions, animating coordinates`(x, y)`together to follow the line. In this variation, the coordinates are float x and y coordinates used in the first and second parameter of the setter, respectively.

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `target` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:The object whose property is to be animated. This object may have a public method on it called`setName()`, where`name`is the value of the`propertyName`parameter.`propertyName`may also be the case-sensitive complete name of the public setter method. |
| `propertyName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the property being animated or the name of the setter method. |
| `path` | [Path](https://developer.android.com/reference/kotlin/android/graphics/Path.html#)!:The`Path`to animate values along. |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [ObjectAnimator](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#)! | An ObjectAnimator object that is set up to animate along`path`. |

### ofMultiFloat

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun ofMultiFloat(
    target: Any!, 
    propertyName: String!, 
    values: Array<FloatArray!>!
): ObjectAnimator!
```

Constructs and returns an ObjectAnimator that animates over float values for a multiple parameters setter. Only public methods that take only float parameters are supported. Each`float[]`contains a complete set of parameters to the setter method. At least two`float[]`values must be provided, a start and end. More than two values imply a starting value, values to animate through along the way, and an ending value (these values will be distributed evenly across the duration of the animation).

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `target` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:The object whose property is to be animated. This object may have a public method on it called`setName()`, where`name`is the value of the`propertyName`parameter.`propertyName`may also be the case-sensitive complete name of the public setter method. |
| `propertyName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the property being animated or the name of the setter method. |
| `values` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!\>!:A set of values that the animation will animate between over time. |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [ObjectAnimator](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#)! | An ObjectAnimator object that is set up to animate between the given values. |

### ofMultiInt

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
@SafeVarargs static fun <T : Any!> ofMultiInt(
    target: Any!, 
    propertyName: String!, 
    converter: TypeConverter<T, IntArray!>!, 
    evaluator: TypeEvaluator<T>!, 
    vararg values: T
): ObjectAnimator!
```

Constructs and returns an ObjectAnimator that animates over values for a multiple int parameters setter. Only public methods that take only int parameters are supported.

At least two values must be provided, a start and end. More than two values imply a starting value, values to animate through along the way, and an ending value (these values will be distributed evenly across the duration of the animation).

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `target` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:The object whose property is to be animated. This object may have a public method on it called`setName()`, where`name`is the value of the`propertyName`parameter.`propertyName`may also be the case-sensitive complete name of the public setter method. |
| `propertyName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the property being animated or the name of the setter method. |
| `converter` | [TypeConverter](https://developer.android.com/reference/kotlin/android/animation/TypeConverter)\<T, [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!\>!:Converts T objects into int parameters for the multi-value setter. |
| --- | --- |
| `evaluator` | [TypeEvaluator](https://developer.android.com/reference/kotlin/android/animation/TypeEvaluator)\<T\>!:A TypeEvaluator that will be called on each animation frame to provide the necessary interpolation between the Object values to derive the animated value. |
| `values` | T:A set of values that the animation will animate between over time. |

| Return ||
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [ObjectAnimator](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#)! | An ObjectAnimator object that is set up to animate between the given values. |

### ofMultiInt

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun ofMultiInt(
    target: Any!, 
    propertyName: String!, 
    path: Path!
): ObjectAnimator!
```

Constructs and returns an ObjectAnimator that animates the target using a multi-int setter along the given`Path`. A`Path`animation moves in two dimensions, animating coordinates`(x, y)`together to follow the line. In this variation, the coordinates are integer x and y coordinates used in the first and second parameter of the setter, respectively.

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `target` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:The object whose property is to be animated. This object may have a public method on it called`setName()`, where`name`is the value of the`propertyName`parameter.`propertyName`may also be the case-sensitive complete name of the public setter method. |
| `propertyName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the property being animated or the name of the setter method. |
| `path` | [Path](https://developer.android.com/reference/kotlin/android/graphics/Path.html#)!:The`Path`to animate values along. |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [ObjectAnimator](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#)! | An ObjectAnimator object that is set up to animate along`path`. |

### ofMultiInt

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun ofMultiInt(
    target: Any!, 
    propertyName: String!, 
    values: Array<IntArray!>!
): ObjectAnimator!
```

Constructs and returns an ObjectAnimator that animates over int values for a multiple parameters setter. Only public methods that take only int parameters are supported. Each`int[]`contains a complete set of parameters to the setter method. At least two`int[]`values must be provided, a start and end. More than two values imply a starting value, values to animate through along the way, and an ending value (these values will be distributed evenly across the duration of the animation).

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `target` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:The object whose property is to be animated. This object may have a public method on it called`setName()`, where`name`is the value of the`propertyName`parameter.`propertyName`may also be the case-sensitive complete name of the public setter method. |
| `propertyName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the property being animated or the name of the setter method. |
| `values` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!\>!:A set of values that the animation will animate between over time. |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [ObjectAnimator](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#)! | An ObjectAnimator object that is set up to animate between the given values. |

### ofObject

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun ofObject(
    target: Any!, 
    propertyName: String!, 
    converter: TypeConverter<PointF!, *>?, 
    path: Path!
): ObjectAnimator
```

Constructs and returns an ObjectAnimator that animates a property along a`Path`. A`Path`animation moves in two dimensions, animating coordinates`(x, y)`together to follow the line. This variant animates the coordinates in a`PointF`to follow the`Path`. If the`Property`associated with`propertyName`uses a type other than`PointF`,`converter`can be used to change from`PointF`to the type associated with the`Property`.

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `target` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:The object whose property is to be animated. This object should have a public method on it called`setName()`, where`name`is the value of the`propertyName`parameter. |
| `propertyName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the property being animated. |
| `converter` | [TypeConverter](https://developer.android.com/reference/kotlin/android/animation/TypeConverter)\< [PointF](https://developer.android.com/reference/kotlin/android/graphics/PointF.html#)!,\*\>?:Converts a PointF to the type associated with the setter. May be null if conversion is unnecessary. |
| --- | --- |
| `path` | [Path](https://developer.android.com/reference/kotlin/android/graphics/Path.html#)!:The`Path`to animate values along. |

| Return ||
|----------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [ObjectAnimator](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#) | An ObjectAnimator object that is set up to animate along`path`. This value cannot be`null`. |

### ofObject

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun ofObject(
    target: Any!, 
    propertyName: String!, 
    evaluator: TypeEvaluator<Any!>!, 
    vararg values: Any!
): ObjectAnimator!
```

Constructs and returns an ObjectAnimator that animates between Object values. A single value implies that that value is the one being animated to, in which case the start value will be derived from the property being animated and the target object when #start() is called for the first time. Two values imply starting and ending values. More than two values imply a starting value, values to animate through along the way, and an ending value (these values will be distributed evenly across the duration of the animation).

**Note:**The values are stored as references to the original objects, which means that changes to those objects after this method is called will affect the values on the animator. If the objects will be mutated externally after this method is called, callers should pass a copy of those objects instead.

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `target` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:The object whose property is to be animated. This object should have a public method on it called`setName()`, where`name`is the value of the`propertyName`parameter. |
| `propertyName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the property being animated. |
| `evaluator` | [TypeEvaluator](https://developer.android.com/reference/kotlin/android/animation/TypeEvaluator)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>!:A TypeEvaluator that will be called on each animation frame to provide the necessary interpolation between the Object values to derive the animated value. |
| --- | --- |
| `values` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:A set of values that the animation will animate between over time. |

| Return ||
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [ObjectAnimator](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#)! | An ObjectAnimator object that is set up to animate between the given values. |

### ofObject

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
@SafeVarargs static fun <T : Any!, V : Any!, P : Any!> ofObject(
    target: T, 
    property: Property<T, P>!, 
    converter: TypeConverter<V, P>!, 
    evaluator: TypeEvaluator<V>!, 
    vararg values: V
): ObjectAnimator
```

Constructs and returns an ObjectAnimator that animates between Object values. A single value implies that that value is the one being animated to, in which case the start value will be derived from the property being animated and the target object when #start() is called for the first time. Two values imply starting and ending values. More than two values imply a starting value, values to animate through along the way, and an ending value (these values will be distributed evenly across the duration of the animation). This variant supplies a`TypeConverter`to convert from the animated values to the type of the property. If only one value is supplied, the`TypeConverter`must be a [android.animation.BidirectionalTypeConverter](https://developer.android.com/reference/kotlin/android/animation/BidirectionalTypeConverter) to retrieve the current value.

**Note:**The values are stored as references to the original objects, which means that changes to those objects after this method is called will affect the values on the animator. If the objects will be mutated externally after this method is called, callers should pass a copy of those objects instead.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `target` | T:The object whose property is to be animated. |
| `property` | [Property](https://developer.android.com/reference/kotlin/android/util/Property.html#)\<T,P\>!:The property being animated. |
| `converter` | [TypeConverter](https://developer.android.com/reference/kotlin/android/animation/TypeConverter)\<V,P\>!:Converts the animated object to the Property type. |
| --- | --- |
| `evaluator` | [TypeEvaluator](https://developer.android.com/reference/kotlin/android/animation/TypeEvaluator)\<V\>!:A TypeEvaluator that will be called on each animation frame to provide the necessary interpolation between the Object values to derive the animated value. |
| `values` | V:A set of values that the animation will animate between over time. |

| Return ||
|----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [ObjectAnimator](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#) | An ObjectAnimator object that is set up to animate between the given values. This value cannot be`null`. |

### ofObject

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun <T : Any!, V : Any!> ofObject(
    target: T, 
    property: Property<T, V>, 
    converter: TypeConverter<PointF!, V>?, 
    path: Path!
): ObjectAnimator
```

Constructs and returns an ObjectAnimator that animates a property along a`Path`. A`Path`animation moves in two dimensions, animating coordinates`(x, y)`together to follow the line. This variant animates the coordinates in a`PointF`to follow the`Path`. If`property`uses a type other than`PointF`,`converter`can be used to change from`PointF`to the type associated with the`Property`.

The PointF passed to`converter`or`property`, if`converter`is`null`, is reused on each animation frame and should not be stored by the setter or TypeConverter.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `target` | T:The object whose property is to be animated. |
| `property` | [Property](https://developer.android.com/reference/kotlin/android/util/Property.html#)\<T,V\>:The property being animated. Should not be null. |
| `converter` | [TypeConverter](https://developer.android.com/reference/kotlin/android/animation/TypeConverter)\< [PointF](https://developer.android.com/reference/kotlin/android/graphics/PointF.html#)!,V\>?:Converts a PointF to the type associated with the setter. May be null if conversion is unnecessary. |
| --- | --- |
| `path` | [Path](https://developer.android.com/reference/kotlin/android/graphics/Path.html#)!:The`Path`to animate values along. |

| Return ||
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [ObjectAnimator](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#) | An ObjectAnimator object that is set up to animate along`path`. |

### ofObject

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
@SafeVarargs static fun <T : Any!, V : Any!> ofObject(
    target: T, 
    property: Property<T, V>!, 
    evaluator: TypeEvaluator<V>!, 
    vararg values: V
): ObjectAnimator
```

Constructs and returns an ObjectAnimator that animates between Object values. A single value implies that that value is the one being animated to, in which case the start value will be derived from the property being animated and the target object when #start() is called for the first time. Two values imply starting and ending values. More than two values imply a starting value, values to animate through along the way, and an ending value (these values will be distributed evenly across the duration of the animation).

**Note:**The values are stored as references to the original objects, which means that changes to those objects after this method is called will affect the values on the animator. If the objects will be mutated externally after this method is called, callers should pass a copy of those objects instead.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `target` | T:The object whose property is to be animated. |
| `property` | [Property](https://developer.android.com/reference/kotlin/android/util/Property.html#)\<T,V\>!:The property being animated. |
| `evaluator` | [TypeEvaluator](https://developer.android.com/reference/kotlin/android/animation/TypeEvaluator)\<V\>!:A TypeEvaluator that will be called on each animation frame to provide the necessary interpolation between the Object values to derive the animated value. |
| --- | --- |
| `values` | V:A set of values that the animation will animate between over time. |

| Return ||
|----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [ObjectAnimator](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#) | An ObjectAnimator object that is set up to animate between the given values. This value cannot be`null`. |

### ofPropertyValuesHolder

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun ofPropertyValuesHolder(
    target: Any!, 
    vararg values: PropertyValuesHolder!
): ObjectAnimator
```

Constructs and returns an ObjectAnimator that animates between the sets of values specified in`PropertyValueHolder`objects. This variant should be used when animating several properties at once with the same ObjectAnimator, since PropertyValuesHolder allows you to associate a set of animation values with a property name.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `target` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:The object whose property is to be animated. Depending on how the PropertyValuesObjects were constructed, the target object should either have the objects used to construct the PropertyValuesHolder objects or (if the PropertyValuesHOlder objects were created with property names) the target object should have public methods on it called`setName()`, where`name`is the name of the property passed in as the`propertyName`parameter for each of the PropertyValuesHolder objects. |
| `values` | [PropertyValuesHolder](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder)!:A set of PropertyValuesHolder objects whose values will be animated between over time. |

| Return ||
|----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [ObjectAnimator](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#) | An ObjectAnimator object that is set up to animate between the given values. This value cannot be`null`. |

### setAutoCancel

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setAutoCancel(cancel: Boolean): Unit
```

autoCancel controls whether an ObjectAnimator will be canceled automatically when any other ObjectAnimator with the same target and properties is started. Setting this flag may make it easier to run different animators on the same target object without having to keep track of whether there are conflicting animators that need to be manually canceled. Canceling animators must have the same exact set of target properties, in the same order.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cancel` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Whether future ObjectAnimators with the same target and properties as this ObjectAnimator will cause this ObjectAnimator to be canceled. |

### setDuration

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setDuration(duration: Long): ObjectAnimator
```

Sets the length of the animation. The default duration is 300 milliseconds.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------|
| `duration` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The length of the animation, in milliseconds. |

| Return ||
|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ObjectAnimator](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#) | ObjectAnimator The object called with setDuration(). This return value makes it easier to compose statements together that construct and then set the duration, as in`ObjectAnimator.ofInt(target, propertyName, 0, 10).setDuration(500).start()`. This value cannot be`null`. |

### setFloatValues

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setFloatValues(vararg values: Float): Unit
```

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `values` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):A set of values that the animation will animate between over time. |

### setIntValues

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setIntValues(vararg values: Int): Unit
```

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `values` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A set of values that the animation will animate between over time. |

### setObjectValues

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setObjectValues(vararg values: Any!): Unit
```

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------|
| `values` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:The set of values to animate between. |

### setProperty

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setProperty(property: Property<Any!, Any!>): Unit
```

Sets the property that will be animated. Property objects will take precedence over properties specified by the [setPropertyName(java.lang.String)](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#setPropertyName(kotlin.String))method. Animations should be set up to use one or the other, not both.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `property` | [Property](https://developer.android.com/reference/kotlin/android/util/Property.html#)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!, [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>:The property being animated. Should not be null. |

### setPropertyName

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setPropertyName(propertyName: String): Unit
```

Sets the name of the property that will be animated. This name is used to derive a setter function that will be called to set animated values. For example, a property name of`foo`will result in a call to the function`setFoo()`on the target object. If either`valueFrom`or`valueTo`is null, then a getter function will also be derived and called.

For best performance of the mechanism that calls the setter function determined by the name of the property being animated, use`float`or`int`typed values, and make the setter function for those properties have a`void`return value. This will cause the code to take an optimized path for these constrained circumstances. Other property types and return types will work, but will have more overhead in processing the requests due to normal reflection mechanisms.

Note that the setter function derived from this property name must take the same parameter type as the`valueFrom`and`valueTo`properties, otherwise the call to the setter function will fail.

If this ObjectAnimator has been set up to animate several properties together, using more than one PropertyValuesHolder objects, then setting the propertyName simply sets the propertyName in the first of those PropertyValuesHolder objects.

| Parameters ||
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `propertyName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The name of the property being animated. Should not be null. |

### setTarget

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setTarget(target: Any?): Unit
```

Sets the target object whose property will be animated by this animation. Not all subclasses operate on target objects (for example, [ValueAnimator](https://developer.android.com/reference/kotlin/android/animation/ValueAnimator), but this method is on the superclass for the convenience of dealing generically with those subclasses that do handle targets.

**Note:**The target is stored as a weak reference internally to avoid leaking resources by having animators directly reference old targets. Therefore, you should ensure that animator targets always have a hard reference elsewhere.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------|
| `target` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?:This value may be`null`. |

### setupEndValues

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setupEndValues(): Unit
```  

### setupStartValues

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setupStartValues(): Unit
```  

### start

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun start(): Unit
```  

### toString

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |
