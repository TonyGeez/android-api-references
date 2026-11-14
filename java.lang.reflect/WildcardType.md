# WildcardType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WildcardType

```
interface WildcardType : Type
```

| [java.lang.reflect.WildcardType](../java/lang/reflect/WildcardType.md) |

WildcardType represents a wildcard type expression, such as`?`,`? extends Number`, or`? super Integer`.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Type](../java/lang/reflect/Type.md)!\> | [getLowerBounds](../java/lang/reflect/WildcardType.md))`()` Returns an array of`Type`objects representing the lower bound(s) of this type variable. |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Type](../java/lang/reflect/Type.md)!\> | [getUpperBounds](../java/lang/reflect/WildcardType.md))`()` Returns an array of`Type`objects representing the upper bound(s) of this type variable. |

| Inherited functions ||
|---|---|
| From class [Type](../java/lang/reflect/Type.md) |----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getTypeName](../java/lang/reflect/Type.md))`()` <br /> Returns a string describing this type, including information about any type parameters. <br /> | ||

## Public methods

### getLowerBounds

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getLowerBounds(): Array<Type!>
```

Returns an array of`Type`objects representing the lower bound(s) of this type variable. If no lower bound is explicitly declared, the lower bound is the type of`null`. In this case, a zero length array is returned.

For each lower bound B :

- if B is a parameterized type or a type variable, it is created, (see [ParameterizedType](../java/lang/reflect/ParameterizedType.md) for the details of the creation process for parameterized types).
- Otherwise, B is resolved.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Type](../java/lang/reflect/Type.md)!> | an array of Types representing the lower bound(s) of this type variable |

| Exceptions ||
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| `java.lang.TypeNotPresentException` | if any of the bounds refers to a non-existent type declaration |
| `java.lang.reflect.MalformedParameterizedTypeException` | if any of the bounds refer to a parameterized type that cannot be instantiated for any reason |

### getUpperBounds

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getUpperBounds(): Array<Type!>
```

Returns an array of`Type`objects representing the upper bound(s) of this type variable. If no upper bound is explicitly declared, the upper bound is`Object`.

For each upper bound B :

- if B is a parameterized type or a type variable, it is created, (see [ParameterizedType](../java/lang/reflect/ParameterizedType.md) for the details of the creation process for parameterized types).
- Otherwise, B is resolved.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Type](../java/lang/reflect/Type.md)!> | an array of Types representing the upper bound(s) of this type variable |

| Exceptions ||
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| `java.lang.TypeNotPresentException` | if any of the bounds refers to a non-existent type declaration |
| `java.lang.reflect.MalformedParameterizedTypeException` | if any of the bounds refer to a parameterized type that cannot be instantiated for any reason |
