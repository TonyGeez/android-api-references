# MethodHandles

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MethodHandles

```
open class MethodHandles
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.lang.invoke.MethodHandles](MethodHandles.md) |

This class consists exclusively of static methods that operate on or return method handles. They fall into several categories:

- Lookup methods which help create method handles for methods and fields.
- Combinator methods, which combine or transform pre-existing method handles into new ones.
- Other factory methods to create method handles that emulate other common JVM operations or control flow patterns.

<br />

<br />

## Summary

| Nested classes ||
|---|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Lookup](../java/lang/invoke/MethodHandles.Lookup.md) A *lookup object* is a factory for creating method handles, when the creation requires access checking. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open static [MethodHandle](MethodHandle.md)! | [arrayConstructor](MethodHandles.md))`(`arrayClass:` ` [Class](../java.lang/Class.md)<*>!`)` Produces a method handle constructing arrays of a desired type, as if by the `anewarray` bytecode. |
| open static [MethodHandle](MethodHandle.md)! | [arrayElementGetter](MethodHandles.md))`(`arrayClass:` ` [Class](../java.lang/Class.md)<*>!`)` Produces a method handle giving read access to elements of an array. |
| open static [MethodHandle](MethodHandle.md)! | [arrayElementSetter](MethodHandles.md))`(`arrayClass:` ` [Class](../java.lang/Class.md)<*>!`)` Produces a method handle giving write access to elements of an array. |
| --- | --- |
| open static [VarHandle](VarHandle.md)! | [arrayElementVarHandle](MethodHandles.md))`(`arrayClass:` ` [Class](../java.lang/Class.md)<*>!`)` Produces a VarHandle giving access to elements of an array of type `arrayClass`. |
| open static [MethodHandle](MethodHandle.md)! | [arrayLength](MethodHandles.md))`(`arrayClass:` ` [Class](../java.lang/Class.md)<*>!`)` Produces a method handle returning the length of an array, as if by the `arraylength` bytecode. |
| open static [VarHandle](VarHandle.md)! | [byteArrayViewVarHandle](MethodHandles.md))`(`viewArrayClass:` ` [Class](../java.lang/Class.md)<*>!`, `byteOrder:` ` [ByteOrder](../java.nio/ByteOrder.md)!`)` Produces a VarHandle giving access to elements of a `byte[]` array viewed as if it were a different primitive array type, such as `int[]` or `long[]`. |
| --- | --- |
| open static [VarHandle](VarHandle.md)! | [byteBufferViewVarHandle](MethodHandles.md))`(`viewArrayClass:` ` [Class](../java.lang/Class.md)<*>!`, `byteOrder:` ` [ByteOrder](../java.nio/ByteOrder.md)!`)` Produces a VarHandle giving access to elements of a `ByteBuffer` viewed as if it were an array of elements of a different primitive component type to that of `byte`, such as `int[]` or `long[]`. |
| open static [MethodHandle](MethodHandle.md)! | [catchException](MethodHandles.md))`(`target:` ` [MethodHandle](MethodHandle.md)!`, `exType:` ` [Class](../java.lang/Class.md)<out` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!>!`, `handler:` ` [MethodHandle](MethodHandle.md)!`)` Makes a method handle which adapts a target method handle, by running it inside an exception handler. |
| open static [MethodHandle](MethodHandle.md)! | [collectArguments](MethodHandles.md))`(`target:` ` [MethodHandle](MethodHandle.md)!`, `pos:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `filter:` ` [MethodHandle](MethodHandle.md)!`)` Adapts a target method handle by pre-processing a sub-sequence of its arguments with a filter (another method handle). |
| --- | --- |
| open static [MethodHandle](MethodHandle.md)! | [constant](MethodHandles.md))`(`type:` ` [Class](../java.lang/Class.md)<*>!`, `value:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Produces a method handle of the requested return type which returns the given constant value every time it is invoked. |
| open static [MethodHandle](MethodHandle.md)! | [countedLoop](MethodHandles.md))`(`iterations:` ` [MethodHandle](MethodHandle.md)!`, `init:` ` [MethodHandle](MethodHandle.md)!`, `body:` ` [MethodHandle](MethodHandle.md)!`)` Constructs a loop that runs a given number of iterations. |
| open static [MethodHandle](MethodHandle.md)! | [countedLoop](MethodHandles.md))`(`start:` ` [MethodHandle](MethodHandle.md)!`, `end:` ` [MethodHandle](MethodHandle.md)!`, `init:` ` [MethodHandle](MethodHandle.md)!`, `body:` ` [MethodHandle](MethodHandle.md)!`)` Constructs a loop that counts over a range of numbers. |
| --- | --- |
| open static [MethodHandle](MethodHandle.md)! | [doWhileLoop](MethodHandles.md))`(`init:` ` [MethodHandle](MethodHandle.md)!`, `body:` ` [MethodHandle](MethodHandle.md)!`, `pred:` ` [MethodHandle](MethodHandle.md)!`)` Constructs a `do-while` loop from an initializer, a body, and a predicate. |
| open static [MethodHandle](MethodHandle.md)! | [dropArguments](MethodHandles.md))`(`target:` ` [MethodHandle](MethodHandle.md)!`, `pos:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `vararg` `valueTypes:` ` [Class](../java.lang/Class.md)<*>!`)` Produces a method handle which will discard some placeholder arguments before calling some other specified *target* method handle. |
| open static [MethodHandle](MethodHandle.md)! | [dropArguments](MethodHandles.md))`(`target:` ` [MethodHandle](MethodHandle.md)!`, `pos:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `valueTypes:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Class](../java.lang/Class.md)<*>!>!`)` Produces a method handle which will discard some placeholder arguments before calling some other specified *target* method handle. |
| --- | --- |
| open static [MethodHandle](MethodHandle.md)! | [dropArgumentsToMatch](MethodHandles.md))`(`target:` ` [MethodHandle](MethodHandle.md)!`, `skip:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newTypes:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Class](../java.lang/Class.md)<*>!>!`, `pos:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Adapts a target method handle to match the given parameter type list. |
| open static [MethodHandle](MethodHandle.md)! | [dropReturn](MethodHandles.md))`(`target:` ` [MethodHandle](MethodHandle.md)!`)` Drop the return value of the target handle (if any). |
| open static [MethodHandle](MethodHandle.md)! | [empty](MethodHandles.md))`(`type:` ` [MethodType](MethodType.md)!`)` Produces a method handle of the requested type which ignores any arguments, does nothing, and returns a suitable default depending on the return type. |
| --- | --- |
| open static [MethodHandle](MethodHandle.md)! | [exactInvoker](MethodHandles.md))`(`type:` ` [MethodType](MethodType.md)!`)` Produces a special *invoker method handle* which can be used to invoke any method handle of the given type, as if by [invokeExact](MethodHandle.md)). |
| open static [MethodHandle](MethodHandle.md)! | [explicitCastArguments](MethodHandles.md))`(`target:` ` [MethodHandle](MethodHandle.md)!`, `newType:` ` [MethodType](MethodType.md)!`)` Produces a method handle which adapts the type of the given method handle to a new type by pairwise argument and return type conversion. |
| open static [MethodHandle](MethodHandle.md)! | [filterArguments](MethodHandles.md))`(`target:` ` [MethodHandle](MethodHandle.md)!`, `pos:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `vararg` `filters:` ` [MethodHandle](MethodHandle.md)!`)` Adapts a target method handle by pre-processing one or more of its arguments, each with its own unary filter function, and then calling the target with each pre-processed argument replaced by the result of its corresponding filter function. |
| --- | --- |
| open static [MethodHandle](MethodHandle.md)! | [filterReturnValue](MethodHandles.md))`(`target:` ` [MethodHandle](MethodHandle.md)!`, `filter:` ` [MethodHandle](MethodHandle.md)!`)` Adapts a target method handle by post-processing its return value (if any) with a filter (another method handle). |
| open static [MethodHandle](MethodHandle.md)! | [foldArguments](MethodHandles.md))`(`target:` ` [MethodHandle](MethodHandle.md)!`, `pos:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `combiner:` ` [MethodHandle](MethodHandle.md)!`)` Adapts a target method handle by pre-processing some of its arguments, starting at a given position, and then calling the target with the result of the pre-processing, inserted into the original sequence of arguments just before the folded arguments. |
| open static [MethodHandle](MethodHandle.md)! | [foldArguments](MethodHandles.md))`(`target:` ` [MethodHandle](MethodHandle.md)!`, `combiner:` ` [MethodHandle](MethodHandle.md)!`)` Adapts a target method handle by pre-processing some of its arguments, and then calling the target with the result of the pre-processing, inserted into the original sequence of arguments. |
| --- | --- |
| open static [MethodHandle](MethodHandle.md)! | [guardWithTest](MethodHandles.md))`(`test:` ` [MethodHandle](MethodHandle.md)!`, `target:` ` [MethodHandle](MethodHandle.md)!`, `fallback:` ` [MethodHandle](MethodHandle.md)!`)` Makes a method handle which adapts a target method handle, by guarding it with a test, a boolean-valued method handle. |
| open static [MethodHandle](MethodHandle.md)! | [identity](MethodHandles.md))`(`type:` ` [Class](../java.lang/Class.md)<*>!`)` Produces a method handle which returns its sole argument when invoked. |
| open static [MethodHandle](MethodHandle.md)! | [insertArguments](MethodHandles.md))`(`target:` ` [MethodHandle](MethodHandle.md)!`, `pos:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `vararg` `values:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Provides a target method handle with one or more *bound arguments* in advance of the method handle's invocation. |
| --- | --- |
| open static [MethodHandle](MethodHandle.md)! | [invoker](MethodHandles.md))`(`type:` ` [MethodType](MethodType.md)!`)` Produces a special *invoker method handle* which can be used to invoke any method handle compatible with the given type, as if by [invoke](MethodHandle.md)). |
| open static [MethodHandle](MethodHandle.md)! | [iteratedLoop](MethodHandles.md))`(`iterator:` ` [MethodHandle](MethodHandle.md)!`, `init:` ` [MethodHandle](MethodHandle.md)!`, `body:` ` [MethodHandle](MethodHandle.md)!`)` Constructs a loop that ranges over the values produced by an `Iterator<T>`. |
| open static [MethodHandles.Lookup](../java/lang/invoke/MethodHandles.Lookup.md)! | [lookup](MethodHandles.md))`()` Returns a [lookup object](../java/lang/invoke/MethodHandles.Lookup.md) with full capabilities to emulate all supported bytecode behaviors of the caller. |
| --- | --- |
| open static [MethodHandle](MethodHandle.md)! | [loop](MethodHandles.md))`(`vararg` `clauses:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [MethodHandle](MethodHandle.md)!>!`)` Constructs a method handle representing a loop with several loop variables that are updated and checked upon each iteration. |
| open static [MethodHandle](MethodHandle.md)! | [permuteArguments](MethodHandles.md))`(`target:` ` [MethodHandle](MethodHandle.md)!`, `newType:` ` [MethodType](MethodType.md)!`, `vararg` `reorder:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Produces a method handle which adapts the calling sequence of the given method handle to a new type, by reordering the arguments. |
| open static [MethodHandles.Lookup](../java/lang/invoke/MethodHandles.Lookup.md)! | [privateLookupIn](MethodHandles.md))`(`targetClass:` ` [Class](../java.lang/Class.md)<*>!`, `lookup:` ` [MethodHandles.Lookup](../java/lang/invoke/MethodHandles.Lookup.md)!`)` Returns a [lookup object](../java/lang/invoke/MethodHandles.Lookup.md) with full capabilities to emulate all supported bytecode behaviors, including [private access](../java/lang/invoke/MethodHandles.Lookup.md), on a target class. |
| --- | --- |
| open static [MethodHandles.Lookup](../java/lang/invoke/MethodHandles.Lookup.md)! | [publicLookup](MethodHandles.md))`()` Returns a [lookup object](../java/lang/invoke/MethodHandles.Lookup.md) which is trusted minimally. |
| open static T | [reflectAs](MethodHandles.md))`(`expected:` ` [Class](../java.lang/Class.md)<T>!`, `target:` ` [MethodHandle](MethodHandle.md)!`)` Performs an unchecked "crack" of a [direct method handle](MethodHandleInfo.md). |
| open static [MethodHandle](MethodHandle.md)! | [spreadInvoker](MethodHandles.md))`(`type:` ` [MethodType](MethodType.md)!`, `leadingArgCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Produces a method handle which will invoke any method handle of the given `type`, with a given number of trailing arguments replaced by a single trailing `Object[]` array. |
| --- | --- |
| open static [MethodHandle](MethodHandle.md)! | [tableSwitch](MethodHandles.md))`(`fallback:` ` [MethodHandle](MethodHandle.md)!`, `vararg` `targets:` ` [MethodHandle](MethodHandle.md)!`)` Creates a table switch method handle, which can be used to switch over a set of target method handles, based on a given target index, called selector. |
| open static [MethodHandle](MethodHandle.md)! | [throwException](MethodHandles.md))`(`returnType:` ` [Class](../java.lang/Class.md)<*>!`, `exType:` ` [Class](../java.lang/Class.md)<out` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!>!`)` Produces a method handle which will throw exceptions of the given `exType`. |
| open static [MethodHandle](MethodHandle.md)! | [tryFinally](MethodHandles.md))`(`target:` ` [MethodHandle](MethodHandle.md)!`, `cleanup:` ` [MethodHandle](MethodHandle.md)!`)` Makes a method handle that adapts a `target` method handle by wrapping it in a `try-finally` block. |
| --- | --- |
| open static [MethodHandle](MethodHandle.md)! | [varHandleExactInvoker](MethodHandles.md))`(`accessMode:` ` [VarHandle.AccessMode](../java/lang/invoke/VarHandle.AccessMode.md)!`, `type:` ` [MethodType](MethodType.md)!`)` Produces a special *invoker method handle* which can be used to invoke a signature-polymorphic access mode method on any VarHandle whose associated access mode type is compatible with the given type. |
| open static [MethodHandle](MethodHandle.md)! | [varHandleInvoker](MethodHandles.md))`(`accessMode:` ` [VarHandle.AccessMode](../java/lang/invoke/VarHandle.AccessMode.md)!`, `type:` ` [MethodType](MethodType.md)!`)` Produces a special *invoker method handle* which can be used to invoke a signature-polymorphic access mode method on any VarHandle whose associated access mode type is compatible with the given type. |
| open static [MethodHandle](MethodHandle.md)! | [whileLoop](MethodHandles.md))`(`init:` ` [MethodHandle](MethodHandle.md)!`, `pred:` ` [MethodHandle](MethodHandle.md)!`, `body:` ` [MethodHandle](MethodHandle.md)!`)` Constructs a `while` loop from an initializer, a body, and a predicate. |
| --- | --- |
| open static [MethodHandle](MethodHandle.md)! | [zero](MethodHandles.md))`(`type:` ` [Class](../java.lang/Class.md)<*>!`)` Produces a constant method handle of the requested return type which returns the default value for that type every time it is invoked. |

## Public methods

### arrayConstructor

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun arrayConstructor(arrayClass: Class<*>!): MethodHandle!
```

