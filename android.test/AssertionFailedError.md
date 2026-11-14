# AssertionFailedError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AssertionFailedError

Kotlin| [Java](AssertionFailedError.md) 
| --- | --- |

```
open class AssertionFailedError : Error
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Error](../java.lang/Error.md) ||
| | | ↳ | [android.test.AssertionFailedError](AssertionFailedError.md) |
| --- | --- | --- | --- |

| Known Direct Subclasses [ComparisonFailure](ComparisonFailure.md) |----------------------------------------------------------------------------------------------------|--------------------------------------------------| | [ComparisonFailure](ComparisonFailure.md) | Thrown when an assert equals for Strings failed. | |
| --- | --- | --- | --- | --- | --- | --- |

| **This exception was deprecated in API level 16.**
|
| use junit.framework.AssertionFailedError

Thrown when an assertion failed.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AssertionFailedError](AssertionFailedError.md))`()` It is more typical to call [AssertionFailedError(java.lang.String)](AssertionFailedError.md)). |
| [AssertionFailedError](AssertionFailedError.md))`(`errorMessage:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

## Public constructors

### AssertionFailedError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AssertionFailedError()
```

It is more typical to call [AssertionFailedError(java.lang.String)](AssertionFailedError.md)). 

### AssertionFailedError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AssertionFailedError(errorMessage: String!)
```
