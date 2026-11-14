# Retention

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Retention

```
@Target([AnnotationTarget.ANNOTATION_CLASS]) class Retention
```

| [java.lang.annotation.Retention](../java/lang/annotation/Retention.md) |

Indicates how long annotations with the annotated interface are to be retained. If no Retention annotation is present on an annotation interface declaration, the retention policy defaults to`RetentionPolicy.CLASS`.

A Retention meta-annotation has effect only if the meta-annotated interface is used directly for annotation. It has no effect if the meta-annotated interface is used as a member interface in another annotation interface.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Retention](../java/lang/annotation/Retention.md))`(`value:` ` [RetentionPolicy](../java/lang/annotation/RetentionPolicy.md)`)` Indicates how long annotations with the annotated interface are to be retained. |

| Properties ||
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [RetentionPolicy](../java/lang/annotation/RetentionPolicy.md) | [value](../java/lang/annotation/Retention.md) Returns the retention policy. |

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
| [RetentionPolicy](../java/lang/annotation/RetentionPolicy.md) | the retention policy |
