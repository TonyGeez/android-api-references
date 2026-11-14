# Retention

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Retention

```
@Target([AnnotationTarget.ANNOTATION_CLASS]) class Retention
```

| [java.lang.annotation.Retention](https://developer.android.com/reference/kotlin/java/lang/annotation/Retention#) |

Indicates how long annotations with the annotated interface are to be retained. If no Retention annotation is present on an annotation interface declaration, the retention policy defaults to`RetentionPolicy.CLASS`.

A Retention meta-annotation has effect only if the meta-annotated interface is used directly for annotation. It has no effect if the meta-annotated interface is used as a member interface in another annotation interface.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Retention](https://developer.android.com/reference/kotlin/java/lang/annotation/Retention#Retention(java.lang.annotation.RetentionPolicy))`(`value:` ` [RetentionPolicy](https://developer.android.com/reference/kotlin/java/lang/annotation/RetentionPolicy)`)` Indicates how long annotations with the annotated interface are to be retained. |

| Properties ||
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [RetentionPolicy](https://developer.android.com/reference/kotlin/java/lang/annotation/RetentionPolicy) | [value](https://developer.android.com/reference/kotlin/java/lang/annotation/Retention#value:java.lang.annotation.RetentionPolicy) Returns the retention policy. |

## Public constructors

### Retention

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Retention(value: RetentionPolicy)
```

Indicates how long annotations with the annotated interface are to be retained. If no Retention annotation is present on an annotation interface declaration, the retention policy defaults to`RetentionPolicy.CLASS`.

A Retention meta-annotation has effect only if the meta-annotated interface is used directly for annotation. It has no effect if the meta-annotated interface is used as a member interface in another annotation interface.

## Properties

### value

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val value: RetentionPolicy
```

Returns the retention policy.

| Return ||
|--------------------------------------------------------------------------------------------------------|----------------------|
| [RetentionPolicy](https://developer.android.com/reference/kotlin/java/lang/annotation/RetentionPolicy) | the retention policy |
