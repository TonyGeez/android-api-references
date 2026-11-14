# RetentionPolicy

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RetentionPolicy

```
class RetentionPolicy
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [kotlin.Enum](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-enum/index.html)\< [java.lang.annotation.RetentionPolicy](https://developer.android.com/reference/kotlin/java/lang/annotation/RetentionPolicy#)\> ||
| | ↳ | [java.lang.annotation.RetentionPolicy](https://developer.android.com/reference/kotlin/java/lang/annotation/RetentionPolicy#) |

| Known Direct Subclasses [RetentionPolicy.CLASS](https://developer.android.com/reference/kotlin/java/lang/annotation/RetentionPolicy#ENUM_VALUE:CLASS), [RetentionPolicy.RUNTIME](https://developer.android.com/reference/kotlin/java/lang/annotation/RetentionPolicy#ENUM_VALUE:RUNTIME), [RetentionPolicy.SOURCE](https://developer.android.com/reference/kotlin/java/lang/annotation/RetentionPolicy#ENUM_VALUE:SOURCE) |-----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------| | [RetentionPolicy.CLASS](https://developer.android.com/reference/kotlin/java/lang/annotation/RetentionPolicy#ENUM_VALUE:CLASS) | Annotations are to be recorded in the class file by the compiler but need not be retained by the VM at run time. | | [RetentionPolicy.RUNTIME](https://developer.android.com/reference/kotlin/java/lang/annotation/RetentionPolicy#ENUM_VALUE:RUNTIME) | Annotations are to be recorded in the class file by the compiler and retained by the VM at run time, so they may be read reflectively. | | [RetentionPolicy.SOURCE](https://developer.android.com/reference/kotlin/java/lang/annotation/RetentionPolicy#ENUM_VALUE:SOURCE) | Annotations are to be discarded by the compiler. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Annotation retention policy. The constants of this enumerated class describe the various policies for retaining annotations. They are used in conjunction with the [Retention](https://developer.android.com/reference/kotlin/java/lang/annotation/Retention) meta-annotation interface to specify how long annotations are to be retained.

## Summary

| Enum values ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CLASS](https://developer.android.com/reference/kotlin/java/lang/annotation/RetentionPolicy#ENUM_VALUE:CLASS) Annotations are to be recorded in the class file by the compiler but need not be retained by the VM at run time. |
| [RUNTIME](https://developer.android.com/reference/kotlin/java/lang/annotation/RetentionPolicy#ENUM_VALUE:RUNTIME) Annotations are to be recorded in the class file by the compiler and retained by the VM at run time, so they may be read reflectively. |
| [SOURCE](https://developer.android.com/reference/kotlin/java/lang/annotation/RetentionPolicy#ENUM_VALUE:SOURCE) Annotations are to be discarded by the compiler. |

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

- [java.lang.reflect.AnnotatedElement](https://developer.android.com/reference/kotlin/java/lang/reflect/AnnotatedElement.html#) 

### SOURCE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val SOURCE : RetentionPolicy
```

Annotations are to be discarded by the compiler.
