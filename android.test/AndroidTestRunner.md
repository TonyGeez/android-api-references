# AndroidTestRunner

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AndroidTestRunner

Kotlin| [Java](https://developer.android.com/reference/android/test/AndroidTestRunner "View this page in Java") 

```
open class AndroidTestRunner
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.test.AndroidTestRunner](https://developer.android.com/reference/kotlin/android/test/AndroidTestRunner#) |

| **This class was deprecated in API level 24.**
|
| Use [AndroidJUnitRunner](https://developer.android.com/reference/android/support/test/runner/AndroidJUnitRunner.html) instead. New tests should be written using the [Android Testing Support Library](https://developer.android.com/tools/testing-support-library/index.html).

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------|---|
| [AndroidTestRunner](https://developer.android.com/reference/kotlin/android/test/AndroidTestRunner#AndroidTestRunner())`()` <br /> |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addTestListener](https://developer.android.com/reference/kotlin/android/test/AndroidTestRunner#addTestListener(TestListener))`(`testListener:` `TestListener!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearTestListeners](https://developer.android.com/reference/kotlin/android/test/AndroidTestRunner#clearTestListeners())`()` <br /> |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<TestCase!\>! | [getTestCases](https://developer.android.com/reference/kotlin/android/test/AndroidTestRunner#getTestCases())`()` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getTestClassName](https://developer.android.com/reference/kotlin/android/test/AndroidTestRunner#getTestClassName())`()` <br /> |
| openTestResult! | [getTestResult](https://developer.android.com/reference/kotlin/android/test/AndroidTestRunner#getTestResult())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [runTest](https://developer.android.com/reference/kotlin/android/test/AndroidTestRunner#runTest())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [runTest](https://developer.android.com/reference/kotlin/android/test/AndroidTestRunner#runTest(TestResult))`(`testResult:` `TestResult!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setContext](https://developer.android.com/reference/kotlin/android/test/AndroidTestRunner#setContext(android.content.Context))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInstrumentaiton](https://developer.android.com/reference/kotlin/android/test/AndroidTestRunner#setInstrumentaiton(android.app.Instrumentation))`(`instrumentation:` ` [Instrumentation](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInstrumentation](https://developer.android.com/reference/kotlin/android/test/AndroidTestRunner#setInstrumentation(android.app.Instrumentation))`(`instrumentation:` ` [Instrumentation](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTest](https://developer.android.com/reference/kotlin/android/test/AndroidTestRunner#setTest(Test))`(`test:` `Test!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTestClassName](https://developer.android.com/reference/kotlin/android/test/AndroidTestRunner#setTestClassName(kotlin.String,%20kotlin.String))`(`testClassName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `testMethodName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [testEnded](https://developer.android.com/reference/kotlin/android/test/AndroidTestRunner#testEnded(kotlin.String))`(`testName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [testFailed](https://developer.android.com/reference/kotlin/android/test/AndroidTestRunner#testFailed(kotlin.Int,%20Test,%20kotlin.Throwable))`(`status:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `test:` `Test!`, `t:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [testStarted](https://developer.android.com/reference/kotlin/android/test/AndroidTestRunner#testStarted(kotlin.String))`(`testName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

| Protected methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openTestResult! | [createTestResult](https://developer.android.com/reference/kotlin/android/test/AndroidTestRunner#createTestResult())`()` <br /> |
| open [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>! | [loadSuiteClass](https://developer.android.com/reference/kotlin/android/test/AndroidTestRunner#loadSuiteClass(kotlin.String))`(`suiteClassName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [runFailed](https://developer.android.com/reference/kotlin/android/test/AndroidTestRunner#runFailed(kotlin.String))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

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

**Deprecated:** *Incorrect spelling, use [setInstrumentation(android.app.Instrumentation)](https://developer.android.com/reference/kotlin/android/test/AndroidTestRunner#setInstrumentation(android.app.Instrumentation))instead.* 

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
