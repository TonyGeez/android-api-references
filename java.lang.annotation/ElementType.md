# ElementType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ElementType

```
class ElementType
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [kotlin.Enum](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-enum/index.html)\< [java.lang.annotation.ElementType](ElementType.md)\> ||
| | ↳ | [java.lang.annotation.ElementType](ElementType.md) |

| Known Direct Subclasses [ElementType.ANNOTATION_TYPE](ElementType.md), [ElementType.CONSTRUCTOR](ElementType.md), [ElementType.FIELD](ElementType.md), [ElementType.LOCAL_VARIABLE](ElementType.md), [ElementType.METHOD](ElementType.md), [ElementType.MODULE](ElementType.md), [ElementType.PACKAGE](ElementType.md), [ElementType.PARAMETER](ElementType.md), [ElementType.RECORD_COMPONENT](ElementType.md), [ElementType.TYPE](ElementType.md), [ElementType.TYPE_PARAMETER](ElementType.md), [ElementType.TYPE_USE](ElementType.md) |---------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------| | [ElementType.ANNOTATION_TYPE](ElementType.md) | Annotation interface declaration (Formerly known as an annotation type.) | | [ElementType.CONSTRUCTOR](ElementType.md) | Constructor declaration | | [ElementType.FIELD](ElementType.md) | Field declaration (includes enum constants) | | [ElementType.LOCAL_VARIABLE](ElementType.md) | Local variable declaration | | [ElementType.METHOD](ElementType.md) | Method declaration | | [ElementType.MODULE](ElementType.md) | Module declaration. | | [ElementType.PACKAGE](ElementType.md) | Package declaration | | [ElementType.PARAMETER](ElementType.md) | Formal parameter declaration | | [ElementType.RECORD_COMPONENT](ElementType.md) | Record component | | [ElementType.TYPE](ElementType.md) | Class, interface (including annotation interface), enum, or record declaration | | [ElementType.TYPE_PARAMETER](ElementType.md) | Type parameter declaration | | [ElementType.TYPE_USE](ElementType.md) | Use of a type | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

The constants of this enumerated class provide a simple classification of the syntactic locations where annotations may appear in a Java program. These constants are used in [Target](Target.md) meta-annotations to specify where it is legal to write annotations of a given type.

The syntactic locations where annotations may appear are split into*declaration contexts* , where annotations apply to declarations, and*type contexts*, where annotations apply to types used in declarations and expressions.

The constants [ANNOTATION_TYPE](ElementType.md), [CONSTRUCTOR](ElementType.md), [FIELD](ElementType.md), [LOCAL_VARIABLE](ElementType.md), [METHOD](ElementType.md), [PACKAGE](ElementType.md), [MODULE](ElementType.md), [PARAMETER](ElementType.md), [TYPE](ElementType.md), and [TYPE_PARAMETER](ElementType.md) correspond to the declaration contexts in JLS 9.6.4.1.

For example, an annotation whose interface is meta-annotated with`@Target(ElementType.FIELD)`may only be written as a modifier for a field declaration.

The constant [TYPE_USE](ElementType.md) corresponds to the type contexts in JLS 4.11, as well as to two declaration contexts: class and interface declarations (including annotation declarations) and type parameter declarations.

For example, an annotation whose interface is meta-annotated with`@Target(ElementType.TYPE_USE)`may be written on the class or interface of a field (or within the class or interface of the field, if it is a nested or parameterized class or interface, or array class), and may also appear as a modifier for, say, a class declaration.

The`TYPE_USE`constant includes class and interface declarations and type parameter declarations as a convenience for designers of type checkers which give semantics to annotation interfaces. For example, if the annotation interface`NonNull`is meta-annotated with`@Target(ElementType.TYPE_USE)`, then`@NonNull``class C {...}`could be treated by a type checker as indicating that all variables of class`C`are non-null, while still allowing variables of other classes to be non-null or not non-null based on whether`@NonNull`appears at the variable's declaration.

## Summary

| Enum values ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ANNOTATION_TYPE](ElementType.md) Annotation interface declaration (Formerly known as an annotation type.) |
| [CONSTRUCTOR](ElementType.md) Constructor declaration |
| [FIELD](ElementType.md) Field declaration (includes enum constants) |
| [LOCAL_VARIABLE](ElementType.md) Local variable declaration |
| [METHOD](ElementType.md) Method declaration |
| [MODULE](ElementType.md) Module declaration. |
| [PACKAGE](ElementType.md) Package declaration |
| [PARAMETER](ElementType.md) Formal parameter declaration |
| [RECORD_COMPONENT](ElementType.md) Record component |
| [TYPE](ElementType.md) Class, interface (including annotation interface), enum, or record declaration |
| [TYPE_PARAMETER](ElementType.md) Type parameter declaration |
| [TYPE_USE](ElementType.md) Use of a type |

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
