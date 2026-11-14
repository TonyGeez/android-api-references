# GenericArrayType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GenericArrayType

```
interface GenericArrayType : Type
```

| [java.lang.reflect.GenericArrayType](GenericArrayType.md) |

`GenericArrayType`represents an array type whose component type is either a parameterized type or a type variable.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Type](Type.md) | [getGenericComponentType](GenericArrayType.md))`()` Returns a`Type`object representing the component type of this array. |

| Inherited functions ||
|---|---|
| From class [Type](Type.md) |----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getTypeName](Type.md))`()` <br /> Returns a string describing this type, including information about any type parameters. <br /> | ||

## Public methods

### getGenericComponentType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getGenericComponentType(): Type
```

Returns a`Type`object representing the component type of this array. This method creates the component type of the array. See the declaration of for the semantics of the creation process for parameterized types and see [TypeVariable](TypeVariable.md) for the creation process for type variables.

| Return ||
|-------------------------------------------------------------------------------|-------------------------------------------------------------|
| [Type](Type.md) | a`Type`object representing the component type of this array |

| Exceptions ||
|---------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| `java.lang.TypeNotPresentException` | if the underlying array type's component type refers to a non-existent type declaration |
| `java.lang.reflect.MalformedParameterizedTypeException` | if the underlying array type's component type refers to a parameterized type that cannot be instantiated for any reason |
