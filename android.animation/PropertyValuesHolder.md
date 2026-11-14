# PropertyValuesHolder

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PropertyValuesHolder

Kotlin| [Java](https://developer.android.com/reference/android/animation/PropertyValuesHolder "View this page in Java") 

```
open class PropertyValuesHolder : Cloneable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.animation.PropertyValuesHolder](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder#) |

This class holds information about a property and the values that that property should take on during an animation. PropertyValuesHolder objects can be used to create animations with ValueAnimator or ObjectAnimator that operate on several different properties in parallel.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [PropertyValuesHolder](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder#) | [clone](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder#clone())`()` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getPropertyName](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder#getPropertyName())`()` Gets the name of the property that will be animated. |
| openstatic [PropertyValuesHolder](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder#)! | [ofFloat](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder#ofFloat(android.util.Property,%20kotlin.Float))`(`property:` ` [Property](https://developer.android.com/reference/kotlin/android/util/Property.html#)<*,` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)!>!`, `vararg` `values:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Constructs and returns a PropertyValuesHolder with a given property and set of float values. |
| openstatic [PropertyValuesHolder](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder#)! | [ofFloat](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder#ofFloat(kotlin.String,%20kotlin.Float))`(`propertyName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `vararg` `values:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Constructs and returns a PropertyValuesHolder with a given property name and set of float values. |
| openstatic [PropertyValuesHolder](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder#)! | [ofInt](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder#ofInt(android.util.Property,%20kotlin.Int))`(`property:` ` [Property](https://developer.android.com/reference/kotlin/android/util/Property.html#)<*,` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!>!`, `vararg` `values:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs and returns a PropertyValuesHolder with a given property and set of int values. |
| openstatic [PropertyValuesHolder](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder#)! | [ofInt](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder#ofInt(kotlin.String,%20kotlin.Int))`(`propertyName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `vararg` `values:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs and returns a PropertyValuesHolder with a given property name and set of int values. |
| openstatic [PropertyValuesHolder](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder#)! | [ofKeyframe](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder#ofKeyframe(android.util.Property,%20android.animation.Keyframe))`(`property:` ` [Property](https://developer.android.com/reference/kotlin/android/util/Property.html#)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!,` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>!`, `vararg` `values:` ` [Keyframe](https://developer.android.com/reference/kotlin/android/animation/Keyframe)!`)` Constructs and returns a PropertyValuesHolder object with the specified property and set of values. |
| openstatic [PropertyValuesHolder](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder#)! | [ofKeyframe](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder#ofKeyframe(kotlin.String,%20android.animation.Keyframe))`(`propertyName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `vararg` `values:` ` [Keyframe](https://developer.android.com/reference/kotlin/android/animation/Keyframe)!`)` Constructs and returns a PropertyValuesHolder object with the specified property name and set of values. |
| openstatic [PropertyValuesHolder](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder#)! | [ofMultiFloat](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder#ofMultiFloat(kotlin.String,%20android.animation.TypeConverter,%20android.animation.TypeEvaluator,%20android.animation.Keyframe))`(`propertyName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `converter:` ` [TypeConverter](https://developer.android.com/reference/kotlin/android/animation/TypeConverter)<T,` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!>!`, `evaluator:` ` [TypeEvaluator](https://developer.android.com/reference/kotlin/android/animation/TypeEvaluator)<T>!`, `vararg` `values:` ` [Keyframe](https://developer.android.com/reference/kotlin/android/animation/Keyframe)!`)` Constructs and returns a PropertyValuesHolder object with the specified property name or setter name for use in a multi-float setter function using ObjectAnimator. |
| openstatic [PropertyValuesHolder](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder#)! | [ofMultiFloat](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder#ofMultiFloat(kotlin.String,%20android.animation.TypeConverter,%20android.animation.TypeEvaluator,%20android.animation.PropertyValuesHolder.ofMultiFloat.V))`(`propertyName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `converter:` ` [TypeConverter](https://developer.android.com/reference/kotlin/android/animation/TypeConverter)<V,` ` [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!>!`, `evaluator:` ` [TypeEvaluator](https://developer.android.com/reference/kotlin/android/animation/TypeEvaluator)<V>!`, `vararg` `values:` `V`)` Constructs and returns a PropertyValuesHolder with a given property and set of Object values for use with ObjectAnimator multi-value setters. |
| openstatic [PropertyValuesHolder](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder#)! | [ofMultiFloat](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder#ofMultiFloat(kotlin.String,%20android.graphics.Path))`(`propertyName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `path:` ` [Path](https://developer.android.com/reference/kotlin/android/graphics/Path.html#)!`)` Constructs and returns a PropertyValuesHolder with a given property name to use as a multi-float setter. |
| openstatic [PropertyValuesHolder](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder#)! | [ofMultiFloat](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder#ofMultiFloat(kotlin.String,%20kotlin.Array))`(`propertyName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `values:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!>!`)` Constructs and returns a PropertyValuesHolder with a given property name and set of`float[]`values. |
| openstatic [PropertyValuesHolder](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder#)! | [ofMultiInt](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder#ofMultiInt(kotlin.String,%20android.animation.TypeConverter,%20android.animation.TypeEvaluator,%20android.animation.Keyframe))`(`propertyName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `converter:` ` [TypeConverter](https://developer.android.com/reference/kotlin/android/animation/TypeConverter)<T,` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!>!`, `evaluator:` ` [TypeEvaluator](https://developer.android.com/reference/kotlin/android/animation/TypeEvaluator)<T>!`, `vararg` `values:` ` [Keyframe](https://developer.android.com/reference/kotlin/android/animation/Keyframe)!`)` Constructs and returns a PropertyValuesHolder object with the specified property name or setter name for use in a multi-int setter function using ObjectAnimator. |
| openstatic [PropertyValuesHolder](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder#)! | [ofMultiInt](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder#ofMultiInt(kotlin.String,%20android.animation.TypeConverter,%20android.animation.TypeEvaluator,%20android.animation.PropertyValuesHolder.ofMultiInt.V))`(`propertyName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `converter:` ` [TypeConverter](https://developer.android.com/reference/kotlin/android/animation/TypeConverter)<V,` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!>!`, `evaluator:` ` [TypeEvaluator](https://developer.android.com/reference/kotlin/android/animation/TypeEvaluator)<V>!`, `vararg` `values:` `V`)` Constructs and returns a PropertyValuesHolder with a given property and set of Object values for use with ObjectAnimator multi-value setters. |
| openstatic [PropertyValuesHolder](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder#)! | [ofMultiInt](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder#ofMultiInt(kotlin.String,%20android.graphics.Path))`(`propertyName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `path:` ` [Path](https://developer.android.com/reference/kotlin/android/graphics/Path.html#)!`)` Constructs and returns a PropertyValuesHolder with a given property name to use as a multi-int setter. |
| openstatic [PropertyValuesHolder](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder#)! | [ofMultiInt](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder#ofMultiInt(kotlin.String,%20kotlin.Array))`(`propertyName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `values:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!>!`)` Constructs and returns a PropertyValuesHolder with a given property name and set of`int[]`values. |
| openstatic [PropertyValuesHolder](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder#)! | [ofObject](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder#ofObject(android.util.Property,%20android.animation.TypeEvaluator,%20android.animation.PropertyValuesHolder.ofObject.V))`(`property:` ` [Property](https://developer.android.com/reference/kotlin/android/util/Property.html#)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!,` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>!`, `evaluator:` ` [TypeEvaluator](https://developer.android.com/reference/kotlin/android/animation/TypeEvaluator)<V>!`, `vararg` `values:` `V`)` Constructs and returns a PropertyValuesHolder with a given property and set of Object values. |
| openstatic [PropertyValuesHolder](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder#)! | [ofObject](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder#ofObject(android.util.Property,%20android.animation.TypeConverter,%20android.graphics.Path))`(`property:` ` [Property](https://developer.android.com/reference/kotlin/android/util/Property.html#)<*,` `V>!`, `converter:` ` [TypeConverter](https://developer.android.com/reference/kotlin/android/animation/TypeConverter)< [PointF](https://developer.android.com/reference/kotlin/android/graphics/PointF.html#)!,` `V>!`, `path:` ` [Path](https://developer.android.com/reference/kotlin/android/graphics/Path.html#)!`)` Constructs and returns a PropertyValuesHolder with a given property and a Path along which the values should be animated. |
| openstatic [PropertyValuesHolder](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder#)! | [ofObject](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder#ofObject(android.util.Property,%20android.animation.TypeConverter,%20android.animation.TypeEvaluator,%20android.animation.PropertyValuesHolder.ofObject.T))`(`property:` ` [Property](https://developer.android.com/reference/kotlin/android/util/Property.html#)<*,` `V>!`, `converter:` ` [TypeConverter](https://developer.android.com/reference/kotlin/android/animation/TypeConverter)<T,` `V>!`, `evaluator:` ` [TypeEvaluator](https://developer.android.com/reference/kotlin/android/animation/TypeEvaluator)<T>!`, `vararg` `values:` `T`)` Constructs and returns a PropertyValuesHolder with a given property and set of Object values. |
| openstatic [PropertyValuesHolder](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder#)! | [ofObject](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder#ofObject(kotlin.String,%20android.animation.TypeConverter,%20android.graphics.Path))`(`propertyName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `converter:` ` [TypeConverter](https://developer.android.com/reference/kotlin/android/animation/TypeConverter)< [PointF](https://developer.android.com/reference/kotlin/android/graphics/PointF.html#)!,` `*>!`, `path:` ` [Path](https://developer.android.com/reference/kotlin/android/graphics/Path.html#)!`)` Constructs and returns a PropertyValuesHolder with a given property name and a Path along which the values should be animated. |
| openstatic [PropertyValuesHolder](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder#)! | [ofObject](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder#ofObject(kotlin.String,%20android.animation.TypeEvaluator,%20kotlin.Any))`(`propertyName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `evaluator:` ` [TypeEvaluator](https://developer.android.com/reference/kotlin/android/animation/TypeEvaluator)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>!`, `vararg` `values:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Constructs and returns a PropertyValuesHolder with a given property name and set of Object values. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setConverter](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder#setConverter(android.animation.TypeConverter))`(`converter:` ` [TypeConverter](https://developer.android.com/reference/kotlin/android/animation/TypeConverter)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!,` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>!`)` Sets the converter to convert from the values type to the setter's parameter type. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEvaluator](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder#setEvaluator(android.animation.TypeEvaluator))`(`evaluator:` ` [TypeEvaluator](https://developer.android.com/reference/kotlin/android/animation/TypeEvaluator)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>!`)` The TypeEvaluator will be automatically determined based on the type of values supplied to PropertyValuesHolder. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFloatValues](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder#setFloatValues(kotlin.Float))`(`vararg` `values:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Set the animated values for this object to this set of floats. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setIntValues](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder#setIntValues(kotlin.Int))`(`vararg` `values:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the animated values for this object to this set of ints. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setKeyframes](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder#setKeyframes(android.animation.Keyframe))`(`vararg` `values:` ` [Keyframe](https://developer.android.com/reference/kotlin/android/animation/Keyframe)!`)` Set the animated values for this object to this set of Keyframes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setObjectValues](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder#setObjectValues(kotlin.Any))`(`vararg` `values:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Set the animated values for this object to this set of Objects. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setProperty](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder#setProperty(android.util.Property))`(`property:` ` [Property](https://developer.android.com/reference/kotlin/android/util/Property.html#)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!,` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>!`)` Sets the property that will be animated. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPropertyName](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder#setPropertyName(kotlin.String))`(`propertyName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the name of the property that will be animated. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder#toString())`()` <br /> |

## Public methods

### clone

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clone(): PropertyValuesHolder
```

| Return ||
|----------------------------------------------------------------------------------------------------------------|---------------------------|
| [PropertyValuesHolder](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder#) | a clone of this instance. |

| Exceptions ||
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the`Cloneable`interface. Subclasses that override the`clone`method can also throw this exception to indicate that an instance cannot be cloned. |

### getPropertyName

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPropertyName(): String!
```

Gets the name of the property that will be animated. This name will be used to derive a setter function that will be called to set animated values. For example, a property name of`foo`will result in a call to the function`setFoo()`on the target object. If either`valueFrom`or`valueTo`is null, then a getter function will also be derived and called. 

### ofFloat

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun ofFloat(
    property: Property<*, Float!>!, 
    vararg values: Float
): PropertyValuesHolder!
```

Constructs and returns a PropertyValuesHolder with a given property and set of float values.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `property` | [Property](https://developer.android.com/reference/kotlin/android/util/Property.html#)\<\*, [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)!\>!:The property being animated. Should not be null. |
| `values` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The values that the property will animate between. |

| Return ||
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [PropertyValuesHolder](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder#)! | PropertyValuesHolder The constructed PropertyValuesHolder object. |

### ofFloat

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun ofFloat(
    propertyName: String!, 
    vararg values: Float
): PropertyValuesHolder!
```

Constructs and returns a PropertyValuesHolder with a given property name and set of float values.

| Parameters ||
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `propertyName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the property being animated. |
| `values` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The values that the named property will animate between. |

| Return ||
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [PropertyValuesHolder](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder#)! | PropertyValuesHolder The constructed PropertyValuesHolder object. |

### ofInt

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun ofInt(
    property: Property<*, Int!>!, 
    vararg values: Int
): PropertyValuesHolder!
```

Constructs and returns a PropertyValuesHolder with a given property and set of int values.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `property` | [Property](https://developer.android.com/reference/kotlin/android/util/Property.html#)\<\*, [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\>!:The property being animated. Should not be null. |
| `values` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The values that the property will animate between. |

| Return ||
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [PropertyValuesHolder](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder#)! | PropertyValuesHolder The constructed PropertyValuesHolder object. |

### ofInt

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun ofInt(
    propertyName: String!, 
    vararg values: Int
): PropertyValuesHolder!
```

Constructs and returns a PropertyValuesHolder with a given property name and set of int values.

| Parameters ||
|----------------|-------------------------------------------------------------------------------------------------------------------------------------|
| `propertyName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the property being animated. |
| `values` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The values that the named property will animate between. |

| Return ||
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [PropertyValuesHolder](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder#)! | PropertyValuesHolder The constructed PropertyValuesHolder object. |

### ofKeyframe

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun ofKeyframe(
    property: Property<Any!, Any!>!, 
    vararg values: Keyframe!
): PropertyValuesHolder!
```

Constructs and returns a PropertyValuesHolder object with the specified property and set of values. These values can be of any type, but the type should be consistent so that an appropriate [android.animation.TypeEvaluator](https://developer.android.com/reference/kotlin/android/animation/TypeEvaluator) can be found that matches the common type.

If there is only one value, it is assumed to be the end value of an animation, and an initial value will be derived, if possible, by calling the property's [android.util.Property#get(Object)](https://developer.android.com/reference/kotlin/android/util/Property.html#get(android.util.Property.T))function. Also, if any value is null, the value will be filled in when the animation starts in the same way. This mechanism of automatically getting null values only works if the PropertyValuesHolder object is used in conjunction with [ObjectAnimator](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator), since otherwise PropertyValuesHolder has no way of determining what the value should be.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `property` | [Property](https://developer.android.com/reference/kotlin/android/util/Property.html#)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!, [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>!:The property associated with this set of values. Should not be null. |
| `values` | [Keyframe](https://developer.android.com/reference/kotlin/android/animation/Keyframe)!:The set of values to animate between. |

### ofKeyframe

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun ofKeyframe(
    propertyName: String!, 
    vararg values: Keyframe!
): PropertyValuesHolder!
```

Constructs and returns a PropertyValuesHolder object with the specified property name and set of values. These values can be of any type, but the type should be consistent so that an appropriate [android.animation.TypeEvaluator](https://developer.android.com/reference/kotlin/android/animation/TypeEvaluator) can be found that matches the common type.

If there is only one value, it is assumed to be the end value of an animation, and an initial value will be derived, if possible, by calling a getter function on the object. Also, if any value is null, the value will be filled in when the animation starts in the same way. This mechanism of automatically getting null values only works if the PropertyValuesHolder object is used in conjunction [ObjectAnimator](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator), and with a getter function derived automatically from`propertyName`, since otherwise PropertyValuesHolder has no way of determining what the value should be.

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `propertyName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the property associated with this set of values. This can be the actual property name to be used when using a ObjectAnimator object, or just a name used to get animated values, such as if this object is used with an ValueAnimator object. |
| `values` | [Keyframe](https://developer.android.com/reference/kotlin/android/animation/Keyframe)!:The set of values to animate between. |

### ofMultiFloat

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <T : Any!> ofMultiFloat(
    propertyName: String!, 
    converter: TypeConverter<T, FloatArray!>!, 
    evaluator: TypeEvaluator<T>!, 
    vararg values: Keyframe!
): PropertyValuesHolder!
```

Constructs and returns a PropertyValuesHolder object with the specified property name or setter name for use in a multi-float setter function using ObjectAnimator. The values can be of any type, but the type should be consistent so that the supplied [android.animation.TypeEvaluator](https://developer.android.com/reference/kotlin/android/animation/TypeEvaluator) can be used to to evaluate the animated value. The`converter`converts the values to parameters in the setter function.

At least two values must be supplied, a start and an end value.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `propertyName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the property to associate with the set of values. This may also be the complete name of a setter function. |
| `converter` | [TypeConverter](https://developer.android.com/reference/kotlin/android/animation/TypeConverter)\<T, [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!\>!:Converts`values`into float parameters for the setter. Can be null if the Keyframes have float\[\] values. |
| `evaluator` | [TypeEvaluator](https://developer.android.com/reference/kotlin/android/animation/TypeEvaluator)\<T\>!:Used to interpolate between values. |
| `values` | [Keyframe](https://developer.android.com/reference/kotlin/android/animation/Keyframe)!:The values at specific fractional times to evaluate between |

| Return ||
|-----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| [PropertyValuesHolder](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder#)! | A PropertyValuesHolder for a multi-float parameter setter. |

### ofMultiFloat

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
@SafeVarargs open static fun <V : Any!> ofMultiFloat(
    propertyName: String!, 
    converter: TypeConverter<V, FloatArray!>!, 
    evaluator: TypeEvaluator<V>!, 
    vararg values: V
): PropertyValuesHolder!
```

Constructs and returns a PropertyValuesHolder with a given property and set of Object values for use with ObjectAnimator multi-value setters. The Object values are converted to`float[]`using the converter.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `propertyName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The property being animated or complete name of the setter. Should not be null. |
| `converter` | [TypeConverter](https://developer.android.com/reference/kotlin/android/animation/TypeConverter)\<V, [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!\>!:Used to convert the animated value to setter parameters. |
| `evaluator` | [TypeEvaluator](https://developer.android.com/reference/kotlin/android/animation/TypeEvaluator)\<V\>!:A TypeEvaluator that will be called on each animation frame to provide the necessary interpolation between the Object values to derive the animated value. |
| `values` | V:The values that the property will animate between. |

| Return ||
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [PropertyValuesHolder](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder#)! | PropertyValuesHolder The constructed PropertyValuesHolder object. |

**See Also**

- [android.animation.ObjectAnimator#ofMultiFloat(Object, String, TypeConverter, TypeEvaluator, Object[])](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#ofMultiFloat(kotlin.Any,%20kotlin.String,%20android.animation.TypeConverter,%20android.animation.TypeEvaluator,%20android.animation.ObjectAnimator.ofMultiFloat.T)) 

### ofMultiFloat

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun ofMultiFloat(
    propertyName: String!, 
    path: Path!
): PropertyValuesHolder!
```

Constructs and returns a PropertyValuesHolder with a given property name to use as a multi-float setter. The values are animated along the path, with the first parameter of the setter set to the x coordinate and the second set to the y coordinate.

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `propertyName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the property being animated. Can also be the case-sensitive name of the entire setter method. Should not be null. The setter must take exactly two`float`parameters. |
| `path` | [Path](https://developer.android.com/reference/kotlin/android/graphics/Path.html#)!:The Path along which the values should be animated. |

| Return ||
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [PropertyValuesHolder](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder#)! | PropertyValuesHolder The constructed PropertyValuesHolder object. |

**See Also**

- [android.animation.ObjectAnimator#ofPropertyValuesHolder(Object, PropertyValuesHolder...)](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#ofPropertyValuesHolder(kotlin.Any,%20android.animation.PropertyValuesHolder)) 

### ofMultiFloat

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun ofMultiFloat(
    propertyName: String!, 
    values: Array<FloatArray!>!
): PropertyValuesHolder!
```

Constructs and returns a PropertyValuesHolder with a given property name and set of`float[]`values. At least two`float[]`values must be supplied, a start and end value. If more values are supplied, the values will be animated from the start, through all intermediate values to the end value. When used with ObjectAnimator, the elements of the array represent the parameters of the setter function.

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `propertyName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the property being animated. Can also be the case-sensitive name of the entire setter method. Should not be null. |
| `values` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html)!\>!:The values that the property will animate between. |

| Return ||
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [PropertyValuesHolder](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder#)! | PropertyValuesHolder The constructed PropertyValuesHolder object. |

**See Also**

- [android.animation.FloatArrayEvaluator#FloatArrayEvaluator(float[])](https://developer.android.com/reference/kotlin/android/animation/FloatArrayEvaluator#FloatArrayEvaluator(kotlin.FloatArray))
- [android.animation.ObjectAnimator#ofMultiFloat(Object, String, TypeConverter, TypeEvaluator, Object[])](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#ofMultiFloat(kotlin.Any,%20kotlin.String,%20android.animation.TypeConverter,%20android.animation.TypeEvaluator,%20android.animation.ObjectAnimator.ofMultiFloat.T)) 

### ofMultiInt

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <T : Any!> ofMultiInt(
    propertyName: String!, 
    converter: TypeConverter<T, IntArray!>!, 
    evaluator: TypeEvaluator<T>!, 
    vararg values: Keyframe!
): PropertyValuesHolder!
```

Constructs and returns a PropertyValuesHolder object with the specified property name or setter name for use in a multi-int setter function using ObjectAnimator. The values can be of any type, but the type should be consistent so that the supplied [android.animation.TypeEvaluator](https://developer.android.com/reference/kotlin/android/animation/TypeEvaluator) can be used to to evaluate the animated value. The`converter`converts the values to parameters in the setter function.

At least two values must be supplied, a start and an end value.

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `propertyName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the property to associate with the set of values. This may also be the complete name of a setter function. |
| `converter` | [TypeConverter](https://developer.android.com/reference/kotlin/android/animation/TypeConverter)\<T, [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!\>!:Converts`values`into int parameters for the setter. Can be null if the Keyframes have int\[\] values. |
| `evaluator` | [TypeEvaluator](https://developer.android.com/reference/kotlin/android/animation/TypeEvaluator)\<T\>!:Used to interpolate between values. |
| `values` | [Keyframe](https://developer.android.com/reference/kotlin/android/animation/Keyframe)!:The values at specific fractional times to evaluate between |

| Return ||
|-----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| [PropertyValuesHolder](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder#)! | A PropertyValuesHolder for a multi-int parameter setter. |

### ofMultiInt

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
@SafeVarargs open static fun <V : Any!> ofMultiInt(
    propertyName: String!, 
    converter: TypeConverter<V, IntArray!>!, 
    evaluator: TypeEvaluator<V>!, 
    vararg values: V
): PropertyValuesHolder!
```

Constructs and returns a PropertyValuesHolder with a given property and set of Object values for use with ObjectAnimator multi-value setters. The Object values are converted to`int[]`using the converter.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `propertyName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The property being animated or complete name of the setter. Should not be null. |
| `converter` | [TypeConverter](https://developer.android.com/reference/kotlin/android/animation/TypeConverter)\<V, [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!\>!:Used to convert the animated value to setter parameters. |
| `evaluator` | [TypeEvaluator](https://developer.android.com/reference/kotlin/android/animation/TypeEvaluator)\<V\>!:A TypeEvaluator that will be called on each animation frame to provide the necessary interpolation between the Object values to derive the animated value. |
| `values` | V:The values that the property will animate between. |

| Return ||
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [PropertyValuesHolder](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder#)! | PropertyValuesHolder The constructed PropertyValuesHolder object. |

**See Also**

- [android.animation.ObjectAnimator#ofMultiInt(Object, String, TypeConverter, TypeEvaluator, Object[])](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#ofMultiInt(kotlin.Any,%20kotlin.String,%20android.animation.TypeConverter,%20android.animation.TypeEvaluator,%20android.animation.ObjectAnimator.ofMultiInt.T))
- [android.animation.ObjectAnimator#ofPropertyValuesHolder(Object, PropertyValuesHolder...)](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#ofPropertyValuesHolder(kotlin.Any,%20android.animation.PropertyValuesHolder)) 

### ofMultiInt

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun ofMultiInt(
    propertyName: String!, 
    path: Path!
): PropertyValuesHolder!
```

Constructs and returns a PropertyValuesHolder with a given property name to use as a multi-int setter. The values are animated along the path, with the first parameter of the setter set to the x coordinate and the second set to the y coordinate.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `propertyName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the property being animated. Can also be the case-sensitive name of the entire setter method. Should not be null. The setter must take exactly two`int`parameters. |
| `path` | [Path](https://developer.android.com/reference/kotlin/android/graphics/Path.html#)!:The Path along which the values should be animated. |

| Return ||
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [PropertyValuesHolder](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder#)! | PropertyValuesHolder The constructed PropertyValuesHolder object. |

**See Also**

- [android.animation.ObjectAnimator#ofPropertyValuesHolder(Object, PropertyValuesHolder...)](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#ofPropertyValuesHolder(kotlin.Any,%20android.animation.PropertyValuesHolder)) 

### ofMultiInt

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun ofMultiInt(
    propertyName: String!, 
    values: Array<IntArray!>!
): PropertyValuesHolder!
```

Constructs and returns a PropertyValuesHolder with a given property name and set of`int[]`values. At least two`int[]`values must be supplied, a start and end value. If more values are supplied, the values will be animated from the start, through all intermediate values to the end value. When used with ObjectAnimator, the elements of the array represent the parameters of the setter function.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `propertyName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the property being animated. Can also be the case-sensitive name of the entire setter method. Should not be null. |
| `values` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!\>!:The values that the property will animate between. |

| Return ||
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [PropertyValuesHolder](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder#)! | PropertyValuesHolder The constructed PropertyValuesHolder object. |

**See Also**

- [android.animation.IntArrayEvaluator#IntArrayEvaluator(int[])](https://developer.android.com/reference/kotlin/android/animation/IntArrayEvaluator#IntArrayEvaluator(kotlin.IntArray))
- [android.animation.ObjectAnimator#ofMultiInt(Object, String, TypeConverter, TypeEvaluator, Object[])](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator#ofMultiInt(kotlin.Any,%20kotlin.String,%20android.animation.TypeConverter,%20android.animation.TypeEvaluator,%20android.animation.ObjectAnimator.ofMultiInt.T)) 

### ofObject

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
@SafeVarargs open static fun <V : Any!> ofObject(
    property: Property<Any!, Any!>!, 
    evaluator: TypeEvaluator<V>!, 
    vararg values: V
): PropertyValuesHolder!
```

Constructs and returns a PropertyValuesHolder with a given property and set of Object values. This variant also takes a TypeEvaluator because the system cannot automatically interpolate between objects of unknown type.

**Note:**The Object values are stored as references to the original objects, which means that changes to those objects after this method is called will affect the values on the PropertyValuesHolder. If the objects will be mutated externally after this method is called, callers should pass a copy of those objects instead.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `property` | [Property](https://developer.android.com/reference/kotlin/android/util/Property.html#)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!, [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>!:The property being animated. Should not be null. |
| `evaluator` | [TypeEvaluator](https://developer.android.com/reference/kotlin/android/animation/TypeEvaluator)\<V\>!:A TypeEvaluator that will be called on each animation frame to provide the necessary interpolation between the Object values to derive the animated value. |
| `values` | V:The values that the property will animate between. |

| Return ||
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [PropertyValuesHolder](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder#)! | PropertyValuesHolder The constructed PropertyValuesHolder object. |

### ofObject

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <V : Any!> ofObject(
    property: Property<*, V>!, 
    converter: TypeConverter<PointF!, V>!, 
    path: Path!
): PropertyValuesHolder!
```

Constructs and returns a PropertyValuesHolder with a given property and a Path along which the values should be animated. This variant supports a`TypeConverter`to convert from`PointF`to the target type.

The PointF passed to`converter`or`property`, if`converter`is`null`, is reused on each animation frame and should not be stored by the setter or TypeConverter.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `property` | [Property](https://developer.android.com/reference/kotlin/android/util/Property.html#)\<\*,V\>!:The property being animated. Should not be null. |
| `converter` | [TypeConverter](https://developer.android.com/reference/kotlin/android/animation/TypeConverter)\< [PointF](https://developer.android.com/reference/kotlin/android/graphics/PointF.html#)!,V\>!:Converts a PointF to the type associated with the setter. May be null if conversion is unnecessary. |
| `path` | [Path](https://developer.android.com/reference/kotlin/android/graphics/Path.html#)!:The Path along which the values should be animated. |

| Return ||
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [PropertyValuesHolder](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder#)! | PropertyValuesHolder The constructed PropertyValuesHolder object. |

### ofObject

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
@SafeVarargs open static fun <T : Any!, V : Any!> ofObject(
    property: Property<*, V>!, 
    converter: TypeConverter<T, V>!, 
    evaluator: TypeEvaluator<T>!, 
    vararg values: T
): PropertyValuesHolder!
```

Constructs and returns a PropertyValuesHolder with a given property and set of Object values. This variant also takes a TypeEvaluator because the system cannot automatically interpolate between objects of unknown type. This variant also takes a`TypeConverter`to convert from animated values to the type of the property. If only one value is supplied, the`TypeConverter`must be a [android.animation.BidirectionalTypeConverter](https://developer.android.com/reference/kotlin/android/animation/BidirectionalTypeConverter) to retrieve the current value.

**Note:**The Object values are stored as references to the original objects, which means that changes to those objects after this method is called will affect the values on the PropertyValuesHolder. If the objects will be mutated externally after this method is called, callers should pass a copy of those objects instead.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `property` | [Property](https://developer.android.com/reference/kotlin/android/util/Property.html#)\<\*,V\>!:The property being animated. Should not be null. |
| `converter` | [TypeConverter](https://developer.android.com/reference/kotlin/android/animation/TypeConverter)\<T,V\>!:Converts the animated object to the Property type. |
| `evaluator` | [TypeEvaluator](https://developer.android.com/reference/kotlin/android/animation/TypeEvaluator)\<T\>!:A TypeEvaluator that will be called on each animation frame to provide the necessary interpolation between the Object values to derive the animated value. |
| `values` | T:The values that the property will animate between. |

| Return ||
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [PropertyValuesHolder](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder#)! | PropertyValuesHolder The constructed PropertyValuesHolder object. |

**See Also**

- [#setConverter(TypeConverter)](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder#setConverter(android.animation.TypeConverter))
- [android.animation.TypeConverter](https://developer.android.com/reference/kotlin/android/animation/TypeConverter) 

### ofObject

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun ofObject(
    propertyName: String!, 
    converter: TypeConverter<PointF!, *>!, 
    path: Path!
): PropertyValuesHolder!
```

Constructs and returns a PropertyValuesHolder with a given property name and a Path along which the values should be animated. This variant supports a`TypeConverter`to convert from`PointF`to the target type.

The PointF passed to`converter`or`property`, if`converter`is`null`, is reused on each animation frame and should not be stored by the setter or TypeConverter.

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `propertyName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the property being animated. |
| `converter` | [TypeConverter](https://developer.android.com/reference/kotlin/android/animation/TypeConverter)\< [PointF](https://developer.android.com/reference/kotlin/android/graphics/PointF.html#)!,\*\>!:Converts a PointF to the type associated with the setter. May be null if conversion is unnecessary. |
| `path` | [Path](https://developer.android.com/reference/kotlin/android/graphics/Path.html#)!:The Path along which the values should be animated. |

| Return ||
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [PropertyValuesHolder](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder#)! | PropertyValuesHolder The constructed PropertyValuesHolder object. |

### ofObject

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun ofObject(
    propertyName: String!, 
    evaluator: TypeEvaluator<Any!>!, 
    vararg values: Any!
): PropertyValuesHolder!
```

Constructs and returns a PropertyValuesHolder with a given property name and set of Object values. This variant also takes a TypeEvaluator because the system cannot automatically interpolate between objects of unknown type.

**Note:**The Object values are stored as references to the original objects, which means that changes to those objects after this method is called will affect the values on the PropertyValuesHolder. If the objects will be mutated externally after this method is called, callers should pass a copy of those objects instead.

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `propertyName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the property being animated. |
| `evaluator` | [TypeEvaluator](https://developer.android.com/reference/kotlin/android/animation/TypeEvaluator)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>!:A TypeEvaluator that will be called on each animation frame to provide the necessary interpolation between the Object values to derive the animated value. |
| `values` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:The values that the named property will animate between. |

| Return ||
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [PropertyValuesHolder](https://developer.android.com/reference/kotlin/android/animation/PropertyValuesHolder#)! | PropertyValuesHolder The constructed PropertyValuesHolder object. |

### setConverter

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setConverter(converter: TypeConverter<Any!, Any!>!): Unit
```

Sets the converter to convert from the values type to the setter's parameter type. If only one value is supplied, converter must be a [android.animation.BidirectionalTypeConverter](https://developer.android.com/reference/kotlin/android/animation/BidirectionalTypeConverter).

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `converter` | [TypeConverter](https://developer.android.com/reference/kotlin/android/animation/TypeConverter)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!, [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>!:The converter to use to convert values. |

### setEvaluator

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setEvaluator(evaluator: TypeEvaluator<Any!>!): Unit
```

The TypeEvaluator will be automatically determined based on the type of values supplied to PropertyValuesHolder. The evaluator can be manually set, however, if so desired. This may be important in cases where either the type of the values supplied do not match the way that they should be interpolated between, or if the values are of a custom type or one not currently understood by the animation system. Currently, only values of type float and int (and their Object equivalents: Float and Integer) are correctly interpolated; all other types require setting a TypeEvaluator.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `evaluator` | [TypeEvaluator](https://developer.android.com/reference/kotlin/android/animation/TypeEvaluator)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>!: |

### setFloatValues

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setFloatValues(vararg values: Float): Unit
```

Set the animated values for this object to this set of floats. If there is only one value, it is assumed to be the end value of an animation, and an initial value will be derived, if possible, by calling a getter function on the object. Also, if any value is null, the value will be filled in when the animation starts in the same way. This mechanism of automatically getting null values only works if the PropertyValuesHolder object is used in conjunction [ObjectAnimator](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator), and with a getter function derived automatically from`propertyName`, since otherwise PropertyValuesHolder has no way of determining what the value should be.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `values` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):One or more values that the animation will animate between. |

### setIntValues

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setIntValues(vararg values: Int): Unit
```

Set the animated values for this object to this set of ints. If there is only one value, it is assumed to be the end value of an animation, and an initial value will be derived, if possible, by calling a getter function on the object. Also, if any value is null, the value will be filled in when the animation starts in the same way. This mechanism of automatically getting null values only works if the PropertyValuesHolder object is used in conjunction [ObjectAnimator](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator), and with a getter function derived automatically from`propertyName`, since otherwise PropertyValuesHolder has no way of determining what the value should be.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------|
| `values` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):One or more values that the animation will animate between. |

### setKeyframes

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setKeyframes(vararg values: Keyframe!): Unit
```

Set the animated values for this object to this set of Keyframes.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `values` | [Keyframe](https://developer.android.com/reference/kotlin/android/animation/Keyframe)!:One or more values that the animation will animate between. |

### setObjectValues

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setObjectValues(vararg values: Any!): Unit
```

Set the animated values for this object to this set of Objects. If there is only one value, it is assumed to be the end value of an animation, and an initial value will be derived, if possible, by calling a getter function on the object. Also, if any value is null, the value will be filled in when the animation starts in the same way. This mechanism of automatically getting null values only works if the PropertyValuesHolder object is used in conjunction [ObjectAnimator](https://developer.android.com/reference/kotlin/android/animation/ObjectAnimator), and with a getter function derived automatically from`propertyName`, since otherwise PropertyValuesHolder has no way of determining what the value should be.

**Note:**The Object values are stored as references to the original objects, which means that changes to those objects after this method is called will affect the values on the PropertyValuesHolder. If the objects will be mutated externally after this method is called, callers should pass a copy of those objects instead.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `values` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:One or more values that the animation will animate between. |

### setProperty

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setProperty(property: Property<Any!, Any!>!): Unit
```

Sets the property that will be animated.

Note that if this PropertyValuesHolder object is used with ObjectAnimator, the property must exist on the target object specified in that ObjectAnimator.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `property` | [Property](https://developer.android.com/reference/kotlin/android/util/Property.html#)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!, [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>!:The property being animated. |

### setPropertyName

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPropertyName(propertyName: String!): Unit
```

Sets the name of the property that will be animated. This name is used to derive a setter function that will be called to set animated values. For example, a property name of`foo`will result in a call to the function`setFoo()`on the target object. If either`valueFrom`or`valueTo`is null, then a getter function will also be derived and called.

Note that the setter function derived from this property name must take the same parameter type as the`valueFrom`and`valueTo`properties, otherwise the call to the setter function will fail.

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------------------------|
| `propertyName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the property being animated. |

### toString

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |
