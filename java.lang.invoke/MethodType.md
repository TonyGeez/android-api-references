# MethodType

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MethodType

```
class MethodType : Serializable, TypeDescriptor.OfMethod<Class<*>!, MethodType!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.lang.invoke.MethodType](../java/lang/invoke/MethodType.md) |

A method type represents the arguments and return type accepted and returned by a method handle, or the arguments and return type passed and expected by a method handle caller. Method types must be properly matched between a method handle and all its callers, and the JVM's operations enforce this matching at, specifically during calls to [MethodHandle.invokeExact](../java/lang/invoke/MethodHandle.md))and [MethodHandle.invoke](../java/lang/invoke/MethodHandle.md)), and during execution of`invokedynamic`instructions.

The structure is a return type accompanied by any number of parameter types. The types (primitive,`void`, and reference) are represented by [Class](../java/lang/Class.md) objects. (For ease of exposition, we treat`void`as if it were a type. In fact, it denotes the absence of a return type.)

All instances of`MethodType`are immutable. Two instances are completely interchangeable if they compare equal. Equality depends on pairwise correspondence of the return and parameter types and on nothing else.

This type can be created only by factory methods. All factory methods may cache values, though caching is not guaranteed. Some factory methods are static, while others are virtual methods which modify precursor method types, e.g., by changing a selected parameter.

Factory methods which operate on groups of parameter types are systematically presented in two versions, so that both Java arrays and Java lists can be used to work with groups of parameter types. The query methods`parameterArray`and`parameterList`also provide a choice between arrays and lists.

`MethodType`objects are sometimes derived from bytecode instructions such as`invokedynamic`, specifically from the type descriptor strings associated with the instructions in a class file's constant pool.

Like classes and strings, method types can also be represented directly in a class file's constant pool as constants. A method type may be loaded by an`ldc`instruction which refers to a suitable`CONSTANT_MethodType`constant pool entry. The entry refers to a`CONSTANT_Utf8`spelling for the descriptor string. (For full details on method type constants, see sections 4.4.8 and 5.4.3.5 of the Java Virtual Machine Specification.)

When the JVM materializes a`MethodType`from a descriptor string, all classes named in the descriptor must be accessible, and will be loaded. (But the classes need not be initialized, as is the case with a`CONSTANT_Class`.) This loading may occur at any time before the`MethodType`object is first derived.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MethodType](../java/lang/invoke/MethodType.md)! | [appendParameterTypes](../java/lang/invoke/MethodType.md))`(`vararg` `ptypesToInsert:` ` [Class](../java/lang/Class.md)<*>!`)` Finds or creates a method type with additional parameter types. |
| [MethodType](../java/lang/invoke/MethodType.md)! | [appendParameterTypes](../java/lang/invoke/MethodType.md))`(`ptypesToInsert:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Class](../java/lang/Class.md)<*>!>!`)` Finds or creates a method type with additional parameter types. |
| [MethodType](../java/lang/invoke/MethodType.md)! | [changeParameterType](../java/lang/invoke/MethodType.md))`(`num:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `nptype:` ` [Class](../java/lang/Class.md)<*>!`)` Finds or creates a method type with a single different parameter type. |
| --- | --- |
| [MethodType](../java/lang/invoke/MethodType.md)! | [changeReturnType](../java/lang/invoke/MethodType.md))`(`nrtype:` ` [Class](../java/lang/Class.md)<*>!`)` Finds or creates a method type with a different return type. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [descriptorString](../java/lang/invoke/MethodType.md))`()` Returns a descriptor string for this method type. |
| [MethodType](../java/lang/invoke/MethodType.md)! | [dropParameterTypes](../java/lang/invoke/MethodType.md))`(`start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Finds or creates a method type with some parameter types omitted. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../java/lang/invoke/MethodType.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Compares the specified object with this type for equality. |
| [MethodType](../java/lang/invoke/MethodType.md)! | [erase](../java/lang/invoke/MethodType.md))`()` Erases all reference types to`Object`. |
| static [MethodType](../java/lang/invoke/MethodType.md)! | [fromMethodDescriptorString](../java/lang/invoke/MethodType.md))`(`descriptor:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `loader:` ` [ClassLoader](../java/lang/ClassLoader.md)!`)` Finds or creates an instance of a method type, given the spelling of its bytecode descriptor. |
| --- | --- |
| [MethodType](../java/lang/invoke/MethodType.md)! | [generic](../java/lang/invoke/MethodType.md))`()` Converts all types, both reference and primitive, to`Object`. |
| static [MethodType](../java/lang/invoke/MethodType.md)! | [genericMethodType](../java/lang/invoke/MethodType.md))`(`objectArgCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Finds or creates a method type whose components are all`Object`. |
| static [MethodType](../java/lang/invoke/MethodType.md)! | [genericMethodType](../java/lang/invoke/MethodType.md))`(`objectArgCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `finalArray:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Finds or creates a method type whose components are`Object`with an optional trailing`Object[]`array. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasPrimitives](../java/lang/invoke/MethodType.md))`()` Reports if this type contains a primitive argument or return value. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasWrappers](../java/lang/invoke/MethodType.md))`()` Reports if this type contains a wrapper argument or return value. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../java/lang/invoke/MethodType.md))`()` Returns the hash code value for this method type. |
| --- | --- |
| [MethodType](../java/lang/invoke/MethodType.md)! | [insertParameterTypes](../java/lang/invoke/MethodType.md))`(`num:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `vararg` `ptypesToInsert:` ` [Class](../java/lang/Class.md)<*>!`)` Finds or creates a method type with additional parameter types. |
| [MethodType](../java/lang/invoke/MethodType.md)! | [insertParameterTypes](../java/lang/invoke/MethodType.md))`(`num:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `ptypesToInsert:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Class](../java/lang/Class.md)<*>!>!`)` Finds or creates a method type with additional parameter types. |
| [Class](../java/lang/Class.md)\<\*\>! | [lastParameterType](../java/lang/invoke/MethodType.md))`()` Returns the last parameter type of this method type. |
| --- | --- |
| static [MethodType](../java/lang/invoke/MethodType.md)! | [methodType](../java/lang/invoke/MethodType.md))`(`rtype:` ` [Class](../java/lang/Class.md)<*>!`)` Finds or creates a method type with the given components. |
| static [MethodType](../java/lang/invoke/MethodType.md)! | [methodType](../java/lang/invoke/MethodType.md))`(`rtype:` ` [Class](../java/lang/Class.md)<*>!`, `ptype0:` ` [Class](../java/lang/Class.md)<*>!`)` Finds or creates a method type with the given components. |
| static [MethodType](../java/lang/invoke/MethodType.md)! | [methodType](../java/lang/invoke/MethodType.md))`(`rtype:` ` [Class](../java/lang/Class.md)<*>!`, `ptype0:` ` [Class](../java/lang/Class.md)<*>!`, `vararg` `ptypes:` ` [Class](../java/lang/Class.md)<*>!`)` Finds or creates a method type with the given components. |
| --- | --- |
| static [MethodType](../java/lang/invoke/MethodType.md)! | [methodType](../java/lang/invoke/MethodType.md))`(`rtype:` ` [Class](../java/lang/Class.md)<*>!`, `ptypes:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Class](../java/lang/Class.md)<*>!>!`)` Finds or creates an instance of the given method type. |
| static [MethodType](../java/lang/invoke/MethodType.md)! | [methodType](../java/lang/invoke/MethodType.md))`(`rtype:` ` [Class](../java/lang/Class.md)<*>!`, `ptypes:` ` [MethodType](../java/lang/invoke/MethodType.md)!`)` Finds or creates a method type with the given components. |
| static [MethodType](../java/lang/invoke/MethodType.md)! | [methodType](../java/lang/invoke/MethodType.md))`(`rtype:` ` [Class](../java/lang/Class.md)<*>!`, `ptypes:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Class](../java/lang/Class.md)<*>!>!`)` Finds or creates a method type with the given components. |
| --- | --- |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Class](../java/lang/Class.md)\<\*\>!\>! | [parameterArray](../java/lang/invoke/MethodType.md))`()` Presents the parameter types as an array (a convenience method). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [parameterCount](../java/lang/invoke/MethodType.md))`()` Returns the number of parameter types in this method type. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Class](../java/lang/Class.md)\<\*\>!\>! | [parameterList](../java/lang/invoke/MethodType.md))`()` Presents the parameter types as a list (a convenience method). |
| --- | --- |
| [Class](../java/lang/Class.md)\<\*\>! | [parameterType](../java/lang/invoke/MethodType.md))`(`num:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the parameter type at the specified index, within this method type. |
| [Class](../java/lang/Class.md)\<\*\>! | [returnType](../java/lang/invoke/MethodType.md))`()` Returns the return type of this method type. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toMethodDescriptorString](../java/lang/invoke/MethodType.md))`()` Produces a bytecode descriptor representation of the method type. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../java/lang/invoke/MethodType.md))`()` Returns a string representation of the method type, of the form`"(PT0,PT1...)RT"`. |
| [MethodType](../java/lang/invoke/MethodType.md)! | [unwrap](../java/lang/invoke/MethodType.md))`()` Converts all wrapper types to their corresponding primitive types. |
| [MethodType](../java/lang/invoke/MethodType.md)! | [wrap](../java/lang/invoke/MethodType.md))`()` Converts all primitive types to their corresponding wrapper types. |
| --- | --- |

