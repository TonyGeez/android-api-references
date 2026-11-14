Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ComparisonFailure

Kotlin | [Java](../android/test/ComparisonFailure.md)
| --- | --- |

```
open class ComparisonFailure : AssertionFailedError
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Error](../java/lang/Error.md) |||
| | | ↳ | [android.test.AssertionFailedError](../android/test/AssertionFailedError.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [android.test.ComparisonFailure](../android/test/ComparisonFailure.md) |

| **This exception was deprecated in API level 16.**
|
| use org.junit.ComparisonFailure

Thrown when an assert equals for Strings failed.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/test/ComparisonFailure#ComparisonFailure(kotlin.String,%20kotlin.String,%20kotlin.String)(message: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, expected: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, actual: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` <br /> |

| Properties ||
|---|---|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/test/ComparisonFailure#message:kotlin.String` Returns the detail message string of this throwable. |

## Public constructors

### ComparisonFailure

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ComparisonFailure(
    message: String!, 
    expected: String!, 
    actual: String!)
```

## Properties

### message

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open val message: String?
```

Returns the detail message string of this throwable.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | the detail message string of this `Throwable` instance (which may be `null`). |
