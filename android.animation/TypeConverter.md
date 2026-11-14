# TypeConverter

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TypeConverter

Kotlin| [Java](https://developer.android.com/reference/android/animation/TypeConverter "View this page in Java") 

```
abstract class TypeConverter<T : Any!, V : Any!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.animation.TypeConverter](https://developer.android.com/reference/kotlin/android/animation/TypeConverter#) |

| Known Direct Subclasses [BidirectionalTypeConverter](https://developer.android.com/reference/kotlin/android/animation/BidirectionalTypeConverter) |---------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------| | [BidirectionalTypeConverter](https://developer.android.com/reference/kotlin/android/animation/BidirectionalTypeConverter) | Abstract base class used convert type T to another type V and back again. | |

Abstract base class used convert type T to another type V. This is necessary when the value types of in animation are different from the property type.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [TypeConverter](https://developer.android.com/reference/kotlin/android/animation/TypeConverter#TypeConverter(java.lang.Class,%20java.lang.Class))`(`fromClass:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<T>!`, `toClass:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<V>!`)` <br /> |

| Public methods ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstractV | [convert](https://developer.android.com/reference/kotlin/android/animation/TypeConverter#convert(android.animation.TypeConverter.T))`(`value:` `T`)` Converts a value from one type to another. |

## Public constructors

### TypeConverter

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TypeConverter(
    fromClass: Class<T>!, 
    toClass: Class<V>!)
```

## Public methods

### convert

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun convert(value: T): V
```

Converts a value from one type to another.

| Parameters ||
|---------|--------------------------|
| `value` | T:The Object to convert. |

| Return ||
|---|-------------------------------------------|
| V | A value of type V, converted from`value`. |