## Public methods

### appendParameterTypes

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun appendParameterTypes(vararg ptypesToInsert: Class<*>!): MethodType!
```

Finds or creates a method type with additional parameter types. Convenience method for [methodType](../java/lang/invoke/MethodType.md)).

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ptypesToInsert` | [Class](../java/lang/Class.md)\<\*\>!:zero or more new parameter types to insert after the end of the parameter list |

| Return ||
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [MethodType](../java/lang/invoke/MethodType.md)! | the same type, except with the selected parameter(s) appended |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if any element of`ptypesToInsert`is`void.class`or if the resulting method type would have more than 255 parameter slots |
| `java.lang.NullPointerException` | if`ptypesToInsert`or any of its elements is null |

### appendParameterTypes

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun appendParameterTypes(ptypesToInsert: MutableList<Class<*>!>!): MethodType!
```

Finds or creates a method type with additional parameter types. Convenience method for [methodType](../java/lang/invoke/MethodType.md)).

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ptypesToInsert` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Class](../java/lang/Class.md)\<\*\>!\>!:zero or more new parameter types to insert after the end of the parameter list |

| Return ||
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [MethodType](../java/lang/invoke/MethodType.md)! | the same type, except with the selected parameter(s) appended |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if any element of`ptypesToInsert`is`void.class`or if the resulting method type would have more than 255 parameter slots |
| `java.lang.NullPointerException` | if`ptypesToInsert`or any of its elements is null |

