# VarHandle

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# VarHandle

```
abstract class VarHandle
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.lang.invoke.VarHandle](VarHandle.md) |

A VarHandle is a dynamically strongly typed reference to a variable, or to a parametrically-defined family of variables, including static fields, non-static fields, array elements, or components of an off-heap data structure. Access to such variables is supported under various*access modes*, including plain read/write access, volatile read/write access, and compare-and-set.

VarHandles are immutable and have no visible state. VarHandles cannot be subclassed by the user.

A VarHandle has:

- a [variable type](VarHandle.md))T, the type of every variable referenced by this VarHandle; and
- a list of [coordinate types](VarHandle.md))`CT1, CT2, ..., CTn`, the types of*coordinate expressions*that jointly locate a variable referenced by this VarHandle.

Variable and coordinate types may be primitive or reference, and are represented by`Class`objects. The list of coordinate types may be empty.

Factory methods that produce or [lookup](../java/lang/invoke/MethodHandles.Lookup.md) VarHandle instances document the supported variable type and the list of coordinate types.

Each access mode is associated with one*access mode method* , a [signature polymorphic](MethodHandle.md) method named for the access mode. When an access mode method is invoked on a VarHandle instance, the initial arguments to the invocation are coordinate expressions that indicate in precisely which object the variable is to be accessed. Trailing arguments to the invocation represent values of importance to the access mode. For example, the various compare-and-set or compare-and-exchange access modes require two trailing arguments for the variable's expected value and new value.

The arity and types of arguments to the invocation of an access mode method are not checked statically. Instead, each access mode method specifies an [access mode type](VarHandle.md)), represented as an instance of [MethodType](MethodType.md), that serves as a kind of method signature against which the arguments are checked dynamically. An access mode type gives formal parameter types in terms of the coordinate types of a VarHandle instance and the types for values of importance to the access mode. An access mode type also gives a return type, often in terms of the variable type of a VarHandle instance. When an access mode method is invoked on a VarHandle instance, the symbolic type descriptor at the call site, the run time types of arguments to the invocation, and the run time type of the return value, must [match](VarHandle.md) the types given in the access mode type. A runtime exception will be thrown if the match fails. For example, the access mode method [compareAndSet](VarHandle.md))specifies that if its receiver is a VarHandle instance with coordinate types`CT1, ..., CTn`and variable type`T`, then its access mode type is`(CT1 c1, ..., CTn cn, T expectedValue, T newValue)boolean`. Suppose that a VarHandle instance can access array elements, and that its coordinate types are`String[]`and`int`while its variable type is`String`. The access mode type for`compareAndSet`on this VarHandle instance would be`(String[] c1, int c2, String expectedValue, String newValue)boolean`. Such a VarHandle instance may be produced by the [array factory method](MethodHandles.md))and access array elements as follows: 

```kotlin
<code>String[] sa = ...
  VarHandle avh = MethodHandles.arrayElementVarHandle(String[].class);
  boolean r = avh.compareAndSet(sa, 10, "expected", "new");
  </code>
```

Access modes control atomicity and consistency properties.*Plain* read (`get`) and write (`set`) accesses are guaranteed to be bitwise atomic only for references and for primitive values of at most 32 bits, and impose no observable ordering constraints with respect to threads other than the executing thread.*Opaque* operations are bitwise atomic and coherently ordered with respect to accesses to the same variable. In addition to obeying Opaque properties,*Acquire* mode reads and their subsequent accesses are ordered after matching*Release* mode writes and their previous accesses. In addition to obeying Acquire and Release properties, all*Volatile*operations are totally ordered with respect to each other.

Access modes are grouped into the following categories:

- read access modes that get the value of a variable under specified memory ordering effects. The set of corresponding access mode methods belonging to this group consists of the methods [get](VarHandle.md)), [getVolatile](VarHandle.md)), [getAcquire](VarHandle.md)), [getOpaque](VarHandle.md)).
- write access modes that set the value of a variable under specified memory ordering effects. The set of corresponding access mode methods belonging to this group consists of the methods [set](VarHandle.md)), [setVolatile](VarHandle.md)), [setRelease](VarHandle.md)), [setOpaque](VarHandle.md)).
- atomic update access modes that, for example, atomically compare and set the value of a variable under specified memory ordering effects. The set of corresponding access mode methods belonging to this group consists of the methods [compareAndSet](VarHandle.md)), [weakCompareAndSetPlain](VarHandle.md)), [weakCompareAndSet](VarHandle.md)), [weakCompareAndSetAcquire](VarHandle.md)), [weakCompareAndSetRelease](VarHandle.md)), [compareAndExchangeAcquire](VarHandle.md)), [compareAndExchange](VarHandle.md)), [compareAndExchangeRelease](VarHandle.md)), [getAndSet](VarHandle.md)), [getAndSetAcquire](VarHandle.md)), [getAndSetRelease](VarHandle.md)).
- numeric atomic update access modes that, for example, atomically get and set with addition the value of a variable under specified memory ordering effects. The set of corresponding access mode methods belonging to this group consists of the methods [getAndAdd](VarHandle.md)), [getAndAddAcquire](VarHandle.md)), [getAndAddRelease](VarHandle.md)),
- bitwise atomic update access modes that, for example, atomically get and bitwise OR the value of a variable under specified memory ordering effects. The set of corresponding access mode methods belonging to this group consists of the methods [getAndBitwiseOr](VarHandle.md)), [getAndBitwiseOrAcquire](VarHandle.md)), [getAndBitwiseOrRelease](VarHandle.md)), [getAndBitwiseAnd](VarHandle.md)), [getAndBitwiseAndAcquire](VarHandle.md)), [getAndBitwiseAndRelease](VarHandle.md)), [getAndBitwiseXor](VarHandle.md)), [getAndBitwiseXorAcquire](VarHandle.md)), [getAndBitwiseXorRelease](VarHandle.md)).

Factory methods that produce or [lookup](../java/lang/invoke/MethodHandles.Lookup.md) VarHandle instances document the set of access modes that are supported, which may also include documenting restrictions based on the variable type and whether a variable is read-only. If an access mode is not supported then the corresponding access mode method will on invocation throw an`UnsupportedOperationException`. Factory methods should document any additional undeclared exceptions that may be thrown by access mode methods. The [get](VarHandle.md))access mode is supported for all VarHandle instances and the corresponding method never throws`UnsupportedOperationException`. If a VarHandle references a read-only variable (for example a`final`field) then write, atomic update, numeric atomic update, and bitwise atomic update access modes are not supported and corresponding methods throw`UnsupportedOperationException`. Read/write access modes (if supported), with the exception of`get`and`set`, provide atomic access for reference types and all primitive types. Unless stated otherwise in the documentation of a factory method, the access modes`get`and`set`(if supported) provide atomic access for reference types and all primitives types, with the exception of`long`and`double`on 32-bit platforms.

Access modes will override any memory ordering effects specified at the declaration site of a variable. For example, a VarHandle accessing a field using the`get`access mode will access the field as specified*by its access mode* even if that field is declared`volatile`. When mixed access is performed extreme care should be taken since the Java Memory Model may permit surprising results.

In addition to supporting access to variables under various access modes, a set of static methods, referred to as memory fence methods, is also provided for fine-grained control of memory ordering. The Java Language Specification permits other threads to observe operations as if they were executed in orders different than are apparent in program source code, subject to constraints arising, for example, from the use of locks,`volatile`fields or VarHandles. The static methods, [fullFence](VarHandle.md)), [acquireFence](VarHandle.md)), [releaseFence](VarHandle.md)), [loadLoadFence](VarHandle.md))and [storeStoreFence](VarHandle.md)), can also be used to impose constraints. Their specifications, as is the case for certain access modes, are phrased in terms of the lack of "reorderings" -- observable ordering effects that might otherwise occur if the fence was not present. More precise phrasing of the specification of access mode methods and memory fence methods may accompany future updates of the Java Language Specification.

# Compiling invocation of access mode methods

A Java method call expression naming an access mode method can invoke a VarHandle from Java source code. From the viewpoint of source code, these methods can take any arguments and their polymorphic result (if expressed) can be cast to any return type. Formally this is accomplished by giving the access mode methods variable arity`Object`arguments and`Object`return types (if the return type is polymorphic), but they have an additional quality called*signature polymorphism* which connects this freedom of invocation directly to the JVM execution stack.

As is usual with virtual methods, source-level calls to access mode methods compile to an`invokevirtual`instruction. More unusually, the compiler must record the actual argument types, and may not perform method invocation conversions on the arguments. Instead, it must generate instructions to push them on the stack according to their own unconverted types. The VarHandle object itself will be pushed on the stack before the arguments. The compiler then generates an`invokevirtual`instruction that invokes the access mode method with a symbolic type descriptor which describes the argument and return types.

To issue a complete symbolic type descriptor, the compiler must also determine the return type (if polymorphic). This is based on a cast on the method invocation expression, if there is one, or else`Object`if the invocation is an expression, or else`void`if the invocation is a statement. The cast may be to a primitive type (but not`void`).

As a corner case, an uncasted`null`argument is given a symbolic type descriptor of`java.lang.Void`. The ambiguity with the type`Void`is harmless, since there are no references of type`Void`except the null reference.

# Performing invocation of access mode methods

The first time an`invokevirtual`instruction is executed it is linked by symbolically resolving the names in the instruction and verifying that the method call is statically legal. This also holds for calls to access mode methods. In this case, the symbolic type descriptor emitted by the compiler is checked for correct syntax, and names it contains are resolved. Thus, an`invokevirtual`instruction which invokes an access mode method will always link, as long as the symbolic type descriptor is syntactically well-formed and the types exist.

When the`invokevirtual`is executed after linking, the receiving VarHandle's access mode type is first checked by the JVM to ensure that it matches the symbolic type descriptor. If the type match fails, it means that the access mode method which the caller is invoking is not present on the individual VarHandle being invoked.

Invocation of an access mode method behaves as if an invocation of [MethodHandle.invoke](MethodHandle.md)), where the receiving method handle accepts the VarHandle instance as the leading argument. More specifically, the following, where`{access-mode}`corresponds to the access mode method name: 

```kotlin
<code>VarHandle vh = ..
  R r = (R) vh.{access-mode}(p1, p2, ..., pN);
  </code>
