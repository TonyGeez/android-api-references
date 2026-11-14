# Constructor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Constructor

```
class Constructor<T : Any!> : Executable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [java.lang.reflect.AccessibleObject](../java/lang/reflect/AccessibleObject.md) |||
| | ↳ | [java.lang.reflect.Executable](../java/lang/reflect/Executable.md) ||
| | | ↳ | [java.lang.reflect.Constructor](../java/lang/reflect/Constructor.md) |
| --- | --- | --- | --- |

`Constructor`provides information about, and access to, a single constructor for a class.

`Constructor`permits widening conversions to occur when matching the actual parameters to newInstance() with the underlying constructor's formal parameters, but throws an`IllegalArgumentException`if a narrowing conversion would occur.

## Summary

| Inherited constants ||
|---|---|
| From class [Member](../java/lang/reflect/Member.md) |----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DECLARED](../java/lang/reflect/Member.md) <br /> Identifies the set of declared members of a class or interface. Inherited members are not included. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PUBLIC](../java/lang/reflect/Member.md) <br /> Identifies the set of all public members of a class or interface, including inherited members. <br /> | ||

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../java/lang/reflect/Constructor.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Compares this`Constructor`against the specified object. |
| T? | [getAnnotation](../java/lang/reflect/Constructor.md))`(`annotationClass:` ` [Class](../java/lang/Class.md)<T>`)` Returns this element's annotation for the specified type if such an annotation is*present*, else null. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Annotation](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-annotation/index.html)!\> | [getDeclaredAnnotations](../java/lang/reflect/Constructor.md))`()` Returns annotations that are*directly present*on this element. |
| --- | --- |
| [Class](../java/lang/Class.md)\<T\> | [getDeclaringClass](../java/lang/reflect/Constructor.md))`()` Returns the`Class`object representing the class or interface that declares the executable represented by this object. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Class](../java/lang/Class.md)\<\*\>!\> | [getExceptionTypes](../java/lang/reflect/Constructor.md))`()` Returns an array of`Class`objects that represent the types of exceptions declared to be thrown by the underlying executable represented by this object. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Type](../java/lang/reflect/Type.md)!\> | [getGenericExceptionTypes](../java/lang/reflect/Constructor.md))`()` Returns an array of`Type`objects that represent the exceptions declared to be thrown by this executable object. |
| --- | --- |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Type](../java/lang/reflect/Type.md)!\> | [getGenericParameterTypes](../java/lang/reflect/Constructor.md))`()` Returns an array of`Type`objects that represent the formal parameter types, in declaration order, of the executable represented by this object. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getModifiers](../java/lang/reflect/Constructor.md))`()` Returns the Java language [modifiers](../java/lang/reflect/Modifier.md) for the executable represented by this object. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getName](../java/lang/reflect/Constructor.md))`()` Returns the name of this constructor, as a string. |
| --- | --- |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Annotation](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-annotation/index.html)!\>!\> | [getParameterAnnotations](../java/lang/reflect/Constructor.md))`()` Returns an array of arrays of`Annotation`s that represent the annotations on the formal parameters, in declaration order, of the`Executable`represented by this object. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getParameterCount](../java/lang/reflect/Constructor.md))`()` Returns the number of formal parameters (whether explicitly declared or implicitly declared or neither) for the executable represented by this object. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Class](../java/lang/Class.md)\<\*\>!\> | [getParameterTypes](../java/lang/reflect/Constructor.md))`()` Returns an array of`Class`objects that represent the formal parameter types, in declaration order, of the executable represented by this object. |
| --- | --- |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [TypeVariable](../java/lang/reflect/TypeVariable.md)\< [Constructor](../java/lang/reflect/Constructor.md)\<T\>!\>!\> | [getTypeParameters](../java/lang/reflect/Constructor.md))`()` Returns an array of`TypeVariable`objects that represent the type variables declared by the generic declaration represented by this`GenericDeclaration`object, in declaration order. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../java/lang/reflect/Constructor.md))`()` Returns a hashcode for this`Constructor`. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSynthetic](../java/lang/reflect/Constructor.md))`()` Returns`true`if this executable is a synthetic construct; returns`false`otherwise. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isVarArgs](../java/lang/reflect/Constructor.md))`()` Returns`true`if this executable was declared to take a variable number of arguments; returns`false`otherwise. |
| T | [newInstance](../java/lang/reflect/Constructor.md))`(`vararg` `initargs:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Uses the constructor represented by this`Constructor`object to create and initialize a new instance of the constructor's declaring class, with the specified initialization parameters. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toGenericString](../java/lang/reflect/Constructor.md))`()` Returns a string describing this`Constructor`, including type parameters. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../java/lang/reflect/Constructor.md))`()` Returns a string describing this`Constructor`. |

| Inherited functions ||
|---|---|
| From class [AccessibleObject](../java/lang/reflect/AccessibleObject.md) |---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Annotation](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-annotation/index.html)!> | [getAnnotations](../java/lang/reflect/AccessibleObject.md))`()` <br /> | | T? | [getDeclaredAnnotation](../java/lang/reflect/AccessibleObject.md))`(`annotationClass:` ` [Class](../java/lang/Class.md)<T>`)` <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<T>! | [getDeclaredAnnotationsByType](../java/lang/reflect/AccessibleObject.md))`(`annotationClass:` ` [Class](../java/lang/Class.md)<T>`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAccessible](../java/lang/reflect/AccessibleObject.md))`()` <br /> Get the value of the`accessible`flag for this object. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAccessible](../java/lang/reflect/AccessibleObject.md))`(`flag:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Set the`accessible`flag for this object to the indicated boolean value. A value of`true`indicates that the reflected object should suppress Java language access checking when it is used. A value of`false`indicates that the reflected object should enforce Java language access checks. First, if there is a security manager, its`checkPermission`method is called with a`ReflectPermission("suppressAccessChecks")`permission. A`SecurityException`is raised if`flag`is`true`but accessibility of this object may not be changed (for example, if this element object is a [Constructor](../java/lang/reflect/Constructor.md) object for the class [java.lang.Class](../java/lang/Class.md)). A`SecurityException`is raised if this object is a object for the class`java.lang.Class`, and`flag`is true. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAccessible](../java/lang/reflect/AccessibleObject.md))`(`array:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [AccessibleObject](../java/lang/reflect/AccessibleObject.md)!>!`, `flag:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Convenience method to set the`accessible`flag for an array of objects with a single security check (for efficiency). First, if there is a security manager, its`checkPermission`method is called with a`ReflectPermission("suppressAccessChecks")`permission. A`SecurityException`is raised if`flag`is`true`but accessibility of any of the elements of the input`array`may not be changed (for example, if the element object is a [Constructor](../java/lang/reflect/Constructor.md) object for the class ). In the event of such a SecurityException, the accessibility of objects is set to`flag`for array elements upto (and excluding) the element for which the exception occurred; the accessibility of elements beyond (and including) the element for which the exception occurred is unchanged. <br /> | ||
| From class [Executable](../java/lang/reflect/Executable.md) |--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<T>! | [getAnnotationsByType](../java/lang/reflect/Executable.md))`(`annotationClass:` ` [Class](../java/lang/Class.md)<T>`)` <br /> Returns annotations that are*associated* with this element. If there are no annotations*associated* with this element, the return value is an array of length 0. The difference between this method and [getAnnotation(java.lang.Class)](../java/lang/reflect/AnnotatedElement.md))is that this method detects if its argument is a*repeatable annotation type*(JLS 9.6), and if so, attempts to find one or more annotations of that type by "looking through" a container annotation. The caller of this method is free to modify the returned array; it will have no effect on the arrays returned to other callers. <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Parameter](../java/lang/reflect/Parameter.md)!> | [getParameters](../java/lang/reflect/Executable.md))`()` <br /> Returns an array of`Parameter`objects that represent all the parameters to the underlying executable represented by this object. Returns an array of length 0 if the executable has no parameters. The parameters of the underlying executable do not necessarily have unique names, or names that are legal identifiers in the Java programming language (JLS 3.8). <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAnnotationPresent](../java/lang/reflect/Executable.md))`(`annotationType:` ` [Class](../java/lang/Class.md)<out` ` [Annotation](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-annotation/index.html)!>`)` <br /> | ||

