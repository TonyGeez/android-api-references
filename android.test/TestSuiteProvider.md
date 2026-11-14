# TestSuiteProvider

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TestSuiteProvider

Kotlin| [Java](https://developer.android.com/reference/android/test/TestSuiteProvider "View this page in Java") 
| --- | --- |

```
interface TestSuiteProvider
```

| [android.test.TestSuiteProvider](https://developer.android.com/reference/kotlin/android/test/TestSuiteProvider#) |

| Known Direct Subclasses [InstrumentationTestRunner](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestRunner) |--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------| | [InstrumentationTestRunner](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestRunner) | An [Instrumentation](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#) that runs various types of junit. | |
| --- | --- | --- | --- | --- | --- | --- |

| **This interface was deprecated in API level 24.**
|
| Use [AndroidJUnitRunner](https://developer.android.com/reference/android/support/test/runner/AndroidJUnitRunner.html) instead. New tests should be written using the [Android Testing Support Library](https://developer.android.com/tools/testing-support-library/index.html).

Implementors will know how to get a test suite.

## Summary

| Public methods ||
|--------------------|-------------------------------------------------------------------------------------------------------------------------|
| abstractTestSuite! | [getTestSuite](https://developer.android.com/reference/kotlin/android/test/TestSuiteProvider#getTestSuite())`()` <br /> |

## Public methods

### getTestSuite

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getTestSuite(): TestSuite!
```

**Deprecated:** *Deprecated in Java.*