### changeParameterType

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun changeParameterType(
    num: Int, 
    nptype: Class<*>!
): MethodType!
```

Finds or creates a method type with a single different parameter type. Convenience method for [methodType](../java/lang/invoke/MethodType.md)).

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------|
| `index` | the index of the parameter to change |
| `paramType` | a field descriptor describing the new parameter type |
| `num` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index (zero-based) of the parameter type to change |
| --- | --- |
| `nptype` | [Class](../java/lang/Class.md)\<\*\>!:a new parameter type to replace the old one with |

| Return ||
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [MethodType](../java/lang/invoke/MethodType.md)! | the same type, except with the selected parameter changed |

| Exceptions ||
|---------------------------------------|----------------------------------------------------|
| `java.lang.NullPointerException` | if`nptype`is null |
| `java.lang.IndexOutOfBoundsException` | if`num`is not a valid index into`parameterArray()` |
| `java.lang.IllegalArgumentException` | if`nptype`is`void.class` |
| --- | --- |

### changeReturnType

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun changeReturnType(nrtype: Class<*>!): MethodType!
```

Finds or creates a method type with a different return type. Convenience method for [methodType](../java/lang/invoke/MethodType.md)).

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `newReturn` | a field descriptor for the new return type |
| `nrtype` | [Class](../java/lang/Class.md)\<\*\>!:a return parameter type to replace the old one with |

