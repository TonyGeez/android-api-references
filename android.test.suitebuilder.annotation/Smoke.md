# Smoke

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Smoke

Kotlin| [Java](Smoke.md) 
| --- | --- |

```
@Target([AnnotationTarget.FUNCTION, AnnotationTarget.PROPERTY_GETTER, AnnotationTarget.PROPERTY_SETTER, AnnotationTarget.CLASS, AnnotationTarget.FILE]) class Smoke
```

| [android.test.suitebuilder.annotation.Smoke](Smoke.md) |

| **This annotation was deprecated in API level 24.**
|
| New tests should be written using the [Android Testing Support Library](https://developer.android.com/tools/testing-support-library/index.html).

Marks a test that should run as part of the smoke tests. The`android.test.suitebuilder.SmokeTestSuiteBuilder`will run all tests with this annotation.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Smoke](Smoke.md))`()` Marks a test that should run as part of the smoke tests. |

## Public constructors

### Smoke

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Smoke()
```

**Deprecated:** *New tests should be written using the [Android Testing Support Library](https://developer.android.com/tools/testing-support-library/index.html).*

Marks a test that should run as part of the smoke tests. The`android.test.suitebuilder.SmokeTestSuiteBuilder`will run all tests with this annotation.
