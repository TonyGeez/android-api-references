# RetentionPolicy

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RetentionPolicy

```
class RetentionPolicy
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [kotlin.Enum](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-enum/index.html)\< [java.lang.annotation.RetentionPolicy](../java/lang/annotation/RetentionPolicy.md)\> ||
| | ↳ | [java.lang.annotation.RetentionPolicy](../java/lang/annotation/RetentionPolicy.md) |

| Known Direct Subclasses [RetentionPolicy.CLASS](../java/lang/annotation/RetentionPolicy.md), [RetentionPolicy.RUNTIME](../java/lang/annotation/RetentionPolicy.md), [RetentionPolicy.SOURCE](../java/lang/annotation/RetentionPolicy.md) |-----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------| | [RetentionPolicy.CLASS](../java/lang/annotation/RetentionPolicy.md) | Annotations are to be recorded in the class file by the compiler but need not be retained by the VM at run time. | | [RetentionPolicy.RUNTIME](../java/lang/annotation/RetentionPolicy.md) | Annotations are to be recorded in the class file by the compiler and retained by the VM at run time, so they may be read reflectively. | | [RetentionPolicy.SOURCE](../java/lang/annotation/RetentionPolicy.md) | Annotations are to be discarded by the compiler. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Annotation retention policy. The constants of this enumerated class describe the various policies for retaining annotations. They are used in conjunction with the [Retention](../java/lang/annotation/Retention.md) meta-annotation interface to specify how long annotations are to be retained.

## Summary

| Enum values ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CLASS](../java/lang/annotation/RetentionPolicy.md) Annotations are to be recorded in the class file by the compiler but need not be retained by the VM at run time. |
| [RUNTIME](../java/lang/annotation/RetentionPolicy.md) Annotations are to be recorded in the class file by the compiler and retained by the VM at run time, so they may be read reflectively. |
| [SOURCE](../java/lang/annotation/RetentionPolicy.md) Annotations are to be discarded by the compiler. |

## Enum values

### CLASS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val CLASS : RetentionPolicy
```

Annotations are to be recorded in the class file by the compiler but need not be retained by the VM at run time. This is the default behavior. 

### RUNTIME

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val RUNTIME : RetentionPolicy
```

Annotations are to be recorded in the class file by the compiler and retained by the VM at run time, so they may be read reflectively. 
**See Also**

- [java.lang.reflect.AnnotatedElement](../java/lang/reflect/AnnotatedElement.md) 

### SOURCE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val SOURCE : RetentionPolicy
```

Annotations are to be discarded by the compiler.
