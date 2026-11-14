# AssertionFailedError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AssertionFailedError

Kotlin| [Java](../android/test/AssertionFailedError.md) 
| --- | --- |

```
open class AssertionFailedError : Error
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Error](../java/lang/Error.md) ||
| | | ↳ | [android.test.AssertionFailedError](../android/test/AssertionFailedError.md) |
| --- | --- | --- | --- |

| Known Direct Subclasses [ComparisonFailure](../android/test/ComparisonFailure.md) |----------------------------------------------------------------------------------------------------|--------------------------------------------------| | [ComparisonFailure](../android/test/ComparisonFailure.md) | Thrown when an assert equals for Strings failed. | |
| --- | --- | --- | --- | --- | --- | --- |

| **This exception was deprecated in API level 16.**
|
| use junit.framework.AssertionFailedError

Thrown when an assertion failed.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AssertionFailedError](../android/test/AssertionFailedError.md))`()` It is more typical to call [AssertionFailedError(java.lang.String)](../android/test/AssertionFailedError.md)). |
| [AssertionFailedError](../android/test/AssertionFailedError.md))`(`errorMessage:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

## Public constructors

### AssertionFailedError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AssertionFailedError()
```

It is more typical to call [AssertionFailedError(java.lang.String)](../android/test/AssertionFailedError.md)). 

### AssertionFailedError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AssertionFailedError(errorMessage: String!)
```
