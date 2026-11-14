# MethodHandleInfo

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MethodHandleInfo

```
interface MethodHandleInfo
```

| [java.lang.invoke.MethodHandleInfo](MethodHandleInfo.md) |

A symbolic reference obtained by cracking a direct method handle into its consitutent symbolic parts. To crack a direct method handle, call [Lookup.revealDirect](../java/lang/invoke/MethodHandles.Lookup.md)).

# Direct Method Handles

A*direct method handle* represents a method, constructor, or field without any intervening argument bindings or other transformations. The method, constructor, or field referred to by a direct method handle is called its*underlying member* . Direct method handles may be obtained in any of these ways:

- By executing an`ldc`instruction on a`CONSTANT_MethodHandle`constant. (See the Java Virtual Machine Specification, sections 4.4.8 and 5.4.3.)
- By calling one of the [Lookup Factory Methods](../java/lang/invoke/MethodHandles.Lookup.md), such as [Lookup.findVirtual](../java/lang/invoke/MethodHandles.Lookup.md)), to resolve a symbolic reference into a method handle. A symbolic reference consists of a class, name string, and type.
- By calling the factory method [Lookup.unreflect](../java/lang/invoke/MethodHandles.Lookup.md))or [Lookup.unreflectSpecial](../java/lang/invoke/MethodHandles.Lookup.md))to convert a [Method](../java.lang.reflect/Method.md) into a method handle.
- By calling the factory method [Lookup.unreflectConstructor](../java/lang/invoke/MethodHandles.Lookup.md))to convert a [Constructor](../java.lang.reflect/Constructor.md) into a method handle.
- By calling the factory method [Lookup.unreflectGetter](../java/lang/invoke/MethodHandles.Lookup.md))or [Lookup.unreflectSetter](../java/lang/invoke/MethodHandles.Lookup.md))to convert a [Field](../java.lang.reflect/Field.md) into a method handle.

# Restrictions on Cracking

Given a suitable`Lookup`object, it is possible to crack any direct method handle to recover a symbolic reference for the underlying method, constructor, or field. Cracking must be done via a`Lookup`object equivalent to that which created the target method handle, or which has enough access permissions to recreate an equivalent method handle.

<br />

If the underlying method is [caller sensitive](../java/lang/invoke/MethodHandles.Lookup.md), the direct method handle will have been "bound" to a particular caller class, the [lookup class](../java/lang/invoke/MethodHandles.Lookup.md))of the lookup object used to create it. Cracking this method handle with a different lookup class will fail even if the underlying method is public (like`Class.forName`).

The requirement of lookup object matching provides a "fast fail" behavior for programs which may otherwise trust erroneous revelation of a method handle with symbolic information (or caller binding) from an unexpected scope. Use [java.lang.invoke.MethodHandles#reflectAs](MethodHandles.md))to override this limitation.

# Reference kinds

The [Lookup Factory Methods](../java/lang/invoke/MethodHandles.Lookup.md) correspond to all major use cases for methods, constructors, and fields. These use cases may be distinguished using small integers as follows:

| reference kind | descriptive name | scope | member | behavior |
|----------------|------------------------|----------------------|---------------------|----------------------|
| `1` | `REF_getField` | `class` | `FT f;` | `(T) this.f;` |
| `2` | `REF_getStatic` | `class`or`interface` | `static` `FT f;` | `(T) C.f;` |
| `3` | `REF_putField` | `class` | `FT f;` | `this.f = x;` |
| --- | --- | --- | --- | --- |
| `4` | `REF_putStatic` | `class` | `static` `FT f;` | `C.f = arg;` |
| `5` | `REF_invokeVirtual` | `class` | `T m(A*);` | `(T) this.m(arg*);` |
| `6` | `REF_invokeStatic` | `class`or`interface` | `static` `T m(A*);` | `(T) C.m(arg*);` |
| --- | --- | --- | --- | --- |
| `7` | `REF_invokeSpecial` | `class`or`interface` | `T m(A*);` | `(T) super.m(arg*);` |
| `8` | `REF_newInvokeSpecial` | `class` | `C(A*);` | `new C(arg*);` |
| `9` | `REF_invokeInterface` | `interface` | `T m(A*);` | `(T) this.m(arg*);` |
| --- | --- | --- | --- | --- |

## Summary

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REF_getField](MethodHandleInfo.md) A direct method handle reference kind, as defined in the [table above](MethodHandleInfo.md). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REF_getStatic](MethodHandleInfo.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REF_invokeInterface](MethodHandleInfo.md) <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REF_invokeSpecial](MethodHandleInfo.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REF_invokeStatic](MethodHandleInfo.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REF_invokeVirtual](MethodHandleInfo.md) <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REF_newInvokeSpecial](MethodHandleInfo.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REF_putField](MethodHandleInfo.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REF_putStatic](MethodHandleInfo.md) <br /> |
| --- | --- |

