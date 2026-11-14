# InstrumentationTestSuite

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InstrumentationTestSuite

Kotlin| [Java](InstrumentationTestSuite.md) 
| --- | --- |

```
open class InstrumentationTestSuite
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.test.InstrumentationTestSuite](InstrumentationTestSuite.md) |

| **This class was deprecated in API level 24.**
|
| Use [InstrumentationRegistry](../android/support/test/InstrumentationRegistry.md) instead. New tests should be written using the [Android Testing Support Library](https://developer.android.com/tools/testing-support-library/index.html).

A junit.framework.TestSuite that injects [android.app.Instrumentation](../android.app/Instrumentation.md) into [InstrumentationTestCase](InstrumentationTestCase.md) before running them.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [InstrumentationTestSuite](InstrumentationTestSuite.md))`(`instr:` ` [Instrumentation](../android.app/Instrumentation.md)!`)` <br /> |
| [InstrumentationTestSuite](InstrumentationTestSuite.md))`(`theClass:` ` [Class](../java.lang/Class.md)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>!`, `instr:` ` [Instrumentation](../android.app/Instrumentation.md)!`)` <br /> |
| [InstrumentationTestSuite](InstrumentationTestSuite.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `instr:` ` [Instrumentation](../android.app/Instrumentation.md)!`)` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addTestSuite](InstrumentationTestSuite.md))`(`testClass:` ` [Class](../java.lang/Class.md)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [runTest](InstrumentationTestSuite.md))`(`test:` `Test!`, `result:` `TestResult!`)` <br /> |

## Public constructors

### InstrumentationTestSuite

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
InstrumentationTestSuite(instr: Instrumentation!)
```

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `instr` | [Instrumentation](../android.app/Instrumentation.md)!:The instrumentation that will be injected into each test before running it. |

### InstrumentationTestSuite

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
InstrumentationTestSuite(
    theClass: Class<Any!>!, 
    instr: Instrumentation!)
```

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `theClass` | [Class](../java.lang/Class.md)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>!:Inspected for methods starting with 'test' |
| `instr` | [Instrumentation](../android.app/Instrumentation.md)!:The instrumentation to inject into each test before running. |

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