Produces a method handle constructing arrays of a desired type, as if by the `anewarray` bytecode. The return type of the method handle will be the array type. The type of its sole argument will be `int`, which specifies the size of the array.

If the returned method handle is invoked with a negative array size, a `NegativeArraySizeException` will be thrown.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------|
| `arrayClass` | [Class](../java.lang/Class.md)\<\*\>!: an array type |

| Return ||
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [MethodHandle](MethodHandle.md)! | a method handle which can create arrays of the given type |

| Exceptions ||
|--------------------------------------|--------------------------------------|
| `java.lang.NullPointerException` | if the argument is `null` |
| `java.lang.IllegalArgumentException` | if `arrayClass` is not an array type |

**See Also**

- [java.lang.reflect.Array#newInstance(Class, int)](../java.lang.reflect/Array.md)) 

### arrayElementGetter

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun arrayElementGetter(arrayClass: Class<*>!): MethodHandle!
```

Produces a method handle giving read access to elements of an array. The type of the method handle will have a return type of the array's element type. Its first argument will be the array type, and the second will be `int`.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------|
| `arrayClass` | [Class](../java.lang/Class.md)\<\*\>!: an array type |

| Return ||
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [MethodHandle](MethodHandle.md)! | a method handle which can load values from the given array type |

| Exceptions ||
|--------------------------------------|------------------------------------|
| `java.lang.NullPointerException` | if the argument is null |
| `java.lang.IllegalArgumentException` | if arrayClass is not an array type |

### arrayElementSetter

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun arrayElementSetter(arrayClass: Class<*>!): MethodHandle!
```

Produces a method handle giving write access to elements of an array. The type of the method handle will have a void return type. Its last argument will be the array's element type. The first and second arguments will be the array type and int.

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------|
| `arrayClass` | [Class](../java.lang/Class.md)\<\*\>!: the class of an array |

| Return ||
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------|
| [MethodHandle](MethodHandle.md)! | a method handle which can store values into the array type |

| Exceptions ||
|--------------------------------------|------------------------------------|
| `java.lang.NullPointerException` | if the argument is null |
| `java.lang.IllegalArgumentException` | if arrayClass is not an array type |

### arrayElementVarHandle

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun arrayElementVarHandle(arrayClass: Class<*>!): VarHandle!
```

Produces a VarHandle giving access to elements of an array of type `arrayClass`. The VarHandle's variable type is the component type of `arrayClass` and the list of coordinate types is `(arrayClass, int)`, where the `int` coordinate type corresponds to an argument that is an index into an array.

Certain access modes of the returned VarHandle are unsupported under the following conditions:

- if the component type is anything other than `byte`, `short`, `char`, `int`, `long`, `float`, or `double` then numeric atomic update access modes are unsupported.
- if the field type is anything other than `boolean`, `byte`, `short`, `char`, `int` or `long` then bitwise atomic update access modes are unsupported.

If the component type is `float` or `double` then numeric and atomic update access modes compare values using their bitwise representation (see [Float.floatToRawIntBits](../java.lang/Float.md)) and [Double.doubleToRawLongBits](../java.lang/Double.md)), respectively).

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------|
| `arrayClass` | [Class](../java.lang/Class.md)\<\*\>!: the class of an array, of type `T[]` |

| Return ||
|-----------------------------------------------------------------------------------------|---------------------------------------------------|
| [VarHandle](VarHandle.md)! | a VarHandle giving access to elements of an array |

| Exceptions ||
|--------------------------------------|------------------------------------|
| `java.lang.NullPointerException` | if the arrayClass is null |
| `java.lang.IllegalArgumentException` | if arrayClass is not an array type |

### arrayLength

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun arrayLength(arrayClass: Class<*>!): MethodHandle!
```

Produces a method handle returning the length of an array, as if by the `arraylength` bytecode. The type of the method handle will have `int` as return type, and its sole argument will be the array type.

If the returned method handle is invoked with a `null` array reference, a `NullPointerException` will be thrown.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------|
| `arrayClass` | [Class](../java.lang/Class.md)\<\*\>!: an array type |

| Return ||
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [MethodHandle](MethodHandle.md)! | a method handle which can retrieve the length of an array of the given array type |

| Exceptions ||
|--------------------------------------|------------------------------------|
| `java.lang.NullPointerException` | if the argument is `null` |
| `java.lang.IllegalArgumentException` | if arrayClass is not an array type |

### byteArrayViewVarHandle

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun byteArrayViewVarHandle(
    viewArrayClass: Class<*>!, 
    byteOrder: ByteOrder!
): VarHandle!
```

Produces a VarHandle giving access to elements of a `byte[]` array viewed as if it were a different primitive array type, such as `int[]` or `long[]`. The VarHandle's variable type is the component type of `viewArrayClass` and the list of coordinate types is `(byte[], int)`, where the `int` coordinate type corresponds to an argument that is an index into a `byte[]` array. The returned VarHandle accesses bytes at an index in a `byte[]` array, composing bytes to or from a value of the component type of `viewArrayClass` according to the given endianness.

The supported component types (variables types) are `short`, `char`, `int`, `long`, `float` and `double`.

Access of bytes at a given index will result in an `IndexOutOfBoundsException` if the index is less than `0` or greater than the `byte[]` array length minus the size (in bytes) of `T`.

Access of bytes at an index may be aligned or misaligned for `T`, with respect to the underlying memory address, `A` say, associated with the array and index. If access is misaligned then access for anything other than the `get` and `set` access modes will result in an `IllegalStateException`. In such cases atomic access is only guaranteed with respect to the largest power of two that divides the GCD of `A` and the size (in bytes) of `T`. If access is aligned then following access modes are supported and are guaranteed to support atomic access:

- read write access modes for all `T`, with the exception of access modes `get` and `set` for `long` and `double` on 32-bit platforms.
- atomic update access modes for `int`, `long`, `float` or `double`. (Future major platform releases of the JDK may support additional types for certain currently unsupported access modes.)
- numeric atomic update access modes for `int` and `long`. (Future major platform releases of the JDK may support additional numeric types for certain currently unsupported access modes.)
- bitwise atomic update access modes for `int` and `long`. (Future major platform releases of the JDK may support additional numeric types for certain currently unsupported access modes.)

Misaligned access, and therefore atomicity guarantees, may be determined for `byte[]` arrays without operating on a specific array. Given an `index`, `T` and it's corresponding boxed type, `T_BOX`, misalignment may be determined as follows: 

```kotlin
<code>int sizeOfT = T_BOX.BYTES;  // size in bytes of T
  int misalignedAtZeroIndex = ByteBuffer.wrap(new byte[0]).
      alignmentOffset(0, sizeOfT);
  int misalignedAtIndex = (misalignedAtZeroIndex + index) % sizeOfT;
  boolean isMisaligned = misalignedAtIndex != 0;
  </code>
```

If the variable type is `float` or `double` then atomic update access modes compare values using their bitwise representation (see [Float.floatToRawIntBits](../java.lang/Float.md)) and [Double.doubleToRawLongBits](../java.lang/Double.md)), respectively).

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `viewArrayClass` | [Class](../java.lang/Class.md)\<\*\>!: the view array class, with a component type of type `T` |
| `byteOrder` | [ByteOrder](../java.nio/ByteOrder.md)!: the endianness of the view array elements, as stored in the underlying `byte` array |

| Return ||
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [VarHandle](VarHandle.md)! | a VarHandle giving access to elements of a `byte[]` array viewed as if elements corresponding to the components type of the view array class |

| Exceptions ||
|-------------------------------------------|-----------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if viewArrayClass or byteOrder is null |
| `java.lang.IllegalArgumentException` | if viewArrayClass is not an array type |
| `java.lang.UnsupportedOperationException` | if the component type of viewArrayClass is not supported as a variable type |
| --- | --- |

### byteBufferViewVarHandle

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun byteBufferViewVarHandle(
    viewArrayClass: Class<*>!, 
    byteOrder: ByteOrder!
): VarHandle!
```

Produces a VarHandle giving access to elements of a `ByteBuffer` viewed as if it were an array of elements of a different primitive component type to that of `byte`, such as `int[]` or `long[]`. The VarHandle's variable type is the component type of `viewArrayClass` and the list of coordinate types is `(ByteBuffer, int)`, where the `int` coordinate type corresponds to an argument that is an index into a `byte[]` array. The returned VarHandle accesses bytes at an index in a `ByteBuffer`, composing bytes to or from a value of the component type of `viewArrayClass` according to the given endianness.

The supported component types (variables types) are `short`, `char`, `int`, `long`, `float` and `double`.

Access will result in a `ReadOnlyBufferException` for anything other than the read access modes if the `ByteBuffer` is read-only.

Access of bytes at a given index will result in an `IndexOutOfBoundsException` if the index is less than `0` or greater than the `ByteBuffer` limit minus the size (in bytes) of `T`.

Access of bytes at an index may be aligned or misaligned for `T`, with respect to the underlying memory address, `A` say, associated with the `ByteBuffer` and index. If access is misaligned then access for anything other than the `get` and `set` access modes will result in an `IllegalStateException`. In such cases atomic access is only guaranteed with respect to the largest power of two that divides the GCD of `A` and the size (in bytes) of `T`. If access is aligned then following access modes are supported and are guaranteed to support atomic access:

- read write access modes for all `T`, with the exception of access modes `get` and `set` for `long` and `double` on 32-bit platforms.
- atomic update access modes for `int`, `long`, `float` or `double`. (Future major platform releases of the JDK may support additional types for certain currently unsupported access modes.)
- numeric atomic update access modes for `int` and `long`. (Future major platform releases of the JDK may support additional numeric types for certain currently unsupported access modes.)
- bitwise atomic update access modes for `int` and `long`. (Future major platform releases of the JDK may support additional numeric types for certain currently unsupported access modes.)

Misaligned access, and therefore atomicity guarantees, may be determined for a `ByteBuffer`, `bb` (direct or otherwise), an `index`, `T` and it's corresponding boxed type, `T_BOX`, as follows: 

```kotlin
<code>int sizeOfT = T_BOX.BYTES;  // size in bytes of T
  ByteBuffer bb = ...
  int misalignedAtIndex = bb.alignmentOffset(index, sizeOfT);
  boolean isMisaligned = misalignedAtIndex != 0;
  </code>
```

If the variable type is `float` or `double` then atomic update access modes compare values using their bitwise representation (see [Float.floatToRawIntBits](../java.lang/Float.md)) and [Double.doubleToRawLongBits](../java.lang/Double.md)), respectively).

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `viewArrayClass` | [Class](../java.lang/Class.md)\<\*\>!: the view array class, with a component type of type `T` |
| `byteOrder` | [ByteOrder](../java.nio/ByteOrder.md)!: the endianness of the view array elements, as stored in the underlying `ByteBuffer` (Note this overrides the endianness of a `ByteBuffer`) |

| Return ||
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [VarHandle](VarHandle.md)! | a VarHandle giving access to elements of a `ByteBuffer` viewed as if elements corresponding to the components type of the view array class |

| Exceptions ||
|-------------------------------------------|-----------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if viewArrayClass or byteOrder is null |
| `java.lang.IllegalArgumentException` | if viewArrayClass is not an array type |
| `java.lang.UnsupportedOperationException` | if the component type of viewArrayClass is not supported as a variable type |
| --- | --- |

### catchException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun catchException(
    target: MethodHandle!, 
    exType: Class<out Throwable!>!, 
    handler: MethodHandle!
): MethodHandle!
```

Makes a method handle which adapts a target method handle, by running it inside an exception handler. If the target returns normally, the adapter returns that value. If an exception matching the specified type is thrown, the fallback handle is called instead on the exception, plus the original arguments.

The target and handler must have the same corresponding argument and return types, except that handler may omit trailing arguments (similarly to the predicate in [guardWithTest](MethodHandles.md))). Also, the handler must have an extra leading parameter of `exType` or a supertype.

Here is pseudocode for the resulting adapter. In the code, `T` represents the return type of the `target` and `handler`, and correspondingly that of the resulting adapter; `A`/`a`, the types and values of arguments to the resulting handle consumed by `handler`; and `B`/`b`, those of arguments to the resulting handle discarded by `handler`. 

```kotlin
<code>T target(A..., B...);
  T handler(ExType, A...);
  T adapter(A... a, B... b) {
    try {
      return target(a..., b...);
    } catch (ExType ex) {
      return handler(ex, a...);
    }
  }
  </code>
```
Note that the saved arguments (`a...` in the pseudocode) cannot be modified by execution of the target, and so are passed unchanged from the caller to the handler, if the handler is invoked.

The target and handler must return the same type, even if the handler always throws. (This might happen, for instance, because the handler is simulating a `finally` clause). To create such a throwing handler, compose the handler creation logic with [throwException](MethodHandles.md)), in order to create a method handle of the correct return type.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `target` | [MethodHandle](MethodHandle.md)!: method handle to call |
| `exType` | [Class](../java.lang/Class.md)\<out [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!\>!: the type of exception which the handler will catch |
| `handler` | [MethodHandle](MethodHandle.md)!: method handle to call if a matching exception is thrown |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [MethodHandle](MethodHandle.md)! | method handle which incorporates the specified try/catch logic |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if any argument is null |
| `java.lang.IllegalArgumentException` | if `handler` does not accept the given exception type, or if the method handle types do not match in their return types and their corresponding parameters |

**See Also**

- [java.lang.invoke.MethodHandles#tryFinally(MethodHandle, MethodHandle)](MethodHandles.md)) 

### collectArguments

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun collectArguments(
    target: MethodHandle!, 
    pos: Int, 
    filter: MethodHandle!
): MethodHandle!
```