| Public methods ||
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Class](../java.lang/Class.md)\<\*\>! | [getDeclaringClass](MethodHandleInfo.md))`()` Returns the class in which the cracked method handle's underlying member was defined. |
| abstract [MethodType](MethodType.md)! | [getMethodType](MethodHandleInfo.md))`()` Returns the nominal type of the cracked symbolic reference, expressed as a method type. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getModifiers](MethodHandleInfo.md))`()` Returns the access modifiers of the underlying member. |
| --- | --- |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getName](MethodHandleInfo.md))`()` Returns the name of the cracked method handle's underlying member. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getReferenceKind](MethodHandleInfo.md))`()` Returns the reference kind of the cracked method handle, which in turn determines whether the method handle's underlying member was a constructor, method, or field. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isVarArgs](MethodHandleInfo.md))`()` Determines if the underlying member was a variable arity method or constructor. |
| --- | --- |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [refKindIsField](MethodHandleInfo.md))`(`refKind:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [refKindIsValid](MethodHandleInfo.md))`(`refKind:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [refKindName](MethodHandleInfo.md))`(`refKind:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [referenceKindToString](MethodHandleInfo.md))`(`referenceKind:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the descriptive name of the given reference kind, as defined in the [table above](MethodHandleInfo.md). |
| abstractT | [reflectAs](MethodHandleInfo.md))`(`expected:` ` [Class](../java.lang/Class.md)<T>!`, `lookup:` ` [MethodHandles.Lookup](../java/lang/invoke/MethodHandles.Lookup.md)!`)` Reflects the underlying member as a method, constructor, or field object. |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toString](MethodHandleInfo.md))`(`kind:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `defc:` ` [Class](../java.lang/Class.md)<*>!`, `name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `type:` ` [MethodType](MethodType.md)!`)` Returns a string representation for a`MethodHandleInfo`, given the four parts of its symbolic reference. |
| --- | --- |

## Constants

### REF_getField

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REF_getField: Int
```

A direct method handle reference kind, as defined in the [table above](MethodHandleInfo.md). 

 Value: 1

### REF_getStatic

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REF_getStatic: Int
```  

 Value: 2

### REF_invokeInterface

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REF_invokeInterface: Int
```  

 Value: 9

### REF_invokeSpecial

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REF_invokeSpecial: Int
```  

 Value: 7

### REF_invokeStatic

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REF_invokeStatic: Int
```  

 Value: 6

### REF_invokeVirtual

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REF_invokeVirtual: Int
```  

 Value: 5

### REF_newInvokeSpecial

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REF_newInvokeSpecial: Int
```  

 Value: 8

### REF_putField

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REF_putField: Int
```  

 Value: 3

### REF_putStatic

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REF_putStatic: Int
```  

 Value: 4

## Public methods

### getDeclaringClass

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getDeclaringClass(): Class<*>!
```

Returns the class in which the cracked method handle's underlying member was defined.

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------|
| [Class](../java.lang/Class.md)<*>! | the declaring class of the underlying member |

### getMethodType

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getMethodType(): MethodType!
```

Returns the nominal type of the cracked symbolic reference, expressed as a method type. If the reference is to a constructor, the return type will be`void`. If it is to a non-static method, the method type will not mention the`this`parameter. If it is to a field and the requested access is to read the field, the method type will have no parameters and return the field type. If it is to a field and the requested access is to write the field, the method type will have one parameter of the field type and return`void`.

Note that original direct method handle may include a leading`this`parameter, or (in the case of a constructor) will replace the`void`return type with the constructed class. The nominal type does not include any`this`parameter, and (in the case of a constructor) will return`void`.

| Return ||
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [MethodType](MethodType.md)! | the type of the underlying member, expressed as a method type |

### getModifiers

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getModifiers(): Int
```

Returns the access modifiers of the underlying member.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the Java language modifiers for underlying member, or -1 if the member cannot be accessed |

**See Also**

