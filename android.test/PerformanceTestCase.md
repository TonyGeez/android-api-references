# PerformanceTestCase

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PerformanceTestCase

Kotlin| [Java](https://developer.android.com/reference/android/test/PerformanceTestCase "View this page in Java") 

```
interface PerformanceTestCase
```

| [android.test.PerformanceTestCase](https://developer.android.com/reference/kotlin/android/test/PerformanceTestCase#) |

| **This interface was deprecated in API level 24.**
|
| Use [AndroidJUnitRunner](https://developer.android.com/reference/android/support/test/runner/AndroidJUnitRunner.html) instead. New tests should be written using the [Android Testing Support Library](https://developer.android.com/tools/testing-support-library/index.html).

More complex interface performance for test cases. If you want your test to be used as a performance test, you must implement this interface.

## Summary

| Nested classes ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [Intermediates](https://developer.android.com/reference/kotlin/android/test/PerformanceTestCase.Intermediates) Callbacks for [PerformanceTestCase](https://developer.android.com/reference/kotlin/android/test/PerformanceTestCase#). |

| Public methods ||
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPerformanceOnly](https://developer.android.com/reference/kotlin/android/test/PerformanceTestCase#isPerformanceOnly())`()` This method is used to determine what modes this test case can run in. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [startPerformance](https://developer.android.com/reference/kotlin/android/test/PerformanceTestCase#startPerformance(android.test.PerformanceTestCase.Intermediates))`(`intermediates:` ` [PerformanceTestCase.Intermediates](https://developer.android.com/reference/kotlin/android/test/PerformanceTestCase.Intermediates)!`)` Set up to begin performance tests. |

## Public methods

### isPerformanceOnly

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isPerformanceOnly(): Boolean
```

**Deprecated:** *Deprecated in Java.*

This method is used to determine what modes this test case can run in.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this test case can only be run in performance mode. |

### startPerformance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun startPerformance(intermediates: PerformanceTestCase.Intermediates!): Int
```

**Deprecated:** *Deprecated in Java.*

Set up to begin performance tests. The 'intermediates' is a communication channel to send back intermediate performance numbers -- if you use it, you will probably want to ensure your test is only executed once by returning 1. Otherwise, return 0 to allow the test harness to decide the number of iterations.

If you return a non-zero iteration count, you should call [intermediates.startTiming](https://developer.android.com/reference/kotlin/android/test/PerformanceTestCase.Intermediates#startTiming(kotlin.Boolean))and [intermediates.endTiming](https://developer.android.com/reference/kotlin/android/test/PerformanceTestCase.Intermediates#finishTiming(kotlin.Boolean))to report the duration of the test whose performance should actually be measured.

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `intermediates` | [PerformanceTestCase.Intermediates](https://developer.android.com/reference/kotlin/android/test/PerformanceTestCase.Intermediates)!:Callback for sending intermediate results. |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | int Maximum number of iterations to run, or 0 to let the caller decide. |
