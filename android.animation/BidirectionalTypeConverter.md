# BidirectionalTypeConverter

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BidirectionalTypeConverter

Kotlin | [Java](BidirectionalTypeConverter.md) 
| --- | --- |

```
abstract class BidirectionalTypeConverter<T : Any!, V : Any!> : TypeConverter<T, V>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.animation.TypeConverter](TypeConverter.md)\<T, V\> ||
| | ↳ | [android.animation.BidirectionalTypeConverter](BidirectionalTypeConverter.md) |

Abstract base class used convert type T to another type V and back again. This is necessary when the value types of in animation are different from the property type. BidirectionalTypeConverter is needed when only the final value for the animation is supplied to animators.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [BidirectionalTypeConverter](BidirectionalTypeConverter.md))`(`fromClass:` ` [Class](../java.lang/Class.md)<T>!`, `toClass:` ` [Class](../java.lang/Class.md)<V>!`)` <br /> |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract T | [convertBack](BidirectionalTypeConverter.md))`(`value:` `V`)` Does a conversion from the target type back to the source type. |
| open [BidirectionalTypeConverter](BidirectionalTypeConverter.md)\<V, T\>! | [invert](BidirectionalTypeConverter.md))`()` Returns the inverse of this converter, where the from and to classes are reversed. |

| Inherited functions ||
|---|---|
| From class [TypeConverter](TypeConverter.md) |---|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | V | [convert](TypeConverter.md))`(`value:` `T`)` Converts a value from one type to another. <br /> | ||

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

Returns the inverse of this converter, where the from and to classes are reversed. The inverted converter uses this convert to call [convertBack(java.lang.Object)](BidirectionalTypeConverter.md)) for [convert(java.lang.Object)](TypeConverter.md)) calls and [convert(java.lang.Object)](TypeConverter.md)) for [convertBack(java.lang.Object)](BidirectionalTypeConverter.md)) calls.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [BidirectionalTypeConverter](BidirectionalTypeConverter.md)<V,` `T>! | The inverse of this converter, where the from and to classes are reversed. |
