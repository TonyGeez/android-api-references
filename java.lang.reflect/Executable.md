Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Executable

```
abstract class Executable : AccessibleObject, GenericDeclaration, Member
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.lang.reflect.AccessibleObject](AccessibleObject.md) ||
| | ↳ | [java.lang.reflect.Executable](Executable.md) |

| Known Direct Subclasses [Constructor](Constructor.md), [Method](Method.md) |---|---| | [Constructor](Constructor.md) | `Constructor` provides information about, and access to, a single constructor for a class. | | [Method](Method.md) | A `Method` provides information about, and access to, a single method on a class or interface. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A shared superclass for the common functionality of `https://developer.android.com/reference/kotlin/java/lang/reflect/Method` and `https://developer.android.com/reference/kotlin/java/lang/reflect/Constructor`.

## Summary

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/java/lang/reflect/Member` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/lang/reflect/Member#DECLARED:kotlin.Int` Identifies the set of declared members of a class or interface. Inherited members are not included. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/lang/reflect/Member#PUBLIC:kotlin.Int` Identifies the set of all public members of a class or interface, including inherited members. <br /> | ||

| Public methods ||
|---|---|
| open T? | `https://developer.android.com/reference/kotlin/java/lang/reflect/Executable#getAnnotation(java.lang.Class)(annotationClass: https://developer.android.com/reference/kotlin/java/lang/Class.html#<T>)` Returns this element's annotation for the specified type if such an annotation is *present*, else null. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>! | `https://developer.android.com/reference/kotlin/java/lang/reflect/Executable#getAnnotationsByType(java.lang.Class)(annotationClass: https://developer.android.com/reference/kotlin/java/lang/Class.html#<T>)` Returns annotations that are *associated* with this element. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Annotation](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-annotation/index.html)!\> | `https://developer.android.com/reference/kotlin/java/lang/reflect/Executable#getDeclaredAnnotations()()` Returns annotations that are *directly present* on this element. |
| --- | --- |
| abstract [Class](../java.lang/Class.md)\<\*\> | `https://developer.android.com/reference/kotlin/java/lang/reflect/Executable#getDeclaringClass()()` Returns the `Class` object representing the class or interface that declares the executable represented by this object. |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Class](../java.lang/Class.md)\<\*\>!\> | `https://developer.android.com/reference/kotlin/java/lang/reflect/Executable#getExceptionTypes()()` Returns an array of `Class` objects that represent the types of exceptions declared to be thrown by the underlying executable represented by this object. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Type](Type.md)!\> | `https://developer.android.com/reference/kotlin/java/lang/reflect/Executable#getGenericExceptionTypes()()` Returns an array of `Type` objects that represent the exceptions declared to be thrown by this executable object. |
| --- | --- |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Type](Type.md)!\> | `https://developer.android.com/reference/kotlin/java/lang/reflect/Executable#getGenericParameterTypes()()` Returns an array of `Type` objects that represent the formal parameter types, in declaration order, of the executable represented by this object. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/reflect/Executable#getModifiers()()` Returns the Java language [modifiers](Modifier.md) for the executable represented by this object. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/lang/reflect/Executable#getName()()` Returns the name of the executable represented by this object. |
| --- | --- |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Annotation](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-annotation/index.html)!\>!\> | `https://developer.android.com/reference/kotlin/java/lang/reflect/Executable#getParameterAnnotations()()` Returns an array of arrays of `Annotation`s that represent the annotations on the formal parameters, in declaration order, of the `Executable` represented by this object. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/lang/reflect/Executable#getParameterCount()()` Returns the number of formal parameters (whether explicitly declared or implicitly declared or neither) for the executable represented by this object. |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Class](../java.lang/Class.md)\<\*\>!\> | `https://developer.android.com/reference/kotlin/java/lang/reflect/Executable#getParameterTypes()()` Returns an array of `Class` objects that represent the formal parameter types, in declaration order, of the executable represented by this object. |
| --- | --- |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Parameter](Parameter.md)!\> | `https://developer.android.com/reference/kotlin/java/lang/reflect/Executable#getParameters()()` Returns an array of `Parameter` objects that represent all the parameters to the underlying executable represented by this object. |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [TypeVariable](TypeVariable.md)\<\*\>!\> | `https://developer.android.com/reference/kotlin/java/lang/reflect/Executable#getTypeParameters()()` Returns an array of `TypeVariable` objects that represent the type variables declared by the generic declaration represented by this `GenericDeclaration` object, in declaration order. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/reflect/Executable#isAnnotationPresent(java.lang.Class)(annotationType: https://developer.android.com/reference/kotlin/java/lang/Class.html#<out https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-annotation/index.html!>)` Returns true if an annotation for the specified type is *present* on this element, else false. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/reflect/Executable#isSynthetic()()` Returns `true` if this executable is a synthetic construct; returns `false` otherwise. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/reflect/Executable#isVarArgs()()` Returns `true` if this executable was declared to take a variable number of arguments; returns `false` otherwise. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/lang/reflect/Executable#toGenericString()()` Returns a string describing this `Executable`, including any type parameters. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/java/lang/reflect/AccessibleObject` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-annotation/index.html!>` | `https://developer.android.com/reference/kotlin/java/lang/reflect/AccessibleObject#getAnnotations()()` <br /> | | `T?` | `https://developer.android.com/reference/kotlin/java/lang/reflect/AccessibleObject#getDeclaredAnnotation(java.lang.Class)(annotationClass: https://developer.android.com/reference/kotlin/java/lang/Class.html#<T>)` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<T>!` | `https://developer.android.com/reference/kotlin/java/lang/reflect/AccessibleObject#getDeclaredAnnotationsByType(java.lang.Class)(annotationClass: https://developer.android.com/reference/kotlin/java/lang/Class.html#<T>)` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/lang/reflect/AccessibleObject#isAccessible()()` Get the value of the `accessible` flag for this object. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/java/lang/reflect/AccessibleObject#setAccessible(kotlin.Boolean)(flag: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Set the `accessible` flag for this object to the indicated boolean value. A value of `true` indicates that the reflected object should suppress Java language access checking when it is used. A value of `false` indicates that the reflected object should enforce Java language access checks. First, if there is a security manager, its `checkPermission` method is called with a `ReflectPermission("suppressAccessChecks")` permission. A `SecurityException` is raised if `flag` is `true` but accessibility of this object may not be changed (for example, if this element object is a `https://developer.android.com/reference/kotlin/java/lang/reflect/Constructor` object for the class `https://developer.android.com/reference/kotlin/java/lang/Class.html#`). A `SecurityException` is raised if this object is a `https://developer.android.com/reference/kotlin/java/lang/reflect/Constructor` object for the class `java.lang.Class`, and `flag` is true. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/java/lang/reflect/AccessibleObject#setAccessible(kotlin.Array,%20kotlin.Boolean)(array: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/lang/reflect/AccessibleObject!>!, flag: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Convenience method to set the `accessible` flag for an array of objects with a single security check (for efficiency). First, if there is a security manager, its `checkPermission` method is called with a `ReflectPermission("suppressAccessChecks")` permission. A `SecurityException` is raised if `flag` is `true` but accessibility of any of the elements of the input `array` may not be changed (for example, if the element object is a `https://developer.android.com/reference/kotlin/java/lang/reflect/Constructor` object for the class `https://developer.android.com/reference/kotlin/java/lang/Class.html#`). In the event of such a SecurityException, the accessibility of objects is set to `flag` for array elements upto (and excluding) the element for which the exception occurred; the accessibility of elements beyond (and including) the element for which the exception occurred is unchanged. <br /> | ||

