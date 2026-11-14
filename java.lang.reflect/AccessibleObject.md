Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AccessibleObject

```
open class AccessibleObject : AnnotatedElement
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.lang.reflect.AccessibleObject](AccessibleObject.md) |

| Known Direct Subclasses [Executable](Executable.md), [Field](Field.md) |---|---| | [Executable](Executable.md) | A shared superclass for the common functionality of `https://developer.android.com/reference/kotlin/java/lang/reflect/Method` and `https://developer.android.com/reference/kotlin/java/lang/reflect/Constructor`. | | [Field](Field.md) | A `Field` provides information about, and dynamic access to, a single field of a class or an interface. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [Constructor](Constructor.md), [Method](Method.md) |---|---| | [Constructor](Constructor.md) | `Constructor` provides information about, and access to, a single constructor for a class. | | [Method](Method.md) | A `Method` provides information about, and access to, a single method on a class or interface. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

The AccessibleObject class is the base class for Field, Method and Constructor objects. It provides the ability to flag a reflected object as suppressing default Java language access control checks when it is used. The access checks--for public, default (package) access, protected, and private members--are performed when Fields, Methods or Constructors are used to set or get fields, to invoke methods, or to create and initialize new instances of classes, respectively.

Setting the `accessible` flag in a reflected object permits sophisticated applications with sufficient privilege, such as Java Object Serialization or other persistence mechanisms, to manipulate objects in a manner that would normally be prohibited.

By default, a reflected object is *not* accessible.

## Summary

| Protected constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/reflect/AccessibleObject#AccessibleObject()()` Constructor: only used by the Java Virtual Machine. |

| Public methods ||
|---|---|
| open T? | `https://developer.android.com/reference/kotlin/java/lang/reflect/AccessibleObject#getAnnotation(java.lang.Class)(annotationClass: https://developer.android.com/reference/kotlin/java/lang/Class.html#<T>)` <br /> |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Annotation](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-annotation/index.html)!\> | `https://developer.android.com/reference/kotlin/java/lang/reflect/AccessibleObject#getAnnotations()()` <br /> |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>! | `https://developer.android.com/reference/kotlin/java/lang/reflect/AccessibleObject#getAnnotationsByType(java.lang.Class)(annotationClass: https://developer.android.com/reference/kotlin/java/lang/Class.html#<T>)` <br /> |
| --- | --- |
| open T? | `https://developer.android.com/reference/kotlin/java/lang/reflect/AccessibleObject#getDeclaredAnnotation(java.lang.Class)(annotationClass: https://developer.android.com/reference/kotlin/java/lang/Class.html#<T>)` <br /> |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Annotation](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-annotation/index.html)!\> | `https://developer.android.com/reference/kotlin/java/lang/reflect/AccessibleObject#getDeclaredAnnotations()()` <br /> |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>! | `https://developer.android.com/reference/kotlin/java/lang/reflect/AccessibleObject#getDeclaredAnnotationsByType(java.lang.Class)(annotationClass: https://developer.android.com/reference/kotlin/java/lang/Class.html#<T>)` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/reflect/AccessibleObject#isAccessible()()` Get the value of the `accessible` flag for this object. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/lang/reflect/AccessibleObject#isAnnotationPresent(java.lang.Class)(annotationClass: https://developer.android.com/reference/kotlin/java/lang/Class.html#<out https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-annotation/index.html!>)` Returns true if an annotation for the specified type is *present* on this element, else false. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/lang/reflect/AccessibleObject#setAccessible(kotlin.Boolean)(flag: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Set the `accessible` flag for this object to the indicated boolean value. |
| --- | --- |
| open static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/lang/reflect/AccessibleObject#setAccessible(kotlin.Array,%20kotlin.Boolean)(array: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/lang/reflect/AccessibleObject#!>!, flag: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Convenience method to set the `accessible` flag for an array of objects with a single security check (for efficiency). |

## Protected constructors

### AccessibleObject

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected AccessibleObject()
```

Constructor: only used by the Java Virtual Machine.

## Public methods

### getAnnotation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun <T : Annotation!> getAnnotation(annotationClass: Class<T>): T?
```

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