| Return ||
|--------------------------------------------------------------------------------------------|---------------------------------------------------|
| [MethodType](../java/lang/invoke/MethodType.md)! | the same type, except with the return type change |

| Exceptions ||
|----------------------------------|-------------------|
| `java.lang.NullPointerException` | if`nrtype`is null |

### descriptorString

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun descriptorString(): String
```

Returns a descriptor string for this method type.

If this method type can be [described nominally](../java/lang/invoke/MethodType.md), then the result is a method type descriptor (JVMS {@jvms 4.3.3}).

If this method type cannot be [described nominally](../java/lang/invoke/MethodType.md) and the result is a string of the form:
`"(<parameter-descriptors>)<return-descriptor>"`where`<parameter-descriptors>`is the concatenation of the [descriptor string](../java/lang/Class.md))of all of the parameter types and the [descriptor string](../java/lang/Class.md))of the return type.

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the descriptor string for this method type |

**See Also**

### dropParameterTypes

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun dropParameterTypes(
    start: Int, 
    end: Int
): MethodType!
```

Finds or creates a method type with some parameter types omitted. Convenience method for [methodType](../java/lang/invoke/MethodType.md)).

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index (zero-based) of the first parameter type to remove |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index (greater than`start`) of the first parameter type after not to remove |

| Return ||
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [MethodType](../java/lang/invoke/MethodType.md)! | the same type, except with the selected parameter(s) removed |

| Exceptions ||
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | if`start`is negative or greater than`parameterCount()`or if`end`is negative or greater than`parameterCount()`or if`start`is greater than`end` |

### equals

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Compares the specified object with this type for equality. That is, it returns true if and only if the specified object is also a method type with exactly the same parameters and return type.

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |
| `x` | object to compare |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

**See Also**

- [java.lang.Object#equals(Object)](../java/lang/Object.md)) 

### erase

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun erase(): MethodType!
```

Erases all reference types to`Object`. Convenience method for [methodType](../java/lang/invoke/MethodType.md)). All primitive types (including`void`) will remain unchanged.

| Return ||
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [MethodType](../java/lang/invoke/MethodType.md)! | a version of the original type with all reference types replaced |

### fromMethodDescriptorString

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun fromMethodDescriptorString(
    descriptor: String!, 
    loader: ClassLoader!
): MethodType!
```

Finds or creates an instance of a method type, given the spelling of its bytecode descriptor. Convenience method for [methodType](../java/lang/invoke/MethodType.md)). Any class or interface name embedded in the descriptor string will be resolved by calling [ClassLoader.loadClass(java.lang.String)](../java/lang/ClassLoader.md))on the given loader (or if it is null, on the system class loader).

Note that it is possible to encounter method types which cannot be constructed by this method, because their component types are not all reachable from a common class loader.

This method is included for the benefit of applications that must generate bytecodes that process method handles and`invokedynamic`.

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `descriptor` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a bytecode-level type descriptor string "(T...)T" |
| `loader` | [ClassLoader](../java/lang/ClassLoader.md)!:the class loader in which to look up the types |

| Return ||
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [MethodType](../java/lang/invoke/MethodType.md)! | a method type matching the bytecode-level type descriptor |

| Exceptions ||
|--------------------------------------|----------------------------------|
| `java.lang.NullPointerException` | if the string is null |
| `java.lang.IllegalArgumentException` | if the string is not well-formed |
| `java.lang.TypeNotPresentException` | if a named type cannot be found |
| --- | --- |

### generic

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun generic(): MethodType!
```

Converts all types, both reference and primitive, to`Object`. Convenience method for [genericMethodType](../java/lang/invoke/MethodType.md)). The expression`type.wrap().erase()`produces the same value as`type.generic()`.

| Return ||
|--------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [MethodType](../java/lang/invoke/MethodType.md)! | a version of the original type with all types replaced |

### genericMethodType

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun genericMethodType(objectArgCount: Int): MethodType!
```