Adapts a target method handle by pre-processing a sub-sequence of its arguments with a filter (another method handle). The pre-processed arguments are replaced by the result (if any) of the filter function. The target is then called on the modified (usually shortened) argument list.

If the filter returns a value, the target must accept that value as its argument in position `pos`, preceded and/or followed by any arguments not passed to the filter. If the filter returns void, the target must accept all arguments not passed to the filter. No arguments are reordered, and a result returned from the filter replaces (in order) the whole subsequence of arguments originally passed to the adapter.

The argument types (if any) of the filter replace zero or one argument types of the target, at position `pos`, in the resulting adapted method handle. The return type of the filter (if any) must be identical to the argument type of the target at position `pos`, and that target argument is supplied by the return value of the filter.

In all cases, `pos` must be greater than or equal to zero, and `pos` must also be less than or equal to the target's arity.

**Example:** 

```kotlin
<code>import static java.lang.invoke.MethodHandles.*;
 import static java.lang.invoke.MethodType.*;
 ...
 MethodHandle deepToString = publicLookup()
 .findStatic(Arrays.class, "deepToString", methodType(String.class, Object[].class));
 
 MethodHandle ts1 = deepToString.asCollector(String[].class, 1);
 assertEquals("[strange]", (String) ts1.invokeExact("strange"));
 
 MethodHandle ts2 = deepToString.asCollector(String[].class, 2);
 assertEquals("[up, down]", (String) ts2.invokeExact("up", "down"));
 
 MethodHandle ts3 = deepToString.asCollector(String[].class, 3);
 MethodHandle ts3_ts2 = collectArguments(ts3, 1, ts2);
 assertEquals("[top, [up, down], strange]",
            (String) ts3_ts2.invokeExact("top", "up", "down", "strange"));
 
 MethodHandle ts3_ts2_ts1 = collectArguments(ts3_ts2, 3, ts1);
 assertEquals("[top, [up, down], [strange]]",
            (String) ts3_ts2_ts1.invokeExact("top", "up", "down", "strange"));
 
 MethodHandle ts3_ts2_ts3 = collectArguments(ts3_ts2, 1, ts3);
 assertEquals("[top, [[up, down, strange], charm], bottom]",
            (String) ts3_ts2_ts3.invokeExact("top", "up", "down", "strange", "charm", "bottom"));
     </code>
```

Here is pseudocode for the resulting adapter: 

```kotlin
<code>T target(A...,V,C...);
     V filter(B...);
     T adapter(A... a,B... b,C... c) {
       V v = filter(b...);
       return target(a...,v,c...);
     }
     // and if the filter has no arguments:
     T target2(A...,V,C...);
     V filter2();
     T adapter2(A... a,C... c) {
       V v = filter2();
       return target2(a...,v,c...);
     }
     // and if the filter has a void return:
     T target3(A...,C...);
     void filter3(B...);
     void adapter3(A... a,B... b,C... c) {
       filter3(b...);
       return target3(a...,c...);
     }
     </code>
```

A collection adapter `collectArguments(mh, 0, coll)` is equivalent to one which first "folds" the affected arguments, and then drops them, in separate steps as follows: 

```kotlin
<code>mh = MethodHandles.dropArguments(mh, 1, coll.type().parameterList()); //step 2
     mh = MethodHandles.foldArguments(mh, coll); //step 1
     </code>
```
If the target method handle consumes no arguments besides than the result (if any) of the filter `coll`, then `collectArguments(mh, 0, coll)` is equivalent to `filterReturnValue(coll, mh)`. If the filter method handle `coll` consumes one argument and produces a non-void result, then `collectArguments(mh, N, coll)` is equivalent to `filterArguments(mh, N, coll)`. Other equivalences are possible but would require argument permutation.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `target` | [MethodHandle](MethodHandle.md)!: the method handle to invoke after filtering the subsequence of arguments |
| `pos` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the position of the first adapter argument to pass to the filter, and/or the target argument which receives the result of the filter |
| `filter` | [MethodHandle](MethodHandle.md)!: method handle to call on the subsequence of arguments |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [MethodHandle](MethodHandle.md)! | method handle which incorporates the specified argument subsequence filtering logic |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if either argument is null |
| `java.lang.IllegalArgumentException` | if the return type of `filter` is non-void and is not the same as the `pos` argument of the target, or if `pos` is not between 0 and the target's arity, inclusive, or if the resulting method handle's type would have [too many parameters](MethodHandle.md) |

**See Also**

- [java.lang.invoke.MethodHandles#filterArguments](MethodHandles.md))
- [java.lang.invoke.MethodHandles#filterReturnValue](MethodHandles.md)) 

### constant

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun constant(
    type: Class<*>!, 
    value: Any!
): MethodHandle!
```

Produces a method handle of the requested return type which returns the given constant value every time it is invoked.

Before the method handle is returned, the passed-in value is converted to the requested type. If the requested type is primitive, widening primitive conversions are attempted, else reference conversions are attempted.

The returned method handle is equivalent to `identity(type).bindTo(value)`.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------|
| `type` | [Class](../java.lang/Class.md)\<\*\>!: the return type of the desired method handle |
| `value` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: the value to return |

| Return ||
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [MethodHandle](MethodHandle.md)! | a method handle of the given return type and no arguments, which always returns the given value |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------|
| `java.lang.NullPointerException` | if the `type` argument is null |
| `java.lang.ClassCastException` | if the value cannot be converted to the required return type |
| `java.lang.IllegalArgumentException` | if the given type is `void.class` |
| --- | --- |

### countedLoop

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun countedLoop(
    iterations: MethodHandle!, 
    init: MethodHandle!, 
    body: MethodHandle!
): MethodHandle!
```

Constructs a loop that runs a given number of iterations. This is a convenience wrapper for the [generic loop combinator](MethodHandles.md)).

The number of iterations is determined by the `iterations` handle evaluation result. The loop counter `i` is an extra loop iteration variable of type `int`. It will be initialized to 0 and incremented by 1 in each iteration.

If the `body` handle returns a non-`void` type `V`, a leading loop iteration variable of that type is also present. This variable is initialized using the optional `init` handle, or to the [default value](MethodHandles.md)) of type `V` if that handle is `null`.

In each iteration, the iteration variables are passed to an invocation of the `body` handle. A non-`void` value returned from the body (of type `V`) updates the leading iteration variable. The result of the loop handle execution will be the final `V` value of that variable (or `void` if there is no `V` variable).

The following rules hold for the argument handles:

- The `iterations` handle must not be `null`, and must return the type `int`, referred to here as `I` in parameter type lists.
- The `body` handle must not be `null`; its type must be of the form `(V I A...)V`, where `V` is non-`void`, or else `(I A...)void`. (In the `void` case, we assign the type `void` to the name `V`, and we will write `(V I A...)V` with the understanding that a `void` type `V` is quietly dropped from the parameter list, leaving `(I A...)V`.)
- The parameter list `(V I A...)` of the body contributes to a list of types called the *internal parameter list*. It will constrain the parameter lists of the other loop parts.
- As a special case, if the body contributes only `V` and `I` types, with no additional `A` types, then the internal parameter list is extended by the argument types `A...` of the `iterations` handle.
- If the iteration variable types `(V I)` are dropped from the internal parameter list, the resulting shorter list `(A...)` is called the *external parameter list*.
- The body return type `V`, if non-`void`, determines the type of an additional state variable of the loop. The body must both accept a leading parameter and return a value of this type `V`.
- If `init` is non-`null`, it must have return type `V`. Its parameter list (of some [form `(A*)`](MethodHandles.md)) must be [effectively identical](MethodHandles.md) to the external parameter list `(A...)`.
- If `init` is `null`, the loop variable will be initialized to its [default value](MethodHandles.md)).
- The parameter list of `iterations` (of some form `(A*)`) must be effectively identical to the external parameter list `(A...)`.

The resulting loop handle's result type and parameter signature are determined as follows:

- The loop handle's result type is the result type `V` of the body.
- The loop handle's parameter types are the types `(A...)`, from the external parameter list.

Here is pseudocode for the resulting loop handle. In the code, `V`/`v` represent the type / value of the second loop variable as well as the result type of the loop; and `A...`/`a...` represent arguments passed to the loop. 

```kotlin
<code>int iterations(A...);
  V init(A...);
  V body(V, int, A...);
  V countedLoop(A... a...) {
    int end = iterations(a...);
    V v = init(a...);
    for (int i = 0; i &lt; end; ++i) {
      v = body(v, i, a...);
    }
    return v;
  }
  </code>
```

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `iterations` | [MethodHandle](MethodHandle.md)!: a non-`null` handle to return the number of iterations this loop should run. The handle's result type must be `int`. See above for other constraints. |
| `init` | [MethodHandle](MethodHandle.md)!: optional initializer, providing the initial value of the loop variable. May be `null`, implying a default initial value. See above for other constraints. |
| `body` | [MethodHandle](MethodHandle.md)!: body of the loop, which may not be `null`. It controls the loop parameters and result type in the standard case (see above for details). It must accept its own return type (if non-void) plus an `int` parameter (for the counter), and may accept any number of additional types. See above for other constraints. |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------------------|----------------------------------------|
| [MethodHandle](MethodHandle.md)! | a method handle representing the loop. |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------|
| `java.lang.NullPointerException` | if either of the `iterations` or `body` handles is `null`. |
| `java.lang.IllegalArgumentException` | if any argument violates the rules formulated above. |

**See Also**