## Public methods

### getAnnotation

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun <T : Annotation!> getAnnotation(annotationClass: Class<T>): T?
```

Returns this element's annotation for the specified type if such an annotation is *present*, else null.

| Parameters ||
|---|---|
| `<T>` | the type of the annotation to query for and return if present |
| `annotationClass` | [Class](../java.lang/Class.md)\<T\>: the Class object corresponding to the annotation type |

| Return ||
|---|---|
| `T?` | this element's annotation for the specified annotation type if present on this element, else null |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the given annotation class is null |

### getAnnotationsByType

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun <T : Annotation!> getAnnotationsByType(annotationClass: Class<T>): Array<T>!
```

Returns annotations that are *associated* with this element. If there are no annotations *associated* with this element, the return value is an array of length 0. The difference between this method and `https://developer.android.com/reference/kotlin/java/lang/reflect/AnnotatedElement#getAnnotation(java.lang.Class)` is that this method detects if its argument is a *repeatable annotation type* (JLS 9.6), and if so, attempts to find one or more annotations of that type by "looking through" a container annotation. The caller of this method is free to modify the returned array; it will have no effect on the arrays returned to other callers.

| Parameters ||
|---|---|
| `<T>` | the type of the annotation to query for and return if present |
| `annotationClass` | [Class](../java.lang/Class.md)\<T\>: the Class object corresponding to the annotation type |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<T>!` | all this element's annotations for the specified annotation type if associated with this element, else an array of length zero |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the given annotation class is null |

### getDeclaredAnnotations

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDeclaredAnnotations(): Array<Annotation!>
```

