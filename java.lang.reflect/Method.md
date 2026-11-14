# Method

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Method

```
class Method : Executable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [java.lang.reflect.AccessibleObject](https://developer.android.com/reference/kotlin/java/lang/reflect/AccessibleObject) |||
| | ↳ | [java.lang.reflect.Executable](https://developer.android.com/reference/kotlin/java/lang/reflect/Executable) ||
| | | ↳ | [java.lang.reflect.Method](https://developer.android.com/reference/kotlin/java/lang/reflect/Method#) |
| --- | --- | --- | --- |

A `Method` provides information about, and access to, a single method on a class or interface. The reflected method may be a class method or an instance method (including an abstract method).

A `Method` permits widening conversions to occur when matching the actual parameters to invoke with the underlying method's formal parameters, but it throws an `IllegalArgumentException` if a narrowing conversion would occur.

## Summary

| Inherited constants ||
|---|---|
| From class [Member](https://developer.android.com/reference/kotlin/java/lang/reflect/Member) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DECLARED](https://developer.android.com/reference/kotlin/java/lang/reflect/Member#DECLARED:kotlin.Int) Identifies the set of declared members of a class or interface. Inherited members are not included. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PUBLIC](https://developer.android.com/reference/kotlin/java/lang/reflect/Member#PUBLIC:kotlin.Int) Identifies the set of all public members of a class or interface, including inherited members. <br /> | ||

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/java/lang/reflect/Method#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Compares this `Method` against the specified object. |
| T? | [getAnnotation](https://developer.android.com/reference/kotlin/java/lang/reflect/Method#getAnnotation(java.lang.Class))`(`annotationClass:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<T>`)` Returns this element's annotation for the specified type if such an annotation is *present*, else null. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Annotation](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-annotation/index.html)!\> | [getDeclaredAnnotations](https://developer.android.com/reference/kotlin/java/lang/reflect/Method#getDeclaredAnnotations())`()` Returns annotations that are *directly present* on this element. |
| --- | --- |
| [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<\*\> | [getDeclaringClass](https://developer.android.com/reference/kotlin/java/lang/reflect/Method#getDeclaringClass())`()` Returns the `Class` object representing the class or interface that declares the executable represented by this object. |
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)? | [getDefaultValue](https://developer.android.com/reference/kotlin/java/lang/reflect/Method#getDefaultValue())`()` Returns the default value for the annotation member represented by this `Method` instance. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<\*\>!\> | [getExceptionTypes](https://developer.android.com/reference/kotlin/java/lang/reflect/Method#getExceptionTypes())`()` Returns an array of `Class` objects that represent the types of exceptions declared to be thrown by the underlying executable represented by this object. |
| --- | --- |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Type](https://developer.android.com/reference/kotlin/java/lang/reflect/Type)!\> | [getGenericExceptionTypes](https://developer.android.com/reference/kotlin/java/lang/reflect/Method#getGenericExceptionTypes())`()` Returns an array of `Type` objects that represent the exceptions declared to be thrown by this executable object. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Type](https://developer.android.com/reference/kotlin/java/lang/reflect/Type)!\> | [getGenericParameterTypes](https://developer.android.com/reference/kotlin/java/lang/reflect/Method#getGenericParameterTypes())`()` Returns an array of `Type` objects that represent the formal parameter types, in declaration order, of the executable represented by this object. |
| [Type](https://developer.android.com/reference/kotlin/java/lang/reflect/Type) | [getGenericReturnType](https://developer.android.com/reference/kotlin/java/lang/reflect/Method#getGenericReturnType())`()` Returns a `Type` object that represents the formal return type of the method represented by this `Method` object. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getModifiers](https://developer.android.com/reference/kotlin/java/lang/reflect/Method#getModifiers())`()` Returns the Java language [modifiers](https://developer.android.com/reference/kotlin/java/lang/reflect/Modifier) for the executable represented by this object. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getName](https://developer.android.com/reference/kotlin/java/lang/reflect/Method#getName())`()` Returns the name of the method represented by this `Method` object, as a `String`. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Annotation](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-annotation/index.html)!\>!\> | [getParameterAnnotations](https://developer.android.com/reference/kotlin/java/lang/reflect/Method#getParameterAnnotations())`()` Returns an array of arrays of `Annotation`s that represent the annotations on the formal parameters, in declaration order, of the `Executable` represented by this object. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getParameterCount](https://developer.android.com/reference/kotlin/java/lang/reflect/Method#getParameterCount())`()` Returns the number of formal parameters (whether explicitly declared or implicitly declared or neither) for the executable represented by this object. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<\*\>!\> | [getParameterTypes](https://developer.android.com/reference/kotlin/java/lang/reflect/Method#getParameterTypes())`()` Returns an array of `Class` objects that represent the formal parameter types, in declaration order, of the executable represented by this object. |
| [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<\*\> | [getReturnType](https://developer.android.com/reference/kotlin/java/lang/reflect/Method#getReturnType())`()` Returns a `Class` object that represents the formal return type of the method represented by this `Method` object. |
| --- | --- |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [TypeVariable](https://developer.android.com/reference/kotlin/java/lang/reflect/TypeVariable)\< [Method](https://developer.android.com/reference/kotlin/java/lang/reflect/Method#)!\>!\> | [getTypeParameters](https://developer.android.com/reference/kotlin/java/lang/reflect/Method#getTypeParameters())`()` Returns an array of `TypeVariable` objects that represent the type variables declared by the generic declaration represented by this `GenericDeclaration` object, in declaration order. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/java/lang/reflect/Method#hashCode())`()` Returns a hashcode for this `Method`. |
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)? | [invoke](https://developer.android.com/reference/kotlin/java/lang/reflect/Method#invoke(kotlin.Any,%20kotlin.Any))`(`obj:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`, `vararg` `args:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Invokes the underlying method represented by this `Method` object, on the specified object with the specified parameters. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isBridge](https://developer.android.com/reference/kotlin/java/lang/reflect/Method#isBridge())`()` Returns `true` if this method is a bridge method; returns `false` otherwise. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDefault](https://developer.android.com/reference/kotlin/java/lang/reflect/Method#isDefault())`()` Returns `true` if this method is a default method; returns `false` otherwise. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSynthetic](https://developer.android.com/reference/kotlin/java/lang/reflect/Method#isSynthetic())`()` Returns `true` if this executable is a synthetic construct; returns `false` otherwise. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isVarArgs](https://developer.android.com/reference/kotlin/java/lang/reflect/Method#isVarArgs())`()` Returns `true` if this executable was declared to take a variable number of arguments; returns `false` otherwise. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toGenericString](https://developer.android.com/reference/kotlin/java/lang/reflect/Method#toGenericString())`()` Returns a string describing this `Method`, including type parameters. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/lang/reflect/Method#toString())`()` Returns a string describing this `Method`. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [AccessibleObject](https://developer.android.com/reference/kotlin/java/lang/reflect/AccessibleObject) |---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Annotation](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-annotation/index.html)!> | [getAnnotations](https://developer.android.com/reference/kotlin/java/lang/reflect/AccessibleObject#getAnnotations())`()` <br /> | | T? | [getDeclaredAnnotation](https://developer.android.com/reference/kotlin/java/lang/reflect/AccessibleObject#getDeclaredAnnotation(java.lang.Class))`(`annotationClass:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<T>`)` <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<T>! | [getDeclaredAnnotationsByType](https://developer.android.com/reference/kotlin/java/lang/reflect/AccessibleObject#getDeclaredAnnotationsByType(java.lang.Class))`(`annotationClass:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<T>`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAccessible](https://developer.android.com/reference/kotlin/java/lang/reflect/AccessibleObject#isAccessible())`()` Get the value of the `accessible` flag for this object. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAccessible](https://developer.android.com/reference/kotlin/java/lang/reflect/AccessibleObject#setAccessible(kotlin.Boolean))`(`flag:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Set the `accessible` flag for this object to the indicated boolean value. A value of `true` indicates that the reflected object should suppress Java language access checking when it is used. A value of `false` indicates that the reflected object should enforce Java language access checks. First, if there is a security manager, its `checkPermission` method is called with a `ReflectPermission("suppressAccessChecks")` permission. A `SecurityException` is raised if `flag` is `true` but accessibility of this object may not be changed (for example, if this element object is a [Constructor](https://developer.android.com/reference/kotlin/java/lang/reflect/Constructor) object for the class [java.lang.Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)). A `SecurityException` is raised if this object is a object for the class `java.lang.Class`, and `flag` is true. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAccessible](https://developer.android.com/reference/kotlin/java/lang/reflect/AccessibleObject#setAccessible(kotlin.Array,%20kotlin.Boolean))`(`array:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [AccessibleObject](https://developer.android.com/reference/kotlin/java/lang/reflect/AccessibleObject)!>!`, `flag:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Convenience method to set the `accessible` flag for an array of objects with a single security check (for efficiency). First, if there is a security manager, its `checkPermission` method is called with a `ReflectPermission("suppressAccessChecks")` permission. A `SecurityException` is raised if `flag` is `true` but accessibility of any of the elements of the input `array` may not be changed (for example, if the element object is a [Constructor](https://developer.android.com/reference/kotlin/java/lang/reflect/Constructor) object for the class ). In the event of such a SecurityException, the accessibility of objects is set to `flag` for array elements upto (and excluding) the element for which the exception occurred; the accessibility of elements beyond (and including) the element for which the exception occurred is unchanged. <br /> | ||
| From class [Executable](https://developer.android.com/reference/kotlin/java/lang/reflect/Executable) |--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<T>! | [getAnnotationsByType](https://developer.android.com/reference/kotlin/java/lang/reflect/Executable#getAnnotationsByType(java.lang.Class))`(`annotationClass:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<T>`)` Returns annotations that are *associated* with this element. If there are no annotations *associated* with this element, the return value is an array of length 0. The difference between this method and [getAnnotation(java.lang.Class)](https://developer.android.com/reference/kotlin/java/lang/reflect/AnnotatedElement#getAnnotation(java.lang.Class)) is that this method detects if its argument is a *repeatable annotation type* (JLS 9.6), and if so, attempts to find one or more annotations of that type by "looking through" a container annotation. The caller of this method is free to modify the returned array; it will have no effect on the arrays returned to other callers. <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Parameter](https://developer.android.com/reference/kotlin/java/lang/reflect/Parameter)!> | [getParameters](https://developer.android.com/reference/kotlin/java/lang/reflect/Executable#getParameters())`()` Returns an array of `Parameter` objects that represent all the parameters to the underlying executable represented by this object. Returns an array of length 0 if the executable has no parameters. The parameters of the underlying executable do not necessarily have unique names, or names that are legal identifiers in the Java programming language (JLS 3.8). <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAnnotationPresent](https://developer.android.com/reference/kotlin/java/lang/reflect/Executable#isAnnotationPresent(java.lang.Class))`(`annotationType:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<out` ` [Annotation](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-annotation/index.html)!>`)` <br /> | ||

## Public methods

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Compares this `Method` against the specified object. Returns true if the objects are the same. Two `Methods` are the same if they were declared by the same class and have the same name and formal parameter types and return type.

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true` if this object is the same as the obj argument; `false` otherwise. |

### getAnnotation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun <T : Annotation!> getAnnotation(annotationClass: Class<T>): T?
```

Returns this element's annotation for the specified type if such an annotation is *present*, else null.

| Parameters ||
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | the type of the annotation to query for and return if present |
| `annotationClass` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<T\>: the Class object corresponding to the annotation type |

| Return ||
|----|---------------------------------------------------------------------------------------------------|
| T? | this element's annotation for the specified annotation type if present on this element, else null |

| Exceptions ||
|----------------------------------|---------------------------------------|
| `java.lang.NullPointerException` | if the given annotation class is null |

### getDeclaredAnnotations

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDeclaredAnnotations(): Array<Annotation!>
```

Returns annotations that are *directly present* on this element. This method ignores inherited annotations. If there are no annotations *directly present* on this element, the return value is an array of length 0. The caller of this method is free to modify the returned array; it will have no effect on the arrays returned to other callers.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Annotation](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-annotation/index.html)!> | annotations directly present on this element |

### getDeclaringClass

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDeclaringClass(): Class<*>
```

Returns the `Class` object representing the class or interface that declares the executable represented by this object.

| Return ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<*> | an object representing the declaring class of the underlying member |

### getDefaultValue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDefaultValue(): Any?
```

Returns the default value for the annotation member represented by this `Method` instance. If the member is of a primitive type, an instance of the corresponding wrapper type is returned. Returns null if no default is associated with the member, or if the method instance does not represent a declared member of an annotation type.

| Return ||
|-----------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)? | the default value for the annotation member represented by this `Method` instance. |

| Exceptions ||
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.TypeNotPresentException` | if the annotation is of type [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#) and no definition can be found for the default class value. |

### getExceptionTypes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getExceptionTypes(): Array<Class<*>!>
```

Returns an array of `Class` objects that represent the types of exceptions declared to be thrown by the underlying executable represented by this object. Returns an array of length 0 if the executable declares no exceptions in its `throws` clause.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<*>!> | the exception types declared as being thrown by the executable this object represents |

### getGenericExceptionTypes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getGenericExceptionTypes(): Array<Type!>
```

Returns an array of `Type` objects that represent the exceptions declared to be thrown by this executable object. Returns an array of length 0 if the underlying executable declares no exceptions in its `throws` clause.

If an exception type is a type variable or a parameterized type, it is created. Otherwise, it is resolved.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Type](https://developer.android.com/reference/kotlin/java/lang/reflect/Type)!> | an array of Types that represent the exception types thrown by the underlying executable |

| Exceptions ||
|---------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| `java.lang.reflect.GenericSignatureFormatError` | if the generic method signature does not conform to the format specified in The Java™ Virtual Machine Specification |
| `java.lang.TypeNotPresentException` | if the underlying executable's `throws` clause refers to a non-existent type declaration |
| `java.lang.reflect.MalformedParameterizedTypeException` | if the underlying executable's `throws` clause refers to a parameterized type that cannot be instantiated for any reason |
| --- | --- |

### getGenericParameterTypes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getGenericParameterTypes(): Array<Type!>
```

Returns an array of `Type` objects that represent the formal parameter types, in declaration order, of the executable represented by this object. Returns an array of length 0 if the underlying executable takes no parameters.

If a formal parameter type is a parameterized type, the `Type` object returned for it must accurately reflect the actual type parameters used in the source code.

If a formal parameter type is a type variable or a parameterized type, it is created. Otherwise, it is resolved.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Type](https://developer.android.com/reference/kotlin/java/lang/reflect/Type)!> | an array of `Type`s that represent the formal parameter types of the underlying executable, in declaration order |

| Exceptions ||
|---------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.reflect.GenericSignatureFormatError` | if the generic method signature does not conform to the format specified in The Java™ Virtual Machine Specification |
| `java.lang.TypeNotPresentException` | if any of the parameter types of the underlying executable refers to a non-existent type declaration |
| `java.lang.reflect.MalformedParameterizedTypeException` | if any of the underlying executable's parameter types refer to a parameterized type that cannot be instantiated for any reason |
| --- | --- |

### getGenericReturnType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getGenericReturnType(): Type
```

Returns a `Type` object that represents the formal return type of the method represented by this `Method` object.

If the return type is a parameterized type, the `Type` object returned must accurately reflect the actual type parameters used in the source code.

If the return type is a type variable or a parameterized type, it is created. Otherwise, it is resolved.

| Return ||
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [Type](https://developer.android.com/reference/kotlin/java/lang/reflect/Type) | a `Type` object that represents the formal return type of the underlying method |

| Exceptions ||
|---------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| `java.lang.reflect.GenericSignatureFormatError` | if the generic method signature does not conform to the format specified in The Java™ Virtual Machine Specification |
| `java.lang.TypeNotPresentException` | if the underlying method's return type refers to a non-existent type declaration |
| `java.lang.reflect.MalformedParameterizedTypeException` | if the underlying method's return typed refers to a parameterized type that cannot be instantiated for any reason |
| --- | --- |

### getModifiers

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getModifiers(): Int
```

Returns the Java language [modifiers](https://developer.android.com/reference/kotlin/java/lang/reflect/Modifier) for the executable represented by this object.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the Java language modifiers for the underlying member |

### getName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getName(): String
```

Returns the name of the method represented by this `Method` object, as a `String`.

| Return ||
|----------------------------------------------------------------------------------|------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the simple name of the underlying member |

### getParameterAnnotations

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getParameterAnnotations(): Array<Array<Annotation!>!>
```

Returns an array of arrays of `Annotation`s that represent the annotations on the formal parameters, in declaration order, of the `Executable` represented by this object. Synthetic and mandated parameters (see explanation below), such as the outer "this" parameter to an inner class constructor will be represented in the returned array. If the executable has no parameters (meaning no formal, no synthetic, and no mandated parameters), a zero-length array will be returned. If the `Executable` has one or more parameters, a nested array of length zero is returned for each parameter with no annotations. The annotation objects contained in the returned arrays are serializable. The caller of this method is free to modify the returned arrays; it will have no effect on the arrays returned to other callers. A compiler may add extra parameters that are implicitly declared in source ("mandated"), as well as parameters that are neither implicitly nor explicitly declared in source ("synthetic") to the parameter list for a method. See for more information.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Annotation](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-annotation/index.html)!>!> | an array of arrays that represent the annotations on the formal and implicit parameters, in declaration order, of the executable represented by this object |

### getParameterCount

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getParameterCount(): Int
```

Returns the number of formal parameters (whether explicitly declared or implicitly declared or neither) for the executable represented by this object.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The number of formal parameters for the executable this object represents |

### getParameterTypes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getParameterTypes(): Array<Class<*>!>
```

Returns an array of `Class` objects that represent the formal parameter types, in declaration order, of the executable represented by this object. Returns an array of length 0 if the underlying executable takes no parameters.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<*>!> | the parameter types for the executable this object represents |

### getReturnType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getReturnType(): Class<*>
```

Returns a `Class` object that represents the formal return type of the method represented by this `Method` object.

| Return ||
|----------------------------------------------------------------------------------|-------------------------------------------------------|
| [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<*> | the return type for the method this object represents |

### getTypeParameters

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTypeParameters(): Array<TypeVariable<Method!>!>
```

Returns an array of `TypeVariable` objects that represent the type variables declared by the generic declaration represented by this `GenericDeclaration` object, in declaration order. Returns an array of length 0 if the underlying generic declaration declares no type variables.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [TypeVariable](https://developer.android.com/reference/kotlin/java/lang/reflect/TypeVariable)< [Method](https://developer.android.com/reference/kotlin/java/lang/reflect/Method#)!>!> | an array of `TypeVariable` objects that represent the type variables declared by this generic declaration |

| Exceptions ||
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.reflect.GenericSignatureFormatError` | if the generic signature of this generic declaration does not conform to the format specified in The Java™ Virtual Machine Specification |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

Returns a hashcode for this `Method`. The hashcode is computed as the exclusive-or of the hashcodes for the underlying method's declaring class name and the method's name.

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### invoke

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun invoke(
    obj: Any?, 
    vararg args: Any!
): Any?
```

Invokes the underlying method represented by this `Method` object, on the specified object with the specified parameters. Individual parameters are automatically unwrapped to match primitive formal parameters, and both primitive and reference parameters are subject to method invocation conversions as necessary.

If the underlying method is static, then the specified `obj` argument is ignored. It may be null.

If the number of formal parameters required by the underlying method is 0, the supplied `args` array may be of length 0 or null.

If the underlying method is an instance method, it is invoked using dynamic method lookup as documented in The Java Language Specification, Second Edition, section 15.12.4.4; in particular, overriding based on the runtime type of the target object will occur.

If the underlying method is static, the class that declared the method is initialized if it has not already been initialized.

If the method completes normally, the value it returns is returned to the caller of invoke; if the value has a primitive type, it is first appropriately wrapped in an object. However, if the value has the type of an array of a primitive type, the elements of the array are *not* wrapped in objects; in other words, an array of primitive type is returned. If the underlying method return type is void, the invocation returns null.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------|
| `obj` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?: the object the underlying method is invoked from |
| `args` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: the arguments used for the method call |

| Return ||
|-----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)? | the result of dispatching the method represented by this object on `obj` with parameters `args` |

| Exceptions ||
|-----------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalAccessException` | if this `Method` object is enforcing Java language access control and the underlying method is inaccessible. |
| `java.lang.IllegalArgumentException` | if the method is an instance method and the specified object argument is not an instance of the class or interface declaring the underlying method (or of a subclass or implementor thereof); if the number of actual and formal parameters differ; if an unwrapping conversion for primitive arguments fails; or if, after possible unwrapping, a parameter value cannot be converted to the corresponding formal parameter type by a method invocation conversion. |
| `java.lang.reflect.InvocationTargetException` | if the underlying method throws an exception. |
| --- | --- |
| `java.lang.NullPointerException` | if the specified object is null and the method is an instance method. |
| `java.lang.ExceptionInInitializerError` | if the initialization provoked by this method fails. |

### isBridge

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isBridge(): Boolean
```

Returns `true` if this method is a bridge method; returns `false` otherwise.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if and only if this method is a bridge method as defined by the Java Language Specification. |

### isDefault

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isDefault(): Boolean
```

Returns `true` if this method is a default method; returns `false` otherwise. A default method is a public non-abstract instance method, that is, a non-static method with a body, declared in an interface type.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if and only if this method is a default method as defined by the Java Language Specification. |

### isSynthetic

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isSynthetic(): Boolean
```

Returns `true` if this executable is a synthetic construct; returns `false` otherwise.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if and only if this executable is a synthetic construct as defined by The Java™ Language Specification. |

### isVarArgs

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isVarArgs(): Boolean
```

Returns `true` if this executable was declared to take a variable number of arguments; returns `false` otherwise.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true` if an only if this executable was declared to take a variable number of arguments. |

### toGenericString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toGenericString(): String
```

Returns a string describing this `Method`, including type parameters. The string is formatted as the method access modifiers, if any, followed by an angle-bracketed comma-separated list of the method's type parameters, if any, followed by the method's generic return type, followed by a space, followed by the class declaring the method, followed by a period, followed by the method name, followed by a parenthesized, comma-separated list of the method's generic formal parameter types. If this method was declared to take a variable number of arguments, instead of denoting the last parameter as "*Type* \[\]", it is denoted as "*Type*...". A space is used to separate access modifiers from one another and from the type parameters or return type. If there are no type parameters, the type parameter list is elided; if the type parameter list is present, a space separates the list from the class name. If the method is declared to throw exceptions, the parameter list is followed by a space, followed by the word throws followed by a comma-separated list of the generic thrown exception types.

The access modifiers are placed in canonical order as specified by "The Java Language Specification". This is `public`, `protected` or `private` first, and then other modifiers in the following order: `abstract`, `default`, `static`, `final`, `synchronized`, `native`, `strictfp`.

| Return ||
|----------------------------------------------------------------------------------|------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string describing this `Method`, include type parameters |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Returns a string describing this `Method`. The string is formatted as the method access modifiers, if any, followed by the method return type, followed by a space, followed by the class declaring the method, followed by a period, followed by the method name, followed by a parenthesized, comma-separated list of the method's formal parameter types. If the method throws checked exceptions, the parameter list is followed by a space, followed by the word throws followed by a comma-separated list of the thrown exception types. For example: 

```kotlin
public boolean java.lang.Object.equals(java.lang.Object)
  
```

<br />

The access modifiers are placed in canonical order as specified by "The Java Language Specification". This is `public`, `protected` or `private` first, and then other modifiers in the following order: `abstract`, `default`, `static`, `final`, `synchronized`, `native`, `strictfp`.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string describing this `Method` |
