# BidirectionalTypeConverter

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BidirectionalTypeConverter

Kotlin | [Java](https://developer.android.com/reference/android/animation/BidirectionalTypeConverter "View this page in Java") 

```
abstract class BidirectionalTypeConverter<T : Any!, V : Any!> : TypeConverter<T, V>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [android.animation.TypeConverter](https://developer.android.com/reference/kotlin/android/animation/TypeConverter)\<T, V\> ||
| | ↳ | [android.animation.BidirectionalTypeConverter](https://developer.android.com/reference/kotlin/android/animation/BidirectionalTypeConverter#) |

Abstract base class used convert type T to another type V and back again. This is necessary when the value types of in animation are different from the property type. BidirectionalTypeConverter is needed when only the final value for the animation is supplied to animators.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [BidirectionalTypeConverter](https://developer.android.com/reference/kotlin/android/animation/BidirectionalTypeConverter#BidirectionalTypeConverter(java.lang.Class,%20java.lang.Class))`(`fromClass:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<T>!`, `toClass:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<V>!`)` <br /> |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract T | [convertBack](https://developer.android.com/reference/kotlin/android/animation/BidirectionalTypeConverter#convertBack(android.animation.BidirectionalTypeConverter.V))`(`value:` `V`)` Does a conversion from the target type back to the source type. |
| open [BidirectionalTypeConverter](https://developer.android.com/reference/kotlin/android/animation/BidirectionalTypeConverter#)\<V, T\>! | [invert](https://developer.android.com/reference/kotlin/android/animation/BidirectionalTypeConverter#invert())`()` Returns the inverse of this converter, where the from and to classes are reversed. |

| Inherited functions ||
|---|---|
| From class [TypeConverter](https://developer.android.com/reference/kotlin/android/animation/TypeConverter) |---|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | V | [convert](https://developer.android.com/reference/kotlin/android/animation/TypeConverter#convert(android.animation.TypeConverter.T))`(`value:` `T`)` Converts a value from one type to another. <br /> | ||

## Public constructors

### BidirectionalTypeConverter

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BidirectionalTypeConverter(
    fromClass: Class<T>!, 
    toClass: Class<V>!)
```

## Public methods

### convertBack

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun convertBack(value: V): T
```

Does a conversion from the target type back to the source type. The subclass must implement this when a TypeConverter is used in animations and current values will need to be read for an animation.

| Parameters ||
|---------|---------------------------|
| `value` | V: The Object to convert. |

| Return ||
|---|--------------------------------------------|
| T | A value of type T, converted from `value`. |

### invert

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun invert(): BidirectionalTypeConverter<V, T>!
```

Returns the inverse of this converter, where the from and to classes are reversed. The inverted converter uses this convert to call [convertBack(java.lang.Object)](https://developer.android.com/reference/kotlin/android/animation/BidirectionalTypeConverter#convertBack(android.animation.BidirectionalTypeConverter.V)) for [convert(java.lang.Object)](https://developer.android.com/reference/kotlin/android/animation/TypeConverter#convert(android.animation.TypeConverter.T)) calls and [convert(java.lang.Object)](https://developer.android.com/reference/kotlin/android/animation/TypeConverter#convert(android.animation.TypeConverter.T)) for [convertBack(java.lang.Object)](https://developer.android.com/reference/kotlin/android/animation/BidirectionalTypeConverter#convertBack(android.animation.BidirectionalTypeConverter.V)) calls.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [BidirectionalTypeConverter](https://developer.android.com/reference/kotlin/android/animation/BidirectionalTypeConverter#)<V,` `T>! | The inverse of this converter, where the from and to classes are reversed. |
