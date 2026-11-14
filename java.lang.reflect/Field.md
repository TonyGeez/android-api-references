# Field

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Field

```
class Field : AccessibleObject, Member
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.lang.reflect.AccessibleObject](https://developer.android.com/reference/kotlin/java/lang/reflect/AccessibleObject) ||
| | ↳ | [java.lang.reflect.Field](https://developer.android.com/reference/kotlin/java/lang/reflect/Field#) |

A`Field`provides information about, and dynamic access to, a single field of a class or an interface. The reflected field may be a class (static) field or an instance field.

A`Field`permits widening conversions to occur during a get or set access operation, but throws an`IllegalArgumentException`if a narrowing conversion would occur.

## Summary

| Inherited constants ||
|---|---|
| From class [Member](https://developer.android.com/reference/kotlin/java/lang/reflect/Member) |----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DECLARED](https://developer.android.com/reference/kotlin/java/lang/reflect/Member#DECLARED:kotlin.Int) <br /> Identifies the set of declared members of a class or interface. Inherited members are not included. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PUBLIC](https://developer.android.com/reference/kotlin/java/lang/reflect/Member#PUBLIC:kotlin.Int) <br /> Identifies the set of all public members of a class or interface, including inherited members. <br /> | ||

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/java/lang/reflect/Field#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Compares this`Field`against the specified object. |
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)? | [get](https://developer.android.com/reference/kotlin/java/lang/reflect/Field#get(kotlin.Any))`(`obj:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Returns the value of the field represented by this`Field`, on the specified object. |
| T? | [getAnnotation](https://developer.android.com/reference/kotlin/java/lang/reflect/Field#getAnnotation(java.lang.Class))`(`annotationClass:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<T>`)` <br /> |
| --- | --- |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>! | [getAnnotationsByType](https://developer.android.com/reference/kotlin/java/lang/reflect/Field#getAnnotationsByType(java.lang.Class))`(`annotationClass:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<T>`)` Returns annotations that are*associated*with this element. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getBoolean](https://developer.android.com/reference/kotlin/java/lang/reflect/Field#getBoolean(kotlin.Any))`(`obj:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Gets the value of a static or instance`boolean`field. |
| [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [getByte](https://developer.android.com/reference/kotlin/java/lang/reflect/Field#getByte(kotlin.Any))`(`obj:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Gets the value of a static or instance`byte`field. |
| --- | --- |
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [getChar](https://developer.android.com/reference/kotlin/java/lang/reflect/Field#getChar(kotlin.Any))`(`obj:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Gets the value of a static or instance field of type`char`or of another primitive type convertible to type`char`via a widening conversion. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Annotation](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-annotation/index.html)!\> | [getDeclaredAnnotations](https://developer.android.com/reference/kotlin/java/lang/reflect/Field#getDeclaredAnnotations())`()` Returns annotations that are*directly present*on this element. |
| [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<\*\> | [getDeclaringClass](https://developer.android.com/reference/kotlin/java/lang/reflect/Field#getDeclaringClass())`()` Returns the`Class`object representing the class or interface that declares the field represented by this`Field`object. |
| --- | --- |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [getDouble](https://developer.android.com/reference/kotlin/java/lang/reflect/Field#getDouble(kotlin.Any))`(`obj:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Gets the value of a static or instance field of type`double`or of another primitive type convertible to type`double`via a widening conversion. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getFloat](https://developer.android.com/reference/kotlin/java/lang/reflect/Field#getFloat(kotlin.Any))`(`obj:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Gets the value of a static or instance field of type`float`or of another primitive type convertible to type`float`via a widening conversion. |
| [Type](https://developer.android.com/reference/kotlin/java/lang/reflect/Type) | [getGenericType](https://developer.android.com/reference/kotlin/java/lang/reflect/Field#getGenericType())`()` Returns a`Type`object that represents the declared type for the field represented by this`Field`object. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getInt](https://developer.android.com/reference/kotlin/java/lang/reflect/Field#getInt(kotlin.Any))`(`obj:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Gets the value of a static or instance field of type`int`or of another primitive type convertible to type`int`via a widening conversion. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getLong](https://developer.android.com/reference/kotlin/java/lang/reflect/Field#getLong(kotlin.Any))`(`obj:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Gets the value of a static or instance field of type`long`or of another primitive type convertible to type`long`via a widening conversion. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getModifiers](https://developer.android.com/reference/kotlin/java/lang/reflect/Field#getModifiers())`()` Returns the Java language modifiers for the field represented by this`Field`object, as an integer. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getName](https://developer.android.com/reference/kotlin/java/lang/reflect/Field#getName())`()` Returns the name of the field represented by this`Field`object. |
| [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | [getShort](https://developer.android.com/reference/kotlin/java/lang/reflect/Field#getShort(kotlin.Any))`(`obj:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Gets the value of a static or instance field of type`short`or of another primitive type convertible to type`short`via a widening conversion. |
| [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<\*\> | [getType](https://developer.android.com/reference/kotlin/java/lang/reflect/Field#getType())`()` Returns a`Class`object that identifies the declared type for the field represented by this`Field`object. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/java/lang/reflect/Field#hashCode())`()` Returns a hashcode for this`Field`. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAnnotationPresent](https://developer.android.com/reference/kotlin/java/lang/reflect/Field#isAnnotationPresent(java.lang.Class))`(`annotationType:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<out` ` [Annotation](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-annotation/index.html)!>`)` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEnumConstant](https://developer.android.com/reference/kotlin/java/lang/reflect/Field#isEnumConstant())`()` Returns`true`if this field represents an element of an enumerated type; returns`false`otherwise. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSynthetic](https://developer.android.com/reference/kotlin/java/lang/reflect/Field#isSynthetic())`()` Returns`true`if this field is a synthetic field; returns`false`otherwise. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [set](https://developer.android.com/reference/kotlin/java/lang/reflect/Field#set(kotlin.Any,%20kotlin.Any))`(`obj:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`, `value:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Sets the field represented by this`Field`object on the specified object argument to the specified new value. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBoolean](https://developer.android.com/reference/kotlin/java/lang/reflect/Field#setBoolean(kotlin.Any,%20kotlin.Boolean))`(`obj:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`, `z:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets the value of a field as a`boolean`on the specified object. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setByte](https://developer.android.com/reference/kotlin/java/lang/reflect/Field#setByte(kotlin.Any,%20kotlin.Byte))`(`obj:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`, `b:` ` [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html)`)` Sets the value of a field as a`byte`on the specified object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setChar](https://developer.android.com/reference/kotlin/java/lang/reflect/Field#setChar(kotlin.Any,%20kotlin.Char))`(`obj:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`, `c:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` Sets the value of a field as a`char`on the specified object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDouble](https://developer.android.com/reference/kotlin/java/lang/reflect/Field#setDouble(kotlin.Any,%20kotlin.Double))`(`obj:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`, `d:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Sets the value of a field as a`double`on the specified object. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFloat](https://developer.android.com/reference/kotlin/java/lang/reflect/Field#setFloat(kotlin.Any,%20kotlin.Float))`(`obj:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`, `f:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets the value of a field as a`float`on the specified object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInt](https://developer.android.com/reference/kotlin/java/lang/reflect/Field#setInt(kotlin.Any,%20kotlin.Int))`(`obj:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`, `i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the value of a field as an`int`on the specified object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLong](https://developer.android.com/reference/kotlin/java/lang/reflect/Field#setLong(kotlin.Any,%20kotlin.Long))`(`obj:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`, `l:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the value of a field as a`long`on the specified object. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setShort](https://developer.android.com/reference/kotlin/java/lang/reflect/Field#setShort(kotlin.Any,%20kotlin.Short))`(`obj:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`, `s:` ` [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html)`)` Sets the value of a field as a`short`on the specified object. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toGenericString](https://developer.android.com/reference/kotlin/java/lang/reflect/Field#toGenericString())`()` Returns a string describing this`Field`, including its generic type. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/lang/reflect/Field#toString())`()` Returns a string describing this`Field`. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [AccessibleObject](https://developer.android.com/reference/kotlin/java/lang/reflect/AccessibleObject) |---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Annotation](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-annotation/index.html)!> | [getAnnotations](https://developer.android.com/reference/kotlin/java/lang/reflect/AccessibleObject#getAnnotations())`()` <br /> | | T? | [getDeclaredAnnotation](https://developer.android.com/reference/kotlin/java/lang/reflect/AccessibleObject#getDeclaredAnnotation(java.lang.Class))`(`annotationClass:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<T>`)` <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<T>! | [getDeclaredAnnotationsByType](https://developer.android.com/reference/kotlin/java/lang/reflect/AccessibleObject#getDeclaredAnnotationsByType(java.lang.Class))`(`annotationClass:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<T>`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAccessible](https://developer.android.com/reference/kotlin/java/lang/reflect/AccessibleObject#isAccessible())`()` <br /> Get the value of the`accessible`flag for this object. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAccessible](https://developer.android.com/reference/kotlin/java/lang/reflect/AccessibleObject#setAccessible(kotlin.Boolean))`(`flag:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Set the`accessible`flag for this object to the indicated boolean value. A value of`true`indicates that the reflected object should suppress Java language access checking when it is used. A value of`false`indicates that the reflected object should enforce Java language access checks. First, if there is a security manager, its`checkPermission`method is called with a`ReflectPermission("suppressAccessChecks")`permission. A`SecurityException`is raised if`flag`is`true`but accessibility of this object may not be changed (for example, if this element object is a [Constructor](https://developer.android.com/reference/kotlin/java/lang/reflect/Constructor) object for the class [java.lang.Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)). A`SecurityException`is raised if this object is a object for the class`java.lang.Class`, and`flag`is true. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAccessible](https://developer.android.com/reference/kotlin/java/lang/reflect/AccessibleObject#setAccessible(kotlin.Array,%20kotlin.Boolean))`(`array:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [AccessibleObject](https://developer.android.com/reference/kotlin/java/lang/reflect/AccessibleObject)!>!`, `flag:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Convenience method to set the`accessible`flag for an array of objects with a single security check (for efficiency). First, if there is a security manager, its`checkPermission`method is called with a`ReflectPermission("suppressAccessChecks")`permission. A`SecurityException`is raised if`flag`is`true`but accessibility of any of the elements of the input`array`may not be changed (for example, if the element object is a [Constructor](https://developer.android.com/reference/kotlin/java/lang/reflect/Constructor) object for the class ). In the event of such a SecurityException, the accessibility of objects is set to`flag`for array elements upto (and excluding) the element for which the exception occurred; the accessibility of elements beyond (and including) the element for which the exception occurred is unchanged. <br /> | ||

## Public methods

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Compares this`Field`against the specified object. Returns true if the objects are the same. Two`Field`objects are the same if they were declared by the same class and have the same name and type.

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun get(obj: Any?): Any?
```

Returns the value of the field represented by this`Field`, on the specified object. The value is automatically wrapped in an object if it has a primitive type.

The underlying field's value is obtained as follows:

If the underlying field is a static field, the`obj`argument is ignored; it may be null.

Otherwise, the underlying field is an instance field. If the specified`obj`argument is null, the method throws a`NullPointerException`. If the specified object is not an instance of the class or interface declaring the underlying field, the method throws an`IllegalArgumentException`.

If this`Field`object is enforcing Java language access control, and the underlying field is inaccessible, the method throws an`IllegalAccessException`. If the underlying field is static, the class that declared the field is initialized if it has not already been initialized.

Otherwise, the value is retrieved from the underlying instance or static field. If the field has a primitive type, the value is wrapped in an object before being returned, otherwise it is returned as is.

If the field is hidden in the type of`obj`, the field's value is obtained according to the preceding rules.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `obj` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?:object from which the represented field's value is to be extracted |

| Return ||
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)? | the value of the represented field in object`obj`; primitive values are wrapped in an appropriate object before being returned |

| Exceptions ||
|-----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalAccessException` | if this`Field`object is enforcing Java language access control and the underlying field is inaccessible. |
| `java.lang.IllegalArgumentException` | if the specified object is not an instance of the class or interface declaring the underlying field (or a subclass or implementor thereof). |
| `java.lang.NullPointerException` | if the specified object is null and the field is an instance field. |
| --- | --- |
| `java.lang.ExceptionInInitializerError` | if the initialization provoked by this method fails. |

### getAnnotation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun <T : Annotation!> getAnnotation(annotationClass: Class<T>): T?
```

| Parameters ||
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | the type of the annotation to query for and return if present |
| `annotationClass` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<T\>:the Class object corresponding to the annotation type |

| Return ||
|----|---------------------------------------------------------------------------------------------------|
| T? | this element's annotation for the specified annotation type if present on this element, else null |

| Exceptions ||
|----------------------------------|---------------------------------------|
| `java.lang.NullPointerException` | if the given annotation class is null |

### getAnnotationsByType

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun <T : Annotation!> getAnnotationsByType(annotationClass: Class<T>): Array<T>!
```

Returns annotations that are*associated* with this element. If there are no annotations*associated* with this element, the return value is an array of length 0. The difference between this method and [getAnnotation(java.lang.Class)](https://developer.android.com/reference/kotlin/java/lang/reflect/AnnotatedElement#getAnnotation(java.lang.Class))is that this method detects if its argument is a*repeatable annotation type*(JLS 9.6), and if so, attempts to find one or more annotations of that type by "looking through" a container annotation. The caller of this method is free to modify the returned array; it will have no effect on the arrays returned to other callers.

| Parameters ||
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | the type of the annotation to query for and return if present |
| `annotationClass` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<T\>:the Class object corresponding to the annotation type |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<T>! | all this element's annotations for the specified annotation type if associated with this element, else an array of length zero |

| Exceptions ||
|----------------------------------|---------------------------------------|
| `java.lang.NullPointerException` | if the given annotation class is null |

### getBoolean

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getBoolean(obj: Any?): Boolean
```

Gets the value of a static or instance`boolean`field.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------|
| `obj` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?:the object to extract the`boolean`value from |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | the value of the`boolean`field |

| Exceptions ||
|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalAccessException` | if this`Field`object is enforcing Java language access control and the underlying field is inaccessible. |
| `java.lang.IllegalArgumentException` | if the specified object is not an instance of the class or interface declaring the underlying field (or a subclass or implementor thereof), or if the field value cannot be converted to the type`boolean`by a widening conversion. |
| `java.lang.NullPointerException` | if the specified object is null and the field is an instance field. |
| --- | --- |
| `java.lang.ExceptionInInitializerError` | if the initialization provoked by this method fails. |

**See Also**

- [java.lang.reflect.Field#get](https://developer.android.com/reference/kotlin/java/lang/reflect/Field#get(kotlin.Any)) 

### getByte

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getByte(obj: Any?): Byte
```

Gets the value of a static or instance`byte`field.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------|
| `obj` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?:the object to extract the`byte`value from |

| Return ||
|------------------------------------------------------------------------------|-----------------------------|
| [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | the value of the`byte`field |

| Exceptions ||
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalAccessException` | if this`Field`object is enforcing Java language access control and the underlying field is inaccessible. |
| `java.lang.IllegalArgumentException` | if the specified object is not an instance of the class or interface declaring the underlying field (or a subclass or implementor thereof), or if the field value cannot be converted to the type`byte`by a widening conversion. |
| `java.lang.NullPointerException` | if the specified object is null and the field is an instance field. |
| --- | --- |
| `java.lang.ExceptionInInitializerError` | if the initialization provoked by this method fails. |

**See Also**

- [java.lang.reflect.Field#get](https://developer.android.com/reference/kotlin/java/lang/reflect/Field#get(kotlin.Any)) 

### getChar

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getChar(obj: Any?): Char
```

Gets the value of a static or instance field of type`char`or of another primitive type convertible to type`char`via a widening conversion.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------|
| `obj` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?:the object to extract the`char`value from |

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------|
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | the value of the field converted to type`char` |

| Exceptions ||
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalAccessException` | if this`Field`object is enforcing Java language access control and the underlying field is inaccessible. |
| `java.lang.IllegalArgumentException` | if the specified object is not an instance of the class or interface declaring the underlying field (or a subclass or implementor thereof), or if the field value cannot be converted to the type`char`by a widening conversion. |
| `java.lang.NullPointerException` | if the specified object is null and the field is an instance field. |
| --- | --- |
| `java.lang.ExceptionInInitializerError` | if the initialization provoked by this method fails. |

**See Also**

- [java.lang.reflect.Field#get](https://developer.android.com/reference/kotlin/java/lang/reflect/Field#get(kotlin.Any)) 

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
fun getDeclaringClass(): Class<*>
```

Returns the`Class`object representing the class or interface that declares the field represented by this`Field`object.

| Return ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<*> | an object representing the declaring class of the underlying member |

### getDouble

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDouble(obj: Any?): Double
```

Gets the value of a static or instance field of type`double`or of another primitive type convertible to type`double`via a widening conversion.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------------|
| `obj` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?:the object to extract the`double`value from |

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the value of the field converted to type`double` |

| Exceptions ||
|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalAccessException` | if this`Field`object is enforcing Java language access control and the underlying field is inaccessible. |
| `java.lang.IllegalArgumentException` | if the specified object is not an instance of the class or interface declaring the underlying field (or a subclass or implementor thereof), or if the field value cannot be converted to the type`double`by a widening conversion. |
| `java.lang.NullPointerException` | if the specified object is null and the field is an instance field. |
| --- | --- |
| `java.lang.ExceptionInInitializerError` | if the initialization provoked by this method fails. |

**See Also**

- [java.lang.reflect.Field#get](https://developer.android.com/reference/kotlin/java/lang/reflect/Field#get(kotlin.Any)) 

### getFloat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFloat(obj: Any?): Float
```

Gets the value of a static or instance field of type`float`or of another primitive type convertible to type`float`via a widening conversion.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------------|
| `obj` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?:the object to extract the`float`value from |

| Return ||
|--------------------------------------------------------------------------------|-------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | the value of the field converted to type`float` |

| Exceptions ||
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalAccessException` | if this`Field`object is enforcing Java language access control and the underlying field is inaccessible. |
| `java.lang.IllegalArgumentException` | if the specified object is not an instance of the class or interface declaring the underlying field (or a subclass or implementor thereof), or if the field value cannot be converted to the type`float`by a widening conversion. |
| `java.lang.NullPointerException` | if the specified object is null and the field is an instance field. |
| --- | --- |
| `java.lang.ExceptionInInitializerError` | if the initialization provoked by this method fails. |

**See Also**

- [java.lang.reflect.Field#get](https://developer.android.com/reference/kotlin/java/lang/reflect/Field#get(kotlin.Any)) 

### getGenericType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getGenericType(): Type
```

Returns a`Type`object that represents the declared type for the field represented by this`Field`object.

If the`Type`is a parameterized type, the`Type`object returned must accurately reflect the actual type parameters used in the source code.

If the type of the underlying field is a type variable or a parameterized type, it is created. Otherwise, it is resolved.

| Return ||
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [Type](https://developer.android.com/reference/kotlin/java/lang/reflect/Type) | a`Type`object that represents the declared type for the field represented by this`Field`object |

| Exceptions ||
|---------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| `java.lang.reflect.GenericSignatureFormatError` | if the generic field signature does not conform to the format specified in The Java™ Virtual Machine Specification |
| `java.lang.TypeNotPresentException` | if the generic type signature of the underlying field refers to a non-existent type declaration |
| `java.lang.reflect.MalformedParameterizedTypeException` | if the generic signature of the underlying field refers to a parameterized type that cannot be instantiated for any reason |
| --- | --- |

### getInt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getInt(obj: Any?): Int
```

Gets the value of a static or instance field of type`int`or of another primitive type convertible to type`int`via a widening conversion.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------|
| `obj` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?:the object to extract the`int`value from |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the value of the field converted to type`int` |

| Exceptions ||
|-----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalAccessException` | if this`Field`object is enforcing Java language access control and the underlying field is inaccessible. |
| `java.lang.IllegalArgumentException` | if the specified object is not an instance of the class or interface declaring the underlying field (or a subclass or implementor thereof), or if the field value cannot be converted to the type`int`by a widening conversion. |
| `java.lang.NullPointerException` | if the specified object is null and the field is an instance field. |
| --- | --- |
| `java.lang.ExceptionInInitializerError` | if the initialization provoked by this method fails. |

**See Also**

- [java.lang.reflect.Field#get](https://developer.android.com/reference/kotlin/java/lang/reflect/Field#get(kotlin.Any)) 

### getLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLong(obj: Any?): Long
```

Gets the value of a static or instance field of type`long`or of another primitive type convertible to type`long`via a widening conversion.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------|
| `obj` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?:the object to extract the`long`value from |

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the value of the field converted to type`long` |

| Exceptions ||
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalAccessException` | if this`Field`object is enforcing Java language access control and the underlying field is inaccessible. |
| `java.lang.IllegalArgumentException` | if the specified object is not an instance of the class or interface declaring the underlying field (or a subclass or implementor thereof), or if the field value cannot be converted to the type`long`by a widening conversion. |
| `java.lang.NullPointerException` | if the specified object is null and the field is an instance field. |
| --- | --- |
| `java.lang.ExceptionInInitializerError` | if the initialization provoked by this method fails. |

**See Also**

- [java.lang.reflect.Field#get](https://developer.android.com/reference/kotlin/java/lang/reflect/Field#get(kotlin.Any)) 

### getModifiers

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getModifiers(): Int
```

Returns the Java language modifiers for the field represented by this`Field`object, as an integer. The`Modifier`class should be used to decode the modifiers.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the Java language modifiers for the underlying member |

**See Also**

- [java.lang.reflect.Modifier](https://developer.android.com/reference/kotlin/java/lang/reflect/Modifier) 

### getName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getName(): String
```

Returns the name of the field represented by this`Field`object.

| Return ||
|----------------------------------------------------------------------------------|------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the simple name of the underlying member |

### getShort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getShort(obj: Any?): Short
```

Gets the value of a static or instance field of type`short`or of another primitive type convertible to type`short`via a widening conversion.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------------|
| `obj` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?:the object to extract the`short`value from |

| Return ||
|--------------------------------------------------------------------------------|-------------------------------------------------|
| [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html) | the value of the field converted to type`short` |

| Exceptions ||
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalAccessException` | if this`Field`object is enforcing Java language access control and the underlying field is inaccessible. |
| `java.lang.IllegalArgumentException` | if the specified object is not an instance of the class or interface declaring the underlying field (or a subclass or implementor thereof), or if the field value cannot be converted to the type`short`by a widening conversion. |
| `java.lang.NullPointerException` | if the specified object is null and the field is an instance field. |
| --- | --- |
| `java.lang.ExceptionInInitializerError` | if the initialization provoked by this method fails. |

**See Also**

- [java.lang.reflect.Field#get](https://developer.android.com/reference/kotlin/java/lang/reflect/Field#get(kotlin.Any)) 

### getType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getType(): Class<*>
```

Returns a`Class`object that identifies the declared type for the field represented by this`Field`object.

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<*> | a`Class`object identifying the declared type of the field represented by this object |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

Returns a hashcode for this`Field`. This is computed as the exclusive-or of the hashcodes for the underlying field's declaring class name and its name.

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### isAnnotationPresent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isAnnotationPresent(annotationType: Class<out Annotation!>): Boolean
```

| Parameters ||
|-------------------|-------------------------------------------------------|
| `annotationClass` | the Class object corresponding to the annotation type |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if an annotation for the specified annotation type is present on this element, else false |

| Exceptions ||
|----------------------------------|---------------------------------------|
| `java.lang.NullPointerException` | if the given annotation class is null |

### isEnumConstant

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isEnumConstant(): Boolean
```

Returns`true`if this field represents an element of an enumerated type; returns`false`otherwise.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if and only if this field represents an element of an enumerated type. |

### isSynthetic

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isSynthetic(): Boolean
```

Returns`true`if this field is a synthetic field; returns`false`otherwise.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if and only if this field is a synthetic field as defined by the Java Language Specification. |

### set

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun set(
    obj: Any?, 
    value: Any?
): Unit
```

Sets the field represented by this`Field`object on the specified object argument to the specified new value. The new value is automatically unwrapped if the underlying field has a primitive type.

The operation proceeds as follows:

If the underlying field is static, the`obj`argument is ignored; it may be null.

Otherwise the underlying field is an instance field. If the specified object argument is null, the method throws a`NullPointerException`. If the specified object argument is not an instance of the class or interface declaring the underlying field, the method throws an`IllegalArgumentException`.

If this`Field`object is enforcing Java language access control, and the underlying field is inaccessible, the method throws an`IllegalAccessException`.

If the underlying field is final, this`Field`object has*write*access if and only if the following conditions are met:

- [setAccessible(true)](https://developer.android.com/reference/kotlin/java/lang/reflect/AccessibleObject#setAccessible(kotlin.Boolean))has succeeded for this`Field`object;
- the field is non-static; and
- the field's declaring class is not a [record class](https://developer.android.com/reference/kotlin/java/lang/Class.html#isRecord()).

If any of the above checks is not met, this method throws an`IllegalAccessException`.

Setting a final field in this way is meaningful only during deserialization or reconstruction of instances of classes with blank final fields, before they are made available for access by other parts of a program. Use in any other context may have unpredictable effects, including cases in which other parts of a program continue to use the original value of this field.

If the underlying field is of a primitive type, an unwrapping conversion is attempted to convert the new value to a value of a primitive type. If this attempt fails, the method throws an`IllegalArgumentException`.

If, after possible unwrapping, the new value cannot be converted to the type of the underlying field by an identity or widening conversion, the method throws an`IllegalArgumentException`.

If the underlying field is static, the class that declared the field is initialized if it has not already been initialized.

The field is set to the possibly unwrapped and widened new value.

If the field is hidden in the type of`obj`, the field's value is set according to the preceding rules.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------|
| `obj` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?:the object whose field should be modified |
| `value` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?:the new value for the field of`obj`being modified |

| Exceptions ||
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalAccessException` | if this`Field`object is enforcing Java language access control and the underlying field is either inaccessible or final. |
| `java.lang.IllegalArgumentException` | if the specified object is not an instance of the class or interface declaring the underlying field (or a subclass or implementor thereof), or if an unwrapping conversion fails. |
| `java.lang.NullPointerException` | if the specified object is null and the field is an instance field. |
| --- | --- |
| `java.lang.ExceptionInInitializerError` | if the initialization provoked by this method fails. |

### setBoolean

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setBoolean(
    obj: Any?, 
    z: Boolean
): Unit
```

Sets the value of a field as a`boolean`on the specified object. This method is equivalent to`set(obj, zObj)`, where`zObj`is a`Boolean`object and`zObj.booleanValue() == z`.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------------------|
| `obj` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?:the object whose field should be modified |
| `z` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):the new value for the field of`obj`being modified |

| Exceptions ||
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalAccessException` | if this`Field`object is enforcing Java language access control and the underlying field is either inaccessible or final. |
| `java.lang.IllegalArgumentException` | if the specified object is not an instance of the class or interface declaring the underlying field (or a subclass or implementor thereof), or if an unwrapping conversion fails. |
| `java.lang.NullPointerException` | if the specified object is null and the field is an instance field. |
| --- | --- |
| `java.lang.ExceptionInInitializerError` | if the initialization provoked by this method fails. |

**See Also**

- [java.lang.reflect.Field#set](https://developer.android.com/reference/kotlin/java/lang/reflect/Field#set(kotlin.Any,%20kotlin.Any)) 

### setByte

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setByte(
    obj: Any?, 
    b: Byte
): Unit
```

Sets the value of a field as a`byte`on the specified object. This method is equivalent to`set(obj, bObj)`, where`bObj`is a`Byte`object and`bObj.byteValue() == b`.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------------|
| `obj` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?:the object whose field should be modified |
| `b` | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html):the new value for the field of`obj`being modified |

| Exceptions ||
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalAccessException` | if this`Field`object is enforcing Java language access control and the underlying field is either inaccessible or final. |
| `java.lang.IllegalArgumentException` | if the specified object is not an instance of the class or interface declaring the underlying field (or a subclass or implementor thereof), or if an unwrapping conversion fails. |
| `java.lang.NullPointerException` | if the specified object is null and the field is an instance field. |
| --- | --- |
| `java.lang.ExceptionInInitializerError` | if the initialization provoked by this method fails. |

**See Also**

- [java.lang.reflect.Field#set](https://developer.android.com/reference/kotlin/java/lang/reflect/Field#set(kotlin.Any,%20kotlin.Any)) 

### setChar

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setChar(
    obj: Any?, 
    c: Char
): Unit
```

Sets the value of a field as a`char`on the specified object. This method is equivalent to`set(obj, cObj)`, where`cObj`is a`Character`object and`cObj.charValue() == c`.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------------|
| `obj` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?:the object whose field should be modified |
| `c` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):the new value for the field of`obj`being modified |

| Exceptions ||
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalAccessException` | if this`Field`object is enforcing Java language access control and the underlying field is either inaccessible or final. |
| `java.lang.IllegalArgumentException` | if the specified object is not an instance of the class or interface declaring the underlying field (or a subclass or implementor thereof), or if an unwrapping conversion fails. |
| `java.lang.NullPointerException` | if the specified object is null and the field is an instance field. |
| --- | --- |
| `java.lang.ExceptionInInitializerError` | if the initialization provoked by this method fails. |

**See Also**

- [java.lang.reflect.Field#set](https://developer.android.com/reference/kotlin/java/lang/reflect/Field#set(kotlin.Any,%20kotlin.Any)) 

### setDouble

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setDouble(
    obj: Any?, 
    d: Double
): Unit
```

Sets the value of a field as a`double`on the specified object. This method is equivalent to`set(obj, dObj)`, where`dObj`is a`Double`object and`dObj.doubleValue() == d`.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------------------------|
| `obj` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?:the object whose field should be modified |
| `d` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the new value for the field of`obj`being modified |

| Exceptions ||
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalAccessException` | if this`Field`object is enforcing Java language access control and the underlying field is either inaccessible or final. |
| `java.lang.IllegalArgumentException` | if the specified object is not an instance of the class or interface declaring the underlying field (or a subclass or implementor thereof), or if an unwrapping conversion fails. |
| `java.lang.NullPointerException` | if the specified object is null and the field is an instance field. |
| --- | --- |
| `java.lang.ExceptionInInitializerError` | if the initialization provoked by this method fails. |

**See Also**

- [java.lang.reflect.Field#set](https://developer.android.com/reference/kotlin/java/lang/reflect/Field#set(kotlin.Any,%20kotlin.Any)) 

### setFloat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setFloat(
    obj: Any?, 
    f: Float
): Unit
```

Sets the value of a field as a`float`on the specified object. This method is equivalent to`set(obj, fObj)`, where`fObj`is a`Float`object and`fObj.floatValue() == f`.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------------|
| `obj` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?:the object whose field should be modified |
| `f` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):the new value for the field of`obj`being modified |

| Exceptions ||
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalAccessException` | if this`Field`object is enforcing Java language access control and the underlying field is either inaccessible or final. |
| `java.lang.IllegalArgumentException` | if the specified object is not an instance of the class or interface declaring the underlying field (or a subclass or implementor thereof), or if an unwrapping conversion fails. |
| `java.lang.NullPointerException` | if the specified object is null and the field is an instance field. |
| --- | --- |
| `java.lang.ExceptionInInitializerError` | if the initialization provoked by this method fails. |

**See Also**

- [java.lang.reflect.Field#set](https://developer.android.com/reference/kotlin/java/lang/reflect/Field#set(kotlin.Any,%20kotlin.Any)) 

### setInt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setInt(
    obj: Any?, 
    i: Int
): Unit
```

Sets the value of a field as an`int`on the specified object. This method is equivalent to`set(obj, iObj)`, where`iObj`is a`Integer`object and`iObj.intValue() == i`.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------------------|
| `obj` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?:the object whose field should be modified |
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new value for the field of`obj`being modified |

| Exceptions ||
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalAccessException` | if this`Field`object is enforcing Java language access control and the underlying field is either inaccessible or final. |
| `java.lang.IllegalArgumentException` | if the specified object is not an instance of the class or interface declaring the underlying field (or a subclass or implementor thereof), or if an unwrapping conversion fails. |
| `java.lang.NullPointerException` | if the specified object is null and the field is an instance field. |
| --- | --- |
| `java.lang.ExceptionInInitializerError` | if the initialization provoked by this method fails. |

**See Also**

- [java.lang.reflect.Field#set](https://developer.android.com/reference/kotlin/java/lang/reflect/Field#set(kotlin.Any,%20kotlin.Any)) 

### setLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setLong(
    obj: Any?, 
    l: Long
): Unit
```

Sets the value of a field as a`long`on the specified object. This method is equivalent to`set(obj, lObj)`, where`lObj`is a`Long`object and`lObj.longValue() == l`.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------------|
| `obj` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?:the object whose field should be modified |
| `l` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the new value for the field of`obj`being modified |

| Exceptions ||
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalAccessException` | if this`Field`object is enforcing Java language access control and the underlying field is either inaccessible or final. |
| `java.lang.IllegalArgumentException` | if the specified object is not an instance of the class or interface declaring the underlying field (or a subclass or implementor thereof), or if an unwrapping conversion fails. |
| `java.lang.NullPointerException` | if the specified object is null and the field is an instance field. |
| --- | --- |
| `java.lang.ExceptionInInitializerError` | if the initialization provoked by this method fails. |

**See Also**

- [java.lang.reflect.Field#set](https://developer.android.com/reference/kotlin/java/lang/reflect/Field#set(kotlin.Any,%20kotlin.Any)) 

### setShort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setShort(
    obj: Any?, 
    s: Short
): Unit
```

Sets the value of a field as a`short`on the specified object. This method is equivalent to`set(obj, sObj)`, where`sObj`is a`Short`object and`sObj.shortValue() == s`.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------------|
| `obj` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?:the object whose field should be modified |
| `s` | [Short](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-short/index.html):the new value for the field of`obj`being modified |

| Exceptions ||
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalAccessException` | if this`Field`object is enforcing Java language access control and the underlying field is either inaccessible or final. |
| `java.lang.IllegalArgumentException` | if the specified object is not an instance of the class or interface declaring the underlying field (or a subclass or implementor thereof), or if an unwrapping conversion fails. |
| `java.lang.NullPointerException` | if the specified object is null and the field is an instance field. |
| --- | --- |
| `java.lang.ExceptionInInitializerError` | if the initialization provoked by this method fails. |

**See Also**

- [java.lang.reflect.Field#set](https://developer.android.com/reference/kotlin/java/lang/reflect/Field#set(kotlin.Any,%20kotlin.Any)) 

### toGenericString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toGenericString(): String
```

Returns a string describing this`Field`, including its generic type. The format is the access modifiers for the field, if any, followed by the generic field type, followed by a space, followed by the fully-qualified name of the class declaring the field, followed by a period, followed by the name of the field.

The modifiers are placed in canonical order as specified by "The Java Language Specification". This is`public`,`protected`or`private`first, and then other modifiers in the following order:`static`,`final`,`transient`,`volatile`.

| Return ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string describing this`Field`, including its generic type |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Returns a string describing this`Field`. The format is the access modifiers for the field, if any, followed by the field type, followed by a space, followed by the fully-qualified name of the class declaring the field, followed by a period, followed by the name of the field. For example: 

```kotlin
public static final int java.lang.Thread.MIN_PRIORITY
     private int java.io.FileDescriptor.fd
  
```

<br />

The modifiers are placed in canonical order as specified by "The Java Language Specification". This is`public`,`protected`or`private`first, and then other modifiers in the following order:`static`,`final`,`transient`,`volatile`.

| Return ||
|----------------------------------------------------------------------------------|---------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string describing this`Field` |
