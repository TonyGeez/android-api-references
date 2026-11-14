# InstrumentationTestSuite

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InstrumentationTestSuite

Kotlin| [Java](https://developer.android.com/reference/android/test/InstrumentationTestSuite "View this page in Java") 
| --- | --- |

```
open class InstrumentationTestSuite
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.test.InstrumentationTestSuite](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestSuite#) |

| **This class was deprecated in API level 24.**
|
| Use [InstrumentationRegistry](https://developer.android.com/reference/android/support/test/InstrumentationRegistry.html) instead. New tests should be written using the [Android Testing Support Library](https://developer.android.com/tools/testing-support-library/index.html).

A junit.framework.TestSuite that injects [android.app.Instrumentation](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#) into [InstrumentationTestCase](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestCase) before running them.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [InstrumentationTestSuite](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestSuite#InstrumentationTestSuite(android.app.Instrumentation))`(`instr:` ` [Instrumentation](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#)!`)` <br /> |
| [InstrumentationTestSuite](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestSuite#InstrumentationTestSuite(java.lang.Class,%20android.app.Instrumentation))`(`theClass:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>!`, `instr:` ` [Instrumentation](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#)!`)` <br /> |
| [InstrumentationTestSuite](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestSuite#InstrumentationTestSuite(kotlin.String,%20android.app.Instrumentation))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `instr:` ` [Instrumentation](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#)!`)` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addTestSuite](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestSuite#addTestSuite(java.lang.Class))`(`testClass:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [runTest](https://developer.android.com/reference/kotlin/android/test/InstrumentationTestSuite#runTest(Test,%20TestResult))`(`test:` `Test!`, `result:` `TestResult!`)` <br /> |

## Public constructors

### InstrumentationTestSuite

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
InstrumentationTestSuite(instr: Instrumentation!)
```

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `instr` | [Instrumentation](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#)!:The instrumentation that will be injected into each test before running it. |

### InstrumentationTestSuite

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
InstrumentationTestSuite(
    theClass: Class<Any!>!, 
    instr: Instrumentation!)
```

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `theClass` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>!:Inspected for methods starting with 'test' |
| `instr` | [Instrumentation](https://developer.android.com/reference/kotlin/android/app/Instrumentation.html#)!:The instrumentation to inject into each test before running. |

### InstrumentationTestSuite

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
InstrumentationTestSuite(
    name: String!, 
    instr: Instrumentation!)
```

## Public methods

### addTestSuite

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addTestSuite(testClass: Class<Any!>!): Unit
```

**Deprecated:** *Deprecated in Java.* 

### runTest

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun runTest(
    test: Test!, 
    result: TestResult!
): Unit
```

**Deprecated:** *Deprecated in Java.*
