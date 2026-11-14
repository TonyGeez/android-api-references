# FlakyTest

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FlakyTest

Kotlin | [Java](https://developer.android.com/reference/android/test/FlakyTest "View this page in Java") 
| --- | --- |

```
@Target([AnnotationTarget.FUNCTION, AnnotationTarget.PROPERTY_GETTER, AnnotationTarget.PROPERTY_SETTER]) class FlakyTest
```

| [android.test.FlakyTest](https://developer.android.com/reference/kotlin/android/test/FlakyTest#) |

| **This annotation was deprecated in API level 24.**
|
| Use [FlakyTest](https://developer.android.com/reference/android/support/test/filters/FlakyTest.html) instead. New tests should be written using the [Android Testing Support Library](https://developer.android.com/tools/testing-support-library/index.html).

This annotation can be used on an [android.test.InstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase)'s test methods. When the annotation is present, the test method is re-executed if the test fails. The total number of executions is specified by the tolerance and defaults to 1.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [FlakyTest](https://developer.android.com/reference/kotlin/android/test/FlakyTest#FlakyTest(kotlin.Int))`(`tolerance:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` This annotation can be used on an [android.test.InstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase)'s test methods. |

| Properties ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [tolerance](https://developer.android.com/reference/kotlin/android/test/FlakyTest#tolerance:kotlin.Int) Indicates how many times a test can run and fail before being reported as a failed test. |

## Public constructors

### FlakyTest

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FlakyTest(tolerance: Int)
```

**Deprecated:** *Use [FlakyTest](https://developer.android.com/reference/android/support/test/filters/FlakyTest.html) instead. New tests should be written using the [Android Testing Support Library](https://developer.android.com/tools/testing-support-library/index.html).*

This annotation can be used on an [android.test.InstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase)'s test methods. When the annotation is present, the test method is re-executed if the test fails. The total number of executions is specified by the tolerance and defaults to 1.

## Properties

### tolerance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val tolerance: Int
```

**Deprecated:** *Deprecated in Java.*

Indicates how many times a test can run and fail before being reported as a failed test. If the tolerance factor is less than 1, the test runs only once.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The total number of allowed run, the default is 1. |
