Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ParameterizedType

```
interface ParameterizedType : Type
```

| [java.lang.reflect.ParameterizedType](https://developer.android.com/reference/kotlin/java/lang/reflect/ParameterizedType#) |

ParameterizedType represents a parameterized type such as Collection\<String\>.

A parameterized type is created the first time it is needed by a reflective method, as specified in this package. When a parameterized type p is created, the generic type declaration that p instantiates is resolved, and all type arguments of p are created recursively. See `https://developer.android.com/reference/kotlin/java/lang/reflect/TypeVariable` for details on the creation process for type variables. Repeated creation of a parameterized type has no effect.

Instances of classes that implement this interface must implement an equals() method that equates any two instances that share the same generic type declaration and have equal type parameters.

## Summary

| Public methods ||
|---|---|
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Type](https://developer.android.com/reference/kotlin/java/lang/reflect/Type)!\> | `https://developer.android.com/reference/kotlin/java/lang/reflect/ParameterizedType#getActualTypeArguments()()` Returns an array of `Type` objects representing the actual type arguments to this type. |
| abstract [Type](https://developer.android.com/reference/kotlin/java/lang/reflect/Type)? | `https://developer.android.com/reference/kotlin/java/lang/reflect/ParameterizedType#getOwnerType()()` Returns a `Type` object representing the type that this type is a member of. |
| abstract [Type](https://developer.android.com/reference/kotlin/java/lang/reflect/Type) | `https://developer.android.com/reference/kotlin/java/lang/reflect/ParameterizedType#getRawType()()` Returns the `Type` object representing the class or interface that declared this type. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/java/lang/reflect/Type` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | `https://developer.android.com/reference/kotlin/java/lang/reflect/Type#getTypeName()()` Returns a string describing this type, including information about any type parameters. <br /> | ||

## Public methods

### getActualTypeArguments

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getActualTypeArguments(): Array<Type!>
```

Returns an array of `Type` objects representing the actual type arguments to this type.

Note that in some cases, the returned array be empty. This can occur if this type represents a non-parameterized type nested within a parameterized type.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/lang/reflect/Type!>` | an array of `Type` objects representing the actual type arguments to this type |

| Exceptions ||
|---|---|
| `java.lang.TypeNotPresentException` | if any of the actual type arguments refers to a non-existent type declaration |
| `java.lang.reflect.MalformedParameterizedTypeException` | if any of the actual type parameters refer to a parameterized type that cannot be instantiated for any reason |

### getOwnerType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getOwnerType(): Type?
```

Returns a `Type` object representing the type that this type is a member of. For example, if this type is `O<T>.I<S>`, return a representation of `O<T>`.

If this type is a top-level type, `null` is returned.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/reflect/Type?` | a `Type` object representing the type that this type is a member of. If this type is a top-level type, `null` is returned |

| Exceptions ||
|---|---|
| `java.lang.TypeNotPresentException` | if the owner type refers to a non-existent type declaration |
| `java.lang.reflect.MalformedParameterizedTypeException` | if the owner type refers to a parameterized type that cannot be instantiated for any reason |

### getRawType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getRawType(): Type
```

Returns the `Type` object representing the class or interface that declared this type.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/reflect/Type` | the `Type` object representing the class or interface that declared this type |
