# Parameter

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Parameter

```
class Parameter : AnnotatedElement
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.lang.reflect.Parameter](../java/lang/reflect/Parameter.md) |

Information about method parameters. A`Parameter`provides information about method parameters, including its name and modifiers. It also provides an alternate means of obtaining attributes for the parameter.

## Summary

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../java/lang/reflect/Parameter.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Compares based on the executable and the index. |
| T? | [getAnnotation](../java/lang/reflect/Parameter.md))`(`annotationClass:` ` [Class](../java/lang/Class.md)<T>`)` Returns this element's annotation for the specified type if such an annotation is*present*, else null. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Annotation](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-annotation/index.html)!\> | [getAnnotations](../java/lang/reflect/Parameter.md))`()` Returns annotations that are*present*on this element. |
| --- | --- |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>! | [getAnnotationsByType](../java/lang/reflect/Parameter.md))`(`annotationClass:` ` [Class](../java/lang/Class.md)<T>`)` Returns annotations that are*associated*with this element. |
| T? | [getDeclaredAnnotation](../java/lang/reflect/Parameter.md))`(`annotationClass:` ` [Class](../java/lang/Class.md)<T>`)` <br /> |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Annotation](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-annotation/index.html)!\> | [getDeclaredAnnotations](../java/lang/reflect/Parameter.md))`()` Returns annotations that are*directly present*on this element. |
| --- | --- |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>! | [getDeclaredAnnotationsByType](../java/lang/reflect/Parameter.md))`(`annotationClass:` ` [Class](../java/lang/Class.md)<T>`)` <br /> |
| [Executable](../java/lang/reflect/Executable.md) | [getDeclaringExecutable](../java/lang/reflect/Parameter.md))`()` Return the`Executable`which declares this parameter. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getModifiers](../java/lang/reflect/Parameter.md))`()` Get the modifier flags for this the parameter represented by this`Parameter`object. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getName](../java/lang/reflect/Parameter.md))`()` Returns the name of the parameter. |
| [Type](../java/lang/reflect/Type.md) | [getParameterizedType](../java/lang/reflect/Parameter.md))`()` Returns a`Type`object that identifies the parameterized type for the parameter represented by this`Parameter`object. |
| [Class](../java/lang/Class.md)\<\*\> | [getType](../java/lang/reflect/Parameter.md))`()` Returns a`Class`object that identifies the declared type for the parameter represented by this`Parameter`object. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../java/lang/reflect/Parameter.md))`()` Returns a hash code based on the executable's hash code and the index. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isImplicit](../java/lang/reflect/Parameter.md))`()` Returns`true`if this parameter is implicitly declared in source code; returns`false`otherwise. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isNamePresent](../java/lang/reflect/Parameter.md))`()` Returns true if the parameter has a name; returns false otherwise. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSynthetic](../java/lang/reflect/Parameter.md))`()` Returns`true`if this parameter is neither implicitly nor explicitly declared in source code; returns`false`otherwise. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isVarArgs](../java/lang/reflect/Parameter.md))`()` Returns`true`if this parameter represents a variable argument list; returns`false`otherwise. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../java/lang/reflect/Parameter.md))`()` Returns a string describing this parameter. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [AnnotatedElement](../java/lang/reflect/AnnotatedElement.md) |------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAnnotationPresent](../java/lang/reflect/AnnotatedElement.md))`(`annotationClass:` ` [Class](../java/lang/Class.md)<out` ` [Annotation](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-annotation/index.html)!>`)` <br /> Returns true if an annotation for the specified type is*present*on this element, else false. This method is designed primarily for convenient access to marker annotations. The truth value returned by this method is equivalent to:`getAnnotation(annotationClass) != null` The body of the default method is specified to be the code above. <br /> | ||

## Public methods

### equals

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Compares based on the executable and the index.

| Parameters ||
|-------|------------------------|
| `obj` | The object to compare. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Whether or not this is equal to the argument. |

### getAnnotation

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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

### getAnnotations

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAnnotations(): Array<Annotation!>
```

Returns annotations that are*present* on this element. If there are no annotations*present*on this element, the return value is an array of length 0. The caller of this method is free to modify the returned array; it will have no effect on the arrays returned to other callers.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Annotation](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-annotation/index.html)!> | annotations present on this element |

