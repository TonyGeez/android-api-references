# Suppress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Suppress

Kotlin| [Java](https://developer.android.com/reference/android/test/suitebuilder/annotation/Suppress "View this page in Java") 

```
@Target([AnnotationTarget.FUNCTION, AnnotationTarget.PROPERTY_GETTER, AnnotationTarget.PROPERTY_SETTER, AnnotationTarget.CLASS, AnnotationTarget.FILE]) class Suppress
```

| [android.test.suitebuilder.annotation.Suppress](https://developer.android.com/reference/kotlin/android/test/suitebuilder/annotation/Suppress#) |

| **This annotation was deprecated in API level 24.**
|
| Use [Suppress](https://developer.android.com/reference/android/support/test/filters/Suppress.html) instead. New tests should be written using the [Android Testing Support Library](https://developer.android.com/tools/testing-support-library/index.html).

Use this annotation on test classes or test methods that should not be included in a test suite. If the annotation appears on the class then no tests in that class will be included. If the annotation appears only on a test method then only that method will be excluded.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Suppress](https://developer.android.com/reference/kotlin/android/test/suitebuilder/annotation/Suppress#Suppress())`()` Use this annotation on test classes or test methods that should not be included in a test suite. |

## Public constructors

### Suppress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Suppress()
```

**Deprecated:** *Use [Suppress](https://developer.android.com/reference/android/support/test/filters/Suppress.html) instead. New tests should be written using the [Android Testing Support Library](https://developer.android.com/tools/testing-support-library/index.html).*

Use this annotation on test classes or test methods that should not be included in a test suite. If the annotation appears on the class then no tests in that class will be included. If the annotation appears only on a test method then only that method will be excluded.