Finds or creates a method type whose components are all`Object`. Convenience method for [methodType](../java/lang/invoke/MethodType.md)). All parameters and the return type will be Object.

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------|
| `objectArgCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):number of parameters |

| Return ||
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [MethodType](../java/lang/invoke/MethodType.md)! | a generally applicable method type, for all calls of the given argument count |

| Exceptions ||
|--------------------------------------|---------------------------------------------------|
| `java.lang.IllegalArgumentException` | if`objectArgCount`is negative or greater than 255 |

**See Also**

- [#genericMethodType(int, boolean)](../java/lang/invoke/MethodType.md)) 

### genericMethodType

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun genericMethodType(
    objectArgCount: Int, 
    finalArray: Boolean
): MethodType!
```

Finds or creates a method type whose components are`Object`with an optional trailing`Object[]`array. Convenience method for [methodType](../java/lang/invoke/MethodType.md)). All parameters and the return type will be`Object`, except the final array parameter if any, which will be`Object[]`.

| Parameters ||
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `objectArgCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):number of parameters (excluding the final array parameter if any) |
| `finalArray` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):whether there will be a trailing array parameter, of type`Object[]` |

| Return ||
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [MethodType](../java/lang/invoke/MethodType.md)! | a generally applicable method type, for all calls of the given fixed argument count and a collected array of further arguments |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if`objectArgCount`is negative or greater than 255 (or 254, if`finalArray`is true) |

**See Also**

- [#genericMethodType(int)](../java/lang/invoke/MethodType.md)) 

### hasPrimitives

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasPrimitives(): Boolean
```

Reports if this type contains a primitive argument or return value. The return type`void`counts as a primitive.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if any of the types are primitives |

### hasWrappers

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasWrappers(): Boolean
```

Reports if this type contains a wrapper argument or return value. Wrappers are types which box primitive values, such as [Integer](../java/lang/Integer.md). The reference type`java.lang.Void`counts as a wrapper, if it occurs as a return type.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if any of the types are wrappers |

### hashCode

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

Returns the hash code value for this method type. It is defined to be the same as the hashcode of a List whose elements are the return type followed by the parameter types.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the hash code value for this method type |

**See Also**

- [java.lang.Object#hashCode()](../java/lang/Object.md))
- [#equals(Object)](../java/lang/invoke/MethodType.md)) 

### insertParameterTypes

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun insertParameterTypes(
    num: Int, 
    vararg ptypesToInsert: Class<*>!
): MethodType!
```

Finds or creates a method type with additional parameter types. Convenience method for [methodType](../java/lang/invoke/MethodType.md)).

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `pos` | the index at which to insert the first inserted parameter |
| `paramTypes` | field descriptors describing the new parameter types to insert |
| `num` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the position (zero-based) of the inserted parameter type(s) |
| --- | --- |
| `ptypesToInsert` | [Class](../java/lang/Class.md)\<\*\>!:zero or more new parameter types to insert into the parameter list |

| Return ||
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [MethodType](../java/lang/invoke/MethodType.md)! | the same type, except with the selected parameter(s) inserted |

| Exceptions ||
|---------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if`ptypesToInsert`or any of its elements is null |
| `java.lang.IndexOutOfBoundsException` | if`num`is negative or greater than`parameterCount()` |
| `java.lang.IllegalArgumentException` | if any element of`ptypesToInsert`is`void.class`or if the resulting method type would have more than 255 parameter slots |
| --- | --- |

### insertParameterTypes

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun insertParameterTypes(
    num: Int, 
    ptypesToInsert: MutableList<Class<*>!>!
): MethodType!
```

Finds or creates a method type with additional parameter types. Convenience method for [methodType](../java/lang/invoke/MethodType.md)).

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `num` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the position (zero-based) of the inserted parameter type(s) |
| `ptypesToInsert` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Class](../java/lang/Class.md)\<\*\>!\>!:zero or more new parameter types to insert into the parameter list |

| Return ||
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [MethodType](../java/lang/invoke/MethodType.md)! | the same type, except with the selected parameter(s) inserted |

| Exceptions ||
|---------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | if`num`is negative or greater than`parameterCount()` |
| `java.lang.IllegalArgumentException` | if any element of`ptypesToInsert`is`void.class`or if the resulting method type would have more than 255 parameter slots |
| `java.lang.NullPointerException` | if`ptypesToInsert`or any of its elements is null |
| --- | --- |

### lastParameterType

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun lastParameterType(): Class<*>!
```