### getAnnotationsByType

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun <T : Annotation!> getAnnotationsByType(annotationClass: Class<T>): Array<T>!
```

Returns annotations that are*associated* with this element. If there are no annotations*associated* with this element, the return value is an array of length 0. The difference between this method and [getAnnotation(java.lang.Class)](../java/lang/reflect/AnnotatedElement.md))is that this method detects if its argument is a*repeatable annotation type*(JLS 9.6), and if so, attempts to find one or more annotations of that type by "looking through" a container annotation. The caller of this method is free to modify the returned array; it will have no effect on the arrays returned to other callers.

| Parameters ||
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | the type of the annotation to query for and return if present |
| `annotationClass` | [Class](../java/lang/Class.md)\<T\>:the Class object corresponding to the annotation type |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<T>! | all this element's annotations for the specified annotation type if associated with this element, else an array of length zero |

| Exceptions ||
|----------------------------------|---------------------------------------|
| `java.lang.NullPointerException` | if the given annotation class is null |

### getDeclaredAnnotation

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun <T : Annotation!> getDeclaredAnnotation(annotationClass: Class<T>): T?
```

| Parameters ||
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | the type of the annotation to query for and return if directly present |
| `annotationClass` | [Class](../java/lang/Class.md)\<T\>:the Class object corresponding to the annotation type |

| Return ||
|----|------------------------------------------------------------------------------------------------------------|
| T? | this element's annotation for the specified annotation type if directly present on this element, else null |

| Exceptions ||
|----------------------------------|---------------------------------------|
| `java.lang.NullPointerException` | if the given annotation class is null |

### getDeclaredAnnotations

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDeclaredAnnotations(): Array<Annotation!>
```

Returns annotations that are*directly present* on this element. This method ignores inherited annotations. If there are no annotations*directly present*on this element, the return value is an array of length 0. The caller of this method is free to modify the returned array; it will have no effect on the arrays returned to other callers.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Annotation](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-annotation/index.html)!> | annotations directly present on this element |

### getDeclaredAnnotationsByType

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun <T : Annotation!> getDeclaredAnnotationsByType(annotationClass: Class<T>): Array<T>!
```

| Parameters ||
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | the type of the annotation to query for and return if directly or indirectly present |
| `annotationClass` | [Class](../java/lang/Class.md)\<T\>:the Class object corresponding to the annotation type |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<T>! | all this element's annotations for the specified annotation type if directly or indirectly present on this element, else an array of length zero |

| Exceptions ||
|----------------------------------|---------------------------------------|
| `java.lang.NullPointerException` | if the given annotation class is null |

### getDeclaringExecutable

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDeclaringExecutable(): Executable
```

Return the`Executable`which declares this parameter.

| Return ||
|-------------------------------------------------------------------------------------------|------------------------------------------|
| [Executable](../java/lang/reflect/Executable.md) | The`Executable`declaring this parameter. |

### getModifiers

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getModifiers(): Int
```

Get the modifier flags for this the parameter represented by this`Parameter`object.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The modifier flags for this parameter. |

### getName

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getName(): String
```

Returns the name of the parameter. If the parameter's name is [present](../java/lang/reflect/Parameter.md)), then this method returns the name provided by the class file. Otherwise, this method synthesizes a name of the form argN, where N is the index of the parameter in the descriptor of the method which declares the parameter.

| Return ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | The name of the parameter, either provided by the class file or synthesized if the class file does not provide a name. |

### getParameterizedType

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getParameterizedType(): Type
```

Returns a`Type`object that identifies the parameterized type for the parameter represented by this`Parameter`object.

| Return ||
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [Type](../java/lang/reflect/Type.md) | a`Type`object identifying the parameterized type of the parameter represented by this object |

### getType

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getType(): Class<*>
```

Returns a`Class`object that identifies the declared type for the parameter represented by this`Parameter`object.

| Return ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [Class](../java/lang/Class.md)<*> | a`Class`object identifying the declared type of the parameter represented by this object |

### hashCode

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

Returns a hash code based on the executable's hash code and the index.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | A hash code based on the executable's hash code. |

### isImplicit

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isImplicit(): Boolean
```

Returns`true`if this parameter is implicitly declared in source code; returns`false`otherwise.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if and only if this parameter is implicitly declared as defined by The Java™ Language Specification. |

### isNamePresent

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isNamePresent(): Boolean
```

Returns true if the parameter has a name; returns false otherwise. Whether a parameter has a name is determined by compiler options and whether the parameter is synthesized.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if and only if the parameter has a name |

### isSynthetic

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isSynthetic(): Boolean
```

Returns`true`if this parameter is neither implicitly nor explicitly declared in source code; returns`false`otherwise.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if and only if this parameter is a synthetic construct as defined by The Java™ Language Specification. |

### isVarArgs

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isVarArgs(): Boolean
```

Returns`true`if this parameter represents a variable argument list; returns`false`otherwise.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if an only if this parameter represents a variable argument list. |

### toString

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

Returns a string describing this parameter. The format is the modifiers for the parameter, if any, in canonical order as recommended by The Java™ Language Specification, followed by the fully- qualified type of the parameter (excluding the last \[\] if the parameter is variable arity), followed by "..." if the parameter is variable arity, followed by a space, followed by the name of the parameter.

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | A string representation of the parameter and associated information. |