- [#countedLoop(MethodHandle, MethodHandle, MethodHandle, MethodHandle)](MethodHandles.md)) 

### countedLoop

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun countedLoop(
    start: MethodHandle!, 
    end: MethodHandle!, 
    init: MethodHandle!, 
    body: MethodHandle!
): MethodHandle!
```

Constructs a loop that counts over a range of numbers. This is a convenience wrapper for the [generic loop combinator](MethodHandles.md)).

The loop counter `i` is a loop iteration variable of type `int`. The `start` and `end` handles determine the start (inclusive) and end (exclusive) values of the loop counter. The loop counter will be initialized to the `int` value returned from the evaluation of the `start` handle and run to the value returned from `end` (exclusively) with a step width of 1.

If the `body` handle returns a non-`void` type `V`, a leading loop iteration variable of that type is also present. This variable is initialized using the optional `init` handle, or to the [default value](MethodHandles.md)) of type `V` if that handle is `null`.

In each iteration, the iteration variables are passed to an invocation of the `body` handle. A non-`void` value returned from the body (of type `V`) updates the leading iteration variable. The result of the loop handle execution will be the final `V` value of that variable (or `void` if there is no `V` variable).

The following rules hold for the argument handles:

- The `start` and `end` handles must not be `null`, and must both return the common type `int`, referred to here as `I` in parameter type lists.
- The `body` handle must not be `null`; its type must be of the form `(V I A...)V`, where `V` is non-`void`, or else `(I A...)void`. (In the `void` case, we assign the type `void` to the name `V`, and we will write `(V I A...)V` with the understanding that a `void` type `V` is quietly dropped from the parameter list, leaving `(I A...)V`.)
- The parameter list `(V I A...)` of the body contributes to a list of types called the *internal parameter list*. It will constrain the parameter lists of the other loop parts.
- As a special case, if the body contributes only `V` and `I` types, with no additional `A` types, then the internal parameter list is extended by the argument types `A...` of the `end` handle.
- If the iteration variable types `(V I)` are dropped from the internal parameter list, the resulting shorter list `(A...)` is called the *external parameter list*.
- The body return type `V`, if non-`void`, determines the type of an additional state variable of the loop. The body must both accept a leading parameter and return a value of this type `V`.
- If `init` is non-`null`, it must have return type `V`. Its parameter list (of some [form `(A*)`](MethodHandles.md)) must be [effectively identical](MethodHandles.md) to the external parameter list `(A...)`.
- If `init` is `null`, the loop variable will be initialized to its [default value](MethodHandles.md)).
- The parameter list of `start` (of some form `(A*)`) must be effectively identical to the external parameter list `(A...)`.
- Likewise, the parameter list of `end` must be effectively identical to the external parameter list.

The resulting loop handle's result type and parameter signature are determined as follows:

- The loop handle's result type is the result type `V` of the body.
- The loop handle's parameter types are the types `(A...)`, from the external parameter list.

Here is pseudocode for the resulting loop handle. In the code, `V`/`v` represent the type / value of the second loop variable as well as the result type of the loop; and `A...`/`a...` represent arguments passed to the loop. 

```kotlin
<code>int start(A...);
  int end(A...);
  V init(A...);
  V body(V, int, A...);
  V countedLoop(A... a...) {
    int e = end(a...);
    int s = start(a...);
    V v = init(a...);
    for (int i = s; i &lt; e; ++i) {
      v = body(v, i, a...);
    }
    return v;
  }
  </code>
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `start` | [MethodHandle](MethodHandle.md)!: a non-`null` handle to return the start value of the loop counter, which must be `int`. See above for other constraints. |
| `end` | [MethodHandle](MethodHandle.md)!: a non-`null` handle to return the end value of the loop counter (the loop will run to `end-1`). The result type must be `int`. See above for other constraints. |
| `init` | [MethodHandle](MethodHandle.md)!: optional initializer, providing the initial value of the loop variable. May be `null`, implying a default initial value. See above for other constraints. |
| --- | --- |
| `body` | [MethodHandle](MethodHandle.md)!: body of the loop, which may not be `null`. It controls the loop parameters and result type in the standard case (see above for details). It must accept its own return type (if non-void) plus an `int` parameter (for the counter), and may accept any number of additional types. See above for other constraints. |

| Return ||
|-----------------------------------------------------------------------------------------------|----------------------------------------|
| [MethodHandle](MethodHandle.md)! | a method handle representing the loop. |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------|
| `java.lang.NullPointerException` | if any of the `start`, `end`, or `body` handles is `null`. |
| `java.lang.IllegalArgumentException` | if any argument violates the rules formulated above. |

**See Also**

- [#countedLoop(MethodHandle, MethodHandle, MethodHandle)](MethodHandles.md)) 

### doWhileLoop

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun doWhileLoop(
    init: MethodHandle!, 
    body: MethodHandle!, 
    pred: MethodHandle!
): MethodHandle!
```

Constructs a `do-while` loop from an initializer, a body, and a predicate. This is a convenience wrapper for the [generic loop combinator](MethodHandles.md)).

The `pred` handle describes the loop condition; and `body`, its body. The loop resulting from this method will, in each iteration, first execute its body and then evaluate the predicate. The loop will terminate once the predicate evaluates to `false` after an execution of the body.

The `init` handle describes the initial value of an additional optional loop-local variable. In each iteration, this loop-local variable, if present, will be passed to the `body` and updated with the value returned from its invocation. The result of loop execution will be the final value of the additional loop-local variable (if present).

The following rules hold for these argument handles:

- The `body` handle must not be `null`; its type must be of the form `(V A...)V`, where `V` is non-`void`, or else `(A...)void`. (In the `void` case, we assign the type `void` to the name `V`, and we will write `(V A...)V` with the understanding that a `void` type `V` is quietly dropped from the parameter list, leaving `(A...)V`.)
- The parameter list `(V A...)` of the body is called the *internal parameter list*. It will constrain the parameter lists of the other loop parts.
- If the iteration variable type `V` is dropped from the internal parameter list, the resulting shorter list `(A...)` is called the *external parameter list*.
- The body return type `V`, if non-`void`, determines the type of an additional state variable of the loop. The body must both accept and return a value of this type `V`.
- If `init` is non-`null`, it must have return type `V`. Its parameter list (of some [form `(A*)`](MethodHandles.md)) must be [effectively identical](MethodHandles.md) to the external parameter list `(A...)`.
- If `init` is `null`, the loop variable will be initialized to its [default value](MethodHandles.md)).
- The `pred` handle must not be `null`. It must have `boolean` as its return type. Its parameter list (either empty or of the form `(V A*)`) must be effectively identical to the internal parameter list.

The resulting loop handle's result type and parameter signature are determined as follows:

- The loop handle's result type is the result type `V` of the body.
- The loop handle's parameter types are the types `(A...)`, from the external parameter list.

Here is pseudocode for the resulting loop handle. In the code, `V`/`v` represent the type / value of the sole loop variable as well as the result type of the loop; and `A`/`a`, that of the argument passed to the loop. 

```kotlin
<code>V init(A...);
  boolean pred(V, A...);
  V body(V, A...);
  V doWhileLoop(A... a...) {
    V v = init(a...);
    do {
      v = body(v, a...);
    } while (pred(v, a...));
    return v;
  }
  </code>
```

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `init` | [MethodHandle](MethodHandle.md)!: optional initializer, providing the initial value of the loop variable. May be `null`, implying a default initial value. See above for other constraints. |
| `body` | [MethodHandle](MethodHandle.md)!: body of the loop, which may not be `null`. It controls the loop parameters and result type. See above for other constraints. |
| `pred` | [MethodHandle](MethodHandle.md)!: condition for the loop, which may not be `null`. Its result type must be `boolean`. See above for other constraints. |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [MethodHandle](MethodHandle.md)! | a method handle implementing the `while` loop as described by the arguments. |

| Exceptions ||
|--------------------------------------|----------------------------------------------|
| `java.lang.IllegalArgumentException` | if the rules for the arguments are violated. |
| `java.lang.NullPointerException` | if `pred` or `body` are `null`. |

**See Also**

- [#loop(MethodHandle[][])](https://developer.android.com/reference/kotlin/java/lang/invoke/MethodHandles#loop(kotlin.Array))
- [#whileLoop(MethodHandle, MethodHandle, MethodHandle)](MethodHandles.md)) 

### dropArguments

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun dropArguments(
    target: MethodHandle!, 
    pos: Int, 
    vararg valueTypes: Class<*>!
): MethodHandle!
```

Produces a method handle which will discard some placeholder arguments before calling some other specified *target* method handle. The type of the new method handle will be the same as the target's type, except it will also include the placeholder argument types, at some given position.

The `pos` argument may range between zero and *N* , where *N* is the arity of the target. If `pos` is zero, the placeholder arguments will precede the target's real arguments; if `pos` is *N* they will come after.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `target` | [MethodHandle](MethodHandle.md)!: the method handle to invoke after the arguments are dropped |
| `valueTypes` | [Class](../java.lang/Class.md)\<\*\>!: the type(s) of the argument(s) to drop |
| `pos` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): position of first argument to drop (zero for the leftmost) |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [MethodHandle](MethodHandle.md)! | a method handle which drops arguments of the given types, before calling the original method handle |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the target is null, or if the `valueTypes` array or any of its elements is null |
| `java.lang.IllegalArgumentException` | if any element of `valueTypes` is `void.class`, or if `pos` is negative or greater than the arity of the target, or if the new method handle's type would have [too many parameters](MethodHandle.md) |

### dropArguments

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun dropArguments(
    target: MethodHandle!, 
    pos: Int, 
    valueTypes: MutableList<Class<*>!>!
): MethodHandle!
```

Produces a method handle which will discard some placeholder arguments before calling some other specified *target* method handle. The type of the new method handle will be the same as the target's type, except it will also include the placeholder argument types, at some given position.

The `pos` argument may range between zero and *N* , where *N* is the arity of the target. If `pos` is zero, the placeholder arguments will precede the target's real arguments; if `pos` is *N* they will come after.

**Example:** 

```kotlin
<code>import static java.lang.invoke.MethodHandles.*;
 import static java.lang.invoke.MethodType.*;
 ...
 MethodHandle cat = lookup().findVirtual(String.class,
 "concat", methodType(String.class, String.class));
 assertEquals("xy", (String) cat.invokeExact("x", "y"));
 MethodType bigType = cat.type().insertParameterTypes(0, int.class, String.class);
 MethodHandle d0 = dropArguments(cat, 0, bigType.parameterList().subList(0,2));
 assertEquals(bigType, d0.type());
 assertEquals("yz", (String) d0.invokeExact(123, "x", "y", "z"));
     </code>
```

This method is also equivalent to the following code: 

```kotlin
<code><a docref="java.lang.invoke.MethodHandles$dropArguments(java.lang.invoke.MethodHandle, kotlin.Int, kotlin.Array((java.lang.Class((kotlin.Any)))))">dropArguments</a></code><code>(target, pos, valueTypes.toArray(new Class[0]))</code>
```

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `target` | [MethodHandle](MethodHandle.md)!: the method handle to invoke after the arguments are dropped |
| `valueTypes` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Class](../java.lang/Class.md)\<\*\>!\>!: the type(s) of the argument(s) to drop |
| `pos` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): position of first argument to drop (zero for the leftmost) |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [MethodHandle](MethodHandle.md)! | a method handle which drops arguments of the given types, before calling the original method handle |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the target is null, or if the `valueTypes` list or any of its elements is null |
| `java.lang.IllegalArgumentException` | if any element of `valueTypes` is `void.class`, or if `pos` is negative or greater than the arity of the target, or if the new method handle's type would have too many parameters |

### dropArgumentsToMatch

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun dropArgumentsToMatch(
    target: MethodHandle!, 
    skip: Int, 
    newTypes: MutableList<Class<*>!>!, 
    pos: Int
): MethodHandle!
```

Adapts a target method handle to match the given parameter type list. If necessary, adds placeholder arguments. Some leading parameters can be skipped before matching begins. The remaining types in the `target`'s parameter type list must be a sub-list of the `newTypes` type list at the starting position `pos`. The resulting handle will have the target handle's parameter type list, with any non-matching parameter types (before or after the matching sub-list) inserted in corresponding positions of the target's original parameters, as if by .

The resulting handle will have the same return type as the target handle.

In more formal terms, assume these two type lists:

- The target handle has the parameter type list `S..., M...`, with as many types in `S` as indicated by `skip`. The `M` types are those that are supposed to match part of the given type list, `newTypes`.
- The `newTypes` list contains types `P..., M..., A...`, with as many types in `P` as indicated by `pos`. The `M` types are precisely those that the `M` types in the target handle's parameter type list are supposed to match. The types in `A` are additional types found after the matching sub-list.

Given these assumptions, the result of an invocation of `dropArgumentsToMatch` will have the parameter type list `S..., P..., M..., A...`, with the `P` and `A` types inserted as if by [dropArguments(java.lang.invoke.MethodHandle,int,java.lang.Class[])](https://developer.android.com/reference/kotlin/java/lang/invoke/MethodHandles#dropArguments(java.lang.invoke.MethodHandle,%20kotlin.Int,%20java.lang.Class)).

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `target` | [MethodHandle](MethodHandle.md)!: the method handle to adapt |
| `skip` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): number of targets parameters to disregard (they will be unchanged) |
| `newTypes` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Class](../java.lang/Class.md)\<\*\>!\>!: the list of types to match `target`'s parameter type list to |
| --- | --- |
| `pos` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): place in `newTypes` where the non-skipped target parameters must occur |

| Return ||
|-----------------------------------------------------------------------------------------------|----------------------------------|
| [MethodHandle](MethodHandle.md)! | a possibly adapted method handle |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if either argument is null |
| `java.lang.IllegalArgumentException` | if any element of `newTypes` is `void.class`, or if `skip` is negative or greater than the arity of the target, or if `pos` is negative or greater than the newTypes list size, or if `newTypes` does not contain the `target`'s non-skipped parameter types at position `pos`. |

### dropReturn

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun dropReturn(target: MethodHandle!): MethodHandle!
```

Drop the return value of the target handle (if any). The returned method handle will have a `void` return type.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------|
| `target` | [MethodHandle](MethodHandle.md)!: the method handle to adapt |

| Return ||
|-----------------------------------------------------------------------------------------------|----------------------------------|
| [MethodHandle](MethodHandle.md)! | a possibly adapted method handle |

| Exceptions ||
|----------------------------------|---------------------|
| `java.lang.NullPointerException` | if `target` is null |

### empty

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun empty(type: MethodType!): MethodHandle!
```

Produces a method handle of the requested type which ignores any arguments, does nothing, and returns a suitable default depending on the return type. That is, it returns a zero primitive value, a `null`, or `void`.

The returned method handle is equivalent to `dropArguments(zero(type.returnType()), 0, type.parameterList())`.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------|
| `type` | [MethodType](MethodType.md)!: the type of the desired method handle |

| Return ||
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [MethodHandle](MethodHandle.md)! | a constant method handle of the given type, which returns a default value of the given return type |

| Exceptions ||
|----------------------------------|-------------------------|
| `java.lang.NullPointerException` | if the argument is null |

**See Also**

- [java.lang.invoke.MethodHandles#zero](MethodHandles.md))
- [java.lang.invoke.MethodHandles#constant](MethodHandles.md)) 

### exactInvoker

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun exactInvoker(type: MethodType!): MethodHandle!
```

Produces a special *invoker method handle* which can be used to invoke any method handle of the given type, as if by [invokeExact](MethodHandle.md)). The resulting invoker will have a type which is exactly equal to the desired type, except that it will accept an additional leading argument of type `MethodHandle`.

This method is equivalent to the following code (though it may be more efficient): `publicLookup().findVirtual(MethodHandle.class, "invokeExact", type)`

*Discussion:* Invoker method handles can be useful when working with variable method handles of unknown types. For example, to emulate an `invokeExact` call to a variable method handle `M`, extract its type `T`, look up the invoker method `X` for `T`, and call the invoker method, as `X.invoke(T, A...)`. (It would not work to call `X.invokeExact`, since the type `T` is unknown.) If spreading, collecting, or other argument transformations are required, they can be applied once to the invoker `X` and reused on many `M` method handle values, as long as they are compatible with the type of `X`.

*(Note: The invoker method is not available via the Core Reflection API. An attempt to call [java.lang.reflect.Method.invoke](../java.lang.reflect/Method.md)) on the declared `invokeExact` or `invoke` method will raise an [UnsupportedOperationException](../java.lang/UnsupportedOperationException.md).)*

This method throws no reflective or security exceptions.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------|
| `type` | [MethodType](MethodType.md)!: the desired target type |

| Return ||
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [MethodHandle](MethodHandle.md)! | a method handle suitable for invoking any method handle of the given type |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the resulting method handle's type would have [too many parameters](MethodHandle.md) |

### explicitCastArguments

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun explicitCastArguments(
    target: MethodHandle!, 
    newType: MethodType!
): MethodHandle!
```

Produces a method handle which adapts the type of the given method handle to a new type by pairwise argument and return type conversion. The original type and new type must have the same number of arguments. The resulting method handle is guaranteed to report a type which is equal to the desired new type.

If the original type and new type are equal, returns target.

The same conversions are allowed as for [MethodHandle.asType](MethodHandle.md)), and some additional conversions are also applied if those conversions fail. Given types *T0* , *T1* , one of the following conversions is applied if possible, before or instead of any conversions done by `asType`:

- If *T0* and *T1* are references, and *T1* is an interface type, then the value of type *T0* is passed as a *T1* without a cast. (This treatment of interfaces follows the usage of the bytecode verifier.)
- If *T0* is boolean and *T1* is another primitive, the boolean is converted to a byte value, 1 for true, 0 for false. (This treatment follows the usage of the bytecode verifier.)
- If *T1* is boolean and *T0* is another primitive, *T0* is converted to byte via Java casting conversion (JLS 5.5), and the low order bit of the result is tested, as if by `(x & 1) != 0`.
- If *T0* and *T1* are primitives other than boolean, then a Java casting conversion (JLS 5.5) is applied. (Specifically, *T0* will convert to *T1* by widening and/or narrowing.)
- If *T0* is a reference and *T1* a primitive, an unboxing conversion will be applied at runtime, possibly followed by a Java casting conversion (JLS 5.5) on the primitive value, possibly followed by a conversion from byte to boolean by testing the low-order bit.
- If *T0* is a reference and *T1* a primitive, and if the reference is null at runtime, a zero value is introduced.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `target` | [MethodHandle](MethodHandle.md)!: the method handle to invoke after arguments are retyped |
| `newType` | [MethodType](MethodType.md)!: the expected type of the new method handle |

| Return ||
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MethodHandle](MethodHandle.md)! | a method handle which delegates to the target after performing any necessary argument conversions, and arranges for any necessary return value conversions |

