# AndroidTestRunner

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AndroidTestRunner

Kotlin| [Java](../android/test/AndroidTestRunner.md) 
| --- | --- |

```
open class AndroidTestRunner
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.test.AndroidTestRunner](../android/test/AndroidTestRunner.md) |

| **This class was deprecated in API level 24.**
|
| Use [AndroidJUnitRunner](../android/support/test/runner/AndroidJUnitRunner.md) instead. New tests should be written using the [Android Testing Support Library](https://developer.android.com/tools/testing-support-library/index.html).

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------|---|
| [AndroidTestRunner](../android/test/AndroidTestRunner.md))`()` <br /> |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addTestListener](../android/test/AndroidTestRunner.md))`(`testListener:` `TestListener!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearTestListeners](../android/test/AndroidTestRunner.md))`()` <br /> |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<TestCase!\>! | [getTestCases](../android/test/AndroidTestRunner.md))`()` <br /> |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getTestClassName](../android/test/AndroidTestRunner.md))`()` <br /> |
| openTestResult! | [getTestResult](../android/test/AndroidTestRunner.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [runTest](../android/test/AndroidTestRunner.md))`()` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [runTest](../android/test/AndroidTestRunner.md))`(`testResult:` `TestResult!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setContext](../android/test/AndroidTestRunner.md))`(`context:` ` [Context](../android/content/Context.md)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInstrumentaiton](../android/test/AndroidTestRunner.md))`(`instrumentation:` ` [Instrumentation](../android/app/Instrumentation.md)!`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInstrumentation](../android/test/AndroidTestRunner.md))`(`instrumentation:` ` [Instrumentation](../android/app/Instrumentation.md)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTest](../android/test/AndroidTestRunner.md))`(`test:` `Test!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTestClassName](../android/test/AndroidTestRunner.md))`(`testClassName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `testMethodName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [testEnded](../android/test/AndroidTestRunner.md))`(`testName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [testFailed](../android/test/AndroidTestRunner.md))`(`status:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `test:` `Test!`, `t:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [testStarted](../android/test/AndroidTestRunner.md))`(`testName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| --- | --- |

| Protected methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openTestResult! | [createTestResult](../android/test/AndroidTestRunner.md))`()` <br /> |
| open [Class](../java/lang/Class.md)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>! | [loadSuiteClass](../android/test/AndroidTestRunner.md))`(`suiteClassName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [runFailed](../android/test/AndroidTestRunner.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| --- | --- |

## Public constructors

### AndroidTestRunner

```
AndroidTestRunner()
```

## Public methods

### addTestListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addTestListener(testListener: TestListener!): Unit
```

**Deprecated:** *Deprecated in Java.* 

### clearTestListeners

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clearTestListeners(): Unit
```

**Deprecated:** *Deprecated in Java.* 

### getTestCases

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTestCases(): MutableList<TestCase!>!
```

**Deprecated:** *Deprecated in Java.* 

### getTestClassName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTestClassName(): String!
```

**Deprecated:** *Deprecated in Java.* 

### getTestResult

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTestResult(): TestResult!
```

**Deprecated:** *Deprecated in Java.* 

### runTest

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun runTest(): Unit
```

**Deprecated:** *Deprecated in Java.* 

### runTest

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun runTest(testResult: TestResult!): Unit
```

**Deprecated:** *Deprecated in Java.* 

### setContext

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setContext(context: Context!): Unit
```

**Deprecated:** *Deprecated in Java.* 

### setInstrumentaiton

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setInstrumentaiton(instrumentation: Instrumentation!): Unit
```

**Deprecated:** *Incorrect spelling, use [setInstrumentation(android.app.Instrumentation)](../android/test/AndroidTestRunner.md))instead.* 

### setInstrumentation

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setInstrumentation(instrumentation: Instrumentation!): Unit
```

**Deprecated:** *Deprecated in Java.* 

### setTest

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTest(test: Test!): Unit
```

**Deprecated:** *Deprecated in Java.* 

### setTestClassName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTestClassName(
    testClassName: String!, 
    testMethodName: String!
): Unit
```

**Deprecated:** *Deprecated in Java.* 

### testEnded

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun testEnded(testName: String!): Unit
```

**Deprecated:** *Deprecated in Java.* 

### testFailed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun testFailed(
    status: Int, 
    test: Test!, 
    t: Throwable!
): Unit
```

**Deprecated:** *Deprecated in Java.* 

### testStarted

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun testStarted(testName: String!): Unit
```

**Deprecated:** *Deprecated in Java.*

## Protected methods

### createTestResult

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun createTestResult(): TestResult!
```

**Deprecated:** *Deprecated in Java.* 

### loadSuiteClass

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun loadSuiteClass(suiteClassName: String!): Class<Any!>!
```

**Deprecated:** *Deprecated in Java.* 

### runFailed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun runFailed(message: String!): Unit
```

**Deprecated:** *Deprecated in Java.*
