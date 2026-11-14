# UiThreadTest

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UiThreadTest

Kotlin| [Java](../android/test/UiThreadTest.md) 
| --- | --- |

```
@Target([AnnotationTarget.FUNCTION, AnnotationTarget.PROPERTY_GETTER, AnnotationTarget.PROPERTY_SETTER]) class UiThreadTest
```

| [android.test.UiThreadTest](../android/test/UiThreadTest.md) |

| **This annotation was deprecated in API level 24.**
|
| Use [UiThreadTest](../android/support/test/annotation/UiThreadTest.md) instead. New tests should be written using the [Android Testing Support Library](https://developer.android.com/tools/testing-support-library/index.html).

This annotation can be used on an [InstrumentationTestCase](../android/test/InstrumentationTestCase.md)'s test methods. When the annotation is present, the test method is executed on the application's main thread (or UI thread.) Note that instrumentation methods may not be used when this annotation is present.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [UiThreadTest](../android/test/UiThreadTest.md))`()` This annotation can be used on an [InstrumentationTestCase](../android/test/InstrumentationTestCase.md)'s test methods. |

## Public constructors

### UiThreadTest

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
UiThreadTest()
```

**Deprecated:** *Use [UiThreadTest](../android/support/test/annotation/UiThreadTest.md) instead. New tests should be written using the [Android Testing Support Library](https://developer.android.com/tools/testing-support-library/index.html).*

This annotation can be used on an [InstrumentationTestCase](../android/test/InstrumentationTestCase.md)'s test methods. When the annotation is present, the test method is executed on the application's main thread (or UI thread.) Note that instrumentation methods may not be used when this annotation is present.
