# ClassCircularityError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ClassCircularityError

```
open class ClassCircularityError : LinkageError
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Error](../java/lang/Error.md) |||
| | | ↳ | [java.lang.LinkageError](../java/lang/LinkageError.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.lang.ClassCircularityError](../java/lang/ClassCircularityError.md) |

Thrown when the Java Virtual Machine detects a circularity in the superclass hierarchy of a class being loaded.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ClassCircularityError](../java/lang/ClassCircularityError.md))`()` Constructs a `ClassCircularityError` with no detail message. |
| [ClassCircularityError](../java/lang/ClassCircularityError.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Constructs a `ClassCircularityError` with the specified detail message. |

## Public constructors

### ClassCircularityError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ClassCircularityError()
```

Constructs a `ClassCircularityError` with no detail message. 

### ClassCircularityError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ClassCircularityError(s: String!)
```

Constructs a `ClassCircularityError` with the specified detail message.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------|
| `s` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The detail message |
