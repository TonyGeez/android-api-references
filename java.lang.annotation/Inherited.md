# Inherited

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Inherited

```
@Target([AnnotationTarget.ANNOTATION_CLASS]) class Inherited
```

| [java.lang.annotation.Inherited](https://developer.android.com/reference/kotlin/java/lang/annotation/Inherited#) |

Indicates that an annotation interface is automatically inherited. If an Inherited meta-annotation is present on an annotation interface declaration, and the user queries the annotation interface on a class declaration, and the class declaration has no annotation for this interface, then the class's superclass will automatically be queried for the annotation interface. This process will be repeated until an annotation for this interface is found, or the top of the class hierarchy (Object) is reached. If no superclass has an annotation for this interface, then the query will indicate that the class in question has no such annotation.

Note that this meta-annotation interface has no effect if the annotated interface is used to annotate anything other than a class. Note also that this meta-annotation only causes annotations to be inherited from superclasses; annotations on implemented interfaces have no effect.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Inherited](https://developer.android.com/reference/kotlin/java/lang/annotation/Inherited#Inherited())`()` Indicates that an annotation interface is automatically inherited. |

## Public constructors

### Inherited

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Inherited()
```

Indicates that an annotation interface is automatically inherited. If an Inherited meta-annotation is present on an annotation interface declaration, and the user queries the annotation interface on a class declaration, and the class declaration has no annotation for this interface, then the class's superclass will automatically be queried for the annotation interface. This process will be repeated until an annotation for this interface is found, or the top of the class hierarchy (Object) is reached. If no superclass has an annotation for this interface, then the query will indicate that the class in question has no such annotation.

Note that this meta-annotation interface has no effect if the annotated interface is used to annotate anything other than a class. Note also that this meta-annotation only causes annotations to be inherited from superclasses; annotations on implemented interfaces have no effect.