## Public methods

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Compares this`Constructor`against the specified object. Returns true if the objects are the same. Two`Constructor`objects are the same if they were declared by the same class and have the same formal parameter types.

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getAnnotation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun <T : Annotation!> getAnnotation(annotationClass: Class<T>): T?
```

Returns this element's annotation for the specified type if such an annotation is*present*, else null.

| Parameters ||
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | the type of the annotation to query for and return if present |
| `annotationClass` | [Class](../java/lang/Class.md)\<T\>:the Class object corresponding to the annotation type |

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

Returns annotations that are*directly present* on this element. This method ignores inherited annotations. If there are no annotations*directly present*on this element, the return value is an array of length 0. The caller of this method is free to modify the returned array; it will have no effect on the arrays returned to other callers.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Annotation](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-annotation/index.html)!> | annotations directly present on this element |

### getDeclaringClass

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDeclaringClass(): Class<T>
```

Returns the`Class`object representing the class or interface that declares the executable represented by this object.

| Return ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [Class](../java/lang/Class.md)<T> | an object representing the declaring class of the underlying member |

### getExceptionTypes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getExceptionTypes(): Array<Class<*>!>
```

Returns an array of`Class`objects that represent the types of exceptions declared to be thrown by the underlying executable represented by this object. Returns an array of length 0 if the executable declares no exceptions in its`throws`clause.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Class](../java/lang/Class.md)<*>!> | the exception types declared as being thrown by the executable this object represents |

### getGenericExceptionTypes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getGenericExceptionTypes(): Array<Type!>
```

