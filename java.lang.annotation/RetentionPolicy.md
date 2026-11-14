# RetentionPolicy

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RetentionPolicy

```
class RetentionPolicy
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [kotlin.Enum](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-enum/index.html)\< [java.lang.annotation.RetentionPolicy](RetentionPolicy.md)\> ||
| | ↳ | [java.lang.annotation.RetentionPolicy](RetentionPolicy.md) |

| Known Direct Subclasses [RetentionPolicy.CLASS](RetentionPolicy.md), [RetentionPolicy.RUNTIME](RetentionPolicy.md), [RetentionPolicy.SOURCE](RetentionPolicy.md) |-----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------| | [RetentionPolicy.CLASS](RetentionPolicy.md) | Annotations are to be recorded in the class file by the compiler but need not be retained by the VM at run time. | | [RetentionPolicy.RUNTIME](RetentionPolicy.md) | Annotations are to be recorded in the class file by the compiler and retained by the VM at run time, so they may be read reflectively. | | [RetentionPolicy.SOURCE](RetentionPolicy.md) | Annotations are to be discarded by the compiler. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Annotation retention policy. The constants of this enumerated class describe the various policies for retaining annotations. They are used in conjunction with the [Retention](Retention.md) meta-annotation interface to specify how long annotations are to be retained.

## Summary

| Enum values ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CLASS](RetentionPolicy.md) Annotations are to be recorded in the class file by the compiler but need not be retained by the VM at run time. |
| [RUNTIME](RetentionPolicy.md) Annotations are to be recorded in the class file by the compiler and retained by the VM at run time, so they may be read reflectively. |
| [SOURCE](RetentionPolicy.md) Annotations are to be discarded by the compiler. |

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

- [java.lang.reflect.AnnotatedElement](../java.lang.reflect/AnnotatedElement.md) 

### SOURCE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val SOURCE : RetentionPolicy
```

Annotations are to be discarded by the compiler.