```
behaves as if: 

```kotlin
<code>VarHandle vh = ..
  VarHandle.AccessMode am = VarHandle.AccessMode.valueFromMethodName("{access-mode}");
  MethodHandle mh = MethodHandles.varHandleExactInvoker(
                        am,
                        vh.accessModeType(am));
 
  R r = (R) mh.invoke(vh, p1, p2, ..., pN)
  </code>
```
(modulo access mode methods do not declare throwing of`Throwable`). This is equivalent to: 

```kotlin
<code>MethodHandle mh = MethodHandles.lookup().findVirtual(
                        VarHandle.class,
                        "{access-mode}",
                        MethodType.methodType(R, p1, p2, ..., pN));
 
  R r = (R) mh.invokeExact(vh, p1, p2, ..., pN)
  </code>
```
where the desired method type is the symbolic type descriptor and a [MethodHandle.invokeExact](MethodHandle.md))is performed, since before invocation of the target, the handle will apply reference casts as necessary and box, unbox, or widen primitive values, as if by [asType](MethodHandle.md))(see also [MethodHandles.varHandleInvoker](MethodHandles.md))). More concisely, such behaviour is equivalent to: 

```kotlin
<code>VarHandle vh = ..
  VarHandle.AccessMode am = VarHandle.AccessMode.valueFromMethodName("{access-mode}");
  MethodHandle mh = vh.toMethodHandle(am);
 
  R r = (R) mh.invoke(p1, p2, ..., pN)
  </code>