Returns the last parameter type of this method type. If this type has no parameters, the sentinel value`void.class`is returned instead.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------------|
| [Class](../java/lang/Class.md)<*>! | the last parameter type if any, else`void.class` |

### methodType

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun methodType(rtype: Class<*>!): MethodType!
```

Finds or creates a method type with the given components. Convenience method for [methodType](../java/lang/invoke/MethodType.md)). The resulting method has no parameter types.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------|
| `rtype` | [Class](../java/lang/Class.md)\<\*\>!:the return type |

| Return ||
|--------------------------------------------------------------------------------------------|-------------------------------------------|
| [MethodType](../java/lang/invoke/MethodType.md)! | a method type with the given return value |

| Exceptions ||
|----------------------------------|------------------|
| `java.lang.NullPointerException` | if`rtype`is null |

### methodType

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun methodType(
    rtype: Class<*>!, 
    ptype0: Class<*>!
): MethodType!
```

Finds or creates a method type with the given components. Convenience method for [methodType](../java/lang/invoke/MethodType.md)). The resulting method has the single given parameter type.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------|
| `rtype` | [Class](../java/lang/Class.md)\<\*\>!:the return type |
| `ptype0` | [Class](../java/lang/Class.md)\<\*\>!:the parameter type |

| Return ||
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [MethodType](../java/lang/invoke/MethodType.md)! | a method type with the given return value and parameter type |

| Exceptions ||
|--------------------------------------|----------------------------|
| `java.lang.NullPointerException` | if`rtype`or`ptype0`is null |
| `java.lang.IllegalArgumentException` | if`ptype0`is`void.class` |

### methodType

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun methodType(
    rtype: Class<*>!, 
    ptype0: Class<*>!, 
    vararg ptypes: Class<*>!
): MethodType!
```

Finds or creates a method type with the given components. Convenience method for [methodType](../java/lang/invoke/MethodType.md)). The leading parameter type is prepended to the remaining array.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------|
| `rtype` | [Class](../java/lang/Class.md)\<\*\>!:the return type |
| `ptype0` | [Class](../java/lang/Class.md)\<\*\>!:the first parameter type |
| `ptypes` | [Class](../java/lang/Class.md)\<\*\>!:the remaining parameter types |
| --- | --- |

| Return ||
|--------------------------------------------------------------------------------------------|-----------------------------------------|
| [MethodType](../java/lang/invoke/MethodType.md)! | a method type with the given components |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------|
| `java.lang.NullPointerException` | if`rtype`or`ptype0`or`ptypes`or any element of`ptypes`is null |
| `java.lang.IllegalArgumentException` | if`ptype0`or`ptypes`or any element of`ptypes`is`void.class` |

### methodType

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun methodType(
    rtype: Class<*>!, 
    ptypes: Array<Class<*>!>!
): MethodType!
```

Finds or creates an instance of the given method type.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `rtype` | [Class](../java/lang/Class.md)\<\*\>!:the return type |
| `ptypes` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Class](../java/lang/Class.md)\<\*\>!\>!:the parameter types |

| Return ||
|--------------------------------------------------------------------------------------------|-----------------------------------------|
| [MethodType](../java/lang/invoke/MethodType.md)! | a method type with the given components |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------|
| `java.lang.NullPointerException` | if`rtype`or`ptypes`or any element of`ptypes`is null |
| `java.lang.IllegalArgumentException` | if any element of`ptypes`is`void.class` |

### methodType

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun methodType(
    rtype: Class<*>!, 
    ptypes: MethodType!
): MethodType!
```

Finds or creates a method type with the given components. Convenience method for [methodType](../java/lang/invoke/MethodType.md)). The resulting method has the same parameter types as`ptypes`, and the specified return type.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `rtype` | [Class](../java/lang/Class.md)\<\*\>!:the return type |
| `ptypes` | [MethodType](../java/lang/invoke/MethodType.md)!:the method type which supplies the parameter types |

| Return ||
|--------------------------------------------------------------------------------------------|-----------------------------------------|
| [MethodType](../java/lang/invoke/MethodType.md)! | a method type with the given components |

| Exceptions ||
|----------------------------------|----------------------------|
| `java.lang.NullPointerException` | if`rtype`or`ptypes`is null |

### methodType

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun methodType(
    rtype: Class<*>!, 
    ptypes: MutableList<Class<*>!>!
): MethodType!
```