### getAnnotations

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAnnotations(): Array<Annotation!>
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-annotation/index.html!>` | annotations present on this element |

### getAnnotationsByType

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun <T : Annotation!> getAnnotationsByType(annotationClass: Class<T>): Array<T>!
```

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

### getDeclaredAnnotation

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun <T : Annotation!> getDeclaredAnnotation(annotationClass: Class<T>): T?
```

| Parameters ||
|---|---|
| `<T>` | the type of the annotation to query for and return if directly present |
| `annotationClass` | [Class](../java.lang/Class.md)\<T\>: the Class object corresponding to the annotation type |

| Return ||
|---|---|
| `T?` | this element's annotation for the specified annotation type if directly present on this element, else null |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the given annotation class is null |

### getDeclaredAnnotations

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDeclaredAnnotations(): Array<Annotation!>
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-annotation/index.html!>` | annotations directly present on this element |

### getDeclaredAnnotationsByType

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun <T : Annotation!> getDeclaredAnnotationsByType(annotationClass: Class<T>): Array<T>!
```

| Parameters ||
|---|---|
| `<T>` | the type of the annotation to query for and return if directly or indirectly present |
| `annotationClass` | [Class](../java.lang/Class.md)\<T\>: the Class object corresponding to the annotation type |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<T>!` | all this element's annotations for the specified annotation type if directly or indirectly present on this element, else an array of length zero |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the given annotation class is null |

### isAccessible

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isAccessible(): Boolean
```

Get the value of the `accessible` flag for this object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | the value of the object's `accessible` flag |

### isAnnotationPresent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isAnnotationPresent(annotationClass: Class<out Annotation!>): Boolean
```

Returns true if an annotation for the specified type is *present* on this element, else false. This method is designed primarily for convenient access to marker annotations.

The truth value returned by this method is equivalent to: `getAnnotation(annotationClass) != null`

The body of the default method is specified to be the code above.

| Parameters ||
|---|---|
| `annotationClass` | [Class](../java.lang/Class.md)\<out [Annotation](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-annotation/index.html)!\>: the Class object corresponding to the annotation type |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if an annotation for the specified annotation type is present on this element, else false |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the given annotation class is null |

### setAccessible

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setAccessible(flag: Boolean): Unit
```

Set the `accessible` flag for this object to the indicated boolean value. A value of `true` indicates that the reflected object should suppress Java language access checking when it is used. A value of `false` indicates that the reflected object should enforce Java language access checks.

First, if there is a security manager, its `checkPermission` method is called with a `ReflectPermission("suppressAccessChecks")` permission.

A `SecurityException` is raised if `flag` is `true` but accessibility of this object may not be changed (for example, if this element object is a `https://developer.android.com/reference/kotlin/java/lang/reflect/Constructor` object for the class `https://developer.android.com/reference/kotlin/java/lang/Class.html#`).

A `SecurityException` is raised if this object is a `https://developer.android.com/reference/kotlin/java/lang/reflect/Constructor` object for the class `java.lang.Class`, and `flag` is true.

| Parameters ||
|---|---|
| `flag` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): the new value for the `accessible` flag |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if the request is denied. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/RuntimePermission.html#`

### setAccessible

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun setAccessible(
    array: Array<AccessibleObject!>!, 
    flag: Boolean
): Unit
```

Convenience method to set the `accessible` flag for an array of objects with a single security check (for efficiency).

First, if there is a security manager, its `checkPermission` method is called with a `ReflectPermission("suppressAccessChecks")` permission.

A `SecurityException` is raised if `flag` is `true` but accessibility of any of the elements of the input `array` may not be changed (for example, if the element object is a `https://developer.android.com/reference/kotlin/java/lang/reflect/Constructor` object for the class `https://developer.android.com/reference/kotlin/java/lang/Class.html#`). In the event of such a SecurityException, the accessibility of objects is set to `flag` for array elements upto (and excluding) the element for which the exception occurred; the accessibility of elements beyond (and including) the element for which the exception occurred is unchanged.

| Parameters ||
|---|---|
| `array` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [AccessibleObject](AccessibleObject.md)!\>!: the array of AccessibleObjects |
| `flag` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): the new value for the `accessible` flag in each object |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if the request is denied. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/RuntimePermission.html#`