| Exceptions ||
|---------------------------------------------|----------------------------------|
| `java.lang.NullPointerException` | if either argument is null |
| `java.lang.invoke.WrongMethodTypeException` | if the conversion cannot be made |

**See Also**

- [java.lang.invoke.MethodHandle#asType](MethodHandle.md)) 

### filterArguments

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun filterArguments(
    target: MethodHandle!, 
    pos: Int, 
    vararg filters: MethodHandle!
): MethodHandle!
```

Adapts a target method handle by pre-processing one or more of its arguments, each with its own unary filter function, and then calling the target with each pre-processed argument replaced by the result of its corresponding filter function.

The pre-processing is performed by one or more method handles, specified in the elements of the `filters` array. The first element of the filter array corresponds to the `pos` argument of the target, and so on in sequence. The filter functions are invoked in left to right order.

Null arguments in the array are treated as identity functions, and the corresponding arguments left unchanged. (If there are no non-null elements in the array, the original target is returned.) Each filter is applied to the corresponding argument of the adapter.

If a filter `F` applies to the `N`th argument of the target, then `F` must be a method handle which takes exactly one argument. The type of `F`'s sole argument replaces the corresponding argument type of the target in the resulting adapted method handle. The return type of `F` must be identical to the corresponding parameter type of the target.

It is an error if there are elements of `filters` (null or not) which do not correspond to argument positions in the target.

**Example:** 

```kotlin
<code>import static java.lang.invoke.MethodHandles.*;
 import static java.lang.invoke.MethodType.*;
 ...
 MethodHandle cat = lookup().findVirtual(String.class,
 "concat", methodType(String.class, String.class));
 MethodHandle upcase = lookup().findVirtual(String.class,
 "toUpperCase", methodType(String.class));
 assertEquals("xy", (String) cat.invokeExact("x", "y"));
 MethodHandle f0 = filterArguments(cat, 0, upcase);
 assertEquals("Xy", (String) f0.invokeExact("x", "y")); // Xy
 MethodHandle f1 = filterArguments(cat, 1, upcase);
 assertEquals("xY", (String) f1.invokeExact("x", "y")); // xY
 MethodHandle f2 = filterArguments(cat, 0, upcase, upcase);
 assertEquals("XY", (String) f2.invokeExact("x", "y")); // XY
     </code>
```

Here is pseudocode for the resulting adapter. In the code, `T` denotes the return type of both the `target` and resulting adapter. `P`/`p` and `B`/`b` represent the types and values of the parameters and arguments that precede and follow the filter position `pos`, respectively. `A[i]`/`a[i]` stand for the types and values of the filtered parameters and arguments; they also represent the return types of the `filter[i]` handles. The latter accept arguments `v[i]` of type `V[i]`, which also appear in the signature of the resulting adapter. 

```kotlin
<code>T target(P... p, A[i]... a[i], B... b);
     A[i] filter[i](V[i]);
     T adapter(P... p, V[i]... v[i], B... b) {
       return target(p..., filter[i](v[i])..., b...);
     }
     </code>
```

*Note:* The resulting adapter is never a [variable-arity method handle](MethodHandle.md)), even if the original target method handle was.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `target` | [MethodHandle](MethodHandle.md)!: the method handle to invoke after arguments are filtered |
| `pos` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the position of the first argument to filter |
| `filters` | [MethodHandle](MethodHandle.md)!: method handles to call initially on filtered arguments |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [MethodHandle](MethodHandle.md)! | method handle which incorporates the specified argument filtering logic |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the target is null or if the `filters` array is null |
| `java.lang.IllegalArgumentException` | if a non-null element of `filters` does not match a corresponding argument type of target as described above, or if the `pos+filters.length` is greater than `target.type().parameterCount()`, or if the resulting method handle's type would have [too many parameters](MethodHandle.md) |

### filterReturnValue

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun filterReturnValue(
    target: MethodHandle!, 
    filter: MethodHandle!
): MethodHandle!
```

Adapts a target method handle by post-processing its return value (if any) with a filter (another method handle). The result of the filter is returned from the adapter.

If the target returns a value, the filter must accept that value as its only argument. If the target returns void, the filter must accept no arguments.

The return type of the filter replaces the return type of the target in the resulting adapted method handle. The argument type of the filter (if any) must be identical to the return type of the target.

**Example:** 

```kotlin
<code>import static java.lang.invoke.MethodHandles.*;
 import static java.lang.invoke.MethodType.*;
 ...
 MethodHandle cat = lookup().findVirtual(String.class,
 "concat", methodType(String.class, String.class));
 MethodHandle length = lookup().findVirtual(String.class,
 "length", methodType(int.class));
 System.out.println((String) cat.invokeExact("x", "y")); // xy
 MethodHandle f0 = filterReturnValue(cat, length);
 System.out.println((int) f0.invokeExact("x", "y")); // 2
     </code>
```

Here is pseudocode for the resulting adapter. In the code, `T`/`t` represent the result type and value of the `target`; `V`, the result type of the `filter`; and `A`/`a`, the types and values of the parameters and arguments of the `target` as well as the resulting adapter. 

```kotlin
<code>T target(A...);
     V filter(T);
     V adapter(A... a) {
       T t = target(a...);
       return filter(t);
     }
     // and if the target has a void return:
     void target2(A...);
     V filter2();
     V adapter2(A... a) {
       target2(a...);
       return filter2();
     }
     // and if the filter has a void return:
     T target3(A...);
     void filter3(V);
     void adapter3(A... a) {
       T t = target3(a...);
       filter3(t);
     }
     </code>
```

*Note:* The resulting adapter is never a [variable-arity method handle](MethodHandle.md)), even if the original target method handle was.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `target` | [MethodHandle](MethodHandle.md)!: the method handle to invoke before filtering the return value |
| `filter` | [MethodHandle](MethodHandle.md)!: method handle to call on the return value |

| Return ||
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [MethodHandle](MethodHandle.md)! | method handle which incorporates the specified return value filtering logic |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if either argument is null |
| `java.lang.IllegalArgumentException` | if the argument list of `filter` does not match the return type of target as described above |

### foldArguments

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun foldArguments(
    target: MethodHandle!, 
    pos: Int, 
    combiner: MethodHandle!
): MethodHandle!
```

Adapts a target method handle by pre-processing some of its arguments, starting at a given position, and then calling the target with the result of the pre-processing, inserted into the original sequence of arguments just before the folded arguments.

This method is closely related to [foldArguments(java.lang.invoke.MethodHandle,java.lang.invoke.MethodHandle)](MethodHandles.md)), but allows to control the position in the parameter list at which folding takes place. The argument controlling this, `pos`, is a zero-based index. The aforementioned method [foldArguments(java.lang.invoke.MethodHandle,java.lang.invoke.MethodHandle)](MethodHandles.md)) assumes position 0.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `target` | [MethodHandle](MethodHandle.md)!: the method handle to invoke after arguments are combined |
| `pos` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the position at which to start folding and at which to insert the folding result; if this is `0`, the effect is the same as for [foldArguments(java.lang.invoke.MethodHandle,java.lang.invoke.MethodHandle)](MethodHandles.md)). |
| `combiner` | [MethodHandle](MethodHandle.md)!: method handle to call initially on the incoming arguments |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [MethodHandle](MethodHandle.md)! | method handle which incorporates the specified argument folding logic |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if either argument is null |
| `java.lang.IllegalArgumentException` | if either of the following two conditions holds: (1) `combiner`'s return type is non-`void` and not the same as the argument type at position `pos` of the target signature; (2) the `N` argument types at position `pos` of the target signature (skipping one matching the `combiner`'s return type) are not identical with the argument types of `combiner`. |

**See Also**

- [#foldArguments(MethodHandle, MethodHandle)](MethodHandles.md)) 

### foldArguments

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun foldArguments(
    target: MethodHandle!, 
    combiner: MethodHandle!
): MethodHandle!
```

Adapts a target method handle by pre-processing some of its arguments, and then calling the target with the result of the pre-processing, inserted into the original sequence of arguments.

The pre-processing is performed by `combiner`, a second method handle. Of the arguments passed to the adapter, the first `N` arguments are copied to the combiner, which is then called. (Here, `N` is defined as the parameter count of the combiner.) After this, control passes to the target, with any result from the combiner inserted before the original `N` incoming arguments.

If the combiner returns a value, the first parameter type of the target must be identical with the return type of the combiner, and the next `N` parameter types of the target must exactly match the parameters of the combiner.

If the combiner has a void return, no result will be inserted, and the first `N` parameter types of the target must exactly match the parameters of the combiner.

The resulting adapter is the same type as the target, except that the first parameter type is dropped, if it corresponds to the result of the combiner.

(Note that [dropArguments](MethodHandles.md)) can be used to remove any arguments that either the combiner or the target does not wish to receive. If some of the incoming arguments are destined only for the combiner, consider using java.lang.invoke.MethodHandle#asCollector instead, since those arguments will not need to be live on the stack on entry to the target.)

**Example:** 

```kotlin
<code>import static java.lang.invoke.MethodHandles.*;
 import static java.lang.invoke.MethodType.*;
 ...
 MethodHandle trace = publicLookup().findVirtual(java.io.PrintStream.class,
 "println", methodType(void.class, String.class))
   .bindTo(System.out);
 MethodHandle cat = lookup().findVirtual(String.class,
 "concat", methodType(String.class, String.class));
 assertEquals("boojum", (String) cat.invokeExact("boo", "jum"));
 MethodHandle catTrace = foldArguments(cat, trace);
 // also prints "boo":
 assertEquals("boojum", (String) catTrace.invokeExact("boo", "jum"));
     </code>
```

Here is pseudocode for the resulting adapter. In the code, `T` represents the result type of the `target` and resulting adapter. `V`/`v` represent the type and value of the parameter and argument of `target` that precedes the folding position; `V` also is the result type of the `combiner`. `A`/`a` denote the types and values of the `N` parameters and arguments at the folding position. `B`/`b` represent the types and values of the `target` parameters and arguments that follow the folded parameters and arguments. 

```kotlin
<code>// there are N arguments in A...
     T target(V, A[N]..., B...);
     V combiner(A...);
     T adapter(A... a, B... b) {
       V v = combiner(a...);
       return target(v, a..., b...);
     }
     // and if the combiner has a void return:
     T target2(A[N]..., B...);
     void combiner2(A...);
     T adapter2(A... a, B... b) {
       combiner2(a...);
       return target2(a..., b...);
     }
     </code>
```

*Note:* The resulting adapter is never a [variable-arity method handle](MethodHandle.md)), even if the original target method handle was.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `target` | [MethodHandle](MethodHandle.md)!: the method handle to invoke after arguments are combined |
| `combiner` | [MethodHandle](MethodHandle.md)!: method handle to call initially on the incoming arguments |

| Return ||
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [MethodHandle](MethodHandle.md)! | method handle which incorporates the specified argument folding logic |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if either argument is null |
| `java.lang.IllegalArgumentException` | if `combiner`'s return type is non-void and not the same as the first argument type of the target, or if the initial `N` argument types of the target (skipping one matching the `combiner`'s return type) are not identical with the argument types of `combiner` |

### guardWithTest

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun guardWithTest(
    test: MethodHandle!, 
    target: MethodHandle!, 
    fallback: MethodHandle!
): MethodHandle!
```

Makes a method handle which adapts a target method handle, by guarding it with a test, a boolean-valued method handle. If the guard fails, a fallback handle is called instead. All three method handles must have the same corresponding argument and return types, except that the return type of the test must be boolean, and the test is allowed to have fewer arguments than the other two method handles.

Here is pseudocode for the resulting adapter: 

```kotlin
<code>boolean test(A...);
  T target(A...,B...);
  T fallback(A...,B...);
  T adapter(A... a,B... b) {
    if (test(a...))
      return target(a..., b...);
    else
      return fallback(a..., b...);
  }
  </code>
```
Note that the test arguments (`a...` in the pseudocode) cannot be modified by execution of the test, and so are passed unchanged from the caller to the target or fallback as appropriate.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `test` | [MethodHandle](MethodHandle.md)!: method handle used for test, must return boolean |
| `target` | [MethodHandle](MethodHandle.md)!: method handle to call if test passes |
| `fallback` | [MethodHandle](MethodHandle.md)!: method handle to call if test fails |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [MethodHandle](MethodHandle.md)! | method handle which incorporates the specified if/then/else logic |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if any argument is null |
| `java.lang.IllegalArgumentException` | if `test` does not return boolean, or if all three method types do not match (with the return type of `test` changed to match that of the target). |

### identity

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun identity(type: Class<*>!): MethodHandle!
```

Produces a method handle which returns its sole argument when invoked.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `type` | [Class](../java.lang/Class.md)\<\*\>!: the type of the sole parameter and return value of the desired method handle |

| Return ||
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [MethodHandle](MethodHandle.md)! | a unary method handle which accepts and returns the given type |

| Exceptions ||
|--------------------------------------|-----------------------------------|
| `java.lang.NullPointerException` | if the argument is null |
| `java.lang.IllegalArgumentException` | if the given type is `void.class` |

