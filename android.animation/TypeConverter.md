# TypeConverter

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TypeConverter

Kotlin| [Java](TypeConverter.md) 
| --- | --- |

```
abstract class TypeConverter<T : Any!, V : Any!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.animation.TypeConverter](TypeConverter.md) |

| Known Direct Subclasses [BidirectionalTypeConverter](BidirectionalTypeConverter.md) |---------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------| | [BidirectionalTypeConverter](BidirectionalTypeConverter.md) | Abstract base class used convert type T to another type V and back again. | |
| --- | --- | --- | --- | --- | --- | --- |

Abstract base class used convert type T to another type V. This is necessary when the value types of in animation are different from the property type.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [TypeConverter](TypeConverter.md))`(`fromClass:` ` [Class](../java.lang/Class.md)<T>!`, `toClass:` ` [Class](../java.lang/Class.md)<V>!`)` <br /> |

| Public methods ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstractV | [convert](TypeConverter.md))`(`value:` `T`)` Converts a value from one type to another. |

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
