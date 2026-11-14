# TestSuiteProvider

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TestSuiteProvider

Kotlin| [Java](../android/test/TestSuiteProvider.md) 
| --- | --- |

```
interface TestSuiteProvider
```

| [android.test.TestSuiteProvider](../android/test/TestSuiteProvider.md) |

| Known Direct Subclasses [InstrumentationTestRunner](../android/test/InstrumentationTestRunner.md) |--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------| | [InstrumentationTestRunner](../android/test/InstrumentationTestRunner.md) | An [Instrumentation](../android/app/Instrumentation.md) that runs various types of junit. | |
| --- | --- | --- | --- | --- | --- | --- |

| **This interface was deprecated in API level 24.**
|
| Use [AndroidJUnitRunner](../android/support/test/runner/AndroidJUnitRunner.md) instead. New tests should be written using the [Android Testing Support Library](https://developer.android.com/tools/testing-support-library/index.html).

Implementors will know how to get a test suite.

## Summary

| Public methods ||
|--------------------|-------------------------------------------------------------------------------------------------------------------------|
| abstractTestSuite! | [getTestSuite](../android/test/TestSuiteProvider.md))`()` <br /> |

## Public methods

### getTestSuite

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getTestSuite(): TestSuite!
```

**Deprecated:** *Deprecated in Java.*