```
Where, in this case, the method handle is bound to the VarHandle instance.

# Invocation checking

In typical programs, VarHandle access mode type matching will usually succeed. But if a match fails, the JVM will throw a [WrongMethodTypeException](WrongMethodTypeException.md).

Thus, an access mode type mismatch which might show up as a linkage error in a statically typed program can show up as a dynamic`WrongMethodTypeException`in a program which uses VarHandles.

Because access mode types contain "live"`Class`objects, method type matching takes into account both type names and class loaders. Thus, even if a VarHandle`VH`is created in one class loader`L1`and used in another`L2`, VarHandle access mode method calls are type-safe, because the caller's symbolic type descriptor, as resolved in`L2`, is matched against the original callee method's symbolic type descriptor, as resolved in`L1`. The resolution in`L1`happens when`VH`is created and its access mode types are assigned, while the resolution in`L2`happens when the`invokevirtual`instruction is linked.

Apart from type descriptor checks, a VarHandles's capability to access it's variables is unrestricted. If a VarHandle is formed on a non-public variable by a class that has access to that variable, the resulting VarHandle can be used in any place by any caller who receives a reference to it.

Unlike with the Core Reflection API, where access is checked every time a reflective method is invoked, VarHandle access checking is performed [when the VarHandle is created](../java/lang/invoke/MethodHandles.Lookup.md). Thus, VarHandles to non-public variables, or to variables in non-public classes, should generally be kept secret. They should not be passed to untrusted code unless their use from the untrusted code would be harmless.

# VarHandle creation

Java code can create a VarHandle that directly accesses any field that is accessible to that code. This is done via a reflective, capability-based API called [MethodHandles.Lookup](../java/lang/invoke/MethodHandles.Lookup.md). For example, a VarHandle for a non-static field can be obtained from [Lookup.findVarHandle](../java/lang/invoke/MethodHandles.Lookup.md)). There is also a conversion method from Core Reflection API objects, [Lookup.unreflectVarHandle](../java/lang/invoke/MethodHandles.Lookup.md)).

Access to protected field members is restricted to receivers only of the accessing class, or one of its subclasses, and the accessing class must in turn be a subclass (or package sibling) of the protected member's defining class. If a VarHandle refers to a protected non-static field of a declaring class outside the current package, the receiver argument will be narrowed to the type of the accessing class.

# Interoperation between VarHandles and the Core Reflection API

Using factory methods in the [Lookup](../java/lang/invoke/MethodHandles.Lookup.md) API, any field represented by a Core Reflection API object can be converted to a behaviorally equivalent VarHandle. For example, a reflective [Field](../java.lang.reflect/Field.md) can be converted to a VarHandle using [Lookup.unreflectVarHandle](../java/lang/invoke/MethodHandles.Lookup.md)). The resulting VarHandles generally provide more direct and efficient access to the underlying fields.

As a special case, when the Core Reflection API is used to view the signature polymorphic access mode methods in this class, they appear as ordinary non-polymorphic methods. Their reflective appearance, as viewed by [Class.getDeclaredMethod](../java.lang/Class.md)), is unaffected by their special status in this API. For example, java.lang.reflect.Method#getModifiers will report exactly those modifier bits required for any similarly declared method, including in this case`native`and`varargs`bits.

As with any reflected method, these methods (when reflected) may be invoked directly via [java.lang.reflect.Method.invoke](../java.lang.reflect/Method.md)), via JNI, or indirectly via [Lookup.unreflect](../java/lang/invoke/MethodHandles.Lookup.md)). However, such reflective calls do not result in access mode method invocations. Such a call, if passed the required argument (a single one, of type`Object[]`), will ignore the argument and will throw an`UnsupportedOperationException`.

Since`invokevirtual`instructions can natively invoke VarHandle access mode methods under any symbolic type descriptor, this reflective view conflicts with the normal presentation of these methods via bytecodes. Thus, these native methods, when reflectively viewed by`Class.getDeclaredMethod`, may be regarded as placeholders only.

In order to obtain an invoker method for a particular access mode type, use [java.lang.invoke.MethodHandles#varHandleExactInvoker](MethodHandles.md))or [java.lang.invoke.MethodHandles#varHandleInvoker](MethodHandles.md)). The [Lookup.findVirtual](../java/lang/invoke/MethodHandles.Lookup.md))API is also able to return a method handle to call an access mode method for any specified access mode type and is equivalent in behaviour to [java.lang.invoke.MethodHandles#varHandleInvoker](MethodHandles.md)).

# Interoperation between VarHandles and Java generics

A VarHandle can be obtained for a variable, such as a field, which is declared with Java generic types. As with the Core Reflection API, the VarHandle's variable type will be constructed from the erasure of the source-level type. When a VarHandle access mode method is invoked, the types of its arguments or the return value cast type may be generic types or type instances. If this occurs, the compiler will replace those types by their erasures when it constructs the symbolic type descriptor for the`invokevirtual`instruction.

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [AccessMode](../java/lang/invoke/VarHandle.AccessMode.md) The set of access modes that specify how a variable, referenced by a VarHandle, is accessed. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MethodType](MethodType.md)! | [accessModeType](VarHandle.md))`(`accessMode:` ` [VarHandle.AccessMode](../java/lang/invoke/VarHandle.AccessMode.md)!`)` Obtains the access mode type for this VarHandle and a given access mode. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [acquireFence](VarHandle.md))`()` Ensures that loads before the fence will not be reordered with loads and stores after the fence. |
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [compareAndExchange](VarHandle.md))`(`vararg` `args:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Atomically sets the value of a variable to the`newValue`with the memory semantics of [setVolatile](VarHandle.md))if the variable's current value, referred to as the*witness value* ,`==`the`expectedValue`, as accessed with the memory semantics of [getVolatile](VarHandle.md)). |
| --- | --- |
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [compareAndExchangeAcquire](VarHandle.md))`(`vararg` `args:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Atomically sets the value of a variable to the`newValue`with the memory semantics of [set](VarHandle.md))if the variable's current value, referred to as the*witness value* ,`==`the`expectedValue`, as accessed with the memory semantics of [getAcquire](VarHandle.md)). |
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [compareAndExchangeRelease](VarHandle.md))`(`vararg` `args:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Atomically sets the value of a variable to the`newValue`with the memory semantics of [setRelease](VarHandle.md))if the variable's current value, referred to as the*witness value* ,`==`the`expectedValue`, as accessed with the memory semantics of [get](VarHandle.md)). |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [compareAndSet](VarHandle.md))`(`vararg` `args:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Atomically sets the value of a variable to the`newValue`with the memory semantics of [setVolatile](VarHandle.md))if the variable's current value, referred to as the*witness value* ,`==`the`expectedValue`, as accessed with the memory semantics of [getVolatile](VarHandle.md)). |
| --- | --- |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Class](../java.lang/Class.md)\<\*\>!\>! | [coordinateTypes](VarHandle.md))`()` Returns the coordinate types for this VarHandle. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [fullFence](VarHandle.md))`()` Ensures that loads and stores before the fence will not be reordered with loads and stores after the fence. |
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [get](VarHandle.md))`(`vararg` `args:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Returns the value of a variable, with memory semantics of reading as if the variable was declared non-`volatile`. |
| --- | --- |
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getAcquire](VarHandle.md))`(`vararg` `args:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Returns the value of a variable, and ensures that subsequent loads and stores are not reordered before this access. |
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getAndAdd](VarHandle.md))`(`vararg` `args:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Atomically adds the`value`to the current value of a variable with the memory semantics of [setVolatile](VarHandle.md)), and returns the variable's previous value, as accessed with the memory semantics of [getVolatile](VarHandle.md)). |
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getAndAddAcquire](VarHandle.md))`(`vararg` `args:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Atomically adds the`value`to the current value of a variable with the memory semantics of [set](VarHandle.md)), and returns the variable's previous value, as accessed with the memory semantics of [getAcquire](VarHandle.md)). |
| --- | --- |
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getAndAddRelease](VarHandle.md))`(`vararg` `args:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Atomically adds the`value`to the current value of a variable with the memory semantics of [setRelease](VarHandle.md)), and returns the variable's previous value, as accessed with the memory semantics of [get](VarHandle.md)). |
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getAndBitwiseAnd](VarHandle.md))`(`vararg` `args:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Atomically sets the value of a variable to the result of bitwise AND between the variable's current value and the`mask`with the memory semantics of [setVolatile](VarHandle.md))and returns the variable's previous value, as accessed with the memory semantics of [getVolatile](VarHandle.md)). |
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getAndBitwiseAndAcquire](VarHandle.md))`(`vararg` `args:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Atomically sets the value of a variable to the result of bitwise AND between the variable's current value and the`mask`with the memory semantics of [set](VarHandle.md))and returns the variable's previous value, as accessed with the memory semantics of [getAcquire](VarHandle.md)). |
| --- | --- |
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getAndBitwiseAndRelease](VarHandle.md))`(`vararg` `args:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Atomically sets the value of a variable to the result of bitwise AND between the variable's current value and the`mask`with the memory semantics of [setRelease](VarHandle.md))and returns the variable's previous value, as accessed with the memory semantics of [get](VarHandle.md)). |
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getAndBitwiseOr](VarHandle.md))`(`vararg` `args:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Atomically sets the value of a variable to the result of bitwise OR between the variable's current value and the`mask`with the memory semantics of [setVolatile](VarHandle.md))and returns the variable's previous value, as accessed with the memory semantics of [getVolatile](VarHandle.md)). |
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getAndBitwiseOrAcquire](VarHandle.md))`(`vararg` `args:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Atomically sets the value of a variable to the result of bitwise OR between the variable's current value and the`mask`with the memory semantics of [set](VarHandle.md))and returns the variable's previous value, as accessed with the memory semantics of [getAcquire](VarHandle.md)). |
| --- | --- |
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getAndBitwiseOrRelease](VarHandle.md))`(`vararg` `args:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Atomically sets the value of a variable to the result of bitwise OR between the variable's current value and the`mask`with the memory semantics of [setRelease](VarHandle.md))and returns the variable's previous value, as accessed with the memory semantics of [get](VarHandle.md)). |
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getAndBitwiseXor](VarHandle.md))`(`vararg` `args:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Atomically sets the value of a variable to the result of bitwise XOR between the variable's current value and the`mask`with the memory semantics of [setVolatile](VarHandle.md))and returns the variable's previous value, as accessed with the memory semantics of [getVolatile](VarHandle.md)). |
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getAndBitwiseXorAcquire](VarHandle.md))`(`vararg` `args:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Atomically sets the value of a variable to the result of bitwise XOR between the variable's current value and the`mask`with the memory semantics of [set](VarHandle.md))and returns the variable's previous value, as accessed with the memory semantics of [getAcquire](VarHandle.md)). |
| --- | --- |
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getAndBitwiseXorRelease](VarHandle.md))`(`vararg` `args:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Atomically sets the value of a variable to the result of bitwise XOR between the variable's current value and the`mask`with the memory semantics of [setRelease](VarHandle.md))and returns the variable's previous value, as accessed with the memory semantics of [get](VarHandle.md)). |
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getAndSet](VarHandle.md))`(`vararg` `args:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Atomically sets the value of a variable to the`newValue`with the memory semantics of [setVolatile](VarHandle.md))and returns the variable's previous value, as accessed with the memory semantics of [getVolatile](VarHandle.md)). |
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getAndSetAcquire](VarHandle.md))`(`vararg` `args:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Atomically sets the value of a variable to the`newValue`with the memory semantics of [set](VarHandle.md))and returns the variable's previous value, as accessed with the memory semantics of [getAcquire](VarHandle.md)). |
| --- | --- |
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getAndSetRelease](VarHandle.md))`(`vararg` `args:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Atomically sets the value of a variable to the`newValue`with the memory semantics of [setRelease](VarHandle.md))and returns the variable's previous value, as accessed with the memory semantics of [get](VarHandle.md)). |
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getOpaque](VarHandle.md))`(`vararg` `args:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Returns the value of a variable, accessed in program order, but with no assurance of memory ordering effects with respect to other threads. |
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [getVolatile](VarHandle.md))`(`vararg` `args:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Returns the value of a variable, with memory semantics of reading as if the variable was declared`volatile`. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAccessModeSupported](VarHandle.md))`(`accessMode:` ` [VarHandle.AccessMode](../java/lang/invoke/VarHandle.AccessMode.md)!`)` Returns`true`if the given access mode is supported, otherwise`false`. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [loadLoadFence](VarHandle.md))`()` Ensures that loads before the fence will not be reordered with loads after the fence. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [releaseFence](VarHandle.md))`()` Ensures that loads and stores before the fence will not be reordered with stores after the fence. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [set](VarHandle.md))`(`vararg` `args:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Sets the value of a variable to the`newValue`, with memory semantics of setting as if the variable was declared non-`volatile`and non-`final`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOpaque](VarHandle.md))`(`vararg` `args:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Sets the value of a variable to the`newValue`, in program order, but with no assurance of memory ordering effects with respect to other threads. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRelease](VarHandle.md))`(`vararg` `args:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Sets the value of a variable to the`newValue`, and ensures that prior loads and stores are not reordered after this access. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setVolatile](VarHandle.md))`(`vararg` `args:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Sets the value of a variable to the`newValue`, with memory semantics of setting as if the variable was declared`volatile`. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [storeStoreFence](VarHandle.md))`()` Ensures that stores before the fence will not be reordered with stores after the fence. |
| [MethodHandle](MethodHandle.md)! | [toMethodHandle](VarHandle.md))`(`accessMode:` ` [VarHandle.AccessMode](../java/lang/invoke/VarHandle.AccessMode.md)!`)` Obtains a method handle bound to this VarHandle and the given access mode. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](VarHandle.md))`()` Returns a compact textual description of this [VarHandle](VarHandle.md), including the type of variable described, and a description of its coordinates. |
| [Class](../java.lang/Class.md)\<\*\>! | [varType](VarHandle.md))`()` Returns the variable type of variables referenced by this VarHandle. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [weakCompareAndSet](VarHandle.md))`(`vararg` `args:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Possibly atomically sets the value of a variable to the`newValue`with the memory semantics of [setVolatile](VarHandle.md))if the variable's current value, referred to as the*witness value* ,`==`the`expectedValue`, as accessed with the memory semantics of [getVolatile](VarHandle.md)). |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [weakCompareAndSetAcquire](VarHandle.md))`(`vararg` `args:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Possibly atomically sets the value of a variable to the`newValue`with the semantics of [set](VarHandle.md))if the variable's current value, referred to as the*witness value* ,`==`the`expectedValue`, as accessed with the memory semantics of [getAcquire](VarHandle.md)). |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [weakCompareAndSetPlain](VarHandle.md))`(`vararg` `args:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Possibly atomically sets the value of a variable to the`newValue`with the semantics of [set](VarHandle.md))if the variable's current value, referred to as the*witness value* ,`==`the`expectedValue`, as accessed with the memory semantics of [get](VarHandle.md)). |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [weakCompareAndSetRelease](VarHandle.md))`(`vararg` `args:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Possibly atomically sets the value of a variable to the`newValue`with the semantics of [setRelease](VarHandle.md))if the variable's current value, referred to as the*witness value* ,`==`the`expectedValue`, as accessed with the memory semantics of [get](VarHandle.md)). |
| --- | --- |

## Public methods

### accessModeType

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun accessModeType(accessMode: VarHandle.AccessMode!): MethodType!
```

Obtains the access mode type for this VarHandle and a given access mode.

The access mode type's parameter types will consist of a prefix that is the coordinate types of this VarHandle followed by further types as defined by the access mode method. The access mode type's return type is defined by the return type of the access mode method.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `accessMode` | [VarHandle.AccessMode](../java/lang/invoke/VarHandle.AccessMode.md)!:the access mode, corresponding to the signature-polymorphic method of the same name |

| Return ||
|-------------------------------------------------------------------------------------------|------------------------------------------------|
| [MethodType](MethodType.md)! | the access mode type for the given access mode |

### acquireFence

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun acquireFence(): Unit
```

Ensures that loads before the fence will not be reordered with loads and stores after the fence. 

### compareAndExchange

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun compareAndExchange(vararg args: Any!): Any!
```

Atomically sets the value of a variable to the`newValue`with the memory semantics of [setVolatile](VarHandle.md))if the variable's current value, referred to as the*witness value* ,`==`the`expectedValue`, as accessed with the memory semantics of [getVolatile](VarHandle.md)).

The method signature is of the form`(CT1 ct1, ..., CTn ctn, T expectedValue, T newValue)T`.

The symbolic type descriptor at the call site of`compareAndExchange`must match the access mode type that is the result of calling`accessModeType(VarHandle.AccessMode.COMPARE_AND_EXCHANGE)`on this VarHandle.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `args` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the signature-polymorphic parameter list of the form`(CT1 ct1, ..., CTn ctn, T expectedValue, T newValue)`, statically represented using varargs. |

| Return ||
|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | the signature-polymorphic result that is the witness value, which will be the same as the`expectedValue`if successful , statically represented using`Object`. |

| Exceptions ||
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the access mode is unsupported for this VarHandle. |
| `java.lang.invoke.WrongMethodTypeException` | if the access mode type is not compatible with the caller's symbolic type descriptor. |
| `java.lang.ClassCastException` | if the access mode type is compatible with the caller's symbolic type descriptor, but a reference cast fails. |
| --- | --- |

**See Also**

- [#setVolatile(Object...)](VarHandle.md))
- [#getVolatile(Object...)](VarHandle.md)) 

### compareAndExchangeAcquire

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun compareAndExchangeAcquire(vararg args: Any!): Any!
```

Atomically sets the value of a variable to the`newValue`with the memory semantics of [set](VarHandle.md))if the variable's current value, referred to as the*witness value* ,`==`the`expectedValue`, as accessed with the memory semantics of [getAcquire](VarHandle.md)).

The method signature is of the form`(CT1 ct1, ..., CTn ctn, T expectedValue, T newValue)T`.

The symbolic type descriptor at the call site of`compareAndExchangeAcquire`must match the access mode type that is the result of calling`accessModeType(VarHandle.AccessMode.COMPARE_AND_EXCHANGE_ACQUIRE)`on this VarHandle.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `args` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the signature-polymorphic parameter list of the form`(CT1 ct1, ..., CTn ctn, T expectedValue, T newValue)`, statically represented using varargs. |

| Return ||
|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | the signature-polymorphic result that is the witness value, which will be the same as the`expectedValue`if successful , statically represented using`Object`. |

| Exceptions ||
|---------------------------------------------|----------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the access mode is unsupported for this VarHandle. |
| `java.lang.invoke.WrongMethodTypeException` | if the access mode type does not match the caller's symbolic type descriptor. |
| `java.lang.ClassCastException` | if the access mode type matches the caller's symbolic type descriptor, but a reference cast fails. |
| --- | --- |

**See Also**

- [#set(Object...)](VarHandle.md))
- [#getAcquire(Object...)](VarHandle.md)) 

### compareAndExchangeRelease

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun compareAndExchangeRelease(vararg args: Any!): Any!
```

Atomically sets the value of a variable to the`newValue`with the memory semantics of [setRelease](VarHandle.md))if the variable's current value, referred to as the*witness value* ,`==`the`expectedValue`, as accessed with the memory semantics of [get](VarHandle.md)).

The method signature is of the form`(CT1 ct1, ..., CTn ctn, T expectedValue, T newValue)T`.

The symbolic type descriptor at the call site of`compareAndExchangeRelease`must match the access mode type that is the result of calling`accessModeType(VarHandle.AccessMode.COMPARE_AND_EXCHANGE_RELEASE)`on this VarHandle.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `args` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the signature-polymorphic parameter list of the form`(CT1 ct1, ..., CTn ctn, T expectedValue, T newValue)`, statically represented using varargs. |

| Return ||
|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | the signature-polymorphic result that is the witness value, which will be the same as the`expectedValue`if successful , statically represented using`Object`. |

| Exceptions ||
|---------------------------------------------|----------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the access mode is unsupported for this VarHandle. |
| `java.lang.invoke.WrongMethodTypeException` | if the access mode type does not match the caller's symbolic type descriptor. |
| `java.lang.ClassCastException` | if the access mode type matches the caller's symbolic type descriptor, but a reference cast fails. |
| --- | --- |

**See Also**

- [#setRelease(Object...)](VarHandle.md))
- [#get(Object...)](VarHandle.md)) 

### compareAndSet

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun compareAndSet(vararg args: Any!): Boolean
```

Atomically sets the value of a variable to the`newValue`with the memory semantics of [setVolatile](VarHandle.md))if the variable's current value, referred to as the*witness value* ,`==`the`expectedValue`, as accessed with the memory semantics of [getVolatile](VarHandle.md)).

The method signature is of the form`(CT1 ct1, ..., CTn ctn, T expectedValue, T newValue)boolean`.

The symbolic type descriptor at the call site of`compareAndSet`must match the access mode type that is the result of calling`accessModeType(VarHandle.AccessMode.COMPARE_AND_SET)`on this VarHandle.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `args` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the signature-polymorphic parameter list of the form`(CT1 ct1, ..., CTn ctn, T expectedValue, T newValue)`, statically represented using varargs. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if successful, otherwise`false`if the witness value was not the same as the`expectedValue`. |

| Exceptions ||
|---------------------------------------------|----------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the access mode is unsupported for this VarHandle. |
| `java.lang.invoke.WrongMethodTypeException` | if the access mode type does not match the caller's symbolic type descriptor. |
| `java.lang.ClassCastException` | if the access mode type matches the caller's symbolic type descriptor, but a reference cast fails. |
| --- | --- |

**See Also**

- [#setVolatile(Object...)](VarHandle.md))
- [#getVolatile(Object...)](VarHandle.md)) 

### coordinateTypes

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun coordinateTypes(): MutableList<Class<*>!>!
```

Returns the coordinate types for this VarHandle.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Class](../java.lang/Class.md)<*>!>! | the coordinate types for this VarHandle. The returned list is unmodifiable |

### fullFence

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun fullFence(): Unit
```

Ensures that loads and stores before the fence will not be reordered with loads and stores after the fence. 

### get

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun get(vararg args: Any!): Any!
```

Returns the value of a variable, with memory semantics of reading as if the variable was declared non-`volatile`. Commonly referred to as plain read access.

The method signature is of the form`(CT1 ct1, ..., CTn ctn)T`.

The symbolic type descriptor at the call site of`get`must match the access mode type that is the result of calling`accessModeType(VarHandle.AccessMode.GET)`on this VarHandle.

This access mode is supported by all VarHandle instances and never throws`UnsupportedOperationException`.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `args` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the signature-polymorphic parameter list of the form`(CT1 ct1, ..., CTn)`, statically represented using varargs. |

| Return ||
|-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | the signature-polymorphic result that is the value of the variable , statically represented using`Object`. |

| Exceptions ||
|---------------------------------------------|----------------------------------------------------------------------------------------------------|
| `java.lang.invoke.WrongMethodTypeException` | if the access mode type does not match the caller's symbolic type descriptor. |
| `java.lang.ClassCastException` | if the access mode type matches the caller's symbolic type descriptor, but a reference cast fails. |

### getAcquire

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAcquire(vararg args: Any!): Any!
```

Returns the value of a variable, and ensures that subsequent loads and stores are not reordered before this access.

The method signature is of the form`(CT1 ct1, ..., CTn ctn)T`.

The symbolic type descriptor at the call site of`getAcquire`must match the access mode type that is the result of calling`accessModeType(VarHandle.AccessMode.GET_ACQUIRE)`on this VarHandle.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `args` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the signature-polymorphic parameter list of the form`(CT1 ct1, ..., CTn ctn)`, statically represented using varargs. |

| Return ||
|-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | the signature-polymorphic result that is the value of the variable , statically represented using`Object`. |

| Exceptions ||
|---------------------------------------------|----------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the access mode is unsupported for this VarHandle. |
| `java.lang.invoke.WrongMethodTypeException` | if the access mode type does not match the caller's symbolic type descriptor. |
| `java.lang.ClassCastException` | if the access mode type matches the caller's symbolic type descriptor, but a reference cast fails. |
| --- | --- |

### getAndAdd

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAndAdd(vararg args: Any!): Any!
```

Atomically adds the`value`to the current value of a variable with the memory semantics of [setVolatile](VarHandle.md)), and returns the variable's previous value, as accessed with the memory semantics of [getVolatile](VarHandle.md)).

The method signature is of the form`(CT1 ct1, ..., CTn ctn, T value)T`.

The symbolic type descriptor at the call site of`getAndAdd`must match the access mode type that is the result of calling`accessModeType(VarHandle.AccessMode.GET_AND_ADD)`on this VarHandle.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `args` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the signature-polymorphic parameter list of the form`(CT1 ct1, ..., CTn ctn, T value)`, statically represented using varargs. |

| Return ||
|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | the signature-polymorphic result that is the previous value of the variable , statically represented using`Object`. |

| Exceptions ||
|---------------------------------------------|----------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the access mode is unsupported for this VarHandle. |
| `java.lang.invoke.WrongMethodTypeException` | if the access mode type does not match the caller's symbolic type descriptor. |
| `java.lang.ClassCastException` | if the access mode type matches the caller's symbolic type descriptor, but a reference cast fails. |
| --- | --- |

**See Also**

- [#setVolatile(Object...)](VarHandle.md))
- [#getVolatile(Object...)](VarHandle.md)) 

### getAndAddAcquire

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAndAddAcquire(vararg args: Any!): Any!
```

Atomically adds the`value`to the current value of a variable with the memory semantics of [set](VarHandle.md)), and returns the variable's previous value, as accessed with the memory semantics of [getAcquire](VarHandle.md)).

The method signature is of the form`(CT1 ct1, ..., CTn ctn, T value)T`.

The symbolic type descriptor at the call site of`getAndAddAcquire`must match the access mode type that is the result of calling`accessModeType(VarHandle.AccessMode.GET_AND_ADD_ACQUIRE)`on this VarHandle.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `args` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the signature-polymorphic parameter list of the form`(CT1 ct1, ..., CTn ctn, T value)`, statically represented using varargs. |

| Return ||
|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | the signature-polymorphic result that is the previous value of the variable , statically represented using`Object`. |

| Exceptions ||
|---------------------------------------------|----------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the access mode is unsupported for this VarHandle. |
| `java.lang.invoke.WrongMethodTypeException` | if the access mode type does not match the caller's symbolic type descriptor. |
| `java.lang.ClassCastException` | if the access mode type matches the caller's symbolic type descriptor, but a reference cast fails. |
| --- | --- |

**See Also**

- [#setVolatile(Object...)](VarHandle.md))
- [#getVolatile(Object...)](VarHandle.md)) 

### getAndAddRelease

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAndAddRelease(vararg args: Any!): Any!
```

Atomically adds the`value`to the current value of a variable with the memory semantics of [setRelease](VarHandle.md)), and returns the variable's previous value, as accessed with the memory semantics of [get](VarHandle.md)).

The method signature is of the form`(CT1 ct1, ..., CTn ctn, T value)T`.

The symbolic type descriptor at the call site of`getAndAddRelease`must match the access mode type that is the result of calling`accessModeType(VarHandle.AccessMode.GET_AND_ADD_RELEASE)`on this VarHandle.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `args` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the signature-polymorphic parameter list of the form`(CT1 ct1, ..., CTn ctn, T value)`, statically represented using varargs. |

| Return ||
|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | the signature-polymorphic result that is the previous value of the variable , statically represented using`Object`. |

| Exceptions ||
|---------------------------------------------|----------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the access mode is unsupported for this VarHandle. |
| `java.lang.invoke.WrongMethodTypeException` | if the access mode type does not match the caller's symbolic type descriptor. |
| `java.lang.ClassCastException` | if the access mode type matches the caller's symbolic type descriptor, but a reference cast fails. |
| --- | --- |

**See Also**

- [#setVolatile(Object...)](VarHandle.md))
- [#getVolatile(Object...)](VarHandle.md)) 

### getAndBitwiseAnd

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAndBitwiseAnd(vararg args: Any!): Any!
```

Atomically sets the value of a variable to the result of bitwise AND between the variable's current value and the`mask`with the memory semantics of [setVolatile](VarHandle.md))and returns the variable's previous value, as accessed with the memory semantics of [getVolatile](VarHandle.md)).

If the variable type is the non-integral`boolean`type then a logical AND is performed instead of a bitwise AND.

The method signature is of the form`(CT1 ct1, ..., CTn ctn, T mask)T`.

The symbolic type descriptor at the call site of`getAndBitwiseAnd`must match the access mode type that is the result of calling`accessModeType(VarHandle.AccessMode.GET_AND_BITWISE_AND)`on this VarHandle.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `args` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the signature-polymorphic parameter list of the form`(CT1 ct1, ..., CTn ctn, T mask)`, statically represented using varargs. |

| Return ||
|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | the signature-polymorphic result that is the previous value of the variable , statically represented using`Object`. |

| Exceptions ||
|---------------------------------------------|----------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the access mode is unsupported for this VarHandle. |
| `java.lang.invoke.WrongMethodTypeException` | if the access mode type does not match the caller's symbolic type descriptor. |
| `java.lang.ClassCastException` | if the access mode type matches the caller's symbolic type descriptor, but a reference cast fails. |
| --- | --- |

**See Also**

- [#setVolatile(Object...)](VarHandle.md))
- [#getVolatile(Object...)](VarHandle.md)) 

### getAndBitwiseAndAcquire

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAndBitwiseAndAcquire(vararg args: Any!): Any!
```

Atomically sets the value of a variable to the result of bitwise AND between the variable's current value and the`mask`with the memory semantics of [set](VarHandle.md))and returns the variable's previous value, as accessed with the memory semantics of [getAcquire](VarHandle.md)).

If the variable type is the non-integral`boolean`type then a logical AND is performed instead of a bitwise AND.

The method signature is of the form`(CT1 ct1, ..., CTn ctn, T mask)T`.

The symbolic type descriptor at the call site of`getAndBitwiseAndAcquire`must match the access mode type that is the result of calling`accessModeType(VarHandle.AccessMode.GET_AND_BITWISE_AND_ACQUIRE)`on this VarHandle.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `args` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the signature-polymorphic parameter list of the form`(CT1 ct1, ..., CTn ctn, T mask)`, statically represented using varargs. |

| Return ||
|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | the signature-polymorphic result that is the previous value of the variable , statically represented using`Object`. |

| Exceptions ||
|---------------------------------------------|----------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the access mode is unsupported for this VarHandle. |
| `java.lang.invoke.WrongMethodTypeException` | if the access mode type does not match the caller's symbolic type descriptor. |
| `java.lang.ClassCastException` | if the access mode type matches the caller's symbolic type descriptor, but a reference cast fails. |
| --- | --- |

**See Also**

- [#set(Object...)](VarHandle.md))
- [#getAcquire(Object...)](VarHandle.md)) 

### getAndBitwiseAndRelease

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAndBitwiseAndRelease(vararg args: Any!): Any!
```

Atomically sets the value of a variable to the result of bitwise AND between the variable's current value and the`mask`with the memory semantics of [setRelease](VarHandle.md))and returns the variable's previous value, as accessed with the memory semantics of [get](VarHandle.md)).

If the variable type is the non-integral`boolean`type then a logical AND is performed instead of a bitwise AND.

The method signature is of the form`(CT1 ct1, ..., CTn ctn, T mask)T`.

The symbolic type descriptor at the call site of`getAndBitwiseAndRelease`must match the access mode type that is the result of calling`accessModeType(VarHandle.AccessMode.GET_AND_BITWISE_AND_RELEASE)`on this VarHandle.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `args` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the signature-polymorphic parameter list of the form`(CT1 ct1, ..., CTn ctn, T mask)`, statically represented using varargs. |

| Return ||
|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | the signature-polymorphic result that is the previous value of the variable , statically represented using`Object`. |

| Exceptions ||
|---------------------------------------------|----------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the access mode is unsupported for this VarHandle. |
| `java.lang.invoke.WrongMethodTypeException` | if the access mode type does not match the caller's symbolic type descriptor. |
| `java.lang.ClassCastException` | if the access mode type matches the caller's symbolic type descriptor, but a reference cast fails. |
| --- | --- |

**See Also**

- [#setRelease(Object...)](VarHandle.md))
- [#get(Object...)](VarHandle.md)) 

### getAndBitwiseOr

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAndBitwiseOr(vararg args: Any!): Any!
```

Atomically sets the value of a variable to the result of bitwise OR between the variable's current value and the`mask`with the memory semantics of [setVolatile](VarHandle.md))and returns the variable's previous value, as accessed with the memory semantics of [getVolatile](VarHandle.md)).

If the variable type is the non-integral`boolean`type then a logical OR is performed instead of a bitwise OR.

The method signature is of the form`(CT1 ct1, ..., CTn ctn, T mask)T`.

The symbolic type descriptor at the call site of`getAndBitwiseOr`must match the access mode type that is the result of calling`accessModeType(VarHandle.AccessMode.GET_AND_BITWISE_OR)`on this VarHandle.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `args` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the signature-polymorphic parameter list of the form`(CT1 ct1, ..., CTn ctn, T mask)`, statically represented using varargs. |

| Return ||
|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | the signature-polymorphic result that is the previous value of the variable , statically represented using`Object`. |

| Exceptions ||
|---------------------------------------------|----------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the access mode is unsupported for this VarHandle. |
| `java.lang.invoke.WrongMethodTypeException` | if the access mode type does not match the caller's symbolic type descriptor. |
| `java.lang.ClassCastException` | if the access mode type matches the caller's symbolic type descriptor, but a reference cast fails. |
| --- | --- |

**See Also**

- [#setVolatile(Object...)](VarHandle.md))
- [#getVolatile(Object...)](VarHandle.md)) 

### getAndBitwiseOrAcquire

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAndBitwiseOrAcquire(vararg args: Any!): Any!
```

Atomically sets the value of a variable to the result of bitwise OR between the variable's current value and the`mask`with the memory semantics of [set](VarHandle.md))and returns the variable's previous value, as accessed with the memory semantics of [getAcquire](VarHandle.md)).

If the variable type is the non-integral`boolean`type then a logical OR is performed instead of a bitwise OR.

The method signature is of the form`(CT1 ct1, ..., CTn ctn, T mask)T`.

The symbolic type descriptor at the call site of`getAndBitwiseOrAcquire`must match the access mode type that is the result of calling`accessModeType(VarHandle.AccessMode.GET_AND_BITWISE_OR_ACQUIRE)`on this VarHandle.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `args` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the signature-polymorphic parameter list of the form`(CT1 ct1, ..., CTn ctn, T mask)`, statically represented using varargs. |

| Return ||
|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | the signature-polymorphic result that is the previous value of the variable , statically represented using`Object`. |

| Exceptions ||
|---------------------------------------------|----------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the access mode is unsupported for this VarHandle. |
| `java.lang.invoke.WrongMethodTypeException` | if the access mode type does not match the caller's symbolic type descriptor. |
| `java.lang.ClassCastException` | if the access mode type matches the caller's symbolic type descriptor, but a reference cast fails. |
| --- | --- |

**See Also**

- [#set(Object...)](VarHandle.md))
- [#getAcquire(Object...)](VarHandle.md)) 

### getAndBitwiseOrRelease

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAndBitwiseOrRelease(vararg args: Any!): Any!
```

Atomically sets the value of a variable to the result of bitwise OR between the variable's current value and the`mask`with the memory semantics of [setRelease](VarHandle.md))and returns the variable's previous value, as accessed with the memory semantics of [get](VarHandle.md)).

If the variable type is the non-integral`boolean`type then a logical OR is performed instead of a bitwise OR.

The method signature is of the form`(CT1 ct1, ..., CTn ctn, T mask)T`.

The symbolic type descriptor at the call site of`getAndBitwiseOrRelease`must match the access mode type that is the result of calling`accessModeType(VarHandle.AccessMode.GET_AND_BITWISE_OR_RELEASE)`on this VarHandle.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `args` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the signature-polymorphic parameter list of the form`(CT1 ct1, ..., CTn ctn, T mask)`, statically represented using varargs. |

| Return ||
|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | the signature-polymorphic result that is the previous value of the variable , statically represented using`Object`. |

| Exceptions ||
|---------------------------------------------|----------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the access mode is unsupported for this VarHandle. |
| `java.lang.invoke.WrongMethodTypeException` | if the access mode type does not match the caller's symbolic type descriptor. |
| `java.lang.ClassCastException` | if the access mode type matches the caller's symbolic type descriptor, but a reference cast fails. |
| --- | --- |

**See Also**

- [#setRelease(Object...)](VarHandle.md))
- [#get(Object...)](VarHandle.md)) 

### getAndBitwiseXor

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAndBitwiseXor(vararg args: Any!): Any!
```

Atomically sets the value of a variable to the result of bitwise XOR between the variable's current value and the`mask`with the memory semantics of [setVolatile](VarHandle.md))and returns the variable's previous value, as accessed with the memory semantics of [getVolatile](VarHandle.md)).

If the variable type is the non-integral`boolean`type then a logical XOR is performed instead of a bitwise XOR.

The method signature is of the form`(CT1 ct1, ..., CTn ctn, T mask)T`.

The symbolic type descriptor at the call site of`getAndBitwiseXor`must match the access mode type that is the result of calling`accessModeType(VarHandle.AccessMode.GET_AND_BITWISE_XOR)`on this VarHandle.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `args` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the signature-polymorphic parameter list of the form`(CT1 ct1, ..., CTn ctn, T mask)`, statically represented using varargs. |

| Return ||
|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | the signature-polymorphic result that is the previous value of the variable , statically represented using`Object`. |

| Exceptions ||
|---------------------------------------------|----------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the access mode is unsupported for this VarHandle. |
| `java.lang.invoke.WrongMethodTypeException` | if the access mode type does not match the caller's symbolic type descriptor. |
| `java.lang.ClassCastException` | if the access mode type matches the caller's symbolic type descriptor, but a reference cast fails. |
| --- | --- |

**See Also**

- [#setVolatile(Object...)](VarHandle.md))
- [#getVolatile(Object...)](VarHandle.md)) 

### getAndBitwiseXorAcquire

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAndBitwiseXorAcquire(vararg args: Any!): Any!
```

Atomically sets the value of a variable to the result of bitwise XOR between the variable's current value and the`mask`with the memory semantics of [set](VarHandle.md))and returns the variable's previous value, as accessed with the memory semantics of [getAcquire](VarHandle.md)).

If the variable type is the non-integral`boolean`type then a logical XOR is performed instead of a bitwise XOR.

The method signature is of the form`(CT1 ct1, ..., CTn ctn, T mask)T`.

The symbolic type descriptor at the call site of`getAndBitwiseXorAcquire`must match the access mode type that is the result of calling`accessModeType(VarHandle.AccessMode.GET_AND_BITWISE_XOR_ACQUIRE)`on this VarHandle.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `args` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the signature-polymorphic parameter list of the form`(CT1 ct1, ..., CTn ctn, T mask)`, statically represented using varargs. |

| Return ||
|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | the signature-polymorphic result that is the previous value of the variable , statically represented using`Object`. |

| Exceptions ||
|---------------------------------------------|----------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the access mode is unsupported for this VarHandle. |
| `java.lang.invoke.WrongMethodTypeException` | if the access mode type does not match the caller's symbolic type descriptor. |
| `java.lang.ClassCastException` | if the access mode type matches the caller's symbolic type descriptor, but a reference cast fails. |
| --- | --- |

**See Also**

- [#set(Object...)](VarHandle.md))
- [#getAcquire(Object...)](VarHandle.md)) 

### getAndBitwiseXorRelease

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAndBitwiseXorRelease(vararg args: Any!): Any!
```

Atomically sets the value of a variable to the result of bitwise XOR between the variable's current value and the`mask`with the memory semantics of [setRelease](VarHandle.md))and returns the variable's previous value, as accessed with the memory semantics of [get](VarHandle.md)).

If the variable type is the non-integral`boolean`type then a logical XOR is performed instead of a bitwise XOR.

The method signature is of the form`(CT1 ct1, ..., CTn ctn, T mask)T`.

The symbolic type descriptor at the call site of`getAndBitwiseXorRelease`must match the access mode type that is the result of calling`accessModeType(VarHandle.AccessMode.GET_AND_BITWISE_XOR_RELEASE)`on this VarHandle.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `args` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the signature-polymorphic parameter list of the form`(CT1 ct1, ..., CTn ctn, T mask)`, statically represented using varargs. |

| Return ||
|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | the signature-polymorphic result that is the previous value of the variable , statically represented using`Object`. |

| Exceptions ||
|---------------------------------------------|----------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the access mode is unsupported for this VarHandle. |
| `java.lang.invoke.WrongMethodTypeException` | if the access mode type does not match the caller's symbolic type descriptor. |
| `java.lang.ClassCastException` | if the access mode type matches the caller's symbolic type descriptor, but a reference cast fails. |
| --- | --- |

**See Also**

- [#setRelease(Object...)](VarHandle.md))
- [#get(Object...)](VarHandle.md)) 

### getAndSet

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAndSet(vararg args: Any!): Any!
```

Atomically sets the value of a variable to the`newValue`with the memory semantics of [setVolatile](VarHandle.md))and returns the variable's previous value, as accessed with the memory semantics of [getVolatile](VarHandle.md)).

The method signature is of the form`(CT1 ct1, ..., CTn ctn, T newValue)T`.

The symbolic type descriptor at the call site of`getAndSet`must match the access mode type that is the result of calling`accessModeType(VarHandle.AccessMode.GET_AND_SET)`on this VarHandle.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `args` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the signature-polymorphic parameter list of the form`(CT1 ct1, ..., CTn ctn, T newValue)`, statically represented using varargs. |

| Return ||
|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | the signature-polymorphic result that is the previous value of the variable , statically represented using`Object`. |

| Exceptions ||
|---------------------------------------------|----------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the access mode is unsupported for this VarHandle. |
| `java.lang.invoke.WrongMethodTypeException` | if the access mode type does not match the caller's symbolic type descriptor. |
| `java.lang.ClassCastException` | if the access mode type matches the caller's symbolic type descriptor, but a reference cast fails. |
| --- | --- |

**See Also**

- [#setVolatile(Object...)](VarHandle.md))
- [#getVolatile(Object...)](VarHandle.md)) 

### getAndSetAcquire

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAndSetAcquire(vararg args: Any!): Any!
```

Atomically sets the value of a variable to the`newValue`with the memory semantics of [set](VarHandle.md))and returns the variable's previous value, as accessed with the memory semantics of [getAcquire](VarHandle.md)).

The method signature is of the form`(CT1 ct1, ..., CTn ctn, T newValue)T`.

The symbolic type descriptor at the call site of`getAndSetAcquire`must match the access mode type that is the result of calling`accessModeType(VarHandle.AccessMode.GET_AND_SET_ACQUIRE)`on this VarHandle.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `args` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the signature-polymorphic parameter list of the form`(CT1 ct1, ..., CTn ctn, T newValue)`, statically represented using varargs. |

| Return ||
|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | the signature-polymorphic result that is the previous value of the variable , statically represented using`Object`. |

| Exceptions ||
|---------------------------------------------|----------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the access mode is unsupported for this VarHandle. |
| `java.lang.invoke.WrongMethodTypeException` | if the access mode type does not match the caller's symbolic type descriptor. |
| `java.lang.ClassCastException` | if the access mode type matches the caller's symbolic type descriptor, but a reference cast fails. |
| --- | --- |

**See Also**

- [#setVolatile(Object...)](VarHandle.md))
- [#getVolatile(Object...)](VarHandle.md)) 

### getAndSetRelease

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAndSetRelease(vararg args: Any!): Any!
```

Atomically sets the value of a variable to the`newValue`with the memory semantics of [setRelease](VarHandle.md))and returns the variable's previous value, as accessed with the memory semantics of [get](VarHandle.md)).

The method signature is of the form`(CT1 ct1, ..., CTn ctn, T newValue)T`.

The symbolic type descriptor at the call site of`getAndSetRelease`must match the access mode type that is the result of calling`accessModeType(VarHandle.AccessMode.GET_AND_SET_RELEASE)`on this VarHandle.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `args` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the signature-polymorphic parameter list of the form`(CT1 ct1, ..., CTn ctn, T newValue)`, statically represented using varargs. |

| Return ||
|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | the signature-polymorphic result that is the previous value of the variable , statically represented using`Object`. |

| Exceptions ||
|---------------------------------------------|----------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the access mode is unsupported for this VarHandle. |
| `java.lang.invoke.WrongMethodTypeException` | if the access mode type does not match the caller's symbolic type descriptor. |
| `java.lang.ClassCastException` | if the access mode type matches the caller's symbolic type descriptor, but a reference cast fails. |
| --- | --- |

**See Also**

- [#setVolatile(Object...)](VarHandle.md))
- [#getVolatile(Object...)](VarHandle.md)) 

### getOpaque

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getOpaque(vararg args: Any!): Any!
```

Returns the value of a variable, accessed in program order, but with no assurance of memory ordering effects with respect to other threads.

The method signature is of the form`(CT1 ct1, ..., CTn ctn)T`.

The symbolic type descriptor at the call site of`getOpaque`must match the access mode type that is the result of calling`accessModeType(VarHandle.AccessMode.GET_OPAQUE)`on this VarHandle.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `args` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the signature-polymorphic parameter list of the form`(CT1 ct1, ..., CTn ctn)`, statically represented using varargs. |

| Return ||
|-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | the signature-polymorphic result that is the value of the variable , statically represented using`Object`. |

| Exceptions ||
|---------------------------------------------|----------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the access mode is unsupported for this VarHandle. |
| `java.lang.invoke.WrongMethodTypeException` | if the access mode type does not match the caller's symbolic type descriptor. |
| `java.lang.ClassCastException` | if the access mode type matches the caller's symbolic type descriptor, but a reference cast fails. |
| --- | --- |

### getVolatile

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getVolatile(vararg args: Any!): Any!
```

Returns the value of a variable, with memory semantics of reading as if the variable was declared`volatile`.

The method signature is of the form`(CT1 ct1, ..., CTn ctn)T`.

The symbolic type descriptor at the call site of`getVolatile`must match the access mode type that is the result of calling`accessModeType(VarHandle.AccessMode.GET_VOLATILE)`on this VarHandle.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `args` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the signature-polymorphic parameter list of the form`(CT1 ct1, ..., CTn ctn)`, statically represented using varargs. |

| Return ||
|-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | the signature-polymorphic result that is the value of the variable , statically represented using`Object`. |

| Exceptions ||
|---------------------------------------------|----------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the access mode is unsupported for this VarHandle. |
| `java.lang.invoke.WrongMethodTypeException` | if the access mode type does not match the caller's symbolic type descriptor. |
| `java.lang.ClassCastException` | if the access mode type matches the caller's symbolic type descriptor, but a reference cast fails. |
| --- | --- |

### isAccessModeSupported

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isAccessModeSupported(accessMode: VarHandle.AccessMode!): Boolean
```

Returns`true`if the given access mode is supported, otherwise`false`.

The return of a`false`value for a given access mode indicates that an`UnsupportedOperationException`is thrown on invocation of the corresponding access mode method.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `accessMode` | [VarHandle.AccessMode](../java/lang/invoke/VarHandle.AccessMode.md)!:the access mode, corresponding to the signature-polymorphic method of the same name |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the given access mode is supported, otherwise`false`. |

### loadLoadFence

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun loadLoadFence(): Unit
```

Ensures that loads before the fence will not be reordered with loads after the fence. 

### releaseFence

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun releaseFence(): Unit
```

Ensures that loads and stores before the fence will not be reordered with stores after the fence. 

### set

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun set(vararg args: Any!): Unit
```

Sets the value of a variable to the`newValue`, with memory semantics of setting as if the variable was declared non-`volatile`and non-`final`. Commonly referred to as plain write access.

The method signature is of the form`(CT1 ct1, ..., CTn ctn, T newValue)void`

The symbolic type descriptor at the call site of`set`must match the access mode type that is the result of calling`accessModeType(VarHandle.AccessMode.SET)`on this VarHandle.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `args` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the signature-polymorphic parameter list of the form`(CT1 ct1, ..., CTn ctn, T newValue)`, statically represented using varargs. |

| Exceptions ||
|---------------------------------------------|----------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the access mode is unsupported for this VarHandle. |
| `java.lang.invoke.WrongMethodTypeException` | if the access mode type does not match the caller's symbolic type descriptor. |
| `java.lang.ClassCastException` | if the access mode type matches the caller's symbolic type descriptor, but a reference cast fails. |
| --- | --- |

### setOpaque

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setOpaque(vararg args: Any!): Unit
```

Sets the value of a variable to the`newValue`, in program order, but with no assurance of memory ordering effects with respect to other threads.

The method signature is of the form`(CT1 ct1, ..., CTn ctn, T newValue)void`.

The symbolic type descriptor at the call site of`setOpaque`must match the access mode type that is the result of calling`accessModeType(VarHandle.AccessMode.SET_OPAQUE)`on this VarHandle.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `args` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the signature-polymorphic parameter list of the form`(CT1 ct1, ..., CTn ctn, T newValue)`, statically represented using varargs. |

| Exceptions ||
|---------------------------------------------|----------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the access mode is unsupported for this VarHandle. |
| `java.lang.invoke.WrongMethodTypeException` | if the access mode type does not match the caller's symbolic type descriptor. |
| `java.lang.ClassCastException` | if the access mode type matches the caller's symbolic type descriptor, but a reference cast fails. |
| --- | --- |

### setRelease

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setRelease(vararg args: Any!): Unit
```

Sets the value of a variable to the`newValue`, and ensures that prior loads and stores are not reordered after this access.

The method signature is of the form`(CT1 ct1, ..., CTn ctn, T newValue)void`.

The symbolic type descriptor at the call site of`setRelease`must match the access mode type that is the result of calling`accessModeType(VarHandle.AccessMode.SET_RELEASE)`on this VarHandle.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `args` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the signature-polymorphic parameter list of the form`(CT1 ct1, ..., CTn ctn, T newValue)`, statically represented using varargs. |

| Exceptions ||
|---------------------------------------------|----------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the access mode is unsupported for this VarHandle. |
| `java.lang.invoke.WrongMethodTypeException` | if the access mode type does not match the caller's symbolic type descriptor. |
| `java.lang.ClassCastException` | if the access mode type matches the caller's symbolic type descriptor, but a reference cast fails. |
| --- | --- |

### setVolatile

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setVolatile(vararg args: Any!): Unit
```

Sets the value of a variable to the`newValue`, with memory semantics of setting as if the variable was declared`volatile`.

The method signature is of the form`(CT1 ct1, ..., CTn ctn, T newValue)void`.

The symbolic type descriptor at the call site of`setVolatile`must match the access mode type that is the result of calling`accessModeType(VarHandle.AccessMode.SET_VOLATILE)`on this VarHandle.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `args` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the signature-polymorphic parameter list of the form`(CT1 ct1, ..., CTn ctn, T newValue)`, statically represented using varargs. |

| Exceptions ||
|---------------------------------------------|----------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the access mode is unsupported for this VarHandle. |
| `java.lang.invoke.WrongMethodTypeException` | if the access mode type does not match the caller's symbolic type descriptor. |
| `java.lang.ClassCastException` | if the access mode type matches the caller's symbolic type descriptor, but a reference cast fails. |
| --- | --- |

### storeStoreFence

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun storeStoreFence(): Unit
```

Ensures that stores before the fence will not be reordered with stores after the fence. 

### toMethodHandle

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toMethodHandle(accessMode: VarHandle.AccessMode!): MethodHandle!
```

Obtains a method handle bound to this VarHandle and the given access mode.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `accessMode` | [VarHandle.AccessMode](../java/lang/invoke/VarHandle.AccessMode.md)!:the access mode, corresponding to the signature-polymorphic method of the same name |

| Return ||
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [MethodHandle](MethodHandle.md)! | a method handle bound to this VarHandle and the given access mode |

### toString

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Returns a compact textual description of this [VarHandle](VarHandle.md), including the type of variable described, and a description of its coordinates.

| Return ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | A compact textual description of this [VarHandle](VarHandle.md) |

### varType

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun varType(): Class<*>!
```

Returns the variable type of variables referenced by this VarHandle.

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------------|
| [Class](../java.lang/Class.md)<*>! | the variable type of variables referenced by this VarHandle |

### weakCompareAndSet

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun weakCompareAndSet(vararg args: Any!): Boolean
```

Possibly atomically sets the value of a variable to the`newValue`with the memory semantics of [setVolatile](VarHandle.md))if the variable's current value, referred to as the*witness value* ,`==`the`expectedValue`, as accessed with the memory semantics of [getVolatile](VarHandle.md)).

This operation may fail spuriously (typically, due to memory contention) even if the witness value does match the expected value.

The method signature is of the form`(CT1 ct1, ..., CTn ctn, T expectedValue, T newValue)boolean`.

The symbolic type descriptor at the call site of`weakCompareAndSet`must match the access mode type that is the result of calling`accessModeType(VarHandle.AccessMode.WEAK_COMPARE_AND_SET)`on this VarHandle.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `args` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the signature-polymorphic parameter list of the form`(CT1 ct1, ..., CTn ctn, T expectedValue, T newValue)`, statically represented using varargs. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if successful, otherwise`false`if the witness value was not the same as the`expectedValue`or if this operation spuriously failed. |

| Exceptions ||
|---------------------------------------------|----------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the access mode is unsupported for this VarHandle. |
| `java.lang.invoke.WrongMethodTypeException` | if the access mode type does not match the caller's symbolic type descriptor. |
| `java.lang.ClassCastException` | if the access mode type matches the caller's symbolic type descriptor, but a reference cast fails. |
| --- | --- |

**See Also**

- [#setVolatile(Object...)](VarHandle.md))
- [#getVolatile(Object...)](VarHandle.md)) 

### weakCompareAndSetAcquire

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun weakCompareAndSetAcquire(vararg args: Any!): Boolean
```

Possibly atomically sets the value of a variable to the`newValue`with the semantics of [set](VarHandle.md))if the variable's current value, referred to as the*witness value* ,`==`the`expectedValue`, as accessed with the memory semantics of [getAcquire](VarHandle.md)).

This operation may fail spuriously (typically, due to memory contention) even if the witness value does match the expected value.

The method signature is of the form`(CT1 ct1, ..., CTn ctn, T expectedValue, T newValue)boolean`.

The symbolic type descriptor at the call site of`weakCompareAndSetAcquire`must match the access mode type that is the result of calling`accessModeType(VarHandle.AccessMode.WEAK_COMPARE_AND_SET_ACQUIRE)`on this VarHandle.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `args` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the signature-polymorphic parameter list of the form`(CT1 ct1, ..., CTn ctn, T expectedValue, T newValue)`, statically represented using varargs. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if successful, otherwise`false`if the witness value was not the same as the`expectedValue`or if this operation spuriously failed. |

| Exceptions ||
|---------------------------------------------|----------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the access mode is unsupported for this VarHandle. |
| `java.lang.invoke.WrongMethodTypeException` | if the access mode type does not match the caller's symbolic type descriptor. |
| `java.lang.ClassCastException` | if the access mode type matches the caller's symbolic type descriptor, but a reference cast fails. |
| --- | --- |

**See Also**

- [#set(Object...)](VarHandle.md))
- [#getAcquire(Object...)](VarHandle.md)) 

### weakCompareAndSetPlain

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun weakCompareAndSetPlain(vararg args: Any!): Boolean
```

Possibly atomically sets the value of a variable to the`newValue`with the semantics of [set](VarHandle.md))if the variable's current value, referred to as the*witness value* ,`==`the`expectedValue`, as accessed with the memory semantics of [get](VarHandle.md)).

This operation may fail spuriously (typically, due to memory contention) even if the witness value does match the expected value.

The method signature is of the form`(CT1 ct1, ..., CTn ctn, T expectedValue, T newValue)boolean`.

The symbolic type descriptor at the call site of`weakCompareAndSetPlain`must match the access mode type that is the result of calling`accessModeType(VarHandle.AccessMode.WEAK_COMPARE_AND_SET_PLAIN)`on this VarHandle.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `args` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the signature-polymorphic parameter list of the form`(CT1 ct1, ..., CTn ctn, T expectedValue, T newValue)`, statically represented using varargs. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if successful, otherwise`false`if the witness value was not the same as the`expectedValue`or if this operation spuriously failed. |

| Exceptions ||
|---------------------------------------------|----------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the access mode is unsupported for this VarHandle. |
| `java.lang.invoke.WrongMethodTypeException` | if the access mode type does not match the caller's symbolic type descriptor. |
| `java.lang.ClassCastException` | if the access mode type matches the caller's symbolic type descriptor, but a reference cast fails. |
| --- | --- |

**See Also**

- [#set(Object...)](VarHandle.md))
- [#get(Object...)](VarHandle.md)) 

### weakCompareAndSetRelease

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun weakCompareAndSetRelease(vararg args: Any!): Boolean
```

Possibly atomically sets the value of a variable to the`newValue`with the semantics of [setRelease](VarHandle.md))if the variable's current value, referred to as the*witness value* ,`==`the`expectedValue`, as accessed with the memory semantics of [get](VarHandle.md)).

This operation may fail spuriously (typically, due to memory contention) even if the witness value does match the expected value.

The method signature is of the form`(CT1 ct1, ..., CTn ctn, T expectedValue, T newValue)boolean`.

The symbolic type descriptor at the call site of`weakCompareAndSetRelease`must match the access mode type that is the result of calling`accessModeType(VarHandle.AccessMode.WEAK_COMPARE_AND_SET_RELEASE)`on this VarHandle.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `args` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:the signature-polymorphic parameter list of the form`(CT1 ct1, ..., CTn ctn, T expectedValue, T newValue)`, statically represented using varargs. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if successful, otherwise`false`if the witness value was not the same as the`expectedValue`or if this operation spuriously failed. |

| Exceptions ||
|---------------------------------------------|----------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the access mode is unsupported for this VarHandle. |
| `java.lang.invoke.WrongMethodTypeException` | if the access mode type does not match the caller's symbolic type descriptor. |
| `java.lang.ClassCastException` | if the access mode type matches the caller's symbolic type descriptor, but a reference cast fails. |
| --- | --- |

**See Also**

- [#setRelease(Object...)](VarHandle.md))
- [#get(Object...)](VarHandle.md))