### insertArguments

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun insertArguments(
    target: MethodHandle!, 
    pos: Int, 
    vararg values: Any!
): MethodHandle!
```

Provides a target method handle with one or more *bound arguments* in advance of the method handle's invocation. The formal parameters to the target corresponding to the bound arguments are called *bound parameters*. Returns a new method handle which saves away the bound arguments. When it is invoked, it receives arguments for any non-bound parameters, binds the saved arguments to their corresponding parameters, and calls the original target.

The type of the new method handle will drop the types for the bound parameters from the original target type, since the new method handle will no longer require those arguments to be supplied by its callers.

Each given argument object must match the corresponding bound parameter type. If a bound parameter type is a primitive, the argument object must be a wrapper, and will be unboxed to produce the primitive value.

The `pos` argument selects which parameters are to be bound. It may range between zero and *N-L* (inclusively), where *N* is the arity of the target method handle and *L* is the length of the values array.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `target` | [MethodHandle](MethodHandle.md)!: the method handle to invoke after the argument is inserted |
| `pos` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): where to insert the argument (zero for the first) |
| `values` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: the series of arguments to insert |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [MethodHandle](MethodHandle.md)! | a method handle which inserts an additional argument, before calling the original method handle |

| Exceptions ||
|----------------------------------|---------------------------------------------|
| `java.lang.NullPointerException` | if the target or the `values` array is null |

**See Also**

- [java.lang.invoke.MethodHandle#bindTo](MethodHandle.md)) 

### invoker

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun invoker(type: MethodType!): MethodHandle!
```

Produces a special *invoker method handle* which can be used to invoke any method handle compatible with the given type, as if by [invoke](MethodHandle.md)). The resulting invoker will have a type which is exactly equal to the desired type, except that it will accept an additional leading argument of type `MethodHandle`.

Before invoking its target, if the target differs from the expected type, the invoker will apply reference casts as necessary and box, unbox, or widen primitive values, as if by [asType](MethodHandle.md)). Similarly, the return value will be converted as necessary. If the target is a [variable arity method handle](MethodHandle.md)), the required arity conversion will be made, again as if by [asType](MethodHandle.md)).

This method is equivalent to the following code (though it may be more efficient): `publicLookup().findVirtual(MethodHandle.class, "invoke", type)`

*Discussion:* A java.lang.invoke.MethodType#genericMethodType is one which mentions only `Object` arguments and return values. An invoker for such a type is capable of calling any method handle of the same arity as the general type.

*(Note: The invoker method is not available via the Core Reflection API. An attempt to call [java.lang.reflect.Method.invoke](../java.lang.reflect/Method.md)) on the declared `invokeExact` or `invoke` method will raise an [UnsupportedOperationException](../java.lang/UnsupportedOperationException.md).)*

This method throws no reflective or security exceptions.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------|
| `type` | [MethodType](MethodType.md)!: the desired target type |

| Return ||
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [MethodHandle](MethodHandle.md)! | a method handle suitable for invoking any method handle convertible to the given type |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the resulting method handle's type would have [too many parameters](MethodHandle.md) |

### iteratedLoop

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun iteratedLoop(
    iterator: MethodHandle!, 
    init: MethodHandle!, 
    body: MethodHandle!
): MethodHandle!
```

Constructs a loop that ranges over the values produced by an `Iterator<T>`. This is a convenience wrapper for the [generic loop combinator](MethodHandles.md)).

The iterator itself will be determined by the evaluation of the `iterator` handle. Each value it produces will be stored in a loop iteration variable of type `T`.

If the `body` handle returns a non-`void` type `V`, a leading loop iteration variable of that type is also present. This variable is initialized using the optional `init` handle, or to the [default value](MethodHandles.md)) of type `V` if that handle is `null`.

In each iteration, the iteration variables are passed to an invocation of the `body` handle. A non-`void` value returned from the body (of type `V`) updates the leading iteration variable. The result of the loop handle execution will be the final `V` value of that variable (or `void` if there is no `V` variable).

The following rules hold for the argument handles:

- The `body` handle must not be `null`; its type must be of the form `(V T A...)V`, where `V` is non-`void`, or else `(T A...)void`. (In the `void` case, we assign the type `void` to the name `V`, and we will write `(V T A...)V` with the understanding that a `void` type `V` is quietly dropped from the parameter list, leaving `(T A...)V`.)
- The parameter list `(V T A...)` of the body contributes to a list of types called the *internal parameter list*. It will constrain the parameter lists of the other loop parts.
- As a special case, if the body contributes only `V` and `T` types, with no additional `A` types, then the internal parameter list is extended by the argument types `A...` of the `iterator` handle; if it is `null` the single type `Iterable` is added and constitutes the `A...` list.
- If the iteration variable types `(V T)` are dropped from the internal parameter list, the resulting shorter list `(A...)` is called the *external parameter list*.
- The body return type `V`, if non-`void`, determines the type of an additional state variable of the loop. The body must both accept a leading parameter and return a value of this type `V`.
- If `init` is non-`null`, it must have return type `V`. Its parameter list (of some [form `(A*)`](MethodHandles.md)) must be [effectively identical](MethodHandles.md) to the external parameter list `(A...)`.
- If `init` is `null`, the loop variable will be initialized to its [default value](MethodHandles.md)).
- If the `iterator` handle is non-`null`, it must have the return type `java.util.Iterator` or a subtype thereof. The iterator it produces when the loop is executed will be assumed to yield values which can be converted to type `T`.
- The parameter list of an `iterator` that is non-`null` (of some form `(A*)`) must be effectively identical to the external parameter list `(A...)`.
- If `iterator` is `null` it defaults to a method handle which behaves like [java.lang.Iterable#iterator()](../java.lang/Iterable.md)). In that case, the internal parameter list `(V T A...)` must have at least one `A` type, and the default iterator handle parameter is adjusted to accept the leading `A` type, as if by the [asType](MethodHandle.md)) conversion method. The leading `A` type must be `Iterable` or a subtype thereof. This conversion step, done at loop construction time, must not throw a `WrongMethodTypeException`.

The type `T` may be either a primitive or reference. Since type `Iterator<T>` is erased in the method handle representation to the raw type `Iterator`, the `iteratedLoop` combinator adjusts the leading argument type for `body` to `Object` as if by the [asType](MethodHandle.md)) conversion method. Therefore, if an iterator of the wrong type appears as the loop is executed, runtime exceptions may occur as the result of dynamic conversions performed by [MethodHandle.asType(MethodType)](MethodHandle.md)).

The resulting loop handle's result type and parameter signature are determined as follows:

- The loop handle's result type is the result type `V` of the body.
- The loop handle's parameter types are the types `(A...)`, from the external parameter list.

Here is pseudocode for the resulting loop handle. In the code, `V`/`v` represent the type / value of the loop variable as well as the result type of the loop; `T`/`t`, that of the elements of the structure the loop iterates over, and `A...`/`a...` represent arguments passed to the loop. 

```kotlin
<code>Iterator&lt;T&gt; iterator(A...);  // defaults to Iterable::iterator
  V init(A...);
  V body(V,T,A...);
  V iteratedLoop(A... a...) {
    Iterator&lt;T&gt; it = iterator(a...);
    V v = init(a...);
    while (it.hasNext()) {
      T t = it.next();
      v = body(v, t, a...);
    }
    return v;
  }
  </code>
```

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `iterator` | [MethodHandle](MethodHandle.md)!: an optional handle to return the iterator to start the loop. If non-`null`, the handle must return [java.util.Iterator](../java.util/Iterator.md) or a subtype. See above for other constraints. |
| `init` | [MethodHandle](MethodHandle.md)!: optional initializer, providing the initial value of the loop variable. May be `null`, implying a default initial value. See above for other constraints. |
| `body` | [MethodHandle](MethodHandle.md)!: body of the loop, which may not be `null`. It controls the loop parameters and result type in the standard case (see above for details). It must accept its own return type (if non-void) plus a `T` parameter (for the iterated values), and may accept any number of additional types. See above for other constraints. |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [MethodHandle](MethodHandle.md)! | a method handle embodying the iteration loop functionality. |

| Exceptions ||
|--------------------------------------|--------------------------------------------------|
| `java.lang.NullPointerException` | if the `body` handle is `null`. |
| `java.lang.IllegalArgumentException` | if any argument violates the above requirements. |

### lookup

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun lookup(): MethodHandles.Lookup!
```

Returns a [lookup object](../java/lang/invoke/MethodHandles.Lookup.md) with full capabilities to emulate all supported bytecode behaviors of the caller. These capabilities include [private access](../java/lang/invoke/MethodHandles.Lookup.md) to the caller. Factory methods on the lookup object can create [direct method handles](MethodHandleInfo.md) for any member that the caller has access to via bytecodes, including protected and private fields and methods. This lookup object is a *capability* which may be delegated to trusted agents. Do not store it in place where untrusted code can access it.

This method is caller sensitive, which means that it may return different values to different callers.

For any given caller class `C`, the lookup object returned by this call has equivalent capabilities to any lookup object supplied by the JVM to the bootstrap method of an [invokedynamic instruction](_package.md) executing in the same caller class `C`.

| Return ||
|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [MethodHandles.Lookup](../java/lang/invoke/MethodHandles.Lookup.md)! | a lookup object for the caller of this method, with private access |

