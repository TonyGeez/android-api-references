# AssertionFailedError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AssertionFailedError

Kotlin| [Java](https://developer.android.com/reference/android/test/AssertionFailedError "View this page in Java") 

```
open class AssertionFailedError : Error
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Error](https://developer.android.com/reference/kotlin/java/lang/Error.html#) ||
| | | ↳ | [android.test.AssertionFailedError](https://developer.android.com/reference/kotlin/android/test/AssertionFailedError#) |

| Known Direct Subclasses [ComparisonFailure](https://developer.android.com/reference/kotlin/android/test/ComparisonFailure) |----------------------------------------------------------------------------------------------------|--------------------------------------------------| | [ComparisonFailure](https://developer.android.com/reference/kotlin/android/test/ComparisonFailure) | Thrown when an assert equals for Strings failed. | |

| **This exception was deprecated in API level 16.**
|
| use junit.framework.AssertionFailedError

Thrown when an assertion failed.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AssertionFailedError](https://developer.android.com/reference/kotlin/android/test/AssertionFailedError#AssertionFailedError())`()` It is more typical to call [AssertionFailedError(java.lang.String)](https://developer.android.com/reference/kotlin/android/test/AssertionFailedError#AssertionFailedError(kotlin.String)). |
| [AssertionFailedError](https://developer.android.com/reference/kotlin/android/test/AssertionFailedError#AssertionFailedError(kotlin.String))`(`errorMessage:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

## Public constructors

### AssertionFailedError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AssertionFailedError()
```

It is more typical to call [AssertionFailedError(java.lang.String)](https://developer.android.com/reference/kotlin/android/test/AssertionFailedError#AssertionFailedError(kotlin.String)). 

### AssertionFailedError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AssertionFailedError(errorMessage: String!)
```