Returns an array of`Type`objects that represent the exceptions declared to be thrown by this executable object. Returns an array of length 0 if the underlying executable declares no exceptions in its`throws`clause.

If an exception type is a type variable or a parameterized type, it is created. Otherwise, it is resolved.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Type](../java/lang/reflect/Type.md)!> | an array of Types that represent the exception types thrown by the underlying executable |

| Exceptions ||
|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| `java.lang.reflect.GenericSignatureFormatError` | if the generic method signature does not conform to the format specified in The Java™ Virtual Machine Specification |
| `java.lang.TypeNotPresentException` | if the underlying executable's`throws`clause refers to a non-existent type declaration |
| `java.lang.reflect.MalformedParameterizedTypeException` | if the underlying executable's`throws`clause refers to a parameterized type that cannot be instantiated for any reason |
| --- | --- |

### getGenericParameterTypes

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getGenericParameterTypes(): Array<Type!>
```

Returns an array of`Type`objects that represent the formal parameter types, in declaration order, of the executable represented by this object. Returns an array of length 0 if the underlying executable takes no parameters.

If a formal parameter type is a parameterized type, the`Type`object returned for it must accurately reflect the actual type parameters used in the source code.

If a formal parameter type is a type variable or a parameterized type, it is created. Otherwise, it is resolved.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Type](../java/lang/reflect/Type.md)!> | an array of`Type`s that represent the formal parameter types of the underlying executable, in declaration order |

| Exceptions ||
|---------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.reflect.GenericSignatureFormatError` | if the generic method signature does not conform to the format specified in The Java™ Virtual Machine Specification |
| `java.lang.TypeNotPresentException` | if any of the parameter types of the underlying executable refers to a non-existent type declaration |
| `java.lang.reflect.MalformedParameterizedTypeException` | if any of the underlying executable's parameter types refer to a parameterized type that cannot be instantiated for any reason |
| --- | --- |

### getModifiers

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getModifiers(): Int
```

Returns the Java language [modifiers](../java/lang/reflect/Modifier.md) for the executable represented by this object.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the Java language modifiers for the underlying member |

### getName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getName(): String
```

Returns the name of this constructor, as a string. This is the binary name of the constructor's declaring class.

| Return ||
|----------------------------------------------------------------------------------|------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the simple name of the underlying member |

### getParameterAnnotations

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getParameterAnnotations(): Array<Array<Annotation!>!>
```

Returns an array of arrays of`Annotation`s that represent the annotations on the formal parameters, in declaration order, of the`Executable`represented by this object. Synthetic and mandated parameters (see explanation below), such as the outer "this" parameter to an inner class constructor will be represented in the returned array. If the executable has no parameters (meaning no formal, no synthetic, and no mandated parameters), a zero-length array will be returned. If the`Executable`has one or more parameters, a nested array of length zero is returned for each parameter with no annotations. The annotation objects contained in the returned arrays are serializable. The caller of this method is free to modify the returned arrays; it will have no effect on the arrays returned to other callers. A compiler may add extra parameters that are implicitly declared in source ("mandated"), as well as parameters that are neither implicitly nor explicitly declared in source ("synthetic") to the parameter list for a method. See for more information.

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

Returns an array of`Class`objects that represent the formal parameter types, in declaration order, of the executable represented by this object. Returns an array of length 0 if the underlying executable takes no parameters.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Class](../java/lang/Class.md)<*>!> | the parameter types for the executable this object represents |

### getTypeParameters

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTypeParameters(): Array<TypeVariable<Constructor<T>!>!>
```

