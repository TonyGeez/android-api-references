# UnitTestSuiteBuilder

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# UnitTestSuiteBuilder

Kotlin | [Java](https://developer.android.com/reference/android/test/suitebuilder/UnitTestSuiteBuilder "View this page in Java") 
| --- | --- |

```
open class UnitTestSuiteBuilder : TestSuiteBuilder
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.test.suitebuilder.TestSuiteBuilder](https://developer.android.com/reference/kotlin/android/test/suitebuilder/TestSuiteBuilder) ||
| | ↳ | [android.test.suitebuilder.UnitTestSuiteBuilder](https://developer.android.com/reference/kotlin/android/test/suitebuilder/UnitTestSuiteBuilder#) |

| **This class was deprecated in API level 31.**
|
| android.test.runner is obsolete

A suite builder that finds unit tests.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [UnitTestSuiteBuilder](https://developer.android.com/reference/kotlin/android/test/suitebuilder/UnitTestSuiteBuilder#UnitTestSuiteBuilder(java.lang.Class))`(`clazz:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!>!`)` <br /> |
| [UnitTestSuiteBuilder](https://developer.android.com/reference/kotlin/android/test/suitebuilder/UnitTestSuiteBuilder#UnitTestSuiteBuilder(kotlin.String,%20java.lang.ClassLoader))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `classLoader:` ` [ClassLoader](https://developer.android.com/reference/kotlin/java/lang/ClassLoader.html#)!`)` <br /> |

| Inherited functions ||
|---|---|
| From class [TestSuiteBuilder](https://developer.android.com/reference/kotlin/android/test/suitebuilder/TestSuiteBuilder) |----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | TestSuite! | [build](https://developer.android.com/reference/kotlin/android/test/suitebuilder/TestSuiteBuilder#build())`()` Call this method once you've configured your builder as desired. <br /> | | [TestSuiteBuilder](https://developer.android.com/reference/kotlin/android/test/suitebuilder/TestSuiteBuilder)! | [excludePackages](https://developer.android.com/reference/kotlin/android/test/suitebuilder/TestSuiteBuilder#excludePackages(kotlin.String))`(`vararg` `packageNames:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Exclude all tests in the given packages and all sub-packages, unless otherwise specified. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getSuiteName](https://developer.android.com/reference/kotlin/android/test/suitebuilder/TestSuiteBuilder#getSuiteName())`()` Subclasses use this method to determine the name of the suite. <br /> | | [TestSuiteBuilder](https://developer.android.com/reference/kotlin/android/test/suitebuilder/TestSuiteBuilder)! | [includeAllPackagesUnderHere](https://developer.android.com/reference/kotlin/android/test/suitebuilder/TestSuiteBuilder#includeAllPackagesUnderHere())`()` Include all junit tests that satisfy the requirements in the calling class' package and all sub-packages. <br /> | | [TestSuiteBuilder](https://developer.android.com/reference/kotlin/android/test/suitebuilder/TestSuiteBuilder)! | [includePackages](https://developer.android.com/reference/kotlin/android/test/suitebuilder/TestSuiteBuilder#includePackages(kotlin.String))`(`vararg` `packageNames:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Include all tests that satisfy the requirements in the given packages and all sub-packages, unless otherwise specified. <br /> | | [TestSuiteBuilder](https://developer.android.com/reference/kotlin/android/test/suitebuilder/TestSuiteBuilder)! | [named](https://developer.android.com/reference/kotlin/android/test/suitebuilder/TestSuiteBuilder#named(kotlin.String))`(`newSuiteName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Override the default name for the suite being built. This should generally be called if you call `addRequirements(com.android.internal.util.Predicate[])` to make it clear which tests will be included. The name you specify is automatically prefixed with the package containing the tests to be run. If more than one package is specified, the first is used. <br /> | ||

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