### loop

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun loop(vararg clauses: Array<MethodHandle!>!): MethodHandle!
```

Constructs a method handle representing a loop with several loop variables that are updated and checked upon each iteration. Upon termination of the loop due to one of the predicates, a corresponding finalizer is run and delivers the loop's result, which is the return value of the resulting handle.

Intuitively, every loop is formed by one or more "clauses", each specifying a local *iteration variable* and/or a loop exit. Each iteration of the loop executes each clause in order. A clause can optionally update its iteration variable; it can also optionally perform a test and conditional loop exit. In order to express this logic in terms of method handles, each clause will specify up to four independent actions:

- *init:* Before the loop executes, the initialization of an iteration variable `v` of type `V`.
- *step:* When a clause executes, an update step for the iteration variable `v`.
- *pred:* When a clause executes, a predicate execution to test for loop exit.
- *fini:* If a clause causes a loop exit, a finalizer execution to compute the loop's return value.

The full sequence of all iteration variable types, in clause order, will be notated as `(V...)`. The values themselves will be `(v...)`. When we speak of "parameter lists", we will usually be referring to types, but in some contexts (describing execution) the lists will be of actual values.

Some of these clause parts may be omitted according to certain rules, and useful default behavior is provided in this case. See below for a detailed description.

*Parameters optional everywhere:* Each clause function is allowed but not required to accept a parameter for each iteration variable `v`. As an exception, the init functions cannot take any `v` parameters, because those values are not yet computed when the init functions are executed. Any clause function may neglect to take any trailing subsequence of parameters it is entitled to take. In fact, any clause function may take no arguments at all.

*Loop parameters:* A clause function may take all the iteration variable values it is entitled to, in which case it may also take more trailing parameters. Such extra values are called *loop parameters* , with their types and values notated as `(A...)` and `(a...)`. These become the parameters of the resulting loop handle, to be supplied whenever the loop is executed. (Since init functions do not accept iteration variables `v`, any parameter to an init function is automatically a loop parameter `a`.) As with iteration variables, clause functions are allowed but not required to accept loop parameters. These loop parameters act as loop-invariant values visible across the whole loop.

*Parameters visible everywhere:* Each non-init clause function is permitted to observe the entire loop state, because it can be passed the full list `(v... a...)` of current iteration variable values and incoming loop parameters. The init functions can observe initial pre-loop state, in the form `(a...)`. Most clause functions will not need all of this information, but they will be formally connected to it as if by #dropArguments. More specifically, we shall use the notation `(V*)` to express an arbitrary prefix of a full sequence `(V...)` (and likewise for `(v*)`, `(A*)`, `(a*)`). In that notation, the general form of an init function parameter list is `(A*)`, and the general form of a non-init function parameter list is `(V*)` or `(V... A*)`.

*Checking clause structure:* Given a set of clauses, there is a number of checks and adjustments performed to connect all the parts of the loop. They are spelled out in detail in the steps below. In these steps, every occurrence of the word "must" corresponds to a place where [IllegalArgumentException](../java.lang/IllegalArgumentException.md) will be thrown if the required constraint is not met by the inputs to the loop combinator.

*Effectively identical sequences:* A parameter list `A` is defined to be *effectively identical* to another parameter list `B` if `A` and `B` are identical, or if `A` is shorter and is identical with a proper prefix of `B`. When speaking of an unordered set of parameter lists, we say they the set is "effectively identical" as a whole if the set contains a longest list, and all members of the set are effectively identical to that longest list. For example, any set of type sequences of the form `(V*)` is effectively identical, and the same is true if more sequences of the form `(V... A*)` are added.

*Step 0: Determine clause structure.*

1. The clause array (of type `MethodHandle[][]`) must be non-`null` and contain at least one element.
2. The clause array may not contain `null`s or sub-arrays longer than four elements.
3. Clauses shorter than four elements are treated as if they were padded by `null` elements to length four. Padding takes place by appending elements to the array.
4. Clauses with all `null`s are disregarded.
5. Each clause is treated as a four-tuple of functions, called "init", "step", "pred", and "fini".

*Step 1A: Determine iteration variable types `(V...)`.*

1. The iteration variable type for each clause is determined using the clause's init and step return types.
2. If both functions are omitted, there is no iteration variable for the corresponding clause (`void` is used as the type to indicate that). If one of them is omitted, the other's return type defines the clause's iteration variable type. If both are given, the common return type (they must be identical) defines the clause's iteration variable type.
3. Form the list of return types (in clause order), omitting all occurrences of `void`.
4. This list of types is called the "iteration variable types" (`(V...)`).

*Step 1B: Determine loop parameters `(A...)`.*

- Examine and collect init function parameter lists (which are of the form `(A*)`).
- Examine and collect the suffixes of the step, pred, and fini parameter lists, after removing the iteration variable types. (They must have the form `(V... A*)`; collect the `(A*)` parts only.)
- Do not collect suffixes from step, pred, and fini parameter lists that do not begin with all the iteration variable types. (These types will be checked in step 2, along with all the clause function types.)
- Omitted clause functions are ignored. (Equivalently, they are deemed to have empty parameter lists.)
- All of the collected parameter lists must be effectively identical.
- The longest parameter list (which is necessarily unique) is called the "external parameter list" (`(A...)`).
- If there is no such parameter list, the external parameter list is taken to be the empty sequence.
- The combined list consisting of iteration variable types followed by the external parameter types is called the "internal parameter list".

*Step 1C: Determine loop return type.*

1. Examine fini function return types, disregarding omitted fini functions.
2. If there are no fini functions, the loop return type is `void`.
3. Otherwise, the common return type `R` of the fini functions (their return types must be identical) defines the loop return type.

*Step 1D: Check other types.*

1. There must be at least one non-omitted pred function.
2. Every non-omitted pred function must have a `boolean` return type.

*Step 2: Determine parameter lists.*

1. The parameter list for the resulting loop handle will be the external parameter list `(A...)`.
2. The parameter list for init functions will be adjusted to the external parameter list. (Note that their parameter lists are already effectively identical to this list.)
3. The parameter list for every non-omitted, non-init (step, pred, and fini) function must be effectively identical to the internal parameter list `(V... A...)`.

*Step 3: Fill in omitted functions.*

1. If an init function is omitted, use a [default value](MethodHandles.md)) for the clause's iteration variable type.
2. If a step function is omitted, use an [identity function](MethodHandles.md)) of the clause's iteration variable type; insert dropped argument parameters before the identity function parameter for the non-`void` iteration variables of preceding clauses. (This will turn the loop variable into a local loop invariant.)
3. If a pred function is omitted, use a constant `true` function. (This will keep the loop going, as far as this clause is concerned. Note that in such cases the corresponding fini function is unreachable.)
4. If a fini function is omitted, use a [default value](MethodHandles.md)) for the loop return type.

*Step 4: Fill in missing parameter types.*

1. At this point, every init function parameter list is effectively identical to the external parameter list `(A...)`, but some lists may be shorter. For every init function with a short parameter list, pad out the end of the list.
2. At this point, every non-init function parameter list is effectively identical to the internal parameter list `(V... A...)`, but some lists may be shorter. For every non-init function with a short parameter list, pad out the end of the list.
3. Argument lists are padded out by [dropping unused trailing arguments](MethodHandles.md)).

*Final observations.*

1. After these steps, all clauses have been adjusted by supplying omitted functions and arguments.
2. All init functions have a common parameter type list `(A...)`, which the final loop handle will also have.
3. All fini functions have a common return type `R`, which the final loop handle will also have.
4. All non-init functions have a common parameter type list `(V... A...)`, of (non-`void`) iteration variables `V` followed by loop parameters.
5. Each pair of init and step functions agrees in their return type `V`.
6. Each non-init function will be able to observe the current values `(v...)` of all iteration variables.
7. Every function will be able to observe the incoming values `(a...)` of all loop parameters.

*Example.* As a consequence of step 1A above, the `loop` combinator has the following property:

- Given `N` clauses `Cn = {null, Sn, Pn}` with `n = 1..N`.
- Suppose predicate handles `Pn` are either `null` or have no parameters. (Only one `Pn` has to be non-`null`.)
- Suppose step handles `Sn` have signatures `(B1..BX)Rn`, for some constant `X>=N`.
- Suppose `Q` is the count of non-void types `Rn`, and `(V1...VQ)` is the sequence of those types.
- It must be that `Vn == Bn` for `n = 1..min(X,Q)`.
- The parameter types `Vn` will be interpreted as loop-local state elements `(V...)`.
- Any remaining types `BQ+1..BX` (if `Q<X`) will determine the resulting loop handle's parameter types `(A...)`.

In this example, the loop handle parameters `(A...)` were derived from the step functions, which is natural if most of the loop computation happens in the steps. For some loops, the burden of computation might be heaviest in the pred functions, and so the pred functions might need to accept the loop parameter values. For loops with complex exit logic, the fini functions might need to accept loop parameters, and likewise for loops with complex entry logic, where the init functions will need the extra parameters. For such reasons, the rules for determining these parameters are as symmetric as possible, across all clause parts. In general, the loop parameters function as common invariant values across the whole loop, while the iteration variables function as common variant values, or (if there is no step function) as internal loop invariant temporaries.

*Loop execution.*

1. When the loop is called, the loop input values are saved in locals, to be passed to every clause function. These locals are loop invariant.
2. Each init function is executed in clause order (passing the external arguments `(a...)`) and the non-`void` values are saved (as the iteration variables `(v...)`) into locals. These locals will be loop varying (unless their steps behave as identity functions, as noted above).
3. All function executions (except init functions) will be passed the internal parameter list, consisting of the non-`void` iteration values `(v...)` (in clause order) and then the loop inputs `(a...)` (in argument order).
4. The step and pred functions are then executed, in clause order (step before pred), until a pred function returns `false`.
5. The non-`void` result from a step function call is used to update the corresponding value in the sequence `(v...)` of loop variables. The updated value is immediately visible to all subsequent function calls.
6. If a pred function returns `false`, the corresponding fini function is called, and the resulting value (of type `R`) is returned from the loop as a whole.
7. If all the pred functions always return true, no fini function is ever invoked, and the loop cannot exit except by throwing an exception.

*Usage tips.*

- Although each step function will receive the current values of *all* the loop variables, sometimes a step function only needs to observe the current value of its own variable. In that case, the step function may need to explicitly #dropArguments. This will require mentioning their types, in an expression like `dropArguments(step, 0, V0.class, ...)`.
- Loop variables are not required to vary; they can be loop invariant. A clause can create a loop invariant by a suitable init function with no step, pred, or fini function. This may be useful to "wire" an incoming loop argument into the step or pred function of an adjacent loop variable.
- If some of the clause functions are virtual methods on an instance, the instance itself can be conveniently placed in an initial invariant loop "variable", using an initial clause like `new MethodHandle[]{identity(ObjType.class)}`. In that case, the instance reference will be the first iteration variable value, and it will be easy to use virtual methods as clause parts, since all of them will take a leading instance reference matching that value.

Here is pseudocode for the resulting loop handle. As above, `V` and `v` represent the types and values of loop variables; `A` and `a` represent arguments passed to the whole loop; and `R` is the common result type of all finalizers as well as of the resulting loop. 

```kotlin
<code>V... init...(A...);
  boolean pred...(V..., A...);
  V... step...(V..., A...);
  R fini...(V..., A...);
  R loop(A... a) {
    V... v... = init...(a...);
    for (;;) {
      for ((v, p, s, f) in (v..., pred..., step..., fini...)) {
        v = s(v..., a...);
        if (!p(v..., a...)) {
          return f(v..., a...);
        }
      }
    }
  }
  </code>
```
Note that the parameter type lists `(V...)` and `(A...)` have been expanded to their full length, even though individual clause functions may neglect to take them all. As noted above, missing parameters are filled in as if by [dropArgumentsToMatch(java.lang.invoke.MethodHandle,int,java.util.List,int)](MethodHandles.md)).

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `clauses` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [MethodHandle](MethodHandle.md)!\>!: an array of arrays (4-tuples) of [MethodHandle](MethodHandle.md) s adhering to the rules described above. |

| Return ||
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [MethodHandle](MethodHandle.md)! | a method handle embodying the looping behavior as defined by the arguments. |

| Exceptions ||
|--------------------------------------|-------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | in case any of the constraints described above is violated. |

**See Also**

- [java.lang.invoke.MethodHandles#whileLoop(MethodHandle, MethodHandle, MethodHandle)](MethodHandles.md))
- [java.lang.invoke.MethodHandles#doWhileLoop(MethodHandle, MethodHandle, MethodHandle)](MethodHandles.md))
- [java.lang.invoke.MethodHandles#countedLoop(MethodHandle, MethodHandle, MethodHandle)](MethodHandles.md))
- [java.lang.invoke.MethodHandles#iteratedLoop(MethodHandle, MethodHandle, MethodHandle)](MethodHandles.md)) 

### permuteArguments

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun permuteArguments(
    target: MethodHandle!, 
    newType: MethodType!, 
    vararg reorder: Int
): MethodHandle!
```

Produces a method handle which adapts the calling sequence of the given method handle to a new type, by reordering the arguments. The resulting method handle is guaranteed to report a type which is equal to the desired new type.

The given array controls the reordering. Call `I` the number of incoming parameters (the value `newType.parameterCount()`, and call `O` the number of outgoing parameters (the value `target.type().parameterCount()`). Then the length of the reordering array must be `O`, and each element must be a non-negative number less than `I`. For every `N` less than `O`, the `N`-th outgoing argument will be taken from the `I`-th incoming argument, where `I` is `reorder[N]`.

No argument or return value conversions are applied. The type of each incoming argument, as determined by `newType`, must be identical to the type of the corresponding outgoing parameter or parameters in the target method handle. The return type of `newType` must be identical to the return type of the original target.

The reordering array need not specify an actual permutation. An incoming argument will be duplicated if its index appears more than once in the array, and an incoming argument will be dropped if its index does not appear in the array. As in the case of [dropArguments](MethodHandles.md)), incoming arguments which are not mentioned in the reordering array are may be any type, as determined only by `newType`. 

```kotlin
<code>import static java.lang.invoke.MethodHandles.*;
 import static java.lang.invoke.MethodType.*;
 ...
 MethodType intfn1 = methodType(int.class, int.class);
 MethodType intfn2 = methodType(int.class, int.class, int.class);
 MethodHandle sub = ... (int x, int y) -&gt; (x-y) ...;
 assert(sub.type().equals(intfn2));
 MethodHandle sub1 = permuteArguments(sub, intfn2, 0, 1);
 MethodHandle rsub = permuteArguments(sub, intfn2, 1, 0);
 assert((int)rsub.invokeExact(1, 100) == 99);
 MethodHandle add = ... (int x, int y) -&gt; (x+y) ...;
 assert(add.type().equals(intfn2));
 MethodHandle twice = permuteArguments(add, intfn1, 0, 0);
 assert(twice.type().equals(intfn1));
 assert((int)twice.invokeExact(21) == 42);
     </code>
```

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `target` | [MethodHandle](MethodHandle.md)!: the method handle to invoke after arguments are reordered |
| `newType` | [MethodType](MethodType.md)!: the expected type of the new method handle |
| `reorder` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): an index array which controls the reordering |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [MethodHandle](MethodHandle.md)! | a method handle which delegates to the target after it drops unused arguments and moves and/or duplicates the other arguments |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if any argument is null |
| `java.lang.IllegalArgumentException` | if the index array length is not equal to the arity of the target, or if any index array element not a valid index for a parameter of `newType`, or if two corresponding parameter types in `target.type()` and `newType` are not identical, |

### privateLookupIn

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun privateLookupIn(
    targetClass: Class<*>!, 
    lookup: MethodHandles.Lookup!
): MethodHandles.Lookup!
```

Returns a [lookup object](../java/lang/invoke/MethodHandles.Lookup.md) with full capabilities to emulate all supported bytecode behaviors, including [private access](../java/lang/invoke/MethodHandles.Lookup.md), on a target class.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `targetClass` | [Class](../java.lang/Class.md)\<\*\>!: the target class |
| `lookup` | [MethodHandles.Lookup](../java/lang/invoke/MethodHandles.Lookup.md)!: the caller lookup object |

| Return ||
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [MethodHandles.Lookup](../java/lang/invoke/MethodHandles.Lookup.md)! | a lookup object for the target class, with private access |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------|
| `java.lang.IllegalArgumentException` | if `targetClass` is a primitive type or array class |
| `java.lang.NullPointerException` | if `targetClass` or `caller` is `null` |
| `java.lang.IllegalAccessException` | is not thrown on Android |
| --- | --- |

### publicLookup

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun publicLookup(): MethodHandles.Lookup!
```

Returns a [lookup object](../java/lang/invoke/MethodHandles.Lookup.md) which is trusted minimally. It can only be used to create method handles to publicly accessible fields and methods.

As a matter of pure convention, the [lookup class](../java/lang/invoke/MethodHandles.Lookup.md)) of this lookup object will be [java.lang.Object](../java.lang/Object.md).

*Discussion:* The lookup class can be changed to any other class `C` using an expression of the form [publicLookup().in(C.class)](../java/lang/invoke/MethodHandles.Lookup.md)). Since all classes have equal access to public names, such a change would confer no new access rights. A public lookup object is always subject to [security manager checks](../java/lang/invoke/MethodHandles.Lookup.md). Also, it cannot access [caller sensitive methods](../java/lang/invoke/MethodHandles.Lookup.md).

| Return ||
|---------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| [MethodHandles.Lookup](../java/lang/invoke/MethodHandles.Lookup.md)! | a lookup object which is trusted minimally |

### reflectAs

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <T : Member!> reflectAs(
    expected: Class<T>!, 
    target: MethodHandle!
): T
```

Performs an unchecked "crack" of a [direct method handle](MethodHandleInfo.md). The result is as if the user had obtained a lookup object capable enough to crack the target method handle, called [Lookup.revealDirect](../java/lang/invoke/MethodHandles.Lookup.md)) on the target to obtain its symbolic reference, and then called [MethodHandleInfo.reflectAs](MethodHandleInfo.md)) to resolve the symbolic reference to a member.

If there is a security manager, its `checkPermission` method is called with a `ReflectPermission("suppressAccessChecks")` permission.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | the desired type of the result, either [Member](../java.lang.reflect/Member.md) or a subtype |
| `target` | [MethodHandle](MethodHandle.md)!: a direct method handle to crack into symbolic reference components |
| `expected` | [Class](../java.lang/Class.md)\<T\>!: a class object representing the desired result type `T` |
| --- | --- |

| Return ||
|---|---------------------------------------------------------|
| T | a reference to the method, constructor, or field object |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------|
| `java.lang.SecurityException` | if the caller is not privileged to call `setAccessible` |
| `java.lang.NullPointerException` | if either argument is `null` |
| `java.lang.IllegalArgumentException` | if the target is not a direct method handle |
| --- | --- |
| `java.lang.ClassCastException` | if the member is not of the expected type |

### spreadInvoker

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun spreadInvoker(
    type: MethodType!, 
    leadingArgCount: Int
): MethodHandle!
```

Produces a method handle which will invoke any method handle of the given `type`, with a given number of trailing arguments replaced by a single trailing `Object[]` array. The resulting invoker will be a method handle with the following arguments:

- a single `MethodHandle` target
- zero or more leading values (counted by `leadingArgCount`)
- an `Object[]` array containing trailing arguments

<br />

The invoker will invoke its target like a call to [invoke](MethodHandle.md)) with the indicated `type`. That is, if the target is exactly of the given `type`, it will behave like `invokeExact`; otherwise it behave as if [asType](MethodHandle.md)) is used to convert the target to the required `type`.

