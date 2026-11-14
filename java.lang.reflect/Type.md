# Type

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Type

```
interface Type
```

| [java.lang.reflect.Type](../java/lang/reflect/Type.md) |

| Known Direct Subclasses [Class](../java/lang/Class.md), [GenericArrayType](../java/lang/reflect/GenericArrayType.md), [ParameterizedType](../java/lang/reflect/ParameterizedType.md), [TypeVariable](../java/lang/reflect/TypeVariable.md), [WildcardType](../java/lang/reflect/WildcardType.md) |---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------| | [Class](../java/lang/Class.md) | Instances of the class represent classes and interfaces in a running Java application. | | [GenericArrayType](../java/lang/reflect/GenericArrayType.md) | `GenericArrayType`represents an array type whose component type is either a parameterized type or a type variable. | | [ParameterizedType](../java/lang/reflect/ParameterizedType.md) | ParameterizedType represents a parameterized type such as Collection\<String\>. | | [TypeVariable](../java/lang/reflect/TypeVariable.md) | TypeVariable is the common superinterface for type variables of kinds. | | [WildcardType](../java/lang/reflect/WildcardType.md) | WildcardType represents a wildcard type expression, such as`?`,`? extends Number`, or`? super Integer`. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Type is the common superinterface for all types in the Java programming language. These include raw types, parameterized types, array types, type variables and primitive types.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getTypeName](../java/lang/reflect/Type.md))`()` Returns a string describing this type, including information about any type parameters. |

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
