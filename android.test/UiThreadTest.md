# UiThreadTest

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UiThreadTest

Kotlin| [Java](https://developer.android.com/reference/android/test/UiThreadTest "View this page in Java") 

```
@Target([AnnotationTarget.FUNCTION, AnnotationTarget.PROPERTY_GETTER, AnnotationTarget.PROPERTY_SETTER]) class UiThreadTest
```

| [android.test.UiThreadTest](https://developer.android.com/reference/kotlin/android/test/UiThreadTest#) |

| **This annotation was deprecated in API level 24.**
|
| Use [UiThreadTest](https://developer.android.com/reference/android/support/test/annotation/UiThreadTest.html) instead. New tests should be written using the [Android Testing Support Library](https://developer.android.com/tools/testing-support-library/index.html).

This annotation can be used on an [InstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase)'s test methods. When the annotation is present, the test method is executed on the application's main thread (or UI thread.) Note that instrumentation methods may not be used when this annotation is present.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [UiThreadTest](https://developer.android.com/reference/kotlin/android/test/UiThreadTest#UiThreadTest())`()` This annotation can be used on an [InstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase)'s test methods. |

## Public constructors

### UiThreadTest

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
UiThreadTest()
```

**Deprecated:** *Use [UiThreadTest](https://developer.android.com/reference/android/support/test/annotation/UiThreadTest.html) instead. New tests should be written using the [Android Testing Support Library](https://developer.android.com/tools/testing-support-library/index.html).*

This annotation can be used on an [InstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase)'s test methods. When the annotation is present, the test method is executed on the application's main thread (or UI thread.) Note that instrumentation methods may not be used when this annotation is present.