The type of the returned invoker will not be the given `type`, but rather will have all parameters except the first `leadingArgCount` replaced by a single array of type `Object[]`, which will be the final parameter.

Before invoking its target, the invoker will spread the final array, apply reference casts as necessary, and unbox and widen primitive arguments. If, when the invoker is called, the supplied array argument does not have the correct number of elements, the invoker will throw an [IllegalArgumentException](../java.lang/IllegalArgumentException.md) instead of invoking the target.

This method is equivalent to the following code (though it may be more efficient): 

```kotlin
<code>MethodHandle invoker = MethodHandles.invoker(type);
 int spreadArgCount = type.parameterCount() - leadingArgCount;
 invoker = invoker.asSpreader(Object[].class, spreadArgCount);
 return invoker;
     </code>
```
This method throws no reflective or security exceptions.

| Parameters ||
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `type` | [MethodType](MethodType.md)!: the desired target type |
| `leadingArgCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): number of fixed arguments, to be passed unchanged to the target |

| Return ||
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [MethodHandle](MethodHandle.md)! | a method handle suitable for invoking any method handle of the given type |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if `type` is null |
| `java.lang.IllegalArgumentException` | if `leadingArgCount` is not in the range from 0 to `type.parameterCount()` inclusive, or if the resulting method handle's type would have [too many parameters](MethodHandle.md) |

### tableSwitch

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun tableSwitch(
    fallback: MethodHandle!, 
    vararg targets: MethodHandle!
): MethodHandle!
```

Creates a table switch method handle, which can be used to switch over a set of target method handles, based on a given target index, called selector.

For a selector value of `n`, where `n` falls in the range `[0, N)`, and where `N` is the number of target method handles, the table switch method handle will invoke the n-th target method handle from the list of target method handles.

For a selector value that does not fall in the range `[0, N)`, the table switch method handle will invoke the given fallback method handle.

All method handles passed to this method must have the same type, with the additional requirement that the leading parameter be of type `int`. The leading parameter represents the selector.

Any trailing parameters present in the type will appear on the returned table switch method handle as well. Any arguments assigned to these parameters will be forwarded, together with the selector value, to the selected method handle when invoking it.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fallback` | [MethodHandle](MethodHandle.md)!: the fallback method handle that is called when the selector is not within the range `[0, N)`. |
| `targets` | [MethodHandle](MethodHandle.md)!: array of target method handles. |

| Return ||
|-----------------------------------------------------------------------------------------------|---------------------------------|
| [MethodHandle](MethodHandle.md)! | the table switch method handle. |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if `fallback`, the `targets` array, or any any of the elements of the `targets` array are `null`. |
| `java.lang.IllegalArgumentException` | if the `targets` array is empty, if the leading parameter of the fallback handle or any of the target handles is not `int`, or if the types of the fallback handle and all of target handles are not the same. |

### throwException

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun throwException(
    returnType: Class<*>!, 
    exType: Class<out Throwable!>!
): MethodHandle!
```

Produces a method handle which will throw exceptions of the given `exType`. The method handle will accept a single argument of `exType`, and immediately throw it as an exception. The method type will nominally specify a return of `returnType`. The return type may be anything convenient: It doesn't matter to the method handle's behavior, since it will never return normally.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `returnType` | [Class](../java.lang/Class.md)\<\*\>!: the return type of the desired method handle |
| `exType` | [Class](../java.lang/Class.md)\<out [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!\>!: the parameter type of the desired method handle |

| Return ||
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| [MethodHandle](MethodHandle.md)! | method handle which can throw the given exceptions |

| Exceptions ||
|----------------------------------|----------------------------|
| `java.lang.NullPointerException` | if either argument is null |

### tryFinally

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun tryFinally(
    target: MethodHandle!, 
    cleanup: MethodHandle!
): MethodHandle!
```

Makes a method handle that adapts a `target` method handle by wrapping it in a `try-finally` block. Another method handle, `cleanup`, represents the functionality of the `finally` block. Any exception thrown during the execution of the `target` handle will be passed to the `cleanup` handle. The exception will be rethrown, unless `cleanup` handle throws an exception first. The value returned from the `cleanup` handle's execution will be the result of the execution of the `try-finally` handle.

The `cleanup` handle will be passed one or two additional leading arguments. The first is the exception thrown during the execution of the `target` handle, or `null` if no exception was thrown. The second is the result of the execution of the `target` handle, or, if it throws an exception, a `null`, zero, or `false` value of the required type is supplied as a placeholder. The second argument is not present if the `target` handle has a `void` return type. (Note that, except for argument type conversions, combinators represent `void` values in parameter lists by omitting the corresponding paradoxical arguments, not by inserting `null` or zero values.)

The `target` and `cleanup` handles must have the same corresponding argument and return types, except that the `cleanup` handle may omit trailing arguments. Also, the `cleanup` handle must have one or two extra leading parameters:

- a `Throwable`, which will carry the exception thrown by the `target` handle (if any); and
- a parameter of the same type as the return type of both `target` and `cleanup`, which will carry the result from the execution of the `target` handle. This parameter is not present if the `target` returns `void`.

The pseudocode for the resulting adapter looks as follows. In the code, `V` represents the result type of the `try/finally` construct; `A`/`a`, the types and values of arguments to the resulting handle consumed by the cleanup; and `B`/`b`, those of arguments to the resulting handle discarded by the cleanup. 

```kotlin
<code>V target(A..., B...);
  V cleanup(Throwable, V, A...);
  V adapter(A... a, B... b) {
    V result = (zero value for V);
    Throwable throwable = null;
    try {
      result = target(a..., b...);
    } catch (Throwable t) {
      throwable = t;
      throw t;
    } finally {
      result = cleanup(throwable, result, a...);
    }
    return result;
  }
  </code>
```

Note that the saved arguments (`a...` in the pseudocode) cannot be modified by execution of the target, and so are passed unchanged from the caller to the cleanup, if it is invoked.

The target and cleanup must return the same type, even if the cleanup always throws. To create such a throwing cleanup, compose the cleanup logic with [throwException](MethodHandles.md)), in order to create a method handle of the correct return type.

Note that `tryFinally` never converts exceptions into normal returns. In rare cases where exceptions must be converted in that way, first wrap the target with [catchException(java.lang.invoke.MethodHandle,java.lang.Class,java.lang.invoke.MethodHandle)](MethodHandles.md)) to capture an outgoing exception, and then wrap with `tryFinally`.

It is recommended that the first parameter type of `cleanup` be declared `Throwable` rather than a narrower subtype. This ensures `cleanup` will always be invoked with whatever exception that `target` throws. Declaring a narrower type may result in a `ClassCastException` being thrown by the `try-finally` handle if the type of the exception thrown by `target` is not assignable to the first parameter type of `cleanup`. Note that various exception types of `VirtualMachineError`, `LinkageError`, and `RuntimeException` can in principle be thrown by almost any kind of Java code, and a finally clause that catches (say) only `IOException` would mask any of the others behind a `ClassCastException`.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `target` | [MethodHandle](MethodHandle.md)!: the handle whose execution is to be wrapped in a `try` block. |
| `cleanup` | [MethodHandle](MethodHandle.md)!: the handle that is invoked in the finally block. |

| Return ||
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [MethodHandle](MethodHandle.md)! | a method handle embodying the `try-finally` block composed of the two arguments. |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if any argument is null |
| `java.lang.IllegalArgumentException` | if `cleanup` does not accept the required leading arguments, or if the method handle types do not match in their return types and their corresponding trailing parameters |

**See Also**

- [java.lang.invoke.MethodHandles#catchException(MethodHandle, Class, MethodHandle)](MethodHandles.md)) 

### varHandleExactInvoker

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun varHandleExactInvoker(
    accessMode: VarHandle.AccessMode!, 
    type: MethodType!
): MethodHandle!
```

Produces a special *invoker method handle* which can be used to invoke a signature-polymorphic access mode method on any VarHandle whose associated access mode type is compatible with the given type. The resulting invoker will have a type which is exactly equal to the desired given type, except that it will accept an additional leading argument of type `VarHandle`.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `accessMode` | [VarHandle.AccessMode](../java/lang/invoke/VarHandle.AccessMode.md)!: the VarHandle access mode |
| `type` | [MethodType](MethodType.md)!: the desired target type |

| Return ||
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [MethodHandle](MethodHandle.md)! | a method handle suitable for invoking an access mode method of any VarHandle whose access mode type is of the given type. |

### varHandleInvoker

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun varHandleInvoker(
    accessMode: VarHandle.AccessMode!, 
    type: MethodType!
): MethodHandle!
```

Produces a special *invoker method handle* which can be used to invoke a signature-polymorphic access mode method on any VarHandle whose associated access mode type is compatible with the given type. The resulting invoker will have a type which is exactly equal to the desired given type, except that it will accept an additional leading argument of type `VarHandle`.

Before invoking its target, if the access mode type differs from the desired given type, the invoker will apply reference casts as necessary and box, unbox, or widen primitive values, as if by [asType](MethodHandle.md)). Similarly, the return value will be converted as necessary.

This method is equivalent to the following code (though it may be more efficient): `publicLookup().findVirtual(VarHandle.class, accessMode.name(), type)`

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `accessMode` | [VarHandle.AccessMode](../java/lang/invoke/VarHandle.AccessMode.md)!: the VarHandle access mode |
| `type` | [MethodType](MethodType.md)!: the desired target type |

| Return ||
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [MethodHandle](MethodHandle.md)! | a method handle suitable for invoking an access mode method of any VarHandle whose access mode type is convertible to the given type. |

### whileLoop

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun whileLoop(
    init: MethodHandle!, 
    pred: MethodHandle!, 
    body: MethodHandle!
): MethodHandle!
```

Constructs a `while` loop from an initializer, a body, and a predicate. This is a convenience wrapper for the [generic loop combinator](MethodHandles.md)).

The `pred` handle describes the loop condition; and `body`, its body. The loop resulting from this method will, in each iteration, first evaluate the predicate and then execute its body (if the predicate evaluates to `true`). The loop will terminate once the predicate evaluates to `false` (the body will not be executed in this case).

The `init` handle describes the initial value of an additional optional loop-local variable. In each iteration, this loop-local variable, if present, will be passed to the `body` and updated with the value returned from its invocation. The result of loop execution will be the final value of the additional loop-local variable (if present).

The following rules hold for these argument handles:

- The `body` handle must not be `null`; its type must be of the form `(V A...)V`, where `V` is non-`void`, or else `(A...)void`. (In the `void` case, we assign the type `void` to the name `V`, and we will write `(V A...)V` with the understanding that a `void` type `V` is quietly dropped from the parameter list, leaving `(A...)V`.)
- The parameter list `(V A...)` of the body is called the *internal parameter list*. It will constrain the parameter lists of the other loop parts.
- If the iteration variable type `V` is dropped from the internal parameter list, the resulting shorter list `(A...)` is called the *external parameter list*.
- The body return type `V`, if non-`void`, determines the type of an additional state variable of the loop. The body must both accept and return a value of this type `V`.
- If `init` is non-`null`, it must have return type `V`. Its parameter list (of some [form `(A*)`](MethodHandles.md)) must be [effectively identical](MethodHandles.md) to the external parameter list `(A...)`.
- If `init` is `null`, the loop variable will be initialized to its [default value](MethodHandles.md)).
- The `pred` handle must not be `null`. It must have `boolean` as its return type. Its parameter list (either empty or of the form `(V A*)`) must be effectively identical to the internal parameter list.

The resulting loop handle's result type and parameter signature are determined as follows:

- The loop handle's result type is the result type `V` of the body.
- The loop handle's parameter types are the types `(A...)`, from the external parameter list.

Here is pseudocode for the resulting loop handle. In the code, `V`/`v` represent the type / value of the sole loop variable as well as the result type of the loop; and `A`/`a`, that of the argument passed to the loop. 

```kotlin
<code>V init(A...);
  boolean pred(V, A...);
  V body(V, A...);
  V whileLoop(A... a...) {
    V v = init(a...);
    while (pred(v, a...)) {
      v = body(v, a...);
    }
    return v;
  }
  </code>
```

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `init` | [MethodHandle](MethodHandle.md)!: optional initializer, providing the initial value of the loop variable. May be `null`, implying a default initial value. See above for other constraints. |
| `pred` | [MethodHandle](MethodHandle.md)!: condition for the loop, which may not be `null`. Its result type must be `boolean`. See above for other constraints. |
| `body` | [MethodHandle](MethodHandle.md)!: body of the loop, which may not be `null`. It controls the loop parameters and result type. See above for other constraints. |
| --- | --- |

| Return ||
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [MethodHandle](MethodHandle.md)! | a method handle implementing the `while` loop as described by the arguments. |

| Exceptions ||
|--------------------------------------|----------------------------------------------|
| `java.lang.IllegalArgumentException` | if the rules for the arguments are violated. |
| `java.lang.NullPointerException` | if `pred` or `body` are `null`. |

**See Also**

- [#loop(MethodHandle[][])](https://developer.android.com/reference/kotlin/java/lang/invoke/MethodHandles#loop(kotlin.Array))
- [#doWhileLoop(MethodHandle, MethodHandle, MethodHandle)](MethodHandles.md)) 

### zero

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun zero(type: Class<*>!): MethodHandle!
```

Produces a constant method handle of the requested return type which returns the default value for that type every time it is invoked. The resulting constant method handle will have no side effects.

The returned method handle is equivalent to `empty(methodType(type))`. It is also equivalent to `explicitCastArguments(constant(Object.class, null), methodType(type))`, since `explicitCastArguments` converts `null` to default values.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `type` | [Class](../java.lang/Class.md)\<\*\>!: the expected return type of the desired method handle |

| Return ||
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [MethodHandle](MethodHandle.md)! | a constant method handle that takes no arguments and returns the default value of the given type (or void, if the type is void) |

| Exceptions ||
|----------------------------------|-------------------------|
| `java.lang.NullPointerException` | if the argument is null |

**See Also**

- [java.lang.invoke.MethodHandles#constant](MethodHandles.md))
- [java.lang.invoke.MethodHandles#empty](MethodHandles.md))
- [java.lang.invoke.MethodHandles#explicitCastArguments](MethodHandles.md))
