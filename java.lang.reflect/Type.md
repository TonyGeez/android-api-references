# Type

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Type

```
interface Type
```

| [java.lang.reflect.Type](Type.md) |

| Known Direct Subclasses [Class](../java.lang/Class.md), [GenericArrayType](GenericArrayType.md), [ParameterizedType](ParameterizedType.md), [TypeVariable](TypeVariable.md), [WildcardType](WildcardType.md) |---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------| | [Class](../java.lang/Class.md) | Instances of the class represent classes and interfaces in a running Java application. | | [GenericArrayType](GenericArrayType.md) | `GenericArrayType`represents an array type whose component type is either a parameterized type or a type variable. | | [ParameterizedType](ParameterizedType.md) | ParameterizedType represents a parameterized type such as Collection\<String\>. | | [TypeVariable](TypeVariable.md) | TypeVariable is the common superinterface for type variables of kinds. | | [WildcardType](WildcardType.md) | WildcardType represents a wildcard type expression, such as`?`,`? extends Number`, or`? super Integer`. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Type is the common superinterface for all types in the Java programming language. These include raw types, parameterized types, array types, type variables and primitive types.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getTypeName](Type.md))`()` Returns a string describing this type, including information about any type parameters. |

## Public methods

### getTypeName

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTypeName(): String
```

Returns a string describing this type, including information about any type parameters.

| Return ||
|----------------------------------------------------------------------------------|-------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string describing this type |
