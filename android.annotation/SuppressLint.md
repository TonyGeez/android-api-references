# SuppressLint

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SuppressLint

Kotlin| [Java](SuppressLint.md) 
| --- | --- |

```
@Target([AnnotationTarget.CLASS, AnnotationTarget.FILE, AnnotationTarget.FIELD, AnnotationTarget.FUNCTION, AnnotationTarget.PROPERTY_GETTER, AnnotationTarget.PROPERTY_SETTER, AnnotationTarget.VALUE_PARAMETER, AnnotationTarget.CONSTRUCTOR, AnnotationTarget.LOCAL_VARIABLE]) class SuppressLint
```

| [android.annotation.SuppressLint](SuppressLint.md) |

Indicates that Lint should ignore the specified warnings for the annotated element.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SuppressLint](SuppressLint.md))`(`vararg` `value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Indicates that Lint should ignore the specified warnings for the annotated element. |

| Properties ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)\> | [value](SuppressLint.md) The set of warnings (identified by the lint issue id) that should be ignored by lint. |

## Public constructors

### SuppressLint

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SuppressLint(vararg value: String)
```

Indicates that Lint should ignore the specified warnings for the annotated element.

## Properties

### value

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val value: Array<String>
```

The set of warnings (identified by the lint issue id) that should be ignored by lint. It is not an error to specify an unrecognized name.
