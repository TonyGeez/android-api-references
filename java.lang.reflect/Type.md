# Type

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Type

```
interface Type
```

| [java.lang.reflect.Type](https://developer.android.com/reference/kotlin/java/lang/reflect/Type#) |

| Known Direct Subclasses [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#), [GenericArrayType](https://developer.android.com/reference/kotlin/java/lang/reflect/GenericArrayType), [ParameterizedType](https://developer.android.com/reference/kotlin/java/lang/reflect/ParameterizedType), [TypeVariable](https://developer.android.com/reference/kotlin/java/lang/reflect/TypeVariable), [WildcardType](https://developer.android.com/reference/kotlin/java/lang/reflect/WildcardType) |---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------| | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#) | Instances of the class represent classes and interfaces in a running Java application. | | [GenericArrayType](https://developer.android.com/reference/kotlin/java/lang/reflect/GenericArrayType) | `GenericArrayType`represents an array type whose component type is either a parameterized type or a type variable. | | [ParameterizedType](https://developer.android.com/reference/kotlin/java/lang/reflect/ParameterizedType) | ParameterizedType represents a parameterized type such as Collection\<String\>. | | [TypeVariable](https://developer.android.com/reference/kotlin/java/lang/reflect/TypeVariable) | TypeVariable is the common superinterface for type variables of kinds. | | [WildcardType](https://developer.android.com/reference/kotlin/java/lang/reflect/WildcardType) | WildcardType represents a wildcard type expression, such as`?`,`? extends Number`, or`? super Integer`. | |

Type is the common superinterface for all types in the Java programming language. These include raw types, parameterized types, array types, type variables and primitive types.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getTypeName](https://developer.android.com/reference/kotlin/java/lang/reflect/Type#getTypeName())`()` Returns a string describing this type, including information about any type parameters. |

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
