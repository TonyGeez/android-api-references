# TargetApi

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TargetApi

Kotlin| [Java](TargetApi.md) 
| --- | --- |

```
@Target([AnnotationTarget.CLASS, AnnotationTarget.FILE, AnnotationTarget.FUNCTION, AnnotationTarget.PROPERTY_GETTER, AnnotationTarget.PROPERTY_SETTER, AnnotationTarget.CONSTRUCTOR, AnnotationTarget.FIELD]) class TargetApi
```

| [android.annotation.TargetApi](TargetApi.md) |

Indicates that Lint should treat this type as targeting a given API level, no matter what the project target is.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [TargetApi](TargetApi.md))`(`value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Indicates that Lint should treat this type as targeting a given API level, no matter what the project target is. |

| Properties ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [value](TargetApi.md) This sets the target api level for the type. |

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
