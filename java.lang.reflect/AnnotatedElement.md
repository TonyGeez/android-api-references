# AnnotatedElement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AnnotatedElement

```
interface AnnotatedElement
```

| [java.lang.reflect.AnnotatedElement](AnnotatedElement.md) |

| Known Direct Subclasses [AccessibleObject](AccessibleObject.md), [Class](../java.lang/Class.md), [GenericDeclaration](GenericDeclaration.md), [Package](../java.lang/Package.md), [Parameter](Parameter.md), [RecordComponent](RecordComponent.md) |-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------| | [AccessibleObject](AccessibleObject.md) | The AccessibleObject class is the base class for Field, Method and Constructor objects. | | [Class](../java.lang/Class.md) | Instances of the class represent classes and interfaces in a running Java application. | | [GenericDeclaration](GenericDeclaration.md) | A common interface for all entities that declare type variables. | | [Package](../java.lang/Package.md) | `Package`objects contain version information about the implementation and specification of a Java package. | | [Parameter](Parameter.md) | Information about method parameters. | | [RecordComponent](RecordComponent.md) | A`RecordComponent`provides information about, and dynamic access to, a component of a record class. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [Class](../java.lang/Class.md), [Constructor](Constructor.md), [Constructor](Constructor.md), [Executable](Executable.md), [Executable](Executable.md), [Field](Field.md), [Method](Method.md) [Method](Method.md) |---------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Class](../java.lang/Class.md) | Instances of the class represent classes and interfaces in a running Java application. | | [Constructor](Constructor.md) | `Constructor`provides information about, and access to, a single constructor for a class. | | [Constructor](Constructor.md) | `Constructor`provides information about, and access to, a single constructor for a class. | | [Executable](Executable.md) | A shared superclass for the common functionality of [Method](Method.md) and [Constructor](Constructor.md). | | [Executable](Executable.md) | A shared superclass for the common functionality of [Method](Method.md) and [Constructor](Constructor.md). | | [Field](Field.md) | A`Field`provides information about, and dynamic access to, a single field of a class or an interface. | | [Method](Method.md) | A`Method`provides information about, and access to, a single method on a class or interface. | | [Method](Method.md) | A`Method`provides information about, and access to, a single method on a class or interface. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Represents an annotated element of the program currently running in this VM. This interface allows annotations to be read reflectively. All annotations returned by methods in this interface are immutable and serializable. The arrays returned by methods of this interface may be modified by callers without affecting the arrays returned to other callers.

Android note: methods that return multiple annotations of different types such as [getAnnotations()](AnnotatedElement.md))and [getDeclaredAnnotations()](AnnotatedElement.md))can be affected by the explicit character-code ordering of annotations types specified by the DEX format. Annotations of different types on a single element are not guaranteed to be returned in the order they are declared in source.

The [getAnnotationsByType(java.lang.Class)](AnnotatedElement.md))and [getDeclaredAnnotationsByType(java.lang.Class)](AnnotatedElement.md))methods support multiple annotations of the same type on an element. If the argument to either method is a repeatable annotation type (JLS 9.6), then the method will "look through" a container annotation (JLS 9.7), if present, and return any annotations inside the container. Container annotations may be generated at compile-time to wrap multiple annotations of the argument type.

The terms*directly present* ,*indirectly present* ,*present* , and*associated*are used throughout this interface to describe precisely which annotations are returned by methods:

- An annotation*A* is*directly present* on an element*E* if*E* is annotated by*A*in the original source.
- An annotation*A* is*indirectly present* on an element*E* if*E* is annotated by a container annotation of*A*.
- An annotation*A* is present on an element*E* if either:
 - *A* is directly present on*E*; or
 - No annotation of*A* 's type is directly present on*E* , and*E* is a class, and*A* 's type is inheritable, and*A* is present on the superclass of*E*.
- An annotation*A* is*associated* with an element*E* if either:
 - *A* is directly or indirectly present on*E*; or
 - No annotation of*A* 's type is directly or indirectly present on*E* , and*E* is a class, and*A* 's type is inheritable, and*A* is associated with the superclass of*E*.

The table below summarizes which kind of annotation presence different methods in this interface examine.

| Method || Kind of Presence ||||
| --- | --- | --- | --- | --- | --- |
| Return Type | Signature | Directly Present | Indirectly Present | Present | Associated |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|--------------------|---------|------------|
| `T` | [getAnnotation(Class<T>)](AnnotatedElement.md)) | | | X | |
| `Annotation[]` | [getAnnotations()](AnnotatedElement.md)) | | | X | |
| `T[]` | [getAnnotationsByType(Class<T>)](AnnotatedElement.md)) | | | | X |
| --- | --- | --- | --- | --- | --- |
| `T` | [getDeclaredAnnotation(Class<T>)](AnnotatedElement.md)) | X | | | |
| `Annotation[]` | [getDeclaredAnnotations()](AnnotatedElement.md)) | X | | | |
| `T[]` | [getDeclaredAnnotationsByType(Class<T>)](AnnotatedElement.md)) | X | X | | |
| --- | --- | --- | --- | --- | --- |

