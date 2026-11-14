# RecordComponent

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RecordComponent

```
class RecordComponent : AnnotatedElement
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.lang.reflect.RecordComponent](RecordComponent.md) |

A`RecordComponent`provides information about, and dynamic access to, a component of a record class.

## Summary

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Method](Method.md) | [getAccessor](RecordComponent.md))`()` Returns a`Method`that represents the accessor for this record component. |
| T? | [getAnnotation](RecordComponent.md))`(`annotationClass:` ` [Class](../java.lang/Class.md)<T>`)` Returns this element's annotation for the specified type if such an annotation is*present*, else null. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Annotation](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-annotation/index.html)!\> | [getAnnotations](RecordComponent.md))`()` Returns annotations that are*present*on this element. |
| --- | --- |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Annotation](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-annotation/index.html)!\> | [getDeclaredAnnotations](RecordComponent.md))`()` Returns annotations that are*directly present*on this element. |
| [Class](../java.lang/Class.md)\<\*\> | [getDeclaringRecord](RecordComponent.md))`()` Returns the record class which declares this record component. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getGenericSignature](RecordComponent.md))`()` Returns a`String`that describes the generic type signature for this record component. |
| --- | --- |
| [Type](Type.md) | [getGenericType](RecordComponent.md))`()` Returns a`Type`object that represents the declared type for this record component. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getName](RecordComponent.md))`()` Returns the name of this record component. |
| [Class](../java.lang/Class.md)\<\*\> | [getType](RecordComponent.md))`()` Returns a`Class`that identifies the declared type for this record component. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](RecordComponent.md))`()` Returns a string describing this record component. |

| Inherited functions ||
|---|---|
| From class [AnnotatedElement](AnnotatedElement.md) |------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<T>! | [getAnnotationsByType](AnnotatedElement.md))`(`annotationClass:` ` [Class](../java.lang/Class.md)<T>`)` <br /> Returns annotations that are*associated* with this element. If there are no annotations*associated* with this element, the return value is an array of length 0. The difference between this method and [getAnnotation(java.lang.Class)](AnnotatedElement.md))is that this method detects if its argument is a*repeatable annotation type*(JLS 9.6), and if so, attempts to find one or more annotations of that type by "looking through" a container annotation. The caller of this method is free to modify the returned array; it will have no effect on the arrays returned to other callers. <br /> | | T? | [getDeclaredAnnotation](AnnotatedElement.md))`(`annotationClass:` ` [Class](../java.lang/Class.md)<T>`)` <br /> Returns this element's annotation for the specified type if such an annotation is*directly present*, else null. This method ignores inherited annotations. (Returns null if no annotations are directly present on this element.) <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<T>! | [getDeclaredAnnotationsByType](AnnotatedElement.md))`(`annotationClass:` ` [Class](../java.lang/Class.md)<T>`)` <br /> Returns this element's annotation(s) for the specified type if such annotations are either*directly present* or*indirectly present* . This method ignores inherited annotations. If there are no specified annotations directly or indirectly present on this element, the return value is an array of length 0. The difference between this method and [getDeclaredAnnotation(java.lang.Class)](AnnotatedElement.md))is that this method detects if its argument is a*repeatable annotation type*(JLS 9.6), and if so, attempts to find one or more annotations of that type by "looking through" a container annotation if one is present. The caller of this method is free to modify the returned array; it will have no effect on the arrays returned to other callers. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAnnotationPresent](AnnotatedElement.md))`(`annotationClass:` ` [Class](../java.lang/Class.md)<out` ` [Annotation](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-annotation/index.html)!>`)` <br /> Returns true if an annotation for the specified type is*present*on this element, else false. This method is designed primarily for convenient access to marker annotations. The truth value returned by this method is equivalent to:`getAnnotation(annotationClass) != null` The body of the default method is specified to be the code above. <br /> | ||

## Public methods

### getAccessor

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAccessor(): Method
```

Returns a`Method`that represents the accessor for this record component.

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [Method](Method.md) | a`Method`that represents the accessor for this record component |

### getAnnotation

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun <T : Annotation!> getAnnotation(annotationClass: Class<T>): T?
```

Returns this element's annotation for the specified type if such an annotation is*present*, else null.

Note that any annotation returned by this method is a declaration annotation.

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

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAnnotations(): Array<Annotation!>
```

Returns annotations that are*present* on this element. If there are no annotations*present*on this element, the return value is an array of length 0. The caller of this method is free to modify the returned array; it will have no effect on the arrays returned to other callers.

Note that any annotations returned by this method are declaration annotations.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Annotation](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-annotation/index.html)!> | annotations present on this element |

### getDeclaredAnnotations

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDeclaredAnnotations(): Array<Annotation!>
```

Returns annotations that are*directly present* on this element. This method ignores inherited annotations. If there are no annotations*directly present*on this element, the return value is an array of length 0. The caller of this method is free to modify the returned array; it will have no effect on the arrays returned to other callers.

Note that any annotations returned by this method are declaration annotations.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Annotation](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-annotation/index.html)!> | annotations directly present on this element |

### getDeclaringRecord

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDeclaringRecord(): Class<*>
```

Returns the record class which declares this record component.

| Return ||
|----------------------------------------------------------------------------------|---------------------------------------------------|
| [Class](../java.lang/Class.md)<*> | The record class declaring this record component. |

### getGenericSignature

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getGenericSignature(): String?
```

Returns a`String`that describes the generic type signature for this record component.

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | a`String`that describes the generic type signature for this record component |

### getGenericType

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getGenericType(): Type
```

Returns a`Type`object that represents the declared type for this record component.

If the declared type of the record component is a parameterized type, the`Type`object returned reflects the actual type arguments used in the source code.

If the type of the underlying record component is a type variable or a parameterized type, it is created. Otherwise, it is resolved.

| Return ||
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [Type](Type.md) | a`Type`object that represents the declared type for this record component |

| Exceptions ||
|---------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.reflect.GenericSignatureFormatError` | if the generic record component signature does not conform to the format specified in The Java Virtual Machine Specification |
| `java.lang.TypeNotPresentException` | if the generic type signature of the underlying record component refers to a non-existent type declaration |
| `java.lang.reflect.MalformedParameterizedTypeException` | if the generic signature of the underlying record component refers to a parameterized type that cannot be instantiated for any reason |
| --- | --- |

### getName

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getName(): String
```

Returns the name of this record component.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the name of this record component |

### getType

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getType(): Class<*>
```

Returns a`Class`that identifies the declared type for this record component.

| Return ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [Class](../java.lang/Class.md)<*> | a`Class`identifying the declared type of the component represented by this record component |

### toString

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Returns a string describing this record component. The format is the record component type, followed by a space, followed by the name of the record component. For example: 

```kotlin
java.lang.String name
     int age
  
```

<br />

| Return ||
|----------------------------------------------------------------------------------|-------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string describing this record component |