Returns annotations that are *directly present* on this element. This method ignores inherited annotations. If there are no annotations *directly present* on this element, the return value is an array of length 0. The caller of this method is free to modify the returned array; it will have no effect on the arrays returned to other callers.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-annotation/index.html!>` | annotations directly present on this element |

### getDeclaringClass

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getDeclaringClass(): Class<*>
```

Returns the `Class` object representing the class or interface that declares the executable represented by this object.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/Class.html#<*>` | an object representing the declaring class of the underlying member |

### getExceptionTypes

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getExceptionTypes(): Array<Class<*>!>
```

Returns an array of `Class` objects that represent the types of exceptions declared to be thrown by the underlying executable represented by this object. Returns an array of length 0 if the executable declares no exceptions in its `throws` clause.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/lang/Class.html#<*>!>` | the exception types declared as being thrown by the executable this object represents |

### getGenericExceptionTypes

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getGenericExceptionTypes(): Array<Type!>
```

Returns an array of `Type` objects that represent the exceptions declared to be thrown by this executable object. Returns an array of length 0 if the underlying executable declares no exceptions in its `throws` clause.

If an exception type is a type variable or a parameterized type, it is created. Otherwise, it is resolved.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/lang/reflect/Type!>` | an array of Types that represent the exception types thrown by the underlying executable |

| Exceptions ||
|---|---|
| `java.lang.TypeNotPresentException` | if the underlying executable's `throws` clause refers to a non-existent type declaration |
| `java.lang.reflect.GenericSignatureFormatError` | if the generic method signature does not conform to the format specified in The Java™ Virtual Machine Specification |
| `java.lang.reflect.MalformedParameterizedTypeException` | if the underlying executable's `throws` clause refers to a parameterized type that cannot be instantiated for any reason |
| --- | --- |

### getGenericParameterTypes

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getGenericParameterTypes(): Array<Type!>
```

Returns an array of `Type` objects that represent the formal parameter types, in declaration order, of the executable represented by this object. Returns an array of length 0 if the underlying executable takes no parameters.

If a formal parameter type is a parameterized type, the `Type` object returned for it must accurately reflect the actual type parameters used in the source code.

If a formal parameter type is a type variable or a parameterized type, it is created. Otherwise, it is resolved.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/lang/reflect/Type!>` | an array of `Type`s that represent the formal parameter types of the underlying executable, in declaration order |

| Exceptions ||
|---|---|
| `java.lang.TypeNotPresentException` | if any of the parameter types of the underlying executable refers to a non-existent type declaration |
| `java.lang.reflect.GenericSignatureFormatError` | if the generic method signature does not conform to the format specified in The Java™ Virtual Machine Specification |
| `java.lang.reflect.MalformedParameterizedTypeException` | if any of the underlying executable's parameter types refer to a parameterized type that cannot be instantiated for any reason |
| --- | --- |

### getModifiers

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getModifiers(): Int
```

Returns the Java language [modifiers](Modifier.md) for the executable represented by this object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the Java language modifiers for the underlying member |

### getName

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getName(): String
```

Returns the name of the executable represented by this object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | the simple name of the underlying member |