For an invocation of`get[Declared]AnnotationsByType( Class < T >)`, the order of annotations which are directly or indirectly present on an element*E* is computed as if indirectly present annotations on*E* are directly present on*E*in place of their container annotation, in the order in which they appear in the value element of the container annotation.

There are several compatibility concerns to keep in mind if an annotation type*T* is originally*not* repeatable and later modified to be repeatable. The containing annotation type for*T* is*TC*.

- Modifying*T* to be repeatable is source and binary compatible with existing uses of*T* and with existing uses of*TC* . That is, for source compatibility, source code with annotations of type*T* or of type*TC* will still compile. For binary compatibility, class files with annotations of type*T* or of type*TC* (or with other kinds of uses of type*T* or of type*TC* ) will link against the modified version of*T* if they linked against the earlier version. (An annotation type*TC* may informally serve as an acting containing annotation type before*T* is modified to be formally repeatable. Alternatively, when*T* is made repeatable,*TC*can be introduced as a new type.)
- If an annotation type*TC* is present on an element, and*T* is modified to be repeatable with*TC* as its containing annotation type then:
 - The change to*T* is behaviorally compatible with respect to the`get[Declared]Annotation(Class<T>)`(called with an argument of*T* or*TC* ) and`get[Declared]Annotations()`methods because the results of the methods will not change due to*TC* becoming the containing annotation type for*T*.
 - The change to*T* changes the results of the`get[Declared]AnnotationsByType(Class<T>)`methods called with an argument of*T* , because those methods will now recognize an annotation of type*TC* as a container annotation for*T* and will "look through" it to expose annotations of type*T*.
- If an annotation of type*T* is present on an element and*T* is made repeatable and more annotations of type*T* are added to the element:
 - The addition of the annotations of type*T*is both source compatible and binary compatible.
 - The addition of the annotations of type*T* changes the results of the`get[Declared]Annotation(Class<T>)`methods and`get[Declared]Annotations()`methods, because those methods will now only see a container annotation on the element and not see an annotation of type*T*.
 - The addition of the annotations of type*T* changes the results of the`get[Declared]AnnotationsByType(Class<T>)`methods, because their results will expose the additional annotations of type*T* whereas previously they exposed only a single annotation of type*T*.

If an annotation returned by a method in this interface contains (directly or indirectly) a [Class](../java.lang/Class.md)-valued member referring to a class that is not accessible in this VM, attempting to read the class by calling the relevant Class-returning method on the returned annotation will result in a [TypeNotPresentException](../java.lang/TypeNotPresentException.md).

Similarly, attempting to read an enum-valued member will result in a [EnumConstantNotPresentException](../java.lang/EnumConstantNotPresentException.md) if the enum constant in the annotation is no longer present in the enum type.

If an annotation type*T* is (meta-)annotated with an`@Repeatable`annotation whose value element indicates a type*TC* , but*TC* does not declare a`value()`method with a return type of*T* `[]`, then an exception of type [java.lang.annotation.AnnotationFormatError](../java.lang.annotation/AnnotationFormatError.md) is thrown.

Finally, attempting to read a member whose definition has evolved incompatibly will result in a or an [java.lang.annotation.IncompleteAnnotationException](../java.lang.annotation/IncompleteAnnotationException.md).

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstractT? | [getAnnotation](AnnotatedElement.md))`(`annotationClass:` ` [Class](../java.lang/Class.md)<T>`)` Returns this element's annotation for the specified type if such an annotation is*present*, else null. |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Annotation](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-annotation/index.html)!\> | [getAnnotations](AnnotatedElement.md))`()` Returns annotations that are*present*on this element. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>! | [getAnnotationsByType](AnnotatedElement.md))`(`annotationClass:` ` [Class](../java.lang/Class.md)<T>`)` Returns annotations that are*associated*with this element. |
| --- | --- |
| openT? | [getDeclaredAnnotation](AnnotatedElement.md))`(`annotationClass:` ` [Class](../java.lang/Class.md)<T>`)` Returns this element's annotation for the specified type if such an annotation is*directly present*, else null. |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Annotation](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-annotation/index.html)!\> | [getDeclaredAnnotations](AnnotatedElement.md))`()` Returns annotations that are*directly present*on this element. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>! | [getDeclaredAnnotationsByType](AnnotatedElement.md))`(`annotationClass:` ` [Class](../java.lang/Class.md)<T>`)` Returns this element's annotation(s) for the specified type if such annotations are either*directly present* or*indirectly present*. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAnnotationPresent](AnnotatedElement.md))`(`annotationClass:` ` [Class](../java.lang/Class.md)<out` ` [Annotation](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-annotation/index.html)!>`)` Returns true if an annotation for the specified type is*present*on this element, else false. |

## Public methods