Finds or creates a method type with the given components. Convenience method for [methodType](../java/lang/invoke/MethodType.md)).

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `rtype` | [Class](../java/lang/Class.md)\<\*\>!:the return type |
| `ptypes` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Class](../java/lang/Class.md)\<\*\>!\>!:the parameter types |

| Return ||
|--------------------------------------------------------------------------------------------|-----------------------------------------|
| [MethodType](../java/lang/invoke/MethodType.md)! | a method type with the given components |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------|
| `java.lang.NullPointerException` | if`rtype`or`ptypes`or any element of`ptypes`is null |
| `java.lang.IllegalArgumentException` | if any element of`ptypes`is`void.class` |

### parameterArray

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun parameterArray(): Array<Class<*>!>!
```

Presents the parameter types as an array (a convenience method). Changes to the array will not result in changes to the type.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Class](../java/lang/Class.md)<*>!>! | the parameter types (as a fresh copy if necessary) |

### parameterCount

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun parameterCount(): Int
```

Returns the number of parameter types in this method type.

| Return ||
|----------------------------------------------------------------------------|-------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of parameter types |

### parameterList

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun parameterList(): MutableList<Class<*>!>!
```

Presents the parameter types as a list (a convenience method). The list will be immutable.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Class](../java/lang/Class.md)<*>!>! | the parameter types (as an immutable list) |

### parameterType

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun parameterType(num: Int): Class<*>!
```

Returns the parameter type at the specified index, within this method type.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------------|
| `i` | the index of the parameter |
| `num` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index (zero-based) of the desired parameter type |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------|
| [Class](../java/lang/Class.md)<*>! | the selected parameter type |

| Exceptions ||
|---------------------------------------|----------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | if`num`is not a valid index into`parameterArray()` |

### returnType

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun returnType(): Class<*>!
```

Returns the return type of this method type.

| Return ||
|-----------------------------------------------------------------------------------|-----------------|
| [Class](../java/lang/Class.md)<*>! | the return type |

### toMethodDescriptorString

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toMethodDescriptorString(): String!
```

Produces a bytecode descriptor representation of the method type.

Note that this is not a strict inverse of [fromMethodDescriptorString](../java/lang/invoke/MethodType.md)). Two distinct classes which share a common name but have different class loaders will appear identical when viewed within descriptor strings.

This method is included for the benefit of applications that must generate bytecodes that process method handles and`invokedynamic`. [fromMethodDescriptorString](../java/lang/invoke/MethodType.md)), because the latter requires a suitable class loader argument.

| Return ||
|-----------------------------------------------------------------------------------|---------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the bytecode type descriptor representation |

### toString

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Returns a string representation of the method type, of the form`"(PT0,PT1...)RT"`. The string representation of a method type is a parenthesis enclosed, comma separated list of type names, followed immediately by the return type.

Each type is represented by its [simple name](../java/lang/Class.md)).

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### unwrap

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun unwrap(): MethodType!
```

Converts all wrapper types to their corresponding primitive types. Convenience method for [methodType](../java/lang/invoke/MethodType.md)). All primitive types (including`void`) will remain unchanged. A return type of`java.lang.Void`is changed to`void`.

| Return ||
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [MethodType](../java/lang/invoke/MethodType.md)! | a version of the original type with all wrapper types replaced |

### wrap

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun wrap(): MethodType!
```

Converts all primitive types to their corresponding wrapper types. Convenience method for [methodType](../java/lang/invoke/MethodType.md)). All reference types (including wrapper types) will remain unchanged. A`void`return type is changed to the type`java.lang.Void`. The expression`type.wrap().erase()`produces the same value as`type.generic()`.

| Return ||
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [MethodType](../java/lang/invoke/MethodType.md)! | a version of the original type with all primitive types replaced |
