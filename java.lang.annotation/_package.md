# java.lang.annotation

# java.lang.annotation

## Interfaces

| [Annotation](https://developer.android.com/reference/kotlin/java/lang/annotation/Annotation) | The common interface extended by all annotation interfaces. |
| --- | --- |

## Exceptions

| [AnnotationFormatError](https://developer.android.com/reference/kotlin/java/lang/annotation/AnnotationFormatError) | Thrown when the annotation parser attempts to read an annotation from a class file and determines that the annotation is malformed. |
| --- | --- |
| [AnnotationTypeMismatchException](https://developer.android.com/reference/kotlin/java/lang/annotation/AnnotationTypeMismatchException) | Thrown to indicate that a program has attempted to access an element of an annotation whose type has changed after the annotation was compiled (or serialized). |
| [IncompleteAnnotationException](https://developer.android.com/reference/kotlin/java/lang/annotation/IncompleteAnnotationException) | Thrown to indicate that a program has attempted to access an element of an annotation interface that was added to the annotation interface definition after the annotation was compiled (or serialized). |

## Annotations

| [Documented](https://developer.android.com/reference/kotlin/java/lang/annotation/Documented) | If the annotation`@Documented`is present on the declaration of an annotation interface*A* , then any`@A`annotation on an element is considered part of the element's public contract. |
| --- | --- |
| [Inherited](https://developer.android.com/reference/kotlin/java/lang/annotation/Inherited) | Indicates that an annotation interface is automatically inherited. |
| [Native](https://developer.android.com/reference/kotlin/java/lang/annotation/Native) | Indicates that a field defining a constant value may be referenced from native code. |
| [Repeatable](https://developer.android.com/reference/kotlin/java/lang/annotation/Repeatable) | The annotation interface`java.lang.annotation.Repeatable`is used to indicate that the annotation interface whose declaration it (meta-)annotates is*repeatable*. |
| --- | --- |
| [Retention](https://developer.android.com/reference/kotlin/java/lang/annotation/Retention) | Indicates how long annotations with the annotated interface are to be retained. |
| [Target](https://developer.android.com/reference/kotlin/java/lang/annotation/Target) | Indicates the contexts in which an annotation interface is applicable. |

## Enums

| [ElementType](https://developer.android.com/reference/kotlin/java/lang/annotation/ElementType) | The constants of this enumerated class provide a simple classification of the syntactic locations where annotations may appear in a Java program. |
| --- | --- |
| [RetentionPolicy](https://developer.android.com/reference/kotlin/java/lang/annotation/RetentionPolicy) | Annotation retention policy. |
