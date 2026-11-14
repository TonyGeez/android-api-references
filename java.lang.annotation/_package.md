# java.lang.annotation

# java.lang.annotation

## Interfaces

| [Annotation](Annotation.md) | The common interface extended by all annotation interfaces. |
| --- | --- |

## Exceptions

| [AnnotationFormatError](AnnotationFormatError.md) | Thrown when the annotation parser attempts to read an annotation from a class file and determines that the annotation is malformed. |
| --- | --- |
| [AnnotationTypeMismatchException](AnnotationTypeMismatchException.md) | Thrown to indicate that a program has attempted to access an element of an annotation whose type has changed after the annotation was compiled (or serialized). |
| [IncompleteAnnotationException](IncompleteAnnotationException.md) | Thrown to indicate that a program has attempted to access an element of an annotation interface that was added to the annotation interface definition after the annotation was compiled (or serialized). |

## Annotations

| [Documented](Documented.md) | If the annotation`@Documented`is present on the declaration of an annotation interface*A* , then any`@A`annotation on an element is considered part of the element's public contract. |
| --- | --- |
| [Inherited](Inherited.md) | Indicates that an annotation interface is automatically inherited. |
| [Native](Native.md) | Indicates that a field defining a constant value may be referenced from native code. |
| [Repeatable](Repeatable.md) | The annotation interface`java.lang.annotation.Repeatable`is used to indicate that the annotation interface whose declaration it (meta-)annotates is*repeatable*. |
| --- | --- |
| [Retention](Retention.md) | Indicates how long annotations with the annotated interface are to be retained. |
| [Target](Target.md) | Indicates the contexts in which an annotation interface is applicable. |

## Enums

| [ElementType](ElementType.md) | The constants of this enumerated class provide a simple classification of the syntactic locations where annotations may appear in a Java program. |
| --- | --- |
| [RetentionPolicy](RetentionPolicy.md) | Annotation retention policy. |
