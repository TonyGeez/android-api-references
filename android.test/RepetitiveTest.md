# RepetitiveTest

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RepetitiveTest

Kotlin| [Java](../android/test/RepetitiveTest.md) 
| --- | --- |

```
@Target([AnnotationTarget.FUNCTION, AnnotationTarget.PROPERTY_GETTER, AnnotationTarget.PROPERTY_SETTER]) class RepetitiveTest
```

| [android.test.RepetitiveTest](../android/test/RepetitiveTest.md) |

| **This annotation was deprecated in API level 29.**
|
| New tests should be written using the [Android Testing Support Library](https://developer.android.com/tools/testing-support-library/index.html).

This annotation can be used on an [android.test.InstrumentationTestCase](../android/test/InstrumentationTestCase.md)'s test methods. When the annotation is present, the test method is executed the number of times specified by numIterations and defaults to 1.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [RepetitiveTest](../android/test/RepetitiveTest.md))`(`numIterations:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` This annotation can be used on an [android.test.InstrumentationTestCase](../android/test/InstrumentationTestCase.md)'s test methods. |

| Properties ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [numIterations](../android/test/RepetitiveTest.md) Indicates the number of times a test case should be run. |

## Public constructors

### RepetitiveTest

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
RepetitiveTest(numIterations: Int)
```

**Deprecated:** *New tests should be written using the [Android Testing Support Library](https://developer.android.com/tools/testing-support-library/index.html).*

This annotation can be used on an [android.test.InstrumentationTestCase](../android/test/InstrumentationTestCase.md)'s test methods. When the annotation is present, the test method is executed the number of times specified by numIterations and defaults to 1.

## Properties

### numIterations

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val numIterations: Int
```

**Deprecated:** *Deprecated in Java.*

Indicates the number of times a test case should be run.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The total number of iterations, the default is 1. |
