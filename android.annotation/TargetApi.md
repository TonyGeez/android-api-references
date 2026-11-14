# TargetApi

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TargetApi

Kotlin| [Java](https://developer.android.com/reference/android/annotation/TargetApi "View this page in Java") 
| --- | --- |

```
@Target([AnnotationTarget.CLASS, AnnotationTarget.FILE, AnnotationTarget.FUNCTION, AnnotationTarget.PROPERTY_GETTER, AnnotationTarget.PROPERTY_SETTER, AnnotationTarget.CONSTRUCTOR, AnnotationTarget.FIELD]) class TargetApi
```

| [android.annotation.TargetApi](https://developer.android.com/reference/kotlin/android/annotation/TargetApi#) |

Indicates that Lint should treat this type as targeting a given API level, no matter what the project target is.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [TargetApi](https://developer.android.com/reference/kotlin/android/annotation/TargetApi#TargetApi(kotlin.Int))`(`value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Indicates that Lint should treat this type as targeting a given API level, no matter what the project target is. |

| Properties ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [value](https://developer.android.com/reference/kotlin/android/annotation/TargetApi#value:kotlin.Int) This sets the target api level for the type. |

## Public constructors

### TargetApi

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TargetApi(value: Int)
```

Indicates that Lint should treat this type as targeting a given API level, no matter what the project target is.

## Properties

### value

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val value: Int
```

This sets the target api level for the type..
