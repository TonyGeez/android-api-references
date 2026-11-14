# TypeVariable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TypeVariable

```
interface TypeVariable<D : GenericDeclaration!> : Type
```

| [java.lang.reflect.TypeVariable](../java/lang/reflect/TypeVariable.md) |

TypeVariable is the common superinterface for type variables of kinds. A type variable is created the first time it is needed by a reflective method, as specified in this package. If a type variable t is referenced by a type (i.e, class, interface or annotation type) T, and T is declared by the nth enclosing class of T (see JLS 8.1.2), then the creation of t requires the resolution (see JVMS 5) of the ith enclosing class of T, for i = 0 to n, inclusive. Creating a type variable must not cause the creation of its bounds. Repeated creation of a type variable has no effect.

Multiple objects may be instantiated at run-time to represent a given type variable. Even though a type variable is created only once, this does not imply any requirement to cache instances representing the type variable. However, all instances representing a type variable must be equal() to each other. As a consequence, users of type variables must not rely on the identity of instances of classes implementing this interface.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Type](../java/lang/reflect/Type.md)!\> | [getBounds](../java/lang/reflect/TypeVariable.md))`()` Returns an array of`Type`objects representing the upper bound(s) of this type variable. |
| abstractD | [getGenericDeclaration](../java/lang/reflect/TypeVariable.md))`()` Returns the`GenericDeclaration`object representing the generic declaration declared this type variable. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getName](../java/lang/reflect/TypeVariable.md))`()` Returns the name of this type variable, as it occurs in the source code. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [Type](../java/lang/reflect/Type.md) |----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getTypeName](../java/lang/reflect/Type.md))`()` <br /> Returns a string describing this type, including information about any type parameters. <br /> | ||

## Public methods

### getBounds

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getBounds(): Array<Type!>
```

Returns an array of`Type`objects representing the upper bound(s) of this type variable. If no upper bound is explicitly declared, the upper bound is`Object`.

For each upper bound B:

- if B is a parameterized type or a type variable, it is created, (see for the details of the creation process for parameterized types).
- Otherwise, B is resolved.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Type](../java/lang/reflect/Type.md)!> | an array of`Type`s representing the upper bound(s) of this type variable |

| Exceptions ||
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| `java.lang.TypeNotPresentException` | if any of the bounds refers to a non-existent type declaration |
| `java.lang.reflect.MalformedParameterizedTypeException` | if any of the bounds refer to a parameterized type that cannot be instantiated for any reason |

### getGenericDeclaration

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getGenericDeclaration(): D
```

Returns the`GenericDeclaration`object representing the generic declaration declared this type variable.

| Return ||
|---|----------------------------------------------------------|
| D | the generic declaration declared for this type variable. |

### getName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getName(): String
```

Returns the name of this type variable, as it occurs in the source code.

| Return ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the name of this type variable, as it appears in the source code |
