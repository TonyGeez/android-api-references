# java.lang.annotation

# java.lang.annotation

## Interfaces

| [Annotation](../java/lang/annotation/Annotation.md) | The common interface extended by all annotation interfaces. |
| --- | --- |

## Exceptions

| [AnnotationFormatError](../java/lang/annotation/AnnotationFormatError.md) | Thrown when the annotation parser attempts to read an annotation from a class file and determines that the annotation is malformed. |
| --- | --- |
| [AnnotationTypeMismatchException](../java/lang/annotation/AnnotationTypeMismatchException.md) | Thrown to indicate that a program has attempted to access an element of an annotation whose type has changed after the annotation was compiled (or serialized). |
| [IncompleteAnnotationException](../java/lang/annotation/IncompleteAnnotationException.md) | Thrown to indicate that a program has attempted to access an element of an annotation interface that was added to the annotation interface definition after the annotation was compiled (or serialized). |

## Annotations

| [Documented](../java/lang/annotation/Documented.md) | If the annotation`@Documented`is present on the declaration of an annotation interface*A* , then any`@A`annotation on an element is considered part of the element's public contract. |
| --- | --- |
| [Inherited](../java/lang/annotation/Inherited.md) | Indicates that an annotation interface is automatically inherited. |
| [Native](../java/lang/annotation/Native.md) | Indicates that a field defining a constant value may be referenced from native code. |
| [Repeatable](../java/lang/annotation/Repeatable.md) | The annotation interface`java.lang.annotation.Repeatable`is used to indicate that the annotation interface whose declaration it (meta-)annotates is*repeatable*. |
| --- | --- |
| [Retention](../java/lang/annotation/Retention.md) | Indicates how long annotations with the annotated interface are to be retained. |
| [Target](../java/lang/annotation/Target.md) | Indicates the contexts in which an annotation interface is applicable. |

## Enums

| [ElementType](../java/lang/annotation/ElementType.md) | The constants of this enumerated class provide a simple classification of the syntactic locations where annotations may appear in a Java program. |
| --- | --- |
| [RetentionPolicy](../java/lang/annotation/RetentionPolicy.md) | Annotation retention policy. |