Returns an array of`TypeVariable`objects that represent the type variables declared by the generic declaration represented by this`GenericDeclaration`object, in declaration order. Returns an array of length 0 if the underlying generic declaration declares no type variables.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [TypeVariable](../java/lang/reflect/TypeVariable.md)< [Constructor](../java/lang/reflect/Constructor.md)<T>!>!> | an array of`TypeVariable`objects that represent the type variables declared by this generic declaration |

| Exceptions ||
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.reflect.GenericSignatureFormatError` | if the generic signature of this generic declaration does not conform to the format specified in The Java™ Virtual Machine Specification |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

Returns a hashcode for this`Constructor`. The hashcode is the same as the hashcode for the underlying constructor's declaring class name.

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### isSynthetic

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isSynthetic(): Boolean
```

Returns`true`if this executable is a synthetic construct; returns`false`otherwise.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if and only if this executable is a synthetic construct as defined by The Java™ Language Specification. |

### isVarArgs

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isVarArgs(): Boolean
```

Returns`true`if this executable was declared to take a variable number of arguments; returns`false`otherwise.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if an only if this executable was declared to take a variable number of arguments. |

### newInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun newInstance(vararg initargs: Any!): T
```

Uses the constructor represented by this`Constructor`object to create and initialize a new instance of the constructor's declaring class, with the specified initialization parameters. Individual parameters are automatically unwrapped to match primitive formal parameters, and both primitive and reference parameters are subject to method invocation conversions as necessary.

If the number of formal parameters required by the underlying constructor is 0, the supplied`initargs`array may be of length 0 or null.

If the constructor's declaring class is an inner class in a non-static context, the first argument to the constructor needs to be the enclosing instance; see section 15.9.3 of The Java™ Language Specification.

If the required access and argument checks succeed and the instantiation will proceed, the constructor's declaring class is initialized if it has not already been initialized.

If the constructor completes normally, returns the newly created and initialized instance.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `initargs` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:array of objects to be passed as arguments to the constructor call; values of primitive types are wrapped in a wrapper object of the appropriate type (e.g. a`float`in a [Float](../java/lang/Float.md)) |

| Return ||
|---|------------------------------------------------------------------------|
| T | a new object created by calling the constructor this object represents |

| Exceptions ||
|-----------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalAccessException` | if this`Constructor`object is enforcing Java language access control and the underlying constructor is inaccessible. |
| `java.lang.IllegalArgumentException` | if the number of actual and formal parameters differ; if an unwrapping conversion for primitive arguments fails; or if, after possible unwrapping, a parameter value cannot be converted to the corresponding formal parameter type by a method invocation conversion; if this constructor pertains to an enum type. |
| `java.lang.InstantiationException` | if the class that declares the underlying constructor represents an abstract class. |
| --- | --- |
| `java.lang.reflect.InvocationTargetException` | if the underlying constructor throws an exception. |
| `java.lang.ExceptionInInitializerError` | if the initialization provoked by this method fails. |

### toGenericString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toGenericString(): String
```

Returns a string describing this`Constructor`, including type parameters. The string is formatted as the constructor access modifiers, if any, followed by an angle-bracketed comma separated list of the constructor's type parameters, if any, followed by the fully-qualified name of the declaring class, followed by a parenthesized, comma-separated list of the constructor's generic formal parameter types. If this constructor was declared to take a variable number of arguments, instead of denoting the last parameter as "*Type* \[\]", it is denoted as "*Type* ...". A space is used to separate access modifiers from one another and from the type parameters or return type. If there are no type parameters, the type parameter list is elided; if the type parameter list is present, a space separates the list from the class name. If the constructor is declared to throw exceptions, the parameter list is followed by a space, followed by the word "`throws`" followed by a comma-separated list of the thrown exception types.

The only possible modifiers for constructors are the access modifiers`public`,`protected`or`private`. Only one of these may appear, or none if the constructor has default (package) access.

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string describing this`Constructor`, include type parameters |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Returns a string describing this`Constructor`. The string is formatted as the constructor access modifiers, if any, followed by the fully-qualified name of the declaring class, followed by a parenthesized, comma-separated list of the constructor's formal parameter types. For example: 

```kotlin
public java.util.Hashtable(int,float)
  
```

<br />

The only possible modifiers for constructors are the access modifiers`public`,`protected`or`private`. Only one of these may appear, or none if the constructor has default (package) access.

| Return ||
|----------------------------------------------------------------------------------|---------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string describing this`Constructor` |