### getParameterAnnotations

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getParameterAnnotations(): Array<Array<Annotation!>!>
```

Returns an array of arrays of `Annotation`s that represent the annotations on the formal parameters, in declaration order, of the `Executable` represented by this object. Synthetic and mandated parameters (see explanation below), such as the outer "this" parameter to an inner class constructor will be represented in the returned array. If the executable has no parameters (meaning no formal, no synthetic, and no mandated parameters), a zero-length array will be returned. If the `Executable` has one or more parameters, a nested array of length zero is returned for each parameter with no annotations. The annotation objects contained in the returned arrays are serializable. The caller of this method is free to modify the returned arrays; it will have no effect on the arrays returned to other callers. A compiler may add extra parameters that are implicitly declared in source ("mandated"), as well as parameters that are neither implicitly nor explicitly declared in source ("synthetic") to the parameter list for a method. See `https://developer.android.com/reference/kotlin/java/lang/reflect/Parameter` for more information.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-annotation/index.html!>!>` | an array of arrays that represent the annotations on the formal and implicit parameters, in declaration order, of the executable represented by this object |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/reflect/Parameter`
- `https://developer.android.com/reference/kotlin/java/lang/reflect/Parameter#getAnnotations()`

### getParameterCount

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getParameterCount(): Int
```

Returns the number of formal parameters (whether explicitly declared or implicitly declared or neither) for the executable represented by this object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The number of formal parameters for the executable this object represents |

### getParameterTypes

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getParameterTypes(): Array<Class<*>!>
```

Returns an array of `Class` objects that represent the formal parameter types, in declaration order, of the executable represented by this object. Returns an array of length 0 if the underlying executable takes no parameters.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/lang/Class.html#<*>!>` | the parameter types for the executable this object represents |

### getParameters

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getParameters(): Array<Parameter!>
```

Returns an array of `Parameter` objects that represent all the parameters to the underlying executable represented by this object. Returns an array of length 0 if the executable has no parameters.

The parameters of the underlying executable do not necessarily have unique names, or names that are legal identifiers in the Java programming language (JLS 3.8).

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/lang/reflect/Parameter!>` | an array of `Parameter` objects representing all the parameters to the executable this object represents. |

| Exceptions ||
|---|---|
| `java.lang.reflect.MalformedParametersException` | if the class file contains a MethodParameters attribute that is improperly formatted. |

### getTypeParameters

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getTypeParameters(): Array<TypeVariable<*>!>
```

Returns an array of `TypeVariable` objects that represent the type variables declared by the generic declaration represented by this `GenericDeclaration` object, in declaration order. Returns an array of length 0 if the underlying generic declaration declares no type variables.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/lang/reflect/TypeVariable<*>!>` | an array of `TypeVariable` objects that represent the type variables declared by this generic declaration |

| Exceptions ||
|---|---|
| `java.lang.reflect.GenericSignatureFormatError` | if the generic signature of this generic declaration does not conform to the format specified in The Java™ Virtual Machine Specification |

### isAnnotationPresent

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isAnnotationPresent(annotationType: Class<out Annotation!>): Boolean
```

Returns true if an annotation for the specified type is *present* on this element, else false. This method is designed primarily for convenient access to marker annotations.

The truth value returned by this method is equivalent to: `getAnnotation(annotationClass) != null`

The body of the default method is specified to be the code above.

| Parameters ||
|---|---|
| `annotationClass` | the Class object corresponding to the annotation type |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if an annotation for the specified annotation type is present on this element, else false |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the given annotation class is null |

### isSynthetic

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isSynthetic(): Boolean
```

Returns `true` if this executable is a synthetic construct; returns `false` otherwise.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if and only if this executable is a synthetic construct as defined by The Java™ Language Specification. |

### isVarArgs

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isVarArgs(): Boolean
```

Returns `true` if this executable was declared to take a variable number of arguments; returns `false` otherwise.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if an only if this executable was declared to take a variable number of arguments. |

### toGenericString

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun toGenericString(): String
```

Returns a string describing this `Executable`, including any type parameters.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string describing this `Executable`, including any type parameters |
