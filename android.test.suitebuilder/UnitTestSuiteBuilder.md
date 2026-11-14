# UnitTestSuiteBuilder

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UnitTestSuiteBuilder

Kotlin | [Java](UnitTestSuiteBuilder.md) 
| --- | --- |

```
open class UnitTestSuiteBuilder : TestSuiteBuilder
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.test.suitebuilder.TestSuiteBuilder](TestSuiteBuilder.md) ||
| | ↳ | [android.test.suitebuilder.UnitTestSuiteBuilder](UnitTestSuiteBuilder.md) |

| **This class was deprecated in API level 31.**
|
| android.test.runner is obsolete

A suite builder that finds unit tests.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [UnitTestSuiteBuilder](UnitTestSuiteBuilder.md))`(`clazz:` ` [Class](../java.lang/Class.md)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>!`)` <br /> |
| [UnitTestSuiteBuilder](UnitTestSuiteBuilder.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `classLoader:` ` [ClassLoader](../java.lang/ClassLoader.md)!`)` <br /> |

| Inherited functions ||
|---|---|
| From class [TestSuiteBuilder](TestSuiteBuilder.md) |----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | TestSuite! | [build](TestSuiteBuilder.md))`()` Call this method once you've configured your builder as desired. <br /> | | [TestSuiteBuilder](TestSuiteBuilder.md)! | [excludePackages](TestSuiteBuilder.md))`(`vararg` `packageNames:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Exclude all tests in the given packages and all sub-packages, unless otherwise specified. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSuiteName](TestSuiteBuilder.md))`()` Subclasses use this method to determine the name of the suite. <br /> | | [TestSuiteBuilder](TestSuiteBuilder.md)! | [includeAllPackagesUnderHere](TestSuiteBuilder.md))`()` Include all junit tests that satisfy the requirements in the calling class' package and all sub-packages. <br /> | | [TestSuiteBuilder](TestSuiteBuilder.md)! | [includePackages](TestSuiteBuilder.md))`(`vararg` `packageNames:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Include all tests that satisfy the requirements in the given packages and all sub-packages, unless otherwise specified. <br /> | | [TestSuiteBuilder](TestSuiteBuilder.md)! | [named](TestSuiteBuilder.md))`(`newSuiteName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Override the default name for the suite being built. This should generally be called if you call `addRequirements(com.android.internal.util.Predicate[])` to make it clear which tests will be included. The name you specify is automatically prefixed with the package containing the tests to be run. If more than one package is specified, the first is used. <br /> | ||

## Public constructors

### UnitTestSuiteBuilder

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
UnitTestSuiteBuilder(clazz: Class<Any!>!)
```  

### UnitTestSuiteBuilder

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
UnitTestSuiteBuilder(
    name: String!, 
    classLoader: ClassLoader!)
```
