# FlakyTest

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FlakyTest

Kotlin | [Java](FlakyTest.md) 
| --- | --- |

```
@Target([AnnotationTarget.FUNCTION, AnnotationTarget.PROPERTY_GETTER, AnnotationTarget.PROPERTY_SETTER]) class FlakyTest
```

| [android.test.FlakyTest](FlakyTest.md) |

| **This annotation was deprecated in API level 24.**
|
| Use [FlakyTest](../android/support/test/filters/FlakyTest.md) instead. New tests should be written using the [Android Testing Support Library](https://developer.android.com/tools/testing-support-library/index.html).

This annotation can be used on an [android.test.InstrumentationTestCase](InstrumentationTestCase.md)'s test methods. When the annotation is present, the test method is re-executed if the test fails. The total number of executions is specified by the tolerance and defaults to 1.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [FlakyTest](FlakyTest.md))`(`tolerance:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` This annotation can be used on an [android.test.InstrumentationTestCase](InstrumentationTestCase.md)'s test methods. |

| Properties ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [tolerance](FlakyTest.md) Indicates how many times a test can run and fail before being reported as a failed test. |

## Public constructors

### FlakyTest

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FlakyTest(tolerance: Int)
```

**Deprecated:** *Use [FlakyTest](../android/support/test/filters/FlakyTest.md) instead. New tests should be written using the [Android Testing Support Library](https://developer.android.com/tools/testing-support-library/index.html).*

This annotation can be used on an [android.test.InstrumentationTestCase](InstrumentationTestCase.md)'s test methods. When the annotation is present, the test method is re-executed if the test fails. The total number of executions is specified by the tolerance and defaults to 1.

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
