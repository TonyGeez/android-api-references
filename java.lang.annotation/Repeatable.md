# Repeatable

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Repeatable

```
@Target([AnnotationTarget.ANNOTATION_CLASS]) class Repeatable
```

| [java.lang.annotation.Repeatable](https://developer.android.com/reference/kotlin/java/lang/annotation/Repeatable#) |

The annotation interface`java.lang.annotation.Repeatable`is used to indicate that the annotation interface whose declaration it (meta-)annotates is*repeatable* . The value of`@Repeatable`indicates the*containing annotation interface*for the repeatable annotation interface.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Repeatable](https://developer.android.com/reference/kotlin/java/lang/annotation/Repeatable#Repeatable(kotlin.reflect.KClass))`(`value:` ` [KClass](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.reflect/-k-class/index.html)<out` ` [Annotation](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-annotation/index.html)!>`)` The annotation interface`java.lang.annotation.Repeatable`is used to indicate that the annotation interface whose declaration it (meta-)annotates is*repeatable*. |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [KClass](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.reflect/-k-class/index.html)\<out [Annotation](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-annotation/index.html)!\> | [value](https://developer.android.com/reference/kotlin/java/lang/annotation/Repeatable#value:kotlin.reflect.KClass) Indicates the*containing annotation interface*for the repeatable annotation interface. |

## Public constructors

### Repeatable

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Repeatable(value: KClass<out Annotation!>)
```

The annotation interface`java.lang.annotation.Repeatable`is used to indicate that the annotation interface whose declaration it (meta-)annotates is*repeatable* . The value of`@Repeatable`indicates the*containing annotation interface*for the repeatable annotation interface.

## Properties

### value

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val value: KClass<out Annotation!>
```

Indicates the*containing annotation interface*for the repeatable annotation interface.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| [KClass](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.reflect/-k-class/index.html)<out` ` [Annotation](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-annotation/index.html)!> | the containing annotation interface |
