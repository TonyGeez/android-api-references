# ElementType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ElementType

```
class ElementType
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [kotlin.Enum](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-enum/index.html)\< [java.lang.annotation.ElementType](https://developer.android.com/reference/kotlin/java/lang/annotation/ElementType#)\> ||
| | ↳ | [java.lang.annotation.ElementType](https://developer.android.com/reference/kotlin/java/lang/annotation/ElementType#) |

| Known Direct Subclasses [ElementType.ANNOTATION_TYPE](https://developer.android.com/reference/kotlin/java/lang/annotation/ElementType#ENUM_VALUE:ANNOTATION_TYPE), [ElementType.CONSTRUCTOR](https://developer.android.com/reference/kotlin/java/lang/annotation/ElementType#ENUM_VALUE:CONSTRUCTOR), [ElementType.FIELD](https://developer.android.com/reference/kotlin/java/lang/annotation/ElementType#ENUM_VALUE:FIELD), [ElementType.LOCAL_VARIABLE](https://developer.android.com/reference/kotlin/java/lang/annotation/ElementType#ENUM_VALUE:LOCAL_VARIABLE), [ElementType.METHOD](https://developer.android.com/reference/kotlin/java/lang/annotation/ElementType#ENUM_VALUE:METHOD), [ElementType.MODULE](https://developer.android.com/reference/kotlin/java/lang/annotation/ElementType#ENUM_VALUE:MODULE), [ElementType.PACKAGE](https://developer.android.com/reference/kotlin/java/lang/annotation/ElementType#ENUM_VALUE:PACKAGE), [ElementType.PARAMETER](https://developer.android.com/reference/kotlin/java/lang/annotation/ElementType#ENUM_VALUE:PARAMETER), [ElementType.RECORD_COMPONENT](https://developer.android.com/reference/kotlin/java/lang/annotation/ElementType#ENUM_VALUE:RECORD_COMPONENT), [ElementType.TYPE](https://developer.android.com/reference/kotlin/java/lang/annotation/ElementType#ENUM_VALUE:TYPE), [ElementType.TYPE_PARAMETER](https://developer.android.com/reference/kotlin/java/lang/annotation/ElementType#ENUM_VALUE:TYPE_PARAMETER), [ElementType.TYPE_USE](https://developer.android.com/reference/kotlin/java/lang/annotation/ElementType#ENUM_VALUE:TYPE_USE) |---------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------| | [ElementType.ANNOTATION_TYPE](https://developer.android.com/reference/kotlin/java/lang/annotation/ElementType#ENUM_VALUE:ANNOTATION_TYPE) | Annotation interface declaration (Formerly known as an annotation type.) | | [ElementType.CONSTRUCTOR](https://developer.android.com/reference/kotlin/java/lang/annotation/ElementType#ENUM_VALUE:CONSTRUCTOR) | Constructor declaration | | [ElementType.FIELD](https://developer.android.com/reference/kotlin/java/lang/annotation/ElementType#ENUM_VALUE:FIELD) | Field declaration (includes enum constants) | | [ElementType.LOCAL_VARIABLE](https://developer.android.com/reference/kotlin/java/lang/annotation/ElementType#ENUM_VALUE:LOCAL_VARIABLE) | Local variable declaration | | [ElementType.METHOD](https://developer.android.com/reference/kotlin/java/lang/annotation/ElementType#ENUM_VALUE:METHOD) | Method declaration | | [ElementType.MODULE](https://developer.android.com/reference/kotlin/java/lang/annotation/ElementType#ENUM_VALUE:MODULE) | Module declaration. | | [ElementType.PACKAGE](https://developer.android.com/reference/kotlin/java/lang/annotation/ElementType#ENUM_VALUE:PACKAGE) | Package declaration | | [ElementType.PARAMETER](https://developer.android.com/reference/kotlin/java/lang/annotation/ElementType#ENUM_VALUE:PARAMETER) | Formal parameter declaration | | [ElementType.RECORD_COMPONENT](https://developer.android.com/reference/kotlin/java/lang/annotation/ElementType#ENUM_VALUE:RECORD_COMPONENT) | Record component | | [ElementType.TYPE](https://developer.android.com/reference/kotlin/java/lang/annotation/ElementType#ENUM_VALUE:TYPE) | Class, interface (including annotation interface), enum, or record declaration | | [ElementType.TYPE_PARAMETER](https://developer.android.com/reference/kotlin/java/lang/annotation/ElementType#ENUM_VALUE:TYPE_PARAMETER) | Type parameter declaration | | [ElementType.TYPE_USE](https://developer.android.com/reference/kotlin/java/lang/annotation/ElementType#ENUM_VALUE:TYPE_USE) | Use of a type | |

The constants of this enumerated class provide a simple classification of the syntactic locations where annotations may appear in a Java program. These constants are used in [Target](https://developer.android.com/reference/kotlin/java/lang/annotation/Target) meta-annotations to specify where it is legal to write annotations of a given type.

The syntactic locations where annotations may appear are split into*declaration contexts* , where annotations apply to declarations, and*type contexts*, where annotations apply to types used in declarations and expressions.

The constants [ANNOTATION_TYPE](https://developer.android.com/reference/kotlin/java/lang/annotation/ElementType#), [CONSTRUCTOR](https://developer.android.com/reference/kotlin/java/lang/annotation/ElementType#), [FIELD](https://developer.android.com/reference/kotlin/java/lang/annotation/ElementType#), [LOCAL_VARIABLE](https://developer.android.com/reference/kotlin/java/lang/annotation/ElementType#), [METHOD](https://developer.android.com/reference/kotlin/java/lang/annotation/ElementType#), [PACKAGE](https://developer.android.com/reference/kotlin/java/lang/annotation/ElementType#), [MODULE](https://developer.android.com/reference/kotlin/java/lang/annotation/ElementType#), [PARAMETER](https://developer.android.com/reference/kotlin/java/lang/annotation/ElementType#), [TYPE](https://developer.android.com/reference/kotlin/java/lang/annotation/ElementType#), and [TYPE_PARAMETER](https://developer.android.com/reference/kotlin/java/lang/annotation/ElementType#) correspond to the declaration contexts in JLS 9.6.4.1.

For example, an annotation whose interface is meta-annotated with`@Target(ElementType.FIELD)`may only be written as a modifier for a field declaration.

The constant [TYPE_USE](https://developer.android.com/reference/kotlin/java/lang/annotation/ElementType#) corresponds to the type contexts in JLS 4.11, as well as to two declaration contexts: class and interface declarations (including annotation declarations) and type parameter declarations.

For example, an annotation whose interface is meta-annotated with`@Target(ElementType.TYPE_USE)`may be written on the class or interface of a field (or within the class or interface of the field, if it is a nested or parameterized class or interface, or array class), and may also appear as a modifier for, say, a class declaration.

The`TYPE_USE`constant includes class and interface declarations and type parameter declarations as a convenience for designers of type checkers which give semantics to annotation interfaces. For example, if the annotation interface`NonNull`is meta-annotated with`@Target(ElementType.TYPE_USE)`, then`@NonNull``class C {...}`could be treated by a type checker as indicating that all variables of class`C`are non-null, while still allowing variables of other classes to be non-null or not non-null based on whether`@NonNull`appears at the variable's declaration.

## Summary

| Enum values ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ANNOTATION_TYPE](https://developer.android.com/reference/kotlin/java/lang/annotation/ElementType#ENUM_VALUE:ANNOTATION_TYPE) Annotation interface declaration (Formerly known as an annotation type.) |
| [CONSTRUCTOR](https://developer.android.com/reference/kotlin/java/lang/annotation/ElementType#ENUM_VALUE:CONSTRUCTOR) Constructor declaration |
| [FIELD](https://developer.android.com/reference/kotlin/java/lang/annotation/ElementType#ENUM_VALUE:FIELD) Field declaration (includes enum constants) |
| [LOCAL_VARIABLE](https://developer.android.com/reference/kotlin/java/lang/annotation/ElementType#ENUM_VALUE:LOCAL_VARIABLE) Local variable declaration |
| [METHOD](https://developer.android.com/reference/kotlin/java/lang/annotation/ElementType#ENUM_VALUE:METHOD) Method declaration |
| [MODULE](https://developer.android.com/reference/kotlin/java/lang/annotation/ElementType#ENUM_VALUE:MODULE) Module declaration. |
| [PACKAGE](https://developer.android.com/reference/kotlin/java/lang/annotation/ElementType#ENUM_VALUE:PACKAGE) Package declaration |
| [PARAMETER](https://developer.android.com/reference/kotlin/java/lang/annotation/ElementType#ENUM_VALUE:PARAMETER) Formal parameter declaration |
| [RECORD_COMPONENT](https://developer.android.com/reference/kotlin/java/lang/annotation/ElementType#ENUM_VALUE:RECORD_COMPONENT) Record component |
| [TYPE](https://developer.android.com/reference/kotlin/java/lang/annotation/ElementType#ENUM_VALUE:TYPE) Class, interface (including annotation interface), enum, or record declaration |
| [TYPE_PARAMETER](https://developer.android.com/reference/kotlin/java/lang/annotation/ElementType#ENUM_VALUE:TYPE_PARAMETER) Type parameter declaration |
| [TYPE_USE](https://developer.android.com/reference/kotlin/java/lang/annotation/ElementType#ENUM_VALUE:TYPE_USE) Use of a type |

## Enum values

### ANNOTATION_TYPE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val ANNOTATION_TYPE : ElementType
```

Annotation interface declaration (Formerly known as an annotation type.) 

### CONSTRUCTOR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val CONSTRUCTOR : ElementType
```

Constructor declaration 

### FIELD

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val FIELD : ElementType
```

Field declaration (includes enum constants) 

### LOCAL_VARIABLE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val LOCAL_VARIABLE : ElementType
```

Local variable declaration 

### METHOD

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val METHOD : ElementType
```

Method declaration 

### MODULE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val MODULE : ElementType
```

Module declaration. 

### PACKAGE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val PACKAGE : ElementType
```

Package declaration 

### PARAMETER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val PARAMETER : ElementType
```

Formal parameter declaration 

### RECORD_COMPONENT

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val RECORD_COMPONENT : ElementType
```

Record component 

### TYPE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val TYPE : ElementType
```

Class, interface (including annotation interface), enum, or record declaration 

### TYPE_PARAMETER

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val TYPE_PARAMETER : ElementType
```

Type parameter declaration 

### TYPE_USE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val TYPE_USE : ElementType
```

Use of a type
