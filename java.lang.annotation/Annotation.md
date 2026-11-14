# Annotation

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Annotation

```
interface Annotation
```

| [java.lang.annotation.Annotation](Annotation.md) |

The common interface extended by all annotation interfaces. Note that an interface that manually extends this one does*not* define an annotation interface. Also note that this interface does not itself define an annotation interface. More information about annotation interfaces can be found in section {@jls 9.6} of The Java Language Specification. The [java.lang.reflect.AnnotatedElement](../java.lang.reflect/AnnotatedElement.md) interface discusses compatibility concerns when evolving an annotation interface from being non-repeatable to being repeatable.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Class](../java.lang/Class.md)\<out [Annotation](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-annotation/index.html)!\>! | [annotationType](Annotation.md))`()` Returns the annotation interface of this annotation. |

## Public methods

### annotationType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun annotationType(): Class<out Annotation!>!
```

Returns the annotation interface of this annotation.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| [Class](../java.lang/Class.md)<out` ` [Annotation](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-annotation/index.html)!>! | the annotation interface of this annotation |

**See Also**

- [java.lang.Enum#getDeclaringClass](../java.lang/Enum.md))