- [java.lang.reflect.Modifier](../java.lang.reflect/Modifier.md)
- [#reflectAs](MethodHandleInfo.md)) 

### getName

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getName(): String!
```

Returns the name of the cracked method handle's underlying member. This is`"<init>"`if the underlying member was a constructor, else it is a simple method name or field name.

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the simple name of the underlying member |

### getReferenceKind

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getReferenceKind(): Int
```

Returns the reference kind of the cracked method handle, which in turn determines whether the method handle's underlying member was a constructor, method, or field. See the [table above](MethodHandleInfo.md) for definitions.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the integer code for the kind of reference used to access the underlying member |

### isVarArgs

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isVarArgs(): Boolean
```

Determines if the underlying member was a variable arity method or constructor. Such members are represented by method handles that are varargs collectors.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if and only if the underlying member was declared with variable arity. |

### refKindIsField

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun refKindIsField(refKind: Int): Boolean
```

**Deprecated:** *This internal method was accidentally added to API 26 and must not be used. No replacement is available but it is possible to replicate using information from the [table above](MethodHandleInfo.md), e.g.`refKind >= 1 && refKind <= 4`. There are no guarantees that this logic will work if future versions extend the table.* 

### refKindIsValid

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun refKindIsValid(refKind: Int): Boolean
```

**Deprecated:** *This internal method was accidentally added to API 26 and must not be used. No replacement is available but it is possible to replicate using information from the [table above](MethodHandleInfo.md), e.g.`refKind >= 1 && refKind <= 9`. There are no guarantees that this logic will work if future versions extend the table.* 

### refKindName

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun refKindName(refKind: Int): String!
```

**Deprecated:** *This internal method was accidentally added to API 26 and must not be used. Use [MethodHandleInfo.referenceKindToString(int)](MethodHandleInfo.md))instead.* 

### referenceKindToString

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun referenceKindToString(referenceKind: Int): String!
```

Returns the descriptive name of the given reference kind, as defined in the [table above](MethodHandleInfo.md). The conventional prefix "REF_" is omitted.

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `referenceKind` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):an integer code for a kind of reference used to access a class member |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | a mixed-case string such as`"getField"` |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the argument is not a valid [reference kind number](MethodHandleInfo.md) |

### reflectAs

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <T : Member!> reflectAs(
    expected: Class<T>!, 
    lookup: MethodHandles.Lookup!
): T
```

Reflects the underlying member as a method, constructor, or field object. If the underlying member is public, it is reflected as if by`getMethod`,`getConstructor`, or`getField`. Otherwise, it is reflected as if by`getDeclaredMethod`,`getDeclaredConstructor`, or`getDeclaredField`. The underlying member must be accessible to the given lookup object.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | the desired type of the result, either [Member](../java.lang.reflect/Member.md) or a subtype |
| `expected` | [Class](../java.lang/Class.md)\<T\>!:a class object representing the desired result type`T` |
| `lookup` | [MethodHandles.Lookup](../java/lang/invoke/MethodHandles.Lookup.md)!:the lookup object that created this MethodHandleInfo, or one with equivalent access privileges |
| --- | --- |

| Return ||
|---|---------------------------------------------------------|
| T | a reference to the method, constructor, or field object |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the member is not of the expected type |
| `java.lang.NullPointerException` | if either argument is`null` |
| `java.lang.IllegalArgumentException` | if the underlying member is not accessible to the given lookup object |
| --- | --- |

### toString

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun toString(
    kind: Int, 
    defc: Class<*>!, 
    name: String!, 
    type: MethodType!
): String!
```

Returns a string representation for a`MethodHandleInfo`, given the four parts of its symbolic reference. This is defined to be of the form`"RK C.N:MT"`, where`RK`is the [reference kind string](MethodHandleInfo.md))for`kind`,`C`is the [name](../java.lang/Class.md))of`defc``N`is the`name`, and`MT`is the`type`. These four values may be obtained from the [reference kind](MethodHandleInfo.md)), [declaring class](MethodHandleInfo.md)), [member name](MethodHandleInfo.md)), and [method type](MethodHandleInfo.md))of a`MethodHandleInfo`object.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `kind` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the [reference kind](MethodHandleInfo.md))part of the symbolic reference |
| `defc` | [Class](../java.lang/Class.md)\<\*\>!:the [declaring class](MethodHandleInfo.md))part of the symbolic reference |
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the [member name](MethodHandleInfo.md))part of the symbolic reference |
| --- | --- |
| `type` | [MethodType](MethodType.md)!:the [method type](MethodHandleInfo.md))part of the symbolic reference |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | a string of the form`"RK C.N:MT"` |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the first argument is not a valid [reference kind number](MethodHandleInfo.md) |
| `java.lang.NullPointerException` | if any reference argument is`null` |