### getAnnotation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <T : Annotation!> getAnnotation(annotationClass: Class<T>): T?
```

Returns this element's annotation for the specified type if such an annotation is*present*, else null.

| Parameters ||
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | the type of the annotation to query for and return if present |
| `annotationClass` | [Class](../java.lang/Class.md)\<T\>:the Class object corresponding to the annotation type |

| Return ||
|----|---------------------------------------------------------------------------------------------------|
| T? | this element's annotation for the specified annotation type if present on this element, else null |

| Exceptions ||
|----------------------------------|---------------------------------------|
| `java.lang.NullPointerException` | if the given annotation class is null |

### getAnnotations

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getAnnotations(): Array<Annotation!>
```

Returns annotations that are*present* on this element. If there are no annotations*present*on this element, the return value is an array of length 0. The caller of this method is free to modify the returned array; it will have no effect on the arrays returned to other callers.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Annotation](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-annotation/index.html)!> | annotations present on this element |

### getAnnotationsByType

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <T : Annotation!> getAnnotationsByType(annotationClass: Class<T>): Array<T>!
```

Returns annotations that are*associated* with this element. If there are no annotations*associated* with this element, the return value is an array of length 0. The difference between this method and [getAnnotation(java.lang.Class)](AnnotatedElement.md))is that this method detects if its argument is a*repeatable annotation type*(JLS 9.6), and if so, attempts to find one or more annotations of that type by "looking through" a container annotation. The caller of this method is free to modify the returned array; it will have no effect on the arrays returned to other callers.

| Parameters ||
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | the type of the annotation to query for and return if present |
| `annotationClass` | [Class](../java.lang/Class.md)\<T\>:the Class object corresponding to the annotation type |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<T>! | all this element's annotations for the specified annotation type if associated with this element, else an array of length zero |

| Exceptions ||
|----------------------------------|---------------------------------------|
| `java.lang.NullPointerException` | if the given annotation class is null |

### getDeclaredAnnotation

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <T : Annotation!> getDeclaredAnnotation(annotationClass: Class<T>): T?
```

Returns this element's annotation for the specified type if such an annotation is*directly present*, else null. This method ignores inherited annotations. (Returns null if no annotations are directly present on this element.)

| Parameters ||
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | the type of the annotation to query for and return if directly present |
| `annotationClass` | [Class](../java.lang/Class.md)\<T\>:the Class object corresponding to the annotation type |

| Return ||
|----|------------------------------------------------------------------------------------------------------------|
| T? | this element's annotation for the specified annotation type if directly present on this element, else null |

| Exceptions ||
|----------------------------------|---------------------------------------|
| `java.lang.NullPointerException` | if the given annotation class is null |

### getDeclaredAnnotations

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getDeclaredAnnotations(): Array<Annotation!>
```

Returns annotations that are*directly present* on this element. This method ignores inherited annotations. If there are no annotations*directly present*on this element, the return value is an array of length 0. The caller of this method is free to modify the returned array; it will have no effect on the arrays returned to other callers.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Annotation](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-annotation/index.html)!> | annotations directly present on this element |

### getDeclaredAnnotationsByType

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <T : Annotation!> getDeclaredAnnotationsByType(annotationClass: Class<T>): Array<T>!
```

Returns this element's annotation(s) for the specified type if such annotations are either*directly present* or*indirectly present* . This method ignores inherited annotations. If there are no specified annotations directly or indirectly present on this element, the return value is an array of length 0. The difference between this method and [getDeclaredAnnotation(java.lang.Class)](AnnotatedElement.md))is that this method detects if its argument is a*repeatable annotation type*(JLS 9.6), and if so, attempts to find one or more annotations of that type by "looking through" a container annotation if one is present. The caller of this method is free to modify the returned array; it will have no effect on the arrays returned to other callers.

| Parameters ||
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | the type of the annotation to query for and return if directly or indirectly present |
| `annotationClass` | [Class](../java.lang/Class.md)\<T\>:the Class object corresponding to the annotation type |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<T>! | all this element's annotations for the specified annotation type if directly or indirectly present on this element, else an array of length zero |

| Exceptions ||
|----------------------------------|---------------------------------------|
| `java.lang.NullPointerException` | if the given annotation class is null |

### isAnnotationPresent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isAnnotationPresent(annotationClass: Class<out Annotation!>): Boolean
```

Returns true if an annotation for the specified type is*present*on this element, else false. This method is designed primarily for convenient access to marker annotations.

The truth value returned by this method is equivalent to:`getAnnotation(annotationClass) != null`

The body of the default method is specified to be the code above.

| Parameters ||
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `annotationClass` | [Class](../java.lang/Class.md)\<out [Annotation](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-annotation/index.html)!\>:the Class object corresponding to the annotation type |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if an annotation for the specified annotation type is present on this element, else false |

| Exceptions ||
|----------------------------------|---------------------------------------|
| `java.lang.NullPointerException` | if the given annotation class is null |
